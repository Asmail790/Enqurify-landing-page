# Enquirify landing page — change log

Every instruction given for this page, in the order it was given, with what was changed as a result.

---

## 1. Add a dark/light mode toggle at the top

- Added a round icon button in the header (moon in light mode, sun in dark mode) with `aria-pressed` and a dynamic label.
- Added `@custom-variant dark` to `input.css` for class-based dark mode plus dark overrides for `.surface`, `.dot-grid`, `.step-line`, `.step-circle` and the wave divider.
- Added `dark:` variants across nav, hero, product mockups, features, waves and footer.
- Theme is applied before first paint via an inline script, saved in `localStorage`, and follows `prefers-color-scheme` until the visitor chooses explicitly.
- Fixed the footer wordmark readability in dark mode by placing it on a white pill.

## 2. Rewrite the hero title and description so the service is clear immediately

- Replaced "Never let a customer slip through your fingers. Ever again."
- New headline: "AI that answers every call, chat and enquiry. 24/7." with the gradient + squiggle underline kept on "24/7.".
- New description explaining B2B AI support: answers phone calls, website chats and forms, qualifies customers, books the order, no extra support staff, open around the clock.
- Rewrote the eyebrow and the benefit checklist (calls/chats/forms covered, no extra support staff, always open).
- Updated `<title>` and meta description to match.

## 3. Remove the duplicated logo at the bottom-left of the footer

- Removed the footer brand column (logo image + wordmark + tagline).
- Changed footer grid from 4 columns to 3 (Product / Company / Legal).
- Kept the single large centred footer logo.

## 4. Add a pricing section with clear, upfront pricing; make the Pricing menu item work

- New `#pricing` section: "Simple pricing, no surprises".
- Three plans with prices shown immediately: Starter £79/mo, Growth £199/mo (Most popular), Scale £399/mo.
- Each card lists features and "Billed monthly. Cancel any time."
- Footnote: prices exclude VAT, free consultation and installation.
- Removed the disabled "N/A" state from Pricing in the desktop and mobile nav; footer Pricing also links to `#pricing`.
- Added smooth scrolling and `scroll-mt` offsets for anchored sections.

## 5. Add an integrations section

- New `#integrations`: "Works with the tools you already use".
- Eight integration cards: Google Calendar, Microsoft 365, Shopify, Square, Stripe, HubSpot, Slack, Zapier (brand icons, short role text).
- Closing note about Xero, QuickBooks, WooCommerce and custom systems, with a link to contact.
- Footer "Integrations" link now points to `#integrations`.

## 6. Add a section with satisfied customer reviews

- New `#reviews`: "Businesses that never miss a customer".
- Rating badge: 4.9/5 from 120+ businesses.
- Six review cards with 5 stars, quote, initials avatar, name, role/company and city.
- Reused the `.surface` card style and dark-mode colours.

## 7. Add a section after the reviews quantitatively explaining cost reduction

- New `#savings` section contrasting hiring reception staff with Enquirify.
- Included a monthly cost comparison card (£1,700 receptionist, £450 overtime/callbacks, £199 Enquirify Growth) and a "~£1,950 saved per month / £23,400 a year" callout.

## 8. Replace the detailed cost numbers with larger headline claims

- Removed the comparison card and £-figures.
- Four stat tiles instead: **30%** lower support costs, **20%** more enquiries handled, **3×** faster first reply, **0** missed calls.
- Added footnote: average results reported by customers in their first six months.

## 9. Remove the "Get Started" button from the header menu

- Removed it from the desktop nav and the mobile menu (the hero already had one).

## 10. Turn the "FEATURES" section into an add-ons style section without repeating Forms/Voice

- Replaced the two Forms/Voice cards with an **ADD-ONS** section: "The extras that finish the job".
- Six cards: Priority scoring, Smart follow-ups, Auto-booking, Payments in the chat, Human handover, Multi-site routing.
- Retained the handsets information as a bottom strip at the time.

