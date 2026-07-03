# ⚔ Wheel of Legends — MTG Commander Roller

A browser-based tool for randomly rolling eligible commanders for Magic: The Gathering's Commander format.

**[Live Demo →](https://your-username.github.io/wheel-of-legends)**

---

## Features

- **Colour identity picker** — all 32 archetypes by official guild/shard/wedge name (Gruul, Esper, Abzan, Yore-Tiller, Five-Colour, etc.)
- **Partner support** — rolls valid partner pairs (Tana + Tymna, etc.) alongside solo commanders, with a toggle to disable
- **Creature type filter** — searchable list of 80+ types (Dragon, Wizard, Eldrazi, Ninja, and more)
- **Price filter** — ceiling options from Under $1 to Under $50, using live Scryfall pricing
- **Roll count** — roll 1–5 commanders at once, displayed side by side
- **Pool size display** — live count of eligible commanders for the current filter combination
- **Shareable rolls** — copy a link that reproduces your exact roll for anyone to open
- **Sound design** — synthesised card-shuffle and reveal sounds via Web Audio API (toggleable)
- **Plane themes** — six atmospheric visual themes: Ravnica, Innistrad, Zendikar, Kaladesh, Theros, Eldraine — each with animated particle effects

## Data sources

Card data, images, and pricing are served live from [Scryfall's free public API](https://scryfall.com/docs/api). No API key required. Each card links through to its [EDHREC](https://edhrec.com) commander page for deck-building inspiration.

## Hosting on GitHub Pages

1. [Create a new repository](https://github.com/new) on GitHub (public, no template needed)
2. Upload `index.html` to the repository root — you can drag and drop it on the GitHub web UI
3. Go to **Settings → Pages**
4. Under **Source**, select **Deploy from a branch**
5. Choose **main** branch, **/ (root)** folder, and click **Save**
6. After a minute or two, your site will be live at `https://your-username.github.io/your-repo-name`

> **Note:** the app requires a real HTTP/HTTPS origin to make API calls to Scryfall. Opening `index.html` directly from your file system (`file://`) will be blocked by browser security. GitHub Pages handles this automatically.

## Local development

If you want to run it locally before pushing:

```bash
# Python 3
python3 -m http.server 8080
# then open http://localhost:8080
```

```bash
# Node.js (if you have npx)
npx serve .
# then open http://localhost:3000
```

## Legal

Magic: The Gathering is © Wizards of the Coast. Card images and data are provided by Scryfall under their [terms of service](https://scryfall.com/docs/terms). This is an unofficial fan tool, unaffiliated with Wizards of the Coast, Scryfall, or EDHREC. No card artwork is hosted or redistributed by this project — images are loaded directly from Scryfall's CDN at runtime.
