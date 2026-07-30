# 🤖 Pi Agent Skills

A collection of reusable [Pi Coding Agent](https://github.com/earendil-works/pi-coding-agent) skills that extend the agent's capabilities for development workflows.

## Overview

Pi skills are YAML-frontmatter-driven prompt templates that define specialized behaviors for coding agents. Each skill file is self-contained and can be triggered by name or description to guide the agent through specific tasks.

## Skills

| Skill | Description |
|---|---|
| **doc-standardizer** | Ensures documentation, READMEs, and code comments follow consistent branding and formatting standards |
| **generate-readme** | Generates or updates comprehensive README files by inspecting project structure, source code, and configuration |
| **project-architect** | Creates development plans (`DEVPLAN.md`) with phased roadmaps for existing projects |
| **project-launcher** | Bootstraps new projects from scratch — folder creation, git init, templates, and planning |
| **python-ruff-linter** | Lints and formats Python code using Ruff (error checking, style enforcement, PEP 8 compliance) |
| **test-creator-js** | Generates unit tests for JavaScript/TypeScript code using Vitest with AAA pattern |

## Quick Start

### Adding Skills to Pi

Copy or symlink this repository into your Pi skills directory:

```bash
cp -r skills/* ~/.pi/agent/skills/
```

Pi will automatically discover and register the skills on next launch.

## Skill Format

Each skill is a single Markdown file with YAML frontmatter:

```yaml
---
name: skill-name
description: "Brief description of what the skill does"
---
```

The body of the file contains the instructions the agent follows when the skill is triggered.

## Development

### Creating a New Skill

1. Create a new file in this directory named after the skill (lowercase, hyphenated).
2. Add YAML frontmatter with `name` and `description`.
3. Write clear, step-by-step instructions in the body.
4. Commit the file.

### Structure

```
skills/
├── doc-standardizer
├── generate-readme
├── project-architect
├── project-launcher
├── python-ruff-linter
└── test-creator-js
```

## License

MIT
