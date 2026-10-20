# Catalog A2 — Weapons (missiles)

Every shipped `[MISSILE]` entry: display name, description, unlock, template, base values (template values included), explosion and warheads, users, upgrades and the target traits that change its effect. `canbeintercepted` is shown as a percentage.

## Templates

| Template | Used by | Can be fired at |
|---|---|---|
| `AntiAir` | 9 weapons | aircraft |
| `AntiAirAll` | 1 weapons | aircraft, missiles, ballistic missiles in flight |
| `AntiAirNuke` | 4 weapons | aircraft |
| `AntiMissile` | 3 weapons | missiles |
| `AntiMissileAA` | 2 weapons | aircraft, missiles |
| `AntiMissileMidcourse` | 5 weapons | ballistic missiles in flight |
| `AntiMissileTerminal` | 1 weapons | missiles, ballistic missiles in flight |
| `AntiRadiation` | 1 weapons | Radar Site, Short-Wave Radar Vehicle, AA Gun Site, Over-The-Horizon Radar, Naval Monitoring Station, Space Radar, SAM Site, Midcourse ABM Site, Mobile SAM, Jamming Vehicle, Terminal ABM Site |
| `AntiSat` | 7 weapons | Spy Satellite, Space Shuttle |
| `AntiShip` | 0 weapons | ships |
| `Army` | 2 weapons | ground units |
| `Biological` | 15 weapons | cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base |
| `CFLaser` | 1 weapons | ground units, ships |
| `Chemical` | 16 weapons | cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base |
| `ChemicalArtillery` | 4 weapons | Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base |
| `CyberAttack` | 1 weapons | cities, Intelligence Center, Research Center, Cyber Warfare Center |
| `Default` | 19 weapons | ground units, ships, cities, map points |
| `DepthCharge` | 3 weapons | submarines |
| `LandAttack` | 1 weapons | ground units |
| `Laser_Weapon` | 1 weapons | ballistic missiles in flight, missiles |
| `Massacre` | 1 weapons | cities, map points |
| `No Attack` | 5 weapons | — |
| `Nuke` | 94 weapons | ground units, ships, cities, map points |
| `NukeArtillery` | 2 weapons | ground units, ships |
| `SemiGuided` | 2 weapons | ground units, ships |
| `Small Arms` | 1 weapons | Bomb Truck, Heavy Bomb Truck, Spec-Ops Team, Security Checkpoint, Spec-Ops Helicopter, Naval Helicopter, Cyber Warfare Center |
| `Torpedo` | 3 weapons | ships, submarines |
| `TorpedoNuke` | 0 weapons | ships, map points, submarines, cities |

## Nuclear weapons

### 10 Megaton Cobalt HGV (`10M Cobalt HGV`)

<!-- img:missile Units/Images/Missiles/HGV.png -->

A hypersonic glide vehicle containing a 10MT cobalt warhead.

**How to get it:** available from the start — technology `M_10M_Cobalt_HGV`.

**Template:** `Nuke`.

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 500 |
| `precision` | 1 |
| `canbeintercepted` | 4% |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `nuke_10000_Cobalt`: damage 75, blast radius 400 km, full effect within 150 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 10 Megaton Enhanced Salted HGV (`10M Salt HGV`)

<!-- img:missile Units/Images/Missiles/HGV.png -->

A hypersonic glide vehicle containing a 10MT enhanced salted warhead.

**How to get it:** available from the start — technology `M_10M_Salt_HGV`.

**Template:** `Nuke`.

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 500 |
| `precision` | 1 |
| `canbeintercepted` | 4% |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `nuke_10000_Salt`: damage 90, blast radius 500 km, full effect within 180 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 10 Megaton HGV (`10M HGV`)

<!-- img:missile Units/Images/Missiles/HGV.png -->

A hypersonic glide vehicle containing a 10MT warhead.

**How to get it:** available from the start — technology `M_10M_HGV`.

