# autoresearch

This repository is a bootstrap for an autonomous LLM agent that is expected to run AI research end to end with minimal human intervention.

The repo includes several instruction templates:

- [AGENTS.md](AGENTS.md): the generic autonomous AI research template
- [AGENTS-BUILDING-ON-TOP-OF.md](AGENTS-BUILDING-ON-TOP-OF.md): a variant for projects that start from an existing paper and codebase
- [AGENTS-NO-DRIVE.md](AGENTS-NO-DRIVE.md): the generic template without remote-drive references
- [AGENTS-BUILDING-ON-TOP-OF-NO-DRIVE.md](AGENTS-BUILDING-ON-TOP-OF-NO-DRIVE.md): the paper/codebase variant without remote-drive references

The core behavior defined by these templates includes:

- search for relevant libraries, repos, and techniques before building custom solutions
- set up the environment and dependencies explicitly
- use the available local compute and remote storage resources for the project
- implement iteratively with tests, logging, and regular execution checks
- run experiments, inspect outputs, record findings, and revise the plan continuously
- keep `README.md` and `AGENTS.md` up to date as living project documents
- commit and push progress regularly to GitHub
- produce end artifacts including code, experiment results, model outputs, and a LaTeX research paper

The intent is not just to write code. The agent is instructed to own the full loop of AI research and engineering work: planning, implementation, experimentation, debugging, documentation, and paper writing.

In practice, this repo serves as an execution scaffold for autonomous AI research projects where an LLM agent is expected to:

- work through an AI research problem from setup to results
- make grounded decisions based on code, experiments, and external research
- keep an explicit running plan in version control
- validate that results are meaningful, reproducible, and well logged
- continue iterating until the project reaches a complete research-paper stage

The workflow assumes `uv` for environment management, GitHub for version control, and optional remote artifact storage via `rclone`, for example `rclone ls googledrive:projects/<project-name>`.

If you want to understand how the agent should behave, start with the template that matches your project constraints.
