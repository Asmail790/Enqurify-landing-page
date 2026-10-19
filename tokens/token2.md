# Atlassian Design System - Semantic Tokens Reference

This document categorizes and lists Atlassian's semantic design tokens across colors (background, text, border, icon), spacing, typography, opacity, and elevation.

---

## 1. Color Tokens

### A. Surface & Background (`color.background.*`)

#### Standard Backgrounds
* `color.background.default` (Base canvas background)
* `color.background.default.hovered`
* `color.background.default.pressed`
* `color.background.neutral`
* `color.background.neutral.hovered`
* `color.background.neutral.pressed`
* `color.background.neutral.subtle`
* `color.background.neutral.subtle.hovered`
* `color.background.neutral.subtle.pressed`
* `color.background.neutral.bold`
* `color.background.neutral.bold.hovered`
* `color.background.neutral.bold.pressed`

#### Elevated & Layered Surfaces
* `color.background.elevation.surface`
* `color.background.elevation.surface.hovered`
* `color.background.elevation.surface.pressed`
* `color.background.elevation.surface.overlay`
* `color.background.elevation.surface.raised`
* `color.background.elevation.surface.sunken`

#### Feedback & State Backgrounds
* **Brand / Selected:**
  * `color.background.selected`
  * `color.background.selected.hovered`
  * `color.background.selected.pressed`
  * `color.background.selected.bold`
  * `color.background.selected.bold.hovered`
  * `color.background.selected.bold.pressed`
* **Information:**
  * `color.background.information`
  * `color.background.information.hovered`
  * `color.background.information.pressed`
  * `color.background.information.bold`
  * `color.background.information.bold.hovered`
  * `color.background.information.bold.pressed`
* **Success:**
  * `color.background.success`
  * `color.background.success.hovered`
  * `color.background.success.pressed`
  * `color.background.success.bold`
  * `color.background.success.bold.hovered`
  * `color.background.success.bold.pressed`
* **Warning:**
  * `color.background.warning`
  * `color.background.warning.hovered`
  * `color.background.warning.pressed`
  * `color.background.warning.bold`
  * `color.background.warning.bold.hovered`
  * `color.background.warning.bold.pressed`
* **Danger / Error:**
  * `color.background.danger`
  * `color.background.danger.hovered`
  * `color.background.danger.pressed`
  * `color.background.danger.bold`
  * `color.background.danger.bold.hovered`
  * `color.background.danger.bold.pressed`
* **Discovery / Accent:**
  * `color.background.discovery`
  * `color.background.discovery.bold`
  * `color.background.disabled`

#### Accent Color Swatches (Categorized by `.subtlest`, `.subtler`, `.subtle`, `.bolder` + hover/pressed)
* `color.background.accent.lime.*`
* `color.background.accent.red.*`
* `color.background.accent.orange.*`
* `color.background.accent.yellow.*`
* `color.background.accent.green.*`
* `color.background.accent.teal.*`
* `color.background.accent.blue.*`
* `color.background.accent.purple.*`
* `color.background.accent.magenta.*`
* `color.background.accent.gray.*`

---

### B. Text Tokens (`color.text.*`)

* `color.text` (Primary default text color)
* `color.text.subtle` (Secondary body/meta text)
* `color.text.subtlest` (Tertiary/placeholder text)
* `color.text.disabled` (Disabled state text)
* `color.text.inverse` (Text on bold colored backgrounds)
* `color.text.brand`
* `color.text.selected`
* `color.text.information`
* `color.text.success`
* `color.text.warning`
* `color.text.warning.inverse`
* `color.text.danger`
* `color.text.discovery`

#### Text Accent Tokens
* `color.text.accent.lime` / `.bolder`
* `color.text.accent.red` / `.bolder`
* `color.text.accent.orange` / `.bolder`
* `color.text.accent.yellow` / `.bolder`
* `color.text.accent.green` / `.bolder`
* `color.text.accent.teal` / `.bolder`
* `color.text.accent.blue` / `.bolder`
* `color.text.accent.purple` / `.bolder`
* `color.text.accent.magenta` / `.bolder`
* `color.text.accent.gray` / `.bolder`

---

### C. Border Tokens (`color.border.*`)

* `color.border` (Default subtle borders)
* `color.border.neutral`
* `color.border.focused` (Focus rings & input outlines)
* `color.border.input` (Form field controls)
* `color.border.disabled`
* `color.border.brand`
* `color.border.selected`
* `color.border.information`
* `color.border.success`
* `color.border.warning`
* `color.border.danger`
* `color.border.discovery`

---

### D. Icon Tokens (`color.icon.*`)

* `color.icon` (Default icon fill)
* `color.icon.subtle`
* `color.icon.disabled`
* `color.icon.inverse`
* `color.icon.brand`
* `color.icon.selected`
* `color.icon.information`
* `color.icon.success`
* `color.icon.warning`
* `color.icon.danger`
* `color.icon.discovery`

---

## 2. Spacing & Layout Tokens (`space.*`)

* `space.0` (0px)
* `space.025` (2px)
* `space.050` (4px)
* `space.075` (6px)
* `space.100` (8px - Base unit)
* `space.150` (12px)
* `space.200` (16px)
* `space.250` (20px)
* `space.300` (24px)
* `space.400` (32px)
* `space.500` (40px)
* `space.600` (48px)
* `space.800` (64px)
* `space.1000` (80px)

---

## 3. Typography Tokens (`font.*`)

### Font Families
* `font.family.body`
* `font.family.heading`
* `font.family.code`

### Font Sizes & Line Heights
* `font.heading.xxlarge`
* `font.heading.xlarge`
* `font.heading.large`
* `font.heading.medium`
* `font.heading.small`
* `font.heading.xsmall`
* `font.body.large`
* `font.body.medium` (Default)
* `font.body.small`
* `font.code.medium`

### Font Weights
* `font.weight.regular`
* `font.weight.medium`
* `font.weight.semibold`
* `font.weight.bold`

---

## 4. Elevation & Shadows (`elevation.*`)

* `elevation.shadow.raised` (Cards, subtle floating containers)
* `elevation.shadow.overflow` (Scroll containers with shadow indicators)
* `elevation.shadow.overlay` (Modals, popovers, dropdowns)
* `elevation.surface.current`

---

## 5. Border Widths & Radii (`border.*`)

* `border.width` (1px)
* `border.width.selected` (2px)
* `border.width.focused` (2px)
* `border.radius.050` (2px)
* `border.radius.100` (4px)
* `border.radius.200` (8px)
* `border.radius.300` (12px)
* `border.radius.circle` (9999px)

---

## 6. Opacity Tokens (`opacity.*`)

* `opacity.disabled` (0.4)
* `opacity.loading` (0.6)