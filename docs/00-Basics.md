# 00 — Basics: file format, mods, editing existing entries

[Index](index.md)

## 1. Files

| File | Contains | Entry headers |
|---|---|---|
| `tech.txt` | Technologies, tech-tree categories, tech levels, unit classes, DEFCON states | `[TECHNOLOGY]`, `[TYPE]`, `[LEVEL]`, `[UNIT_CLASS]`, `[DEFCON]` |
| `TechLevels.txt` | Tech-level progression (how much each tech moves you up a level) | line commands, see [05](05-Technologies.md#techlevelstxt) |
| `Tech_faction.txt` | Template for the built-in faction techs — **do not edit** | — |
| `Units/explosion.txt` | Explosions | `[EXPLOSION]` |
| `Units/Radars.txt` | Radar templates and sensors | `[TYPE]`, `[RADAR]` |
| `Units/Missiles.txt` | Only `USE "Units/Missile_types.txt"` and `USE "Units/Missile_defs.txt"` | — |
| `Units/Missile_types.txt` | Geneva & AI categories, missile templates | `[GENEVA_CATEGORY]`, `[AI_CATEGORY]`, `[TYPE]` |
| `Units/Missile_defs.txt` | Weapons | `[MISSILE]` |
| `Units/Units.txt` | Unit types, global unit settings, the `VirtualCity` pseudo-unit | `[UNIT]` |
| `lang/<Language>/tech_t.lng` | Display names/descriptions used by `Name`/`Description` in `tech.txt` | `"ID" LANG "text"` |

Display names of units, missiles and radars always come from the **technology** named in their `Tech`
property — there is no separate name field.

## 2. Syntax

* The format is free-form: line breaks do not matter to the parser, but put one property per line.
* Keywords are case-insensitive. **Unit, missile, radar and explosion IDs are case-sensitive**; technology
  IDs (and unit classes) are matched ignoring case. A `LeadsTo`/`Parent`/`BlockedBy` link to a technology
  that does not exist is silently ignored.
* Comments: `// …` to end of line and `/* … */` blocks.
* Strings: `"…"`. Numbers: `12`, `0.75`. Booleans: `Yes`/`No`, `true`/`false`.
* Flags such as `Slave`, `Ballistic` or `NoAutoDeploy` may be written bare (= Yes) or followed by
  `Yes`/`No`.
* Colours: `"RRGGBBAA"`, `RGB r g b`, or `RGBA r g b a` (0–255). Radar colours are the exception: four
  floats 0–1 (`RadarColor 0.0 0.0 0.15 0.15`).
* A file ends at `[END]` or end-of-file.

### ⚠ An unknown keyword stops the file

The game reads an entry's properties until it meets a word it does not recognise. It then goes back
to the top level and expects a new `[HEADER]`, `USE`, `IF` or a global setting. **If it finds anything
else, it stops reading that file** and shows an error such as
`Units/Missile_defs.txt: unknown keyword "Rnage" - the rest of this file was not loaded`.

```
[MISSILE] "SAM" MODIFY
  Rnage 400          // typo: loading of this file stops here; the ABM entry below is not loaded
[MISSILE] "ABM" MODIFY
  Range 900
```

Fix the word the message names and reload. The error names the word where the *top level* gave up,
which is the first unrecognised word after the last valid property.

## 3. Mods and file overriding

A mod folder mirrors the game folder. A file with the same relative path (for example
`MyMod/Units/Missile_defs.txt`) **replaces** the original. To extend instead of replace, start the file
with a `USE` of the previous version and then add or modify entries:

```
USE PREVIOUS "Units/Missile_defs.txt"     // the version from the game or from mods loaded before this one

[MISSILE] "SAM" MODIFY
  Range 350
```

| Form | Loads |
|---|---|
| `USE "path"` | The file as currently resolved (would include this mod's own copy — use only for *other* files) |
| `USE PREVIOUS "path"` | The same file as it was before this mod (base game or earlier mods) |
| `USE ORIGINAL "path"` | The unmodded game file |
| `USE MOD "ModName" "path"` | That file from a specific mod |

An optional `REPLACE` keyword after the form is accepted and ignored.

Using `USE PREVIOUS` plus `MODIFY` keeps your mod compatible with other mods that change other entries.

## 4. Creating, replacing and modifying entries

| Header form | Effect |
|---|---|
| `[UNIT] "New_ID"` | Creates a new entry. Required fields must be present. |
| `[UNIT] "Existing_ID"` | **Replaces** the entry: all its properties are reset to defaults and re-read. |
| `[UNIT] "Existing_ID" MODIFY` | Keeps everything and applies only the properties you write. |
| `[UNIT] "New_ID" COPY "Existing_ID"` | Units only: creates a new unit type as a copy, then applies what you write. |
| `[MISSILE] … MODIFY`, `[RADAR] … MODIFY`, `[EXPLOSION] … MODIFY`, `[TECHNOLOGY] … MODIFY` | Same as for units. |
| `[TECHNOLOGY] "Existing_ID" remove` | Removes a technology from the tree (it can never be researched). |

In `MODIFY` mode:

* **Single-value** properties (`Range`, `Speed`, `Tech`, …) are overwritten.
* **List** properties (`Weapon`, `Config`, `Radar`, `CanDetect`, `CanBeUsedAgainst`, `Modifier`,
  `ImprovedBy`, `AffectedBy`, `LeadsTo`, …) are **appended**. Use `delete` or `reset` to remove.

### `delete` and `reset`

`delete <property> <which>` removes one item; `reset <property>` clears the whole list.

| Object | `delete …` accepts | `reset …` accepts |
|---|---|---|
| Unit | `ImprovedBy`, `AffectedBy`, `Config "name"`, `Modifier "tech"`, `AchievementProperty "id"`, `Weapon "missile" [From "config"]`, `CanStoreMissiles "missile"`, `Radar "radar"`, `Airway n`, `CanHostAircraft "unit"`, `CanCarryUnit "unit"`, `AttackerInPlanner`, `NoAutoDeploy`, `AttackIfDestroyed`, `CanPatrolPoint`, `CanHangInTheAir`, `HiddenFromAllies`, `CanAccessGlobalStorage`, `NoAutoAttack`, `NoAutoAttackSub`, `CheckCoverage "missile"`, `CheckTargeting BY "missile"`, `Slave`, `Icon`, `RoundIcon`, `AbstractMovie`, `DisablingTech`, `Produces "unit or missile"`, `MoveToTarget "unit"`/`ANY` | `ImprovedBy`, `AffectedBy`, `Modifiers`, `AchievementProperties`, `Weapon` (all configs), `CanStoreMissiles`, `Radars`, `Airways`, `CanHostAircraft`, `CheckCoverage`, `CheckTargeting`, `CanCarryUnit`, `Produces`, `MoveToTarget` |
| Missile | `ImprovedBy`, `AffectedBy`, `Explosion "exp"`, `Ballistic`, `FreeFalling`, `AutoSlowDown`, `SingleAttack`, `CanBeUsedAgainst <class or "unit">`, `Affects <class>`, `GlobalShowType <group>`, `DisablingTech`, `AchievementProperty "id"` | `ImprovedBy`, `AffectedBy`, `CanBeUsedAgainst`, `Affects`, `GlobalShowType`, `AchievementProperties` |
| Radar | `ImprovedBy`, `AffectedBy`, `CanDetect <class or "unit">`, `GlobalShowType <group>`, `DoNotShow` | `ImprovedBy`, `AffectedBy`, `CanDetect`, `GlobalShowType` |
| Explosion | `Emulated`, `ImprovedBy`, `AffectedBy`, `AchievementProperty "id"` | `ImprovedBy`, `AffectedBy`, `AchievementProperties` |
| Technology | `LeadsTo "tech"`, `Parent "tech"`, `BlockedBy "tech"`, `AchievementProperty "id"` | `LeadsTo`, `Parent`, `BlockedBy`, `AchievementProperty` |

For the `delete ImprovedBy …` / `delete AffectedBy …` forms (by tech, by `Unit`, by `InRange`, `ALL <property>`)
see [06 — Tech modifiers](06-Tech-Modifiers.md#10-deleting-modifiers).

## 5. Conditional content: `IF` / `ELSE` / `ENDIF`

Every definition file supports conditions on **mod markers**. Each mod's name is automatically a marker;
a mod can declare more with `marker "text"` in its `info.txt`.

```
IF "Natural Resources Mod" AND NOT "OLD AI"
[UNIT] "Oil_Resource" MODIFY
  ProductionCost 5
ELSE
[UNIT] "Army_Base" MODIFY
  ProductionCost 4
ENDIF
```

* Conditions: `"marker"`, `NOT "marker"`, `( … )`, combined with `AND` / `OR`.
* `IF`/`ELSE`/`ENDIF` are only recognised **between entries**, never inside one. Wrap whole entries;
  an `IF` in the middle of a property list ends the entry and stops loading the file ([see above](#-an-unknown-keyword-stops-the-file)).

## 6. Units of measure

| Quantity | Unit | Notes |
|---|---|---|
| Distances: `Range`, `MinRange`, `Precision`, `Size`, explosion radii, radar range, `ResupplyRange`, `RepairRange`, `OccupationRadius`, `MaxAutoEngageRange`, `SplitMinDist` | km | The globe is modelled with a 40 960 km circumference (π radians = 20 480 km). |
| Altitudes: `MaxElevation`, `MinElevation`, radar `MaxHeight` | km | |
| `Speed` | km per game time unit | Same scale for units and missiles, and shown as-is in the unit panel, so compare values relative to each other. `VirtualSpeed` uses the same scale. |
| `TurnSpeed` | relative turn rate | Higher turns faster. |
| **"Seconds"** fields — unit `AttackDelay`, `ModelLaunchTime`, `SelfDestructTime`, `TimeToBoard`, `TimeToUnboard`, `TimeToHighState`, `TimeToLowState`, `AutoOnRestDelay`, `AutoCoolDownDelay`, `SensorsActivationDelay`, `WeaponsActivationDelay`, `OnDeployLaunchHostedDelay`; global `MinTimeToOccupyCity`, `MaxTimeToOccupyCity`, `MinTimeToOccupyUnit`, `CityOccupationMultPerPercent`; explosion `InstantFlashDuration`/`Growth` | 1 = 60 simulation ticks | |
| **Reload-time** fields — `Weapon … Time`, `Airway … Time`, `HangarExit … Time`, `Modify Weapon … Time` (non-multiply operations), explosion `LastingEffect` | 1 = 2 simulation ticks | So `Time 30` equals `1` in the row above; `Time 1800` = 60. The shipped data comments call **both** groups "seconds" (e.g. `Airway Launch 2 Time 180 // in seconds` and `TimeToHighState 3.0 // 3 seconds`), but the scales differ by 30: `Time 180` here lasts as long as `6` in the row above. |
| `DecayTimer` | ticks | Lifetime from full Power to zero. |
| `Power` (units and missiles) | hit points | Damage from explosions is subtracted from it. |
| `Damage` (explosions) | hit points | For cities it scales casualties instead, see [03](03-Explosions.md#3-hitting-cities). |
| `ProductionCost` | production points | Relative build cost. |
| Tech `Points` | research points | Multiplied by 0.01 and scaled by tech level. |
| Probabilities: `CanBeIntercepted` | 0–1 | Chance that one interceptor hit counts. |

## 7. Required fields

| Entry | Must have | Error if missing |
|---|---|---|
| `[UNIT]` | `Tech`, `Movie`, `Type`, `ProductionCost > 0`; `Crash` if the unit has a flight `Range` | "No technology assigned", "No movie assigned", "No type assigned", "Incorrect production cost", "No Crash explosion set for the ranged unit" |
| `[MISSILE]` | `Tech`, at least one `Explosion`, `Icon`; `Heads + FakeHeads` within the warhead limit | "No technology…", "No explosion type…", "No image…", "Too many warheads" |
| `[RADAR]` | `Tech` | "No technology assigned" |
| `[TECHNOLOGY]` | `Name`, `Description` | "No technology name", "No technology description" |

A missile entry that fails these checks while being *created* by a `MODIFY` header is skipped with a
warning instead of stopping the game.

## 8. Referencing and forward references

* A missile, radar, explosion or technology must exist before an entry refers to it (by load order above).
* Unit types may refer to unit types defined **later** in `Units.txt` (`CanHostAircraft`, `CanCarryUnit`,
  `HighState`, `LowState`, `Produces`, `ChangeTypeOnTech`, `MoveToTarget`). If such a unit is never
  defined, loading stops with "Unit type referenced but not defined".
