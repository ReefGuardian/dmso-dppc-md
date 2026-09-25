# Next steps

Updated: 2026-09-25  
Current stage: private repository established; training preparation pending  
Current repository URL: https://github.com/ReefGuardian/dmso-dppc-md (verified PRIVATE)  
Last verified research run: none documented  
Immediate task: verify GROMACS and builder availability on the intended training Mac.
Local folder: `/Users/mila/Downloads/dmso-dppc-md`  
Local branch: `main` (tracking `origin/main`)

## Setup stopping point

Private repository creation and initial push succeeded. Initial commit `dab237e5930ec1c7fa7dc4bdec9d63190c5e299a` was verified on remote `main`. GitHub owner is the authenticated personal account `ReefGuardian`. No access issue remains. All scientific settings, stars, explanations, sources, and open decisions are preserved. No simulations were run.

Next single step (not executed): check `gmx --version` and installed builder availability on the intended training Mac, recording executable paths and versions. These checks establish the current tools for the approximately 50-DPPC, DMSO-free training system selected in P05/R1. Expected output is a software inventory, not a membrane or simulation.

## After GitHub setup

- Verify the actual execution machine and gmx --version before doing simulation work.
- Inspect installed builder tools and choose how to create the 50-lipid training system.
- Resolve the candidate pressure-control combination for the chosen GROMACS version.
- Prepare and explain one concrete training step with input sources and expected output.
- Record and execute only the authorized step.

## Research decisions still open

- Control water count and hydration policy across mixtures.
- Integer water/DMSO counts and resulting actual mol%.
- Box dimensions and leaflet matching procedure.
- Minimization, equilibration, and production settings.
- Training duration and analysis/output intervals.
- Independent-repeat count, seeds, and uncertainty method.
- CIRCE executable/module, scheduler resources, and backed-up data location.

## Restart rule

Read this file and the latest RUN_LOG entry, then inspect actual files and Git status. A note that something was planned does not establish that it was executed. Update this file whenever the stopping point changes.

