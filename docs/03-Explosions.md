# 03 — Explosions and combat mechanics (`Units/explosion.txt`)

[Index](index.md) · [Basics](00-Basics.md) · Catalog: [A3](A3-Catalog-Explosions.md)

An `[EXPLOSION]` holds everything that happens at impact: damage, blast radii, casualties, pollution,
lasting effects, and the visual/sound effect. Missiles refer to explosions with `Explosion "…"`; units
refer to one with `Crash "…"`.

```
[EXPLOSION] "nuke_100"                     // shipped entry
  Emulated "Units/Emulated/100K.txt"
  Sound 72 or 104 or 105
    Priority 1
    Volume 2
    MuteLength 0.05
  Kilotons 100
  Damage 225
  Range 60                 // outer (affected) radius, km
  FullEffectRange 10       // full-damage radius, km
  DrawSize 9
  TimeGrowing 3.0
  TimeTotal 3.0
  DrawYShift 0.55
  PollutionSize 80         // makes it Nuclear and "mass destruction"
  ScorchSize 40

  Variant Water            // replaces the visuals when it explodes over water
    Emulated "Units/Emulated/Water_100K.txt"
    DrawSize 27
    PollutionSize 80
```

---

## 1. Properties

### 1.1 Effect

| Property                    | Syntax                                                    | Default                         | Meaning                                                                                                                                                                                                                                                                                                                               |
| --------------------------- | --------------------------------------------------------- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Damage`                    | `<float>`                                                 | 1                               | Hit points removed from units at full effect; for cities it drives casualties (see §3). Tech-modifiable *through the missile* (`ImprovedBy … Damage` on the `[MISSILE]`).                                                                                                                                                             |
| `Range`                     | `<km>`                                                    | 1                               | Outer blast radius (the missile property name for it is `AffectedRange`).                                                                                                                                                                                                                                                             |
| `FullEffectRange`           | `<km>`                                                    | 1                               | Radius of full damage. Clamped to `Range`.                                                                                                                                                                                                                                                                                            |
| `MinCasualties`             | `<int>`                                                   | 0                               | People killed in every city the blast reaches, on top of the formula ("guaranteed casualties").                                                                                                                                                                                                                                       |
| `DoNotShowInEncyclopedia` | `[Yes\|No]` | No | Never mentioned in the Explodopedia ([14](14-Explodopedia.md)): no page, and no icon, link or row naming it on other pages. Alias `DoNotShowInExplodopedia`. A burst variant with it is left out of its yield's page; the ground burst with it: no page for the yield. |
| `Kilotons`                  | `<int>`                                                   | 0                               | Yield shown in the UI and used in statistics. ≥ 100 also sets `TriggerNuclearAttackAlert`.                                                                                                                                                                                                                                            |
| `Type`                      | `Nuclear\|Chemical\|Biological\|EMP\|Conventional\|Other` | auto                            | Category of the blast (reports, scripts, AI response, `NUKE`/`CHEM`/`BIO`/`EMP` event parameters). If not set: Damage > 0 with `PollutionSize` → Nuclear; with `LastingEffect` and `LastingDamage` → Biological; with `LastingEffect` only → Chemical; otherwise Conventional. Damage 0: with `MinCasualties` → Other, otherwise EMP. |
| `PollutionSize`             | `<float>`                                                 | 0                               | Radioactive cloud size; adds global pollution (scaled by the top-level `PollutionMultiplier` and the map's pollution speed). > 0 also sets `TriggerResponse`.                                                                                                                                                                         |
| `TriggerResponse`           | `Yes\|No`                                                 | No (Yes if `PollutionSize > 0`) | The explosion counts as **mass destruction**: it triggers the AI's nuclear response logic and the weapon belongs to the `MASS DESTRUCTION` class in event scripts.                                                                                                                                                                    |
| `TriggerNuclearAttackAlert` | `Yes\|No`                                                 | No (Yes if Kilotons ≥ 100)      | Shows the nuclear-attack alert.                                                                                                                                                                                                                                                                                                       |
| `Collateral`                | `Yes\|No`                                                 | Yes                             | Whether the lasting effect also applies to the attacker's own units.                                                                                                                                                                                                                                                                  |

### 1.2 Lasting effects (EMP, chemical, biological, cyber…)

```
LastingEffect <time> [StringID <strID>] [LastingDamage <v>] [MinHealthPercentage <0…1>] [LastingDamageType Fixed|Percent|FadingFixed|FadingPercent]
```

| Part | Meaning |
|---|---|
| `LastingEffect <time>` | How long units/cities hit by this explosion stay "affected", in reload units (`1800` = 60 "seconds"). While affected, `AffectedBy Explosion "this_id"` modifiers apply to them (e.g. EMP disables production, see `VirtualCity`). |
| `StringID` | Text shown in the unit panel while affected. |
| `LastingDamage` | Damage applied continuously while affected. Units lose Power; cities lose population. A negative value heals. |
| `LastingDamageType` | `Fixed` — `LastingDamage` per step; `Percent` — fraction of current Power/population per step; `FadingFixed`/`FadingPercent` — same, fading linearly to 0 over the effect's duration. |
| `MinHealthPercentage` | Lasting damage never takes the unit below this fraction of its full Power (cities: of their initial population). |

`LastingEffect`, `LastingDamage` and `MinHealthPercentage` can be changed by `ImprovedBy`/`AffectedBy`
written **in the explosion entry** (own techs of the attacker / techs of the target's owner):

```
[EXPLOSION] "Chemical_1" MODIFY
  AffectedBy "Chem_Protection" LastingDamage 0.5
