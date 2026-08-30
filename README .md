# Ledger — Animated SaaS Landing Page Pack

Three fully-coded, animated landing page templates built for app/SaaS launches. Each one is a single self-contained HTML file — open it in a browser and it just works. No build tools, no dependencies to install, no framework required.

## What's included

| File | Style | Best for |
|---|---|---|
| `ledger-variant-a-ink-lime.html` | Dark mode, condensed bold type, acid-lime accent | Fintech, budgeting, ledger/tracking apps |
| `ledger-variant-b-paper-indigo.html` | Light mode, editorial serif headline, indigo accent | Premium/calm finance, wellness, professional tools |
| `ledger-variant-c-signal-coral.html` | Near-black, wide expanded type, coral accent, mirrored layout | Startups, launches, anything that wants to feel loud and fast |

All three share the same page structure (nav → hero with phone mockup → 3-step feature grid → footer) and the same animation engine, so you can mix content freely between them.

## What's animated

- **Headline** — lines slide up and fade in on page load, staggered
- **Live counter** — the "per month" figure counts up from $0 on load (easing curve, not linear)
- **Phone mockup** — floats gently with a slow bob
- **Expense rows** — fade in one-by-one as the user scrolls to them (using IntersectionObserver)
- **Feature cards** — fade up into view on scroll

All animations respect `prefers-reduced-motion` automatically, so the page stays accessible without any extra work from you.

## How to customize

Everything you need to change lives in two places: the `<style>` block at the top and the HTML content below it. No build step — edit and refresh.

### 1. Change the copy
Search for these sections in the HTML body and replace the text directly:
- `<h1>` — the main headline (each `<span class="line"><span>...</span></span>` is one animated line)
- `.sub` — the paragraph under the headline
- `.ledger-strip` — the three small stats (per month / per year / accounts)
- `.item-row` blocks — the four rows inside the phone mockup (icon, name, amount)
- `.feature` blocks — the 3-step "how it works" section

### 2. Change the colors
Every color is a CSS variable at the top of the `<style>` block:

```css
:root{
  --bg: #0E1210;        /* page background */
  --surface: #171C1A;    /* card/panel background */
  --ink: #F4F2EA;        /* main text color */
  --ink-dim: #9CA39D;    /* secondary text */
  --accent: #C6FF3D;     /* your brand color — buttons, highlights */
  --line: #2A302D;       /* dividers */
}
```
Change these six values and the whole page re-themes itself — buttons, rings, borders, and text all reference these variables.

### 3. Change the fonts
Each variant loads its fonts from Google Fonts in the `<head>`. Swap the `<link href="...">` URL and the `font-family` values in the CSS to use different typefaces. Current pairings:
- **Variant A:** Big Shoulders Display + Inter + IBM Plex Mono
- **Variant B:** Fraunces + Inter + IBM Plex Mono
- **Variant C:** Archivo Expanded + Inter + IBM Plex Mono

### 4. Adapt it to a different kind of app
The phone mockup is written as generic "spending dashboard" content, but the layout works for any app with a headline stat and a short list. To repurpose it:
- Swap the big number (`.totals .big`) for your app's key metric (steps, tasks done, hours saved, API calls, etc.)
- Swap the four `.item-row` entries for your own categories
- Update the `target` value in the `<script>` at the bottom to match your new headline number — this is what the counter animates toward

### 5. Change the button destination
The `.btn-primary`, `.cta-pill`, and `.btn-ghost` elements are currently plain buttons/links (`href="#"`). Point them at your app store link, waitlist form, or signup page.

## File structure
Each file is fully self-contained — HTML, CSS, and JS all in one document, with fonts loaded from Google Fonts via CDN. There's nothing else to install or configure.

## Browser support
Tested on current Chrome, Safari, and Firefox. Uses standard CSS Grid, CSS custom properties, and IntersectionObserver — all well-supported in modern browsers going back several years.

## License
[Add your license terms here before publishing — e.g. single-use commercial license, no resale/redistribution of the template files themselves, attribution not required.]

## Credits
Fonts used are all free and open-source via Google Fonts (Big Shoulders Display, Fraunces, Archivo Expanded, Inter, IBM Plex Mono).

---

Questions or customization help? [Add your contact/support link here.]
