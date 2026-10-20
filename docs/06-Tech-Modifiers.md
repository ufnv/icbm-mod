# 06 — Tech modifiers: `ImprovedBy` and `AffectedBy`

[Index](index.md) · [Basics](00-Basics.md)

Tech modifiers change a property of a unit type, missile, radar or explosion **at run time**, depending on
technologies, unit tags, auras, lasting explosion effects or terrain. They are the main balancing tool:
almost every upgrade in the shipped game is a tech modifier.

```
// (tech names below are illustrative)
ImprovedBy "Air_refuel" Range 1.5                                   // own tech: ×1.5
ImprovedBy "Powerful_Engine" Set Speed 65                            // own tech: = 65
ImprovedBy Unit "Advanced_Sonar" Add Range 100                      // own tech + unit has that tag: +100
AffectedBy Unit "Bomber_Stealth_Bonus_Modifier_1" Range 0.55        // target has that tag: ×0.55 (shipped)
AffectedBy InRange "EW" Sub Min 100 Range 500 Unless InRange "ACTIVE_EW_DEFENCE"
```

---

## 1. General form

```
ImprovedBy | AffectedBy   [Unit | InRange | Terrain | Explosion]  "name"   [AND <condition>]…
    <body>                                    — or —      { <body> <body> … }

<body> :=   [Modify Weapon "missile"]  <operator>  <Property> ["tag"]  <value | value | Complex …>  [Unless <condition>]
         |  Movie …                    (appearance, see §6)
         |  Config "name" <Weapon lines>      (units only, see §6)
         |  Radar "radar" …                  (units only, see §6)
```

* A **header** decides *when* the modifier is active.
* `AND <condition>` adds extra conditions (up to 32) that must also hold.
* `{ … }` lets one header carry several bodies (each body may have its own `Unless`):

  ```
  ImprovedBy "Generation_4_Aircraft"
  {
    Set Size 0.03
    Set Speed 1000
    Set Range 3750
  }
  ```

## 2. Headers

"Self" = the unit that owns the object being modified (for a missile: the launching unit; for a radar: the
unit carrying it). "Target" = the other unit involved (the unit hit, the unit being looked at).

| Header | Active when | Typical use |
|---|---|---|
| `ImprovedBy "tech"` | Self's faction knows `tech`. | Research upgrades. |
| `ImprovedBy Unit "tag"` | Self's faction knows `tag` **and** self's unit type has `Modifier "tag"`. | Unit-specific upgrades; per-unit values via `value`. |
| `ImprovedBy InRange "missile"` | Self is inside the range of an **active** `missile` weapon of an own or allied unit. | Buff auras (research, espionage, force fields). |
| `ImprovedBy Terrain "group"` | Self (a ground unit) stands on terrain of that group (from the map's TerrainTypeMap). | Terrain bonuses. |
| `AffectedBy "tech"` | The **target's** faction knows `tech`. | Enemy counter-research (e.g. target's armour tech reduces your damage). |
| `AffectedBy Unit "tag"` | The target's faction knows `tag` and the target's unit type has `Modifier "tag"`. | Stealth, hardening, special vulnerabilities. |
| `AffectedBy InRange "missile"` | Self is inside the range of an active `missile` weapon of an **enemy** unit. | Jamming, debuff auras. |
| `AffectedBy Explosion "explosion"` | Self was hit by that explosion and its `LastingEffect` is still running. | EMP, chemical, cyber effects. |
| `AffectedBy Terrain "group"` | The target (a ground unit) stands on that terrain group. | Cover/terrain protection. |

Notes:

* `InRange` works only for weapons that are switched on, and for at most 32 different aura weapons per
  unit type. The aura's reach is the weapon's `Range`.
* For cities (`VirtualCity`), "self" is the city.
* Explosion modifiers written **in an explosion entry** use the attacker as self and the unit hit as target.

## 3. Operators

