# Component Specifications
 
 ## Button
 Variants: primary, secondary, outline, ghost
 Sizes: sm (32px), md (40px), lg (48px)
 States: default, hover, active, disabled, focus
 Icon support: left, right, icon-only, none
 Total variants: 4 x 3 x 4 x 4 = 192
 
 Token bindings:
 - Fill (primary): semantic/primary/default → hover → active
 - Fill (secondary): semantic/surface/neutral-subtle → hover → active
 - Text (primary): semantic/text/on-primary
 - Text (secondary): semantic/text/primary
 - Border radius: radius/component/button (8px)
 - Padding horizontal: spacing/component/padding-md (12px)
 - Padding vertical: spacing/component/padding-sm (8px)
 - Typography: typography/button/md (14px, weight 500)
 
 ## Input Field
 Types: text, email, password, number, search
 Sizes: sm (32px), md (40px), lg (48px)
 States: default, focused, error, disabled
 Features: label, helper text, error message, prefix/suffix icon
 
 Token bindings:
 - Border: semantic/border/default → semantic/border/focus (focused) → semantic/border/error (error)
 - Background: semantic/surface/input
 - Text: semantic/text/primary
 - Placeholder: semantic/text/subtle
 - Label: semantic/text/secondary
 - Border radius: radius/component/input (8px)
 - Padding: spacing/component/padding-md
 
 ## Card
 Elevation: flat, raised, elevated
 Padding: compact (16px), default (24px), spacious (32px)
 States: default, hover, pressed, disabled
 Structure: header (optional), body, footer (optional)
 
 Token bindings:
 - Background: semantic/surface/card
 - Border: semantic/border/default
 - Border radius: radius/component/card (12px)
 - Padding: spacing/component/padding-[size]
 - Shadow: elevation/[level]
 
 [Add all 8 components with their full specs]