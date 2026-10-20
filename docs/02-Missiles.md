# 02 — Missiles and weapons (`Units/Missile_types.txt`, `Units/Missile_defs.txt`)

[Index](index.md) · [Basics](00-Basics.md) · Catalog: [A2](A2-Catalog-Missiles.md)

A `[MISSILE]` is anything a unit can fire or apply: missiles, bombs, shells, torpedoes, lasers, cyber
attacks, espionage/research buffs, jammers. It travels from the launcher to a target point (or acts
instantly) and then produces its **explosions** ([03](03-Explosions.md)), which do the actual damage.

```
[MISSILE] "SAM"                         // shipped entry, shortened
  Tech "M_Surface_to_air_missile"       // required: availability + display name
  Type "AntiAir"                        // template: targeting classes etc. — write it FIRST
  Icon "Units/Images/Missiles/SAM.png"  // required
  Explosion "std_bomb_small"            // required (one or more)
  Range 300
  Speed 3000
  Precision 0.16
  MaxElevation 75
  CanBeLimited false
  ImprovedBy "SAM_Mk2" Set Range 400
  ImprovedBy "SAM_Mk2" Precision 0.75            // 25 % more accurate
  AffectedBy Unit "ECM_Bonus_1" Precision 1.075  // targets with ECM are harder to hit
  AffectedBy Unit "ECM_Bonus_1" Damage 0.90
```

---

## 1. Templates: `[TYPE]` in `Missile_types.txt`

`[TYPE] "Name"` defines a template with the same properties as a missile. `Type "Name"` inside a missile
copies from the template: targeting classes (`CanBeUsedAgainst`, `Affects`, extra target types),
`RequiresPreciseTargeting`, `Subwater*`, `GlobalShowType`, `AutoSlowDown`, Geneva and AI categories,
`SingleAttack`, `Ballistic`, `FreeFalling`, `CanRetarget`, `MaximizeExposure`,
`PreferPopulationOverDistance`, `ProductionCostDegrades`, `Class`, `Hidden`, `HideRange`, `Switchable`,
`CanBeLimited`, `MaxNumberToOrder`, `HideNumberOfMissiles`, `DoesNotTriggerWarOnAttack`, drawing
settings, **and the numeric stats** (`Range`, `MinRange`, `Speed`, `Power`, `Precision`, `TurnSpeed`,
`CanBeIntercepted`, `ProductionCost`, elevations, `LeadGuidance`, `AttackAngle`), `ProducedByAnotherUnit`,
`AIHint`s and achievement properties.

> ⚠ Because `Type` also copies the numeric stats, **write `Type` before any stat**. A `Range` written above
> the `Type` line is overwritten by the template's value.

