# Instructions for this research repository

## Understand the current state

Read README.md, PROJECT_PLAN.md, PARAMETERS.md, NEXT_STEPS.md, and recent RUN_LOG.md entries before changing the workflow. Relevant run records and actual output evidence determine what has really happened.

Explain one concrete next step in plain language: what it does, why it is needed, where values came from, and the expected output. Identify the actual execution machine; a cloud shell is not automatically Tony's Mac or CIRCE.

## Research records

- A star in PARAMETERS.md means a selected working choice, not validated science or PI approval.
- When the user agrees to a parameter choice, add/retain the star and explain the reason below the tables. Record the date, source, previous value/status, new choice, and affected runs in RUN_LOG.md.
- Keep unselected examples unstarred. Do not turn an assistant proposal into an agreement without evidence of acceptance.
- Preserve the history of failures and changes. Label proposed commands as not executed.
- Cite the source for every numerical input; distinguish published/model values, computed values, and project choices.
- Do not claim a simulation, commit, push, or validation succeeded without its actual output.

## Scientific scope

Use the selected modern Martini 3/2025-lipid plan. Historical 2004/2006 D1/D2 parameters are reference material and must not be mixed into the modern model.

Treat self-assembly and INSANE as two starting-structure routes using the same force field. Verify actual leaflet counts. Keep model, composition, conditions, and analysis comparable.

The control/mixture counts, final runtime settings, repeat count, and several analysis decisions remain open. Resolve concrete missing decisions when they become necessary.

Check the GROMACS pressure-coupling compatibility issue before creating a run-ready protocol. Reference snapshots are not approved executable inputs.

## Files and Git

Preserve existing user work. Inspect the repository/remotes before initializing or pushing. Use the authenticated account and existing configured identity; do not invent them. Keep this repository private unless the user explicitly changes that instruction.

Commit and push when requested or already authorized by the task. Stage relevant small files deliberately. Keep large simulation outputs and credentials out of Git, while retaining their documented storage/backup locations. Do not force-push or overwrite unrelated work.

Update RUN_LOG.md and NEXT_STEPS.md after meaningful work. State the commit hash and actual push outcome when saving to GitHub.

## Execution scope

The user personally runs all experimental commands. The assistant performs documentation and GitHub recordkeeping only: read project records, document user-reported outcomes with their evidence attribution, preserve copies of existing files when authorized, and commit/push relevant records when authorized.

Do not install software, execute experimental setup/build commands, rebuild structures, run simulations, submit cluster jobs, or perform scientific analyses. Commands supplied as already executed are historical records to transcribe, not instructions to run. The user will obtain/verify force-field files and prepare topology and minimization inputs. A future change in this division of responsibility requires an explicit instruction from the user.

Distinguish user-reported Terminal/screenshot evidence from checks actually performed in the documentation session. Do not claim to have independently reviewed unavailable evidence. Preserve originals when archiving; never copy Python environments. Keep construction/visualization completion separate from minimization, equilibration, or MD completion.

If a required file cannot be opened or read, identify it and the access/read problem promptly. Continue other useful authorized work.

