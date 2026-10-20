# Catalog A4 — Sensors (radars)

Every `[RADAR]`: display name, template, range, altitude ceiling, what it detects, carriers, upgrades, and the traits (stealth, cover) and effects (jamming, EMP) that reduce it.

### Air Vision (`Air Vision`)

**Technology:** `R_Air_Default`; template `AirDetectionSW`.

**Carried by:** [Fighter](A1-Catalog-Units.md#fighter-fighter), [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Naval Helicopter](A1-Catalog-Units.md#naval-helicopter-navy_helicopter), [Special Mission Aircraft](A1-Catalog-Units.md#special-mission-aircraft-sof_aircraft), [Air Transport](A1-Catalog-Units.md#air-transport-air_transport), [Space Shuttle](A1-Catalog-Units.md#space-shuttle-space_shuttle).

**Detects:** ships, aircraft, missiles.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 100 |
| `maxheight` | 100 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.75: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)
- `range` ×0: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

### Digital Spy Camera (`Datalink Satellite Camera`)

A digital satellite camera that can transmit its data to a control center.

**Technology:** `R_Data_Sat_Camera`; template `DataSat`.

**Carried by:** [Spy Satellite](A1-Catalog-Units.md#spy-satellite-satellite).

**Detects:** ground units, ships, aircraft.

| Stat | Base value |
|---|---|
| `range` | 0 |
| `maxheight` | 3 000 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.25: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

**Jamming and other effects:**

- Inside the range of an active friendly [Satellite Relay](A2-Catalog-Missiles.md#satellite-relay-satellite-relay): `range` = 600
- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Ground Reconnaissance (`Reconnaissance`)

Coverage by reconnaissance forces.

**Technology:** `R_Reconnaissance`; template `ShortWave`.

**Carried by:** [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Forward Operating Base](A1-Catalog-Units.md#forward-operating-base-forward_operating_base).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 125 |
| `maxheight` | 100 |

**Upgrades:**

- With [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics) (`Portable_Electronic_Optics`): `range` = 150
- With [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics) (`Tactical_Optics`): `range` = 175
- With [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`): `range` = 200
- With [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles) (`Light_Unmanned_Vehicles`): `range` = 225
- With [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry) (`Robotic_Infantry`): `range` = 250

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`), [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range` ×0: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)
- `range` ×0.4: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

### HD Spy Camera (`High-Resolution Satellite Camera`)

A high-definition surveillance camera that streams data in real time.

**Technology:** `R_HD_Sat_Camera`; template `DataSat2`.

**Carried by:** [Spy Satellite](A1-Catalog-Units.md#spy-satellite-satellite).

**Detects:** ground units, ships, aircraft, ballistic missiles in flight.

**Special:** provides precise targeting, reveals launch positions.

| Stat | Base value |
|---|---|
| `range` | 0 |
| `maxheight` | 3 000 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.25: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

**Jamming and other effects:**

- Inside the range of an active friendly [Satellite Relay](A2-Catalog-Missiles.md#satellite-relay-satellite-relay): `range` = 1 200
- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Infrared Launch Sensors (`Satellite EWS`)

Detects nuclear missiles from space.

**Technology:** `R_Satellite_EWS`; template `OverHorizon`.

**Carried by:** [Launch Warning Satellite](A1-Catalog-Units.md#launch-warning-satellite-early_warning_satellite).

**Detects:** ballistic missiles in flight.

**Special:** provides precise targeting, reveals launch positions.

| Stat | Base value |
|---|---|
| `range` | 0 |
| `maxheight` | 3 000 |

**Jamming and other effects:**

- Inside the range of an active friendly [Satellite Relay](A2-Catalog-Missiles.md#satellite-relay-satellite-relay):
    - `range`:
        - = 7 250 if you have researched [Advanced Launch Warning Satellites](A5-Catalog-Technologies.md#advanced-launch-warning-satellites-advanced_launch_warning_satellite) (`Advanced_Launch_Warning_Satellite`)
        - = 4 000 if you have researched [Improved Launch Warning Satellites](A5-Catalog-Technologies.md#improved-launch-warning-satellites-improved_launch_warning_satellite) (`Improved_Launch_Warning_Satellite`)
        - otherwise = 1 500
- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Kinetic Rod Range (`Kinetic Strike Range`)

The maximum effective range of the kinetic strike rods.

**Technology:** `R_Kinetic_Range`; template `DummySat`.

**Carried by:** [Kinetic Strike Satellite](A1-Catalog-Units.md#kinetic-strike-satellite-kinetic_strike_satellite).

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `maxheight` | 3 000 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.25: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

### Maximum Laser Range (`DEW Range`)

The maximum effective range of the laser.

**Technology:** `R_DEW_Range`; template `DummySat`.

**Carried by:** [Counterforce Laser Satellite](A1-Catalog-Units.md#counterforce-laser-satellite-countervalue_laser_satellite).

| Stat | Base value |
|---|---|
| `range` | 1 250 |
| `maxheight` | 3 000 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.25: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

### Maximum Optical Range (Satellite EWS Display) (`Satellite EWS Display`)

The maximum range of this unit's optics when supported by a satellite relay center.

**Technology:** `R_Dummy_EWS_Camera`; template `DummySat`.

**Carried by:** [Launch Warning Satellite](A1-Catalog-Units.md#launch-warning-satellite-early_warning_satellite).

| Stat | Base value |
|---|---|
| `range` | 1 500 |
| `maxheight` | 100 |

**Upgrades:**

- With [Improved Launch Warning Satellites](A5-Catalog-Technologies.md#improved-launch-warning-satellites-improved_launch_warning_satellite) (`Improved_Launch_Warning_Satellite`): `range` = 4 000
- With [Advanced Launch Warning Satellites](A5-Catalog-Technologies.md#advanced-launch-warning-satellites-advanced_launch_warning_satellite) (`Advanced_Launch_Warning_Satellite`): `range` = 7 250

### Maximum Optical Range (Satellite Optics Display) (`Satellite Optics Display`)

The maximum range of this unit's optics when supported by a satellite relay center.

**Technology:** `R_Dummy_Sat_Camera`; template `DummySat`.

**Carried by:** [Spy Satellite](A1-Catalog-Units.md#spy-satellite-satellite).

| Stat | Base value |
|---|---|
| `range` | 300 |
| `maxheight` | 100 |

**Upgrades:**

- With [Electro-Optical Data-linked Satellites](A5-Catalog-Technologies.md#electro-optical-data-linked-satellites-improved_optics) (`Improved_optics`): `range` = 600
- With [Real-Time HD Satellites](A5-Catalog-Technologies.md#real-time-hd-satellites-advanced_sat_optics) (`Advanced_Sat_Optics`): `range` = 1 200
- With [Ultra-Resolution Streaming Satellites](A5-Catalog-Technologies.md#ultra-resolution-streaming-satellites-experimental_sat_optics) (`Experimental_Sat_Optics`): `range` = 1 750

### Occupation Zone Finder (`Occupation Zone Finder`)

**Technology:** `R_Occupation_Zone_Finder`; template `OccupationZoneFinder`.

**Carried by:** [Special Mission Aircraft](A1-Catalog-Units.md#special-mission-aircraft-sof_aircraft), [Air Transport](A1-Catalog-Units.md#air-transport-air_transport), [Landing Ship](A1-Catalog-Units.md#landing-ship-landing_ship).

**Detects:** Army Division (Army Division), Army Base.

| Stat | Base value |
|---|---|
| `range` | 130 |
| `maxheight` | 100 |

### Periscope (`Periscope`)

A periscope. Allows submarines to see land targets in a short radius.

**Technology:** `R_Periscope`; template `Optical`.

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 100 |
| `maxheight` | 100 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`), [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)
- `range` ×0: [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

### Reconnaissance Camera (`Spy Plane Camera`)

A spy plane reconnaissance camera.

**Technology:** `R_Spy_Plane_Camera`; template `Optical`.

**Carried by:** [Spy Plane](A1-Catalog-Units.md#spy-plane-spy_plane).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 150 |
| `maxheight` | 100 |

**Upgrades:**

- With [3rd Generation Aircraft](A5-Catalog-Technologies.md#3rd-generation-aircraft-generation_3_aircraft) (`Generation_3_Aircraft`): `range` = 160
- With [6th Generation Aircraft](A5-Catalog-Technologies.md#6th-generation-aircraft-generation_6_aircraft) (`Generation_6_Aircraft`): `range` = 175

**Against targets with these traits** (stealth, cover…):

- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Resupply Range (Resupply Range FOB) (`Resupply Range FOB`)

The distance that this unit can resupply other units from.

**Technology:** `R_Resupply_FOB`; template `Resupply`.

**Carried by:** [Forward Operating Base](A1-Catalog-Units.md#forward-operating-base-forward_operating_base), [Army Base](A1-Catalog-Units.md#army-base-army_base).

| Stat | Base value |
|---|---|
| `range` | 150 |
| `maxheight` | 100 |

### Resupply Range (Resupply Range) (`Resupply Range`)

The distance that this unit can resupply other units from.

**Technology:** `R_Resupply`; template `Resupply`.

**Carried by:** [Resupply Ship](A1-Catalog-Units.md#resupply-ship-resupply_ship).

| Stat | Base value |
|---|---|
| `range` | 225 |
| `maxheight` | 100 |

### Satellite Film Camera (`Satellite Film Camera`)

A very early film-based satellite camera.

**Technology:** `R_Basic_Sat_Camera`; template `FilmSat`.

**Carried by:** [Spy Satellite](A1-Catalog-Units.md#spy-satellite-satellite).

**Detects:** ground units.

| Stat | Base value |
|---|---|
| `range` | 0 |
| `maxheight` | 3 000 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.25: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

**Jamming and other effects:**

- Inside the range of an active friendly [Satellite Relay](A2-Catalog-Missiles.md#satellite-relay-satellite-relay): `range` = 300
- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Satellite Relay (`Satellite Relay Range`)

Sends and receives satellite communications which allows satellites to operate effectively.

**Technology:** `R_Satellite_Relay`; template `Resupply`.

**Carried by:** [Satellite Relay Center](A1-Catalog-Units.md#satellite-relay-center-satellite_relay_station).

| Stat | Base value |
|---|---|
| `range` | 20 500 |
| `maxheight` | 100 |

### Search Radar (Fixed Long Wave) (`Fixed Long Wave`)

**Technology:** `R_Long_wave_radar`; template `LongWave`.

**Carried by:** [Radar Site](A1-Catalog-Units.md#radar-site-fixed_lw_radar), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 550 |
| `maxheight` | 100 |

**Upgrades:**

- With [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`):
    - `range` = 725
    - `maxheight` = 250
- With [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`):
    - `range` = 850
    - `maxheight` = 300
- With [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`):
    - `range` = 1 000
    - `maxheight` = 400
- With [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5) (`LW_Mk5`):
    - `range` = 1 250
    - `maxheight` = 500

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range`: ×1 if you have researched [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`); ×0.85 if you have researched [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`); ×0.7 if you have researched [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`); otherwise ×0.1: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Search Radar (STD Long Wave) (`STD Long Wave`)

**Technology:** `R_Long_wave_radar`; template `LongWave`.

**Carried by:** [Carrier](A1-Catalog-Units.md#carrier-carrier), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Air Base](A1-Catalog-Units.md#air-base-airport), [Tactical Airbase](A1-Catalog-Units.md#tactical-airbase-tactical_airbase), [Specialized Airbase](A1-Catalog-Units.md#specialized-airbase-specialized_airport), [Coastal Missile Battery](A1-Catalog-Units.md#coastal-missile-battery-coastal), [Fixed Coastal Gun](A1-Catalog-Units.md#fixed-coastal-gun-fixed_coastal_gun), [EW Aircraft](A1-Catalog-Units.md#ew-aircraft-ew_aircraft).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 400 |
| `maxheight` | 100 |

**Upgrades:**

- With [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`):
    - `range` = 450
    - `maxheight` = 250
- With [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`):
    - `range` = 500
    - `maxheight` = 300
- With [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`):
    - `range` = 600
    - `maxheight` = 400
- With [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5) (`LW_Mk5`):
    - `range` = 700
    - `maxheight` = 500

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range`: ×1 if you have researched [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`); ×0.85 if you have researched [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`); ×0.7 if you have researched [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`); otherwise ×0.1: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Sonar (AWACS Sonar) (`AWACS Sonar`)

**Technology:** `R_Sonar`; template `Sonar`.

**Carried by:** [Naval Helicopter](A1-Catalog-Units.md#naval-helicopter-navy_helicopter).

**Detects:** ships, submarines, underwater missiles.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 150 |
| `maxheight` | 100 |

**Upgrades:**

- With [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2) (`Sonar_Mk2`): `range` ×1.2
- With [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3) (`Sonar_Mk3`): `range` ×1.2
- With [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4) (`Sonar_Mk4`): `range` ×1.2
- With [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5) (`Sonar_Mk5`): `range` ×1.2

**Against targets with these traits** (stealth, cover…):

- `range` ×0.8: [“Submarine Stealth”](A1-Catalog-Units.md#submarine-stealth-submarine_stealth) (`Submarine_Stealth`)
- `range` ×0.9: [“Submarine Stealth Weak”](A1-Catalog-Units.md#submarine-stealth-weak-submarine_stealth_weak) (`Submarine_Stealth_Weak`)
- `range` ×0.95: [“Sonar Quieting SSN 1”](A1-Catalog-Units.md#sonar-quieting-ssn-1-sonar_quieting_ssn_1) (`Sonar_Quieting_SSN_1`), [“Sonar Quieting SSGN 1”](A1-Catalog-Units.md#sonar-quieting-ssgn-1-sonar_quieting_ssgn_1) (`Sonar_Quieting_SSGN_1`), [“Sonar Quieting SSBN 1”](A1-Catalog-Units.md#sonar-quieting-ssbn-1-sonar_quieting_ssbn_1) (`Sonar_Quieting_SSBN_1`)
- `range` ×0.875: [“Sonar Quieting SSN 2”](A1-Catalog-Units.md#sonar-quieting-ssn-2-sonar_quieting_ssn_2) (`Sonar_Quieting_SSN_2`), [“Sonar Quieting SSN 3”](A1-Catalog-Units.md#sonar-quieting-ssn-3-sonar_quieting_ssn_3) (`Sonar_Quieting_SSN_3`), [“Sonar Quieting SSN 4”](A1-Catalog-Units.md#sonar-quieting-ssn-4-sonar_quieting_ssn_4) (`Sonar_Quieting_SSN_4`), [“Sonar Quieting SSN 5”](A1-Catalog-Units.md#sonar-quieting-ssn-5-sonar_quieting_ssn_5) (`Sonar_Quieting_SSN_5`), [“Sonar Quieting SSGN 2”](A1-Catalog-Units.md#sonar-quieting-ssgn-2-sonar_quieting_ssgn_2) (`Sonar_Quieting_SSGN_2`), [“Sonar Quieting SSGN 3”](A1-Catalog-Units.md#sonar-quieting-ssgn-3-sonar_quieting_ssgn_3) (`Sonar_Quieting_SSGN_3`), [“Sonar Quieting SSGN 4”](A1-Catalog-Units.md#sonar-quieting-ssgn-4-sonar_quieting_ssgn_4) (`Sonar_Quieting_SSGN_4`), [“Sonar Quieting SSGN 5”](A1-Catalog-Units.md#sonar-quieting-ssgn-5-sonar_quieting_ssgn_5) (`Sonar_Quieting_SSGN_5`), [“Sonar Quieting SSBN 2”](A1-Catalog-Units.md#sonar-quieting-ssbn-2-sonar_quieting_ssbn_2) (`Sonar_Quieting_SSBN_2`), [“Sonar Quieting SSBN 4”](A1-Catalog-Units.md#sonar-quieting-ssbn-4-sonar_quieting_ssbn_4) (`Sonar_Quieting_SSBN_4`)
- `range` ×0.766: [“Sonar Quieting SSBN 3”](A1-Catalog-Units.md#sonar-quieting-ssbn-3-sonar_quieting_ssbn_3) (`Sonar_Quieting_SSBN_3`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Sonar (Sonar) (`Sonar`)

**Technology:** `R_Sonar`; template `Sonar`.

**Carried by:** [Attack Submarine (Submarine)](A1-Catalog-Units.md#attack-submarine-submarine-submarine), [SSGN (SSGN)](A1-Catalog-Units.md#ssgn-ssgn-ssgn), [SSBN (SSBN)](A1-Catalog-Units.md#ssbn-ssbn-ssbn), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station).

**Detects:** ships, submarines, underwater missiles.

**Special:** provides precise targeting, sees under ice.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `maxheight` | 100 |

**Upgrades:**

- On units with the [“Debuffed Sonar”](A1-Catalog-Units.md#debuffed-sonar-debuffed_sonar) (`Debuffed_Sonar`) trait: `range` ×0.8
- On units with the [“Advanced Sonar”](A1-Catalog-Units.md#advanced-sonar-advanced_sonar) (`Advanced_Sonar`) trait: `range` ×1.35
- On units with the [“Mega Sonar”](A1-Catalog-Units.md#mega-sonar-mega_sonar) (`Mega_Sonar`) trait: `range` ×1.45
- With [Improved Sonar](A5-Catalog-Technologies.md#improved-sonar-sonar_mk2) (`Sonar_Mk2`): `range` ×1.2
- With [Enhanced Sonar](A5-Catalog-Technologies.md#enhanced-sonar-sonar_mk3) (`Sonar_Mk3`): `range` ×1.2
- With [Advanced Sonar](A5-Catalog-Technologies.md#advanced-sonar-sonar_mk4) (`Sonar_Mk4`): `range` ×1.2
- With [Experimental Sonar](A5-Catalog-Technologies.md#experimental-sonar-sonar_mk5) (`Sonar_Mk5`): `range` ×1.2

**Against targets with these traits** (stealth, cover…):

- `range` ×0.8: [“Submarine Stealth”](A1-Catalog-Units.md#submarine-stealth-submarine_stealth) (`Submarine_Stealth`)
- `range` ×0.9: [“Submarine Stealth Weak”](A1-Catalog-Units.md#submarine-stealth-weak-submarine_stealth_weak) (`Submarine_Stealth_Weak`)
- `range` ×0.95: [“Sonar Quieting SSN 1”](A1-Catalog-Units.md#sonar-quieting-ssn-1-sonar_quieting_ssn_1) (`Sonar_Quieting_SSN_1`), [“Sonar Quieting SSGN 1”](A1-Catalog-Units.md#sonar-quieting-ssgn-1-sonar_quieting_ssgn_1) (`Sonar_Quieting_SSGN_1`), [“Sonar Quieting SSBN 1”](A1-Catalog-Units.md#sonar-quieting-ssbn-1-sonar_quieting_ssbn_1) (`Sonar_Quieting_SSBN_1`)
- `range` ×0.875: [“Sonar Quieting SSN 2”](A1-Catalog-Units.md#sonar-quieting-ssn-2-sonar_quieting_ssn_2) (`Sonar_Quieting_SSN_2`), [“Sonar Quieting SSN 3”](A1-Catalog-Units.md#sonar-quieting-ssn-3-sonar_quieting_ssn_3) (`Sonar_Quieting_SSN_3`), [“Sonar Quieting SSN 4”](A1-Catalog-Units.md#sonar-quieting-ssn-4-sonar_quieting_ssn_4) (`Sonar_Quieting_SSN_4`), [“Sonar Quieting SSN 5”](A1-Catalog-Units.md#sonar-quieting-ssn-5-sonar_quieting_ssn_5) (`Sonar_Quieting_SSN_5`), [“Sonar Quieting SSGN 2”](A1-Catalog-Units.md#sonar-quieting-ssgn-2-sonar_quieting_ssgn_2) (`Sonar_Quieting_SSGN_2`), [“Sonar Quieting SSGN 3”](A1-Catalog-Units.md#sonar-quieting-ssgn-3-sonar_quieting_ssgn_3) (`Sonar_Quieting_SSGN_3`), [“Sonar Quieting SSGN 4”](A1-Catalog-Units.md#sonar-quieting-ssgn-4-sonar_quieting_ssgn_4) (`Sonar_Quieting_SSGN_4`), [“Sonar Quieting SSGN 5”](A1-Catalog-Units.md#sonar-quieting-ssgn-5-sonar_quieting_ssgn_5) (`Sonar_Quieting_SSGN_5`), [“Sonar Quieting SSBN 2”](A1-Catalog-Units.md#sonar-quieting-ssbn-2-sonar_quieting_ssbn_2) (`Sonar_Quieting_SSBN_2`), [“Sonar Quieting SSBN 4”](A1-Catalog-Units.md#sonar-quieting-ssbn-4-sonar_quieting_ssbn_4) (`Sonar_Quieting_SSBN_4`)
- `range` ×0.766: [“Sonar Quieting SSBN 3”](A1-Catalog-Units.md#sonar-quieting-ssbn-3-sonar_quieting_ssbn_3) (`Sonar_Quieting_SSBN_3`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Special Reconnaissance (`Counter-spy`)

This unit can detect covert units more easily.

**Technology:** `R_Counterspy`; template `Optical`.

**Carried by:** [Intelligence Center](A1-Catalog-Units.md#intelligence-center-intelligence_center), [Spec-Ops Team](A1-Catalog-Units.md#spec-ops-team-spec_ops_team), [Spec-Ops Helicopter](A1-Catalog-Units.md#spec-ops-helicopter-spec_ops_helicopter), [Special Mission Aircraft](A1-Catalog-Units.md#special-mission-aircraft-sof_aircraft), [Attack Helicopter](A1-Catalog-Units.md#attack-helicopter-attack_helicopter), [Security Checkpoint](A1-Catalog-Units.md#security-checkpoint-security_checkpoint).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `maxheight` | 100 |

**Upgrades:**

- With [Portable Electronic Optics](A5-Catalog-Technologies.md#portable-electronic-optics-portable_electronic_optics) (`Portable_Electronic_Optics`): `range` = 225
- With [Early Tactical Optics](A5-Catalog-Technologies.md#early-tactical-optics-tactical_optics) (`Tactical_Optics`): `range` = 250
- With [Advanced Tactical Optics](A5-Catalog-Technologies.md#advanced-tactical-optics-advanced_tactical_optics) (`Advanced_Tactical_Optics`): `range` = 300
- With [Light Unmanned Vehicles](A5-Catalog-Technologies.md#light-unmanned-vehicles-light_unmanned_vehicles) (`Light_Unmanned_Vehicles`): `range` = 350
- With [Robotic Infantry Aids](A5-Catalog-Technologies.md#robotic-infantry-aids-robotic_infantry) (`Robotic_Infantry`): `range` = 400

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range` ×0: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)
- `range` ×1: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

### STD Vision (`STD Vision`)

**Technology:** `R_Visor`; template `Optical`.

**Carried by:** [Central Command Bunker](A1-Catalog-Units.md#central-command-bunker-central_command_bunker), [Intelligence Center](A1-Catalog-Units.md#intelligence-center-intelligence_center), [Research Center](A1-Catalog-Units.md#research-center-research_center), [Cyber Warfare Center](A1-Catalog-Units.md#cyber-warfare-center-cyber_warfare_center), [Naval Helicopter](A1-Catalog-Units.md#naval-helicopter-navy_helicopter), [Spec-Ops Team](A1-Catalog-Units.md#spec-ops-team-spec_ops_team), [Spec-Ops Helicopter](A1-Catalog-Units.md#spec-ops-helicopter-spec_ops_helicopter), [Attack Helicopter](A1-Catalog-Units.md#attack-helicopter-attack_helicopter), [Carrier](A1-Catalog-Units.md#carrier-carrier), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Air Base](A1-Catalog-Units.md#air-base-airport), [Tactical Airbase](A1-Catalog-Units.md#tactical-airbase-tactical_airbase), [Makeshift Airbase](A1-Catalog-Units.md#makeshift-airbase-improvised_airbase), [Specialized Airbase](A1-Catalog-Units.md#specialized-airbase-specialized_airport), [Coastal Missile Battery](A1-Catalog-Units.md#coastal-missile-battery-coastal), [Fixed Coastal Gun](A1-Catalog-Units.md#fixed-coastal-gun-fixed_coastal_gun), [MRBM TEL Vehicle](A1-Catalog-Units.md#mrbm-tel-vehicle-mobile_mrbm), [ICBM TEL Vehicle](A1-Catalog-Units.md#icbm-tel-vehicle-mobile_icbm), [SRBM TEL Vehicle](A1-Catalog-Units.md#srbm-tel-vehicle-mobile_srbm), [ICBM Launchpad](A1-Catalog-Units.md#icbm-launchpad-icbm_launchpad), [Missile Silo](A1-Catalog-Units.md#missile-silo-missile_silo), [Radar Site](A1-Catalog-Units.md#radar-site-fixed_lw_radar), [Short-Wave Radar Vehicle](A1-Catalog-Units.md#short-wave-radar-vehicle-mobile_sw_radar), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station), [Over-The-Horizon Radar](A1-Catalog-Units.md#over-the-horizon-radar-over_horizon_radar), [Space Radar](A1-Catalog-Units.md#space-radar-space_radar), [AA Gun Site](A1-Catalog-Units.md#aa-gun-site-aa_site_old), [SAM Site](A1-Catalog-Units.md#sam-site-sam_site), [Midcourse ABM Site](A1-Catalog-Units.md#midcourse-abm-site-abm_site), [Mobile SAM](A1-Catalog-Units.md#mobile-sam-mobile_sam), [Terminal ABM Site](A1-Catalog-Units.md#terminal-abm-site-terminal_abm), [Mobile Defence Laser](A1-Catalog-Units.md#mobile-defence-laser-mobile_abm_laser), [Laser Defence Complex](A1-Catalog-Units.md#laser-defence-complex-laser_defence_complex), [Security Checkpoint](A1-Catalog-Units.md#security-checkpoint-security_checkpoint), [Army Division (Army Division)](A1-Catalog-Units.md#army-division-army-division-army_division), [Forward Operating Base](A1-Catalog-Units.md#forward-operating-base-forward_operating_base), [Combat Engineers](A1-Catalog-Units.md#combat-engineers-combat_engineers), [Bomb Truck](A1-Catalog-Units.md#bomb-truck-bomb_truck), [Heavy Bomb Truck](A1-Catalog-Units.md#heavy-bomb-truck-heavy_bomb_truck), [Army Base](A1-Catalog-Units.md#army-base-army_base), [Landing Ship](A1-Catalog-Units.md#landing-ship-landing_ship), [Resupply Ship](A1-Catalog-Units.md#resupply-ship-resupply_ship), [Space Center](A1-Catalog-Units.md#space-center-space_operations_center), [Satellite Relay Center](A1-Catalog-Units.md#satellite-relay-center-satellite_relay_station).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 50 |
| `maxheight` | 100 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.75: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)
- `range` ×0: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

### STD Vision Air (`STD Vision Air`)

**Technology:** `R_Visor_Air`; template `Optical`.

**Carried by:** [Fighter](A1-Catalog-Units.md#fighter-fighter), [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Interceptor](A1-Catalog-Units.md#interceptor-interceptor), [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [EW Aircraft](A1-Catalog-Units.md#ew-aircraft-ew_aircraft).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 100 |
| `maxheight` | 100 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

### Submarine Radar Mast (`Submarine Radar Mast`)

**Technology:** `R_Submarine_Radar_Mast`; template `LongWave`.

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `maxheight` | 100 |

**Upgrades:**

- With [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`):
    - `range` = 225
    - `maxheight` = 250
- With [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`):
    - `range` = 250
    - `maxheight` = 300
- With [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`):
    - `range` = 300
    - `maxheight` = 400
- With [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5) (`LW_Mk5`):
    - `range` = 350
    - `maxheight` = 500

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range` ×0: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`), [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### SW Targeting Radar (`Interceptor Short Wave`)

Interceptor Radar.

**Technology:** `R_Interceptor_Short_Wave`; template `ShortWave`.

**Carried by:** [Interceptor](A1-Catalog-Units.md#interceptor-interceptor).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 250 |
| `maxheight` | 100 |

**Upgrades:**

- With [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`):
    - `range` = 325
    - `maxheight` = 250
- With [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`):
    - `range` = 400
    - `maxheight` = 300
- With [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`):
    - `range` = 500
    - `maxheight` = 400
- With [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5) (`SW_Mk5`):
    - `range` = 600
    - `maxheight` = 500

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Targeting Radar (Fixed Short Wave) (`Fixed Short Wave`)

**Technology:** `R_Short_wave_radar`; template `ShortWave`.

**Carried by:** [Radar Site](A1-Catalog-Units.md#radar-site-fixed_lw_radar), [Short-Wave Radar Vehicle](A1-Catalog-Units.md#short-wave-radar-vehicle-mobile_sw_radar), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 300 |
| `maxheight` | 100 |

**Upgrades:**

- With [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`):
    - `range` = 375
    - `maxheight` = 250
- With [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`):
    - `range` = 450
    - `maxheight` = 300
- With [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`):
    - `range` = 550
    - `maxheight` = 400
- With [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5) (`SW_Mk5`):
    - `range` = 650
    - `maxheight` = 500

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range`: ×1 if you have researched [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`); ×0.85 if you have researched [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`); ×0.7 if you have researched [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`); otherwise ×0.1: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Targeting Radar (STD Short Wave) (`STD Short Wave`)

**Technology:** `R_Short_wave_radar`; template `ShortWave`.

**Carried by:** [Fighter](A1-Catalog-Units.md#fighter-fighter), [Multirole Attacker](A1-Catalog-Units.md#multirole-attacker-attack), [Strategic Bomber](A1-Catalog-Units.md#strategic-bomber-bomber), [High-Speed Bomber](A1-Catalog-Units.md#high-speed-bomber-high_speed_bomber), [Carrier](A1-Catalog-Units.md#carrier-carrier), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [AA Gun Site](A1-Catalog-Units.md#aa-gun-site-aa_site_old), [SAM Site](A1-Catalog-Units.md#sam-site-sam_site), [Midcourse ABM Site](A1-Catalog-Units.md#midcourse-abm-site-abm_site), [Mobile SAM](A1-Catalog-Units.md#mobile-sam-mobile_sam), [Terminal ABM Site](A1-Catalog-Units.md#terminal-abm-site-terminal_abm), [Mobile Defence Laser](A1-Catalog-Units.md#mobile-defence-laser-mobile_abm_laser), [Laser Defence Complex](A1-Catalog-Units.md#laser-defence-complex-laser_defence_complex), [Army Base](A1-Catalog-Units.md#army-base-army_base).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 200 |
| `maxheight` | 100 |

**Upgrades:**

- With [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`):
    - `range` = 225
    - `maxheight` = 250
- With [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`):
    - `range` = 250
    - `maxheight` = 300
- With [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`):
    - `range` = 300
    - `maxheight` = 400
- With [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5) (`SW_Mk5`):
    - `range` = 350
    - `maxheight` = 500

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range`: ×1 if you have researched [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`); ×0.85 if you have researched [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`); ×0.7 if you have researched [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`); otherwise ×0.1: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Ultra-HD Spy Camera (`Ultra-Resolution Satellite Camera`)

An extremely high-resolution camera that streams extreme amounts of visual information to a command center in real time.

**Technology:** `R_Ultra_Sat_Camera`; template `DataSat3`.

**Carried by:** [Spy Satellite](A1-Catalog-Units.md#spy-satellite-satellite).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting, reveals launch positions.

| Stat | Base value |
|---|---|
| `range` | 0 |
| `maxheight` | 3 000 |

**Against targets with these traits** (stealth, cover…):

- `range` ×0.25: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

**Jamming and other effects:**

- Inside the range of an active friendly [Satellite Relay](A2-Catalog-Missiles.md#satellite-relay-satellite-relay): `range` = 1 750
- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Air Detection (`AWACS Air Detection`)

Air Detection

**Technology:** `R_AWACS_Air_Detection`; template `AirDetectionLW`.

**Carried by:** [AWACS](A1-Catalog-Units.md#awacs-awacs), [Carrier AWACS](A1-Catalog-Units.md#carrier-awacs-naval-awacs).

**Detects:** ships, aircraft, missiles.

| Stat | Base value |
|---|---|
| `range` | 800 |
| `maxheight` | 1 500 |

**Upgrades:**

- On units with the [“Carrier AWACS”](A1-Catalog-Units.md#carrier-awacs-naval_awacs_mod) (`Naval_AWACS_Mod`) trait: `range` ×0.75
- With [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`): `range` = 950
- With [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`): `range` = 1 100
- With [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`): `range` = 1 300
- With [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5) (`LW_Mk5`): `range` = 1 600

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range`: ×1 if you have researched [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`); ×0.85 if you have researched [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`); ×0.7 if you have researched [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`); otherwise ×0.1: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Air Targeting (`AWACS Air Targeting`)

Air Targeting

**Technology:** `R_AWACS_Air_Targeting`; template `AirDetectionSW`.

**Carried by:** [AWACS](A1-Catalog-Units.md#awacs-awacs), [Carrier AWACS](A1-Catalog-Units.md#carrier-awacs-naval-awacs).

**Detects:** ships, aircraft, missiles.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 600 |
| `maxheight` | 1 500 |

**Upgrades:**

- On units with the [“Carrier AWACS”](A1-Catalog-Units.md#carrier-awacs-naval_awacs_mod) (`Naval_AWACS_Mod`) trait: `range` ×0.75
- With [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`): `range` = 700
- With [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`): `range` = 825
- With [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`): `range` = 975
- With [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5) (`SW_Mk5`): `range` = 1 200

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range`: ×1 if you have researched [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`); ×0.85 if you have researched [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`); ×0.7 if you have researched [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`); otherwise ×0.1: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Ground Detection (`AWACS Long Wave`)

Ground Detection

**Technology:** `R_AWACS_Ground_Detection`; template `LongWave`.

**Carried by:** [AWACS](A1-Catalog-Units.md#awacs-awacs), [Carrier AWACS](A1-Catalog-Units.md#carrier-awacs-naval-awacs), [Naval Helicopter](A1-Catalog-Units.md#naval-helicopter-navy_helicopter).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

| Stat | Base value |
|---|---|
| `range` | 400 |
| `maxheight` | 1 500 |

**Upgrades:**

- With [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`): `range` = 450
- With [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`): `range` = 500
- With [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`): `range` = 600
- With [Experimental LW Search Radar](A5-Catalog-Technologies.md#experimental-lw-search-radar-lw_mk5) (`LW_Mk5`): `range` = 700

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range`: ×1 if you have researched [AESA Search Radar](A5-Catalog-Technologies.md#aesa-search-radar-lw_mk4) (`LW_Mk4`); ×0.85 if you have researched [Phased Array Search Radar](A5-Catalog-Technologies.md#phased-array-search-radar-lw_mk3) (`LW_Mk3`); ×0.7 if you have researched [Pulse Compression Search Radar](A5-Catalog-Technologies.md#pulse-compression-search-radar-lw_mk2) (`LW_Mk2`); otherwise ×0.1: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Ground Targeting (`AWACS Short Wave`)

Ground Targeting

**Technology:** `R_AWACS_Ground_Targeting`; template `ShortWave`.

**Carried by:** [AWACS](A1-Catalog-Units.md#awacs-awacs), [Carrier AWACS](A1-Catalog-Units.md#carrier-awacs-naval-awacs), [Naval Helicopter](A1-Catalog-Units.md#naval-helicopter-navy_helicopter).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 300 |
| `maxheight` | 1 500 |

**Upgrades:**

- With [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`): `range` = 350
- With [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`): `range` = 400
- With [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`): `range` = 500
- With [Experimental Tracking Radars](A5-Catalog-Technologies.md#experimental-tracking-radars-sw_mk5) (`SW_Mk5`): `range` = 600

**Against targets with these traits** (stealth, cover…):

- `range` ×0.6: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-aircraft_stealth_bonus_modifier_1) (`Aircraft_Stealth_Bonus_Modifier_1`)
- `range` ×0.75: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-aircraft_stealth_bonus_modifier_2) (`Aircraft_Stealth_Bonus_Modifier_2`), [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-warship_stealth_bonus_modifier_2) (`Warship_Stealth_Bonus_Modifier_2`)
- `range` ×0.55: [“Stealth Technology”](A1-Catalog-Units.md#stealth-technology-bomber_stealth_bonus_modifier_1) (`Bomber_Stealth_Bonus_Modifier_1`)
- `range` ×0.65: [“Advanced Stealth”](A1-Catalog-Units.md#advanced-stealth-bomber_stealth_bonus_modifier_2) (`Bomber_Stealth_Bonus_Modifier_2`)
- `range` ×0.7: [“Novel Stealth Applications”](A1-Catalog-Units.md#novel-stealth-applications-warship_stealth_bonus_modifier_1) (`Warship_Stealth_Bonus_Modifier_1`)
- `range`: ×1 if you have researched [AESA Targeting Radar](A5-Catalog-Technologies.md#aesa-targeting-radar-sw_mk4) (`SW_Mk4`); ×0.85 if you have researched [Phased Array Tracking Radar](A5-Catalog-Technologies.md#phased-array-tracking-radar-sw_mk3) (`SW_Mk3`); ×0.7 if you have researched [Pulse Doppler Tracking Radar](A5-Catalog-Technologies.md#pulse-doppler-tracking-radar-sw_mk2) (`SW_Mk2`); otherwise ×0.1: [“Spy Plane”](A1-Catalog-Units.md#spy-plane-spy_plane_modifier) (`Spy_Plane_Modifier`)
- `range` ×0.5: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Overhorizon Radar (Naval Over Horizon) (`Naval_Over_Horizon`)

**Technology:** `R_Over_horizon_radar`; template `OverHorizon`.

**Detects:** ballistic missiles in flight.

**Special:** provides precise targeting, reveals launch positions.

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `maxheight` | 3 000 |

**Upgrades:**

- With [Advanced Early Warning Radar](A5-Catalog-Technologies.md#advanced-early-warning-radar-over_horizon_radar_mk2) (`Over_horizon_radar_Mk2`): `range` = 1 500

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Overhorizon Radar (Naval Small Over Horizon) (`Naval_Small_Over_Horizon`)

**Technology:** `R_Over_horizon_radar`; template `OverHorizon`.

**Carried by:** [Cruiser](A1-Catalog-Units.md#cruiser-cruiser).

**Detects:** ballistic missiles in flight.

**Special:** provides precise targeting, reveals launch positions.

| Stat | Base value |
|---|---|
| `range` | 750 |
| `maxheight` | 3 000 |

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Overhorizon Radar (Over Horizon) (`Over_Horizon`)

**Technology:** `R_Over_horizon_radar`; template `OverHorizon`.

**Carried by:** [Over-The-Horizon Radar](A1-Catalog-Units.md#over-the-horizon-radar-over_horizon_radar).

**Detects:** ballistic missiles in flight.

**Special:** provides precise targeting, reveals launch positions.

| Stat | Base value |
|---|---|
| `range` | 4 000 |
| `maxheight` | 3 000 |

**Upgrades:**

- With [Advanced Early Warning Radar](A5-Catalog-Technologies.md#advanced-early-warning-radar-over_horizon_radar_mk2) (`Over_horizon_radar_Mk2`): `range` = 6 000

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Overhorizon Radar (Small Over Horizon) (`Small_Over_Horizon`)

**Technology:** `R_Space_radar_OTH`; template `OverHorizon`.

**Carried by:** [Space Radar](A1-Catalog-Units.md#space-radar-space_radar).

**Detects:** ballistic missiles in flight.

**Special:** provides precise targeting, reveals launch positions.

| Stat | Base value |
|---|---|
| `range` | 850 |
| `maxheight` | 3 000 |

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Space radar (Naval Space Radar) (`Naval Space_Radar`)

**Technology:** `R_Space_radar`; template `SpaceObserver`.

**Carried by:** [Cruiser](A1-Catalog-Units.md#cruiser-cruiser).

**Detects:** satellites, ballistic missiles in flight, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 500 |
| `maxheight` | 50 000 |

**Upgrades:**

- With [Actively Tracked Space Radar](A5-Catalog-Technologies.md#actively-tracked-space-radar-space_radar_mk2) (`Space_radar_Mk2`): `range` = 625
- With [High-Fidelity ASAT Space Radar](A5-Catalog-Technologies.md#high-fidelity-asat-space-radar-space_radar_mk3) (`Space_radar_Mk3`): `range` = 750
- With [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4) (`Space_radar_Mk4`): `range` = 800

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- When the target's owner has researched [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`): `range` ×0.7 — not if the target's owner has researched [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4) (`Space_radar_Mk4`)
- When the target's owner has researched [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `range` ×0.8
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Space radar (Satellite Mini Space Radar) (`Satellite_Mini_Space_Radar`)

**Technology:** `R_Space_radar_sat`; template `SpaceObserver`.

**Carried by:** [Laser Defence Satellite](A1-Catalog-Units.md#laser-defence-satellite-laser_defence_satellite), [Hunter-Killer Satellite](A1-Catalog-Units.md#hunter-killer-satellite-hunter-killer_satellite).

**Detects:** satellites, ballistic missiles in flight, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 1 000 |
| `maxheight` | 50 000 |

**Upgrades:**

- With [Actively Tracked Space Radar](A5-Catalog-Technologies.md#actively-tracked-space-radar-space_radar_mk2) (`Space_radar_Mk2`): `range` = 1 250
- With [High-Fidelity ASAT Space Radar](A5-Catalog-Technologies.md#high-fidelity-asat-space-radar-space_radar_mk3) (`Space_radar_Mk3`): `range` = 1 500
- With [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4) (`Space_radar_Mk4`): `range` = 1 625

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- When the target's owner has researched [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`): `range` ×0.7 — not if the target's owner has researched [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4) (`Space_radar_Mk4`)
- When the target's owner has researched [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `range` ×0.8
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Space radar (Space Radar) (`Space_Radar`)

**Technology:** `R_Space_radar`; template `SpaceObserver`.

**Carried by:** [Space Radar](A1-Catalog-Units.md#space-radar-space_radar).

**Detects:** satellites, ballistic missiles in flight, Space Shuttle.

| Stat | Base value |
|---|---|
| `range` | 2 000 |
| `maxheight` | 50 000 |

**Upgrades:**

- With [Actively Tracked Space Radar](A5-Catalog-Technologies.md#actively-tracked-space-radar-space_radar_mk2) (`Space_radar_Mk2`): `range` = 2 500
- With [High-Fidelity ASAT Space Radar](A5-Catalog-Technologies.md#high-fidelity-asat-space-radar-space_radar_mk3) (`Space_radar_Mk3`): `range` = 3 000
- With [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4) (`Space_radar_Mk4`): `range` = 3 250

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
- When the target's owner has researched [Novel Stealth Applications](A5-Catalog-Technologies.md#novel-stealth-applications-novel_stealth_applications) (`Novel_Stealth_Applications`): `range` ×0.7 — not if the target's owner has researched [Counter-Stealth Space Radar](A5-Catalog-Technologies.md#counter-stealth-space-radar-space_radar_mk4) (`Space_radar_Mk4`)
- When the target's owner has researched [Advanced Stealth](A5-Catalog-Technologies.md#advanced-stealth-advanced_stealth) (`Advanced_Stealth`): `range` ×0.8
- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6

### Overhorizon Radar (AWACS Over Horizon) (`AWACS_Over_Horizon`)

AWACS-mounted Overhorizon Radar.

**Technology:** `R_AWACS_Over_Horizon_Radar`; template `OverHorizon`.

**Carried by:** [AWACS](A1-Catalog-Units.md#awacs-awacs), [Carrier AWACS](A1-Catalog-Units.md#carrier-awacs-naval-awacs).

**Detects:** ballistic missiles in flight.

**Special:** provides precise targeting, reveals launch positions.

| Stat | Base value |
|---|---|
| `range` | 2 000 |
| `maxheight` | 3 000 |

**Upgrades:**

- On units with the [“Carrier AWACS”](A1-Catalog-Units.md#carrier-awacs-naval_awacs_mod) (`Naval_AWACS_Mod`) trait: `range` ×0.75
- With [Advanced Early Warning Radar](A5-Catalog-Technologies.md#advanced-early-warning-radar-over_horizon_radar_mk2) (`Over_horizon_radar_Mk2`): `range` = 2 000

**Jamming and other effects:**

- Inside the range of an active enemy [Jamming Equipment](A2-Catalog-Missiles.md#jamming-equipment-ew-jammer): `range` ×0.6
- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### High-Power Quantum Radar (`Quantum Radar Strong`)

A quantum radar system, which is not affected by stealth or jamming.

**Technology:** `R_Quantum_Radar_Strong`; template `ShortWave`.

**Carried by:** [AWACS](A1-Catalog-Units.md#awacs-awacs), [Radar Site](A1-Catalog-Units.md#radar-site-fixed_lw_radar), [Naval Monitoring Station](A1-Catalog-Units.md#naval-monitoring-station-naval_monitoring_station).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 950 |
| `maxheight` | 100 |

**Upgrades:**

- On units with the [“Carrier AWACS”](A1-Catalog-Units.md#carrier-awacs-naval_awacs_mod) (`Naval_AWACS_Mod`) trait: `range` ×0.75
- With [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6) (`Radar_Mk6`): `range` ×1

**Against targets with these traits** (stealth, cover…):

- `range` ×0.75: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0

### Quantum Radar (`Quantum Radar Weak`)

A quantum radar system, which is not affected by stealth or jamming.

**Technology:** `R_Quantum_Radar_Weak`; template `ShortWave`.

**Carried by:** [Carrier AWACS](A1-Catalog-Units.md#carrier-awacs-naval-awacs), [Carrier](A1-Catalog-Units.md#carrier-carrier), [Destroyer](A1-Catalog-Units.md#destroyer-destroyer), [Cruiser](A1-Catalog-Units.md#cruiser-cruiser), [Short-Wave Radar Vehicle](A1-Catalog-Units.md#short-wave-radar-vehicle-mobile_sw_radar).

**Detects:** ground units, ships, aircraft, missiles, ballistic missiles in flight.

**Special:** provides precise targeting.

| Stat | Base value |
|---|---|
| `range` | 525 |
| `maxheight` | 100 |

**Upgrades:**

- With [Quantum Radar](A5-Catalog-Technologies.md#quantum-radar-radar_mk6) (`Radar_Mk6`): `range` ×1

**Against targets with these traits** (stealth, cover…):

- `range` ×0.75: [“Underground”](A1-Catalog-Units.md#underground-underground) (`Underground`)
- `range` ×0: [“Covert Unit”](A1-Catalog-Units.md#covert-unit-covert_unit) (`Covert_Unit`), [“Space Shuttle”](A1-Catalog-Units.md#space-shuttle-space_shuttle_mod) (`Space_Shuttle_Mod`)

**Jamming and other effects:**

- While under the lasting effect of EMP Blast:
    - `range`:
        - ×0.4 if you have researched [Comprehensive EMP Shielding](A5-Catalog-Technologies.md#comprehensive-emp-shielding-emp_defence_mk2) (`EMP_Defence_Mk2`)
        - ×0.25 if you have researched [Basic EMP Shielding](A5-Catalog-Technologies.md#basic-emp-shielding-emp_defence) (`EMP_Defence`)
        - otherwise ×0
