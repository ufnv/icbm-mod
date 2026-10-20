# 10 — The Cheats build

[Index](index.md) · [Maps](09-Maps.md) · [Tuning guide](07-Tuning-Guide.md)

The **Cheats build** is the edition of the game made for modders and mission designers. It plays exactly
like the normal game and reads the same data, but adds key combinations for testing (instant research,
instant production, free placement, switching sides), the map-making tools of
[09 — Maps](09-Maps.md#9-building-the-border-and-region-files-processborders), and saving a game as a
scenario. The main menu shows **CHEATS** after the version number.

Most cheats work in single player only.

## 1. Key combinations

### Sides and research

| Keys | Effect |
|---|---|
| **Shift + 0 … 9** | Play as the faction in slot 0 … 9 (the order of the `Player` blocks in the map). The faction you leave is taken over by the computer. |
| **Shift + T** | Instantly research every technology in the current faction's research queue (all research streams). Queue the technologies you want first, then press Shift + T. |
| **Shift + click on the pause button** (while only watching a game) | Take control of the first faction. |

### Units and production

| Keys | Effect |
|---|---|
| **Ctrl + click** on a unit in the production panel | The unit is added already built: it appears at once among the units ready to deploy. |
| **Ctrl** held while deploying a unit | The unit can be placed anywhere — on any faction's territory, outside your own borders and on occupied ground. |
| **Ctrl + T** | Move the selected unit instantly to the point under the cursor. Its orders are cleared. |

### Territory

| Keys | Effect |
|---|---|
| **Ctrl + O** | The region under the cursor passes to your faction. |
| **Ctrl + P** | Hold / release region ownership changes (while held, captured regions do not change owner). |

### Information

| Keys | Effect |
|---|---|
| **Shift** (held) | Shows the map coordinates `x, y` under the cursor and copies them to the clipboard every two seconds — ready to paste into map, event or relocation files. |
| **Shift + Alt** (held) | The same, as a 3D point on the unit sphere (`x, y, z`), the form used by `AffectedArea`. |
| **Shift + Ctrl** (held) over a unit | Shows and copies the unit's UID (for event scripts). |
| **Shift** (held) while a technology's details are shown | Shows and copies the technology's ID. |
| **Ctrl + 0 … 9**, **Alt + 0 … 8**, **Ctrl + −**, **Ctrl + +** | Show the AI placement map for one point type, for checking a generated AI cache ([09 §6](09-Maps.md#6-starting-setup-and-ai)). Ctrl + 0 … 9 = `MissileSilo`, `CityDefence`, `Radar`, `OverHorizonRadar`, `Airbase`, `SubmarineAttack`, `SubmarineHide`, `CarrierAttack`, `MobileMissile`, `ObjectDefence`; Alt + 0 … 8 (and Ctrl + −, Ctrl + +) continue with `NavalBase`, `Orbit`, `Shore`, `CityControl`, `BorderDefence`, `MarinesLanding`, `AirborneTroopsLanding`, `TroopsTraining`, `Industry`. |
| In the diplomacy screen | Details of every faction are shown, not only of allies. |

### Interface, saving and replays

| Keys | Effect |
|---|---|
| **Alt + T** | Hide / show the whole interface (for screenshots and videos). |
| **Shift** held when confirming *Save* | Save as a **scenario** instead of a saved game (§2). |
| **T** while watching a replay | Let the replay run 1000 ticks further. |
| **Ctrl + T** while watching a replay | Stop the replay and continue the game from this moment, playing the first active faction. |
| **R** in the mask editor (`EditSVG`) | Detect the segment hierarchy and save ([09 §3](09-Maps.md#editing-masks-interactively-editsvg)). |

A multiplayer lobby can also be started with a single player, for testing multiplayer maps alone.

**Automatic load:** a file `autoload.txt` next to `ICBM.CFG` (the *My Games* folder) whose first line names a save
(`SAVE838`, `AUTO1`, `QUICK1`, `DATA`, or a path to the save folder) makes the cheats build load that game straight
from the main menu at startup. The file is deleted once read, so only that start is affected. An AI-only game watched
as an observer then runs immediately instead of waiting for Shift + Space. (`-LOAD <save>` on the command line does the
same, but Steam asks for a confirmation before passing arguments.)

## 2. Saving as a scenario

Holding **Shift** when confirming *Save* writes the game as a **scenario**: the same folder as a normal save
(`Documents/My Games/ICBM-Escalation/SAVES/SAVEn/`), with `world.txt` and `world.txt.remap.txt`, but
`world.txt` holds only what a new game needs:

* the map part (`MAP …`, masks, regions, `Player` blocks, cities, display settings) and every unit on the
  map, with the factions' technologies and stocks;
* no game clock, mod list, replay, AI plans, diplomacy history, pollution or score;
* regions keep their current owners (written to `world.txt.remap.txt`, read through
  `Default AUTO_FROM_SAVE`), but not the record of who occupied them;
* a commented-out `ScenarioInfo` template, and for every active faction an
  `Events FromFile "Scenario/MY_SCENARIO_NAME/MISSION_N/Events/<faction>.txt"` placeholder.

It is the starting point for both a mission map (see the *Campaign & Scenario Structure* reference) and a
new map ([09 §11](09-Maps.md#11-making-a-map-from-a-saved-game)).

## 3. Typical workflow: setting up a starting position

1. Start a single-player game on a standard map.
2. Research what each faction should have: queue the technologies and press **Shift + T**.
3. Build units with **Ctrl + click** in the production panel; deploy them (hold **Ctrl** to place them
   anywhere) and fine-tune positions with **Ctrl + T**.
4. Change borders with **Ctrl + O** if needed.
5. Switch to the next faction with **Shift + 0 … 9** and repeat steps 2–4.
6. Save with **Shift** held (save as scenario).