## 11. Move "No setup hassle" and the checklist into OUR PLATFORM

- Removed the shield line and the checklist from the hero.
- Placed the four items under the OUR PLATFORM intro (No setup hassle, Calls/chats/forms covered, No extra support staff, Always open).
- Widened that header to `max-w-3xl`.

## 12. Connect "See how it works" to the How it works section

- Added `id="how-it-works"` and `scroll-mt-20` to the section.
- Hero button now targets `#how-it-works`.

## 13. Add a "Book a demo" button at the top and a "Get started" button at the bottom

- Added Book a demo to the desktop nav and mobile menu.
- Added a centred Get started button in the footer.

## 14. Undo the changes (two-column demo layout)

- Reverted the ENQUIRIFY VOICE order swap and the micro-demo two-column restructure.

## 15. Remove "Get started" at the bottom

- Deleted the footer Get started button.

## 16. Link Get started to pricing; add Book a demo between Get started and See how it works

- Hero buttons became: Get started → `#pricing`, Book a demo → `#contact`, See how it works → `#how-it-works`.

## 17. Make the top Book a demo open email like the bottom one

- Hero, desktop nav and mobile menu Book a demo buttons all used `mailto:hello@enquirify.com`.

## 18. Remove the Book a demo button in the header

- Removed from the desktop nav and the mobile menu.

## 19. Add an FAQ section before the footer

- New `#faq`: "Questions, answered".
- Six native `<details>` accordions with a rotating +/× icon: go-live time, hardware, AI disclosure, fallback handling, integrations, contracts/fees.
- Added CSS to hide the default disclosure marker.

## 20. Move the FAQ before the Book a demo section

- Order became: Pricing → FAQ → wave → CTA (Book a demo) → footer.

## 21. Turn the Book a demo section into a form (email + phone), keeping the button

- Added email and phone inputs with required validation, hidden labels and dark/indigo styling.
- Kept the "Book a demo" submit button.
- On valid submit, the form is replaced by a confirmation message; no-JS fallback posts via `mailto:`.

## 22. Change the FAQ footer line to include a second contact link

- Now reads: "Still have a question? **Book a demo** or **ask us directly.**"
- "ask us directly." links to `mailto:questions@enquirify.com`.

## 23. Make the FAQ "Book a demo" link point to the Book a demo section

- Changed from `mailto:hello@enquirify.com` to `#contact`.

## 24. Rename "ADD-ONS" to "Smart features" and remove the handsets card

- New eyebrow `SMART FEATURES`, heading "Smart features that take work off your plate", rewritten intro about streamlining support.
- Card titles rewritten: Auto-prioritised enquiries, Follow-ups on autopilot, Bookings that fill themselves, Payments in the chat, Human handover when it matters, One inbox, every site.
- Removed the "Optional handsets, free installation" strip entirely.
- Section id changed to `#smart-features`.

## 25. Add a testable mini demo under the 1-2-3 steps in How it works

- Tabbed widget (one panel visible at a time) with Voice and Forms demos.
- Voice: "Start the call" plays a scripted conversation with a call timer, ending in "Call ended" and "Call again".
- Forms: typing a message shows a bubble, a typing indicator, then a keyword-matched reply.
- Noted in the UI that these are scripted samples and no data is stored.

## 26. Rewrite the micro demo intro and add two buttons beneath it

- Eyebrow changed to "TRY A MICRO DEMO OF ENQUIRIFY".
- Heading "See the agent answer for itself" with copy explaining what the Voice and Forms demos do.
- Added **Book a demo** (`#contact`) and **Get started** (`#pricing`) buttons under the demo.
- Added an idle hint in the voice panel; fixed a malformed script line introduced during the edit.

## 27. Undo the changes (micro demo layout)

- Reverted to the stacked layout: title → tabs → panel → buttons.

