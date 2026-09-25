# Run log and electronic lab notebook

Entries describe work actually done. Planned commands and proposed runs must be labeled as planned. Dates use ISO format. Include a timezone when recording command execution times.

## Simulation index

No completed simulation has been established from the records reviewed for this package.

| Run ID | Purpose | Actual state | Record |
| --- | --- | --- | --- |
| TRAIN-001 | Approximately 50-DPPC, DMSO-free training system | Planned; inputs, builder, box, and duration not yet finalized | No run record yet |

Reserve research IDs such as SA-D000-R01 and IN-D006-R01 only when preparing actual runs. SA = self-assembly, IN = INSANE; D000/D006/D012 indicate target DMSO mol%; R01 identifies a repeat. Record actual composition separately.

## 2026-09-25 — Establish the project record

**Goal:** organize the project, source the parameter table, and prepare a Codex/GitHub handoff.

**Work completed in this organizational session:**
- Reviewed the available parameter/method records and the earlier accuracy audit.
- Carried forward the selected modern Martini project and two construction methods.
- Added a parameter table with source references, explicit status, starred choices, and explanations.
- Prepared copyable Codex prompts for setup, resuming, parameter decisions, and end-of-session commits.
- Preserved source snapshots used for the parameter review, with SHA-256 identifiers in references/source_evidence.json.

**Evidence carried forward, not newly executed on the Mac:**
- A saved September 23 terminal record shows successful gmx --version output: GROMACS 2026.3-Homebrew.
- That record reports 64-bit memory model, mixed precision, thread_mpi, and GPU support disabled.
- This does not establish the current state of CIRCE or prove that any bilayer simulation has run.

**Decisions recorded:**
- Preserve the modern Martini 3/2025-lipid plan.
- Use approximately 50 DPPC for training; 512 for research.
- Use 323 K, 1 bar, and the initial 0/6/12 mol% comparison.
- Compare self-assembled and INSANE-built membranes after appropriate equilibration.
- Retain 800 ns as an initial research planning target.
- Use a private GitHub repository with this notebook as the working record after setup.

**Unresolved:** final runtime-control combination; hydration and mixture counts; training duration; repeat count; output and analysis intervals; CIRCE version/resources/storage.

**Git status:** the starter package itself is not a GitHub repository. No remote URL, commit, or successful push is claimed. The Codex setup task must record those facts after they exist.

**Research results:** none generated in this organizational session.

**Next action:** open the extracted project folder in Codex and use Prompt 1 in CODEX_PROMPTS.md.

## Future entries

Copy templates/SESSION_ENTRY.md below for each work session. For any simulation, also create a run record from templates/RUN_RECORD.md.

When making a parameter choice, state the old and new values, source, reason, date, who agreed, affected runs, and whether reruns are needed. Preserve the record of failed attempts.


## 2026-09-24 20:58:01 EDT — Prompt 1: local repository preparation

- Scope: organization and initial private GitHub setup, authorized by the user. No simulations or simulation-software installation performed.
- Execution environment: local macOS, Darwin arm64, project `/Users/mila/Downloads/dmso-dppc-md`; not CIRCE. Starter dates remain as written; this entry uses the machine's local EDT date.
- Read the project notebook, plan, parameters, sources, templates, environment record, and Prompt 1. Inspected all 18 small text files; no trajectory, checkpoint, energy, credential, or supplied PDF files are included.
- `git status --short` initially returned `fatal: not a git repository (or any of the parent directories): .git`; no existing repository or remote was present.
- `git --version`: 2.50.1 (Apple Git-155). Existing configured identity retained: ReefGuardian <ayacono@usf.edu>.
- `gh` initially returned `command not found`; `brew install gh` succeeded, installing GitHub CLI 2.101.0. `gh auth status` then reported no signed-in GitHub hosts. Browser authorization started with `gh auth login --hostname github.com --git-protocol https --web`; completion pending.
- `git init -b main` succeeded. SHA-256 checks of all four reference snapshots matched `references/source_evidence.json`. Original-file hashes were retained temporarily outside the repository for preservation checks.
- Scientific parameters, source citations, asterisks, explanations, unresolved decisions, and historical reference snapshots remain unchanged. Existing ignore rules exclude large simulation outputs and credentials.
- Current outcome: local Git initialized; initial commit and remote creation/push pending. No GitHub URL or successful push is claimed at this point.
- Next action: complete GitHub sign-in, verify the authenticated personal owner and whether `dmso-dppc-md` exists, then commit and push without overwriting existing work.
