# 07 — Tuning guide: recipes, testing, and event scripts

[Index](index.md) · [Basics](00-Basics.md)

This chapter collects the common balance changes and shows the smallest correct way to make each one.
All examples are written as **mod files** that load the previous version and modify it
([00 §3](00-Basics.md#3-mods-and-file-overriding)).

---

## 1. Workflow

1. Create `MODS/<YourMod>/info.txt` with `ICBM MOD "Your mod"`.
2. For each game file you change, create the same path in your mod and start it with
   `USE PREVIOUS "<same path>"`.
3. Change existing entries with `MODIFY`; create new ones with a new ID (or `COPY` for units).
4. Start a skirmish: an "unknown keyword" error means a typo stopped the file ([see 00](00-Basics.md#-an-unknown-keyword-stops-the-file)). Then check your changes in game.
5. Test with the [Cheats build](10-Cheats-Build.md): Shift + T researches the queued technologies at
   once, Ctrl + click in the production panel builds a unit instantly, Shift + 0 … 9 switches faction.
6. Multiplayer: every player needs the identical mod set; the game compares CRCs of the loaded data.

## 2. Recipes

### Make a unit tougher or cheaper

```
USE PREVIOUS "Units/Units.txt"

[UNIT] "Destroyer" MODIFY
  Power 12                 // hit points
  ProductionCost 7
```

Remember that `AutoRepair` speed is inversely proportional to `ProductionCost`, so a cheaper unit also
repairs faster.

### Change a weapon's range only after research

```
USE PREVIOUS "Units/Missile_defs.txt"

[MISSILE] "SAM" MODIFY
  delete ImprovedBy "SAM_Mk2"            // drop the old upgrade…
  ImprovedBy "SAM_Mk2" Set Range 450     // …and give a new one
```

For a chain of upgrades use `Set` in increasing order; later known techs are applied later and win.

### Make nukes more or less deadly for cities

Edit the explosion, not the missile:

```
USE PREVIOUS "Units/explosion.txt"

[EXPLOSION] "nuke_100" MODIFY
  FullEffectRange 7        // was 10: full-effect area −51 %
  Range 45                 // was 60
```

Casualties scale with the covered area (radius²) and only slowly with `Damage` (see
[03 §3](03-Explosions.md#3-hitting-cities)). `MinCasualties` adds a flat number per city hit.

### Make a missile harder to intercept

```
[MISSILE] "ICBM (1M Light)" MODIFY
  CanBeIntercepted 0.25    // chance that an interceptor hit counts
  Power 2                  // needs two counted hits of a Damage-1 interceptor
```

`FakeHeads n "decoy"` and higher `Speed` also help. The opposite knobs on the defence side are the
interceptor's `Precision`, its explosion `Range`/`Damage`, `Launch` per salvo, and
`MinMissilesPerTarget`/`MaxMissilesPerTarget`.

### Make a unit stealthier against radar

```
USE PREVIOUS "Units/Units.txt"
[UNIT] "Bomber" MODIFY
  Modifier "Bomber_Stealth_Bonus_Modifier_1" value 0.6          // tag the unit type (tag = a tech ID)

USE PREVIOUS "Units/Radars.txt"                    // (in Units/Radars.txt of the mod)
[RADAR] "STD Long Wave" MODIFY
  AffectedBy Unit "Bomber_Stealth_Bonus_Modifier_1" Range value   // range × 0.6 against tagged units
```

The effect is active only while the unit's owner knows the tech `Bomber_Stealth_Bonus_Modifier_1`.

### A buff aura (e.g. faster reload near a command post)

```
[MISSILE] "Command_Aura"                     // Units/Missile_defs.txt (new, illustrative)
  Tech "M_Command_Aura"
  Type "No Attack"
  Icon "Units/Images/Missiles/Buff.png"
  Explosion "No_Explosion"
  Range 150                                 // aura radius
  Hidden Yes
  HideRange No
  Switchable ON
  CanBeLimited false

[UNIT] "Command_Post" MODIFY                 // Units/Units.txt (illustrative unit)
  Weapon "Command_Aura" 1                   // the aura works while the weapon is switched on

[UNIT] "Army_Division" MODIFY
  ImprovedBy InRange "Command_Aura" Modify Weapon "Land Forces" Time 0.8   // 20 % faster reload
```

### A lasting debuff (EMP-style)

```
[EXPLOSION] "My_EMP"                         // explosion.txt
  Damage 0
  Range 80
  FullEffectRange 80
  LastingEffect 3600 StringID 1908           // 120 "seconds"
  TriggerResponse No

[UNIT] "VirtualCity" MODIFY                  // Units.txt
  AffectedBy Explosion "My_EMP" Production 0.5
```

### Faction-specific unit

```
[TECHNOLOGY] "U_My_Unit"                     // tech.txt
  Name "U_MY_UNIT_NAME"
  Description "U_MY_UNIT_DESC"
  Parent "Your_Research_Tech"               // the research tech that unlocks it
  Parent "PREFIX_EA" HideLink                // only factions using the EA model set
```

### Move a unit in the tech tree

Change which research tech has its zero-cost unit tech as a child:

```
[TECHNOLOGY] "Old_Parent" MODIFY
  delete LeadsTo "U_My_Unit"
[TECHNOLOGY] "New_Parent" MODIFY
  LeadsTo "U_My_Unit"
```

### Global knobs

| Want | Where | Setting |
|---|---|---|
| All units faster/slower | `Units.txt` | `GlobalSpeedModifier 1.2` |
| All missiles faster/slower | `Missile_defs.txt` | `GlobalSpeedModifier 1.2` |
| All reloads slower | `Units.txt` | `GlobalMissileLaunchDelayModifier 1.5` |
| All aircraft launch slower | `Units.txt` | `GlobalAircraftLaunchDelayModifier 1.5` |
| Cities easier to hit | `Units.txt` | `GlobalCitySizeModifier 1.2` |
| City capture time | `Units.txt` | `CityOccupationMultPerPercent`, `Min/MaxTimeToOccupyCity` |
| Less pollution | `explosion.txt` | `PollutionMultiplier 0.25` |
| Research cost per level | `TechLevels.txt` | `NextLevelMultiplier 1.3` |

## 3. Event scripts and unit definitions

Mission event scripts (`EVENTS/*.txt`, see the *ICBM – Events script* reference) cannot change the numbers
in these files, but they interact with them through technologies, weapons and unit types. The robust
pattern is: **put the balance change in the data files behind a technology, and let the script grant the
technology.**

| Script feature | Connects to |
|---|---|
| `GRANT_TECH(FactionID, "tech")` (also a set of techs) | Grants the tech **and its unknown parents** without triggering `Researched` events. Anything behind `ImprovedBy "tech"` switches on. Works for `CanBeResearched No` techs; never for techs parented to `BLOCKER`. |
| `TECH_AVAILABLE`, `GET_FACTION_TECHS`, `TECH_NAME` | Tech IDs from `tech.txt`. |
| `ON Researched "tech" BY …`, `ON Tech_Available "tech" …` | Tech IDs. |
| `Build "Unit_ID"`, `CREATE_UNIT`, `CREATE_GROUP`, `ANY "Unit_ID"`, `SELECT … TYPE == "Unit_ID"` | `[UNIT]` IDs; `CLASS` compares with unit classes (`Ground`, `Naval`, …). |
| `Disable` / `Enable Missiles NUKE\|BIO\|CHEM\|EMP\|MASS DESTRUCTION\|GENEVA "cat"\|AI_CATEGORY "cat"\|"missile"` | Explosion `Type`s, `TriggerResponse` (= mass destruction), Geneva and AI categories, missile IDs. Only missiles with `CanBeLimited Yes` are affected by category bans. |
| `Unit X Weapon_Use "missile" Never\|Always\|WhenAttacked…` | Overrides a weapon's `AutoEngage` for one unit. |
| `Weapon_Switch "missile" ON\|OFF` | Turns `Switchable` weapons on/off. |
| `SET_WEAPON_CONFIG`, `GET_WEAPON_CONFIG`, `WEAPON_CONFIG_AVAILABLE` | Config names from the unit's `Config "…"` lines. |
| `WEAPON_RANGE`, `WEAPON_YIELD`, `WEAPON_GENEVA_CATEGORY`, `WEAPON_AI_CATEGORY`, `HAS_WEAPON`, `NUM_AVAILABLE` | Read the (modified) weapon values and categories. |
| `RANGE`, `SAFE_RANGE`, `SPEED`, `RADAR_RANGE`, `ATTACK_RANGE`, `HEALTH`, `HEALTH_PERCENT` | Read unit values after tech modifiers. |
| `ON Exploded "missile"\|NUKE… IN …`, `ON Damaged … BY "missile"`, `ON Launched "missile" …` | Missile IDs and explosion types. |

Example — a scenario reward that unlocks a hidden upgrade (the tech has `Points 100` and
`CanBeResearched No` in `tech.txt`; its effect is `ImprovedBy "Scenario_Railgun_Bonus" Range 1.25` on the
railgun):

```
BLOCK GrantRailgunBonus()
  GRANT_TECH(SelfID, "Scenario_Railgun_Bonus")
  Message "Railgun range increased" Position TopLeft
END

ON Mission "Secure the lab" SUCCESS GrantRailgunBonus()
END
```

(`Mission "…"` must match a mission name declared in the map's `ScenarioInfo`.)

## 4. Before you publish

* The game starts without "unknown keyword" errors.
* Every new object has a `Tech` with `Name`/`Description` strings in every language file you ship.
* New weapons are in some unit's config, new units are buildable (`CanBeBuilt`, class, tech reachable),
  new aircraft are hosted somewhere.
* `IF` markers wrap whole entries.
* You used `MODIFY` + `USE PREVIOUS` wherever possible, so your mod combines with others.
