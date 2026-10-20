# 13 — Tutorial missions

[Index](index.md) · [Cheats build](10-Cheats-Build.md) · [Campaigns and scenarios](11-Campaigns-and-Scenarios.md)

A tutorial mission is a saved game plus a script, `Tutorial.txt`, that walks the player through it: it
shows the instructor's messages, waits for the player to do what they were asked, switches parts of the
interface on and off, highlights units and places, and moves on to the next mission. The script uses its
own simple step-by-step command language. It is not an event script (see the Events Script Reference):
there are no conditions or expressions, just a list of steps carried out one after another.

Contents

1. [Files and the Tutorial menu](#1-files-and-the-tutorial-menu)
2. [How a script runs](#2-how-a-script-runs)
3. [Syntax](#3-syntax)
4. [Messages](#4-messages)
5. [Waiting for the player: events and variables](#5-waiting-for-the-player-events-and-variables)
6. [Actions](#6-actions)
7. [Timers and subroutines](#7-timers-and-subroutines)
8. [Event reference](#8-event-reference)
9. [Names: controls, keys, window positions](#9-names-controls-keys-window-positions)
10. [Making a tutorial mission](#10-making-a-tutorial-mission)
11. [Checking a script](#11-checking-a-script)
12. [Pitfalls](#12-pitfalls)

---

## 1. Files and the Tutorial menu

Each mission is a folder `Tutorial/MissionN/`, where N is 1 to 12:

| File | Contents |
|---|---|
| `world.txt`, `icbm.rnt`, `monitor.st`, `version.num` | A saved game, exactly as the game writes it to `Documents/My Games/ICBM-Escalation/SAVES/SAVEn/` (`replay.bin` is not needed). The mission starts from this position, with the player controlling the faction the game was saved with. |
| `Tutorial.txt` | The script (this chapter). |
| `available.txt` | Written by the game the first time the mission is started. The game counts these files to tell how many tutorial missions the player has played. Don't ship it. |

The **Tutorial** submenu of the main menu always shows mission 1. It shows mission N when
`Tutorial/MissionN/Tutorial.txt` exists. The title of mission N's button is the `UI.lng` string
**3300 − N**: 3299 `"1. Basic Controls"` … 3289 `"11. Combined Strike Plans"`; mission 12 uses 3288.

Mods are searched before the game folder. A mod can therefore replace a mission by shipping its folder,
or add mission 12 by shipping `Tutorial/Mission12/` (and string 3288 in its language file).

While a mission runs, the player can press **Escape** (if the script allows that key, §9). The dialog
offers to leave the tutorial, to restart the mission from its saved game, or to go back to it.

---

## 2. How a script runs

The script is a list of **steps**: messages and actions. The game carries them out in order. A step
either finishes at once (most actions) or **blocks** until something happens:

* a message with an OK button waits for the player to press OK;
* a message without an OK button, or a `Wait` action, waits for **events** — things the player or the
  game did, such as `"SELECTED [24792]"` or `"BUILT [Army_Base]"` (§5, §8);
* `WaitTicks` waits for game time to pass.

When the last step is done, the tutorial script is over and the game simply goes on. To end a mission,
finish the script with `Action Load "Tutorial/MissionN/"` (start the next mission) or `Action Finish`
(return to the menu).

**Time.** All tick counts are game ticks: 60 ticks are one second of game time at normal speed. They
pass only while the game runs, not while it is paused. The exception is the duration of
`HighlightPosition`, which counts real time.

**AI factions are passive** while a tutorial script runs: they make no decisions of their own until the
script gives the first `AIAttack` order (§6).

---

## 3. Syntax

```
// comment to the end of the line          /* block comment */

Message 3500 Dim                            // a step: show message 3500 with the screen dimmed
Action EnableKey "SPACE"                    // a step: an action with one parameter
Message 3502 NoOK Wait "UNPAUSED"           // a step: blocks until the player unpauses
Action HighlightUnit #ThisAirbase           // a parameter taken from a variable
END
```

* The file is a sequence of steps that starts with `Message`, `Action`, `Timer` or `Sub`, and ends with
  `END`. Line breaks don't matter: a step runs until the next `Message`, `Action`, `Timer`, `Sub`, `END`
  or `Clear`.
* `Message`, `Action`, `Timer`, `Sub`, `END`, `Clear` and the message options (`Dim`, `NoOK`, `Wait`,
  `WaitOr`, `WaitTicks`) can be written in any letter case.
* **Action names and named values are case-sensitive**: `EnableControl ViewSwitch`, not
  `enablecontrol viewswitch`.
* Parameters are numbers, named values (§9), `"text in quotes"` (key names, unit type IDs, event names,
  paths) or `#Variables` (§5). A comma after a number is ignored, so `0.36, 0.49` works.
* A word that is neither a number, nor a named value, nor in quotes stops the game with
  *Tutorial.txt, Line N, unknown word …*. An unknown action stops it with *wrong Action*, and anything
  other than a step stops it with *Expected Message or Action*.

---

## 4. Messages

```
Message <UI.lng number> [Dim] [NoOK] [WaitTicks <ticks>] [Wait "event" [#Var]] [WaitOr "event" [#Var]] …
```

The text is the string with that number in `Lang/<language>/UI.lng`, so it is translated with the rest of
the game. The instructor's portrait (`Images/TUTORIAL_PORTRAIT.png`) is shown next to it, in the window
position and size set by `WindowPosition` and `WindowSize`.

| Option | Effect |
|---|---|
| *(none)* | The message has an OK button; the script goes on when the player presses it. |
| `Dim` | Darkens the screen behind the message. Use it for introductions and conclusions. |
| `NoOK` | No OK button: the message stays until its `Wait` events have happened (all of them, or one of them with `WaitOr`), or until `WaitTicks` have passed. A `NoOK` message with neither closes at once. |
| `WaitTicks <ticks>` | Closes the message after that many game ticks. |
| `Wait "event" [#Var]` | With `NoOK`: wait for this event (§5). Give several `Wait`s to wait for all of them. |
| `WaitOr "event" [#Var]` | With `NoOK`: like `Wait`, but the message closes as soon as **any one** of its events has happened. |

`Wait` and `WaitOr` are ignored on a message that has an OK button: the OK button decides. The same
number can be shown again later in the script.

---

## 5. Waiting for the player: events and variables

### Events

The game reports what happens as **event texts**: a name in capitals, followed by details in square
brackets:

```
"SELECTED [24792]"                      the player selected the unit with UID 24792
"LAUNCHED [3] [Fighter]"                faction 3 launched a unit of type Fighter
"HOSTED CONFIG [24792] [Bomber] [10 Megaton]"
"KILLED POPULATION [Moscow]"
```

A `Wait` matches when the event text is **exactly** the same, character for character, including
spaces and brackets. Many events are reported in several forms (by unit type, by UID, by owner), so
choose the form that says what you need. §8 lists them all.

Give the same `Wait` twice to require the event twice:
`Message 3607 NoOK Wait "CQADDED [Army_Division]" Wait "CQADDED [Army_Division]"` waits until two
divisions have been queued.

### Events that happened earlier

An event that matches none of the waiting step's `Wait`s is normally lost. A `Wait` that comes later
does not see it. The exceptions are kept until a later `Wait` uses them:

* `"DESTROYED [uid]"` and `"DESTROYED TYPE [type]"` are always kept, so a script can wait for a unit
  that may already be dead;
* any event named with `Action Remember "event"` is kept from then on. `Action Forget "event"` stops
  this and drops a kept copy.

### Variables

A variable is a name after `#`. It holds a whole number and needs no declaration. Variable names may
contain only letters and digits, and letter case doesn't matter.

* **Set it**: `Action Set #Var 24792`, or with `#Var` as the first parameter of `AddUnit`,
  `HighlightPosition`, `CreateOffer` or `MakeCounterOffer`.
* **From an event**: put `#Var` after a `Wait`. When the event happens, the variable receives the
  event's value (§8; usually the UID of the unit concerned):
  `Message 3718 NoOK Wait "OFFER SENT [9]" #PartnershipOffer`.
* **Use it** as a parameter (`Action HighlightUnit #ThisAirbase`) or inside an event text
  (`Wait "SELECTED [#ThisAirbase]"`). The number replaces the name when the step runs.

A variable used before it has a value stops the game with *Tutorial Variable not found*.

---

## 6. Actions

`UID` is a unit's unique number: in the [Cheats build](10-Cheats-Build.md#information), hold
**Shift + Ctrl** over a unit to see and copy it. A unit in the mission's saved game keeps its UID. A unit
created while the mission runs gets a new UID, so store it in a variable. Map coordinates `x y` are the
0…1 values that **Shift** shows in the Cheats build. Factions are numbered 0–9 in the order of the
`Player` blocks of the map.

### Interface

| Action | Effect |
|---|---|
| `DisableAllKeys` / `EnableAllKeys` | Ignore / accept every keyboard key. |
| `DisableKey "KEY"` / `EnableKey "KEY"` | One key (names in §9). An unknown name does nothing. |
| `AllowKeyboard true\|false` | `true`: while a message is shown, key presses still reach the game (camera movement, speed keys). `false`: the message takes them. |
| `DisableAllControls` / `EnableAllControls` | Switch every interface control (§9) off / on. A disabled control shows *not available in the tutorial* when clicked. |
| `DisableControl Name` / `EnableControl Name` | One control (§9). |
| `WindowPosition Pos` | Where the following messages appear (§9). Default `Center`. |
| `WindowSize Size` | `SizeStandard` (default), `SizeWide` or `SizeSmall`. |
| `HighlightUnit UID` | A pulsing ring around the unit, until `ClearHighlights`. |
| `HighlightPosition [#Var] x y [radius] [ticks]` | A pulsing ring at a map point. `radius` sets the size: 50 by default, 100 is twice as large. `ticks` sets how long it is shown in real time; without it, the ring stays until cleared. `#Var` receives the ring's number for `ClearHighlight`. |
| `ClearHighlight #Var` | Removes the one ring made by `HighlightPosition #Var …`. |
| `ClearHighlights` | Removes all rings. |
| `CenterUnit UID`, `Focus UID` | Moves the view to the unit and zooms in (if the player can see it). |
| `JournalCode code true\|false` | Whether the journal message with this `UI.lng` number pauses the game (`false`: it doesn't). The shipped missions switch off the pauses for routine messages ("unit built", "construction complete" …) so that they don't interrupt `SkipTime`. The codes are the ones listed in a saved game's `monitor.st`. |

### Game flow

| Action | Effect |
|---|---|
| `Wait "event" ["event" …]` | Blocks until all the events have happened, with no message on screen. |
| `WaitOr "event" ["event" …]` | Blocks until any one of them has happened. |
| `WaitTicks ticks` | Blocks for that much game time. |
| `SetGameSpeed n` | `0`: pause. `1`–`4`: set that game speed. |
| `SkipTime ticks` | Fast-forwards: the game runs that many ticks as quickly as the computer allows. Use it with `SetGameSpeed 4` to let construction or research finish. Journal messages that pause the game stop it — switch them off with `JournalCode` first. |
| `Remember "event"` / `Forget "event"` | Keep / stop keeping this event for a later `Wait` (§5). |
| `Set #Var value` | Sets a variable. |
| `Exec "name"` | Runs the subroutine `name` (§7), then goes on with the next step. |
| `Load "Tutorial/MissionN/"` | Ends this mission and starts the mission in that folder (mind the closing `/`). |
| `Finish` | Ends the tutorial as won and returns to the menu. |

### Units and AI

| Action | Effect |
|---|---|
| `AddUnit #Var x y "TypeID" faction` | Creates a unit of that type for the faction at the map point; `#Var` receives its UID. |
| `KillUnit UID` | Destroys the unit. |
| `ForceAttack UID targetUID` | Orders the unit to attack the target. If the unit has a readiness state for attacking, it switches to it. |
| `AIAttack faction enemy` | The AI faction treats `enemy` as its attacker and plans its attacks against it. The first `AIAttack` also lets all AI factions make their own decisions from then on (§2). |

Actions on a unit that no longer exists (`HighlightUnit`, `CenterUnit`, `Focus`, `KillUnit`,
`ForceAttack`) do nothing.

### Diplomacy

| Action | Effect |
|---|---|
| `SetAIDecisionMode Mode` | How the AI answers the player's diplomatic offers: `Auto` (normally), `AlwaysAccept`, `AlwaysReject`, `NoDecision` (no answer yet — the offer waits). |
| `CreateOffer #Var from to` | Creates an empty offer from faction `from` to faction `to`; `#Var` receives its number. Fill it with `AddRequest` / `AddOffer`. |
| `MakeCounterOffer #Var offer` | Rejects the offer with that number (for example one the player sent, caught with `Wait "OFFER SENT [9]" #Offer`) and answers it with a copy that has the sides swapped; `#Var` receives the counter-offer's number. The same variable can be used for both. |
| `AddRequest offer Item [value] [count]`, `AddOffer offer Item [value] [count]` | Adds an item to what the offer asks for / gives. |

Diplomatic items: `CeaseFire`, `PeaceTreaty`, `Partnership`, `Alliance`, `Intelligence`,
`WithdrawForces` (no value); `CooperationAgreement` + one of `Production`, `Intelligence`, `Research`,
`RadarData`, `NuclearAssets`; `War` + faction number; `Contributions` + amount; `Technology` + `"TechID"`;
`Territory` + `"region name"`; `Hardware` + `"UnitTypeID"` + count (default 1). Example from mission 3:

```
Message 3718 NoOK Wait "OFFER SENT [9]" #PartnershipOffer
Action MakeCounterOffer #PartnershipOffer #PartnershipOffer
Action AddRequest #PartnershipOffer Hardware "Cruiser" 1
Action SetAIDecisionMode Auto
```

---

## 7. Timers and subroutines

### Timer

```
Timer <ticks> <steps…> END
Timer <ticks> <steps…> Clear "event"
```

A timer runs alongside the script. When it is reached, the script does not wait: it goes straight on to
the next step while the timer counts down. When the time is up, the timer's steps run all at once and
waits in them are skipped. Put only actions in a timer: a message shown from a timer replaces the
script's current message, and its OK button moves the main script on. With `Clear "event"`, the timer is
cancelled if that event happens first. From mission 7:

```
Timer 200000 Action HighlightUnit 55480 Clear "VISIBLE [55480]"
Message 4108 NoOk Wait "VISIBLE [55480]"
```

A timer ends at its own `END` or at `Clear "…"`. Everything up to there belongs to it, so a timer without
either swallows the rest of the script.

### Subroutine

```
Sub "name" <steps…> END          // defines it; nothing runs here
Action Exec "name"               // runs its steps, then continues after the Exec
```

A subroutine can be run any number of times, and can itself `Exec` others. Names are not
case-sensitive. `Exec` of an unknown name does nothing, and an `Exec` inside a timer is ignored.

---

## 8. Event reference

*Value* is what a `#Var` after the `Wait` receives. `uid` is a unit's UID; `type` a unit, missile or
technology ID; `faction` a faction number (0–9). Events about "the player" are reported only for the
player's own actions.

### Units

| Event texts | When | Value |
|---|---|---|
| `SELECTED`, `SELECTED [uid]` | The player selects a unit. | uid |
| `MOVE ORDERED [type]`, `MOVE ORDERED [uid]` | The player orders a unit to move. | uid |
| `ATTACK ORDERED [type]`, `ATTACK ORDERED [uid] [target uid]` (`0` without a target unit) | The player orders an attack. | uid |
| `ORDERS COMPLETED`, `ORDERS COMPLETED [type]`, `ORDERS COMPLETED [uid]` | A unit finished its last order. | uid |
| `LAUNCHED [faction] [type]`, `LAUNCHED [carrier uid] [type]` | An aircraft, missile or other unit is launched from a base, carrier or silo. `faction` is the carrier's owner. | uid of the launched unit |
| `HOSTED CONFIG [hosted type] [config]`, `HOSTED CONFIG [carrier uid] [hosted type] [config]` | The player picks a weapon configuration for hosted units, e.g. `[Bomber] [Cruise Missiles]`. | carrier uid |
| `STATE RAISED [uid]`, `STATE LOWERED [uid]` | One of the player's units changes to its higher / lower readiness state (surfacing, deploying …). | — |
| `DEPLOY [type]` | The player places a unit from the ready-to-deploy list. | new uid |
| `DEPLOYED [type]`, `DEPLOYED [uid]` | A unit of the player has been deployed. | uid |
| `VISIBLE [uid]`, `VISIBLE TYPE [type]` | A unit becomes visible to the player. | uid |
| `VISIBLE [uid] [GHOST]`, `VISIBLE TYPE [type] [GHOST]` | A unit becomes visible only as a last-known-position ghost. | uid |
| `DESTROYED [uid]`, `DESTROYED TYPE [type]` | A unit is destroyed. These two are kept for later `Wait`s (§5). | uid |

### Production and research

| Event texts | When | Value |
|---|---|---|
| `CONSTRUCTION SCREEN`, `AP SPLITTER` | The player opens the construction screen. | — |
| `SCIENCE SCREEN`, `RESEARCH CLICKED` | The player opens the research screen. | — |
| `RESEARCH CLICKED [tech]` | The player puts a technology into research. | — |
| `CQADDED [type]` | The player adds a unit to the construction queue. | queue item number |
| `CQMOVED [number]` | The player moves a queue item to the front. | queue item number |
| `BUILT [type]` | A unit or missile of the player is completed. | — |
| `TECH AVAILABLE [tech]` | The player gets a technology. | — |

### Map, cities and war

| Event texts | When | Value |
|---|---|---|
| `KILLED POPULATION [faction]`, `KILLED POPULATION [city]` | A strike kills people in a city (`faction` = the city's owner). | city uid |
| `CITY BESIEGED [faction]`, `CITY BESIEGED [city]` | Enemy troops besiege a city. | city uid |
| `CITY OCCUPIED [city]` | A city is captured. | city uid |
| `REGION OCCUPIED [region]` | A region changes owner by occupation. | — |
| `END GAME` | The game ends. | — |

### Interface

| Event texts | When | Value |
|---|---|---|
| `PAUSED`, `UNPAUSED` | The player pauses / unpauses. | — |
| `GAME SPEED CHANGED`, `GAME SPEED CHANGED [speed]` | The game speed changes. | speed |
| `JOURNAL` | The journal is shown for the first time. | — |
| `NUCLEAR WAR MODE` | The player switches the journal's nuclear war mode. | — |
| `GLOBAL SCREEN` | The player returns to the map from another screen. | — |
| `RADAR COVERAGE` | The player switches the radar coverage display. | — |
| `ALLOWED CONTROL PRESSED` | The player presses OK on a message. | — |

### Strike planner

| Event texts | When | Value |
|---|---|---|
| `NEW STRIKE PLAN` | The player creates a strike plan, and again when they confirm it. | plan slot |
| `ADVANCED STRIKE PLAN` | The player opens the advanced view. | — |
| `EDIT ATTACKERS`, `EDIT TARGETS` | The player edits attackers / targets. | — |
| `SP_ATTACKER [type]`, `SP_TARGET [type]` | The player switches a unit type among the attackers / targets. | — |
| `TARGET REGION [region]` | The player switches a region among the targets. | — |
| `SP_ICON` | The player picks a plan icon. | — |
| `PLAN ELEMENT ADDED` | The player adds a sub-plan. | — |
| `SP INVASION` | The player turns a sub-plan into an invasion. | — |
| `EXECUTE STRIKE PLAN`, `EXECUTE STRIKE PLAN [slot]` | The player executes a plan. | plan slot |

### Diplomacy

| Event texts | When | Value |
|---|---|---|
| `DIPLOMACY SCREEN` | The player opens diplomacy. | — |
| `FACTION SELECTED`, `FACTION SELECTED [faction]` | The player selects a faction there. | faction |
| `OFFER SENT`, `OFFER SENT [faction]` | The player sends an offer to the faction. | faction; offer number with `[faction]` |
| `OFFER ACCEPTED`, `OFFER ACCEPTED [faction]`, `OFFER REJECTED`, `OFFER REJECTED [faction]` | The player accepts / rejects the faction's offer. | faction |
| `ALLIANCE FORMED` | The player's faction becomes partner of another. | the other faction |
| `ALLIANCE SETTINGS`, `GENEVA CONVENTION` | The player opens that agreements tab. | — |
| `VOTING STARTED` | The player starts an alliance vote. | vote number |
| `VOTING FINISHED` | A vote ends. | vote number |

---

## 9. Names: controls, keys, window positions

### Controls (`EnableControl` / `DisableControl`)

| Name | What it covers |
|---|---|
| `Journal` | The journal (event list). |
| `Clocks` | Pause and game speed buttons. |
| `Diplomacy`, `Espionage`, `Science` | Those screens. |
| `TerritoryOverlay`, `RadarCoverage` | The map overlay buttons. |
| `ViewSwitch` | Switching between the globe and flat views. |
| `SCE` | The research and construction buttons as a whole. |
| `SelectUnit` | Selecting units. |
| `DeployUnit`, `ConstructUnit`, `DeleteCQ` | Deploying units, adding to and removing from the construction queue. |
| `APSplitter` | The slider that splits the budget between research and construction. |
| `Shifter` | The unit's action buttons (surface/submerge, refill, cancel orders …). |
| `NuclearMode` | The journal's nuclear war mode button. |
| `StrikePlanner`, `StrikePlannerOK`, `StrikePlannerCancel`, `StrikePlannerExec`, `StrikePlannerAdvanced` | The strike planner and its buttons. |

### Keys (`EnableKey` / `DisableKey`)

Upper case, in quotes: `"A"` … `"Z"`, `"0"` … `"9"`, `"PAD 0"` … `"PAD 9"`, `"F1"` … `"F12"`, `"ESCAPE"`,
`"TILDE"`, `"MINUS"`, `"EQUALS"`, `"BACKSPACE"`, `"TAB"`, `"OPENBRACE"`, `"CLOSEBRACE"`, `"ENTER"`,
`"SEMICOLON"`, `"QUOTE"`, `"BACKSLASH"`, `"COMMA"`, `"FULLSTOP"`, `"SLASH"`, `"SPACE"`, `"INSERT"`,
`"DELETE"`, `"HOME"`, `"END"`, `"PGUP"`, `"PGDN"`, `"LEFT"`, `"RIGHT"`, `"UP"`, `"DOWN"`, `"PAD /"`, `"PAD *"`,
`"PAD -"`, `"PAD +"`, `"PAD DELETE"`, `"PAD ENTER"`, `"PAD ="`, `"PRINTSCREEN"`, `"PAUSE"`, `"LSHIFT"`,
`"RSHIFT"`, `"LCTRL"`, `"RCTRL"`, `"ALT"` (left Alt), `"ALTGR"`, `"LWIN"`, `"RWIN"`, `"MENU"`, `"COMMAND"`,
`"SCROLLLOCK"`, `"NUMLOCK"`, `"CAPSLOCK"`.

Keep `"ESCAPE"` enabled so that the player can leave or restart the mission, and `"ENTER"` /
`"PAD ENTER"` so that OK can be pressed from the keyboard.

### Other named values

| For | Names |
|---|---|
| `WindowPosition` | `Center`, `TopLeft`, `TopRight`, `BottomLeft`, `BottomRight`, `CenterLeft`, `CenterRight` |
| `WindowSize` | `SizeStandard`, `SizeWide`, `SizeSmall` |
| `SetAIDecisionMode` | `Auto`, `AlwaysAccept`, `AlwaysReject`, `NoDecision` |
| true / false | `true`, `false`, `yes`, `no` (also `True`, `TRUE` …) |

---

## 10. Making a tutorial mission

1. **Prepare the position** in the [Cheats build](10-Cheats-Build.md). Start a single-player game on the
   map you want, then use the cheats to set up every faction: research, build, place and move units,
   change borders. Switch at the end to the faction the player will command.
2. **Save normally** (without Shift). A normal save keeps the game clock, diplomacy and AI plans, which
   a tutorial usually needs. Copy the save folder `Documents/My Games/ICBM-Escalation/SAVES/SAVEn/` to
   `Tutorial/MissionN/` in your mod (leave out `replay.bin`).
3. **Collect the numbers** the script needs. In the Cheats build, load the save. Hold **Shift + Ctrl**
   over each unit you will refer to (UID) and **Shift** over each place (coordinates).
4. **Write the texts** into `Lang/Eng/UI.lng` (and the other languages) under free numbers, and the
   mission title under 3300 − N.
5. **Write `Tutorial.txt`.** A typical opening locks everything down and then opens the interface one
   piece at a time:

   ```
   Action JournalCode 2112 false            // "unit built" no longer pauses the game
   Action AllowKeyboard true
   Action DisableAllKeys
   Action EnableKey "ESCAPE"
   Action EnableKey "ENTER"
   Action EnableKey "PAD ENTER"
   Action DisableAllControls
   Action EnableControl ViewSwitch

   Message 5000 Dim                          // introduction

   Action WindowPosition TopRight
   Action EnableControl SelectUnit
   Action HighlightUnit 24792
   Message 5001 NoOK Wait "SELECTED [24792]" // "select the airbase"
   Action ClearHighlights

   Message 5002 NoOK Wait "LAUNCHED [24792] [Fighter]"
   Action WaitTicks 600

   Action WindowPosition Center
   Message 5003 Dim                          // conclusion
   Action Load "TUTORIAL/MISSION2/"
   END
   ```

6. **Check** the script (§11), then play it through. **Escape → Restart** reloads the mission with the
   current script, so you can edit `Tutorial.txt` and restart without leaving the game.

---

## 11. Checking a script

`tools/tutorial_lint.py` reads the scripts the way the game does and reports, before you start the game:

* unknown actions, words and named values;
* unknown keys, controls, window positions and decision modes;
* unknown event names;
* message numbers missing from `Lang/Eng/UI.lng`;
* variables that never get a value;
* `Exec` without its `Sub`;
* `Load` targets without a `Tutorial.txt`;
* timers that are never closed.

```bash
python3 tools/tutorial_lint.py GAME_FOLDER                      # every Tutorial/Mission*/Tutorial.txt
python3 tools/tutorial_lint.py GAME_FOLDER MyMod/Tutorial/Mission12/Tutorial.txt
```

It cannot check UIDs, unit type IDs or the details inside event brackets against the saved game. Check
those by playing the mission.

---

## 12. Pitfalls

* **Event texts must match exactly.** `"SELECTED [24792]"` is not `"SELECTED[24792]"` or
  `"Selected [24792]"`. Type and technology IDs are case-sensitive. When a `NoOK` message never closes,
  check its event text against §8 first.
* **A `Wait` only sees events from the moment its step is reached**, except `DESTROYED` events and
  events named with `Remember`. Place the message before the action the player is asked to do, or
  `Remember` the event.
* **`Wait` on a message with an OK button does nothing.** Add `NoOK`.
* **Lock the player in, then let them out.** Every key and control the script disabled stays disabled
  until it is enabled again or the mission ends. Forgetting `EnableKey "ESCAPE"` leaves the player
  without a way to quit.
* **Journal pauses interrupt fast-forwarding.** Switch the routine journal messages off with
  `JournalCode … false` before using `SkipTime`.
* **UIDs come from the saved game.** If you re-save the mission's position, units placed again get new
  UIDs; collect them again. Units created by `AddUnit` must be referred to through their variable.
* **AI factions stay passive until `AIAttack`** — plan the mission's opposition with that in mind.
* **`Load` takes the folder** (`"Tutorial/Mission2/"`, with the closing slash), not the script file.
