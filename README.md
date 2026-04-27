<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/branding/01-horizontal-dark.png">
    <img src="assets/branding/02-horizontal-light.png" alt="FX Studio AI" width="600"/>
  </picture>
</div>

<h1 align="center">Superpowers</h1>

<p align="center">
  <strong>Agentic skills framework and software development methodology for coding agents</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Claude%20Code-blueviolet" alt="Platform"/>
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License"/>
  <img src="https://img.shields.io/badge/language-Shell-lightgrey" alt="Language"/>
</p>

## What It Does

Superpowers is a structured software development methodology built on the principle that each skill should do 1% of the work and delegate the rest via subagents. Originally created by [Jesse Vincent](https://github.com/obra) (obra/superpowers), this is a fork and distribution. It provides 14 specialized skills that cover the entire development lifecycle -- from brainstorming through code review to branch management.

## Features

- **The 1% Rule** -- Each skill handles exactly one concern and delegates everything else, keeping agents focused and composable.
- **14 Specialized Skills** -- Purpose-built skills for every phase of development.
- **Subagent Delegation** -- Skills spawn focused subagents for parallel execution and deep work.
- **Full Lifecycle Coverage** -- From initial brainstorming to finishing and landing a development branch.
- **Test-Driven Development** -- RED-GREEN-REFACTOR enforced at every step.
- **Adversarial Review** -- Two-stage review (spec compliance, then code quality) catches issues early.

## Installation

```bash
claude plugin add fx-studio-ai/superpowers
```

## Skills

| Skill | Description |
|-------|-------------|
| `using-superpowers` | Router -- initializes the framework and routes to the right skill |
| `brainstorming` | Socratic design refinement and ideation |
| `writing-plans` | Detailed implementation plans with exact file paths and verification steps |
| `executing-plans` | Batch execution with human checkpoints |
| `test-driven-development` | TDD workflow with red-green-refactor cycle |
| `subagent-driven-development` | Decompose work and dispatch to subagents with two-stage review |
| `dispatching-parallel-agents` | Launch multiple agents concurrently for independent tasks |
| `requesting-code-review` | Pre-review checklist and structured review requests |
| `receiving-code-review` | Process review feedback and apply changes |
| `systematic-debugging` | 4-phase root cause analysis and fix |
| `verification-before-completion` | Final verification pass before marking work done |
| `finishing-a-development-branch` | Merge/PR decision workflow and worktree cleanup |
| `using-git-worktrees` | Parallel development with isolated branches |
| `writing-skills` | Create new superpowers skills following best practices |

## Usage

Start any session by invoking the router:

```bash
/using-superpowers
```

The router analyzes your task and activates the appropriate skill. You can also invoke any skill directly by name.

## Architecture

```
/using-superpowers (router)
  |
  +-- brainstorming --> writing-plans --> executing-plans
  |                                         |
  |                     +-------------------+
  |                     |
  +-- subagent-driven-development
  |     |
  |     +-- dispatching-parallel-agents
  |     +-- requesting-code-review
  |     +-- receiving-code-review
  |
  +-- test-driven-development (enforced across all execution)
  |
  +-- systematic-debugging --> verification-before-completion
  |
  +-- finishing-a-development-branch
        |
        +-- using-git-worktrees
```

## License

MIT

---

<div align="center">
  <strong>Built by <a href="https://github.com/fernandoxavier02">Fernando Xavier</a></strong>
  <br/>
  <a href="https://fxstudioai.com">FX Studio AI</a> — Business Automation with AI
</div>