```

### 1.3 Variants

An explosion can have per-environment variants — `Variant Ground|Water|Air|Space` — used instead of the
parent depending on where it goes off (see `nuke_100` above). A variant starts as a full copy of the
parent and then applies its own lines; `Variant Water MODIFY` changes an existing variant instead of
recreating it. Variants must come **after** all of the parent's own properties.

★ The thresholds are real heights, converted to the game's (Real heights in [01](01-Units.md)): its aircraft fly
higher than real ones (fighters at 25 game km, spy planes at 52), all in the air-burst band; its ballistic missiles
peak at about 1.85 times their `Elevation` (an ICBM at 1000 about 1850 km up), far above both thresholds.

★ An explosion from 30 real km up (61 game km, see Real heights in [01](01-Units.md): an ABM or an EMP missile bursting high, a satellite hit) uses its `Space`
variant, over land or sea alike; without one, the explosion itself (never its `Water` variant). Shipped: every
nuclear explosion is a ground burst itself (its yield's mushroom, also the ABM and EMP ones, though they rarely go
off low) and has a `Variant Air`, a `Variant Space` and a `Variant Water`, chosen by the height it goes off at. The
`Space` one: the flash, the shell and the auroras of `ABM` at three times its `DrawSize` (`TimeTotal` at least 3,
`ScorchSize 0`, `ForcedInstantFlash 150` below 10 kt); for the ABM warheads (`Tac_Nuke_ABM` and its twin,
`std_bomb_ABM_nuke`) their `ABM` look and for the EMP ones their `EMP` look, at their own sizes and times (before,
these looks were the explosions themselves). The `Water` one as the ground nuke of the yield at sea (`Water_10K` …
`Water_10M`).

★ An explosion from 3 to 30 real km up (9.6 to 61 game km: an interceptor or an anti-aircraft warhead at its target,
any aircraft) uses its `Air` variant,
over land or sea alike; without one, the explosion itself (never its `Water` variant). Shipped: every nuclear
explosion has one (`Air_10K`, `Air_100K`, `ScorchSize 0`): the fireball does not touch the ground, so no stem, no
dust ring and no scorch mark. The `ABM` ones (`Tac_Nuke_ABM`, `Tac_Nuke_ABM_Fusion`, `std_bomb_ABM_nuke`) draw a
fireball there (`Air_10K`, a third of their `DrawSize`) and their auroras only from 30 real km up.

### 1.4 Visuals and sound

| Property | Syntax | Meaning |
|---|---|---|
| `Movie` | `"file"` | Sprite animation. |
| `Video` | `"file"` | Video-based explosion. |
| `Emulated` | `"parameter file"` | Procedural (emulated) explosion defined in a separate file, see §6. `delete Emulated` removes it. |
| `DrawSize` | `<float>` | Visual size (default 32). |
| `TimeGrowing`, `TimeTotal` | `<float>` | Growth and total duration of the animation (defaults 1 and 3). |
| `DrawYShift` | `<float>` | Vertical offset of the sprite. |
| `DrawElevation` | `<km>` | The emulated explosion is drawn at least this high, whatever height it went off at: a burst high in the sky seen there, not on the ground. Only the picture: the damage, the effects and the lights stay where it went off. Shipped: none (the EMP missiles go off 400 km high themselves: `MinExplosionHeight`, [02](02-Missiles.md)). An emulated explosion high up (above about 10 km: an interceptor bursting at its target) is drawn where a missile at that height is drawn, on the same exaggerated height scale, in every view and zoom. In the terrain view the glows of an `[AURORA]` (the flash, the shell, the curtains) face the tilted camera, so a burst in the sky is seen from the side, not as discs lying flat; zoomed out, looking straight down, they lie flat. |
| `RandomAngle` | `Yes\|No` | Random rotation. |
| `ScorchSize` (alias `LightmapWashoutRadius`) | `<km>` | Sets both the washout and the scorch mark below (they used to be one value). Defaults to `PollutionSize`. `ScorchSize 0` leaves no trace on the ground, e.g. for a burst high in the sky (`Tac_Nuke_ABM`). |
| `WashoutRadius` | `<km>` | Only the lightened, burnt patch painted into the map texture. Defaults to `PollutionSize`. Write it **after** `ScorchSize`, which would overwrite it. |
| `ScorchMarkSize` | `<km>` | Only the dark scorch mark drawn with the radioactive cloud. Defaults to `PollutionSize`. Write it **after** `ScorchSize`. |
| `ForcedInstantFlash` | `<float>` | The flash on the map at the moment of the explosion, with this size. Explosions of 10 kt and more get it anyway (size `PollutionSize` × 5); below that only with this setting. |
| `InstantFlashColor` | colour | Flash colour. |
| `InstantFlashDuration`, `InstantFlashGrowth` | `<s>` | Flash timing, real seconds (not game time: the same when paused, at any game speed and frame rate): its whole time (default 0.4) and its rise to full (default 0.05). It reaches full brightness almost at once and dies away fast, with a faint afterglow at the end. |
| `DrawWave [Color <colour>]` | flag | Draw a shock-wave ring. |
| `Sound` | `Sound <id> [or <id>]… [Priority n] [SoundSize f] [Volume f] [Speed f] [MuteLength f]` | Explosion sound, random among the listed ones. |
| `AchievementProperty` | `"ACH_ID" [check "tech"]` | Achievement hook. |

### 1.5 Global setting

`PollutionMultiplier <f>` at the top level of the file scales pollution from all explosions (shipped: 0.35).

## 2. Hitting units

When a missile reaches its impact point, every unit whose class is in the missile's `Affects` set is
tested against every explosion of the missile:

1. **Impact point.** Before the test, the impact point is moved by a random distance between 0 and the
   missile's `Precision` (km) in a random direction. A ballistic missile is moved this way when it is
   launched; one fired at a point (no target unit) when it gets there. ★ A non-ballistic one (a guided
   missile, a gun's round, a `DirectLaunch` shot) at a unit is moved this way only if one of its
   explosions has a `Range` of 1 km or less (a precise hit). If all its explosions reach farther (an
   area burst, such as `Gunfire_AA`'s 5 km), `Precision` is not used: it bursts right on the target, so
   *d* below is just −`Size`. A `DirectLaunch` shot's deviation is rolled when it is fired, around where
   its target is then, and applied around where the target is when the shot arrives.
2. **Effective distance** *d* = distance from impact to the unit − the unit's `Size`.
   Adjustments: airborne targets ×2 (harder to hit), submarines at sea ×1.5, submarines on land ×1000.
3. **Damage.** With *F* = `FullEffectRange` and *R* = `Range` (both after the missile's modifiers):

   | Condition | Damage |
   |---|---|
   | *d* ≤ *F* | `Damage` |
   | *F* < *d* ≤ *R* | `Damage × (1 − (d − F)/(R − F))²` |
   | *d* > *R* | 0 |

4. The damage is subtracted from the unit's `Power`. At ≤ 0 it is destroyed. Hosted units may be dropped
   by an AI carrier/bomber below 25 % / 55 % of its Power.

`Damage`, `FullEffectRange` and the outer range can all be changed per target by the **missile's**
modifiers — this is how armour, bunkers and stealth are modelled:

```
[MISSILE] "Free fall bomb" MODIFY
  AffectedBy Unit "Collateral_Damage_Modifier" Damage 1500000   // target tag → massive damage vs cities
[MISSILE] "EMP Missile" MODIFY
  AffectedBy Unit "EMP_Killable" Set Damage 100                   // one-shot unshielded aircraft
