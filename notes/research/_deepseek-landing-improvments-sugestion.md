# Enquirify Landing Page — UX Review

A focused review of the recreated Enquirify landing page: what works well and what can be improved.

---

## What's great

- **Strong, benefit-led hero** — "Never let a customer slip through your fingers. Ever again." passes the 5-second test: it states the transformation, not the product.
- **Consistent single CTA** — "Get started" / "Book a demo" repeats throughout, guiding toward one conversion path.
- **Product-first demos** — the animated mock cards (Forms chat + Voice call) show the product working instead of just describing it. This is the most persuasive part of the page.
- **Clear scannable structure** — eyebrow labels ("OUR PLATFORM", "FEATURES", "HOW IT WORKS") create a predictable rhythm, and the 3-step process section is easy to digest.
- **Trust microcopy** — "No setup hassle", "Live now", "Free consultation and installation included" all reduce perceived risk near CTAs.

---

## What can be improved

### 1. Missing social proof (biggest gap)

There are no testimonials, metrics, or client logos anywhere. Social proof is the #1 trust builder.

- Add 2–3 customer quotes with a name, role, and a concrete result (e.g. "We stopped missing after-hours bookings — £2k/month extra").
- Add a metrics strip: "X enquiries answered · Y calls handled · Z% more orders".

### 2. "Login" in the nav is a conversion leak

It sits next to "Get Started" but points nowhere meaningful on a landing page. For a conversion-focused page, either remove it or move it to the far edge and de-emphasize it (ghost link). The nav should have **zero distractions** from the primary CTA.

### 3. Mobile nav lacks persistent access

The hamburger only appears on small screens, which is fine, but there's no way back to a CTA while scrolled deep on mobile. Add a sticky bottom CTA bar on mobile, or keep the header CTA visible.

### 4. No form / friction in the conversion step

"Book a demo" is a `mailto:` link — that's a jarring, slow conversion path. A 2-field form (name + email) with "No credit card required" microcopy converts much better, or link to a scheduling page. At minimum, add a clearer expectation: "Book a free 15-min demo".

### 5. Accessibility details

- The floating "AI powered" / "Live now" badges overlap content on narrow screens — fine, but give decorative icons proper `aria-hidden` (already partly done).
- The squiggle underline animation relies on `stroke-dashoffset`; ensure the hero headline text still reads without it.
- Consider `prefers-reduced-motion` (already supported).

### 6. Performance

- The two logo PNGs are large (~120 KB and ~98 KB). Convert to SVG or compress; logos are above the fold.
- Font Awesome loads the full icon set — consider a subset or inline SVGs for the ~15 icons used.
- Google Fonts loads 6 weights; only ~4 are used.

### 7. Footer long-logo is redundant

A huge 110px logo in the footer adds visual noise without value. Keep the compact logo and copyright only.

### 8. Micro-interactions could guide the eye more

The animated cards are great; the buttons could use a subtle press effect, and the "Get started" hero button could pulse gently once on load to draw attention.

---

## Quick wins (highest impact, least effort)

1. Add a social-proof strip right below the hero.
2. Replace `mailto:` with a small inline form (or at least reword the CTA).
3. Add a mobile sticky CTA bar.
4. Compress/swap the logo assets to SVG.

**Recommended starting point:** #1 (social proof) and #2 (real conversion form) — these have the biggest effect on conversion rate.
