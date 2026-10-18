# Semantic design tokens — Enquirify

A single, framework-agnostic set of **semantic** tokens (no raw palette, no numbered
scales like `space-100` or `color-green-300`). Names describe **what** the token is
for, never **how** it looks.

Sources of inspiration:

- Atlassian Design System (`color.background.*`, `color.text.*`, `color.border.*`, `color.icon.*`) — see `token2.md`
- The existing `token.css` (raw palette + first semantic layer: `--text-default`, `--surface-*`, `--action-*`)
- shadcn/ui (`--background`, `--foreground`, `--muted-foreground`, `--primary`), Radix Themes, Open Props, GitHub Primer, IBM Carbon, Material 3, W3C Design Tokens spec

---

## Naming convention

`--<category>-<role>[-<state>]`

| Category | Meaning | Example |
|---|---|---|
| `color-fg` | text / icon colour | `color-fg-muted` |
| `color-bg` / `color-surface` | backgrounds | `color-surface-raised` |
| `color-border` | outlines & dividers | `color-border-focus` |
| `color-icon` | icon fill | `color-icon-success` |
| `color-<action>` | button/action surfaces | `color-primary`, `color-danger` |
| `font` / `text` / `weight` / `leading` / `tracking` | typography | `font-display`, `text-xl`, `weight-semibold` |
| `space` | spacing (semantic names only) | `space-md`, `space-xl` |
| `radius` | corner rounding | `radius-lg` |
| `shadow` | elevation | `shadow-raised`, `shadow-overlay` |
| `opacity` | state opacity | `opacity-disabled` |
| `duration` / `ease` | motion | `duration-fast` |

Rules

1. No raw palette tokens — `color-barberry-500`, `color-green-300` live only in a
   private, non-semantic "primitives" layer and are never used directly.
2. No numbered scales for spacing/radius — use t-shirt sizes (`xs … 4xl`).
3. Every state is a separate token (`hovered`, `pressed`, `disabled`, `focused`),
   never a modifier that changes the colour.

---

## 1. Colour — text & icons (`color-fg-*`, `color-icon-*`)

| Token | Purpose | Light value | Dark value |
|---|---|---|---|
| `color-fg` | Default text / primary icon | zinc-950 | white |
| `color-fg-muted` | Secondary body text | zinc-600 | zinc-300 |
| `color-fg-subtle` | Tertiary, captions, meta | zinc-500 | zinc-400 |
| `color-fg-disabled` | Disabled text | zinc-400 | zinc-600 |
| `color-fg-placeholder` | Input placeholders | zinc-400 | zinc-500 |
| `color-fg-inverse` | Text on inverted / bold surfaces | white | zinc-950 |
| `color-fg-link` | Links | blue-700 | blue-300 |
| `color-fg-brand` | Brand accent text | barberry-700 | barberry-300 |
| `color-fg-success` | Success text | green-700 | green-300 |
| `color-fg-warning` | Warning text | barberry-800 | barberry-200 |
| `color-fg-danger` | Error / destructive text | red-700 | red-300 |
| `color-fg-info` | Informational text | blue-700 | blue-300 |

| Token | Purpose | Light | Dark |
|---|---|---|---|
| `color-icon` | Default icon | zinc-900 | zinc-100 |
| `color-icon-muted` | Muted icon | zinc-500 | zinc-400 |
| `color-icon-inverse` | Icon on brand/dark surface | white | zinc-950 |
| `color-icon-brand` | Brand icon | barberry-600 | barberry-300 |
| `color-icon-success` | Success icon | green-600 | green-300 |
| `color-icon-warning` | Warning icon | barberry-600 | barberry-300 |
| `color-icon-danger` | Danger icon | red-600 | red-300 |
| `color-icon-info` | Info icon | blue-600 | blue-300 |

> Example utility: `text-fg-muted`, `text-fg-danger`, `text-fg-inverse`.

## 2. Colour — backgrounds & surfaces (`color-bg-*`, `color-surface-*`)

| Token | Purpose | Light | Dark |
|---|---|---|---|
| `color-bg` | Page canvas | zinc-50 | zinc-950 |
| `color-surface` | Card / panel | white | zinc-900 |
| `color-surface-raised` | Elevated card, dropdowns | white | zinc-800 |
| `color-surface-overlay` | Modal / popover | white | zinc-800 |
| `color-surface-subtle` | Muted inset, code blocks | zinc-100 | zinc-800 |
| `color-surface-inverse` | Inverse band (dark footer/CTA) | zinc-900 | white |
| `color-surface-hovered` | Row/card hover | zinc-100 | zinc-800 |
| `color-surface-pressed` | Row/card pressed | zinc-200 | zinc-700 |
| `color-surface-selected` | Selected item | barberry-50 | barberry-950 |
| `color-surface-disabled` | Disabled control fill | zinc-100 | zinc-800 |

Status backgrounds (subtle, non-bold variant):

| Token | Light | Dark |
|---|---|---|
| `color-bg-success` | green-100 | green-950 |
| `color-bg-warning` | barberry-100 | barberry-950 |
| `color-bg-danger` | red-100 | red-950 |
| `color-bg-info` | blue-100 | blue-950 |

> Example utility: `bg-surface`, `bg-surface-subtle`, `bg-bg-success`.

## 3. Colour — borders (`color-border-*`)