**Template:** `Nuke`.

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 500 |
| `precision` | 1 |
| `canbeintercepted` | 4% |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 100kt Warhead (`100kt MRBM MIRV warhead`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A medium-range MIRV warhead with a 100kt blast yield.

**How to get it:** available from the start — technology `M_100K_WARHEAD_MRBM`.

**Template:** `Nuke`.

**Warhead of:** [3x100kt MIRV MRBM](#3x100kt-mirv-mrbm-3x100kt_mrbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 5 500 |
| `speed` | 2 200 |
| `precision` | 0 |
| `canbeintercepted` | 45% |

**Explosion:**

- `nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 1M ICBM Warhead (`1M ICBM MIRV warhead`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

An ICBM MIRV warhead with a megaton blast yield.

**How to get it:** available from the start — technology `M_1M_ICBM_Warhead`.

**Template:** `Nuke`.

**Warhead of:** [6x1M Heavy MIRV ICBM](#6x1m-heavy-mirv-icbm-6x1m-icbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 000 |
| `precision` | 0 |
| `canbeintercepted` | 30% |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 1M Pure Fusion Warhead (`1M warhead fusion`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A pure-fusion MIRV warhead with a 1 megaton blast yield.

**How to get it:** available from the start — technology `M_1M_WARHEAD_FUSION`.

**Template:** `Nuke`.

**Warhead of:** [8x1MT Pure Fusion MIRV MRBM](#8x1mt-pure-fusion-mirv-mrbm-8x1mt_mrbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 000 |
| `precision` | 0 |
| `canbeintercepted` | 30% |

**Explosion:**

- `nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 25 Megaton HGV (`25M HGV`)

<!-- img:missile Units/Images/Missiles/HGV.png -->

A hypersonic glide vehicle containing a 25MT warhead.

**How to get it:** available from the start — technology `M_25M_HGV`.

**Template:** `Nuke`.

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 500 |
| `precision` | 1 |
| `canbeintercepted` | 4% |

**Explosion:**

- `nuke_25000`: damage 6 750, blast radius 270 km, full effect within 65 km, yield 25 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 250kt ICBM Warhead (`250kt ICBM MIRV warhead`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

An ICBM MIRV warhead with a 250kt blast yield.

**How to get it:** available from the start — technology `M_250K_WARHEAD_ICBM`.

**Template:** `Nuke`.

**Warhead of:** [3x250kt Heavy MIRV ICBM](#3x250kt-heavy-mirv-icbm-3x250kt-icbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 000 |
| `precision` | 0 |
| `canbeintercepted` | 30% |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 250kt Warhead (`250kt MRBM MIRV warhead`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A medium-range MIRV warhead with a 250kt blast yield.

**How to get it:** available from the start — technology `M_250K_WARHEAD_MRBM`.

**Template:** `Nuke`.

**Warhead of:** [3x250kt MIRV MRBM](#3x250kt-mirv-mrbm-3x250kt_mrbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 5 500 |
| `speed` | 2 200 |
| `precision` | 0 |
| `canbeintercepted` | 45% |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 5 Megaton HGV (`5M HGV`)

<!-- img:missile Units/Images/Missiles/HGV.png -->

A hypersonic glide vehicle containing a 5MT warhead.

**How to get it:** available from the start — technology `M_5M_HGV`.

**Template:** `Nuke`.

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 500 |
| `precision` | 1 |
| `canbeintercepted` | 4% |

**Explosion:**

- `nuke_5000`: damage 1 600, blast radius 175 km, full effect within 37.5 km, yield 5 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 50 Megaton Pure Fusion HGV (`50M Pure Fusion HGV`)

<!-- img:missile Units/Images/Missiles/HGV.png -->

A hypersonic glide vehicle containing a 50MT warhead.

**How to get it:** available from the start — technology `M_50M_HGV`.

**Template:** `Nuke`.

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 500 |
| `precision` | 1 |
| `canbeintercepted` | 4% |

**Explosion:**

- `nuke_50000_Fusion`: damage 10 000, blast radius 280 km, full effect within 80 km, yield 50 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500 Kiloton HGV (`500kt HGV`)

<!-- img:missile Units/Images/Missiles/HGV.png -->

A hypersonic glide vehicle containing a 500kt warhead.

**How to get it:** available from the start — technology `M_500kt_HGV`.

**Template:** `Nuke`.

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 500 |
| `precision` | 1 |
| `canbeintercepted` | 4% |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt ICBM Warhead (`500kt ICBM MIRV warhead`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

An ICBM MIRV warhead with a 500kt blast yield.

**How to get it:** available from the start — technology `M_500K_WARHEAD_ICBM`.

**Template:** `Nuke`.

**Warhead of:** [3x500kt Heavy MIRV ICBM](#3x500kt-heavy-mirv-icbm-3x500kt-icbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `speed` | 3 000 |
| `precision` | 0 |
| `canbeintercepted` | 30% |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt Warhead (`500kt MRBM MIRV warhead`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A medium-range MIRV warhead with a 500kt blast yield.

**How to get it:** available from the start — technology `M_500K_WARHEAD_MRBM`.

**Template:** `Nuke`.

**Warhead of:** [6x500kt MIRV MRBM](#6x500kt-mirv-mrbm-6x500kt_mrbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 5 500 |
| `speed` | 2 200 |
| `precision` | 0 |
| `canbeintercepted` | 45% |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Heavy 500 Kiloton Bomb (`500kt nuke_heavy`)

<!-- img:missile Units/Images/Missiles/Level_1/500kt_nuke_heavy.png -->

An early nuclear fission bomb with a 500kt blast yield, designed to be deployed by strategic bombers.

**How to get it:** [Nuclear Fission Weapons](A5-Catalog-Technologies.md#nuclear-fission-weapons-nuclear_fission) (`Nuclear_Fission`) — technology `M_500kt_nuke_heavy`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 30 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 2.4 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Light 100 Kiloton Bomb (`100kt_nuke_light`)

<!-- img:missile Units/Images/Missiles/Level_1/100kt_nuke_light.png -->

A lightweight nuclear fission bomb with a 100 kiloton blast yield, which is small enough to deploy using multirole fighters.

**How to get it:** [Nuclear Fission Weapons](A5-Catalog-Technologies.md#nuclear-fission-weapons-nuclear_fission) (`Nuclear_Fission`) — technology `M_100kt_nuke_light`.

**Template:** `Nuke`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 0.75 |

**Explosion:**

- `nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 100 Kiloton MRBM (`100kt_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_1/MRBM.png -->

A medium-range ballistic missile with a 100kt fission warhead, fired from land-based systems. Effective against tactical and strategic targets.

**How to get it:** [Nuclear Fission Weapons](A5-Catalog-Technologies.md#nuclear-fission-weapons-nuclear_fission) (`Nuclear_Fission`) + [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) — technology `M_100kt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 40% |
| `productioncost` | 1 |

**Explosion:**

- `nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 100 Kiloton SLBM (`100kt_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_1/SLBM.png -->

A submarine-launched ballistic missile with a 100kt fission warhead.

**How to get it:** [Nuclear Fission Weapons](A5-Catalog-Technologies.md#nuclear-fission-weapons-nuclear_fission) (`Nuclear_Fission`) + [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) — technology `M_100kt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1 |

**Explosion:**

- `nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 250 Kiloton MRBM (`250kt_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_2/MRBM.png -->

A medium-range ballistic missile with a 250kt thermonuclear warhead, fired from land-based systems. Effective against tactical and strategic targets.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) — technology `M_250kt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 40% |
| `productioncost` | 1.5 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 250 Kiloton SLBM (`250kt_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_2/SLBM.png -->

A submarine-launched ballistic missile with a 250kt warhead.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) — technology `M_250kt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 5 Megaton ICBM (`ICBM (5M Heavy)`)

<!-- img:missile Units/Images/Missiles/Level_2/ICBM_Heavy.png -->

A heavy ICBM equipped with a 5 megaton thermonuclear warhead. Only usable by ICBM launchpads, or silos upgraded to support high-powered rockets.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) — technology `M_ICBM_5M_Heavy`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 6 |

**Explosion:**

- `nuke_5000`: damage 1 600, blast radius 175 km, full effect within 37.5 km, yield 5 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 20
    - new appearance
- With [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles) (`Hypersonic_Glide_Vehicles`):
    - `heads` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500 Kiloton Heavy ICBM (`ICBM (500kt Heavy)`)

<!-- img:missile Units/Images/Missiles/Level_1/ICBM_Heavy.png -->

An ICBM equipped with an early 500kt fission warhead. Only usable by ICBM launchpads, or silos upgraded to support high-powered rockets.

**How to get it:** [Nuclear Fission Weapons](A5-Catalog-Technologies.md#nuclear-fission-weapons-nuclear_fission) (`Nuclear_Fission`) + [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) — technology `M_ICBM_500kt_Heavy`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 4 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 20
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles) (`Hypersonic_Glide_Vehicles`):
    - `heads` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Heavy 10 Megaton Bomb (`10M nuke_heavy`)

<!-- img:missile Units/Images/Missiles/Level_2/10M_nuke_heavy.png -->

A thermonuclear free-fall bomb with a 10 megaton blast yield, designed to be deployed by strategic bombers.

**How to get it:** [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) — technology `M_10M_nuke_heavy`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Light 250 Kiloton Bomb (`250kt_nuke_light`)

<!-- img:missile Units/Images/Missiles/Level_2/250kt_nuke_light.png -->

A lightweight thermonuclear bomb with a 250 kiloton blast yield, which is small enough to deploy using multirole fighters.

**How to get it:** [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) — technology `M_250kt_nuke_light`.

**Template:** `Nuke`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Neutron-Kill ABM (`Light Nuclear ABM`)

<!-- img:missile Units/Images/Missiles/ABM_Basic.png -->

An anti-ballistic missile designed to destroy incoming missiles in the midcourse phase of their trajectory. It uses a small nuclear warhead to release neutron radiation, which disables incoming missiles. This causes it to release radioactive fallout.

**How to get it:** [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Nuclear Midcourse ABM](A5-Catalog-Technologies.md#nuclear-midcourse-abm-nuke_abm) (`Nuke_ABM`) — technology `M_Nuke_ABM_Light`.

**Template:** `AntiMissileMidcourse`.

**Used by:** [Midcourse ABM Site](A1-Catalog-Units.md#midcourse-abm-site-abm_site).

**Can be fired at:** ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 950 |
| `minrange` | 650 |
| `speed` | 7 250 |
| `precision` | 0.05 |
| `maxelevation` | 8 000 |

**Explosion:**

- `std_bomb_ABM_nuke`: damage 10, blast radius 0.05 km, full effect within 0.01 km, yield 1 kt, fallout

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)

### Nuclear Artillery (`Nuclear Artillery`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/NUKE_ARTILLERY.png -->

Heavy artillery that utilizes low-yield tactical nuclear warheads. Used by army bases and army divisions to dramatically increase their destructive potential when in combat.  
Releases nuclear fallout, but has no production cost.

**How to get it:** [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) — technology `M_Nuclear_Artillery`.

**Template:** `NukeArtillery`.

**Used by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** ground units, ships.

**Replaced after:** [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`).

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 500 |
| `precision` | 1 |

**Explosion:**

- `Tac_Nuke_Army`: damage 6, blast radius 20 km, full effect within 0.5 km, yield 2 kt, fallout
- `Guaranteed_Casualties_300`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` = 140
- On units with the [“Portable Electronic Optics”](A1-Catalog-Units.md#portable-electronic-optics-portable_electronic_optics_entmod) (`Portable_Electronic_Optics_EntMod`) trait: `range` = 145
- With [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`):
    - `damage` ×1.1
    - `precision` ×0.8
- On units with the [“Early Tactical Optics”](A1-Catalog-Units.md#early-tactical-optics-tactical_optics_entmod) (`Tactical_Optics_EntMod`) trait: `range` = 150
- On units with the “Advanced Tactical Optics” (`Advanced_Tactical_Optics_Entmod`) trait (active after researching [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`)): `range` = 155
- On units with the [“Light Unmanned Vehicles”](A1-Catalog-Units.md#light-unmanned-vehicles-light_unmanned_vehicles_entmod) (`Light_Unmanned_Vehicles_EntMod`) trait: `range` = 160
- On units with the [“Robotic Infantry Aids”](A1-Catalog-Units.md#robotic-infantry-aids-robotic_infantry_entmod) (`Robotic_Infantry_EntMod`) trait: `range` = 165

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)

### Nuclear SAM (`Nuclear SAM`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/SAM_NUKE.png -->

A nuclear tipped surface to air missile. It reliably destroys any aircraft it targets and can destroy multiple targets with splash damage, but requires expensive ammunition, takes longer to reload and drops fallout over where it explodes.  
\+ Very effective against enemy aircraft.  
\+ Long range. Doesn't need precise targeting.  
\+ Can destroy tightly grouped aircraft.  
\- Expensive, requires production.  
\- Pollutes friendly territory.

**How to get it:** [Surface-To-Air Missiles](A5-Catalog-Technologies.md#surface-to-air-missiles-surface_to_air_missile) (`Surface_to_air_missile`) + [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) — technology `M_SAM_Nuke`.

**Template:** `AntiAirNuke`.

**Used by:** [SAM Site](A1-Catalog-Units.md#sam-site-sam_site).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 250 |
| `speed` | 2 500 |
| `precision` | 0.27 |
| `maxelevation` | 75 |
| `productioncost` | 0.25 |

**Explosion:**

- `Tac_Nuke_2`: damage 50, blast radius 150 km, full effect within 50 km, yield 2 kt, fallout

**Upgrades:**

- With [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2) (`SAM_Mk2`):
    - `range` = 300
    - `speed` = 3 000
    - `precision` ×0.8
    - new appearance
- With [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3) (`SAM_Mk3`):
    - `range` = 400
    - `speed` = 3 500
    - `precision` ×0.8
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `precision` ×0.8
- With [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4) (`SAM_Mk4`):
    - `range` = 600
    - `speed` = 6 000
    - `precision` ×0.8
- With [Surface-To-Air Missiles](A5-Catalog-Technologies.md#surface-to-air-missiles-surface_to_air_missile) (`Surface_to_air_missile`) + [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)

### Nuclear SRBM (`SRBM-N`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/SRBM_N.png -->

A short-ranged ballistic missile armed with a small tactical nuclear warhead. Used by ballistic missile sites and SRBM TEL Vehicles.  
\+ Quick re-fire rate.  
\+ Cheap, expendable.  
\- Produces fallout.  
\- Limited blast yield for a nuclear weapon.

**How to get it:** [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) — technology `M_SRBM-N`.

**Template:** `Nuke`.

**Used by:** [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site), [SRBM TEL Vehicle](A1-Catalog-Units.md#srbm-tel-vehicle-mobile_srbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `minrange` | 100 |
| `speed` | 2 000 |
| `precision` | 1.2 |
| `canbeintercepted` | 50% |
| `productioncost` | 0.1 |

**Explosion:**

- `nuke_10`: damage 80, blast radius 20 km, full effect within 0.5 km, yield 10 kt, fallout
- `Guaranteed_Casualties_300`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)

### Nuclear SSM (`Nuclear Cruise Missile`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/CRUISE_MISSILE_N_1.png -->

A surface-to-surface cruise missile, armed with a low-yield tactical nuclear warhead. Used to target hardened or high-value targets on land or at sea. Can attack and destroy a variety of surface targets thanks to its wider area of effect.

**How to get it:** [Early Cruise Missiles](A5-Catalog-Technologies.md#early-cruise-missiles-cruise_missiles) (`Cruise_missiles`) + [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) — technology `M_Nuclear_Cruise_Missile`.

**Template:** `Default`.

**Used by:** [SSGN (SSGN)](A1-Catalog-Units.md#ssgn-ssgn-ssgn), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser).

**Can be fired at:** ground units, ships, cities, map points.

**Replaced after:** [Early Cruise Missiles](A5-Catalog-Technologies.md#early-cruise-missiles-cruise_missiles) (`Cruise_missiles`) + [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`).

| Stat | Base value |
|---|---|
| `range` | 650 |
| `speed` | 800 |
| `precision` | 2.5 |
| `canbeintercepted` | 40% |

**Explosion:**

- `nuke_10`: damage 80, blast radius 20 km, full effect within 0.5 km, yield 10 kt, fallout
- `Guaranteed_Casualties_300`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`):
    - `precision` = 1.25
    - `range` = 700
    - new appearance
- With [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles) (`Enhanced_cruise_missiles`):
    - `precision` ×0.8
    - `range` = 800
    - `speed` = 1 000
    - `canbeintercepted` ×0.3
    - new appearance
- With [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles) (`Advanced_cruise_missiles`):
    - `precision` ×0.75
    - `range` = 1 000
    - `speed` = 1 250
    - `canbeintercepted` ×0.9
    - new appearance
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles) (`Experimental_cruise_missiles`):
    - `range` = 1 200
    - `speed` ×4
    - `canbeintercepted` ×0.3
    - new appearance

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)

### 100kt ALBM (`100kt ALBM`)

<!-- img:missile Units/Images/Missiles/Level_1/ALBM.png -->

A medium-range air-launched ballistic missile, armed with a 100kt nuclear warhead. Deployable by long-range bombers.

**How to get it:** [Nuclear Fission Weapons](A5-Catalog-Technologies.md#nuclear-fission-weapons-nuclear_fission) (`Nuclear_Fission`) + [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) — technology `M_100kt_ALBM`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 800 |
| `speed` | 2 750 |
| `precision` | 15 |
| `canbeintercepted` | 40% |
| `productioncost` | 1.2 |

**Explosion:**

- `nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 250 Kiloton Light ICBM (`ICBM (250kt Light)`)

<!-- img:missile Units/Images/Missiles/Level_1/ICBM_LIGHT.png -->

An ICBM equipped with an early 250kt fission warhead. Can be launched from mobile launchers.

**How to get it:** [Nuclear Fission Weapons](A5-Catalog-Technologies.md#nuclear-fission-weapons-nuclear_fission) (`Nuclear_Fission`) + [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) — technology `M_ICBM_250kt_Light`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 1.3 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 250kt ALBM (`250kt ALBM`)

<!-- img:missile Units/Images/Missiles/Level_2/ALBM.png -->

A medium-range air-launched ballistic missile, armed with a 250kt nuclear warhead. Deployable by long-range bombers.

**How to get it:** [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) + [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) — technology `M_250kt_ALBM`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 800 |
| `speed` | 2 750 |
| `precision` | 15 |
| `canbeintercepted` | 40% |
| `productioncost` | 1.8 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500 Kiloton Light ICBM (`ICBM (500kt Light)`)

<!-- img:missile Units/Images/Missiles/Level_2/ICBM_Light.png -->

An ICBM equipped with a 500kt warhead. Can be launched from mobile launchers.

**How to get it:** [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) + [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) — technology `M_ICBM_500kt_Light`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### High-Yield Midcourse ABM (`Nuclear ABM`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/ABM_BASIC_NUKE.png -->

A nuclear tipped anti-ballistic missile. Can reliably destroy incoming ballistic missiles and warheads, but is expensive to produce and pollutes the territory it explodes over. It can also potentially harm friendly cities, but not nearly as badly as a successful enemy strike. It is not equipped by default.  
\+ Destroys ballistic missiles.  
\+ Wide blast radius, effective against MIRVs.  
\- Expensive ammunition requires production.  
\- Does not stop low, non-ballistic missiles.  
\- Close detonations hurt friendly cities.  
\- Pollutes friendly territory.

**How to get it:** [Nuclear Midcourse ABM](A5-Catalog-Technologies.md#nuclear-midcourse-abm-nuke_abm) (`Nuke_ABM`) + [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) — technology `M_Nuke_ABM`.

**Template:** `AntiMissileMidcourse`.

**Used by:** [Midcourse ABM Site](A1-Catalog-Units.md#midcourse-abm-site-abm_site).

**Can be fired at:** ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 950 |
| `minrange` | 650 |
| `speed` | 7 250 |
| `precision` | 0.5 |
| `maxelevation` | 8 000 |
| `productioncost` | 1.8 |

**Explosion:**

- `Tac_Nuke_ABM`: damage 50, blast radius 30 km, full effect within 25 km, yield 2 kt, fallout

**Upgrades:**

- With [Conventional Midcourse ABM](A5-Catalog-Technologies.md#conventional-midcourse-abm-anti_ballistic_missile) (`anti_ballistic_missile`):
    - `range` = 1 000
    - `speed` = 7 250
    - `maxelevation` = 9 000
    - new appearance
- With [Hit-To-Kill Midcourse ABM](A5-Catalog-Technologies.md#hit-to-kill-midcourse-abm-abm_mk2) (`ABM_Mk2`):
    - `range` = 1 200
    - `speed` = 7 500
    - `maxelevation` = 9 000
    - new appearance
- With [Advanced Midcourse ABM](A5-Catalog-Technologies.md#advanced-midcourse-abm-abm_mk3) (`ABM_Mk3`):
    - `range` = 1 400
    - `speed` = 8 000
    - `maxelevation` = 9 500
    - new appearance
- With [Experimental Midcourse ABM](A5-Catalog-Technologies.md#experimental-midcourse-abm-abm_mk4) (`ABM_Mk4`):
    - `range` = 1 600
    - `speed` = 8 500
    - `maxelevation` = 10 000
    - new appearance
- With [Nuclear Midcourse ABM](A5-Catalog-Technologies.md#nuclear-midcourse-abm-nuke_abm) (`Nuke_ABM`) + [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`), [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)

### Nuclear AAM (`Nuclear AAM`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/AAM_Nuke.png -->

A nuclear tipped air-to-air missile, which is capable of destroying groups of aircraft if they are close enough together. Pollutes the territory that it explodes over.  
\+ Reliably destroys aircraft.  
\+ Potential to hit several aircraft at once  
\+ Does not require precise targeting.  
\- Expensive to produce.  
\- Can only be fired by interceptors.  
\- Releases radioactive fallout.

**How to get it:** [Early Infrared Air-to-Air Missiles](A5-Catalog-Technologies.md#early-infrared-air-to-air-missiles-air_to_air_missile) (`Air_to_Air_Missile`) + [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft) (`Interceptor_aircraft`) + [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) — technology `M_Air_to_air_missile_Nuke`.

**Template:** `AntiAirNuke`.

**Used by:** [Interceptor](A1-Catalog-Units.md#interceptor-interceptor).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 400 |
| `minrange` | 150 |
| `speed` | 2 500 |
| `precision` | 10 |
| `maxelevation` | 100 |
| `productioncost` | 0.25 |

**Explosion:**

- `Tac_Nuke_2`: damage 50, blast radius 150 km, full effect within 50 km, yield 2 kt, fallout

**Upgrades:**

- With [All-Aspect AAMs](A5-Catalog-Technologies.md#all-aspect-aams-aam_improved) (`AAM_Improved`):
    - `precision` ×0.75
    - `range` = 600
    - `speed` = 2 750
- With [F&F Radar-Guided AAMs](A5-Catalog-Technologies.md#ff-radar-guided-aams-aam_enhanced) (`AAM_Enhanced`):
    - `precision` ×0.75
    - `range` = 800
    - `speed` = 3 000
- With [Off-Boresight Ramjet AAMs](A5-Catalog-Technologies.md#off-boresight-ramjet-aams-aam_advanced) (`AAM_Advanced`):
    - `precision` ×0.75
    - `range` = 1 000
    - `speed` = 3 750
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `precision` ×0.8
- With [Advanced Hybrid Guidance AAMs](A5-Catalog-Technologies.md#advanced-hybrid-guidance-aams-aam_experimental) (`AAM_Experimental`):
    - `range` = 1 200
    - `speed` = 6 000
- With [Early Infrared Air-to-Air Missiles](A5-Catalog-Technologies.md#early-infrared-air-to-air-missiles-air_to_air_missile) (`Air_to_Air_Missile`) + [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft) (`Interceptor_aircraft`) + [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)
- `range` ×0.75: [“Helicopters”](A1-Catalog-Units.md#helicopters-helicopter_modifier) (`Helicopter_Modifier`)

### Nuclear ALCM (`ALCM-N`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/ALCM_N_1.png -->

An air-launched cruise missile armed with a tactical nuclear warhead. Has a longer range than regular AGMs and comes with the benefit of being much more destructive. Usable by long-range bombers and 4th generation multirole fighters or better.  
\+ Good range for a tactical weapon.  
\+ Deployable by multirole fighters.  
\+ Easy to fire many at once.  
\+ Can upgrade to a hypersonic variant.  
\- Has a production cost.  
\- Contaminates the area it explodes in.

**How to get it:** [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`) + [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`) — technology `M_ALCM-N`.

**Template:** `Default`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 600 |
| `speed` | 900 |
| `precision` | 1.25 |
| `canbeintercepted` | 50% |
| `productioncost` | 0.5 |

**Explosion:**

- `nuke_10`: damage 80, blast radius 20 km, full effect within 0.5 km, yield 10 kt, fallout
- `Guaranteed_Casualties_300`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles) (`Enhanced_cruise_missiles`):
    - new appearance
    - `range` = 900
    - `speed` = 1 200
- With [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm) (`Enhanced_AGM`): `precision` ×0.8
- With [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles) (`Advanced_cruise_missiles`):
    - new appearance
    - `range` = 1 200
    - `speed` = 1 500
    - `canbeintercepted` ×0.8
- With [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm) (`Advanced_AGM`): `precision` ×0.75
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles) (`Experimental_cruise_missiles`):
    - new appearance
    - `range` ×1.25
    - `speed` = 5 000
    - `canbeintercepted` ×0.3
    - `damage` ×1.125
- With [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm) (`Experimental_AGM`): `precision` ×0.8
- With [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`) + [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)

### Nuclear ASAT (`Nuclear ASAT`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/NUKE_ASAT.png -->

A nuclear-armed missile designed to destroy enemy satellites.  
\+ Extremely damaging over a wide area.  
\+ Will not miss.  
\- Creates EMPs which affect cities.  
\- Massive collateral damage potential.

**How to get it:** [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Nuclear Anti-Satellite Weapons](A5-Catalog-Technologies.md#nuclear-anti-satellite-weapons-nuke_asat) (`Nuke_ASAT`) — technology `M_ASAT_Nuke`.

**Template:** `AntiSat`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** Spy Satellite, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 2 500 |
| `speed` | 8 000 |
| `precision` | 1 |
| `canbeintercepted` | 0% |
| `maxelevation` | 50 000 |
| `productioncost` | 1.65 |

**Explosion:**

- `EMP_Blast`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s
- `Nuke_ASAT_EMP`: damage 0
- `Tac_Nuke_2`: damage 50, blast radius 150 km, full effect within 50 km, yield 2 kt, fallout

**Upgrades:**

- With [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`):
    - `fulleffectrange` = 250
    - `affectedrange` = 250
- With [Precision ASAT Weapons](A5-Catalog-Technologies.md#precision-asat-weapons-asat) (`ASAT`):
    - `range` = 3 000
    - `speed` = 9 000

**Against targets with these traits:**

- `canbeintercepted` = 1: [“Satellite Defence”](A1-Catalog-Units.md#satellite-defence-satellite_defence) (`Satellite_Defence`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)
- `damage` = 100: [“EMP Killable”](A1-Catalog-Units.md#emp-killable-emp_killable) (`EMP_Killable`)

### Nuclear Torpedo (`Nuclear Torpedo`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/NUKE_Torpedo.png -->

An anti-ship torpedo armed with a tactical nuclear warhead. Capable of targeting ships and submarines. Produces pollution and has a production cost.  
\+ Can instantly destroy enemy ships.  
\+ Can destroy tightly grouped targets.  
\+ Can upgrade to a high-speed variant.  
\- Expensive to produce.  
\- Contaminates the area it explodes in.

**How to get it:** [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) — technology `M_Nuclear_Torpedo_Tac`.

**Template:** `Torpedo`.

**Used by:** [Attack Submarine (Submarine)](A1-Catalog-Units.md#attack-submarine-submarine-submarine).

**Can be fired at:** ships, submarines.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `speed` | 120 |
| `precision` | 1 |
| `productioncost` | 0.5 |

**Explosion:**

- `Tac_Nuke_2_Wet`: damage 50, blast radius 100 km, full effect within 25 km, yield 2 kt, fallout

**Upgrades:**

- With [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons) (`Enhanced_Underwater_Weapons`):
    - new appearance
    - `range` = 210
    - `speed` ×2.5
- With [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons) (`Advanced_Underwater_Weapons`):
    - `range` = 220
    - `precision` ×0.75
- With [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons) (`Experimental_Underwater_Weapons`):
    - `range` = 230
    - `precision` = 0.2
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

### 10 Megaton ICBM (`ICBM (10M)`)

<!-- img:missile Units/Images/Missiles/Level_3/ICBM_Heavy.png -->

A heavy ICBM equipped with a 10 megaton thermonuclear warhead. Only usable by ICBM launchpads, or silos upgraded to support high-powered rockets.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_ICBM_10M_Heavy`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 6 |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 20
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built
- With [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles) (`Hypersonic_Glide_Vehicles`):
    - `heads` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 1M EMP ICBM (`ICBM (1M EMP)`)

<!-- img:missile Units/Images/Missiles/Special/ICBM_LIGHT_EMP.png -->

A nuclear ICBM designed to explode at high-altitude and generate a high-intensity electromagnetic pulse, which is capable of disabling unshielded military equipment and shutting down civilian infrastructure, doing drastic damage to the economy.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`) — technology `M_ICBM_1M_EMP`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `EMP_Blast`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s
- `nuke_1000_EMP`: damage 0, yield 1 Mt, fallout

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`):
    - `fulleffectrange` = 700
    - `affectedrange` = 700
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp) (`Super_EMP`): can no longer be built

**Against targets with these traits:**

- `damage` = 100: [“EMP Killable”](A1-Catalog-Units.md#emp-killable-emp_killable) (`EMP_Killable`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### 3x100kt MIRV MRBM (`3x100kt_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_2/MIRV_MRBM.png -->

A medium-range ballistic missile MIRV that deploys 3 100kt warheads. Fired from land-based systems.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) — technology `M_3x100kt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 20 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.2 |

**Explosion:**

- `nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout; warheads 3 × [100kt Warhead](#100kt-warhead-100kt-mrbm-mirv-warhead) (`nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 3x100kt MIRV SLBM (`3x100kt_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_2/SLBM_MIRV.png -->

A submarine-launched MIRV that releases three 100kt warheads.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) — technology `M_3x100kt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 20 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.5 |

**Explosion:**

- `nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout; warheads 3 × [100kt Warhead](#100kt-warhead-100kt-mrbm-mirv-warhead) (`nuke_100`: damage 225, blast radius 60 km, full effect within 10 km, yield 100 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 3x250kt Heavy MIRV ICBM (`3x250kt ICBM`)

<!-- img:missile Units/Images/Missiles/Level_2/MIRV_ICBM_HEAVY.png -->

An MIRV ICBM that deploys 3 separate 250kt warheads in mid-flight. Only usable by ICBM launchpads or silos upgraded to support high-powered rockets.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb) (`Thermonuclear_bomb`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) — technology `M_3x250kt_ICBM`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 20 |
| `canbeintercepted` | 30% |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout; warheads 3 × [250kt ICBM Warhead](#250kt-icbm-warhead-250kt-icbm-mirv-warhead) (`nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 2 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`): can no longer be built
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 3x250kt MIRV MRBM (`3x250kt_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_3/MIRV_MRBM.png -->

A medium-range ballistic missile MIRV that deploys 3 250kt warheads. Fired from land-based systems.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_3x250kt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 20 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.2 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout; warheads 3 × [250kt Warhead](#250kt-warhead-250kt-mrbm-mirv-warhead) (`nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 3x250kt MIRV SLBM (`3x250kt_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_3/SLBM_MIRV.png -->

A submarine-launched MIRV that releases three 250kt warheads.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_3x250kt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 20 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.5 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout; warheads 3 × [250kt Warhead](#250kt-warhead-250kt-mrbm-mirv-warhead) (`nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 3x500kt Heavy MIRV ICBM (`3x500kt ICBM`)

<!-- img:missile Units/Images/Missiles/Level_3/MIRV_ICBM_HEAVY.png -->

An MIRV ICBM that deploys 3 separate 500kt warheads in mid-flight. Only usable by ICBM launchpads or silos that can support high-powered rockets.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [MIRV](A5-Catalog-Technologies.md#mirv-mirv) (`MIRV`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_3x500kt_ICBM`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 20 |
| `canbeintercepted` | 30% |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 3 × [500kt ICBM Warhead](#500kt-icbm-warhead-500kt-icbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 2 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500 Kiloton MRBM (`500kt_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_3/MRBM.png -->

A medium-range ballistic missile with a 500kt thermonuclear warhead, fired from land-based systems. Effective against tactical and strategic targets.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_500kt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500 Kiloton SLBM (`500kt_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_3/SLBM.png -->

A submarine-launched ballistic missile with a 500kt warhead.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_500kt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt ALBM (`500kt ALBM`)

<!-- img:missile Units/Images/Missiles/Level_3/ALBM.png -->

A medium-range air-launched ballistic missile, armed with a 500kt nuclear warhead. Deployable by long-range bombers.

**How to get it:** [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_500kt_ALBM`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 800 |
| `speed` | 2 750 |
| `precision` | 15 |
| `canbeintercepted` | 40% |
| `productioncost` | 1.8 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 1
    - new appearance
- With [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt EMP MRBM (`500kt_MRBM_EMP`)

<!-- img:missile Units/Images/Missiles/Special/MRBM_EMP.png -->

A nuclear MRBM designed to explode at high-altitude and generate a high-intensity electromagnetic pulse, which is capable of disabling unshielded military equipment and shutting down civilian infrastructure, doing drastic damage to the economy.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`) — technology `M_500kt_MRBM_EMP`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `EMP_Blast`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s
- `nuke_500_EMP`: damage 0, yield 500 kt, fallout

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`):
    - `fulleffectrange` = 300
    - `affectedrange` = 300
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp) (`Super_EMP`): can no longer be built

**Against targets with these traits:**

- `damage` = 100: [“EMP Killable”](A1-Catalog-Units.md#emp-killable-emp_killable) (`EMP_Killable`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### 500kt EMP SLBM (`500kt_SLBM_EMP`)

<!-- img:missile Units/Images/Missiles/Special/SLBM_EMP.png -->

A nuclear SLBM designed to explode at high-altitude and generate a high-intensity electromagnetic pulse, which is capable of disabling unshielded military equipment and shutting down civilian infrastructure, doing drastic damage to the economy.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`) — technology `M_500kt_SLBM_EMP`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `EMP_Blast`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s
- `nuke_500_EMP`: damage 0, yield 500 kt, fallout

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`):
    - `fulleffectrange` = 300
    - `affectedrange` = 300
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp) (`Super_EMP`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` = 100: [“EMP Killable”](A1-Catalog-Units.md#emp-killable-emp_killable) (`EMP_Killable`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### Heavy 25 Megaton Bomb (`25M nuke_heavy`)

<!-- img:missile Units/Images/Missiles/Level_3/25M_nuke_heavy.png -->

A thermonuclear free-fall bomb with a 25 megaton blast yield, designed to be deployed by strategic bombers.

**How to get it:** [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_25M_nuke_heavy`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_25000`: damage 6 750, blast radius 270 km, full effect within 65 km, yield 25 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Light 500 kiloton Bomb (`500kt nuke_light`)

<!-- img:missile Units/Images/Missiles/Level_3/500kt_nuke_light.png -->

A lightweight thermonuclear bomb with a 500 kiloton blast yield, which is small enough to deploy using multirole fighters.

**How to get it:** [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_500kt_nuke_light`.

**Template:** `Nuke`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Megaton Light ICBM (`ICBM (1M Light)`)

<!-- img:missile Units/Images/Missiles/Level_3/ICBM_LIGHT.png -->

An ICBM equipped with a megaton warhead. Can be launched from mobile launchers.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) — technology `M_ICBM_1M_Light`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 10 Megaton Cobalt Bomb (`Cobalt_Bomb`)

<!-- img:missile Units/Images/Missiles/Special/10M_cobalt_bomb.png -->

A salted thermonuclear bomb with a 10 megaton blast yield. This weapon has been coated with cobalt in order to produce enhanced levels of radiation and fallout, providing increased lethality and area denial. The increased fallout will also kill people in cities far from the blast. Deployed by strategic bombers.

**How to get it:** [Cobalt Bombs](A5-Catalog-Technologies.md#cobalt-bombs-cobalt_bomb) (`Cobalt_Bomb`) — technology `M_10M_Cobalt_bomb`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `nuke_10000_Cobalt`: damage 75, blast radius 400 km, full effect within 150 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 10M Heavy Cobalt ICBM (`ICBM (10M Cobalt)`)

<!-- img:missile Units/Images/Missiles/Special/ICBM_HEAVY_COBALT.png -->

A heavy ICBM equipped with a salted cobalt warhead, which has a 10 megaton blast yield. This weapon produces enhanced levels of radiation and fallout, making it more dangerous. The increased fallout will also kill people in cities far from the blast.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Cobalt Bombs](A5-Catalog-Technologies.md#cobalt-bombs-cobalt_bomb) (`Cobalt_Bomb`) — technology `M_ICBM_10M_Cobalt`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 6 |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `nuke_10000_Cobalt`: damage 75, blast radius 400 km, full effect within 150 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 20
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles) (`Hypersonic_Glide_Vehicles`):
    - `heads` = 1
    - new appearance
- With [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 1M Light Cobalt ICBM (`ICBM (1M Cobalt)`)

<!-- img:missile Units/Images/Missiles/Special/ICBM_LIGHT_COBALT.png -->

A lightweight ICBM equipped with a salted cobalt warhead, which has a megaton blast yield. This weapon produces enhanced levels of radiation and fallout, making it more dangerous. The increased fallout will also kill people in cities far from the blast.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Cobalt Bombs](A5-Catalog-Technologies.md#cobalt-bombs-cobalt_bomb) (`Cobalt_Bomb`) — technology `M_ICBM_1M_Cobalt`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `nuke_1000_Cobalt`: damage 45, blast radius 120 km, full effect within 45 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt Cobalt ALBM (`500kt Cobalt ALBM`)

<!-- img:missile Units/Images/Missiles/Special/ALBM_COBALT_1.png -->

A medium-range air-launched ballistic missile, armed with a with a salted 500kt warhead. This weapon has been coated in cobalt to produce extra nuclear fallout upon detonating. Deployable by long-range bombers.

**How to get it:** [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Cobalt Bombs](A5-Catalog-Technologies.md#cobalt-bombs-cobalt_bomb) (`Cobalt_Bomb`) — technology `M_500kt_Cobalt_ALBM`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 800 |
| `speed` | 2 750 |
| `precision` | 15 |
| `canbeintercepted` | 40% |
| `productioncost` | 1.8 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `nuke_500_Cobalt`: damage 35, blast radius 80 km, full effect within 30 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 1
    - new appearance
- With [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt Cobalt MRBM (`500kt_Cobalt_MRBM`)

<!-- img:missile Units/Images/Missiles/Special/MRBM_COBALT.png -->

A medium-range ballistic missile with a salted 500kt thermonuclear warhead, fired from land-based systems. Effective against tactical and strategic targets. This weapon has been coated with cobalt to increase the amount of radioactive fallout it produces.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Cobalt Bombs](A5-Catalog-Technologies.md#cobalt-bombs-cobalt_bomb) (`Cobalt_Bomb`) — technology `M_500kt_Cobalt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `nuke_500_Cobalt`: damage 35, blast radius 80 km, full effect within 30 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt Cobalt SLBM (`500kt_Cobalt_SLBM`)

<!-- img:missile Units/Images/Missiles/Special/SLBM_Cobalt.png -->

A submarine-launched ballistic missile with a salted 500kt warhead. This weapon has been coated in cobalt to produce extra nuclear fallout upon detonating.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Cobalt Bombs](A5-Catalog-Technologies.md#cobalt-bombs-cobalt_bomb) (`Cobalt_Bomb`) — technology `M_500kt_Cobalt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `nuke_500_Cobalt`: damage 35, blast radius 80 km, full effect within 30 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Light 500kt Cobalt Bomb (`500kt Light Cobalt Bomb`)

<!-- img:missile Units/Images/Missiles/Special/500kt_nuke_cobalt.png -->

A lightweight salted thermonuclear bomb with a 500 kiloton blast yield, which is small enough to deploy using multirole fighters. This bomb has been coated in cobalt to increase the amount of nuclear fallout it releases.

**How to get it:** [Cobalt Bombs](A5-Catalog-Technologies.md#cobalt-bombs-cobalt_bomb) (`Cobalt_Bomb`) — technology `M_500kt_cobalt_light`.

**Template:** `Nuke`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `nuke_500_Cobalt`: damage 35, blast radius 80 km, full effect within 30 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 3x250kt Light MIRV ICBM (`3x250kt Light ICBM`)

<!-- img:missile Units/Images/Missiles/Level_3/MIRV_ICBM_LIGHT.png -->

A light MIRV ICBM that releases three 250kt warheads. Small enough to be fired from ICBM vehicles.

**How to get it:** [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) — technology `M_3x250kt_ICBM_Light`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 13 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 5.2 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout; warheads 3 × [250kt ICBM Warhead](#250kt-icbm-warhead-250kt-icbm-mirv-warhead) (`nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 2 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 6x250kt MIRV MRBM (`6x250kt_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_3/MIRV_MRBM_2.png -->

A medium-range ballistic missile MIRV that deploys 6 250kt warheads. Fired from land-based systems.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) — technology `M_6x250kt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 5 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.2 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout; warheads 6 × [250kt Warhead](#250kt-warhead-250kt-mrbm-mirv-warhead) (`nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 6x250kt MIRV SLBM (`6x250kt_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_3/SLBM_MIRV_2.png -->

A submarine-launched MIRV that releases six 250kt warheads.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) — technology `M_6x250kt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 5 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.5 |

**Explosion:**

- `nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout; warheads 6 × [250kt Warhead](#250kt-warhead-250kt-mrbm-mirv-warhead) (`nuke_250`: damage 300, blast radius 75 km, full effect within 15 km, yield 250 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 6x500kt Heavy MIRV ICBM (`6x500kt ICBM`)

<!-- img:missile Units/Images/Missiles/Level_3/MIRV_ICBM_HEAVY_2.png -->

An MIRV ICBM that deploys 6 separate 500kt warheads in mid-flight. Only usable by ICBM launchpads or silos that can support high-powered rockets.

**How to get it:** [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads) (`Mega-warheads`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) — technology `M_6x500kt_ICBM`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 18 750 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 6 × [500kt ICBM Warhead](#500kt-icbm-warhead-500kt-icbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 2 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 10M Super EMP ICBM (`ICBM (10M Super EMP)`)

<!-- img:missile Units/Images/Missiles/Special/ICBM_HEAVY_SEMP.png -->

A 10 megaton 'super' EMP ICBM, which explodes at high-altitude and delivers a massive and overwhelming electromagnetic pulse. The high blast yield of this weapon as well as its optimization to generate an EMP makes it capable of destroying electronics over thousands of miles, and greatly disrupting the economy as a result.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp) (`Super_EMP`) — technology `M_ICBM_10M_EMP_Super`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 6 |

**Explosion:**

- `EMP_Blast`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s
- `nuke_10000_EMP_Super`: damage 0, yield 10 Mt, fallout

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 20
    - new appearance
- With [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`):
    - `fulleffectrange` = 2 000
    - `affectedrange` = 2 000
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `damage` = 100: [“EMP Killable”](A1-Catalog-Units.md#emp-killable-emp_killable) (`EMP_Killable`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### 1M Super EMP ICBM (`ICBM (1M Super EMP)`)

<!-- img:missile Units/Images/Missiles/Special/ICBM_LIGHT_SEMP.png -->

A megaton 'super' EMP ICBM, which is finely optimized to explode at high altitude and produce an extremely powerful electromagnetic pulse. This weapon is more efficient than older EMP weapons, and as a result has a larger area of effect and will disrupt the civilian economy even further.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp) (`Super_EMP`) — technology `M_ICBM_1M_EMP_Super`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `EMP_Blast`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s
- `nuke_1000_EMP_Super`: damage 0, yield 1 Mt, fallout

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`):
    - `fulleffectrange` = 1 000
    - `affectedrange` = 1 000
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `damage` = 100: [“EMP Killable”](A1-Catalog-Units.md#emp-killable-emp_killable) (`EMP_Killable`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### 25 Megaton ICBM (`ICBM (25M)`)

<!-- img:missile Units/Images/Missiles/Level_4/ICBM_Heavy.png -->

A heavy ICBM equipped with a 25 megaton thermonuclear warhead. Only usable by ICBM launchpads, or silos upgraded to support high-powered rockets.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_ICBM_25M_Heavy`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 6 |

**Explosion:**

- `nuke_25000`: damage 6 750, blast radius 270 km, full effect within 65 km, yield 25 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 20
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles) (`Hypersonic_Glide_Vehicles`):
    - `heads` = 1
    - new appearance
- With [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 3x500kt Light MIRV ICBM (`3x500kt Light ICBM`)

<!-- img:missile Units/Images/Missiles/Level_4/MIRV_ICBM_LIGHT.png -->

A light MIRV ICBM that releases three 500kt warheads. Small enough to be fired from ICBM vehicles.

**How to get it:** [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_3x500kt_ICBM_Light`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 13 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 5.2 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 3 × [500kt ICBM Warhead](#500kt-icbm-warhead-500kt-icbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 2 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) + [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 5 Megaton Light ICBM (`ICBM (5M Light)`)

<!-- img:missile Units/Images/Missiles/Level_4/ICBM_LIGHT.png -->

An ICBM equipped with a 5 megaton warhead. Can be launched from mobile launchers.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_ICBM_5M_Light`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `nuke_5000`: damage 1 600, blast radius 175 km, full effect within 37.5 km, yield 5 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt Super EMP MRBM (`500kt_MRBM_EMP_Super`)

<!-- img:missile Units/Images/Missiles/Special/MRBM_SEMP.png -->

A 'super' EMP MRBM, which is finely optimized to explode at high altitude and produce an extremely powerful electromagnetic pulse. This weapon is more efficient than older EMP weapons, and as a result has a larger area of effect and will disrupt the civilian economy even further.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp) (`Super_EMP`) — technology `M_500kt_MRBM_EMP_Super`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `EMP_Blast`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s
- `nuke_500_EMP_Super`: damage 0, yield 500 kt, fallout

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`):
    - `fulleffectrange` = 400
    - `affectedrange` = 400
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `damage` = 100: [“EMP Killable”](A1-Catalog-Units.md#emp-killable-emp_killable) (`EMP_Killable`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### 500kt Super EMP SLBM (`500kt_SLBM_EMP_Super`)

<!-- img:missile Units/Images/Missiles/Special/SLBM_SEMP.png -->

A 'super' EMP SLBM, which is finely optimized to explode at high altitude and produce an extremely powerful electromagnetic pulse. This weapon is more efficient than older EMP weapons, and as a result has a larger area of effect and will disrupt the civilian economy even further.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp) (`Super_EMP`) — technology `M_500kt_SLBM_EMP_Super`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `EMP_Blast`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s
- `nuke_500_EMP_Super`: damage 0, yield 500 kt, fallout

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp) (`Specialized_EMP`):
    - `fulleffectrange` = 400
    - `affectedrange` = 400
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `damage` = 100: [“EMP Killable”](A1-Catalog-Units.md#emp-killable-emp_killable) (`EMP_Killable`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### 6x1M Heavy MIRV ICBM (`6x1M ICBM`)

<!-- img:missile Units/Images/Missiles/Level_4/MIRV_ICBM_HEAVY_2.png -->

An MIRV ICBM that deploys 6 separate megaton warheads in mid-flight. Only usable by ICBM launchpads or silos that can support high-powered rockets.

**How to get it:** [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_6x1M_ICBM`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 18 750 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout; warheads 6 × [1M ICBM Warhead](#1m-icbm-warhead-1m-icbm-mirv-warhead) (`nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 2 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) + [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 6x500kt MIRV MRBM (`6x500kt_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_4/MIRV_MRBM_2.png -->

A medium-range ballistic missile MIRV that deploys 6 500kt warheads. Fired from land-based systems.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_6x500kt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 5 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.2 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 6 × [500kt Warhead](#500kt-warhead-500kt-mrbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) + [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light) (`Novel_BM_Light`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 6x500kt MIRV SLBM (`6x500kt_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_4/SLBM_MIRV_2.png -->

A submarine-launched MIRV that releases six 500kt warheads.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_6x500kt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 5 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.5 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 6 × [500kt Warhead](#500kt-warhead-500kt-mrbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) + [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light) (`Novel_BM_Light`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Heavy 50 Megaton Bomb (`50M nuke_heavy`)

<!-- img:missile Units/Images/Missiles/Level_4/50M_nuke_heavy.png -->

A thermonuclear free-fall bomb with a 50 megaton blast yield, designed to be deployed by strategic bombers.

**How to get it:** [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_50M_nuke_heavy`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_50000`: damage 10 000, blast radius 280 km, full effect within 80 km, yield 50 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Light Megaton Bomb (`1M nuke_light`)

<!-- img:missile Units/Images/Missiles/Level_4/1M_nuke_light.png -->

A lightweight thermonuclear bomb with a megaton blast yield, which is small enough to deploy using multirole fighters.

**How to get it:** [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_1M_nuke_light`.

**Template:** `Nuke`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1 |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Megaton ALBM (`1M ALBM`)

<!-- img:missile Units/Images/Missiles/Level_4/ALBM.png -->

A medium-range air-launched ballistic missile, armed with a 1 megaton nuclear warhead. Deployable by long-range bombers.

**How to get it:** [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_1M_ALBM`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 800 |
| `speed` | 2 750 |
| `precision` | 15 |
| `canbeintercepted` | 40% |
| `productioncost` | 1.8 |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 1
    - new appearance
- With [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Megaton MRBM (`1M_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_4/MRBM.png -->

A medium-range ballistic missile with a 1 megaton thermonuclear warhead, fired from land-based systems. Effective against tactical and strategic targets.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_1M_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Megaton SLBM (`1M_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_4/SLBM.png -->

A submarine-launched ballistic missile with a 1 megaton warhead.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) — technology `M_1M_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 10 Megaton Salted Bomb (`Salted_Bomb`)

<!-- img:missile Units/Images/Missiles/Special/10M_Salted_bomb.png -->

An enhanced salted thermonuclear bomb with a 10 megaton blast yield. This weapon is specially designed to produce drastically enhanced levels of fallout compared to a regular nuclear weapon, giving it increased lethality. The increased fallout will also cause deaths in an extended range from the blast. Deployed by strategic bombers.

**How to get it:** [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`) — technology `M_10M_Salt_bomb`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `nuke_10000_Salt`: damage 90, blast radius 500 km, full effect within 180 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 10M Heavy Salted ICBM (`ICBM (10M Salt)`)

<!-- img:missile Units/Images/Missiles/Special/ICBM_HEAVY_SALT.png -->

A heavy ICBM equipped with a specially designed salted warhead with a 10 megaton blast yield. This weapon is designed to produce dramatically enhanced levels of radiation and fallout, making it more dangerous than a similar unsalted weapon. The increased fallout will also kill people in an extended range far from the blast.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`) — technology `M_ICBM_10M_Salt`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 6 |

**Explosion:**

- `nuke_10000`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `nuke_10000_Salt`: damage 90, blast radius 500 km, full effect within 180 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 20
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles) (`Hypersonic_Glide_Vehicles`):
    - `heads` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 1M Light Salted ICBM (`ICBM (1M Salt)`)

<!-- img:missile Units/Images/Missiles/Special/ICBM_LIGHT_SALT.png -->

A lightweight ICBM equipped with a specially designed salted warhead with a megaton blast yield. This weapon is designed to produce dramatically enhanced levels of radiation and fallout, making it more dangerous than a similar unsalted weapon. The increased fallout will also kill people in an extended range far from the blast.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`) — technology `M_ICBM_1M_Salt`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `nuke_1000`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout
- `nuke_1000_Salt`: damage 70, blast radius 150 km, full effect within 60 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt Salted ALBM (`500kt Salt ALBM`)

<!-- img:missile Units/Images/Missiles/Special/ALBM_SALT_1.png -->

A medium-range air-launched ballistic missile, armed with a specially salted 500kt warhead. This weapon has been modified to produce dramatically increased levels of nuclear fallout upon detonating. Deployable by long-range bombers.

**How to get it:** [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`) — technology `M_500kt_Salt_ALBM`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 800 |
| `speed` | 2 750 |
| `precision` | 15 |
| `canbeintercepted` | 40% |
| `productioncost` | 1.8 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `nuke_500_Salt`: damage 60, blast radius 100 km, full effect within 35 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt Salted MRBM (`500kt_Salt_MRBM`)

<!-- img:missile Units/Images/Missiles/Special/MRBM_SALT.png -->

A medium-range ballistic missile with a specially salted 500kt thermonuclear warhead, fired from land-based systems. Effective against tactical and strategic targets. This weapon has been specially designed to dramatically increase the amount of radioactive fallout it produces.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`) — technology `M_500kt_Salt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `nuke_500_Salt`: damage 60, blast radius 100 km, full effect within 35 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 500kt Salted SLBM (`500kt_Salt_SLBM`)

<!-- img:missile Units/Images/Missiles/Special/SLBM_Salt.png -->

A submarine-launched ballistic missile with a specially salted 500kt warhead. This weapon has been modified to produce dramatically increased levels of nuclear fallout upon detonating.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`) — technology `M_500kt_Salt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `nuke_500_Salt`: damage 60, blast radius 100 km, full effect within 35 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Light 500kt Salted Bomb (`500kt Light Salt Bomb`)

<!-- img:missile Units/Images/Missiles/Special/500kt_nuke_salted.png -->

A lightweight specially salted thermonuclear bomb with a 500 kiloton blast yield, which is small enough to deploy using multirole fighters. This bomb is specially designed to release a much higher amount of nuclear fallout.

**How to get it:** [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons) (`Enhanced_Salted_Weapons`) — technology `M_500kt_Salt_light`.

**Template:** `Nuke`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout
- `nuke_500_Salt`: damage 60, blast radius 100 km, full effect within 35 km, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 12x500kt Heavy MIRV ICBM (`12x500kt ICBM`)

<!-- img:missile Units/Images/Missiles/Level_4/MIRV_ICBM_HEAVY_3.png -->

A heavy MIRV ICBM that deploys 12 separate 500kt warheads in mid-flight, which almost guarantees one will hit the target.

**How to get it:** [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) + [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`) — technology `M_12x500kt_ICBM`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 18 750 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 12 × [500kt ICBM Warhead](#500kt-icbm-warhead-500kt-icbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 4 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 8x500kt Light MIRV ICBM (`8x500kt Light ICBM`)

<!-- img:missile Units/Images/Missiles/Level_4/MIRV_ICBM_LIGHT_2.png -->

A light MIRV ICBM that releases eight 500kt warheads. Small enough to be fired from ICBM vehicles.

**How to get it:** [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) + [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`) — technology `M_8x500kt_ICBM_Light`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 13 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 5.2 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 8 × [500kt ICBM Warhead](#500kt-icbm-warhead-500kt-icbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 2 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 8x500kt MIRV MRBM (`8x500kt_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_4/MIRV_MRBM_3.png -->

A medium-range ballistic missile MIRV that deploys 8 500kt warheads. Fired from land-based systems.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) + [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light) (`Novel_BM_Light`) — technology `M_8x500kt_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 5 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.2 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 8 × [500kt Warhead](#500kt-warhead-500kt-mrbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light) (`Novel_BM_Light`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 8x500kt MIRV SLBM (`8x500kt_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_4/SLBM_MIRV_3.png -->

A submarine-launched MIRV that releases eight 500kt warheads.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons) (`Advanced_Multi-Stage_Weapons`) + [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light) (`Novel_BM_Light`) — technology `M_8x500kt_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 5 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.5 |

**Explosion:**

- `nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout; warheads 8 × [500kt Warhead](#500kt-warhead-500kt-mrbm-mirv-warhead) (`nuke_500`: damage 450, blast radius 100 km, full effect within 20 km, yield 500 kt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light) (`Novel_BM_Light`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 10M Pure Fusion ICBM (`ICBM (10M Fusion Light)`)

<!-- img:missile Units/Images/Missiles/Level_5/ICBM_LIGHT.png -->

An ICBM equipped with a pure-fusion 10 megaton warhead. Produces less pollution than other nuclear weapons. Small enough to be fired from ICBM vehicles.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_ICBM_10M_Fusion`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `nuke_10000_Fusion`: damage 3 500, blast radius 235 km, full effect within 50 km, yield 10 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 12x1M Pure Fusion MIRV (`12x1M ICBM`)

<!-- img:missile Units/Images/Missiles/Level_5/MIRV_ICBM_HEAVY_3.png -->

A heavy MIRV ICBM that deploys 12 separate one-megaton pure fusion warheads in mid-flight, which almost guarantees a hit on the target. This weapon can absolutely annihilate even the largest cities if there is no effort made to stop it. Its pure-fusion warheads also produce less pollution than conventional warheads.

**How to get it:** [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_12x1M_ICBM`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 18 750 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout; warheads 12 × [1M Pure Fusion Warhead](#1m-pure-fusion-warhead-1m-warhead-fusion) (`nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 4 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 5 Megaton MRBM (`5M_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_5/MRBM.png -->

A medium-range ballistic missile with a 5 megaton pure fusion warhead, fired from land-based systems. Effective against tactical and strategic targets. Pure fusion weapons produce less nuclear fallout.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_5M_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `nuke_5000_Fusion`: damage 1 600, blast radius 175 km, full effect within 37.5 km, yield 5 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - new appearance
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 5 Megaton SLBM (`5M_Fusion_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_5/5M_Fusion_SLBM.png -->

A submarine-launched ballistic missile with a 5 megaton pure-fusion warhead. Pure-fusion warheads produce less pollution than regular nuclear warheads.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_5M_Fusion_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.6 |

**Explosion:**

- `nuke_5000_Fusion`: damage 1 600, blast radius 175 km, full effect within 37.5 km, yield 5 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 15
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 50 Megaton Pure Fusion ICBM (`ICBM (50M Fusion)`)

<!-- img:missile Units/Images/Missiles/Level_5/ICBM_HEAVY.png -->

A heavy ICBM equipped with a pure-fusion 50 megaton warhead. Only usable by ICBM launchpads, or silos upgraded to support high-powered rockets. Produces less pollution than other nuclear weapons.

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_ICBM_50M_Fusion`.

**Template:** `Nuke`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 12 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 6 |

**Explosion:**

- `nuke_50000_Fusion`: damage 10 000, blast radius 280 km, full effect within 80 km, yield 50 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 20
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles) (`Hypersonic_Glide_Vehicles`):
    - `heads` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 5M Pure Fusion ALBM (`5M ALBM`)

<!-- img:missile Units/Images/Missiles/Level_5/ALBM.png -->

A medium-range air-launched ballistic missile armed with a 5 megaton pure fusion warhead. Deployable by long-range bombers.

**How to get it:** [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_5M_ALBM`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 800 |
| `speed` | 2 750 |
| `precision` | 15 |
| `canbeintercepted` | 40% |
| `productioncost` | 1.8 |

**Explosion:**

- `nuke_5000_Fusion`: damage 1 600, blast radius 175 km, full effect within 37.5 km, yield 5 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 8x1M Light Fusion MIRV (`8x1M Light ICBM`)

<!-- img:missile Units/Images/Missiles/Level_5/MIRV_ICBM_LIGHT_2.png -->

A light MIRV ICBM that releases eight 1-megaton pure-fusion warheads. Produces less pollution than other nuclear weapons. Small enough to be fired from ICBM vehicles.

**How to get it:** [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_8x1M_ICBM_Light`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 13 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 5.2 |

**Explosion:**

- `nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout; warheads 8 × [1M Pure Fusion Warhead](#1m-pure-fusion-warhead-1m-warhead-fusion) (`nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km); decoys 2 × [Decoy Warhead](#decoy-warhead-false-icbm-warhead)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 8x1M Pure Fusion MIRV SLBM (`8x1M_Fusion_SLBM`)

<!-- img:missile Units/Images/Missiles/Level_5/SLBM_MIRV_Fusion.png -->

A submarine-launched MIRV that releases eight 1-megaton pure-fusion warheads. Pure-fusion warheads produce less pollution than regular nuclear warheads.

**How to get it:** [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm) (`SLBM`) + [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) + [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light) (`Novel_BM_Light`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_8x1M_Fusion_SLBM`.

**Template:** `Nuke`.

**Used by:** [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 6 000 |
| `minrange` | 400 |
| `speed` | 2 200 |
| `precision` | 5 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.5 |

**Explosion:**

- `nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout; warheads 8 × [1M Pure Fusion Warhead](#1m-pure-fusion-warhead-1m-warhead-fusion) (`nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### 8x1MT Pure Fusion MIRV MRBM (`8x1MT_MRBM`)

<!-- img:missile Units/Images/Missiles/Level_5/MIRV_MRBM_3.png -->

A medium-range ballistic missile MIRV that deploys eight one-megaton pure fusion warheads. Produces less pollution than other nuclear weapons.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light) (`Novel_BM_Light`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_8x1MT_MRBM`.

**Template:** `Nuke`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 5 |
| `canbeintercepted` | 45% |
| `productioncost` | 3.2 |

**Explosion:**

- `nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout; warheads 8 × [1M Pure Fusion Warhead](#1m-pure-fusion-warhead-1m-warhead-fusion) (`nuke_1000_Fusion`: damage 850, blast radius 150 km, full effect within 30 km, yield 1 Mt, fallout) (`Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km)
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Fusion Artillery (`Fusion Artillery`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/FUSION_ARTILLERY.png -->

Heavy artillery that utilizes low-yield tactical pure-fusion warheads. Used by army bases and army divisions to dramatically increase their destructive potential when in combat.  
Releases trace amounts of fallout, and has no production cost.

**How to get it:** [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_Fusion_Artillery`.

**Template:** `NukeArtillery`.

**Used by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** ground units, ships.

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 500 |
| `precision` | 1 |

**Explosion:**

- `Tac_Nuke_Army_Fusion`: damage 6, blast radius 20 km, full effect within 0.5 km, yield 2 kt, fallout
- `Guaranteed_Casualties_300`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` = 140
- On units with the [“Portable Electronic Optics”](A1-Catalog-Units.md#portable-electronic-optics-portable_electronic_optics_entmod) (`Portable_Electronic_Optics_EntMod`) trait: `range` = 145
- With [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`):
    - `damage` ×1.1
    - `precision` ×0.8
- On units with the [“Early Tactical Optics”](A1-Catalog-Units.md#early-tactical-optics-tactical_optics_entmod) (`Tactical_Optics_EntMod`) trait: `range` = 150
- On units with the “Advanced Tactical Optics” (`Advanced_Tactical_Optics_Entmod`) trait (active after researching [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`)): `range` = 155
- On units with the [“Light Unmanned Vehicles”](A1-Catalog-Units.md#light-unmanned-vehicles-light_unmanned_vehicles_entmod) (`Light_Unmanned_Vehicles_EntMod`) trait: `range` = 160
- On units with the [“Robotic Infantry Aids”](A1-Catalog-Units.md#robotic-infantry-aids-robotic_infantry_entmod) (`Robotic_Infantry_EntMod`) trait: `range` = 165

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)

### Fusion Midcourse ABM (`Fusion ABM`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/ABM_FUSION.png -->

A pure-fusion anti-ballistic missile. Can reliably destroy incoming ballistic missiles and warheads, but is expensive to produce. It can also potentially harm friendly cities, but not nearly as badly as a successful enemy strike. It is not equipped by default.  
\+ Destroys ballistic missiles.  
\+ Wide blast radius, effective against MIRVs.  
\+ Much less fallout than other nuclear ABMs.  
\- Expensive ammunition requires production.  
\- Does not stop low, non-ballistic missiles.  
\- Close detonations hurt friendly cities.

**How to get it:** [Nuclear Midcourse ABM](A5-Catalog-Technologies.md#nuclear-midcourse-abm-nuke_abm) (`Nuke_ABM`) + [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_Fusion_ABM`.

**Template:** `AntiMissileMidcourse`.

**Used by:** [Midcourse ABM Site](A1-Catalog-Units.md#midcourse-abm-site-abm_site).

**Can be fired at:** ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 950 |
| `minrange` | 650 |
| `speed` | 7 250 |
| `precision` | 0.5 |
| `maxelevation` | 8 000 |
| `productioncost` | 1.8 |

**Explosion:**

- `Tac_Nuke_ABM_Fusion`: damage 50, blast radius 30 km, full effect within 25 km, yield 2 kt, fallout

**Upgrades:**

- With [Conventional Midcourse ABM](A5-Catalog-Technologies.md#conventional-midcourse-abm-anti_ballistic_missile) (`anti_ballistic_missile`):
    - `range` = 1 000
    - `speed` = 7 250
    - `maxelevation` = 9 000
    - new appearance
- With [Hit-To-Kill Midcourse ABM](A5-Catalog-Technologies.md#hit-to-kill-midcourse-abm-abm_mk2) (`ABM_Mk2`):
    - `range` = 1 200
    - `speed` = 7 500
    - `maxelevation` = 9 000
    - new appearance
- With [Advanced Midcourse ABM](A5-Catalog-Technologies.md#advanced-midcourse-abm-abm_mk3) (`ABM_Mk3`):
    - `range` = 1 400
    - `speed` = 8 000
    - `maxelevation` = 9 500
    - new appearance
- With [Experimental Midcourse ABM](A5-Catalog-Technologies.md#experimental-midcourse-abm-abm_mk4) (`ABM_Mk4`):
    - `range` = 1 600
    - `speed` = 8 500
    - `maxelevation` = 10 000
    - new appearance

**Against targets with these traits:**

- `damage` ×0.5: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`), [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)

### Fusion SRBM (`Fusion SRBM`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/SRBM_Fusion.png -->

A short-ranged ballistic missile armed with a small tactical pure-fusion warhead. Used by ballistic missile sites and SRBM TEL Vehicles.  
\+ Quick re-fire rate.  
\+ Cheap, expendable.  
\- Limited blast yield for a nuclear weapon.

**How to get it:** [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_SRBM_Fusion`.

**Template:** `Nuke`.

**Used by:** [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site), [SRBM TEL Vehicle](A1-Catalog-Units.md#srbm-tel-vehicle-mobile_srbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `minrange` | 100 |
| `speed` | 2 000 |
| `precision` | 1.2 |
| `canbeintercepted` | 50% |
| `productioncost` | 0.1 |

**Explosion:**

- `nuke_10_fusion`: damage 80, blast radius 20 km, full effect within 0.5 km, yield 10 kt, fallout
- `Guaranteed_Casualties_300`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)

### Fusion SSM (`Fusion Cruise Missile`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/CRUISE_MISSILE_PF_1.png -->

A surface-to-surface cruise missile, armed with a low-yield tactical pure-fusion warhead. Used to target hardened or high-value targets on land or at sea. Can attack and destroy a variety of surface targets thanks to its wider area of effect.

**How to get it:** [Early Cruise Missiles](A5-Catalog-Technologies.md#early-cruise-missiles-cruise_missiles) (`Cruise_missiles`) + [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_Fusion_Cruise_Missile`.

**Template:** `Default`.

**Used by:** [SSGN (SSGN)](A1-Catalog-Units.md#ssgn-ssgn-ssgn), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 650 |
| `speed` | 800 |
| `precision` | 2.5 |
| `canbeintercepted` | 40% |

**Explosion:**

- `nuke_10_fusion`: damage 80, blast radius 20 km, full effect within 0.5 km, yield 10 kt, fallout
- `Guaranteed_Casualties_300`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`):
    - `precision` = 1.25
    - `range` = 700
    - new appearance
- With [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles) (`Enhanced_cruise_missiles`):
    - `precision` ×0.8
    - `range` = 800
    - `speed` = 1 000
    - `canbeintercepted` ×0.3
    - new appearance
- With [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles) (`Advanced_cruise_missiles`):
    - `precision` ×0.75
    - `range` = 1 000
    - `speed` = 1 250
    - `canbeintercepted` ×0.9
    - new appearance
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles) (`Experimental_cruise_missiles`):
    - `range` = 1 200
    - `speed` ×4
    - `canbeintercepted` ×0.3
    - new appearance

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)

### Fusion Torpedo (`Fusion Torpedo`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/Fusion_Torpedo.png -->

An anti-ship torpedo armed with a tactical pure fusion warhead. Capable of targeting ships and submarines. Produces very light pollution and has a production cost.  
\+ Can instantly destroy enemy ships.  
\+ Can destroy tightly grouped targets.  
\+ Can upgrade to a high-speed variant.  
\+ Mild fallout.  
\- Expensive to produce.

**How to get it:** [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_Fusion_Torpedo_Tac`.

**Template:** `Torpedo`.

**Used by:** [Attack Submarine (Submarine)](A1-Catalog-Units.md#attack-submarine-submarine-submarine).

**Can be fired at:** ships, submarines.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `speed` | 120 |
| `precision` | 1 |
| `productioncost` | 0.5 |

**Explosion:**

- `Tac_Nuke_2_Wet_Fusion`: damage 50, blast radius 100 km, full effect within 25 km, yield 2 kt, fallout

**Upgrades:**

- With [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons) (`Enhanced_Underwater_Weapons`):
    - new appearance
    - `range` = 210
    - `speed` ×2.5
- With [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons) (`Advanced_Underwater_Weapons`):
    - `range` = 220
    - `precision` ×0.75
- With [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons) (`Experimental_Underwater_Weapons`):
    - `range` = 230
    - `precision` = 0.2

### Heavy 100M Fusion Bomb (`100M nuke_heavy`)

<!-- img:missile Units/Images/Missiles/Level_5/100M_nuke_heavy.png -->

A pure fusion bomb, capable of delivering an unprecedented 100 megaton blast yield, while still being relatively small and light enough that it can be deployed by a strategic bomber in a practical manner. Produces little radioactive fallout, but still pollutes the environment by throwing debris and ash high into the upper atmosphere.

**How to get it:** [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_100M_nuke_heavy`.

**Template:** `Nuke`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 6.4 |

**Explosion:**

- `nuke_100000_Fusion`: damage 12 500, blast radius 300 km, full effect within 90 km, yield 100 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Light 5M Pure Fusion Bomb (`5M nuke_light`)

<!-- img:missile Units/Images/Missiles/Level_5/5M_nuke_light.png -->

A lightweight pure fusion bomb, small enough to be deployed by multirole fighters. Has a 5 megaton blast yield and produces limited pollution compared to other nuclear weapons. Extremely deadly when used in large numbers.

**How to get it:** [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_5M_nuke_light`.

**Template:** `Nuke`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1 |

**Explosion:**

- `nuke_5000_Fusion`: damage 1 600, blast radius 175 km, full effect within 37.5 km, yield 5 Mt, fallout
- `Guaranteed_Casualties_4750`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Pure Fusion ALCM (`Fusion ALCM`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/ALCM_PF_1.png -->

An air-launched cruise missile armed with a tactical pure-fusion warhead. Has a longer range than regular AGMs and comes with the benefit of being much more destructive. Usable by long-range bombers and 4th generation multirole fighters or better.  
\+ Good range for a tactical weapon.  
\+ Deployable by multirole fighters.  
\+ Easy to fire many at once.  
\+ Can upgrade to a hypersonic variant.  
\+ Relatively limited fallout.  
\- Has a production cost.

**How to get it:** [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`) + [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_ALCM_Fusion`.

**Template:** `Default`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 600 |
| `speed` | 900 |
| `precision` | 1.25 |
| `canbeintercepted` | 50% |
| `productioncost` | 0.5 |

**Explosion:**

- `nuke_10_fusion`: damage 80, blast radius 20 km, full effect within 0.5 km, yield 10 kt, fallout
- `Guaranteed_Casualties_300`: damage 0, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles) (`Enhanced_cruise_missiles`):
    - new appearance
    - `range` = 900
    - `speed` = 1 200
- With [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm) (`Enhanced_AGM`): `precision` ×0.8
- With [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles) (`Advanced_cruise_missiles`):
    - new appearance
    - `range` = 1 200
    - `speed` = 1 500
    - `canbeintercepted` ×0.8
- With [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm) (`Advanced_AGM`): `precision` ×0.75
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles) (`Experimental_cruise_missiles`):
    - new appearance
    - `range` ×1.25
    - `speed` = 5 000
    - `canbeintercepted` ×0.3
    - `damage` ×1.125
- With [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm) (`Experimental_AGM`): `precision` ×0.8

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)
- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)

### Pure Fusion SAM (`Fusion SAM`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/SAM_PF.png -->

A pure-fusion surface to air missile. It reliably destroys any aircraft it targets and can destroy multiple targets with splash damage, but requires expensive ammunition, takes longer to reload and drops a small amount of fallout over where it explodes.  
\+ Very effective against enemy aircraft.  
\+ Long range. Doesn't need precise targeting.  
\+ Can destroy tightly grouped aircraft.  
\+ Produces minimal fallout.  
\- Expensive, requires production.

**How to get it:** [Surface-To-Air Missiles](A5-Catalog-Technologies.md#surface-to-air-missiles-surface_to_air_missile) (`Surface_to_air_missile`) + [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_SAM_Fusion`.

**Template:** `AntiAirNuke`.

**Used by:** [SAM Site](A1-Catalog-Units.md#sam-site-sam_site).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 250 |
| `speed` | 2 500 |
| `precision` | 0.27 |
| `maxelevation` | 75 |
| `productioncost` | 0.25 |

**Explosion:**

- `Tac_Nuke_2_Fusion`: damage 50, blast radius 150 km, full effect within 50 km, yield 2 kt, fallout

**Upgrades:**

- With [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2) (`SAM_Mk2`):
    - `range` = 300
    - `speed` = 3 000
    - `precision` ×0.8
    - new appearance
- With [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3) (`SAM_Mk3`):
    - `range` = 400
    - `speed` = 3 500
    - `precision` ×0.8
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `precision` ×0.8
- With [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4) (`SAM_Mk4`):
    - `range` = 600
    - `speed` = 6 000
    - `precision` ×0.8

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)

### Pure-Fusion AAM (`Fusion AAM`)

<!-- img:missile Units/Images/Missiles/Tac_Nukes/AAM_PF.png -->

A pure-fusion air-to-air missile, which is capable of destroying groups of aircraft if they are close enough together. Releases neutrons upon detonating, producing very mild fallout.  
\+ Reliably destroys aircraft.  
\+ Potential to hit several aircraft at once  
\+ Does not require precise targeting.  
\+ Reduced fallout compared to fission designs.  
\- Expensive to produce.  
\- Can only be fired by interceptors.

**How to get it:** [Early Infrared Air-to-Air Missiles](A5-Catalog-Technologies.md#early-infrared-air-to-air-missiles-air_to_air_missile) (`Air_to_Air_Missile`) + [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft) (`Interceptor_aircraft`) + [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`) — technology `M_Air_to_air_missile_Fusion`.

**Template:** `AntiAirNuke`.

**Used by:** [Interceptor](A1-Catalog-Units.md#interceptor-interceptor).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 400 |
| `minrange` | 150 |
| `speed` | 2 500 |
| `precision` | 10 |
| `maxelevation` | 100 |
| `productioncost` | 0.25 |

**Explosion:**

- `Tac_Nuke_2_Fusion`: damage 50, blast radius 150 km, full effect within 50 km, yield 2 kt, fallout

**Upgrades:**

- With [All-Aspect AAMs](A5-Catalog-Technologies.md#all-aspect-aams-aam_improved) (`AAM_Improved`):
    - `precision` ×0.75
    - `range` = 600
    - `speed` = 2 750
- With [F&F Radar-Guided AAMs](A5-Catalog-Technologies.md#ff-radar-guided-aams-aam_enhanced) (`AAM_Enhanced`):
    - `precision` ×0.75
    - `range` = 800
    - `speed` = 3 000
- With [Off-Boresight Ramjet AAMs](A5-Catalog-Technologies.md#off-boresight-ramjet-aams-aam_advanced) (`AAM_Advanced`):
    - `precision` ×0.75
    - `range` = 1 000
    - `speed` = 3 750
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `precision` ×0.8
- With [Advanced Hybrid Guidance AAMs](A5-Catalog-Technologies.md#advanced-hybrid-guidance-aams-aam_experimental) (`AAM_Experimental`):
    - `range` = 1 200
    - `speed` = 6 000

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)
- `range` ×0.75: [“Helicopters”](A1-Catalog-Units.md#helicopters-helicopter_modifier) (`Helicopter_Modifier`)

## Chemical and biological weapons

### Biological Warhead (`Biological_Warhead`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A warhead containing the Medusa Fever engineered bioweapon.

**How to get it:** available from the start — technology `Bio_WARHEAD`.

**Template:** `Biological`.

**Warhead of:** [3xBW Bioweapon MIRV](#3xbw-bioweapon-mirv-bioweapon_mirv).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 13 500 |
| `speed` | 3 000 |
| `precision` | 0 |
| `canbeintercepted` | 30% |

**Explosion:**

- `BiologicalX`: damage 0.75, blast radius 1 000 km, full effect within 900 km, lasting effect 240 s

**Upgrades:**

- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Mustard Gas Bomblet (`Chemical_Warhead_1`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A warhead containing mustard gas.

**How to get it:** available from the start — technology `Chem_WARHEAD_1`.

**Template:** `Chemical`.

**Warhead of:** [Mustard Gas MRBM](#mustard-gas-mrbm-chemical_mrbm).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 5 500 |
| `speed` | 2 200 |
| `precision` | 0.2 |

**Explosion:**

- `Chemical_1`: damage 2.5, blast radius 200 km, full effect within 75 km, lasting effect 60 s

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Novichok-2000 Bomblet (`Chemical_Warhead_4`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A warhead containing the Novichok-2000 nerve agent.

**How to get it:** available from the start — technology `Chem_WARHEAD_4`.

**Template:** `Chemical`.

**Warhead of:** [Novichok-2000 MRBM](#novichok-2000-mrbm-experimental_chemical_mrbm).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 5 500 |
| `speed` | 2 200 |
| `precision` | 0.2 |

**Explosion:**

- `Chemical_4`: damage 6, blast radius 200 km, full effect within 60 km, lasting effect 120 s

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Sarin Bomblet (`Chemical_Warhead_2`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A warhead containing the nerve agent Sarin.

**How to get it:** available from the start — technology `Chem_WARHEAD_2`.

**Template:** `Chemical`.

**Warhead of:** [Sarin MRBM](#sarin-mrbm-improved_chemical_mrbm).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 5 500 |
| `speed` | 2 200 |
| `precision` | 0.2 |

**Explosion:**

- `Chemical_2`: damage 3.2, blast radius 200 km, full effect within 68 km, lasting effect 80 s

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### VX Gas Bomblet (`Chemical_Warhead_3`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A warhead containing the VX nerve agent.

**How to get it:** available from the start — technology `Chem_WARHEAD_3`.

**Template:** `Chemical`.

**Warhead of:** [VX Gas MRBM](#vx-gas-mrbm-advanced_chemical_mrbm).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 5 500 |
| `speed` | 2 200 |
| `precision` | 0.2 |

**Explosion:**

- `Chemical_3`: damage 4.5, blast radius 200 km, full effect within 65 km, lasting effect 100 s

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Mustard Gas Artillery (`Chemical Artillery`)

<!-- img:missile Units/Images/Missiles/BioChem/CHEM_ARTILLERY_1.png -->

Artillery systems loaded with mustard gas. Used by army divisions and army bases to attack opposing armies and bases, but at the cost of causing significant collateral damage and self-inflicted casualties.

**How to get it:** [Basic Chemical Weapons](A5-Catalog-Technologies.md#basic-chemical-weapons-chemical_weapons) (`Chemical_Weapons`) — technology `M_Chem_Artillery_1`.

**Template:** `ChemicalArtillery`.

**Used by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`).

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 500 |
| `precision` | 2 |

**Explosion:**

- `Chemical_1`: damage 2.5, blast radius 200 km, full effect within 75 km, lasting effect 60 s

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` = 140
- On units with the [“Portable Electronic Optics”](A1-Catalog-Units.md#portable-electronic-optics-portable_electronic_optics_entmod) (`Portable_Electronic_Optics_EntMod`) trait: `range` = 145
- On units with the [“Early Tactical Optics”](A1-Catalog-Units.md#early-tactical-optics-tactical_optics_entmod) (`Tactical_Optics_EntMod`) trait: `range` = 150
- On units with the “Advanced Tactical Optics” (`Advanced_Tactical_Optics_Entmod`) trait (active after researching [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`)): `range` = 155
- On units with the [“Light Unmanned Vehicles”](A1-Catalog-Units.md#light-unmanned-vehicles-light_unmanned_vehicles_entmod) (`Light_Unmanned_Vehicles_EntMod`) trait: `range` = 160
- On units with the [“Robotic Infantry Aids”](A1-Catalog-Units.md#robotic-infantry-aids-robotic_infantry_entmod) (`Robotic_Infantry_EntMod`) trait: `range` = 165

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Mustard Gas Bomb (`Chemical_bomb`)

<!-- img:missile Units/Images/Missiles/BioChem/ChemBomb_1.png -->

A large airburst bomb designed to disperse mustard gas over a target area.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Basic Chemical Weapons](A5-Catalog-Technologies.md#basic-chemical-weapons-chemical_weapons) (`Chemical_Weapons`) — technology `Chemical_Bomb`.

**Template:** `Chemical`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`).

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |

**Explosion:**

- `Chemical_1`: damage 2.5, blast radius 200 km, full effect within 75 km, lasting effect 60 s

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Mustard Gas SRBM (`Chemical_SRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Chem_SRBM_1.png -->

A short-range ballistic missile outfitted with a warhead designed to disperse mustard gas bo.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Basic Chemical Weapons](A5-Catalog-Technologies.md#basic-chemical-weapons-chemical_weapons) (`Chemical_Weapons`) — technology `M_Chem_SRBM_1`.

**Template:** `Chemical`.

**Used by:** [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site), [SRBM TEL Vehicle](A1-Catalog-Units.md#srbm-tel-vehicle-mobile_srbm).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`).

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `minrange` | 100 |
| `speed` | 2 000 |
| `precision` | 1 |
| `canbeintercepted` | 50% |

**Explosion:**

- `Chemical_1`: damage 2.5, blast radius 200 km, full effect within 75 km, lasting effect 60 s; warheads 3 × [Mustard Gas Bomblet](#mustard-gas-bomblet-chemical_warhead_1) (`Chemical_1`: damage 2.5, blast radius 200 km, full effect within 75 km, lasting effect 60 s)

**Upgrades:**

- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - new appearance
    - `canbeintercepted` ×0.9
    - `precision` ×0.85

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Rabbit Fever Bomb (`Bioweapon_bomb`)

<!-- img:missile Units/Images/Missiles/BioChem/BioBomb_1.png -->

A large airburst bomb designed to disperse Tularemia, also know as Rabbit Fever, over a target area.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Basic Biological Weapons](A5-Catalog-Technologies.md#basic-biological-weapons-biological_weapons) (`Biological_Weapons`) — technology `Bioweapon_Bomb`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1.25 |

**Explosion:**

- `Biological`: damage 0.25, blast radius 350 km, full effect within 300 km, lasting effect 120 s

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2) (`Biological_Weapons_Mk2`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Mustard Gas MRBM (`Chemical_MRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Chem_MRBM_1.png -->

A medium-range ballistic missile outfitted with a warhead designed to disperse mustard gas bomblets over a wide area.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Basic Chemical Weapons](A5-Catalog-Technologies.md#basic-chemical-weapons-chemical_weapons) (`Chemical_Weapons`) + [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) — technology `M_Chemical_MRBM_1`.

**Template:** `Chemical`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`).

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |

**Explosion:**

- `Chemical_1`: damage 2.5, blast radius 200 km, full effect within 75 km, lasting effect 60 s; warheads 4 × [Mustard Gas Bomblet](#mustard-gas-bomblet-chemical_warhead_1) (`Chemical_1`: damage 2.5, blast radius 200 km, full effect within 75 km, lasting effect 60 s)

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### Rabbit Fever MRBM (`Bioweapon_MRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Bio_MRBM.png -->

A medium-range ballistic missile outfitted with a warhead designed to disperse Tularemia, also know as Rabbit Fever, over an area.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Basic Biological Weapons](A5-Catalog-Technologies.md#basic-biological-weapons-biological_weapons) (`Biological_Weapons`) + [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) — technology `Bioweapon_MRBM`.

**Template:** `Biological`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `Biological`: damage 0.25, blast radius 350 km, full effect within 300 km, lasting effect 120 s

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2) (`Biological_Weapons_Mk2`): can no longer be built
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Rabbit Fever ICBM (`Bioweapon_ICBM`)

<!-- img:missile Units/Images/Missiles/BioChem/BIO_ICBM_LIGHT.png -->

An ICBM originally designed for a light nuclear warhead, which has been modified to disperse Tularemia, also know as Rabbit Fever, instead.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Basic Biological Weapons](A5-Catalog-Technologies.md#basic-biological-weapons-biological_weapons) (`Biological_Weapons`) + [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) — technology `Bioweapon_ICBM`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `Biological`: damage 0.25, blast radius 350 km, full effect within 300 km, lasting effect 120 s

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2) (`Biological_Weapons_Mk2`) + [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`): can no longer be built
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Sarin Artillery (`Improved Chemical Artillery`)

<!-- img:missile Units/Images/Missiles/BioChem/CHEM_ARTILLERY_2.png -->

Artillery systems loaded with the nerve agent Sarin. Used by army divisions and army bases to attack opposing armies and bases, but at the cost of causing significant collateral damage and self-inflicted casualties.

**How to get it:** [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`) — technology `M_Chem_Artillery_2`.

**Template:** `ChemicalArtillery`.

**Used by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`).

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 500 |
| `precision` | 2 |

**Explosion:**

- `Chemical_2`: damage 3.2, blast radius 200 km, full effect within 68 km, lasting effect 80 s

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` = 140
- On units with the [“Portable Electronic Optics”](A1-Catalog-Units.md#portable-electronic-optics-portable_electronic_optics_entmod) (`Portable_Electronic_Optics_EntMod`) trait: `range` = 145
- On units with the [“Early Tactical Optics”](A1-Catalog-Units.md#early-tactical-optics-tactical_optics_entmod) (`Tactical_Optics_EntMod`) trait: `range` = 150
- On units with the “Advanced Tactical Optics” (`Advanced_Tactical_Optics_Entmod`) trait (active after researching [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`)): `range` = 155
- On units with the [“Light Unmanned Vehicles”](A1-Catalog-Units.md#light-unmanned-vehicles-light_unmanned_vehicles_entmod) (`Light_Unmanned_Vehicles_EntMod`) trait: `range` = 160
- On units with the [“Robotic Infantry Aids”](A1-Catalog-Units.md#robotic-infantry-aids-robotic_infantry_entmod) (`Robotic_Infantry_EntMod`) trait: `range` = 165

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Sarin Bomb (`Improved_Chemical_bomb`)

<!-- img:missile Units/Images/Missiles/BioChem/ChemBomb_2.png -->

A large airburst bomb designed to disperse the nerve agent known as sarin over a target area.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`) — technology `Improved_Chemical_Bomb`.

**Template:** `Chemical`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`).

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |

**Explosion:**

- `Chemical_2`: damage 3.2, blast radius 200 km, full effect within 68 km, lasting effect 80 s

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Sarin MRBM (`Improved_Chemical_MRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Imp_Chem_MRBM_1.png -->

A medium-range ballistic missile outfitted with a warhead designed to disperse Sarin bomblets over a wide area.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`) — technology `M_Chemical_MRBM_2`.

**Template:** `Chemical`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`).

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |

**Explosion:**

- `Chemical_2`: damage 3.2, blast radius 200 km, full effect within 68 km, lasting effect 80 s; warheads 4 × [Sarin Bomblet](#sarin-bomblet-chemical_warhead_2) (`Chemical_2`: damage 3.2, blast radius 200 km, full effect within 68 km, lasting effect 80 s)

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### Sarin SRBM (`Improved_Chemical_SRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Imp_Chem_SRBM_1.png -->

A short-range ballistic missile outfitted with a warhead designed to disperse Sarin gas bomblets.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`) — technology `M_Chem_SRBM_2`.

**Template:** `Chemical`.

**Used by:** [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site), [SRBM TEL Vehicle](A1-Catalog-Units.md#srbm-tel-vehicle-mobile_srbm).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`).

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `minrange` | 100 |
| `speed` | 2 000 |
| `precision` | 1 |
| `canbeintercepted` | 50% |

**Explosion:**

- `Chemical_2`: damage 3.2, blast radius 200 km, full effect within 68 km, lasting effect 80 s; warheads 3 × [Sarin Bomblet](#sarin-bomblet-chemical_warhead_2) (`Chemical_2`: damage 3.2, blast radius 200 km, full effect within 68 km, lasting effect 80 s)

**Upgrades:**

- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - new appearance
    - `canbeintercepted` ×0.9
    - `precision` ×0.85

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Smallpox Bomb (`Improved_Bioweapon_bomb`)

<!-- img:missile Units/Images/Missiles/BioChem/BioBomb_2.png -->

A large airburst bomb designed to disperse weaponized Smallpox over a target area.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2) (`Biological_Weapons_Mk2`) — technology `Improved_Bioweapon_Bomb`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1.25 |

**Explosion:**

- `Biological2`: damage 0.3, blast radius 500 km, full effect within 450 km, lasting effect 140 s

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3) (`Biological_Weapons_Mk3`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Smallpox ICBM (`Improved_Bioweapon_ICBM`)

<!-- img:missile Units/Images/Missiles/BioChem/IMP_BIO_ICBM_LIGHT.png -->

An ICBM originally designed for a light nuclear warhead, which has been modified to disperse weaponized Smallpox instead.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2) (`Biological_Weapons_Mk2`) + [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) — technology `Improved_Bioweapon_ICBM`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `Biological2`: damage 0.3, blast radius 500 km, full effect within 450 km, lasting effect 140 s

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3) (`Biological_Weapons_Mk3`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Smallpox MRBM (`Improved_Bioweapon_MRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Imp_Bio_MRBM.png -->

A medium-range ballistic missile outfitted with a warhead designed to disperse weaponized Smallpox over an area.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2) (`Biological_Weapons_Mk2`) — technology `Improved_Bioweapon_MRBM`.

**Template:** `Biological`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `Biological2`: damage 0.3, blast radius 500 km, full effect within 450 km, lasting effect 140 s

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3) (`Biological_Weapons_Mk3`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Ebola Bomb (`Advanced_Bioweapon_bomb`)

<!-- img:missile Units/Images/Missiles/BioChem/BioBomb_3.png -->

A large airburst bomb designed to disperse a modified strain of Ebola over a target area.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3) (`Biological_Weapons_Mk3`) — technology `Advanced_Bioweapon_Bomb`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1.25 |

**Explosion:**

- `Biological3`: damage 0.4, blast radius 700 km, full effect within 650 km, lasting effect 160 s

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5
- With [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`): can no longer be built

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Ebola ICBM (`Advanced_Bioweapon_ICBM`)

<!-- img:missile Units/Images/Missiles/BioChem/ADV_BIO_ICBM_LIGHT.png -->

An ICBM originally designed for a light nuclear warhead, which has been modified to disperse a modified strain of Ebola instead.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3) (`Biological_Weapons_Mk3`) — technology `Advanced_Bioweapon_ICBM`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `Biological3`: damage 0.4, blast radius 700 km, full effect within 650 km, lasting effect 160 s

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Ebola MRBM (`Advanced_Bioweapon_MRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Adv_Bio_MRBM.png -->

A medium-range ballistic missile outfitted with a warhead designed to disperse a modified strain of Ebola over an area.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3) (`Biological_Weapons_Mk3`) — technology `Advanced_Bioweapon_MRBM`.

**Template:** `Biological`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `Biological3`: damage 0.4, blast radius 700 km, full effect within 650 km, lasting effect 160 s

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance
- With [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### VX Gas Artillery (`Advanced Chemical Artillery`)

<!-- img:missile Units/Images/Missiles/BioChem/CHEM_ARTILLERY_3.png -->

Artillery systems loaded with the nerve agent known as VX Gas. Used by army divisions and army bases to attack opposing armies and bases, but at the cost of causing significant collateral damage and self-inflicted casualties.

**How to get it:** [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`) — technology `M_Chem_Artillery_3`.

**Template:** `ChemicalArtillery`.

**Used by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`).

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 500 |
| `precision` | 2 |

**Explosion:**

- `Chemical_3`: damage 4.5, blast radius 200 km, full effect within 65 km, lasting effect 100 s

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` = 140
- On units with the [“Portable Electronic Optics”](A1-Catalog-Units.md#portable-electronic-optics-portable_electronic_optics_entmod) (`Portable_Electronic_Optics_EntMod`) trait: `range` = 145
- On units with the [“Early Tactical Optics”](A1-Catalog-Units.md#early-tactical-optics-tactical_optics_entmod) (`Tactical_Optics_EntMod`) trait: `range` = 150
- On units with the “Advanced Tactical Optics” (`Advanced_Tactical_Optics_Entmod`) trait (active after researching [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`)): `range` = 155
- On units with the [“Light Unmanned Vehicles”](A1-Catalog-Units.md#light-unmanned-vehicles-light_unmanned_vehicles_entmod) (`Light_Unmanned_Vehicles_EntMod`) trait: `range` = 160
- On units with the [“Robotic Infantry Aids”](A1-Catalog-Units.md#robotic-infantry-aids-robotic_infantry_entmod) (`Robotic_Infantry_EntMod`) trait: `range` = 165

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### VX Gas Bomb (`Advanced_Chemical_bomb`)

<!-- img:missile Units/Images/Missiles/BioChem/ChemBomb_3.png -->

A large airburst bomb designed to disperse the highly toxic nerve agent known as VX Gas over a target area.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`) — technology `Advanced_Chemical_Bomb`.

**Template:** `Chemical`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`).

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |

**Explosion:**

- `Chemical_3`: damage 4.5, blast radius 200 km, full effect within 65 km, lasting effect 100 s

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### VX Gas MRBM (`Advanced_Chemical_MRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Adv_Chem_MRBM_1.png -->

A medium-range ballistic missile outfitted with a warhead designed to disperse VX Gas bomblets over a wide area.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`) — technology `M_Chemical_MRBM_3`.

**Template:** `Chemical`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`).

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |

**Explosion:**

- `Chemical_3`: damage 4.5, blast radius 200 km, full effect within 65 km, lasting effect 100 s; warheads 4 × [VX Gas Bomblet](#vx-gas-bomblet-chemical_warhead_3) (`Chemical_3`: damage 4.5, blast radius 200 km, full effect within 65 km, lasting effect 100 s)

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### VX Gas SRBM (`Advanced_Chemical_SRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Adv_Chem_SRBM_1.png -->

A short-range ballistic missile outfitted with a warhead designed to disperse VX Gas bomblets.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`) — technology `M_Chem_SRBM_3`.

**Template:** `Chemical`.

**Used by:** [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site), [SRBM TEL Vehicle](A1-Catalog-Units.md#srbm-tel-vehicle-mobile_srbm).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

**Replaced after:** [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`).

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `minrange` | 100 |
| `speed` | 2 000 |
| `precision` | 1 |
| `canbeintercepted` | 50% |

**Explosion:**

- `Chemical_3`: damage 4.5, blast radius 200 km, full effect within 65 km, lasting effect 100 s; warheads 3 × [VX Gas Bomblet](#vx-gas-bomblet-chemical_warhead_3) (`Chemical_3`: damage 4.5, blast radius 200 km, full effect within 65 km, lasting effect 100 s)

**Upgrades:**

- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - new appearance
    - `canbeintercepted` ×0.9
    - `precision` ×0.85

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### 3xBW Bioweapon MIRV (`Bioweapon_MIRV`)

<!-- img:missile Units/Images/Missiles/BioChem/BIO_MIRV_ICBM_LIGHT.png -->

An MIRV armed with 3 Medusa Fever bioweapon warheads. The use of multiple warheads allows it to more effectively bypass ABM systems and potentially produce more casualties. Can be fired from launch vehicles.

**How to get it:** [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv) (`Improved_MIRV`) + [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) — technology `M_3x_Bioweapon_MIRV`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 13 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 20 |
| `canbeintercepted` | 30% |
| `productioncost` | 6.5 |

**Explosion:**

- `BiologicalX`: damage 0.75, blast radius 1 000 km, full effect within 900 km, lasting effect 240 s; warheads 3 × [Biological Warhead](#biological-warhead-biological_warhead) (`BiologicalX`: damage 0.75, blast radius 1 000 km, full effect within 900 km, lasting effect 240 s)

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5
- With [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) + [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`): can no longer be built

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### EMeVHF-24 Bomb (`Engineered_Bioweapon_bomb`)

<!-- img:missile Units/Images/Missiles/BioChem/BioBomb_4.png -->

A large airburst bomb designed to disperse the engineered bioweapon known as Medusa Fever over a target area.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) — technology `Engineered_Bioweapon_Bomb`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |
| `productioncost` | 1.25 |

**Explosion:**

- `BiologicalX`: damage 0.75, blast radius 1 000 km, full effect within 900 km, lasting effect 240 s

**Upgrades:**

- On units with the [“Bomb Truck”](A1-Catalog-Units.md#bomb-truck-bomb_truck-2) (`Bomb_Truck`) trait: `range` = 0.5

**Against targets with these traits:**

- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### EMeVHF-24 ICBM (`Engineered_Bioweapon_ICBM`)

<!-- img:missile Units/Images/Missiles/BioChem/EXP_BIO_ICBM_LIGHT.png -->

An ICBM originally designed for a light nuclear warhead, which has been modified to disperse the engineered bioweapon known as Medusa Fever instead.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) — technology `Engineered_Bioweapon_ICBM`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 30 |
| `canbeintercepted` | 30% |
| `productioncost` | 2 |

**Explosion:**

- `BiologicalX`: damage 0.75, blast radius 1 000 km, full effect within 900 km, lasting effect 240 s

**Upgrades:**

- On units with the [“AL-ICBM Range Adjust”](A1-Catalog-Units.md#al-icbm-range-adjust-al-icbm_range_adjust) (`AL-ICBM_Range_Adjust`) trait: `minrange` = 100
- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`): `precision` = 20
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`):
    - `productioncost` ×0.8
    - new appearance
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - `range` ×1.5
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`): `precision` = 5

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### EMeVHF-24 MRBM (`Engineered_Bioweapon_MRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Exp_Bio_MRBM.png -->

A medium-range ballistic missile outfitted with a warhead designed to disperse the engineered bioweapon known as Medusa Fever over an area.  
Does less damage than a similar-sized nuclear weapon, but is capable of infecting other cities within a wide radius and inflicting casualties. Produces no nuclear fallout. Will affect your own cities if they are within range. Use with caution!

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) — technology `Engineered_Bioweapon_MRBM`.

**Template:** `Biological`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |
| `productioncost` | 1.5 |

**Explosion:**

- `BiologicalX`: damage 0.75, blast radius 1 000 km, full effect within 900 km, lasting effect 240 s

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×7.5: [“Unit BioChem Modifier”](A1-Catalog-Units.md#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

### Novichok-2000 Artillery (`Experimental Chemical Artillery`)

<!-- img:missile Units/Images/Missiles/BioChem/CHEM_ARTILLERY_4.png -->

Artillery systems loaded with the Novichok-2000 nerve agent. Used by army divisions and army bases to attack opposing armies and bases, but at the cost of causing significant collateral damage and self-inflicted casualties.

**How to get it:** [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) — technology `M_Chem_Artillery_4`.

**Template:** `ChemicalArtillery`.

**Used by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 500 |
| `precision` | 2 |

**Explosion:**

- `Chemical_4`: damage 6, blast radius 200 km, full effect within 60 km, lasting effect 120 s

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` = 140
- On units with the [“Portable Electronic Optics”](A1-Catalog-Units.md#portable-electronic-optics-portable_electronic_optics_entmod) (`Portable_Electronic_Optics_EntMod`) trait: `range` = 145
- On units with the [“Early Tactical Optics”](A1-Catalog-Units.md#early-tactical-optics-tactical_optics_entmod) (`Tactical_Optics_EntMod`) trait: `range` = 150
- On units with the “Advanced Tactical Optics” (`Advanced_Tactical_Optics_Entmod`) trait (active after researching [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`)): `range` = 155
- On units with the [“Light Unmanned Vehicles”](A1-Catalog-Units.md#light-unmanned-vehicles-light_unmanned_vehicles_entmod) (`Light_Unmanned_Vehicles_EntMod`) trait: `range` = 160
- On units with the [“Robotic Infantry Aids”](A1-Catalog-Units.md#robotic-infantry-aids-robotic_infantry_entmod) (`Robotic_Infantry_EntMod`) trait: `range` = 165

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Novichok-2000 Bomb (`Experimental_Chemical_bomb`)

<!-- img:missile Units/Images/Missiles/BioChem/ChemBomb_4.png -->

A large airburst bomb designed to disperse a highly toxic chemical agent known as Novichok-2000 over a target area.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) — technology `Experimental_Chemical_Bomb`.

**Template:** `Chemical`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 3 |

**Explosion:**

- `Chemical_4`: damage 6, blast radius 200 km, full effect within 60 km, lasting effect 120 s

**Against targets with these traits:**

- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### Novichok-2000 MRBM (`Experimental_Chemical_MRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Exp_Chem_MRBM_1.png -->

A medium-range ballistic missile outfitted with a warhead designed to disperse Novichok-2000 bomblets over a wide area.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) + [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) — technology `M_Chemical_MRBM_4`.

**Template:** `Chemical`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 25 |
| `canbeintercepted` | 45% |

**Explosion:**

- `Chemical_4`: damage 6, blast radius 200 km, full effect within 60 km, lasting effect 120 s; warheads 4 × [Novichok-2000 Bomblet](#novichok-2000-bomblet-chemical_warhead_4) (`Chemical_4`: damage 6, blast radius 200 km, full effect within 60 km, lasting effect 120 s)

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 15
    - new appearance
- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 5
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### Novichok-2000 SRBM (`Experimental_Chemical_SRBM`)

<!-- img:missile Units/Images/Missiles/BioChem/Exp_Chem_SRBM_1.png -->

A short-range ballistic missile outfitted with a warhead designed to disperse Novichok-2000 bomblets.  
Has no production cost, produces no nuclear fallout and can be used to slow down and damage combat engineers, armies and their bases. However, it also has a wide contamination radius and will affect nearby cities and friendly units.

**How to get it:** [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) — technology `M_Chem_SRBM_4`.

**Template:** `Chemical`.

**Used by:** [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site), [SRBM TEL Vehicle](A1-Catalog-Units.md#srbm-tel-vehicle-mobile_srbm).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `minrange` | 100 |
| `speed` | 2 000 |
| `precision` | 1 |
| `canbeintercepted` | 50% |

**Explosion:**

- `Chemical_4`: damage 6, blast radius 200 km, full effect within 60 km, lasting effect 120 s; warheads 3 × [Novichok-2000 Bomblet](#novichok-2000-bomblet-chemical_warhead_4) (`Chemical_4`: damage 6, blast radius 200 km, full effect within 60 km, lasting effect 120 s)

**Upgrades:**

- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - new appearance
    - `canbeintercepted` ×0.9
    - `precision` ×0.85

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×0.015: [“Resist Nuke ABM”](A1-Catalog-Units.md#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`)

### 8xBW Bioweapon MIRV (`8x Bioweapon_MIRV`)

<!-- img:missile Units/Images/Missiles/BioChem/BIO_MIRV_ICBM_LIGHT_2.png -->

An MIRV armed with 8 Medusa Fever bioweapon warheads. The use of multiple warheads allows it to more effectively bypass ABM systems and potentially produce more casualties. Can be fired from launch vehicles.

**How to get it:** [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`) + [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy) (`Novel_BM_Heavy`) — technology `M_8x_Bioweapon_MIRV`.

**Template:** `Biological`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** cities, map points, Army Base, Army Division (Army Division), Army Division (Army Mobile Mode), Army Division (Army Entrenched), Combat Engineers, Forward Operating Base.

| Stat | Base value |
|---|---|
| `range` | 13 500 |
| `minrange` | 3 000 |
| `speed` | 3 000 |
| `precision` | 5 |
| `canbeintercepted` | 30% |
| `productioncost` | 6.5 |

**Explosion:**

- `BiologicalX`: damage 0.75, blast radius 1 000 km, full effect within 900 km, lasting effect 240 s; warheads 8 × [Biological Warhead](#biological-warhead-biological_warhead) (`BiologicalX`: damage 0.75, blast radius 1 000 km, full effect within 900 km, lasting effect 240 s)

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `productioncost` ×0.8
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.5: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`), [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×0.8: [“Basic CBRN Defence”](A1-Catalog-Units.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`), [“CBRN Countermeasures”](A1-Catalog-Units.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)
- `damage` ×0.85: [“Specialized CBRN Reconnaissance”](A1-Catalog-Units.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`), [“Advanced CBRN Equipment”](A1-Catalog-Units.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`), [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)

## Air and missile defence

### AA Gun (`AA Gun Old`)

<!-- img:missile Units/Images/Missiles/AAGun.png -->

A Basic Anti-Aircraft Gun. Effective at short range against certain types of aircraft, especially helicopters.

**How to get it:** available from the start — technology `M_AA_Gun_Old`.

**Template:** `AntiAir`.

**Used by:** [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [AA Gun Site](A1-Catalog-Units.md#aa-gun-site-aa_site_old), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 3 000 |
| `precision` | 12 |
| `maxelevation` | 30 |

**Explosion:**

- `Gunfire_AA`: damage 0.07, blast radius 5 km, full effect within 0.2 km

**Upgrades:**

- With [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`):
    - `range` = 140
    - `precision` = 9
- With [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization) (`Weapon_Modernization`): `damage` ×1.1
- With [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`):
    - `range` = 160
    - `precision` = 8
- With [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons) (`Improved_Army_Weapons`): `damage` ×1.1
- With [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`):
    - `range` = 180
    - `precision` = 7
- With [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons) (`Enhanced_Army_Weapons`): `damage` ×1.1
- With [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons) (`Advanced_Army_Weapons`): `damage` ×1.1
- With [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5) (`SW_Mk5`):
    - `range` = 200
    - `precision` = 6.5
- With [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons) (`Experimental_Army_Weapons`): `damage` ×1.1

**Against targets with these traits:**

- `damage` ×1.2: [“Helicopters”](A1-Catalog-Units.md#helicopters-helicopter_modifier) (`Helicopter_Modifier`)

### Autocannon (`Plane Gun`)

<!-- img:missile Units/Images/Missiles/PLANE GUN.png -->

A large-caliber plane-mounted cannon capable of extremely rapid fire. Mounted on small fixed-wing combat aircraft and effective against other planes at short range.

**How to get it:** available from the start — technology `M_Plane_Gun`.

**Template:** `AntiAir`.

**Used by:** [Fighter](A1-Catalog-Units.md#fighter-fighter), [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 250 |
| `speed` | 5 000 |
| `precision` | 0.75 |
| `maxelevation` | 40 |

**Explosion:**

- `Gunfire_Plane`: damage 0.25, blast radius 5 km, full effect within 0.2 km

**Upgrades:**

- With [2nd Generation Aircraft](A5-Catalog-Technologies.md#2nd-generation-aircraft-generation_2_aircraft) (`Generation_2_Aircraft`): `damage` ×1.1
- With [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft) (`Generation_3_Aircraft`): `damage` ×1.2

### Midcourse ABM (ABM Submunition) (`ABM Submunition`)

<!-- img:missile Units/Images/Missiles/ABM.png -->

An anti-ballistic missile designed to destroy incoming missiles in the midcourse phase of their trajectory.

**How to get it:** available from the start — technology `M_anti_ballistic_missile_sub`.

**Template:** `AntiMissileMidcourse`.

**Can be fired at:** ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 1 600 |
| `speed` | 8 500 |
| `precision` | 0.05 |
| `maxelevation` | 10 000 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

### Space-To-Ground Laser (`Fusion Laser`)

<!-- img:missile Units/Images/Missiles/LASER_HP.png -->

An extremely powerful nuclear-powered laser, capable of penetrating the Earth's atmosphere and damaging and destroying targets on the ground.

**How to get it:** available from the start — technology `M_Satellite_Laser_Fusion`.

**Template:** `CFLaser`.

**Used by:** [Counterforce Laser Satellite](A1-Catalog-Units.md#counterforce-laser-satellite-countervalue_laser_satellite).

**Can be fired at:** ground units, ships.

| Stat | Base value |
|---|---|
| `range` | 0 |
| `speed` | 200 000 |
| `precision` | 1 |

**Explosion:**

- `DEW_Sat_Laser`: damage 5, blast radius 10 km, full effect within 3 km

**Situational effects:**

- Inside the range of an active friendly [Satellite Relay](#satellite-relay-satellite-relay): `range` = 1 250

### AAM (`AAM`)

<!-- img:missile Units/Images/Missiles/AAM.png -->

An air-to-air missile, used by combat aircraft to destroy other aircraft.

**How to get it:** [Early Infrared Air-to-Air Missiles](A5-Catalog-Technologies.md#early-infrared-air-to-air-missiles-air_to_air_missile) (`Air_to_Air_Missile`) — technology `M_Air_to_air_missile`.

**Template:** `AntiAir`.

**Used by:** [Fighter](A1-Catalog-Units.md#fighter-fighter), [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 300 |
| `speed` | 2 000 |
| `precision` | 0.1 |
| `maxelevation` | 75 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [All-Aspect AAMs](A5-Catalog-Technologies.md#all-aspect-aams-aam_improved) (`AAM_Improved`):
    - new appearance
    - `precision` ×0.75
    - `range` = 400
    - `speed` = 2 250
- With [F&F Radar-Guided AAMs](A5-Catalog-Technologies.md#ff-radar-guided-aams-aam_enhanced) (`AAM_Enhanced`):
    - new appearance
    - `precision` ×0.75
    - `range` = 500
    - `speed` = 3 000
- With [Off-Boresight Ramjet AAMs](A5-Catalog-Technologies.md#off-boresight-ramjet-aams-aam_advanced) (`AAM_Advanced`):
    - new appearance
    - `precision` ×0.75
    - `range` = 600
    - `speed` = 3 750
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `precision` ×0.8
- With [Advanced Hybrid Guidance AAMs](A5-Catalog-Technologies.md#advanced-hybrid-guidance-aams-aam_experimental) (`AAM_Experimental`):
    - new appearance
    - `range` = 800
    - `speed` = 5 000
    - `damage` ×1.5

**Against targets with these traits:**

- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `range` ×0.75: [“Helicopters”](A1-Catalog-Units.md#helicopters-helicopter_modifier) (`Helicopter_Modifier`)

### Heavy SAM (`SAM`)

<!-- img:missile Units/Images/Missiles/SAM.png -->

A heavy surface-to-air missile system used by fixed sites, specialized vehicles and certain warships to shoot down enemy aircraft from long range.  
Can be upgraded to intercept incoming missiles with the appropriate technology.

**How to get it:** [Surface-To-Air Missiles](A5-Catalog-Technologies.md#surface-to-air-missiles-surface_to_air_missile) (`Surface_to_air_missile`) — technology `M_Surface_to_air_missile`.

**Template:** `AntiAir`.

**Used by:** [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [SAM Site](A1-Catalog-Units.md#sam-site-sam_site), [Mobile SAM](A1-Catalog-Units.md#mobile-sam-mobile_sam).

**Can be fired at:** aircraft.

**Replaced after:** [Missile Defence SAMs](A5-Catalog-Technologies.md#missile-defence-sams-tac_missile_defence) (`Tac_Missile_Defence`).

| Stat | Base value |
|---|---|
| `range` | 300 |
| `speed` | 3 000 |
| `precision` | 0.16 |
| `maxelevation` | 75 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2) (`SAM_Mk2`):
    - `range` = 400
    - `speed` = 3 500
    - `precision` ×0.75
    - new appearance

**Against targets with these traits:**

- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### CIWS (`CIWS`)

<!-- img:missile Units/Images/Missiles/CIWS.png -->

Close-In Weapons Systems, or CIWS, are designed to shoot down incoming missiles as a last-line of defence.

**How to get it:** [Missile-Armed Warships](A5-Catalog-Technologies.md#missile-armed-warships-missile_warships) (`Missile_Warships`) + [Close-In Weapon Systems](A5-Catalog-Technologies.md#close-in-weapon-systems-close_in_weapon_systems) (`Close_In_Weapon_Systems`) — technology `M_CIWS`.

**Template:** `AntiMissile`.

**Used by:** [Carrier](A1-Catalog-Units.md#carrier-carrier), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station), [Landing Ship](A1-Catalog-Units.md#landing-ship-landing_ship).

**Can be fired at:** missiles.

**Replaced after:** [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`) + [High-Powered Lasers](A5-Catalog-Technologies.md#high-powered-lasers-high_powered_lasers) (`High_Powered_Lasers`) + [Laser CIWS](A5-Catalog-Technologies.md#laser-ciws-laser_ciws) (`Laser_CIWS`).

| Stat | Base value |
|---|---|
| `range` | 135 |
| `speed` | 5 000 |
| `precision` | 0.3 |
| `maxelevation` | 50 |

**Explosion:**

- `Gunfire_Plane`: damage 0.25, blast radius 5 km, full effect within 0.2 km

### LAAM (`LAAM`)

<!-- img:missile Units/Images/Missiles/LAAM_1.png -->

A long-range air-to-air missile, used by interceptor aircraft. Very effective against large aircraft like bombers, AWACS and spy planes, but less effective against fighter-sized aircraft, and incapable of engaging helicopters.

**How to get it:** [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft) (`Interceptor_aircraft`) — technology `M_LAAM`.

**Template:** `AntiAir`.

**Used by:** [Interceptor](A1-Catalog-Units.md#interceptor-interceptor).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 500 |
| `minrange` | 150 |
| `speed` | 2 750 |
| `precision` | 0.15 |
| `maxelevation` | 100 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft) (`Interceptor_aircraft`): `damage` ×1.5
- With [All-Aspect AAMs](A5-Catalog-Technologies.md#all-aspect-aams-aam_improved) (`AAM_Improved`):
    - new appearance
    - `range` = 600
    - `speed` = 3 000
- With [F&F Radar-Guided AAMs](A5-Catalog-Technologies.md#ff-radar-guided-aams-aam_enhanced) (`AAM_Enhanced`):
    - new appearance
    - `precision` ×0.75
    - `range` = 800
    - `speed` = 3 500
- With [Off-Boresight Ramjet AAMs](A5-Catalog-Technologies.md#off-boresight-ramjet-aams-aam_advanced) (`AAM_Advanced`):
    - new appearance
    - `precision` ×0.75
    - `range` = 1 000
    - `speed` = 4 500
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `precision` ×0.8
- With [Advanced Hybrid Guidance AAMs](A5-Catalog-Technologies.md#advanced-hybrid-guidance-aams-aam_experimental) (`AAM_Experimental`):
    - new appearance
    - `range` = 1 200
    - `speed` = 7 000
    - `damage` ×1.5

**Against targets with these traits:**

- `precision` ×5: “Fighter” (`U_Fighter`), “Multirole Attacker” (`U_Attack`), “Interceptor” (`U_Interceptor`)
- `maxelevation` ×0: [“Helicopters”](A1-Catalog-Units.md#helicopters-helicopter_modifier) (`Helicopter_Modifier`)
- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### Light SAM (`Light SAM`)

<!-- img:missile Units/Images/Missiles/LIGHT_SAM.png -->

A lightweight surface-to-air missile carried by vehicles to protect against attacking aircraft.  
Can be upgraded to intercept incoming missiles with the appropriate technology.

**How to get it:** [Mobile SAM Systems](A5-Catalog-Technologies.md#mobile-sam-systems-mobile_sam) (`Mobile_SAM`) — technology `M_Light_SAM`.

**Template:** `AntiAir`.

**Used by:** [Carrier](A1-Catalog-Units.md#carrier-carrier), [AA Gun Site](A1-Catalog-Units.md#aa-gun-site-aa_site_old), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** aircraft.

**Replaced after:** [Missile Defence SAMs](A5-Catalog-Technologies.md#missile-defence-sams-tac_missile_defence) (`Tac_Missile_Defence`).

| Stat | Base value |
|---|---|
| `range` | 200 |
| `speed` | 2 500 |
| `precision` | 0.25 |
| `maxelevation` | 35 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2) (`SAM_Mk2`):
    - `range` = 250
    - `speed` = 2 750
    - `precision` ×0.75

**Against targets with these traits:**

- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### MANPADS (`MANPAD`)

<!-- img:missile Units/Images/Missiles/MANPAD.png -->

Man-Portable Air Defence System. A shoulder-fired guided missile launcher used to destroy enemy aircraft.

**How to get it:** [Surface-To-Air Missiles](A5-Catalog-Technologies.md#surface-to-air-missiles-surface_to_air_missile) (`Surface_to_air_missile`) + [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons) (`Improved_Army_Weapons`) — technology `M_MANPAD`.

**Template:** `AntiAir`.

**Used by:** [Spec-Ops Team](A1-Catalog-Units.md#spec-ops-team-spec_ops_team), [Attack Helicopter](A1-Catalog-Units.md#attack-helicopter-attack_helicopter), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station), [Security Checkpoint](A1-Catalog-Units.md#security-checkpoint-security_checkpoint), [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Forward Operating Base](A1-Catalog-Units.md#forward-operating-base-forward_operating_base), [Combat Engineers](A1-Catalog-Units.md#combat-engineers-combat_engineers), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 1 000 |
| `precision` | 0.15 |
| `maxelevation` | 15 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- On units with the [“Helicopters”](A1-Catalog-Units.md#helicopters-helicopter_modifier) (`Helicopter_Modifier`) trait: `maxelevation` = 6
- With [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2) (`SAM_Mk2`):
    - `range` +30
    - `speed` = 1 250
    - `precision` ×0.8
- With [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons) (`Enhanced_Army_Weapons`): `damage` ×1.2
- With [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons) (`Advanced_Army_Weapons`): `damage` ×1.2
- With [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3) (`SAM_Mk3`):
    - `range` +25
    - `speed` = 1 500
    - `precision` ×0.8
- With [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons) (`Experimental_Army_Weapons`): `damage` ×1.2
- With [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4) (`SAM_Mk4`):
    - `range` +25
    - `speed` = 2 000
    - `precision` ×0.8

**Against targets with these traits:**

- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### Midcourse ABM (ABM) (`ABM`)

<!-- img:missile Units/Images/Missiles/ABM.png -->

An anti-ballistic missile designed to destroy incoming missiles in the midcourse phase of their trajectory.

**How to get it:** [Conventional Midcourse ABM](A5-Catalog-Technologies.md#conventional-midcourse-abm-anti_ballistic_missile) (`anti_ballistic_missile`) — technology `M_anti_ballistic_missile`.

**Template:** `AntiMissileMidcourse`.

**Used by:** [Midcourse ABM Site](A1-Catalog-Units.md#midcourse-abm-site-abm_site).

**Can be fired at:** ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `minrange` | 650 |
| `speed` | 7 250 |
| `precision` | 0.05 |
| `maxelevation` | 9 000 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Hit-To-Kill Midcourse ABM](A5-Catalog-Technologies.md#hit-to-kill-midcourse-abm-abm_mk2) (`ABM_Mk2`):
    - `range` = 1 200
    - `speed` = 7 500
    - new appearance
    - `maxelevation` = 9 000
- With [Advanced Midcourse ABM](A5-Catalog-Technologies.md#advanced-midcourse-abm-abm_mk3) (`ABM_Mk3`):
    - `range` = 1 400
    - `speed` = 8 000
    - new appearance
    - `maxelevation` = 9 500
- With [Experimental Midcourse ABM](A5-Catalog-Technologies.md#experimental-midcourse-abm-abm_mk4) (`ABM_Mk4`):
    - `heads` = 3
    - `range` = 1 600
    - `speed` = 8 500
    - new appearance
    - `maxelevation` = 10 000

### Terminal ABM (`Terminal ABM`)

<!-- img:missile Units/Images/Missiles/ABM_Terminal.png -->

An anti-ballistic missile used to defeat incoming warheads in the last phase of their trajectory. Very effective at short range, but has limited reach and struggles against multiple targets.

**How to get it:** [Terminal Ballistic Missile Defences](A5-Catalog-Technologies.md#terminal-ballistic-missile-defences-terminal_bm_defence) (`Terminal_BM_Defence`) — technology `M_Terminal_ABM`.

**Template:** `AntiMissileTerminal`.

**Used by:** [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Terminal ABM Site](A1-Catalog-Units.md#terminal-abm-site-terminal_abm).

**Can be fired at:** missiles, ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 300 |
| `speed` | 9 000 |
| `precision` | 0.05 |
| `maxelevation` | 200 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Hit-To-Kill Terminal ABM](A5-Catalog-Technologies.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2) (`Terminal_BM_Defence_Mk2`):
    - `range` = 350
    - `speed` = 9 250
    - `maxelevation` = 225
    - new appearance
- With [Advanced Terminal ABM](A5-Catalog-Technologies.md#advanced-terminal-abm-terminal_bm_defence_mk3) (`Terminal_BM_Defence_Mk3`):
    - `range` = 400
    - `speed` = 9 500
    - `maxelevation` = 250
    - new appearance

### Heavy Missile Defence SAM (`SAM MD`)

<!-- img:missile Units/Images/Missiles/sam_mk2.png -->

A heavy surface-to-air missile system used by fixed sites, specialized vehicles and certain warships to shoot down enemy aircraft from long range.  
This model has been upgraded to be able to intercept incoming missiles as well as aircraft.

**How to get it:** [Missile Defence SAMs](A5-Catalog-Technologies.md#missile-defence-sams-tac_missile_defence) (`Tac_Missile_Defence`) — technology `M_Surface_to_air_missile_MD`.

**Template:** `AntiMissileAA`.

**Used by:** [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [SAM Site](A1-Catalog-Units.md#sam-site-sam_site), [Mobile SAM](A1-Catalog-Units.md#mobile-sam-mobile_sam).

**Can be fired at:** aircraft, missiles.

| Stat | Base value |
|---|---|
| `range` | 400 |
| `speed` | 3 500 |
| `precision` | 0.12 |
| `maxelevation` | 75 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3) (`SAM_Mk3`):
    - `range` = 550
    - `speed` = 4 000
    - `precision` ×0.65
    - `damage` ×1.4
- With [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4) (`SAM_Mk4`):
    - `range` = 700
    - `speed` = 6 000
    - `precision` ×0.65
    - `damage` ×1.4

**Against targets with these traits:**

- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### Light Missile Defence SAM (`Light SAM MD`)

<!-- img:missile Units/Images/Missiles/LIGHT_SAM.png -->

A lightweight surface-to-air missile carried by vehicles to protect against attacking aircraft.  
This model has been upgraded to be able to intercept incoming missiles as well as aircraft.

**How to get it:** [Missile Defence SAMs](A5-Catalog-Technologies.md#missile-defence-sams-tac_missile_defence) (`Tac_Missile_Defence`) — technology `M_Light_SAM_MD`.

**Template:** `AntiMissileAA`.

**Used by:** [Carrier](A1-Catalog-Units.md#carrier-carrier), [AA Gun Site](A1-Catalog-Units.md#aa-gun-site-aa_site_old), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** aircraft, missiles.

| Stat | Base value |
|---|---|
| `range` | 250 |
| `speed` | 2 750 |
| `precision` | 0.188 |
| `maxelevation` | 35 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3) (`SAM_Mk3`):
    - `range` = 325
    - `speed` = 3 250
    - `precision` ×0.75
- With [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4) (`SAM_Mk4`):
    - `damage` ×1.2
    - `range` = 425
    - `speed` = 4 000
    - `precision` ×0.75
    - `damage` ×1.25

**Against targets with these traits:**

- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### C-RAM (`C-RAM`)

<!-- img:missile Units/Images/Missiles/CIWS.png -->

Counter Rocket Artillery Mortar systems, or C-RAM, are point-defence systems used to destroy incoming explosive projectiles before they can hit the ground.

**How to get it:** [Counter-RAM Systems](A5-Catalog-Technologies.md#counter-ram-systems-counter_rocket_artillery_mortar) (`Counter_Rocket_Artillery_Mortar`) — technology `M_CRAM`.

**Template:** `AntiMissile`.

**Used by:** [Air Base](A1-Catalog-Units.md#air-base-airport), [Tactical Airbase](A1-Catalog-Units.md#tactical-airbase-tactical_airbase), [Specialized Airbase](A1-Catalog-Units.md#specialized-airbase-specialized_airport), [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Forward Operating Base](A1-Catalog-Units.md#forward-operating-base-forward_operating_base), [Combat Engineers](A1-Catalog-Units.md#combat-engineers-combat_engineers), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** missiles.

| Stat | Base value |
|---|---|
| `range` | 135 |
| `speed` | 5 000 |
| `precision` | 0.3 |
| `maxelevation` | 50 |

**Explosion:**

- `Gunfire_Plane`: damage 0.25, blast radius 5 km, full effect within 0.2 km

### Laser CIWS (`Laser CIWS`)

<!-- img:missile Units/Images/Missiles/LASER_CIWS.png -->

A Laser Close-in Weapon System is a defence system that uses a high-powered laser to blind and prematurely detonate incoming missiles.

**How to get it:** [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`) + [High-Powered Lasers](A5-Catalog-Technologies.md#high-powered-lasers-high_powered_lasers) (`High_Powered_Lasers`) + [Laser CIWS](A5-Catalog-Technologies.md#laser-ciws-laser_ciws) (`Laser_CIWS`) — technology `M_Laser_CIWS`.

**Template:** `AntiMissile`.

**Used by:** [Carrier](A1-Catalog-Units.md#carrier-carrier), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station), [Landing Ship](A1-Catalog-Units.md#landing-ship-landing_ship).

**Can be fired at:** missiles.

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 5 000 |
| `precision` | 0.75 |
| `maxelevation` | 100 |

**Explosion:**

- `std_torpedo`: damage 3, blast radius 0.1 km, full effect within 0.025 km

### Aircraft Laser (`Plane Laser`)

<!-- img:missile Units/Images/Missiles/LASER_HP.png -->

A high-powered laser used by highly advanced aircraft for air-to-air combat.

**How to get it:** [Anti-Air Laser Weapons](A5-Catalog-Technologies.md#anti-air-laser-weapons-aa_laser) (`AA_Laser`) + [Deadly Laser Weapons](A5-Catalog-Technologies.md#deadly-laser-weapons-offensive_laser_weapons) (`Offensive_Laser_Weapons`) — technology `M_Plane_Laser`.

**Template:** `AntiAir`.

**Used by:** [Fighter](A1-Catalog-Units.md#fighter-fighter), [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 275 |
| `speed` | 5 000 |
| `precision` | 0.95 |
| `maxelevation` | 100 |

**Explosion:**

- `Laser_Plane`: damage 0.25, blast radius 1 km, full effect within 0.2 km

### Anti-Air Laser (`AA Laser`)

<!-- img:missile Units/Images/Missiles/LASER_HP.png -->

A high-powered laser capable of shooting down aircraft.

**How to get it:** [Anti-Air Laser Weapons](A5-Catalog-Technologies.md#anti-air-laser-weapons-aa_laser) (`AA_Laser`) + [Deadly Laser Weapons](A5-Catalog-Technologies.md#deadly-laser-weapons-offensive_laser_weapons) (`Offensive_Laser_Weapons`) — technology `M_AA_Laser`.

**Template:** `AntiAir`.

**Used by:** [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** aircraft.

| Stat | Base value |
|---|---|
| `range` | 250 |
| `speed` | 5 000 |
| `precision` | 0.9 |
| `maxelevation` | 60 |

**Explosion:**

- `Laser_Plane`: damage 0.25, blast radius 1 km, full effect within 0.2 km

### Terminal Defence Laser (`Terminal ABM Laser`)

<!-- img:missile Units/Images/Missiles/LASER_HP.png -->

A massively powerful laser capable of delivering the energy needed to destroy incoming high-speed ballistic missiles. Extremely effective as a point defence weapon against single warheads, but has a limited effective range and can be overwhelmed by multiple warheads.

**How to get it:** [Terminal Defence Lasers](A5-Catalog-Technologies.md#terminal-defence-lasers-terminal_defence_laser) (`Terminal_Defence_Laser`) + [Deadly Laser Weapons](A5-Catalog-Technologies.md#deadly-laser-weapons-offensive_laser_weapons) (`Offensive_Laser_Weapons`) — technology `M_Terminal_ABM_Laser`.

**Template:** `AntiAirAll`.

**Used by:** [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Mobile Defence Laser](A1-Catalog-Units.md#mobile-defence-laser-mobile_abm_laser), [Laser Defence Complex](A1-Catalog-Units.md#laser-defence-complex-laser_defence_complex).

**Can be fired at:** aircraft, missiles, ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 225 |
| `speed` | 9 000 |
| `precision` | 0.95 |
| `maxelevation` | 250 |

**Explosion:**

- `big_bomb`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` = 275

## Naval weapons

### Depth Charge (`DepthCharge`)

<!-- img:missile Units/Images/Missiles/DEPTH_CHARGE.png -->

A bomb designed to explode at a certain depth underwater to destroy enemy submarines. Used by naval helicopters.

**How to get it:** available from the start — technology `M_DepthCharge`.

**Template:** `DepthCharge`.

**Used by:** [Naval Helicopter](A1-Catalog-Units.md#naval-helicopter-navy_helicopter).

**Can be fired at:** submarines.

**Replaced after:** [Guided Torpedoes](A5-Catalog-Technologies.md#guided-torpedoes-guided_torpedoes) (`Guided_Torpedoes`).

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 0.9 |

**Explosion:**

- `std_torpedo`: damage 3, blast radius 0.1 km, full effect within 0.025 km

### Torpedo (`Torpedo`)

<!-- img:missile Units/Images/Missiles/Torpedo_1.png -->

An underwater weapon that can be used to target submarines and surface ships.

**How to get it:** available from the start — technology `M_Torpedo`.

**Template:** `Torpedo`.

**Used by:** [Attack Submarine (Submarine)](A1-Catalog-Units.md#attack-submarine-submarine-submarine), [SSGN (SSGN)](A1-Catalog-Units.md#ssgn-ssgn-ssgn), [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer).

**Can be fired at:** ships, submarines.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `speed` | 100 |
| `precision` | 1.2 |

**Explosion:**

- `std_torpedo`: damage 3, blast radius 0.1 km, full effect within 0.025 km

**Upgrades:**

- On units with the [“Submarine Stealth”](A1-Catalog-Units.md#submarine-stealth-submarine_stealth) (`Submarine_Stealth`) trait:
    - `range` ×1.1
    - `damage` ×1.35
    - `precision` ×0.85
- With [Guided Torpedoes](A5-Catalog-Technologies.md#guided-torpedoes-guided_torpedoes) (`Guided_Torpedoes`):
    - new appearance
    - `precision` ×0.75
    - `range` = 220
- With [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`):
    - new appearance
    - `range` = 275
    - `speed` = 120
- With [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons) (`Enhanced_Underwater_Weapons`):
    - new appearance
    - `range` = 300
    - `speed` = 125
    - `precision` ×0.75
- With [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons) (`Advanced_Underwater_Weapons`):
    - new appearance
    - `damage` ×1.2
    - `range` = 310
    - `speed` = 130
    - `precision` ×0.75
- With [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons) (`Experimental_Underwater_Weapons`):
    - new appearance
    - `range` = 325
    - `speed` = 150
    - `precision` ×0.75

**Against targets with these traits:**

- `precision` ×1.5: [“Antitorpedo”](A1-Catalog-Units.md#antitorpedo-antitorpedo) (`Antitorpedo`)
- `damage` ×0.35: [“Torpedo Net Mod”](A1-Catalog-Units.md#torpedo-net-mod-torpedo_net_mod) (`Torpedo_Net_Mod`)

### Airdropped Torpedo (`Air-Dropped Torpedo`)

<!-- img:missile Units/Images/Missiles/LIGHT_TORPEDO.png -->

A lightweight homing torpedo which can be deployed by air. Replaces depth charges and is effective against submarines. Deployed by naval helicopters.

**How to get it:** [Guided Torpedoes](A5-Catalog-Technologies.md#guided-torpedoes-guided_torpedoes) (`Guided_Torpedoes`) — technology `M_Airdropped_Torpedo`.

**Template:** `DepthCharge`.

**Used by:** [Naval Helicopter](A1-Catalog-Units.md#naval-helicopter-navy_helicopter).

**Can be fired at:** submarines.

| Stat | Base value |
|---|---|
| `range` | 75 |
| `speed` | 100 |
| `precision` | 1.2 |

**Explosion:**

- `std_torpedo`: damage 3, blast radius 0.1 km, full effect within 0.025 km

**Upgrades:**

- With [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`): `precision` ×0.8
- With [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons) (`Enhanced_Underwater_Weapons`): `precision` ×0.75
- With [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons) (`Advanced_Underwater_Weapons`): `precision` ×0.75
- With [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons) (`Experimental_Underwater_Weapons`): `precision` ×0.75

**Against targets with these traits:**

- `precision` ×1.5: [“Antitorpedo”](A1-Catalog-Units.md#antitorpedo-antitorpedo) (`Antitorpedo`)

### ASROC (`ASROC`)

<!-- img:missile Units/Images/Missiles/ASROC.png -->

An Anti-Submarine Rocket. This weapon consists of a rocket which houses a torpedo. The rocket is launched over long distances, and then deploys the torpedo upon hitting the water. The torpedo then homes in on enemy submarines and destroys them.

**How to get it:** [Missile-Armed Warships](A5-Catalog-Technologies.md#missile-armed-warships-missile_warships) (`Missile_Warships`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) — technology `M_ASROC`.

**Template:** `DepthCharge`.

**Used by:** [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station).

**Can be fired at:** submarines.

| Stat | Base value |
|---|---|
| `range` | 400 |
| `speed` | 700 |
| `precision` | 1.8 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons) (`Enhanced_Underwater_Weapons`):
    - `range` ×1.25
    - `damage` ×1.1
- With [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons) (`Advanced_Underwater_Weapons`):
    - `range` ×1.1
    - `precision` ×0.75
- With [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons) (`Experimental_Underwater_Weapons`):
    - `range` ×1.1
    - `damage` ×1.2
    - `precision` ×0.8

## Conventional strike weapons

### Anti-Ship Gun (`Coastal Gun Old`)

<!-- img:missile Units/Images/Missiles/Coastal_Gun_Old.png -->

A large-caliber, unguided coastal anti-ship gun firing heavy shells. Used by coastal gun sites.

**How to get it:** available from the start — technology `M_Coastal_Gun_Old`.

**Used by:** [Fixed Coastal Gun](A1-Catalog-Units.md#fixed-coastal-gun-fixed_coastal_gun).

**Can be fired at:** ships.

| Stat | Base value |
|---|---|
| `range` | 500 |
| `speed` | 800 |
| `precision` | 0.7 |
| `canbeintercepted` | 40% |

**Explosion:**

- `big_bomb_old`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)

### Bombs (`Free fall bomb`)

<!-- img:missile Units/Images/Missiles/bomb.png -->

Unguided free-fall iron bombs. Destructive, but crude and inaccurate, which limits their effectiveness.

**How to get it:** available from the start — technology `M_Free_fall_bomb`.

**Template:** `Default`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `precision` | 1.75 |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Against targets with these traits:**

- `damage` ×1 500 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Car Bomb (`Car Bomb`)

<!-- img:missile Units/Images/Missiles/Demo_Charge.png -->

A large explosive device planted in a motor vehicle and then detonated remotely or as a suicide weapon. Can be used to damage or destroy static infrastructure like radar sites or buildings. Far less effective than nuclear weapons, but does not come with a production cost.

**How to get it:** available from the start — technology `M_Car_Bomb`.

**Template:** `Default`.

**Used by:** [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 0.5 |
| `precision` | 0.1 |

**Explosion:**

- `Big_Conventional`: damage 5, blast radius 1.2 km, full effect within 0.15 km

**Upgrades:**

- With [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization) (`Weapon_Modernization`): `damage` ×1.15
- With [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons) (`Improved_Army_Weapons`): `damage` ×1.15
- With [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons) (`Enhanced_Army_Weapons`): `damage` ×1.15
- With [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons) (`Advanced_Army_Weapons`): `damage` ×1.15
- With [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons) (`Experimental_Army_Weapons`): `damage` ×1.15

### Chaingun (`Chaingun`)

<!-- img:missile Units/Images/Missiles/CHAINGUN.png -->

A chin-mounted chaingun used by attack helicopters to engage infantry and other soft targets, such as light vehicles and structures.

**How to get it:** available from the start — technology `M_Chaingun`.

**Template:** `Default`.

**Used by:** [Attack Helicopter](A1-Catalog-Units.md#attack-helicopter-attack_helicopter).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `speed` | 5 000 |
| `precision` | 1.5 |

**Explosion:**

- `Gunfire_Plane`: damage 0.25, blast radius 5 km, full effect within 0.2 km

### Combined Arms (Land Forces Mobile) (`Land Forces Mobile`)

<!-- img:missile Units/Images/Missiles/COMBINED_ARMS.png -->

The mixed weapons used by an army division performing combined arms tactics, ranging from infantry small arms, to vehicle autocannons, to heavy tank guns, to howitzers.

**How to get it:** available from the start — technology `M_Land_Force_ARMY`.

**Template:** `Army`.

**Can be fired at:** ground units.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 2 000 |
| `precision` | 0.25 |

**Explosion:**

- `Gunfire_Army`: damage 0.5, blast radius 4 km, full effect within 2 km

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`):
    - `damage` ×1.05
    - new appearance
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`):
    - `damage` ×1.05
    - new appearance
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`):
    - `damage` ×1.025
    - new appearance
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`):
    - `damage` ×1.025
    - new appearance

**Against targets with these traits:**

- `damage` ×5: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Combined Arms (Land Forces) (`Land Forces`)

<!-- img:missile Units/Images/Missiles/COMBINED_ARMS.png -->

The mixed weapons used by an army division performing combined arms tactics, ranging from infantry small arms, to vehicle autocannons, to heavy tank guns, to howitzers.

**How to get it:** available from the start — technology `M_Land_Force_ARMY`.

**Template:** `Army`.

**Used by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** ground units.

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 2 000 |
| `precision` | 0.25 |

**Explosion:**

- `Gunfire_Army`: damage 0.5, blast radius 4 km, full effect within 2 km

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` = 140
- With [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization) (`Weapon_Modernization`): `damage` ×1.15
- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`):
    - `damage` ×1.05
    - new appearance
- On units with the [“Portable Electronic Optics”](A1-Catalog-Units.md#portable-electronic-optics-portable_electronic_optics_entmod) (`Portable_Electronic_Optics_EntMod`) trait: `range` = 145
- With [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics) (`Portable_Electronic_Optics`): `damage` ×1.025
- With [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons) (`Improved_Army_Weapons`): `damage` ×1.15
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`):
    - `damage` ×1.05
    - new appearance
- On units with the [“Early Tactical Optics”](A1-Catalog-Units.md#early-tactical-optics-tactical_optics_entmod) (`Tactical_Optics_EntMod`) trait: `range` = 150
- With [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics) (`Tactical_Optics`): `damage` ×1.025
- With [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons) (`Enhanced_Army_Weapons`): `damage` ×1.15
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`):
    - `damage` ×1.025
    - new appearance
- On units with the “Advanced Tactical Optics” (`Advanced_Tactical_Optics_Entmod`) trait (active after researching [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`)): `range` = 155
- With [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`): `damage` ×1.025
- With [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons) (`Advanced_Army_Weapons`): `damage` ×1.15
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`):
    - `damage` ×1.025
    - new appearance
- On units with the [“Light Unmanned Vehicles”](A1-Catalog-Units.md#light-unmanned-vehicles-light_unmanned_vehicles_entmod) (`Light_Unmanned_Vehicles_EntMod`) trait: `range` = 160
- With [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles) (`Light_Unmanned_Vehicles`): `damage` ×1.025
- With [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons) (`Experimental_Army_Weapons`): `damage` ×1.15
- On units with the [“Robotic Infantry Aids”](A1-Catalog-Units.md#robotic-infantry-aids-robotic_infantry_entmod) (`Robotic_Infantry_EntMod`) trait: `range` = 165
- With [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry) (`Robotic_Infantry`): `damage` ×1.025

**Against targets with these traits:**

- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)
- `damage` ×5: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Demolition Charge (`Demolition Charge`)

<!-- img:missile Units/Images/Missiles/Demo_Charge.png -->

An explosive charge used to destroy things. Used by spec-ops teams to destroy enemy equipment.

**How to get it:** available from the start — technology `M_Demolition_Charge`.

**Template:** `Default`.

**Used by:** [Spec-Ops Team](A1-Catalog-Units.md#spec-ops-team-spec_ops_team).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 37 |
| `speed` | 10 000 |
| `precision` | 0 |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- On units with the [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`) trait: `damage` ×10
- With [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization) (`Weapon_Modernization`): `damage` ×1.15
- With [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons) (`Improved_Army_Weapons`): `damage` ×1.15
- With [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons) (`Enhanced_Army_Weapons`): `damage` ×1.15
- With [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons) (`Advanced_Army_Weapons`): `damage` ×1.15
- With [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons) (`Experimental_Army_Weapons`): `damage` ×1.15

**Against targets with these traits:**

- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)
- `range` = 37: [“Cyber Warfare Center”](A1-Catalog-Units.md#cyber-warfare-center-u_cyber_warfare_center) (`U_Cyber_Warfare_Center`)

### Heavy Bomb (`Heavy Iron Bomb`)

<!-- img:missile Units/Images/Missiles/HEAVY_IRON_BOMB.png -->

A heavy conventional bomb used by high-speed bombers, which are only capable of dropping a single large bomb.

**How to get it:** available from the start — technology `M_Heavy_Iron_Bomb`.

**Template:** `Default`.

**Used by:** [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `speed` | 100 |
| `precision` | 2 |

**Explosion:**

- `Big_Conventional`: damage 5, blast radius 1.2 km, full effect within 0.15 km

**Against targets with these traits:**

- `damage` ×2 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Jamming Equipment (`EW Jammer`)

<!-- img:missile Units/Images/Missiles/JAMMER.png -->

A suite of electronic warfare equipment used to confuse and blind enemy radar systems, rendering many weapon systems ineffective or less capable.

**How to get it:** available from the start — technology `M_EW_Ground`.

**Used by:** [Jamming Vehicle](A1-Catalog-Units.md#jamming-vehicle-ew_mobile), [EW Aircraft](A1-Catalog-Units.md#ew-aircraft-ew_aircraft).

| Stat | Base value |
|---|---|
| `range` | 400 |
| `speed` | 1 |

**Explosion:**

- `std_torpedo`: damage 3, blast radius 0.1 km, full effect within 0.025 km

**Upgrades:**

- On units with the [“EW Aircraft”](A1-Catalog-Units.md#ew-aircraft-mod_ew_aircraft) (`Mod_EW_Aircraft`) trait: `range` ×0.85
- With [SEAD/EW Aircraft](A5-Catalog-Technologies.md#seadew-aircraft-jammers_mk2) (`Jammers_Mk2`): `range` = 600
- With [DRFM Jamming Systems](A5-Catalog-Technologies.md#drfm-jamming-systems-jammers_mk3) (`Jammers_Mk3`): `range` = 900
- With [Advanced AESA Jammers](A5-Catalog-Technologies.md#advanced-aesa-jammers-jammers_mk4) (`Jammers_Mk4`): `range` = 1 200

### Kinetic Strike Rod (`Orbital Kinetic Bomb`)

<!-- img:missile Units/Images/Missiles/Kinetic_Rod.png -->

A large, narrow metal rod designed to be dropped on strategic targets from orbit at very high speeds. Deployed by kinetic attack satellites.

**How to get it:** available from the start — technology `M_Orbital_Strike`.

**Template:** `Default`.

**Used by:** [Kinetic Strike Satellite](A1-Catalog-Units.md#kinetic-strike-satellite-kinetic_strike_satellite).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 0 |
| `speed` | 5 000 |
| `precision` | 5 |

**Explosion:**

- `Kinetic_Hit`: damage 100, blast radius 10 km, full effect within 1 km

**Situational effects:**

- Inside the range of an active friendly [Satellite Relay](#satellite-relay-satellite-relay): `range` = 1 000

### Massacre Civilians (`Massacre Civilians`)

<!-- img:missile Units/Images/Missiles/MASSACRE.png -->

Allows armies to destroy cities within their occupation range by attacking infrastructure and targeting civilians.

**How to get it:** available from the start — technology `M_Massacre`.

**Template:** `Massacre`.

**Used by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division).

**Can be fired at:** cities, map points.

| Stat | Base value |
|---|---|
| `range` | 75 |
| `speed` | 2 000 |
| `precision` | 20 |

**Explosion:**

- `Gunfire_Massacre`: damage 4 000, blast radius 5 km, full effect within 5 km

**Upgrades:**

- With [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization) (`Weapon_Modernization`): `damage` ×1.15
- With [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons) (`Improved_Army_Weapons`): `damage` ×1.15
- With [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons) (`Enhanced_Army_Weapons`): `damage` ×1.15
- With [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons) (`Advanced_Army_Weapons`): `damage` ×1.15
- With [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons) (`Experimental_Army_Weapons`): `damage` ×1.15

### Naval Gun (`Ship Gun`)

<!-- img:missile Units/Images/Missiles/SHIP_GUN.png -->

A heavy gun mounted on warships. Effective at short range against surface targets like land units by the coast or other ships.

**How to get it:** available from the start — technology `M_Ship_Gun`.

**Template:** `Default`.

**Used by:** [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser).

**Can be fired at:** ground units, ships, cities, map points.

**Replaced after:** [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`) + [Railguns](A5-Catalog-Technologies.md#railguns-railguns) (`Railguns`).

| Stat | Base value |
|---|---|
| `range` | 500 |
| `speed` | 800 |
| `precision` | 0.8 |
| `canbeintercepted` | 40% |

**Explosion:**

- `big_bomb_old`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×800 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Rocket Pod (`Rocket Pod`)

<!-- img:missile Units/Images/Missiles/ROCKETPOD.png -->

A rocket launcher containing several small unguided rockets that can be fired in quick succession. They are less powerful than bombs but can attack from a greater distance.

**How to get it:** available from the start — technology `M_Rocket_Pod`.

**Template:** `Default`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Attack Helicopter](A1-Catalog-Units.md#attack-helicopter-attack_helicopter).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 185 |
| `speed` | 1 500 |
| `precision` | 4 |

**Explosion:**

- `rocket_explosion`: damage 0.8, blast radius 0.05 km, full effect within 0.05 km

**Against targets with these traits:**

- `damage` ×1 500 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Small Arms (`Small Arms`)

<!-- img:missile Units/Images/Missiles/SMALL_ARMS_DEFAULT.png -->

Small man-portable firearms. Useful for personal defence against small units. Also indicative of the combat capabilities of a larger fighting unit like an army.

**How to get it:** available from the start — technology `M_Small_Arms`.

**Template:** `Small Arms`.

**Used by:** [Intelligence Center](A1-Catalog-Units.md#intelligence-center-intelligence_center), [Spec-Ops Team](A1-Catalog-Units.md#spec-ops-team-spec_ops_team), [Spec-Ops Helicopter](A1-Catalog-Units.md#spec-ops-helicopter-spec_ops_helicopter), [Air Base](A1-Catalog-Units.md#air-base-airport), [Tactical Airbase](A1-Catalog-Units.md#tactical-airbase-tactical_airbase), [Specialized Airbase](A1-Catalog-Units.md#specialized-airbase-specialized_airport), [Security Checkpoint](A1-Catalog-Units.md#security-checkpoint-security_checkpoint), [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Forward Operating Base](A1-Catalog-Units.md#forward-operating-base-forward_operating_base), [Combat Engineers](A1-Catalog-Units.md#combat-engineers-combat_engineers), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Can be fired at:** Bomb Truck, Heavy Bomb Truck, Spec-Ops Team, Security Checkpoint, Spec-Ops Helicopter, Naval Helicopter, Cyber Warfare Center.

| Stat | Base value |
|---|---|
| `range` | 100 |
| `speed` | 3 000 |
| `precision` | 0.01 |
| `maxelevation` | 5 |

**Explosion:**

- `Gunfire_Spec_Ops`: damage 0.055, blast radius 2 km, full effect within 1 km

**Upgrades:**

- On units with the [“Static Defender Bonus”](A1-Catalog-Units.md#static-defender-bonus-static_defender_bonus) (`Static_Defender_Bonus`) trait: `range` ×1.25
- With [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization) (`Weapon_Modernization`):
    - `damage` ×1.15
    - new appearance
- With [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics) (`Portable_Electronic_Optics`):
    - `range` = 105
    - `damage` ×1.025
- With [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons) (`Improved_Army_Weapons`):
    - `damage` ×1.15
    - new appearance
- With [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics) (`Tactical_Optics`):
    - `range` = 110
    - `damage` ×1.025
- With [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons) (`Enhanced_Army_Weapons`):
    - `damage` ×1.15
    - new appearance
- With [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`):
    - `range` = 115
    - `damage` ×1.025
- With [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons) (`Advanced_Army_Weapons`):
    - `damage` ×1.15
    - new appearance
- With [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles) (`Light_Unmanned_Vehicles`):
    - `range` = 120
    - `damage` ×1.025
- With [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons) (`Experimental_Army_Weapons`):
    - `damage` ×1.15
    - new appearance
- With [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry) (`Robotic_Infantry`):
    - `range` = 125
    - `damage` ×1.025

### SRBM (`SRBM`)

<!-- img:missile Units/Images/Missiles/SRBM.png -->

A short-ranged ballistic missile armed with a conventional warhead. Used by ballistic missile sites and SRBM TEL Vehicles.

**How to get it:** available from the start — technology `M_SRBM`.

**Template:** `Default`.

**Used by:** [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site), [SRBM TEL Vehicle](A1-Catalog-Units.md#srbm-tel-vehicle-mobile_srbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `minrange` | 100 |
| `speed` | 2 000 |
| `precision` | 1.2 |
| `canbeintercepted` | 50% |

**Explosion:**

- `Big_Conventional`: damage 5, blast radius 1.2 km, full effect within 0.15 km

**Upgrades:**

- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - new appearance
    - `canbeintercepted` ×0.9
    - `precision` ×0.85

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)
- `damage` ×2 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### AGM (`AGM`)

<!-- img:missile Units/Images/Missiles/AGM_1.png -->

An air-to-ground missile, used by multirole attack aircraft and bombers to destroy targets on the ground.

**How to get it:** [Early CLOS Air-to-Ground Weapons](A5-Catalog-Technologies.md#early-clos-air-to-ground-weapons-air_to_ground_missile) (`Air_to_Ground_missile`) + [2nd Generation Aircraft](A5-Catalog-Technologies.md#2nd-generation-aircraft-generation_2_aircraft) (`Generation_2_Aircraft`) — technology `M_Air_to_Ground_missile`.

**Template:** `SemiGuided`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack).

**Can be fired at:** ground units, ships.

| Stat | Base value |
|---|---|
| `range` | 275 |
| `speed` | 650 |
| `precision` | 0.6 |
| `canbeintercepted` | 45% |

**Explosion:**

- `big_bomb_old`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Upgrades:**

- With [Basic Laser Guidance](A5-Catalog-Technologies.md#basic-laser-guidance-basic_laser_guidance) (`Basic_Laser_Guidance`):
    - `precision` ×0.9
    - `damage` ×1.1
- With [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`):
    - new appearance
    - `precision` ×0.7
    - `range` = 300
    - `speed` = 900
    - `damage` ×1.1
- With [Advanced Laser Guidance](A5-Catalog-Technologies.md#advanced-laser-guidance-advanced_laser_guidance) (`Advanced_Laser_Guidance`):
    - `precision` ×0.9
    - `damage` ×1.1
- With [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm) (`Enhanced_AGM`):
    - new appearance
    - `range` = 350
    - `precision` ×0.75
    - `damage` ×1.5
- With [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm) (`Advanced_AGM`):
    - new appearance
    - `range` = 550
    - `precision` ×0.5
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm) (`Experimental_AGM`):
    - new appearance
    - `precision` ×0.75
    - `range` = 600
    - `speed` = 1 200
    - `damage` ×1.25
    - `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `damage` ×800 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### AShM (`Anti Ship Missile`)

<!-- img:missile Units/Images/Missiles/AShM_1.png -->

A heavy guided missile designed to target and destroy surface ships. Used by surface combatant warships, submarines and coastal missile batteries.

**How to get it:** [Early Cruise Missiles](A5-Catalog-Technologies.md#early-cruise-missiles-cruise_missiles) (`Cruise_missiles`) — technology `M_Anti_Ship_Missile`.

**Used by:** [Attack Submarine (Submarine)](A1-Catalog-Units.md#attack-submarine-submarine-submarine), [SSGN (SSGN)](A1-Catalog-Units.md#ssgn-ssgn-ssgn), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Coastal Missile Battery](A1-Catalog-Units.md#coastal-missile-battery-coastal).

**Can be fired at:** ships.

| Stat | Base value |
|---|---|
| `range` | 550 |
| `speed` | 1 000 |
| `precision` | 0.7 |
| `canbeintercepted` | 35% |

**Explosion:**

- `Antiship2`: damage 3, blast radius 0.1 km, full effect within 0.02 km

**Upgrades:**

- With [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`):
    - `range` = 650
    - new appearance
- With [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles) (`Enhanced_cruise_missiles`):
    - new appearance
    - `precision` ×0.8
    - `range` = 750
    - `speed` = 1 250
    - `canbeintercepted` ×0.75
- With [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles) (`Advanced_cruise_missiles`):
    - new appearance
    - `precision` ×0.75
    - `range` = 900
    - `speed` = 1 500
    - `canbeintercepted` ×0.9
    - `damage` ×1.25
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles) (`Experimental_cruise_missiles`):
    - new appearance
    - `speed` = 5 000
    - `canbeintercepted` ×0.3
    - `damage` ×1.25

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### GBU (`GBU`)

<!-- img:missile Units/Images/Missiles/GBU_1.png -->

Air-dropped bombs that offer increased accuracy over their earlier counterparts. Costlier and available in lesser numbers than unguided bombs, but considerably more accurate and effective.

**How to get it:** [Early CLOS Air-to-Ground Weapons](A5-Catalog-Technologies.md#early-clos-air-to-ground-weapons-air_to_ground_missile) (`Air_to_Ground_missile`) + [Long-Range Bombers](A5-Catalog-Technologies.md#long-range-bombers-generation_2_bomber) (`Generation_2_Bomber`) — technology `M_Guided_Bomb`.

**Template:** `Default`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 125 |
| `speed` | 125 |
| `precision` | 1.75 |

**Explosion:**

- `big_bomb_old`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Upgrades:**

- With [Basic Laser Guidance](A5-Catalog-Technologies.md#basic-laser-guidance-basic_laser_guidance) (`Basic_Laser_Guidance`):
    - `precision` ×0.9
    - `damage` ×1.1
- With [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`):
    - new appearance
    - `precision` ×0.85
    - `damage` ×1.1
- With [Advanced Laser Guidance](A5-Catalog-Technologies.md#advanced-laser-guidance-advanced_laser_guidance) (`Advanced_Laser_Guidance`):
    - `precision` ×0.9
    - `damage` ×1.1
- With [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm) (`Enhanced_AGM`):
    - new appearance
    - `precision` ×0.65
    - `damage` ×1.25
    - `range` = 150
    - `speed` = 150
- With [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm) (`Advanced_AGM`):
    - new appearance
    - `precision` ×0.8
    - `range` = 250
    - `speed` = 250
    - `damage` ×1.2
- With [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm) (`Experimental_AGM`):
    - new appearance
    - `precision` ×0.75
    - `damage` ×1.25
    - `range` = 300
    - `speed` = 300

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `damage` ×1 500 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### SSM (`SSM`)

<!-- img:missile Units/Images/Missiles/CRUISE_MISSILE_1.png -->

A Surface-to-Surface cruise missile, used to target infrastructure on land such as airports, army bases or air defence sites. Available in large numbers.

**How to get it:** [Early Cruise Missiles](A5-Catalog-Technologies.md#early-cruise-missiles-cruise_missiles) (`Cruise_missiles`) — technology `M_Surface_to_surface_missile`.

**Template:** `LandAttack`.

**Used by:** [Attack Submarine (Submarine)](A1-Catalog-Units.md#attack-submarine-submarine-submarine), [SSGN (SSGN)](A1-Catalog-Units.md#ssgn-ssgn-ssgn), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser).

**Can be fired at:** ground units.

| Stat | Base value |
|---|---|
| `range` | 650 |
| `speed` | 800 |
| `precision` | 2 |
| `canbeintercepted` | 40% |

**Explosion:**

- `big_bomb_old`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Upgrades:**

- With [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`):
    - `precision` = 1.25
    - `range` = 700
    - new appearance
- With [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles) (`Enhanced_cruise_missiles`):
    - new appearance
    - `precision` ×0.8
    - `range` = 800
    - `speed` = 1 000
    - `canbeintercepted` ×0.75
- With [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles) (`Advanced_cruise_missiles`):
    - new appearance
    - `precision` ×0.75
    - `range` = 1 000
    - `speed` = 1 250
    - `canbeintercepted` ×0.9
    - `damage` ×1.25
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles) (`Experimental_cruise_missiles`):
    - new appearance
    - `range` = 1 200
    - `speed` ×4
    - `canbeintercepted` ×0.3
    - `damage` ×1.25

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×800 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Conventional MRBM (`Conventional MRBM`)

<!-- img:missile Units/Images/Missiles/MRBM.png -->

A medium-range ballistic missile with a conventional high-explosive warhead, fired from land-based systems. Effective against tactical and strategic targets, has no production cost and produces no fallout. Far less damaging than nuclear weapons.

**How to get it:** [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) — technology `M_MRBM`.

**Template:** `Default`.

**Used by:** [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [Ballistic Missile Site](A1-Catalog-Units.md#ballistic-missile-site-srbm_site).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `minrange` | 400 |
| `speed` | 1 500 |
| `precision` | 6 |
| `canbeintercepted` | 40% |

**Explosion:**

- `Big_Conventional`: damage 5, blast radius 1.2 km, full effect within 0.15 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 4
    - new appearance
- With [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`):
    - `canbeintercepted` ×0.9
    - `precision` ×0.85
    - new appearance
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 2
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×2 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Helicopter ATGM (`Helicopter ATGM`)

<!-- img:missile Units/Images/Missiles/ATGM_1.png -->

A short range anti-tank air-to-ground missile used by attack helicopters. Intended to destroy armored vehicles, but can easily be repurposed to attack any other nearby targets.

**How to get it:** [Early CLOS Air-to-Ground Weapons](A5-Catalog-Technologies.md#early-clos-air-to-ground-weapons-air_to_ground_missile) (`Air_to_Ground_missile`) + [Turboshaft Helicopters](A5-Catalog-Technologies.md#turboshaft-helicopters-helicopter_2) (`Helicopter_2`) — technology `M_Heli_ATGM`.

**Template:** `SemiGuided`.

**Used by:** [Attack Helicopter](A1-Catalog-Units.md#attack-helicopter-attack_helicopter).

**Can be fired at:** ground units, ships.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `speed` | 600 |
| `precision` | 0.75 |
| `canbeintercepted` | 65% |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Basic Laser Guidance](A5-Catalog-Technologies.md#basic-laser-guidance-basic_laser_guidance) (`Basic_Laser_Guidance`):
    - `precision` ×0.9
    - `damage` ×1.1
- With [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`):
    - new appearance
    - `precision` ×0.6
    - `range` = 225
    - `speed` = 900
    - `damage` ×1.1
- With [Advanced Laser Guidance](A5-Catalog-Technologies.md#advanced-laser-guidance-advanced_laser_guidance) (`Advanced_Laser_Guidance`):
    - `precision` ×0.9
    - `damage` ×1.1
- With [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm) (`Enhanced_AGM`):
    - new appearance
    - `precision` ×0.75
    - `damage` ×1.5
    - `range` = 275
- With [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm) (`Advanced_AGM`):
    - new appearance
    - `precision` ×0.5
    - `range` = 350
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm) (`Experimental_AGM`):
    - new appearance
    - `precision` ×0.75
    - `range` = 450
    - `speed` = 1 100
    - `damage` ×1.25
    - `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### Light AShM (`Light_AShM`)

<!-- img:missile Units/Images/Missiles/Air_AShM.png -->

A lightweight anti-ship missile capable of being fired from a helicopter. Also used by naval monitoring stations.

**How to get it:** [Early CLOS Air-to-Ground Weapons](A5-Catalog-Technologies.md#early-clos-air-to-ground-weapons-air_to_ground_missile) (`Air_to_Ground_missile`) + [Coastal Missile Batteries](A5-Catalog-Technologies.md#coastal-missile-batteries-coastal_defence) (`Coastal_Defence`) — technology `M_Light_AShM`.

**Used by:** [Naval Helicopter](A1-Catalog-Units.md#naval-helicopter-navy_helicopter), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station).

**Can be fired at:** ships.

| Stat | Base value |
|---|---|
| `range` | 300 |
| `speed` | 600 |
| `precision` | 0.25 |
| `canbeintercepted` | 45% |

**Explosion:**

- `big_bomb_old`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Upgrades:**

- With [Basic Laser Guidance](A5-Catalog-Technologies.md#basic-laser-guidance-basic_laser_guidance) (`Basic_Laser_Guidance`):
    - `precision` ×0.9
    - `damage` ×1.1
- With [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`):
    - `precision` ×0.6
    - `range` = 350
    - `speed` = 900
    - `damage` ×1.1
- With [Advanced Laser Guidance](A5-Catalog-Technologies.md#advanced-laser-guidance-advanced_laser_guidance) (`Advanced_Laser_Guidance`):
    - `precision` ×0.9
    - `damage` ×1.1
- With [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm) (`Enhanced_AGM`):
    - `precision` ×0.75
    - `damage` ×1.5
    - `range` = 400
- With [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm) (`Advanced_AGM`):
    - `precision` ×0.5
    - `range` = 700
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm) (`Experimental_AGM`):
    - `precision` ×0.75
    - `range` = 900
    - `speed` = 1 350
    - `damage` ×1.25
    - `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### ALBM (`ALBM`)

<!-- img:missile Units/Images/Missiles/ALBM.png -->

A medium-range air-launched ballistic missile, armed with a conventional warhead. Deployable by long-range bombers.

**How to get it:** [Air-Launched Ballistic Missiles](A5-Catalog-Technologies.md#air-launched-ballistic-missiles-aircraft-launched_mrbm) (`Aircraft-launched_MRBM`) — technology `M_ALBM`.

**Template:** `Default`.

**Used by:** [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 1 800 |
| `speed` | 2 750 |
| `precision` | 5 |
| `canbeintercepted` | 40% |

**Explosion:**

- `Big_Conventional`: damage 5, blast radius 1.2 km, full effect within 0.15 km

**Upgrades:**

- With [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`):
    - `precision` = 3
    - new appearance
- With [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`):
    - `precision` = 1
    - new appearance

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25: [“BM Accuracy Damage Penalty”](A1-Catalog-Units.md#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`)
- `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05: [“Naval Target Damage Penalty”](A1-Catalog-Units.md#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)
- `damage` ×2 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### ALCM (`ALCM`)

<!-- img:missile Units/Images/Missiles/ALCM_1.png -->

A conventional air-launched cruise missile. These have a longer range than regular ASMs, but take longer to fire and can't be carried in large numbers. This makes them ideal for cautious, long-range strikes that don't require as much target saturation.

**How to get it:** [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`) + [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`) — technology `M_ALCM`.

**Template:** `Default`.

**Used by:** [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 600 |
| `speed` | 900 |
| `precision` | 1.25 |
| `canbeintercepted` | 50% |

**Explosion:**

- `big_bomb_old`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Upgrades:**

- With [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles) (`Enhanced_cruise_missiles`):
    - new appearance
    - `range` = 900
    - `speed` = 1 200
- With [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm) (`Enhanced_AGM`): `precision` ×0.8
- With [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles) (`Advanced_cruise_missiles`):
    - new appearance
    - `range` = 1 200
    - `speed` = 1 500
    - `canbeintercepted` ×0.8
- With [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm) (`Advanced_AGM`):
    - `damage` ×1.25
    - `precision` ×0.75
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles) (`Experimental_cruise_missiles`):
    - new appearance
    - `range` ×1.25
    - `speed` = 5 000
    - `canbeintercepted` ×0.3
    - `damage` ×1.125
- With [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm) (`Experimental_AGM`):
    - `damage` ×1.25
    - `precision` ×0.8

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `damage` ×800 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

### Anti-Radar Missile (`Anti-Radiation Missile`)

<!-- img:missile Units/Images/Missiles/SEAD_1.png -->

An anti-radiation missile (ARM) used by electronic warfare aircraft to counteract enemy air defences. It has better range and performance compared to other AGMs, but can only attack targets with strong radio emissions. This includes fixed and mobile SAM and radar sites, and enemy jamming vehicles. It will not be able to attack other targets.

**How to get it:** [SEAD/EW Aircraft](A5-Catalog-Technologies.md#seadew-aircraft-jammers_mk2) (`Jammers_Mk2`) + [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm) (`Improved_AGM`) — technology `M_Anti-Radiation_Missile`.

**Template:** `AntiRadiation`.

**Used by:** [EW Aircraft](A1-Catalog-Units.md#ew-aircraft-ew_aircraft).

**Can be fired at:** Radar Site, Short-Wave Radar Vehicle, AA Gun Site, Over-The-Horizon Radar, Naval Monitoring Station, Space Radar, SAM Site, Midcourse ABM Site, Mobile SAM, Jamming Vehicle, Terminal ABM Site.

| Stat | Base value |
|---|---|
| `range` | 450 |
| `speed` | 1 000 |
| `precision` | 0.25 |
| `canbeintercepted` | 40% |

**Explosion:**

- `big_bomb_old`: damage 2, blast radius 0.1 km, full effect within 0.02 km

**Upgrades:**

- With [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm) (`Enhanced_AGM`):
    - new appearance
    - `precision` ×0.75
    - `damage` ×1.5
    - `range` = 600
    - `speed` = 1 200
- With [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm) (`Advanced_AGM`):
    - new appearance
    - `precision` ×0.5
    - `range` = 750
    - `speed` = 1 500
    - `canbeintercepted` ×0.9
- With [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons) (`Stealth_Weapons`): `canbeintercepted` ×0.8
- With [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm) (`Experimental_AGM`):
    - new appearance
    - `precision` ×0.5
    - `range` = 1 000
    - `speed` = 2 000
    - `damage` ×1.25
    - `canbeintercepted` ×0.9

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×0.9: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)
- `precision` ×1.075: [“Chaff and Flare Countermeasures”](A1-Catalog-Units.md#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`), [“Active Missile Interference”](A1-Catalog-Units.md#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`), [“Advanced Chaff and IR Decoys”](A1-Catalog-Units.md#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`), [“Seeker Blinding Lasers”](A1-Catalog-Units.md#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`)

### Decoy Warhead (`False ICBM Warhead`)

<!-- img:missile Units/Images/Missiles/warhead.png -->

A fake MIRV warhead, indistinguishable from a genuine warhead until it reenters the atmosphere and slows down. Used to draw midcourse ABM fire and help actual warheads hit their targets, but ineffective against terminal ABM systems.

**How to get it:** [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`) — technology `M_WARHEAD_FALSE`.

**Template:** `Default`.

**Warhead of:** [3x250kt Heavy MIRV ICBM](#3x250kt-heavy-mirv-icbm-3x250kt-icbm).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 0 |
| `speed` | 3 000 |
| `precision` | 0 |
| `canbeintercepted` | 45% |

**Explosion:**

- `No_Explosion`: damage 0

**Upgrades:**

- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`): `range` ×1.5
- With [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads) (`False_warheads`): `range` = 12 500

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `canbeintercepted` = 0: [“Terminal Ballistic Missile Defences”](A1-Catalog-Units.md#terminal-ballistic-missile-defences-terminal_abm_no_target_decoy_modifier) (`Terminal_ABM_No_Target_Decoy_Modifier`)
- `damage` ×0.85: [“Nuclear Survival Plan”](A1-Catalog-Units.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`), [“Emergency Broadcast System”](A1-Catalog-Units.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)
- `damage` ×0.875: [“Public Fallout Shelters”](A1-Catalog-Units.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)
- `damage` ×0.9: [“Civilian CBRN Casualty Treatment”](A1-Catalog-Units.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`), [“Web-Based Survival Tools”](A1-Catalog-Units.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`), [“Comprehensive Survival Infrastructure”](A1-Catalog-Units.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`), [“DEFCON 4”](A1-Catalog-Units.md#defcon-4-defcon_4) (`DEFCON_4`)
- `damage` ×0.75: [“DEFCON 3”](A1-Catalog-Units.md#defcon-3-defcon_3) (`DEFCON_3`)
- `damage` ×0.65: [“DEFCON 2”](A1-Catalog-Units.md#defcon-2-defcon_2) (`DEFCON_2`)
- `damage` ×0.5: [“DEFCON 1”](A1-Catalog-Units.md#defcon-1-defcon_1) (`DEFCON_1`)

### Missile Defence Laser (`Satellite Laser`)

<!-- img:missile Units/Images/Missiles/Laser.png -->

A satellite-mounted laser designed to shoot down incoming ballistic missiles in the exo-atmospheric phase of their trajectory, when they're in space and the most vulnerable to lasers.

**How to get it:** [High-Powered Lasers](A5-Catalog-Technologies.md#high-powered-lasers-high_powered_lasers) (`High_Powered_Lasers`) + [Laser Defence Satellites](A5-Catalog-Technologies.md#laser-defence-satellites-satellite_defence_lasers) (`Satellite_Defence_Lasers`) — technology `M_Laser_weapon`.

**Template:** `Laser_Weapon`.

**Used by:** [Laser Defence Satellite](A1-Catalog-Units.md#laser-defence-satellite-laser_defence_satellite), [Hunter-Killer Satellite](A1-Catalog-Units.md#hunter-killer-satellite-hunter-killer_satellite).

**Can be fired at:** ballistic missiles in flight, missiles.

| Stat | Base value |
|---|---|
| `range` | 2 500 |
| `speed` | 5 000 |
| `precision` | 0.8 |
| `maxelevation` | 4 000 |

**Explosion:**

- `std_bomb_small`: damage 1, blast radius 0.05 km, full effect within 0.01 km

### Railgun (`Railgun`)

<!-- img:missile Units/Images/Missiles/RAILGUN.png -->

A weapon that uses tremendous electromagnetic force to fire a heavy projectile at upwards of 8 times the speed of sound.

**How to get it:** [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`) + [Railguns](A5-Catalog-Technologies.md#railguns-railguns) (`Railguns`) — technology `M_Railgun`.

**Template:** `Default`.

**Used by:** [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser).

**Can be fired at:** ground units, ships, cities, map points.

| Stat | Base value |
|---|---|
| `range` | 650 |
| `speed` | 5 000 |
| `precision` | 0.7 |
| `canbeintercepted` | 5% |

**Explosion:**

- `Railgun_Hit`: damage 3, blast radius 0.3 km, full effect within 0.05 km

**Against targets with these traits:**

- `canbeintercepted` ×1.3: [“Hit-To-Kill Midcourse ABM”](A1-Catalog-Units.md#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`), [“Hit-To-Kill Terminal ABM”](A1-Catalog-Units.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`), [“Advanced Terminal ABM”](A1-Catalog-Units.md#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`)
- `canbeintercepted` ×1.25: [“Advanced Midcourse ABM”](A1-Catalog-Units.md#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`)
- `damage` ×2 000: [“Collateral Damage Modifier”](A1-Catalog-Units.md#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`)

## Anti-satellite weapons

### Air-Launched ASAT (`Aircraft ASAT`)

<!-- img:missile Units/Images/Missiles/ASAT.png -->

An ASAT missile designed to be fired from an interceptor.  
\+ Does not require a silo launch.  
\+ Interceptor allows for flexibility.  
\- Difficult to use.  
\- Limited launch window.

**How to get it:** [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft) (`Interceptor_aircraft`) + [4th Generation Aircraft](A5-Catalog-Technologies.md#4th-generation-aircraft-generation_4_aircraft) (`Generation_4_Aircraft`) + [Precision ASAT Weapons](A5-Catalog-Technologies.md#precision-asat-weapons-asat) (`ASAT`) — technology `M_ASAT_Plane`.

**Template:** `AntiSat`.

**Used by:** [Interceptor](A1-Catalog-Units.md#interceptor-interceptor).

**Can be fired at:** Spy Satellite, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 1 500 |
| `speed` | 10 000 |
| `precision` | 0.1 |
| `canbeintercepted` | 0% |
| `maxelevation` | 50 000 |
| `productioncost` | 1.5 |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat) (`Advanced_ASAT`):
    - `range` = 2 500
    - `canbeintercepted` ×0.75
    - `precision` ×0.5
    - `damage` ×1.5

**Against targets with these traits:**

- `canbeintercepted` = 1: [“Satellite Defence”](A1-Catalog-Units.md#satellite-defence-satellite_defence) (`Satellite_Defence`)

### ASAT (`ASAT`)

<!-- img:missile Units/Images/Missiles/ASAT_Missile.png -->

A direct-ascent anti-satellite missile, fired from the ground to directly hit and kill enemy satellites.  
\+ Can engage enemy satellites.  
\+ Precise, will not destroy other satellites.  
\+ No fallout or EMP effects.  
\- Can only target satellites.  
\- May miss its target.

**How to get it:** [Precision ASAT Weapons](A5-Catalog-Technologies.md#precision-asat-weapons-asat) (`ASAT`) — technology `M_ASAT`.

**Template:** `AntiSat`.

**Used by:** [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** Spy Satellite, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 3 000 |
| `speed` | 9 000 |
| `precision` | 0.4 |
| `canbeintercepted` | 0% |
| `maxelevation` | 50 000 |
| `productioncost` | 1.5 |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat) (`Advanced_ASAT`):
    - `range` = 4 500
    - `canbeintercepted` ×0.75
    - `precision` ×0.5
    - `damage` ×1.5

**Against targets with these traits:**

- `canbeintercepted` = 1: [“Satellite Defence”](A1-Catalog-Units.md#satellite-defence-satellite_defence) (`Satellite_Defence`)

### Co-Orbital ASAT (`Co-Orbital ASAT`)

<!-- img:missile Units/Images/Missiles/CO-ORBITAL_ASAT.png -->

A long-range ASAT that orbits the planet and slowly converges on an enemy satellite's path before intercepting it and exploding.  
\+ Long range.  
\+ Has a much longer launch window.  
\- Slow and easy to intercept.

**How to get it:** [Precision ASAT Weapons](A5-Catalog-Technologies.md#precision-asat-weapons-asat) (`ASAT`) — technology `M_ASAT_ICBM`.

**Template:** `AntiSat`.

**Used by:** [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo).

**Can be fired at:** Spy Satellite, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 20 000 |
| `speed` | 5 000 |
| `precision` | 0.4 |
| `canbeintercepted` | 0% |
| `maxelevation` | 50 000 |
| `productioncost` | 3 |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Upgrades:**

- With [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat) (`Advanced_ASAT`):
    - `speed` = 6 500
    - `canbeintercepted` ×0.75
    - `precision` ×0.5
    - `damage` ×1.5

**Against targets with these traits:**

- `canbeintercepted` = 1: [“Satellite Defence”](A1-Catalog-Units.md#satellite-defence-satellite_defence) (`Satellite_Defence`)

### Satellite ASAT Laser (`ASAT Laser`)

<!-- img:missile Units/Images/Missiles/LASER_HP.png -->

A satellite-mounted laser capable of targeting and destroying other satellites.

**How to get it:** [High-Powered Lasers](A5-Catalog-Technologies.md#high-powered-lasers-high_powered_lasers) (`High_Powered_Lasers`) + [Space-To-Space Weapons](A5-Catalog-Technologies.md#space-to-space-weapons-space_to_space_weapons) (`Space_to_Space_Weapons`) — technology `M_Laser_weapon_ASAT`.

**Template:** `AntiSat`.

**Used by:** [Laser Defence Satellite](A1-Catalog-Units.md#laser-defence-satellite-laser_defence_satellite), [Hunter-Killer Satellite](A1-Catalog-Units.md#hunter-killer-satellite-hunter-killer_satellite).

**Can be fired at:** Spy Satellite, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 2 500 |
| `speed` | 5 000 |
| `precision` | 0.9 |
| `maxelevation` | 10 000 |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

### Satellite Launched ASAT (`Satellite ASAT`)

<!-- img:missile Units/Images/Missiles/ASAT_Missile.png -->

An anti-satellite missile which is fired from orbit, used exclusively by hunter-killer satellites.

**How to get it:** [Space-To-Space Weapons](A5-Catalog-Technologies.md#space-to-space-weapons-space_to_space_weapons) (`Space_to_Space_Weapons`) + [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat) (`Advanced_ASAT`) — technology `M_Satellite_ASAT`.

**Template:** `AntiSat`.

**Used by:** [Hunter-Killer Satellite](A1-Catalog-Units.md#hunter-killer-satellite-hunter-killer_satellite).

**Can be fired at:** Spy Satellite, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 9 000 |
| `speed` | 9 000 |
| `precision` | 0.25 |
| `canbeintercepted` | 0% |
| `maxelevation` | 50 000 |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

**Against targets with these traits:**

- `canbeintercepted` = 1: [“Satellite Defence”](A1-Catalog-Units.md#satellite-defence-satellite_defence) (`Satellite_Defence`)

### Ground-Based ASAT Laser (`Ground ASAT Laser`)

<!-- img:missile Units/Images/Missiles/LASER_HP.png -->

A massively powerful laser, capable of targeting overhead satellites, blinding their optics and thermally damaging their electronics until they are destroyed.

**How to get it:** [Terminal Defence Lasers](A5-Catalog-Technologies.md#terminal-defence-lasers-terminal_defence_laser) (`Terminal_Defence_Laser`) + [Deadly Laser Weapons](A5-Catalog-Technologies.md#deadly-laser-weapons-offensive_laser_weapons) (`Offensive_Laser_Weapons`) — technology `M_Laser_weapon_ASAT_Ground`.

**Template:** `AntiSat`.

**Used by:** [Laser Defence Complex](A1-Catalog-Units.md#laser-defence-complex-laser_defence_complex).

**Can be fired at:** Spy Satellite, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 300 |
| `speed` | 5 000 |
| `precision` | 0.9 |
| `maxelevation` | 10 000 |

**Explosion:**

- `std_bomb`: damage 1, blast radius 0.05 km, full effect within 0.01 km

## Electronic warfare, cyber and support effects

### Body Armour (`Body Armor`)

<!-- img:missile Units/Images/Missiles/Body_Armor_0.png -->

Protective equipment used and worn by military personnel to help them survive in combat situations.

**How to get it:** available from the start — technology `M_Body_Armor`.

**Template:** `No Attack`.

**Used by:** [Spec-Ops Team](A1-Catalog-Units.md#spec-ops-team-spec_ops_team), [Security Checkpoint](A1-Catalog-Units.md#security-checkpoint-security_checkpoint), [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Forward Operating Base](A1-Catalog-Units.md#forward-operating-base-forward_operating_base), [Combat Engineers](A1-Catalog-Units.md#combat-engineers-combat_engineers), [Army Base](A1-Catalog-Units.md#army-base-army_base).


**Explosion:**

- `No_Explosion`: damage 0

**Upgrades:**

- With [Improved Personal Army Equipment](A5-Catalog-Technologies.md#improved-personal-army-equipment-improved_basic_protection) (`Improved_Basic_Protection`): new appearance
- With [Basic Woven Body Armour](A5-Catalog-Technologies.md#basic-woven-body-armour-basic_body_armor) (`Basic_Body_Armor`): new appearance
- With [Improved Ceramic Armour](A5-Catalog-Technologies.md#improved-ceramic-armour-improved_body_armor) (`Improved_Body_Armor`): new appearance
- With [Composite Liquid Armour](A5-Catalog-Technologies.md#composite-liquid-armour-advanced_body_armor) (`Advanced_Body_Armor`): new appearance
- With [Powered Nanomaterial Armour](A5-Catalog-Technologies.md#powered-nanomaterial-armour-experimental_body_armor) (`Experimental_Body_Armor`): new appearance

### Espionage Support (`Espionage_Buff`)

<!-- img:missile Units/Images/Missiles/papers.png -->

Supports the efforts of your spies all around the world.

**How to get it:** available from the start — technology `Espionage_Buff`.

**Template:** `No Attack`.

**Used by:** [Intelligence Center](A1-Catalog-Units.md#intelligence-center-intelligence_center).

*Aura / background effect — not shown in the weapon panel.*

| Stat | Base value |
|---|---|
| `range` | 20 500 |
| `speed` | 1 |

**Explosion:**

- `std_torpedo`: damage 3, blast radius 0.1 km, full effect within 0.025 km

**Situational effects:**

- While under the lasting effect of Cyber Warfare effect: `range` ×0
- While under the lasting effect of EMP Blast: `range` ×0

### Optics (`Optics`)

<!-- img:missile Units/Images/Missiles/Optics_0.png -->

Equipment used by military personnel, especially reconnaissance teams, to visually locate and identify enemy forces.

**How to get it:** available from the start — technology `M_Optics`.

**Template:** `No Attack`.

**Used by:** [Spec-Ops Team](A1-Catalog-Units.md#spec-ops-team-spec_ops_team), [Security Checkpoint](A1-Catalog-Units.md#security-checkpoint-security_checkpoint), [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Forward Operating Base](A1-Catalog-Units.md#forward-operating-base-forward_operating_base), [Combat Engineers](A1-Catalog-Units.md#combat-engineers-combat_engineers), [Army Base](A1-Catalog-Units.md#army-base-army_base).


**Explosion:**

- `No_Explosion`: damage 0

**Upgrades:**

- With [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics) (`Portable_Electronic_Optics`): new appearance
- With [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics) (`Tactical_Optics`): new appearance
- With [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`): new appearance
- With [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles) (`Light_Unmanned_Vehicles`): new appearance
- With [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry) (`Robotic_Infantry`): new appearance

### Research Support (`Research_Buff`)

<!-- img:missile Units/Images/Missiles/Clipboard.png -->

Supports the efforts of your researchers, allowing new technologies to be discovered more quickly.

**How to get it:** available from the start — technology `Research_Buff`.

**Template:** `No Attack`.

**Used by:** [Research Center](A1-Catalog-Units.md#research-center-research_center).

*Aura / background effect — not shown in the weapon panel.*

| Stat | Base value |
|---|---|
| `range` | 20 500 |
| `speed` | 1 |

**Explosion:**

- `std_torpedo`: damage 3, blast radius 0.1 km, full effect within 0.025 km

**Situational effects:**

- While under the lasting effect of Cyber Warfare effect: `range` ×0
- While under the lasting effect of EMP Blast: `range` ×0

### Satellite Relay (`Satellite Relay`)

<!-- img:missile Units/Images/Missiles/SpyGun.png -->

Sends and receives satellite communications which allows satellites to operate effectively.

**How to get it:** available from the start — technology `M_Satellite_Relay`.

**Template:** `No Attack`.

**Used by:** [Satellite Relay Center](A1-Catalog-Units.md#satellite-relay-center-satellite_relay_station).

*Aura / background effect — not shown in the weapon panel.*

| Stat | Base value |
|---|---|
| `range` | 20 500 |
| `speed` | 1 |
| `maxelevation` | 99 999 |

**Explosion:**

- `std_torpedo`: damage 3, blast radius 0.1 km, full effect within 0.025 km

### Cyber Warfare (`Cyber_Warfare_Debuff`)

<!-- img:missile Units/Images/Missiles/t3h_1337_H4xx0rz.png -->

Initiates a cyber attack against an enemy civilian target. Different targets are affected by cyber attacks in different ways:  
When used against an enemy city, it temporarily nullifies the espionage capabilites of that city and also reduces its science and espionage GDP outputs.  
When uses against an espionage or research center, it temporarily nullifies the bonuses provided by the building.  
When used against an enemy cyber warfare center, it prevents it from executing an attack of its own.

**How to get it:** [Cyber Warfare](A5-Catalog-Technologies.md#cyber-warfare-espionage_4) (`Espionage_4`) — technology `M_Cyber_Warfare_Debuff`.

**Template:** `CyberAttack`.

**Used by:** [Intelligence Center](A1-Catalog-Units.md#intelligence-center-intelligence_center), [Cyber Warfare Center](A1-Catalog-Units.md#cyber-warfare-center-cyber_warfare_center).

**Can be fired at:** cities, Intelligence Center, Research Center, Cyber Warfare Center.

| Stat | Base value |
|---|---|
| `range` | 20 500 |
| `precision` | 1 |

**Explosion:**

- `Cyber_Attack_Hit`: damage 0, blast radius 1 km, full effect within 1 km, lasting effect 60 s

**Situational effects:**

- While under the lasting effect of Cyber Warfare effect: `range` ×0
- While under the lasting effect of EMP Blast: `range` ×0
