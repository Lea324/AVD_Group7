# AVD
AERO60002 - Aerospace Vehicle Design. Year 3 group project.

AVD — Aerospace Vehicle Design

AERO60002 Aerospace Vehicle Design, Year 3 group project. MATLAB Live Scripts support preliminary aircraft mass estimation, fuselage sizing, wing design, constraint analysis, engine selection, and mission planning.

## Requirements

The Live Scripts were originally saved with **MATLAB R2025b Update 3**. Install:

- **MATLAB** for Live Scripts, tables, numerical calculations, and plots.
- **Aerospace Toolbox** for the ISA atmosphere function `atmosisa`.
- **Symbolic Math Toolbox** for the fuselage cross-section calculation using `syms` and `solve`.

Check product and function availability in MATLAB:

```matlab
ver
which atmosisa
which syms
```

The recent cleanup passed static MATLAB syntax checks and executable-token comparisons. Equations, numerical constants, parameter names, and calculation order were preserved. Formatting, section headings, comments, and display wording were cleaned; semicolons suppress intermediate console echo. Cached Live Script outputs were cleared. The edited scripts have **not yet been executed in MATLAB**.

## Current scripts

| File | Purpose |
| --- | --- |
| [Mass_initiation_readinput.mlx](Mass_initiation_readinput.mlx) | Cruise and loiter speeds, mission fuel fractions, payload and crew masses, and takeoff-mass convergence. |
| [Fuselage_sizing_double_new_readinput.mlx](Fuselage_sizing_double_new_readinput.mlx) | Baggage and cargo volumes, LD3 rows, cabin widths, symbolic cross-section sizing, seating, and fuselage lengths. |
| [Wing_design.mlx](Wing_design.mlx) | Wing geometry, sweep, twist, lift estimates, high-lift devices, and stall speeds. |
| [untitled.mlx](untitled.mlx) | **Current constraint diagram:** takeoff, climb, cruise, ceiling, landing, and stall constraints; design-point selection. |
| [Engine_desing.mlx](Engine_desing.mlx) | Thrust requirements, preliminary engine estimates, and engine comparison. |
| [flight_time_calculation.mlx](flight_time_calculation.mlx) | Mission segment durations and cumulative flight time. |
| [mission_profile.mlx](mission_profile.mlx) | Schematic mission altitude profile. |
| [Presentation chart](Presentation%20chart/) | Presentation figures and supporting plotting scripts. |


## Running the calculations

Starting from the existing parameter record, run and inspect each sizing script individually:

```matlab
run('Mass_initiation_readinput.mlx');
run('Fuselage_sizing_double_new_readinput.mlx');
run('Wing_design.mlx');
run('untitled.mlx');
```

After reviewing the sizing, run engine selection and mission scripts as needed:

```matlab
run('Engine_desing.mlx');
run('flight_time_calculation.mlx');
run('mission_profile.mlx');
```

Presentation scripts that read the shared CSV also need the intended parameter record in the current working directory.

## Parameter record

[Key_Param_recording.csv](Key_Param_recording.csv):

| Column | Meaning |
| --- | --- |
| `Parameter` | Exact MATLAB parameter key; preserve spelling and case. |
| `Value` | Stored numerical value. |
| `Unit` | Recorded unit label. |
| `Description` | Physical or computational meaning. |
| `Notes` | Usage in current scripts, including recorded results, unused settings, and legacy-only references. |


## Stored sizing snapshot

These values are copied from the current CSV, not from a new MATLAB execution. They replace the older README summary where it differed from the parameter record.

| Quantity | Parameter | Stored value | Unit |
| --- | --- | --- | --- |
| Maximum takeoff mass | `W_0_guess` | 290558.513640926 | kg |
| Fuel mass | `W_f` | 107049.997546463 | kg |
| Empty mass | `W_e` | 126360.516094463 | kg |
| Passenger and baggage mass | `W_pax` | 16518 | kg |
| Crew mass | `W_crew` | 630 | kg |
| Cargo mass | `W_cargo` | 40000 | kg |
| Fuselage total length | `L_total` | 64.9168404087387 | m |
| Upper-deck cabin and cargo-section length | `L_main` | 44.3854847951087 | m |
| Lower-deck cargo-section length | `L_under` | 44.8447146870154 | m |
| Fuselage outer diameter | `D_outer` | 5.86834637591485 | m |
| Fuselage inner diameter | `D_inner` | 5.51274637591485 | m |
| Cargo density | `rho_cargo` | 160 | kg/m³ |
| Wing aspect ratio | `AR` | 9 | Dimensionless |
| Wing reference area | `S_ref` | 468.657384820577 | m² |
| Wing loading | `Wing_loading` | 6082.01025128141 | N/m² in code; see unit note above |
| Thrust-to-weight ratio | `Thrust_to_weight` | 0.29834142601804 | Dimensionless |

### Previously recorded mission durations

These durations are retained from the earlier project README and have not been regenerated during cleanup.

| Segment | Duration (min) | Cumulative (min) |
| --- | --- | --- |
| 0–1 Taxi and takeoff | 15 | 15 |
| 1–2 Climb and accelerate | 25 | 40 |
| 2–3 Main cruise (5500 nmi) | 701.64 | 741.64 |
| 3–4 Initial descent | 25 | 766.64 |
| 4–5 Missed approach and climb | 25 | 791.64 |
| 5–6 Cruise to alternate (370 km) | 32.521 | 824.16 |
| 6–7 Loiter at 5000 ft | 45 | 869.16 |
| 7–8 Final descent | 20 | 889.16 |
| 8–9 Landing and taxi | 10 | 899.16 |

Previously recorded considered mission time: **12.78 hours**. Total mission time: **14 h 59 min**.

### Recorded design selections

- Engine: **Trent XWB-97**.
- Wing aerofoil: **SC(2)-0614**.

## References

### Passenger and crew mass standards

- [EASA Easy Access Rules for Air Operations](https://www.easa.europa.eu/en/document-library/easy-access-rules/online-publications/easy-access-rules-air-operations).
- [EASA Annex to ED Decision 2014/015/R, Part-CAT](https://www.easa.europa.eu/sites/default/files/dfu/Annex%20to%20ED%20Decision%202014-015-R%20-%20Part-CAT_0.pdf).

### Cabin and fuselage sizing

- Roskam, *Airplane Design, Part 3*, 2002.
- Torenbeek, *Synthesis of Subsonic Airplane Design*, 1982.

### Wetted area analysis

- [Wetted and Projected Area Relationships in Commercial Airplane Design](https://www.scribd.com/document/897371895/Wetted-and-Projected-Area-Relationships-in-Commercial-Airplane-Design).


# Mass EASA Standard
Easy Access Rules for Air Operations (EASA, current): https://www.easa.europa.eu/en/document-library/easy-access-rules/online-publications/easy-access-rules-air-operations

EASA Annex to ED Decision 2014/015/R, Part-CAT (PDF): https://www.easa.europa.eu/sites/default/files/dfu/Annex%20to%20ED%20Decision%202014-015-R%20-%20Part-CAT_0.pdf
# Cabin and fuselage sizing
Roskam, Airplane Design Part 3, 2002

Torenbeek, Synthesis of Subsonic Airplane Design, 1982

# Wetted Area Analysis in Airplane Design
https://www.scribd.com/document/897371895/Wetted-and-Projected-Area-Relationships-in-Commercial-Airplane-Design

### Install Aerospace toolbox for wing desgin!!!
