# autoresearch

This repository is a bootstrap for an autonomous LLM agent that is expected to run AI research end to end with minimal human intervention.

The repo includes several instruction templates:

File names are additive: a name includes the features that are present in that template.

- `FROM-SCRATCH`: starts without paper or existing-codebase inputs
- `BUILDING-ON-TOP-OF`: includes paper and existing-codebase inputs
- `DRIVE`: includes remote storage guidance via `rclone`
- `HARDWARE`: includes local compute or hardware guidance

Available templates:

- [AGENTS-FROM-SCRATCH.md](AGENTS-FROM-SCRATCH.md): the base from-scratch template
- [AGENTS-FROM-SCRATCH-DRIVE.md](AGENTS-FROM-SCRATCH-DRIVE.md): from-scratch template with drive guidance
- [AGENTS-FROM-SCRATCH-HARDWARE.md](AGENTS-FROM-SCRATCH-HARDWARE.md): from-scratch template with hardware guidance
- [AGENTS-FROM-SCRATCH-DRIVE-HARDWARE.md](AGENTS-FROM-SCRATCH-DRIVE-HARDWARE.md): from-scratch template with both drive and hardware guidance
- [AGENTS-BUILDING-ON-TOP-OF.md](AGENTS-BUILDING-ON-TOP-OF.md): paper/codebase variant
- [AGENTS-BUILDING-ON-TOP-OF-DRIVE.md](AGENTS-BUILDING-ON-TOP-OF-DRIVE.md): paper/codebase variant with drive guidance
- [AGENTS-BUILDING-ON-TOP-OF-HARDWARE.md](AGENTS-BUILDING-ON-TOP-OF-HARDWARE.md): paper/codebase variant with hardware guidance
- [AGENTS-BUILDING-ON-TOP-OF-DRIVE-HARDWARE.md](AGENTS-BUILDING-ON-TOP-OF-DRIVE-HARDWARE.md): paper/codebase variant with both drive and hardware guidance

The core behavior defined by these templates includes:

- search for relevant libraries, repos, and techniques before building custom solutions
- set up the environment and dependencies explicitly
- when the chosen template includes them, use the available storage and hardware resources for the project
- implement iteratively with tests, logging, and regular execution checks
- run experiments, inspect outputs, record findings, and revise the plan continuously
- keep `README.md` and `AGENTS.md` up to date as living project documents
- commit and push progress regularly to GitHub
- produce end artifacts including code, experiment results, trained, fine-tuned, or steered model artifacts, and a LaTeX research paper

The intent is not just to write code. The agent is instructed to own the full loop of AI research and engineering work: planning, implementation, experimentation, debugging, documentation, and paper writing.

In practice, this repo serves as an execution scaffold for autonomous AI research projects where an LLM agent is expected to:

- work through an AI research problem from setup to results
- make grounded decisions based on code, experiments, and external research
- keep an explicit running plan in version control
- validate that results make sense, that the code runs end to end, and that logging is sufficient
- continue iterating until the project reaches a complete research-paper stage

The workflow assumes [`uv`](https://docs.astral.sh/uv/) for environment management and GitHub for version control. Some variants also include optional remote artifact storage via [`rclone`](https://rclone.org/), for example [`rclone ls`](https://rclone.org/commands/rclone_ls/) `googledrive:projects/<project-name>` (where `googledrive` is the name of a configured rclone remote).

If you want to understand how the agent should behave, start with the template that matches your project constraints.

The keep-or-discard research loop, the autonomy rules and the example pacing in the templates are adapted from [`program.md`](https://github.com/karpathy/autoresearch/blob/master/program.md) in [karpathy/autoresearch](https://github.com/karpathy/autoresearch).

Do not remove any lines above the Scratchpad.
# Scratchpad
