# Next steps

Milestone date: 2026-09-24 (America/New_York)  
Current stage: small practice construction and visualization completed (user-reported)  
Current repository URL: https://github.com/ReefGuardian/dmso-dppc-md (verified PRIVATE)  
Last verified research run: none documented  
Immediate experimental task: user to obtain and verify Martini force-field files, prepare the topology, and prepare energy minimization inputs.
Local folder: `/Users/mila/Downloads/dmso-dppc-md`  
Local branch: `main` (tracking `origin/main`)

## Current stopping point

See [TRAIN-001 notebook](practice-runs/TRAIN-001/README.md) for the September 24, 2026 milestone. The user reports completing construction of a 50-DPPC system and visualization in PyMOL. Copies of `dppc_start.pdb`, `topol.top`, and `dppc_start_view.pse` are archived there. No energy minimization, equilibration, or molecular dynamics performed. Simulation force-field files are not yet prepared in the practice folder; `topol.top` is preliminary builder output.

## Next experimental work — user executes

The user will obtain and verify the Martini force-field files, prepare the topology, and prepare energy minimization inputs. This supplies the simulation definitions missing from the builder output. Expected outputs are identified force-field files, a prepared topology, and minimization input files. No such work is executed by this documentation task.

The assistant performs documentation and GitHub recordkeeping only, as specified in AGENTS.md. Record the user's subsequent commands, source/version details, and results when provided. PyMOL's exact version remains unrecorded. Keep the small practice build separate from the larger 512-lipid research plan. Resolve the pressure-control compatibility issue before later run-ready equilibration/production preparation.

## Research decisions still open

- Control water count and hydration policy across mixtures.
- Integer water/DMSO counts and resulting actual mol%.
- Research-system box dimensions and leaflet matching procedure (practice build choices are recorded separately).
- Minimization, equilibration, and production settings.
- Training duration and analysis/output intervals.
- Independent-repeat count, seeds, and uncertainty method.
- CIRCE executable/module, scheduler resources, and backed-up data location.

## Restart rule

Read this file and the latest RUN_LOG entry, then inspect actual files and Git status. A note that something was planned does not establish that it was executed. Update this file whenever the stopping point changes.