| Operator | Written | Result |
|---|---|---|
| Multiply (default) | `Range 1.5` or `Multiply Range 1.5` | value × 1.5 |
| Set | `Set Range 850` | value = 850 |
| Set Max | `Set Max Range 850` | value = max(value, 850) |
| Set Min | `Set Min Range 850` | value = min(value, 850) |
| Add | `Add Range 100` | value + 100 |
| Sub | `Sub Range 100` | value − 100 |
| Clamped variants | `Add\|Sub\|Multiply  Min <a> [Max <b>] \| Max <b>` then property and value | apply, then clamp to ≥ a and/or ≤ b. Example: `Sub Min 100 Range 500` = subtract 500 but not below 100. |
| Complex | `Complex Range` followed by `case`/`default` lines | choose an operation by condition (§5) |
| Delete | `Delete Modifier "tag"` | removes a unit tag (only with `Modifier`) |

`value` instead of a number (only in `Unit` headers or `case Unit`): uses the tag's value from the unit's
`Modifier "tag" value <v>` line.

## 4. Property names

The same keyword can mean different things on different objects (they share one
stored value). **Only use the names listed for the object you are modifying** — a name from another column is
accepted silently but changes a different property.

| Keyword | Unit type | City (`VirtualCity`) | Missile | Radar | Explosion | `Modify Weapon` |
|---|---|---|---|---|---|---|
| `Range` | flight range | — | attack range | detection range | — | — |
| `MinRange` | = Size ⚠ | = Size ⚠ | min range | (no effect) | — | — |
| `Size` | size | city size | = MinRange ⚠ | — | — | — |
| `Precision` | = MaxNumberOnMap ⚠ | = MaxNumberOnMap ⚠ | precision | (no effect) | — | — |
| `MaxNumberOnMap` | max on map | max on map | = Precision ⚠ | — | — | — |
| `Damage` | = VirtualSpeed ⚠ | — | explosion damage | — | — | — |
| `VirtualSpeed` | virtual speed | — | = Damage ⚠ | — | — | — |
| `Speed` | speed ¹ | — | speed ¹ | — | — | — |
| `TurnSpeed` | turn speed | — | turn speed | — | — | — |
| `CanBeIntercepted` | = RepairRange ⚠ | = RepairRange ⚠ | interception chance | — | — | = Load ⚠ |
| `RepairRange` | repair range | repair range | = CanBeIntercepted ⚠ | — | — | = Load ⚠ |
| `ProductionCost` | cost | — | cost | — | — | — |
| `MaxElevation` / `Elevation` / `MaxHeight` | max altitude | — | max altitude | max height | — | — |
| `MinElevation` | min altitude | — | min altitude | — | — | — |
| `Power` | hit points | city power | missile hit points | — | — | — |
| `DisassembleTime` | disassemble time | — | = LeadGuidance ⚠ | — | — | — |
| `LeadGuidance` | = DisassembleTime ⚠ | — | lead guidance | — | — | — |
| `Heads` / `Launch` / `Production` / `AttackDelay` / `LastingEffect` | **AttackDelay** | **Production** | **Heads** | — | **LastingEffect** | **Launch** |
| `FakeHeads` / `Time` / `Science` / `AttackOnMove` / `LastingDamage` | **AttackOnMove** | **Science** | **FakeHeads** | — | **LastingDamage** | **Time** |
| `ResupplyRange` / `FullEffectRange` / `MinHealthPercentage` | **ResupplyRange** | **ResupplyRange** | **FullEffectRange** | — | **MinHealthPercentage** | — |
| `AffectedRange` / `Espionage` / `ModelLaunchTime` | **ModelLaunchTime** | **Espionage** | **AffectedRange** (outer blast radius) | — | — | — |
| `Load` | — | — | — | — | — | (no effect) |
| `CanBeBuilt` | can be built (0/1) | — | can be built | — | — | — |
| `Movie` | appearance (§6) | — | appearance (§6) | — | — | — |
| `Modifier` | unit tags (§7) | city tags | — | — | — | — |

In the rows with several keywords, every keyword of the row is interchangeable; the bold word is what it
actually changes on that object. For readability write the matching word (`Production` on a city,
`AttackDelay` on a unit, `Heads` on a missile).

