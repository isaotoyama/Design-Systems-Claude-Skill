SKILL.md Template (Copy-Paste Ready):

---
name: design-system
description: Apply my design system tokens, naming conventions, component specs, and accessibility rules to all UI and design work including Figma components and React code.
---

# [Your System Name] Design System

Use this Skill when:
- Creating new Figma components
- Building UI layouts
- Generating React/TypeScript components
- Writing design documentation
- Reviewing components for consistency
- Exporting tokens or Storybook stories

## Core Principles

1. Every color, spacing, and typography value MUST use semantic tokens
2. No hardcoded values — ever
3. All components meet WCAG 2.1 AA minimum
4. Naming follows: category/role/state pattern
5. All components support light and dark mode
6. Mobile-first responsive
7. Keyboard navigation throughout

## Token Architecture

### Naming Conventions

Colors (Primitive): primitive/[color]/[shade]
Examples: primitive/blue/600, primitive/gray/100

Colors (Semantic): semantic/[category]/[state]
Examples: semantic/primary/default, semantic/primary/hover, semantic/text/on-primary, semantic/surface/neutral-subtle

Spacing: spacing/[context]/[size]
Examples: spacing/component/padding-sm, spacing/layout/gap-md

Typography: typography/[usage]/[size]
Examples: typography/heading/lg, typography/body/md

Border Radius: radius/component/[component-name]
Examples: radius/component/button, radius/component/card

### Variable Collections
1. Colors — modes: light, dark
2. Spacing — single mode
3. Border Radius — single mode
4. Typography — single mode
5. Icon Sizes — single mode

### Spacing Scale
Base unit: 4px
Scale: 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96px

### Border Radius Values
sm: 4px, md: 8px, lg: 12px, xl: 16px, full: 9999px

## Color Tokens
For full color token list with light/dark mode values:
See [references/color-tokens.md](references/color-tokens.md)

## Typography Tokens
For font families, sizes, weights, and line heights:
See [references/typography.md](references/typography.md)

## Spacing Tokens
For complete spacing scale and usage guidelines:
See [references/spacing.md](references/spacing.md)

## Component Specifications
For component APIs, variants, states, and token bindings:
See [references/components.md](references/components.md)

## Component Building Rules

1. Generate HTML artifact first (cheaper tokens), iterate until correct, then push to Figma
2. All fills must bind to semantic color variables
3. All strokes must bind to semantic color variables
4. All text must use typography tokens
5. All spacing must use spacing scale tokens
6. Every component needs: default, hover, active, disabled, focus states
7. Batch similar operations (create all variants at once)
8. Take a screenshot after creation for verification

## Quality Checklist (Run Before Finalizing Any Component)
- [ ] All fills bound to semantic color variables
- [ ] All strokes bound to semantic color variables
- [ ] All text uses typography tokens
- [ ] All spacing uses spacing scale tokens
- [ ] Light and dark mode variants exist
- [ ] All required states present (default, hover, active, disabled, focus)
- [ ] No hardcoded values in any property
- [ ] Accessible contrast ratios (4.5:1 text, 3:1 UI elements)
- [ ] Naming follows convention
- [ ] Screenshot taken and reviewed

## Storybook Requirements
- React + TypeScript
- CSS custom properties for all styling (no hardcoded values)
- Props match Figma variants
- CSF3 format for stories
- Dark mode toggle included
- Zero hardcoded values in final components