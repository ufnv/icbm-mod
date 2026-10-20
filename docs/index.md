# ICBM: Escalation — Modder's Reference for Units, Weapons, Sensors and Technologies

This folder documents every property that the game reads from its unit, missile, radar, explosion and
technology definition files, what each one does in the simulation, its default value, and how to tune it
safely, plus the AI configuration files in `AI/` ([chapter 08](08-AI.md)) the map files in `MAPS/` ([chapter 09](09-Maps.md)), the Cheats build ([chapter 10](10-Cheats-Build.md)) and campaigns ([chapter 11](11-Campaigns-and-Scenarios.md)), and the texts of the Explodopedia ([chapter 14](14-Explodopedia.md)). Everything here describes how the game reads and uses these values, and the value
catalogs (A1–A5) were generated from the shipped data files.

| # | Document | What it covers |
|---|---|---|
| 00 | [Basics](00-Basics.md) | File layout, load order, mods (`USE PREVIOUS`), `MODIFY` / `COPY` / `delete` / `reset`, `IF` markers, units of measure, what happens on an unknown keyword |
| 01 | [Units](01-Units.md) | Every `[UNIT]` property: stats, weapon configs, hangars/airways, readiness states, occupation, AI hints, global unit settings, `VirtualCity` |
| 02 | [Missiles](02-Missiles.md) | Every `[MISSILE]` / `[TYPE]` property: targeting classes, range/speed/precision, MIRVs, Geneva & AI categories, AI hints, trajectories |
| 03 | [Explosions & combat](03-Explosions.md) | Every `[EXPLOSION]` property, the exact damage, precision, interception and city-casualty formulas, the emulated (procedural) explosion files, and the ICBM Explosion Simulator that plays and edits them |
| 04 | [Radars](04-Radars.md) | Every `[RADAR]` / `[TYPE]` property: detection classes, range, altitude ceiling, precise targeting |
| 05 | [Technologies](05-Technologies.md) | `tech.txt`: `[TECHNOLOGY]`, `[TYPE]`, `[LEVEL]`, `[UNIT_CLASS]`, `[DEFCON]`, costs and tech levels, built-in techs, `TechLevels.txt` |
| 06 | [Tech modifiers](06-Tech-Modifiers.md) | `ImprovedBy` / `AffectedBy`: all headers, operators, `Complex`/`case`, `Unless`, `AND`, `{ }` blocks, `Modifier` tags, which property names work on which object, evaluation order |
| 07 | [Tuning guide](07-Tuning-Guide.md) | Recipes for common balance changes, how to test them, and how event scripts interact with these definitions |
| 08 | [AI configuration](08-AI.md) | The `AI/` folder: support and nuclear roles, defence groups, group compositions and targets, strategies and research lists, dynamic build rules, research reactions, war thresholds, pitfalls |
| 09 | [Maps](09-Maps.md) | The map file in `MAPS/`: names, water and land masks, terrain, regions and factions, cities, starting setup, AI cache, lobby defaults, display settings, region-building tools, making a new map, map-specific mods |
| 10 | [Cheats build](10-Cheats-Build.md) | The modding edition of the game: every cheat key combination (instant research and production, free placement, switching sides, territory, coordinates and IDs), saving as a scenario |
| 11 | [Campaigns and scenarios](11-Campaigns-and-Scenarios.md) | The top-level `SCENARIO` file, `ScenarioInfo`, missions in event scripts, chaining missions, DLC campaigns, preparing a mission map in the Cheats build, mission-specific mods, a 3-mission tutorial |
| 12 | [Other configuration files](12-Config-Files.md) | Mod `info.txt`, `DefaultMap.txt`, `Limits.txt`, `speed.txt`, `espionage.txt`, `AdditionalElements.txt`, `model_info.txt`, emulated explosions, picture and model files, music, interface layout, language files, player files, Cheats-build-only files, game modes (Blitz, Standoff, Conquest) and their mods, `NewGameSettings.txt` |
| 13 | [Tutorial missions](13-Tutorials.md) | `Tutorial/MissionN/`: the tutorial script language — messages, waiting for the player's actions (events and variables), actions that lock and unlock the interface, highlight units, add units and drive diplomacy, timers and subroutines, the full event list, making and checking a tutorial mission |
| 14 | [Explodopedia](14-Explodopedia.md) | The in-game encyclopedia: which objects get pages and where each part of a page comes from, `explodopedia.lng` (category and field descriptions, explosion texts), general information articles in plain text or basic HTML (links, pictures), adding them in a mod or a translation |
| A1 | [Unit catalog](A1-Catalog-Units.md) | Base values of all shipped unit types, their weapon configs, radars, hosted units and modifier tags |
| A2 | [Missile catalog](A2-Catalog-Missiles.md) | Base values of all shipped weapons, type templates, Geneva and AI categories |
| A3 | [Explosion catalog](A3-Catalog-Explosions.md) | Damage, radii, yields and lasting effects of all explosions |
| A4 | [Radar catalog](A4-Catalog-Radars.md) | Range, altitude ceiling and detection classes of all sensors |
| A5 | [Technology catalog](A5-Catalog-Technologies.md) | Every technology with display name, cost, level, category and unlocks |

## How the pieces fit together

```
tech.txt ──────────────► Technology  ◄─── every unit / missile / radar needs one (Tech "…"): it gives the
   │                        ▲             display name and makes the object available when researched
   │                        │
   │                ImprovedBy / AffectedBy "tech"  (06)
   │                        │
Units/Radars.txt ───► Radar ─┐
Units/explosion.txt ► Explosion ◄── Explosion "…" ── Missile ◄── Weapon "…" in a Config ── Unit type
Units/Missiles.txt ─► (Missile_types.txt + Missile_defs.txt)            Radar "…" ──────────┘
Units/Units.txt ────► Unit types (and the VirtualCity pseudo-unit)
```

* A **unit type** carries **weapon configs** (lists of missiles with stock, salvo size and reload time),
  **radars**, hosted units, and **modifier tags**.
* A **missile** is any weapon or effect a unit can apply — guns, lasers, cyber attacks, buffs and
  debuffs are all missiles. It flies (or acts instantly) and then produces one or more **explosions**.
* An **explosion** carries the actual damage, blast radii, casualties, pollution and lasting effects.
* A **radar** is any sensor (radar, sonar, optics, satellite camera).
* **Technologies** unlock objects and drive almost all balance through **tech modifiers**.

## Load order at start-up

1. `Units/explosion.txt` (explosions)
2. `Units/Radars.txt`
3. `Units/Missiles.txt` (which `USE`s `Missile_types.txt` then `Missile_defs.txt`)
4. `Units/Units.txt`
5. `tech.txt` is loaded before all of these (the object files look technologies up by ID).

An object can only refer to things loaded earlier or in the same file (unit types may forward-reference
other unit types in the same file). A multiplayer game compares a CRC of the loaded values, so every
player must run the same mods.

## Source of truth

When this document and the shipped data disagree about a *value*, the data files win — the catalogs are
a snapshot. When it disagrees about *syntax or behaviour* with what the game does, the game wins; please report it.
