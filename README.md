# KeyTester — Keyboard & Mouse Tester

A free, minimalist, single-file web app to test every key on any keyboard and every button on any mouse — instantly, in the browser.

**Live:** [keytester.app](https://huzaifa003.github.io/Keyboard_Tester/)) *(update with your deployed URL)*

---

## Features

- **Full keyboard layout** — all standard keys including Escape, function row, numpad, nav cluster, and arrow keys
- **Dynamic extra key discovery** — media keys, macro keys, browser keys, and any non-standard key appear automatically in an Extra Keys section the first time you press them
- **Auto layout detection** — uses the Keyboard Layout API (Chrome/Edge) to detect QWERTY US/UK, AZERTY, QWERTZ, Dvorak, and Colemak; falls back to a manual dropdown
- **Mouse testing** — left, right, middle, forward, back buttons, plus scroll wheel up/down
- **Live key display** — shows `event.key · event.code` for every keystroke
- **Browser action blocking** — prevents F5, Ctrl+R, Ctrl+F, Backspace navigation, and other shortcuts from interfering with testing
- **No dependencies** — single HTML file, vanilla JS, zero npm, zero build step

## Keyboard Support

| Layout | Region |
|--------|--------|
| QWERTY US | United States |
| QWERTY UK | United Kingdom |
| AZERTY | France |
| QWERTZ | Germany / Central Europe |
| Dvorak | Dvorak Simplified |
| Colemak | Colemak |

> **Why can't the Fn key be detected?**  
> The `Fn` key is handled directly by keyboard hardware firmware before any signal reaches the OS or browser. This is a physical limitation — no browser-based tester can capture it.

## Usage

1. Open `index.html` in any modern browser — or deploy it anywhere static hosting is available.
2. Press every key on your keyboard. Each key lights up teal when pressed and stays highlighted after release.
3. Media or macro keys appear automatically in the **Special / Extra Keys** section.
4. Click every mouse button and scroll up/down to test the wheel.
5. Use **Reset** to clear and test again.

## Deployment

This is a single static HTML file — no server, no build, no dependencies.

```bash
# GitHub Pages (simplest)
# Push to a repo, enable Pages from Settings → Pages → Deploy from branch (main / root)

# Netlify drag-and-drop
# Drag the folder onto netlify.com/drop

# Vercel
vercel deploy
```

Update the `<link rel="canonical">` and `og:url` meta tags in `index.html` with your deployed URL before publishing.

## SEO & GEO

The page includes:
- Full Open Graph and Twitter Card meta tags
- `WebApplication` schema (Schema.org)
- `FAQPage` schema — answers 7 common questions for AI answer engines (ChatGPT, Perplexity, Google SGE)
- `HowTo` schema — step-by-step usage for rich results
- Canonical URL, theme color, robots directives

## Browser Compatibility

| Browser | Keyboard testing | Layout auto-detect |
|---------|-----------------|-------------------|
| Chrome / Edge | ✅ Full | ✅ Auto |
| Firefox | ✅ Full | Manual dropdown |
| Safari | ✅ Full | Manual dropdown |

## Tech Stack

- HTML5
- CSS3 (custom properties, Grid, Flexbox)
- Vanilla JavaScript (ES2020)
- No frameworks, no dependencies, no build tools

## License

MIT — free to use, modify, and deploy.
