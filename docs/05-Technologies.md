# 05 — Technologies (`tech.txt`, `TechLevels.txt`)

[Index](index.md) · [Basics](00-Basics.md) · Catalog: [A5](A5-Catalog-Technologies.md)

Technologies do three jobs:

1. **The research tree** — techs with a cost that factions research.
2. **Availability and names** — every unit, missile and radar names a `Tech`; the object exists for a
   faction when that tech is known, and takes its display name from it.
3. **Switches for balance** — every `ImprovedBy`/`AffectedBy` names a tech, and unit **modifier tags**
   are techs too.

```
[TECHNOLOGY] "Nuclear_Fission"
  Name "NUCLEAR_FISSION_NAME"           // string ID in lang/<Language>/tech_t.lng — required
  Description "NUCLEAR_FISSION_DESC"    // required
  Image "Images/Science/Nuclear_Fission.png"
  Points 45
  TechLevel 1
  Type "Weapons of Mass Destruction"    // tree category
  LeadsTo "M_100kt_nuke_light"          // zero-cost child: the tech of the 100 kt bomb
  LeadsTo "Thermonuclear_bomb"          // next research step
```

---

## 1. Kinds of entries

| Header | Purpose |
|---|---|
| `[TECHNOLOGY] "id"` | A technology (researchable if it has `Points`, otherwise a zero-cost tech). |
| `[TYPE] "id"` | A **tech-tree category** (tab). Techs join it with `Type "id"`. Also a normal tech in every other respect. |
| `[LEVEL] "id"` | A **tech level** (L_1 … L_10). Linked to numbers in `TechLevels.txt`. |
| `[UNIT_CLASS] "id"` | A **unit class** for the production UI (`UC_Building`, `UC_Naval`, …). Units/missiles use it with `Class "id"`; `AutoAssignTo <unit type>` makes it the default class for that unit type. |
| `[DEFCON] "id"` | A **DEFCON state**, listed from DEFCON 5 down to 1 (the first entry is the peace-time state). While a faction is at a state, that tech counts as known, so modifiers such as `ImprovedBy "DEFCON_2" Production 0.75` on `VirtualCity` apply. `Points` sets the switching delay: the delay is taken from the state being **left**, and because `Points` is stored ×0.01 the value is in hundredths of a tick (`Points 90000` = 900 ticks = 15 "seconds", which is also the default when `Points` is omitted). |

Top-level setting: `DRAWING [SCALE <f>] [DISTANCE <f>]` — layout scale and spacing of the tech-tree view.

## 2. Properties

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `Name` | `"STRING_ID"` | **required** | Display name (looked up in `tech_t.lng`). |
| `Description` | `"STRING_ID"` | **required** | Description text. |
| `Points` | `<float>` | 0 | Research cost. 0 = **zero-cost tech**: known automatically as soon as all its parents are known (or always, if it has no parent). Multiplied by 0.01 and by the tech-level factor (§4). |
| `LeadsTo` | `LeadsTo "tech" [HideLink]` | none | Makes `tech` a child of this one. `HideLink` = no connecting line in the tree. List property. |
| `Parent` | `Parent "tech" [Before "sibling"] [HideLink]` | none | The same link written from the child's side. `Before` orders the child before a sibling in the tree. |
| `BlockedBy` | `BlockedBy "tech"` | none | The tech is disabled for every faction that is able to research `tech` (used for faction-specific alternatives). List property. |
| `CanBeResearched` | `Yes\|No` | Yes | No = cannot be researched in the tree; it can still be known by being zero-cost, granted by a scenario or granted by a script (`GRANT_TECH`). |
| `TechLevel` | `<int>` | inherited | Tech level 1–10. If not set, the highest level among its parents. Affects cost (§4) and start-of-game unlocking. |
| `NoAutoUnlockTillLevel` | `<int>` | = `TechLevel` | When a game or scenario starts at tech level *N*, techs with `TechLevel ≤ N` **and** `NoAutoUnlockTillLevel ≤ N` are granted automatically. Raise it to keep a tech locked. |
| `Type` | `"category"` | none | Tree category (a `[TYPE]`). List property. |
| `ResearchStream` | `standard\|default` (0) or `nuclear\|wmd` (1) | inherited | Which parallel research queue the tech uses. |
| `AutoAssignTo` | `<unit type>` | — | For `[UNIT_CLASS]`: default class for units of that `Type`. |
| `AvailableFrom` | `<tick>` | 0 | Cannot be researched before this game tick. |
| `Image` | `"file.png"` | missing-image icon | Tree icon. |
| `Movie` | `"file"` | none | Animated tree icon. |
| `ResetBlockedZone` | `"zone_type"` / `NULL` | none | When known, clears AI "blocked zones" of that type (see unit `BlockedZoneTypeID`). |
| `AchievementProperty` | `"ACH_ID"` | none | Achievement hook. |
| `Place` | `Place Before\|After "tech"` | — | Moves the entry to another position in the tech list (display order). Written after the entry. |

