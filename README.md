# UNK Travel — Best Lakes of Kyrgyzstan

A single-page travel landing for a private 7-day tour across Kyrgyzstan's highland lakes. Built as a zero-dependency HTML file — no build step, no framework.

## Live demo

Open `index.html` in any modern browser, or serve locally:

```bash
npx serve .
# → http://localhost:3000
```

## What's inside

**Sections**

| Section | Description |
|---|---|
| Hero | Full-viewport mountain backdrop with GSAP entrance sequence |
| Route | Interactive split-screen — 7 clickable day stops with crossfade image preview |
| Program | 7-day itinerary cards with alternating image / text layout |
| Highlights | 4 experience cards with custom SVG stroke icons |
| Lake | Parallax section on Issyk-Kul with key stats |
| Included | What's in the tour price |
| CTA | Booking call-to-action |

**Features**

- GSAP 3 + ScrollTrigger scroll-reveal animations
- `document.hidden` guard — animations skip in background tabs so the page never freezes
- EN / RU language toggle (zero reload, pure JS)
- Responsive down to 375 px
- Cormorant-free — uses Playfair Display + Lato for legibility at all sizes
- No npm, no bundler — single `.html` file, ships as-is

## Tech

| Thing | Detail |
|---|---|
| Animations | [GSAP 3.12.5](https://gsap.com) via CDN |
| Fonts | [Playfair Display + Lato](https://fonts.google.com) via Google Fonts |
| Images | [Unsplash](https://unsplash.com) — free-to-use, linked directly |
| Icons | Inline SVG, hand-drawn stroke style |

## Structure

```
index.html   ← everything: markup, CSS, JS in one file (~1 000 lines)
```

Keeping it in one file is intentional — the page is a standalone deliverable, not a component library.

## Customisation

All design tokens live in `:root` at the top of the `<style>` block:

```css
:root {
  --bg:    #FDFAF6;   /* cream background */
  --rust:  #C14428;   /* primary accent */
  --amber: #E8923A;   /* highlight / CTA */
  --hero:  #0D0806;   /* dark hero background */
  --text:  #1E1410;
  --text2: #6B5344;
}
```

Images map 1-to-1 with days — swap any `src` attribute in the `.rv-img` list or `.day-img` sections.

## License

MIT
