# DMSO-DPPC lab notebook: parameters and sources

Version 0.1 | Record initialized 2026-09-25 | Researcher: Antonio (Tony)

## How to read the table

An asterisk (*) marks a **selected working project choice**. Each starred row has an explanation below the tables, identified by its row ID.

A star records agreement, not successful validation, a completed run, or PI approval. Proposed values and examples awaiting a technical decision remain unstarred. Values fixed by a selected published molecular model are identified as model definitions, rather than separate choices we invented.

Agreement basis: earlier project decisions and Tony's acceptance of the staged recommendation followed by the request to organize the project. The source column distinguishes published values, official examples, project choices, and historical software evidence.

## A. System and workflow

| ID | Parameter | Current value | Where we obtained it | Status |
| --- | --- | --- | --- | --- |
| P01 | Simulation approach | Coarse-grained molecular dynamics* | Project scope; 2006 study [S1] | Selected |
| P02 | Simulation engine | GROMACS* | Project scope; paper and Martini workflow [S1, S5] | Selected |
| P03 | Molecular model | Martini 3.0.0 with the 2025 lipid update* | Earlier parameter documents; official lipid release and tutorial [S5, S6, S7] | Selected; exact active files to be recorded per run |
| P04 | Lipid | DPPC* | 2006 study and updated PC lipid topology [S1, S7] | Selected |
| P05 | Local learning system | Approximately 50 DPPC; no DMSO* | Tony's request for a smaller system and accepted training plan [R1] | Selected training choice; no verified run yet |
| P06 | Research lipid count | 512 DPPC total* | 2006 main paper and supplement, S1 [S1, S2] | Selected |
| P07 | Lipids in each leaflet | 256 + 256 is a symmetric target; measure the actual counts | 512 divided by two; tutorial warns self-assembly can be asymmetric [S5] | Target only; not a guaranteed assembly result |
| P08 | Research temperature | 323 K (49.85 °C)* | 2006 main paper and supplement, S1 [S1, S2] | Selected |
| P09 | Research pressure | 1 bar* | 2006 main paper and supplement, S1 [S1, S2] | Selected |
| P10 | Initial DMSO comparison | 0, 6, and 12 mol% of solvent* | Earlier proposal; 6% and 12% cases in the supplement; accepted staged plan [S2, R1] | Selected initial comparison; counts still unresolved |
| P11 | Water in 0% research control | 5,888 regular W beads | Earlier proposed upper-end starting count; historical range 2,355–5,888 in S1 [S2, R1] | Proposed, not finalized |
| P12 | Hydration if P11 is adopted | 23,552 real-water equivalents; 46 per lipid | Calculation: 5,888 × 4 / 512 [S2, S8] | Derived from a proposal; not a measured value |
| P13 | Water and DMSO counts at 6% and 12% | To be calculated | Requires a selected hydration policy and the modern mapping [S8] | Unresolved |
| P14 | Boundaries | Periodic in x, y, and z* | 2006 supplement, S1; Martini example [S2, S9] | Selected |
| P15 | Starting-membrane methods | Self-assembly and INSANE* | Retrieved September 23 decision and accepted current plan [R1, S5, S12] | Selected comparison |
| P16 | When DMSO is added | After forming and equilibrating the DMSO-free membrane in each route* | Accepted staged recommendation [R1]; historical preparation context [S2] | Selected first-study workflow |
| P17 | Production ensemble | NPT* | Historical conditions and modern bilayer workflow [S2, S5] | Selected; stage-specific coupling settings still to be checked |
| P18 | Practice duration | 100 ns | Earlier parameter/method proposal [R1] | Proposed; not required merely because the system has 50 lipids |
| P19 | Initial research production target | 800 ns per condition and repeat* | Accepted planning target, informed by reported runs up to 0.8 microseconds [S1, R1] | Selected planning target; extend or revise based on sampling |
| P20 | Computing locations | Mac for small training work; CIRCE for longer research runs* | Existing access and accepted staged plan [R1] | Selected; CIRCE environment/resources not verified here |
| P21 | Primary measurement | Area per lipid* | 2006 results, Martini analysis tutorial, and project plan [S2, S5, R1] | Selected |
| P22 | Supporting measurements | Bilayer thickness and DMSO distribution* | 2006 results and project plan [S1, S2, R1] | Selected |
| P23 | Additional observation | Water penetration, membrane integrity, and possible pores | 2006 mechanism [S1] | Exploratory; pores are not an expected success criterion |
| P24 | Independent repeats | Required; number and seed plan not selected | Existing methods overview and accepted recommendation [R1]; uncertainty guidance [S14] | Unresolved numerical design |
| P25 | Visualization | PyMOL or OVITO | Prior project discussions [R1] | Available options; exact tool/version to record when used |

