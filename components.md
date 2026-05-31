I'm building a design system called [Your System Name]. Here's the context:
Brand: [Professional/playful/modern/etc.]
Tech stack: [React/Vue/etc.]
Target users: [Enterprise/consumers/etc.]
Accessibility: WCAG AA minimum
Color approach: [Describe your color strategy]
Design philosophy: [Component-first/minimal/etc.]
Constraints:
- Must support light and dark mode
- Mobile-first responsive
- Keyboard navigation throughout
- Minimize bundle size
Before we start building, acknowledge you understand this context and summarize the key principles back to me.


Token Creation Prompt

Create a design token system in Figma with these specifications:
COLORS:
- Primitive layer: Raw color scales (Blue: 50-900, Gray: 50-900, Green, Red, Yellow, Orange)
- Semantic layer: Purpose-based tokens that alias to primitives
Semantic token format: semantic/[category]/[state]
Examples: 
- semantic/primary/default
- semantic/primary/hover
- semantic/text/on-primary
- semantic/surface/neutral-subtle
TYPOGRAPHY:
- Families: [Your fonts]
- Sizes: [12, 14, 16, 18, 20, 24, 32, 40, 48, 64px]
- Weights: 400, 500, 600, 700
- Format: typography/[usage]/[size]
SPACING:
- Base unit: 4px
- Scale: 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96px
- Format: spacing/[context]/[size]
BORDER RADIUS:
- Values: 0, 4, 8, 12, 9999px
- Format: radius/component/[component-name]
Create separate variable collections for:
1. Colors (light mode)
2. Colors/Dark (dark mode overrides)
3. Spacing
4. Border Radius
5. Typography
6. Icon Sizes
Use descriptive names and add descriptions to each token explaining its purpose.


Component Creation Prompts
Button Component

Build a Button component set in Figma with:
Variants:
- Primary, Secondary, Outline, Ghost
Sizes:
- Small (32px height), Medium (40px), Large (48px)
States:
- Default, Hover, Pressed, Disabled
Icon support:
- Icon Left, Icon Right, Icon Only, No Icon
Requirements:
- All fills, strokes, and text must bind to semantic variables (no hardcoded values)
- Use typography/body-md for Medium buttons
- Use semantic/primary/default for Primary variant background
- Use spacing/component/padding-* for internal spacing
- Apply proper border radius from radius/component/button
Total variants: 4 variants × 3 sizes × 4 states × 3 icon configs = 144 variants
After creation, take a screenshot so I can review.
Input Component

Create an Input Field component set with:
Types:
- Text, Email, Password, Number, Search
Sizes:
- Small (32px), Medium (40px), Large (48px)
States:
- Default, Focused, Error, Disabled
Features:
- Label (optional)
- Helper text (optional)
- Error message (conditional on Error state)
- Prefix/suffix icon support
Token requirements:
- Border: semantic/border/default
- Border (focused): semantic/border/focus
- Border (error): semantic/border/error
- Background: semantic/surface/input
- Text: semantic/text/primary
- Placeholder: semantic/text/subtle
Bind all values to variables. Take a screenshot when done.
Card Component

Build a Card component with:
Elevation levels:
- Flat (no shadow), Raised (subtle shadow), Elevated (prominent shadow)
Padding options:
- Compact (16px), Default (24px), Spacious (32px)
States:
- Default, Hover, Pressed, Disabled
Structure:
- Header (optional)
- Body (content area)
- Footer (optional, for actions)
Use:
- semantic/surface/card for background
- Elevation tokens for shadows
- spacing/component/padding-* for internal spacing
- radius/component/card for corners
Screenshot after creation.


Audit Prompt:

Audit this [component name] for:
1. Variable coverage - Are ALL fills, strokes, and text bound to variables? List any hardcoded values.
2. Naming consistency - Do variant names follow our conventions?
3. Token accuracy - Is each property using the correct semantic token?
4. Accessibility - Are focus states visible? Does text meet contrast requirements?
5. Responsiveness - Does it work at different sizes?
Give me a scored report and flag any issues.
Fix Prompt (if issues found):

Fix the issues you found:
- Replace hardcoded [#hexvalue] with semantic/[correct-token]
- Rename variants to match [naming pattern]
- Add missing [state/variant]
Then verify with another screenshot.



Documentation Prompt:

Generate developer documentation for the [Component Name] component:
Include:
1. Component description (what it's for, when to use it)
2. Anatomy (what parts make up the component)
3. Props/Variants (all configurable options)
4. States (default, hover, pressed, disabled, etc.)
5. Token map (which design tokens are used where)
6. Accessibility notes (ARIA labels, keyboard navigation, focus management)
7. Usage guidelines (dos and don'ts)
8. Code example structure (pseudo-code for React)
Format as markdown.


Token Export
Export Prompt:

Export all design tokens from this Figma file as design_tokens.json in W3C Design Token Community Group format.
Include:
- All variable collections
- Resolved values
- Alias chains (show which semantic tokens point to which primitives)
- Descriptions
- Token type ($type: color, dimension, fontFamily, etc.)
- Light and dark mode splits
Organize by collection, then by category.