```

## 3. Hitting cities

A city is a disc of radius `2 × GlobalCitySizeModifier × 40 × city scale` (km). For each explosion:

1. The disc is split into the part inside the full-damage circle (*F*) and the part inside the outer
   circle (*R*) but outside *F*, using exact circle-intersection areas.
2. The partial ring gets a mean damage factor: the falloff `(1 − (x − F)/(R − F))` averaged over the ring's
   near and far edge, then squared.
3. Each part kills `area fraction × population × M(damage)`, where the kill multiplier *M* is:

   | Damage (after modifiers) | M |
   |---|---|
   | ≤ 10 (conventional) | Damage ÷ 100 |
   | 10 – 100 | 0.1 → 0.2 linearly |
   | 100 – 1000 | 0.2 → 0.4 linearly |
   | > 1000 | 0.4 + 0.6 × (Damage − 1000) ÷ 10 000 |

4. `MinCasualties` is added. Casualties never exceed the population.

So the shipped 100 kt blast (`Damage 225`) kills about 23 % of the people inside its 10 km full-effect
circle, fewer in the 10–60 km ring. Against cities, doubling `Damage` is much weaker than enlarging
`FullEffectRange`/`Range`, because the kill multiplier grows slowly with damage while the affected area
grows with the square of the radius.

## 4. Interception

When an interceptor (a missile whose type targets `Missile`/`HighMissile`) reaches a missile in flight:

* Its hit is tested with the interceptor's `Precision` and explosion radius like any other hit, and
* even a geometric hit only counts with probability equal to the **target** missile's
  `CanBeIntercepted`; if it counts, the interceptor's explosion `Damage` is subtracted from the target
  missile's `Power`.

To make a missile harder to shoot down: lower `CanBeIntercepted`, raise its `Power`, raise `Speed`, or
give it `FakeHeads`. To make a defence better: raise its `Damage` (vs `Power`), improve `Precision`,
enlarge the explosion `Range`, or increase `Launch` per salvo. `MinMissilesPerTarget` /
`MaxMissilesPerTarget` in the missile file control how many interceptors gang up on one target.

## 5. Crash explosions

A unit's `Crash` explosion is produced when it is destroyed or runs out of fuel. It damages ground and
naval units and cities around the wreck with the same rules as above (without a missile's modifiers).

## 6. Emulated explosion files (`Units/Emulated/*.txt`)

`Emulated "Units/Emulated/1M.txt"` in an `[EXPLOSION]` draws a procedural explosion: hundreds of smoke,
fire, spray and glow sprites, shaded by the `ee_material` shader (relighting, noise detail, a heat
ramp for the fire). The parameter file describes its parts; the **ICBM Explosion Simulator**
([§6.10](#610-the-icbm-explosion-simulator)) shows them and lets you change them while it plays. Shipped files:

| File | Used by |
|---|---|
| `10K`, `100K`, `500K`, `1M`, `10M`, `50M` | Ground bursts. `10K` (a smaller, quicker and cheaper `100K`) is used by `nuke_10`, `nuke_10_fusion` and the ground tactical nukes (`Tac_Nuke_Army`, `Tac_Nuke_2`, `Tac_Nuke_2_Wet` and their `_Fusion` twins), all with `DrawSize 6`. |
| `Water_10K`, `Water_100K` … `Water_50M` | The `Variant Water` of the same explosions (`Water_10K`: `DrawSize 18`). |
| ★ `Air_10K`, `Air_100K` | The `Variant Air` of the nuclear explosions (3–30 real km up; `Air_100K` also for the bigger ones, at their own `DrawSize`): `[HAT]` only, round (`XYRatio 0.85`) and rising little (`GoUpSpeed 0.5`), with the white-hot orb (`OrbScale 0.6`), no fallout, a `[WILSON]` dome all around the fireball (`MaxAngle 180`), and a weaker light far below (`[LIGHT]` `Scale 0.5`). |
| `ABM` | A burst high in the atmosphere or in space (`Tac_Nuke_ABM`, `Tac_Nuke_ABM_Fusion`, and smaller `std_bomb_ABM_nuke`): only light, see `[AURORA]`. A white flash, a pink shell, green curtains. |
| `EMP` | The EMP nukes (`nuke_500_EMP`, `nuke_1000_EMP`, their `_Super` twins, `nuke_10000_EMP_Super`), going off 400 km high (`MinExplosionHeight 400` on their missiles): also `[AURORA]` only, but told apart from `ABM` at a glance: a blue-white flash, a thin cyan ring racing far out (the colour of the EMP wave), a wide sky glow and fewer, taller, slower curtains; colours by height (`ColorByHeight`): at 400 km red and violet. The EMP wave is drawn on the ground under it. |
| `Water_chem`, `Water_bio` | The gas of chemical weapons, and the same gas for biological weapons in another colour. |
| ★ `Fallout` | The fallout plume of the cobalt and salted bombs, drawn by their extra explosions (`nuke_500_Cobalt` … `nuke_10000_Salt`, `DrawSize` about 4 times the main explosion's; nothing was drawn before): a low cloud of grey-brown ash spreading from under the mushroom and drawn out downwind into a long, patchy plume that outlasts it. Made as the gas (`[WATER_RING]` only, `FrameWidth 1` for a filled cloud, `CrownSize 0`: the crown is drawn over the mushroom caps, `WindDrift 1`, `WindStretch 3`, `Patchiness 0.65`, `GasColor RGB 160 148 128`, `FadeStart 1.6`). |
| `Sprite_small_1`, `Sprite_big_1`, `Sprite_big_1_smoke`, `Sprite_big_1_beam`, `Sprite_Nuke1` | The ordinary explosions (bombs, missile and gun hits, the kinetic strike), see `[SPRITE]`. |

`GameMode/Blitz/Units/Emulated/` has its own copies.

The file has these sections, **in this order**; a part whose section is missing is not drawn:

| Section | Part |
|---|---|
| `[BASE]` | The stem and the ring of smoke on the ground (land explosions). |
| `[WATER_RING]` | The water explosion: the expanding ring of spray (base surge) and the crown thrown up in the middle. |
| `[HAT]` | The mushroom cap: white-hot, then fire, then smoke; with fallout and a fire ring. |
| `[RING]` ×3 | The condensation rings: first, top, third. |
| ★ `[WILSON]` | The Wilson cloud: a thin dome of condensation around the fireball, appearing and evaporating quickly. Optional, not used by the shipped files. |
| ★ `[AURORA]` | A burst high in the atmosphere or in space: flash, glowing debris shell and aurora curtains, no smoke. |
| ★ `[SPRITE]` | An ordinary explosion: a sequence of pictures (the frames of the old movie explosions). |
| `[LIGHT]` | The light on the terrain (drawn by default unless `[WATER_RING]` is drawn). |

★ Inside a section the settings can be in **any order**, each one optional; given twice, the last one
counts (before, they had to be in the order of the tables below, and one out of order was not recognised,
with the settings after it in that section skipped). The sections themselves stay in the order above. A
name the section does not know ends its settings. Names are case-insensitive; `//` starts a comment.

Times are given as **progress**, from 0 (the start) to 2 (the end of `TimeTotal`). `LOD` sets the number
of sprites (a grid of LOD × LOD per half); the sprite count, and with it the cost, grows with its square.
`Detail` is the strength of the noise the shader adds to the sprites (0 = none), `DetailScale` its
frequency: 1, 2 or 4 noise tiles per 64 texture pixels (other values are rounded to these).

Settings marked ★ came with the shader-based rendering. Their defaults keep the old look, except where
the table says what the default was before.

### 6.1 `[BASE]`

| Setting | Default | Meaning |
|---|---|---|
| `Draw` | Yes | `No` hides the part while keeping its settings. |
| `Size` | 1.5 | Size compared to the hat. |
| `ImageMov` | `Images/Explosion/Emulation_black_combined_512.midx` | Smoke frames. |
| `WhiteMov` | `Images/Explosion/Emulation_White.midx` | Glow sprite of the stem light. |
| `LOD` | 16 | Number of smoke puffs. Shipped: 22 for 1M–50M, 16 for 100K/500K. |
| `MaxHeightMult` | 1 | How tall the stem grows. |
| `RotationSpeed`, `GrowthSpeed` | 1 | How fast the puffs turn and grow. |
| `StemWidthMult` | 1 | Width of the stem. |
| ★ `RingStartFront`, `RingStartBack` | 0.5 | Where the ring of smoke on the ground starts (part of the radius) in front of the stem and behind it; inside it only some puffs are kept (`CenterDensity`). Before: 0.8 in front, which left an empty space there. |
| ★ `CenterDensity` | 2 | How many puffs are kept inside the ring (1 = every 4th in front, every 8th behind, as before). |
| ★ `Detail` | 1.2 | Noise strength on the smoke (before: 1). |
| ★ `DetailScale` | 4 | Noise frequency: fine detail instead of lumps of the puff size (before: 1). |
| ★ `Blur` | 0 | Blur of the smoke sprites, in texture pixels. |
| ★ `ElementScale` | 1 | Size of the smoke puffs at the outer edge of the ring. With a higher `LOD`: more and smaller puffs, finer smoke. Shipped: 0.45 (1M–50M), 0.6 (100K/500K). |
| ★ `CenterElementScale` | 1 | Size of the stem puffs and of the middle; the ring goes from this size to `ElementScale` towards its edge. Keeps the stem wide and the middle closed with small outer puffs. |
| ★ `RingDarkness` | 0.5 | How much the ring is darkened towards its middle (0 = not at all, 1 = to black; before: 0.8). |
| ★ `SpreadStart` | 0 | The ring of dust spreads outwards like a real base surge: its radius at the start compared to the old full size. 0 = as before (at its full size from the start, growing by only a quarter, while the puffs kept inflating: it stalled and grew heavier than the cap). `SpreadEnd` … `PuffGrowth` work only with `SpreadStart` > 0. Shipped: 0.3 in all the ground files. |
| ★ `SpreadEnd` | 1.35 | The radius at the end (progress 2), compared to the old full size. Shipped: 2 (`10K`: 1.6). |
| ★ `SpreadTime` | 0.5 | Progress over which most of the way is done: fast at first, then slowing down, but still moving at the end. Shipped: 0.5 (`10K`: 0.4). |
| ★ `ThinOut` | 0 | The ring thins out while it spreads: its opacity at the end is 1 − `ThinOut`. The darkening of its middle (`RingDarkness`) and the foot of the stem (the low puffs around it) fade the same way, so no dark disc is left under the stem. Shipped: 0.6 (`10K`: 0.7). |
| ★ `PuffGrowth` | 1 | How much the ring puffs still inflate on their own (1 = as before); the spreading grows them instead. Shipped: 0.3. |

The front half of the ring is drawn under the light of the fireball and the flash glow, so the fireball
lights the dust around it instead of being covered by it.

### 6.2 `[WATER_RING]`

★ Its ring of puffs (the spray, a gas cloud, a fallout plume) lies on the ground: it is drawn in two halves as the
`[BASE]` dust ring, the back one before anything else and the front one after the dust ring, both under the mushroom
caps of all the explosions around (before, over them). The crown and the `[RING]`s are still drawn over everything.

| Setting | Default | Meaning |
|---|---|---|
| `Draw` | Yes | |
| `ImageMov` | `Images/Explosion/Emulation_water.midx` | Spray sprite of the ring and the crown. |
| `WhiteMov` | `Images/Explosion/Emulation_solid_white.midx` | |
| `LOD` | 16 | Number of puffs. Shipped: 24. |
| `FrameWidth` | 0.25 | Width of the expanding band of puffs (part of the radius). |
| `ElementSizeMult` | 1 | Size of the ring puffs. Shipped: half of the old values (0.5; 0.75 for 10M/50M). |
| `CrownHeight` | 1 | How high the crown is thrown. `Water_chem`, `Water_bio`: 0.1, gas stays low. |
| `CrownSize` | 1 | Part of the radius the crown covers. |
| ★ `Detail`, `DetailScale` | 1, 1 | Noise on the ring and crown puffs. Shipped: 0.8, 2 (stronger or coarser noise looks like bubbles). |
| ★ `CrownElementScale` | 1 | Size of the crown puffs. |
| ★ `CrownDetail` | −1 | Noise strength of the crown; < 0 = `Detail`. The crown puffs are much bigger than the ring ones, so the same noise shows as a honeycomb. Shipped: 0.3. |
| ★ `ShadeVariation` | 0 | Each ring puff darker by its own random amount, up to this part. All puffs are the same image; overlapping they give a flat white otherwise. Shipped: 0.25. |
| ★ `Blur` | 0 | Blur of the ring puffs in texture pixels: soft edges blending with the water. The spray's own edges are hard; late in the explosion, when the puffs gather in a dense band, it shows as a hard-edged rim otherwise. Shipped: 12 (the nuclear ones). |
| ★ `FlashScale` | 0 | Size of the fireball flash at the start (on land the hat has the flash, the water explosion has no hat); 0 = none. Shipped: 1 for the nuclear ones, none for the gas (`Water_chem`, `Water_bio`). |
| ★ `FlashEnd` | 0.5 | Progress at which the flash has faded out. |
| ★ `CrownOnTop` | No | Draw the crown over all the rings, not between them. Needed once the rings are misty (`[RING]` `Detail`), they hide it otherwise. |
| ★ `CrownMov` | = `ImageMov` | Other frames for the crown puffs. |
| ★ `CrownBrightness` | 1 | Brighter crown puffs (> 1: the result goes towards white). Shipped: 1.7, the spray as a white mist. |
| ★ `CrownBlur` | 0 | Blur of the crown puffs in texture pixels: softer edges blending with the mist. Shipped: 6. |
| ★ `CrownRootFade` | 0 | The root of the crown (its inner, lower puffs) fades into the rings: transparent and more blurred there, opaque from this part of the crown's radius on. Without it the crown looks like a separate element. Shipped: 1. |
| ★ `CrownHeightJitter` | 0 | Each crown puff higher or lower by its own random amount, up to this part of the crown's height. The puffs are placed in rows, which show as bands otherwise. Shipped: 0.25. |
| ★ `CrownDesaturate` | 0 | Removes the colour of the crown puffs (0…1) before `CrownBrightness`: brightened, the bluish spray turns cyan otherwise. Shipped: 1. |
| ★ `Lobes` | 0 | A gas cloud instead of a round one: its outline in lobes (0 = round, up to about 0.6). The same outline is used for the rings. `Lobes` … `FadeStart` work only with `[WATER_RING]` drawn. Shipped: 0.35 in `Water_chem` and `Water_bio`. |
| ★ `WindDrift` | 0 | The cloud drifts with a wind of random direction (one per explosion), by this part of the explosion size at the end. Also moves the rings. Shipped: 0.4 in `Water_chem` and `Water_bio`. |
| ★ `WindStretch` | 0 | The cloud is stretched along the wind by this part at the end. Shipped: 0.5 in `Water_chem` and `Water_bio`. |
| ★ `RotationSpeed` | 1 | How fast the puffs turn (each at its own random speed). Shipped: 0.2 in `Water_chem` and `Water_bio`, which last much longer than the nuclear explosions. |
| ★ `Patchiness` | 0 | Denser and thinner patches across the gas cloud, also on the rings (0 = even, 1 = transparent in the thinnest ones). They move with the cloud. Shipped: 0.5 in `Water_chem` and `Water_bio`. |
| ★ `GasColor` | white | Colour the puffs and the rings are tinted with, as `RGB r g b` (0–255). White keeps the textures' own colours. Shipped: `RGB 225 235 150` (yellow-green) in `Water_chem`, `RGB 235 165 135` (pale orange-red, the biohazard colour) in `Water_bio`. |
| ★ `FadeStart` | 0 | Progress (0…2) from which the whole cloud thins out evenly to nothing at the end, instead of keeping its density. 0 = no thinning. Shipped: 1.3 in `Water_chem` and `Water_bio`. |
| ★ `Rise` | 0 | The cloud rises as it goes, like warm smoke: by this part of its starting size at the end, slowly at first, each puff by its own amount (¾ to 1¼ of it). 0 = it stays on the ground. Needs a gas cloud setting (`Lobes` … `FadeStart`, or itself). Shipped: 1.5 in `LaunchSmoke`. |

### 6.3 `[HAT]`

| Setting | Default | Meaning |
|---|---|---|
| `Draw` | Yes | |
| `ImageMov` | `Images/Explosion/Emulation_combined_512.midx` | The fire-to-smoke movie (48 frames: white, yellow, fire, smoke). |
| `WhiteMov` | `Images/Explosion/Emulation_White.midx` | Glow sprite of the flash. |
| `LOD` | 12 | Number of puffs. Shipped: 12. |
| `ScalingFrame` | 0.25 | Near the rim (below this height) the puffs fade out and shrink. |
| `XYRatio` | 0.4 | How flat the hat becomes. |
| `GoUpSpeed` | 0.75 | How fast the hat rises (together with `[BASE]` `MaxHeightMult`). |
| `FalloutScale`, `FalloutZSpeed`, `FalloutLengthSpeed` | 0 | Size of the fallout puffs, how fast they fall and spread. All three > 0 to draw it. Shipped `FalloutScale`: 0.85 (`100K`, 1.25 before), 1.0 (`500K`, 1.5 before), 0.7 (`1M`, 1.0 before), 0.6 (`10K`): smaller falling puffs. |
| `YellowTint` | 0 | Yellower flash. |
| `FireRing` | No | A ring of fire around the hat. |
| ★ `Detail`, `DetailScale` | 1, 1 | Noise on the hat and fallout puffs. Shipped: `DetailScale 2`. |
| ★ `ElementScale` | 1 | Size of the hat puffs. With a higher `LOD`: more and smaller puffs, finer smoke. Shipped: 0.75 with `LOD 12`. |
| ★ `SmokeEnd` | 0 | Progress at which the hat reaches the last frame of its movie. The smoke part (the last 30 % of the frames) is slowed down to end there; the white and the fire keep their timing, the embers fade with the smoke. 0 = as fast as the rest (the last frame at about 1.0, then held for the second half). Shipped: 1.6. |
| ★ `SpawnFade` | 0.35 | The puffs start on the top of the hat (its middle on screen) and roll to the rim. Over this angle from the top (radians) they fade in and grow from 40 % of their size, instead of appearing at once. 0 = at once (as before). Shipped: 0.6. |
| ★ `CapScale` | 1.3 | One slowly turning puff just under the top, covering the middle where the puffs fade in; its size compared to the others. 0 = none (as before). |
| ★ `OrbScale` | 0 | The first instant: a crisp, white-hot sphere in the middle of the hat, its radius compared to the hat size; the hat puffs come up as it fades. 0 = none. Not used by the shipped files (try 0.6). |
| ★ `OrbEnd` | 0.06 | Progress at which the orb is gone. |
| ★ `FalloutBlur` | 0 | Blur of the fallout puffs, in texture pixels: soft borders instead of distinct lumps (0 = sharp, as the hat puffs). Shipped: 4 in `10K`, `100K`, `500K` and `1M`. |
| ★ `FrameSpread` | Yes | Each hat and fallout puff changes to the next frame of its movie at its own moment, one after another, instead of all at once: the change from fire to smoke has no visible steps of the whole hat. `No` = all at once (as before). |
| ★ `SmokeLighten` | 0 | The cooled smoke of the hat lighter, towards a white grey (0 = the dark grey of the dust a ground burst draws up, 1 = white-grey): a burst high in the air raises no dust, its cloud turns white as its water condenses. Shipped: 0.8 in `Air_10K` and `Air_100K`. |
| ★ `FadeStart` | 0 | Progress (0…2) from which the hat (its puffs, the cap, the fallout) thins away to nothing at the end. 0 = it stays till the last moments, as a ground burst's dust cloud. Shipped: 1.1 in `Air_10K` and `Air_100K` (no dust keeps an air burst's cloud). |

### 6.4 `[RING]` (three times)

| Setting | Default | Meaning |
|---|---|---|
| `Draw` | Yes | |
| `Size` | per ring | Initial size compared to the hat. |
| `ShiftY` | per ring | Height above the base. |
| `WhiteMov` | `Images/Explosion/Emulation_white.midx` | The ring sprite (`Emulation_brown.midx` for gas). |
| `LOD` | 48 | Number of sprites. |
| `FirstAppearFrame`, `FadeInFrame` | per ring | Progress at which the ring appears and is fully visible. |
| `StartDecolorFrame` | per ring | Progress at which it turns from yellowish to neutral grey. |
| `SpeedMult` | per ring | How fast it grows. |
| `ElementMult` | per ring | How thick it is. |
| `Intensity` | per ring | Opacity. |
| `ShrinkSpeed` | 1 | How fast the sprites shrink. |
| `BothPositive` | No | Both halves drawn in front. |
| ★ `Detail`, `DetailScale` | 0, 1 | Noise on the soft ring sprites: a misty structure with frayed edges instead of a flat glow. 0 = smooth (as before). Shipped: 1, 1 in the water explosions, whose thick rings otherwise form a flat white disc. |

### 6.5 ★ `[WILSON]`

The Wilson cloud: when the shock wave passes through humid air, a thin dome of condensation flashes up
around the fireball and evaporates within seconds. Made of soft white sprites spread over the dome; its
rim, seen edge-on through many of them, is denser. Its back half is drawn behind the explosion, the front
half over it. Sizes are compared to the hat size. Not used by the shipped files.

| Setting | Default | Meaning |
|---|---|---|
| `Draw` | Yes | |
| `LOD` | 160 | Number of sprites on the dome (not squared). |
| `Appear`, `Full` | 0.03, 0.08 | Progress at which it appears and is fully dense. |
| `FadeStart`, `End` | 0.15, 0.4 | It evaporates in patches, one after another, from `FadeStart`; gone at `End`. |
| `StartSize`, `Size` | 1, 1.8 | Radius when it appears and at the end (fast at first, then slower). |
| `Height` | 0.9 | Vertical radius compared to the horizontal one. |
| `CenterZ` | 0 | Its centre over the middle of the hat. The part under the ground is not drawn. |
| `MaxAngle` | 105 | The dome from the top down to this angle (degrees; 90 = half a sphere). |
| `ElementScale` | 0.3 | Sprite radius compared to the dome radius (smaller = a thinner shell). |
| `Opacity` | 0.18 | Of one sprite. |
| `Warm` | 0.5 | Warm tint by the fireball light while it glows (0 = white). |
| `Detail`, `DetailScale` | 0.6, 2 | Noise on the sprites. |

Tried on `50M`: `LOD 320`, `StartSize 1.3`, `Size 2.6`, `ElementScale 0.26`, `Opacity 0.22`,
`Detail 0.1`, `DetailScale 1`.

### 6.6 ★ `[AURORA]`

A nuclear burst high in the atmosphere or in space has no fireball on the ground and no mushroom cloud:
a brief, intensely bright flash, a glowing shell of debris expanding and cooling, then curtains of
aurora around it — vertical rays, green below and red above — waving, drifting outwards and fading.
Everything is additive light. A file with only this section (`ABM`) draws nothing else. Sizes are
compared to the explosion size; use a longer `TimeTotal` in the `[EXPLOSION]` so the auroras can play
out (`Tac_Nuke_ABM`: 3).

| Setting | Default | Meaning |
|---|---|---|
| `Draw` | Yes | |
| `Altitude` | 0.6 | Height of the flash and the shell over the point of the explosion. Shipped: 0 in `ABM` and `EMP`: an ABM bursts at the height of the missile it hits, an EMP missile at 400 km (`MinExplosionHeight`). |
| `FlashSize` | 1.6 | Radius of the flash: it grows from a point in the first fifth of `FlashEnd`, a white core in a halo and a wide glow, with a short glint of light rays across it. 0 = no flash. |
| `FlashEnd` | 0.12 | Progress at which the flash is gone. |
| `ShellSize` | 1.2 | Radius of the debris shell at its end. 0 = none. |
| `ShellEnd` | 0.6 | Progress at which the shell is gone. |
| `ShellColor` | `RGB 255 115 140` | The colour the shell cools to (white at first). |
| ★ `ShellThickness` | 0.35 | Width of the shell ring compared to its radius: 0.35 a soft shell, small a thin sharp ring. Shipped: 0.06 in `EMP`. |
| `Curtains` | 5 | Number of aurora curtains around the burst. |
| `Rays` | 28 | Rays in one curtain. Shipped: 36. |
| `Radius` | 1 | Distance of the curtains from the burst. |
| `Drift` | 0.5 | How much further out they are at the end (0.5 = half as far again). |
| `Arc` | 1.4 | Length of a curtain, in radians. |
| `RayHeight`, `RayAltitude` | 0.9, 0.2 | Height of the rays and of their lower edge over the map. |
| `Start`, `Peak`, `FadeStart` | 0.15, 0.5, 1 | Progress at which the curtains appear, are the brightest, and start fading out (gone at the end). |
| `Brightness` | 0.6 | Light of the curtains (each a soft green band under its rays). Shipped: 1. |
| `Wave` | 1 | How much the curtains wave. |
| `Shimmer` | 0.4 | How much the rays flicker. |
| `LowColor`, `HighColor` | `RGB 90 255 128`, `RGB 240 64 115` | The lower and the upper part of the rays (the green and the red light of oxygen). |
| `GlowSize`, `GlowColor` | 2, `RGB 205 50 90` | A faint glow of the sky around (0 = none). |
| ★ `GlowLight` | 0.12 | How bright that glow is. Shipped: 0.3 in `EMP`. |
| ★ `ColorByHeight` | No | The colours of the rays and of the glow from the height the burst went off at, instead of `LowColor`, `HighColor`, `GlowColor`: the light of the air there. Below about 100 km the blue-violet of nitrogen, 100–250 km the green of oxygen, above about 200 km its red, far above the violet of the sunlit tops. The lower part of the rays shines as the air at the burst's height, the upper part as the air 300 km higher. So an ABM burst at 200 km: green rays with red tops; an EMP at 400 km: red with violet tops. Higher than 500 km (a satellite hit, up to geostationary) as at 500 km: no air there, the burst lights the upper air below it. Shipped: Yes in `ABM` and `EMP`. |
| `Detail`, `DetailScale` | 0.6, 2 | Noise along the rays. Shipped: 0.15, 1 (stronger noise shows as speckles). |

### 6.7 ★ `[SPRITE]`

An ordinary explosion (a bomb, a missile or gun hit, a kinetic strike) drawn from a sequence of pictures,
the frames of the old movie explosions, through the same emulation as the nuclear ones: the same size scale
(sizes in one unit, directly comparable), the same heights, globe and terrain view. In the terrain view the
picture stands up facing the camera; zoomed out it lies flat. A file with only this section draws nothing
else. The pictures come from the explosion atlas, `Images/Explosion/Emulation_atlas_2048.png`, with the
nuclear sprites; make it with `ICBM_ExplosionSimulator.exe -makeatlas` ([§6.10](#610-the-icbm-explosion-simulator)).

| Setting | Default | Meaning |
|---|---|---|
| `Draw` | Yes | |
| `Movie` | — | The pictures, e.g. `"Images/Explosion/Emulation_sprite_small_1.midx"`. Without it the section draws nothing. |
| `Size` | 12.8 | Width of a picture compared with the explosion size: 12.8 is the size the movie explosions had. |
| `FramesEnd` | 1 | Progress at which the last picture is reached (the movie's `TimeGrowing` / `TimeTotal`; progress 1 is `TimeTotal`). |
| `FadeEnd` | 1 | Progress at which the last picture has faded out. |
| `ShiftY` | 0 | Moved north (up on the map) by this part of half its height, as `DrawYShift` moved the movie. |
| `Lift` | 1 | In the terrain view its middle this part of half its height over the ground (1: standing on it). |
| `Brightness` | 1 | |
| `Blend` | Yes | Cross-fade from one picture to the next. |

Shipped: `Sprite_small_1` (bombs, rockets, the railgun, torpedoes, `Big_Conventional`), `Sprite_big_1`
(gunfire, lasers on units), `Sprite_big_1_smoke` (`big_bomb_old`, `Antiship2`: fire, then smoke),
`Sprite_big_1_beam` (`DEW_Sat_Laser`), `Sprite_Nuke1` (`Kinetic_Hit`, `big_bomb`), all with `[LIGHT] Draw No`
as the movies had no light on the terrain. Up to 2048 of them are drawn at once, counted apart from the
other emulated explosions (512), so a battle full of hits never takes the place of a nuclear cloud.

Their `DrawSize` keeps them below the smallest nuclear explosion (10 kt, about 44 km): special forces' gunfire about 6 km, gunfire
about 10 km, rockets, the railgun and small bombs about 18 km, bombs and torpedoes about 20 km, anti-ship and big bombs 27–30 km, the
kinetic strike about 35 km (about 13.5 km per `DrawSize`).

An ordinary explosion that hits a unit is drawn somewhere on the unit's model, not all of them at its middle (the
models are drawn far bigger than the units): on its top as seen from above, in the middle 70% of its length. On
loading, each model gets its top surface on a 24 × 12 grid; a mast or an antenna, a cell or two wide, takes the
height of the deck around it, and animated parts count as they are in the model file. A projectile fired at the
unit picks its spot as it flies and is drawn bending onto it on the way, more as it comes nearer, so it ends where
its explosion is drawn; a hit without one (a laser) takes a spot from the hit point. It only takes the spots it
reaches turning aside at most 10° (the missile's `MaxVisualAimAngle`, see [02](02-Missiles.md)) as seen from where it was fired, and between half and twice as far as the unit's middle; a unit firing from
right beside or inside a big base's model finds none, its projectile flies straight and its explosion is drawn where
it hit. The spot comes from the projectile's and the unit's IDs and where it was fired from,
so every player sees the same one; a save keeps it. It is visual only:
the explosion's position for the game (damage, pollution, territory) and the projectile's flight do not change. A miss, beside the model, is drawn where it fell.

### 6.8 `[LIGHT]`

`Draw` (Yes; No when `[WATER_RING]` is drawn), `Scale` (1), `ProgressSpeedMultiplier` (1.5),
`ColorProgressSpeedMultiplier` (1.5), `MinHeight` (0), `MaxHeight` (0.2), `StartCol` (white),
`EndCol` (orange), ★ `GroundFadeEnd` (0.3); colours as `RGB r g b` (0–255) or a colour name.

The light the flash casts on the ground follows the flash of the explosion: the hat's flash on land, the
`[WATER_RING]` `FlashScale` flash on water, the `[AURORA]` flash high above. It is gone when the flash is
gone, and turns from warm white to the orange of the cooling fireball. With a `[BASE]` it is also gone at
progress `GroundFadeEnd`, before the dust of the base, which is drawn over it, covers the lit ground
(0 = with the flash only).

### 6.9 Performance

Each puff costs four vertices in shared buffers of about a million. With many explosions on screen at
once, the game thins out the `[BASE]` and `[HAT]` puffs automatically, the same for all explosions in a
frame: above about 130 000 puffs only every 2nd is drawn (×1.41 bigger), above twice that every 4th (×2).
A 1M explosion has about 800 such puffs. Flashes, rings, the water ring, `[WILSON]` and `[AURORA]`
are not thinned. Keep this in mind when raising `LOD`: the cost grows with its square (in `[WILSON]` it
is the sprite count itself; in `[AURORA]` each ray is three sprites, `Curtains` × `Rays` × 3).

### 6.10 The ICBM Explosion Simulator

`ICBM_ExplosionSimulator.exe`, next to `ICBM.exe`, plays one emulated explosion with the game's own
drawing code, and lets you change its settings and see the result at once. Start it from the game folder;
with no file named on the command line it opens `Units/Emulated/1M.txt`.

**Where it reads and saves.** The simulator never writes into the game folder. It saves into the save
folder, *Documents/My Games/ICBM-Escalation* (or the `DataPath` set in `ICBM.CFG`), under the same name:
`Units/Emulated/1M.txt` becomes *Documents/My Games/ICBM-Escalation/Units/Emulated/1M.txt*. The game looks
there first, so the saved copy replaces the shipped file in the game too. The simulator reads files the
same way: a copy in the save folder first, then the game's file. The panel shows which one is open: the
game's file, the modified copy, or the game's file while a modified copy also exists.

| File menu | What it does |
|---|---|
| New from... | A new explosion file, starting from the settings of an existing one. *Save* then asks for its name. |
| Open from the game folder... (`O`) | The game's own file, even if a modified copy exists. |
| Open from the save folder... | A modified copy, or a file of your own. |
| Reload (`F5`) | Reads the file again, as the game would (the modified copy first). |
| Save (`Ctrl+S`), Save as... | Into the save folder. Only names in `Units/Emulated` (or `GameMode/<mode>/Units/Emulated`) are accepted: the simulator saves explosion settings, nothing else. |
| Also save the Blitz copy | On by default: if the game has a Blitz version of the file (`GameMode/Blitz/Units/Emulated/<name>`), its modified copy is saved too. |
| Delete my modified copy | Deletes the open file from the save folder: the game uses its own file again. |
| Show the save folder | Opens it in Explorer. |
| Screenshot (`S`) | The scene, without the panels, as `ExplosionSimulator_<n>.png` in the `ExplosionSimulator` folder of the save folder (*Documents/My Games/ICBM-Escalation/ExplosionSimulator*). |

**Saving changes the file, it does not rewrite it.** The first time a shipped file is saved, the copy
starts from its text; after that only the changed values are written, in their own lines, with your
comments kept. A setting that was not in the file is inserted where the game expects it (the order of the
tables above), a section switched on is added, a section switched off gets `Draw false`. A new name starts
from the text of the file it was made from. After saving, the simulator reads the file back and reports
any setting that does not read back as shown. A new file is used by the game only once an `[EXPLOSION]`
refers to it with `Emulated "..."` (for instance in a mod's `explosion.txt`).

**The panels.**

| Panel | Contents |
|---|---|
| Playback | Play / pause (`Space`), one step (`Right`), restart (`R`), loop (`L`), a timeline (dragging it runs the explosion to that moment), the speed (`Up` / `Down`). |
| Explosion type | `TimeTotal`, `DrawSize` and `DrawElevation` as in the `[EXPLOSION]` (`[` `]`, `-` `=`). They are not part of the file: set them in `explosion.txt`. |
| Settings | Every section of this chapter with all its settings. A change rebuilds the explosion at the same moment, with the same random layout of the puffs (*New layout* shuffles it; with *Lock* off every restart gets a new layout). Changed values are orange; the tooltip has the help text, the file's value and the default; a right click sets a value back to the file's or to the default. *Undo* / *Redo* (`Ctrl+Z` / `Ctrl+Y`), *Revert* (everything back to the file). `Drawn` switches a section on or off. The texture settings (`ImageMov`, `WhiteMov`, `CrownMov`) are not shown; they stay as written in the file. |
| View | Zoom (mouse wheel), tilt (`PgUp` / `PgDn`), the ground under the explosion (`B`); drag the scene to move it, `Home` resets the view. *View > Text size* sets the size of the panels' text. |
| Diagnostics | Material shading on or off (`M`), the parts to show (`1`-`7`; the base also split into its ring of dust, stem and light passes), the puff budget (`D`, as with many explosions on screen), the renderer (Direct3D or OpenGL), HDR, frames per second and the time of a frame: what an explosion costs close up. |

Unsaved changes are kept until you open another file or quit; then the simulator asks.

**The command line**, for comparisons and batch work:

| Option | Meaning |
|---|---|
| `<file>` | The settings file, e.g. `Units/Emulated/10K.txt`. |
| `-time T`, `-size S` | `TimeTotal` and `DrawSize` of the explosion (defaults 3.5 and 14). |
| `-elev E` | `DrawElevation` of the explosion, km (default 0). |
| `-makeatlas` | Makes the explosion atlas `Images/Explosion/Emulation_atlas_2048.png` in the game folder: the nuclear sprites (`Emulation_combined_512.png`, at its corner, so their clips do not change) and the prepared 128 px frames of the movie explosions (`small_1`, `big_1`, every 4th frame of `Nuke1`), with the `.midx` files that use it (`Emulation_sprite_<movie>.midx`, and the `Emulation_*.midx` of the nuclear sprites pointing at it). Then quits. Put them in the pack to ship them. |
| `-speed X`, `-zoom Z` | Starting speed and zoom. |
| `-tilt T` | The camera's tilt, 0 (looking straight down, as the map zoomed out) to 1 (the terrain view zoomed in closest, the default). |
| `-unit NAME`, `-heading A` | Draws the 3D model of a unit from `Units/Units.txt` (e.g. `Army_Division`, `Destroyer`) under the explosion, at its size in the game and with this heading in degrees: the explosion next to what it hits. Also *View* > *Unit*. |
| ★ `-hit N` | With `-unit`: the explosion as a hit on that unit, on spot N of its model, placed as the game places hits on models (on its top seen from above, see [§6.7](#67--sprite)). Also *View* > *Hit spot*. |
| ★ `-laser FILE` | Draws the laser beams as the game does into the picture FILE and exits: at the top the old flat beam, below the usual pulsed beam, a steady one, the Fusion Laser's, the Terminal ABM Laser's (wider) and a pulsed one as thin as on the whole map, each just fired, at a quarter, half and near the end of its life; at the bottom beams up into the sky (with `-tilt`, the terrain view's perspective: they keep facing the camera). |
| ★ `-trails FILE` | Draws trails as the game does into the picture FILE and exits, over 3000 km of the map. Left, missiles: an ICBM climbing to 600 km, the same fading after its missile is gone, a warhead coming down (re-entry glow), a SAM turning low down, a trail at satellite height, a cruise missile at 100 m. Right, the other `Trajectory` styles: a tracer, a shell, a railgun slug, a torpedo's wake, a chemical and a biological warhead. With `-tilt`, the terrain view's perspective. |
| ★ `-with F S T` | A second explosion at the same spot, added after the first one as the game adds a bomb's extra explosion: settings file F, `DrawSize` S, `TimeTotal` T. Shows how two explosions overlap, e.g. `Units/Emulated/1M.txt -size 14 -with Units/Emulated/Fallout.txt 56 5`, a cobalt bomb's mushroom with its fallout plume. |
| `-gl` | OpenGL instead of Direct3D. |
| `-hdr` | HDR output (Direct3D, Windows HDR on), whatever `ICBM.CFG` says. |
| `-hdrsim H` | Simulated HDR output with headroom H: with `-shots`, each picture also gets `..._hdr.png`, the brightness above SDR white in false colours, and the log the peak brightness. |
| `-bgcolor N`, `-bg image` | The ground: 0 land, 1 sea, 2 grey, 3 black, 4 white; or a picture. Without them the ground follows each file loaded: sea under a water explosion (one with `[WATER_RING]`, except `Water_chem`), land otherwise; a grey, black or white ground picked in *View* stays. |
| `-shots P,P,...` | Saves `ExplosionSimulator_shot_<P>_mask<M>.png` (in the same folder as the screenshots) when the progress (0-2) reaches each P, then quits. |
| `-hud` | The `-shots` pictures with the panels. |
| `-exact` | The `-shots` pictures taken by running the explosion at once to each moment instead of playing it: exact and quick, at any spacing (names with three decimals). |
| `-start P` | Starts at progress P (0-2) and plays on from there. |
| `-still` | The noise of the sprites stands still (it drifts with the clock otherwise), so pictures differ only by the explosion itself. |
| `-bench N` | Holds the explosion at the `-start` moment, draws N frames as fast as they go (no vsync), writes the time per frame to the log and quits (with `-zoom` and `-mask`: what each part costs). |
| `-d3d` | Direct3D, whatever `ForceOpenGL` in `ICBM.CFG` says (`-gl`: OpenGL). |
| `-oldshader` | Draws with the shaders from before the material shading, to compare their cost. |
| `-plain`, `-mask N`, `-budget N` | Start with the material shading off, with parts hidden (the `1`-`7` bits: 1 stem, 2 flash, 4 hat, 8 fallout, 16 fire ring, 32 water explosion, 64 rings; 256 the old sprites), with a fixed puff budget (0 all, 1 every 2nd, 2 every 4th). |
| `-set S.K=V` | Changes a setting at the start: S the section (`BASE`, `WATER_RING`, `HAT`, `RING1`, `RING2`, `RING3`, `WILSON`, `AURORA`, `LIGHT`), K the setting or `Draw`, V the value (colours as `r,g,b`). Can be repeated. |
| `-save NAME` | Saves the settings (with the `-set` changes) as NAME into the save folder, as *Save* does, then quits. |

For example, `ICBM_ExplosionSimulator.exe Units/Emulated/1M.txt -set HAT.OrbScale=0.6 -shots 0.02,0.1,0.5`
takes three pictures of 1M with the orb, and `... -set BASE.ThinOut=0.4 -save Units/Emulated/1M.txt` saves
that change as a modified copy. The simulator writes `ExplosionSimulator.log` there too (it writes nothing into the game folder): where the
settings were read from, what was saved, and why something failed.
