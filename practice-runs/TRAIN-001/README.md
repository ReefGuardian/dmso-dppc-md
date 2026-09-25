# Small DPPC practice system: construction and visualization.

Date: September 24, 2026 (2026-09-24, America/New_York / EDT). Exact experimental command times not recorded.
Practice record: TRAIN-001. Operator: the user, on the user's Mac.

## Evidence and responsibility

These are user-reported results. The user identifies Terminal output and screenshots reviewed in the chat as supporting evidence. This documentation session records that report; it did not rerun commands, independently review those earlier screenshots, or perform scientific analysis. The raw Terminal transcript and screenshots are not included in this archive. File accessibility and byte-identical copying were checked for recordkeeping only.

The user personally executes all experimental commands. The assistant's role is documentation, archival copying, and GitHub recordkeeping only.

## Software reported by the user

| Software | Version or revision | Evidence/status |
| --- | --- | --- |
| Python | 3.12.11 | User-reported Terminal evidence |
| INSANE | 1.2.0 | User-reported Terminal evidence |
| INSANE GitHub revision | `25d03f0422ec5fb0546c7f8632289e5d633937a2` | User-reported installation revision |
| NumPy | 2.5.3 | User-reported Terminal evidence |
| setuptools | 81.0.0 | User-reported Terminal evidence |
| simopt | 0.4.0 | User-reported Terminal evidence |
| PyMOL | Exact version not yet recorded | Used by the user for visualization |

## Setup commands already executed by the user

The following is a historical record, not commands executed by the assistant in this documentation session. The pip URL is written as a plain URL rather than chat Markdown link syntax.

```sh
python3 -m venv "$HOME/Desktop/dmso-dppc-env"
source "$HOME/Desktop/dmso-dppc-env/bin/activate"
python -m pip install git+https://github.com/Tsjerk/Insane
insane -h
mkdir -p "$HOME/Desktop/DPPC-small-test"
cd "$HOME/Desktop/DPPC-small-test"
```

## Build command already executed by the user

```sh
insane -ff M3 -l DPPC -x 4 -y 4 -z 8 -a 0.64 -sol W -o dppc_start.pdb -p topol.top
```

This command was adapted for this small practice system, not copied verbatim from the Martini tutorial.

## Chosen input parameters

| Parameter | Value | Source | Status |
| --- | --- | --- | --- |
| Lipid | DPPC* | Project plan; user-reported `-l DPPC` | Used for this practice build |
| Lipid count target | 50 total lipids*, targeting 25 per leaflet | User's request for a small local test; chosen box and packing | Working target; observed counts recorded separately below |
| Builder templates | Martini 3 builder templates (`-ff M3`)* | Project plan; user-reported INSANE command | Used; does not establish prepared simulation force-field files |
| Initial box | 4 × 4 × 8 nm* | Assistant proposal used by the user; `-x 4 -y 4 -z 8` | Provisional practice choice |
| Initial packing area | 0.64 nm²/lipid* | Assistant proposal: 4 × 4 / 25 = 0.64; `-a 0.64` | Initial input, not a measured equilibrium area |
| Solvent | Martini water W*, with no DMSO or added salt | User-reported `-sol W`; simple DMSO-free practice scope | Used for this practice build |

These choices were used by the user for this small practice build. A star marks a working choice, not validated production settings or PI approval. DPPC and Martini 3 follow the project plan. The 50-lipid target follows the user's request for a small local test. The assistant proposed the box dimensions and packing: 4 × 4 / 25 = 0.64 nm² per lipid per leaflet. The 8 nm height was a provisional choice to provide water space. Water without DMSO or salt keeps this first practice system simple. The initial packing area is not a measured equilibrium area.

Decision history: before this milestone, TRAIN-001 had approximately 50 DPPC and no DMSO selected, while builder, box, and packing were not finalized in the record. The user now reports using the above choices on September 24, 2026. This records actual practice use, not approval of research production settings. Affected record: TRAIN-001 only; no completed MD results exist here to reevaluate. The separate 512-lipid research plan, existing parameter sources, stars, and unresolved production decisions remain unchanged.

## Observed build results — user-reported

These are reported outputs, not chosen input parameters or independently recalculated results.

| Observation | Reported result |
| --- | --- |
| Upper leaflet | 25 DPPC |
| Lower leaflet | 25 DPPC |
| Membrane beads | 600 |
| Solvent beads | 531 |
| Total beads | 1,131 |
| Total charge | 0 |

## Warnings

INSANE printed a `pkg_resources` deprecation warning, but both its help command and the structure build completed. No dependency changes were made in response. pip also displayed an update notice. This session made no software changes.

## Visualization — user-reported

The user loaded `dppc_start.pdb` in PyMOL, used menus to display spheres, selected water residues 51–581 through the sequence panel, and hid the water using **H → everything** on the selection. A screenshot showed the membrane with water hidden. The user confirmed saving `dppc_start_view.pse`. These actions changed the display, not the simulation coordinates. The session file is archived without opening or executing it.

## Files archived

Original source folder: `~/Desktop/DPPC-small-test/`, resolved here to `/Users/mila/Desktop/DPPC-small-test/`.
Repository archive: `practice-runs/TRAIN-001/`.

All three existing files were accessible and copied without moving, overwriting, or regenerating the originals. Copy bytes were checked against the source files. The Python environment was not copied. SHA-256 values identify archived bytes; they are not scientific validation.

| File | Bytes | SHA-256 |
| --- | --- | --- |
| `dppc_start.pdb` | 91745 | `dbae20916db0d7bba91bf0651f801b1b95ad477011aa2c314f8ee0862c8f6e94` |
| `topol.top` | 267 | `0d271d95b8d42a0a3dcfd0a1df15cae2f0d5f0c535decf3ab27e3fba79e39b5b` |
| `dppc_start_view.pse` | 285124 | `030c92d5741d9f1e0805f29eaf71269696c4469b5aee5ffe3ed146d6c34539b5` |

## Sources supplied for this milestone

- [Martini Lipid Bilayers II tutorial](https://cgmartini.nl/docs/tutorials/Martini3/LipidsII/).
- [INSANE repository](https://github.com/Tsjerk/Insane); user-reported installed revision above.
- User's milestone report, attributing results to Terminal output and screenshots reviewed in the chat.

The links are retained as supplied provenance; this record does not claim a new source audit or that the practice box/packing were published tutorial values.

## Current status and next experimental work

Construction and visualization completed, as reported by the user. No energy minimization, equilibration, or molecular dynamics performed. Martini simulation force-field files have not yet been prepared in the practice folder. `topol.top` is preliminary builder output, not a completed simulation topology. The larger 512-lipid research plan remains separate.

Next experimental work: the user will obtain and verify the Martini force-field files, prepare the topology, and prepare energy minimization inputs. This is needed to turn the builder output into a properly specified simulation setup. Expected outputs are identified force-field files, a prepared topology, and minimization input files; none are claimed as prepared or executed here. The assistant will document the user's subsequent actions and results.
