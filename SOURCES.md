# Sources and provenance

Source review recorded: 2026-09-25. Source IDs match PARAMETERS.md.

Published values establish what a paper/model used. Project records establish what we selected. Neither establishes that a new simulation has run successfully.

## Papers supplied for the project

| ID | Source | Where it is used |
| --- | --- | --- |
| S1 | Notman, Noro, O'Malley, and Anwar (2006). Molecular Basis for Dimethylsulfoxide (DMSO) Action on Lipid Membranes. JACS 128, 13982–13983. https://doi.org/10.1021/ja063363t | 512 DPPC, 323 K, 1 bar, reported concentration range/durations, structural trends, and historical pore example |
| S2 | Supplement to S1. Supplied filename: suplemental info from 2006 paper.pdf. Locate through the supporting information associated with S1 if a new copy is needed. | S1: water range, preparation, ensemble and boundaries. S2–S4: D1/D2 parameterization, interactions, and mapping. S6–S9: structural/mechanical figures. Historical dimer mapping is about 2.2 DMSO molecules. |
| S3 | Marrink, de Vries, and Mark (2004). Coarse Grained Model for Semiquantitative Lipid Simulations. J. Phys. Chem. B 108, 750–760. https://doi.org/10.1021/jp036508g | Original coarse-grained model and its effective-time convention; background, not the active Martini 3 parameters |
| S4 | Gurtovenko and Anwar (2007). Modulating the Structure and Properties of Cell Membranes: The Molecular Mechanism of Action of Dimethyl Sulfoxide. J. Phys. Chem. B 111, 10453–10460. https://doi.org/10.1021/jp073113e | Later atomistic/united-atom comparison; 128 DPPC and 350 K belong to that separate study |
| S14 | Jorgensen et al. Permeability Benchmarking: Guidelines for Comparing in Silico, in Vitro, and in Vivo Measurements. https://doi.org/10.1021/acs.jcim.4c01815 | Background on comparability, assumptions, convergence, and uncertainty; not a source of our specific bilayer input values |

## Official model and software resources

| ID | Source | Exact resource or relevant section |
| --- | --- | --- |
| S5 | Martini Lipid Bilayers I tutorial: https://cgmartini.nl/docs/tutorials/Martini3/LipidsI/ | Spontaneous assembly; bilayer equilibration; pressure geometry; leaflet asymmetry; APL/thickness analysis. The tutorial example is DSPC, so its example lipid identity and temperature must not be copied as our DPPC research choices. |
| S6 | Martini 3 particle definitions: https://cgmartini.nl/docs/downloads/force-field-parameters/martini3/particle-definitions.html | Martini 3.0.0 particle interaction definitions; release archive. Full particle-definition file still needed for an executable run setup. |
| S7 | Martini lipid update: https://github.com/Martini-Force-Field-Initiative/M3-Lipid-Parameters | ITPs/martini_v3.0.0_phospholipids_PC_v2.itp, DPPC section; ITPs/martini_v3.0.0_ffbonded_v2.itp. Main-branch URLs may change, so snapshots/checksums identify the contents reviewed here. |
| S8 | Solvent models: https://cgmartini.nl/docs/downloads/force-field-parameters/martini3/solvents.html | martini_v3.0.0_solvents_v1.itp, WATER and DIMETHYLSULFOXIDE entries; two-bead SC6/TP6 DMSO topology |
| S9 | Martini production example: https://cgmartini-library.s3.ca-central-1.amazonaws.com/1_Downloads/example_input_files/mdps/martini_v3.0_prod.mdp | Header date 20 December 2024; candidate controls. This is a source example, not an approved project run file. |
| S10 | GROMACS pressure-control change: https://gitlab.com/gromacs/gromacs/-/merge_requests/5424 | Minimum of 25 coupling integration steps per tau-p for C-rescale. Associated reported tutorial warning: https://github.com/orgs/Martini-Force-Field-Initiative/discussions/71 |
| S11 | GROMACS .mdp definitions: https://manual.gromacs.org/current/user-guide/mdp-options.html | Units and semantics of coupling, neighbor lists, constraints, and output settings. The current link resolved to 2026.3 during this review; use the actual executable's version-specific manual when finalizing a run. |
| S12 | INSANE: https://github.com/Tsjerk/Insane | Starting-structure builder; record the actual installed version/commit and the builder command when used |

The reference snapshots preserve the exact bytes retrieved during organization. Their presence does not establish that all required model files are installed or that a run has been validated.

## Project records (R1)

- simulation parameters.docx: saved 2026-09-23; concise modern project table. It labels several values as proposed.
- DMSO_DPPC_Parameters_GROMACS_Martini3.docx: saved 2026-09-16; system values, official example controls, modern DMSO model, and concentration definition.
- DMSO_DPPC_Methods_Overview_Martini3.docx: saved 2026-09-16; preparation, measurements, repeat runs, and uncertainty.
- Pasted markdown(6).md: historical September 23 Mac installation and successful gmx --version output.
- Relevant retrieved conversation excerpts: modern Martini/self-assembly/INSANE decision; request for a smaller approximately 50-lipid training system.
- Current conversation: accuracy audit, recommendation, Tony's acceptance, and request to organize the project and mark agreed choices with an asterisk.

This is a curated starting record. Complete verbatim transcripts of every Lab chat were not available. If a later transcript supplies a missing or superseding decision, log the evidence and update the working record.

## GitHub and Codex setup references

- Local Codex workflow: https://learn.chatgpt.com/docs/codex/cli
- Adding a local project to GitHub: https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github
- GitHub CLI repository creation: https://cli.github.com/manual/gh_repo_create

## File fingerprints

These hashes identify source content, not scientific approval. Source URLs and byte counts are also retained in references/source_evidence.json.

| Source | Snapshot or supplied file | SHA-256 |
| --- | --- | --- |
| S8 | references/snapshots/solvents_snapshot.itp.txt | e6a78414b317c38a1a816eded4aee6082a5da1ed229a126359f0cc92314dcb4e |
| S9 | references/snapshots/production_example.mdp.txt | 1ce9d6a5a09ffa149be64fa01ab1002561234e3607696de11cd68d082a405b73 |
| S7 | references/snapshots/lipids_pc_v2.itp.txt | 43fc3e9976ea2a11af1b3df5d841ed1d2677dddd93a73a7e86304ad875ffb150 |
| S7 | references/snapshots/lipid_bonded_v2.itp.txt | 149f98c48e32a9aab95e205b36c10e68332349d831aec3980bc55b4b428ab3fb |
| S14 | 01-Permeability-Benchmarking-Guidelines-for-Comparing-in-Silico-in-Vitro-and-in-Vivo-Measurements.pdf | 58696deb22f744a277bc057e99442c57d38c2015b25a1169e01217d5c2b7c8c8 |
| S1 | 02-2006-paper.pdf | b15fe817674a3926cea6db2d8a12667ed917044b7f7cd7fb06e1ce7442534e70 |
| S4 | 03-2007-paper.pdf | 1af33082d49ee3ecea1b945ebc25d3154cb53f12ad48d04bb43a7cedc062f9f3 |
| S2 | 04-suplemental-info-from-2006-paper.pdf | 9a4ed1f72b28d4a0e114ab25dc56db41ac5b3510782ec756813b3e45da44bc00 |
| S3 | 05-2004JPhysChemBMarrink.pdf | f9ad8276ce9640575867d4e8ee9a5175e783c6dd9ac61a2522bb85b3a991cddf |