¹ Do not change `Speed` with dynamic headers (`InRange`, `Explosion`, `Terrain`, `AffectedBy`); movement
code caches it. Use simple `ImprovedBy` / `ImprovedBy Unit` only.

### Modify Weapon

On a unit: `ImprovedBy "tech" Modify Weapon "missile" <op> Launch|Time <value>` changes that weapon
in all of the unit's configs — salvo size or reload time (`Load` is accepted but currently has no effect). With `Set`/`Add`/`Sub`
the `Time` value is in reload units like the `Weapon` line; with `Multiply` it is a factor.
`Modify Weapon` cannot be used inside a weapon-config upgrade.

## 5. Complex modifiers

```
AffectedBy InRange "EW" Complex Range
  case InRange "ACTIVE_EW_DEFENCE" Multiply 1.0
  case "Anti-Jammers_Mk3"          Multiply 0.95
  case "Anti-Jammers_Mk2"          Multiply 0.85
  default                          Multiply 0.75
```

* When the header is active, the `case` lines are tested **in order and the first true one is applied**;
  `default` always matches — put it last.
* Each case has its own operator (including clamped variants) and value (or `value` for `case Unit`).
* Case conditions (same syntax as `Unless` and `AND`):

| Condition | True when |
|---|---|
| `"tech"` | the checked faction knows `tech` |
| `Unit "tag"` | the checked faction knows `tag` and the checked unit type has that tag |
| `InRange "missile"` (optionally `InRange Allied\|Own "missile"`) | the checked unit is inside an own/allied active `missile` aura |
| `InRange Enemy "missile"` | inside an enemy active `missile` aura |
| `Explosion "explosion"` | the checked unit is under that explosion's lasting effect |
| `Terrain "group"` | the checked unit stands on that terrain group |
| `NOT <condition>` | inverts it |

Up to 32 cases.

## 6. Unless and AND

* `Unless <condition>` at the end of a body: the body is **not** applied if the condition is true
  ("this tech counters that effect"). One `Unless` per body.

  ```
  AffectedBy "Satellite_Stealth_Bonus_Modifier_1" Range 0.7 Unless "Space_radar_Mk4"
  ```
* `AND <condition>` right after the header name: all conditions must be true for the header to be active.

  ```
  ImprovedBy Unit "Naval_Sonar" AND InRange "Sonar_Buoy" Range 1.3     // illustrative names
  ```

### 6.1 `self` and `target` in conditions

Write `self` or `target` right after `case`, `Unless`, `AND` (after an optional `NOT`) to choose whose
faction/unit is checked:

| Header type | Checked by default | To check the other side write |
|---|---|---|
| All `ImprovedBy …`, and `AffectedBy InRange` / `AffectedBy Explosion` | self | `target` |
| `AffectedBy "tech"`, `AffectedBy Unit`, `AffectedBy Terrain` | target | `self` |

Example — reduce damage against hardened targets unless the attacker has better guidance:

```
AffectedBy Unit "BM_Accuracy_Damage_Penalty" Complex Damage
  case self "Advanced_Inertial_Guidance" Multiply 1
  case self "Improved_Inertial_Guidance" Multiply 0.75
  default Multiply 0.5
```

## 7. Special bodies (units and missiles)

### Appearance: `Movie`

Simple `ImprovedBy "tech"` only, no operator:

| Form | Effect |
|---|---|
| `ImprovedBy "tech" Movie Image "icon.png"` | Replace only the icon (missiles, units). |
| `ImprovedBy "tech" Movie "sprite.midx" [Icon "icon.png"] [RoundIcon "round.png"]` | Replace the map sprite, optionally the icons (icon defaults to frame `IconIDX` of the sprite, round icon to the icon). |
| `ImprovedBy "tech" Movie Model "model.midx"` | Replace the 3D model. Can be combined with the previous form in the same `{ }` block. |
| ★ *(sizes)* | An upgrade's picture or model that is drawn bigger or smaller in its frame than the unit's first one gets a `Scale` in its own `.midx` ([12](12-Config-Files.md#pictures-and-models)); the upgrade itself has no size (a `DrawSize` here was read before, it is not any more). |

`delete ImprovedBy ALL Movie` removes all appearance modifiers (handy in `MODIFY` entries before adding
new ones).

### Weapon configs and radar sets (units only)

Simple `ImprovedBy "tech"` only:

* `ImprovedBy "tech" Config "name"` + `Weapon …` lines — adds or replaces a config when `tech` is known.
  Written right after a config's own weapon list, `ImprovedBy "tech"` + `Weapon` lines replaces that
  config's contents ([01 §3.3](01-Units.md#33-upgrading-configs-with-technologies)).
* `ImprovedBy "tech" Radar "radar" [Radar …]` — replaces the whole radar list when `tech` is known
  ([01 §4](01-Units.md#4-sensors)).

## 8. Modifier tags

With the property `Modifier "tag"` a tech modifier adds, changes or removes a **tag** on the unit (or city)
at run time; other objects then react to the tag through `AffectedBy Unit "tag"`/`ImprovedBy Unit "tag"`.

```
[UNIT] "VirtualCity" MODIFY
  ImprovedBy InRange "FORCE_FIELD" Set Modifier "INVINCIBLE" 1.0     // cities under the field get the tag

[MISSILE] "Low-power nuclear bomb" MODIFY
  AffectedBy Unit "INVINCIBLE" Set Damage 0                            // …and take no damage

[UNIT] "Stealth_Bomber" MODIFY                                         // illustrative unit
  AffectedBy InRange "EW" Delete Modifier "Bomber_Stealth_Bonus_Modifier_1"          // loses stealth inside enemy EW
```

Tag changes are evaluated only for these headers: simple `ImprovedBy "tech"`, `ImprovedBy InRange`,
`AffectedBy InRange`, `AffectedBy Explosion`. (`ImprovedBy Unit`, simple `AffectedBy`, `AffectedBy Unit`
and `Terrain` headers do not change tags.) A tag set to value 0 still exists — use `Delete` to remove it.

## 9. Evaluation order

For each property the base value is modified in this order; within each group, in the order the lines
appear (across `MODIFY` entries, appended lines come last):

1. simple `ImprovedBy "tech"`
2. `ImprovedBy Unit`
3. `ImprovedBy Terrain`
4. `ImprovedBy InRange`
5. `AffectedBy InRange`
6. `AffectedBy Explosion`
7. simple `AffectedBy "tech"`
8. `AffectedBy Unit`
9. `AffectedBy Terrain`

Because operations are applied in sequence, `Set` discards everything before it and multiplications
compound: `ImprovedBy "A" Range 1.2` + `ImprovedBy "B" Range 1.2` = ×1.44. To make an upgrade chain where
the last known level wins, use `Set` in increasing order (the shipped data does this: `Set Range 850`,
then `Set Range 1000`).

Steps 1–2 (and a Complex whose cases only test techs) are cached per faction and cheap. Steps 3–9 and any
`value`, `InRange`, `Explosion` or `Terrain` condition are evaluated per unit and cost CPU on large maps.

## 10. Deleting modifiers

| Form | Removes |
|---|---|
| `delete ImprovedBy "tech"` | All simple `ImprovedBy` lines with that tech, for every property. |
| `delete ImprovedBy Unit "tag"` | All `ImprovedBy Unit "tag"` lines. |
| `delete ImprovedBy InRange "missile"` | All `ImprovedBy InRange "missile"` lines. |
| `delete ImprovedBy ALL <Property>` | All simple `ImprovedBy` lines for that property (`… Unit ALL <Property>`, `… InRange ALL <Property>` likewise). |
| `delete AffectedBy …` | Same forms, plus `Explosion "explosion"`. |
| `reset AffectedBy` | Every `AffectedBy` of the object. |
| `reset ImprovedBy` | Every `ImprovedBy` of the object. |