The shipped templates (see [A2](A2-Catalog-Missiles.md#templates)) are named by role:
`Default`, `SemiGuided`, `LandAttack`, `Nuke`, `NukeArtillery`, `Torpedo`, `TorpedoNuke`, `AntiShip`,
`AntiAir`, `AntiAirNuke`, `AntiAirAll`, `AntiMissile`, `AntiMissileMidcourse`, `AntiMissileTerminal`,
`AntiMissileAA`, `AntiRadiation`, `AntiSat`, `Laser_Weapon`, `CFLaser`, `DepthCharge`, `Chemical`,
`ChemicalArtillery`, `Biological`, `Army`, `Small Arms`, `Massacre`, `CyberAttack`, `No Attack`.

## 2. Targeting classes

| Property | Syntax | Meaning |
|---|---|---|
| `CanBeUsedAgainst` | `CanBeUsedAgainst <class>` or `CanBeUsedAgainst "Unit_ID"` | What the weapon may be **aimed at**. Classes: `Ground`, `Naval`, `Subwater`, `Airborne`, `Missile`, `HighMissile`, `SubwaterMissile`, `Satellite`, `City`, `AbstractPosition` (a point on the map). A quoted unit ID adds one specific unit type (e.g. anti-radiation missiles against radar sites). List property. |
| `Affects` | `Affects <class>` | What the explosion **damages** in addition to the aim classes (collateral). Every `CanBeUsedAgainst` class is automatically in `Affects`. Example: nukes aim at ground/naval/city but also affect `Airborne` and `Subwater`. |
| `RequiresPreciseTargeting` | `Yes\|No` | Yes = can only be fired at a target that one of the faction's radars with `PreciseTargeting` currently sees ([04](04-Radars.md)). |
| `AttackAngle` | `<degrees>` | The target must lie within this cone around the launcher's heading (default 360). Forced to 360 for `Ballistic` missiles and 60 for `FreeFalling` ones. |

How a missile counts as a target for other weapons (its own class):

* `Ballistic` with `MaxElevation > 0` → `HighMissile` (hit by mid-course interceptors, seen by
  over-the-horizon radars);
* `Subwater Yes` → `SubwaterMissile`;
* otherwise → `Missile`.

## 3. Flight and hit statistics

All numeric stats can be changed by tech modifiers ([06](06-Tech-Modifiers.md#4-property-names)).

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `Range` | `<km>` | 20 | Maximum attack distance. |
| `MinRange` | `<km>` | 0 | Cannot be fired at closer targets. |
| `Speed` | `<float>` | 100 | Flight speed (same scale as unit speed). Scaled by the global `GlobalSpeedModifier` of this file. Do not change with dynamic modifiers. |
| `TurnSpeed` | `<float>` | auto | Turning rate. If not set it is derived from `Range` and `AttackAngle`; loading fails with "Turn speed too slow" if the turn rate makes the effective range less than half of `Range`. Ballistic missiles do not turn. |
| `Precision` | `<km>` | 1 | Maximum miss distance: the impact point is moved by a random distance 0…`Precision` in a random direction. Smaller = more accurate. For weapons that hit missiles, a value below 2 means the hit deviates by that amount around the target. ★ A non-ballistic weapon fired at a unit uses it only if one of its explosions has a `Range` of 1 km or less; one bursting wider (all its explosions' `Range` above 1 km) hits right on the target, its `Precision` unused (see [Hitting units](03-Explosions.md#2-hitting-units)). |
| `CanBeIntercepted` | `0…1` | 0 | Chance that **one interceptor hit on this missile counts**. 0 = interceptors never engage it automatically and hits (practically) never count. A counted hit subtracts the interceptor's explosion damage from this missile's `Power`. |
| `DisableCanBeIntercepted` (alias `DisableCanBeInterceptedBitscale`) | class names | none | ★ Interceptor classes that can never shoot this missile down: against them its `CanBeIntercepted` is 0 and they are not fired at it. Classes, by the interceptor weapon: `EMP` (one of its explosions is an EMP), `Laser` (`DrawLaser` or `Immediate`), `DirectHit` (`DirectLaunch`: CIWS, C-RAM), `Missile` (any other); also `All`, and `None` to clear the earlier ones (for mods). Several on one line or repeated lines add up. Example: the railgun slug, `CanBeIntercepted 0.05` with `DisableCanBeIntercepted DirectHit Missile EMP` — only lasers can stop it. |
| `Power` | `<float>` | 1 | Hit points of the missile in flight (not its damage). |
| `MaxElevation` (alias `Elevation`), `MinElevation` | `<km>` [`Real`] | 0 | Flight altitude band. ★ With `Real` in real km ([01](01-Units.md), Real heights): shipped for the anti-aircraft weapons (small arms 1.5, MANPAD 5, AA gun 13, light SAM and plane gun 15, AA laser 27, SAM and AAM 30, LAAM 40), each reaching the same aircraft as before; the anti-missile ones stay in game km. A ballistic missile with `MaxElevation > 0` is a `HighMissile`; radars need a `MaxHeight` above it to see it at apogee. For interceptors this is the altitude band in which they can engage. |
| `LeadGuidance` | `<float>` | 0 | > 0 makes interceptors aim ahead of the target (prediction). Experimental; tune by testing. |
| `Ballistic` | flag | off | Ballistic trajectory (no steering, may be high-altitude). |
| `FreeFalling` | flag | off | Unpowered bomb (use with `Ballistic`): drops at the target, 60° attack cone. |
| ★ `DirectLaunch` | flag | off | Direct fire (a gun's round, a railgun slug): fired straight at its target from any launcher, not along a moving launcher's (a ship's) heading turning toward it after, nor spread among its launchers; and drawn flying a straight line to it (not curving down onto a low target with the drawn heights' scale). Its end and whether it hits are decided as it is fired (its target led, the hit rolled as at the end before), so it flies straight there: a miss (or a shot whose target is gone on the way) flies on past and is gone, exploding only where it reaches some unit; a missile it kills is drawn meeting it (the earliest killing shot's), one it only damages keeps its way. |
| ★ `MinExplosionHeight` | `<km>` [`Real`] | 0 | A ballistic missile goes off at least this high over its target: its trajectory ends there, and its explosion is there (from 61 game km, 30 real, its `Variant Space`, see [03 §1.3](03-Explosions.md#13-variants)). The reach of its effects is measured along the ground, so it stays the same; but the interceptors only reach it within their own `MaxElevation` (the terminal ABMs, 200–250 km, never catch one bursting at 400 km). A falling bomb goes off no higher than it was dropped from. Shipped: 400 on the EMP missiles (Starfish Prime, 1962). |
| ★ `MaxVisualAimAngle` | `<degrees>` | 10 | Visual only. Fired at a unit with a model, the projectile is drawn bending onto a spot on the model, where its explosion is then drawn (see [03](03-Explosions.md), hits on models); it only takes the spots it reaches turning aside at most this much, as seen from where it was fired, and between half and twice as far as the unit's middle along its way. Smaller: the hits stay near its line of fire. None of them (0, or fired from right beside or inside a big unit's model): it flies straight and its explosion is drawn where it hit. Up to 80. |
| `Subwater` | `Yes\|No` | No | Travels under water (torpedo): also sets `SubwaterLaunch` and `CheckSubwaterRoute`. |
| `SubwaterLaunch` | `Yes\|No` | No | Can be launched by a submerged unit. |
| `CheckSubwaterRoute` | `Yes\|No` | No | The path to the target must be through water (depth charges, torpedoes). |
| `CanRetarget` | `Yes\|No` | No | Picks a new target automatically if the original one disappears. |

## 4. Warheads, explosions and MIRVs

| Property | Syntax | Meaning |
|---|---|---|
| `Explosion` | `Explosion "explosion_id"` | **Required.** List property: every listed explosion is applied at impact (e.g. a blast plus a "guaranteed casualties" explosion). Up to 64. |
| `Heads` | `Heads <n> "missile_id"` | MIRV: the missile splits into `n` warheads of the given missile type. Often written on the same line as the explosion: `Explosion "nuke_250" Heads 6 "250kt MRBM MIRV warhead"`. The bus's Geneva/AI categories are copied to the warhead type. |
| `FakeHeads` | `FakeHeads <n> "missile_id"` | Decoy warheads released with the real ones. `Heads + FakeHeads ≤ 20`. |
| `SplitPathPercent` | `<0…1>` | Where along the path the warheads separate (default 0.66). |
| `SplitMinDist` | `<km>` | Separation happens at least this far before the target. |
| `IndependentTargeting` | `Yes\|No` | Warheads may be redirected to other visible enemy units that are closer than 75 % of the distance to the original target (only for unit targets, not cities). |

## 5. Production and availability

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `Tech` | `"tech_id"` | **required** | Availability and display name. |
| `DisablingTech` | `"tech_id"` | none | Weapon becomes unavailable when the owner knows this tech (used to swap in improved versions). |
| `Class` | `"UC_…"` / `NULL` | auto | Unit class for production UI (`UC_Nuke_Weapon`, `UC_Nuke_Tac_Weapon`, `UC_Spec_Weapon`, `UC_Non_Nuclear_Weapons`, …). |
| `ProductionCost` | `<float>` | 0 | Build cost. Only weapons with a cost > 0 appear in the production list; 0 = the weapon exists only as unit stock (guns, lasers, buffs). |
| `ProductionCostDegrades` | flag | off | Cost is multiplied by the faction's **nuclear efficiency** factor (1 ÷ current efficiency), so nukes become cheaper as the match's efficiency grows (see `TechLevels.txt`/match settings). |
| `ProducedByAnotherUnit` | flag | off | Built by a unit with `Produces`, not in the faction's production. |
| `MaxNumberToOrder` | `<int>` | unlimited | Queue limit. |
| `CanBeBuilt` | `Yes\|No` | Yes | Tech-modifiable number (0 = no). |

## 6. Rules of engagement and politics

| Property | Syntax | Default | Meaning |
|---|---|---|---|
| `GenevaCategory` | `GenevaCategory "category" [Yes\|No]` | none | Adds (or with `No` removes) a Geneva category. Categories are what the diplomacy "weapon ban" offers operate on. Must be declared with `[GENEVA_CATEGORY]`. |
| `AICategory` | `AICategory "category" [Yes\|No]` | none | AI weapon category (used by the AI's escalation logic and by scripts via `AI_CATEGORY`). Declared with `[AI_CATEGORY]`. |
| `CanBeLimited` | `Yes\|No` | Yes | Whether the weapon can be disabled by Geneva bans / limited-escalation rules. Set No for conventional weapons. |
| `Switchable` | `Switchable [Yes\|No] [ON\|OFF]` | No | Player can switch the weapon on/off; `OFF` = off by default. Scripts use `Weapon_Switch`. |
| `DoesNotTriggerWarOnAttack` | `Yes\|No` | No | Using it does not start a war (espionage, cyber). |
| `SingleAttack` | flag | off | Firing this weapon is the whole attack — the unit does not add other weapons to the same salvo, and a target that only this weapon can hit counts as "single attack" (nukes). |
| `MaximizeExposure` | `Yes\|No` | No | AI/war planner spreads these weapons to cover more area instead of focusing. |
| `PreferPopulationOverDistance` | `Yes\|No` | No | AI picks city targets by population rather than proximity. |
| `AutoSlowDown` | flag | off | In single-player (if enabled in settings) the game slows down when such a missile is launched at or by the human player. |

### Declaring categories (in `Missile_types.txt`)

```
[GENEVA_CATEGORY] "Chemical" Name 3260     // Name = string ID in UI.lng
[AI_CATEGORY] "Strategic Nuclear"          // Name optional
```

At most 32 Geneva categories and 32 AI categories.

## 7. AI hints

`AIHint` gives the AI a base value when choosing a weapon config. 1.0 is normal, 0 means "never useful",
10 means ten times better; the final score is further multiplied by target value, precision vs target
size, damage vs remaining health, etc. A 0 cannot be raised by other factors.

| Form | Meaning |
|---|---|
| `AIHint CounterValue <v>` | Value against cities / population (default 1; automatically 0 if the weapon cannot hit cities). |
| `AIHint CounterForce <v>` | Value against military units (default 1). |
| `AIHint Specific "Unit_ID" <v>` | Value against a specific unit type (e.g. chemical weapons vs armies). |
| `AIHint Specific "Unit_ID" Delete` | Removes a specific hint (useful in `MODIFY`). |

## 8. Display and sound

| Property | Syntax | Meaning |
|---|---|---|
| `Icon` | `"file.png"` | **Required.** Weapon icon. |
| `RoundIcon` | `"file.png"` | Round icon (defaults to `Icon`). |
| `Movie`, `Model` | `"file"` | 2D sprite / 3D model in flight. |
| `DrawSize`, `ModelDrawSize`, `AbstractDrawSize` | `<float>` | Size on screen (default 8): `DrawSize` the picture, ★ `ModelDrawSize` the size among the 3D models (default `DrawSize`), `AbstractDrawSize` the zoomed-out icon. `ModelDrawSize` is its real size next to the units' models: a projectile with a `Model` is drawn that big; one with a picture only (`Movie`: a shell, a tracer, a cruise missile) turns into that size as it zooms in to the models (its picture as long as its model would be), in the terrain views at once. Shipped: by the real lengths, squeezed (a round 2, a shell or a railgun slug 3, bombs 3–5, the Tsar bomb 8, an air-to-air missile 7, a cruise missile 8, a SAM 9, an SRBM 10, an ICBM 14–16). |
| `DrawNuke` | flag | Draw as a nuclear missile (and enables the trajectory trail). ★ It is marked by what it carries (its `Explosion`s' types): a nuclear or EMP warhead with a red ring when zoomed out and a red head on its trail zoomed in, a biological one violet; the decoys a MIRV carries (`FakeHeads`) pass for its warheads; anything else (a kinetic rod) is not marked. It is always drawn where it really is. |
| `DrawBomb` | flag | Draw as a bomb (`DrawNuke` + `DrawBomb` = nuclear bomb). |
| `DrawLaser` | flag | Draw as a beam: a white-hot core in a coloured glow, a glow at the muzzle (the weapon's `LaunchPoint` on the unit's model) and on the target; `Color`, `DrawSteps`, `DrawCycles` and the `Laser…` properties below control it. |
| `Immediate` | flag | Instant effect with an invisible beam (hit-scan). |
| `DrawWave [Passive]` | flag | Draw as a wave (jammers, EMP-like effects). |
| `Color` | `"RRGGBBAA"` / `RGB r g b` / `RGBA r g b a` | Beam colour: its glow; the alpha is its strength (default 255 77 51 191, a red beam). Alpha 0: no beam drawn. |
| `DrawSteps`, `DrawCycles` | `<int>` | Beam timing (defaults 3 and 1): it lasts `DrawSteps` × `DrawCycles` ticks (60 a second at normal speed) and hits at the end; a pulsed beam's pulse runs to the target every 2 × `DrawSteps` ticks (at least 6). |
| ★ `LaserCore` | colour, as `Color` | The beam's white-hot core (default white). |
| ★ `LaserStyle` | `Pulse` \| `Steady` | `Pulse` (default): a bright pulse runs to the target, the beam dimmer around it. `Steady`: an even beam, for the big continuous lasers. |
| ★ `LaserWidth` | `<float>` (0.1–10) | The beam's width, times the usual (default 1). |
| `Trajectory` | `Trajectory [Style Missile\|Tracer\|Shell\|Railgun\|Wake\|Gas] [Disabled] [StandardBlend] [MaxPoints n] [MaxLength km] [WidthMult f] [StartColor "RRGGBBAA"] [EndColor "RRGGBBAA"] [BlendR f] [BlendG f] [BlendB f] [BlendA f]` | Trajectory trail. Defaults: 200 points, full length, white → transparent, blend powers 1/2/4/1. Lower `MaxPoints` (≈20) and `MaxLength` (≈1000) for short-range weapons to save performance. ★ `Style` sets how it looks. `Missile` (default) follows the height: in space a thin glowing line with a white-hot core and light running along it; in the air (below about 40 km in the game's heights) a pale smoke trail spreading behind; a warhead coming down through the upper air glows orange instead. `Tracer` (gun rounds): a short bright streak, hot at the round, at any height. `Shell`: a thin warm streak with a short wisp of smoke. `Railgun`: an intense crackling streak with an ionised glow (give it blue-white `StartColor`/`EndColor`). `Wake` (torpedoes): white foam spreading behind. `Gas` (chemical, biological): a wide soft billowing cloud in the trail's colours. The trail reaches the projectile where it is drawn and, after it is gone, fades away from its tail: in 20 ticks (a tracer), 40 (a shell), 90 (a missile), 45 (a railgun), 150 (a wake) or 240 (gas); 60 ticks are a second at normal speed. ★ A ballistic missile flying out of the air (its `MaxElevation` above 80 km, with the `Missile` style: not gun rounds, shells, rocket pods, torpedoes, bombs or warheads) also leaves a launch plume, on its own: the thick column of smoke of its climb through the air (below 80 km), staying where it was left after the missile has flown on, widening and thinning out over about 20 seconds. ★ A nuclear burst clears the smoke around it as its flash grows (1.5 × its `FullEffectRange`, at least 5 km): its own warhead's last stretch, plumes and wakes in the blast. ★ A MIRV's warheads' trails fan out from where its bus released them, with a glint and the thrusters' gas there (the emulated explosion `MIRV_Split` of `explosion.txt`, `Units/Emulated/MIRVSplit.txt`). |
| `SmokeSpeedMult`, `SmokeSizeMult`, `LaunchLightSize` | `<float>` | Launch smoke and flash (high ballistic missiles get defaults 1 and 50). The smoke is the emulated explosion `Launch_Smoke` of `explosion.txt` (`Units/Emulated/LaunchSmoke.txt`), drawn on the launcher's model at its exhaust, a quarter of the model's height up (a ship's deck), `DrawSize` launcher lengths across times `SmokeSizeMult` (a ship's: `Launch_Smoke_Naval` when there is one, DrawSize 0.5 shipped: a ship is much longer than a silo); without that type the old smoke sprites (`SmokeSpeedMult` is theirs). ★ A submarine makes no smoke: surfaced (or firing a missile it cannot fire under water) only the launch plume; submerged a short burst of white spray where the missile breaks the surface (`Launch_Spray`, `Units/Emulated/LaunchSpray.txt`; nothing without that type). |
| `Sound` | `Sound <id> [or <id>]… [Priority n] [SoundSize f] [Volume f] [Speed f] [MuteLength f]` | Launch sound, random among up to 8. |
| `Hidden` | `Yes\|No` | Not listed in the unit's weapon panel or diplomacy screens (internal effects). |
| `DoNotShowInEncyclopedia` | `[Yes\|No]` | Never mentioned in the Explodopedia ([14](14-Explodopedia.md)): no page, and no icon, link or row naming it on other pages. Alias `DoNotShowInExplodopedia`. Its MIRV warheads are left out with it. A `Type` written after it does not clear it. Default No. |
| `HideRange` | `Yes\|No` | Range circle not drawn. |
| `HideNumberOfMissiles` | `Yes\|No` | Stock count not shown. |
| `GlobalShowType` | `GlobalShowType <group>` | Range-display group: `SAM_RANGES`, `ABM_RANGES`, `MRBM_RANGES`, `ICBM_RANGES`, `JAMMER_RANGES`, `LW_RANGES`, `SW_RANGES`, `OVERHORIZONT_RANGES`, `SONAR_RANGES`, `SPACE_RANGES`, `SATELLITE_RANGES`, `OPTICAL_RANGES`. List property. |
| `InRangeStringID` | `<strID>` | Text shown in the unit panel of a unit that is inside this weapon's range (aura effects). |
| `FixedRotationAngle`, `ForceMipMap` | `Yes\|No` | Sprite options. |
| `SimplifiedVisibilityCheck` | `Yes\|No` | Cheaper visibility test for short-lived projectiles (bombs, shells). |
| `AchievementProperty` | `"ACH_ID" [check "tech"]` | Achievement hook. |

## 9. Global settings (top level of the missile files)

| Setting | Default | Meaning |
|---|---|---|
| `GlobalSpeedModifier <f>` | 1 | Multiplies every missile's speed. |
| `MinMissilesPerTarget <n>` | 2 | Interceptors fired at one target before other defences redistribute. |
| `MaxMissilesPerTarget <n>` | 1024 | Maximum interceptors that will engage one target. |

(`GlobalMissileLaunchDelayModifier`, which scales reload times, lives in `Units.txt`.)

## 10. Weapons that are not missiles

Buffs, debuffs and utility effects use the same format. The usual pattern:

1. A missile with `Type "No Attack"` (or a narrow template), `Hidden`/`HideRange`, a large stock and
   `Switchable` so the player can toggle it — e.g. `Research_Buff`, `Espionage_Buff`, `EW Jammer`.
2. Other objects react to it with `ImprovedBy InRange "missile"` (own/allied aura) or
   `AffectedBy InRange "missile"` (enemy aura):

```
[UNIT] "VirtualCity" MODIFY
  ImprovedBy InRange "Research_Buff" Science 1.10       // cities near an active Research Center

[RADAR] "Fixed Long Wave" MODIFY
  AffectedBy InRange "EW" Complex Range                 // radars inside an enemy jammer's range
    case "Anti-Jammers" Multiply 0.80
    default Multiply 0.75
```

An aura counts when the weapon is switched on and the affected unit is within the weapon's `Range` of the
emitting unit. A unit can be tracked for at most 32 different aura weapons.

## 11. Checklist for a new weapon

1. Technology `M_My_Weapon` in `tech.txt` (+ strings).
2. Explosion(s) in `explosion.txt` (or reuse existing ones).
3. `[MISSILE]` with `Tech`, `Type` (first), `Icon`, `Explosion`, and the stats.
4. Put it in a unit's `Config` with stock, `Launch`, `Time`, and `AutoEngage` if it should fire on its own.
5. If it is a nuke or WMD: `Class`, `GenevaCategory`, `AICategory`, `CanBeLimited` (default Yes),
   `ProductionCostDegrades`, `AIHint`s.
