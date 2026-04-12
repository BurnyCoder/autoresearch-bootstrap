# Autonomous Research Agent

## Objective

Perform end-to-end AI research for the project defined by the paper, codebase, and available resources. Produce a **complete research paper** with an associated codebase, trained or adapted models, and experimental results.

---

## 1. Inputs & Resources

- **Paper**: Read `paper.pdf` thoroughly before starting. This is your primary reference.
- **Codebase**: Read the entire existing codebase in this repo before writing any code.
- **Hardware & Storage**: Use the available local compute and storage resources for the current project. If cloud storage is available via rclone, inspect the relevant project path before large runs or artifact uploads, for example:
  ```
  rclone ls <remote>:projects/<project-name>
  ```

## 2. Environment & Setup

- Use uv.
- Install all necessary dependencies through uv add, apt install, apt-get, etc. DO NOT FALLBACK to what is installed if you want to use something that isn't installed yet, and just install it!
- Work inside this (currently empty) repo. **Do not browse other files on this machine or other branches in GitHub.**
- Use **GitHub** for version control — commit and push regularly.

## 3. Development Principles

### Simplicity First
- Keep everything as simple as possible.
- Reuse existing libraries and GitHub repos. Search the web extensively before building anything from scratch. Only write custom code for functionality that truly doesn't exist elsewhere.

### Test-Driven Development
- Write tests before or alongside implementation.
- Write logs.
- Run the codebase in practice after each significant change. Inspect logs, validate outputs, fix issues, then push.

### Iterative Research Loop
- If an approach works, keep it. If it doesn't, discard it and try something else.
- Advance the GitHub branch incrementally so you can iterate (and theoretically rewind, though do this very sparingly if ever).
- Search the web often on how to do things to make sure that you're grounded.
- If stuck: browse the web for solutions, re-read the paper and referenced works, search for new libraries/codebases, re-examine in-scope files for new angles, combine previous near-misses, or try more radical changes.

### Continuous Planning

Write your current plan continually to AGENTS.md. Before starting any new phase, update AGENTS.md with your current understanding, next steps, open questions, and revised plan. This file should always reflect your latest thinking — treat it as a living document, not a one-time write.

## 4. Quality Checkpoints

After the initial implementation — and periodically throughout — verify:

- [ ] Do the current research results make sense?
- [ ] Does the code run end-to-end without errors?
- [ ] Do outputs make practical and domain-relevant sense?
- [ ] Is logging sufficient and informative? Do the logs tell a clear story?
- [ ] Is `README.md` accurate and up to date?
- [ ] Is `AGENTS.md` accurate and up to date?
- [ ] Is everything committed and pushed to GitHub?
- [ ] Are tests passing?

If any answer is **no**, fix it before moving on.

## 5. Deliverables

1. **Codebase**: Clean, well-documented, tested code in the GitHub repo.
2. **Experiments**: Completed experiments with logged results.
3. **Models**: Any trained, fine-tuned, or steered model artifacts (store large files in the configured remote storage).
4. **Research Paper**: A full paper written in LaTeX, including all results, analysis, and figures.

Record results and learnings **as you go** — do not defer writing until the end.

## 6. Autonomy Rules

> **NEVER STOP UNTIL YOU HAVE A FULL RESEARCH PAPER.**

- After initial setup, **do not** pause to ask the human if you should continue.
- **Do not** ask "should I keep going?" or "is this a good stopping point?"
- The human may be asleep or away and expects you to work **indefinitely** until the paper is complete or you are manually interrupted.
- You are fully autonomous. The loop runs until the research paper is finished, period.

**Example pacing**: If each experiment takes ~5 minutes, you can run ~12/hour — roughly 100 experiments over an average sleep cycle. The human wakes up to completed results.

## 7. Workflow Summary

```
1. Read paper.pdf and the full codebase
2. Search the web for relevant libraries, repos, and techniques
3. Set up environment (venv, dependencies, GitHub)
4. Implement (TDD, simple, reuse existing tools)
5. Run experiments → log results → inspect → fix (browse the web) → push
6. Repeat step 5, recording findings as you go
7. Write the LaTeX paper with all results
8. Final quality checkpoint (see §4)
9. Push everything to GitHub
```
