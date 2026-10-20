# 04 — Radars and sensors (`Units/Radars.txt`)

[Index](index.md) · [Basics](00-Basics.md) · Catalog: [A4](A4-Catalog-Radars.md)

A `[RADAR]` is any sensor a unit carries — radar, sonar, optics, satellite camera, even the "occupation
zone finder" used by armies. Units see nothing without at least one sensor. Units list their sensors with
`Radar "…"` ([01 §4](01-Units.md#4-sensors)).

```
[TYPE] "LongWave"                        // template
  PreciseTargeting No
  CanDetect Ground
  CanDetect Naval
  CanDetect Airborne
  CanDetect Missile
  CanDetect HighMissile
  RadarColor 0.02 0.05 0.16 0.15
  GlobalShowType LW_RANGES

[RADAR] "STD Long Wave"                  // shipped entry, shortened
  Tech "R_Long_wave_radar"               // required
  Type "LongWave"
  Range 400
  ImprovedBy "LW_Mk2" Set Range 450
  ImprovedBy "LW_Mk2" Set MaxHeight 250
  ImprovedBy "LW_Mk3" Set Range 500
  AffectedBy Explosion "EMP_Blast" Complex Range      // blinded while hit by an EMP…
    case self "EMP_Defence_Mk2" Multiply 0.40         // …less so with EMP hardening
    case self "EMP_Defence" Multiply 0.25
    default Multiply 0.0
  AffectedBy Unit "Aircraft_Stealth_Bonus_Modifier_1" Range 0.60   // shorter range vs stealth-tagged aircraft
  AffectedBy Unit "Bomber_Stealth_Bonus_Modifier_1" Range 0.55
```

## 1. How detection works

A sensor on unit *A* sees unit *B* when all of these hold:

1. *B*'s current class (`Ground`, `Naval`, `Subwater`, `Airborne`, `Satellite`, `Missile`, `HighMissile`,
   `SubwaterMissile`, `City`) is in the sensor's `CanDetect` set, or *B*'s unit type is listed as an extra
   `CanDetect "Unit_ID"`. A surfaced submarine counts as `Naval`.
2. *B*'s altitude ≤ the sensor's `MaxHeight` (after modifiers for this specific target).
3. *B* is not under an ice cap, unless the sensor has `CanSeeUnderIce`.
4. The distance is within the sensor's `Range`, **computed for this specific target**: every
   `AffectedBy Unit "tag"` modifier checks *B*'s modifier tags, so stealth, underground bunkers etc. are
   expressed as range multipliers on the sensors.
5. The sensor is switched on and past the unit's `SensorsActivationDelay`.

Seeing a target is not always enough to shoot it: weapons with `RequiresPreciseTargeting` need a sensor
with `PreciseTargeting Yes` that currently sees the target.

## 2. Properties

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `Tech` | `"tech_id"` | **required** | Display name (and availability of the sensor's upgrades). |
| `Type` | `"template"` | — | Copies `CanDetect` (+ extra unit types), `PreciseTargeting`, `CanCalculateLaunchPosition`, `CanSeeUnderIce`, `RadarColor`, `GlobalShowType` and `DoNotShow` from a `[TYPE]`. It does **not** copy `Range` or `MaxHeight`. Write it before overriding any of these. |
| `Range` | `<km>` | 20 | Detection range. |
| `MaxHeight` | `<km>` [`Real`] | 100 | Highest altitude it can see (ballistic missiles at apogee, satellites). ★ With `Real` in real km ([01](01-Units.md), Real heights); the shipped radars stay in game km (all above the aircraft). |
| `RangeByHeight` | `From <height> [Real] [mult\|set] <value> To <height> [Real] [mult\|set] <value> [To …]` | none | **Satellites only.** The range changes with the satellite's orbit height. Each point gives a height (game km, or real km with `Real`) and the range there: `mult` (the default, the keyword can be left out) multiplies the range, `set` gives the range in km directly. Between two points the range changes evenly with the height (in real km); below the first and above the last point it stays at their values. Heights must rise; up to 8 points. The multiplier applies to the range after its tech modifiers; a `set` value replaces it, upgrades included. A range that is 0 at the moment (e.g. a camera without a relay in range) stays 0. Example: `RangeByHeight From 2000 Real 1.0 To 35786 0.35` keeps the full range up to 2000 real km and 35 % at the geostationary height. On a unit that changes its height (an aircraft) it is ignored, with a warning in `Fatal.txt`. Not copied by `Type`. |
| `CanDetect` | `CanDetect <class>` / `CanDetect "Unit_ID"` | nothing | Detectable classes / extra unit types. List property. |
| `PreciseTargeting` | `Yes\|No` | No | Provides precise coordinates for weapons with `RequiresPreciseTargeting`. |
| `CanCalculateLaunchPosition` | `Yes\|No` | No | Reveals a hidden launcher when it sees the missile it fired. Only works together with `PreciseTargeting`. |
| `CanSeeUnderIce` | `Yes\|No` | No | Sees submarines under ice caps. |
| `RadarColor` | `r g b a` (0–1 floats) | 0 0 0.15 0.15 | Colour of the range circle. Circles of the same colour are merged, so a smaller circle with the same colour is hidden inside a bigger one. |
| `GlobalShowType` | `<group>` | none | Which "show ranges" toggle displays it: `LW_RANGES`, `SW_RANGES`, `OVERHORIZONT_RANGES`, `SONAR_RANGES`, `SPACE_RANGES`, `SATELLITE_RANGES`, `OPTICAL_RANGES`, `JAMMER_RANGES`, `SAM_RANGES`, `ABM_RANGES`, `MRBM_RANGES`, `ICBM_RANGES`. List property. |
| `IdentifiesCovert` | `[Yes\|No]` | No | A unit with hidden ownership (`HideOwnership`, e.g. spec-ops teams and bomb trucks) detected by this sensor is **identified**: the detecting faction learns its owner, also after the unit is destroyed. Without identification such a unit, its attacks and its wreck stay anonymous. Not shipped (the `Counter-spy` radar has it commented out): covert units are identified only by their destruction. |
| `DoNotShow` | `DoNotShow [Yes\|No]` | shown | Range not drawn by default. |
| `DoNotShowInEncyclopedia` | `DoNotShowInEncyclopedia [Yes\|No]` | No | Never mentioned in the Explodopedia ([14](14-Explodopedia.md)): no page, and no icon, link or row naming it on other pages. Alias `DoNotShowInExplodopedia`. A `Type` written after it does not clear it. |
| `Icon` | `"file.png"` | air-detection icon | Icon in the unit panel. |
| `MinRange`, `Sector`, `Precision` | `<float>` | 0 / 360° / 1 | Not used by detection. |

## 3. Tech modifiers on radars

Property names: `Range`, `MaxElevation` (aliases `MaxHeight`, `Elevation`). (`MinRange` and `Precision`
are accepted but have no effect.) All headers work ([06](06-Tech-Modifiers.md)). For radars, "self" is the
unit carrying the radar and "target" is the unit being looked at:

| You want | Write in the radar |
|---|---|
| Upgrade with own research | `ImprovedBy "LW_Mk3" Set Range 1000` |
| Stealth: shorter range vs tagged units | `AffectedBy Unit "Aircraft_Stealth_Bonus_Modifier_1" Range 0.60` (shipped) |
| Stealth strength per unit (tag value) | `AffectedBy Unit "My_Stealth" Range value` + `Modifier "My_Stealth" value 0.5` on the unit |
| Counter-stealth tech cancels it | `AffectedBy "Satellite_Stealth_Bonus_Modifier_1" Range 0.7 Unless "Space_radar_Mk4"` (shipped) |
| Enemy jamming | `AffectedBy InRange "EW" Complex Range` + `case`/`default` lines |
| Own support aura | `ImprovedBy InRange "Sensor_Buff" Range 1.2` |

In `AffectedBy Unit` on a radar, an `Unless`/`case` without `self`/`target` checks the **target**'s owner
for plain tech conditions; add `self` to test the radar owner's techs instead — see
[06 §7](06-Tech-Modifiers.md#61-self-and-target-in-conditions).

## 4. Editing

```
[RADAR] "STD Long Wave" MODIFY
  Range 1000
  delete CanDetect HighMissile
  delete ImprovedBy "LW_Mk2"           // remove all LW_Mk2 upgrades
  ImprovedBy "LW_Mk2" Set Range 1200

[RADAR] "Satellite EWS Display" MODIFY
  RangeByHeight From 2000 Real set 4000 To 35786 Real 0.35   // replaces any earlier RangeByHeight
//  delete RangeByHeight                                      // or: the same range at every height
```

`[TYPE]` templates cannot be modified; redefining a template with the same name replaces it (only for
radars defined afterwards).