## B. Simulation controls: examples awaiting validation

These are sourced candidate settings. **This table is not a ready-to-run .mdp file.** The official production example was last updated 20 December 2024 and contains a pressure-control combination that requires review with newer GROMACS.

| ID | Parameter | Sourced value or instruction | Where we obtained it | Status |
| --- | --- | --- | --- | --- |
| C01 | Production timestep | 20 fs = 0.02 ps | Official Martini production example [S9] | Candidate; validate with the actual system |
| C02 | Temperature algorithm | V-rescale | Official production example [S9] | Candidate |
| C03 | Temperature coupling time | 1 ps | Official production example [S9] | Candidate |
| C04 | Temperature groups | Lipids; water plus DMSO | Earlier modern parameter document and tutorial guidance [R1, S5] | Proposed grouping; specify actual index groups |
| C05 | Pressure coupling geometry | Isotropic during tutorial-style assembly; semi-isotropic after forming and orienting a planar bilayer | Martini Lipids I tutorial [S5] | Planned by stage; record actual protocol |
| C06 | Pressure-control algorithm | C-rescale | Official example; supported from GROMACS 2021 [S5, S9] | Candidate; executable must support it |
| C07 | Pressure coupling time | 4 ps in the older example | Official production example [S9] | Example only; review together with C08 and C01 |
| C08 | Pressure update interval | Every 20 steps in the older example | Official production example [S9] | Example only; not accepted as a validated tuple with C07 |
| C09 | Temperature update interval | Every 20 steps in the example | Official production example [S9] | Candidate; review as part of the complete settings |
| C10 | Compressibility input | 3 × 10^-4 bar^-1 in xy and z for the planar bilayer | Official production example [S9] | Candidate; this is not the measured membrane stiffness |
| C11 | van der Waals treatment | 1.1 nm cutoff; Potential-shift-verlet | Official production example [S9] | Candidate Martini settings |
| C12 | Electrostatics | Reaction field; cutoff 1.1 nm; relative dielectric 15; epsilon_rf = 0 (infinite external dielectric) | Official production example and GROMACS definitions [S9, S11] | Candidate Martini settings |
| C13 | Neighbor list | Verlet; rlist 1.35 nm; nstlist 20; verlet-buffer-tolerance -1 | Official production example [S9] | Candidate combination; retain the buffer setting when evaluating it |
| C14 | Bond constraints | Topology-defined constraints; example LINCS order 8 and 2 iterations | Official production example [S9] | Candidate; inspect constraints actually present |
| C15 | Saved data interval | Example: coordinates every 1 ns; energies/log every 0.5 ns | Official production example [S9] | Not selected; adapt to the analysis and retain a rationale |

**Compatibility issue to resolve:** at dt = 0.02 ps and nstpcouple = 20, pressure updates occur every 0.4 ps. With tau-p = 4 ps, the ratio is 10. The GROMACS change introduced a minimum of 25 coupling integration steps per tau-p for C-rescale; the example combination has produced warnings in GROMACS 2025.4. Validate a compatible combination for the actual executable and record the reason for any change. Do not suppress the warning to declare the setup validated. [S10]

## C. Molecular definitions supplied by the selected model