## 28. Make the top Book a demo go to the Book a demo section

- Hero Book a demo changed from `mailto:` to `#contact`.

## 29. Two-column micro demo: text right, demo (with buttons) on the other side

- Implemented as: demo + buttons on the left, title/description on the right, text first on mobile.

## 30. Undo

- Reverted to the previous stacked demo layout.

## 31. Make "No setup hassle" use a check icon and lay the four items out 2×2

- Replaced the shield icon with an indigo check.
- Changed the row to a two-column grid.

## 32. Remove the "Live now" and "AI powered" boxes; change the hero title

- Removed both floating badges from the hero card.
- New headline: "AI powered customer support that answers every call, chat and enquiry 24/7."
- Adjusted heading sizes/`text-balance` so it settles on four lines at desktop.

## 33. Make the hero title span the whole page

- Moved the eyebrow + H1 into a full-width block above the two-column hero area.
- Paragraph and buttons stayed left, carousel card on the right.

## 34. Voice block: card right / text left; micro demo: text to the left

- Swapped the voice card and text order for consistency with the Forms block.
- Turned the micro demo into a two-column layout.

## 35. Undo

- Reverted both layout changes.

## 36. Remove the red/yellow/green dots in ENQUIRIFY FORMS and add an icon like the Voice card

- Removed the window dots.
- Forms card header now matches the Voice card pattern: icon + "Live chat / Customer dashboard" + green "Online" chip.

## 37. Put the four intro items back in a single row

- Restored the centred flex row for No setup hassle / Calls, chats and forms covered / No extra support staff / Always open.

## 38. Add a button in the top section that jumps to customer reviews

- Added a **★ Reviews** button linking to `#reviews`.
- Tightened hero button padding/gap so all four buttons fit on one line.

## 39. Turn the hero right card into an auto-switching carousel

- Two slides: Enquirify Voice (call mock) and Enquirify Forms (chat mock).
- Crossfade every 5 seconds, two dot controls, pause on hover/focus, respects `prefers-reduced-motion`, accessible slide labels.

## 40. Make the carousel dot buttons larger and easier to click

- Dots grew from 10px to 16px.
- Added a transparent pseudo-element to expand the hit area to roughly 36px.

## 41. Link every section in the top menu, in page order; make Login a separate button

- Desktop nav links: Our platform, Smart features, How it works, Reviews, The numbers, Integrations, Pricing, FAQ, Book a demo.
- Login became an outlined button on the right, next to the theme toggle.
- Mobile panel mirrors the links and adds a full-width Login button.
- Breakpoint for collapsing the menu moved to `xl` so the longer nav never overflows.

## 42. Make every menu label match its section title

- Menu labels now mirror the section eyebrows: Our platform, Smart features, How it works, Reviews, The numbers, Integrations, Pricing, FAQ, and Book a demo for the CTA section.

---

## Final page structure (top to bottom)

1. **Header** — logo, section links, Login button, theme toggle, mobile menu.
2. **Hero** — full-width headline, description, Get started / Book a demo / See how it works / Reviews buttons, auto-rotating Voice + Forms carousel.
3. **Our platform** (`#products`) — intro with four check items, Enquirify Forms block, Enquirify Voice block.
4. **Smart features** (`#smart-features`) — six automation cards.
5. **How it works** (`#how-it-works`) — three steps plus the Voice/Forms micro demo and CTAs.
6. **Reviews** (`#reviews`) — rating summary and six testimonials.
7. **The numbers** (`#savings`) — 30% / 20% / 3× / 0 stat tiles.
8. **Integrations** (`#integrations`) — eight tools plus a custom-integration note.
9. **Pricing** (`#pricing`) — Starter / Growth / Scale.
10. **FAQ** (`#faq`) — six accordion items.
11. **Book a demo** (`#contact`) — indigo band with email + phone form.
12. **Footer** — Product / Company / Legal links, small logo, copyright.
