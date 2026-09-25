# Run record — RUN_ID

State: planned / prepared / running / failed / completed / analyzed  
Created:  
Last updated:

## Identity and execution

| Field | Value |
| --- | --- |
| Purpose / research question | |
| Training or research | |
| Construction route | |
| Operator | |
| Date/time/timezone | |
| Machine / cluster | |
| Code and input commit used to start | |
| Branch | |
| GROMACS executable/version | |
| Builder/version/command/seed | |
| SLURM job ID, partition, resources | |
| Working and output locations | |
| Backup/archive location and last confirmed backup | |

## Actual system and inputs

| Field | Value |
| --- | --- |
| DPPC count / upper and lower leaflet counts | |
| Water bead count / mapping | |
| DMSO molecule count / bead count / mapping | |
| Target and actual DMSO mol% | |
| Hydration policy | |
| Box dimensions / orientation / periodicity | |
| Initial coordinate file and checksum | |
| Topology/force-field filenames, versions, and checksums | |
| Stage-specific .mdp files and final processed settings | |
| Temperature / pressure / coupling groups | |
| Timestep / nsteps / raw simulation duration | |
| Velocity and thermostat/barostat random seeds | |
| Constraints / restraints, if any | |
| Saved output intervals | |

## Evidence

- Build, minimization, equilibration, preprocessing, and run commands:
- Warnings/errors and resolutions:
- Actual start/end or checkpoint reached:
- Trajectory, energy, log, compiled-input, and checkpoint paths:
- Exact input snapshot / processed .mdp / version output:
- Any differences from the planned protocol:

## Analysis

- Equilibration portion excluded and reason:
- Analysis interval / selection definitions:
- APL definition and actual leaflet populations:
- Thickness definition:
- DMSO distribution method:
- Independent-repeat relationship:
- Uncertainty / autocorrelation treatment:
- Analysis script version/commit:
- Findings and limitations:
- Next action:

Fill only what is known. "Not recorded" is preferable to an invented value. Large run outputs and checkpoints need identified storage and backups even when excluded from Git.