| ID | Parameter | Model definition | Where we obtained it | Status |
| --- | --- | --- | --- | --- |
| M01 | DPPC representation | 12 beads | DPPC section of phospholipids_PC_v2 [S7] | Verified in source snapshot; not yet installed in a research run |
| M02 | DPPC headgroup charges | NC3: +1; PO4: -1; other beads: 0 | DPPC atoms table [S7] | Published model definition |
| M03 | Water mapping | One regular W bead represents four water molecules | Martini water mapping; supplement explicitly states the historical four-water mapping [S2, S8, R1] | Use this mapping when counting regular W beads |
| M04 | Modern DMSO representation | One DMSO molecule represented by two beads: SC6 and TP6 | DIMETHYLSULFOXIDE entry in solvents_v1 [S8]; small-molecule mapping [R1] | Verified topology; use modern molecular counting |
| M05 | DMSO bead charges | 0 on both beads | DMSO atoms table [S8] | Published model definition |
| M06 | DMSO bond | 0.300 nm; harmonic force constant 8,000 kJ mol^-1 nm^-2 | DMSO bonds table [S8] | Published model definition |
| M07 | Remaining bonded and nonbonded parameters | Matching official Martini particle definitions and lipid v2 bonded definitions | Official particle release and lipid files [S6, S7] | Record exact active files and their checksums before a run |

### Concentration calculation

For the selected regular-water and modern-DMSO mapping:

DMSO mol% = 100 × N_DMSO / (N_DMSO + 4 × N_W)

N_DMSO is the number of complete modern DMSO molecules, not the number of DMSO beads. N_W is the number of regular W beads. Lipids are excluded.

The 2006 D1/D2 dimer instead represented about 2.2 real DMSO molecules. That factor belongs to the historical model and must not be applied to the modern SC6/TP6 model. [S2, S8]

P10 selects the desired concentrations; it does not fix all molecule counts. First decide how solvent amount/hydration is maintained between mixtures, then round to integer model counts and record the resulting actual mol%.

## D. Software and analysis records

| ID | Item | Current evidence or definition | Source | Status |
| --- | --- | --- | --- | --- |
| E01 | Mac GROMACS | 2026.3-Homebrew; successful historical gmx --version output | Pasted markdown(6).md, reviewed in this conversation [R1] | Historically verified; recheck before a new run |
| E02 | CIRCE GROMACS | Not verified | No authenticated module/version output available in this package | Open; earlier mention of 2020.4 remains unconfirmed |
| E03 | INSANE version | Not recorded | Inspect the installed builder before use [S12] | Open |
| E04 | Projected area per lipid | Lx × Ly / actual lipids in the leaflet, for a flat intact xy bilayer | Martini tutorial [S5] | Definition; use 256 only when confirmed |
| E05 | Initial thickness definition | Separation of phosphate-density peaks | Martini tutorial and existing methods overview [S5, R1] | Working definition; retain it consistently |
| E06 | Equilibration/analysis window | To be established from system behavior; exclude preparation and non-equilibrated data | Tutorial and methods overview [S5, R1] | Open |
| E07 | Uncertainty method | To be specified; account for correlated frames and independent repeats | Existing methods overview; benchmarking guidance [R1, S14] | Open |
| E08 | Simulation-time reporting | Report raw GROMACS ps/ns; any effective-time conversion must be justified separately | 2004 paper's effective-time discussion [S3] | Reporting rule; no automatic factor-of-four conversion |

## Why we chose the starred parameters

