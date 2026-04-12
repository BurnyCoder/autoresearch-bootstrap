# autoresearch

This repository is a bootstrap for an autonomous LLM agent that is expected to run research end to end with minimal human intervention.

The core instructions live in [AGENTS.md](AGENTS.md). That file defines how the agent should operate across the full research lifecycle:

- read the source paper and the entire in-repo codebase before making changes
- search for relevant libraries, repos, and techniques before building custom solutions
- set up the environment and dependencies explicitly
- implement iteratively with tests, logging, and regular execution checks
- run experiments, inspect outputs, record findings, and revise the plan continuously
- keep `README.md` and `AGENTS.md` up to date as living project documents
- commit and push progress regularly to GitHub
- produce end artifacts including code, experiment results, model outputs, and a LaTeX research paper

The intent is not just to write code. The agent is instructed to own the full loop of scientific and engineering work: planning, implementation, experimentation, debugging, documentation, and paper writing.

In practice, this repo serves as an execution scaffold for autonomous research projects where an LLM agent is expected to:

- work through a paper-driven problem from setup to results
- make grounded decisions based on code, experiments, and external research
- keep an explicit running plan in version control
- validate that results are meaningful, reproducible, and well logged
- continue iterating until the project reaches a complete research-paper stage

If you want to understand how the agent should behave, start with [AGENTS.md](AGENTS.md).
