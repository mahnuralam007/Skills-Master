# 🧠 Skills Master

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Antigravity Compatible](https://img.shields.io/badge/Agent-Antigravity%20%2F%20Claude%20Code-blueviolet.svg)](#)
[![Skills Count](https://img.shields.io/badge/Skills-16%20Included-success.svg)](#-skills-catalog)
[![Portfolios](https://img.shields.io/badge/Portfolios-4%20Templates-orange.svg)](#-portfolios-showcase)

**The premier agentic engineering toolkit & production skills library for Antigravity, Claude Code, and autonomous AI agents.**

[Explore Skills](#-skills-catalog) • [Portfolios](#-portfolios-showcase) • [Installation](#-installation--quick-start) • [Skill Authoring](#-skill-authoring-guide) • [Contributing](#-contributing)

</div>

---

## 📖 Overview

**Skills Master** provides battle-tested behavioral skills, engineering workflows, and orchestration protocols designed for modern AI coding assistants (such as Google Antigravity and Claude Code). 

Agents equipped with these skills follow rigorous software engineering discipline:
- **Test-Driven Development (TDD)** and **Systematic Debugging** instead of haphazard trial-and-error.
- **Git Worktree Isolation** and **Structured Branch Finishing** for safe multitasking.
- **Multi-Agent Orchestration** and **Subagent Delegation** for parallel execution.
- **Evidence-Before-Assertions** verification protocols prior to declaring tasks complete.

Additionally, this repository contains **4 modern web portfolio templates** ready for immediate deployment.

---

## 🗂️ Skills Catalog

All skills reside in [`.agent/skills/`](.agent/skills/) and adhere strictly to the Antigravity YAML frontmatter and progressive disclosure specifications.

| Category | Skill Name | Description | Triggers / Use Cases |
| :--- | :--- | :--- | :--- |
| **Strategy & Planning** | [`brainstorming`](.agent/skills/brainstorming/) | Explores intent, requirements, and design before implementation. | Creative feature work, component architecture, UX design. |
| | [`writing-plans`](.agent/skills/writing-plans/) | Produces granular, step-by-step implementation plans with checkpoints. | Multi-step tasks, architectural refactors, feature specs. |
| | [`executing-plans`](.agent/skills/executing-plans/) | Executes implementation plans in structured batches with review stops. | Step-by-step task execution from a written plan. |
| **Engineering Quality** | [`test-driven-development`](.agent/skills/test-driven-development/) | Strict RED-GREEN-REFACTOR cycle with failing test verification. | Writing new features, bug fixes, API implementations. |
| | [`systematic-debugging`](.agent/skills/systematic-debugging/) | 4-phase root-cause investigation before proposing fixes. | Test failures, unexpected runtime errors, performance regressions. |
| | [`verification-before-completion`](.agent/skills/verification-before-completion/) | Mandates running verification commands and observing evidence. | Before claiming tasks are fixed, complete, or ready to merge. |
| **Code Review & Alignment**| [`requesting-code-review`](.agent/skills/requesting-code-review/) | Prepares structured review requests against requirements. | Completing features, before merging branches. |
| | [`receiving-code-review`](.agent/skills/receiving-code-review/) | Technical rigor when processing review feedback—requires verification. | Handling code review comments or suggested changes. |
| **Git & Workspace** | [`using-git-worktrees`](.agent/skills/using-git-worktrees/) | Creates isolated git worktrees with safety checks and clean directory selection. | Isolated feature development, parallel tasks, avoiding git stash conflicts. |
| | [`finishing-a-development-branch`](.agent/skills/finishing-a-development-branch/) | Formulates 4 clear completion choices: Merge, PR, Keep, or Discard. | When work is done and tests pass. |
| **Agent Orchestration** | [`dispatching-parallel-agents`](.agent/skills/dispatching-parallel-agents/) | Dispatches 2+ independent tasks across parallel subagents without shared state. | Multi-file independent migrations, parallel test suites. |
| | [`subagent-driven-development`](.agent/skills/subagent-driven-development/) | Drives implementation plans by dispatching specialized subagents per task. | Large feature plans needing isolated context per step. |
| | [`using-superpowers`](.agent/skills/using-superpowers/) | Core routing protocol ensuring skills are invoked before any action or answer. | Automatically triggered at the start of conversations. |
| **Authoring & Brand** | [`creating-skills`](.agent/skills/creating-skills/) | Interactive generation of predictable `.agent/skills/` structures. | When asked to create or scaffold new agent skills. |
| | [`writing-skills`](.agent/skills/writing-skills/) | Comprehensive authoring manual, constraints, and test scenarios for skills. | Authoring, editing, or auditing skill files. |
| | [`brand-identity`](.agent/skills/brand-identity/) | Single source of truth for design tokens, technology stack, and tone of voice. | UI design, styling, component building, copywriting. |

---

## 🎨 Portfolios Showcase

Located in the [`portfolios/`](portfolios/) directory, these standalone, responsive web portfolios demonstrate modern design aesthetics without heavy framework overhead:

- **[Classic Portfolio](portfolios/classic/index.html)**: Clean, professional resume-style portfolio showcasing projects, experience, and contact forms.
- **[Glassmorphic Portfolio](portfolios/glassmorphic/index.html)**: Dark-mode aesthetic featuring frosted glass cards, subtle blur effects, and vibrant neon accents.
- **[Interactive Portfolio](portfolios/interactive/index.html)**: Dynamic layout with terminal-style command line accents, interactive cards, and smooth transitions.
- **[Minimalist Portfolio](portfolios/minimalist/index.html)**: Typography-centric, distraction-free aesthetic with high contrast and fast load times.

To preview any portfolio locally:
```bash
# Open directly in your default browser (PowerShell)
Start-Process ./portfolios/glassmorphic/index.html
```

---

## 🚀 Installation & Quick Start

### Option 1: Use in an Existing Project (Workspace Level)
Copy the `.agent/skills` folder directly into your project's root:

```bash
# Clone this repository
git clone https://github.com/your-username/skills-master.git

# Copy skills to your target workspace
cp -r skills-master/.agent/skills /path/to/your-project/.agent/skills
```

### Option 2: Global Configuration (Antigravity IDE)
To make these skills available across all your workspaces in Antigravity:

```bash
# Copy into global Antigravity config
cp -r skills-master/.agent/skills/* ~/.gemini/config/skills/
```

---

## ✍️ Skill Authoring Guide

Want to build your own skills? Follow the system instructions in [`antigravity-skill-creator.md`](antigravity-skill-creator.md):

1. **Folder Hierarchy**:
   ```
   .agent/skills/<skill-name>/
   ├── SKILL.md       # (Required) Main instructions & frontmatter
   ├── scripts/       # (Optional) Executable scripts
   ├── examples/      # (Optional) Reference implementations
   └── resources/     # (Optional) Templates, assets, or configs
   ```
2. **Naming Convention**: Use gerund form in kebab-case (e.g., `managing-databases`, `optimizing-queries`).
3. **YAML Frontmatter**:
   ```yaml
   ---
   name: your-skill-name
   description: Brief description in third person. Must specify triggers and keywords.
   ---
   ```
4. **Progressive Disclosure**: Keep `SKILL.md` under 500 lines. Break complex topics into dedicated secondary files linked within the document.

---

## 🤝 Contributing

Contributions are welcome! Whether you are adding a new skill, refining an existing one, or contributing an aesthetic portfolio template:

1. Review [CONTRIBUTING.md](CONTRIBUTING.md) for style and validation requirements.
2. Fork the repository and create your feature branch:
   ```bash
   git checkout -b feature/new-skill-name
   ```
3. Submit a Pull Request referencing the checklist in `.github/pull_request_template.md`.

---

## 📄 License

This repository is licensed under the [MIT License](LICENSE).
