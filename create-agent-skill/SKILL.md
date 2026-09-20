---
name: create-agent-skill
description: Create and validate reusable agent skills with the standard SKILL.md format.
---

# Create Agent Skill

## Overview
This skill teaches how to create custom skills for various AI agents (opencode, Qwen Code, Zed). It covers the structure, location, and validation requirements for each agent's skill format.

## Skill Structure
A skill is a Markdown file with a specific structure:
- File name: `SKILL.md`
- Frontmatter with `name` and `description` fields
- Content in markdown format

## Agent-Specific Locations
- **opencode**: `~/.config/opencode/skills/` or `~/.agents/skills/`
- **Qwen Code**: `~/.qwen/skills/` or `~/.agents/skills/`
- **Zed**: `~/.config/zed/skills/` or `~/.agents/skills/`

## Validation Requirements
- **opencode**: Name must match regex pattern `^[a-z][a-z0-9_-]*[a-z0-9]$`
- **Qwen Code**: Allows Unicode in names
- **Zed**: Uses `disable-model-invocation` field

## Skill Types
1. **Global Skills**: Stored in shared directory `~/.agents/skills/` for all agents
2. **Project Skills**: Stored in project's `.qwen/skills/` or `.zed/skills/` directory

## Creating a Skill
1. Create a new Markdown file named `SKILL.md`
2. Add required frontmatter with `name` and `description`
3. Add your skill content in markdown format
4. Place in appropriate directory based on scope