| Token | Purpose | Light | Dark |
|---|---|---|---|
| `color-border` | Default border | zinc-950 @ 20% | zinc-50 @ 25% |
| `color-border-subtle` | Dividers, card edges | zinc-950 @ 7% | zinc-50 @ 12% |
| `color-border-strong` | Emphasis border | zinc-950 @ 40% | zinc-50 @ 40% |
| `color-border-focus` | Focus ring | barberry-700 | barberry-300 |
| `color-border-input` | Form control | zinc-950 @ 20% | zinc-50 @ 25% |
| `color-border-disabled` | Disabled control | zinc-950 @ 8% | zinc-50 @ 10% |
| `color-border-brand` | Brand outline | barberry-600 | barberry-300 |
| `color-border-success` | Success outline | green-500 | green-400 |
| `color-border-warning` | Warning outline | barberry-500 | barberry-400 |
| `color-border-danger` | Error outline | red-500 | red-400 |
| `color-border-info` | Info outline | blue-500 | blue-400 |

## 4. Colour — actions (`color-*` button roles)

| Token | Purpose | Light / Dark |
|---|---|---|
| `color-primary` | Primary button bg | barberry-500 (both) |
| `color-primary-hovered` | Primary hover | barberry-600 |
| `color-primary-pressed` | Primary pressed | barberry-700 |
| `color-primary-foreground` | Text on primary | barberry-950 |
| `color-secondary` | Secondary button bg | zinc-50 / zinc-900 |
| `color-secondary-hovered` | Secondary hover | zinc-100 / zinc-800 |
| `color-secondary-pressed` | Secondary pressed | zinc-200 / zinc-950 |
| `color-secondary-foreground` | Text on secondary | zinc-950 / white |
| `color-secondary-border` | Secondary outline | zinc-200 / zinc-700 |
| `color-destructive` | Destructive button bg | red-600 |
| `color-destructive-hovered` | Destructive hover | red-700 |
| `color-destructive-pressed` | Destructive pressed | red-800 |
| `color-destructive-foreground` | Text on destructive | white |
| `color-link` | Link button text | blue-700 / blue-300 |

> Example utility: `bg-primary text-primary-foreground hover:bg-primary-hovered`.

## 5. Spacing (`space-*`) — semantic names only

| Token | px |
|---|---|
| `space-2xs` | 4 |
| `space-xs` | 8 |
| `space-sm` | 12 |
| `space-md` | 16 |
| `space-lg` | 24 |
| `space-xl` | 32 |
| `space-2xl` | 40 |
| `space-3xl` | 48 |
| `space-4xl` | 64 |
| `space-5xl` | 80 |

## 6. Typography

| Group | Token | Value |
|---|---|---|
| Font family | `font-sans` | Inter |
| | `font-display` | Inter |
| | `font-mono` | ui-monospace |
| Font size | `text-xs` … `text-6xl` | 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 48 / 60 / 72 |
| Font weight | `weight-regular` / `weight-medium` / `weight-semibold` / `weight-bold` | 400 / 500 / 600 / 700 |
| Line height | `leading-tight` / `leading-snug` / `leading-normal` / `leading-relaxed` | 1.1 / 1.25 / 1.5 / 1.7 |
| Letter spacing | `tracking-tight` / `tracking-normal` / `tracking-wide` | -0.025em / 0 / 0.05em |

> Text roles can also be a semantic pair: `text-body` (16/1.5), `text-body-sm` (14/1.5), `text-caption` (12/1.4), `text-label` (14/1.5 medium), `text-display-*` for hero headings.

## 7. Radius (`radius-*`)

`radius-none` 0 · `radius-xs` 6 · `radius-sm` 8 · `radius-md` 12 · `radius-lg` 16 · `radius-xl` 24 · `radius-full` 9999

## 8. Elevation (`shadow-*`)

`shadow-xs` · `shadow-sm` · `shadow-md` · `shadow-raised` (cards) · `shadow-overlay` (modals/popovers) · `shadow-overflow` (scroll edges)

## 9. Opacity & motion

| Token | Value |
|---|---|
| `opacity-disabled` | 0.4 |
| `opacity-loading` | 0.6 |
| `duration-fast` | 150ms |
| `duration-base` | 200ms |
| `duration-slow` | 300ms |
| `ease-standard` | cubic-bezier(0.2, 0, 0, 1) |

---

## Tailwind v4 integration (the only mapping you need)

Because every colour token above is named `color-*`, Tailwind auto-generates the
utilities — no extra config required:

```css
@theme {
  /* semantic colours → text-*, bg-*, border-*, etc. */
  --color-fg: var(--color-zinc-950);
  --color-fg-muted: var(--color-zinc-600);
  --color-bg: var(--color-zinc-50);
  --color-surface: var(--color-white);
  --color-border: color-mix(in oklab, var(--color-zinc-950) 20%, transparent);
  --color-primary: var(--color-barberry-500);
  --color-primary-foreground: var(--color-barberry-950);
  /* … etc. */
}
```

Dark mode keeps the same utility classes; only the variable values change:

```css
.dark {
  --color-fg: var(--color-white);
  --color-bg: var(--color-zinc-950);
  --color-surface: var(--color-zinc-900);
  /* … */
}
```

Usage:

```html
<body class="bg-bg text-fg">
  <h1 class="text-fg">Headline</h1>
  <p class="text-fg-muted">Secondary copy</p>
  <div class="border-border bg-surface">Card</div>
  <button class="bg-primary text-primary-foreground">Book a demo</button>
</body>
```
