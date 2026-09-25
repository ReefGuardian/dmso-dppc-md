# Next steps

Updated: 2026-09-25  
Current stage: organizational setup  
Current repository URL: not created yet  
Last verified research run: none documented  
Immediate task: complete browser sign-in, verify the personal GitHub owner, and create/push the private repository.
Local folder: `/Users/mila/Downloads/dmso-dppc-md`  
Local branch: `main` (initialized; initial commit pending)

## Setup stopping point

The local repository is initialized and GitHub CLI 2.101.0 is installed. GitHub browser authorization is pending. The existing configured commit identity is retained. All four source snapshots match their recorded checksums. No simulation work was performed.

Next: finish browser authorization, verify the authenticated personal account and any existing `dmso-dppc-md` repository, then commit the inspected small files and push to a verified private remote. Record actual commit and push outcomes after execution. Do not paste credentials into the notebook.

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

