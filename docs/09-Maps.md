# 09 — Maps (the `MAPS/` folder)

[Index](index.md) · [Basics](00-Basics.md)

A map is one text file in the game's `MAPS/` folder (for example `MAPS/EarthRRUltra.txt`) plus the data
files it points to: water and land masks, regions, cities, terrain, height map, the AI cache and the
texture pack. This chapter documents every keyword of the map file and the format of the text files it
uses.

Contents

1. [How the game finds and reads a map](#1-how-the-game-finds-and-reads-a-map)
2. [Header: name, description, view](#2-header-name-description-view)
3. [Geography: water, land, terrain, height, textures](#3-geography-water-land-terrain-height-textures)
4. [Regions and factions: `OwnershipMap`](#4-regions-and-factions-ownershipmap)
5. [Cities](#5-cities)
6. [Starting setup and AI](#6-starting-setup-and-ai)
7. [Game rules (lobby defaults)](#7-game-rules-lobby-defaults)
8. [Display settings](#8-display-settings)
9. [Building the border and region files: `ProcessBorders`](#9-building-the-border-and-region-files-processborders)
10. [Making a new map, step by step (Cheats build)](#10-making-a-new-map-step-by-step-cheats-build)
11. [Making a map from a saved game](#11-making-a-map-from-a-saved-game)
12. [Keys used by saved games and scenarios](#12-keys-used-by-saved-games-and-scenarios)
13. [Map-specific mods](#13-map-specific-mods)
14. [Pitfalls](#14-pitfalls)

---

## 1. How the game finds and reads a map

### Files

| File | Contents |
|---|---|
| `MAPS/<Map>.txt` | The map file — this chapter. |
| `MAPS/<Map>.virtual/` | The map's data: binary masks (`*.vec`, `*.vec.cmap`, `*.bin`), region files (`V7_*.txt`), cities (`earth_cities.csv`, `*.reloc.txt`), AI cache (`ai_cache_new.bin`), city models, faction event scripts (`Events/*.txt`). `SRC/` holds the sources used to generate them (`AIConfig.txt`, SVG/PNG drawings). |
| `MAPS/<TexturePack>/` (e.g. `MAPS/EARTH256K/`) | The texture pack: `map.e5i` + `map.e5p` (the tiled globe texture), `Default.jxl`/`.webp`/`.png` (full overview), `Default_small.png` (map-list preview), `HeightMap.cmap`, `config.txt`. Several maps can share one pack. |
| `MAPS/Events/` | Event scripts shared by several maps (e.g. `CommonAI.txt`). |

Paths inside the map file are relative to the game folder (`"Maps/EarthRRUltraV3.virtual/V7_split.bin"`);
the lookup is case-insensitive on Windows. Mods are searched before the game folder, so a mod can replace a
map file or any data file by shipping the same path.

### The map list

The *Select map* screen lists every file in `MAPS/` of the game and of each enabled mod that

* starts with `MAP`, followed directly by its `Name` lines (and optionally `Description`, `Restrictions`,
  `WaterMap`), and
* contains a `TextureMap` whose folder has a `default_small.png` (the preview).

A file without these is not listed. A map with the same file name in a mod hides the original.

### Reading

The file is a sequence of keywords in free format (see [00 — Basics](00-Basics.md#2-syntax): `//` and
`/* */` comments, `"strings"`, case-insensitive keywords). Keywords may come in any order and the file ends
at `END`. `USE "file"` reads another file in the same format at that point, and `IF`/`ELSE`/`ENDIF` work as
in the other data files.

An unknown keyword stops loading with the message *Error reading map …, formatting error line N*; nothing
after it is read. Use the order of the shipped maps: the multiplayer consistency check reads the
geography keywords first, then `OwnershipMap` with its `Player` list, then `Cities`, then the AI tolerances
(§6), and looks only for those positions.

A **saved game** and a **scenario** are the same format: the map part followed by the state of the game
(units, research, diplomacy…). §12 lists the keys that belong only there.

### Units used in map files

| Quantity | Unit |
|---|---|
| Map coordinates `x y` | 0–1 across the whole globe: `x` from 180° W (0) eastwards to 180° E (1), `y` from the North Pole (0) to the South Pole (1). So `x = (longitude + 180) / 360`, `y = (90 − latitude) / 180`. |
| Distances | km, unless noted |
| Times | simulation ticks; 60 ticks = one game second ([00 — Basics](00-Basics.md#6-units-of-measure)) |
| Colours | `"RRGGBB"` or `"RRGGBBAA"` (hex), or `#RRGGBB` |

---

## 2. Header: name, description, view

```
MAP

Name idx "Atomic Earth, 10 Players"
Name RUS "Атомная Земля, 10 игроков"
Description ENG "Ten massive regional factions vie for global supremacy…"

Restrictions MinScale 0.75 MaxScale 100.0 CenterX 0.5 CenterY 0.5 ShiftX 2 ShiftY 2
```

| Keyword | Meaning |
|---|---|
| `MAP` | First word of the file. |
| `Name [LOCALE] "text"`, repeatable | Map name. The first line is the fallback; a line whose locale (`ENG`, `CHN`, `ESP`, `FRA`, `GER`, `ITA`, `RUS`, case-insensitive) matches the game language wins. Without a locale the line counts as the current language. `Name ID n` uses UI string *n*. The shipped maps use the placeholder locale `idx` for the fallback line. |
| `Description [LOCALE] "text"`, repeatable | Description shown in the lobby. Same rules. |
| `Restrictions MinScale a MaxScale b CenterX x CenterY y ShiftX sx ShiftY sy` | Camera limits: zoom range and the initial centre (map coordinates). All six values are required, in this order. |
| `MapSpecificMod "folder" [ForceLoading]` | A mod that is loaded together with this map: its data files take part in the game only on this map (§13). |
| `USE "file"` | Reads another file in this format here. |

---

## 3. Geography: water, land, terrain, height, textures

```
WaterMap       "Maps/EarthRRUltraV3.virtual/watermap_16K.vec"
WaterMapNoIce  "Maps/EarthRRUltraV3.virtual/watermap_no_ice_16K.vec"
WaterMapLand   "Maps/EarthRRUltraV3.virtual/watermap_land_16K.vec"
ConditionalWaterMap "Maps/EarthRRUltraV3.virtual/Conditional.bin"
LandingPairs   "Maps/EarthRRUltraV3.virtual/landing_pairs.bin"
TerrainTypeMap "Maps/EarthRRUltraV3.virtual/terrain_type.vec"
  Terrain "Water"  Color #8CC8FA
  Terrain "Savanna" Color #C6CF5D Group "Grassland"
HeightMap  "Maps/EARTH256K/HeightMap.cmap"
TextureMap "Maps/EARTH256K"
```

### Water and land masks

The three masks are vector maps of the sea, used for movement and path finding. Each `X.vec` has a
companion `X.vec.cmap` (coded version) that the game loads automatically.

| Keyword | Used for |
|---|---|
| `WaterMap "file.vec"` | Surface ships: the sea, with pack ice treated as land. |
| `WaterMapNoIce "file.vec"` | Submarines: the sea including the area under the ice. |
| `WaterMapLand "file.vec"` | Ground units: the land (land paths). |
| `ConditionalWaterMap "file.bin" [generate]` | Land paths through each region, so ground units can be blocked by region ownership (e.g. not moving through neutral territory). Regenerate whenever region borders or their numbering change. |
| `LandingPairs "file.bin" [generate]` | Precomputed pairs of nearby land and sea points, used to embark and land troops by sea. Regenerate when cities or regions change. |

**Generating a mask.** Instead of loading, a mask can be built from a picture and, as Earth's are, from an
SVG drawing of its outlines:

```
WaterMap "Maps/MyMap.virtual/watermap_16K.vec"
  Generate from "Maps/MyMap.virtual/SRC/test_16K_ice.svg.view.png" SVG "Maps/MyMap.virtual/SRC/test_16K_ice.svg"
  [smooth 36000] [filter 25000] [MapSize 16384 [ShiftX n] [ShiftY n]] [water black]
```

| Option | Meaning | Default |
|---|---|---|
| `from "image.png"` | The mask picture. A pixel is water when the average of its red, green and blue is above 200 (white); with `water black`, below 56 (black). The picture's height sets the grid size. | — |
| `SVG "file.svg"` | Take the outlines from this drawing (the file [`EditSVG`](#editing-masks-interactively-editsvg) edits) instead of tracing them from the picture. The picture is still needed: export it from the SVG's `.view.svg`. | — |
| `smooth s`, `filter f` | Smoothing and small-detail filtering of outlines traced from the picture (larger = finer); not used with `SVG`. | 36000, 25000 |
| `MapSize n` | Grid size, a power of 2. `ShiftX`/`ShiftY` shift the grid. | twice the picture height |
| `water black` | Water is black in the picture, land white (as in an exported `.view.png`). | water is white |

`pfcache "file" [generate]` after a mask is read but does nothing in 1.1.5.

Put the `Generate …` line in (remove its `//`) and start the map in single player. The game draws the new mask
for checking (its coded map as the overlay; with the overlay off, its outlines in yellow) and writes `X.vec` and
`X.vec.cmap` into *Documents/My Games/ICBM-Escalation* under the same path as in the map file (for the line
above, `Documents/My Games/ICBM-Escalation/Maps/MyMap.virtual/watermap_16K.vec`; ICBM.CFG's `DataPath` instead
when it is set). Quit, move both files into your mod's folder, put the `Generate …` line behind `//` again and
delete the copies from *Documents*: files there are read before the mods' and would hide your mod's.

A run that generates a mask (or a [simple ownership picture](#simple-ownership-picture)) leaves out the regions and
the cities' processing: generate nothing else in the same run.

> **Which `generate` options work where.** The normal game generates the water masks, the simple ownership
> picture, the city list (`FromFile … Generate From`), city relocation (`relocate … generate`) and the AI cache.
> `ConditionalWaterMap … generate`, `LandingPairs … generate`, `TerrainTypeMap … Generate`, `HeightMap …
> generate`, city models (`ModelsPath … generate`), `EditSVG` and `ProcessBorders` work only in the
> [Cheats build](10-Cheats-Build.md). The normal game reads these lines without an error but does nothing;
> worse, a `generate` left after `ConditionalWaterMap`, `LandingPairs`, `HeightMap` or `TerrainTypeMap` makes it
> load nothing for that line. Put every one of them behind `//` before publishing.

### Editing masks interactively: `EditSVG`

```
EditSVG "Maps/MyMap.virtual/SRC/test_16K.svg" [Size n] [Save "out.svg"]
  [Second "Maps/MyMap.virtual/SRC/test_16K_ice.svg" [Save "out2.svg"]]
  [Mask WaterMap | WaterMapNoIce | WaterMapLand]
```

In the Cheats build, opens the outlines of an SVG drawing on the battle map (flat view) for editing. Earth's drawings are in
`Maps/EarthRRUltraV3.virtual/SRC/`: `test_16K_ice.svg` for `WaterMap` (the sea ice counted as land),
`test_16K.svg` for `WaterMapNoIce` (the sea under the ice is water), `test_16K_land.svg` for `WaterMapLand`.

| Part | Meaning |
|---|---|
| `EditSVG "file.svg"` | The drawing to edit. Every path and every subpath of it is one closed outline; curves are reduced to their end points, colours are ignored. Its outlines are drawn in yellow, lakes (once known, see **R**) in orange. |
| `Save "file.svg"` | Where to save it. Default: the file itself. |
| `Second "file.svg" [Save …]` | A second drawing edited together with the first (drawn in blue): the outlines with and without the sea ice are the same away from the poles, so a vertex moved in both moves in both. |
| `Mask WaterMap` / `WaterMapNoIce` / `WaterMapLand` | Draws that mask, as the map file has already loaded it, in red underneath for reference — e.g. `WaterMap` while editing the land map. |
| `Size n` | The width the drawing's coordinates are divided by. Default: twice the drawing's height. |

**Mouse and keys** (a vertex under the cursor snaps within 16 screen pixels):

| Action | Does |
|---|---|
| Left drag a vertex | moves it |
| Left drag an edge | puts a new vertex there and moves it |
| Right click a vertex | deletes it (an outline left with one vertex goes) |
| Shift + left click on empty space | a new small square outline, to drag into shape |
| Shift held while letting a dragged vertex go on another outline's edge | splices the two outlines there (joins them, or splits one in two) |
| Alt held | leaves the first drawing alone (acts on `Second` only) |
| Ctrl held | leaves the `Second` drawing alone |
| **R** | works out which outline lies inside which (lakes in land, islands in lakes) and saves |

There is no undo: back the drawings up before a session. Every change saves the drawing(s) at once. Press **R**
before you finish: until then every outline counts as land, lakes too. Outlines must not cross each other or
themselves. The editor has no end: quit the game when done and put the `EditSVG` lines behind `//`.

**What is saved.** The drawing itself, its outlines as white paths (a land outline with its lakes as subpaths),
and `<file>.view.svg`: the same on a black background, with the outlines that cross the map's left or right edge
(the polar caps) taken round along its top or bottom. The game writes no picture. Open `<file>.view.svg` in a vector
editor (Inkscape), export it as a PNG of the drawing's own size and name it `<file>.view.png`: that picture and the
drawing are what `Generate from "<file>.view.png" SVG "<file>" water black` reads.

### Terrain types

```
TerrainTypeMap "file.vec" [Generate from "terrain.png"]
  Terrain "Name" [NameIDX n] [DescriptionIDX n] [Color c] [Group "Earlier terrain"]
  …
```

Each `Terrain` is one terrain type; the colour is its colour in the terrain overlay and, when generating,
the colour that identifies it in the source picture. `Group "X"` makes the type count as the earlier type
*X* for game rules — technology modifiers check terrain **groups**
([`ImprovedBy Terrain "group"`](06-Tech-Modifiers.md)). Up to 254 types.
`NameIDX`/`DescriptionIDX` give translated names from the UI strings.

### Height map and textures

| Keyword | Meaning |
|---|---|
| `HeightMap "file.cmap" [generate size]` | Elevation, used for the terrain view and for the ground height of units. |
| `TextureMap "folder" [LightBlendAlpha Yes/No] [LightBlendPower f] [AffectedArea x y z r]…` | The texture pack. The folder needs `map.e5i`/`map.e5p`, a `default.jxl`, `default.webp` or `default.png` overview and `default_small.png`. `config.txt` in the folder may list required content as `ID n "name"` lines; other lines are ignored. `AffectedArea` entries (a point on the unit sphere and a radius) mark areas where the texture is altered. |
| `EdgesMap "image"` | Optional edge texture. |
| `MapShader`, `TerrainShader`, `UnitShader`, `SilhouetteShader` | No longer used: the game always draws the map with `water_effect_v_mod`/`water_effect_f` and units with its own shaders. The lines are skipped in older maps and saves. To change a shader for one map, give the map a map-specific mod with its own copy of the shader file under `shaders/HLSL/` and `shaders/GLSL/`. |

---

## 4. Regions and factions: `OwnershipMap`

A map is divided into **regions** (provinces); each region belongs to a **faction** (player slot). The
shipped maps use the *multi-country* form:

```
OwnershipMap "Maps/EarthRRUltraV3.Virtual/V7_default.vec"
  MultiCountry "Maps/EarthRRUltraV3.Virtual/V7_segment_names.txt"
  Borders   "Maps/EarthRRUltraV3.Virtual/V7_split.bin"
  Ownership "Maps/EarthRRUltraV3.Virtual/V7_split.vec"
  Default   "Maps/EarthRRUltraV3.Virtual/V7_default.txt"

  Player "North America" Color "1188FF" Name "Blue" Portrait Index 15
    ModelPrefix "NA"
    Events FromFile "Maps/EarthRRUltraV3.Virtual/Events/North America.txt"
  Player "Central America" Color "FF9911" Name "Orange" Portrait Index 24
    …
```

| Part | Meaning |
|---|---|
| `OwnershipMap "file.vec"` | Faction borders for the default assignment (generated, with `.vec.cmap`). |
| `MultiCountry "names.txt"` | Region list (below). |
| `Borders "split.bin"` | The border segments (generated). |
| `Ownership "split.vec"` | The territory of each region (generated). |
| `Default "default.txt"` | Which faction owns each region at the start (below). |
| `GDPInfo "file"` | Optional; read and kept but not used. |
| `Player …` | One block per faction, at most 10, in slot order (slot 0 is the first `Player`). |

### Region list (`V7_segment_names.txt`)

One line per region, then `END`:

```
"Alaska" Production 0.04286 Science 0.02190 Espionage 0.08403 0
"Ecuador" Production 0.083624 Science 0.115385 Espionage 0.037879 27 28
```

* `"Name"` — region name (also used in the default file, events and the UI).
* `Production p Science s Espionage e` — the region's share of its faction's economy in each field; within
  one faction the shares normally add up to 1. `GDP g` sets all three to *g*.
* Then the numbers of the border segments (from `Borders`) that make up the region. A region with no
  segment numbers is dropped.

### Default assignment (`V7_default.txt`)

```
"Alaska" 0
"Northwest Mexico" 1
…
VARIANT "Cold War"
RENAME "Ukraine" "Ukrainian SSR"
  "Ukraine" 4
  …
END
```

| Line | Meaning |
|---|---|
| `"Region" faction [Original n] [OccupiedSince tick] [OccupationBitscale b] [highlight colour]` | Owner at the start (faction slot, 0-based). `Original` sets a different original owner (an occupied region). `highlight` draws the region with an extra colour. Names are matched ignoring case; regions not listed have no owner. |
| `RENAME "Region" "Display name"` | Shows the region under another name. |
| `VARIANT "Name"` | Starts an alternative start-up assignment (with its own `RENAME`s and region lines) that can be picked in the lobby. The lines before the first `VARIANT` are the default. |
| `END` | End of file. |

### `Player` block

The faction's name is the quoted string after `Player`; it is what `DefaultEnemy`, `AIConfig.txt` (`for
"faction"`) and event scripts refer to (exact match). Properties may follow in any order:

| Property | Meaning |
|---|---|
| `Color "RRGGBB[AA]" [Name "colour name"]` | Faction colour and the name of the colour shown in the lobby. |
| `ColorRemap n` | Colour slot to use instead of the faction's own. |
| `Portrait Index n` / `Portrait "image"` | Leader portrait (built-in index or a picture). |
| `Icon Index n` / `Icon "image"` | Faction icon. |
| `ModelPrefix "XX"` | Faction-specific unit pictures and models: every picture or model is looked for first under the folder `XX/` (e.g. `NA/Units/…`), then at its normal path. The prefix must be listed in `model_info.txt` ([12 — Other configuration files](12-Config-Files.md)). |
| `Events FromFile "file"` | The faction's event script (missions, AI behaviour scripts) — see the event-scripting reference. `Events` followed directly by script blocks embeds the script. |
| `Achievement ACH_…` | Steam achievement for winning with this faction (official maps only). |
| `Active Yes/No` | The slot is in play. |
| `AI Yes/No [Suspended]` | Computer player. |
| `NoSurrender Yes/No` / `NoSurrender manual` | Never surrender automatically while it has active units / surrender only by player command. |
| `TechLevel f` | Starting tech level of this faction. |
| `tech "id" available` / `tech "id" points` | A technology known at start, or research points already invested. |
| `AvailableUnits ut …`, `AvailableMissiles mt …` | This faction's own starting deployment (same syntax as §6). |
| `ProductionBoost f`, `ScienceBoost f`, `EspionageBoost f` | Economy multipliers for this faction. |
| `MTSwitchOverride "unit" "missile"` | Default weapon for that unit type. |

Further `Player` properties (diplomacy, research state, statistics) are written by saved games; see §11.

### Simple ownership picture

Instead of `MultiCountry`, a map can take faction territories straight from a picture painted in the
`Player` colours:

```
OwnershipMap "Maps/MyMap.virtual/ownership.vec"
  Player "North" Color "1188FF"
  Player "South" Color "FF0011"
  Generate from "Maps/MyMap.virtual/SRC/owners.png" [smooth 36000] [filter 25000]
```

Paint with a hard (non-antialiased) brush using exactly the `Player` colours; every area must touch its
neighbours along pixel edges, not only at corners; a stray pixel or one touching only at a corner can crash
the run. If it does, put all but one `Player` behind `//` and add them back one at a time to find the colour at
fault. Run the map once to generate the `.vec` (it goes into *Documents*, as the masks of §3), then remove the
`Generate` line. Each faction is then one region. This works in the normal game too.

---

## 5. Cities

```
Cities
  ModelsPath "Maps/EarthRRUltraV3.Virtual/CityModels"
  MaxPerPlayer 500  FromFile "Maps/EarthRRUltraV3.Virtual/earth_cities.csv"

relocate "Maps/EarthRRUltraV3.Virtual/earth_cities.reloc.txt"

rename "Bombay" "Mumbai"
rename "Kiev" "Kyiv"
```

`relocate` and the `rename` lines are part of the `Cities` entry: they must follow it directly.

| Keyword | Meaning | Default |
|---|---|---|
| `ModelsPath "folder" [Generate]`, repeatable | Folders searched for the 3D city models `<City name>.bin`. `Generate` creates missing models. | `Units/Images/City` |
| `MaxPerPlayer n` | Upper limit of cities per faction. Over the limit, of the two closest cities of a faction the smaller is removed, until the limit is met. | no limit |
| `FromFile "file.csv" [Generate From "source.csv"]` | City list (below). With `Generate From`, the source list is read and the final list (after relocation) is written to the first file. Without `FromFile`, the list follows inline, ending with `END`. | — |
| `relocate "file" [generate]` | Moves cities to adjusted positions (below). With `generate`, cities on water are moved inside the land and the result is written to the file. | — |
| `rename "CSV name" "Display name"` | Shows a city under another name; matched exactly. | — |
| `SetTotalInitialPopulation "faction" n …` | One value per faction, in slot order: the population used as each faction's 100 %. | sum of its cities |

Cities on neutral ground and cities of inactive factions are removed at start. A city belongs to the faction
that owns the region it stands in.

### City list (`earth_cities.csv`)

Semicolon-separated, one city per line:

```
Absolute
Albuquerque;916528;0.203801;0.305030
Atlanta; 4975300 ;0.265594;0.312479
```

* First line `Absolute` (or `Absolute;;;`): coordinates are map coordinates `x;y`. Without it, the two
  fields are geographic: `DD MM SS N|S;DDD MM SS E|W`.
* `Name;population;x;y`. Population is people.
* Optional `WithInitial` line after `Absolute`: each line starts with the initial population
  (`initial;Name;population;x;y`) — used by saved games.
* Optional per-city lines after a city: `Images "folder"` (custom city pictures; default
  `Units/Images/City/<Name>`).
* `END` (or `END;;;`) ends the list.

### Relocation file (`earth_cities.reloc.txt`)

```
reloc "Virginia Beach" 0.288773 0.295201
```

`reloc "Name" x y` — new position (map coordinates) of the named city (exact name from the CSV).

---

## 6. Starting setup and AI

```
Default AvailableUnits
  ut "Fighter" 10
  ut "Army_Division" 10
Default AvailableMissiles
  mt "Low-power nuclear bomb" 10
AvailablePoints -1

AICache "Maps/EarthRRUltraV3.Virtual/ai_cache_new.bin"
DefaultEnemy "North America" "Russia"

MIN_POSITIONING_DISTANCE 50
BOARD_TOLERANCE 120
HOST_TOLERANCE 20
```

### Starting forces and technologies

| Keyword | Meaning |
|---|---|
| `Default AvailableUnits` + `ut "Unit_ID" n [at tick]` lines | Units every faction starts with (to deploy). `at` sets when they were added (auto-deployment counts from it). |
| `Default AvailableMissiles` + `mt "missile_id" n [extra launchers delay autouse]` lines | Starting missile stock. |
| `Default AvailableTechnologies` + `tech "id"` lines | Technologies every faction knows at start. |
| `Default DisabledTechnologies` + `tech "id"` lines | Technologies that cannot be researched on this map (lobby default). |
| `Default TechLevel f` | Starting tech level. |
| `AvailablePoints n` | Points for buying the starting setup. `-1` = calculated from the default units, missiles and technologies; a larger value adds the difference as extra points. |
| `LimitedEscalationDisabledMissiles "missile" …` | Weapons blocked during the limited-escalation period (lobby default). |
| `DisabledForAIMissiles "missile" bits …` | Weapons the computer factions whose bits are set (bit 0 = slot 0) do not use. |

Each `Default` line starts one list; several `Default` lines may follow each other.

### AI

| Keyword | Meaning |
|---|---|
| `AICache "file.bin" [generate from "AIConfig.txt"]` | Precomputed AI positioning data (good places for silos, airbases, radars…). Regenerate when regions or city positions change. Generating takes a long time. |
| `DefaultEnemy "faction" "faction"` | The first faction prefers the second as its enemy. Repeatable. `DefaultAlly` is accepted but has no effect. |
| `AIDisabled` | No computer players on this map. |
| `MIN_POSITIONING_DISTANCE km` | Minimal distance between units the AI places next to each other. Default 100. |
| `BOARD_TOLERANCE`, `HOST_TOLERANCE` | How close the AI brings units to a transport or landing point / to the point where it hands them over. Defaults 200 and 25. `BOARD_TOLERANCE` is also the boarding distance used when generating `LandingPairs`. `AIR_BOARD_TOLERANCE` and `GROUND_BOARD_TOLERANCE` are accepted but have no effect. |
| `MIN_SHORE_DIST n`, `MIN_BORDER_DIST n`, `SHORE_VERTICAL_SHIFT n`, `BORDER_VERTICAL_SHIFT n` | Spacing of placement points from shores and borders, in tenths of a km. Defaults 3, 7, 0, 0. |

### `AIConfig.txt` (input for `AICache … generate`)

```
MAX_THREADS 12
MIN_POSITIONING_DISTANCE 30
SHORE_DIST 16          // tenths of a km
MAX Default 10
MAX SubmarineAttack 15
dist 10000 min 4000 for MissileSilo
dist 120 min 50 for CityControl
END
```

| Line | Meaning |
|---|---|
| `MAX_THREADS n` | Threads used for the calculation. |
| `MIN_AI_LAND_POINTS n`, `MIN_AI_SEA_POINTS n`, `MIN_AI_SHORE_POINTS n` | Minimum number of points of each kind per region. |
| `MIN_POSITIONING_DISTANCE km` | As in the map file, for the calculation. |
| `MISSILE_DEFENCE_DIST km`, `SATELLITE_RANGE km` | Ranges assumed for missile defence and satellites. |
| `BORDER_DIST`, `WIDE_BORDER_DIST`, `WIDE_BORDER_MIN_DIST` (`< WIDE_BORDER_DIST`) | Border-zone widths. |
| `SHORE_DIST`, `INLAND_SHORE_DIST` | Shore-zone widths, in tenths of a km. |
| `WATER_SEGMENT n` | Which sea is the open ocean (`-1` = the largest). |
| `MAX <PointType> n` / `MAX <PointType> for "faction" n …` / `MAX Default n` | Maximum number of points of a type (per faction). Default 60. |
| `dist km [min km] for <PointType> [for <PointType>…]` | Distance bands for which point values are precomputed (reach to the enemy, cities…). |

Point types are those of the AI group placements ([08 — AI §7](08-AI.md#7-groupsconquesttxt--group-compositions)):
`MissileSilo`, `CityDefence`, `Radar`, `OverHorizonRadar`, `Airbase`, `SubmarineAttack`, `SubmarineHide`,
`CarrierAttack`, `MobileMissile`, `ObjectDefence`, `NavalBase`, `Orbit`, `Shore`, `CityControl`,
`BorderDefence`, `MarinesLanding`, `AirborneTroopsLanding`, `TroopsTraining`, `Industry`. `ObjectDefence` and
`Orbit` points are created automatically.

---

## 7. Game rules (lobby defaults)

These values become the defaults of the game-setup screen for this map; the host can still change them.

| Keyword | Meaning | Default |
|---|---|---|
| `ScoringMode n` | `2398` default, `2399` survival, `2400` genocide, `3361` conquest. | 2398 |
| `PeaceTimer ticks` | Time from the start with no attacks at all. | 0 |
| `NoNukesTimer ticks` | Time from the start without nuclear weapons. | 0 |
| `PeaceTimerAddedNum n`, `NoNukeTimerAddedNum n` | How many times players may extend these timers. | 0 |
| `CeasefireTimeout ticks` | Minimum duration of a ceasefire. | 36000 (10 game minutes) |
| `PeaceTreatyTimeout ticks` | Minimum duration of a peace treaty. | 90000 (25 game minutes) |
| `MinPartnershipTimeToPermanentAlliance ticks` | Partnership time before an alliance can become permanent. | 432000 (2 game hours) |
| `TimeToAutoDeploy ticks` | Undeployed starting units are deployed automatically after this time. | 54000 |
| `TimeToFullProductionAfterOccupation ticks` | An occupied region reaches full production after this time. | 36000 |
| `TimeToFinish ticks` | Length of the end-of-game countdown. | 72000 |
| `CountdownTrigger f` | Global pollution level that starts the end-game countdown (`TimeToFinish`). | 0.5 |
| `OccupationThreshold f` | Share of a region's city population that must be occupied to take over the region; 0.5 or less turns region capture off. | 1.0 |
| `RegionDestructionThreshold f` | A region whose population falls below this share of its initial population is destroyed; 0 = off. | 0 |
| `AutoSurrenderThreshold f` | A faction surrenders when its population falls below this share. | 0.15 |
| `PollutionSpeedCoeff f` | Speed at which radioactive contamination builds up. | 1.0 |
| `GlobalProductionBoost f`, `GlobalScienceBoost f`, `GlobalEspionageBoost f` | Economy multipliers for everyone. | 1.0 |
| `ProductionDegradesWithLosses Yes/No` | Production falls with population losses. | Yes |
| `LimitedProductionBenefitFromExpansion Yes/No` | Captured regions add less production. | Yes |
| `AllowAlliances Yes/No` | Alliances allowed. | Yes |
| `AllowInstantTechSharing Yes/No` | Allies may share research instantly. | Yes |
| `GenevaRequiresConsensus Yes/No` | Geneva Convention votes must be unanimous. | No |
| `AggressiveAISettings Yes/No` | Computer players invade without first completing their defence and research plans. | No |
| `PredefinedTeams Yes/No` | Factions start allied in the teams set in the lobby. | No |
| `AllowBuildingOnAlliedTerritory Yes/No` | Units may be deployed on allied territory. | Yes |
| `AutoSlowDownAllowed Yes/No` | In single player, the game speed drops to at most ×3 while nuclear missiles are in the air. | Yes |
| `DisableMaxRangeOptimization Yes/No` | Recalculate every unit's attack range every tick instead of periodically (slower). | No |
| `UseIntermediatePointForInvasion Yes/No` | Invasions gather at an intermediate point first. | — |
| `NoPlayerGameSpeed n` | Game speed when no human player is left. | 3 |
| `MinKilledToReport n` | Smallest number of casualties reported in the event log. | 100 |
| `ScoreByKillCoeff`, `ScoreByLossCoeff`, `ScoreByPollutionCoeff`, `ScoreByOccupationCoeff`, `ScoreByTerritoryLossCoeff` | Weights of the score components. | 1.0 |
| `ScenarioTotalScore n` | Score to reach in a scenario. | 0 |

---

## 8. Display settings

| Keyword | Meaning | Default |
|---|---|---|
| `UIToUse "UI/UI.txt"` | Interface layout file. | the game's |
| `SpecularHighlight Yes/No`, `SpecularColor c` | Specular light on the globe. | — |
| `UseAtmoGlow Yes/No`, `AtmoGlow c` | Atmosphere glow and its colour. | — |
| `OwnershipOverlayAlpha n` | Opacity (0–255) of the faction-colour overlay. | 50 |
| `MapContrastAdjustment n` | Contrast of the map texture. | 30 |
| `DrawInternalBorders f` | Strength of borders between regions (0–2; 1 = faint). | 1.0 |
| `DynamicBorderScaling f` | 0–1: border width follows zoom. | 0 |
| `DrawOverlayType n` (`DrawTerrainTypeOverlay n`) | Overlay shown at start. | ownership |
| `DrawOwnershipOverlay n` | Bit mask of factions whose territory is coloured. | all |
| `DrawRadarCoverage Yes/No`, `DrawRadarCoverageForAllies Yes/No`, `CoverageBitScale n` | Radar coverage display. | off |
| `DrawPollution Yes/No` | Show contamination. | — |
| `UnitsInPlayerColor Yes/No` | Tint units in faction colour. | No |
| `UnitScaling f`, `CityScaling f`, `ExplosionScaling f`, `OrdersScaling f` | Size of unit icons, cities, explosions and order markers. | 0.75, 1, 1, 1 |
| `UnitMips Yes/No` | Mip-mapping for unit pictures. | No |
| `MinDiscolorZoom f`, `MaxDiscolorZoom f` | Zoom range over which the map texture desaturates. | — |
| `DrawZoomHelper Yes/No`, `StartHelperZoom f`, `MinHelperTransparency f`, `FullHelperZoomTime ticks`, `HelperColor c` | The "zoom helper" outlines drawn when zoomed out. | on |
| `MinUnitZoom f`, `MaxUnitZoom f`, `MinExplosionZoom f`, `MaxExplosionZoom f` | Zoom range in which units / explosions are drawn. | all |
| `ZoomFadeLimit f`, `ZoomFadePower f`, `ZoomFadePowerExtra f` | How icons fade with zoom. | 10, 0.5, 0.75 |
| ★ `ModelZoomFadeLimit f`, `ModelZoomFadePower f` | The units' 3D models grow with the map up to the zoom `ModelZoomFadeLimit`, then slower, as `MapScale^ModelZoomFadePower`: zoomed in they get smaller compared to the map (closer to the real scale), never smaller than at that zoom. The ordinary explosions and the spots where hits are drawn on the models shrink with them. `ModelZoomFadePower 1`: as the map. | 10, 0.65 |
| `GlobeView Yes/No` | Start in globe view. | No |
| `MapScale f`, `MapShiftX f`, `MapShiftY f`, `MapShiftXRel f`, `MapShiftYRel f` | Initial zoom and position. | — |

---

## 9. Building the border and region files: `ProcessBorders`

The region files of §4 are made by the steps of `ProcessBorders`. Each step runs when the map is loaded, in the
[Cheats build](10-Cheats-Build.md) only (the normal game reads the lines and does nothing). Put one step at a
time in (remove its `//`), run the map, quit, put it back behind `//` and go on with the next:
[§10](#10-making-a-new-map-step-by-step-cheats-build) walks through them.

```
ProcessBorders
//ReadSVG "Maps/MyMap.virtual/SRC/borders.svg" Generate "Maps/MyMap.virtual/SRC/V7_split.txt" SaveEdited "Maps/MyMap.virtual/SRC/V7_split_mod.txt"
//EditPoints "Maps/MyMap.virtual/SRC/V7_split.txt" SaveEdited "Maps/MyMap.virtual/SRC/V7_split_mod.txt"
//GenerateSplit Load "Maps/MyMap.virtual/SRC/V7_split.txt" Generate "Maps/MyMap.virtual/SRC/V7_split.bin" Names "Maps/MyMap.virtual/SRC/V7_segment_names.txt"
//GenerateOwnership LoadBin "Maps/MyMap.virtual/SRC/V7_split.bin" GenerateDimmable LoadNames "Maps/MyMap.virtual/SRC/V7_segment_names.txt" SaveDefaults "Maps/MyMap.virtual/SRC/V7_default" Generate "Maps/MyMap.virtual/SRC/V7_split.vec"
//GenerateDefaults Names "Maps/MyMap.virtual/V7_default.txt" Vec "Maps/MyMap.virtual/V7_default.vec"
```

`ProcessBorders` must come after the `OwnershipMap` block (with its `Player` lines), and that block must load:
until your own region files exist, leave it pointing at Earth's.

| Step | Does |
|---|---|
| `ReadSVG "drawing.svg" Generate "graph.txt" [SaveEdited "graph_mod.txt"]` | Optional. Reads a drawing of the borders (each path a line, curves sampled, colours ignored), joins the points that lie on each other into a graph, writes it to `Generate` at once and opens the border editor on it. The drawing's coordinates are taken as map coordinates, so it must be drawn 1 × 1 units (x and y from 0 to 1). |
| `EditPoints "graph.txt" [SaveEdited "graph_mod.txt"]` | The border editor (below). Saves to `SaveEdited`, else to the file itself. |
| `GenerateSplit Load "graph.txt" Generate "split.bin" Names "names.txt" [SplitCenterPoints "file"]` | Naming the regions (below): each click inside a closed area makes it the next region and writes `split.bin`, the names file and the centre points (`<split.bin>.points.txt`, or `SplitCenterPoints`). |
| `GenerateOwnership LoadBin "split.bin" [GenerateDimmable] LoadNames "names.txt" SaveDefaults "base" Generate "regions.vec" [MAP_SIZE 4096]` | Builds the regions' territories (`regions.vec`, the `Ownership` file of §4), writes `base.txt` (every region with a **random** owner among the `Player`s, to edit) and `base.vec` with its `.vec.cmap` (the `OwnershipMap` file). `GenerateDimmable` adds to `split.bin` which border lines lie inside one faction (drawn faintly) — needed by `ConditionalWaterMap`: always use it. `MAP_SIZE` is the grid size (power of 2). |
| `GenerateDefaults Names "default.txt" Vec "default.vec"` | Writes the region owners as they are when the game starts into `default.txt`, and the faction borders for them into `default.vec` (`.vec.cmap`). |

Every step writes into *Documents/My Games/ICBM-Escalation* under the path given, as the masks of §3 do; move the
files into your mod.

### The border editor (`EditPoints`)

The borders are a graph of points and straight lines on the battle map. A point snaps to an existing one within
1/4096 of the map.

| Action | Does |
|---|---|
| Left click on empty space | puts a point there and starts a line from it (or goes on with the line being drawn) |
| Left click on an existing point | starts the line there, or ends the line being drawn on it |
| Left click on the line's own first point | closes it |
| Left click on an existing line | puts a point into it and ends the line being drawn there |
| Right click | deletes the one line (between two points) nearest the cursor; points left without lines go. Does nothing while a line is being drawn. |

The point or line the cursor would snap to is marked: green while a line is being drawn, red otherwise. A line is
saved when it is ended and after each deletion; a line still being drawn is not. There is no undo (back the file
up now and then) and no end: quit the game when done.

Rules for the borders: every region must be a closed area — no loose ends, no lines crossing (join them at a
point instead), no area wholly inside another. Regions cover land and the sea near it as you draw them; the
coasts come from the water masks, so a border may run out into the sea.

### Naming the regions (`GenerateSplit`)

The game does not know which area is which region until you click them. The cursor shows the name of the next
region; a left click inside a closed area makes it that region. The first click is region 0 and takes the first
line of the names file, the next region 1 and the second line, and so on. A click with no line left adds `"Segment
N"` to the names file (with Production, Science and Espionage 1).

Prepare the names file beforehand to have the right names shown as you click — one line per region, numbered
from 0 in the order you will click them:

```
"Alaska" GDP 1.0 0
"Canada" GDP 1.0 1
"Greenland" GDP 1.0 2
END
```

Each click also rewrites `split.bin` and the centre points file. When the map is loaded again the clicks are
replayed from that file, so the work can be resumed in a later run, and after a border change (a new graph from
`EditPoints`) the same clicks name the regions again. There is no undo: to take a click back, quit, delete its
line (the last) from the centre points file and run again.

### File formats

* **Graph** (`V7_split.txt`): `P x y` lines (points in map coordinates, numbered from 0 in order), then for each
  point `FOR n` followed by `E m length` lines (a line to point *m*; the length is not checked). A point without
  lines is dropped. The smallest useful graph, a square in the middle of the map to start drawing from:

  ```
  P 0.5 0.5
  P 0.6 0.5
  P 0.6 0.6
  P 0.5 0.6
  FOR 0
    E 1 0.1
  FOR 1
    E 2 0.1
  FOR 2
    E 3 0.1
  FOR 3
    E 0 0.1
  ```
* **Centre points** (`V7_split.bin.points.txt`): `Point x y` per region, in click order (a `// comment` with the
  region name is allowed).
* **Names** (`V7_segment_names.txt`, the `MultiCountry` file of §4): one line per region,
  `"Name" GDP g n …` or `"Name" Production p Science s Espionage e n …`. The numbers after the shares are the
  areas (in click order, from 0) that make the region: a region of several areas — an island group — lists them
  all (`"Ecuador" … 27 28`). Keep them in rising order. `GenerateSplit` writes the long form.
* **Defaults** (`V7_default.txt`): §4. `GenerateDefaults` writes plain `"Region" faction` lines only: add
  `RENAME`, `VARIANT` and the other options afterwards, and never run it on a file that has them.

## 10. Making a new map, step by step (Cheats build)

A new map of the Earth with your own regions, factions and cities, made with the
[Cheats build](10-Cheats-Build.md) on top of Earth's map: its texture (`TextureMap "Maps/EARTH256K"`), height map
and terrain types stay as they are. The shipped map file carries the same steps as comments.

**How a step runs.** Each step is a line of the map file put in (its `//` removed) for one run: start the game,
pick the map in the new-game screen, start it, check the result, quit. Generated files go to
*Documents/My Games/ICBM-Escalation* under the path the line names (ICBM.CFG's `DataPath` instead when it is
set). After each step move them into your mod's folder at the same path, delete what is left in *Documents* (it
would hide your mod's files) and put the line behind `//` again. Do one step per run, in this order: each needs
the files of the ones before it.

Want only new factions on Earth's regions? Do steps 1, 6, 9 and 10 (the `Player` blocks, who owns each region,
the AI cache, the setup); Earth's borders, cities and masks stay.

### Step 1. Your copy of Earth's map

1. Make a mod (a folder under the game's `MODS/` with an `info.txt`, [12 §2](12-Config-Files.md#2-mods-infotxt))
   with a `Maps/` folder.
2. Copy the game's `Maps/EarthRRUltra.txt` to `MODS/<mod>/Maps/MyMap.txt` and the folder
   `Maps/EarthRRUltraV3.virtual` to `MODS/<mod>/Maps/MyMap.virtual`.
3. In `MyMap.txt`, replace every `Maps/EarthRRUltraV3.virtual/` (in any case) by `Maps/MyMap.virtual/`; leave
   `Maps/EARTH256K` and `Maps/Events` alone. Change the `Name` and `Description` lines (§2): the map is listed
   under its first `Name`.
4. Enable the mod and check that the map appears in the map list and starts.

### Step 2. Water and land masks (optional)

Earth's coasts need no change for a map of the Earth: skip this step unless you want to change the sea (a new
canal, a strait closed). A changed mask means every later step must be made again.

1. **Edit the outlines.** Put the `EditSVG` lines in (§3), e.g.

   ```
   EditSVG "Maps/MyMap.virtual/Src/test_16K.svg" Save "Maps/MyMap.virtual/Src/test_16K.svg"
           Second "Maps/MyMap.virtual/Src/test_16K_ice.svg" Save "Maps/MyMap.virtual/Src/test_16K_ice.svg"
           Mask WaterMapLand
   ```

   for the sea maps, or `EditSVG "…/test_16K_land.svg" … Mask WaterMap` for the land map. Edit, press **R**,
   quit. The drawings are saved in *Documents* with their `.view.svg`.
2. **Export the pictures.** Open each changed `.view.svg` in Inkscape and export it as PNG at the drawing's own size
   to `<name>.svg.view.png` beside it.
3. **Generate the masks.** Put the `Generate from …` lines of `WaterMap`, `WaterMapNoIce` and `WaterMapLand` in (the
   shipped file has them, with `water black`), run, check the overlay, quit. Move the drawings, the pictures and
   the new `.vec` and `.vec.cmap` files into the mod.

### Step 3. Draw the region borders

Put `ProcessBorders` and its `EditPoints` line in (§9):

```
ProcessBorders
  EditPoints "Maps/MyMap.virtual/SRC/V7_split.txt" SaveEdited "Maps/MyMap.virtual/SRC/V7_split_mod.txt"
```

Start from Earth's own border graph (`SRC/V7_split.txt`, the line above) to change its regions, or from the
small square of §9's *File formats* in a new `V7_split.txt` to draw all of them yourself. (With a drawing of the
borders made 1 × 1 units, `ReadSVG` makes the graph from it instead.) Keep the `OwnershipMap` block as it is:
Earth's region files load until yours replace them in step 5.

Draw the borders with the editor (§9): every region one closed area, no loose ends, no crossings. Each finished
line is saved in `V7_split_mod.txt` (in *Documents*). Quit when done, copy it into the mod's `SRC/` as
`V7_split.txt` (keep the old one as a backup) and put `EditPoints` behind `//`.

### Step 4. Name the regions

1. Optionally write `SRC/V7_segment_names.txt` beforehand: your region names in the order you will click them
   (§9). Earth's file has Earth's 150 names and its own order: replace it when the regions are new.
2. Empty or delete `SRC/V7_split.bin.points.txt`, or the game replays Earth's clicks.
3. Put the `GenerateSplit` line in, run, and click inside each region in turn: the cursor names the next one.
   The work is saved after every click; a later run goes on where you left off.
4. Quit. Move `V7_split.bin`, `V7_split.bin.points.txt` and `V7_segment_names.txt` into the mod's `SRC/`. Put
   `GenerateSplit` behind `//`.
5. In `V7_segment_names.txt`, join regions that should be one (list their numbers on one line, delete the other
   lines) and set the economy: each region's `Production`, `Science` and `Espionage` are its shares of its
   faction's, adding up to 1 within a faction (§4). They can be changed at any time later without making anything
   again.

### Step 5. Build the regions

1. Put the `GenerateOwnership` line in, with `GenerateDimmable`:

   ```
   GenerateOwnership LoadBin "Maps/MyMap.virtual/SRC/V7_split.bin" GenerateDimmable LoadNames "Maps/MyMap.virtual/SRC/V7_segment_names.txt" SaveDefaults "Maps/MyMap.virtual/SRC/V7_default" Generate "Maps/MyMap.virtual/SRC/V7_split.vec"
   ```

   Run and quit. It writes `V7_split.vec` (`.vec.cmap`), `V7_default.txt` (random owners), `V7_default.vec`
   (`.vec.cmap`) and a new `V7_split.bin`.
2. Move them into the mod: `MyMap.virtual/V7_split.bin`, `V7_split.vec` (with its `.vec.cmap`),
   `V7_default.vec` (with its `.vec.cmap`) and `V7_default.txt`, and `SRC/V7_segment_names.txt` to
   `MyMap.virtual/V7_segment_names.txt`. Put `GenerateOwnership` and `ProcessBorders` behind `//`.
3. The `OwnershipMap` block now names your files (the paths of step 1):

   ```
   OwnershipMap "Maps/MyMap.virtual/V7_default.vec"
     MultiCountry "Maps/MyMap.virtual/V7_segment_names.txt"
     Borders "Maps/MyMap.virtual/V7_split.bin"
     Ownership "Maps/MyMap.virtual/V7_split.vec"
     Default "Maps/MyMap.virtual/V7_default.txt"
   ```

   Start the map: your regions are drawn, with random owners.

### Step 6. Factions and who owns each region

1. **The factions** are the `Player` lines of the `OwnershipMap` block (§4), at most 10: their names, colours,
   portraits and `Events FromFile` scripts (Earth's scripts fit any faction: they use the common AI script). A
   faction's name is what `DefaultEnemy`, `AIConfig.txt` and event scripts refer to.
2. **The owners and the faction borders.** Put `ProcessBorders` and its `GenerateDefaults` line in (§9). Then
   either write `V7_default.txt` by hand — `"Region" faction` per region, the faction a `Player`'s number from 0
   (§4) — and start the map, or pick the map in the new-game screen, give the regions to the factions there as
   they should start, and start the game. Either way the game writes the owners it started with to
   `V7_default.txt` and the faction borders for them to `V7_default.vec` (`.vec.cmap`). Move them into the mod and
   put the lines behind `//`. Do it again whenever the owners change.
3. `RENAME` and `VARIANT` sections go into `V7_default.txt` only after this: `GenerateDefaults` drops them.

### Step 7. Cities

A city belongs to the faction whose region it stands in; cities on nobody's land go at the start. Earth's list
(`earth_cities.csv`) works for any regions: `MaxPerPlayer` limits the cities per faction.

* **Your own list:** write it in the CSV format of §5 (geographic or `Absolute` coordinates) as `SRC/cities.csv`
  and read it with `FromFile "Maps/MyMap.virtual/cities.csv" Generate From "Maps/MyMap.virtual/SRC/cities.csv"`:
  the game writes the final list to the first file.
* **Cities on the coast:** `relocate "Maps/MyMap.virtual/cities.reloc.txt" generate` moves cities lying on water
  into the land and writes their new places (§5).
* **City models:** a city whose name is not Earth's has no 3D model. `ModelsPath
  "Maps/MyMap.virtual/CityModels" generate` makes the missing ones.

The three can run together; move the files into the mod and put the `generate` options behind `//`. Use `rename`
lines for names shown differently.

### Step 8. Ground paths and landings

Put in `generate` after both lines and run once:

```
ConditionalWaterMap "Maps/MyMap.virtual/Conditional.bin" generate
LandingPairs "Maps/MyMap.virtual/landing_pairs.bin" generate
```

`ConditionalWaterMap` is the land units' paths across the regions' borders (it needs the `GenerateDimmable`
`V7_split.bin` of step 5); `LandingPairs` the points where troops embark and land (they need the cities). Move
both files into the mod.

### Step 9. The AI cache

1. Edit `SRC/AIConfig.txt` (§6): any line naming a faction (`for "North America"`) must name one of yours, or go.
2. Put in `AICache "Maps/MyMap.virtual/ai_cache_new.bin" generate from "Maps/MyMap.virtual/SRC/AIConfig.txt"`
   and run. It takes a long time. Move the file into the mod.
3. Check it: in the Cheats build **Ctrl + 0 … 9** and **Alt + 0 … 8** show the AI's places of each kind
   ([10 §1](10-Cheats-Build.md#1-key-combinations)).

### Step 10. Setup

`DefaultEnemy` pairs with your factions' names (delete Earth's), starting units and technologies (§6), lobby
defaults (§7), display settings (§8). Play a game against the computer.

### Step 11. Publish

Put every `generate`, `EditSVG` and `ProcessBorders` line behind `//`. Delete your map's files from
*Documents/My Games/ICBM-Escalation/Maps* and play the map from the mod alone once. The mod needs `MyMap.txt` and
`MyMap.virtual/` with the masks, the region files, the cities, `Conditional.bin`, `landing_pairs.bin`, the AI
cache, the city models and the events; `SRC/` holds only sources.

### What to make again after a change

| You changed | Make again |
|---|---|
| The masks (step 2) | everything from step 3: borders near the coasts, regions, cities on the coast, paths, landings, AI cache |
| Borders (step 3) | steps 4 (the saved clicks replay; click any new region), 5, 6 (owners and faction borders), 8, 9 |
| Owners only | step 6 (`GenerateDefaults`) |
| Region names, economy | nothing |
| Cities | city models, landing pairs, AI cache |
| Faction names | `AIConfig.txt`, `DefaultEnemy`, event scripts naming them; the AI cache if `AIConfig.txt` names factions |

## 11. Making a map from a saved game

A saved game is a map file with the game state appended, so any position — borders changed by a war,
technologies researched, armies deployed — can become a new map that starts from that position. The
quickest way uses the [Cheats build](10-Cheats-Build.md):

1. **Set up the position.** Start a single-player game on an existing map. Use the cheats to prepare each
   faction: research with **Shift + T**, build with **Ctrl + click**, place units (hold **Ctrl** to deploy
   anywhere, **Ctrl + T** to move a unit), give regions away with **Ctrl + O**, switch faction with
   **Shift + 0 … 9** ([10 §3](10-Cheats-Build.md#3-typical-workflow-setting-up-a-starting-position)).
2. **Save as a scenario**: hold **Shift** when confirming *Save*. The game writes
   `Documents/My Games/ICBM-Escalation/SAVES/SAVEn/world.txt` and `world.txt.remap.txt`.
3. **Copy both files** into your mod's `MAPS/` folder under the new map's name, keeping the pairing:
   `MAPS/MyMap.txt` and `MAPS/MyMap.txt.remap.txt`. The region owners are read from the file named like
   the map file plus `.remap.txt` (`Default AUTO_FROM_SAVE` in the `OwnershipMap` entry).
4. **Edit the header of `MyMap.txt`:**
   * Replace the first line `MAP Name ID …` with `MAP` and your `Name` lines, and check `Description`
     (§2). The map is listed only when `MAP` and `Name` come first.
   * Remove or fill in the `Events FromFile "Scenario/MY_SCENARIO_NAME/…"` placeholders in the `Player`
     blocks: a script file that does not exist stops loading.
   * Leave the commented-out `ScenarioInfo` template alone (or delete it); it is needed only for missions.
5. **Adjust the setup:** lobby defaults (§7), `Default AvailableUnits` for the starting deployment (§6),
   display settings (§8). Everything else — masks, regions, cities, AI cache — is shared with the original
   map and needs no regeneration as long as only owners, units and technologies changed.
6. Start the game: the new map appears in the map list and starts with the saved units in place.

A normal save (without Shift) can be used the same way, but it also carries the game clock (`Time …` at the
top — remove it, or the map is not listed), the mod list, AI plans, diplomacy, pollution and score; the
scenario save leaves all of that out.

---

## 12. Keys used by saved games and scenarios

Saved games and scenarios use the same file with more keys. Map authors do not need them; they are listed
so that the keywords in a saved file are recognisable:

| Keys | Hold |
|---|---|
| `GlobalPollution`, `TicksWithoutWarheads`, `TicksWithoutWarheadsForPlayer`, `NuclearWarningPlayed` | Global state. |
| `CameraFollowMeUnitUID` | Camera target. |
| `ScenarioInfo …` | Campaign and mission description — see the event-scripting reference. |
| `Alliance …`, `AIVoting …`, `BannedTechnologies tech "id" …` | Diplomacy and Geneva Convention state. |
| `Modifications mod x y type segment [wmap n] …` | Changes to the water masks made during the game. |
| `UnitFilter …`, `Highlights hl …` | UI state. |
| `Player` properties `APValue`, `SpyingOn`, `SpyPriority`, `NuclearEfficiency`, `DEFCONLevel`, `Construction`, `CurrentResearch`, `NextResearch`, `SpyTech`, `SpyUnit`, `DisassembledUnits`, `Relations`, `CeaseFire`, `PartnershipFrom`, `MyAlliance`, `Agreements`, `Reparations`, `Score`, `stats`, `History`, … | The faction's state. |
| City lines `stat`, `OccupiedSince`, `captured`, `OriginalOwner`, `InRangeOfCheckedMissile…` | City state. |
| `UID …` (after the map part) | Units, explosions, plans and the rest of the game state; the map part ends here. |

---

## 13. Map-specific mods

A map can bring its own mod: data changes that apply only while this map is played. The campaign missions
use one to adjust the economy or a few units for their story. A map for a special scenario can do the same
with any data file: units, technologies, explosions, AI files, `espionage.txt`, language files.

```
MAP
Name idx "Border Crisis"
MapSpecificMod "Maps/BorderCrisis.virtual/Mod"
…
```

`MapSpecificMod "folder"` names a mod folder, relative to the game folder, with an `info.txt` like any mod
([12 §2](12-Config-Files.md#2-mods-infotxt)) and files laid out like the game folder. The folder is looked
up like any file — first in *Documents/My Games/ICBM-Escalation*, then in the enabled mods, then in the game
folder — so it can live inside your own mod. A folder without a valid `info.txt` (`ICBM MOD "Name"`) is
skipped without a message.

**When it is active.** The mod is switched on when the map is loaded:

* when the map is picked in the game-setup screen;
* when the game starts;
* when a game saved on this map is loaded (the saved map part keeps the `MapSpecificMod` line).

It is switched off when another map is loaded or the game ends. It doesn't appear in the mod list, the
player can't turn it off, and it doesn't affect achievements. The map list itself (name, description,
preview) is read without it.

**Priority.** The map's mod is searched before everything else: before the game mode's mod
([12 §8](12-Config-Files.md#8-game-modes-blitz-standoff-conquest)) and before the player's enabled mods. Start
its files with `USE PREVIOUS` to change the current data rather than replace it, so that it works on top of
any game mode and mod:

```
// Maps/BorderCrisis.virtual/Mod/Tech.txt
USE PREVIOUS "tech.txt"
[TECHNOLOGY] "BORDER_CRISIS_ECONOMY"      // no Points, no parent: every faction has it (05)
  Name "BORDER_CRISIS_ECONOMY"
[END]

// Maps/BorderCrisis.virtual/Mod/Units/Units.txt
USE PREVIOUS "Units/units.txt"
[UNIT] "VirtualCity" MODIFY
  ImprovedBy "BORDER_CRISIS_ECONOMY" Production 2.0
[END]
```

This is the pattern of the main campaign's `Scenario/Main/GDP-Mod`. A zero-cost technology without
parents is known to every faction from the start ([05](05-Technologies.md#2-properties)), and the
modifier attached to it changes the value on this map only.

**`ForceLoading`.** Before a campaign mission starts, the screen where the player spends the mission's
starting points reads the map *without* its mod. Add `ForceLoading` to load the mod there too. You need it
when the starting setup or the point costs depend on units or technologies that only the mod defines (the
SNARE campaign uses it). A game saved on such a map keeps `MapSpecificMod` but not `ForceLoading`. If you
turn the save into a mission map, add it back.

**Multiplayer.** Every player needs the same map-mod files, just as they need the map itself; the game
compares the data before the game starts.

---

## 14. Pitfalls

* **Order at the start of the file.** `MAP`, then the `Name` lines, then `Description`, then `Restrictions`,
  or the map is not listed. Keep the remaining order of the shipped maps (§1).
* **`relocate` and `rename` belong to `Cities`** and must follow it directly; elsewhere they stop loading.
* **Names must match exactly**: faction names in `DefaultEnemy`, `AIConfig.txt` and events; city names in
  `rename` and the relocation file. Region names in the default file are matched ignoring case.
* **Regenerate the derived files** (`ConditionalWaterMap`, `LandingPairs`, AI cache) after changing regions
  or cities, or ground movement, landings and AI placement will not match the map.
* **Generated files in *Documents/My Games/ICBM-Escalation*** take priority over the mod's files of the same path.
  Delete them after moving the files into your mod.
* **A `generate` left in a published map** makes the normal game skip that file (§3).
* **At most 10 `Player` blocks.**
* An unknown word stops loading the rest of the map file (§1); check the line number in the message.
