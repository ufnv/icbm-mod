# 01 — Unit types (`Units/Units.txt`)

[Index](index.md) · [Basics](00-Basics.md) · Catalog: [A1](A1-Catalog-Units.md)

A `[UNIT]` entry defines a **unit type**: anything that exists on the map and belongs to a faction —
buildings, armies, ships, submarines, aircraft, satellites. (Missiles in flight also behave as units on the map,
but they are defined in `Missile_defs.txt`; cities are handled by the special `VirtualCity` entry.)

```
[UNIT] "Fighter"
  Tech "U_Fighter"                       // required: availability + display name
  Type Airborne                          // required
  Movie "Units/Images/Airborne/Topdown/Fighter_1.midx"   // required
  Power 0.65
  Speed 700
  Range 2400                             // flight range: needs a Crash explosion
  Size 0.05
  TurnSpeed 9
  MaxElevation 20
  ProductionCost 1.0                     // required, > 0
  Crash "std_bomb"
  Slave
  AutoReturn Yes
  Radar "STD Vision Air"
  Radar "Air Vision"
  Config "Air-To-Air" Default
    Weapon "AAM" 2 Launch 1 Time 120 AutoEngage
    Weapon "Plane Gun" 20000 Launch 1 Time 6 AutoEngage
  ImprovedBy "Generation_2_Aircraft"
  {
    Set Speed 800
    Set Range 2800
  }
```

Properties can appear in any order. Everything not written takes the default shown below.

---

## 1. Identity and availability

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `Tech` | `Tech "tech_id"` | — **required** | The unit can be built only when this technology is known; its name is the unit's display name. Give every unit its own zero-cost tech whose parent is the real research tech. |
| `DisablingTech` | `DisablingTech "tech_id"` / `NULL` | none | When the owner knows this tech the unit type is no longer available (used for obsolescence). |
| `Type` | `Type Ground\|Naval\|Subwater\|Airborne\|Satellite` | — **required** | Movement domain and targeting class. Also accepted but meant for internal types: `Missile`, `HighMissile`, `SubwaterMissile`, `City`, `AbstractPosition`. Setting `Type` also sets defaults: Airborne → `AutoReturn Yes`; Naval/Subwater → `MaxTiltDivider ×5`; Ground → can access unit and weapon stockpiles; Ground/Naval/Subwater → `TargetInPlanner Yes`. |
| `Class` | `Class "UC_…"` / `NULL` | auto by `Type` | Unit class (an `[UNIT_CLASS]` from `tech.txt`), used in the production and diplomacy UI. If absent, the class whose `AutoAssignTo` matches the unit's `Type` is used. |
| `ChangeTypeOnTech` | `ChangeTypeOnTech "tech" to "Unit_ID"` / `NULL` | none | Existing units of this type automatically turn into `Unit_ID` when the owner learns `tech`. Ignored if the target is the same type, or if `tech` equals the unit's own `Tech`. |
| `AchievementProperty` | `AchievementProperty "ACH_ID" [check "tech"]` | none | Marks the type for a Steam achievement check (optionally only when `tech` is known). |

## 2. Core combat statistics

