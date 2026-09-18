# Contributing to Skills Master

Thank you for your interest in contributing to **Skills Master**! We welcome contributions for new agent skills, workflow improvements, and portfolio templates.

---

## 🎯 Contribution Principles

Every skill in this repository serves as executable knowledge for autonomous AI agents (such as Antigravity and Claude Code). To ensure reliable agent performance, all contributions must adhere to the standards outlined below.

---

## 📋 Skill Standards & Quality Checklist

### 1. Naming Standards
- Folder and YAML frontmatter name must use **gerund form** in kebab-case:
  - ✅ Good: `optimizing-queries`, `securing-endpoints`, `managing-dependencies`
  - ❌ Avoid: `query-optimizer`, `endpoint-security`, `dependency-manager`
- Maximum length: **64 characters**.
- Use lowercase alphanumeric characters and hyphens only (`[a-z0-9-]`).
- Never prefix names with company or platform trademarks (e.g., no `claude-`, `anthropic-`).

### 2. YAML Frontmatter Standards
Every `SKILL.md` must begin with YAML frontmatter:
```yaml
---
name: gerund-name
description: Third-person explanation of what this skill does and explicit trigger conditions.
---
```
- **Description**: Written in **third-person** (e.g., *"Analyzes database schemas..."* not *"I analyze schemas..."* or *"Use this to analyze schemas..."*).
- **Triggers**: Must clearly list keywords or circumstances that activate the skill.
- Maximum description length: **1024 characters**.

### 3. File Organization & Progressive Disclosure
- **Directory Hierarchy**:
  ```
  .agent/skills/<skill-name>/
  ├── SKILL.md                 # Primary instructions & triggers
  ├── scripts/                 # (Optional) Helper scripts
  ├── examples/                # (Optional) Reference implementations
  └── resources/               # (Optional) Templates, schemas, data
  ```
- **File Length**: Keep `SKILL.md` under **500 lines**.
- **Progressive Disclosure**: If deep documentation or extensive reference material is required, link secondary files one level deep (e.g., `[See ADVANCED.md](resources/ADVANCED.md)`).
- **Paths**: Always use forward slashes (`/`), never backslashes (`\`).

### 4. Degrees of Freedom
- **Bullet Points**: Use for heuristics, guidelines, and flexible decision-making.
- **Code Blocks / Pseudocode**: Use for templates and structural patterns.
- **Specific Terminal Commands**: Use for strict, fragile, or order-dependent operations.

---

## 🚀 Development & Submission Workflow

1. **Fork the Repository**:
   Click **Fork** on GitHub and clone your fork locally.

2. **Create a Feature Branch**:
   ```bash
   git checkout -b skill/your-skill-name
   # or for portfolios:
   git checkout -b portfolio/your-theme-name
   ```

3. **Author Your Skill / Asset**:
   - Reference [`antigravity-skill-creator.md`](antigravity-skill-creator.md) and [`.agent/skills/writing-skills/SKILL.md`](.agent/skills/writing-skills/SKILL.md) for detailed templates.
   - Run local validation: verify that links work, YAML syntax is valid, and line limits are respected.

4. **Commit Your Changes**:
   Follow conventional commits:
   ```bash
   git commit -m "feat(skills): add managing-containers skill"
   ```

5. **Submit a Pull Request**:
   Push your branch to GitHub and open a PR against the `main` branch. Complete the checklist provided in the PR template.

---

## ❓ Questions & Support

Have questions about designing a new workflow or structuring complex skills? Open a discussion or file a [New Skill Proposal](.github/ISSUE_TEMPLATE/new_skill.md) issue.
