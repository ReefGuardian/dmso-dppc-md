# DMSO-DPPC molecular dynamics project

Researcher: Antonio (Tony)  
Laboratory: Dr. Samanta, USF  
Record initialized: 2026-09-25  
Current stage: organization and preparation for a small training system

Study how DMSO changes a DPPC membrane using GROMACS and Martini 3 with the 2025 lipid update. Compare self-assembled and INSANE-built starting membranes and compare the resulting trends with Notman et al. (2006).

This is a modern-model comparison with the 2006 study. No completed research simulation is established by the records reviewed for this starter package.

## Start here

| File | Purpose |
| --- | --- |
| [PROJECT_PLAN.md](PROJECT_PLAN.md) | Research questions, stages, and what counts as completing a stage |
| [PARAMETERS.md](PARAMETERS.md) | Parameter tables, sources, status, and explanations for starred choices |
| [RUN_LOG.md](RUN_LOG.md) | Dated record of work, evidence, errors, and actual runs |
| [NEXT_STEPS.md](NEXT_STEPS.md) | Current stopping point and next actions |
| [CODEX_PROMPTS.md](CODEX_PROMPTS.md) | Copyable prompts for GitHub setup and future sessions |
| [SOURCES.md](SOURCES.md) | Papers, official documentation, and source file identification |
| [templates/SESSION_ENTRY.md](templates/SESSION_ENTRY.md) | Template for a new notebook entry |
| [templates/RUN_RECORD.md](templates/RUN_RECORD.md) | Template for each simulation |
| [environment/VERIFIED_SETUP.md](environment/VERIFIED_SETUP.md) | Historical software evidence and verification still needed |

A star (*) means that Tony and the assistant have selected a working project choice. It does not mean that the value has been validated by simulation or approved by the PI. Unselected numerical examples remain unstarred.

## GitHub setup

Suggested private repository name: dmso-dppc-md.

Extract the starter ZIP, open this folder in a local Codex session, and use Prompt 1 in CODEX_PROMPTS.md. No GitHub repository or commit has been created by preparing this package. Authentication and the actual push will be performed in the user's Codex environment.

The GitHub repository becomes the working record after the initial upload. Update the files there; the downloaded starter and standalone previews are initial snapshots.

## Daily routine

1. Read NEXT_STEPS.md and the latest RUN_LOG.md entry.
2. Record the purpose of the next step and the source of any new setting.
3. Do the authorized step and retain its actual output.
4. Update the notebook, parameter decisions, and stopping point.
5. Commit the small project files and push when the current task authorizes it.

Git saves the files committed to it. It does not automatically record terminal commands, failed attempts, or reasons for a decision.

## What belongs in this repository

Keep notes, small starting structures, .mdp/.top/.itp files, scripts, small analysis tables, and figures. Keep large trajectories, energy files, compiled run inputs, and restart checkpoints in identified research storage with backups. Record their paths and identifiers in the run record. The .gitignore is a starting aid; inspect staged files before committing.

The references folder contains source snapshots used for this audit, not an executable force-field installation. Active simulation inputs still need to be assembled and checked.

