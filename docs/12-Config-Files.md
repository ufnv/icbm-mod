# 12 — Other configuration files

[Index](index.md) · [Basics](00-Basics.md)

Besides the unit, technology, AI, map and scenario files of the other chapters, the game reads a number of
smaller text files — not all of them with a `.txt` extension. All use the common format of
[00 — Basics](00-Basics.md#2-syntax) (`//` and `/* */` comments, `"strings"`, case-insensitive keywords) and
are looked up through the mod system, so a mod replaces one by shipping the same path; files that accept
`USE` can also extend the previous version with `USE PREVIOUS`.

Contents

1. [Overview](#1-overview)
2. [Mods: `info.txt`](#2-mods-infotxt)
3. [Game-wide settings](#3-game-wide-settings)
4. [Graphics and sound](#4-graphics-and-sound)
5. [Language files](#5-language-files)
6. [Player files](#6-player-files)
7. [Files used only by the Cheats build](#7-files-used-only-by-the-cheats-build)
8. [Game modes: Blitz, Standoff, Conquest](#8-game-modes-blitz-standoff-conquest)

---

## 1. Overview

**Game files** (in the game folder; a mod may replace or extend them):

| File | Contents | § |
|---|---|---|
| `MODS/<mod>/info.txt`, `Seasonal/<mod>/info.txt`, `GameMode/<mode>/info.txt` | Mod description | [2](#2-mods-infotxt) |
| `GameMode/Blitz/`, `GameMode/Standoff/`, `GameMode/Conquest/` | The game modes' own mods | [8](#8-game-modes-blitz-standoff-conquest) |
| `NewGameSettings.txt` | Game-setup defaults of a game mode | [8](#newgamesettingstxt) |
| `DefaultMap.txt` | Map and interface used by default | [3](#defaultmaptxt) |
| `Limits.txt` | Ranges of the game-setup sliders | [3](#limitstxt) |
| `Explodopedia.txt` | The Explodopedia's tab and category icons and its start page | [14](14-Explodopedia.md#explodopediatxt-icons-and-the-start-page) |
| `speed.txt` | Game-speed steps | [3](#speedtxt) |
| `espionage.txt` | Intelligence actions | [3](#espionagetxt) |
| `AdditionalElements.txt` | Extra pictures on the main menu, scroll speeds | [3](#additionalelementstxt) |
| `model_info.txt` | Faction model prefixes | [4](#model_infotxt) |
| `Units/pollution.txt` *(optional)* | Colours of fallout clouds | [4](#unitspollutiontxt) |
| `Units/Emulated/*.txt` | Procedural explosion animations | [4](#emulated-explosions-unitsemulatedtxt) |
| `*.MIDX`, variant files, model descriptors | Unit pictures and 3D models | [4](#pictures-and-models) |
| `ogg/music.txt` | Music for each game situation | [4](#oggmusictxt) |
| `UI/UI.txt` | Interface sprite sheet | [4](#uiuitxt) |
| `Lang/<language>/…` | Translations, fonts, loading hints, premade decks | [5](#5-language-files) |

Documented elsewhere: `Tech.txt` and `TechLevels.txt`, `ProductionEfficiency.txt` ([05](05-Technologies.md)),
`Tech_faction.txt` ([00](00-Basics.md#1-files)), `Units/*.txt` ([01](01-Units.md)–[04](04-Radars.md)), `AI/`
([08](08-AI.md)), `MAPS/` ([09](09-Maps.md)), `Scenario/` ([11](11-Campaigns-and-Scenarios.md)) and event scripts
(Events Script Reference) and the tutorial missions in `Tutorial/` ([13](13-Tutorials.md)).

**Player files** (in *Documents/My Games/ICBM-Escalation*) — [§6](#6-player-files).

**Cheats build only** — [§7](#7-files-used-only-by-the-cheats-build).

---

## 2. Mods: `info.txt`

The game collects mods from these folders, in this order: Steam Workshop items, the game's `MODS/`, the
game's `Seasonal/`, the game's `DLC/`, and `MODS/` in *Documents/My Games/ICBM-Escalation*. Each mod is a
folder with an `info.txt`:

```
ICBM MOD "NIGHT MAP" DefaultOff Silent
StaticSwitch 2866
Version "1.0.0"
Description "NIGHT MAP, by badtatts"
ChangeLog "First version."
marker "Night"
after "Some Other Mod"
```

The first group is read once, **in this order** (a key out of order is not recognised):

| Key | Meaning | Default |
|---|---|---|
| `ICBM MOD "Name"` | **Required, first.** The mod's name — also its first marker for `IF` and the name other mods refer to. | — |
| `DefaultOff` | The mod starts disabled. | enabled |
| `Silent` | Not listed among the host's mods in a multiplayer lobby. | listed |
| `StaticSwitch n` | Shown as an on/off switch on the main menu, labelled with UI string *n*, instead of in the mod list. | — |
| `Seasonal [From "YYYY-MM-DD"] [to "YYYY-MM-DD"]` | The mod exists only between these dates. | always |
| `Version "x"` | Version shown in the mod list. | `1.0` |
| `Description "text"` | Description in the mod list. | "No description" |
| `ChangeLog "text"` | Change log in the mod list. | — |
| `Path "folder"` | Data folder of the mod, if not the folder of `info.txt` (relative to the game folder). | the `info.txt` folder |

Then, in any order and any number of times:

| Key | Meaning |
|---|---|
| `marker "text"` | An extra marker for `IF` conditions in data files ([00 §5](00-Basics.md#5-conditional-content-if--else--endif)). |
| `before "Mod"` / `after "Mod"` | Load order relative to another mod. |
| `block "Mod"` | When this mod is enabled, that mod is disabled. |
| `Incompatible "Mod"` | This mod is disabled while that mod is enabled. |
| `Requires "Mod"` | This mod is disabled unless that mod is enabled. |
| `delete [file] "path"` | Accepted, no effect. |

**Game modes** are mods too, in `GameMode/`, applied automatically for the chosen mode — see
[§8](#8-game-modes-blitz-standoff-conquest). A map can bring its own mod as well ([09 §13](09-Maps.md#13-map-specific-mods)).

---

## 3. Game-wide settings

### `DefaultMap.txt`

```
DefaultMap "MAPS/EarthRRUltra.txt"
DefaultUI "UI/UI.txt"
```

The map selected by default in the game setup, and the interface layout used outside a game. Both lines are
optional, in this order.

### `Limits.txt`

Ranges and step sizes of the sliders in the game-setup screen. Any line may be left out; times are in ticks
(60 ticks = one game second).

| Keys | Slider | Defaults (min / max / step) |
|---|---|---|
| `MinEfficiencyTime`, `MaxEfficiencyTime`, `StepEfficiencyTime` | Full nuclear efficiency from | 0 / 720000 / 360 |
| `MinPeaceTimer`, `MaxPeaceTimer`, `StepPeaceTimer` | Peace timer | 0 / 144000 / 360 |
| `MaxNoNukesTimer`, `StepNoNukesTimer` | No-nukes timer (at least the peace maximum) | 216000 / 360 |
| `MaxConfigurableTimer`, `StepConfigurableTimer` | Limited-escalation timer (at least the no-nukes maximum) | 288000 / 360 |
| `MinCeasefireTimer`, `MaxCeasefireTimer`, `StepCeasefireTimer` | Ceasefire duration | 10800 / 54000 / 120 |
| `MaxPeaceTreatyTimer`, `StepPeaceTreatyTimer` | Peace-treaty duration | 108000 / 120 |
| `MinPermanentAllianceTimer`, `MaxPermanentAllianceTimer`, `StepPermanentAllianceTimer` | Partnership time to permanent alliance | 0 / 648000 / 360 |
| `MinPollution`, `MaxPollution` | Contamination speed | 0.25 / 2.25 |
| `MinGlobalProductionBoost`, `MaxGlobalProductionBoost` | Production boost | 0.25 / 4.0 |
| `MinGlobalScienceBoost`, `MaxGlobalScienceBoost` | Science boost | 0.25 / 4.0 |
| `MinCountdown`, `MaxCountdown` | End-game countdown trigger | 0.5 / 0.85 |
| `MinCountdownTime`, `MaxCountdownTime`, `StepCountdownTime` | End-game countdown length | 0 / 216000 / 120 |
| `MinAutoDeployTime`, `MaxAutoDeployTime`, `StepAutoDeployTime` | Auto-deployment time | — |
| `MinFullProductionAfterOccupation`, `MaxFullProductionAfterOccupation`, `StepFullProductionAfterOccupation` | Full production after occupation | 0 / 216000 / 360 |

`USE` is accepted. Inconsistent values are corrected (a maximum below its minimum is raised to it, steps
below 1 become 1).

### `speed.txt`

```
Speed   1 2 4 16
Divider 1 1 1 1 // ignored if the speed is > 1

ReplaySpeed 1 5 20 2000
Divider     1 1 1  1
```

The four game-speed buttons: `Speed` is the number of simulation steps per frame for each button;
`Divider` makes a speed of 1 slower by running one step every *n* frames. `ReplaySpeed`/`Divider` are the
same for replays. All four lines are required, in this order.

### `espionage.txt`

```
EventProbability 6750.0

Action RevealUnit          weight 100 success_rate 5
Action RevealConstruction  weight 100 success_rate 10
Action RevealProject       weight 100 success_rate 5
Action StealTechnology     weight 100 success_rate 1
Action RevealUnitInReserve weight 100 success_rate 10
Action RevealTechnology    weight 100 success_rate 15
```

| Key | Meaning |
|---|---|
| `EventProbability f` | How often intelligence operations are attempted (higher = more often); scaled by each faction's espionage spending and the number of factions. |
| `Action <type> weight w success_rate p` | For each operation type: its relative weight when an operation is chosen, and its chance of success in %. Types: `RevealUnit`, `RevealConstruction`, `RevealProject` (current research), `StealTechnology`, `RevealUnitInReserve`, `RevealTechnology`. |

### `AdditionalElements.txt`

```
Element "Images/ICBM_night-mode.png" 0.25 0.33
Scroller TechTree 1.5 ResearchQueue 1.0 General 1.2
```

| Key | Meaning |
|---|---|
| `Element "picture" x y` | Draws a picture on the main menu; `x`, `y` are its centre's offset from the screen centre as a fraction of the screen size. Repeatable. |
| `Scroller [TechTree f] [ResearchQueue f] [AvailableUnits f] [ConstructionUnits f] [ConstructionQueue f] [General f] [DestroyedCities f]` | Mouse-wheel scroll speed multipliers of the lists (`General` multiplies the map scroll speed). The parts are optional, in this order. |
| `USE "file"` | Includes another file (mods add elements with `USE PREVIOUS "AdditionalElements.txt"`). |

---

## 4. Graphics and sound

### `model_info.txt`

```
PREFIX "NA"
PREFIX "EU"
[END]
```

The faction prefixes that maps can give a faction with `ModelPrefix` ([09 §4](09-Maps.md#player-block)).
For a faction with prefix `XX`, every picture and model is looked for first under the folder `XX/` (e.g.
`NA/Units/IMAGES/…`) and then at its normal path; each prefix also creates the technology `PREFIX_XX`
([05](05-Technologies.md)). The order of the lines numbers the prefixes (from 0) for variant files below.
`USE` and `IF` are accepted; the file ends at `[END]`.

### `Units/pollution.txt`

Optional. `CloudColor c`, `FalloutColor c`, `FlashColor c` — colours of contamination clouds, fallout and
the flash, in this order.

### Emulated explosions (`Units/Emulated/*.txt`)

The procedural mushroom-cloud animations that explosions refer to with `Emulated "file"`
([03](03-Explosions.md)). Sections and keys are read **in the order below**; a key out of order is not
recognised. Every section and key is optional.

| Section | Keys |
|---|---|
| *(before the first section)* | `Size f`, `Angle f` — preview values, ignored by the game |
| `[BASE]` | `Draw`, `Size`, then `ImageMov "file"`, `WhiteMov "file"`, `LOD n`, `MaxHeightMult`, `RotationSpeed`, `GrowthSpeed`, `StemWidthMult` |
| `[WATER_RING]` | `Draw`, then `ImageMov`, `WhiteMov`, `LOD`, `FrameWidth`, `ElementSizeMult`, `CrownHeight`, `CrownSize` |
| `[HAT]` | `Draw`, then `ImageMov`, `WhiteMov`, `LOD`, `ScalingFrame`, `XYRatio`, `GoUpSpeed`, `FalloutScale`, `FalloutZSpeed`, `FalloutLengthSpeed`, `YellowTint`, `FireRing Yes/No` |
| `[RING]` (up to three: lower, top, third) | `Draw`, `Size`, `ShiftY`, then `WhiteMov`, `LOD`, `FirstAppearFrame`, `FadeInFrame`, `StartDecolorFrame`, `SpeedMult`, `ElementMult`, `Intensity`, `ShrinkSpeed`, `BothPositive` |
| `[LIGHT]` | `Draw`, `Scale`, `ProgressSpeedMultiplier`, `ColorProgressSpeedMultiplier`, `MinHeight`, `MaxHeight`, `StartCol c`, `EndCol c` |

A section that is absent is not drawn. `ImageMov`/`WhiteMov` default to the textures named in the comment
at the top of the shipped files.

The table names the original keys only. [03 §6](03-Explosions.md#6-emulated-explosion-files-unitsemulatedtxt)
has every setting, including the later ones and the `[WILSON]` and `[AURORA]` sections (between the last
`[RING]` and `[LIGHT]`), with defaults and shipped values. The **ICBM Explosion Simulator**
(`ICBM_ExplosionSimulator.exe`, [03 §6.10](03-Explosions.md#610-the-icbm-explosion-simulator)) plays these files
and edits them; it saves its changes into *Documents/My Games/ICBM-Escalation*, where the game looks first.

### Pictures and models

**Picture index (`*.MIDX`)** — what a unit's `Movie` (and other picture keys) point to:

```
Size 1
"units/images/airborne/abstract/SOF_AIRCRAFT.png"
```

| Form | Meaning |
|---|---|
| `AutoRotate` *(first line)* | The picture is rotated with the unit's heading. |
| ★ `Scale f` *(at the start, before or after `AutoRotate`)* | A unit's picture drawn *f* times bigger than its `DrawSize` gives (0.1–10): a picture drawn bigger or smaller in its frame than the unit's first one (an upgrade's, a faction's own) shows as big as the first. Not the abstract icon. |
| `Size n` + *n* `"picture"` lines | An animation of *n* frames (one frame = a still picture). |
| `Indexed [Prefix "path"] [Ext "png"] Size n [ExtraPerFrame n] [StartFrom n] [Every n]` | Frames numbered `Prefix000.png`, `Prefix001.png`, …, with 128/64/32-pixel versions in sub-folders. |
| `SplitBitmap "sheet" [Size] n` + *n* `Clip x y sx sy` | Frames cut from one picture. |
| `YShift f` | Vertical offset of the picture. |
| `Overlay "picture" x f y f sx f sy f speed n` | An animated overlay. |

**Faction variants** — instead of a picture or model file, a unit can point to a text file:

```
Default "Units/IMAGES/Tank.MIDX"
Variant 0 "Units/IMAGES/Tank_NA.MIDX"
Variant 4 "Units/IMAGES/Tank_RU.MIDX"
```

`Variant n` is used for factions with the *n*-th prefix of `model_info.txt` (counting from 0); others use
`Default`. Without such a file, the `XX/` folder rule of `model_info.txt` applies.

**3D model descriptor** — a model may be a small text file naming the model file (`MODEL "file.fbx"`) and
its animated parts (`TURREL`, `BARREL`, `HEAD`, `WING`, `EXHAUST`, `MISSILE`, `ELEMENT` entries). ★ `Scale f`
(0.1–10) draws the model *f* times bigger than the unit's `ModelDrawSize` gives, its hit spots and launch
points with it: a model that is thinner or smaller than the unit's first one (an upgrade's, a faction's own
in its `XX/` folder) shows as big as the others. ★ `Pivot Center` makes the model turn around, and stand
on the unit's spot with, the middle of its bounding box seen from above instead of its file's origin (for a
model whose origin is near one end); `Pivot x z` is that far from the middle, across and along, in lengths of
the model (−1–1). `Middle` after either also takes the middle of its height instead of its file's origin (for a
projectile, which flies centred on its spot: `Pivot Center Middle`). Its shadow, exhaust, launch points and hit spots follow. A file in the pack is changed by
putting the edited copy at the same path in the game folder.

### `ogg/music.txt`

```
"Peace" = "Peace Is Our Profession.ogg"
"Tension" = "Warheads Wide Awake.ogg", "Twitch In The Dead Hand.ogg"
```

`"Situation" = "track", "track", …` — the music tracks (in `ogg/`) for each game situation: `Open`,
`Peace`, `Tension`, `Conventional Invasion`, `Huge Invasion`, `Nuclear Sting`, `Battered Peace`,
`Victory Sting`, `Apocalyptic Violence`, `End Game`. Situation names are exact (case-sensitive).

### `UI/UI.txt`

The interface sprite sheets:

```
Source "UI/UI_2048.png"
Element Info_Top, 0, 0, 614, 60
Offset 12, 4, -2
```

| Key | Meaning |
|---|---|
| `Source "picture"` | A sprite sheet; the `Element`s that follow are cut from it. Repeatable. |
| `Element Name, x, y, width, height` | One interface element (the names are fixed by the game; a quoted name adds a new named element). |
| `Offset id, x, y` | Drawing offset of an element. |

A map can use its own layout file with `UIToUse` ([09 §8](09-Maps.md#8-display-settings)).

---

## 5. Language files

Each language is a folder `Lang/<language>/` (`Eng`, `Rus`, …):

| File | Contents |
|---|---|
| `codepage.table` | `Locale "name"`, the fonts (`BasicFont`, `ItalicFont`, `BoldFont`, `CondensedFont`, `AltFont` — `.ttf`/`.otf` in the game folder), their sizes (`FontSizes`, `ItalicFontSizes`, `BoldFontSizes`, `CondensedFontSizes`, `AltFontSizes`, twelve values each, smallest to largest), then `Uppercase` and `"lower" High "UPPER"` letter pairs, then `END`. |
| `UI.lng` | Interface strings: `<number> LANG "text"`, ending with `END`. Numbers are the string IDs used everywhere (`Name ID`, `Text ID`, `UI_STRING(…)`). |
| `tech_t.lng` | Technology names and descriptions: `"key" LANG "text"`. |
| `unit.lng`, `city.lng`, `scenario.lng` | Same `"key" LANG "text"` form, for unit, city and region, and scenario names. |
| `explodopedia.lng` | The Explodopedia's texts: category and research field descriptions, explosion texts, general information articles ([chapter 14](14-Explodopedia.md)). |
| `loading.lng` | Loading-screen hints: one `"text"` per hint, ending with `END`. Loading-screen pictures are taken from `Images/loading/` (`.jpg`/`.png`). |
| `videolinks.txt` | Links opened from the menus, e.g. `MainMenu "https://…"`, ending with `END`. |
| `UNIT_NAME/default.txt`, `UNIT_NAME/<prefix>.txt` | Premade unit decks (below). |

All string files accept `USE` (e.g. `USE PREVIOUS "LANG/Eng/UI.lng"`) and `IF`; a later entry with the same
key replaces the earlier one. A mod reserves its own range of numeric IDs to avoid collisions.

**Premade decks** (`UNIT_NAME/*.txt`) — the unit names offered for a faction prefix:

```
DECK_NAME "United States Pre-Made Deck"
Unit "Missile_Silo"
"U_Missile_Silo" NAME "Blast Door Silo"
END
```

`DECK_NAME "name"`; then for each `Unit "Unit_ID"`, pairs `"technology" NAME "display name"` — the name the
unit shows once that technology (of its upgrade line) is known. `default.txt` is the deck for factions
without a prefix.

---

## 6. Player files

These live in *Documents/My Games/ICBM-Escalation* and belong to the player, not to a mod:

| File | Contents |
|---|---|
| `GRAPHICS.txt`, `hotkeys.txt`, `autopause.txt` | Graphics, key and auto-pause settings — edited with the configurator `ICBM_CFG.exe` or the in-game options. |
| `NewGameSettings.txt` *(optional)* | Not written by the game. If you put one here, it is used instead of the game mode's game-setup defaults, in every mode ([§8](#newgamesettingstxt)). |
| `DECKS/` | Unit decks saved by the player. |
| `SAVES/`, `SAVES_MP/` | Saved games ([09 §11](09-Maps.md#11-making-a-map-from-a-saved-game)). |
| `MAPS/` | Generated map files, which take priority over mods ([09](09-Maps.md#water-and-land-masks)). |

---

## 7. Files used only by the Cheats build

The [Cheats build](10-Cheats-Build.md) reads these when generating map data ([09](09-Maps.md)); the normal
game never opens them:

| File | Read by | Format |
|---|---|---|
| Border drawing (`.svg`) | `ProcessBorders ReadSVG` | vector drawing of the region borders |
| Point-and-edge file (`V7_split.txt`) | `ProcessBorders EditPoints`, `GenerateSplit Load` | [09 §9](09-Maps.md#9-building-the-border-and-region-files-processborders) |
| Segment centre points (`V7_split.bin.points.txt`) | `GenerateSplit … SplitCenterPoints` | [09 §9](09-Maps.md#9-building-the-border-and-region-files-processborders) |
| Mask outlines (`.svg`, `.svg.view.png`) | `EditSVG`, `WaterMap … Generate … SVG` | [09 §3](09-Maps.md#editing-masks-interactively-editsvg) |
| Terrain picture (`.png`) | `TerrainTypeMap … Generate from` | picture in the `Terrain` colours |

The Cheats build writes its scenarios with the normal save format ([10 §2](10-Cheats-Build.md#2-saving-as-a-scenario)).
`AIConfig.txt` (input of `AICache … generate`) and the mask, city and relocation generators work in both
builds ([09](09-Maps.md)).

---

## 8. Game modes: Blitz, Standoff, Conquest

*New Game* offers four choices: **Blitz**, **Standoff**, **Conquest** and **Campaign** (UI strings
3342–3345, descriptions 3346–3349). A multiplayer host picks one of the first three, and the players who
join switch to the host's mode. Each of the three is a **mod** in the game's `GameMode/` folder, with the
usual `info.txt` ([§2](#2-mods-infotxt)). The game turns it on by itself when the mode is chosen and turns
it off when the game ends; it never appears in the mod list.

### Which files win

A game-mode mod is searched **before** the mods the player enabled. A map-specific mod
([09 §13](09-Maps.md#13-map-specific-mods)) is searched before both:

```
map-specific mod  →  game-mode mod  →  enabled mods (in their order)  →  game folder
```

The first file found with the requested path is used. A file that starts with `USE PREVIOUS "path"` reads
the next one down the chain, so changes stack:

* **Standoff and Conquest** extend the base files with `USE PREVIOUS`. Your mod's changes to the same
  files still apply in these modes, with the mode's changes on top.
* **Blitz** replaces its files completely, without `USE PREVIOUS`. In Blitz, your mod's versions of
  `Tech.txt`, `Units/Units.txt`, `Units/Missiles.txt`, `Units/Radars.txt`, `Units/explosion.txt`, the AI
  files and the other files Blitz ships are **not read**: such a mod changes only the other modes. Files
  that Blitz does not ship (for example `Limits.txt` or `espionage.txt`) are still read from your mod.

**Where the mode's folder comes from.** The game looks for `GameMode/<mode>/info.txt` like any other file:
first in *Documents/My Games/ICBM-Escalation*, then in the enabled mods, then in the game folder. The mode
then reads its files from the folder where that `info.txt` was found. A mod that ships its own
`GameMode/Blitz/` folder (with `info.txt`) therefore **replaces the whole Blitz folder**. Copy every file
of the original folder into it and change what you need; keep the `ICBM MOD "BLITZ"` name, so that `IF`
markers still work.

Achievements are not awarded in Blitz.

### What each mode changes

| Mode | `GameMode/…` files | Effect |
|---|---|---|
| **Blitz** | `Tech.txt`, `TechLevels.txt`, `ProductionEfficiency.txt`, `Units/Units.txt`, `Units/Missiles.txt`, `Units/Radars.txt`, `Units/explosion.txt`, `Units/Emulated/*.txt`, `AI/` (`SupportTypes`, `NuclearTypes`, `DefenceDef`, `GroupsConquest`, `StrategyConquest`, `Conditional`, `MissileCategoryMapping`), `Lang/*/tech_t.lng`, `MAPS/EarthRRUltra.txt`, `MAPS/IronCurtain.txt` | A separate, simpler game: its own technology tree, units, weapons, sensors, explosions and AI, and its own versions of two maps (they hide the base maps of the same name while Blitz is on). |
| **Standoff** | `NewGameSettings.txt`, `Limits.txt`, `Tech.txt`, `Units/Units.txt` | Faster economy: production ×1.35, science ×6, espionage ×3, with slider ranges production 1–4 and science 3–8. Also: a 10-minute peace timer and 15-minute no-nukes timer, no instant tech sharing with allies, regions destroyed below 1 % of their population. `Tech.txt` adds an empty technology `GDP_MOD`; the matching `VirtualCity` change in `Units/Units.txt` is commented out. |
| **Conquest** | `NewGameSettings.txt`, `Limits.txt`, `Units/explosion.txt`, `Maps/Events/CommonAI.txt` | The base economy, scored as **Conquest** with no end-of-game countdown (`TimeToFinish 0`). The same timers as Standoff, no instant tech sharing, regions destroyed below 1 %, surrender below 10 % population. Pollution from explosions is scaled by 0.2 (`PollutionMultiplier`), with the contamination slider set to 0.1–5.0. `CommonAI.txt` adds event blocks for a gradual escalation (`DisableMassDestruction()` and the blocks that re-enable weapons when they are used against a faction); `SetCommonAIEvents()` does not call them. |
| **Campaign** | — | No game-mode mod: the base game's data, plus each mission's own map-specific mod ([11 §8](11-Campaigns-and-Scenarios.md#8-mission-specific-mods)). |

Tutorial missions also run without a game-mode mod.

A saved game remembers its mode (`GameMode 3342` … `3345` in `version.num`); loading it turns the same
game-mode mod on again.

### `NewGameSettings.txt`

The defaults of the game-setup screen for a mode. The game reads it when the setup screen opens and when
**Reset to default** is pressed. The map's own lobby defaults ([09 §7](09-Maps.md#7-game-rules-lobby-defaults))
are applied after it, so a value set in the map file wins. The keys are those of 09 §7, plus:

| Key | Meaning |
|---|---|
| `ScoringMode Default\|Survival\|Genocide\|Conquest` | Scoring (names instead of the numbers of 09 §7). |
| `AIDifficulty VeryEasy\|Easy\|Normal\|Hard\|VeryHard\|Insane` | Computer players' difficulty. |
| `StartInAlliance`, `AllowObservers`, `EqualizePopulation`, `EqualizeGDP`, `RandomSide`, `RatedMatch` `Yes\|No` | The matching switches of the setup screen. |
| `TotalPointsToDistribute f`, `MaxPointsToDistribute f` | Points for buying the starting setup. |
| `MinAllowedRating n` | Lowest rating that may join a rated multiplayer game. |
| `PauseTime ms` | Pause time each multiplayer player may use, in milliseconds. |
| `ContaminationSpeed f` | The contamination-speed slider (the map file calls it `PollutionSpeedCoeff`). |

The file ends at `END`. `USE PREVIOUS "NewGameSettings.txt"` (as in the shipped modes) first reads the
previous version, if any. Reading stops at the first unknown keyword, and the rest of the file is ignored.

A `NewGameSettings.txt` in *Documents/My Games/ICBM-Escalation* is found before every mod, so it replaces
the game modes' files in every mode.

### Making a mode-specific change

* **Change one mode only:** a regular mod cannot target one mode. Put an `IF` around the change in the
  data file instead — the game-mode mods' names are markers like any mod's (`"BLITZ"`, `"CONQUEST"`,
  `"Standoff Mode"`; [00 §5](00-Basics.md#5-conditional-content-if--else--endif)).
* **Change the game-setup defaults of a mode:** a plain `NewGameSettings.txt` in your mod is not used,
  because the mode's file is found first. Ship a complete copy of the mode's folder (above) with your
  changed `NewGameSettings.txt`, or set the defaults in the map file (09 §7), since the map's values win.
* **Change Blitz:** ship a complete copy of `GameMode/Blitz/` with your changes (above).
* **Change one map only:** use a map-specific mod ([09 §13](09-Maps.md#13-map-specific-mods)).
