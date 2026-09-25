# Prompts to paste into Codex

Use these in the project folder. Prompt 1 creates the repository; the later prompts maintain the record.

The files in this starter package are the initial record. Codex can inspect local files and use local tools when running in an appropriate local environment. Creating or pushing a GitHub repository also requires GitHub authentication and the necessary account permissions.

## Before Prompt 1

Download and extract DMSO_DPPC_Project_Starter.zip. Open the extracted dmso-dppc-md folder in your local Codex environment. If working only in a cloud environment, first make the project files available there; a cloud shell is not automatically your Mac or CIRCE.

## Prompt 1 — Set up the private GitHub repository

I am organizing my USF Samanta Lab DMSO-DPPC molecular dynamics project. The current folder contains the starter files prepared for this project.

Read README.md, AGENTS.md, PROJECT_PLAN.md, PARAMETERS.md, RUN_LOG.md, and NEXT_STEPS.md. Use these existing files as the starting record.

Create a PRIVATE GitHub repository named dmso-dppc-md under my authenticated personal GitHub account, initialize the local Git repository if needed, commit these files, and push them. This prompt authorizes the initial private repository creation, commit, and push.

First inspect the current folder, any existing Git repository/remotes, the Git installation, configured commit identity, and available GitHub authentication. Verify the actual owner and remote. If this named repository already exists, inspect it and preserve its existing work. Do not create a second repository or overwrite unrelated content.

If GitHub CLI is available, check its authentication without printing tokens. If it is missing, explain the minimal setup needed and help me complete it. If a login or missing commit identity requires my input, give me the exact step; do not invent a name/email or ask me to paste a password/token into chat. Continue all local preparation that can be completed while remote access is unresolved.

Keep the parameter values, sources, agreement markers, and unresolved statuses as written. In PARAMETERS.md, a star means a selected working project choice, and its reason appears below the tables. Do not turn an unselected example into an agreed value.

Inspect the files being committed. Include the small notebook, source-reference, and template files. Keep trajectory/checkpoint/energy files and credentials out of the commit. Source snapshots under references are historical reference material, not active simulation inputs.

Record the setup actions and actual outcomes in RUN_LOG.md and NEXT_STEPS.md. Commit the prepared project with a clear message, then create/push the private remote using the available authenticated workflow. Never report a push as successful until it has succeeded. Do not force-push or replace an existing remote without resolving the actual conflict.

This is an organization task. Do not build a membrane, change the scientific settings, install simulation software, or launch simulations during this task.

Finish by reporting:
1. The actual repository URL and verified private visibility.
2. The local project folder and active branch.
3. The commit hash and whether the push succeeded.
4. Any unresolved access issue, stated precisely.
5. The next single practical step in plain language.

## Prompt 2 — Resume after a break

Continue my DMSO-DPPC project from this repository.

Read AGENTS.md, PROJECT_PLAN.md, PARAMETERS.md, NEXT_STEPS.md, the latest RUN_LOG.md entries, and relevant run records. Inspect the actual Git status and existing inputs/output evidence. Do not assume an earlier planned command ran.

Tell me briefly:
- Which machine/environment you are working in.
- What has been completed and what evidence supports it.
- What remains proposed or unresolved.
- The next concrete step and why it is needed.

Complete any read-only setup checks needed to make that step concrete. Do not change selected parameters or start a long simulation merely to resume the project. If an expected file cannot be opened, name the file and explain the access/read problem.

## Prompt 3 — Record a parameter decision

We have agreed to the following parameter decision:

[Paste the parameter name, selected value, and our discussion or reason here.]

Read the current PARAMETERS.md and relevant sources. Update the matching row, add a star to the selected working value, and add or revise its explanation below the tables. Record the source title, exact paper page or official file, version/date where known, and whether the value came directly from a source or is our own project choice.

Add a dated RUN_LOG.md entry stating the previous value/status, the new decision, its rationale, who agreed, affected runs, and whether existing results would need reevaluation. Update NEXT_STEPS.md if this resolves an open item.

Preserve earlier decisions in the log. Do not claim that agreement proves validation. If the requested value conflicts with the model or a documented software requirement, explain the conflict before changing an executable protocol.

Review the changes, then commit and push only these project-record changes. This prompt authorizes that commit and push to the verified private repository. Report the commit hash and the push result.

## Prompt 4 — Save the end of a work session

Record and save the work actually completed in this DMSO-DPPC session.

Inspect the current changes and available command output. Update RUN_LOG.md with the goal, date/timezone, machine, software versions, commands actually executed, input files, results, errors, fixes, and unresolved items. Clearly label commands that were only proposed.

For any simulation performed, update its run record with its actual composition, exact settings, seeds, start structure, software/model versions, job ID when applicable, output location, and status. Include the code/input commit used to launch it. Do not fabricate missing metadata.

Update PARAMETERS.md only for decisions we actually made, retaining the star-and-explanation rule. Update NEXT_STEPS.md with the stopping point and exact next action.

Review the diff and file list. Commit only the relevant small project files and push to the verified private remote. This prompt authorizes the commit and push. Report the commit hash, push outcome, and remaining issues. If a run is still active, record that state and the next check; do not imply completion or stop it merely to end the notebook session.

## Prompt 5 — Prepare the small training step

Prepare the next step for our approximately 50-DPPC, DMSO-free training system.

Read the project records and inspect the actual execution environment first. Verify gmx --version and relevant installed builder tools. Do not assume a cloud shell has access to my Mac installation or CIRCE.

Give me one concrete step with:
- What we are doing and why.
- Exact inputs and their sources.
- Any proposed values clearly labeled.
- The command or small script to use.
- Expected output and a simple success check.
- A realistic note if the workload belongs on CIRCE.

Prepare the needed small input files when the choices are already settled. If a scientific value is unresolved, explain the concrete decision rather than silently choosing it. Keep the modern model separate from historical D1/D2 parameters. Resolve the GROMACS pressure-control compatibility issue before generating a run-ready protocol. This prompt is preparation only; do not launch production runs or submit cluster jobs.

## Prompt 6 — Apply a reviewed instruction from this chat

Apply the following reviewed instruction to the existing DMSO-DPPC project:

[Paste the instruction here.]

Read the project records first and identify the files and parameter decisions affected. Carry out the work within the instruction's scope, recording commands and results in RUN_LOG.md. Preserve selected parameters unless the pasted instruction explicitly changes them. Update source references, explanations for starred choices, and NEXT_STEPS.md when applicable.

If the instruction requests execution, verify the relevant machine/environment and run only the stated work. Do not expand a small task into additional research simulations.

Review the resulting diff, commit the relevant small files, and push to the verified private repository. This prompt authorizes the commit and push. Report what changed, what was actually checked or run, the commit hash, and the push result.

## Reference instructions

- Codex CLI/local repository workflow: https://learn.chatgpt.com/docs/codex/cli
- Adding a local project to GitHub: https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github
- GitHub CLI repository creation: https://cli.github.com/manual/gh_repo_create

Documentation checked 2026-09-25. The prompts require inspecting the actual environment rather than assuming a particular interface or authentication state.

