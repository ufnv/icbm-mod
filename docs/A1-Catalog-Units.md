# Catalog A1 — Unit types

Every shipped unit type with its display name and description, the research that unlocks it, base values, weapon configurations, sensors, upgrades per technology, and the protection its traits give against enemy weapons and sensors. Values are the base values in `Units/Units.txt`; the **Upgrades** lines show how technologies change them. Operators are shown as written: `×` multiply, `=` set, `+`/`−` add/subtract. Reload times in weapon lines are converted to game seconds (`Time 30` = 1 s).
Mode variants (surfaced submarines, army modes) are listed inside their base unit.

## Buildings and installations

### Air Base (`Airport`)

<!-- img:unit Units/Images/Icons/Ground/Airbase.png -->

An air base is a military facility used to house, operate and maintain military aircraft, such as fighters, bombers and AWACS, to name a few. Air bases usually consist of an airfield and several supporting facilities like hangars, radars and control towers. Air bases are a necessity to project air power within and beyond a nation's borders.  
\+ Supports fighters and bombers.  
\+ Can support AWACS and interceptors.  
\+ Has built-in radar.  
\- Immobile, large target.  
\- Useless without aircraft.

**How to get it:** available from the start — technology `U_Airport`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 30 |
| `size` | 1.5 |
| `productioncost` | 9 |
| `selfdestructtime` | 45 s |

**Weapons**:

- *default*:
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, off by default, principal)
    - [C-RAM](A2-Catalog-Missiles.md#c-ram-c-ram) (`C-RAM`) (unlimited, reload 0.2 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km).

**Aircraft hosted:** 10 × [Fighter](#fighter-fighter), 5 × [Strategic Bomber](#strategic-bomber-bomber), 4 × [Interceptor](#interceptor-interceptor), 2 × [AWACS](#awacs-awacs).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)

**Sensor vulnerabilities:**

- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Army Base (`Army_Base`)

<!-- img:unit Units/Images/Icons/Ground/Army_Base.png -->

Army bases house aircraft and helicopters that can be used to transport army divisions and spec-ops teams long distances. Moving one of those units into an army base will make it board an aircraft, which can then fly to its destination and deploy the unit.  
\+ Hosts air transports for army divisions.  
\+ Hosts helicopters for spec-ops teams.  
\+ Defends against nearby enemy ground units.  
\+ Resistant to conventional weapons.  
\- Immobile and easy to hit.

**How to get it:** available from the start — technology `U_Army_Base`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 125 |
| `size` | 0.5 |
| `productioncost` | 10 |
| `occupationradius` | 125 |
| `resupplyrange` | 150 |
| `repairrange` | 150 |
| `selfdestructtime` | 60 s |

**Weapons**:

- *default*:
    - [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces) (`Land Forces`) (unlimited, reload 0.3 s, auto-engages, principal)
    - [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery) (`Nuclear Artillery`) (unlimited, reload 5 s, auto-engages)
    - [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery) (`Fusion Artillery`) (unlimited, reload 5 s, auto-engages)
    - [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery) (`Chemical Artillery`) (unlimited, reload 3.3 s, auto-engages)
    - [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery) (`Improved Chemical Artillery`) (unlimited, reload 3.3 s, auto-engages)
    - [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery) (`Advanced Chemical Artillery`) (unlimited, reload 3.3 s, auto-engages)
    - [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery) (`Experimental Chemical Artillery`) (unlimited, reload 3.3 s, auto-engages)
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, off by default)
    - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.4 s, auto-engages, off by default)
    - [Anti-Air Laser](A2-Catalog-Missiles.md#anti-air-laser-aa-laser) (`AA Laser`) (unlimited, reload 0.4 s, auto-engages, off by default)
    - [Light SAM](A2-Catalog-Missiles.md#light-sam-light-sam) (`Light SAM`) (unlimited, reload 4 s, auto-engages, off by default)
    - [Light Missile Defence SAM](A2-Catalog-Missiles.md#light-missile-defence-sam-light-sam-md) (`Light SAM MD`) (unlimited, reload 4 s, auto-engages, off by default)
    - [C-RAM](A2-Catalog-Missiles.md#c-ram-c-ram) (`C-RAM`) (unlimited, reload 0.2 s, auto-engages, off by default)
    - [Body Armour](A2-Catalog-Missiles.md#body-armour-body-armor) (`Body Armor`) (×1)
    - [Optics](A2-Catalog-Missiles.md#optics-optics) (`Optics`) (×1)
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (unlimited, reload 2.5 s, auto-engages, off by default)

**Sensors:** [Resupply Range (Resupply Range FOB)](A4-Catalog-Radars.md#resupply-range-resupply-range-fob-resupply-range-fob) (150 km), [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km).

**Aircraft hosted:** 3 × [Air Transport](#air-transport-air_transport), 2 × [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), 5 × [Attack Helicopter](#attack-helicopter-attack_helicopter).

**Produces:** [Army Division (Army Division)](#army-division-army-division-army_division), [Combat Engineers](#combat-engineers-combat_engineers).

**Upgrades:**

- With [Improved Personal Army Equipment](A5-Catalog-Technologies.md#improved-personal-army-equipment-improved_basic_protection) (`Improved_Basic_Protection`): `power` ×1.15
- With [Basic Woven Body Armour](A5-Catalog-Technologies.md#basic-woven-body-armour-basic_body_armor) (`Basic_Body_Armor`): `power` ×1.15
- With [Improved Ceramic Armour](A5-Catalog-Technologies.md#improved-ceramic-armour-improved_body_armor) (`Improved_Body_Armor`): `power` ×1.15
- With [Composite Liquid Armour](A5-Catalog-Technologies.md#composite-liquid-armour-advanced_body_armor) (`Advanced_Body_Armor`): `power` ×1.15
- With [Powered Nanomaterial Armour](A5-Catalog-Technologies.md#powered-nanomaterial-armour-experimental_body_armor) (`Experimental_Body_Armor`): `power` ×1.15

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces): [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2), [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3), [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4), [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5), [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery): [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes)
- [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery): [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes)
- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5), [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons)
- [Light SAM](A2-Catalog-Missiles.md#light-sam-light-sam): [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2)
- [Light Missile Defence SAM](A2-Catalog-Missiles.md#light-missile-defence-sam-light-sam-md): [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic CBRN Defence”](#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`) (always active): enemy weapons (114): `damage` ×0.5
- [“Basic CBRN Defence”](#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`) (active after researching [Basic CBRN Defence](A5-Catalog-Technologies.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`)): enemy weapons (136): `damage` ×0.8
- [“CBRN Countermeasures”](#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`) (active after researching [CBRN Countermeasures](A5-Catalog-Technologies.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)): enemy weapons (136): `damage` ×0.8
- [“Specialized CBRN Reconnaissance”](#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`) (active after researching [Specialized CBRN Reconnaissance](A5-Catalog-Technologies.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`)): enemy weapons (136): `damage` ×0.85
- [“Advanced CBRN Equipment”](#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`) (active after researching [Advanced CBRN Equipment](A5-Catalog-Technologies.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)): enemy weapons (136): `damage` ×0.85
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Unit BioChem Modifier”](#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`) (always active): enemy weapons (13): `damage` ×7.5

**Other traits:** `Static_Defender_Bonus`, `Portable_Electronic_Optics_EntMod`, `Tactical_Optics_EntMod`, `Advanced_Tactical_Optics_EntMod`, `Light_Unmanned_Vehicles_EntMod`, `Robotic_Infantry_EntMod`.

### Ballistic Missile Site (`SRBM_Site`)

<!-- img:unit Units/Images/Icons/Ground/SRBM_Site.png -->

A launch site for short and medium-range ballistic missiles. Although the range is limited, it is still longer-ranged than many options and can be equipped with nuclear weapons.  
\+ Good firing distance against conventional units.  
\+ Relatively cheap.  
\- Immobile and vulnerable to enemy attack.  
\- Limited range/firepower compared to other systems.

**How to get it:** available from the start — technology `U_SRBM_Site`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 4 |
| `size` | 0.2 |
| `productioncost` | 9 |
| `attackdelay` | 5 s |
| `selfdestructtime` | 5 s |

**Weapons** (switchable configurations):

- *Conventional SRBM*: [SRBM](A2-Catalog-Missiles.md#srbm-srbm) (`SRBM`) (unlimited, reload 12.8 s)
- *Chemical SRBM*:
    - [Mustard Gas SRBM](A2-Catalog-Missiles.md#mustard-gas-srbm-chemical_srbm) (`Chemical_SRBM`) (unlimited, reload 12.8 s)
    - [Sarin SRBM](A2-Catalog-Missiles.md#sarin-srbm-improved_chemical_srbm) (`Improved_Chemical_SRBM`) (unlimited, reload 12.8 s)
    - [VX Gas SRBM](A2-Catalog-Missiles.md#vx-gas-srbm-advanced_chemical_srbm) (`Advanced_Chemical_SRBM`) (unlimited, reload 12.8 s)
    - [Novichok-2000 SRBM](A2-Catalog-Missiles.md#novichok-2000-srbm-experimental_chemical_srbm) (`Experimental_Chemical_SRBM`) (unlimited, reload 12.8 s)
- *Nuclear SRBM*: [Nuclear SRBM](A2-Catalog-Missiles.md#nuclear-srbm-srbm-n) (`SRBM-N`) (×1, reload 12.8 s)
- *Fusion SRBM*: [Fusion SRBM](A2-Catalog-Missiles.md#fusion-srbm-fusion-srbm) (`Fusion SRBM`) (×1, reload 12.8 s)
- *Conventional MRBM (default)*: [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm) (`Conventional MRBM`) (unlimited, reload 15 s)
- *Chemical MRBM (default)*:
    - [Mustard Gas MRBM](A2-Catalog-Missiles.md#mustard-gas-mrbm-chemical_mrbm) (`Chemical_MRBM`) (unlimited, reload 15 s)
    - [Sarin MRBM](A2-Catalog-Missiles.md#sarin-mrbm-improved_chemical_mrbm) (`Improved_Chemical_MRBM`) (unlimited, reload 15 s)
    - [VX Gas MRBM](A2-Catalog-Missiles.md#vx-gas-mrbm-advanced_chemical_mrbm) (`Advanced_Chemical_MRBM`) (unlimited, reload 15 s)
    - [Novichok-2000 MRBM](A2-Catalog-Missiles.md#novichok-2000-mrbm-experimental_chemical_mrbm) (`Experimental_Chemical_MRBM`) (unlimited, reload 15 s)
- *Bioweapon MRBM (default)*: [Rabbit Fever MRBM](A2-Catalog-Missiles.md#rabbit-fever-mrbm-bioweapon_mrbm) (`Bioweapon_MRBM`) (×1, reload 15 s)
- *Improved Bioweapon MRBM (default)*: [Smallpox MRBM](A2-Catalog-Missiles.md#smallpox-mrbm-improved_bioweapon_mrbm) (`Improved_Bioweapon_MRBM`) (×1, reload 15 s)
- *Advanced Bioweapon MRBM (default)*: [Ebola MRBM](A2-Catalog-Missiles.md#ebola-mrbm-advanced_bioweapon_mrbm) (`Advanced_Bioweapon_MRBM`) (×1, reload 15 s)
- *Experimental Bioweapon MRBM (default)*: [EMeVHF-24 MRBM](A2-Catalog-Missiles.md#emevhf-24-mrbm-engineered_bioweapon_mrbm) (`Engineered_Bioweapon_MRBM`) (×1, reload 15 s)
- *100kt MRBM (default)*: [100 Kiloton MRBM](A2-Catalog-Missiles.md#100-kiloton-mrbm-100kt_mrbm) (`100kt_MRBM`) (×1, reload 15 s)
- *250kt MRBM (default)*: [250 Kiloton MRBM](A2-Catalog-Missiles.md#250-kiloton-mrbm-250kt_mrbm) (`250kt_MRBM`) (×1, reload 15 s)
- *500kt MRBM (default)*: [500 Kiloton MRBM](A2-Catalog-Missiles.md#500-kiloton-mrbm-500kt_mrbm) (`500kt_MRBM`) (×1, reload 15 s)
- *Megaton MRBM (default)*: [Megaton MRBM](A2-Catalog-Missiles.md#megaton-mrbm-1m_mrbm) (`1M_MRBM`) (×1, reload 15 s)
- *5M MRBM (default)*: [5 Megaton MRBM](A2-Catalog-Missiles.md#5-megaton-mrbm-5m_mrbm) (`5M_MRBM`) (×1, reload 15 s)
- *500kt Cobalt MRBM (default)*: [500kt Cobalt MRBM](A2-Catalog-Missiles.md#500kt-cobalt-mrbm-500kt_cobalt_mrbm) (`500kt_Cobalt_MRBM`) (×1, reload 15 s)
- *500kt Enhanced Salted MRBM (default)*: [500kt Salted MRBM](A2-Catalog-Missiles.md#500kt-salted-mrbm-500kt_salt_mrbm) (`500kt_Salt_MRBM`) (×1, reload 15 s)
- *500kt EMP MRBM*: [500kt EMP MRBM](A2-Catalog-Missiles.md#500kt-emp-mrbm-500kt_mrbm_emp) (`500kt_MRBM_EMP`) (×1, reload 15 s)
- *500kt Super EMP MRBM*: [500kt Super EMP MRBM](A2-Catalog-Missiles.md#500kt-super-emp-mrbm-500kt_mrbm_emp_super) (`500kt_MRBM_EMP_Super`) (×1, reload 15 s)
- *3x100kt MIRV MRBM (default)*: [3x100kt MIRV MRBM](A2-Catalog-Missiles.md#3x100kt-mirv-mrbm-3x100kt_mrbm) (`3x100kt_MRBM`) (×1, reload 15 s)
- *3x250kt MIRV MRBM (default)*: [3x250kt MIRV MRBM](A2-Catalog-Missiles.md#3x250kt-mirv-mrbm-3x250kt_mrbm) (`3x250kt_MRBM`) (×1, reload 15 s)
- *6x250kt MIRV MRBM (default)*: [6x250kt MIRV MRBM](A2-Catalog-Missiles.md#6x250kt-mirv-mrbm-6x250kt_mrbm) (`6x250kt_MRBM`) (×1, reload 15 s)
- *6x500kt MIRV MRBM (default)*: [6x500kt MIRV MRBM](A2-Catalog-Missiles.md#6x500kt-mirv-mrbm-6x500kt_mrbm) (`6x500kt_MRBM`) (×1, reload 15 s)
- *8x500 MIRV MRBM (default)*: [8x500kt MIRV MRBM](A2-Catalog-Missiles.md#8x500kt-mirv-mrbm-8x500kt_mrbm) (`8x500kt_MRBM`) (×1, reload 15 s)
- *8x1MT MRBM (default)*: [8x1MT Pure Fusion MIRV MRBM](A2-Catalog-Missiles.md#8x1mt-pure-fusion-mirv-mrbm-8x1mt_mrbm) (`8x1MT_MRBM`) (×1, reload 15 s)

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `attackdelay` ×0.35

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [SRBM](A2-Catalog-Missiles.md#srbm-srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Mustard Gas SRBM](A2-Catalog-Missiles.md#mustard-gas-srbm-chemical_srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Sarin SRBM](A2-Catalog-Missiles.md#sarin-srbm-improved_chemical_srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [VX Gas SRBM](A2-Catalog-Missiles.md#vx-gas-srbm-advanced_chemical_srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Novichok-2000 SRBM](A2-Catalog-Missiles.md#novichok-2000-srbm-experimental_chemical_srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Nuclear SRBM](A2-Catalog-Missiles.md#nuclear-srbm-srbm-n): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [MARV](A5-Catalog-Technologies.md#marv-marv), [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [Fusion SRBM](A2-Catalog-Missiles.md#fusion-srbm-fusion-srbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm): [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Mustard Gas MRBM](A2-Catalog-Missiles.md#mustard-gas-mrbm-chemical_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Sarin MRBM](A2-Catalog-Missiles.md#sarin-mrbm-improved_chemical_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [VX Gas MRBM](A2-Catalog-Missiles.md#vx-gas-mrbm-advanced_chemical_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Novichok-2000 MRBM](A2-Catalog-Missiles.md#novichok-2000-mrbm-experimental_chemical_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Rabbit Fever MRBM](A2-Catalog-Missiles.md#rabbit-fever-mrbm-bioweapon_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Smallpox MRBM](A2-Catalog-Missiles.md#smallpox-mrbm-improved_bioweapon_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Ebola MRBM](A2-Catalog-Missiles.md#ebola-mrbm-advanced_bioweapon_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [EMeVHF-24 MRBM](A2-Catalog-Missiles.md#emevhf-24-mrbm-engineered_bioweapon_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [100 Kiloton MRBM](A2-Catalog-Missiles.md#100-kiloton-mrbm-100kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [250 Kiloton MRBM](A2-Catalog-Missiles.md#250-kiloton-mrbm-250kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads)
- [500 Kiloton MRBM](A2-Catalog-Missiles.md#500-kiloton-mrbm-500kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Megaton MRBM](A2-Catalog-Missiles.md#megaton-mrbm-1m_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [5 Megaton MRBM](A2-Catalog-Missiles.md#5-megaton-mrbm-5m_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt Cobalt MRBM](A2-Catalog-Missiles.md#500kt-cobalt-mrbm-500kt_cobalt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [500kt Salted MRBM](A2-Catalog-Missiles.md#500kt-salted-mrbm-500kt_salt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt EMP MRBM](A2-Catalog-Missiles.md#500kt-emp-mrbm-500kt_mrbm_emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt Super EMP MRBM](A2-Catalog-Missiles.md#500kt-super-emp-mrbm-500kt_mrbm_emp_super): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [3x100kt MIRV MRBM](A2-Catalog-Missiles.md#3x100kt-mirv-mrbm-3x100kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [MIRV](A5-Catalog-Technologies.md#mirv-mirv), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3x250kt MIRV MRBM](A2-Catalog-Missiles.md#3x250kt-mirv-mrbm-3x250kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [6x250kt MIRV MRBM](A2-Catalog-Missiles.md#6x250kt-mirv-mrbm-6x250kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [6x500kt MIRV MRBM](A2-Catalog-Missiles.md#6x500kt-mirv-mrbm-6x500kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light)
- [8x500kt MIRV MRBM](A2-Catalog-Missiles.md#8x500kt-mirv-mrbm-8x500kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [8x1MT Pure Fusion MIRV MRBM](A2-Catalog-Missiles.md#8x1mt-pure-fusion-mirv-mrbm-8x1mt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Fixed Coastal Gun (`Fixed_Coastal_Gun`)

<!-- img:unit Units/Images/Icons/Ground/Coastal_Gun.png -->

A heavy fixed gun emplacement designed for anti-shipping purposes. They are large, slow, immobile and vulnerable, but will provide a limited degree of protection against enemy units until more effective defences such as cruise missiles can be procured.  
\+ Can fire at enemy units.  
\- Easy to destroy and immobile.  
\- Relatively ineffective firepower.

**How to get it:** available from the start — technology `U_Coastal_Gun_Old`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 3 |
| `size` | 0.1 |
| `productioncost` | 4.5 |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*: [Anti-Ship Gun](A2-Catalog-Missiles.md#anti-ship-gun-coastal-gun-old) (`Coastal Gun Old`) (unlimited, reload 10 s, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km).

**Upgrades:**

- With [Coastal Missile Batteries](A5-Catalog-Technologies.md#coastal-missile-batteries-coastal_defence) (`Coastal_Defence`): can no longer be built

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)

**Sensor vulnerabilities:**

- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Forward Operating Base (`Forward_Operating_Base`)

<!-- img:unit Units/Images/Icons/Ground/FOB.png -->

A forward operating base, or FOB, is a small military facility used to support and resupply friendly troops close to the frontlines. FOBs can be deployed by combat engineers, by producing a FOB and then dropping it on a combat engineer unit, which can then move into enemy territory and build it.  
\+ Repairs nearby friendly units  
\+ Can be deployed by engineers  
\+ Hosts Spec-Ops helicopters  
\- Immobile once deployed  
\- Limited self-defence measures  
\- Limited use without other units

**How to get it:** available from the start — technology `U_FOB`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 30 |
| `size` | 0.5 |
| `productioncost` | 6 |
| `resupplyrange` | 150 |
| `repairrange` | 150 |
| `selfdestructtime` | 15 s |

**Weapons**:

- *default*:
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, off by default)
    - [Body Armour](A2-Catalog-Missiles.md#body-armour-body-armor) (`Body Armor`) (×1)
    - [Optics](A2-Catalog-Missiles.md#optics-optics) (`Optics`) (×1)
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (unlimited, reload 2.5 s, auto-engages, off by default)
    - [C-RAM](A2-Catalog-Missiles.md#c-ram-c-ram) (`C-RAM`) (unlimited, reload 0.2 s, auto-engages, off by default)

**Sensors:** [Resupply Range (Resupply Range FOB)](A4-Catalog-Radars.md#resupply-range-resupply-range-fob-resupply-range-fob) (150 km), [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance) (125 km).

**Aircraft hosted:** 1 × [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), 2 × [Attack Helicopter](#attack-helicopter-attack_helicopter).

**Upgrades:**

- With [Improved Personal Army Equipment](A5-Catalog-Technologies.md#improved-personal-army-equipment-improved_basic_protection) (`Improved_Basic_Protection`): `power` ×1.15
- With [Basic Woven Body Armour](A5-Catalog-Technologies.md#basic-woven-body-armour-basic_body_armor) (`Basic_Body_Armor`): `power` ×1.15
- With [Improved Ceramic Armour](A5-Catalog-Technologies.md#improved-ceramic-armour-improved_body_armor) (`Improved_Body_Armor`): `power` ×1.15
- With [Composite Liquid Armour](A5-Catalog-Technologies.md#composite-liquid-armour-advanced_body_armor) (`Advanced_Body_Armor`): `power` ×1.15
- With [Powered Nanomaterial Armour](A5-Catalog-Technologies.md#powered-nanomaterial-armour-experimental_body_armor) (`Experimental_Body_Armor`): `power` ×1.15

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance): [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic CBRN Defence”](#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`) (always active): enemy weapons (114): `damage` ×0.5
- [“Basic CBRN Defence”](#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`) (active after researching [Basic CBRN Defence](A5-Catalog-Technologies.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`)): enemy weapons (136): `damage` ×0.8
- [“CBRN Countermeasures”](#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`) (active after researching [CBRN Countermeasures](A5-Catalog-Technologies.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)): enemy weapons (136): `damage` ×0.8
- [“Specialized CBRN Reconnaissance”](#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`) (active after researching [Specialized CBRN Reconnaissance](A5-Catalog-Technologies.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`)): enemy weapons (136): `damage` ×0.85
- [“Advanced CBRN Equipment”](#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`) (active after researching [Advanced CBRN Equipment](A5-Catalog-Technologies.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)): enemy weapons (136): `damage` ×0.85

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Unit BioChem Modifier”](#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`) (always active): enemy weapons (13): `damage` ×7.5

**Other traits:** `Static_Defender_Bonus`, `Portable_Electronic_Optics_EntMod`, `Tactical_Optics_EntMod`, `Advanced_Tactical_Optics_EntMod`, `Light_Unmanned_Vehicles_EntMod`, `Robotic_Infantry_EntMod`.

### Radar Site (`Fixed_LW_radar`)

<!-- img:upgrades Units/Images/Icons/Ground/Radar_Site_1.png=Base|Units/Images/Icons/Ground/Radar_Site_2.png=Pulse Doppler Radar|Units/Images/Icons/Ground/Radar_Site_3.png=AESA Radar -->

Radar sites use radio waves to detect enemy activity over long distances. Radar was originally developed to detect aircraft during WWII, but sufficiently advanced radars can detect objects at sea, on the ground and even in space. Good radar coverage is crucial to be able to detect enemy units, especially incoming aircraft and other threats. However, radar sites themselves are quite vulnerable to enemy strikes or sabotage, and should be defended accordingly.  
\+ Can detect enemy units from long range.  
\- Vulnerable and defenceless.

**How to get it:** available from the start — technology `U_Long_wave_radar`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 3 |
| `size` | 0.6 |
| `productioncost` | 3.5 |
| `selfdestructtime` | 5 s |

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave) (550 km), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) (300 km), [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong) (950 km).

**Upgrades:**

- With [Pulse Doppler Radar](A5-Catalog-Technologies.md#pulse-doppler-radar-radar_mk2) (`Radar_Mk2`): new appearance
- With [AESA Radar](A5-Catalog-Technologies.md#aesa-radar-radar_mk4) (`Radar_Mk4`): new appearance

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong): [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6)

**Sensor vulnerabilities:**

- [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Specialized Airbase (`Specialized_Airport`)

<!-- img:unit Units/Images/Icons/Ground/Airbase_Special.png -->

A large airport with especially long runways capable of facilitating the takeoff, landing and maintenance of specialized aircraft like high-speed supersonic bombers and spy planes.  
\+ Can host specialized transports for spec-ops  
\+ Can host spy planes  
\+ Can host high-speed bombers  
\- Limited uses for tactical warfare  
\- Expensive to build  
\- Few personal defences

**How to get it:** available from the start — technology `U_Specialized_Airport`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 40 |
| `size` | 2.5 |
| `productioncost` | 10 |
| `selfdestructtime` | 60 s |

**Weapons**:

- *default*:
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, off by default, principal)
    - [C-RAM](A2-Catalog-Missiles.md#c-ram-c-ram) (`C-RAM`) (unlimited, reload 0.2 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km).

**Aircraft hosted:** 5 × [Fighter](#fighter-fighter), 2 × [Special Mission Aircraft](#special-mission-aircraft-sof_aircraft), 5 × [Interceptor](#interceptor-interceptor), 5 × [High-Speed Bomber](#high-speed-bomber-high_speed_bomber), 2 × [Spy Plane](#spy-plane-spy_plane).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)

**Sensor vulnerabilities:**

- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Tactical Airbase (`Tactical_Airbase`)

<!-- img:unit Units/Images/Icons/Ground/Airbase_Tac.png -->

An airbase hosting tactical fighter wings, which can efficiently defend against enemy aircraft and strike targets relatively close to the base. They are very effective in a short-range defence role, but have a limited capacity to attack targets at a distance.  
\+ Supports multirole and air superiority fighters.  
\+ Carries electronic warfare aircraft.  
\+ Very effective at short-range air defence.  
\+ Effective against nearby enemy assets.  
\+ Has built-in radar.  
\- Immobile and easy to hit.  
\- Limited effective range.

**How to get it:** available from the start — technology `U_Tactical_Airbase`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 25 |
| `size` | 1.25 |
| `productioncost` | 7 |
| `selfdestructtime` | 30 s |

**Weapons**:

- *default*:
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, off by default, principal)
    - [C-RAM](A2-Catalog-Missiles.md#c-ram-c-ram) (`C-RAM`) (unlimited, reload 0.2 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km).

**Aircraft hosted:** 10 × [Fighter](#fighter-fighter), 10 × [Multirole Attacker](#multirole-attacker-attack), 4 × [EW Aircraft](#ew-aircraft-ew_aircraft), 1 × [AWACS](#awacs-awacs).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)

**Sensor vulnerabilities:**

- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Central Command Bunker (`Central_Command_Bunker`)

<!-- img:unit Units/Images/Icons/Ground/Command_Bunker.png -->

A highly reinforced underground structure used to house the top-ranking military and government officials during a nuclear war. It is extremely difficult to destroy, and can be used to set the current DEFCON level.  
Different DEFCON levels trade GDP for defensive bonuses that increase your ability to mobilize army divisions and minimize casualties when cities are attacked.  
Limit one per faction.  
\+ Allows you to set a DEFCON level.  
\+ Extremely resistant to damage.  
\- Set DEFCON level is reset when destroyed.

**How to get it:** [Nuclear Survival Plan](A5-Catalog-Technologies.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`) + [Centralized Defence Planning](A5-Catalog-Technologies.md#centralized-defence-planning-defence_planning) (`Defence_Planning`) — technology `U_DEFCON_Bunker`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 5 000 |
| `size` | 0.25 |
| `productioncost` | 36 |
| `maxnumberonmap` | 1 |
| `selfdestructtime` | 90 s |

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Intelligence Center (`Intelligence_Center`)

This building will serve as the center of your intelligence and counter-intelligence operations. It increases the effectiveness of your intelligence operations worldwide.  
Limit one per faction.

**How to get it:** [Intelligence Organization](A5-Catalog-Technologies.md#intelligence-organization-espionage_1) (`Espionage_1`) — technology `U_Intel_Center`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `size` | 0.1 |
| `productioncost` | 24 |
| `maxnumberonmap` | 1 |
| `attackdelay` | 60 s |
| `selfdestructtime` | 30 s |

**Weapons**:

- *Intel Center*:
    - [Espionage Support](A2-Catalog-Missiles.md#espionage-support-espionage_buff) (`Espionage_Buff`) (unlimited, off by default)
    - [Cyber Warfare](A2-Catalog-Missiles.md#cyber-warfare-cyber_warfare_debuff) (`Cyber_Warfare_Debuff`) (unlimited, reload 60 s)
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 1 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy) (200 km).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Over-The-Horizon Radar (`Over_Horizon_radar`)

<!-- img:unit Units/Images/Icons/Ground/Over_Horizon_Radar.png -->

Over-the-horizon radar, or OTH is a type of radar system with the ability to detect targets at very long ranges, beyond the radar horizon, which is the distance limit for ordinary radar systems. Their primary role is to detect incoming enemy missiles long before they reach your territory, so your missile defence systems have time to intercept them and your own nuclear forces have time to respond.  
\+ Extremely long missile detection range.  
\+ Precisely determines the launch source.  
\- Only detects ballistic missiles.

**How to get it:** [Over-The-Horizon Warning Radar](A5-Catalog-Technologies.md#over-the-horizon-warning-radar-over_horizon_radar) (`Over_horizon_radar`) — technology `U_Over_horizon_radar`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 7.5 |
| `size` | 0.8 |
| `productioncost` | 30 |
| `selfdestructtime` | 10 s |

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Overhorizon Radar (Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-over-horizon-over_horizon) (4 000 km).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Overhorizon Radar (Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-over-horizon-over_horizon): [Advanced Early Warning Radar](A5-Catalog-Technologies.md#advanced-early-warning-radar-over_horizon_radar_mk2)

**Sensor vulnerabilities:**

- [Overhorizon Radar (Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-over-horizon-over_horizon) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Overhorizon Radar (Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-over-horizon-over_horizon) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_invulnerable) (`EMP_Defence_Invulnerable`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0

### Research Center (`Research_Center`)

This building will serve as the primary headquarters for your research and development efforts. Having one will make it easier to discover new technologies, regardless of where it's built.  
Limit one per faction.

**How to get it:** [Defence Research Agency](A5-Catalog-Technologies.md#defence-research-agency-science_booster_1) (`Science_Booster_1`) — technology `U_Research_Center`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `size` | 0.1 |
| `productioncost` | 24 |
| `maxnumberonmap` | 1 |
| `selfdestructtime` | 30 s |

**Weapons**:

- *default*: [Research Support](A2-Catalog-Missiles.md#research-support-research_buff) (`Research_Buff`) (unlimited, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### SAM Site (`SAM_site`)

<!-- img:upgrades Units/Images/Icons/Ground/Fixed_SAM_Site.png=Base|Units/Images/Icons/Ground/Fixed_SAM_Site_2.png=Improved SAMs -->

A series of static surface-to-air missile installations as well as the support and command elements needed for them to operate. SAM sites are very effective at destroying nearby enemy aircraft and can destroy low-altitude missiles with the appropriate upgrades.  
\+ Effective against enemy aircraft.  
\+ Can shoot down missiles with upgrades.  
\- Immobile, somewhat limited coverage.  
\- Vulnerable to non-airborne threats.

**How to get it:** [Surface-To-Air Missiles](A5-Catalog-Technologies.md#surface-to-air-missiles-surface_to_air_missile) (`Surface_to_air_missile`) — technology `U_SAM_site`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 3 |
| `size` | 0.1 |
| `productioncost` | 5 |
| `attackdelay` | 0.5 s |
| `selfdestructtime` | 5 s |

**Weapons** (switchable configurations):

- *Default (default)*:
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, reload 2.3 s, auto-engages)
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, reload 2.3 s, auto-engages)
- *Nuclear SAM*: [Nuclear SAM](A2-Catalog-Missiles.md#nuclear-sam-nuclear-sam) (`Nuclear SAM`) (×1, reload 3.3 s, auto-engages)
- *Pure Fusion SAM*: [Pure Fusion SAM](A2-Catalog-Missiles.md#pure-fusion-sam-fusion-sam) (`Fusion SAM`) (×1, reload 3.3 s, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km).

**Upgrades:**

- With [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2) (`SAM_Mk2`):
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): `launch` = 2
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): `launch` = 2
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): `time` = 35
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): `time` = 35
    - new appearance
- With [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3) (`SAM_Mk3`):
    - `size` = 0.05
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): `launch` = 3
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): `launch` = 3
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): `time` = 22
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): `time` = 20

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2)
- [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Nuclear SAM](A2-Catalog-Missiles.md#nuclear-sam-nuclear-sam): [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons), [Surface-To-Air Missiles](A5-Catalog-Technologies.md#surface-to-air-missiles-surface_to_air_missile), [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [Pure Fusion SAM](A2-Catalog-Missiles.md#pure-fusion-sam-fusion-sam): [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### ICBM Launchpad (`ICBM_Launchpad`)

<!-- img:unit Units/Images/Icons/Ground/ICBM_Pad.png -->

A large complex built to launch heavy ICBMs. Early ICBMs were especially large and inefficient, and required large, above-ground structures to facilitate their launch. ICBM launchpads are big, easily identified and vulnerable, but offer the earliest means to fire ICBMs, and can launch heavy ICBMs without advanced rocket technology.  
\+ First ICBM-capable unit  
\+ Fires heavy ICBMs without upgrades  
\- Large, easy to hit  
\- No built-in defenses  
\- Expensive

**How to get it:** [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm) (`Launchpad_ICBM`) — technology `U_Launchpad_ICBM`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 10 |
| `size` | 0.3 |
| `productioncost` | 27.5 |
| `attackdelay` | 14 s |
| `selfdestructtime` | 30 s |

**Weapons** (switchable configurations):

- *Unarmed*: no weapons (a technology adds them)
- *Bioweapon ICBM (default)*: [Rabbit Fever ICBM](A2-Catalog-Missiles.md#rabbit-fever-icbm-bioweapon_icbm) (`Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Improved Bioweapon ICBM (default)*: [Smallpox ICBM](A2-Catalog-Missiles.md#smallpox-icbm-improved_bioweapon_icbm) (`Improved_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Advanced Bioweapon ICBM (default)*: [Ebola ICBM](A2-Catalog-Missiles.md#ebola-icbm-advanced_bioweapon_icbm) (`Advanced_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Engineered Bioweapon ICBM (default)*: [EMeVHF-24 ICBM](A2-Catalog-Missiles.md#emevhf-24-icbm-engineered_bioweapon_icbm) (`Engineered_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *3x Biological MIRV (default)*: [3xBW Bioweapon MIRV](A2-Catalog-Missiles.md#3xbw-bioweapon-mirv-bioweapon_mirv) (`Bioweapon_MIRV`) (×1, reload 49.3 s)
- *8x Biological MIRV (default)*: [8xBW Bioweapon MIRV](A2-Catalog-Missiles.md#8xbw-bioweapon-mirv-8x-bioweapon_mirv) (`8x Bioweapon_MIRV`) (×1, reload 49.3 s)
- *Lightweight 250kt (default)*: [250 Kiloton Light ICBM](A2-Catalog-Missiles.md#250-kiloton-light-icbm-icbm-250kt-light) (`ICBM (250kt Light)`) (×1, reload 49.3 s)
- *Lightweight 500kt (default)*: [500 Kiloton Light ICBM](A2-Catalog-Missiles.md#500-kiloton-light-icbm-icbm-500kt-light) (`ICBM (500kt Light)`) (×1, reload 49.3 s)
- *Lightweight Megaton (default)*: [Megaton Light ICBM](A2-Catalog-Missiles.md#megaton-light-icbm-icbm-1m-light) (`ICBM (1M Light)`) (×1, reload 49.3 s)
- *Lightweight 5Mt (default)*: [5 Megaton Light ICBM](A2-Catalog-Missiles.md#5-megaton-light-icbm-icbm-5m-light) (`ICBM (5M Light)`) (×1, reload 49.3 s)
- *Lightweight 10Mt Fusion (default)*: [10M Pure Fusion ICBM](A2-Catalog-Missiles.md#10m-pure-fusion-icbm-icbm-10m-fusion-light) (`ICBM (10M Fusion Light)`) (×1, reload 49.3 s)
- *Heavy 500kt (default)*: [500 Kiloton Heavy ICBM](A2-Catalog-Missiles.md#500-kiloton-heavy-icbm-icbm-500kt-heavy) (`ICBM (500kt Heavy)`) (×1, reload 60 s)
- *Heavy 5 Megaton (default)*: [5 Megaton ICBM](A2-Catalog-Missiles.md#5-megaton-icbm-icbm-5m-heavy) (`ICBM (5M Heavy)`) (×1, reload 60 s)
- *Heavy 10 Megaton (default)*: [10 Megaton ICBM](A2-Catalog-Missiles.md#10-megaton-icbm-icbm-10m) (`ICBM (10M)`) (×1, reload 60 s)
- *Heavy 25 Megaton (default)*: [25 Megaton ICBM](A2-Catalog-Missiles.md#25-megaton-icbm-icbm-25m) (`ICBM (25M)`) (×1, reload 60 s)
- *Heavy 50 Megaton Fusion (default)*: [50 Megaton Pure Fusion ICBM](A2-Catalog-Missiles.md#50-megaton-pure-fusion-icbm-icbm-50m-fusion) (`ICBM (50M Fusion)`) (×1, reload 60 s)
- *3x250kt Light MIRV*: [3x250kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-light-mirv-icbm-3x250kt-light-icbm) (`3x250kt Light ICBM`) (×1, reload 49.3 s)
- *3x500kt Light MIRV*: [3x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-light-mirv-icbm-3x500kt-light-icbm) (`3x500kt Light ICBM`) (×1, reload 49.3 s)
- *8x500kt Light MIRV*: [8x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#8x500kt-light-mirv-icbm-8x500kt-light-icbm) (`8x500kt Light ICBM`) (×1, reload 49.3 s)
- *8x1M Light MIRV*: [8x1M Light Fusion MIRV](A2-Catalog-Missiles.md#8x1m-light-fusion-mirv-8x1m-light-icbm) (`8x1M Light ICBM`) (×1, reload 49.3 s)
- *3x250kt MIRV (default)*: [3x250kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-heavy-mirv-icbm-3x250kt-icbm) (`3x250kt ICBM`) (×1, reload 60 s)
- *3x500kt MIRV (default)*: [3x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-heavy-mirv-icbm-3x500kt-icbm) (`3x500kt ICBM`) (×1, reload 60 s)
- *6x500kt MIRV (default)*: [6x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#6x500kt-heavy-mirv-icbm-6x500kt-icbm) (`6x500kt ICBM`) (×1, reload 60 s)
- *6x1Mt MIRV (default)*: [6x1M Heavy MIRV ICBM](A2-Catalog-Missiles.md#6x1m-heavy-mirv-icbm-6x1m-icbm) (`6x1M ICBM`) (×1, reload 60 s)
- *12x500kt MIRV (default)*: [12x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#12x500kt-heavy-mirv-icbm-12x500kt-icbm) (`12x500kt ICBM`) (×1, reload 60 s)
- *12x1Mt Fusion MIRV (default)*: [12x1M Pure Fusion MIRV](A2-Catalog-Missiles.md#12x1m-pure-fusion-mirv-12x1m-icbm) (`12x1M ICBM`) (×1, reload 60 s)
- *1MT Cobalt (default)*: [1M Light Cobalt ICBM](A2-Catalog-Missiles.md#1m-light-cobalt-icbm-icbm-1m-cobalt) (`ICBM (1M Cobalt)`) (×1, reload 49.3 s)
- *10MT Cobalt (default)*: [10M Heavy Cobalt ICBM](A2-Catalog-Missiles.md#10m-heavy-cobalt-icbm-icbm-10m-cobalt) (`ICBM (10M Cobalt)`) (×1, reload 60 s)
- *1MT Salted (default)*: [1M Light Salted ICBM](A2-Catalog-Missiles.md#1m-light-salted-icbm-icbm-1m-salt) (`ICBM (1M Salt)`) (×1, reload 49.3 s)
- *10MT Enhanced Salted (default)*: [10M Heavy Salted ICBM](A2-Catalog-Missiles.md#10m-heavy-salted-icbm-icbm-10m-salt) (`ICBM (10M Salt)`) (×1, reload 60 s)
- *1M EMP ICBM*: [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp) (`ICBM (1M EMP)`) (×1, reload 49.3 s)
- *1M Super EMP ICBM*: [1M Super EMP ICBM](A2-Catalog-Missiles.md#1m-super-emp-icbm-icbm-1m-super-emp) (`ICBM (1M Super EMP)`) (×1, reload 49.3 s)
- *10M Super EMP ICBM*: [10M Super EMP ICBM](A2-Catalog-Missiles.md#10m-super-emp-icbm-icbm-10m-super-emp) (`ICBM (10M Super EMP)`) (×1, reload 60 s)
- *Nuclear ASAT*: [Nuclear ASAT](A2-Catalog-Missiles.md#nuclear-asat-nuclear-asat) (`Nuclear ASAT`) (×1)
- *ASAT*: [ASAT](A2-Catalog-Missiles.md#asat-asat) (`ASAT`) (×1)
- *Co-Orbital ASAT*: [Co-Orbital ASAT](A2-Catalog-Missiles.md#co-orbital-asat-co-orbital-asat) (`Co-Orbital ASAT`) (×1, reload 49.3 s)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `attackdelay` ×0.35

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Rabbit Fever ICBM](A2-Catalog-Missiles.md#rabbit-fever-icbm-bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Smallpox ICBM](A2-Catalog-Missiles.md#smallpox-icbm-improved_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Ebola ICBM](A2-Catalog-Missiles.md#ebola-icbm-advanced_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [EMeVHF-24 ICBM](A2-Catalog-Missiles.md#emevhf-24-icbm-engineered_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3xBW Bioweapon MIRV](A2-Catalog-Missiles.md#3xbw-bioweapon-mirv-bioweapon_mirv): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy)
- [8xBW Bioweapon MIRV](A2-Catalog-Missiles.md#8xbw-bioweapon-mirv-8x-bioweapon_mirv): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)
- [250 Kiloton Light ICBM](A2-Catalog-Missiles.md#250-kiloton-light-icbm-icbm-250kt-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [500 Kiloton Light ICBM](A2-Catalog-Missiles.md#500-kiloton-light-icbm-icbm-500kt-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Megaton Light ICBM](A2-Catalog-Missiles.md#megaton-light-icbm-icbm-1m-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [5 Megaton Light ICBM](A2-Catalog-Missiles.md#5-megaton-light-icbm-icbm-5m-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [10M Pure Fusion ICBM](A2-Catalog-Missiles.md#10m-pure-fusion-icbm-icbm-10m-fusion-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [500 Kiloton Heavy ICBM](A2-Catalog-Missiles.md#500-kiloton-heavy-icbm-icbm-500kt-heavy): [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [5 Megaton ICBM](A2-Catalog-Missiles.md#5-megaton-icbm-icbm-5m-heavy): [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [10 Megaton ICBM](A2-Catalog-Missiles.md#10-megaton-icbm-icbm-10m): [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [25 Megaton ICBM](A2-Catalog-Missiles.md#25-megaton-icbm-icbm-25m): [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [50 Megaton Pure Fusion ICBM](A2-Catalog-Missiles.md#50-megaton-pure-fusion-icbm-icbm-50m-fusion): [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3x250kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-light-mirv-icbm-3x250kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [3x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-light-mirv-icbm-3x500kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy)
- [8x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#8x500kt-light-mirv-icbm-8x500kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [8x1M Light Fusion MIRV](A2-Catalog-Missiles.md#8x1m-light-fusion-mirv-8x1m-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)
- [3x250kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-heavy-mirv-icbm-3x250kt-icbm): [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm), [MIRV](A5-Catalog-Technologies.md#mirv-mirv), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-heavy-mirv-icbm-3x500kt-icbm): [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [6x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#6x500kt-heavy-mirv-icbm-6x500kt-icbm): [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [6x1M Heavy MIRV ICBM](A2-Catalog-Missiles.md#6x1m-heavy-mirv-icbm-6x1m-icbm): [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy)
- [12x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#12x500kt-heavy-mirv-icbm-12x500kt-icbm): [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [12x1M Pure Fusion MIRV](A2-Catalog-Missiles.md#12x1m-pure-fusion-mirv-12x1m-icbm): [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)
- [1M Light Cobalt ICBM](A2-Catalog-Missiles.md#1m-light-cobalt-icbm-icbm-1m-cobalt): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [10M Heavy Cobalt ICBM](A2-Catalog-Missiles.md#10m-heavy-cobalt-icbm-icbm-10m-cobalt): [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Launchpad ICBM](A5-Catalog-Technologies.md#launchpad-icbm-launchpad_icbm), [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [1M Light Salted ICBM](A2-Catalog-Missiles.md#1m-light-salted-icbm-icbm-1m-salt): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [10M Heavy Salted ICBM](A2-Catalog-Missiles.md#10m-heavy-salted-icbm-icbm-10m-salt): [Hypersonic Glide Vehicles](A5-Catalog-Technologies.md#hypersonic-glide-vehicles-hypersonic_glide_vehicles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp)
- [1M Super EMP ICBM](A2-Catalog-Missiles.md#1m-super-emp-icbm-icbm-1m-super-emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [10M Super EMP ICBM](A2-Catalog-Missiles.md#10m-super-emp-icbm-icbm-10m-super-emp): [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Nuclear ASAT](A2-Catalog-Missiles.md#nuclear-asat-nuclear-asat): [Precision ASAT Weapons](A5-Catalog-Technologies.md#precision-asat-weapons-asat), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp)
- [ASAT](A2-Catalog-Missiles.md#asat-asat): [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat)
- [Co-Orbital ASAT](A2-Catalog-Missiles.md#co-orbital-asat-co-orbital-asat): [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Makeshift Airbase (`Improvised_Airbase`)

<!-- img:unit Units/Images/Icons/Ground/Airbase_Makeshift.png -->

An improvised airbase with very limited facilities, which can only support a limited number of multirole fighters and some helicopters. Benefits from being cheap to build and easy to produce in emergencies.  
\+ Cheap to build compared to regular air bases.  
\+ Hosts multirole fighters and helicopters.  
\- Supports a very small number of aircraft.  
\- No built-in radar facilities.

**How to get it:** [Improvised Airbases](A5-Catalog-Technologies.md#improvised-airbases-improvised_airbase) (`Improvised_Airbase`) — technology `U_Improvised_Airbase`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 15 |
| `size` | 0.75 |
| `productioncost` | 6 |
| `selfdestructtime` | 15 s |

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Aircraft hosted:** 6 × [Multirole Attacker](#multirole-attacker-attack), 2 × [Attack Helicopter](#attack-helicopter-attack_helicopter).

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Midcourse ABM Site (`ABM_Site`)

<!-- img:upgrades Units/Images/Icons/Ground/ABM_Site.png=Base|Units/Images/Icons/Ground/ABM_Site_Adv.png=Hit-To-Kill Midcourse ABM -->

A fixed site used for launching midcourse ABMs. This is the only unit capable of launching nuclear ABMs, and it offers greater range than terminal ABM sites. However, it has a minimum range, and is better suited for broad area defence.  
\+ Fires conventional and nuclear ABMs.  
\+ Great anti-missile capability.  
\- Only has ABMs for weaponry.  
\- Requires OTH radar to be effective.

**How to get it:** [Nuclear Midcourse ABM](A5-Catalog-Technologies.md#nuclear-midcourse-abm-nuke_abm) (`Nuke_ABM`) — technology `U_ABM_site`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2.5 |
| `size` | 0.1 |
| `productioncost` | 10 |
| `attackdelay` | 0.05 s |
| `selfdestructtime` | 5 s |

**Weapons** (switchable configurations):

- *Unarmed*: no weapons (a technology adds them)
- *Conventional ABM (default)*: [Neutron-Kill ABM](A2-Catalog-Missiles.md#neutron-kill-abm-light-nuclear-abm) (`Light Nuclear ABM`) (unlimited, reload 5 s, auto-engages)
- *Heavy ABM*: no weapons (a technology adds them)
- *Fusion ABM*: no weapons (a technology adds them)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km).

**Upgrades:**

- With [Conventional Midcourse ABM](A5-Catalog-Technologies.md#conventional-midcourse-abm-anti_ballistic_missile) (`anti_ballistic_missile`):
    - weapon config “Conventional ABM” becomes:
        - [Midcourse ABM (ABM)](A2-Catalog-Missiles.md#midcourse-abm-abm-abm) (`ABM`) (unlimited, reload 4 s, auto-engages)
    - weapon config “Heavy ABM” becomes:
        - [High-Yield Midcourse ABM](A2-Catalog-Missiles.md#high-yield-midcourse-abm-nuclear-abm) (`Nuclear ABM`) (×1, reload 4 s, auto-engages)
    - weapon config “Fusion ABM” becomes:
        - [Fusion Midcourse ABM](A2-Catalog-Missiles.md#fusion-midcourse-abm-fusion-abm) (`Fusion ABM`) (×1, reload 4 s, auto-engages)
- With [Nuclear Midcourse ABM](A5-Catalog-Technologies.md#nuclear-midcourse-abm-nuke_abm) (`Nuke_ABM`) + [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`):
    - weapon config “Heavy ABM” becomes:
        - [High-Yield Midcourse ABM](A2-Catalog-Missiles.md#high-yield-midcourse-abm-nuclear-abm) (`Nuclear ABM`) (×1, reload 5 s, auto-engages)
- With [Hit-To-Kill Midcourse ABM](A5-Catalog-Technologies.md#hit-to-kill-midcourse-abm-abm_mk2) (`ABM_Mk2`):
    - weapon config “Conventional ABM” becomes:
        - [Midcourse ABM (ABM)](A2-Catalog-Missiles.md#midcourse-abm-abm-abm) (`ABM`) (unlimited, salvo 2, reload 4 s, auto-engages)
    - new appearance
- With [Advanced Midcourse ABM](A5-Catalog-Technologies.md#advanced-midcourse-abm-abm_mk3) (`ABM_Mk3`):
    - weapon config “Conventional ABM” becomes:
        - [Midcourse ABM (ABM)](A2-Catalog-Missiles.md#midcourse-abm-abm-abm) (`ABM`) (unlimited, salvo 2, reload 3 s, auto-engages)
    - weapon config “Heavy ABM” becomes:
        - [High-Yield Midcourse ABM](A2-Catalog-Missiles.md#high-yield-midcourse-abm-nuclear-abm) (`Nuclear ABM`) (×1, reload 3 s, auto-engages)
    - weapon config “Fusion ABM” becomes:
        - [Fusion Midcourse ABM](A2-Catalog-Missiles.md#fusion-midcourse-abm-fusion-abm) (`Fusion ABM`) (×1, reload 3 s, auto-engages)
- With [Experimental Midcourse ABM](A5-Catalog-Technologies.md#experimental-midcourse-abm-abm_mk4) (`ABM_Mk4`):
    - weapon config “Conventional ABM” becomes:
        - [Midcourse ABM (ABM)](A2-Catalog-Missiles.md#midcourse-abm-abm-abm) (`ABM`) (unlimited, salvo 2, reload 2.5 s, auto-engages)
    - weapon config “Heavy ABM” becomes:
        - [High-Yield Midcourse ABM](A2-Catalog-Missiles.md#high-yield-midcourse-abm-nuclear-abm) (`Nuclear ABM`) (×1, reload 2.5 s, auto-engages)
    - weapon config “Fusion ABM” becomes:
        - [Fusion Midcourse ABM](A2-Catalog-Missiles.md#fusion-midcourse-abm-fusion-abm) (`Fusion ABM`) (×1, reload 2.5 s, auto-engages)
- With [Nuclear Midcourse ABM](A5-Catalog-Technologies.md#nuclear-midcourse-abm-nuke_abm) (`Nuke_ABM`) + [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes) (`Advanced_Tactical_nukes`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`):
    - weapon config “Fusion ABM” becomes:
        - [Fusion Midcourse ABM](A2-Catalog-Missiles.md#fusion-midcourse-abm-fusion-abm) (`Fusion ABM`) (×1, reload 5 s, auto-engages)

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Hit-To-Kill Midcourse ABM”](#hit-to-kill-midcourse-abm-abm_mk2_modifier) (`ABM_Mk2_Modifier`) (active after researching [Hit-To-Kill Midcourse ABM](A5-Catalog-Technologies.md#hit-to-kill-midcourse-abm-abm_mk2) (`ABM_Mk2`)): enemy weapons (118): `canbeintercepted` ×1.3
- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Advanced Midcourse ABM”](#advanced-midcourse-abm-abm_mk3_modifier) (`ABM_Mk3_Modifier`) (active after researching [Advanced Midcourse ABM](A5-Catalog-Technologies.md#advanced-midcourse-abm-abm_mk3) (`ABM_Mk3`)): enemy weapons (118): `canbeintercepted` ×1.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_invulnerable) (`EMP_Defence_Invulnerable`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0

**Other traits:** `ABM_Mk4_Modifier`.

### Missile Silo (`Missile_Silo`)

<!-- img:unit Units/Images/Icons/Ground/ICBM_Silo.png -->

An underground missile silo used to house and launch ICBMs. Missile silos are hardened structures which are difficult to destroy, and being underground and well-hidden makes them difficult to detect. Missile silos can fire heavy ICBMs with the appropriate upgrades and are much less vulnerable than the earlier missile launchpads.  
\+ Can fire light ICBMs without upgrades.  
\+ Has the potential to use heavy ICBMs.  
\+ Harder to locate than other units.  
\+ Hardened structure, heightened survivability.  
\+ Shorter firing delay than ICBM launchpads.  
\- No built-in defences.  
\- Immobile, vulnerable when detected.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) — technology `U_Missile_Silo`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 225 |
| `size` | 0.2 |
| `productioncost` | 27.5 |
| `attackdelay` | 9 s |
| `selfdestructtime` | 20 s |

**Weapons** (switchable configurations):

- *Unarmed*: no weapons (a technology adds them)
- *Bioweapon ICBM (default)*: [Rabbit Fever ICBM](A2-Catalog-Missiles.md#rabbit-fever-icbm-bioweapon_icbm) (`Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Improved\_Bioweapon ICBM (default)*: [Smallpox ICBM](A2-Catalog-Missiles.md#smallpox-icbm-improved_bioweapon_icbm) (`Improved_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Advanced Bioweapon ICBM (default)*: [Ebola ICBM](A2-Catalog-Missiles.md#ebola-icbm-advanced_bioweapon_icbm) (`Advanced_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Engineered Bioweapon ICBM (default)*: [EMeVHF-24 ICBM](A2-Catalog-Missiles.md#emevhf-24-icbm-engineered_bioweapon_icbm) (`Engineered_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *3x Biological MIRV (default)*: [3xBW Bioweapon MIRV](A2-Catalog-Missiles.md#3xbw-bioweapon-mirv-bioweapon_mirv) (`Bioweapon_MIRV`) (×1, reload 49.3 s)
- *8x Biological MIRV (default)*: [8xBW Bioweapon MIRV](A2-Catalog-Missiles.md#8xbw-bioweapon-mirv-8x-bioweapon_mirv) (`8x Bioweapon_MIRV`) (×1, reload 49.3 s)
- *Lightweight 250kt (default)*: [250 Kiloton Light ICBM](A2-Catalog-Missiles.md#250-kiloton-light-icbm-icbm-250kt-light) (`ICBM (250kt Light)`) (×1, reload 49.3 s)
- *Lightweight 500kt (default)*: [500 Kiloton Light ICBM](A2-Catalog-Missiles.md#500-kiloton-light-icbm-icbm-500kt-light) (`ICBM (500kt Light)`) (×1, reload 49.3 s)
- *Lightweight Megaton (default)*: [Megaton Light ICBM](A2-Catalog-Missiles.md#megaton-light-icbm-icbm-1m-light) (`ICBM (1M Light)`) (×1, reload 49.3 s)
- *Lightweight 5Mt (default)*: [5 Megaton Light ICBM](A2-Catalog-Missiles.md#5-megaton-light-icbm-icbm-5m-light) (`ICBM (5M Light)`) (×1, reload 49.3 s)
- *Lightweight 10Mt Fusion (default)*: [10M Pure Fusion ICBM](A2-Catalog-Missiles.md#10m-pure-fusion-icbm-icbm-10m-fusion-light) (`ICBM (10M Fusion Light)`) (×1, reload 49.3 s)
- *Heavy 500kt (default)*: no weapons (a technology adds them)
- *Heavy 5 Megaton (default)*: no weapons (a technology adds them)
- *Heavy 10 Megaton (default)*: no weapons (a technology adds them)
- *Heavy 25 Megaton (default)*: no weapons (a technology adds them)
- *Heavy 50 Megaton Fusion (default)*: no weapons (a technology adds them)
- *3x250kt Light MIRV*: [3x250kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-light-mirv-icbm-3x250kt-light-icbm) (`3x250kt Light ICBM`) (×1, reload 49.3 s)
- *3x500kt Light MIRV*: [3x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-light-mirv-icbm-3x500kt-light-icbm) (`3x500kt Light ICBM`) (×1, reload 49.3 s)
- *8x500kt Light MIRV*: [8x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#8x500kt-light-mirv-icbm-8x500kt-light-icbm) (`8x500kt Light ICBM`) (×1, reload 49.3 s)
- *8x1M Light MIRV*: [8x1M Light Fusion MIRV](A2-Catalog-Missiles.md#8x1m-light-fusion-mirv-8x1m-light-icbm) (`8x1M Light ICBM`) (×1, reload 49.3 s)
- *3x250kt MIRV (default)*: no weapons (a technology adds them)
- *3x500kt MIRV (default)*: no weapons (a technology adds them)
- *6x500kt MIRV (default)*: no weapons (a technology adds them)
- *6x1Mt MIRV (default)*: no weapons (a technology adds them)
- *12x500kt MIRV (default)*: no weapons (a technology adds them)
- *12x1Mt Fusion MIRV (default)*: no weapons (a technology adds them)
- *1MT Cobalt (default)*: [1M Light Cobalt ICBM](A2-Catalog-Missiles.md#1m-light-cobalt-icbm-icbm-1m-cobalt) (`ICBM (1M Cobalt)`) (×1, reload 49.3 s)
- *10MT Cobalt (default)*: no weapons (a technology adds them)
- *1MT Salted (default)*: [1M Light Salted ICBM](A2-Catalog-Missiles.md#1m-light-salted-icbm-icbm-1m-salt) (`ICBM (1M Salt)`) (×1, reload 49.3 s)
- *10MT Enhanced Salted (default)*: no weapons (a technology adds them)
- *1M EMP ICBM*: [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp) (`ICBM (1M EMP)`) (×1, reload 49.3 s)
- *1M Super EMP ICBM*: [1M Super EMP ICBM](A2-Catalog-Missiles.md#1m-super-emp-icbm-icbm-1m-super-emp) (`ICBM (1M Super EMP)`) (×1, reload 49.3 s)
- *10M Super EMP ICBM*: no weapons (a technology adds them)
- *Nuclear ASAT*: [Nuclear ASAT](A2-Catalog-Missiles.md#nuclear-asat-nuclear-asat) (`Nuclear ASAT`) (×1)
- *ASAT*: [ASAT](A2-Catalog-Missiles.md#asat-asat) (`ASAT`) (×1)
- *Co-Orbital ASAT*: [Co-Orbital ASAT](A2-Catalog-Missiles.md#co-orbital-asat-co-orbital-asat) (`Co-Orbital ASAT`) (×1, reload 49.3 s)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `attackdelay` ×0.35
- With [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles) (`Heavy_Missiles`):
    - weapon config “Heavy 500kt” becomes:
        - [500 Kiloton Heavy ICBM](A2-Catalog-Missiles.md#500-kiloton-heavy-icbm-icbm-500kt-heavy) (`ICBM (500kt Heavy)`) (×1, reload 60 s)
    - weapon config “Heavy 5 Megaton” becomes:
        - [5 Megaton ICBM](A2-Catalog-Missiles.md#5-megaton-icbm-icbm-5m-heavy) (`ICBM (5M Heavy)`) (×1, reload 60 s)
    - weapon config “Heavy 10 Megaton” becomes:
        - [10 Megaton ICBM](A2-Catalog-Missiles.md#10-megaton-icbm-icbm-10m) (`ICBM (10M)`) (×1, reload 60 s)
    - weapon config “Heavy 25 Megaton” becomes:
        - [25 Megaton ICBM](A2-Catalog-Missiles.md#25-megaton-icbm-icbm-25m) (`ICBM (25M)`) (×1, reload 60 s)
    - weapon config “Heavy 50 Megaton Fusion” becomes:
        - [50 Megaton Pure Fusion ICBM](A2-Catalog-Missiles.md#50-megaton-pure-fusion-icbm-icbm-50m-fusion) (`ICBM (50M Fusion)`) (×1, reload 60 s)
    - weapon config “3x250kt MIRV” becomes:
        - [3x250kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-heavy-mirv-icbm-3x250kt-icbm) (`3x250kt ICBM`) (×1, reload 60 s)
    - weapon config “3x500kt MIRV” becomes:
        - [3x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-heavy-mirv-icbm-3x500kt-icbm) (`3x500kt ICBM`) (×1, reload 60 s)
    - weapon config “6x500kt MIRV” becomes:
        - [6x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#6x500kt-heavy-mirv-icbm-6x500kt-icbm) (`6x500kt ICBM`) (×1, reload 60 s)
    - weapon config “6x1Mt MIRV” becomes:
        - [6x1M Heavy MIRV ICBM](A2-Catalog-Missiles.md#6x1m-heavy-mirv-icbm-6x1m-icbm) (`6x1M ICBM`) (×1, reload 60 s)
    - weapon config “12x500kt MIRV” becomes:
        - [12x500kt Heavy MIRV ICBM](A2-Catalog-Missiles.md#12x500kt-heavy-mirv-icbm-12x500kt-icbm) (`12x500kt ICBM`) (×1, reload 60 s)
    - weapon config “12x1Mt Fusion MIRV” becomes:
        - [12x1M Pure Fusion MIRV](A2-Catalog-Missiles.md#12x1m-pure-fusion-mirv-12x1m-icbm) (`12x1M ICBM`) (×1, reload 60 s)
    - weapon config “10MT Cobalt” becomes:
        - [10M Heavy Cobalt ICBM](A2-Catalog-Missiles.md#10m-heavy-cobalt-icbm-icbm-10m-cobalt) (`ICBM (10M Cobalt)`) (×1, reload 60 s)
    - weapon config “10MT Enhanced Salted” becomes:
        - [10M Heavy Salted ICBM](A2-Catalog-Missiles.md#10m-heavy-salted-icbm-icbm-10m-salt) (`ICBM (10M Salt)`) (×1, reload 60 s)
    - weapon config “10M Super EMP ICBM” becomes:
        - [10M Super EMP ICBM](A2-Catalog-Missiles.md#10m-super-emp-icbm-icbm-10m-super-emp) (`ICBM (10M Super EMP)`) (×1, reload 60 s)

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Rabbit Fever ICBM](A2-Catalog-Missiles.md#rabbit-fever-icbm-bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Smallpox ICBM](A2-Catalog-Missiles.md#smallpox-icbm-improved_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Ebola ICBM](A2-Catalog-Missiles.md#ebola-icbm-advanced_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [EMeVHF-24 ICBM](A2-Catalog-Missiles.md#emevhf-24-icbm-engineered_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3xBW Bioweapon MIRV](A2-Catalog-Missiles.md#3xbw-bioweapon-mirv-bioweapon_mirv): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy)
- [8xBW Bioweapon MIRV](A2-Catalog-Missiles.md#8xbw-bioweapon-mirv-8x-bioweapon_mirv): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)
- [250 Kiloton Light ICBM](A2-Catalog-Missiles.md#250-kiloton-light-icbm-icbm-250kt-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [500 Kiloton Light ICBM](A2-Catalog-Missiles.md#500-kiloton-light-icbm-icbm-500kt-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Megaton Light ICBM](A2-Catalog-Missiles.md#megaton-light-icbm-icbm-1m-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [5 Megaton Light ICBM](A2-Catalog-Missiles.md#5-megaton-light-icbm-icbm-5m-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [10M Pure Fusion ICBM](A2-Catalog-Missiles.md#10m-pure-fusion-icbm-icbm-10m-fusion-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3x250kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-light-mirv-icbm-3x250kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [3x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-light-mirv-icbm-3x500kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy)
- [8x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#8x500kt-light-mirv-icbm-8x500kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [8x1M Light Fusion MIRV](A2-Catalog-Missiles.md#8x1m-light-fusion-mirv-8x1m-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)
- [1M Light Cobalt ICBM](A2-Catalog-Missiles.md#1m-light-cobalt-icbm-icbm-1m-cobalt): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [1M Light Salted ICBM](A2-Catalog-Missiles.md#1m-light-salted-icbm-icbm-1m-salt): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp)
- [1M Super EMP ICBM](A2-Catalog-Missiles.md#1m-super-emp-icbm-icbm-1m-super-emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Nuclear ASAT](A2-Catalog-Missiles.md#nuclear-asat-nuclear-asat): [Precision ASAT Weapons](A5-Catalog-Technologies.md#precision-asat-weapons-asat), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp)
- [ASAT](A2-Catalog-Missiles.md#asat-asat): [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat)
- [Co-Orbital ASAT](A2-Catalog-Missiles.md#co-orbital-asat-co-orbital-asat): [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Underground”](#underground-underground) (`Underground`) (always active):
    - enemy sensors (3): `range` ×0.75
    - enemy sensors (11): `range` ×0.5
    - enemy sensors (6): `range` ×0.25

### Cyber Warfare Center (`Cyber_Warfare_Center`)

A discreet office space staffed by hackers and intelligence operatives with the provisions necessary to conduct anonymous cyber attacks against foreign entities. Cyber Attacks will not trigger war and cannot be traced back to the attacker unless it's possible to deduce who was responsible by other means. This can be useful for subtly weakening your opponent's GDP output without being immediately culpable.  
Different targets are affected by cyber attacks in different ways:  
When used against an enemy city, it temporarily nullifies the espionage capabilites of that city and also reduces its science and espionage GDP outputs.  
When uses against an espionage or research center, it temporarily nullifies the bonuses provided by the building.  
When used against an enemy cyber warfare center, it prevents it from executing an attack of its own.  
\+ Can be used to cripple enemy espionage.  
\+ Can be used to harm enemy GDP outputs.  
\+ Does not reveal itself when attacking.  
\+ Can be built in numbers for greater effect.  
\- No direct offensive capabilities.  
\- Very vulnerable if discovered.  
\- Not dramatic or exciting.

**How to get it:** [Cyber Warfare](A5-Catalog-Technologies.md#cyber-warfare-espionage_4) (`Espionage_4`) — technology `U_Cyber_Warfare_Center`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `size` | 0.1 |
| `productioncost` | 4 |
| `maxnumberonmap` | 5 |
| `attackdelay` | 60 s |
| `selfdestructtime` | 10 s |

**Weapons**:

- *default*: [Cyber Warfare](A2-Catalog-Missiles.md#cyber-warfare-cyber_warfare_debuff) (`Cyber_Warfare_Debuff`) (unlimited, reload 60 s, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Covert Unit”](#covert-unit-covert_unit) (`Covert_Unit`) (always active):
    - enemy [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces), [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `range` ×0
    - enemy [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision): `range` ×0.75
    - enemy sensors (20): `range` ×0
    - enemy [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): `range` ×1
    - enemy [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance): `range` ×0.4
    - enemy [Periscope](A4-Catalog-Radars.md#periscope-periscope): `range` ×0.5
- [“Cyber Warfare Center”](#cyber-warfare-center-u_cyber_warfare_center) (`U_Cyber_Warfare_Center`) (active after researching [Cyber Warfare](A5-Catalog-Technologies.md#cyber-warfare-espionage_4) (`Espionage_4`)): enemy [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `range` = 37

### Laser Defence Complex (`Laser_Defence_Complex`)

<!-- img:unit Units/Images/Icons/Ground/ABM_Laser_Site.png -->

A fixed anti-missile site that houses a high-powered laser capable of destroying incoming ballistic missiles. Extremely effective within its range against single warheads, but with limited range. Excellent against missiles that are usually difficult to intercept, like hypersonic glide vehicles. Best used in conjunction with other missile defences. More effective than its mobile counterparts, and extremely effective at point-defence for priority targets like large cities or key military installations.  
\+ Very effective against hypersonic weapons.  
\+ High interception rate against all targets.  
\+ Powerful enough to destroy satellites.  
\- Very limited range.  
\- Expensive.

**How to get it:** [Terminal Defence Lasers](A5-Catalog-Technologies.md#terminal-defence-lasers-terminal_defence_laser) (`Terminal_Defence_Laser`) — technology `U_Laser_Site`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 8 |
| `size` | 0.2 |
| `productioncost` | 12 |
| `selfdestructtime` | 15 s |

**Weapons**:

- *default*:
    - [Terminal Defence Laser](A2-Catalog-Missiles.md#terminal-defence-laser-terminal-abm-laser) (`Terminal ABM Laser`) (unlimited, reload 0.3 s, auto-engages)
    - [Ground-Based ASAT Laser](A2-Catalog-Missiles.md#ground-based-asat-laser-ground-asat-laser) (`Ground ASAT Laser`) (unlimited, reload 2 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_invulnerable) (`EMP_Defence_Invulnerable`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Terminal Ballistic Missile Defences”](#terminal-ballistic-missile-defences-terminal_abm_no_target_decoy_modifier) (`Terminal_ABM_No_Target_Decoy_Modifier`) (always active): enemy [Decoy Warhead](A2-Catalog-Missiles.md#decoy-warhead-false-icbm-warhead): `canbeintercepted` = 0

**Other traits:** `Static_Defender_Bonus`.

## Ground forces

### AA Gun Site (`AA_Site_Old`)

<!-- img:upgrades Units/Images/Icons/Ground/AA_Gun_Site_1.png=Base|Units/Images/Icons/Ground/AA_Gun_Site_2.png=Early Infantry Fighting Vehicles|Units/Images/Icons/Ground/AA_Gun_Site_3.png=Modernized Armoured Vehicles|Units/Images/Icons/Ground/AA_Gun_Site_4.png=Novel Fighting Vehicle Concepts -->

A series of AA gun emplacements used to defend against enemy aircraft. They have very limited effectiveness against jet-powered aircraft, but can provide a degree of protection and deterrence until they can be replaced by better anti-air weapons.  
\+ Effective against light aircraft.  
\+ Cheap to build.  
\+ Inherently mobile.  
\+ Fires light SAMs with upgrades.  
\+ Can be upgraded to a laser.  
\+ Air-deployable from transport planes.  
\- Very limited range.  
\- Needs SAMs to engage high-altitude targets.

**How to get it:** available from the start — technology `U_AA_Site_Old`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2.5 |
| `speed` | 40 |
| `size` | 0.1 |
| `turnspeed` | 7.5 |
| `productioncost` | 3 |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*:
    - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, salvo 2, reload 0.4 s, auto-engages)
    - [Light SAM](A2-Catalog-Missiles.md#light-sam-light-sam) (`Light SAM`) (unlimited, salvo 2, reload 1.2 s, auto-engages)
    - [Light Missile Defence SAM](A2-Catalog-Missiles.md#light-missile-defence-sam-light-sam-md) (`Light SAM MD`) (unlimited, salvo 2, reload 1.2 s, auto-engages)
    - [Light SAM](A2-Catalog-Missiles.md#light-sam-light-sam) (`Light SAM`) (unlimited, salvo 2, reload 1.2 s, auto-engages)
    - [Light Missile Defence SAM](A2-Catalog-Missiles.md#light-missile-defence-sam-light-sam-md) (`Light SAM MD`) (unlimited, salvo 2, reload 1.2 s, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km).

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`):
    - `speed` = 45
    - new appearance
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`):
    - `speed` = 55
    - new appearance
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`): `speed` = 65
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`):
    - `speed` = 75
    - new appearance
- With [Anti-Air Laser Weapons](A5-Catalog-Technologies.md#anti-air-laser-weapons-aa_laser) (`AA_Laser`): `weapon` multiply

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5), [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons)
- [Light SAM](A2-Catalog-Missiles.md#light-sam-light-sam): [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2)
- [Light Missile Defence SAM](A2-Catalog-Missiles.md#light-missile-defence-sam-light-sam-md): [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Army Division (Army Division) (`Army_Division`)

<!-- img:upgrades Units/Images/Icons/Ground/Army_Division_1.png=Base|Units/Images/Icons/Ground/Army_Division_2.png=Early Infantry Fighting Vehicles|Units/Images/Icons/Ground/Army_Division_3.png=Modernized Armoured Vehicles|Units/Images/Icons/Ground/Army_Division_4.png=Armoured Mid-life Upgrades|Units/Images/Icons/Ground/Army_Division_5.png=Novel Fighting Vehicle Concepts -->

An army division consists of several different regiments with different roles, which are capable of performing combined arms tactics when working together. An army division has the logistical support to function independently, and is large enough to occupy cities.  
Armies can travel over land and destroy any enemy units they come across. They can also move into enemy cities and occupy them, denying the enemy access to their economic output. Capturing cities also allows you to annex enemy territory. Sending an army to an army base will load it onto a transport plane so it can be deployed by air. Armies can also board landing ships and deploy by sea.  
A historically commonplace yet reprehensible use for armies is to deliberately target civilians and destroy cities. Commanding an army to attack a city (rather than just moving to it) will cause the army to start razing the city to the ground.  
\+ Can occupy enemy cities.  
\+ Hard to destroy.  
\+ Can slowly raze cities.  
\- Instantly visible when in enemy territory.  
\- Very slow.  
\- Only effective against ground assets.  
\- May turn you into a war criminal.

**How to get it:** available from the start — technology `U_Army`.

**Built at / carried by:** [Air Transport](#air-transport-air_transport), [Army Base](#army-base-army_base), [Landing Ship](#landing-ship-landing_ship).

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 150 |
| `speed` | 30 |
| `size` | 1 |
| `turnspeed` | 4 |
| `productioncost` | 18 |
| `occupationradius` | 75 |
| `selfdestructtime` | 60 s |

**Weapons**:

- *Army Weapons*:
    - [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces) (`Land Forces`) (unlimited, reload 0.3 s, auto-engages, principal)
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, off by default)
    - [Body Armour](A2-Catalog-Missiles.md#body-armour-body-armor) (`Body Armor`) (×1)
    - [Optics](A2-Catalog-Missiles.md#optics-optics) (`Optics`) (×1)
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (unlimited, reload 2.5 s, auto-engages, off by default)
    - [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery) (`Nuclear Artillery`) (unlimited, reload 5 s, auto-engages)
    - [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery) (`Fusion Artillery`) (unlimited, reload 5 s, auto-engages)
    - [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery) (`Chemical Artillery`) (unlimited, reload 3.3 s, auto-engages)
    - [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery) (`Improved Chemical Artillery`) (unlimited, reload 3.3 s, auto-engages)
    - [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery) (`Advanced Chemical Artillery`) (unlimited, reload 3.3 s, auto-engages)
    - [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery) (`Experimental Chemical Artillery`) (unlimited, reload 3.3 s, auto-engages)
    - [Massacre Civilians](A2-Catalog-Missiles.md#massacre-civilians-massacre-civilians) (`Massacre Civilians`) (unlimited, reload 3.3 s)
    - [C-RAM](A2-Catalog-Missiles.md#c-ram-c-ram) (`C-RAM`) (unlimited, reload 0.2 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance) (125 km).

**Modes:**

- Army Mobile Mode (`Army_Mobile_Mode`): `power` 100, `speed` 50. Weapons: *Army Weapons*: [Combined Arms (Land Forces Mobile)](A2-Catalog-Missiles.md#combined-arms-land-forces-mobile-land-forces-mobile) (`Land Forces Mobile`) (unlimited, reload 3.3 s, auto-engages, principal); [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, off by default); [Body Armour](A2-Catalog-Missiles.md#body-armour-body-armor) (`Body Armor`) (×1); [Optics](A2-Catalog-Missiles.md#optics-optics) (`Optics`) (×1); [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (unlimited, reload 2.5 s, auto-engages, off by default); [C-RAM](A2-Catalog-Missiles.md#c-ram-c-ram) (`C-RAM`) (unlimited, reload 0.2 s, auto-engages, off by default)
- Army Entrenched (`Army_Entrenched`): `power` 175

**Upgrades:**

- At DEFCON 4: `productioncost` ×0.9
- At DEFCON 3: `productioncost` ×0.85
- At DEFCON 2: `productioncost` ×0.825
- At DEFCON 1: `productioncost` ×0.8
- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`):
    - `speed` ×1.333
    - `power` ×1.05
    - new appearance
- With [Improved Personal Army Equipment](A5-Catalog-Technologies.md#improved-personal-army-equipment-improved_basic_protection) (`Improved_Basic_Protection`): `power` ×1.15
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`):
    - `speed` ×1.125
    - `power` ×1.05
    - new appearance
- With [Basic Woven Body Armour](A5-Catalog-Technologies.md#basic-woven-body-armour-basic_body_armor) (`Basic_Body_Armor`): `power` ×1.15
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`):
    - `speed` ×1.222
    - `power` ×1.05
    - new appearance
- With [Improved Ceramic Armour](A5-Catalog-Technologies.md#improved-ceramic-armour-improved_body_armor) (`Improved_Body_Armor`): `power` ×1.15
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`):
    - `speed` ×1.09
    - `power` ×1.05
    - new appearance
- With [Composite Liquid Armour](A5-Catalog-Technologies.md#composite-liquid-armour-advanced_body_armor) (`Advanced_Body_Armor`): `power` ×1.15
- With [Powered Nanomaterial Armour](A5-Catalog-Technologies.md#powered-nanomaterial-armour-experimental_body_armor) (`Experimental_Body_Armor`): `power` ×1.15

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces): [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2), [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3), [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4), [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5), [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery): [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes)
- [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery): [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes)
- [Massacre Civilians](A2-Catalog-Missiles.md#massacre-civilians-massacre-civilians): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons)
- [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance): [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)

**Situational effects:**

- While under the lasting effect of Chemical 1: `speed` ×0.75
- While under the lasting effect of Chemical 2: `speed` ×0.75
- While under the lasting effect of Chemical 3: `speed` ×0.75
- While under the lasting effect of Chemical 4: `speed` ×0.75
- While under the lasting effect of Biological: `speed` ×0.75
- While under the lasting effect of Biological2: `speed` ×0.75
- While under the lasting effect of Biological3: `speed` ×0.75
- While under the lasting effect of BiologicalX: `speed` ×0.75

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic CBRN Defence”](#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`) (always active): enemy weapons (114): `damage` ×0.5
- [“Basic CBRN Defence”](#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`) (active after researching [Basic CBRN Defence](A5-Catalog-Technologies.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`)): enemy weapons (136): `damage` ×0.8
- [“CBRN Countermeasures”](#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`) (active after researching [CBRN Countermeasures](A5-Catalog-Technologies.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)): enemy weapons (136): `damage` ×0.8
- [“Specialized CBRN Reconnaissance”](#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`) (active after researching [Specialized CBRN Reconnaissance](A5-Catalog-Technologies.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`)): enemy weapons (136): `damage` ×0.85
- [“Advanced CBRN Equipment”](#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`) (active after researching [Advanced CBRN Equipment](A5-Catalog-Technologies.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)): enemy weapons (136): `damage` ×0.85

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Unit BioChem Modifier”](#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`) (always active): enemy weapons (13): `damage` ×7.5

### Combat Engineers (`Combat_Engineers`)

<!-- img:unit Units/Images/Icons/Ground/Combat_Engineers.png -->

The role of combat engineers is to provide support to the rest of the military by eliminating physical obstacles and building military infrastructure like bridges or fortifications. Structures like radar sites, forward operating bases and security checkpoints can be built by combat engineers by producing them and giving the engineers the materials, and then having the engineers deploy them. Since combat engineers are mobile, they can effectively construct fixed friendly assets in enemy territory.  
\+ Can carry and deploy structures in enemy territory.  
\+ Can build makeshift airbases.  
\+ Can build forward operating bases.  
\+ Can build radar and SAM sites.  
\+ Can build security checkpoints.  
\+ Can build ballistic missile sites.  
\- Limited capacity to hold buildable units.  
\- Instantly visible when in enemy territory.  
\- Very limited weaponry, vulnerable to attack.

**How to get it:** available from the start — technology `U_Combat_Engineers`.

**Built at / carried by:** [Air Transport](#air-transport-air_transport), [Army Base](#army-base-army_base), [Landing Ship](#landing-ship-landing_ship).

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 40 |
| `speed` | 30 |
| `size` | 0.8 |
| `turnspeed` | 4 |
| `productioncost` | 12 |
| `selfdestructtime` | 40 s |

**Weapons**:

- *default*:
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, off by default)
    - [Body Armour](A2-Catalog-Missiles.md#body-armour-body-armor) (`Body Armor`) (×1)
    - [Optics](A2-Catalog-Missiles.md#optics-optics) (`Optics`) (×1)
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (unlimited, reload 2.5 s, auto-engages, off by default)
    - [C-RAM](A2-Catalog-Missiles.md#c-ram-c-ram) (`C-RAM`) (unlimited, reload 0.2 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Can transport:** [Radar Site](#radar-site-fixed_lw_radar), [SAM Site](#sam-site-sam_site), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Security Checkpoint](#security-checkpoint-security_checkpoint), [Makeshift Airbase](#makeshift-airbase-improvised_airbase), [Ballistic Missile Site](#ballistic-missile-site-srbm_site).

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`):
    - `speed` ×1.333
    - `power` ×1.05
- With [Improved Personal Army Equipment](A5-Catalog-Technologies.md#improved-personal-army-equipment-improved_basic_protection) (`Improved_Basic_Protection`): `power` ×1.15
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`):
    - `speed` ×1.125
    - `power` ×1.05
- With [Basic Woven Body Armour](A5-Catalog-Technologies.md#basic-woven-body-armour-basic_body_armor) (`Basic_Body_Armor`): `power` ×1.15
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`):
    - `speed` ×1.222
    - `power` ×1.05
- With [Improved Ceramic Armour](A5-Catalog-Technologies.md#improved-ceramic-armour-improved_body_armor) (`Improved_Body_Armor`): `power` ×1.15
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`):
    - `speed` ×1.09
    - `power` ×1.05
- With [Composite Liquid Armour](A5-Catalog-Technologies.md#composite-liquid-armour-advanced_body_armor) (`Advanced_Body_Armor`): `power` ×1.15
- With [Powered Nanomaterial Armour](A5-Catalog-Technologies.md#powered-nanomaterial-armour-experimental_body_armor) (`Experimental_Body_Armor`): `power` ×1.15

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)

**Situational effects:**

- While under the lasting effect of Chemical 1: `speed` ×0.75
- While under the lasting effect of Chemical 2: `speed` ×0.75
- While under the lasting effect of Chemical 3: `speed` ×0.75
- While under the lasting effect of Chemical 4: `speed` ×0.75
- While under the lasting effect of Biological: `speed` ×0.75
- While under the lasting effect of Biological2: `speed` ×0.75
- While under the lasting effect of Biological3: `speed` ×0.75
- While under the lasting effect of BiologicalX: `speed` ×0.75

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Basic CBRN Defence”](#basic-cbrn-defence-cbrn_defence_0) (`CBRN_Defence_0`) (always active): enemy weapons (114): `damage` ×0.5
- [“Basic CBRN Defence”](#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`) (active after researching [Basic CBRN Defence](A5-Catalog-Technologies.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`)): enemy weapons (136): `damage` ×0.8
- [“CBRN Countermeasures”](#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`) (active after researching [CBRN Countermeasures](A5-Catalog-Technologies.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`)): enemy weapons (136): `damage` ×0.8
- [“Specialized CBRN Reconnaissance”](#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`) (active after researching [Specialized CBRN Reconnaissance](A5-Catalog-Technologies.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`)): enemy weapons (136): `damage` ×0.85
- [“Advanced CBRN Equipment”](#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`) (active after researching [Advanced CBRN Equipment](A5-Catalog-Technologies.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`)): enemy weapons (136): `damage` ×0.85

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Unit BioChem Modifier”](#unit-biochem-modifier-unit_biochem_modifier) (`Unit_BioChem_Modifier`) (always active): enemy weapons (13): `damage` ×7.5

### Security Checkpoint (`Security_Checkpoint`)

<!-- img:unit Units/Images/Icons/Ground/Security_Checkpoint.png -->

A static checkpoint used to screen for suspicious vehicles or individuals passing by. Security checkpoints can be used to detect and engage enemy covert units that get too close.  
\+ Great defence against covert units.  
\+ Relatively inexpensive.  
\- Only effective against covert units.  
\- Easily found and destroyed by other means.

**How to get it:** available from the start — technology `U_Security_Checkpoint`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `size` | 0.25 |
| `productioncost` | 3 |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*:
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages, principal)
    - [Body Armour](A2-Catalog-Missiles.md#body-armour-body-armor) (`Body Armor`) (×1)
    - [Optics](A2-Catalog-Missiles.md#optics-optics) (`Optics`) (×1)
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (unlimited, reload 2.5 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy) (200 km).

**Upgrades:**

- With [Improved Personal Army Equipment](A5-Catalog-Technologies.md#improved-personal-army-equipment-improved_basic_protection) (`Improved_Basic_Protection`): `power` ×1.15
- With [Basic Woven Body Armour](A5-Catalog-Technologies.md#basic-woven-body-armour-basic_body_armor) (`Basic_Body_Armor`): `power` ×1.15
- With [Improved Ceramic Armour](A5-Catalog-Technologies.md#improved-ceramic-armour-improved_body_armor) (`Improved_Body_Armor`): `power` ×1.15
- With [Composite Liquid Armour](A5-Catalog-Technologies.md#composite-liquid-armour-advanced_body_armor) (`Advanced_Body_Armor`): `power` ×1.15
- With [Powered Nanomaterial Armour](A5-Catalog-Technologies.md#powered-nanomaterial-armour-experimental_body_armor) (`Experimental_Body_Armor`): `power` ×1.15

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

**Other traits:** `Static_Defender_Bonus`.

### Spec-Ops Team (`Spec_Ops_Team`)

<!-- img:upgrades Units/Images/Icons/Ground/Spec_Ops_1.png=Base|Units/Images/Icons/Ground/Spec_Ops_2.png=Modernized Armoured Vehicles|Units/Images/Icons/Ground/Spec_Ops_3.png=Novel Fighting Vehicle Concepts -->

A team of exceptionally capable soldiers trained to operate behind enemy lines. They are difficult to detect by regular units and can sneak into enemy territory to destroy their infrastructure. They are also better at finding and destroying other covert units than other units are, making them effective at stopping enemy bomb trucks and other spec-ops teams.  
\+ Can only be detected at close range.  
\+ Good at countering other covert units.  
\+ Can destroy undefended enemy equipment.  
\+ Deployable by helicopter.  
\- Limited firepower.  
\- Easily destroyed if spotted.

**How to get it:** available from the start — technology `U_Spec_Ops`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 1 |
| `speed` | 60 |
| `size` | 0.01 |
| `turnspeed` | 8 |
| `productioncost` | 10 |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*:
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages)
    - [Body Armour](A2-Catalog-Missiles.md#body-armour-body-armor) (`Body Armor`) (×1)
    - [Optics](A2-Catalog-Missiles.md#optics-optics) (`Optics`) (×1)
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (unlimited, reload 2.5 s, auto-engages, off by default)
    - [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge) (`Demolition Charge`) (unlimited, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy) (200 km).

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`): `speed` = 70
- With [Improved Personal Army Equipment](A5-Catalog-Technologies.md#improved-personal-army-equipment-improved_basic_protection) (`Improved_Basic_Protection`): `power` ×1.15
- With [Specialized Small Arms Programs](A5-Catalog-Technologies.md#specialized-small-arms-programs-spec_ops_boost_1) (`Spec_Ops_Boost_1`):
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): `time` = 9.5
    - [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `time` ×0.65
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): `time` = 65
    - `power` ×1.05
- With [Improved Special Mission Equipment](A5-Catalog-Technologies.md#improved-special-mission-equipment-spec_ops_boost_2) (`Spec_Ops_Boost_2`):
    - `power` ×1.1
    - `speed` +10
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`):
    - `speed` = 85
    - `power` ×1.05
    - new appearance
- With [Basic Woven Body Armour](A5-Catalog-Technologies.md#basic-woven-body-armour-basic_body_armor) (`Basic_Body_Armor`): `power` ×1.15
- With [Chemical Performance Enhancers](A5-Catalog-Technologies.md#chemical-performance-enhancers-spec_ops_boost_3) (`Spec_Ops_Boost_3`):
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): `time` = 8.5
    - [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `time` ×0.8
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): `time` = 45
    - `power` ×1.05
    - `speed` +5
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`): `speed` = 100
- With [Improved Ceramic Armour](A5-Catalog-Technologies.md#improved-ceramic-armour-improved_body_armor) (`Improved_Body_Armor`): `power` ×1.15
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`):
    - `speed` = 110
    - `power` ×1.05
    - new appearance
- With [Composite Liquid Armour](A5-Catalog-Technologies.md#composite-liquid-armour-advanced_body_armor) (`Advanced_Body_Armor`): `power` ×1.15
- With [Powered Nanomaterial Armour](A5-Catalog-Technologies.md#powered-nanomaterial-armour-experimental_body_armor) (`Experimental_Body_Armor`): `power` ×1.15
- With [Genetically Enhanced Super Soldiers](A5-Catalog-Technologies.md#genetically-enhanced-super-soldiers-spec_ops_boost_4) (`Spec_Ops_Boost_4`):
    - [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): `time` = 7
    - [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `time` ×0.8
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): `time` = 35
    - `power` ×1.1
    - `speed` +5

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons)
- [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Covert Unit”](#covert-unit-covert_unit) (`Covert_Unit`) (always active):
    - enemy [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces), [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `range` ×0
    - enemy [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision): `range` ×0.75
    - enemy sensors (20): `range` ×0
    - enemy [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): `range` ×1
    - enemy [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance): `range` ×0.4
    - enemy [Periscope](A4-Catalog-Radars.md#periscope-periscope): `range` ×0.5

### Jamming Vehicle (`EW_MOBILE`)

<!-- img:unit Units/Images/Icons/Ground/Jamming_Vehicle.png -->

A vehicle equipped with an electronic warfare suite, which can jam enemy radar systems and reduce their effective range. Jamming vehicles are best used to conceal friendly units, and reduce the ability of nearby enemies to detect and attack units from a distance.  
\+ Reduces enemy radar range.  
\+ Can reduce enemy attack range.  
\+ Can potentially conceal friendly units.  
\+ Air-deployable from transport planes.  
\- No conventional weapons.  
\- Very vulnerable when alone.

**How to get it:** [Mobile Jammers](A5-Catalog-Technologies.md#mobile-jammers-jammers) (`Jammers`) — technology `U_EW_MOBILE`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `speed` | 40 |
| `size` | 0.075 |
| `turnspeed` | 7.5 |
| `productioncost` | 4 |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*: [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer) (`EW Jammer`) (×1)

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`): `speed` = 45
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`): `speed` = 55
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`): `speed` = 65
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`): `speed` = 75
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): [SEAD/EW Aircraft](A5-Catalog-Technologies.md#seadew-aircraft-jammers_mk2), [DRFM Jamming Systems](A5-Catalog-Technologies.md#drfm-jamming-systems-jammers_mk3), [Advanced AESA Jammers](A5-Catalog-Technologies.md#advanced-aesa-jammers-jammers_mk4)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Short-Wave Radar Vehicle (`Mobile_SW_Radar`)

<!-- img:unit Units/Images/Icons/Ground/Mobile_Radar.png -->

A temporary, relocatable short-wave radar system. These are best used as an inexpensive way to provide more radar coverage to detect enemy aircraft or escort friendly expeditionary forces, as they lack weapons and have limited range compared to fixed sites. They are still cost effective however, as they are very cheap to produce.  
\+ Detects enemy aircraft.  
\+ Can be relocated.  
\+ Very cheap to produce.  
\+ Air-deployable from transport planes.  
\- Lacks weapons.

**How to get it:** [Pulse Doppler Radar](A5-Catalog-Technologies.md#pulse-doppler-radar-radar_mk2) (`Radar_Mk2`) — technology `U_Mobile_SW_Radar`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `speed` | 50 |
| `size` | 0.1 |
| `turnspeed` | 8 |
| `productioncost` | 3 |
| `selfdestructtime` | 5 s |

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) (300 km), [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) (525 km).

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`): `speed` = 55
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`): `speed` = 65
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`): `speed` = 75
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`): `speed` = 85

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak): [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6)

**Sensor vulnerabilities:**

- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Bomb Truck (`Bomb_Truck`)

<!-- img:unit Units/Images/Icons/Ground/Bomb_Truck.png -->

A civilian cargo truck designed to blend in with regular vehicle traffic. The truck has been modified to carry and conceal a large bomb, and can discreetly drive to a target site before detonating. Effective at surprising the enemy and as a psychological weapon, but not potent or cost-effective enough to warrant being a primary strategy.  
\+ Only detected when very close to enemy units.  
\+ Relatively cheap and simple.  
\+ Offers an element of surprise.  
\- Completely defenseless.  
\- Self-destructs upon attacking.  
\- Very slow.  
\- Not effective as a main strategy.

**How to get it:** [Nuclear Terrorism](A5-Catalog-Technologies.md#nuclear-terrorism-nuclear_terrorism) (`Nuclear_Terrorism`) — technology `U_Bomb_Truck`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 0.5 |
| `speed` | 55 |
| `size` | 0.05 |
| `turnspeed` | 10 |
| `productioncost` | 2.5 |

**Weapons** (switchable configurations):

- *C4 (default)*: [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)
- *Light 100kt Bomb*: [Light 100 Kiloton Bomb](A2-Catalog-Missiles.md#light-100-kiloton-bomb-100kt_nuke_light) (`100kt_nuke_light`) (×1)
- *Light 250kt Bomb*: [Light 250 Kiloton Bomb](A2-Catalog-Missiles.md#light-250-kiloton-bomb-250kt_nuke_light) (`250kt_nuke_light`) (×1)
- *Light 500kt Bomb*: [Light 500 kiloton Bomb](A2-Catalog-Missiles.md#light-500-kiloton-bomb-500kt-nuke_light) (`500kt nuke_light`) (×1)
- *Light Megaton Bomb*: [Light Megaton Bomb](A2-Catalog-Missiles.md#light-megaton-bomb-1m-nuke_light) (`1M nuke_light`) (×1)
- *Light 5 Megaton Bomb*: [Light 5M Pure Fusion Bomb](A2-Catalog-Missiles.md#light-5m-pure-fusion-bomb-5m-nuke_light) (`5M nuke_light`) (×1)
- *Light 500kt Cobalt Bomb*: [Light 500kt Cobalt Bomb](A2-Catalog-Missiles.md#light-500kt-cobalt-bomb-500kt-light-cobalt-bomb) (`500kt Light Cobalt Bomb`) (×1)
- *Light 500kt Enhanced Salted Bomb*: [Light 500kt Salted Bomb](A2-Catalog-Missiles.md#light-500kt-salted-bomb-500kt-light-salt-bomb) (`500kt Light Salt Bomb`) (×1)
- *Tularemia Bomb*:
    - [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb) (`Bioweapon_bomb`) (×1, principal)
    - [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)
- *Smallpox Bomb*:
    - [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb) (`Improved_Bioweapon_bomb`) (×1, principal)
    - [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)
- *Ebola Bomb*:
    - [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb) (`Advanced_Bioweapon_bomb`) (×1, principal)
    - [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)
- *Medusa Fever Bomb*:
    - [EMeVHF-24 Bomb](A2-Catalog-Missiles.md#emevhf-24-bomb-engineered_bioweapon_bomb) (`Engineered_Bioweapon_bomb`) (×1, principal)
    - [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons)
- [Light 250 Kiloton Bomb](A2-Catalog-Missiles.md#light-250-kiloton-bomb-250kt_nuke_light): [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads)
- [Light 500 kiloton Bomb](A2-Catalog-Missiles.md#light-500-kiloton-bomb-500kt-nuke_light): [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [Light Megaton Bomb](A2-Catalog-Missiles.md#light-megaton-bomb-1m-nuke_light): [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [Light 500kt Cobalt Bomb](A2-Catalog-Missiles.md#light-500kt-cobalt-bomb-500kt-light-cobalt-bomb): [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb): [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2)
- [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb): [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3)
- [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb): [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Covert Unit”](#covert-unit-covert_unit) (`Covert_Unit`) (always active):
    - enemy [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces), [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `range` ×0
    - enemy [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision): `range` ×0.75
    - enemy sensors (20): `range` ×0
    - enemy [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): `range` ×1
    - enemy [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance): `range` ×0.4
    - enemy [Periscope](A4-Catalog-Radars.md#periscope-periscope): `range` ×0.5

**Other traits:** `Bomb_Truck`.

### Coastal Missile Battery (`Coastal`)

<!-- img:upgrades Units/Images/Icons/Ground/Coastal_Missile_1.png=Base|Units/Images/Icons/Ground/Coastal_Missile_2.png=Precision Cruise Missiles -->

A mobile missile launcher armed with long-range anti-ship missiles. They are designed to provide a degree of defence against enemy surface ships, and can be relocated to provide protection elsewhere if necessary.  
\+ Can target enemy naval vessels.  
\+ Inexpensive to produce.  
\+ Can be repositioned.  
\+ Air-deployable from transport planes.  
\- Can only target submarines when surfaced.  
\- Can only attack naval targets.

**How to get it:** [Coastal Missile Batteries](A5-Catalog-Technologies.md#coastal-missile-batteries-coastal_defence) (`Coastal_Defence`) — technology `U_COASTAL`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 3.5 |
| `speed` | 40 |
| `size` | 0.08 |
| `turnspeed` | 8 |
| `productioncost` | 6 |
| `attackdelay` | 1 s |
| `selfdestructtime` | 5 s |

**Weapons**:

- *Anti-Shipping*: [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 5 s, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km).

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`): `speed` = 45
- With [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles) (`Improved_cruise_missiles`):
    - new appearance
    - weapon config “Anti-Shipping” becomes:
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 5 s, auto-engages)
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`): `speed` = 55
- With [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles) (`Enhanced_cruise_missiles`):
    - weapon config “Anti-Shipping” becomes:
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 3, reload 5 s, auto-engages)
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`): `speed` = 65
- With [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles) (`Advanced_cruise_missiles`):
    - weapon config “Anti-Shipping” becomes:
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 3, reload 4 s, auto-engages)
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`): `speed` = 75

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile): [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles), [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles), [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles), [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)

**Sensor vulnerabilities:**

- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Mobile SAM (`MOBILE_SAM`)

<!-- img:upgrades Units/Images/Icons/Ground/Mobile_SAM_1.png=Base|Units/Images/Icons/Ground/Mobile_SAM_2.png=Improved SAMs -->

Mobile SAM batteries consist of surface-to-air missiles and their supporting elements mounted to mobile chassis which can be rapidly set-up and fired on short-notice. This makes them suitable for tactical military applications and gives them greater flexibility than earlier fixed sites. Mobile SAMs should be used to accompany land forces as a means of defence against combat aircraft. They can also be placed strategically to deter enemy air incursions.  
\+ Effective against enemy aircraft.  
\+ Can shoot down missiles with upgrades.  
\+ Can escort and support friendly units.  
\+ Air-deployable from transport planes.  
\- Vulnerable to non-airborne threats.  
\- Less cost-effective than fixed sites.

**How to get it:** [Mobile SAM Systems](A5-Catalog-Technologies.md#mobile-sam-systems-mobile_sam) (`Mobile_SAM`) — technology `U_Mobile_SAM`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2.5 |
| `speed` | 40 |
| `size` | 0.05 |
| `turnspeed` | 7.5 |
| `productioncost` | 6 |
| `attackdelay` | 0.25 s |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*:
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, salvo 2, reload 1.7 s, auto-engages)
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, salvo 2, reload 1.7 s, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km).

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`): `speed` = 45
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`): `speed` = 55
- With [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2) (`SAM_Mk2`):
    - new appearance
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): `time` = 35
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): `time` = 35
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): `launch` = 2
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): `launch` = 2
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`): `speed` = 65
- With [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3) (`SAM_Mk3`):
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): `time` = 20
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): `time` = 20
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`): `speed` = 75
- With [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4) (`SAM_Mk4`):
    - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): `time` = 15
    - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): `time` = 15

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam): [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2)
- [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md): [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### MRBM TEL Vehicle (`Mobile_MRBM`)

<!-- img:unit Units/Images/Icons/Ground/MRBM_TEL.png -->

A vehicle capable of carrying and launching medium-range ballistic missiles. Medium-range missiles have the extended range needed to destroy key strategic targets and are cheaper, easier to fire and less conspicuous than ICBMs. They are useful for counter-force applications, but can also be used to target cities.  
\+ Effective against strategic assets.  
\+ Cheaper than ICBMs.  
\+ Good reach against threatening targets.  
\- Not as cost-effective against armies.  
\- Vulnerable when alone.  
\- Cannot deploy by transport plane, only ships.

**How to get it:** [Transporter Erector Launcher Vehicles](A5-Catalog-Technologies.md#transporter-erector-launcher-vehicles-mobile_mrbm) (`Mobile_MRBM`) + [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm) (`MRBM`) — technology `U_Mobile_MRBM`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `speed` | 50 |
| `size` | 0.08 |
| `turnspeed` | 8 |
| `productioncost` | 15.75 |
| `attackdelay` | 5 s |
| `selfdestructtime` | 10 s |

**Weapons** (switchable configurations):

- *Unarmed*: no weapons (a technology adds them)
- *Chemical MRBM (default)*:
    - [Mustard Gas MRBM](A2-Catalog-Missiles.md#mustard-gas-mrbm-chemical_mrbm) (`Chemical_MRBM`) (unlimited, reload 21.3 s)
    - [Sarin MRBM](A2-Catalog-Missiles.md#sarin-mrbm-improved_chemical_mrbm) (`Improved_Chemical_MRBM`) (unlimited, reload 21.3 s)
    - [VX Gas MRBM](A2-Catalog-Missiles.md#vx-gas-mrbm-advanced_chemical_mrbm) (`Advanced_Chemical_MRBM`) (unlimited, reload 21.3 s)
    - [Novichok-2000 MRBM](A2-Catalog-Missiles.md#novichok-2000-mrbm-experimental_chemical_mrbm) (`Experimental_Chemical_MRBM`) (unlimited, reload 21.3 s)
- *Bioweapon MRBM (default)*: [Rabbit Fever MRBM](A2-Catalog-Missiles.md#rabbit-fever-mrbm-bioweapon_mrbm) (`Bioweapon_MRBM`) (×1, reload 21.3 s)
- *Improved Bioweapon MRBM (default)*: [Smallpox MRBM](A2-Catalog-Missiles.md#smallpox-mrbm-improved_bioweapon_mrbm) (`Improved_Bioweapon_MRBM`) (×1, reload 21.3 s)
- *Advanced Bioweapon MRBM (default)*: [Ebola MRBM](A2-Catalog-Missiles.md#ebola-mrbm-advanced_bioweapon_mrbm) (`Advanced_Bioweapon_MRBM`) (×1, reload 21.3 s)
- *Engineered Bioweapon MRBM (default)*: [EMeVHF-24 MRBM](A2-Catalog-Missiles.md#emevhf-24-mrbm-engineered_bioweapon_mrbm) (`Engineered_Bioweapon_MRBM`) (×1, reload 21.3 s)
- *Conventional MRBM (default)*: [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm) (`Conventional MRBM`) (unlimited, reload 21.3 s)
- *100kt MRBM (default)*: [100 Kiloton MRBM](A2-Catalog-Missiles.md#100-kiloton-mrbm-100kt_mrbm) (`100kt_MRBM`) (×1, reload 21.3 s)
- *250kt MRBM (default)*: [250 Kiloton MRBM](A2-Catalog-Missiles.md#250-kiloton-mrbm-250kt_mrbm) (`250kt_MRBM`) (×1, reload 21.3 s)
- *500kt MRBM (default)*: [500 Kiloton MRBM](A2-Catalog-Missiles.md#500-kiloton-mrbm-500kt_mrbm) (`500kt_MRBM`) (×1, reload 21.3 s)
- *Megaton MRBM (default)*: [Megaton MRBM](A2-Catalog-Missiles.md#megaton-mrbm-1m_mrbm) (`1M_MRBM`) (×1, reload 21.3 s)
- *5M MRBM (default)*: [5 Megaton MRBM](A2-Catalog-Missiles.md#5-megaton-mrbm-5m_mrbm) (`5M_MRBM`) (×1, reload 21.3 s)
- *500kt Cobalt MRBM (default)*: [500kt Cobalt MRBM](A2-Catalog-Missiles.md#500kt-cobalt-mrbm-500kt_cobalt_mrbm) (`500kt_Cobalt_MRBM`) (×1, reload 21.3 s)
- *500kt Enhanced Salted MRBM (default)*: [500kt Salted MRBM](A2-Catalog-Missiles.md#500kt-salted-mrbm-500kt_salt_mrbm) (`500kt_Salt_MRBM`) (×1, reload 21.3 s)
- *500kt EMP MRBM*: [500kt EMP MRBM](A2-Catalog-Missiles.md#500kt-emp-mrbm-500kt_mrbm_emp) (`500kt_MRBM_EMP`) (×1, reload 21.3 s)
- *500kt Super EMP MRBM*: [500kt Super EMP MRBM](A2-Catalog-Missiles.md#500kt-super-emp-mrbm-500kt_mrbm_emp_super) (`500kt_MRBM_EMP_Super`) (×1, reload 21.3 s)
- *3x100kt MIRV MRBM (default)*: [3x100kt MIRV MRBM](A2-Catalog-Missiles.md#3x100kt-mirv-mrbm-3x100kt_mrbm) (`3x100kt_MRBM`) (×1, reload 21.3 s)
- *3x250kt MIRV MRBM (default)*: [3x250kt MIRV MRBM](A2-Catalog-Missiles.md#3x250kt-mirv-mrbm-3x250kt_mrbm) (`3x250kt_MRBM`) (×1, reload 21.3 s)
- *6x250kt MIRV MRBM (default)*: [6x250kt MIRV MRBM](A2-Catalog-Missiles.md#6x250kt-mirv-mrbm-6x250kt_mrbm) (`6x250kt_MRBM`) (×1, reload 21.3 s)
- *6x500kt MIRV MRBM (default)*: [6x500kt MIRV MRBM](A2-Catalog-Missiles.md#6x500kt-mirv-mrbm-6x500kt_mrbm) (`6x500kt_MRBM`) (×1, reload 21.3 s)
- *8x500 MIRV MRBM (default)*: [8x500kt MIRV MRBM](A2-Catalog-Missiles.md#8x500kt-mirv-mrbm-8x500kt_mrbm) (`8x500kt_MRBM`) (×1, reload 21.3 s)
- *8x1MT MRBM (default)*: [8x1MT Pure Fusion MIRV MRBM](A2-Catalog-Missiles.md#8x1mt-pure-fusion-mirv-mrbm-8x1mt_mrbm) (`8x1MT_MRBM`) (×1, reload 21.3 s)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `attackdelay` ×0.35
- With [Improved TEL Systems](A5-Catalog-Technologies.md#improved-tel-systems-improved_tel) (`Improved_TEL`):
    - `speed` = 65
    - weapon config “Chemical MRBM” becomes:
        - [Mustard Gas MRBM](A2-Catalog-Missiles.md#mustard-gas-mrbm-chemical_mrbm) (`Chemical_MRBM`) (×1, reload 18 s)
        - [Sarin MRBM](A2-Catalog-Missiles.md#sarin-mrbm-improved_chemical_mrbm) (`Improved_Chemical_MRBM`) (unlimited, reload 18 s)
        - [VX Gas MRBM](A2-Catalog-Missiles.md#vx-gas-mrbm-advanced_chemical_mrbm) (`Advanced_Chemical_MRBM`) (unlimited, reload 18 s)
        - [Novichok-2000 MRBM](A2-Catalog-Missiles.md#novichok-2000-mrbm-experimental_chemical_mrbm) (`Experimental_Chemical_MRBM`) (unlimited, reload 18 s)
    - weapon config “Bioweapon MRBM” becomes:
        - [Rabbit Fever MRBM](A2-Catalog-Missiles.md#rabbit-fever-mrbm-bioweapon_mrbm) (`Bioweapon_MRBM`) (×1, reload 18 s)
    - weapon config “Improved Bioweapon MRBM” becomes:
        - [Smallpox MRBM](A2-Catalog-Missiles.md#smallpox-mrbm-improved_bioweapon_mrbm) (`Improved_Bioweapon_MRBM`) (×1, reload 18 s)
    - weapon config “Advanced Bioweapon MRBM” becomes:
        - [Ebola MRBM](A2-Catalog-Missiles.md#ebola-mrbm-advanced_bioweapon_mrbm) (`Advanced_Bioweapon_MRBM`) (×1, reload 18 s)
    - weapon config “Engineered Bioweapon MRBM” becomes:
        - [EMeVHF-24 MRBM](A2-Catalog-Missiles.md#emevhf-24-mrbm-engineered_bioweapon_mrbm) (`Engineered_Bioweapon_MRBM`) (×1, reload 18 s)
    - weapon config “Conventional MRBM” becomes:
        - [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm) (`Conventional MRBM`) (unlimited, reload 18 s)
    - weapon config “100kt MRBM” becomes:
        - [100 Kiloton MRBM](A2-Catalog-Missiles.md#100-kiloton-mrbm-100kt_mrbm) (`100kt_MRBM`) (×1, reload 18 s)
    - weapon config “250kt MRBM” becomes:
        - [250 Kiloton MRBM](A2-Catalog-Missiles.md#250-kiloton-mrbm-250kt_mrbm) (`250kt_MRBM`) (×1, reload 18 s)
    - weapon config “500kt MRBM” becomes:
        - [500 Kiloton MRBM](A2-Catalog-Missiles.md#500-kiloton-mrbm-500kt_mrbm) (`500kt_MRBM`) (×1, reload 18 s)
    - weapon config “Megaton MRBM” becomes:
        - [Megaton MRBM](A2-Catalog-Missiles.md#megaton-mrbm-1m_mrbm) (`1M_MRBM`) (×1, reload 18 s)
    - weapon config “5M MRBM” becomes:
        - [5 Megaton MRBM](A2-Catalog-Missiles.md#5-megaton-mrbm-5m_mrbm) (`5M_MRBM`) (×1, reload 18 s)
    - weapon config “500kt Cobalt MRBM” becomes:
        - [500kt Cobalt MRBM](A2-Catalog-Missiles.md#500kt-cobalt-mrbm-500kt_cobalt_mrbm) (`500kt_Cobalt_MRBM`) (×1, reload 18 s)
    - weapon config “500kt Enhanced Salted MRBM” becomes:
        - [500kt Salted MRBM](A2-Catalog-Missiles.md#500kt-salted-mrbm-500kt_salt_mrbm) (`500kt_Salt_MRBM`) (×1, reload 18 s)
    - weapon config “500kt EMP MRBM” becomes:
        - [500kt EMP MRBM](A2-Catalog-Missiles.md#500kt-emp-mrbm-500kt_mrbm_emp) (`500kt_MRBM_EMP`) (×1, reload 18 s)
    - weapon config “500kt Super EMP MRBM” becomes:
        - [500kt Super EMP MRBM](A2-Catalog-Missiles.md#500kt-super-emp-mrbm-500kt_mrbm_emp_super) (`500kt_MRBM_EMP_Super`) (×1, reload 18 s)
    - weapon config “3x100kt MIRV MRBM” becomes:
        - [3x100kt MIRV MRBM](A2-Catalog-Missiles.md#3x100kt-mirv-mrbm-3x100kt_mrbm) (`3x100kt_MRBM`) (×1, reload 18 s)
    - weapon config “3x250kt MIRV MRBM” becomes:
        - [3x250kt MIRV MRBM](A2-Catalog-Missiles.md#3x250kt-mirv-mrbm-3x250kt_mrbm) (`3x250kt_MRBM`) (×1, reload 18 s)
    - weapon config “6x250kt MIRV MRBM” becomes:
        - [6x250kt MIRV MRBM](A2-Catalog-Missiles.md#6x250kt-mirv-mrbm-6x250kt_mrbm) (`6x250kt_MRBM`) (×1, reload 18 s)
    - weapon config “6x500kt MIRV MRBM” becomes:
        - [6x500kt MIRV MRBM](A2-Catalog-Missiles.md#6x500kt-mirv-mrbm-6x500kt_mrbm) (`6x500kt_MRBM`) (×1, reload 18 s)
    - weapon config “8x500 MIRV MRBM” becomes:
        - [8x500kt MIRV MRBM](A2-Catalog-Missiles.md#8x500kt-mirv-mrbm-8x500kt_mrbm) (`8x500kt_MRBM`) (×1, reload 18 s)
    - weapon config “8x1MT MRBM” becomes:
        - [8x1MT Pure Fusion MIRV MRBM](A2-Catalog-Missiles.md#8x1mt-pure-fusion-mirv-mrbm-8x1mt_mrbm) (`8x1MT_MRBM`) (×1, reload 18 s)
- With [Advanced TEL Systems](A5-Catalog-Technologies.md#advanced-tel-systems-advanced_tel) (`Advanced_TEL`):
    - `speed` = 75
    - weapon config “Chemical MRBM” becomes:
        - [Mustard Gas MRBM](A2-Catalog-Missiles.md#mustard-gas-mrbm-chemical_mrbm) (`Chemical_MRBM`) (×1, reload 15 s)
        - [Sarin MRBM](A2-Catalog-Missiles.md#sarin-mrbm-improved_chemical_mrbm) (`Improved_Chemical_MRBM`) (unlimited, reload 15 s)
        - [VX Gas MRBM](A2-Catalog-Missiles.md#vx-gas-mrbm-advanced_chemical_mrbm) (`Advanced_Chemical_MRBM`) (unlimited, reload 15 s)
        - [Novichok-2000 MRBM](A2-Catalog-Missiles.md#novichok-2000-mrbm-experimental_chemical_mrbm) (`Experimental_Chemical_MRBM`) (unlimited, reload 15 s)
    - weapon config “Bioweapon MRBM” becomes:
        - [Rabbit Fever MRBM](A2-Catalog-Missiles.md#rabbit-fever-mrbm-bioweapon_mrbm) (`Bioweapon_MRBM`) (×1, reload 15 s)
    - weapon config “Improved Bioweapon MRBM” becomes:
        - [Smallpox MRBM](A2-Catalog-Missiles.md#smallpox-mrbm-improved_bioweapon_mrbm) (`Improved_Bioweapon_MRBM`) (×1, reload 15 s)
    - weapon config “Advanced Bioweapon MRBM” becomes:
        - [Ebola MRBM](A2-Catalog-Missiles.md#ebola-mrbm-advanced_bioweapon_mrbm) (`Advanced_Bioweapon_MRBM`) (×1, reload 15 s)
    - weapon config “Engineered Bioweapon MRBM” becomes:
        - [EMeVHF-24 MRBM](A2-Catalog-Missiles.md#emevhf-24-mrbm-engineered_bioweapon_mrbm) (`Engineered_Bioweapon_MRBM`) (×1, reload 15 s)
    - weapon config “Conventional MRBM” becomes:
        - [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm) (`Conventional MRBM`) (unlimited, reload 15 s)
    - weapon config “100kt MRBM” becomes:
        - [100 Kiloton MRBM](A2-Catalog-Missiles.md#100-kiloton-mrbm-100kt_mrbm) (`100kt_MRBM`) (×1, reload 15 s)
    - weapon config “250kt MRBM” becomes:
        - [250 Kiloton MRBM](A2-Catalog-Missiles.md#250-kiloton-mrbm-250kt_mrbm) (`250kt_MRBM`) (×1, reload 15 s)
    - weapon config “500kt MRBM” becomes:
        - [500 Kiloton MRBM](A2-Catalog-Missiles.md#500-kiloton-mrbm-500kt_mrbm) (`500kt_MRBM`) (×1, reload 15 s)
    - weapon config “Megaton MRBM” becomes:
        - [Megaton MRBM](A2-Catalog-Missiles.md#megaton-mrbm-1m_mrbm) (`1M_MRBM`) (×1, reload 15 s)
    - weapon config “5M MRBM” becomes:
        - [5 Megaton MRBM](A2-Catalog-Missiles.md#5-megaton-mrbm-5m_mrbm) (`5M_MRBM`) (×1, reload 15 s)
    - weapon config “500kt Cobalt MRBM” becomes:
        - [500kt Cobalt MRBM](A2-Catalog-Missiles.md#500kt-cobalt-mrbm-500kt_cobalt_mrbm) (`500kt_Cobalt_MRBM`) (×1, reload 15 s)
    - weapon config “500kt Enhanced Salted MRBM” becomes:
        - [500kt Salted MRBM](A2-Catalog-Missiles.md#500kt-salted-mrbm-500kt_salt_mrbm) (`500kt_Salt_MRBM`) (×1, reload 15 s)
    - weapon config “500kt EMP MRBM” becomes:
        - [500kt EMP MRBM](A2-Catalog-Missiles.md#500kt-emp-mrbm-500kt_mrbm_emp) (`500kt_MRBM_EMP`) (×1, reload 15 s)
    - weapon config “500kt Super EMP MRBM” becomes:
        - [500kt Super EMP MRBM](A2-Catalog-Missiles.md#500kt-super-emp-mrbm-500kt_mrbm_emp_super) (`500kt_MRBM_EMP_Super`) (×1, reload 15 s)
    - weapon config “3x100kt MIRV MRBM” becomes:
        - [3x100kt MIRV MRBM](A2-Catalog-Missiles.md#3x100kt-mirv-mrbm-3x100kt_mrbm) (`3x100kt_MRBM`) (×1, reload 15 s)
    - weapon config “3x250kt MIRV MRBM” becomes:
        - [3x250kt MIRV MRBM](A2-Catalog-Missiles.md#3x250kt-mirv-mrbm-3x250kt_mrbm) (`3x250kt_MRBM`) (×1, reload 15 s)
    - weapon config “6x250kt MIRV MRBM” becomes:
        - [6x250kt MIRV MRBM](A2-Catalog-Missiles.md#6x250kt-mirv-mrbm-6x250kt_mrbm) (`6x250kt_MRBM`) (×1, reload 15 s)
    - weapon config “6x500kt MIRV MRBM” becomes:
        - [6x500kt MIRV MRBM](A2-Catalog-Missiles.md#6x500kt-mirv-mrbm-6x500kt_mrbm) (`6x500kt_MRBM`) (×1, reload 15 s)
    - weapon config “8x500 MIRV MRBM” becomes:
        - [8x500kt MIRV MRBM](A2-Catalog-Missiles.md#8x500kt-mirv-mrbm-8x500kt_mrbm) (`8x500kt_MRBM`) (×1, reload 15 s)
    - weapon config “8x1MT MRBM” becomes:
        - [8x1MT Pure Fusion MIRV MRBM](A2-Catalog-Missiles.md#8x1mt-pure-fusion-mirv-mrbm-8x1mt_mrbm) (`8x1MT_MRBM`) (×1, reload 15 s)

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Mustard Gas MRBM](A2-Catalog-Missiles.md#mustard-gas-mrbm-chemical_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Sarin MRBM](A2-Catalog-Missiles.md#sarin-mrbm-improved_chemical_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [VX Gas MRBM](A2-Catalog-Missiles.md#vx-gas-mrbm-advanced_chemical_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Novichok-2000 MRBM](A2-Catalog-Missiles.md#novichok-2000-mrbm-experimental_chemical_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Rabbit Fever MRBM](A2-Catalog-Missiles.md#rabbit-fever-mrbm-bioweapon_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Smallpox MRBM](A2-Catalog-Missiles.md#smallpox-mrbm-improved_bioweapon_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Ebola MRBM](A2-Catalog-Missiles.md#ebola-mrbm-advanced_bioweapon_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [EMeVHF-24 MRBM](A2-Catalog-Missiles.md#emevhf-24-mrbm-engineered_bioweapon_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm): [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [100 Kiloton MRBM](A2-Catalog-Missiles.md#100-kiloton-mrbm-100kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [250 Kiloton MRBM](A2-Catalog-Missiles.md#250-kiloton-mrbm-250kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads)
- [500 Kiloton MRBM](A2-Catalog-Missiles.md#500-kiloton-mrbm-500kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Megaton MRBM](A2-Catalog-Missiles.md#megaton-mrbm-1m_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [5 Megaton MRBM](A2-Catalog-Missiles.md#5-megaton-mrbm-5m_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt Cobalt MRBM](A2-Catalog-Missiles.md#500kt-cobalt-mrbm-500kt_cobalt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [500kt Salted MRBM](A2-Catalog-Missiles.md#500kt-salted-mrbm-500kt_salt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt EMP MRBM](A2-Catalog-Missiles.md#500kt-emp-mrbm-500kt_mrbm_emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt Super EMP MRBM](A2-Catalog-Missiles.md#500kt-super-emp-mrbm-500kt_mrbm_emp_super): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [3x100kt MIRV MRBM](A2-Catalog-Missiles.md#3x100kt-mirv-mrbm-3x100kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [MIRV](A5-Catalog-Technologies.md#mirv-mirv), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3x250kt MIRV MRBM](A2-Catalog-Missiles.md#3x250kt-mirv-mrbm-3x250kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [6x250kt MIRV MRBM](A2-Catalog-Missiles.md#6x250kt-mirv-mrbm-6x250kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [6x500kt MIRV MRBM](A2-Catalog-Missiles.md#6x500kt-mirv-mrbm-6x500kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light)
- [8x500kt MIRV MRBM](A2-Catalog-Missiles.md#8x500kt-mirv-mrbm-8x500kt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Medium-Range Ballistic Missile](A5-Catalog-Technologies.md#medium-range-ballistic-missile-mrbm), [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [8x1MT Pure Fusion MIRV MRBM](A2-Catalog-Missiles.md#8x1mt-pure-fusion-mirv-mrbm-8x1mt_mrbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### SRBM TEL Vehicle (`Mobile_SRBM`)

<!-- img:unit Units/Images/Icons/Ground/SRBM_TEL.png -->

A vehicle designed to carry and launch short-range ballistic missiles. Short-ranged ballistic missiles are relatively cheap and can be fired quickly, making them effective in both tactical and strategic applications. However, the launchers are vulnerable if left unsupported.  
\+ Can attack land targets from long-range.  
\+ Fires quickly.  
\+ Relatively cheap.  
\+ Air-deployable from transport planes.  
\- Low blast yield compared to heavier weapons.  
\- Short range for a strategic weapon.

**How to get it:** [Transporter Erector Launcher Vehicles](A5-Catalog-Technologies.md#transporter-erector-launcher-vehicles-mobile_mrbm) (`Mobile_MRBM`) — technology `U_Mobile_SRBM`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `speed` | 60 |
| `size` | 0.08 |
| `turnspeed` | 8 |
| `productioncost` | 11.25 |
| `attackdelay` | 5 s |
| `selfdestructtime` | 5 s |

**Weapons** (switchable configurations):

- *Conventional*: [SRBM](A2-Catalog-Missiles.md#srbm-srbm) (`SRBM`) (unlimited, reload 18.3 s)
- *Chemical*:
    - [Mustard Gas SRBM](A2-Catalog-Missiles.md#mustard-gas-srbm-chemical_srbm) (`Chemical_SRBM`) (unlimited, reload 18.3 s)
    - [Sarin SRBM](A2-Catalog-Missiles.md#sarin-srbm-improved_chemical_srbm) (`Improved_Chemical_SRBM`) (unlimited, reload 18.3 s)
    - [VX Gas SRBM](A2-Catalog-Missiles.md#vx-gas-srbm-advanced_chemical_srbm) (`Advanced_Chemical_SRBM`) (unlimited, reload 18.3 s)
    - [Novichok-2000 SRBM](A2-Catalog-Missiles.md#novichok-2000-srbm-experimental_chemical_srbm) (`Experimental_Chemical_SRBM`) (unlimited, reload 18.3 s)
- *Nuclear*: [Nuclear SRBM](A2-Catalog-Missiles.md#nuclear-srbm-srbm-n) (`SRBM-N`) (×1, reload 18.3 s)
- *Pure Fusion*: [Fusion SRBM](A2-Catalog-Missiles.md#fusion-srbm-fusion-srbm) (`Fusion SRBM`) (×1, reload 18.3 s)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `attackdelay` ×0.35
- With [Improved TEL Systems](A5-Catalog-Technologies.md#improved-tel-systems-improved_tel) (`Improved_TEL`):
    - `speed` = 75
    - weapon config “Conventional” becomes:
        - [SRBM](A2-Catalog-Missiles.md#srbm-srbm) (`SRBM`) (unlimited, reload 16 s)
    - weapon config “Chemical” becomes:
        - [Mustard Gas SRBM](A2-Catalog-Missiles.md#mustard-gas-srbm-chemical_srbm) (`Chemical_SRBM`) (unlimited, reload 16 s)
        - [Sarin SRBM](A2-Catalog-Missiles.md#sarin-srbm-improved_chemical_srbm) (`Improved_Chemical_SRBM`) (unlimited, reload 16 s)
        - [VX Gas SRBM](A2-Catalog-Missiles.md#vx-gas-srbm-advanced_chemical_srbm) (`Advanced_Chemical_SRBM`) (unlimited, reload 16 s)
        - [Novichok-2000 SRBM](A2-Catalog-Missiles.md#novichok-2000-srbm-experimental_chemical_srbm) (`Experimental_Chemical_SRBM`) (unlimited, reload 16 s)
    - weapon config “Nuclear” becomes:
        - [Nuclear SRBM](A2-Catalog-Missiles.md#nuclear-srbm-srbm-n) (`SRBM-N`) (×1, reload 16 s)
    - weapon config “Pure Fusion” becomes:
        - [Fusion SRBM](A2-Catalog-Missiles.md#fusion-srbm-fusion-srbm) (`Fusion SRBM`) (×1, reload 16 s)
- With [Advanced TEL Systems](A5-Catalog-Technologies.md#advanced-tel-systems-advanced_tel) (`Advanced_TEL`):
    - `speed` = 90
    - weapon config “Conventional” becomes:
        - [SRBM](A2-Catalog-Missiles.md#srbm-srbm) (`SRBM`) (unlimited, reload 12.8 s)
    - weapon config “Chemical” becomes:
        - [Mustard Gas SRBM](A2-Catalog-Missiles.md#mustard-gas-srbm-chemical_srbm) (`Chemical_SRBM`) (unlimited, reload 12.8 s)
        - [Sarin SRBM](A2-Catalog-Missiles.md#sarin-srbm-improved_chemical_srbm) (`Improved_Chemical_SRBM`) (unlimited, reload 12.8 s)
        - [VX Gas SRBM](A2-Catalog-Missiles.md#vx-gas-srbm-advanced_chemical_srbm) (`Advanced_Chemical_SRBM`) (unlimited, reload 12.8 s)
        - [Novichok-2000 SRBM](A2-Catalog-Missiles.md#novichok-2000-srbm-experimental_chemical_srbm) (`Experimental_Chemical_SRBM`) (unlimited, reload 12.8 s)
    - weapon config “Nuclear” becomes:
        - [Nuclear SRBM](A2-Catalog-Missiles.md#nuclear-srbm-srbm-n) (`SRBM-N`) (×1, reload 12.8 s)
    - weapon config “Pure Fusion” becomes:
        - [Fusion SRBM](A2-Catalog-Missiles.md#fusion-srbm-fusion-srbm) (`Fusion SRBM`) (×1, reload 12.8 s)

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [SRBM](A2-Catalog-Missiles.md#srbm-srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Mustard Gas SRBM](A2-Catalog-Missiles.md#mustard-gas-srbm-chemical_srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Sarin SRBM](A2-Catalog-Missiles.md#sarin-srbm-improved_chemical_srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [VX Gas SRBM](A2-Catalog-Missiles.md#vx-gas-srbm-advanced_chemical_srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Novichok-2000 SRBM](A2-Catalog-Missiles.md#novichok-2000-srbm-experimental_chemical_srbm): [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Nuclear SRBM](A2-Catalog-Missiles.md#nuclear-srbm-srbm-n): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [MARV](A5-Catalog-Technologies.md#marv-marv), [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [Fusion SRBM](A2-Catalog-Missiles.md#fusion-srbm-fusion-srbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [MARV](A5-Catalog-Technologies.md#marv-marv)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### ICBM TEL Vehicle (`Mobile_ICBM`)

<!-- img:unit Units/Images/Icons/Ground/ICBM_TEL.png -->

A heavy vehicle capable of carrying and launching ICBMs. These vehicles are best used as a mobile nuclear deterrent, capable of destroying extremely distant high-value strategic targets or attacking enemy cities, while also being repositionable in order to avoid being located and destroyed.  
\+ Can fire ICBMs.  
\+ Can relocate.  
\- Can only fire light ICBMs.  
\- Vulnerable if undefended.  
\- Cannot deploy by transport plane, only ships.

**How to get it:** [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm) (`ICBM`) + [ICBM TEL Vehicle](A5-Catalog-Technologies.md#icbm-tel-vehicle-mobile_icbm) (`Mobile_ICBM`) — technology `U_Mobile_ICBM`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2.5 |
| `speed` | 40 |
| `size` | 0.1 |
| `turnspeed` | 8 |
| `productioncost` | 21 |
| `attackdelay` | 9 s |
| `selfdestructtime` | 15 s |

**Weapons** (switchable configurations):

- *Unarmed*: no weapons (a technology adds them)
- *Bioweapon ICBM (default)*: [Rabbit Fever ICBM](A2-Catalog-Missiles.md#rabbit-fever-icbm-bioweapon_icbm) (`Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Improved Bioweapon ICBM (default)*: [Smallpox ICBM](A2-Catalog-Missiles.md#smallpox-icbm-improved_bioweapon_icbm) (`Improved_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Advanced Bioweapon ICBM (default)*: [Ebola ICBM](A2-Catalog-Missiles.md#ebola-icbm-advanced_bioweapon_icbm) (`Advanced_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *Experimental Bioweapon ICBM (default)*: [EMeVHF-24 ICBM](A2-Catalog-Missiles.md#emevhf-24-icbm-engineered_bioweapon_icbm) (`Engineered_Bioweapon_ICBM`) (×1, reload 49.3 s)
- *3x Biological MIRV (default)*: [3xBW Bioweapon MIRV](A2-Catalog-Missiles.md#3xbw-bioweapon-mirv-bioweapon_mirv) (`Bioweapon_MIRV`) (×1, reload 49.3 s)
- *8x Biological MIRV (default)*: [8xBW Bioweapon MIRV](A2-Catalog-Missiles.md#8xbw-bioweapon-mirv-8x-bioweapon_mirv) (`8x Bioweapon_MIRV`) (×1, reload 49.3 s)
- *250kt (default)*: [250 Kiloton Light ICBM](A2-Catalog-Missiles.md#250-kiloton-light-icbm-icbm-250kt-light) (`ICBM (250kt Light)`) (×1, reload 49.3 s)
- *500kt (default)*: [500 Kiloton Light ICBM](A2-Catalog-Missiles.md#500-kiloton-light-icbm-icbm-500kt-light) (`ICBM (500kt Light)`) (×1, reload 49.3 s)
- *Megaton (default)*: [Megaton Light ICBM](A2-Catalog-Missiles.md#megaton-light-icbm-icbm-1m-light) (`ICBM (1M Light)`) (×1, reload 49.3 s)
- *5 Megaton (default)*: [5 Megaton Light ICBM](A2-Catalog-Missiles.md#5-megaton-light-icbm-icbm-5m-light) (`ICBM (5M Light)`) (×1, reload 49.3 s)
- *10 Megaton Fusion (default)*: [10M Pure Fusion ICBM](A2-Catalog-Missiles.md#10m-pure-fusion-icbm-icbm-10m-fusion-light) (`ICBM (10M Fusion Light)`) (×1, reload 49.3 s)
- *1MT Cobalt (default)*: [1M Light Cobalt ICBM](A2-Catalog-Missiles.md#1m-light-cobalt-icbm-icbm-1m-cobalt) (`ICBM (1M Cobalt)`) (×1, reload 49.3 s)
- *1MT Enhanced Salted (default)*: [1M Light Salted ICBM](A2-Catalog-Missiles.md#1m-light-salted-icbm-icbm-1m-salt) (`ICBM (1M Salt)`) (×1, reload 49.3 s)
- *1M EMP ICBM*: [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp) (`ICBM (1M EMP)`) (×1, reload 49.3 s)
- *1M Super EMP ICBM*: [1M Super EMP ICBM](A2-Catalog-Missiles.md#1m-super-emp-icbm-icbm-1m-super-emp) (`ICBM (1M Super EMP)`) (×1, reload 49.3 s)
- *3x250kt Light MIRV (default)*: [3x250kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-light-mirv-icbm-3x250kt-light-icbm) (`3x250kt Light ICBM`) (×1, reload 49.3 s)
- *3x500kt Light MIRV (default)*: [3x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-light-mirv-icbm-3x500kt-light-icbm) (`3x500kt Light ICBM`) (×1, reload 49.3 s)
- *8x500kt Light MIRV (default)*: [8x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#8x500kt-light-mirv-icbm-8x500kt-light-icbm) (`8x500kt Light ICBM`) (×1, reload 49.3 s)
- *8x1M Light MIRV (default)*: [8x1M Light Fusion MIRV](A2-Catalog-Missiles.md#8x1m-light-fusion-mirv-8x1m-light-icbm) (`8x1M Light ICBM`) (×1, reload 49.3 s)
- *ASAT*: [ASAT](A2-Catalog-Missiles.md#asat-asat) (`ASAT`) (×1)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Upgrades:**

- With [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets) (`Solid_Fuel_Rockets`): `attackdelay` ×0.35
- With [Improved TEL Systems](A5-Catalog-Technologies.md#improved-tel-systems-improved_tel) (`Improved_TEL`): `speed` = 50
- With [Advanced TEL Systems](A5-Catalog-Technologies.md#advanced-tel-systems-advanced_tel) (`Advanced_TEL`): `speed` = 60

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Rabbit Fever ICBM](A2-Catalog-Missiles.md#rabbit-fever-icbm-bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Smallpox ICBM](A2-Catalog-Missiles.md#smallpox-icbm-improved_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Ebola ICBM](A2-Catalog-Missiles.md#ebola-icbm-advanced_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [EMeVHF-24 ICBM](A2-Catalog-Missiles.md#emevhf-24-icbm-engineered_bioweapon_icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3xBW Bioweapon MIRV](A2-Catalog-Missiles.md#3xbw-bioweapon-mirv-bioweapon_mirv): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy)
- [8xBW Bioweapon MIRV](A2-Catalog-Missiles.md#8xbw-bioweapon-mirv-8x-bioweapon_mirv): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)
- [250 Kiloton Light ICBM](A2-Catalog-Missiles.md#250-kiloton-light-icbm-icbm-250kt-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [500 Kiloton Light ICBM](A2-Catalog-Missiles.md#500-kiloton-light-icbm-icbm-500kt-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [Megaton Light ICBM](A2-Catalog-Missiles.md#megaton-light-icbm-icbm-1m-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [5 Megaton Light ICBM](A2-Catalog-Missiles.md#5-megaton-light-icbm-icbm-5m-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [10M Pure Fusion ICBM](A2-Catalog-Missiles.md#10m-pure-fusion-icbm-icbm-10m-fusion-light): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [1M Light Cobalt ICBM](A2-Catalog-Missiles.md#1m-light-cobalt-icbm-icbm-1m-cobalt): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [1M Light Salted ICBM](A2-Catalog-Missiles.md#1m-light-salted-icbm-icbm-1m-salt): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [Compact ICBM](A5-Catalog-Technologies.md#compact-icbm-icbm), [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp)
- [1M Super EMP ICBM](A2-Catalog-Missiles.md#1m-super-emp-icbm-icbm-1m-super-emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [High-Power Rocket Designs](A5-Catalog-Technologies.md#high-power-rocket-designs-heavy_missiles), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3x250kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-light-mirv-icbm-3x250kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [3x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-light-mirv-icbm-3x500kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy)
- [8x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#8x500kt-light-mirv-icbm-8x500kt-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Novel Heavy Ballistic Missiles](A5-Catalog-Technologies.md#novel-heavy-ballistic-missiles-novel_bm_heavy), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [8x1M Light Fusion MIRV](A2-Catalog-Missiles.md#8x1m-light-fusion-mirv-8x1m-light-icbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)
- [ASAT](A2-Catalog-Missiles.md#asat-asat): [Advanced ASAT Weapons](A5-Catalog-Technologies.md#advanced-asat-weapons-advanced_asat)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Terminal ABM Site (`Terminal_ABM`)

<!-- img:upgrades Units/Images/Icons/Ground/Mobile_ABM.png=Base|Units/Images/Icons/Ground/Mobile_ABM_2.png=Hit-To-Kill Terminal ABM -->

A short-range missile defence site used to protect point targets from incoming warheads in the terminal phase of their trajectory. Terminal ABM sites have limited range, but are highly effective against any targets that it can engage. Use them to defend key targets like major cities and airbases.  
\+ Very effective against single warheads.  
\+ Mobile, can be relocated.  
\- Limited range and engagement time.  
\- Cannot deploy by transport plane, only ships.

**How to get it:** [Terminal Ballistic Missile Defences](A5-Catalog-Technologies.md#terminal-ballistic-missile-defences-terminal_bm_defence) (`Terminal_BM_Defence`) — technology `U_Terminal_ABM`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2.5 |
| `speed` | 40 |
| `size` | 0.07 |
| `turnspeed` | 7.5 |
| `productioncost` | 8 |
| `attackdelay` | 0.01 s |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*: [Terminal ABM](A2-Catalog-Missiles.md#terminal-abm-terminal-abm) (`Terminal ABM`) (unlimited, salvo 2, reload 2.2 s, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km).

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`): `speed` = 45
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`): `speed` = 55
- With [Hit-To-Kill Terminal ABM](A5-Catalog-Technologies.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2) (`Terminal_BM_Defence_Mk2`):
    - weapon config “default” becomes:
        - [Terminal ABM](A2-Catalog-Missiles.md#terminal-abm-terminal-abm) (`Terminal ABM`) (unlimited, salvo 2, reload 2.2 s, auto-engages)
    - new appearance
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`): `speed` = 65
- With [Advanced Terminal ABM](A5-Catalog-Technologies.md#advanced-terminal-abm-terminal_bm_defence_mk3) (`Terminal_BM_Defence_Mk3`):
    - weapon config “default” becomes:
        - [Terminal ABM](A2-Catalog-Missiles.md#terminal-abm-terminal-abm) (`Terminal ABM`) (unlimited, salvo 2, reload 1.5 s, auto-engages)
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`): `speed` = 75

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Terminal ABM](A2-Catalog-Missiles.md#terminal-abm-terminal-abm): [Hit-To-Kill Terminal ABM](A5-Catalog-Technologies.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2), [Advanced Terminal ABM](A5-Catalog-Technologies.md#advanced-terminal-abm-terminal_bm_defence_mk3)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Hit-To-Kill Terminal ABM”](#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`) (active after researching [Hit-To-Kill Terminal ABM](A5-Catalog-Technologies.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2) (`Terminal_BM_Defence_Mk2`)): enemy weapons (117): `canbeintercepted` ×1.3
- [“Advanced Terminal ABM”](#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`) (active after researching [Advanced Terminal ABM](A5-Catalog-Technologies.md#advanced-terminal-abm-terminal_bm_defence_mk3) (`Terminal_BM_Defence_Mk3`)): enemy weapons (117): `canbeintercepted` ×1.3
- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_invulnerable) (`EMP_Defence_Invulnerable`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Terminal Ballistic Missile Defences”](#terminal-ballistic-missile-defences-terminal_abm_no_target_decoy_modifier) (`Terminal_ABM_No_Target_Decoy_Modifier`) (always active): enemy [Decoy Warhead](A2-Catalog-Missiles.md#decoy-warhead-false-icbm-warhead): `canbeintercepted` = 0

### Heavy Bomb Truck (`Heavy_Bomb_Truck`)

<!-- img:unit Units/Images/Icons/Ground/Bomb_Truck_Heavy.png -->

A civilian tractor-trailer truck designed to blend in with regular vehicle traffic. The truck has been modified to carry and conceal a high-yield nuclear bomb, and can discreetly drive to a target site before detonating. Effective at surprising the enemy and as a psychological weapon, but not potent or cost-effective enough to warrant being a main strategy.  
\+ Only detected when very close to enemy units.  
\+ Can be cost effective if successful.  
\+ Offers an element of surprise.  
\- Completely defenseless.  
\- Self-destructs upon attacking.  
\- Extremely slow.  
\- Not effective as a main strategy.

**How to get it:** [Tractor Trailer Suicide Trucks](A5-Catalog-Technologies.md#tractor-trailer-suicide-trucks-heavy_svbied) (`Heavy_SVBIED`) — technology `U_Bomb_Truck_Heavy`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 0.75 |
| `speed` | 45 |
| `size` | 0.075 |
| `turnspeed` | 10 |
| `productioncost` | 6.5 |

**Weapons** (switchable configurations):

- *C4 (default)*: [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)
- *Light 100kt Bomb*: [Light 100 Kiloton Bomb](A2-Catalog-Missiles.md#light-100-kiloton-bomb-100kt_nuke_light) (`100kt_nuke_light`) (×1)
- *Light 250kt Bomb*: [Light 250 Kiloton Bomb](A2-Catalog-Missiles.md#light-250-kiloton-bomb-250kt_nuke_light) (`250kt_nuke_light`) (×1)
- *Light 500kt Bomb*: [Light 500 kiloton Bomb](A2-Catalog-Missiles.md#light-500-kiloton-bomb-500kt-nuke_light) (`500kt nuke_light`) (×1)
- *Light Megaton Bomb*: [Light Megaton Bomb](A2-Catalog-Missiles.md#light-megaton-bomb-1m-nuke_light) (`1M nuke_light`) (×1)
- *Light 5 Megaton Bomb*: [Light 5M Pure Fusion Bomb](A2-Catalog-Missiles.md#light-5m-pure-fusion-bomb-5m-nuke_light) (`5M nuke_light`) (×1)
- *Light 500kt Cobalt Bomb*: [Light 500kt Cobalt Bomb](A2-Catalog-Missiles.md#light-500kt-cobalt-bomb-500kt-light-cobalt-bomb) (`500kt Light Cobalt Bomb`) (×1)
- *Light 500kt Enhanced Salted Bomb*: [Light 500kt Salted Bomb](A2-Catalog-Missiles.md#light-500kt-salted-bomb-500kt-light-salt-bomb) (`500kt Light Salt Bomb`) (×1)
- *Heavy 500 Kiloton*: [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy) (`500kt nuke_heavy`) (×1)
- *Heavy 10 Megaton*: [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy) (`10M nuke_heavy`) (×1)
- *Heavy 25 Megaton*: [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy) (`25M nuke_heavy`) (×1)
- *Heavy 50 Megaton*: [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy) (`50M nuke_heavy`) (×1)
- *Heavy 100 Megaton*: [Heavy 100M Fusion Bomb](A2-Catalog-Missiles.md#heavy-100m-fusion-bomb-100m-nuke_heavy) (`100M nuke_heavy`) (×1)
- *Heavy Cobalt Bomb*: [10 Megaton Cobalt Bomb](A2-Catalog-Missiles.md#10-megaton-cobalt-bomb-cobalt_bomb) (`Cobalt_Bomb`) (×1)
- *Heavy Enhanced Salted Bomb*: [10 Megaton Salted Bomb](A2-Catalog-Missiles.md#10-megaton-salted-bomb-salted_bomb) (`Salted_Bomb`) (×1)
- *Tularemia Bomb*:
    - [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb) (`Bioweapon_bomb`) (×1, principal)
    - [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)
- *Smallpox Bomb*:
    - [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb) (`Improved_Bioweapon_bomb`) (×1, principal)
    - [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)
- *Ebola Bomb*:
    - [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb) (`Advanced_Bioweapon_bomb`) (×1, principal)
    - [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)
- *Medusa Fever Bomb*:
    - [EMeVHF-24 Bomb](A2-Catalog-Missiles.md#emevhf-24-bomb-engineered_bioweapon_bomb) (`Engineered_Bioweapon_bomb`) (×1, principal)
    - [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb) (`Car Bomb`) (×1)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Car Bomb](A2-Catalog-Missiles.md#car-bomb-car-bomb): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons)
- [Light 250 Kiloton Bomb](A2-Catalog-Missiles.md#light-250-kiloton-bomb-250kt_nuke_light): [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads)
- [Light 500 kiloton Bomb](A2-Catalog-Missiles.md#light-500-kiloton-bomb-500kt-nuke_light): [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [Light Megaton Bomb](A2-Catalog-Missiles.md#light-megaton-bomb-1m-nuke_light): [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [Light 500kt Cobalt Bomb](A2-Catalog-Missiles.md#light-500kt-cobalt-bomb-500kt-light-cobalt-bomb): [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy): [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb)
- [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy): [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads)
- [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy): [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy): [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [10 Megaton Cobalt Bomb](A2-Catalog-Missiles.md#10-megaton-cobalt-bomb-cobalt_bomb): [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb): [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2)
- [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb): [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3)
- [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb): [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Covert Unit”](#covert-unit-covert_unit) (`Covert_Unit`) (always active):
    - enemy [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces), [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `range` ×0
    - enemy [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision): `range` ×0.75
    - enemy sensors (20): `range` ×0
    - enemy [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): `range` ×1
    - enemy [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance): `range` ×0.4
    - enemy [Periscope](A4-Catalog-Radars.md#periscope-periscope): `range` ×0.5

**Other traits:** `Bomb_Truck`.

### Mobile Defence Laser (`Mobile_ABM_Laser`)

<!-- img:unit Units/Images/Icons/Ground/ABM_Laser_Truck.png -->

A vehicle armed with a high-powered laser capable of destroying incoming ballistic missiles. Extremely effective within its range against single warheads, but with limited range. Excellent against missiles that are usually difficult to intercept, like hypersonic glide vehicles. Best used in conjunction with other missile defences.  
\+ Very effective against hypersonic weapons.  
\+ High interception rate against all targets.  
\+ Air-deployable from transport planes.  
\- Very limited range.  
\- Limited ability to engage multiple targets.

**How to get it:** [Terminal Defence Lasers](A5-Catalog-Technologies.md#terminal-defence-lasers-terminal_defence_laser) (`Terminal_Defence_Laser`) — technology `U_Laser_Truck`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2.5 |
| `speed` | 40 |
| `size` | 0.07 |
| `turnspeed` | 7.5 |
| `productioncost` | 8 |
| `attackdelay` | 0.01 s |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*: [Terminal Defence Laser](A2-Catalog-Missiles.md#terminal-defence-laser-terminal-abm-laser) (`Terminal ABM Laser`) (unlimited, reload 0.7 s, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km).

**Upgrades:**

- With [Early Infantry Fighting Vehicles](A5-Catalog-Technologies.md#early-infantry-fighting-vehicles-army_mech_mk2) (`Army_Mech_Mk2`): `speed` = 45
- With [Modernized Armoured Vehicles](A5-Catalog-Technologies.md#modernized-armoured-vehicles-army_mech_mk3) (`Army_Mech_Mk3`): `speed` = 55
- With [Armoured Mid-life Upgrades](A5-Catalog-Technologies.md#armoured-mid-life-upgrades-army_mech_mk4) (`Army_Mech_Mk4`): `speed` = 65
- With [Novel Fighting Vehicle Concepts](A5-Catalog-Technologies.md#novel-fighting-vehicle-concepts-army_mech_mk5) (`Army_Mech_Mk5`): `speed` = 75

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_invulnerable) (`EMP_Defence_Invulnerable`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Terminal Ballistic Missile Defences”](#terminal-ballistic-missile-defences-terminal_abm_no_target_decoy_modifier) (`Terminal_ABM_No_Target_Decoy_Modifier`) (always active): enemy [Decoy Warhead](A2-Catalog-Missiles.md#decoy-warhead-false-icbm-warhead): `canbeintercepted` = 0

## Surface ships

### Carrier (`Carrier`)

<!-- img:upgrades Units/Images/Icons/Naval/Carrier_1.png=Base|Units/Images/Icons/Naval/Carrier_2.png=Missile-Armed Warships|Units/Images/Icons/Naval/Carrier_3.png=Improved Warships|Units/Images/Icons/Naval/Carrier_4.png=Advanced Warship Armaments|Units/Images/Icons/Naval/Carrier_5.png=Experimental Stealth Warships -->

An aircraft carrier (or just carrier) is a large warship designed to carry combat aircraft and helicopters. Carriers have built-in runways and facilities to house and launch aircraft, and are crucial to providing air support for naval and marine operations. Because of their immense size, prestige and tactical and strategic importance, carriers have often been designated as the flagships for naval operations in the post-WWII environment. Carriers provide the ability to project air power anywhere in the world without relying on local facilities, and dramatically amplify the force projection capabilities of their fleets.  
\+ Can carry multirole aircraft.  
\+ Can carry naval and special ops helicopters.  
\+ Can store lightweight nuclear bombs.  
\- Limited personal defences.  
\- Vulnerable to submarines.  
\- Expensive.

**How to get it:** available from the start — technology `U_Carrier`.

| Stat | Base value |
|---|---|
| `type` | Naval |
| `power` | 40 |
| `speed` | 35 |
| `size` | 0.4 |
| `turnspeed` | 5 |
| `productioncost` | 12 |
| `selfdestructtime` | 30 s |

**Weapons**:

- *default*:
    - [Light SAM](A2-Catalog-Missiles.md#light-sam-light-sam) (`Light SAM`) (unlimited, salvo 2, reload 2 s, auto-engages, off by default)
    - [Light Missile Defence SAM](A2-Catalog-Missiles.md#light-missile-defence-sam-light-sam-md) (`Light SAM MD`) (unlimited, salvo 2, reload 2 s, auto-engages, off by default)
    - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, salvo 2, reload 0.2 s, auto-engages, off by default)
    - [Laser CIWS](A2-Catalog-Missiles.md#laser-ciws-laser-ciws) (`Laser CIWS`) (unlimited, salvo 2, reload 0.7 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km), [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) (525 km).

**Aircraft hosted:** 30 × [Multirole Attacker](#multirole-attacker-attack), 6 × [EW Aircraft](#ew-aircraft-ew_aircraft), 2 × [Carrier AWACS](#carrier-awacs-naval-awacs), 4 × [Naval Helicopter](#naval-helicopter-navy_helicopter), 2 × [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter).

**Upgrades:**

- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Missile-Armed Warships](A5-Catalog-Technologies.md#missile-armed-warships-missile_warships) (`Missile_Warships`):
    - new appearance
    - `size` = 0.38
    - `speed` = 40
    - `turnspeed` = 5.5
    - `power` = 45
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Improved Warships](A5-Catalog-Technologies.md#improved-warships-improved_warships) (`Improved_Warships`):
    - new appearance
    - `size` = 0.36
    - `speed` = 45
    - `turnspeed` = 6
    - `power` = 50
- With [Modernized Ship Hulls](A5-Catalog-Technologies.md#modernized-ship-hulls-enhanced_warships) (`Enhanced_Warships`):
    - `size` = 0.34
    - `speed` = 50
    - `turnspeed` = 6.5
    - `power` = 55
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`):
    - new appearance
    - `size` = 0.32
    - `speed` = 60
    - `turnspeed` = 7
    - `power` = 60
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`):
    - new appearance
    - `size` = 0.3
    - `speed` = 65
    - `turnspeed` = 7.5
    - `power` = 65

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Light SAM](A2-Catalog-Missiles.md#light-sam-light-sam): [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2)
- [Light Missile Defence SAM](A2-Catalog-Missiles.md#light-missile-defence-sam-light-sam-md): [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak): [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6)

**Sensor vulnerabilities:**

- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Novel Stealth Applications”](#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`) (active after researching [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`)): enemy sensors (12): `range` ×0.7
- [“Advanced Stealth”](#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`) (active after researching [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`) + [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`)): enemy sensors (12): `range` ×0.75
- [“Naval Target Damage Penalty”](#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05

### Cruiser (`Cruiser`)

<!-- img:upgrades Units/Images/Icons/Naval/Cruiser_1.png=Base|Units/Images/Icons/Naval/Cruiser_2.png=Missile-Armed Warships|Units/Images/Icons/Naval/Cruiser_3.png=Improved Warships|Units/Images/Icons/Naval/Cruiser_4.png=Modernized Ship Hulls|Units/Images/Icons/Naval/Cruiser_5.png=Experimental Stealth Warships -->

A cruiser is a large, very heavily armed surface warship. After battleships became obsolete and aircraft carriers became the new standard for capital ships, cruisers were left as the next heaviest surface combatants and also the most capable that didn't rely on air power. The exact role and design of a cruiser varies from navy to navy, but cruisers generally carry large numbers of cruise missiles and heavy guns, giving them extensive anti-surface and land attack capabilities, making them very capable at defeating other warships and destroying ground targets further inland with massive saturation attacks.  
\+ Powerful cruise missile armament.  
\+ Very effective against enemy ships.  
\+ Good at attacking land targets.  
\+ Can carry nuclear cruise missiles.  
\+ Has some anti-missile capabilities.  
\- Vulnerable to submarines.  
\- Expensive.

**How to get it:** available from the start — technology `U_Cruiser`.

| Stat | Base value |
|---|---|
| `type` | Naval |
| `power` | 25 |
| `speed` | 40 |
| `size` | 0.3 |
| `turnspeed` | 5 |
| `productioncost` | 26 |
| `selfdestructtime` | 20 s |

**Weapons**:

- *default*:
    - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, salvo 2, reload 2 s, auto-engages)
    - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 5 s, auto-engages)
    - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.4 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) (200 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km), [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) (525 km), [Space radar (Naval Space Radar)](A4-Catalog-Radars.md#space-radar-naval-space-radar-naval-space_radar) (500 km), [Overhorizon Radar (Naval Small Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-naval-small-over-horizon-naval_small_over_horizon) (750 km).

**Upgrades:**

- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Missile-Armed Warships](A5-Catalog-Technologies.md#missile-armed-warships-missile_warships) (`Missile_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, salvo 2, reload 2 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 6 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 5 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.4 s, auto-engages, off by default)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, reload 5 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, reload 5 s, auto-engages, off by default)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, reload 6.7 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×10 000, reload 13.3 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×10 000, reload 13.3 s, off by default)
    - new appearance
    - `size` = 0.275
    - `speed` = 45
    - `turnspeed` = 5.5
    - `power` = 28
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Improved Warships](A5-Catalog-Technologies.md#improved-warships-improved_warships) (`Improved_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, salvo 2, reload 2 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, reload 4 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, reload 4 s, auto-engages, off by default)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, reload 6 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×10 000, reload 12 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×10 000, reload 12 s, off by default)
    - new appearance
    - `size` = 0.25
    - `speed` = 50
    - `turnspeed` = 6
    - `power` = 32
- With [Modernized Ship Hulls](A5-Catalog-Technologies.md#modernized-ship-hulls-enhanced_warships) (`Enhanced_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, salvo 2, reload 2 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 4, reload 4 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 4, reload 4 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, reload 4 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, reload 4 s, auto-engages, off by default)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, reload 6 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×10 000, salvo 2, reload 11 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×10 000, salvo 2, reload 11 s, off by default)
    - new appearance
    - `size` = 0.225
    - `speed` = 55
    - `turnspeed` = 6.5
    - `power` = 36
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, salvo 2, reload 2 s, auto-engages)
        - [Railgun](A2-Catalog-Missiles.md#railgun-railgun) (`Railgun`) (unlimited, salvo 2, reload 2 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 4, reload 4 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 4, reload 4 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
        - [Laser CIWS](A2-Catalog-Missiles.md#laser-ciws-laser-ciws) (`Laser CIWS`) (unlimited, reload 0.7 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, reload 4 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, reload 4 s, auto-engages, off by default)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, reload 6 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×10 000, salvo 2, reload 11 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×10 000, salvo 2, reload 11 s, off by default)
        - [ASAT](A2-Catalog-Missiles.md#asat-asat) (`ASAT`) (×3, off by default)
        - [Terminal ABM](A2-Catalog-Missiles.md#terminal-abm-terminal-abm) (`Terminal ABM`) (unlimited, salvo 2, reload 4 s, auto-engages, off by default)
    - `size` = 0.2
    - `speed` = 65
    - `turnspeed` = 7
    - `power` = 38
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, salvo 2, reload 1.7 s, auto-engages)
        - [Railgun](A2-Catalog-Missiles.md#railgun-railgun) (`Railgun`) (unlimited, salvo 2, reload 1.7 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 4, reload 3.3 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 4, reload 3.3 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Anti-Air Laser](A2-Catalog-Missiles.md#anti-air-laser-aa-laser) (`AA Laser`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
        - [Laser CIWS](A2-Catalog-Missiles.md#laser-ciws-laser-ciws) (`Laser CIWS`) (unlimited, reload 0.7 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, reload 4 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, reload 4 s, auto-engages, off by default)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, reload 5.3 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×10 000, salvo 2, reload 10 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×10 000, salvo 2, reload 10 s, off by default)
        - [ASAT](A2-Catalog-Missiles.md#asat-asat) (`ASAT`) (×3, off by default)
        - [Terminal ABM](A2-Catalog-Missiles.md#terminal-abm-terminal-abm) (`Terminal ABM`) (unlimited, salvo 2, reload 3.3 s, auto-engages, off by default)
        - [Terminal Defence Laser](A2-Catalog-Missiles.md#terminal-defence-laser-terminal-abm-laser) (`Terminal ABM Laser`) (unlimited, reload 1 s, auto-engages, off by default)
    - new appearance
    - `size` = 0.18
    - `speed` = 70
    - `turnspeed` = 7.5
    - `power` = 40

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [SSM](A2-Catalog-Missiles.md#ssm-ssm): [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles), [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles), [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles), [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5), [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons)
- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2), [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3), [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4), [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak): [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6)
- [Space radar (Naval Space Radar)](A4-Catalog-Radars.md#space-radar-naval-space-radar-naval-space_radar): [Actively Tracked Space Radar](A5-Catalog-Technologies.md#actively-tracked-space-radar-space_radar_mk2), [High-Fidelity ASAT Space Radar](A5-Catalog-Technologies.md#high-fidelity-asat-space-radar-space_radar_mk3), [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4)

**Sensor vulnerabilities:**

- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Space radar (Naval Space Radar)](A4-Catalog-Radars.md#space-radar-naval-space-radar-naval-space_radar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Space radar (Naval Space Radar)](A4-Catalog-Radars.md#space-radar-naval-space-radar-naval-space_radar) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Overhorizon Radar (Naval Small Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-naval-small-over-horizon-naval_small_over_horizon) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Overhorizon Radar (Naval Small Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-naval-small-over-horizon-naval_small_over_horizon) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Novel Stealth Applications”](#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`) (active after researching [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`)): enemy sensors (12): `range` ×0.7
- [“Advanced Stealth”](#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`) (active after researching [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`) + [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`)): enemy sensors (12): `range` ×0.75
- [“Naval Target Damage Penalty”](#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Hit-To-Kill Terminal ABM”](#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`) (active after researching [Hit-To-Kill Terminal ABM](A5-Catalog-Technologies.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2) (`Terminal_BM_Defence_Mk2`)): enemy weapons (117): `canbeintercepted` ×1.3
- [“Advanced Terminal ABM”](#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`) (active after researching [Advanced Terminal ABM](A5-Catalog-Technologies.md#advanced-terminal-abm-terminal_bm_defence_mk3) (`Terminal_BM_Defence_Mk3`)): enemy weapons (117): `canbeintercepted` ×1.3

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Terminal Ballistic Missile Defences”](#terminal-ballistic-missile-defences-terminal_abm_no_target_decoy_modifier) (`Terminal_ABM_No_Target_Decoy_Modifier`) (always active): enemy [Decoy Warhead](A2-Catalog-Missiles.md#decoy-warhead-false-icbm-warhead): `canbeintercepted` = 0

**Other traits:** `Debuffed_Sonar`.

### Destroyer (`Destroyer`)

<!-- img:upgrades Units/Images/Icons/Naval/Destroyer_1.png=Base|Units/Images/Icons/Naval/Destroyer_2.png=Missile-Armed Warships|Units/Images/Icons/Naval/Destroyer_3.png=Improved Warships|Units/Images/Icons/Naval/Destroyer_4.png=Modernized Ship Hulls|Units/Images/Icons/Naval/Destroyer_5.png=Experimental Stealth Warships -->

Although the exact terminology varies by navy, a destroyer is a large, fast and maneuverable surface warship designed to destroy other surface combatants. As naval warfare has evolved, the roles of a destroyer have changed to include air defence, anti-submarine warfare, anti-surface warfare and missile defence. Regardless of how it is defined, destroyers are often used on autonomous patrols or as escorts to defend and support larger warships, like carriers and cruisers.  
\+ Fast for a warship.  
\+ Heightened anti-submarine capability.  
\+ Good anti-air/anti-missile capabilities.  
\- Limited firepower against enemy ships.  
\- No nuclear weapon options.

**How to get it:** available from the start — technology `U_Destroyer`.

| Stat | Base value |
|---|---|
| `type` | Naval |
| `power` | 12 |
| `speed` | 45 |
| `size` | 0.25 |
| `turnspeed` | 4.5 |
| `productioncost` | 15 |
| `selfdestructtime` | 15 s |

**Weapons**:

- *default*:
    - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, reload 2 s, auto-engages)
    - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) (200 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km), [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) (525 km).

**Upgrades:**

- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Missile-Armed Warships](A5-Catalog-Technologies.md#missile-armed-warships-missile_warships) (`Missile_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, reload 2 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 6 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 6 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, reload 3.3 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, reload 3.3 s, auto-engages, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, reload 4 s, auto-engages)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.3 s, auto-engages, off by default)
    - new appearance
    - `size` = 0.225
    - `speed` = 50
    - `turnspeed` = 5.5
    - `power` = 13.5
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Improved Warships](A5-Catalog-Technologies.md#improved-warships-improved_warships) (`Improved_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, reload 2 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 4 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 4 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, reload 2.7 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, reload 2.7 s, auto-engages, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, reload 3 s, auto-engages)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
    - new appearance
    - `size` = 0.2
    - `speed` = 55
    - `turnspeed` = 6
    - `power` = 15
- With [Modernized Ship Hulls](A5-Catalog-Technologies.md#modernized-ship-hulls-enhanced_warships) (`Enhanced_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, reload 2 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 6 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, salvo 2, reload 2.3 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, salvo 2, reload 2.3 s, auto-engages, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, salvo 2, reload 3 s, auto-engages)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
    - new appearance
    - `size` = 0.18
    - `speed` = 60
    - `turnspeed` = 6.5
    - `power` = 16.5
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, reload 2 s, auto-engages)
        - [Railgun](A2-Catalog-Missiles.md#railgun-railgun) (`Railgun`) (unlimited, reload 2 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 6 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Anti-Air Laser](A2-Catalog-Missiles.md#anti-air-laser-aa-laser) (`AA Laser`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, salvo 2, reload 2.3 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, salvo 2, reload 2.3 s, auto-engages, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, salvo 2, reload 3 s, auto-engages)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
        - [Laser CIWS](A2-Catalog-Missiles.md#laser-ciws-laser-ciws) (`Laser CIWS`) (unlimited, reload 0.7 s, auto-engages, off by default)
        - [Terminal ABM](A2-Catalog-Missiles.md#terminal-abm-terminal-abm) (`Terminal ABM`) (unlimited, salvo 2, reload 5 s, auto-engages, off by default)
    - `size` = 0.16
    - `speed` = 70
    - `turnspeed` = 7
    - `power` = 17
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`):
    - weapon config “default” becomes:
        - [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun) (`Ship Gun`) (unlimited, reload 1.7 s, auto-engages)
        - [Railgun](A2-Catalog-Missiles.md#railgun-railgun) (`Railgun`) (unlimited, reload 1.7 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 3 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old) (`AA Gun Old`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Anti-Air Laser](A2-Catalog-Missiles.md#anti-air-laser-aa-laser) (`AA Laser`) (unlimited, reload 0.3 s, auto-engages, off by default)
        - [Heavy SAM](A2-Catalog-Missiles.md#heavy-sam-sam) (`SAM`) (unlimited, salvo 2, reload 2 s, auto-engages, off by default)
        - [Heavy Missile Defence SAM](A2-Catalog-Missiles.md#heavy-missile-defence-sam-sam-md) (`SAM MD`) (unlimited, salvo 2, reload 2 s, auto-engages, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, auto-engages)
        - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, salvo 4, reload 3 s, auto-engages)
        - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
        - [Laser CIWS](A2-Catalog-Missiles.md#laser-ciws-laser-ciws) (`Laser CIWS`) (unlimited, reload 0.7 s, auto-engages, off by default)
        - [Terminal ABM](A2-Catalog-Missiles.md#terminal-abm-terminal-abm) (`Terminal ABM`) (unlimited, salvo 2, reload 4 s, auto-engages, off by default)
    - new appearance
    - `size` = 0.14
    - `speed` = 75
    - `turnspeed` = 7.5
    - `power` = 18

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5), [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons)
- [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): [Guided Torpedoes](A5-Catalog-Technologies.md#guided-torpedoes-guided_torpedoes), [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons), [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons), [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons), [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons)
- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2), [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3), [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4), [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak): [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6)

**Sensor vulnerabilities:**

- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Novel Stealth Applications”](#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`) (active after researching [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`)): enemy sensors (12): `range` ×0.7
- [“Advanced Stealth”](#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`) (active after researching [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`) + [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`)): enemy sensors (12): `range` ×0.75
- [“Naval Target Damage Penalty”](#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Antitorpedo”](#antitorpedo-antitorpedo) (`Antitorpedo`) (always active): enemy [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo), [Airdropped Torpedo](A2-Catalog-Missiles.md#airdropped-torpedo-air-dropped-torpedo): `precision` ×1.5
- [“Hit-To-Kill Terminal ABM”](#hit-to-kill-terminal-abm-terminal_bm_defence_mk2_modifier) (`Terminal_BM_Defence_Mk2_Modifier`) (active after researching [Hit-To-Kill Terminal ABM](A5-Catalog-Technologies.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2) (`Terminal_BM_Defence_Mk2`)): enemy weapons (117): `canbeintercepted` ×1.3
- [“Advanced Terminal ABM”](#advanced-terminal-abm-terminal_bm_defence_mk3_modifier) (`Terminal_BM_Defence_Mk3_Modifier`) (active after researching [Advanced Terminal ABM](A5-Catalog-Technologies.md#advanced-terminal-abm-terminal_bm_defence_mk3) (`Terminal_BM_Defence_Mk3`)): enemy weapons (117): `canbeintercepted` ×1.3

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Terminal Ballistic Missile Defences”](#terminal-ballistic-missile-defences-terminal_abm_no_target_decoy_modifier) (`Terminal_ABM_No_Target_Decoy_Modifier`) (always active): enemy [Decoy Warhead](A2-Catalog-Missiles.md#decoy-warhead-false-icbm-warhead): `canbeintercepted` = 0

### Landing Ship (`Landing_Ship`)

<!-- img:unit Units/Images/Icons/Naval/Landing_Ship.png -->

A transport ship used to carry military forces overseas. Armies can board transport ships by moving to them when they are close together and near the coastline. They can then be carried to an enemy coastline and deployed on land.  
\+ Can carry armies and combat engineers.  
\+ More survivable than air transports.  
\- Extremely vulnerable without an escort.  
\- No offensive weapons.

**How to get it:** available from the start — technology `U_Landing_Ship`.

| Stat | Base value |
|---|---|
| `type` | Naval |
| `power` | 30 |
| `speed` | 40 |
| `size` | 0.4 |
| `turnspeed` | 5 |
| `productioncost` | 4.5 |
| `selfdestructtime` | 20 s |

**Weapons**:

- *default*:
    - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, reload 0.2 s, auto-engages, off by default)
    - [Laser CIWS](A2-Catalog-Missiles.md#laser-ciws-laser-ciws) (`Laser CIWS`) (unlimited, reload 0.7 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Occupation Zone Finder](A4-Catalog-Radars.md#occupation-zone-finder-occupation-zone-finder) (130 km).

**Can transport:** [Army Division (Army Division)](#army-division-army-division-army_division), [Combat Engineers](#combat-engineers-combat_engineers), [AA Gun Site](#aa-gun-site-aa_site_old), [Coastal Missile Battery](#coastal-missile-battery-coastal), [Mobile SAM](#mobile-sam-mobile_sam), [Short-Wave Radar Vehicle](#short-wave-radar-vehicle-mobile_sw_radar), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [SRBM TEL Vehicle](#srbm-tel-vehicle-mobile_srbm), [MRBM TEL Vehicle](#mrbm-tel-vehicle-mobile_mrbm), [ICBM TEL Vehicle](#icbm-tel-vehicle-mobile_icbm), [Terminal ABM Site](#terminal-abm-site-terminal_abm), [Mobile Defence Laser](#mobile-defence-laser-mobile_abm_laser), [Bomb Truck](#bomb-truck-bomb_truck), [Heavy Bomb Truck](#heavy-bomb-truck-heavy_bomb_truck).

**Upgrades:**

- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Missile-Armed Warships](A5-Catalog-Technologies.md#missile-armed-warships-missile_warships) (`Missile_Warships`):
    - `size` = 0.38
    - `speed` = 45
    - `turnspeed` = 5.5
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Improved Warships](A5-Catalog-Technologies.md#improved-warships-improved_warships) (`Improved_Warships`):
    - `size` = 0.36
    - `speed` = 50
    - `turnspeed` = 6
    - `power` = 35
- With [Modernized Ship Hulls](A5-Catalog-Technologies.md#modernized-ship-hulls-enhanced_warships) (`Enhanced_Warships`):
    - `size` = 0.34
    - `speed` = 55
    - `turnspeed` = 6.5
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`):
    - `size` = 0.32
    - `speed` = 65
    - `turnspeed` = 7
    - `power` = 40
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`):
    - `size` = 0.3
    - `speed` = 70
    - `turnspeed` = 7.5
    - `power` = 45

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Naval Target Damage Penalty”](#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

### Naval Monitoring Station (`Naval_Monitoring_Station`)

<!-- img:unit Units/Images/Icons/Naval/Sea_Radar.png -->

A floating offshore facility used to detect enemy submarines and surface ships. Comes equipped with radar as well as sonar. Hosts a naval helicopter.  
\+ Can detect enemy submarines.  
\+ Can detect units on radar.  
\+ Can host naval helicopters.  
\+ Can use MANPADS and light AShMs.  
\+ Can use CIWS.  
\- Easy to hit and destroy.  
\- Limited offensive options.

**How to get it:** available from the start — technology `U_Naval_Radar_Station`.

| Stat | Base value |
|---|---|
| `type` | Naval |
| `power` | 10 |
| `size` | 0.6 |
| `productioncost` | 4.5 |
| `selfdestructtime` | 5 s |

**Weapons**:

- *default*:
    - [Light AShM](A2-Catalog-Missiles.md#light-ashm-light_ashm) (`Light_AShM`) (unlimited, reload 3 s, auto-engages, principal)
    - [ASROC](A2-Catalog-Missiles.md#asroc-asroc) (`ASROC`) (unlimited, reload 5 s, auto-engages)
    - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (unlimited, reload 2.5 s, auto-engages, off by default)
    - [CIWS](A2-Catalog-Missiles.md#ciws-ciws) (`CIWS`) (unlimited, salvo 2, reload 0.2 s, auto-engages, off by default)
    - [Laser CIWS](A2-Catalog-Missiles.md#laser-ciws-laser-ciws) (`Laser CIWS`) (unlimited, salvo 2, reload 0.7 s, auto-engages, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave) (550 km), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) (300 km), [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) (200 km), [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong) (950 km).

**Aircraft hosted:** 2 × [Naval Helicopter](#naval-helicopter-navy_helicopter).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Light AShM](A2-Catalog-Missiles.md#light-ashm-light_ashm): [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm), [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm), [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm), [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm), [Basic Laser Guidance](A5-Catalog-Technologies.md#basic-laser-guidance-basic_laser_guidance), [Advanced Laser Guidance](A5-Catalog-Technologies.md#advanced-laser-guidance-advanced_laser_guidance), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [ASROC](A2-Catalog-Missiles.md#asroc-asroc): [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons), [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons), [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons)
- [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Improved SAMs](A5-Catalog-Technologies.md#improved-sams-sam_mk2), [Advanced SAMs](A5-Catalog-Technologies.md#advanced-sams-sam_mk3), [Hypersonic Hybrid Guidance SAMs](A5-Catalog-Technologies.md#hypersonic-hybrid-guidance-sams-sam_mk4)
- [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2), [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3), [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4), [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5)
- [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong): [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6)

**Sensor vulnerabilities:**

- [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Torpedo Net Mod”](#torpedo-net-mod-torpedo_net_mod) (`Torpedo_Net_Mod`) (always active): enemy [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): `damage` ×0.35
- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

**Other traits:** `Mega_Sonar`.

### Resupply Ship (`Resupply_Ship`)

<!-- img:unit Units/Images/Icons/Naval/Resupply_Ship.png -->

A ship designed to replenish the supplies and equipment of ships away from port. Units within the resupply radius of this ship will slowly recover from damage and can refill their storage as if they were in friendly territory.  
\+ Repairs friendly units.  
\+ Can rearm units with nuclear weapons.  
\+ Good for supporting submarines and carriers.  
\- Not very fast.  
\- Completely defenseless when alone.  
\- Big, easy to hit and fragile.

**How to get it:** available from the start — technology `U_Resupply_Ship`.

| Stat | Base value |
|---|---|
| `type` | Naval |
| `power` | 6 |
| `speed` | 35 |
| `size` | 0.25 |
| `turnspeed` | 5 |
| `productioncost` | 15 |
| `resupplyrange` | 225 |
| `repairrange` | 225 |
| `selfdestructtime` | 15 s |

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Resupply Range (Resupply Range)](A4-Catalog-Radars.md#resupply-range-resupply-range-resupply-range) (225 km).

**Upgrades:**

- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Missile-Armed Warships](A5-Catalog-Technologies.md#missile-armed-warships-missile_warships) (`Missile_Warships`):
    - `size` = 0.24
    - `speed` = 40
    - `turnspeed` = 5.5
    - `power` = 6.5
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Improved Warships](A5-Catalog-Technologies.md#improved-warships-improved_warships) (`Improved_Warships`):
    - `size` = 0.23
    - `speed` = 45
    - `turnspeed` = 6
    - `power` = 7
- With [Modernized Ship Hulls](A5-Catalog-Technologies.md#modernized-ship-hulls-enhanced_warships) (`Enhanced_Warships`):
    - `size` = 0.22
    - `speed` = 50
    - `turnspeed` = 6.5
    - `power` = 8
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Warship Armaments](A5-Catalog-Technologies.md#advanced-warship-armaments-advanced_warships) (`Advanced_Warships`):
    - `size` = 0.21
    - `speed` = 60
    - `turnspeed` = 7
    - `power` = 9
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`):
    - `size` = 0.2
    - `speed` = 65
    - `turnspeed` = 7.5
    - `power` = 10

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Naval Target Damage Penalty”](#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

## Submarines

### Attack Submarine (Submarine) (`Submarine`)

<!-- img:upgrades Units/Images/Icons/Naval/Submarine_1.png=Base|Units/Images/Icons/Naval/Submarine_2.png=Nuclear Submarines|Units/Images/Icons/Naval/Submarine_3.png=Improved Submarines|Units/Images/Icons/Naval/Submarine_4.png=Advanced Submarines|Units/Images/Icons/Naval/Submarine_5.png=Experimental Submarines -->

A relatively small and fast submarine designed for anti-shipping missions. Attack submarines excel at destroying enemy ships and other submarines, are difficult to detect, and can more easily track enemy naval vessels from a distance without being noticed. They can also carry elite commandos and covertly deploy them overseas. However, they are also very expensive, and only have limited land attack capabilities, limiting their effectiveness outside of hunting enemy ships.  
\+ Can only be detected by sonar when submerged.  
\+ Very effective against enemy ships.  
\+ Good at finding enemy submarines.  
\+ Can deploy spec-ops teams.  
\+ Can carry nuclear anti-ship torpedoes.  
\- Limited use outside of anti-shipping.  
\- Must surface to use missiles.  
\- Very expensive.

**How to get it:** available from the start — technology `U_Submarine`.

| Stat | Base value |
|---|---|
| `type` | Subwater |
| `power` | 5 |
| `speed` | 40 |
| `size` | 0.2 |
| `turnspeed` | 5 |
| `productioncost` | 15 |
| `selfdestructtime` | 10 s |

**Weapons** (switchable configurations):

- *Conventional (default)*: [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 5 s, auto-engages)
- *Nuclear Armed (default)*: no weapons (a technology adds them)
- *Fusion Torpedo (default)*: no weapons (a technology adds them)

**Sensors:** [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) (200 km).

**Can transport:** [Spec-Ops Team](#spec-ops-team-spec_ops_team).

**Modes:**

- Submarine Surfaced (`Submarine_Surfaced`): `type` Naval

**Upgrades:**

- With [Nuclear Submarines](A5-Catalog-Technologies.md#nuclear-submarines-nuclear_submarine) (`Nuclear_Submarine`):
    - weapon config “Conventional” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 7 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 7 s, auto-engages)
    - new appearance
    - `size` = 0.19
    - `speed` = 45
    - `power` = 5.5
- With [Improved Submarines](A5-Catalog-Technologies.md#improved-submarines-improved_submarines) (`Improved_Submarines`):
    - weapon config “Conventional” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 4.5 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 6 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 6 s, auto-engages)
    - new appearance
    - `size` = 0.18
    - `speed` = 50
    - `power` = 6
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`):
    - weapon config “Nuclear Armed” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [Nuclear Torpedo](A2-Catalog-Missiles.md#nuclear-torpedo-nuclear-torpedo) (`Nuclear Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Nuclear Submarines](A5-Catalog-Technologies.md#nuclear-submarines-nuclear_submarine) (`Nuclear_Submarine`) + [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`):
    - weapon config “Nuclear Armed” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 7 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 7 s, auto-engages)
        - [Nuclear Torpedo](A2-Catalog-Missiles.md#nuclear-torpedo-nuclear-torpedo) (`Nuclear Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Improved Submarines](A5-Catalog-Technologies.md#improved-submarines-improved_submarines) (`Improved_Submarines`):
    - weapon config “Nuclear Armed” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 4.5 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 6 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 6 s, auto-engages)
        - [Nuclear Torpedo](A2-Catalog-Missiles.md#nuclear-torpedo-nuclear-torpedo) (`Nuclear Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Submarine Midlife Upgrades](A5-Catalog-Technologies.md#submarine-midlife-upgrades-enhanced_submarines) (`Enhanced_Submarines`):
    - weapon config “Conventional” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 6 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 6 s, auto-engages)
    - `size` = 0.17
    - `speed` = 55
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Submarine Midlife Upgrades](A5-Catalog-Technologies.md#submarine-midlife-upgrades-enhanced_submarines) (`Enhanced_Submarines`):
    - weapon config “Nuclear Armed” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 6 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 6 s, auto-engages)
        - [Nuclear Torpedo](A2-Catalog-Missiles.md#nuclear-torpedo-nuclear-torpedo) (`Nuclear Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Advanced Submarines](A5-Catalog-Technologies.md#advanced-submarines-advanced_submarines) (`Advanced_Submarines`):
    - weapon config “Conventional” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 4, reload 4 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 5 s, auto-engages)
    - new appearance
    - `size` = 0.16
    - `speed` = 60
    - `power` = 6.5
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Advanced Submarines](A5-Catalog-Technologies.md#advanced-submarines-advanced_submarines) (`Advanced_Submarines`):
    - weapon config “Nuclear Armed” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 4, reload 4 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [Nuclear Torpedo](A2-Catalog-Missiles.md#nuclear-torpedo-nuclear-torpedo) (`Nuclear Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Experimental Submarines](A5-Catalog-Technologies.md#experimental-submarines-experimental_submarines) (`Experimental_Submarines`):
    - weapon config “Conventional” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 4, reload 3.3 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 4 s, auto-engages)
    - new appearance
    - `size` = 0.15
    - `speed` = 70
    - `power` = 7
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Experimental Submarines](A5-Catalog-Technologies.md#experimental-submarines-experimental_submarines) (`Experimental_Submarines`):
    - weapon config “Nuclear Armed” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 4, reload 3.3 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [Nuclear Torpedo](A2-Catalog-Missiles.md#nuclear-torpedo-nuclear-torpedo) (`Nuclear Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`):
    - weapon config “Fusion Torpedo” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [Fusion Torpedo](A2-Catalog-Missiles.md#fusion-torpedo-fusion-torpedo) (`Fusion Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Nuclear Submarines](A5-Catalog-Technologies.md#nuclear-submarines-nuclear_submarine) (`Nuclear_Submarine`) + [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`):
    - weapon config “Fusion Torpedo” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 7 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 7 s, auto-engages)
        - [Fusion Torpedo](A2-Catalog-Missiles.md#fusion-torpedo-fusion-torpedo) (`Fusion Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Improved Submarines](A5-Catalog-Technologies.md#improved-submarines-improved_submarines) (`Improved_Submarines`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`):
    - weapon config “Fusion Torpedo” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 4.5 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 6 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 6 s, auto-engages)
        - [Fusion Torpedo](A2-Catalog-Missiles.md#fusion-torpedo-fusion-torpedo) (`Fusion Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Submarine Midlife Upgrades](A5-Catalog-Technologies.md#submarine-midlife-upgrades-enhanced_submarines) (`Enhanced_Submarines`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`):
    - weapon config “Fusion Torpedo” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 6 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 6 s, auto-engages)
        - [Fusion Torpedo](A2-Catalog-Missiles.md#fusion-torpedo-fusion-torpedo) (`Fusion Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Advanced Submarines](A5-Catalog-Technologies.md#advanced-submarines-advanced_submarines) (`Advanced_Submarines`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`):
    - weapon config “Fusion Torpedo” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 4, reload 4 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 5 s, auto-engages)
        - [Fusion Torpedo](A2-Catalog-Missiles.md#fusion-torpedo-fusion-torpedo) (`Fusion Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)
- With [Tactical Nuclear Weapons](A5-Catalog-Technologies.md#tactical-nuclear-weapons-tactical_nukes) (`Tactical_nukes`) + [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons) (`Improved_Underwater_Weapons`) + [Experimental Submarines](A5-Catalog-Technologies.md#experimental-submarines-experimental_submarines) (`Experimental_Submarines`) + [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon) (`Pure_Fusion_Weapon`):
    - weapon config “Fusion Torpedo” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 4, reload 3.3 s, auto-engages)
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 4 s, auto-engages)
        - [Fusion Torpedo](A2-Catalog-Missiles.md#fusion-torpedo-fusion-torpedo) (`Fusion Torpedo`) (×4, reload 13.3 s, auto-engages, off by default, principal)

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): [Guided Torpedoes](A5-Catalog-Technologies.md#guided-torpedoes-guided_torpedoes), [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons), [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons), [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons), [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons)
- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2), [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3), [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4), [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5)

**Sensor vulnerabilities:**

- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Naval Target Damage Penalty”](#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05
- [“Submarine Stealth”](#submarine-stealth-submarine_stealth) (`Submarine_Stealth`) (always active): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.8
- [“Sonar Quieting SSN 1”](#sonar-quieting-ssn-1-sonar_quieting_ssn_1) (`Sonar_Quieting_SSN_1`) (active after researching [Nuclear Submarines](A5-Catalog-Technologies.md#nuclear-submarines-nuclear_submarine) (`Nuclear_Submarine`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.95
- [“Sonar Quieting SSN 2”](#sonar-quieting-ssn-2-sonar_quieting_ssn_2) (`Sonar_Quieting_SSN_2`) (active after researching [Improved Submarines](A5-Catalog-Technologies.md#improved-submarines-improved_submarines) (`Improved_Submarines`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875
- [“Sonar Quieting SSN 3”](#sonar-quieting-ssn-3-sonar_quieting_ssn_3) (`Sonar_Quieting_SSN_3`) (active after researching [Submarine Midlife Upgrades](A5-Catalog-Technologies.md#submarine-midlife-upgrades-enhanced_submarines) (`Enhanced_Submarines`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875
- [“Sonar Quieting SSN 4”](#sonar-quieting-ssn-4-sonar_quieting_ssn_4) (`Sonar_Quieting_SSN_4`) (active after researching [Advanced Submarines](A5-Catalog-Technologies.md#advanced-submarines-advanced_submarines) (`Advanced_Submarines`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875
- [“Sonar Quieting SSN 5”](#sonar-quieting-ssn-5-sonar_quieting_ssn_5) (`Sonar_Quieting_SSN_5`) (active after researching [Experimental Submarines](A5-Catalog-Technologies.md#experimental-submarines-experimental_submarines) (`Experimental_Submarines`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

**Other traits:** `Mega_Sonar`.

### SSGN (SSGN) (`SSGN`)

<!-- img:upgrades Units/Images/Icons/Naval/SSGN_1.png=Base|Units/Images/Icons/Naval/SSGN_1.5.png=Nuclear Submarines|Units/Images/Icons/Naval/SSGN_2.png=Improved Submarines|Units/Images/Icons/Naval/SSGN_3.png=Advanced Submarines|Units/Images/Icons/Naval/SSGN_4.png=Experimental Submarines -->

Cruise missile submarines are larger than regular attack submarines and comparable to ballistic missile submarines. However, SSGNs, unlike SSBNs, do not carry long-range ballistic missiles. Instead, they are armed with an extensive arsenal of conventional cruise missiles, with the option to carry tactical nuclear weapons as well. This allows them to easily surface and destroy distant surface ships and inland military targets. However, they are not as capable of fighting other submarines as attack submarines, and they lack the firepower to destroy cities.  
\+ Powerful cruise missile armament.  
\+ Carries tactical nuclear weapons.  
\+ Can submerge for stealth and surprise attacks.  
\- Must surface to fire missiles, exposing itself.  
\- Limited underwater firepower.

**How to get it:** [Early Cruise Missiles](A5-Catalog-Technologies.md#early-cruise-missiles-cruise_missiles) (`Cruise_missiles`) + [SSGN](A5-Catalog-Technologies.md#ssgn-cruise_missile_submarine) (`Cruise_Missile_Submarine`) — technology `U_SSGN_Submarine`.

| Stat | Base value |
|---|---|
| `type` | Subwater |
| `power` | 6 |
| `speed` | 35 |
| `size` | 0.22 |
| `turnspeed` | 5 |
| `productioncost` | 16.5 |
| `selfdestructtime` | 30 s |

**Weapons**:

- *SSGN*:
    - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, reload 5.8 s, auto-engages)
    - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, reload 5.8 s, auto-engages)
    - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×10 000, reload 11.7 s, off by default)
    - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×10 000, reload 11.7 s, off by default)
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)

**Sensors:** [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) (200 km).

**Modes:**

- SSGN Surfaced (`SSGN_Surfaced`): `type` Naval

**Upgrades:**

- With [Nuclear Submarines](A5-Catalog-Technologies.md#nuclear-submarines-nuclear_submarine) (`Nuclear_Submarine`):
    - weapon config “SSGN” becomes:
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 2, reload 8 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 2, reload 8 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×1 000, reload 8 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×1 000, reload 8 s, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - new appearance
    - `size` = 0.21
    - `speed` = 40
    - `power` = 6.25
- With [Improved Submarines](A5-Catalog-Technologies.md#improved-submarines-improved_submarines) (`Improved_Submarines`):
    - weapon config “SSGN” becomes:
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 4, reload 8 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 4, reload 8 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×1 000, reload 8 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×1 000, reload 8 s, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - new appearance
    - `size` = 0.2
    - `speed` = 45
    - `power` = 6.5
- With [Submarine Midlife Upgrades](A5-Catalog-Technologies.md#submarine-midlife-upgrades-enhanced_submarines) (`Enhanced_Submarines`):
    - weapon config “SSGN” becomes:
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 4, reload 5.3 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 4, reload 5.3 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×1 000, salvo 2, reload 5.3 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×1 000, salvo 2, reload 5.3 s, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - `size` = 0.19
- With [Advanced Submarines](A5-Catalog-Technologies.md#advanced-submarines-advanced_submarines) (`Advanced_Submarines`):
    - weapon config “SSGN” becomes:
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 6, reload 5.3 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 6, reload 5.3 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×1 000, salvo 2, reload 5.3 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×1 000, salvo 2, reload 5.3 s, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, auto-engages)
    - new appearance
    - `size` = 0.18
    - `speed` = 55
    - `power` = 7
- With [Experimental Submarines](A5-Catalog-Technologies.md#experimental-submarines-experimental_submarines) (`Experimental_Submarines`):
    - weapon config “SSGN” becomes:
        - [SSM](A2-Catalog-Missiles.md#ssm-ssm) (`SSM`) (unlimited, salvo 8, reload 5 s, auto-engages)
        - [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile) (`Anti Ship Missile`) (unlimited, salvo 8, reload 5 s, auto-engages)
        - [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile) (`Nuclear Cruise Missile`) (×1 000, salvo 2, reload 5 s, off by default)
        - [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile) (`Fusion Cruise Missile`) (×1 000, salvo 2, reload 5 s, off by default)
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, salvo 2, auto-engages)
    - new appearance
    - `size` = 0.17
    - `speed` = 65
    - `power` = 7.5

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [SSM](A2-Catalog-Missiles.md#ssm-ssm): [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles), [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles), [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles), [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile): [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles), [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles), [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles), [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile): [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles), [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles), [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles), [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile): [Precision Cruise Missiles](A5-Catalog-Technologies.md#precision-cruise-missiles-improved_cruise_missiles), [Evasive Hybrid Guidance Cruise Missiles](A5-Catalog-Technologies.md#evasive-hybrid-guidance-cruise-missiles-enhanced_cruise_missiles), [Advanced Stand-Off Cruise Missiles](A5-Catalog-Technologies.md#advanced-stand-off-cruise-missiles-advanced_cruise_missiles), [Hypersonic Cruise Missiles](A5-Catalog-Technologies.md#hypersonic-cruise-missiles-experimental_cruise_missiles), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): [Guided Torpedoes](A5-Catalog-Technologies.md#guided-torpedoes-guided_torpedoes), [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons), [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons), [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons), [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons)
- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2), [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3), [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4), [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5)

**Sensor vulnerabilities:**

- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Naval Target Damage Penalty”](#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05
- [“Submarine Stealth Weak”](#submarine-stealth-weak-submarine_stealth_weak) (`Submarine_Stealth_Weak`) (always active): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.9
- [“Sonar Quieting SSGN 1”](#sonar-quieting-ssgn-1-sonar_quieting_ssgn_1) (`Sonar_Quieting_SSGN_1`) (active after researching [Nuclear Submarines](A5-Catalog-Technologies.md#nuclear-submarines-nuclear_submarine) (`Nuclear_Submarine`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.95
- [“Sonar Quieting SSGN 2”](#sonar-quieting-ssgn-2-sonar_quieting_ssgn_2) (`Sonar_Quieting_SSGN_2`) (active after researching [Improved Submarines](A5-Catalog-Technologies.md#improved-submarines-improved_submarines) (`Improved_Submarines`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875
- [“Sonar Quieting SSGN 3”](#sonar-quieting-ssgn-3-sonar_quieting_ssgn_3) (`Sonar_Quieting_SSGN_3`) (active after researching [Submarine Midlife Upgrades](A5-Catalog-Technologies.md#submarine-midlife-upgrades-enhanced_submarines) (`Enhanced_Submarines`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875
- [“Sonar Quieting SSGN 4”](#sonar-quieting-ssgn-4-sonar_quieting_ssgn_4) (`Sonar_Quieting_SSGN_4`) (active after researching [Advanced Submarines](A5-Catalog-Technologies.md#advanced-submarines-advanced_submarines) (`Advanced_Submarines`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875
- [“Sonar Quieting SSGN 5”](#sonar-quieting-ssgn-5-sonar_quieting_ssgn_5) (`Sonar_Quieting_SSGN_5`) (active after researching [Experimental Submarines](A5-Catalog-Technologies.md#experimental-submarines-experimental_submarines) (`Experimental_Submarines`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

**Other traits:** `Advanced_Sonar`.

### SSBN (SSBN) (`SSBN`)

<!-- img:upgrades Units/Images/Icons/Naval/SSBN_1.png=Base|Units/Images/Icons/Naval/SSBN_2.png=Improved SSBN|Units/Images/Icons/Naval/SSBN_3.png=Advanced SSBN|Units/Images/Icons/Naval/SSBN_4.png=Experimental SSBN -->

A nuclear-powered submarine armed with ballistic missiles. SSBNs are very concealable and can only be located by sonar, unless they surface or start firing. Their ability to keep moving makes them more survivable, allows them to attack from unexpected locations and gives them strategic flexibility. However, they are extremely expensive, not very fast and can be difficult to rearm if they are far away from friendly territory after attacking. They are very effective for surprise attacks or as a second-strike weapon.  
\+ Very concealable and easy to hide.  
\+ Mobility allows for strategic flexibility.  
\+ Good weapon range and payload.  
\- Extremely expensive.  
\- Can be difficult to rearm.  
\- Vulnerable if located.

**How to get it:** [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn) (`SSBN`) — technology `U_SSBN`.

| Stat | Base value |
|---|---|
| `type` | Subwater |
| `power` | 8 |
| `speed` | 40 |
| `size` | 0.25 |
| `turnspeed` | 5 |
| `productioncost` | 20 |
| `selfdestructtime` | 30 s |

**Weapons** (switchable configurations):

- *Disarmed (default)*: [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
- *100kt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [100 Kiloton SLBM](A2-Catalog-Missiles.md#100-kiloton-slbm-100kt_slbm) (`100kt_SLBM`) (×12, reload 18 s, principal)
- *250kt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [250 Kiloton SLBM](A2-Catalog-Missiles.md#250-kiloton-slbm-250kt_slbm) (`250kt_SLBM`) (×12, reload 18 s, principal)
- *500kt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [500 Kiloton SLBM](A2-Catalog-Missiles.md#500-kiloton-slbm-500kt_slbm) (`500kt_SLBM`) (×12, reload 18 s, principal)
- *1M SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [Megaton SLBM](A2-Catalog-Missiles.md#megaton-slbm-1m_slbm) (`1M_SLBM`) (×12, reload 18 s, principal)
- *5M SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [5 Megaton SLBM](A2-Catalog-Missiles.md#5-megaton-slbm-5m_fusion_slbm) (`5M_Fusion_SLBM`) (×12, reload 18 s, principal)
- *500kt Cobalt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [500kt Cobalt SLBM](A2-Catalog-Missiles.md#500kt-cobalt-slbm-500kt_cobalt_slbm) (`500kt_Cobalt_SLBM`) (×12, reload 18 s, principal)
- *500kt Enhanced Salted SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [500kt Salted SLBM](A2-Catalog-Missiles.md#500kt-salted-slbm-500kt_salt_slbm) (`500kt_Salt_SLBM`) (×12, reload 18 s, principal)
- *500kt EMP SLBM*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [500kt EMP SLBM](A2-Catalog-Missiles.md#500kt-emp-slbm-500kt_slbm_emp) (`500kt_SLBM_EMP`) (×12, reload 18 s, principal)
- *500kt Super EMP SLBM*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [500kt Super EMP SLBM](A2-Catalog-Missiles.md#500kt-super-emp-slbm-500kt_slbm_emp_super) (`500kt_SLBM_EMP_Super`) (×12, reload 18 s, principal)
- *3x100kt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [3x100kt MIRV SLBM](A2-Catalog-Missiles.md#3x100kt-mirv-slbm-3x100kt_slbm) (`3x100kt_SLBM`) (×12, reload 18 s, principal)
- *3x250kt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [3x250kt MIRV SLBM](A2-Catalog-Missiles.md#3x250kt-mirv-slbm-3x250kt_slbm) (`3x250kt_SLBM`) (×12, reload 18 s, principal)
- *6x250kt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [6x250kt MIRV SLBM](A2-Catalog-Missiles.md#6x250kt-mirv-slbm-6x250kt_slbm) (`6x250kt_SLBM`) (×12, reload 18 s, principal)
- *6x500kt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [6x500kt MIRV SLBM](A2-Catalog-Missiles.md#6x500kt-mirv-slbm-6x500kt_slbm) (`6x500kt_SLBM`) (×12, reload 18 s, principal)
- *8x500kt SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [8x500kt MIRV SLBM](A2-Catalog-Missiles.md#8x500kt-mirv-slbm-8x500kt_slbm) (`8x500kt_SLBM`) (×12, reload 18 s, principal)
- *8x1M SLBM (default)*:
    - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
    - [8x1M Pure Fusion MIRV SLBM](A2-Catalog-Missiles.md#8x1m-pure-fusion-mirv-slbm-8x1m_fusion_slbm) (`8x1M_Fusion_SLBM`) (×12, reload 18 s, principal)

**Sensors:** [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) (200 km).

**Modes:**

- SSBN Surfaced (`SSBN_Surfaced`): `type` Naval

**Upgrades:**

- With [Improved SSBN](A5-Catalog-Technologies.md#improved-ssbn-improved_ssbn) (`Improved_SSBN`):
    - weapon config “100kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [100 Kiloton SLBM](A2-Catalog-Missiles.md#100-kiloton-slbm-100kt_slbm) (`100kt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [250 Kiloton SLBM](A2-Catalog-Missiles.md#250-kiloton-slbm-250kt_slbm) (`250kt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500 Kiloton SLBM](A2-Catalog-Missiles.md#500-kiloton-slbm-500kt_slbm) (`500kt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “1M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [Megaton SLBM](A2-Catalog-Missiles.md#megaton-slbm-1m_slbm) (`1M_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “5M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [5 Megaton SLBM](A2-Catalog-Missiles.md#5-megaton-slbm-5m_fusion_slbm) (`5M_Fusion_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “500kt Cobalt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Cobalt SLBM](A2-Catalog-Missiles.md#500kt-cobalt-slbm-500kt_cobalt_slbm) (`500kt_Cobalt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “500kt Enhanced Salted SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Salted SLBM](A2-Catalog-Missiles.md#500kt-salted-slbm-500kt_salt_slbm) (`500kt_Salt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “500kt EMP SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt EMP SLBM](A2-Catalog-Missiles.md#500kt-emp-slbm-500kt_slbm_emp) (`500kt_SLBM_EMP`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “500kt Super EMP SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Super EMP SLBM](A2-Catalog-Missiles.md#500kt-super-emp-slbm-500kt_slbm_emp_super) (`500kt_SLBM_EMP_Super`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “3x100kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [3x100kt MIRV SLBM](A2-Catalog-Missiles.md#3x100kt-mirv-slbm-3x100kt_slbm) (`3x100kt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “3x250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [3x250kt MIRV SLBM](A2-Catalog-Missiles.md#3x250kt-mirv-slbm-3x250kt_slbm) (`3x250kt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “6x250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [6x250kt MIRV SLBM](A2-Catalog-Missiles.md#6x250kt-mirv-slbm-6x250kt_slbm) (`6x250kt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “6x500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [6x500kt MIRV SLBM](A2-Catalog-Missiles.md#6x500kt-mirv-slbm-6x500kt_slbm) (`6x500kt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “8x500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [8x500kt MIRV SLBM](A2-Catalog-Missiles.md#8x500kt-mirv-slbm-8x500kt_slbm) (`8x500kt_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - weapon config “8x1M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [8x1M Pure Fusion MIRV SLBM](A2-Catalog-Missiles.md#8x1m-pure-fusion-mirv-slbm-8x1m_fusion_slbm) (`8x1M_Fusion_SLBM`) (×16, salvo 2, reload 16 s, principal)
    - new appearance
    - `size` = 0.225
    - `speed` = 45
    - `power` = 8.5
- With [Advanced SSBN](A5-Catalog-Technologies.md#advanced-ssbn-advanced_ssbn) (`Advanced_SSBN`):
    - weapon config “100kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [100 Kiloton SLBM](A2-Catalog-Missiles.md#100-kiloton-slbm-100kt_slbm) (`100kt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [250 Kiloton SLBM](A2-Catalog-Missiles.md#250-kiloton-slbm-250kt_slbm) (`250kt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500 Kiloton SLBM](A2-Catalog-Missiles.md#500-kiloton-slbm-500kt_slbm) (`500kt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “1M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [Megaton SLBM](A2-Catalog-Missiles.md#megaton-slbm-1m_slbm) (`1M_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “5M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [5 Megaton SLBM](A2-Catalog-Missiles.md#5-megaton-slbm-5m_fusion_slbm) (`5M_Fusion_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “500kt Cobalt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Cobalt SLBM](A2-Catalog-Missiles.md#500kt-cobalt-slbm-500kt_cobalt_slbm) (`500kt_Cobalt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “500kt Enhanced Salted SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Salted SLBM](A2-Catalog-Missiles.md#500kt-salted-slbm-500kt_salt_slbm) (`500kt_Salt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “500kt EMP SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt EMP SLBM](A2-Catalog-Missiles.md#500kt-emp-slbm-500kt_slbm_emp) (`500kt_SLBM_EMP`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “500kt Super EMP SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Super EMP SLBM](A2-Catalog-Missiles.md#500kt-super-emp-slbm-500kt_slbm_emp_super) (`500kt_SLBM_EMP_Super`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “3x100kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [3x100kt MIRV SLBM](A2-Catalog-Missiles.md#3x100kt-mirv-slbm-3x100kt_slbm) (`3x100kt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “3x250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [3x250kt MIRV SLBM](A2-Catalog-Missiles.md#3x250kt-mirv-slbm-3x250kt_slbm) (`3x250kt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “6x250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [6x250kt MIRV SLBM](A2-Catalog-Missiles.md#6x250kt-mirv-slbm-6x250kt_slbm) (`6x250kt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “6x500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [6x500kt MIRV SLBM](A2-Catalog-Missiles.md#6x500kt-mirv-slbm-6x500kt_slbm) (`6x500kt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “8x500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [8x500kt MIRV SLBM](A2-Catalog-Missiles.md#8x500kt-mirv-slbm-8x500kt_slbm) (`8x500kt_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - weapon config “8x1M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [8x1M Pure Fusion MIRV SLBM](A2-Catalog-Missiles.md#8x1m-pure-fusion-mirv-slbm-8x1m_fusion_slbm) (`8x1M_Fusion_SLBM`) (×16, salvo 4, reload 16 s, principal)
    - new appearance
    - `size` = 0.2
    - `speed` = 55
    - `power` = 9
- With [Experimental SSBN](A5-Catalog-Technologies.md#experimental-ssbn-experimental_ssbn) (`Experimental_SSBN`):
    - weapon config “100kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [100 Kiloton SLBM](A2-Catalog-Missiles.md#100-kiloton-slbm-100kt_slbm) (`100kt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [250 Kiloton SLBM](A2-Catalog-Missiles.md#250-kiloton-slbm-250kt_slbm) (`250kt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500 Kiloton SLBM](A2-Catalog-Missiles.md#500-kiloton-slbm-500kt_slbm) (`500kt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “1M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [Megaton SLBM](A2-Catalog-Missiles.md#megaton-slbm-1m_slbm) (`1M_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “5M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [5 Megaton SLBM](A2-Catalog-Missiles.md#5-megaton-slbm-5m_fusion_slbm) (`5M_Fusion_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “500kt Cobalt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Cobalt SLBM](A2-Catalog-Missiles.md#500kt-cobalt-slbm-500kt_cobalt_slbm) (`500kt_Cobalt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “500kt Enhanced Salted SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Salted SLBM](A2-Catalog-Missiles.md#500kt-salted-slbm-500kt_salt_slbm) (`500kt_Salt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “500kt EMP SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt EMP SLBM](A2-Catalog-Missiles.md#500kt-emp-slbm-500kt_slbm_emp) (`500kt_SLBM_EMP`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “500kt Super EMP SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [500kt Super EMP SLBM](A2-Catalog-Missiles.md#500kt-super-emp-slbm-500kt_slbm_emp_super) (`500kt_SLBM_EMP_Super`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “3x100kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [3x100kt MIRV SLBM](A2-Catalog-Missiles.md#3x100kt-mirv-slbm-3x100kt_slbm) (`3x100kt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “3x250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [3x250kt MIRV SLBM](A2-Catalog-Missiles.md#3x250kt-mirv-slbm-3x250kt_slbm) (`3x250kt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “6x250kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [6x250kt MIRV SLBM](A2-Catalog-Missiles.md#6x250kt-mirv-slbm-6x250kt_slbm) (`6x250kt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “6x500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [6x500kt MIRV SLBM](A2-Catalog-Missiles.md#6x500kt-mirv-slbm-6x500kt_slbm) (`6x500kt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “8x500kt SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [8x500kt MIRV SLBM](A2-Catalog-Missiles.md#8x500kt-mirv-slbm-8x500kt_slbm) (`8x500kt_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - weapon config “8x1M SLBM” becomes:
        - [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo) (`Torpedo`) (unlimited, auto-engages)
        - [8x1M Pure Fusion MIRV SLBM](A2-Catalog-Missiles.md#8x1m-pure-fusion-mirv-slbm-8x1m_fusion_slbm) (`8x1M_Fusion_SLBM`) (×20, salvo 4, reload 10 s, principal)
    - new appearance
    - `size` = 0.175
    - `speed` = 65
    - `power` = 10

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): [Guided Torpedoes](A5-Catalog-Technologies.md#guided-torpedoes-guided_torpedoes), [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons), [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons), [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons), [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons)
- [100 Kiloton SLBM](A2-Catalog-Missiles.md#100-kiloton-slbm-100kt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [250 Kiloton SLBM](A2-Catalog-Missiles.md#250-kiloton-slbm-250kt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500 Kiloton SLBM](A2-Catalog-Missiles.md#500-kiloton-slbm-500kt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [Megaton SLBM](A2-Catalog-Missiles.md#megaton-slbm-1m_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [5 Megaton SLBM](A2-Catalog-Missiles.md#5-megaton-slbm-5m_fusion_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt Cobalt SLBM](A2-Catalog-Missiles.md#500kt-cobalt-slbm-500kt_cobalt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [500kt Salted SLBM](A2-Catalog-Missiles.md#500kt-salted-slbm-500kt_salt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt EMP SLBM](A2-Catalog-Missiles.md#500kt-emp-slbm-500kt_slbm_emp): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Super EMP Weapons](A5-Catalog-Technologies.md#super-emp-weapons-super_emp), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [500kt Super EMP SLBM](A2-Catalog-Missiles.md#500kt-super-emp-slbm-500kt_slbm_emp_super): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Specialized EMP Weapons](A5-Catalog-Technologies.md#specialized-emp-weapons-specialized_emp), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance), [MARV](A5-Catalog-Technologies.md#marv-marv)
- [3x100kt MIRV SLBM](A2-Catalog-Missiles.md#3x100kt-mirv-slbm-3x100kt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn), [MIRV](A5-Catalog-Technologies.md#mirv-mirv), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [3x250kt MIRV SLBM](A2-Catalog-Missiles.md#3x250kt-mirv-slbm-3x250kt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn), [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance)
- [6x250kt MIRV SLBM](A2-Catalog-Missiles.md#6x250kt-mirv-slbm-6x250kt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn), [Enhanced MIRVs](A5-Catalog-Technologies.md#enhanced-mirvs-improved_mirv), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [6x500kt MIRV SLBM](A2-Catalog-Missiles.md#6x500kt-mirv-slbm-6x500kt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn), [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons), [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light)
- [8x500kt MIRV SLBM](A2-Catalog-Missiles.md#8x500kt-mirv-slbm-8x500kt_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads), [Submarine Launched Ballistic Missile](A5-Catalog-Technologies.md#submarine-launched-ballistic-missile-slbm), [Basic SSBN](A5-Catalog-Technologies.md#basic-ssbn-ssbn), [Novel Light Ballistic Missiles](A5-Catalog-Technologies.md#novel-light-ballistic-missiles-novel_bm_light), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [8x1M Pure Fusion MIRV SLBM](A2-Catalog-Missiles.md#8x1m-pure-fusion-mirv-slbm-8x1m_fusion_slbm): [Solid Fuel Rocket Systems](A5-Catalog-Technologies.md#solid-fuel-rocket-systems-solid_fuel_rockets), [Penetration Aids](A5-Catalog-Technologies.md#penetration-aids-false_warheads)
- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2), [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3), [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4), [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5)

**Sensor vulnerabilities:**

- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Naval Target Damage Penalty”](#naval-target-damage-penalty-naval_target_damage_penalty) (`Naval_Target_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05
- [“Submarine Stealth Weak”](#submarine-stealth-weak-submarine_stealth_weak) (`Submarine_Stealth_Weak`) (always active): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.9
- [“Sonar Quieting SSBN 1”](#sonar-quieting-ssbn-1-sonar_quieting_ssbn_1) (`Sonar_Quieting_SSBN_1`) (always active): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.95
- [“Sonar Quieting SSBN 2”](#sonar-quieting-ssbn-2-sonar_quieting_ssbn_2) (`Sonar_Quieting_SSBN_2`) (active after researching [Improved SSBN](A5-Catalog-Technologies.md#improved-ssbn-improved_ssbn) (`Improved_SSBN`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875
- [“Sonar Quieting SSBN 3”](#sonar-quieting-ssbn-3-sonar_quieting_ssbn_3) (`Sonar_Quieting_SSBN_3`) (active after researching [Advanced SSBN](A5-Catalog-Technologies.md#advanced-ssbn-advanced_ssbn) (`Advanced_SSBN`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.766
- [“Sonar Quieting SSBN 4”](#sonar-quieting-ssbn-4-sonar_quieting_ssbn_4) (`Sonar_Quieting_SSBN_4`) (active after researching [Experimental SSBN](A5-Catalog-Technologies.md#experimental-ssbn-experimental_ssbn) (`Experimental_SSBN`)): enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

**Other traits:** `Advanced_Sonar`.

## Aircraft

### Air Transport (`Air_Transport`)

<!-- img:upgrades Units/Images/Icons/Airborne/Airlift_1.png=Base|Units/Images/Icons/Airborne/Airlift_2.png=Jet-Powered Heavy Airframes|Units/Images/Icons/Airborne/Airlift_3.png=High Efficiency Heavy Airframes|Units/Images/Icons/Airborne/Airlift_4.png=Blended Wing Airframes -->

Transport planes can be used to carry armies long distances by air and then deploy them on the ground. Moving an army to an army base that has transport planes will load that army onto a plane. The plane can then take off and drop the army on the ground anywhere within range.  
\+ Fastest way to transport armies.  
\+ Can also carry combat engineers.  
\- Vulnerable to anti-air weapons.  
\- Cannot transport all unit types.

**How to get it:** available from the start — technology `U_Air_Transport`.

**Built at / carried by:** [Army Base](#army-base-army_base).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 3 |
| `speed` | 400 |
| `range` | 5 000 |
| `size` | 0.2 |
| `turnspeed` | 4 |
| `maxelevation` | 20 |
| `productioncost` | 5 |

**Sensors:** [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision) (100 km), [Occupation Zone Finder](A4-Catalog-Radars.md#occupation-zone-finder-occupation-zone-finder) (130 km).

**Can transport:** [Army Division (Army Division)](#army-division-army-division-army_division), [Combat Engineers](#combat-engineers-combat_engineers), [AA Gun Site](#aa-gun-site-aa_site_old), [Coastal Missile Battery](#coastal-missile-battery-coastal), [Mobile SAM](#mobile-sam-mobile_sam), [Short-Wave Radar Vehicle](#short-wave-radar-vehicle-mobile_sw_radar), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [SRBM TEL Vehicle](#srbm-tel-vehicle-mobile_srbm), [Mobile Defence Laser](#mobile-defence-laser-mobile_abm_laser).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Jet-Powered Heavy Airframes](A5-Catalog-Technologies.md#jet-powered-heavy-airframes-heavy_airframe_1) (`Heavy_Airframe_1`):
    - new appearance
    - `speed` = 600
    - `turnspeed` = 6
    - `range` = 9 000
    - `power` = 3.6
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [High Efficiency Heavy Airframes](A5-Catalog-Technologies.md#high-efficiency-heavy-airframes-heavy_airframe_2) (`Heavy_Airframe_2`):
    - new appearance
    - `speed` = 750
    - `turnspeed` = 7.5
    - `range` = 12 000
    - `power` = 4.2
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Blended Wing Airframes](A5-Catalog-Technologies.md#blended-wing-airframes-heavy_airframe_3) (`Heavy_Airframe_3`):
    - new appearance
    - `speed` = 900
    - `size` = 0.15
    - `turnspeed` = 9
    - `range` = 18 000
    - `power` = 5

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

### Fighter (`Fighter`)

<!-- img:upgrades Units/Images/Icons/Airborne/Fighter_1.png=Base|Units/Images/Icons/Airborne/Fighter_2.png=2nd Generation Aircraft|Units/Images/Icons/Airborne/Fighter_3.png=3rd Generation Aircraft|Units/Images/Icons/Airborne/Fighter_4.png=4th Generation Aircraft|Units/Images/Icons/Airborne/Fighter_5.png=5th Generation Aircraft|Units/Images/Icons/Airborne/Fighter_6.png=6th Generation Aircraft -->

Fighters are relatively light fixed-wing aircraft designed and equipped for air-to-air combat. The small profile and flight characteristics of fighters make them excellent at destroying other planes while avoiding being shot down themselves. Although most fighters are capable of using air-to-ground weapons in some capacity, certain especially high-performing fighters are relegated almost exclusively to securing air superiority.  
\+ Excellent at destroying enemy aircraft.  
\+ More flexible than ground-based AA.  
\+ Fast response times.  
\- No ground attack capability.  
\- Relatively expendable.

**How to get it:** available from the start — technology `U_Fighter`.

**Built at / carried by:** [Air Base](#air-base-airport), [Tactical Airbase](#tactical-airbase-tactical_airbase), [Specialized Airbase](#specialized-airbase-specialized_airport).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 0.65 |
| `speed` | 700 |
| `range` | 2 400 |
| `size` | 0.05 |
| `turnspeed` | 9 |
| `maxelevation` | 20 |
| `productioncost` | 1 |

**Weapons**:

- *Air-To-Air*:
    - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 4 s, auto-engages)
    - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)

**Sensors:** [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air) (100 km), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision) (100 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [2nd Generation Aircraft](A5-Catalog-Technologies.md#2nd-generation-aircraft-generation_2_aircraft) (`Generation_2_Aircraft`):
    - new appearance
    - `speed` = 800
    - `turnspeed` = 10
    - `range` = 2 800
    - `power` = 0.75
    - weapon config “Air-To-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, reload 3.3 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft) (`Generation_3_Aircraft`):
    - new appearance
    - `size` = 0.04
    - `speed` = 950
    - `turnspeed` = 12
    - `range` = 3 250
    - `power` = 1
    - weapon config “Air-To-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×6, salvo 2, reload 2.7 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [4th Generation Aircraft](A5-Catalog-Technologies.md#4th-generation-aircraft-generation_4_aircraft) (`Generation_4_Aircraft`):
    - new appearance
    - `size` = 0.03
    - `speed` = 1 000
    - `turnspeed` = 15
    - `range` = 3 750
    - `power` = 1.2
    - weapon config “Air-To-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×8, salvo 2, reload 2 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [4.5+ Generation Aircraft](A5-Catalog-Technologies.md#45-generation-aircraft-generation_45_aircraft) (`Generation_4.5_Aircraft`):
    - `size` = 0.025
    - `speed` = 1 000
    - `turnspeed` = 15
    - `range` = 4 000
    - `power` = 1.4
    - weapon config “Air-To-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×8, salvo 2, reload 1.7 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`):
    - new appearance
    - `size` = 0.02
    - `speed` = 1 150
    - `turnspeed` = 18
    - `range` = 4 250
    - `power` = 1.6
    - weapon config “Air-To-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×8, salvo 2, reload 1.7 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`):
    - new appearance
    - `size` = 0.015
    - `speed` = 1 250
    - `turnspeed` = 20
    - `range` = 5 250
    - `power` = 1.8
    - weapon config “Air-To-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×12, salvo 3, reload 1.7 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Anti-Air Laser Weapons](A5-Catalog-Technologies.md#anti-air-laser-weapons-aa_laser) (`AA_Laser`) + [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`) + [Deadly Laser Weapons](A5-Catalog-Technologies.md#deadly-laser-weapons-offensive_laser_weapons) (`Offensive_Laser_Weapons`):
    - weapon config “Air-To-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×12, salvo 3, reload 1.7 s, auto-engages, principal)
        - [Aircraft Laser](A2-Catalog-Missiles.md#aircraft-laser-plane-laser) (`Plane Laser`) (unlimited, reload 0.3 s, auto-engages)

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [AAM](A2-Catalog-Missiles.md#aam-aam): [All-Aspect AAMs](A5-Catalog-Technologies.md#all-aspect-aams-aam_improved), [F&F Radar-Guided AAMs](A5-Catalog-Technologies.md#ff-radar-guided-aams-aam_enhanced), [Off-Boresight Ramjet AAMs](A5-Catalog-Technologies.md#off-boresight-ramjet-aams-aam_advanced), [Advanced Hybrid Guidance AAMs](A5-Catalog-Technologies.md#advanced-hybrid-guidance-aams-aam_experimental), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun): [2nd Generation Aircraft](A5-Catalog-Technologies.md#2nd-generation-aircraft-generation_2_aircraft), [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Stealth Technology”](#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`) (active after researching [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`)): enemy sensors (12): `range` ×0.6
- [“Advanced Stealth”](#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`) (active after researching [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`)): enemy sensors (12): `range` ×0.75
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

### Multirole Attacker (`Attack`)

<!-- img:upgrades Units/Images/Icons/Airborne/Multirole_1.png=Base|Units/Images/Icons/Airborne/Multirole_2.png=2nd Generation Aircraft|Units/Images/Icons/Airborne/Multirole_3.png=3rd Generation Aircraft|Units/Images/Icons/Airborne/Multirole_4.png=4th Generation Aircraft|Units/Images/Icons/Airborne/Multirole_5.png=5th Generation Aircraft|Units/Images/Icons/Airborne/Multirole_6.png=6th Generation Aircraft -->

Multirole aircraft are fighters that are capable of air-to-air combat but also perform well in a ground-attack capacity. Although multirole aircraft equipped for strike missions aren't as capable in an air-to-air role as designated air superiority fighters, they are capable of destroying surface targets and can defend themselves if confronted by enemy aircraft.  
\+ Capable in an air-to-air role.  
\+ Can destroy ground targets.  
\+ Very responsive, good for support.  
\+ Can carry nuclear weapons.  
\- Comparatively limited firepower.  
\- Not as good in air-to-air fights.  
\- Relatively expendable.

**How to get it:** available from the start — technology `U_Attack`.

**Built at / carried by:** [Carrier](#carrier-carrier), [Tactical Airbase](#tactical-airbase-tactical_airbase), [Makeshift Airbase](#makeshift-airbase-improvised_airbase).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 0.65 |
| `speed` | 650 |
| `range` | 2 200 |
| `size` | 0.05 |
| `turnspeed` | 7.5 |
| `maxelevation` | 20 |
| `productioncost` | 1 |

**Weapons** (switchable configurations):

- *Bombs*:
    - [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×4, reload 0.3 s, auto-engages, principal)
    - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
- *Rockets (default)*:
    - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×8, salvo 8, reload 0.2 s, auto-engages, principal)
    - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)

**Sensors:** [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air) (100 km), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision) (100 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [2nd Generation Aircraft](A5-Catalog-Technologies.md#2nd-generation-aircraft-generation_2_aircraft) (`Generation_2_Aircraft`):
    - new appearance
    - `speed` = 750
    - `turnspeed` = 9
    - `range` = 2 600
    - `power` = 0.75
    - weapon config “Air-to-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, reload 4 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Bombs” becomes:
        - [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×4, reload 0.3 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Rockets” becomes:
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×8, salvo 8, reload 0.2 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 4 s, auto-engages)
    - weapon config “AGM” becomes empty
    - `improvedby` multiply
    - `weapon` multiply
    - weapon config “100kt Bomb” becomes:
        - [Light 100 Kiloton Bomb](A2-Catalog-Missiles.md#light-100-kiloton-bomb-100kt_nuke_light) (`100kt_nuke_light`) (×1)
    - weapon config “250kt Bomb” becomes:
        - [Light 250 Kiloton Bomb](A2-Catalog-Missiles.md#light-250-kiloton-bomb-250kt_nuke_light) (`250kt_nuke_light`) (×1)
    - weapon config “500kt Bomb” becomes:
        - [Light 500 kiloton Bomb](A2-Catalog-Missiles.md#light-500-kiloton-bomb-500kt-nuke_light) (`500kt nuke_light`) (×1)
    - weapon config “500kt Cobalt Bomb” becomes:
        - [Light 500kt Cobalt Bomb](A2-Catalog-Missiles.md#light-500kt-cobalt-bomb-500kt-light-cobalt-bomb) (`500kt Light Cobalt Bomb`) (×1)
    - weapon config “500kt Enhanced Salted Bomb” becomes:
        - [Light 500kt Salted Bomb](A2-Catalog-Missiles.md#light-500kt-salted-bomb-500kt-light-salt-bomb) (`500kt Light Salt Bomb`) (×1)
    - weapon config “Megaton Bomb” becomes:
        - [Light Megaton Bomb](A2-Catalog-Missiles.md#light-megaton-bomb-1m-nuke_light) (`1M nuke_light`) (×1)
    - weapon config “5 Megaton Bomb” becomes:
        - [Light 5M Pure Fusion Bomb](A2-Catalog-Missiles.md#light-5m-pure-fusion-bomb-5m-nuke_light) (`5M nuke_light`) (×1)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft) (`Generation_3_Aircraft`):
    - new appearance
    - `size` = 0.04
    - `speed` = 850
    - `turnspeed` = 10
    - `range` = 3 000
    - `power` = 1
    - weapon config “Air-to-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 3.3 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Bombs” becomes:
        - [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×6, reload 0.3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 3.3 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Rockets” becomes:
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 3.3 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “AGM” becomes:
        - [AGM](A2-Catalog-Missiles.md#agm-agm) (`AGM`) (×2, reload 2 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 3.3 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [4th Generation Aircraft](A5-Catalog-Technologies.md#4th-generation-aircraft-generation_4_aircraft) (`Generation_4_Aircraft`):
    - new appearance
    - `size` = 0.03
    - `speed` = 1 000
    - `turnspeed` = 12
    - `range` = 3 500
    - `power` = 1.2
    - weapon config “Air-to-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×8, salvo 2, reload 2.7 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Bombs” becomes:
        - [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×8, reload 0.3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Rockets” becomes:
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “AGM” becomes:
        - [AGM](A2-Catalog-Missiles.md#agm-agm) (`AGM`) (×4, salvo 2, reload 2 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “ALCM” becomes:
        - [ALCM](A2-Catalog-Missiles.md#alcm-alcm) (`ALCM`) (×1, reload 5 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Nuclear ALCM” becomes:
        - [Nuclear ALCM](A2-Catalog-Missiles.md#nuclear-alcm-alcm-n) (`ALCM-N`) (×1, reload 5 s)
    - weapon config “Pure Fusion ALCM” becomes:
        - [Pure Fusion ALCM](A2-Catalog-Missiles.md#pure-fusion-alcm-fusion-alcm) (`Fusion ALCM`) (×1, reload 5 s)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [4.5+ Generation Aircraft](A5-Catalog-Technologies.md#45-generation-aircraft-generation_45_aircraft) (`Generation_4.5_Aircraft`):
    - `size` = 0.025
    - `speed` = 1 000
    - `turnspeed` = 14
    - `range` = 3 750
    - `power` = 1.4
    - weapon config “Air-to-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×8, salvo 2, reload 2.3 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Bombs” becomes:
        - [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×10, reload 0.3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Rockets” becomes:
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2.3 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “AGM” becomes:
        - [AGM](A2-Catalog-Missiles.md#agm-agm) (`AGM`) (×6, salvo 2, reload 1.7 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2.3 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “ALCM” becomes:
        - [ALCM](A2-Catalog-Missiles.md#alcm-alcm) (`ALCM`) (×1, reload 4 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2.3 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Nuclear ALCM” becomes:
        - [Nuclear ALCM](A2-Catalog-Missiles.md#nuclear-alcm-alcm-n) (`ALCM-N`) (×1, reload 4 s)
    - weapon config “Pure Fusion ALCM” becomes:
        - [Pure Fusion ALCM](A2-Catalog-Missiles.md#pure-fusion-alcm-fusion-alcm) (`Fusion ALCM`) (×1, reload 4 s)
- With [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`):
    - new appearance
    - `size` = 0.02
    - `speed` = 1 150
    - `turnspeed` = 16
    - `range` = 4 000
    - `power` = 1.6
    - weapon config “Air-to-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×8, salvo 2, reload 2 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Bombs” becomes:
        - [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×8, reload 0.3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Rockets” becomes:
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “AGM” becomes:
        - [AGM](A2-Catalog-Missiles.md#agm-agm) (`AGM`) (×6, salvo 2, reload 1.5 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “ALCM” becomes:
        - [ALCM](A2-Catalog-Missiles.md#alcm-alcm) (`ALCM`) (×1, reload 3.3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×2, reload 2 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Nuclear ALCM” becomes:
        - [Nuclear ALCM](A2-Catalog-Missiles.md#nuclear-alcm-alcm-n) (`ALCM-N`) (×1, reload 3.3 s)
    - weapon config “Pure Fusion ALCM” becomes:
        - [Pure Fusion ALCM](A2-Catalog-Missiles.md#pure-fusion-alcm-fusion-alcm) (`Fusion ALCM`) (×1, reload 3.3 s)
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`):
    - new appearance
    - `size` = 0.015
    - `speed` = 1 250
    - `turnspeed` = 18
    - `range` = 5 000
    - `power` = 1.8
    - weapon config “Air-to-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×12, salvo 3, reload 1.7 s, auto-engages, principal)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Bombs” becomes:
        - [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×8, reload 0.3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 1.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Rockets” becomes:
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 1.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “AGM” becomes:
        - [AGM](A2-Catalog-Missiles.md#agm-agm) (`AGM`) (×8, salvo 4, reload 1.5 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 1.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “ALCM” becomes:
        - [ALCM](A2-Catalog-Missiles.md#alcm-alcm) (`ALCM`) (×2, salvo 2, reload 3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 1.7 s, auto-engages)
        - [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun) (`Plane Gun`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Nuclear ALCM” becomes:
        - [Nuclear ALCM](A2-Catalog-Missiles.md#nuclear-alcm-alcm-n) (`ALCM-N`) (×1, reload 3 s)
    - weapon config “Pure Fusion ALCM” becomes:
        - [Pure Fusion ALCM](A2-Catalog-Missiles.md#pure-fusion-alcm-fusion-alcm) (`Fusion ALCM`) (×1, reload 3 s)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Anti-Air Laser Weapons](A5-Catalog-Technologies.md#anti-air-laser-weapons-aa_laser) (`AA_Laser`) + [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`) + [Deadly Laser Weapons](A5-Catalog-Technologies.md#deadly-laser-weapons-offensive_laser_weapons) (`Offensive_Laser_Weapons`):
    - weapon config “Air-to-Air” becomes:
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×12, salvo 3, reload 1.7 s, auto-engages, principal)
        - [Aircraft Laser](A2-Catalog-Missiles.md#aircraft-laser-plane-laser) (`Plane Laser`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Bombs” becomes:
        - [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×8, reload 0.3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 1.7 s, auto-engages)
        - [Aircraft Laser](A2-Catalog-Missiles.md#aircraft-laser-plane-laser) (`Plane Laser`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Rockets” becomes:
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 1.7 s, auto-engages)
        - [Aircraft Laser](A2-Catalog-Missiles.md#aircraft-laser-plane-laser) (`Plane Laser`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “AGM” becomes:
        - [AGM](A2-Catalog-Missiles.md#agm-agm) (`AGM`) (×8, salvo 4, reload 1.7 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 1.7 s, auto-engages)
        - [Aircraft Laser](A2-Catalog-Missiles.md#aircraft-laser-plane-laser) (`Plane Laser`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “ALCM” becomes:
        - [ALCM](A2-Catalog-Missiles.md#alcm-alcm) (`ALCM`) (×2, salvo 2, reload 3 s, auto-engages, principal)
        - [AAM](A2-Catalog-Missiles.md#aam-aam) (`AAM`) (×4, salvo 2, reload 1.7 s, auto-engages)
        - [Aircraft Laser](A2-Catalog-Missiles.md#aircraft-laser-plane-laser) (`Plane Laser`) (unlimited, reload 0.3 s, auto-engages)
    - weapon config “Nuclear ALCM” becomes:
        - [Nuclear ALCM](A2-Catalog-Missiles.md#nuclear-alcm-alcm-n) (`ALCM-N`) (×1, reload 3 s)
    - weapon config “Pure Fusion ALCM” becomes:
        - [Pure Fusion ALCM](A2-Catalog-Missiles.md#pure-fusion-alcm-fusion-alcm) (`Fusion ALCM`) (×1, reload 3 s)

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Autocannon](A2-Catalog-Missiles.md#autocannon-plane-gun): [2nd Generation Aircraft](A5-Catalog-Technologies.md#2nd-generation-aircraft-generation_2_aircraft), [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Stealth Technology”](#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`) (active after researching [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`)): enemy sensors (12): `range` ×0.6
- [“Advanced Stealth”](#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`) (active after researching [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`)): enemy sensors (12): `range` ×0.75
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

### Special Mission Aircraft (`SOF_Aircraft`)

<!-- img:upgrades Units/Images/Icons/Airborne/SOF_Aircraft_1.png=Base|Units/Images/Icons/Airborne/SOF_Aircraft_2.png=Jet-Powered Heavy Airframes|Units/Images/Icons/Airborne/SOF_Aircraft_3.png=Blended Wing Airframes -->

A medium airlift aircraft piloted by a highly-trained crew and specially modified to support special operations. Special Mission Aircraft have the equipment necessarily to facilitate high-altitude combat jumps, allowing special forces to HALO or HAHO jump behind enemy lines. However, these aircraft are not stealthy and can easily be intercepted and destroyed if spotted. Because of the training and maintenance requirements demanded by these specific aircraft, they are hosted by specialized airbases.  
\+ Can quickly transport spec-ops teams.  
\+ Semi-covert, faction is hidden unless destroyed.  
\+ Has optics, can spot covert units  
\- Requires specialized airbases.  
\- No stealth advantages, easily detected.  
\- Unarmed and vulnerable.

**How to get it:** available from the start — technology `U_SOF_Aircraft`.

**Built at / carried by:** [Specialized Airbase](#specialized-airbase-specialized_airport).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 1 |
| `speed` | 400 |
| `range` | 5 000 |
| `size` | 0.15 |
| `turnspeed` | 5 |
| `maxelevation` | 30 |
| `productioncost` | 3 |

**Sensors:** [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision) (100 km), [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy) (200 km), [Occupation Zone Finder](A4-Catalog-Radars.md#occupation-zone-finder-occupation-zone-finder) (130 km).

**Can transport:** [Spec-Ops Team](#spec-ops-team-spec_ops_team).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Jet-Powered Heavy Airframes](A5-Catalog-Technologies.md#jet-powered-heavy-airframes-heavy_airframe_1) (`Heavy_Airframe_1`):
    - new appearance
    - `speed` = 600
    - `turnspeed` = 7.5
    - `range` = 9 000
    - `power` = 1.1
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [High Efficiency Heavy Airframes](A5-Catalog-Technologies.md#high-efficiency-heavy-airframes-heavy_airframe_2) (`Heavy_Airframe_2`):
    - `speed` = 750
    - `turnspeed` = 9.5
    - `range` = 12 000
    - `power` = 1.25
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Blended Wing Airframes](A5-Catalog-Technologies.md#blended-wing-airframes-heavy_airframe_3) (`Heavy_Airframe_3`):
    - new appearance
    - `speed` = 900
    - `size` = 0.15
    - `turnspeed` = 11.5
    - `range` = 18 000
    - `power` = 1.5

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

### Strategic Bomber (`Bomber`)

<!-- img:upgrades Units/Images/Icons/Airborne/Bomber_Basic.png=Base|Units/Images/Icons/Airborne/LR_Bomber_1.png=Long-Range Bombers|Units/Images/Icons/Airborne/LR_Bomber_2.png=Late Supersonic Bombers|Units/Images/Icons/Airborne/LR_Bomber_3.png=Stealth Bombers|Units/Images/Icons/Airborne/LR_Bomber_4.png=Advanced Stealth Bombers -->

Strategic bombers are designed to fly long distances and destroy crucial enemy infrastructure to reduce their capacity to wage war. Common targets of strategic bombers include industrial centers, military bases, supply lines and cities. Bombers are capable of carrying heavy payloads, and can deploy oversized nuclear weapons over long distances.  
\+ Can carry heavy nuclear weapons.  
\+ Can potentially use nuclear missiles.  
\+ Good conventional firepower.  
\+ Large combat radius.  
\- Big, easy to hit.  
\- Relatively slow, not as flexible.

**How to get it:** available from the start — technology `U_Bomber`.

**Built at / carried by:** [Air Base](#air-base-airport).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 2 |
| `speed` | 400 |
| `range` | 6 000 |
| `size` | 0.1 |
| `turnspeed` | 3 |
| `maxelevation` | 30 |
| `productioncost` | 4.2 |

**Weapons** (switchable configurations):

- *Bombs (default)*: [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb) (`Free fall bomb`) (×20, salvo 4, auto-engages)
- *100 Kiloton*: [Light 100 Kiloton Bomb](A2-Catalog-Missiles.md#light-100-kiloton-bomb-100kt_nuke_light) (`100kt_nuke_light`) (×1)
- *500 Kiloton*: [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy) (`500kt nuke_heavy`) (×1)
- *10 Megaton*: [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy) (`10M nuke_heavy`) (×1)
- *25 Megaton*: [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy) (`25M nuke_heavy`) (×1)
- *50 Megaton*: [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy) (`50M nuke_heavy`) (×1)
- *100 Megaton*: [Heavy 100M Fusion Bomb](A2-Catalog-Missiles.md#heavy-100m-fusion-bomb-100m-nuke_heavy) (`100M nuke_heavy`) (×1)
- *Chemical Bomb*: [Mustard Gas Bomb](A2-Catalog-Missiles.md#mustard-gas-bomb-chemical_bomb) (`Chemical_bomb`) (×6, salvo 2)
- *Bioweapon*: [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb) (`Bioweapon_bomb`) (×1)
- *Improved Bioweapon*: [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb) (`Improved_Bioweapon_bomb`) (×1)
- *Advanced Bioweapon*: [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb) (`Advanced_Bioweapon_bomb`) (×1)
- *Engineered Bioweapon*: [EMeVHF-24 Bomb](A2-Catalog-Missiles.md#emevhf-24-bomb-engineered_bioweapon_bomb) (`Engineered_Bioweapon_bomb`) (×1)
- *Cobalt Bomb*: [10 Megaton Cobalt Bomb](A2-Catalog-Missiles.md#10-megaton-cobalt-bomb-cobalt_bomb) (`Cobalt_Bomb`) (×1)
- *Enhanced Salted Bomb*: [10 Megaton Salted Bomb](A2-Catalog-Missiles.md#10-megaton-salted-bomb-salted_bomb) (`Salted_Bomb`) (×1)
- *250kt ICBM*: no weapons (a technology adds them)
- *500kt ICBM*: no weapons (a technology adds them)
- *Megaton ICBM*: no weapons (a technology adds them)
- *1MT Cobalt ICBM*: no weapons (a technology adds them)
- *1MT Enhanced Salted ICBM*: no weapons (a technology adds them)
- *5 Megaton ICBM*: no weapons (a technology adds them)
- *10 Megaton Fusion ICBM*: no weapons (a technology adds them)
- *3x250kt Light MIRV*: no weapons (a technology adds them)
- *3x500kt Light MIRV*: no weapons (a technology adds them)
- *8x500kt Light MIRV*: no weapons (a technology adds them)
- *8x1M Light MIRV*: no weapons (a technology adds them)
- *1M EMP ICBM*: no weapons (a technology adds them)
- *1M Super EMP ICBM*: no weapons (a technology adds them)
- *Bioweapon ICBM*: no weapons (a technology adds them)
- *Improved Bioweapon ICBM*: no weapons (a technology adds them)
- *Advanced Bioweapon ICBM*: no weapons (a technology adds them)
- *Engineered Bioweapon ICBM*: no weapons (a technology adds them)
- *3x Biological MIRV*: no weapons (a technology adds them)
- *8x Biological MIRV*: no weapons (a technology adds them)

**Sensors:** [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air) (100 km), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision) (100 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Long-Range Bombers](A5-Catalog-Technologies.md#long-range-bombers-generation_2_bomber) (`Generation_2_Bomber`):
    - new appearance
    - `speed` = 500
    - `turnspeed` = 4
    - `range` = 16 000
    - `power` = 2.2
    - weapon config “GBU Strike” becomes:
        - [GBU](A2-Catalog-Missiles.md#gbu-gbu) (`GBU`) (×10, salvo 4, auto-engages)
    - weapon config “Cruise Missiles” becomes:
        - [ALCM](A2-Catalog-Missiles.md#alcm-alcm) (`ALCM`) (×4, salvo 2, reload 2 s, auto-engages)
    - weapon config “Nuclear Cruise Missiles” becomes:
        - [Nuclear ALCM](A2-Catalog-Missiles.md#nuclear-alcm-alcm-n) (`ALCM-N`) (×1, reload 2 s)
        - [ALCM](A2-Catalog-Missiles.md#alcm-alcm) (`ALCM`) (×3, salvo 3, reload 2 s)
    - weapon config “Fusion Cruise Missiles” becomes:
        - [Pure Fusion ALCM](A2-Catalog-Missiles.md#pure-fusion-alcm-fusion-alcm) (`Fusion ALCM`) (×1, reload 2 s)
        - [ALCM](A2-Catalog-Missiles.md#alcm-alcm) (`ALCM`) (×3, salvo 3, reload 2 s)
    - weapon config “Conventional ALBM” becomes:
        - [ALBM](A2-Catalog-Missiles.md#albm-albm) (`ALBM`) (×1, reload 8 s)
    - weapon config “100kt ALBM” becomes:
        - [100kt ALBM](A2-Catalog-Missiles.md#100kt-albm-100kt-albm) (`100kt ALBM`) (×1, reload 8 s)
    - weapon config “250kt ALBM” becomes:
        - [250kt ALBM](A2-Catalog-Missiles.md#250kt-albm-250kt-albm) (`250kt ALBM`) (×1, reload 8 s)
    - weapon config “500kt ALBM” becomes:
        - [500kt ALBM](A2-Catalog-Missiles.md#500kt-albm-500kt-albm) (`500kt ALBM`) (×1, reload 8 s)
    - weapon config “Megaton ALBM” becomes:
        - [Megaton ALBM](A2-Catalog-Missiles.md#megaton-albm-1m-albm) (`1M ALBM`) (×1, reload 8 s)
    - weapon config “5 Megaton ALBM” becomes:
        - [5M Pure Fusion ALBM](A2-Catalog-Missiles.md#5m-pure-fusion-albm-5m-albm) (`5M ALBM`) (×1, reload 8 s)
    - weapon config “500kt Cobalt ALBM” becomes:
        - [500kt Cobalt ALBM](A2-Catalog-Missiles.md#500kt-cobalt-albm-500kt-cobalt-albm) (`500kt Cobalt ALBM`) (×1, reload 8 s)
    - weapon config “500kt Salt ALBM” becomes:
        - [500kt Salted ALBM](A2-Catalog-Missiles.md#500kt-salted-albm-500kt-salt-albm) (`500kt Salt ALBM`) (×1, reload 8 s)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave)
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`):
    - weapon config “Chemical Bomb” becomes:
        - [Sarin Bomb](A2-Catalog-Missiles.md#sarin-bomb-improved_chemical_bomb) (`Improved_Chemical_bomb`) (×6, salvo 2)
- With [Late Supersonic Bombers](A5-Catalog-Technologies.md#late-supersonic-bombers-generation_4_bomber) (`Generation_4_Bomber`):
    - new appearance
    - `speed` = 900
    - `size` = 0.08
    - `turnspeed` = 7
    - `range` = 16 000
    - `power` = 2.4
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`):
    - weapon config “Chemical Bomb” becomes:
        - [VX Gas Bomb](A2-Catalog-Missiles.md#vx-gas-bomb-advanced_chemical_bomb) (`Advanced_Chemical_bomb`) (×6, salvo 2)
- With [Long-Range Bombers](A5-Catalog-Technologies.md#long-range-bombers-generation_2_bomber) (`Generation_2_Bomber`) + [Aircraft Launched ICBM](A5-Catalog-Technologies.md#aircraft-launched-icbm-aircraft-launched_icbm) (`Aircraft-launched_ICBM`):
    - weapon config “250kt ICBM” becomes:
        - [250 Kiloton Light ICBM](A2-Catalog-Missiles.md#250-kiloton-light-icbm-icbm-250kt-light) (`ICBM (250kt Light)`) (×1, reload 30 s)
    - weapon config “500kt ICBM” becomes:
        - [500 Kiloton Light ICBM](A2-Catalog-Missiles.md#500-kiloton-light-icbm-icbm-500kt-light) (`ICBM (500kt Light)`) (×1, reload 30 s)
    - weapon config “Megaton ICBM” becomes:
        - [Megaton Light ICBM](A2-Catalog-Missiles.md#megaton-light-icbm-icbm-1m-light) (`ICBM (1M Light)`) (×1, reload 30 s)
    - weapon config “1MT Cobalt ICBM” becomes:
        - [1M Light Cobalt ICBM](A2-Catalog-Missiles.md#1m-light-cobalt-icbm-icbm-1m-cobalt) (`ICBM (1M Cobalt)`) (×1, reload 30 s)
    - weapon config “1MT Enhanced Salted ICBM” becomes:
        - [1M Light Salted ICBM](A2-Catalog-Missiles.md#1m-light-salted-icbm-icbm-1m-salt) (`ICBM (1M Salt)`) (×1, reload 30 s)
    - weapon config “5 Megaton ICBM” becomes:
        - [5 Megaton Light ICBM](A2-Catalog-Missiles.md#5-megaton-light-icbm-icbm-5m-light) (`ICBM (5M Light)`) (×1, reload 30 s)
    - weapon config “10 Megaton Fusion ICBM” becomes:
        - [10M Pure Fusion ICBM](A2-Catalog-Missiles.md#10m-pure-fusion-icbm-icbm-10m-fusion-light) (`ICBM (10M Fusion Light)`) (×1, reload 30 s)
    - weapon config “3x250kt Light MIRV” becomes:
        - [3x250kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-light-mirv-icbm-3x250kt-light-icbm) (`3x250kt Light ICBM`) (×1, reload 30 s)
    - weapon config “3x500kt Light MIRV” becomes:
        - [3x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-light-mirv-icbm-3x500kt-light-icbm) (`3x500kt Light ICBM`) (×1, reload 30 s)
    - weapon config “8x500kt Light MIRV” becomes:
        - [8x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#8x500kt-light-mirv-icbm-8x500kt-light-icbm) (`8x500kt Light ICBM`) (×1, reload 30 s)
    - weapon config “8x1M Light MIRV” becomes:
        - [8x1M Light Fusion MIRV](A2-Catalog-Missiles.md#8x1m-light-fusion-mirv-8x1m-light-icbm) (`8x1M Light ICBM`) (×1, reload 30 s)
    - weapon config “1M EMP ICBM” becomes:
        - [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp) (`ICBM (1M EMP)`) (×1, reload 30 s)
    - weapon config “1M Super EMP ICBM” becomes:
        - [1M Super EMP ICBM](A2-Catalog-Missiles.md#1m-super-emp-icbm-icbm-1m-super-emp) (`ICBM (1M Super EMP)`) (×1, reload 30 s)
    - weapon config “Bioweapon ICBM” becomes:
        - [Rabbit Fever ICBM](A2-Catalog-Missiles.md#rabbit-fever-icbm-bioweapon_icbm) (`Bioweapon_ICBM`) (×1, reload 30 s)
    - weapon config “Improved Bioweapon ICBM” becomes:
        - [Smallpox ICBM](A2-Catalog-Missiles.md#smallpox-icbm-improved_bioweapon_icbm) (`Improved_Bioweapon_ICBM`) (×1, reload 30 s)
    - weapon config “Advanced Bioweapon ICBM” becomes:
        - [Ebola ICBM](A2-Catalog-Missiles.md#ebola-icbm-advanced_bioweapon_icbm) (`Advanced_Bioweapon_ICBM`) (×1, reload 30 s)
    - weapon config “Engineered Bioweapon ICBM” becomes:
        - [EMeVHF-24 ICBM](A2-Catalog-Missiles.md#emevhf-24-icbm-engineered_bioweapon_icbm) (`Engineered_Bioweapon_ICBM`) (×1, reload 30 s)
    - weapon config “3x Biological MIRV” becomes:
        - [3xBW Bioweapon MIRV](A2-Catalog-Missiles.md#3xbw-bioweapon-mirv-bioweapon_mirv) (`Bioweapon_MIRV`) (×1, reload 30 s)
    - weapon config “8x Biological MIRV” becomes:
        - [8xBW Bioweapon MIRV](A2-Catalog-Missiles.md#8xbw-bioweapon-mirv-8x-bioweapon_mirv) (`8x Bioweapon_MIRV`) (×1, reload 30 s)
- With [Stealth Bombers](A5-Catalog-Technologies.md#stealth-bombers-generation_5_bomber) (`Generation_5_Bomber`):
    - new appearance
    - `size` = 0.07
    - `turnspeed` = 7
    - `range` = 16 000
    - `power` = 2.8
- With [Aircraft Launched ICBM](A5-Catalog-Technologies.md#aircraft-launched-icbm-aircraft-launched_icbm) (`Aircraft-launched_ICBM`): `speed` ×1
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`):
    - weapon config “Chemical Bomb” becomes:
        - [Novichok-2000 Bomb](A2-Catalog-Missiles.md#novichok-2000-bomb-experimental_chemical_bomb) (`Experimental_Chemical_bomb`) (×6, salvo 2)
- With [Advanced Stealth Bombers](A5-Catalog-Technologies.md#advanced-stealth-bombers-generation_6_bomber) (`Generation_6_Bomber`):
    - new appearance
    - `size` = 0.06
    - `turnspeed` = 8
    - `range` = 24 000
    - `power` = 3

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy): [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb)
- [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy): [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads)
- [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy): [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy): [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb): [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2)
- [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb): [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3)
- [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb): [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem)
- [10 Megaton Cobalt Bomb](A2-Catalog-Missiles.md#10-megaton-cobalt-bomb-cobalt_bomb): [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Stealth Technology”](#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`) (active after researching [Stealth Bombers](A5-Catalog-Technologies.md#stealth-bombers-generation_5_bomber) (`Generation_5_Bomber`)): enemy sensors (12): `range` ×0.55
- [“Advanced Stealth”](#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`) (active after researching [Advanced Stealth Bombers](A5-Catalog-Technologies.md#advanced-stealth-bombers-generation_6_bomber) (`Generation_6_Bomber`)): enemy sensors (12): `range` ×0.65
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

**Other traits:** `AL-ICBM_Range_Adjust`.

### AWACS (`AWACS`)

<!-- img:upgrades Units/Images/Icons/Airborne/AWACS_1.png=Base|Units/Images/Icons/Airborne/AWACS_2.png=Jet-Powered Heavy Airframes|Units/Images/Icons/Airborne/AWACS_3.png=High Efficiency Heavy Airframes|Units/Images/Icons/Airborne/AWACS_4.png=Blended Wing Airframes -->

A heavy aircraft modified to carry a large radar system and a command center to direct friendly aircraft and monitor and control the battlespace. AWACS can detect airborne threats like opposing aircraft and missiles to provide early warning, as well as support the operations of friendly assets. AWACS are best suited for surveilling the airspace, but can also detect units on the ground as well.  
\+ Can detect aircraft from long range.  
\+ Some ground surveillance capability.  
\+ Tracks ballistic missiles with EWS upgrade.  
\- Does not carry weapons.  
\- Vulnerable and easy to hit.  
\- Relatively expensive.  
\- Limited use without supporting units.

**How to get it:** [AWACS](A5-Catalog-Technologies.md#awacs-awacs) (`AWACS`) — technology `U_AWACS`.

**Built at / carried by:** [Air Base](#air-base-airport), [Tactical Airbase](#tactical-airbase-tactical_airbase).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 1.5 |
| `speed` | 400 |
| `range` | 8 000 |
| `size` | 0.075 |
| `turnspeed` | 3 |
| `maxelevation` | 30 |
| `productioncost` | 4 |

**Sensors:** [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) (300 km), [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) (400 km), [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon) (2 000 km), [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection) (800 km), [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting) (600 km), [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong) (950 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Jet-Powered Heavy Airframes](A5-Catalog-Technologies.md#jet-powered-heavy-airframes-heavy_airframe_1) (`Heavy_Airframe_1`):
    - new appearance
    - `speed` = 500
    - `turnspeed` = 4.5
    - `range` = 12 000
    - `power` = 1.75
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [High Efficiency Heavy Airframes](A5-Catalog-Technologies.md#high-efficiency-heavy-airframes-heavy_airframe_2) (`Heavy_Airframe_2`):
    - new appearance
    - `speed` = 700
    - `size` = 0.05
    - `turnspeed` = 6
    - `range` = 16 000
    - `power` = 2
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Blended Wing Airframes](A5-Catalog-Technologies.md#blended-wing-airframes-heavy_airframe_3) (`Heavy_Airframe_3`):
    - new appearance
    - `speed` = 900
    - `size` = 0.06
    - `turnspeed` = 7.8
    - `range` = 20 000
    - `power` = 2.2

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon): [Advanced Early Warning Radar](A5-Catalog-Technologies.md#advanced-early-warning-radar-over_horizon_radar_mk2)
- [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong): [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6)

**Sensor vulnerabilities:**

- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

### Carrier AWACS (`Naval AWACS`)

<!-- img:upgrades Units/Images/Icons/Airborne/AWACS_Naval_1.png=Base|Units/Images/Icons/Airborne/AWACS_Naval_2.png=Blended Wing Airframes -->

A lightweight AWACS capable of launching from aircraft carriers. Like the regular AWACS, it can survey a wide area and detect enemy units from long range, but is less capable due to its smaller size.  
\+ Can detect aircraft from long range.  
\+ Some ground surveillance capability.  
\+ Tracks ballistic missiles with EWS upgrade.  
\+ Launches from carriers, good for support.  
\- Unarmed, vulnerable and expensive.  
\- Limited use without supporting units.  
\- Smaller radar range than regular AWACS.  
\- Comparatively poor flight performance.

**How to get it:** [AWACS](A5-Catalog-Technologies.md#awacs-awacs) (`AWACS`) — technology `U_Naval_AWACS`.

**Built at / carried by:** [Carrier](#carrier-carrier).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 1 |
| `speed` | 400 |
| `range` | 3 000 |
| `size` | 0.06 |
| `turnspeed` | 3 |
| `maxelevation` | 25 |
| `productioncost` | 3.6 |

**Sensors:** [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) (300 km), [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) (400 km), [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon) (2 000 km), [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection) (800 km), [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting) (600 km), [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) (525 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Jet-Powered Heavy Airframes](A5-Catalog-Technologies.md#jet-powered-heavy-airframes-heavy_airframe_1) (`Heavy_Airframe_1`):
    - `range` = 3 500
    - `power` = 1.25
    - `speed` = 450
    - `turnspeed` = 3.5
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [High Efficiency Heavy Airframes](A5-Catalog-Technologies.md#high-efficiency-heavy-airframes-heavy_airframe_2) (`Heavy_Airframe_2`):
    - `range` = 4 500
    - `power` = 1.5
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Blended Wing Airframes](A5-Catalog-Technologies.md#blended-wing-airframes-heavy_airframe_3) (`Heavy_Airframe_3`):
    - new appearance
    - `speed` = 600
    - `turnspeed` = 4.8
    - `range` = 6 000
    - `power` = 2

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon): [Advanced Early Warning Radar](A5-Catalog-Technologies.md#advanced-early-warning-radar-over_horizon_radar_mk2)
- [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak): [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6)

**Sensor vulnerabilities:**

- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

**Other traits:** `Naval_AWACS_Mod`.

### Naval Helicopter (`Navy_Helicopter`)

<!-- img:upgrades Units/Images/Icons/Airborne/Naval_Heli_1.png=Base|Units/Images/Icons/Airborne/Naval_Heli_2.png=Turboshaft Helicopters|Units/Images/Icons/Airborne/Naval_Heli_3.png=Enhanced Helicopters|Units/Images/Icons/Airborne/Naval_Heli_4.png=Advanced Helicopters|Units/Images/Icons/Airborne/Naval_Heli_5.png=Unconventional Rotorcraft -->

A multi-role utility helicopter designed for shipborne and maritime operations in support of the navy. By default, it comes equipped for anti-submarine warfare, armed with a dipping sonar and depth charges. However, it also has the potential to be upgraded to fill a variety of other roles as well. With the development of powerful airborne radar systems, it can be upgraded to detect enemy aircraft and surface assets and provide early warning and reconnaissance. Naval helicopters also have the potential to be equipped with lightweight anti-ship missiles, which are effective against light vessels or larger ships when used in large numbers.  
\+ Can detect and attack submarines.  
\+ Can be upgraded to carry radar with AWACS.  
\+ Can be upgraded with anti-ship missiles.  
\- Limited speed and range.  
\- Vulnerable to anti-air weapons.

**How to get it:** [Helicopters](A5-Catalog-Technologies.md#helicopters-helicopter_1) (`Helicopter_1`) — technology `U_Navy_Helicopter`.

**Built at / carried by:** [Carrier](#carrier-carrier), [Naval Monitoring Station](#naval-monitoring-station-naval_monitoring_station).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 0.8 |
| `speed` | 200 |
| `range` | 1 200 |
| `size` | 0.08 |
| `turnspeed` | 3 |
| `maxelevation` | 5 |
| `productioncost` | 1.5 |

**Weapons** (switchable configurations):

- *ASW (default)*:
    - [Depth Charge](A2-Catalog-Missiles.md#depth-charge-depthcharge) (`DepthCharge`) (×6, salvo 2, reload 1.5 s, auto-engages)
    - [Airdropped Torpedo](A2-Catalog-Missiles.md#airdropped-torpedo-air-dropped-torpedo) (`Air-Dropped Torpedo`) (×6, salvo 2, reload 1.5 s, auto-engages)
- *Anti-Ship*: no weapons (a technology adds them)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision) (100 km), [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) (300 km), [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) (400 km), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar) (150 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [AWACS](A5-Catalog-Technologies.md#awacs-awacs) (`AWACS`): `size` ×1
- With [Early CLOS Air-to-Ground Weapons](A5-Catalog-Technologies.md#early-clos-air-to-ground-weapons-air_to_ground_missile) (`Air_to_Ground_missile`) + [Coastal Missile Batteries](A5-Catalog-Technologies.md#coastal-missile-batteries-coastal_defence) (`Coastal_Defence`):
    - weapon config “Anti-Ship” becomes:
        - [Light AShM](A2-Catalog-Missiles.md#light-ashm-light_ashm) (`Light_AShM`) (×2, reload 0.3 s, auto-engages, principal)
        - [Depth Charge](A2-Catalog-Missiles.md#depth-charge-depthcharge) (`DepthCharge`) (×2, salvo 2, reload 1.5 s, auto-engages)
        - [Airdropped Torpedo](A2-Catalog-Missiles.md#airdropped-torpedo-air-dropped-torpedo) (`Air-Dropped Torpedo`) (×2, salvo 2, reload 1.5 s, auto-engages)
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Turboshaft Helicopters](A5-Catalog-Technologies.md#turboshaft-helicopters-helicopter_2) (`Helicopter_2`):
    - new appearance
    - `speed` = 250
    - `size` = 0.075
    - `turnspeed` = 3.75
    - `range` = 1 400
    - `power` = 1
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Enhanced Helicopters](A5-Catalog-Technologies.md#enhanced-helicopters-helicopter_3) (`Helicopter_3`):
    - new appearance
    - `speed` = 300
    - `size` = 0.075
    - `turnspeed` = 4.5
    - `range` = 1 850
    - `power` = 1.3
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Helicopters](A5-Catalog-Technologies.md#advanced-helicopters-helicopter_4) (`Helicopter_4`):
    - new appearance
    - `speed` = 350
    - `size` = 0.075
    - `turnspeed` = 5.25
    - `range` = 2 450
    - `power` = 1.5
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Unconventional Rotorcraft](A5-Catalog-Technologies.md#unconventional-rotorcraft-helicopter_5) (`Helicopter_5`):
    - new appearance
    - `speed` = 500
    - `size` = 0.075
    - `turnspeed` = 7.5
    - `range` = 4 500
    - `power` = 1.6

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Airdropped Torpedo](A2-Catalog-Missiles.md#airdropped-torpedo-air-dropped-torpedo): [Improved Underwater Weapons](A5-Catalog-Technologies.md#improved-underwater-weapons-improved_underwater_weapons), [Enhanced Underwater Weapons](A5-Catalog-Technologies.md#enhanced-underwater-weapons-enhanced_underwater_weapons), [Advanced Underwater Weapons](A5-Catalog-Technologies.md#advanced-underwater-weapons-advanced_underwater_weapons), [Experimental Underwater Weapons](A5-Catalog-Technologies.md#experimental-underwater-weapons-experimental_underwater_weapons)
- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)
- [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2), [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3), [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4), [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5)

**Sensor vulnerabilities:**

- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Helicopters”](#helicopters-helicopter_modifier) (`Helicopter_Modifier`) (always active):
    - enemy weapons (3): `range` ×0.75
    - enemy [LAAM](A2-Catalog-Missiles.md#laam-laam): `maxelevation` ×0
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100
- [“Helicopters”](#helicopters-helicopter_modifier) (`Helicopter_Modifier`) (always active): enemy [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old): `damage` ×1.2

### Spec-Ops Helicopter (`Spec_Ops_Helicopter`)

<!-- img:upgrades Units/Images/Icons/Airborne/Spec_Ops_Heli_1.png=Base|Units/Images/Icons/Airborne/Spec_Ops_Heli_2.png=Turboshaft Helicopters|Units/Images/Icons/Airborne/Spec_Ops_Heli_3.png=Enhanced Helicopters|Units/Images/Icons/Airborne/Spec_Ops_Heli_4.png=Advanced Helicopters|Units/Images/Icons/Airborne/Spec_Ops_Heli_5.png=Unconventional Rotorcraft -->

A helicopter used for special operations. It can carry spec-ops teams and can pick them up from anywhere. This helicopter and its personnel are also equipped and trained to avoid being detected by regular means, as well as identify other covert units, such as enemy spec-ops teams or bomb trucks.  
\+ Can only be detected at close range.  
\+ Good at finding enemy covert units.  
\+ Can deploy and retrieve Spec-ops teams.  
\- Weapons only effective against covert units.  
\- Vulnerable to anti-air weapons.

**How to get it:** [Helicopters](A5-Catalog-Technologies.md#helicopters-helicopter_1) (`Helicopter_1`) — technology `U_Spec-Ops_Helicopter`.

**Built at / carried by:** [Carrier](#carrier-carrier), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 0.8 |
| `speed` | 200 |
| `range` | 1 750 |
| `size` | 0.08 |
| `turnspeed` | 10 |
| `maxelevation` | 5 |
| `productioncost` | 1.8 |

**Weapons**:

- *default*: [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms) (`Small Arms`) (unlimited, reload 0.3 s, auto-engages)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy) (200 km).

**Can transport:** [Spec-Ops Team](#spec-ops-team-spec_ops_team).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Turboshaft Helicopters](A5-Catalog-Technologies.md#turboshaft-helicopters-helicopter_2) (`Helicopter_2`):
    - new appearance
    - `speed` = 250
    - `size` = 0.075
    - `turnspeed` = 12.5
    - `range` = 2 250
    - `power` = 1
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Enhanced Helicopters](A5-Catalog-Technologies.md#enhanced-helicopters-helicopter_3) (`Helicopter_3`):
    - new appearance
    - `speed` = 300
    - `size` = 0.07
    - `turnspeed` = 15
    - `range` = 2 750
    - `power` = 1.3
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Helicopters](A5-Catalog-Technologies.md#advanced-helicopters-helicopter_4) (`Helicopter_4`):
    - new appearance
    - `speed` = 350
    - `size` = 0.065
    - `turnspeed` = 17.5
    - `range` = 3 500
    - `power` = 1.5
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Unconventional Rotorcraft](A5-Catalog-Technologies.md#unconventional-rotorcraft-helicopter_5) (`Helicopter_5`):
    - new appearance
    - `speed` = 500
    - `size` = 0.06
    - `turnspeed` = 25
    - `range` = 6 500
    - `power` = 1.6

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): [Weapon Modernization](A5-Catalog-Technologies.md#weapon-modernization-weapon_modernization), [Upgraded Mixed Weapons](A5-Catalog-Technologies.md#upgraded-mixed-weapons-improved_army_weapons), [Modular and Smart Army Weapons](A5-Catalog-Technologies.md#modular-and-smart-army-weapons-enhanced_army_weapons), [Advanced Army Weapons](A5-Catalog-Technologies.md#advanced-army-weapons-advanced_army_weapons), [Experimental Army Weapon Concepts](A5-Catalog-Technologies.md#experimental-army-weapon-concepts-experimental_army_weapons), [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)
- [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Covert Unit”](#covert-unit-covert_unit) (`Covert_Unit`) (always active):
    - enemy [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces), [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `range` ×0
    - enemy [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision): `range` ×0.75
    - enemy sensors (20): `range` ×0
    - enemy [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): `range` ×1
    - enemy [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance): `range` ×0.4
    - enemy [Periscope](A4-Catalog-Radars.md#periscope-periscope): `range` ×0.5
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Helicopters”](#helicopters-helicopter_modifier) (`Helicopter_Modifier`) (always active):
    - enemy weapons (3): `range` ×0.75
    - enemy [LAAM](A2-Catalog-Missiles.md#laam-laam): `maxelevation` ×0
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100
- [“Helicopters”](#helicopters-helicopter_modifier) (`Helicopter_Modifier`) (always active): enemy [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old): `damage` ×1.2

### Spy Plane (`Spy_Plane`)

<!-- img:upgrades Units/Images/Icons/Airborne/Recce_Air_1.png=Base|Units/Images/Icons/Airborne/Recce_Air_2.png=3rd Generation Aircraft|Units/Images/Icons/Airborne/Recce_Air_3.png=6th Generation Aircraft -->

Spy planes are designed to perform high-altitude photo reconnaissance and identify the location of enemy strategic assets. They can only be engaged by long-range anti-air missiles like those fired by strategic SAM sites and combat aircraft. With the appropriate aircraft technology they can upgrade to supersonic models which are extremely difficult to intercept.  
\+ Can locate enemy units.  
\+ Immune to short-range SAMs and gunfire.  
\+ Undetectable by basic radar.  
\+ Can upgrade to high-speed variants.  
\+ Cheaper and more controllable than satellites.  
\- No weapons.  
\- Requires a specialized airbase.

**How to get it:** [Spy Planes](A5-Catalog-Technologies.md#spy-planes-spy_plane) (`Spy_Plane`) — technology `U_Spy_Plane`.

**Built at / carried by:** [Specialized Airbase](#specialized-airbase-specialized_airport).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 1.5 |
| `speed` | 700 |
| `range` | 15 000 |
| `size` | 0.02 |
| `turnspeed` | 3.5 |
| `maxelevation` | 60 |
| `productioncost` | 4.5 |

**Sensors:** [Reconnaissance Camera](A4-Catalog-Radars.md#reconnaissance-camera-spy-plane-camera) (150 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft) (`Generation_3_Aircraft`):
    - new appearance
    - `speed` = 3 000
    - `size` ×0.8
    - `turnspeed` = 5
    - `range` = 15 000
    - `power` = 1.75
- With [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`):
    - new appearance
    - `speed` = 4 000
    - `size` ×0.8
    - `turnspeed` = 7
    - `range` = 21 000

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Reconnaissance Camera](A4-Catalog-Radars.md#reconnaissance-camera-spy-plane-camera): [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft), [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft)

**Sensor vulnerabilities:**

- [Reconnaissance Camera](A4-Catalog-Radars.md#reconnaissance-camera-spy-plane-camera) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Spy Plane”](#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`) (always active):
    - enemy sensors (6): `range` ×0
    - enemy sensors (4): `range`: ×1 if you have researched [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`); ×0.85 if you have researched [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`); ×0.7 if you have researched [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`); otherwise ×0.1
    - enemy sensors (4): `range`: ×1 if you have researched [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`); ×0.85 if you have researched [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`); ×0.7 if you have researched [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`); otherwise ×0.1

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

### Attack Helicopter (`Attack_Helicopter`)

<!-- img:upgrades Units/Images/Icons/Airborne/Attack_Heli_2.png=Base|Units/Images/Icons/Airborne/Attack_Heli_3.png=Enhanced Helicopters|Units/Images/Icons/Airborne/Attack_Heli_4.png=Advanced Helicopters|Units/Images/Icons/Airborne/Attack_Heli_5.png=Unconventional Rotorcraft -->

A specially-designed helicopter equipped with armour and heavy weapons. Attack helicopters are designed to support army operations and can engage and destroy enemy land forces and infrastructure. They are vulnerable to anti-air weapons but are excellent at supporting army operations if unopposed.  
\+ Good sustained firepower.  
\+ Fast and can loiter, good responsiveness.  
\+ Has optics, can identify covert units.  
\- Relatively limited range.  
\- Vulnerable to anti-air weapons.

**How to get it:** [Turboshaft Helicopters](A5-Catalog-Technologies.md#turboshaft-helicopters-helicopter_2) (`Helicopter_2`) — technology `U_Attack_Helicopter`.

**Built at / carried by:** [Makeshift Airbase](#makeshift-airbase-improvised_airbase), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 1.2 |
| `speed` | 260 |
| `range` | 1 350 |
| `size` | 0.07 |
| `turnspeed` | 18 |
| `maxelevation` | 5 |
| `productioncost` | 1.8 |

**Weapons** (switchable configurations):

- *Attack Helicopter*: no weapons (a technology adds them)
- *Rocket Pod*:
    - [Chaingun](A2-Catalog-Missiles.md#chaingun-chaingun) (`Chaingun`) (×20, salvo 4, reload 0.1 s, auto-engages)
    - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages)
- *ATGM (default)*: [Helicopter ATGM](A2-Catalog-Missiles.md#helicopter-atgm-helicopter-atgm) (`Helicopter ATGM`) (×4, reload 1.3 s, auto-engages, principal)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy) (200 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Enhanced Helicopters](A5-Catalog-Technologies.md#enhanced-helicopters-helicopter_3) (`Helicopter_3`):
    - weapon config “Rocket Pod” becomes:
        - [Chaingun](A2-Catalog-Missiles.md#chaingun-chaingun) (`Chaingun`) (×25, salvo 5, reload 0.1 s, auto-engages)
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages)
    - weapon config “ATGM” becomes:
        - [Helicopter ATGM](A2-Catalog-Missiles.md#helicopter-atgm-helicopter-atgm) (`Helicopter ATGM`) (×8, salvo 2, reload 0.7 s, auto-engages, principal)
    - new appearance
    - `speed` = 325
    - `size` = 0.065
    - `turnspeed` = 24
    - `range` = 1 850
    - `power` = 1.5
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Helicopters](A5-Catalog-Technologies.md#advanced-helicopters-helicopter_4) (`Helicopter_4`):
    - weapon config “Rocket Pod” becomes:
        - [Chaingun](A2-Catalog-Missiles.md#chaingun-chaingun) (`Chaingun`) (×25, salvo 5, reload 0.1 s, auto-engages)
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages)
        - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (×4, reload 2.5 s, auto-engages, off by default)
    - weapon config “ATGM” becomes:
        - [Helicopter ATGM](A2-Catalog-Missiles.md#helicopter-atgm-helicopter-atgm) (`Helicopter ATGM`) (×8, salvo 2, reload 0.5 s, auto-engages, principal)
        - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (×4, reload 2.5 s, auto-engages, off by default)
    - new appearance
    - `speed` = 375
    - `size` = 0.06
    - `turnspeed` = 27
    - `range` = 2 500
    - `power` = 1.75
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Unconventional Rotorcraft](A5-Catalog-Technologies.md#unconventional-rotorcraft-helicopter_5) (`Helicopter_5`):
    - weapon config “Rocket Pod” becomes:
        - [Chaingun](A2-Catalog-Missiles.md#chaingun-chaingun) (`Chaingun`) (×25, salvo 5, reload 0.1 s, auto-engages)
        - [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod) (`Rocket Pod`) (×16, salvo 8, reload 0.2 s, auto-engages)
        - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (×4, reload 2 s, auto-engages, off by default)
    - weapon config “ATGM” becomes:
        - [Helicopter ATGM](A2-Catalog-Missiles.md#helicopter-atgm-helicopter-atgm) (`Helicopter ATGM`) (×8, salvo 4, reload 0.5 s, auto-engages, principal)
        - [MANPADS](A2-Catalog-Missiles.md#manpads-manpad) (`MANPAD`) (×4, reload 2 s, auto-engages, off by default)
    - new appearance
    - `speed` = 550
    - `size` = 0.055
    - `turnspeed` = 30
    - `range` = 4 500
    - `power` = 2

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Helicopter ATGM](A2-Catalog-Missiles.md#helicopter-atgm-helicopter-atgm): [Optically Guided AGMs](A5-Catalog-Technologies.md#optically-guided-agms-improved_agm), [Specialized Precision AGMs](A5-Catalog-Technologies.md#specialized-precision-agms-enhanced_agm), [Autonomous Active Tracking AGMs](A5-Catalog-Technologies.md#autonomous-active-tracking-agms-advanced_agm), [Neural Network Trained AGMs](A5-Catalog-Technologies.md#neural-network-trained-agms-experimental_agm), [Basic Laser Guidance](A5-Catalog-Technologies.md#basic-laser-guidance-basic_laser_guidance), [Advanced Laser Guidance](A5-Catalog-Technologies.md#advanced-laser-guidance-advanced_laser_guidance), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics), [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics), [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics), [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles), [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry)

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Helicopters”](#helicopters-helicopter_modifier) (`Helicopter_Modifier`) (always active):
    - enemy weapons (3): `range` ×0.75
    - enemy [LAAM](A2-Catalog-Missiles.md#laam-laam): `maxelevation` ×0
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100
- [“Helicopters”](#helicopters-helicopter_modifier) (`Helicopter_Modifier`) (always active): enemy [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old): `damage` ×1.2

### EW Aircraft (`EW_Aircraft`)

<!-- img:upgrades Units/Images/Icons/Airborne/EW_Aircraft_1.png=Base|Units/Images/Icons/Airborne/EW_Aircraft_2.png=2nd Generation Aircraft|Units/Images/Icons/Airborne/EW_Aircraft_3.png=3rd Generation Aircraft|Units/Images/Icons/Airborne/EW_Aircraft_4.png=4.5+ Generation Aircraft|Units/Images/Icons/Airborne/EW_Aircraft_5.png=5th Generation Aircraft -->

A combat aircraft equipped with electronic warfare equipment which is capable of jamming enemy radar, making it difficult for them to acquire and shoot down opposing aircraft. They can also be armed with anti-radiation missiles, which home in on radar-emitting units like radar stations, ABM and SAM sites, and jamming vehicles.  
\+ Jams enemy radar.  
\+ Can easily attack SAM and Radar sites.  
\+ Good reconnaissance potential.  
\- Weapons can't lock onto non-radar emitting targets.  
\- Expensive to build, comes in small numbers.  
\- No anti-air weapons.  
\- Limited to carriers and specialized airbases.

**How to get it:** [SEAD/EW Aircraft](A5-Catalog-Technologies.md#seadew-aircraft-jammers_mk2) (`Jammers_Mk2`) — technology `U_EW_Aircraft`.

**Built at / carried by:** [Carrier](#carrier-carrier), [Tactical Airbase](#tactical-airbase-tactical_airbase).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 0.75 |
| `speed` | 600 |
| `range` | 2 200 |
| `size` | 0.1 |
| `turnspeed` | 5 |
| `maxelevation` | 20 |
| `productioncost` | 4.2 |

**Weapons**:

- *Electronic Attack*: [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer) (`EW Jammer`) (×1, principal)

**Sensors:** [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air) (100 km), [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) (400 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [2nd Generation Aircraft](A5-Catalog-Technologies.md#2nd-generation-aircraft-generation_2_aircraft) (`Generation_2_Aircraft`):
    - new appearance
    - `size` = 0.08
    - `speed` = 700
    - `turnspeed` = 7
    - `range` = 2 600
    - `power` = 0.85
    - weapon config “Electronic Attack” becomes:
        - [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer) (`EW Jammer`) (×1, principal)
        - [Anti-Radar Missile](A2-Catalog-Missiles.md#anti-radar-missile-anti-radiation-missile) (`Anti-Radiation Missile`) (×2, reload 4 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave)
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft) (`Generation_3_Aircraft`):
    - new appearance
    - `size` = 0.05
    - `speed` = 800
    - `turnspeed` = 8
    - `range` = 3 000
    - `power` = 0.95
    - weapon config “Electronic Attack” becomes:
        - [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer) (`EW Jammer`) (×1, principal)
        - [Anti-Radar Missile](A2-Catalog-Missiles.md#anti-radar-missile-anti-radiation-missile) (`Anti-Radiation Missile`) (×2, reload 4 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave)
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [4th Generation Aircraft](A5-Catalog-Technologies.md#4th-generation-aircraft-generation_4_aircraft) (`Generation_4_Aircraft`):
    - `size` = 0.03
    - `speed` = 1 000
    - `turnspeed` = 12
    - `range` = 3 500
    - `power` = 1.4
    - weapon config “Electronic Attack” becomes:
        - [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer) (`EW Jammer`) (×1, principal)
        - [Anti-Radar Missile](A2-Catalog-Missiles.md#anti-radar-missile-anti-radiation-missile) (`Anti-Radiation Missile`) (×4, salvo 2, reload 4 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave)
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [4.5+ Generation Aircraft](A5-Catalog-Technologies.md#45-generation-aircraft-generation_45_aircraft) (`Generation_4.5_Aircraft`):
    - new appearance
    - `size` = 0.025
    - `speed` = 1 000
    - `turnspeed` = 14
    - `range` = 3 750
    - `power` = 1.6
    - weapon config “Electronic Attack” becomes:
        - [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer) (`EW Jammer`) (×1, principal)
        - [Anti-Radar Missile](A2-Catalog-Missiles.md#anti-radar-missile-anti-radiation-missile) (`Anti-Radiation Missile`) (×4, salvo 2, reload 3 s, auto-engages)
- With [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`):
    - new appearance
    - `size` = 0.02
    - `speed` = 1 150
    - `turnspeed` = 16
    - `range` = 4 000
    - `power` = 1.85
    - weapon config “Electronic Attack” becomes:
        - [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer) (`EW Jammer`) (×1, off by default, principal)
        - [Anti-Radar Missile](A2-Catalog-Missiles.md#anti-radar-missile-anti-radiation-missile) (`Anti-Radiation Missile`) (×6, salvo 2, reload 2 s, auto-engages)
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`):
    - `size` = 0.015
    - `speed` = 1 250
    - `turnspeed` = 18
    - `range` = 5 000
    - `power` = 2.05
    - weapon config “Electronic Attack” becomes:
        - [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer) (`EW Jammer`) (×1, off by default, principal)
        - [Anti-Radar Missile](A2-Catalog-Missiles.md#anti-radar-missile-anti-radiation-missile) (`Anti-Radiation Missile`) (×8, salvo 4, reload 2 s, auto-engages)
    - sensors become:
        - [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air)
        - [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave)

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): [SEAD/EW Aircraft](A5-Catalog-Technologies.md#seadew-aircraft-jammers_mk2), [DRFM Jamming Systems](A5-Catalog-Technologies.md#drfm-jamming-systems-jammers_mk3), [Advanced AESA Jammers](A5-Catalog-Technologies.md#advanced-aesa-jammers-jammers_mk4)
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave): [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2), [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3), [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4), [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5)

**Sensor vulnerabilities:**

- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Stealth Technology”](#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`) (active after researching [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`)): enemy sensors (12): `range` ×0.6
- [“Advanced Stealth”](#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`) (active after researching [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`)): enemy sensors (12): `range` ×0.75
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

**Other traits:** `Mod_EW_Aircraft`.

### High-Speed Bomber (`High_Speed_Bomber`)

<!-- img:upgrades Units/Images/Icons/Airborne/HS_Bomber_1.png=Base|Units/Images/Icons/Airborne/HS_Bomber_2.png=Late Supersonic Bombers|Units/Images/Icons/Airborne/HS_Bomber_3.png=Sub-Orbital Bombers -->

High-Speed bombers are faster than regular bombers, but tend to have less endurance, are more expensive, require longer runways and depending on the model, may have considerably less range. However, they can still deliver the same heavy payloads and deliver them faster.  
\+ Faster than Long-Range Bombers  
\+ Difficult to intercept with aircraft.  
\+ Can carry heavy weapons.  
\- Vulnerable to SAMs.  
\- Wide turning radius.  
\- No stand-off range weapons.  
\- Low tolerance for damage.  
\- Expensive, requires specialized airbases.

**How to get it:** [Early Supersonic Bombers](A5-Catalog-Technologies.md#early-supersonic-bombers-generation_3_bomber) (`Generation_3_Bomber`) — technology `U_High_Speed_Bomber`.

**Built at / carried by:** [Specialized Airbase](#specialized-airbase-specialized_airport).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 0.8 |
| `speed` | 1 000 |
| `range` | 9 000 |
| `size` | 0.1 |
| `turnspeed` | 3.5 |
| `maxelevation` | 45 |
| `productioncost` | 5 |

**Weapons** (switchable configurations):

- *Heavy Bomb (default)*: [Heavy Bomb](A2-Catalog-Missiles.md#heavy-bomb-heavy-iron-bomb) (`Heavy Iron Bomb`) (×1, auto-engages)
- *100 Kiloton*: [Light 100 Kiloton Bomb](A2-Catalog-Missiles.md#light-100-kiloton-bomb-100kt_nuke_light) (`100kt_nuke_light`) (×1)
- *500 Kiloton*: [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy) (`500kt nuke_heavy`) (×1)
- *10 Megaton*: [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy) (`10M nuke_heavy`) (×1)
- *25 Megaton*: [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy) (`25M nuke_heavy`) (×1)
- *50 Megaton*: [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy) (`50M nuke_heavy`) (×1)
- *100 Megaton*: [Heavy 100M Fusion Bomb](A2-Catalog-Missiles.md#heavy-100m-fusion-bomb-100m-nuke_heavy) (`100M nuke_heavy`) (×1)
- *Chemical Bomb*: [Mustard Gas Bomb](A2-Catalog-Missiles.md#mustard-gas-bomb-chemical_bomb) (`Chemical_bomb`) (×6, salvo 6)
- *Biological Bomb*: [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb) (`Bioweapon_bomb`) (×1)
- *Improved Biological Bomb*: [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb) (`Improved_Bioweapon_bomb`) (×1)
- *Advanced Biological Bomb*: [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb) (`Advanced_Bioweapon_bomb`) (×1)
- *Engineered Biological Bomb*: [EMeVHF-24 Bomb](A2-Catalog-Missiles.md#emevhf-24-bomb-engineered_bioweapon_bomb) (`Engineered_Bioweapon_bomb`) (×1)
- *Cobalt Bomb*: [10 Megaton Cobalt Bomb](A2-Catalog-Missiles.md#10-megaton-cobalt-bomb-cobalt_bomb) (`Cobalt_Bomb`) (×1)
- *Enhanced Salted Bomb*: [10 Megaton Salted Bomb](A2-Catalog-Missiles.md#10-megaton-salted-bomb-salted_bomb) (`Salted_Bomb`) (×1)

**Sensors:** [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air) (100 km), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) (200 km), [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air) (100 km), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision) (100 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Improved Chemical Weapons](A5-Catalog-Technologies.md#improved-chemical-weapons-chemical_weapons_mk2) (`Chemical_Weapons_Mk2`):
    - weapon config “Chemical Bomb” becomes:
        - [Sarin Bomb](A2-Catalog-Missiles.md#sarin-bomb-improved_chemical_bomb) (`Improved_Chemical_bomb`) (×6, salvo 6)
- With [Late Supersonic Bombers](A5-Catalog-Technologies.md#late-supersonic-bombers-generation_4_bomber) (`Generation_4_Bomber`):
    - new appearance
    - `speed` = 1 800
    - `turnspeed` = 5
    - `range` = 16 000
    - `power` = 1
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [Advanced Chemical Weapons](A5-Catalog-Technologies.md#advanced-chemical-weapons-chemical_weapons_mk3) (`Chemical_Weapons_Mk3`):
    - weapon config “Chemical Bomb” becomes:
        - [VX Gas Bomb](A2-Catalog-Missiles.md#vx-gas-bomb-advanced_chemical_bomb) (`Advanced_Chemical_bomb`) (×6, salvo 6)
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99
- With [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem) (`Experimental_Biochem`):
    - weapon config “Chemical Bomb” becomes:
        - [Novichok-2000 Bomb](A2-Catalog-Missiles.md#novichok-2000-bomb-experimental_chemical_bomb) (`Experimental_Chemical_bomb`) (×6, salvo 6)
- With [Sub-Orbital Bombers](A5-Catalog-Technologies.md#sub-orbital-bombers-generation_7_bomber) (`Generation_7_Bomber`):
    - new appearance
    - `speed` = 3 000
    - `size` = 0.08
    - `turnspeed` = 9
    - `range` = 24 000
    - `power` = 1.2
    - `maxelevation` = 60

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy): [Early Thermonuclear Weapons](A5-Catalog-Technologies.md#early-thermonuclear-weapons-thermonuclear_bomb)
- [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy): [Boosted Fission Stages](A5-Catalog-Technologies.md#boosted-fission-stages-mega-warheads)
- [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy): [Advanced Multi-Stage Weapons](A5-Catalog-Technologies.md#advanced-multi-stage-weapons-advanced_multi-stage_weapons)
- [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy): [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb): [Improved Biological Weapons](A5-Catalog-Technologies.md#improved-biological-weapons-biological_weapons_mk2)
- [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb): [Advanced Biological Weapons](A5-Catalog-Technologies.md#advanced-biological-weapons-biological_weapons_mk3)
- [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb): [Experimental Bio/Chemical Weapons](A5-Catalog-Technologies.md#experimental-biochemical-weapons-experimental_biochem)
- [10 Megaton Cobalt Bomb](A2-Catalog-Missiles.md#10-megaton-cobalt-bomb-cobalt_bomb): [Enhanced Salted Weapons](A5-Catalog-Technologies.md#enhanced-salted-weapons-enhanced_salted_weapons)
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

**Other traits:** `AL-ICBM_Range_Adjust`.

### Interceptor (`Interceptor`)

<!-- img:upgrades Units/Images/Icons/Airborne/Interceptor_1.png=Base|Units/Images/Icons/Airborne/Interceptor_2.png=3rd Generation Aircraft|Units/Images/Icons/Airborne/Interceptor_3.png=4th Generation Aircraft|Units/Images/Icons/Airborne/Interceptor_4.png=5th Generation Aircraft -->

Interceptors are designed to quickly reach and confront strategic enemy aircraft and if necessary, destroy them with long-range missiles. They differ from fighters in that they are bigger, faster, longer-ranged and carry heavier weapons, but are less agile and perform poorly at close range.  
Interceptors are best used against distant enemy bombers or AWACs.  
\+ Much faster than other aircraft.  
\+ Can travel and attack from long distances.  
\+ Can be armed with ASAT missiles.  
\+ Can patrol areas, but must launch manually.  
\- Useless against ground targets.  
\- Poor at short range or without radar support.  
\- Cannot target helicopters.  
\- More expensive and less numerous than fighters.

**How to get it:** [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft) (`Interceptor_aircraft`) — technology `U_Interceptor`.

**Built at / carried by:** [Air Base](#air-base-airport), [Specialized Airbase](#specialized-airbase-specialized_airport).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 0.5 |
| `speed` | 1 200 |
| `range` | 3 000 |
| `size` | 0.06 |
| `turnspeed` | 15 |
| `maxelevation` | 45 |
| `productioncost` | 1.5 |

**Weapons** (switchable configurations):

- *Air to Air (default)*: [LAAM](A2-Catalog-Missiles.md#laam-laam) (`LAAM`) (×2, reload 5 s, auto-engages)
- *ASAT*: no weapons (a technology adds them)
- *Nuclear AAM*: [Nuclear AAM](A2-Catalog-Missiles.md#nuclear-aam-nuclear-aam) (`Nuclear AAM`) (×1)
- *Pure Fusion AAM*: [Pure-Fusion AAM](A2-Catalog-Missiles.md#pure-fusion-aam-fusion-aam) (`Fusion AAM`) (×1)

**Sensors:** [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air) (100 km), [SW Targeting Radar](A4-Catalog-Radars.md#sw-targeting-radar-interceptor-short-wave) (250 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft) (`Generation_3_Aircraft`):
    - weapon config “Air to Air” becomes:
        - [LAAM](A2-Catalog-Missiles.md#laam-laam) (`LAAM`) (×4, salvo 2, reload 4 s, auto-engages)
    - new appearance
    - `size` = 0.05
    - `speed` = 1 800
    - `turnspeed` = 20
    - `range` = 5 000
    - `power` = 0.75
- With [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`): `size` ×0.99
- With [4th Generation Aircraft](A5-Catalog-Technologies.md#4th-generation-aircraft-generation_4_aircraft) (`Generation_4_Aircraft`):
    - weapon config “Air to Air” becomes:
        - [LAAM](A2-Catalog-Missiles.md#laam-laam) (`LAAM`) (×4, salvo 2, reload 3 s, auto-engages)
    - weapon config “ASAT” becomes:
        - [Air-Launched ASAT](A2-Catalog-Missiles.md#air-launched-asat-aircraft-asat) (`Aircraft ASAT`) (×1)
    - new appearance
    - `size` = 0.045
    - `speed` = 2 250
    - `turnspeed` = 24
    - `range` = 7 000
    - `power` = 0.9
- With [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`): `size` ×0.99
- With [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`): `size` ×0.99
- With [4.5+ Generation Aircraft](A5-Catalog-Technologies.md#45-generation-aircraft-generation_45_aircraft) (`Generation_4.5_Aircraft`):
    - `size` = 0.04
    - `speed` = 2 500
    - `turnspeed` = 30
    - `range` = 9 000
    - `power` = 1.05
- With [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`):
    - weapon config “Air to Air” becomes:
        - [LAAM](A2-Catalog-Missiles.md#laam-laam) (`LAAM`) (×6, salvo 2, reload 3 s, auto-engages)
    - new appearance
    - `size` = 0.035
    - `speed` = 3 000
    - `turnspeed` = 36
    - `range` = 12 000
    - `power` = 1.2
- With [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`): `size` ×0.99

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [LAAM](A2-Catalog-Missiles.md#laam-laam): [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft), [All-Aspect AAMs](A5-Catalog-Technologies.md#all-aspect-aams-aam_improved), [F&F Radar-Guided AAMs](A5-Catalog-Technologies.md#ff-radar-guided-aams-aam_enhanced), [Off-Boresight Ramjet AAMs](A5-Catalog-Technologies.md#off-boresight-ramjet-aams-aam_advanced), [Advanced Hybrid Guidance AAMs](A5-Catalog-Technologies.md#advanced-hybrid-guidance-aams-aam_experimental), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [Nuclear AAM](A2-Catalog-Missiles.md#nuclear-aam-nuclear-aam): [All-Aspect AAMs](A5-Catalog-Technologies.md#all-aspect-aams-aam_improved), [F&F Radar-Guided AAMs](A5-Catalog-Technologies.md#ff-radar-guided-aams-aam_enhanced), [Off-Boresight Ramjet AAMs](A5-Catalog-Technologies.md#off-boresight-ramjet-aams-aam_advanced), [Advanced Hybrid Guidance AAMs](A5-Catalog-Technologies.md#advanced-hybrid-guidance-aams-aam_experimental), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons), [Early Infrared Air-to-Air Missiles](A5-Catalog-Technologies.md#early-infrared-air-to-air-missiles-air_to_air_missile), [Interceptor Aircraft](A5-Catalog-Technologies.md#interceptor-aircraft-interceptor_aircraft), [Advanced Tactical Nuclear Weapons](A5-Catalog-Technologies.md#advanced-tactical-nuclear-weapons-advanced_tactical_nukes), [Pure Fusion Weapons](A5-Catalog-Technologies.md#pure-fusion-weapons-pure_fusion_weapon)
- [Pure-Fusion AAM](A2-Catalog-Missiles.md#pure-fusion-aam-fusion-aam): [All-Aspect AAMs](A5-Catalog-Technologies.md#all-aspect-aams-aam_improved), [F&F Radar-Guided AAMs](A5-Catalog-Technologies.md#ff-radar-guided-aams-aam_enhanced), [Off-Boresight Ramjet AAMs](A5-Catalog-Technologies.md#off-boresight-ramjet-aams-aam_advanced), [Advanced Hybrid Guidance AAMs](A5-Catalog-Technologies.md#advanced-hybrid-guidance-aams-aam_experimental), [Stealth Weaponry](A5-Catalog-Technologies.md#stealth-weaponry-stealth_weapons)
- [SW Targeting Radar](A4-Catalog-Radars.md#sw-targeting-radar-interceptor-short-wave): [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2), [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3), [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4), [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5)

**Sensor vulnerabilities:**

- [SW Targeting Radar](A4-Catalog-Radars.md#sw-targeting-radar-interceptor-short-wave) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [SW Targeting Radar](A4-Catalog-Radars.md#sw-targeting-radar-interceptor-short-wave) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25
- [“Stealth Technology”](#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`) (active after researching [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`)): enemy sensors (12): `range` ×0.6
- [“Chaff and Flare Countermeasures”](#chaff-and-flare-countermeasures-ecm_bonus_1) (`ECM_Bonus_1`) (active after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Active Missile Interference”](#active-missile-interference-ecm_bonus_2) (`ECM_Bonus_2`) (active after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Advanced Chaff and IR Decoys”](#advanced-chaff-and-ir-decoys-ecm_bonus_3) (`ECM_Bonus_3`) (active after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075
- [“Seeker Blinding Lasers”](#seeker-blinding-lasers-ecm_bonus_4) (`ECM_Bonus_4`) (active after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`)):
    - enemy weapons (14): `damage` ×0.9
    - enemy weapons (14): `precision` ×1.075

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

## Space

### Space Radar (`Space_radar`)

<!-- img:unit Units/Images/Icons/Ground/Space_Radar.png -->

Space Surveillance Radars can detect, track, catalog and identify artificial objects orbiting the Earth. This allows them to identify enemy satellites and their orbits, revealing the enemy's space capabilities and also providing the information needed to deliver a successful anti-satellite strike.  
\+ Can detect enemy satellites.  
\+ Provides ASAT targeting information.  
\- Cannot detect anything else.  
\- No defences, vulnerable.

**How to get it:** [Object Cataloging Space Radar](A5-Catalog-Technologies.md#object-cataloging-space-radar-space_radar) (`Space_radar`) — technology `U_Space_radar`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 5 |
| `size` | 0.5 |
| `productioncost` | 12 |
| `selfdestructtime` | 10 s |

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Space radar (Space Radar)](A4-Catalog-Radars.md#space-radar-space-radar-space_radar) (2 000 km), [Overhorizon Radar (Small Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-small-over-horizon-small_over_horizon) (850 km).

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Space radar (Space Radar)](A4-Catalog-Radars.md#space-radar-space-radar-space_radar): [Actively Tracked Space Radar](A5-Catalog-Technologies.md#actively-tracked-space-radar-space_radar_mk2), [High-Fidelity ASAT Space Radar](A5-Catalog-Technologies.md#high-fidelity-asat-space-radar-space_radar_mk3), [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4)

**Sensor vulnerabilities:**

- [Space radar (Space Radar)](A4-Catalog-Radars.md#space-radar-space-radar-space_radar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Space radar (Space Radar)](A4-Catalog-Radars.md#space-radar-space-radar-space_radar) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- [Overhorizon Radar (Small Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-small-over-horizon-small_over_horizon) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Overhorizon Radar (Small Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-small-over-horizon-small_over_horizon) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25
- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

### Launch Warning Satellite (`Early_Warning_Satellite`)

<!-- img:upgrades Units/Images/Icons/Satellite/EWS_Satellite_1.png=Base|Units/Images/Icons/Satellite/EWS_Satellite_2.png=Improved Launch Warning Satellites -->

A satellite equipped with infrared cameras, designed to detect the thermal signatures of airborne ballistic missiles.  
\+ Can detect nuclear missiles.  
\+ Wider coverage from movement.  
\+ Provides targeting for ABM sites.  
\- Can't detect other units.  
\- Can't monitor a fixed area.

**How to get it:** [Launch Warning Satellites](A5-Catalog-Technologies.md#launch-warning-satellites-launch_warning_satellite) (`Launch_Warning_Satellite`) — technology `U_Satellite_EWS`.

**Built at / carried by:** [Space Center](#space-center-space_operations_center).

| Stat | Base value |
|---|---|
| `type` | Satellite |
| `power` | 1 |
| `size` | 0.175 |
| `maxelevation` | 10 000 |
| `minelevation` | 4 000 |
| `productioncost` | 13.5 |
| `selfdestructtime` | 10 s |

**Sensors:** [Infrared Launch Sensors](A4-Catalog-Radars.md#infrared-launch-sensors-satellite-ews) (0 km), [Maximum Optical Range (Satellite EWS Display)](A4-Catalog-Radars.md#maximum-optical-range-satellite-ews-display-satellite-ews-display) (1 500 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Improved Launch Warning Satellites](A5-Catalog-Technologies.md#improved-launch-warning-satellites-improved_launch_warning_satellite) (`Improved_Launch_Warning_Satellite`): new appearance
- With [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`): `size` ×0.99
- With [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `size` ×0.99

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Maximum Optical Range (Satellite EWS Display)](A4-Catalog-Radars.md#maximum-optical-range-satellite-ews-display-satellite-ews-display): [Improved Launch Warning Satellites](A5-Catalog-Technologies.md#improved-launch-warning-satellites-improved_launch_warning_satellite), [Advanced Launch Warning Satellites](A5-Catalog-Technologies.md#advanced-launch-warning-satellites-advanced_launch_warning_satellite)

**Sensor vulnerabilities:**

- [Infrared Launch Sensors](A4-Catalog-Radars.md#infrared-launch-sensors-satellite-ews) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_invulnerable) (`EMP_Defence_Invulnerable`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

**Other traits:** `Satellite_Stealth_Bonus_Modifier_1`, `Satellite_Stealth_Bonus_Modifier_2`.

### Satellite Relay Center (`Satellite_Relay_Station`)

<!-- img:upgrades Units/Images/Icons/Ground/Satellite_Relay.png=Base|Units/Images/Icons/Ground/Upgraded_Satellite_Relay.png=Electro-Optical Data-linked Satellites -->

A building used to receive and process the intelligence provided by military satellites as well as transmit orders to them when applicable. Satellites will not be able to operate effectively without at least one active. As a result, it's important to build these centers and protect them if you want to maintain your space capabilities!  
\+ Allows satellites to operate at full capacity.  
\+ Can be built multiple times for redundancy.  
\- No defences, easily destroyed.

**How to get it:** [Spy Satellites](A5-Catalog-Technologies.md#spy-satellites-satellite) (`Satellite`) — technology `U_Satellite_Relay`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 2 |
| `size` | 0.1 |
| `productioncost` | 12 |
| `selfdestructtime` | 10 s |

**Weapons**:

- *default*: [Satellite Relay](A2-Catalog-Missiles.md#satellite-relay-satellite-relay) (`Satellite Relay`) (unlimited, off by default)

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km), [Satellite Relay](A4-Catalog-Radars.md#satellite-relay-satellite-relay-range) (20 500 km).

**Upgrades:**

- With [Electro-Optical Data-linked Satellites](A5-Catalog-Technologies.md#electro-optical-data-linked-satellites-improved_optics) (`Improved_optics`): new appearance

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Space Center (`Space_Operations_Center`)

<!-- img:unit Units/Images/Icons/Ground/Space_Center.png -->

A specialized site that has the facilities needed to launch satellites into orbit. Having an active space center will be necessary to build and deploy new satellites.

**How to get it:** [Spy Satellites](A5-Catalog-Technologies.md#spy-satellites-satellite) (`Satellite`) — technology `U_Space_Base`.

| Stat | Base value |
|---|---|
| `type` | Ground |
| `power` | 10 |
| `size` | 0.5 |
| `productioncost` | 24 |
| `selfdestructtime` | 20 s |

**Sensors:** [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision) (50 km).

**Aircraft hosted:** 1 × [Space Shuttle](#space-shuttle-space_shuttle).

**Produces:** [Spy Satellite](#spy-satellite-satellite), [Launch Warning Satellite](#launch-warning-satellite-early_warning_satellite), [Kinetic Strike Satellite](#kinetic-strike-satellite-kinetic_strike_satellite), [Laser Defence Satellite](#laser-defence-satellite-laser_defence_satellite), [Hunter-Killer Satellite](#hunter-killer-satellite-hunter-killer_satellite), [Counterforce Laser Satellite](#counterforce-laser-satellite-countervalue_laser_satellite).

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“BM Accuracy Damage Penalty”](#bm-accuracy-damage-penalty-bm_accuracy_damage_penalty) (`BM_Accuracy_Damage_Penalty`) (always active): enemy weapons (63): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Spy Satellite (`Satellite`)

<!-- img:upgrades Units/Images/Icons/Satellite/Early_Spy_Sat.png=Base|Units/Images/Icons/Satellite/Spy_Satellite.png=Electro-Optical Data-linked Satellites|Units/Images/Icons/Satellite/Stealth_Satellite.png=Novel Stealth Applications -->

A satellite used to gather strategic intelligence by taking photographs of enemy territory from orbit. Spy satellites can only be shot down with specialized weaponry and follow a fixed path.  
\+ Low-risk way of gathering intelligence.  
\+ Hard to destroy without specialized tech.  
\+ Unlimited range, orbits indefinitely.  
\- Less flexible than other units.  
\- Requires a space center to build.  
\- Requires at least one relay center to operate.  
\- Very expensive.

**How to get it:** [Spy Satellites](A5-Catalog-Technologies.md#spy-satellites-satellite) (`Satellite`) — technology `U_Satellite`.

**Built at / carried by:** [Space Center](#space-center-space_operations_center).

| Stat | Base value |
|---|---|
| `type` | Satellite |
| `power` | 1 |
| `size` | 0.175 |
| `maxelevation` | 10 000 |
| `minelevation` | 4 000 |
| `productioncost` | 15 |
| `selfdestructtime` | 10 s |

**Sensors:** [Maximum Optical Range (Satellite Optics Display)](A4-Catalog-Radars.md#maximum-optical-range-satellite-optics-display-satellite-optics-display) (300 km), [Satellite Film Camera](A4-Catalog-Radars.md#satellite-film-camera-satellite-film-camera) (0 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Electro-Optical Data-linked Satellites](A5-Catalog-Technologies.md#electro-optical-data-linked-satellites-improved_optics) (`Improved_optics`):
    - new appearance
    - sensors become:
        - [Digital Spy Camera](A4-Catalog-Radars.md#digital-spy-camera-datalink-satellite-camera)
        - [Maximum Optical Range (Satellite Optics Display)](A4-Catalog-Radars.md#maximum-optical-range-satellite-optics-display-satellite-optics-display)
- With [Real-Time HD Satellites](A5-Catalog-Technologies.md#real-time-hd-satellites-advanced_sat_optics) (`Advanced_Sat_Optics`):
    - sensors become:
        - [HD Spy Camera](A4-Catalog-Radars.md#hd-spy-camera-high-resolution-satellite-camera)
        - [Maximum Optical Range (Satellite Optics Display)](A4-Catalog-Radars.md#maximum-optical-range-satellite-optics-display-satellite-optics-display)
- With [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`):
    - new appearance
    - `size` ×0.99
- With [Ultra-Resolution Streaming Satellites](A5-Catalog-Technologies.md#ultra-resolution-streaming-satellites-experimental_sat_optics) (`Experimental_Sat_Optics`):
    - sensors become:
        - [Ultra-HD Spy Camera](A4-Catalog-Radars.md#ultra-hd-spy-camera-ultra-resolution-satellite-camera)
        - [Maximum Optical Range (Satellite Optics Display)](A4-Catalog-Radars.md#maximum-optical-range-satellite-optics-display-satellite-optics-display)
- With [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `size` ×0.99

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Maximum Optical Range (Satellite Optics Display)](A4-Catalog-Radars.md#maximum-optical-range-satellite-optics-display-satellite-optics-display): [Electro-Optical Data-linked Satellites](A5-Catalog-Technologies.md#electro-optical-data-linked-satellites-improved_optics), [Real-Time HD Satellites](A5-Catalog-Technologies.md#real-time-hd-satellites-advanced_sat_optics), [Ultra-Resolution Streaming Satellites](A5-Catalog-Technologies.md#ultra-resolution-streaming-satellites-experimental_sat_optics)

**Sensor vulnerabilities:**

- [Satellite Film Camera](A4-Catalog-Radars.md#satellite-film-camera-satellite-film-camera) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100

**Other traits:** `Satellite_Stealth_Bonus_Modifier_1`, `Satellite_Stealth_Bonus_Modifier_2`.

### Hunter-Killer Satellite (`Hunter-Killer_Satellite`)

<!-- img:unit Units/Images/Icons/Satellite/Hunter_Killer_Satellite.png -->

A satellite designed specifically to destroy enemy satellites in space-to-space combat. Similarly equipped to a laser defence satellite, except with a more powerful laser, hardened components for increased resistance to laser blinding, and a battery of anti-satellite missiles.  
\+ Can carry long-range ASAT missiles.  
\+ Effective against enemy satellites.  
\+ Can intercept enemy missiles.  
\- Very expensive.  
\- Limited optics, can only see space-borne targets.

**How to get it:** [Space-To-Space Weapons](A5-Catalog-Technologies.md#space-to-space-weapons-space_to_space_weapons) (`Space_to_Space_Weapons`) — technology `U_Hunter-Killer_Satellite`.

**Built at / carried by:** [Space Center](#space-center-space_operations_center).

| Stat | Base value |
|---|---|
| `type` | Satellite |
| `power` | 5 |
| `size` | 0.175 |
| `maxelevation` | 10 000 |
| `minelevation` | 4 000 |
| `productioncost` | 32 |
| `selfdestructtime` | 10 s |

**Weapons**:

- *default*:
    - [Missile Defence Laser](A2-Catalog-Missiles.md#missile-defence-laser-satellite-laser) (`Satellite Laser`) (unlimited, reload 1.3 s, auto-engages)
    - [Satellite ASAT Laser](A2-Catalog-Missiles.md#satellite-asat-laser-asat-laser) (`ASAT Laser`) (unlimited, reload 1.3 s, auto-engages)
    - [Satellite Launched ASAT](A2-Catalog-Missiles.md#satellite-launched-asat-satellite-asat) (`Satellite ASAT`) (×6, reload 10 s, auto-engages)

**Sensors:** [Space radar (Satellite Mini Space Radar)](A4-Catalog-Radars.md#space-radar-satellite-mini-space-radar-satellite_mini_space_radar) (1 000 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`): `size` ×0.99
- With [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `size` ×0.99

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Space radar (Satellite Mini Space Radar)](A4-Catalog-Radars.md#space-radar-satellite-mini-space-radar-satellite_mini_space_radar): [Actively Tracked Space Radar](A5-Catalog-Technologies.md#actively-tracked-space-radar-space_radar_mk2), [High-Fidelity ASAT Space Radar](A5-Catalog-Technologies.md#high-fidelity-asat-space-radar-space_radar_mk3), [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4)

**Sensor vulnerabilities:**

- [Space radar (Satellite Mini Space Radar)](A4-Catalog-Radars.md#space-radar-satellite-mini-space-radar-satellite_mini_space_radar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Space radar (Satellite Mini Space Radar)](A4-Catalog-Radars.md#space-radar-satellite-mini-space-radar-satellite_mini_space_radar) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100
- [“Satellite Defence”](#satellite-defence-satellite_defence) (`Satellite_Defence`) (always active): enemy weapons (5): `canbeintercepted` = 1

**Other traits:** `Satellite_Stealth_Bonus_Modifier_1`, `Satellite_Stealth_Bonus_Modifier_2`.

### Laser Defence Satellite (`Laser_Defence_Satellite`)

<!-- img:unit Units/Images/Icons/Satellite/Laser_Defence_Satellite.png -->

A satellite armed with a high-energy laser, capable of destroying enemy ICBMs and warheads in the midcourse phase of their trajectory. These lasers are also capable of defeating incoming enemy ASAT weapons, and can be upgraded to target other satellites.  
\+ Can destroy enemy missiles.  
\+ Wide coverage due to constant movement.  
\+ Can target enemy satellites with upgrades.  
\- Ineffective for static defence  
\- Limited optics, can only see space-borne targets.

**How to get it:** [Laser Defence Satellites](A5-Catalog-Technologies.md#laser-defence-satellites-satellite_defence_lasers) (`Satellite_Defence_Lasers`) — technology `U_Laser_Defence_Satellite`.

**Built at / carried by:** [Space Center](#space-center-space_operations_center).

| Stat | Base value |
|---|---|
| `type` | Satellite |
| `power` | 2 |
| `size` | 0.175 |
| `maxelevation` | 10 000 |
| `minelevation` | 4 000 |
| `productioncost` | 21 |
| `selfdestructtime` | 10 s |

**Weapons**:

- *default*:
    - [Missile Defence Laser](A2-Catalog-Missiles.md#missile-defence-laser-satellite-laser) (`Satellite Laser`) (unlimited, reload 2 s, auto-engages)
    - [Satellite ASAT Laser](A2-Catalog-Missiles.md#satellite-asat-laser-asat-laser) (`ASAT Laser`) (unlimited, reload 2 s, auto-engages)

**Sensors:** [Space radar (Satellite Mini Space Radar)](A4-Catalog-Radars.md#space-radar-satellite-mini-space-radar-satellite_mini_space_radar) (1 000 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`): `size` ×0.99
- With [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `size` ×0.99

**Weapon and sensor upgrades** (see the weapon and sensor entries):

- [Space radar (Satellite Mini Space Radar)](A4-Catalog-Radars.md#space-radar-satellite-mini-space-radar-satellite_mini_space_radar): [Actively Tracked Space Radar](A5-Catalog-Technologies.md#actively-tracked-space-radar-space_radar_mk2), [High-Fidelity ASAT Space Radar](A5-Catalog-Technologies.md#high-fidelity-asat-space-radar-space_radar_mk3), [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4)

**Sensor vulnerabilities:**

- [Space radar (Satellite Mini Space Radar)](A4-Catalog-Radars.md#space-radar-satellite-mini-space-radar-satellite_mini_space_radar) — While under the lasting effect of EMP Blast: `range`: ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`); ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`); otherwise ×0
- [Space radar (Satellite Mini Space Radar)](A4-Catalog-Radars.md#space-radar-satellite-mini-space-radar-satellite_mini_space_radar) — Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100
- [“Satellite Defence”](#satellite-defence-satellite_defence) (`Satellite_Defence`) (always active): enemy weapons (5): `canbeintercepted` = 1

**Other traits:** `Satellite_Stealth_Bonus_Modifier_1`, `Satellite_Stealth_Bonus_Modifier_2`.

### Kinetic Strike Satellite (`Kinetic_Strike_Satellite`)

<!-- img:unit Units/Images/Icons/Satellite/Kinetic_Satellite.png -->

Kinetic Strike Satellites come equipped with kinetic energy weapons, which are heavy, inert projectiles that crash into the ground with incredible force. Because of their heavy construction, they are not equipped with optics and require commands from a ground station to use their weapons.  
\+ Kinetic strikes can't be stopped.  
\+ Highly effective against surface targets.  
\+ Does not require precision targeting.  
\- Expensive to build.  
\- No space for optics, completely blind.  
\- Ineffective against cities.  
\- Limited ammunition, can't reload.  
\- Cannot fire without a relay station.

**How to get it:** [Orbital Attack Satellites](A5-Catalog-Technologies.md#orbital-attack-satellites-orbital_attack_satellite) (`Orbital_Attack_Satellite`) — technology `U_Satellite_Attack`.

**Built at / carried by:** [Space Center](#space-center-space_operations_center).

| Stat | Base value |
|---|---|
| `type` | Satellite |
| `power` | 2 |
| `size` | 0.175 |
| `maxelevation` | 10 000 |
| `minelevation` | 4 000 |
| `productioncost` | 32 |
| `selfdestructtime` | 10 s |

**Weapons**:

- *default*: [Kinetic Strike Rod](A2-Catalog-Missiles.md#kinetic-strike-rod-orbital-kinetic-bomb) (`Orbital Kinetic Bomb`) (×8)

**Sensors:** [Kinetic Rod Range](A4-Catalog-Radars.md#kinetic-rod-range-kinetic-strike-range) (1 000 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`): `size` ×0.99
- With [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `size` ×0.99

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100
- [“Satellite Defence”](#satellite-defence-satellite_defence) (`Satellite_Defence`) (always active): enemy weapons (5): `canbeintercepted` = 1

**Other traits:** `Satellite_Stealth_Bonus_Modifier_1`, `Satellite_Stealth_Bonus_Modifier_2`.

### Counterforce Laser Satellite (`Countervalue_Laser_Satellite`)

<!-- img:unit Units/Images/Icons/Satellite/DEW_Sat.png -->

An extremely powerful satellite armed with a nuclear-powered direct-energy laser weapon, capable of massively irradiating targets on the Earth's surface and destroying them with extreme heat.  
\+ Effective against surface units.  
\+ Effectively has unlimited ammo.  
\- No space for optics, completely blind.  
\- Requires external precision targeting.  
\- Cannot fire without a relay station.  
\- Highly vulnerable to ASAT weapons.  
\- Extremely expensive.

**How to get it:** [Deadly Laser Weapons](A5-Catalog-Technologies.md#deadly-laser-weapons-offensive_laser_weapons) (`Offensive_Laser_Weapons`) + [Counterforce DEW Satellite](A5-Catalog-Technologies.md#counterforce-dew-satellite-direct_energy_satellite) (`Direct_Energy_Satellite`) — technology `U_Satellite_Death_Laser`.

**Built at / carried by:** [Space Center](#space-center-space_operations_center).

| Stat | Base value |
|---|---|
| `type` | Satellite |
| `power` | 3 |
| `size` | 0.25 |
| `maxelevation` | 10 000 |
| `minelevation` | 4 000 |
| `productioncost` | 72 |
| `selfdestructtime` | 10 s |

**Weapons**:

- *default*: [Space-To-Ground Laser](A2-Catalog-Missiles.md#space-to-ground-laser-fusion-laser) (`Fusion Laser`) (unlimited, reload 0.5 s, auto-engages)

**Sensors:** [Maximum Laser Range](A4-Catalog-Radars.md#maximum-laser-range-dew-range) (1 250 km).

**Upgrades:**

- With [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`): loses the [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) trait
- With [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`): `size` ×0.99
- With [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `size` ×0.99

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Basic EMP Shielding”](#basic-emp-shielding-emp_defence_mod_1) (`EMP_Defence_Mod_1`) (active after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)): enemy EMP Blast: `lastingeffect` ×0.4
- [“Comprehensive EMP Shielding”](#comprehensive-emp-shielding-emp_defence_mod_2) (`EMP_Defence_Mod_2`) (active after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)): enemy EMP Blast: `lastingeffect` ×0.25

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“EMP Killable”](#emp-killable-emp_killable) (`EMP_Killable`) (always active): enemy weapons (8): `damage` = 100
- [“Satellite Defence”](#satellite-defence-satellite_defence) (`Satellite_Defence`) (always active): enemy weapons (5): `canbeintercepted` = 1

**Other traits:** `Satellite_Stealth_Bonus_Modifier_1`, `Satellite_Stealth_Bonus_Modifier_2`.

### Space Shuttle (`Space_Shuttle`)

<!-- img:unit Units/Images/Icons/Satellite/Shuttle.png -->

A spaceflight shuttle designed to carry astronauts, which has been repurposed to deploy special forces from orbit using reentry capsules. It can quickly deliver a special forces team anywhere in the world very quickly and is immune to most weapons when it reaches its operating altitude.  
\+ Can deploy spec-ops anywhere in the world.  
\+ Unlimited range.  
\+ Immune to non-ASAT weapons when at altitude.  
\- No weapons or sensors.  
\- No defenses if attacked.  
\- Expensive.

**How to get it:** [Infantry Orbital Drop Capsules](A5-Catalog-Technologies.md#infantry-orbital-drop-capsules-infantry_orbital_drop_capsules) (`Infantry_Orbital_Drop_Capsules`) — technology `U_Space_Shuttle`.

**Built at / carried by:** [Space Center](#space-center-space_operations_center).

| Stat | Base value |
|---|---|
| `type` | Airborne |
| `power` | 1 |
| `speed` | 3 000 |
| `range` | 48 000 |
| `size` | 0.5 |
| `turnspeed` | 2 |
| `maxelevation` | 120 |
| `productioncost` | 10 |

**Sensors:** [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision) (100 km).

**Can transport:** [Spec-Ops Team](#spec-ops-team-spec_ops_team).

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Space Shuttle”](#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`) (always active): enemy sensors (18): `range` ×0

## Cities

### City values (`VirtualCity`)

Cities produce, research and spy for their faction. Their values change with technologies, DEFCON and effects on the map:

**Upgrades:**

- At DEFCON 4:
    - `production` ×1
    - `science` ×0.85
    - `espionage` ×0.85
- At DEFCON 3:
    - `production` ×0.9
    - `science` ×0.6
    - `espionage` ×0.6
- At DEFCON 2:
    - `production` ×0.75
    - `science` ×0.35
    - `espionage` ×0.35
- At DEFCON 1:
    - `production` ×0.5
    - `science` ×0.1
    - `espionage` ×0.1
- With [Centralized Defence Planning](A5-Catalog-Technologies.md#centralized-defence-planning-defence_planning) (`Defence_Planning`):
    - `production` ×1.05
    - `science` ×1.05
- With [Improved Machine Tools](A5-Catalog-Technologies.md#improved-machine-tools-production_booster_1) (`Production_Booster_1`): `production` ×1.1
- With [Defence Research Agency](A5-Catalog-Technologies.md#defence-research-agency-science_booster_1) (`Science_Booster_1`): `science` ×1.1
- With [Intelligence Organization](A5-Catalog-Technologies.md#intelligence-organization-espionage_1) (`Espionage_1`): `espionage` ×1.125
- With [Computerized Production Operations](A5-Catalog-Technologies.md#computerized-production-operations-production_booster_2) (`Production_Booster_2`): `production` ×1.1
- With [Complex Research Computers](A5-Catalog-Technologies.md#complex-research-computers-science_booster_2) (`Science_Booster_2`): `science` ×1.1
- With [Electronic Spy Gadgets](A5-Catalog-Technologies.md#electronic-spy-gadgets-espionage_2) (`Espionage_2`): `espionage` ×1.125
- With [Globalized Intelligence](A5-Catalog-Technologies.md#globalized-intelligence-espionage_3) (`Espionage_3`): `espionage` ×1.125
- With [Industrial Robotics](A5-Catalog-Technologies.md#industrial-robotics-production_booster_3) (`Production_Booster_3`): `production` ×1.1
- With [Simulated Physics Modelling](A5-Catalog-Technologies.md#simulated-physics-modelling-science_booster_3) (`Science_Booster_3`): `science` ×1.1
- With [Cyber Warfare](A5-Catalog-Technologies.md#cyber-warfare-espionage_4) (`Espionage_4`): `espionage` ×1.125
- With [Advanced 3D Printing](A5-Catalog-Technologies.md#advanced-3d-printing-production_booster_4) (`Production_Booster_4`): `production` ×1.1
- With [Artificial Intelligence Research Aids](A5-Catalog-Technologies.md#artificial-intelligence-research-aids-science_booster_4) (`Science_Booster_4`): `science` ×1.1
- With [Mass OSINT](A5-Catalog-Technologies.md#mass-osint-espionage_5) (`Espionage_5`): `espionage` ×1.125

**Situational effects:**

- While under the lasting effect of EMP Blast:
    - `production`:
        - ×0.75 if you have researched [Advanced Civil EMP Shielding](A5-Catalog-Technologies.md#advanced-civil-emp-shielding-emp_defence_mk4) (`EMP_Defence_Mk4`)
        - otherwise ×0.25
    - `science`:
        - ×0.75 if you have researched [Advanced Civil EMP Shielding](A5-Catalog-Technologies.md#advanced-civil-emp-shielding-emp_defence_mk4) (`EMP_Defence_Mk4`)
        - otherwise ×0.25
    - `espionage`:
        - ×0.75 if you have researched [Advanced Civil EMP Shielding](A5-Catalog-Technologies.md#advanced-civil-emp-shielding-emp_defence_mk4) (`EMP_Defence_Mk4`)
        - otherwise ×0.25
- Inside the range of an active friendly [Research Support](A2-Catalog-Missiles.md#research-support-research_buff): `science` ×1.1
- Inside the range of an active friendly [Espionage Support](A2-Catalog-Missiles.md#espionage-support-espionage_buff): `espionage` ×1.1
- While under the lasting effect of Cyber Warfare effect:
    - `production` ×0.15
    - `science` ×0.15
    - `espionage` ×0

**Protection** (traits that weaken enemy weapons and sensors used against it):

- [“Resist Nuke ABM”](#resist-nuke-abm-resist_nuke_abm) (`Resist_Nuke_ABM`) (always active):
    - enemy weapons (20): `damage` ×0.015
    - enemy [High-Yield Midcourse ABM](A2-Catalog-Missiles.md#high-yield-midcourse-abm-nuclear-abm), [Fusion Midcourse ABM](A2-Catalog-Missiles.md#fusion-midcourse-abm-fusion-abm): `damage` ×0.5
- [“Civil EMP Preparedness”](#civil-emp-preparedness-emp_defence_mod_3) (`EMP_Defence_Mod_3`) (active after researching [Civil EMP Preparedness](A5-Catalog-Technologies.md#civil-emp-preparedness-emp_defence_mk3) (`EMP_Defence_Mk3`)): enemy EMP Blast: `lastingeffect` ×0.5
- [“Advanced Civil EMP Shielding”](#advanced-civil-emp-shielding-emp_defence_mod_4) (`EMP_Defence_Mod_4`) (active after researching [Advanced Civil EMP Shielding](A5-Catalog-Technologies.md#advanced-civil-emp-shielding-emp_defence_mk4) (`EMP_Defence_Mk4`)): enemy EMP Blast: `lastingeffect` ×0.7
- [“Nuclear Survival Plan”](#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`) (active after researching [Nuclear Survival Plan](A5-Catalog-Technologies.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`)): enemy weapons (135): `damage` ×0.85
- [“Emergency Broadcast System”](#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`) (active after researching [Emergency Broadcast System](A5-Catalog-Technologies.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`)): enemy weapons (135): `damage` ×0.85
- [“Public Fallout Shelters”](#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`) (active after researching [Public Fallout Shelters](A5-Catalog-Technologies.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`)): enemy weapons (135): `damage` ×0.875
- [“Civilian CBRN Casualty Treatment”](#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`) (active after researching [Civilian CBRN Casualty Treatment](A5-Catalog-Technologies.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`)): enemy weapons (135): `damage` ×0.9
- [“Web-Based Survival Tools”](#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`) (active after researching [Web-Based Survival Tools](A5-Catalog-Technologies.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`)): enemy weapons (135): `damage` ×0.9
- [“Comprehensive Survival Infrastructure”](#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`) (active after researching [Comprehensive Survival Infrastructure](A5-Catalog-Technologies.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`)): enemy weapons (135): `damage` ×0.9
- [“DEFCON 4”](#defcon-4-defcon_4) (`DEFCON_4`) (active at DEFCON 4): enemy weapons (122): `damage` ×0.9
- [“DEFCON 3”](#defcon-3-defcon_3) (`DEFCON_3`) (active at DEFCON 3): enemy weapons (122): `damage` ×0.75
- [“DEFCON 2”](#defcon-2-defcon_2) (`DEFCON_2`) (active at DEFCON 2): enemy weapons (122): `damage` ×0.65
- [“DEFCON 1”](#defcon-1-defcon_1) (`DEFCON_1`) (active at DEFCON 1): enemy weapons (122): `damage` ×0.5

**Vulnerabilities** (traits that make enemy weapons more effective against it):

- [“Collateral Damage Modifier”](#collateral-damage-modifier-collateral_damage_modifier) (`Collateral_Damage_Modifier`) (always active):
    - enemy weapons (3): `damage` ×1 500 000
    - enemy weapons (4): `damage` ×800 000
    - enemy weapons (5): `damage` ×2 000
    - enemy [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces), [Combined Arms (Land Forces Mobile)](A2-Catalog-Missiles.md#combined-arms-land-forces-mobile-land-forces-mobile): `damage` ×5
- [“Specialized EMP Weapons”](#specialized-emp-weapons-emp_long_stun_modifier) (`EMP_Long_Stun_Modifier`) (always active): enemy EMP Blast: `lastingeffect` ×10

## Traits

Unit traits (`Modifier "tag"` on a unit type) and what they do. A trait works only while its owner knows the technology of the same ID; objects react to it through `AffectedBy Unit` / `ImprovedBy Unit`.

### Active Missile Interference (`ECM_Bonus_2`)

The introduction of more advanced missiles designed to defeat earlier electronic countermeasures like simple chaff and flares necessitated even better protection systems. Using active targeted radar and infrared emitters, it's possible to actively manipulate and confuse the guidance system of an enemy homing missile and mislead it into missing its target. Sudden randomized pulses of energy are sent out and received by the enemy weapon's seeker head, giving it conflicting information about the location and vector of its target which disorients it and may cause it to miss. Enemy missiles that are directly guided by their launcher can also be actively jammed, and if they are unable to receive commands and correct their course, they are very unlikely to hit their mark. Although chaff and flares are still useful, directly and actively attempting to interfere with the guidance system of a weapon is even more likely to fool it and foil an attack.  
Passively reduces the accuracy and damage done by enemy AShMs, SAMs and AAMs.

**Active:** after researching [Active Missile Interference](A5-Catalog-Technologies.md#active-missile-interference-electronic_counters_mk2) (`Electronic_Counters_Mk2`).

**Units with this trait:** [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [Interceptor](#interceptor-interceptor), [Strategic Bomber](#strategic-bomber-bomber), [High-Speed Bomber](#high-speed-bomber-high_speed_bomber), [AWACS](#awacs-awacs), [Carrier AWACS](#carrier-awacs-naval-awacs), [Naval Helicopter](#naval-helicopter-navy_helicopter), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Special Mission Aircraft](#special-mission-aircraft-sof_aircraft), [Attack Helicopter](#attack-helicopter-attack_helicopter), [Carrier](#carrier-carrier), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [EW Aircraft](#ew-aircraft-ew_aircraft), [Air Transport](#air-transport-air_transport), [Landing Ship](#landing-ship-landing_ship), [Resupply Ship](#resupply-ship-resupply_ship).

**Protects against:**

- enemy weapons (14, e.g. [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile), [AAM](A2-Catalog-Missiles.md#aam-aam), [LAAM](A2-Catalog-Missiles.md#laam-laam), [GBU](A2-Catalog-Missiles.md#gbu-gbu)): `damage` ×0.9
- enemy weapons (14, e.g. [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile), [AAM](A2-Catalog-Missiles.md#aam-aam), [LAAM](A2-Catalog-Missiles.md#laam-laam), [GBU](A2-Catalog-Missiles.md#gbu-gbu)): `precision` ×1.075

### Advanced CBRN Equipment (`CBRN_Defence_4`)

Throughout its evolution, all CBRN equipment has had a similar job and performed it in the same way. In essence, stopping the wearer from being exposed to radiation or toxic agents. CBRN defence revolves around exposure prevention, treatment, early warning and decontamination, and the methods for all of them have followed the same principles, only to be improved upon mainly with advances in chemistry and material science. Making CBRN gear more ergonomic, longer-lived and better-protecting will make it even more effective at preventing casualties, while the use of drones and unmanned ground vehicles in tandem with advanced detecting equipment will make it even easier to detect and identify CBRN threats, so they can be addressed even more efficiently.  
Further increases the ability of army divisions, combat engineers, and army bases to withstand nuclear, chemical and biological weapons.

**Active:** after researching [Advanced CBRN Equipment](A5-Catalog-Technologies.md#advanced-cbrn-equipment-cbrn_defence_4) (`CBRN_Defence_4`).

**Units with this trait:** [Army Division (Army Division)](#army-division-army-division-army_division), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Combat Engineers](#combat-engineers-combat_engineers), [Army Base](#army-base-army_base).

**Protects against:**

- enemy weapons (136, e.g. [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile), [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile), [Nuclear AAM](A2-Catalog-Missiles.md#nuclear-aam-nuclear-aam), [Pure-Fusion AAM](A2-Catalog-Missiles.md#pure-fusion-aam-fusion-aam)): `damage` ×0.85

### Advanced Chaff and IR Decoys (`ECM_Bonus_3`)

As missile guidance became smarter and smarter, electronic countermeasures would have to become more sophisticated and illusive to successfully confuse enemy missiles and throw them off course. Improvements to the shape and composition of chaff would allow it to linger in the air for longer periods of time and produce greater, more confusing radar returns. Additionally, broadcasting a jamming signal directly into a cloud of chaff can create a large, convincing false target for missiles. New countermeasure patterns and dispersion strategies were also developed to defeat tracking algorithms, by being more random and harder to discern, as well as attempting to fool the guidance system in a number of ways at multiple points along its course. Countermeasures for other types of guidance other than just infrared and radar would also be developed, and would evolve to a point where even relatively small systems could be protected, diminishing the effectiveness of enemy homing missiles as a whole. Although some missiles will still be able to bypass these countermeasures, advanced ECM will greatly improve the survivability of units threatened by guided missiles.  
Passively reduces the accuracy and damage done by enemy homing missiles, including those used against armies and combat engineers.

**Active:** after researching [Advanced Chaff and IR Decoys](A5-Catalog-Technologies.md#advanced-chaff-and-ir-decoys-electronic_counters_mk3) (`Electronic_Counters_Mk3`).

**Units with this trait:** [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [Interceptor](#interceptor-interceptor), [Strategic Bomber](#strategic-bomber-bomber), [High-Speed Bomber](#high-speed-bomber-high_speed_bomber), [AWACS](#awacs-awacs), [Carrier AWACS](#carrier-awacs-naval-awacs), [Naval Helicopter](#naval-helicopter-navy_helicopter), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Special Mission Aircraft](#special-mission-aircraft-sof_aircraft), [Attack Helicopter](#attack-helicopter-attack_helicopter), [Carrier](#carrier-carrier), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [EW Aircraft](#ew-aircraft-ew_aircraft), [Army Division (Army Division)](#army-division-army-division-army_division), [Combat Engineers](#combat-engineers-combat_engineers), [Air Transport](#air-transport-air_transport), [Landing Ship](#landing-ship-landing_ship), [Resupply Ship](#resupply-ship-resupply_ship).

**Protects against:**

- enemy weapons (14, e.g. [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile), [AAM](A2-Catalog-Missiles.md#aam-aam), [LAAM](A2-Catalog-Missiles.md#laam-laam), [GBU](A2-Catalog-Missiles.md#gbu-gbu)): `damage` ×0.9
- enemy weapons (14, e.g. [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile), [AAM](A2-Catalog-Missiles.md#aam-aam), [LAAM](A2-Catalog-Missiles.md#laam-laam), [GBU](A2-Catalog-Missiles.md#gbu-gbu)): `precision` ×1.075

### Advanced Civil EMP Shielding (`EMP_Defence_Mod_4`)

The advent of new shielding materials and systems will make it economical and practical to protect more and more devices from EMPs. The adoption of decentralized power generation through the widespread use of emergency generators, solar panels, and other alternative energy sources, will keep more of the electrical grid functioning after an attack and allow it to come back online piece by piece even if major powerplants are affected. This will allow more infrastructure to keep operating and reduce the time needed to fix the damage. Although considerable disruptions will still be inevitable, the civilian economy will be in a much better position to continue operating in the wake of an EMP attack with these measures and technologies in place.  
Further shortens the duration of EMP effects on cities. Also lessens the severity of the effects on GDP.

**Active:** after researching [Advanced Civil EMP Shielding](A5-Catalog-Technologies.md#advanced-civil-emp-shielding-emp_defence_mk4) (`EMP_Defence_Mk4`).

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy EMP Blast: `lastingeffect` ×0.7

### Advanced Midcourse ABM (`ABM_Mk3_Modifier`)

The effectiveness of midcourse ABMs is heavily reliant on accurately tracking and predicting the course of the target projectile, and better guidance and tracking systems are needed to get midcourse ABM systems to a point where a single interceptor could reliably attack and engage an incoming warhead. Although accuracy was always the limiting factor for midcourse ABM performance, improved booster and steering systems would also be necessary to give the interceptors the range and finesse they needed to reliably make the flight adjustments to get on a collision course with their targets.  
Further increases the maximum engagement range and effectiveness of midcourse interceptors.

**Active:** after researching [Advanced Midcourse ABM](A5-Catalog-Technologies.md#advanced-midcourse-abm-abm_mk3) (`ABM_Mk3`).

**Units with this trait:** [Midcourse ABM Site](#midcourse-abm-site-abm_site).

**Protects against:**

- enemy weapons (118, e.g. [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun), [Railgun](A2-Catalog-Missiles.md#railgun-railgun), [Anti-Ship Gun](A2-Catalog-Missiles.md#anti-ship-gun-coastal-gun-old), [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile)): `canbeintercepted` ×1.25

### Advanced Sonar (`Advanced_Sonar`)

**Active:** always active.

**Units with this trait:** [SSGN (SSGN)](#ssgn-ssgn-ssgn), [SSBN (SSBN)](#ssbn-ssbn-ssbn).

**Improves its holder:**

- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): `range` ×1.35

### Advanced Stealth (`Aircraft_Stealth_Bonus_Modifier_2`)

Improvements in material science and engineering will make it possible to develop stealth technology even further, and also solve some of the shortcomings and trade-offs that earlier stealth designs had, though the exact details are closely guarded secrets. Systems that can take advantage of these advancements can expect to be even more difficult to detect, and by extension, easier to protect and more dangerous when on the attack.  
Improves the stealth characteristics of satellites and experimental warships, and allows for the development of 6th generation aircraft designs.

**Active:** after researching [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`).

**Units with this trait:** [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [EW Aircraft](#ew-aircraft-ew_aircraft).

**Protects against:**

- enemy sensors (12, e.g. [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave)): `range` ×0.75

### Advanced Stealth (`Bomber_Stealth_Bonus_Modifier_2`)

Improvements in material science and engineering will make it possible to develop stealth technology even further, and also solve some of the shortcomings and trade-offs that earlier stealth designs had, though the exact details are closely guarded secrets. Systems that can take advantage of these advancements can expect to be even more difficult to detect, and by extension, easier to protect and more dangerous when on the attack.  
Improves the stealth characteristics of satellites and experimental warships, and allows for the development of 6th generation aircraft designs.

**Active:** after researching [Advanced Stealth Bombers](A5-Catalog-Technologies.md#advanced-stealth-bombers-generation_6_bomber) (`Generation_6_Bomber`).

**Units with this trait:** [Strategic Bomber](#strategic-bomber-bomber).

**Protects against:**

- enemy sensors (12, e.g. [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave)): `range` ×0.65

### Advanced Stealth (`Warship_Stealth_Bonus_Modifier_2`)

Improvements in material science and engineering will make it possible to develop stealth technology even further, and also solve some of the shortcomings and trade-offs that earlier stealth designs had, though the exact details are closely guarded secrets. Systems that can take advantage of these advancements can expect to be even more difficult to detect, and by extension, easier to protect and more dangerous when on the attack.  
Improves the stealth characteristics of satellites and experimental warships, and allows for the development of 6th generation aircraft designs.

**Active:** after researching [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`) + [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`).

**Units with this trait:** [Carrier](#carrier-carrier), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser).

**Protects against:**

- enemy sensors (12, e.g. [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave)): `range` ×0.75

### Advanced Tactical Optics (`Advanced_Tactical_Optics_EntMod`)

The latest next-generation night-vision and thermal optics allow infantry to operate in near total darkness as if it were only a minor inconvenience, and increasing the reliability and energy efficiency of these systems only makes them more accessible. Concurrently, making thermal and night-vision sights standard on armoured vehicles greatly increases their situational awareness, and by extension, their ability to strike first and perform effectively in combat. Thanks to a combination of electronic weapon sights, laser designators and infrared illuminators, ground forces will be able to spot, mark, relay and engage targets with ease from further away, even with obstructions like thick vegetation or harsh weather obscuring their targets.  
Increases the detection ranges for spec-ops, security checkpoints and army divisions.  
Increases the range of small arms weapons, and slightly increases their accuracy and damage.  
Increases the attack range for army bases and entrenched armies, and slightly increases their accuracy and damage.  
Army divisions will be better at finding covert units.

**Active:** after researching [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`).

**Units with this trait:** [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base).

**Improves its holder:**

- [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces): `range` = 155
- [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery): `range` = 155
- [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery): `range` = 155
- [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery): `range` = 155
- [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery): `range` = 155
- [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery): `range` = 155
- [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery): `range` = 155

### Advanced Terminal ABM (`Terminal_BM_Defence_Mk3_Modifier`)

Terminal ABM systems would need a continuous stream of improvements to provide a credible defence against increasingly sophisticated ballistic and cruise missile threats. The potential threat posed by hypersonic missiles and hypersonic glide vehicles in particular would spur terminal ABM systems to be more responsive and capable, as these new dynamic threats would only offer minutes of warning, meaning that intercepting an unpredictable maneuvering target would have to be achievable with only dozens of seconds to react.  
Further increases the performance and interception rates of terminal ABM systems.

**Active:** after researching [Advanced Terminal ABM](A5-Catalog-Technologies.md#advanced-terminal-abm-terminal_bm_defence_mk3) (`Terminal_BM_Defence_Mk3`).

**Units with this trait:** [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Terminal ABM Site](#terminal-abm-site-terminal_abm).

**Protects against:**

- enemy weapons (117, e.g. [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun), [Railgun](A2-Catalog-Missiles.md#railgun-railgun), [Anti-Ship Gun](A2-Catalog-Missiles.md#anti-ship-gun-coastal-gun-old), [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile)): `canbeintercepted` ×1.3

### AL-ICBM Range Adjust (`AL-ICBM_Range_Adjust`)

**Active:** always active.

**Units with this trait:** [Strategic Bomber](#strategic-bomber-bomber), [High-Speed Bomber](#high-speed-bomber-high_speed_bomber).

**Improves its holder:**

- [250 Kiloton Light ICBM](A2-Catalog-Missiles.md#250-kiloton-light-icbm-icbm-250kt-light): `minrange` = 100
- [500 Kiloton Light ICBM](A2-Catalog-Missiles.md#500-kiloton-light-icbm-icbm-500kt-light): `minrange` = 100
- [Megaton Light ICBM](A2-Catalog-Missiles.md#megaton-light-icbm-icbm-1m-light): `minrange` = 100
- [5 Megaton Light ICBM](A2-Catalog-Missiles.md#5-megaton-light-icbm-icbm-5m-light): `minrange` = 100
- [10M Pure Fusion ICBM](A2-Catalog-Missiles.md#10m-pure-fusion-icbm-icbm-10m-fusion-light): `minrange` = 100
- [1M Light Cobalt ICBM](A2-Catalog-Missiles.md#1m-light-cobalt-icbm-icbm-1m-cobalt): `minrange` = 100
- [1M Light Salted ICBM](A2-Catalog-Missiles.md#1m-light-salted-icbm-icbm-1m-salt): `minrange` = 100
- [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp): `minrange` = 100
- [1M Super EMP ICBM](A2-Catalog-Missiles.md#1m-super-emp-icbm-icbm-1m-super-emp): `minrange` = 100
- [3x250kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x250kt-light-mirv-icbm-3x250kt-light-icbm): `minrange` = 100
- [3x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#3x500kt-light-mirv-icbm-3x500kt-light-icbm): `minrange` = 100
- [8x500kt Light MIRV ICBM](A2-Catalog-Missiles.md#8x500kt-light-mirv-icbm-8x500kt-light-icbm): `minrange` = 100
- [8x1M Light Fusion MIRV](A2-Catalog-Missiles.md#8x1m-light-fusion-mirv-8x1m-light-icbm): `minrange` = 100
- [Rabbit Fever ICBM](A2-Catalog-Missiles.md#rabbit-fever-icbm-bioweapon_icbm): `minrange` = 100
- [Smallpox ICBM](A2-Catalog-Missiles.md#smallpox-icbm-improved_bioweapon_icbm): `minrange` = 100
- [Ebola ICBM](A2-Catalog-Missiles.md#ebola-icbm-advanced_bioweapon_icbm): `minrange` = 100
- [EMeVHF-24 ICBM](A2-Catalog-Missiles.md#emevhf-24-icbm-engineered_bioweapon_icbm): `minrange` = 100

### Antitorpedo (`Antitorpedo`)

**Active:** always active.

**Units with this trait:** [Destroyer](#destroyer-destroyer).

**Protects against:**

- enemy [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo), [Airdropped Torpedo](A2-Catalog-Missiles.md#airdropped-torpedo-air-dropped-torpedo): `precision` ×1.5

### Basic CBRN Defence (`CBRN_Defence_0`)

CBRN stands for Chemical Biological Radiological Nuclear, and CBRN defence seeks to miminize the effects of all of the above. Although chemical defence measures existed as early as 1915, the advent of nuclear weapons had serious implications for armies. Because armies tend to be large, dispersed and often in cover, the raw destructive power of nuclear weapons is often inefficient against army formations as a whole (yet undeniably effective against localized targets) but the threat of nuclear fallout creates new challenges. Although there’s no surviving a nuclear explosion at close range, personnel who aren't killed instantly can protect themselves from radiation, using respirators and specially-designed clothing which minimizes their exposure to hazardous materials and is easily decontaminated, very similarly to existing chemical defense equipment, but with emphasis on resisting radiation and offering full-body coverage.  
Better CBRN Defense equipment will reduce the damage your army divisions, combat engineers and army bases will sustain from nuclear, chemical and biological weapons, but not their survivability against conventional weapons. Invest in this technology if you're expecting chemical or bioweapon attacks, or if your strategy for nuclear war relies on armies!

**Active:** always active.

**Units with this trait:** [Army Division (Army Division)](#army-division-army-division-army_division), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Combat Engineers](#combat-engineers-combat_engineers), [Army Base](#army-base-army_base).

**Protects against:**

- enemy weapons (114, e.g. [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile), [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile), [Nuclear AAM](A2-Catalog-Missiles.md#nuclear-aam-nuclear-aam), [Pure-Fusion AAM](A2-Catalog-Missiles.md#pure-fusion-aam-fusion-aam)): `damage` ×0.5

### Basic CBRN Defence (`CBRN_Defence_1`)

CBRN stands for Chemical Biological Radiological Nuclear, and CBRN defence seeks to miminize the effects of all of the above. Although chemical defence measures existed as early as 1915, the advent of nuclear weapons had serious implications for armies. Because armies tend to be large, dispersed and often in cover, the raw destructive power of nuclear weapons is often inefficient against army formations as a whole (yet undeniably effective against localized targets) but the threat of nuclear fallout creates new challenges. Although there’s no surviving a nuclear explosion at close range, personnel who aren't killed instantly can protect themselves from radiation, using respirators and specially-designed clothing which minimizes their exposure to hazardous materials and is easily decontaminated, very similarly to existing chemical defense equipment, but with emphasis on resisting radiation and offering full-body coverage.  
Better CBRN Defense equipment will reduce the damage your army divisions, combat engineers and army bases will sustain from nuclear, chemical and biological weapons, but not their survivability against conventional weapons. Invest in this technology if you're expecting chemical or bioweapon attacks, or if your strategy for nuclear war relies on armies!

**Active:** after researching [Basic CBRN Defence](A5-Catalog-Technologies.md#basic-cbrn-defence-cbrn_defence_1) (`CBRN_Defence_1`).

**Units with this trait:** [Army Division (Army Division)](#army-division-army-division-army_division), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Combat Engineers](#combat-engineers-combat_engineers), [Army Base](#army-base-army_base).

**Protects against:**

- enemy weapons (136, e.g. [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile), [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile), [Nuclear AAM](A2-Catalog-Missiles.md#nuclear-aam-nuclear-aam), [Pure-Fusion AAM](A2-Catalog-Missiles.md#pure-fusion-aam-fusion-aam)): `damage` ×0.8

### Basic EMP Shielding (`EMP_Defence_Mod_1`)

When a nuclear weapon explodes, it creates an electromagnetic pulse, or EMP, which can disrupt electronic equipment. The EMP effects of nuclear weapons were predicted even before the very first tests were performed, and in fact the equipment at those tests were shielded accordingly. Electronics can be shielded from EMPs by either encasing them with a metal electrical shield to absorb the current, or by hardening the individual components in the electronics that are most likely to be damaged. Protecting the most crucial and vulnerable military electronics from EMPs will minimize the downtime spent repairing them and allow many of them to keep operating, albeit at an impaired capacity. Civilian assets, however, will still be extremely vulnerable.  
Without this technology, many units will be completely stunned when attacked by an EMP and aircraft will crash instantly. Be sure to invest in this if you ever suspect your enemies will develop EMP weapons!  
Reduces the severity and duration of EMP effects on military hardware.

**Active:** after researching [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`).

**Units with this trait:** [Intelligence Center](#intelligence-center-intelligence_center), [Research Center](#research-center-research_center), [Cyber Warfare Center](#cyber-warfare-center-cyber_warfare_center), [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [Interceptor](#interceptor-interceptor), [Strategic Bomber](#strategic-bomber-bomber), [High-Speed Bomber](#high-speed-bomber-high_speed_bomber), [AWACS](#awacs-awacs), [Carrier AWACS](#carrier-awacs-naval-awacs), [Spy Plane](#spy-plane-spy_plane), [Naval Helicopter](#naval-helicopter-navy_helicopter), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Special Mission Aircraft](#special-mission-aircraft-sof_aircraft), [Attack Helicopter](#attack-helicopter-attack_helicopter), [Carrier](#carrier-carrier), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Air Base](#air-base-airport), [Tactical Airbase](#tactical-airbase-tactical_airbase), [Specialized Airbase](#specialized-airbase-specialized_airport), [Coastal Missile Battery](#coastal-missile-battery-coastal), [Fixed Coastal Gun](#fixed-coastal-gun-fixed_coastal_gun), [Radar Site](#radar-site-fixed_lw_radar), [Short-Wave Radar Vehicle](#short-wave-radar-vehicle-mobile_sw_radar), [Naval Monitoring Station](#naval-monitoring-station-naval_monitoring_station), [Over-The-Horizon Radar](#over-the-horizon-radar-over_horizon_radar), [Space Radar](#space-radar-space_radar), [AA Gun Site](#aa-gun-site-aa_site_old), [SAM Site](#sam-site-sam_site), [Midcourse ABM Site](#midcourse-abm-site-abm_site), [Mobile SAM](#mobile-sam-mobile_sam), [Terminal ABM Site](#terminal-abm-site-terminal_abm), [Mobile Defence Laser](#mobile-defence-laser-mobile_abm_laser), [Laser Defence Complex](#laser-defence-complex-laser_defence_complex), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [EW Aircraft](#ew-aircraft-ew_aircraft), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Air Transport](#air-transport-air_transport), [Army Base](#army-base-army_base), [Spy Satellite](#spy-satellite-satellite), [Launch Warning Satellite](#launch-warning-satellite-early_warning_satellite), [Kinetic Strike Satellite](#kinetic-strike-satellite-kinetic_strike_satellite), [Laser Defence Satellite](#laser-defence-satellite-laser_defence_satellite), [Hunter-Killer Satellite](#hunter-killer-satellite-hunter-killer_satellite), [Counterforce Laser Satellite](#counterforce-laser-satellite-countervalue_laser_satellite).

**Protects against:**

- enemy EMP Blast: `lastingeffect` ×0.4

### BM Accuracy Damage Penalty (`BM_Accuracy_Damage_Penalty`)

**Active:** always active.

**Units with this trait:** [Central Command Bunker](#central-command-bunker-central_command_bunker), [Air Base](#air-base-airport), [Tactical Airbase](#tactical-airbase-tactical_airbase), [Makeshift Airbase](#makeshift-airbase-improvised_airbase), [Specialized Airbase](#specialized-airbase-specialized_airport), [Coastal Missile Battery](#coastal-missile-battery-coastal), [Fixed Coastal Gun](#fixed-coastal-gun-fixed_coastal_gun), [MRBM TEL Vehicle](#mrbm-tel-vehicle-mobile_mrbm), [ICBM TEL Vehicle](#icbm-tel-vehicle-mobile_icbm), [Ballistic Missile Site](#ballistic-missile-site-srbm_site), [SRBM TEL Vehicle](#srbm-tel-vehicle-mobile_srbm), [ICBM Launchpad](#icbm-launchpad-icbm_launchpad), [Missile Silo](#missile-silo-missile_silo), [Radar Site](#radar-site-fixed_lw_radar), [Short-Wave Radar Vehicle](#short-wave-radar-vehicle-mobile_sw_radar), [Naval Monitoring Station](#naval-monitoring-station-naval_monitoring_station), [Over-The-Horizon Radar](#over-the-horizon-radar-over_horizon_radar), [Space Radar](#space-radar-space_radar), [AA Gun Site](#aa-gun-site-aa_site_old), [SAM Site](#sam-site-sam_site), [Midcourse ABM Site](#midcourse-abm-site-abm_site), [Mobile SAM](#mobile-sam-mobile_sam), [Terminal ABM Site](#terminal-abm-site-terminal_abm), [Mobile Defence Laser](#mobile-defence-laser-mobile_abm_laser), [Laser Defence Complex](#laser-defence-complex-laser_defence_complex), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [Security Checkpoint](#security-checkpoint-security_checkpoint), [Army Division (Army Division)](#army-division-army-division-army_division), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base), [Space Center](#space-center-space_operations_center), [Satellite Relay Center](#satellite-relay-center-satellite_relay_station).

**Protects against:**

- enemy weapons (63, e.g. [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm), [100 Kiloton MRBM](A2-Catalog-Missiles.md#100-kiloton-mrbm-100kt_mrbm), [250 Kiloton MRBM](A2-Catalog-Missiles.md#250-kiloton-mrbm-250kt_mrbm), [3x100kt MIRV MRBM](A2-Catalog-Missiles.md#3x100kt-mirv-mrbm-3x100kt_mrbm)): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.75 if you have researched [Improved Inertial Guidance](A5-Catalog-Technologies.md#improved-inertial-guidance-improved_inertial_guidance) (`Improved_Inertial_Guidance`); otherwise ×0.25

### Bomb Truck (`Bomb_Truck`) (2)

A civilian cargo truck designed to blend in with regular vehicle traffic. The truck has been modified to carry a heavy bomb, and can discreetly drive to a target site before detonating.

**Active:** always active.

**Units with this trait:** [Bomb Truck](#bomb-truck-bomb_truck), [Heavy Bomb Truck](#heavy-bomb-truck-heavy_bomb_truck).

**Improves its holder:**

- [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy): `range` = 0.5
- [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy): `range` = 0.5
- [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy): `range` = 0.5
- [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy): `range` = 0.5
- [Heavy 100M Fusion Bomb](A2-Catalog-Missiles.md#heavy-100m-fusion-bomb-100m-nuke_heavy): `range` = 0.5
- [Light 100 Kiloton Bomb](A2-Catalog-Missiles.md#light-100-kiloton-bomb-100kt_nuke_light): `range` = 0.5
- [Light 250 Kiloton Bomb](A2-Catalog-Missiles.md#light-250-kiloton-bomb-250kt_nuke_light): `range` = 0.5
- [Light 500 kiloton Bomb](A2-Catalog-Missiles.md#light-500-kiloton-bomb-500kt-nuke_light): `range` = 0.5
- [Light Megaton Bomb](A2-Catalog-Missiles.md#light-megaton-bomb-1m-nuke_light): `range` = 0.5
- [Light 5M Pure Fusion Bomb](A2-Catalog-Missiles.md#light-5m-pure-fusion-bomb-5m-nuke_light): `range` = 0.5
- [10 Megaton Cobalt Bomb](A2-Catalog-Missiles.md#10-megaton-cobalt-bomb-cobalt_bomb): `range` = 0.5
- [10 Megaton Salted Bomb](A2-Catalog-Missiles.md#10-megaton-salted-bomb-salted_bomb): `range` = 0.5
- [Light 500kt Cobalt Bomb](A2-Catalog-Missiles.md#light-500kt-cobalt-bomb-500kt-light-cobalt-bomb): `range` = 0.5
- [Light 500kt Salted Bomb](A2-Catalog-Missiles.md#light-500kt-salted-bomb-500kt-light-salt-bomb): `range` = 0.5
- [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb): `range` = 0.5
- [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb): `range` = 0.5
- [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb): `range` = 0.5
- [EMeVHF-24 Bomb](A2-Catalog-Missiles.md#emevhf-24-bomb-engineered_bioweapon_bomb): `range` = 0.5

### Carrier AWACS (`Naval_AWACS_Mod`)

A lightweight AWACS capable of launching from aircraft carriers. Like the regular AWACS, it can survey a wide area and detect enemy units from long range, but is less capable due to its smaller size.  
\+ Can detect aircraft from long range.  
\+ Some ground surveillance capability.  
\+ Tracks ballistic missiles with EWS upgrade.  
\+ Launches from carriers, good for support.  
\- Unarmed, vulnerable and expensive.  
\- Limited use without supporting units.  
\- Smaller radar range than regular AWACS.  
\- Comparatively poor flight performance.

**Active:** always active.

**Units with this trait:** [Carrier AWACS](#carrier-awacs-naval-awacs).

**Improves its holder:**

- [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong): `range` ×0.75
- [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection): `range` ×0.75
- [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting): `range` ×0.75
- [Overhorizon Radar (AWACS Over Horizon)](A4-Catalog-Radars.md#overhorizon-radar-awacs-over-horizon-awacs_over_horizon): `range` ×0.75

### CBRN Countermeasures (`CBRN_Defence_2`)

As the threat posed by weapons of mass destruction proliferated, increased emphasis would be placed on giving armies the means to survive them. CBRN Defence equipment would improve in its ergonomics and protective properties, but an increased emphasis would be placed on early warning and mitigating the effects of CBRN weapons directly. Chemical detection paper, geiger counters and antidotes for common chemical weapons would become standard-issue in environments where exposure to CBRN threats was expected. Improved systems for decontaminating CBRN-exposed equipment and personnel would also be developed. These improvements would serve to increase the military's capacity to survive and continue operating in CBRN environments, but of course, weapons of mass destruction are never forgiving, and heavy casualties were still expected.  
Increases the ability of army divisions, combat engineers, and army bases to withstand nuclear, chemical and biological weapons.

**Active:** after researching [CBRN Countermeasures](A5-Catalog-Technologies.md#cbrn-countermeasures-cbrn_defence_2) (`CBRN_Defence_2`).

**Units with this trait:** [Army Division (Army Division)](#army-division-army-division-army_division), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Combat Engineers](#combat-engineers-combat_engineers), [Army Base](#army-base-army_base).

**Protects against:**

- enemy weapons (136, e.g. [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile), [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile), [Nuclear AAM](A2-Catalog-Missiles.md#nuclear-aam-nuclear-aam), [Pure-Fusion AAM](A2-Catalog-Missiles.md#pure-fusion-aam-fusion-aam)): `damage` ×0.8

### Chaff and Flare Countermeasures (`ECM_Bonus_1`)

The development of the first homing missiles created an instant demand for protection against them. Given the primitive guidance systems of these new threats, the most practical and readily developable solution to counteract them was to create ways to confuse their guidance systems and make them miss their targets. Radar-reflecting chaff was developed shortly after the proliferation of radar as a means of giving off confusing and misleading radar returns, and was quickly adapted into a countermeasure against radar-seeking missiles once they became prominent. Infrared decoys were also rapidly developed as a way to confuse heatseeking missiles by giving off multiple false heat-signatures. By misleading and confusing the guidance systems of radar and heatseeking weapons, aircraft and surface ships would improve their chances of survival by minimizing their chances of being hit, or causing the weapons to explode at the wrong time or in the wrong place and do minimal damage.  
Passively reduces the accuracy and damage done by enemy AShMs, SAMs and AAMs.

**Active:** after researching [Chaff and Flare Countermeasures](A5-Catalog-Technologies.md#chaff-and-flare-countermeasures-electronic_counters_mk1) (`Electronic_Counters_Mk1`).

**Units with this trait:** [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [Interceptor](#interceptor-interceptor), [Strategic Bomber](#strategic-bomber-bomber), [High-Speed Bomber](#high-speed-bomber-high_speed_bomber), [AWACS](#awacs-awacs), [Carrier AWACS](#carrier-awacs-naval-awacs), [Naval Helicopter](#naval-helicopter-navy_helicopter), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Special Mission Aircraft](#special-mission-aircraft-sof_aircraft), [Attack Helicopter](#attack-helicopter-attack_helicopter), [Carrier](#carrier-carrier), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [EW Aircraft](#ew-aircraft-ew_aircraft), [Air Transport](#air-transport-air_transport), [Landing Ship](#landing-ship-landing_ship), [Resupply Ship](#resupply-ship-resupply_ship).

**Protects against:**

- enemy weapons (14, e.g. [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile), [AAM](A2-Catalog-Missiles.md#aam-aam), [LAAM](A2-Catalog-Missiles.md#laam-laam), [GBU](A2-Catalog-Missiles.md#gbu-gbu)): `damage` ×0.9
- enemy weapons (14, e.g. [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile), [AAM](A2-Catalog-Missiles.md#aam-aam), [LAAM](A2-Catalog-Missiles.md#laam-laam), [GBU](A2-Catalog-Missiles.md#gbu-gbu)): `precision` ×1.075

### Civil EMP Preparedness (`EMP_Defence_Mod_3`)

Although individual electrical components are relatively easy to shield, protecting an entire power grid is a far, far more complicated and demanding endeavor. Attempting to shield the entire power grid would be untenable as almost every component, including power lines, can be affected by an EMP and would have to be shielded, which is not practically feasible. Taking measures to shield the most important and difficult-to-replace infrastructure, as well as planning a surplus of replacement parts, will make it easier to restore and repair the electrical grid in the wake of an EMP attack. Although the effects will still be severe, they won’t be felt for as long.  
Shortens the duration that cities will be affected by EMPs.

**Active:** after researching [Civil EMP Preparedness](A5-Catalog-Technologies.md#civil-emp-preparedness-emp_defence_mk3) (`EMP_Defence_Mk3`).

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy EMP Blast: `lastingeffect` ×0.5

### Civilian CBRN Casualty Treatment (`Survival_Boost_4`)

Weapons of mass destruction often produce casualties with injuries that regular medical personnel aren’t equipped to deal with. Although a nuclear blast is very similar to an upscaled conventional explosion, it also produces nuclear fallout and causes radiation poisoning, which is often poorly understood and difficult to treat. Chemical weapon injuries also require very specific treatment and antidotes, and casualties exposed to contagious bioweapons must be treated carefully to protect others from being infected. Making medicine for WMD victims publicly accessible and preparing first-responders and medical care teams with the training and supplies they need to properly treat casualties will help to ensure that more civilians survive and recover from their injuries. Although even optimistically, the healthcare system will be hard-pressed to withstand a major WMD attack, these tools will be invaluable to whatever is left of it after the fact.  
Further reduces the number of deaths in your cities when hit.

**Active:** after researching [Civilian CBRN Casualty Treatment](A5-Catalog-Technologies.md#civilian-cbrn-casualty-treatment-survival_boost_4) (`Survival_Boost_4`).

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (135, e.g. [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery), [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery), [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery), [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery)): `damage` ×0.9

### Collateral Damage Modifier (`Collateral_Damage_Modifier`)

**Active:** always active.

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Makes more vulnerable to:**

- enemy [Bombs](A2-Catalog-Missiles.md#bombs-free-fall-bomb), [Rocket Pod](A2-Catalog-Missiles.md#rocket-pod-rocket-pod), [GBU](A2-Catalog-Missiles.md#gbu-gbu): `damage` ×1 500 000
- enemy [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun), [SSM](A2-Catalog-Missiles.md#ssm-ssm), [AGM](A2-Catalog-Missiles.md#agm-agm), [ALCM](A2-Catalog-Missiles.md#alcm-alcm): `damage` ×800 000
- enemy [Railgun](A2-Catalog-Missiles.md#railgun-railgun), [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm), [Heavy Bomb](A2-Catalog-Missiles.md#heavy-bomb-heavy-iron-bomb), [SRBM](A2-Catalog-Missiles.md#srbm-srbm), [ALBM](A2-Catalog-Missiles.md#albm-albm): `damage` ×2 000
- enemy [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces), [Combined Arms (Land Forces Mobile)](A2-Catalog-Missiles.md#combined-arms-land-forces-mobile-land-forces-mobile): `damage` ×5

### Comprehensive EMP Shielding (`EMP_Defence_Mod_2`)

Improved EMP shielding techniques, a degree of system redundancy and a greater emphasis on protecting and hardening sensitive components will make it possible to have military assets effectively invulnerable to EMPs, or at least at a state where the effects are negligible or easily dealt with. With this technology, military assets will be very well protected or outright invulnerable against EMP effects. Civilian infrastructure however, will still be largely susceptible and suffer serious productivity losses.  
Greatly reduces the severity and duration of EMP effects on military hardware. High-cost systems will not be affected by EMPs at all.

**Active:** after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`).

**Units with this trait:** [Intelligence Center](#intelligence-center-intelligence_center), [Research Center](#research-center-research_center), [Cyber Warfare Center](#cyber-warfare-center-cyber_warfare_center), [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [Interceptor](#interceptor-interceptor), [Strategic Bomber](#strategic-bomber-bomber), [High-Speed Bomber](#high-speed-bomber-high_speed_bomber), [AWACS](#awacs-awacs), [Carrier AWACS](#carrier-awacs-naval-awacs), [Spy Plane](#spy-plane-spy_plane), [Naval Helicopter](#naval-helicopter-navy_helicopter), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Special Mission Aircraft](#special-mission-aircraft-sof_aircraft), [Attack Helicopter](#attack-helicopter-attack_helicopter), [Carrier](#carrier-carrier), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Air Base](#air-base-airport), [Tactical Airbase](#tactical-airbase-tactical_airbase), [Specialized Airbase](#specialized-airbase-specialized_airport), [Coastal Missile Battery](#coastal-missile-battery-coastal), [Fixed Coastal Gun](#fixed-coastal-gun-fixed_coastal_gun), [Radar Site](#radar-site-fixed_lw_radar), [Short-Wave Radar Vehicle](#short-wave-radar-vehicle-mobile_sw_radar), [Naval Monitoring Station](#naval-monitoring-station-naval_monitoring_station), [Space Radar](#space-radar-space_radar), [AA Gun Site](#aa-gun-site-aa_site_old), [SAM Site](#sam-site-sam_site), [Mobile SAM](#mobile-sam-mobile_sam), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [EW Aircraft](#ew-aircraft-ew_aircraft), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Air Transport](#air-transport-air_transport), [Army Base](#army-base-army_base), [Spy Satellite](#spy-satellite-satellite), [Kinetic Strike Satellite](#kinetic-strike-satellite-kinetic_strike_satellite), [Laser Defence Satellite](#laser-defence-satellite-laser_defence_satellite), [Hunter-Killer Satellite](#hunter-killer-satellite-hunter-killer_satellite), [Counterforce Laser Satellite](#counterforce-laser-satellite-countervalue_laser_satellite).

**Protects against:**

- enemy EMP Blast: `lastingeffect` ×0.25

### Comprehensive EMP Shielding (`EMP_Defence_Invulnerable`)

Improved EMP shielding techniques, a degree of system redundancy and a greater emphasis on protecting and hardening sensitive components will make it possible to have military assets effectively invulnerable to EMPs, or at least at a state where the effects are negligible or easily dealt with. With this technology, military assets will be very well protected or outright invulnerable against EMP effects. Civilian infrastructure however, will still be largely susceptible and suffer serious productivity losses.  
Greatly reduces the severity and duration of EMP effects on military hardware. High-cost systems will not be affected by EMPs at all.

**Active:** after researching [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`).

**Units with this trait:** [Over-The-Horizon Radar](#over-the-horizon-radar-over_horizon_radar), [Midcourse ABM Site](#midcourse-abm-site-abm_site), [Terminal ABM Site](#terminal-abm-site-terminal_abm), [Mobile Defence Laser](#mobile-defence-laser-mobile_abm_laser), [Laser Defence Complex](#laser-defence-complex-laser_defence_complex), [Launch Warning Satellite](#launch-warning-satellite-early_warning_satellite).

**Protects against:**

- enemy EMP Blast: `lastingeffect` ×0

### Comprehensive Survival Infrastructure (`Survival_Boost_6`)

The logistics and preparations needed to shelter thousands of people from the effects of nuclear blasts and the ensuing radiation is no easy feat, but it is possible, provided a tremendous amount of funding and support. Massive hardened underground shelters can be constructed for the public and furnished with the facilities needed to support huge groups of survivors, complete with amenities like independent power generation and electricity, clean water, food supplies, sleeping accommodations and sanitation. Building and maintaining these shelters would take a substantial amount of time, planning and resources, but they would provide civilians who are unable to evacuate with the most ironclad chance at survival available. This infrastructure can also be repurposed to aid the civil power in other disasters as well, such as tornadoes, uncontrollable wildfires, and any other situation where thousands of people could find themselves suddenly displaced and in need of shelter and other necessities. Other measures, like hardening infrastructure like bridges and underground transit, and having clear and well-coordinated evacuation, response and contingency plans, will help prepare the civilian population for the absolute worst to come. Millions of deaths are still inevitable, but there are still many that can hope to be spared.  
Further reduces the number of deaths in your cities when hit.

**Active:** after researching [Comprehensive Survival Infrastructure](A5-Catalog-Technologies.md#comprehensive-survival-infrastructure-survival_boost_6) (`Survival_Boost_6`).

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (135, e.g. [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery), [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery), [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery), [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery)): `damage` ×0.9

### Covert Unit (`Covert_Unit`)

**Active:** always active.

**Units with this trait:** [Cyber Warfare Center](#cyber-warfare-center-cyber_warfare_center), [Spec-Ops Team](#spec-ops-team-spec_ops_team), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Bomb Truck](#bomb-truck-bomb_truck), [Heavy Bomb Truck](#heavy-bomb-truck-heavy_bomb_truck).

**Protects against:**

- enemy [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces), [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `range` ×0
- enemy [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision): `range` ×0.75
- enemy sensors (20, e.g. [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air), [Reconnaissance Camera](A4-Catalog-Radars.md#reconnaissance-camera-spy-plane-camera), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave)): `range` ×0
- enemy [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy): `range` ×1
- enemy [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance): `range` ×0.4
- enemy [Periscope](A4-Catalog-Radars.md#periscope-periscope): `range` ×0.5

**Improves its holder:**

- [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `damage` ×10

### Cyber Warfare Center (`U_Cyber_Warfare_Center`)

A discreet office space staffed by hackers and intelligence operatives with the provisions necessary to conduct anonymous cyber attacks against foreign entities. Cyber Attacks will not trigger war and cannot be traced back to the attacker unless it's possible to deduce who was responsible by other means. This can be useful for subtly weakening your opponent's GDP output without being immediately culpable.  
Different targets are affected by cyber attacks in different ways:  
When used against an enemy city, it temporarily nullifies the espionage capabilites of that city and also reduces its science and espionage GDP outputs.  
When uses against an espionage or research center, it temporarily nullifies the bonuses provided by the building.  
When used against an enemy cyber warfare center, it prevents it from executing an attack of its own.  
\+ Can be used to cripple enemy espionage.  
\+ Can be used to harm enemy GDP outputs.  
\+ Does not reveal itself when attacking.  
\+ Can be built in numbers for greater effect.  
\- No direct offensive capabilities.  
\- Very vulnerable if discovered.  
\- Not dramatic or exciting.

**Active:** after researching [Cyber Warfare](A5-Catalog-Technologies.md#cyber-warfare-espionage_4) (`Espionage_4`).

**Units with this trait:** [Cyber Warfare Center](#cyber-warfare-center-cyber_warfare_center).

**Protects against:**

- enemy [Demolition Charge](A2-Catalog-Missiles.md#demolition-charge-demolition-charge): `range` = 37

### Debuffed Sonar (`Debuffed_Sonar`)

**Active:** always active.

**Units with this trait:** [Cruiser](#cruiser-cruiser).

**Improves its holder:**

- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): `range` ×0.8

### DEFCON 1 (`DEFCON_1`)

DEFCON 1. Maximum readiness.  
Science and Espionage reduced to 10%.  
Production reduced to 50%.  
Armies cost 20% less to produce, before production penalties.  
Cities take greatly reduced damage.  
Best used during total thermonuclear war scenarios where widespread WMD usage is imminent or in progress.

**Active:** at DEFCON 1.

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (122, e.g. [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy), [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy), [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy), [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy)): `damage` ×0.5

### DEFCON 2 (`DEFCON_2`)

DEFCON 2. Very high readiness.  
Science and Espionage reduced to 35%.  
Production reduced to 75%.  
Armies cost 17.5% less to produce, before production penalties.  
Cities take significantly reduced damage.  
Best used during existentially threatening conflicts with a serious WMD threat.

**Active:** at DEFCON 2.

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (122, e.g. [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy), [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy), [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy), [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy)): `damage` ×0.65

### DEFCON 3 (`DEFCON_3`)

DEFCON 3. Heightened readiness.  
Science and Espionage reduced to 60%.  
Production reduced to 90%.  
Armies cost 15% less to produce, before production penalties.  
Cities take moderately less damage.  
Best used during medium or high-intensity conflicts with the potential for WMD usage.

**Active:** at DEFCON 3.

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (122, e.g. [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy), [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy), [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy), [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy)): `damage` ×0.75

### DEFCON 4 (`DEFCON_4`)

DEFCON 4. Above normal readiness.  
Science and Espionage reduced to 85%.  
Armies cost 10% less to produce.  
Cities take slightly less damage.  
Best used during low-intensity conventional conflicts.

**Active:** at DEFCON 4.

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (122, e.g. [Heavy 500 Kiloton Bomb](A2-Catalog-Missiles.md#heavy-500-kiloton-bomb-500kt-nuke_heavy), [Heavy 10 Megaton Bomb](A2-Catalog-Missiles.md#heavy-10-megaton-bomb-10m-nuke_heavy), [Heavy 25 Megaton Bomb](A2-Catalog-Missiles.md#heavy-25-megaton-bomb-25m-nuke_heavy), [Heavy 50 Megaton Bomb](A2-Catalog-Missiles.md#heavy-50-megaton-bomb-50m-nuke_heavy)): `damage` ×0.9

### Early Tactical Optics (`Tactical_Optics_EntMod`)

Increasing the performance of night-vision and thermal optics even further allows them to be directly integrated with fire control systems on vehicles and used in head-mounted goggles and weapon sights by infantry. Rather than being relegated to reconnaissance teams in bulky packages that were difficult to work with, these new optics were less intrusive to use and could be used more frequently and ubiquitously, with many examples being light and ergonomic enough to be used in live combat. Though at this stage, there were still performance gaps to be filled, like battery life, performance and weight, there was a clear advantage to be had in being able to acquire a target and then immediately engage it.  
Increases the detection ranges for spec-ops, security checkpoints and army divisions.  
Increases the range of small arms weapons, and slightly increases their accuracy and damage.  
Increases the attack range for army bases and entrenched armies, and slightly increases their accuracy and damage.  
Army divisions will be better at finding covert units.

**Active:** after researching [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics) (`Tactical_Optics`).

**Units with this trait:** [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base).

**Improves its holder:**

- [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces): `range` = 150
- [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery): `range` = 150
- [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery): `range` = 150
- [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery): `range` = 150
- [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery): `range` = 150
- [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery): `range` = 150
- [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery): `range` = 150

### Emergency Broadcast System (`Survival_Boost_2`)

Preparing the civilian populace for the threat of a nuclear attack is instrumental in reducing the number of casualties in the event that the threat becomes realized, as is ensuring that they're aware it's even happening when the time comes. Educating the public on how to protect themselves during an attack and how to prepare for nuclear fallout will reduce the initial number of casualties, and advance emergency planning will provide a timely response to prevent further losses and restore order. The use of an emergency broadcast system will give citizens a degree of prior warning so they can seek shelter, rather than be caught off-guard in the open and make sure they know what they need to do to maximize their chances of surviving. Although losses are inevitable, setting up the infrastructure to broadcast this information and putting it into a format that's easily digestible will help save lives.  
Further reduces the number of deaths in your cities when hit.

**Active:** after researching [Emergency Broadcast System](A5-Catalog-Technologies.md#emergency-broadcast-system-survival_boost_2) (`Survival_Boost_2`).

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (135, e.g. [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery), [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery), [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery), [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery)): `damage` ×0.85

### EMP Killable (`EMP_Killable`)

**Active:** always active.

**Units with this trait:** [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [Interceptor](#interceptor-interceptor), [Strategic Bomber](#strategic-bomber-bomber), [High-Speed Bomber](#high-speed-bomber-high_speed_bomber), [AWACS](#awacs-awacs), [Carrier AWACS](#carrier-awacs-naval-awacs), [Spy Plane](#spy-plane-spy_plane), [Naval Helicopter](#naval-helicopter-navy_helicopter), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Special Mission Aircraft](#special-mission-aircraft-sof_aircraft), [Attack Helicopter](#attack-helicopter-attack_helicopter), [EW Aircraft](#ew-aircraft-ew_aircraft), [Air Transport](#air-transport-air_transport), [Spy Satellite](#spy-satellite-satellite), [Launch Warning Satellite](#launch-warning-satellite-early_warning_satellite), [Kinetic Strike Satellite](#kinetic-strike-satellite-kinetic_strike_satellite), [Laser Defence Satellite](#laser-defence-satellite-laser_defence_satellite), [Hunter-Killer Satellite](#hunter-killer-satellite-hunter-killer_satellite), [Counterforce Laser Satellite](#counterforce-laser-satellite-countervalue_laser_satellite).

**Makes more vulnerable to:**

- enemy weapons (8, e.g. [Nuclear ASAT](A2-Catalog-Missiles.md#nuclear-asat-nuclear-asat), [500kt EMP MRBM](A2-Catalog-Missiles.md#500kt-emp-mrbm-500kt_mrbm_emp), [500kt Super EMP MRBM](A2-Catalog-Missiles.md#500kt-super-emp-mrbm-500kt_mrbm_emp_super), [1M EMP ICBM](A2-Catalog-Missiles.md#1m-emp-icbm-icbm-1m-emp)): `damage` = 100

### EW Aircraft (`Mod_EW_Aircraft`)

A combat aircraft equipped with electronic warfare equipment which is capable of jamming enemy radar, making it difficult for them to acquire and shoot down opposing aircraft. They can also be armed with anti-radiation missiles, which home in on radar-emitting units like radar stations, ABM and SAM sites, and jamming vehicles.  
\+ Jams enemy radar.  
\+ Can easily attack SAM and Radar sites.  
\+ Good reconnaissance potential.  
\- Weapons can't lock onto non-radar emitting targets.  
\- Expensive to build, comes in small numbers.  
\- No anti-air weapons.  
\- Limited to carriers and specialized airbases.

**Active:** always active.

**Units with this trait:** [EW Aircraft](#ew-aircraft-ew_aircraft).

**Improves its holder:**

- [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.85

### Helicopters (`Helicopter_Modifier`)

After helicopters became a viable means of transportation, their potential for military applications was quickly realized. Despite the shortcomings of early helicopters, the ability to land without a runway and hover in mid-air made them invaluable as a means to rapidly move personnel and equipment, as well as in specialized roles like anti-submarine warfare and close air support. The new capabilities offered by helicopters would revolutionize warfare on land, in the air and at sea.  
Unlocks Spec-Ops Helicopters and Naval Helicopters.

**Active:** always active.

**Units with this trait:** [Naval Helicopter](#naval-helicopter-navy_helicopter), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Attack Helicopter](#attack-helicopter-attack_helicopter).

**Protects against:**

- enemy [AAM](A2-Catalog-Missiles.md#aam-aam), [Nuclear AAM](A2-Catalog-Missiles.md#nuclear-aam-nuclear-aam), [Pure-Fusion AAM](A2-Catalog-Missiles.md#pure-fusion-aam-fusion-aam): `range` ×0.75
- enemy [LAAM](A2-Catalog-Missiles.md#laam-laam): `maxelevation` ×0

**Makes more vulnerable to:**

- enemy [AA Gun](A2-Catalog-Missiles.md#aa-gun-aa-gun-old): `damage` ×1.2

**Improves its holder:**

- [MANPADS](A2-Catalog-Missiles.md#manpads-manpad): `maxelevation` = 6

### Hit-To-Kill Midcourse ABM (`ABM_Mk2_Modifier`)

Early conventional ABMs were seriously lacking in their capabilities given what was at stake, and although, realistically, the idea of any ABM system successfully repelling a mass missile attack is wishful thinking at best, better interceptors would be needed if midcourse ABMs could be relied on without being nuclear-armed. Eventually, once missile guidance systems and tracking radars became advanced enough, hit-to-kill midcourse interceptors could be developed. Rather than relying on conventional explosives or the overwhelming force of a nuclear blast, this generation of interceptors would directly smash into the incoming warhead (which is already moving towards the ground at upwards of Mach 20) and cause it to violently break apart on impact without detonating properly. Although kinetic interceptors will reliably score kills if they can connect, given the incredible speeds involved and the small size of the targets, scoring a direct hit is a daunting and very expensive challenge.  
Increases the maximum engagement range and effectiveness of midcourse interceptors.

**Active:** after researching [Hit-To-Kill Midcourse ABM](A5-Catalog-Technologies.md#hit-to-kill-midcourse-abm-abm_mk2) (`ABM_Mk2`).

**Units with this trait:** [Midcourse ABM Site](#midcourse-abm-site-abm_site).

**Protects against:**

- enemy weapons (118, e.g. [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun), [Railgun](A2-Catalog-Missiles.md#railgun-railgun), [Anti-Ship Gun](A2-Catalog-Missiles.md#anti-ship-gun-coastal-gun-old), [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile)): `canbeintercepted` ×1.3

### Hit-To-Kill Terminal ABM (`Terminal_BM_Defence_Mk2_Modifier`)

Early terminal ballistic missile defences relied on proximity-fused explosive warheads to destroy their targets, but as guidance systems evolved, eventually it would become possible to develop hit-to-kill systems, which directly impact the incoming warhead and more reliably destroy it with kinetic energy. This new capability, along with other general tracking, guidance and control upgrades, would make terminal ABM systems more effective.  
Increases the performance of Terminal ABM systems and improves their interception chance.

**Active:** after researching [Hit-To-Kill Terminal ABM](A5-Catalog-Technologies.md#hit-to-kill-terminal-abm-terminal_bm_defence_mk2) (`Terminal_BM_Defence_Mk2`).

**Units with this trait:** [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Terminal ABM Site](#terminal-abm-site-terminal_abm).

**Protects against:**

- enemy weapons (117, e.g. [Naval Gun](A2-Catalog-Missiles.md#naval-gun-ship-gun), [Railgun](A2-Catalog-Missiles.md#railgun-railgun), [Anti-Ship Gun](A2-Catalog-Missiles.md#anti-ship-gun-coastal-gun-old), [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile)): `canbeintercepted` ×1.3

### Light Unmanned Vehicles (`Light_Unmanned_Vehicles_EntMod`)

The reconnaissance capabilities of a fighting unit can be expanded even further with the use of expendable unmanned vehicles. Using small, remote-controlled robots and throwable UAVs equipped with surveillance equipment, reconnaissance teams will be able to locate and identify enemy activity from more vantage points while also exposing themselves to less danger. The use of these devices will serve to extend the range and efficiency of reconnaissance patrols, as well as provide real-time information on enemy positions in battle.  
Increases the detection ranges for spec-ops, security checkpoints and army divisions.  
Increases the range of small arms weapons, and slightly increases their accuracy and damage.  
Increases the attack range for army bases and entrenched armies, and slightly increases their accuracy and damage.  
Army divisions will be better at finding covert units.

**Active:** after researching [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles) (`Light_Unmanned_Vehicles`).

**Units with this trait:** [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base).

**Improves its holder:**

- [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces): `range` = 160
- [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery): `range` = 160
- [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery): `range` = 160
- [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery): `range` = 160
- [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery): `range` = 160
- [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery): `range` = 160
- [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery): `range` = 160

### Mega Sonar (`Mega_Sonar`)

**Active:** always active.

**Units with this trait:** [Attack Submarine (Submarine)](#attack-submarine-submarine-submarine), [Naval Monitoring Station](#naval-monitoring-station-naval_monitoring_station).

**Improves its holder:**

- [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar): `range` ×1.45

### Naval Target Damage Penalty (`Naval_Target_Damage_Penalty`)

**Active:** always active.

**Units with this trait:** [Carrier](#carrier-carrier), [Attack Submarine (Submarine)](#attack-submarine-submarine-submarine), [SSGN (SSGN)](#ssgn-ssgn-ssgn), [SSBN (SSBN)](#ssbn-ssbn-ssbn), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Landing Ship](#landing-ship-landing_ship), [Resupply Ship](#resupply-ship-resupply_ship).

**Protects against:**

- enemy weapons (63, e.g. [Conventional MRBM](A2-Catalog-Missiles.md#conventional-mrbm-conventional-mrbm), [100 Kiloton MRBM](A2-Catalog-Missiles.md#100-kiloton-mrbm-100kt_mrbm), [250 Kiloton MRBM](A2-Catalog-Missiles.md#250-kiloton-mrbm-250kt_mrbm), [3x100kt MIRV MRBM](A2-Catalog-Missiles.md#3x100kt-mirv-mrbm-3x100kt_mrbm)): `damage`: ×1 if you have researched [Advanced Inertial Guidance](A5-Catalog-Technologies.md#advanced-inertial-guidance-advanced_inertial_guidance) (`Advanced_Inertial_Guidance`); ×0.8 if you have researched [MARV](A5-Catalog-Technologies.md#marv-marv) (`MARV`); otherwise ×0.05

### Novel Stealth Applications (`Warship_Stealth_Bonus_Modifier_1`)

Although it made its debut on combat aircraft, stealth technology has many potential military applications for both offensive and defencive purposes. Stealth technology can be applied to satellites and naval vessels in order to make them harder to detect and engage, which can be a huge advantage in avoiding unwanted encounters or making the first strike, both of which are crucial in the environments they operate in.  
Satellites gain stealth characteristics and are now harder to detect. Allows for the development of cutting-edge stealth warships.

**Active:** after researching [Experimental Stealth Warships](A5-Catalog-Technologies.md#experimental-stealth-warships-experimental_warships) (`Experimental_Warships`).

**Units with this trait:** [Carrier](#carrier-carrier), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser).

**Protects against:**

- enemy sensors (12, e.g. [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave)): `range` ×0.7

### Nuclear Survival Plan (`Survival_Boost_1`)

With the advent of nuclear weapons, the potential for civilian casualties during wartime increased exponentially. Although in fact, the deadliest air raids of WWII inflicted more damage than the first nuclear attacks, an air raid capable of doing such damage requires dozens of bombers carrying hundreds of tonnes of ordnance. Thanks to nuclear weapons, a single plane with a single weapon can kill tens or hundreds of thousands in seconds. Casualty and damage reduction plans would have to be massively reworked to account for the unique threats posed by nuclear weapons.  
Slightly reduces the number of deaths in your cities when hit.  
Partially unlocks the central command bunker, which allows you to set a DEFCON level and potentially reduce casualties at a GDP penalty.

**Active:** after researching [Nuclear Survival Plan](A5-Catalog-Technologies.md#nuclear-survival-plan-survival_boost_1) (`Survival_Boost_1`).

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (135, e.g. [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery), [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery), [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery), [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery)): `damage` ×0.85

### Portable Electronic Optics (`Portable_Electronic_Optics_EntMod`)

In any battle, knowing exactly where the enemy is can mean the difference between a decisive victory and a crushing defeat. Effective ground reconnaissance allows armies and special forces to identify their targets from farther away and engage them earlier. Early night-vision and infrared imagers were big, cumbersome and had limited effectiveness, but they provided an advantage in finding enemy targets at night and in poor conditions. By sizing down these devices to a more manageable size and improving their performance, ground reconnaissance teams can use them to find enemy forces and precisely determine their positions. This increases the situational awareness of their parent unit and allows for more consistent and effective long-range attacks.  
Increases the detection ranges for spec-ops, security checkpoints and army divisions.  
Increases the range of small arms weapons, and slightly increases their accuracy and damage.  
Increases the attack range for army bases and entrenched armies, and slightly increases their accuracy and damage.  
Army divisions will be better at finding covert units.

**Active:** after researching [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics) (`Portable_Electronic_Optics`).

**Units with this trait:** [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base).

**Improves its holder:**

- [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces): `range` = 145
- [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery): `range` = 145
- [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery): `range` = 145
- [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery): `range` = 145
- [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery): `range` = 145
- [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery): `range` = 145
- [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery): `range` = 145

### Public Fallout Shelters (`Survival_Boost_3`)

Further preparations can be made in order to protect the public from the effects of nuclear weapons. Emergency preparedness can be heightened further by researching the expected effects of nuclear weapons on cities and educating and preparing the public accordingly, as well as creating in-depth contingency and survival plans based on detailed attack scenarios. Perhaps more importantly though, the widespread construction of accessible fallout shelters in public buildings and spaces will provide many civilians with a means to protect themselves from being killed in the initial attack, as well as the ensuing nuclear fallout.  
Further reduces the number of deaths in your cities when hit.

**Active:** after researching [Public Fallout Shelters](A5-Catalog-Technologies.md#public-fallout-shelters-survival_boost_3) (`Survival_Boost_3`).

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (135, e.g. [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery), [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery), [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery), [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery)): `damage` ×0.875

### Resist Nuke ABM (`Resist_Nuke_ABM`)

**Active:** always active.

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (20, e.g. [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery), [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery), [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery), [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery)): `damage` ×0.015
- enemy [High-Yield Midcourse ABM](A2-Catalog-Missiles.md#high-yield-midcourse-abm-nuclear-abm), [Fusion Midcourse ABM](A2-Catalog-Missiles.md#fusion-midcourse-abm-fusion-abm): `damage` ×0.5

### Robotic Infantry Aids (`Robotic_Infantry_EntMod`)

With the widespread use of drones and unmanned vehicles, the next logical thing to unman was people themselves. Armed, remote-controlled robots can supplement (but not replace) the ranks of regular infantry as expendable soldiers that can be tasked to do things that would be far too risky for humans to willingly or safely carry out. Having a sacrificable scapegoat for high-risk action is especially valuable for long-range patrols, where the risk of death or capture is especially high, as well as in regular combat situations. Integrated sensors and data fusion can also serve as a force-multiplier for those fighting alongside the robots, as they’ll be able to provide targeting data as they actively fight alongside their unit.  
Increases the detection ranges for spec-ops, security checkpoints and army divisions.  
Increases the range of small arms weapons, and slightly increases their accuracy and damage.  
Increases the attack range for army bases and entrenched armies, and slightly increases their accuracy and damage.  
Army divisions will be better at finding covert units.

**Active:** after researching [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry) (`Robotic_Infantry`).

**Units with this trait:** [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base).

**Improves its holder:**

- [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces): `range` = 165
- [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery): `range` = 165
- [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery): `range` = 165
- [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery): `range` = 165
- [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery): `range` = 165
- [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery): `range` = 165
- [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery): `range` = 165

### Satellite Defence (`Satellite_Defence`)

**Active:** always active.

**Units with this trait:** [Kinetic Strike Satellite](#kinetic-strike-satellite-kinetic_strike_satellite), [Laser Defence Satellite](#laser-defence-satellite-laser_defence_satellite), [Hunter-Killer Satellite](#hunter-killer-satellite-hunter-killer_satellite), [Counterforce Laser Satellite](#counterforce-laser-satellite-countervalue_laser_satellite).

**Makes more vulnerable to:**

- enemy [Nuclear ASAT](A2-Catalog-Missiles.md#nuclear-asat-nuclear-asat), [ASAT](A2-Catalog-Missiles.md#asat-asat), [Satellite Launched ASAT](A2-Catalog-Missiles.md#satellite-launched-asat-satellite-asat), [Air-Launched ASAT](A2-Catalog-Missiles.md#air-launched-asat-aircraft-asat), [Co-Orbital ASAT](A2-Catalog-Missiles.md#co-orbital-asat-co-orbital-asat): `canbeintercepted` = 1

### Seeker Blinding Lasers (`ECM_Bonus_4`)

Sufficiently powerful lasers are capable of blinding the guidance systems on optically-guided missiles, as well as heating up the electrical components on non-optical weapons to a point where they overheat and stop functioning properly. Lasers that are powerful enough to blind or disable (but not destroy) incoming missiles have the potential to offer a relatively lightweight anti-missile active protection system for small platforms like combat aircraft. Although it's not a perfect defence and these weapons may not be able to always dazzle enemy missiles, a successfully damaged and blinded missile is far, far less likely to score a kill than one that's in working order. Combining active blinding with other passive methods like chaff and flares will make it much harder for incoming missiles to hit their mark, but it doesn't guarantee immunity, especially against multiple sufficiently advanced weapons.  
Passively reduces the accuracy and damage done by enemy homing missiles, including those used against armies and combat engineers.

**Active:** after researching [Seeker Blinding Lasers](A5-Catalog-Technologies.md#seeker-blinding-lasers-electronic_counters_mk4) (`Electronic_Counters_Mk4`).

**Units with this trait:** [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [Interceptor](#interceptor-interceptor), [Strategic Bomber](#strategic-bomber-bomber), [High-Speed Bomber](#high-speed-bomber-high_speed_bomber), [AWACS](#awacs-awacs), [Carrier AWACS](#carrier-awacs-naval-awacs), [Naval Helicopter](#naval-helicopter-navy_helicopter), [Spec-Ops Helicopter](#spec-ops-helicopter-spec_ops_helicopter), [Special Mission Aircraft](#special-mission-aircraft-sof_aircraft), [Attack Helicopter](#attack-helicopter-attack_helicopter), [Carrier](#carrier-carrier), [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Jamming Vehicle](#jamming-vehicle-ew_mobile), [EW Aircraft](#ew-aircraft-ew_aircraft), [Army Division (Army Division)](#army-division-army-division-army_division), [Combat Engineers](#combat-engineers-combat_engineers), [Air Transport](#air-transport-air_transport), [Landing Ship](#landing-ship-landing_ship), [Resupply Ship](#resupply-ship-resupply_ship).

**Protects against:**

- enemy weapons (14, e.g. [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile), [AAM](A2-Catalog-Missiles.md#aam-aam), [LAAM](A2-Catalog-Missiles.md#laam-laam), [GBU](A2-Catalog-Missiles.md#gbu-gbu)): `damage` ×0.9
- enemy weapons (14, e.g. [AShM](A2-Catalog-Missiles.md#ashm-anti-ship-missile), [AAM](A2-Catalog-Missiles.md#aam-aam), [LAAM](A2-Catalog-Missiles.md#laam-laam), [GBU](A2-Catalog-Missiles.md#gbu-gbu)): `precision` ×1.075

### Sonar Quieting SSBN 1 (`Sonar_Quieting_SSBN_1`)

**Active:** always active.

**Units with this trait:** [SSBN (SSBN)](#ssbn-ssbn-ssbn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.95

### Sonar Quieting SSBN 2 (`Sonar_Quieting_SSBN_2`)

**Active:** after researching [Improved SSBN](A5-Catalog-Technologies.md#improved-ssbn-improved_ssbn) (`Improved_SSBN`).

**Units with this trait:** [SSBN (SSBN)](#ssbn-ssbn-ssbn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSBN 3 (`Sonar_Quieting_SSBN_3`)

**Active:** after researching [Advanced SSBN](A5-Catalog-Technologies.md#advanced-ssbn-advanced_ssbn) (`Advanced_SSBN`).

**Units with this trait:** [SSBN (SSBN)](#ssbn-ssbn-ssbn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.766

### Sonar Quieting SSBN 4 (`Sonar_Quieting_SSBN_4`)

**Active:** after researching [Experimental SSBN](A5-Catalog-Technologies.md#experimental-ssbn-experimental_ssbn) (`Experimental_SSBN`).

**Units with this trait:** [SSBN (SSBN)](#ssbn-ssbn-ssbn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSGN 1 (`Sonar_Quieting_SSGN_1`)

**Active:** after researching [Nuclear Submarines](A5-Catalog-Technologies.md#nuclear-submarines-nuclear_submarine) (`Nuclear_Submarine`).

**Units with this trait:** [SSGN (SSGN)](#ssgn-ssgn-ssgn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.95

### Sonar Quieting SSGN 2 (`Sonar_Quieting_SSGN_2`)

**Active:** after researching [Improved Submarines](A5-Catalog-Technologies.md#improved-submarines-improved_submarines) (`Improved_Submarines`).

**Units with this trait:** [SSGN (SSGN)](#ssgn-ssgn-ssgn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSGN 3 (`Sonar_Quieting_SSGN_3`)

**Active:** after researching [Submarine Midlife Upgrades](A5-Catalog-Technologies.md#submarine-midlife-upgrades-enhanced_submarines) (`Enhanced_Submarines`).

**Units with this trait:** [SSGN (SSGN)](#ssgn-ssgn-ssgn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSGN 4 (`Sonar_Quieting_SSGN_4`)

**Active:** after researching [Advanced Submarines](A5-Catalog-Technologies.md#advanced-submarines-advanced_submarines) (`Advanced_Submarines`).

**Units with this trait:** [SSGN (SSGN)](#ssgn-ssgn-ssgn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSGN 5 (`Sonar_Quieting_SSGN_5`)

**Active:** after researching [Experimental Submarines](A5-Catalog-Technologies.md#experimental-submarines-experimental_submarines) (`Experimental_Submarines`).

**Units with this trait:** [SSGN (SSGN)](#ssgn-ssgn-ssgn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSN 1 (`Sonar_Quieting_SSN_1`)

**Active:** after researching [Nuclear Submarines](A5-Catalog-Technologies.md#nuclear-submarines-nuclear_submarine) (`Nuclear_Submarine`).

**Units with this trait:** [Attack Submarine (Submarine)](#attack-submarine-submarine-submarine).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.95

### Sonar Quieting SSN 2 (`Sonar_Quieting_SSN_2`)

**Active:** after researching [Improved Submarines](A5-Catalog-Technologies.md#improved-submarines-improved_submarines) (`Improved_Submarines`).

**Units with this trait:** [Attack Submarine (Submarine)](#attack-submarine-submarine-submarine).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSN 3 (`Sonar_Quieting_SSN_3`)

**Active:** after researching [Submarine Midlife Upgrades](A5-Catalog-Technologies.md#submarine-midlife-upgrades-enhanced_submarines) (`Enhanced_Submarines`).

**Units with this trait:** [Attack Submarine (Submarine)](#attack-submarine-submarine-submarine).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSN 4 (`Sonar_Quieting_SSN_4`)

**Active:** after researching [Advanced Submarines](A5-Catalog-Technologies.md#advanced-submarines-advanced_submarines) (`Advanced_Submarines`).

**Units with this trait:** [Attack Submarine (Submarine)](#attack-submarine-submarine-submarine).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Sonar Quieting SSN 5 (`Sonar_Quieting_SSN_5`)

**Active:** after researching [Experimental Submarines](A5-Catalog-Technologies.md#experimental-submarines-experimental_submarines) (`Experimental_Submarines`).

**Units with this trait:** [Attack Submarine (Submarine)](#attack-submarine-submarine-submarine).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.875

### Space Shuttle (`Space_Shuttle_Mod`)

A spaceflight shuttle designed to carry astronauts, which has been repurposed to deploy special forces from orbit using reentry capsules. It can quickly deliver a special forces team anywhere in the world very quickly and is immune to most weapons when it reaches its operating altitude.  
\+ Can deploy spec-ops anywhere in the world.  
\+ Unlimited range.  
\+ Immune to non-ASAT weapons when at altitude.  
\- No weapons or sensors.  
\- No defenses if attacked.  
\- Expensive.

**Active:** always active.

**Units with this trait:** [Space Shuttle](#space-shuttle-space_shuttle).

**Protects against:**

- enemy sensors (18, e.g. [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision), [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision), [Reconnaissance Camera](A4-Catalog-Radars.md#reconnaissance-camera-spy-plane-camera)): `range` ×0

### Specialized CBRN Reconnaissance (`CBRN_Defence_3`)

Increasingly potent chemical agents and the growing risk posed by tactical nuclear weapons, especially neutron bombs, spurred further developments in CBRN defence technology and doctrine. With the extreme lethality of modern nerve agents and the innate danger of radiation, the best defence is often to avoid or minimize exposure to the threats in the first place. Specialized CBRN reconnaissance vehicles would be developed specifically for the task of identifying chemical agents and evaluating the risk posed by radiological threats, which by extension would allow other units to be more prepared. Improved decontamination systems and ad-hoc CBRN specialist units would also aid in minimizing casualties in the event of a WMD strike, and also extend the longevity of CBRN equipment in a contaminated environment and ensure replacements were available.  
Further increases the ability of army divisions, combat engineers, and army bases to withstand nuclear, chemical and biological weapons.

**Active:** after researching [Specialized CBRN Reconnaissance](A5-Catalog-Technologies.md#specialized-cbrn-reconnaissance-cbrn_defence_3) (`CBRN_Defence_3`).

**Units with this trait:** [Army Division (Army Division)](#army-division-army-division-army_division), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Combat Engineers](#combat-engineers-combat_engineers), [Army Base](#army-base-army_base).

**Protects against:**

- enemy weapons (136, e.g. [Nuclear SSM](A2-Catalog-Missiles.md#nuclear-ssm-nuclear-cruise-missile), [Fusion SSM](A2-Catalog-Missiles.md#fusion-ssm-fusion-cruise-missile), [Nuclear AAM](A2-Catalog-Missiles.md#nuclear-aam-nuclear-aam), [Pure-Fusion AAM](A2-Catalog-Missiles.md#pure-fusion-aam-fusion-aam)): `damage` ×0.85

### Specialized EMP Weapons (`EMP_Long_Stun_Modifier`)

Nuclear explosions release a burst of electromagnetic energy known as an electromagnetic pulse, or EMP, which results in rapidly changing electric and magnetic fields that can damage and disable electronic equipment. At high altitudes, this EMP interacts with the Earth’s magnetic field and ionizes some of the atmosphere, which dramatically increases the EMP’s effects and range. Specialized high altitude EMP weapons, known as HEMPs, are nuclear weapons that explode at altitudes of around 400km in order to maximize this effect and knock out electrical infrastructure like communications and power grids. Although military equipment can be electrically shielded to protect against EMPs, most civilian electronics are vulnerable.  
Unlocks EMP weapons, which will stun certain enemy units without electrical protection, as well dramatically affect the economic outputs of enemy cities within a wide radius. Stunned units will have no sensor capabilities, which prevents them from using weapons that require precise targeting.

**Active:** always active.

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Makes more vulnerable to:**

- enemy EMP Blast: `lastingeffect` ×10

### Spy Plane (`Spy_Plane_Modifier`)

Spy planes are designed to perform high-altitude photo reconnaissance and identify the location of enemy strategic assets. They can only be engaged by long-range anti-air missiles like those fired by strategic SAM sites and combat aircraft. With the appropriate aircraft technology they can upgrade to supersonic models which are extremely difficult to intercept.  
\+ Can locate enemy units.  
\+ Immune to short-range SAMs and gunfire.  
\+ Undetectable by basic radar.  
\+ Can upgrade to high-speed variants.  
\+ Cheaper and more controllable than satellites.  
\- No weapons.  
\- Requires a specialized airbase.

**Active:** always active.

**Units with this trait:** [Spy Plane](#spy-plane-spy_plane).

**Protects against:**

- enemy [STD Vision](A4-Catalog-Radars.md#std-vision-std-vision), [STD Vision Air](A4-Catalog-Radars.md#std-vision-air-std-vision-air), [Air Vision](A4-Catalog-Radars.md#air-vision-air-vision), [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance), [Submarine Radar Mast](A4-Catalog-Radars.md#submarine-radar-mast-submarine-radar-mast): `range` ×0
- enemy [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave), [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave), [Air Targeting](A4-Catalog-Radars.md#air-targeting-awacs-air-targeting): `range`: ×1 if you have researched [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`); ×0.85 if you have researched [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`); ×0.7 if you have researched [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`); otherwise ×0.1
- enemy [Search Radar (STD Long Wave)](A4-Catalog-Radars.md#search-radar-std-long-wave-std-long-wave), [Search Radar (Fixed Long Wave)](A4-Catalog-Radars.md#search-radar-fixed-long-wave-fixed-long-wave), [Ground Detection](A4-Catalog-Radars.md#ground-detection-awacs-long-wave), [Air Detection](A4-Catalog-Radars.md#air-detection-awacs-air-detection): `range`: ×1 if you have researched [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`); ×0.85 if you have researched [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`); ×0.7 if you have researched [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`); otherwise ×0.1

### Static Defender Bonus (`Static_Defender_Bonus`)

**Active:** always active.

**Units with this trait:** [Laser Defence Complex](#laser-defence-complex-laser_defence_complex), [Security Checkpoint](#security-checkpoint-security_checkpoint), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Army Base](#army-base-army_base).

**Improves its holder:**

- [Combined Arms (Land Forces)](A2-Catalog-Missiles.md#combined-arms-land-forces-land-forces): `range` = 140
- [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery): `range` = 140
- [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery): `range` = 140
- [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery): `range` = 140
- [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery): `range` = 140
- [VX Gas Artillery](A2-Catalog-Missiles.md#vx-gas-artillery-advanced-chemical-artillery): `range` = 140
- [Novichok-2000 Artillery](A2-Catalog-Missiles.md#novichok-2000-artillery-experimental-chemical-artillery): `range` = 140
- [Small Arms](A2-Catalog-Missiles.md#small-arms-small-arms): `range` ×1.25
- [Terminal Defence Laser](A2-Catalog-Missiles.md#terminal-defence-laser-terminal-abm-laser): `range` = 275

### Stealth Technology (`Aircraft_Stealth_Bonus_Modifier_1`)

Although the concept of 'stealth' in the traditional sense greatly predates human history, in the recent military context, it refers to a suite of features that render an object or a system difficult to observe or track using conventional methods like radar or thermal imaging. Stealth technology generally relies on radar-absorbing material, a distorting profile that minimizes radar returns and a number of other features designed to stop the object in question from reflecting radar and revealing its position. In military applications, this has obvious benefits as it makes the user much more difficult to find and destroy, and ensures they can keep the element of surprise for much longer.  
Basic stealth technology is a prerequisite to build stealth bombers and 5th generation aircraft.

**Active:** after researching [5th Generation Aircraft](A5-Catalog-Technologies.md#5th-generation-aircraft-generation_5_aircraft) (`Generation_5_Aircraft`).

**Units with this trait:** [Fighter](#fighter-fighter), [Multirole Attacker](#multirole-attacker-attack), [Interceptor](#interceptor-interceptor), [EW Aircraft](#ew-aircraft-ew_aircraft).

**Protects against:**

- enemy sensors (12, e.g. [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave)): `range` ×0.6

### Stealth Technology (`Bomber_Stealth_Bonus_Modifier_1`)

Although the concept of 'stealth' in the traditional sense greatly predates human history, in the recent military context, it refers to a suite of features that render an object or a system difficult to observe or track using conventional methods like radar or thermal imaging. Stealth technology generally relies on radar-absorbing material, a distorting profile that minimizes radar returns and a number of other features designed to stop the object in question from reflecting radar and revealing its position. In military applications, this has obvious benefits as it makes the user much more difficult to find and destroy, and ensures they can keep the element of surprise for much longer.  
Basic stealth technology is a prerequisite to build stealth bombers and 5th generation aircraft.

**Active:** after researching [Stealth Bombers](A5-Catalog-Technologies.md#stealth-bombers-generation_5_bomber) (`Generation_5_Bomber`).

**Units with this trait:** [Strategic Bomber](#strategic-bomber-bomber).

**Protects against:**

- enemy sensors (12, e.g. [Special Reconnaissance](A4-Catalog-Radars.md#special-reconnaissance-counter-spy), [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance), [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave)): `range` ×0.55

### Submarine Stealth (`Submarine_Stealth`)

**Active:** always active.

**Units with this trait:** [Attack Submarine (Submarine)](#attack-submarine-submarine-submarine).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.8

**Improves its holder:**

- [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): `range` ×1.1
- [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): `damage` ×1.35
- [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): `precision` ×0.85

### Submarine Stealth Weak (`Submarine_Stealth_Weak`)

**Active:** always active.

**Units with this trait:** [SSGN (SSGN)](#ssgn-ssgn-ssgn), [SSBN (SSBN)](#ssbn-ssbn-ssbn).

**Protects against:**

- enemy [Sonar (Sonar)](A4-Catalog-Radars.md#sonar-sonar-sonar), [Sonar (AWACS Sonar)](A4-Catalog-Radars.md#sonar-awacs-sonar-awacs-sonar): `range` ×0.9

### Terminal Ballistic Missile Defences (`Terminal_ABM_No_Target_Decoy_Modifier`)

A terminal anti-ballistic missile system is a defencive weapon designed to intercept and destroy incoming ballistic warheads in the last phase of their trajectory, just minutes or seconds before they hit their targets. In order to be effective, terminal ABM systems need a high-degree of precision, advance warning, and incredible acceleration characteristics to intercept and destroy their targets before they can hit. Operating at relatively short ranges gives terminal defence systems a limited window to operate, making them best used as a last-resort to protect priority point targets like major cities or military installations. Because of their short, in-atmosphere operating ranges, they can discern between decoys (which are less dense and fall more slowly in air) and genuine targets. They're very effective within their range, but can't defeat multiple warheads at once, and should be used along with midcourse ABM systems for maximum effectiveness. They'll also require some form of missile detection to operate as well!  
Unlocks mobile Terminal ABM sites, and adds terminal ABMs to advanced destroyers and cruisers. Terminal ABMs are not affected by decoy warheads.

**Active:** always active.

**Units with this trait:** [Destroyer](#destroyer-destroyer), [Cruiser](#cruiser-cruiser), [Terminal ABM Site](#terminal-abm-site-terminal_abm), [Mobile Defence Laser](#mobile-defence-laser-mobile_abm_laser), [Laser Defence Complex](#laser-defence-complex-laser_defence_complex).

**Makes more vulnerable to:**

- enemy [Decoy Warhead](A2-Catalog-Missiles.md#decoy-warhead-false-icbm-warhead): `canbeintercepted` = 0

### Torpedo Net Mod (`Torpedo_Net_Mod`)

**Active:** always active.

**Units with this trait:** [Naval Monitoring Station](#naval-monitoring-station-naval_monitoring_station).

**Protects against:**

- enemy [Torpedo](A2-Catalog-Missiles.md#torpedo-torpedo): `damage` ×0.35

### Underground (`Underground`)

**Active:** always active.

**Units with this trait:** [Missile Silo](#missile-silo-missile_silo).

**Protects against:**

- enemy [Ground Reconnaissance](A4-Catalog-Radars.md#ground-reconnaissance-reconnaissance), [High-Power Quantum Radar](A4-Catalog-Radars.md#high-power-quantum-radar-quantum-radar-strong), [Quantum Radar](A4-Catalog-Radars.md#quantum-radar-quantum-radar-weak): `range` ×0.75
- enemy sensors (11, e.g. [Targeting Radar (STD Short Wave)](A4-Catalog-Radars.md#targeting-radar-std-short-wave-std-short-wave), [Targeting Radar (Fixed Short Wave)](A4-Catalog-Radars.md#targeting-radar-fixed-short-wave-fixed-short-wave), [Ground Targeting](A4-Catalog-Radars.md#ground-targeting-awacs-short-wave), [SW Targeting Radar](A4-Catalog-Radars.md#sw-targeting-radar-interceptor-short-wave)): `range` ×0.5
- enemy [Satellite Film Camera](A4-Catalog-Radars.md#satellite-film-camera-satellite-film-camera), [Digital Spy Camera](A4-Catalog-Radars.md#digital-spy-camera-datalink-satellite-camera), [HD Spy Camera](A4-Catalog-Radars.md#hd-spy-camera-high-resolution-satellite-camera), [Ultra-HD Spy Camera](A4-Catalog-Radars.md#ultra-hd-spy-camera-ultra-resolution-satellite-camera), [Kinetic Rod Range](A4-Catalog-Radars.md#kinetic-rod-range-kinetic-strike-range), [Maximum Laser Range](A4-Catalog-Radars.md#maximum-laser-range-dew-range): `range` ×0.25

### Unit BioChem Modifier (`Unit_BioChem_Modifier`)

**Active:** always active.

**Units with this trait:** [Army Division (Army Division)](#army-division-army-division-army_division), [Forward Operating Base](#forward-operating-base-forward_operating_base), [Combat Engineers](#combat-engineers-combat_engineers), [Army Base](#army-base-army_base).

**Makes more vulnerable to:**

- enemy weapons (13, e.g. [Rabbit Fever Bomb](A2-Catalog-Missiles.md#rabbit-fever-bomb-bioweapon_bomb), [Smallpox Bomb](A2-Catalog-Missiles.md#smallpox-bomb-improved_bioweapon_bomb), [Ebola Bomb](A2-Catalog-Missiles.md#ebola-bomb-advanced_bioweapon_bomb), [Rabbit Fever MRBM](A2-Catalog-Missiles.md#rabbit-fever-mrbm-bioweapon_mrbm)): `damage` ×7.5

### Web-Based Survival Tools (`Survival_Boost_5`)

Thanks to the internet, it’s possible to transmit information all over the world in a matter of seconds. Exploiting the ubiquity of the internet and mass communication, instructions can easily be transmitted to civilians in the event of an attack which will help to ensure they take appropriate action as well as quell the ensuing panic and chaos. The internet also allows everyone to have an easily accessible repository of information that can help them survive in a nuclear war, which will improve their odds further. It will take time and effort to harden the information infrastructure enough to still be somewhat reliable in the wake of a nuclear attack, as well as leverage it properly to inform the public, but doing so will ensure that everyone has access to the information they need to maximize their chances.  
Further reduces the number of deaths in your cities when hit.

**Active:** after researching [Web-Based Survival Tools](A5-Catalog-Technologies.md#web-based-survival-tools-survival_boost_5) (`Survival_Boost_5`).

**Units with this trait:** [VirtualCity](#city-values-virtualcity).

**Protects against:**

- enemy weapons (135, e.g. [Nuclear Artillery](A2-Catalog-Missiles.md#nuclear-artillery-nuclear-artillery), [Fusion Artillery](A2-Catalog-Missiles.md#fusion-artillery-fusion-artillery), [Mustard Gas Artillery](A2-Catalog-Missiles.md#mustard-gas-artillery-chemical-artillery), [Sarin Artillery](A2-Catalog-Missiles.md#sarin-artillery-improved-chemical-artillery)): `damage` ×0.9