All of these can be changed by tech modifiers (see [06](06-Tech-Modifiers.md#4-property-names)).

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `Power` | `Power <float>` | 1 | Hit points. Explosion damage is subtracted; the unit dies at ≤ 0. Also scales repair speed (see `AutoRepair`). |
| `Size` | `Size <km>` | 1 | Physical radius used by hit calculation: a blast reaches the unit if *distance − Size* ≤ blast radius, so bigger units are easier to hit. It also sets the area that bombers/precision weapons are evaluated against. |
| `Speed` | `Speed <float>` | 0 | Movement speed. 0 = immobile. **Do not change it with dynamic modifiers** (`InRange`, `Explosion`, `Terrain`, `AffectedBy`) — use simple `ImprovedBy` only. |
| `VirtualSpeed` | `VirtualSpeed <float>` | 0 | For "teleporting" relocations: the speed used to compute relocation time. |
| `TurnSpeed` | `TurnSpeed <float>` | 1 | How fast the unit turns. |
| `Range` | `Range <km>` | 0 | **Flight range** (fuel) for aircraft. A unit with `Range > 0` must also have a `Crash` explosion. The AI and the path UI keep a safety margin; a unit that exceeds its range crashes. |
| `MinElevation`, `MaxElevation` (alias `Elevation`) | `<km>` [`Real`] | 0 | Altitude band the unit flies in (an aircraft cruises at `MaxElevation`). Radars with a lower `MaxHeight` cannot see it. ★ With `Real` in real km (see below). Shipped: helicopters 1, fighters, attack, EW aircraft and transports 10, bombers, AWACS and SOF aircraft 12, interceptors and high-speed bombers 20, spy planes 25 (`Real`). |
| `ProductionCost` | `ProductionCost <float>` | — **required, > 0** | Production points to build one. Also the base of repair speed. |
| `MaxNumberOnMap` | `MaxNumberOnMap <int>` | 1 000 000 | Maximum alive units of this type per faction. |
| `MaxNumberToOrder` | `MaxNumberToOrder <int>` | unlimited | Maximum that can be in the production queue at once. |
| `CanBeBuilt` | `CanBeBuilt Yes\|No` | Yes | No = never appears in production (units created by scripts, `Produces`, or as states). Tech-modifiable as a number (0 = no). |
| `AutoRepair` (alias `AutoHealing`) | `AutoRepair Yes\|No\|<float>` | 1 (Yes) | Repair rate multiplier for non-flying units. Repair happens only where repair is allowed (own territory, or within a friendly `RepairRange`) and heals `AutoRepair × MaxPower × RepairValue ÷ (ProductionCost × 0.01)` per step — expensive units heal proportionally slower. 0 = never repairs. |
| `DecayTimer` | `DecayTimer <ticks>` | 0 (off) | The unit loses `Power ÷ DecayTimer` every tick, dying after that many ticks (temporary units). |
| `Crash` | `Crash "explosion_id"` | none | Explosion produced when the unit is destroyed or runs out of fuel. Required when `Range > 0`. It hits ground, naval and city targets around it. |
| `SelfDestructTime` | `SelfDestructTime <s>` | 0 | Time the self-destruct order takes. |
| `Disassemble` | `Disassemble <float>` | −1 | Not used by the game. |

★ **Real heights.** The game flies its aircraft higher than real ones for the sake of the view, most of all the lowest:
up to 1000 km a game height is 1000 × (real / 1000)^0.8 (real 1 km is 4 in the game, 10 km is 25, 100 km is 158),
above 1000 km the same. A height followed by `Real` is in real km and converted on loading, e.g.
`MaxElevation 10 Real` (25 game km); without it, in the game's km as before (mods keep working). The info panels
and the Explodopedia show real km. `Real` works for `MaxElevation`, `MinElevation`, `MinExplosionHeight`, a radar's
`MaxHeight`, and the `Set`, `Set Max` and `Set Min` modifiers of these (`ImprovedBy "X" Set MaxElevation 25 Real`);
not with `Add` or `Multiply`. Shipped in real km: the aircraft and helicopters and the anti-aircraft weapons; the
satellites, the shuttle, the ballistic missiles' `Elevation`, the anti-missile weapons and the radars stay in game km.


## 3. Weapons

### 3.1 Weapon configs

A unit has one or more **weapon configs**; the player (or AI) switches between them. Each config is a list
of weapons.

```
Config "ASM" Default                 // [Default] [OnlyFull] [Special]
  Weapon "ASM" 2 Launch 2 Time 90 AutoEngage
  Weapon "AAM" 2 Launch 1 Time 60 AutoEngage Principal
```

A `Weapon` line written without any `Config` before it creates a single config named `default`. A unit
with only one config always treats it as its default.

| Config flag | Meaning |
|---|---|
| `Default` | The config selected when the unit is built. |
| `OnlyFull` | The config can be selected only when the unit is fully loaded. |
| `Special` | Special config (not offered as a normal choice by the AI). |

### 3.2 `Weapon` line

`Weapon "missile_id" <stock> [Launch <n>] [Time <t>] [AutoEngage [WhenAttacked [ByNuke] [AIOnly]]] [Principal] [DefaultOff] [LaunchPoint <n>]`

| Part | Default | Meaning |
|---|---|---|
| `<stock>` | — | Number of missiles carried in this config (use a large number such as 20000 for guns/lasers). |
| `Launch <n>` | 1 | Missiles fired per salvo. |
| `Time <t>` | 1 | Reload time between salvos, in reload units (`Time 30` = one "second", see [00 §6](00-Basics.md#6-units-of-measure)). Scaled by the global `GlobalMissileLaunchDelayModifier`. |
| `AutoEngage` | off | The weapon may fire automatically. `WhenAttacked` = only after the unit was attacked; `ByNuke` = only after a nuclear attack; `AIOnly` = the restriction applies only to AI factions. Scripts can override per unit with `Weapon_Use`. |
| `Principal` | off | The weapon that represents the config in the UI/AI evaluation. |
| `DefaultOff` | off | The weapon starts switched off (the player can switch it on; relevant for `Switchable` missiles). |
| `LaunchPoint <n>` | 0 | Which model launch point (3D) the missile leaves from. |

### 3.3 Upgrading configs with technologies

* **Replace a config's contents when a tech is known** — put `ImprovedBy "tech"` directly after the
  config's weapons, followed by the new weapon list:

  ```
  Config "Air to Air" Default
    Weapon "AAM" 2 Launch 1 Time 120 AutoEngage
    ImprovedBy "Generation_3_Aircraft"
      Weapon "LAAM" 4 Launch 2 Time 120 AutoEngage
  ```
* **A config that exists only after a tech** — an empty `Config` followed by `ImprovedBy "tech"` and weapons
  (used for the bombers' AL-ICBM configs). Alternatively, anywhere in the entry:
  `ImprovedBy "tech" Config "name"` followed by `Weapon` lines.
* **Change launch count / reload of one weapon** — `ImprovedBy "tech" Modify Weapon "missile" <op> Launch|Time <value>`
  (see [06](06-Tech-Modifiers.md#modify-weapon)). Example from the data:
  `ImprovedBy "Spec_Ops_Boost_1" Modify Weapon "Small Arms" Set Time 4`.

Config-replacing `ImprovedBy` must be a simple `ImprovedBy "tech"` (no `Unit`/`InRange`, no `Modify`).

### 3.4 Other weapon-related properties

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `CanStoreMissiles` | `CanStoreMissiles "missile" <n> [DefaultOff]` | none | Extra magazine carried by the unit (e.g. bombers' nuclear stock, carriers' aircraft munitions). Hosted units rearm from it. |
| `AttackDelay` | `AttackDelay <s>` | 0 | Readiness build-up: the unit must "prepare to attack" for this long before its weapons fire; readiness decays while moving (unless it can attack on the move) and cancels after `AutoCoolDownDelay` of inactivity. |
| `AttackOnMove` | `AttackOnMove Yes\|No\|<float>` | Yes (1) | Whether the unit can fire while moving (> 0 = yes). Tech-modifiable, so a tech can grant it. Units that cannot attack on the move also turn to face the target first. |
| `ModelLaunchTime` | `ModelLaunchTime <s>` | 1 | Length of the 3D launch animation. |
| `AutoCoolDownDelay` (alias `AutoCancelReadinessDelay`) | `<s>` | 10 | Idle time after which attack readiness is lost. |
| `WeaponsActivationDelay` (alias `WeaponActivationDelay`) | `<s>` | 0 | Fixed delay before weapons work after deployment/launch. |
| `WeaponsActivationDelayMult` (alias `WeaponActivationDelayMult`) | `<float>` | 0.25 | Additional delay = this × each weapon's reload `Time`. |
| `SensorsActivationDelay` (alias `SensorActivationDelay`) | `<s>` | 0 | Delay before radars work after deployment. |
| `ShowDisabledOnDeploymentMarker` | `Yes\|No` | Yes | Shows the "not yet active" marker during these delays. |
| `NoAutoAttack` | `NoAutoAttack [Yes\|No]` | auto-attack on | The unit never picks targets on its own. |
| `NoAutoAttackSub` | `NoAutoAttackSub [Yes\|No]` | on | Same, against submarines only. |
| `MaxAutoEngageRange` | `<km>` | 1000 | For hosted units (aircraft): the host auto-launches them only against targets within this distance. |
| `CheckTargeting` | `CheckTargeting BY "missile" [OR "missile"…] Message Lock <strID> NoLock <strID>` | none | Shows lock/no-lock messages (string IDs from `UI.lng`) when this unit is or is not covered by the listed enemy weapons (e.g. jammers). Also registers those weapons for `InRange` checks. |
| `CheckCoverage` | `CheckCoverage "missile" BY "radar" [OR "radar"…] Message <strID>` | none | Warns the player (string ID) when firing `missile` without coverage from one of the listed radars. |
| `InfluencesAllies` | `Yes\|No` | Yes | Whether the unit's aura-type weapons (buffs/debuffs checked through `InRange`) also affect allies. |

## 4. Sensors

| Property | Syntax | Meaning |
|---|---|---|
| `Radar` | `Radar "radar_id" [DefaultOff]` | Adds a sensor. `DefaultOff` = starts switched off. List property. |
| Tech-dependent radar set | `ImprovedBy "tech"` followed by `Radar "…"` lines | When `tech` is known, **the whole radar list is replaced** by the listed radars. Sets defined later are checked first; the first set whose tech is known wins. |

> Plain `Radar` lines always belong to the base list, wherever they are written (also in later `MODIFY`
> entries); tech-dependent sets are kept separately.

Radar ranges and detection classes are defined in [04 — Radars](04-Radars.md).

## 5. Carrying other units

### 5.1 Airways (aircraft launch/landing channels)

```
Airway Launch 2 Time 60                      // airway 0
Airway Launch 1 Time 90                      // airway 1
CanHostAircraft "Fighter" 24 Patrol 4 AIAutoPatrol
CanHostAircraft airway 1 "AWACS" 2
```

| Property | Syntax | Meaning |
|---|---|---|
| `Airway` | `Airway [Launch <n>] [Time <t>]` | Declares a launch channel: `n` aircraft per launch (default 1), `t` reload units between launches (default 1). Scaled by `GlobalAircraftLaunchDelayModifier`. |
| `CanHostAircraft` (alias `CanHostAircrafts`) | `CanHostAircraft [airway <i>] "Unit_ID" <count> [Patrol <n> [AIAutoPatrol]]` | Unit type hosted on airway `i` (default 0) with capacity `count`. `Patrol n` = how many can be sent on patrol at once; `AIAutoPatrol` lets the AI patrol automatically. The airway must have been declared. |
| `MaxAutoEngageRange` | see §3.4 | |
| `OnDeployLaunchHostedDelay` | `<s>` | Delay before hosted units can launch after the host deploys. |

A unit may have at most **3 channels in total** (airways plus the hangar channel created by `CanCarryUnit`/`HangarExit`).

### 5.2 Hangar (transport of ground units)

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `CanCarryUnit` | `CanCarryUnit "Unit_ID" [build <n>]` | — | The unit can transport this type in its hangar. `build n` = it comes with `n` of them. Creates the hangar channel automatically. |
| `HangarExit` | `HangarExit [Launch <n>] [Time <t>]` | 1 / 1 | Unload rate of the hangar. |
| `HangarMaxLoad` | `<int>` | sum of `build` loads | Hangar capacity in space units. Raised automatically to fit the initial load. |
| `HangarSpaceRequired` | `<int>` | 1 | Space this unit type takes in someone else's hangar. |
| `TimeToBoard`, `TimeToUnboard` | `<s>` | 0 | Boarding/unboarding time. |
| `ReportAsHosted` | `Yes\|No` | No | While inside a host, the unit is still reported (e.g. listed with the host). |

### 5.3 Being hosted

| Property | Default | Meaning |
|---|---|---|
| `Slave` | No | The unit belongs to a host (aircraft): it must stay within safe return distance of the host, is not a war-planner target and gets different AI handling. |
| `AutoReturn` | Yes for Airborne, else No | Returns to its host automatically after the mission. |
| `CanPatrolPoint` | No | Can be ordered to patrol a point. |
| `CanHangInTheAir` | No | Can loiter (helicopters, drones) instead of needing to keep flying. |
| `ProducedByAnotherUnit` | No | Built by another unit, not by the faction's production (excluded from planner targets). |

## 6. Readiness states (submerge/surface, deploy/undeploy)

Two unit types can form a pair of **states** — for example `Submarine` (low) and `Submarine_Surfaced`
(high). The unit switches between the types, keeping its identity.

```
[UNIT] "Submarine"                    [UNIT] "Submarine_Surfaced" COPY "Submarine"
  HighState "Submarine_Surfaced"        HighState NULL
  TimeToHighState 3.0                   LowState "Submarine"
                                        TimeToLowState 3.0
                                        SpecialState Yes
```

| Property | Syntax | Meaning |
|---|---|---|
| `HighState`, `LowState` | `"Unit_ID"` / `NULL` | The type to switch to. |
| `TimeToHighState`, `TimeToLowState` | `<s>` | Switching time. |
| `SpecialState` | `Yes\|No` | This type is only a state of another unit: it cannot be built and is not a planner target. |
| `RetreatShift`, `AttackShift`, `DefenceShift`, `FastMoveShift`, `UnderIceShift` | `High\|Low\|None` | Automatic state change when the unit retreats, attacks, defends, moves fast or goes under ice. |
| `AutoOnMoveShift` | `High\|Low\|None` | State change when ordered to move. |
| `AutoOnRest` | `High\|Low\|None` | State change after resting for `AutoOnRestDelay` seconds. |
| `HighStateStringIDX`, `LowStateStringIDX`, `StateStringIDX` | `<strID>` | UI strings for the state buttons/label (default 2447). |
| `ToHighStateProcessStringIDX`, `ToLowStateProcessStringIDX` | `<strID>` | UI string while switching. |
| `StateIcon`, `ToHighStateIcon`, `ToLowStateIcon` | `"image"` / `NULL` | Icons for the state UI. |

## 7. Occupation (armies)

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `OccupationRadius` | `<km>` | none | Makes the unit an **occupier** (it can capture cities/units). Not allowed for flying units. Also disables crossing borders in peace time. |
| `TimeToOccupyMult` | `<float>` | 0 | Makes the unit **occupiable** (> 0) and multiplies the time needed to capture it. For cities the time also depends on population, see globals below. |
| `ExecuteOrdersWhenBesieged` | `Yes\|No` | No | Whether an occupiable unit under siege can still act (self-destruct, attack…). |
| `CanCrossBorder` | `Yes\|No` | Yes | No = never leaves own territory. |
| `CanCrossBorderDuringPeaceTime` | `Yes\|No` | Yes | May enter foreign territory before war. |
| `AlwaysVisibleOnEnemyTerritory` | `Yes\|No` | No | Revealed to the territory owner while inside it. |

## 8. Support and logistics

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `ResupplyRange` | `<km>` | 0 | Friendly units within this distance can rearm (and repair) as if at home. Implies `CanAccessGlobalStorage`. |
| `RepairRange` | `<km>` | 0 | Friendly units within this distance repair. |
| `CanAccessGlobalStorage` | `[Yes\|No]` | Ground: Yes | Shortcut for both stockpile flags below. |
| `CanAccessUnitStockpile` | `Yes\|No` | Ground: Yes | Can draw units from the faction's reserve when outside own territory. |
| `CanAccessWeaponStockpile` | `Yes\|No` | Ground: Yes | Can draw weapons (e.g. nukes) from the faction stockpile when outside own territory. |
| `Produces` | `Produces "Unit_ID or missile_id"` / `NULL` | none | The unit can produce these units or missiles itself. List property. |
| `ProductionPlacementRadius` (alias `UnitPlacementRadius`) | `<float>` | 0 | Where produced units appear around the producer. |

## 9. Politics, visibility and war triggers

| Property | Default | Meaning |
|---|---|---|
| `HiddenFromAllies` | No | Allies do not see this unit. |
| `HideOwnership` | No | Enemies (other than permanent allies) do not see who owns it. |
| `AttackIfDestroyed` | No | Losing this unit triggers **limited escalation** (the owner may then nuke cities); automatic attacks on such units are disabled. |
| `DoesNotTriggerWarWhenAttacked` | No | Attacking this unit does not start a war. |
| `DoesNotTriggerWarOnAttack` | No | Attacks *by* this unit do not start a war. |
| `DestroyOnFactionSurrender` | Yes | Removed when its owner surrenders. |
| `CanSetDEFCON` | No | Owning this unit allows changing DEFCON. |

## 10. AI and war-planner hints

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `AttackerInPlanner` | `[Yes\|No]` | No | The war planner may use this unit as an attacker. |
| `TargetInPlanner` | `Yes\|No` | Ground/Naval/Subwater: Yes | The war planner may target it. Cleared by `Slave`, `ProducedByAnotherUnit`, `SpecialState`. |
| `MoveToTarget` | `MoveToTarget ANY` / `MoveToTarget [AVOID] "Unit_ID"` | none | For raiding units (spec-ops): which target types the AI moves towards (`ANY`) or must avoid (`AVOID`). List property. |
| `MoveToTargetInWarPlan` | `[Yes\|No]` | No | Also move towards targets while executing a war plan. |
| `NoAutoDeploy` | `[Yes\|No]` | No | Not deployed automatically at game start / auto-deploy. |
| `DoNotShowInEncyclopedia` | `[Yes\|No]` | No | Never mentioned in the Explodopedia ([14](14-Explodopedia.md)): no page, and no icon, link or row naming it on other pages. Alias `DoNotShowInExplodopedia`. |
| `BlockedZoneTypeID` | `"zone_type"` / `NULL` | none | AI "blocked zone" category this unit creates (areas the AI avoids). A technology can reset zones with `ResetBlockedZone`. |
| `Helper`, `AIVarietyHint` | `"text"` | — | Accepted and ignored. |

## 11. Presentation

| Property | Syntax | Meaning |
|---|---|---|
| `Movie` | `"file.midx"` / `NULL` | **Required.** Map sprite/animation. |
| `AbstractMovie` | `"file"` / `NULL` | Sprite for the abstract (flat) map mode. |
| `Model` | `"file"` / `NULL` | 3D model for terrain view. |
| `Icon`, `RoundIcon` | `"file.png"` | UI icons; default to frame `IconIDX` of the movie; `RoundIcon` defaults to `Icon`. |
| `IconIDX` | `<int>` | Frame of the movie used as icon. |
| `LaunchMePathIcon` | `element "ui_element"` / `NULL` | Path icon used when this unit is launched (default `"path/launch STD"`). |
| `DrawSize`, `ModelDrawSize`, `AbstractDrawSize` | `<float>` | On-screen size (default 32): `DrawSize` the map picture, `ModelDrawSize` the 3D model (default `DrawSize`), `AbstractDrawSize` the zoomed-out icon (default `DrawSize`). A picture or model drawn bigger or smaller in its frame (an upgrade's, a faction's own) gets a `Scale` in its `.midx` ([12](12-Config-Files.md#pictures-and-models)). For a seamless switch the unit itself should look as big in its picture as the model when the unit switches to it. |
| ★ `ModelSwitchSize` | `<float>` | The unit is drawn as its 3D model once the model is this big, in % of the screen's width (default 2); its map picture before. A unit with a big picture (an airport, a base) switches when its model has grown as big as the picture: e.g. `ModelSwitchSize 5.2` with `DrawSize 35`, `ModelDrawSize 90`. |
| ★ `LaunchSmokeSize` | `<float>` | Its missiles' launch smoke this many times as big (default 1; the smoke is measured in the launcher's model lengths). None of the shipped units sets it (`Launch_Smoke` itself is 0.75 launcher lengths). |
| `HideAbstract` | `Yes\|No` | Hide in abstract mode. |
| `FollowRadius` | `<float>` | Radius of the follow/selection circle (default DrawSize ÷ 1.35). |
| `DrawOrder` | `<int>` | Drawing order among units of the same class (smaller first). |
| `FixedRotationAngle` | `Yes\|No` | Sprite does not rotate with heading. |
| `MaxTiltDivider` | `<float ≥ 1>` | Banking when turning (larger = less tilt; default 1.5, ships ×5). |
| `ForceMipMap` | `Yes\|No` | Force mip-mapping for the sprite. |
| `Sound` | `Sound <id> [Volume <f>]` | Selection/voice sound. |
| `LaunchMeSound` | `LaunchMeSound <id> [Priority <n>] [SoundSize <f>] [Speed <f>] [MuteLength <f>]` | Sound when launched from a host. |
| `LaunchMeSoundUI` | `<id>` | UI sound when launched. |
| `DestructionMessage` | `Default\|None\|GroundMobile\|Ground\|Naval\|Subwater\|Airborne\|Missile\|Satellite\|City` (unquoted, case-sensitive) | Which "unit destroyed" message category to use. |

## 12. Modifier tags

`Modifier "tech_id" [value <float>]` attaches a **tag** to the unit type. Tags do nothing by themselves;
tech modifiers elsewhere test for them with `ImprovedBy Unit "tag"` / `AffectedBy Unit "tag"` and can use
the tag's value with the `value` keyword. The tag must be a technology ID in `tech.txt` (usually a
zero-cost tech that is always known, or the tech that activates the effect).

```
[UNIT] "Stealth_Bomber"   Modifier "Bomber_Stealth_Bonus_Modifier_1" value 0.5         // illustrative
[RADAR] "STD Long Wave"   AffectedBy Unit "Bomber_Stealth_Bonus_Modifier_1" Range value    // ×0.5 against that bomber
```

A tag with value 0 is still present. Tags can be added or removed dynamically with the `Modifier`
property of a tech modifier (`Set Modifier`, `Delete Modifier`), see [06](06-Tech-Modifiers.md#8-modifier-tags).

## 13. Tech modifiers on units

`ImprovedBy …` and `AffectedBy …` lines (and `{ … }` blocks) change unit properties when technologies,
tags, auras, explosions or terrain apply. Unit property names usable in modifiers: `Speed`,
`VirtualSpeed`, `TurnSpeed`, `Range`, `Power`, `Size`, `ProductionCost`, `CanBeBuilt`, `MaxNumberOnMap`,
`MaxElevation`, `MinElevation`, `DisassembleTime`, `ResupplyRange`, `RepairRange`, `AttackDelay`,
`AttackOnMove`, `ModelLaunchTime`, `Movie` (appearance), `Modifier` (tags), `Config`/`Radar`
(replacement lists), `Modify Weapon`. Full grammar in [06](06-Tech-Modifiers.md).

```
ImprovedBy "Generation_4_Aircraft"
{
  Movie "Units/Images/Airborne/Topdown/Fighter_4.midx" Icon "Units/Images/Icons/Airborne/Fighter_4.png"
  Movie Model "Units/Images/AIRBORNE/4th Gen Fighter.midx"
  Set Size 0.03
  Set Speed 1000
  Set Range 3750
}
```

## 14. Global unit settings (top level of `Units.txt`, outside any entry)

| Setting | Default | Meaning |
|---|---|---|
| `GlobalSpeedModifier <f>` | 1 | Multiplies every unit's speed. |
| `GlobalAircraftLaunchDelayModifier <f>` | 1 | Multiplies all airway/hangar launch delays. |
| `GlobalMissileLaunchDelayModifier <f>` | 1 | Multiplies all weapon reload times. |
| `GlobalCitySizeModifier <f>` | 1 | Multiplies city radius for blast calculations (bigger = more exposed). |
| `MinTimeToOccupyCity <s>` | 0 | Lower bound of city capture time. |
| `MaxTimeToOccupyCity <s>` | 900 (15 min) | Upper bound of city capture time. |
| `MinTimeToOccupyUnit <s>` | 0 | Lower bound of unit capture time. |
| `CityOccupationMultPerPercent <s>` | 60 | Capture time per 1 % of the faction's initial population living in the city (× occupier's multiplier). |
| `UseAbsolutePopulationForOccupationTime Yes\|No` | No | Use absolute population (per million) instead of percent of the faction. |

Shipped values: `MinTimeToOccupyCity 150`, `MinTimeToOccupyUnit 30`.

## 15. `VirtualCity` — the city pseudo-unit

Cities are not `[UNIT]`s, but `[UNIT] "VirtualCity" MODIFY` (the only allowed form) attaches properties to
all cities. Useful properties:

* `Modifier` tags (e.g. `"Resist_Nuke_ABM"`, `"EMP_Defence_Mod_3"`) that weapons test with `AffectedBy Unit`.
* `ImprovedBy` / `AffectedBy` on the city economy: **`Production`, `Science`, `Espionage`** (multipliers of
  the city's output), plus `Power`, `Size`, `MaxNumberOnMap`, `ResupplyRange`, `RepairRange`.

```
[UNIT] "VirtualCity" MODIFY
  ImprovedBy "Production_Booster_1" Production 1.10
  ImprovedBy InRange "Research_Buff" Science 1.10         // aura from the Research Center
  AffectedBy Explosion "EMP_Blast" Complex Production
    case "EMP_Defence_Mk4" Multiply 0.75
    default Multiply 0.25
  ImprovedBy "DEFCON_2" Production 0.75                   // DEFCON penalties are modelled this way
```

The city's technology is `U_City`. Cities are hit by any missile whose type `Affects City` (see [02](02-Missiles.md#2-targeting-classes)).

## 16. Checklist for a new unit

1. Add `[TECHNOLOGY] "U_My_Unit"` with `Name`/`Description` in `tech.txt`, a `Parent` or a `LeadsTo` from
   the research tech, and the strings in `lang/*/tech_t.lng`.
2. Add `[UNIT] "My_Unit"` with `Tech`, `Type`, `Movie`, `ProductionCost`, `Power`, `Size`, and `Speed`
   if mobile.
3. Give it at least one sensor (`Radar "STD Vision"` or similar) — units see nothing without one.
4. Add weapons (configs), and `Crash` + `Range` if it flies.
5. Add hosting (`CanHostAircraft` on a carrier/base) if it is an aircraft.
6. Start the game and make sure no "unknown keyword" error appears ([see 00](00-Basics.md#-an-unknown-keyword-stops-the-file)).