Editing: `[TECHNOLOGY] "id" MODIFY`, `[TECHNOLOGY] "id" remove`, `delete LeadsTo|Parent|BlockedBy|AchievementProperty "…"`,
`reset LeadsTo|Parent|BlockedBy|AchievementProperty` ([00 §4](00-Basics.md#4-creating-replacing-and-modifying-entries)).

## 3. Built-in technologies (do not define these yourself)

| ID | Known by | Use |
|---|---|---|
| `S_FACTION_ID_0` … `S_FACTION_ID_n` | Only faction *n* | Faction-specific content: `Parent "S_FACTION_ID_3" HideLink` makes a tech available only to faction 3. |
| `PREFIX_XX` (e.g. `PREFIX_NA`) | Factions whose unit-model prefix is `XX` | Region/faction-model-specific techs: `Parent "PREFIX_NA" HideLink`. |
| `BLOCKER` | Nobody, ever | A tech with `Parent "BLOCKER"` is disabled for every faction — even `GRANT_TECH` cannot enable it. Use it to switch content off completely. |
| `BASE` | Everyone | Reserved for the game's own technologies. |
| `U_City` | Everyone | The city pseudo-unit's tech. |

## 4. Research cost and tech levels

Effective cost of a tech for a faction:

```
cost = Points × 0.01 × NextLevelMultiplier ^ max(0, TechLevel − L)
```

where *L* is the faction's current tech level **index** as computed from `TechLevels.txt` (0 for the first
level `L_1`, 1 for `L_2`, …) and `NextLevelMultiplier` comes from `TechLevels.txt` (shipped 1.5).

> Note: tech levels are written 1-based in `tech.txt` but *L* is 0-based, so a
> tech of your own displayed level already costs ×1.5 and one level above ×2.25. Keep this in mind when
> balancing `Points`.

### `TechLevels.txt`

This file defines how research raises the faction's tech level.

| Line | Meaning |
|---|---|
| `MinLevel <f>`, `MaxLevel <f>`, `NumLevels <n>` | Range of the internal tech-level value and number of levels (shipped 1, 10, 10). Level index = ⌊(value − MinLevel) ÷ (MaxLevel − MinLevel + 1) × NumLevels⌋. |
| `Level "L_k" <v>` | Associates the `[LEVEL]` techs with levels, in order. |
| `NextLevelMultiplier <f>` | Cost factor per level above the current one (see above). |
| `GeneralMultiplier <f>` | Scales how much each `Add` also raises the cap. |
| `tech "id" Add <v>` | Knowing this tech adds *v* to the value (and *v* × GeneralMultiplier to the cap). |
| `tech "id" Cap <v>` | Knowing this tech lets the value reach at least *v* (the highest known cap wins). |
| `tech "id" GrowthMult <v>` | Multiplies the automatic growth. |
| `AutoGrowth <f>` | Growth of the value per game second (0 = none). |

`ProductionEfficiency.txt` uses the same format for the faction's **nuclear efficiency** (which drives
`ProductionCostDegrades` weapons), with `Nuclear_Fuel_*` techs as caps/adders.

## 5. Patterns used in the shipped tree

* **One zero-cost tech per object.** `M_100kt_nuke_light` has no `Points` and is a `LeadsTo` child of
  `Nuclear_Fission`; the missile uses `Tech "M_100kt_nuke_light"`. Researching the parent unlocks the
  child and therefore the weapon, and you can move the weapon elsewhere in the tree by moving one link.
* **Upgrade techs** are researched techs used only in modifiers (`ImprovedBy "SAM_Mk2" Set Range 400`).
* **Modifier tags** are zero-cost techs without parents (always known) used in unit `Modifier "…"` lines
  and tested with `ImprovedBy/AffectedBy Unit "…"`.
* **Obsolescence**: `DisablingTech "Newer_Tech"` on a unit or missile removes the old version when the
  newer one is known.
* **Scripted unlocks**: give the tech `Points` (any value > 0) and `CanBeResearched No`, then grant it
  from an event script with `GRANT_TECH(FactionID, "tech")`. (A zero-cost tech without parents is always
  known, and a `BLOCKER` child can never be known, so neither works for this.)
