---
name: The Design System
colors:
  surface: '#0b1326'
  surface-dim: '#0b1326'
  surface-bright: '#31394d'
  surface-container-lowest: '#060e20'
  surface-container-low: '#131b2e'
  surface-container: '#171f33'
  surface-container-high: '#222a3d'
  surface-container-highest: '#2d3449'
  on-surface: '#dae2fd'
  on-surface-variant: '#cbc3d7'
  inverse-surface: '#dae2fd'
  inverse-on-surface: '#283044'
  outline: '#958ea0'
  outline-variant: '#494454'
  surface-tint: '#d0bcff'
  primary: '#d0bcff'
  on-primary: '#3c0091'
  primary-container: '#a078ff'
  on-primary-container: '#340080'
  inverse-primary: '#6d3bd7'
  secondary: '#4edea3'
  on-secondary: '#003824'
  secondary-container: '#00a572'
  on-secondary-container: '#00311f'
  tertiary: '#ffafd3'
  on-tertiary: '#620040'
  tertiary-container: '#e364a7'
  on-tertiary-container: '#560038'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e9ddff'
  primary-fixed-dim: '#d0bcff'
  on-primary-fixed: '#23005c'
  on-primary-fixed-variant: '#5516be'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffd8e7'
  tertiary-fixed-dim: '#ffafd3'
  on-tertiary-fixed: '#3d0026'
  on-tertiary-fixed-variant: '#85145a'
  background: '#0b1326'
  on-background: '#dae2fd'
  surface-variant: '#2d3449'
typography:
  display-lg:
    fontFamily: Sora
    fontSize: 48px
    fontWeight: '700'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Sora
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Sora
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.5'
  label-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1'
    letterSpacing: 0.05em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 4px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 48px
  xxl: 80px
  container-max: 1280px
  gutter: 24px
---

## Brand & Style

This design system is built for the high-end gaming professional, prioritizing architectural clarity over the typical "gamer" noise. It departs from the saturated blue and neon tropes of the industry, moving toward a sophisticated, cinematic aesthetic that treats game development as a craft.

The visual style is **Elevated Glassmorphism**. It combines a structural, charcoal-based minimalism with ethereal, translucent layers. The emotional response is one of precision, maturity, and technical mastery. By utilizing soft shadows and razor-thin borders rather than aggressive glows, the design system allows the portfolio content—the games themselves—to remain the focal point within a premium, gallery-like framework.

## Colors

The palette is anchored in a deep "Obsidian Slate" to provide a neutral, high-contrast foundation that feels more like a professional studio than a bedroom setup. 

*   **Primary (Electric Purple):** Used for primary actions and active states. It provides a sharp, digital energy without feeling dated.
*   **Secondary (Emerald Green):** Reserved for success states, secondary highlights, or specific project categories (e.g., "Shipped Titles").
*   **Neutral/Background:** A strict hierarchy of charcoal and slate. Avoid pure blacks; use deep, desaturated grays to maintain depth and allow shadows to remain visible.
*   **Accents:** Vibrancy is delivered through subtle gradients rather than solid fills, ensuring the "pop" is sophisticated and controlled.

## Typography

This design system utilizes a dual-font strategy to balance character with utility. 

**Sora** is employed for headlines and display text. Its geometric structure and wide stance give it a futuristic, tech-forward feel that aligns with gaming culture while remaining clean. 

**Inter** is used for all body copy, metadata, and labels. It provides maximum legibility for long-form project descriptions and technical breakdowns. 

To maintain the sophisticated tone, use generous line heights for body text and tighter tracking for large headlines. Captions and small labels should often use uppercase with increased tracking for an "architectural" feel.

## Layout & Spacing

The design system follows a 12-column grid system with a focus on asymmetrical balance. 

*   **Desktop:** 12-column grid, 24px gutters, 80px side margins.
*   **Tablet:** 8-column grid, 16px gutters, 40px side margins.
*   **Mobile:** 4-column grid, 16px gutters, 20px side margins.

Spacing should be used to create clear groupings. Large `xxl` gaps should be used between major sections (e.g., between the Hero and the Project Grid) to emphasize the minimalist, "breathing" nature of the portfolio. Grouped items like project tags or metadata should use `sm` or `xs` spacing.

## Elevation & Depth

Depth is conveyed through transparency and "Backdrop Filter" blurs rather than heavy shadows.

1.  **Base Layer:** The deepest background level (Obsidian Slate).
2.  **Glass Layer:** Semi-transparent surfaces (approx. 40-60% opacity) with a high blur (20px-40px). These layers should have a 1px solid border at 10% white to define the edges.
3.  **Floating Elements:** Cards or buttons that sit atop glass layers use a very soft, large-radius shadow (Color: `rgba(0,0,0, 0.4)`, Blur: 30px) to indicate interaction.

Avoid any "glow" effects. Instead, use "inner-glow" style borders—a subtle 1px top-border that is slightly brighter than the side borders—to mimic a light source from above.

## Shapes

The shape language is "Softly Geometric." 

The design system uses a consistent `0.5rem` (8px) corner radius for most containers and cards. This provides a modern, friendly touch without veering into the "bubbly" aesthetic of casual apps. 

Interactive elements like buttons use the same 8px radius to maintain a structural look. Avoid pill-shaped buttons; the rectangular form factor feels more professional and aligned with the "Sora" typeface.

## Components

### Buttons
Primary buttons use a subtle gradient of the primary color with white text. Secondary buttons are "ghost" style: a transparent background with a 1px border and a subtle glass blur. All buttons should have a `0.2s` ease-in-out transition on hover, where the background opacity increases slightly.

### Cards (Project Tiles)
Cards are the core of the portfolio. They feature a glassmorphic background and a 1px elegant border. On hover, the image within the card should subtly scale (1.05x), and the border color should shift toward the primary accent color.

### Chips/Tags
Used for "Tech Stack" or "Roles." These should be small, with a dark slate background and high-contrast Inter labels. No borders; use a very subtle `0.5` opacity for the background.

### Input Fields
Inputs are dark-themed with a subtle glass effect. The active state is indicated by a color change in the 1px border to Emerald or Purple, with no outer glow.

### Additional Components: "The Playback Bar"
A unique component for gaming portfolios: a persistent, glassmorphic bottom bar or side widget that displays "Currently Playing" or "Global Stats," utilizing the label-sm typography for a technical, data-driven feel.