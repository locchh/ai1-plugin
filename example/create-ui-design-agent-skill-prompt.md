# UI Design Skill — Example Input

```
Create an Agent Skill following the agentskills.io standard.

## Skill Definition

- **Name:** ui-design-system
- **What it does:** Generates consistent UI components, layouts, and design tokens following a design system. Enforces spacing, color, typography, and accessibility standards across React/TypeScript projects.
- **When to use it:** When creating new UI components, building page layouts, choosing colors/typography, setting up design tokens, or reviewing UI code for design consistency.
- **Target stack/domain:** React 18+, TypeScript 5+, Tailwind CSS, shadcn/ui
- **Platform:** claude-code

## Core Instructions

1. Read the project's existing design tokens (colors, spacing, typography) before generating any UI code.
2. Use the 8pt spacing grid for all margins and padding (4, 8, 12, 16, 24, 32, 48, 64).
3. Apply the project's color palette via Tailwind classes — never use hardcoded hex/rgb values.
4. Structure components as: container > layout > content elements, using semantic HTML.
5. Ensure all interactive elements meet WCAG 2.1 AA contrast ratios (4.5:1 text, 3:1 large text).
6. Add aria-labels, roles, and keyboard navigation to all interactive components.
7. Use responsive breakpoints: sm (640px), md (768px), lg (1024px), xl (1280px).
8. Prefer shadcn/ui primitives (Button, Dialog, Card, etc.) over custom implementations.
9. Export component props as TypeScript interfaces with JSDoc descriptions.

## Examples (1-2)

**Input:** "Create a user profile card with avatar, name, role, and action buttons"
**Output:** A React component using Card from shadcn/ui, Avatar component, proper spacing (gap-4, p-6), responsive layout, accessible button labels, and typed props interface.

**Input:** "Set up design tokens for a SaaS dashboard"
**Output:** Tailwind config extension with brand colors (primary, secondary, accent, destructive), semantic tokens (background, foreground, muted, border), typography scale, and spacing overrides.

## Edge Cases

- If no design tokens exist yet, generate a starter set and ask user to confirm before proceeding.
- If shadcn/ui is not installed, fall back to plain Tailwind with equivalent patterns.
- If a requested component conflicts with an existing one, flag the overlap and suggest extending the existing component.
- For dark mode, ensure all color tokens have dark variants defined.

## Supporting Files (optional)

- **scripts/**: none
- **references/**: design-tokens-reference.md (starter token sets, color palette guide, typography scales)

## Constraints

- SKILL.md body must be < 500 lines
- Name: lowercase + digits + hyphens only, no leading/trailing/consecutive hyphens
- Description: 1-1024 chars, include keywords for agent discoverability
- Write to: skills/ui-design-system/SKILL.md

Generate the complete SKILL.md with YAML frontmatter + markdown body, plus any supporting files listed above.
```
