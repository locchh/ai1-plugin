# Agent Skill Generator Prompt

Copy this, fill in the `{{placeholders}}`, and give it to your AI agent.

```
Create an Agent Skill following the agentskills.io standard.

## Skill Definition

- **Name:** {{kebab-case-name}}
- **What it does:** {{1-2 sentence description of what this skill does}}
- **When to use it:** {{specific triggers — when should an agent activate this?}}
- **Target stack/domain:** {{e.g. Python/FastAPI, React/TypeScript, DevOps, etc.}}
- **Platform:** {{universal | claude-code}}

## Core Instructions

{{Numbered list of step-by-step actions the agent should follow when this skill is active. Write in imperative mood. Be specific and unambiguous.}}

## Examples (1-2)

**Input:** {{what the agent receives or starts with}}
**Output:** {{what the agent should produce}}

## Edge Cases

{{Bullet list of special scenarios and how to handle them}}

## Supporting Files (optional)

- **scripts/**: {{list executable scripts needed, or "none"}}
- **references/**: {{list reference docs to load on demand, or "none"}}

## Constraints

- SKILL.md body must be < 500 lines
- Name: lowercase + digits + hyphens only, no leading/trailing/consecutive hyphens
- Description: 1-1024 chars, include keywords for agent discoverability
- Write to: {{output directory, e.g. skills/{{name}}/SKILL.md}}

Generate the complete SKILL.md with YAML frontmatter + markdown body, plus any supporting files listed above.
```
