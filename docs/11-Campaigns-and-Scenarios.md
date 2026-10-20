# 11 — Campaigns and scenarios

[Index](index.md) · [Maps](09-Maps.md) · [Cheats build](10-Cheats-Build.md)

*Companion to the Events Script Reference, covering the layer above individual event scripts: how a
campaign is assembled from missions, how a mission's win/lose conditions are declared, and how the
mission map itself is prepared.*

Contents

1. [Overview](#1-overview)
2. [The top-level SCENARIO file](#2-the-top-level-scenario-file)
3. [The map file's ScenarioInfo block](#3-the-map-files-scenarioinfo-block)
4. [Missions in event scripts](#4-missions-in-event-scripts)
5. [Chaining missions across a campaign](#5-chaining-missions-across-a-campaign)
6. [DLC campaigns and the virtual Scenario folder](#6-dlc-campaigns-and-the-virtual-scenario-folder)
7. [Preparing the mission map in the Cheats build](#7-preparing-the-mission-map-in-the-cheats-build)
8. [Mission-specific mods](#8-mission-specific-mods)
9. [Tutorial: a simple 3-mission campaign](#9-tutorial-a-simple-3-mission-campaign)

---

## 1. Overview

A **campaign** is one top-level `SCENARIO` file plus an ordered set of **missions**. Each mission is a
separate map file (`Scenario/<Campaign>/<Campaign>-N.txt`) with its own `ScenarioInfo` block and its own
per-faction event scripts (see *Where event scripts live* in the Events Script Reference).

Top-level campaigns:

* `Scenario/Main.txt` — the base game's main campaign, 11 missions (`Main-1.txt` … `Main-11.txt`).
* `Scenario/SNARE.txt` — a 5-mission campaign (`SNARE-1.txt` … `SNARE-5.txt`).
* Each DLC ships its own top-level `SCENARIO` file (`DLC_1.txt`, `DLC_2.txt`, `DLC_3.txt`), 11 missions
  each. See [§6](#6-dlc-campaigns-and-the-virtual-scenario-folder) for where these physically live.

A mission map is an ordinary map file ([09 — Maps](09-Maps.md)) that also carries the starting position —
units, technologies, borders — and a `ScenarioInfo` block. [§7](#7-preparing-the-mission-map-in-the-cheats-build)
shows how to make one.

---

## 2. The top-level SCENARIO file

```
SCENARIO
Name ID 6000
Description ID 6001
Image "Scenario/Main/Truman_and_MacArthur.jpeg"

MAP "Scenario/Main/Main-1.txt"
Image "Scenario/Main/Main-1.png"

MAP "Scenario/Main/Main-2.txt"
Image "Scenario/Main/Main-2.png"
...
```

* **`SCENARIO`** starts the file.
* **`Name ID`** / **`Description ID`**: the campaign's name and blurb (localised strings) as shown in the
  campaign-select menu.
* **`Image`**: the campaign's own banner/thumbnail.
* **`Faction N`** (optional): the faction pre-selected as the default playable faction when this campaign is
  chosen (`SNARE.txt` → `Faction 0`, `DLC_1.txt` → `Faction 1`, `DLC_3.txt` → `Faction 0`; `Main.txt` has
  none).
* **`MAP "path"` / `Image "path"`** pairs, one per mission, in campaign order: the mission's map file and
  its selection-screen thumbnail. This list sets the campaign menu's ordering and labels; the
  mission-to-mission chaining at run time is done inside each map file's `ScenarioInfo`
  ([§5](#5-chaining-missions-across-a-campaign)).

### String IDs and the LANG file

Every `Name ID`, `Description ID`, `Text ID` and `BriefingText ID` is a number, looked up in a `.lng` file
at run time. From DLC-3's string file, `UI.lng`:

```
// DLC will use the range from 7099 to 7600
USE Previous "LANG/Eng/UI.lng"

7099 LANG "The year is 1946...."
7100 LANG "DLC: Assassin's Mace"
7101 LANG "Assassin's Mace"
7102 LANG "After decades of chaos, China is ready..."
```

* **`USE Previous "path"`** chains this file to the base `.lng` file, so a DLC's strings extend rather than
  replace the base game's.
* Each entry is **`<ID> LANG "<text>"`** — a flat table from numeric ID to the localised string.
* A DLC reserves its own block of IDs so it cannot collide with the base game or another DLC (DLC-3 owns
  7099–7600).
* `DLC_3.txt`'s `Name ID 7101` / `Description ID 7102` resolve this way to the campaign's displayed name
  and blurb; `BriefingText ID` and every mission's `Text ID` work the same way.

---

## 3. The map file's ScenarioInfo block

Each mission's map file (e.g. `Scenario/Main/Main-1.txt`) has a `ScenarioInfo` block:

```
ScenarioInfo
 BriefingText ID 6004
 BriefingImage "Scenario/Main/Main-1/briefing.png"

Primary Mission "Territory"
  Text ID 6005
  Value 1
  ProductionPoints 150

Secondary Mission "NorthKorea"
  Text ID 6006
  Value 1
  ProductionPoints 200

ON Success
  Text ID 6008
  Image "Scenario/Main/Main-1/success.png"

ON Failure
  Text ID 6009
  Image "Scenario/Main/Main-1/failure.png"

EndGameCountdown 600
ResultFileName "Scenario/Main/Main-1.txt.result"
ProceedTo "Scenario/Main/Main-2.txt"
```

* **`BriefingText ID`** / **`BriefingImage`**: the text and image of the mission's briefing screen.
* **`Primary Mission "Name"`** / **`Secondary Mission "Name"`**: one mission slot. `"Name"` is the mission ID
  used from event scripts ([§4](#4-missions-in-event-scripts)). A map can declare several of each; the event
  scripts decide what winning each one means.
  * **`Text ID`**: the mission's description in the mission list during play.
  * **`Value`**: the target count of the mission's progress counter (driven by `Mission "Name" add …` /
    `SET …` from the event scripts). `Value 1` is a plain success/fail mission; `Value 5` (as in
    `Main-2.txt`'s "Missiles" mission) is a counted objective, e.g. "destroy 5 missiles".
  * **`ProductionPoints`**: the reward for completing the mission.
* **`ON Success`** / **`ON Failure`**: text and image of the end-of-mission screen.
* **`EndGameCountdown`**: how long the end-of-mission countdown runs before moving on (600 in Main-1, 1200
  in Main-2, 120 in Main-11).
* **`ResultFileName`**: where this mission's outcome is recorded (by convention the map file's path plus
  `.result`).
* **`ProceedTo`**: the next map file to load once this mission ends. Absent on the last mission.
* **`TransitionFileName`**: the *previous* mission's result file, read on this mission's start. Absent on
  the first mission.

**The campaign's last mission** additionally declares `ON FinalSuccess`, `ON FinalSuccess1` and
`ON FinalSuccess2` (each with its own `Text ID`/`Image`). They are not alternative endings: they are three
end-of-campaign screens shown one after another when the finale mission reaches the `Final_Success`
outcome ([§4](#4-missions-in-event-scripts)).

---

## 4. Missions in event scripts

A mission declared in `ScenarioInfo` is driven from the event scripts with the `MISSION`/`Mission`
keyword (Events Script Reference, *Mission events*):

```
// Main-1.txt / EVENTS/United Nations.txt
ON BESIEGED "Busan" BY ENEMY MISSION "Territory" FAIL
ON REGION_OCCUPIED "North Korea" BY ALLY PLUS ME MISSION "NorthKorea" SUCCESS
```

```
// Main-11.txt / EVENTS/United States.txt  (the campaign's last mission)
if (Total>=15)
  Mission "Casualties" Success
else
  Mission "Casualties" Fail
end
...
BLOCK CheckForFinalSuccess()
  Mission "China" Success
  Mission "Russia" Success
  Mission "Casualties" Final_Success     // triggers the FinalSuccess / FinalSuccess1 / FinalSuccess2 screens
END
```

**`ScenarioInfo` declares the mission slots** (name, description, target value, reward) and **the event
scripts decide when each one succeeds or fails**. `Mission "Name" SUCCESS/FAIL`, `Mission "Name" add N/SET N`
and `MISSION_STATE("Name")` are the only connection between the two files.

---

## 5. Chaining missions across a campaign

Across `Main-1.txt` → `Main-2.txt` → … → `Main-11.txt`, the fields form a linked list:

| Mission | `ProceedTo` | `TransitionFileName` |
|---|---|---|
| `Main-1.txt` (first) | `Main-2.txt` | *(none)* |
| `Main-2.txt` | `Main-3.txt` | `Main-1.txt.result` |
| … | … | … |
| `Main-11.txt` (last) | *(none)* | `Main-10.txt.result` |

Each mission points forward to the next map to load (`ProceedTo`) and back to the previous mission's
recorded outcome (`TransitionFileName`, the previous mission's `ResultFileName`).

---

## 6. DLC campaigns and the virtual Scenario folder

Each DLC ships its own top-level `SCENARIO` file, structured like `Main.txt`/`SNARE.txt`:

```
// DLC_3.txt
SCENARIO
Name ID 7101
Description ID 7102
Image "Scenario/DLC_3/Truman_and_MacArthur.jpeg"
Faction 0

MAP "Scenario/DLC_3/DLC_3-1.txt"
Image "Scenario/DLC_3/DLC_3-1.png"
...
```

Physically, a DLC's `SCENARIO` file and its missions live inside the DLC mod's own package, under
**`DLC_n/Scenario/`**. The mod virtually extends the base game's `Scenario/` tree, so every path inside these
files is still written as `Scenario/DLC_n/...`, as if it were part of the base game's folder (the same
convention as for `USE` paths in event scripts).

**Case study — DLC-3 Mission 1.** Its `ScenarioInfo` declares six mission slots — "All China",
"Destroy Enemy", "Control 2 Territories", "Lose less than 30 divs" (a bonus objective that can fail on its
own), "Complete Faster" and "Casualties" — driven from `EVENTS/Communist Party of China.txt` and
`EVENTS/Kuomintang.txt`. "Complete Faster" is a **timed bonus objective**:

```
// DLC_3-1.txt / EVENTS/Communist Party of China.txt
MISSION "Complete Faster" TIMER FasterTimer
ON TICK +FasterTimer MISSION "Complete Faster" FAIL
```

`MISSION "Name" TIMER <var>` starts a countdown tied to that mission slot; the `ON TICK` fails the mission
once it runs out.

---

## 7. Preparing the mission map in the Cheats build

The quickest way to build a mission's starting position is to set it up in a running game and save it as a
scenario. This uses the [Cheats build](10-Cheats-Build.md).

1. **Load a standard map** (e.g. *Atomic Earth*) in a single-player game in the Cheats build.
2. **Research technologies.** Queue the technologies the faction should start with and press
   **Shift + T** — the whole research queue is completed at once.
3. **Build units.** **Ctrl + click** a unit in the production panel: it is added already built and is
   ready to deploy at once. Repeat for every unit you need.
4. **Place units.** Deploy them on the map — holding **Ctrl** lets you place a unit anywhere, including
   outside your own territory. Select a deployed unit and press **Ctrl + T** to move it instantly to the
   point under the cursor.
5. **Adjust borders** if the mission needs it: **Ctrl + O** gives the region under the cursor to the
   current faction.
6. **Switch factions** with **Shift + 0 … 9** (the faction slot number) and repeat steps 2–5 for every
   faction that needs a prepared position.
7. **Save as scenario:** hold **Shift** when confirming *Save*. The game writes
   `Documents/My Games/ICBM-Escalation/SAVES/SAVEn/world.txt` and `world.txt.remap.txt`.

What a scenario save contains: the map part, all units on the map, each faction's technologies and stocks,
region owners (in `world.txt.remap.txt`), and two templates to fill in — a commented-out `ScenarioInfo`
block and, for every active faction, `Events FromFile "Scenario/MY_SCENARIO_NAME/MISSION_N/Events/<faction>.txt"`.
It leaves out the game clock, the mod list, AI plans, diplomacy history, pollution and score.

Turning it into a mission:

1. Copy the two files into the campaign folder with matching names, e.g.
   `Scenario/BorderCrisis/BorderCrisis-1.txt` and `Scenario/BorderCrisis/BorderCrisis-1.txt.remap.txt`
   (the region owners are read from the map file's name plus `.remap.txt`).
2. Set `MAP Name ID` / `Description ID` to your string IDs.
3. Uncomment the `ScenarioInfo` template and fill it in ([§3](#3-the-map-files-scenarioinfo-block)).
4. Point each `Events FromFile` line to the faction's event script (a file that does not exist stops
   loading), or remove it for factions without a script.
5. Add the map to the top-level `SCENARIO` file ([§2](#2-the-top-level-scenario-file)).

The same save can also become a free-play map — see [09 — Maps §11](09-Maps.md#11-making-a-map-from-a-saved-game).

---

## 8. Mission-specific mods

A campaign runs on the base game's data: no game-mode mod is active
([12 §8](12-Config-Files.md#8-game-modes-blitz-standoff-conquest)). A mission that needs different data —
another economy, changed or extra units, an extra technology — brings it in its own mod, named in the
mission's map file:

```
MAP Name ID 6002
Description ID 6003
Restrictions …
MapSpecificMod "Scenario/Main/GDP-Mod"
```

The mod is active only while that mission is played, has priority over all other mods, and is kept in the
mission's saved games. [09 §13](09-Maps.md#13-map-specific-mods) describes how it works; the points
specific to campaigns are below.

**The shipped campaigns:**

| Mod | Used by | Changes |
|---|---|---|
| `Scenario/Main/GDP-Mod` | Main missions 1, 2, 3, 5, 9, 11 | A zero-cost technology `GDP_MOD` and `ImprovedBy "GDP_MOD" Production 2.0`, `Science 1.0`, `Espionage 2.0` on `VirtualCity`; `UseAbsolutePopulationForOccupationTime true`. |
| `Scenario/Main/GDP-Mod-M4`, `GDP-Mod-M10` | Main missions 4 and 10 | The same with `Production 2.5` and `4.0`. |
| `Scenario/Main/VIP-Mod`, `VIP-KILL-MOD` | Main mission 6, and missions 7–8 | The `GDP-Mod` changes plus a `VIP` unit for the missions' protect / eliminate objectives. |
| `Scenario/SNARE/SNARE_Mod` (`ForceLoading`) | SNARE missions 1–5 | Changed units (e.g. the `SSBN` loadouts), missiles and `espionage.txt`. |

**One mod for several missions, or one each.** Several missions can name the same folder. Make a separate
folder when one mission needs other values (as `GDP-Mod-M4` does). Keep the folders under the campaign's
own `Scenario/<Campaign>/` folder.

**`ForceLoading`.** The screen where the player spends the mission's starting points reads the map
without its mod. Add `ForceLoading` when the starting setup or the point costs use units or technologies
that only the mod defines.

**Preparing such a mission in the Cheats build** ([§7](#7-preparing-the-mission-map-in-the-cheats-build)).
Units and technologies that exist only in the mission's mod are available only while the mod is active.
Add the `MapSpecificMod` line to the map file you start from before you load it. The scenario save keeps
the line (re-add `ForceLoading` if you need it).

---

## 9. Tutorial: a simple 3-mission campaign

This walks through a small original campaign, **"Border Crisis"**, with three missions for one player
faction, "Blue". Each mission's map is prepared as in [§7](#7-preparing-the-mission-map-in-the-cheats-build);
this section covers the scenario structure and the event scripts.

### Folder layout

```
Scenario/BorderCrisis/BorderCrisis.txt        <- top-level SCENARIO file
Scenario/BorderCrisis/BorderCrisis-1.txt      <- Mission 1 map file (+ BorderCrisis-1.txt.remap.txt)
Scenario/BorderCrisis/BorderCrisis-2.txt      <- Mission 2 map file (+ .remap.txt)
Scenario/BorderCrisis/BorderCrisis-3.txt      <- Mission 3 map file (+ .remap.txt)
Scenario/BorderCrisis/BorderCrisis-1/EVENTS/Blue.txt
Scenario/BorderCrisis/BorderCrisis-2/EVENTS/Blue.txt
Scenario/BorderCrisis/BorderCrisis-3/EVENTS/Blue.txt
```

### The top-level file

```
// Scenario/BorderCrisis/BorderCrisis.txt
SCENARIO
Name ID 9000
Description ID 9001
Image "Scenario/BorderCrisis/Banner.jpeg"
Faction 0

MAP "Scenario/BorderCrisis/BorderCrisis-1.txt"
Image "Scenario/BorderCrisis/BorderCrisis-1.png"

MAP "Scenario/BorderCrisis/BorderCrisis-2.txt"
Image "Scenario/BorderCrisis/BorderCrisis-2.png"

MAP "Scenario/BorderCrisis/BorderCrisis-3.txt"
Image "Scenario/BorderCrisis/BorderCrisis-3.png"
```

### Mission 1 — "Skirmish": hold the border

One `Value 1` primary mission (hold a region) and one secondary (spot the enemy).

```
// Scenario/BorderCrisis/BorderCrisis-1.txt  (ScenarioInfo block)
ScenarioInfo
 BriefingText ID 9010
 BriefingImage "Scenario/BorderCrisis/BorderCrisis-1/briefing.png"

Primary Mission "Border"
  Text ID 9011
  Value 1
  ProductionPoints 100

Secondary Mission "Recon"
  Text ID 9012
  Value 1
  ProductionPoints 50

ON Success
  Text ID 9013
  Image "Scenario/BorderCrisis/BorderCrisis-1/success.png"

ON Failure
  Text ID 9014
  Image "Scenario/BorderCrisis/BorderCrisis-1/failure.png"

EndGameCountdown 600
ResultFileName "Scenario/BorderCrisis/BorderCrisis-1.txt.result"
ProceedTo "Scenario/BorderCrisis/BorderCrisis-2.txt"
```

```
// Scenario/BorderCrisis/BorderCrisis-1/EVENTS/Blue.txt
def int Phase = 1

USE "Scenario/LIB/Common.txt"

BLOCK StdMessage(int ID)
  Message UI_STRING(ID) Position TopLeft
END

FOR AI
  SUSPEND AI
FOR PLAYER
  on each Besieged "Blue City" by enemy Mission "Border" fail
  on each Region_Occupied "Redland" by me Mission "Border" success

  on each visible any Ground of Enemy Mission "Recon" success

  ON Mission "Border" FAIL StdMessage(9015)
  ON Mission "Border" SUCCESS StdMessage(9016)
END
```

"Border" fails the moment our own city is besieged and succeeds once we occupy the enemy's region. "Recon"
succeeds the first time we spot an enemy ground unit — a `Value 1` mission needs only one `SUCCESS`.

### Mission 2 — "Escalation": a counted objective

A `Value 3` primary mission — destroy 3 enemy airbases — using `Mission "Name" add 1`, plus a casualties
threshold using `GetFactionCasualties` from `LIB/Common.txt`.

```
// Scenario/BorderCrisis/BorderCrisis-2.txt  (ScenarioInfo block)
ScenarioInfo
 BriefingText ID 9020
 BriefingImage "Scenario/BorderCrisis/BorderCrisis-2/briefing.png"

Primary Mission "Airbases"
  Text ID 9021
  Value 3
  ProductionPoints 150

Primary Mission "Casualties"
  Text ID 9022
  Value 1
  ProductionPoints 100

ON Success
  Text ID 9023
  Image "Scenario/BorderCrisis/BorderCrisis-2/success.png"

ON Failure
  Text ID 9024
  Image "Scenario/BorderCrisis/BorderCrisis-2/failure.png"

EndGameCountdown 900
ResultFileName "Scenario/BorderCrisis/BorderCrisis-2.txt.result"
ProceedTo "Scenario/BorderCrisis/BorderCrisis-3.txt"
TransitionFileName "Scenario/BorderCrisis/BorderCrisis-1.txt.result"
```

```
// Scenario/BorderCrisis/BorderCrisis-2/EVENTS/Blue.txt
USE "Scenario/LIB/Common.txt"

BLOCK CheckCasualties()
  if (GetFactionCasualties(SelfID) > 200000)          // from LIB/Common.txt
    Mission "Casualties" fail
  end
END

FOR AI
  SUSPEND AI
FOR PLAYER
  on each destroyed any "Enemy_Airbase" Mission "Airbases" add 1

  on each TICK +SECONDS(10) CheckCasualties()

  ON Mission "Airbases" SUCCESS Mission "Casualties" success
END
```

"Airbases" succeeds after three `add 1`s reach its `Value 3`; "Casualties" fails only explicitly (once
casualties pass the threshold) and otherwise succeeds when "Airbases" is done — the same "one mission
gates another" pattern `Main-11.txt` uses.

### Mission 3 — "Ceasefire": the campaign's last mission

The last mission has no `ProceedTo`. A real finale could use the three-screen `Final_Success` sequence
([§3](#3-the-map-files-scenarioinfo-block)); this example keeps to plain Success/Failure.

```
// Scenario/BorderCrisis/BorderCrisis-3.txt  (ScenarioInfo block)
ScenarioInfo
 BriefingText ID 9030
 BriefingImage "Scenario/BorderCrisis/BorderCrisis-3/briefing.png"

Primary Mission "Peace"
  Text ID 9031
  Value 1
  ProductionPoints 200

ON Success
  Text ID 9032
  Image "Scenario/BorderCrisis/BorderCrisis-3/success.png"

ON Failure
  Text ID 9033
  Image "Scenario/BorderCrisis/BorderCrisis-3/failure.png"

EndGameCountdown 300
ResultFileName "Scenario/BorderCrisis/BorderCrisis-3.txt.result"
TransitionFileName "Scenario/BorderCrisis/BorderCrisis-2.txt.result"
```

```
// Scenario/BorderCrisis/BorderCrisis-3/EVENTS/Blue.txt
FOR AI
  SUSPEND AI
FOR PLAYER
  ON Surrendered "Red" Mission "Peace" success
  ON "Global War" Mission "Peace" fail
END
```

That is a complete, if minimal, 3-mission campaign: one top-level `SCENARIO` file, three mission maps
prepared in the Cheats build, each with a `ScenarioInfo` block declaring its objectives, three
`EVENTS/Blue.txt` files deciding when those objectives are met, and `ProceedTo`/`TransitionFileName`
chaining them into one playthrough.