- **P01 — Coarse-grained MD:** matches the current project scope and makes membrane simulations accessible over larger systems and longer simulated times than a more detailed representation.
- **P02 — GROMACS:** is the selected simulation engine, works with the Martini files, and is already installed on the Mac.
- **P03 — Martini 3 plus the 2025 lipids:** follows the decision to learn the modern model and compare its behavior with the historical study. A newer model is not assumed automatically to reproduce every historical result better.
- **P04 — DPPC:** keeps the lipid identity consistent with the 2006 comparison.
- **P05 — Approximately 50 training lipids with no DMSO:** follows Tony's request for a small local learning system and reduces setup complexity. It is a workflow test, not a substitute for the research system.
- **P06 — 512 research lipids:** matches the historical lipid count and provides the same total count for comparing construction routes.
- **P08 — 323 K:** matches the 2006 study's temperature; this equals 49.85 °C.
- **P09 — 1 bar:** matches the 2006 pressure and the selected modern comparison conditions.
- **P10 — 0/6/12 mol%:** provides a solvent-free control and two published concentrations for an initial structural comparison. The selection does not assume that a pore must form.
- **P14 — Periodic xyz boundaries:** follows the historical and modern simulation setup for a repeating membrane system.
- **P15 — Two construction routes:** tests whether preparation through self-assembly versus INSANE affects the equilibrated result while using the same physical model.
- **P16 — DMSO after pure-membrane equilibration:** keeps the first study focused on DMSO's effects on an established membrane and helps make the two preparation routes comparable.
- **P17 — NPT:** maintains the chosen temperature and pressure while allowing the box dimensions to relax.
- **P19 — 800 ns initial target:** retains a concrete planning target discussed for this project and informed by the paper's reported maximum duration. It is raw modern simulation time; it is not a guarantee of convergence or a proven match to historical effective time.
- **P20 — Mac then CIRCE:** supports local learning and reserves longer research runs for the available computing cluster.
- **P21 — Area per lipid:** gives a clear first structural measurement for comparison with the paper.
- **P22 — Thickness and DMSO distribution:** help explain how the membrane changes and where DMSO resides.

Unstarred numerical controls are not yet agreed final settings. A later selection must add a star, a dated reason here, and a RUN_LOG entry. Existing agreement can be revised through a documented decision.

## Source key

Full source details, reference snapshots, and checksums are in SOURCES.md.

- **S1:** Notman et al. (2006), Molecular Basis for Dimethylsulfoxide (DMSO) Action on Lipid Membranes. https://doi.org/10.1021/ja063363t
- **S2:** Supplied supplement to S1: S1 (system), S2–S4 (DMSO model and mapping), S6–S9 (structural/mechanical results). Supplied filename: suplemental info from 2006 paper.pdf.
- **S3:** Marrink, de Vries, and Mark (2004), Coarse Grained Model for Semiquantitative Lipid Simulations. https://doi.org/10.1021/jp036508g
- **S5:** Martini Lipid Bilayers I tutorial. https://cgmartini.nl/docs/tutorials/Martini3/LipidsI/
- **S6:** Martini 3 particle definitions. https://cgmartini.nl/docs/downloads/force-field-parameters/martini3/particle-definitions.html
- **S7:** Official 2025 lipid files: martini_v3.0.0_phospholipids_PC_v2.itp and martini_v3.0.0_ffbonded_v2.itp. https://github.com/Martini-Force-Field-Initiative/M3-Lipid-Parameters
- **S8:** Official Martini 3 solvents, martini_v3.0.0_solvents_v1.itp. https://cgmartini.nl/docs/downloads/force-field-parameters/martini3/solvents.html
- **S9:** Official production example, updated 20 December 2024. https://cgmartini-library.s3.ca-central-1.amazonaws.com/1_Downloads/example_input_files/mdps/martini_v3.0_prod.mdp
- **S10:** GROMACS C-rescale update and the reported Martini tutorial warning. https://gitlab.com/gromacs/gromacs/-/merge_requests/5424 and https://github.com/orgs/Martini-Force-Field-Initiative/discussions/71
- **S11:** GROMACS parameter documentation. https://manual.gromacs.org/current/user-guide/mdp-options.html
- **S12:** INSANE repository. https://github.com/Tsjerk/Insane
- **S14:** Jorgensen et al., Permeability Benchmarking: Guidelines for Comparing in Silico, in Vitro, and in Vivo Measurements. https://doi.org/10.1021/acs.jcim.4c01815
- **R1:** Project conversations and saved records: simulation parameters.docx; DMSO_DPPC_Parameters_GROMACS_Martini3.docx; DMSO_DPPC_Methods_Overview_Martini3.docx; Pasted markdown(6).md; and the current acceptance/organization request. These establish project choices and historical setup, not independent scientific validation.

