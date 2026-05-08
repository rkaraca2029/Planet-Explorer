# Space Explorer 🚀

An interactive, browser-based space exploration game where you pilot a spacecraft through a procedurally generated galaxy, discovering unique planets and uncovering their secrets.

## Demo

Open `index.html` in any modern browser — no installation or build step required.

## Features

- **15 procedurally generated planets** across 9 world types: rocky, ocean, desert, ice, jungle, gas giant, volcanic, crystal, and toxic
- **AI-powered discovery logs** — each planet you land on generates a unique explorer's journal entry via the Claude API
- **Fuel system** — your ship's fuel drains with distance and recharges slowly between jumps; scattered fuel cache planets give a +40 boost
- **Ship Log** — tracks every planet you've visited with its type and lore, accessible anytime mid-exploration
- **Atmospheric visuals** — twinkling stars, soft nebula clouds, planetary rings, orbiting moons, and atmospheric halos
- **Touch support** — fully playable on mobile and tablet

## How to Play

1. Open `index.html` in your browser
2. Click any planet to fly your ship there
3. On arrival, an AI-generated explorer's log is written for that planet
4. Manage your fuel — the dashed circle shows your current travel range
5. Open **Ship Log** (top right) to review past discoveries
6. Discover all 15 planets to complete your galactic survey

## Tech Stack

- **Vanilla HTML/CSS/JS** — zero dependencies, no build tools
- **HTML5 Canvas** — all game rendering (stars, planets, ship, animations)
- **Claude API** (`claude-sonnet-4-20250514`) — generates planet lore on first visit

## Project Structure

```
space-explorer/
└── index.html    # Everything lives here — game engine, UI, and API calls
```

## API Key

The game calls the Anthropic API directly from the browser. This is handled automatically when running via [Claude.ai](https://claude.ai) artifacts. If you want to self-host:

1. Sign up at [console.anthropic.com](https://console.anthropic.com)
2. Add your API key to the fetch headers in `index.html`:
   ```js
   headers: {
     'Content-Type': 'application/json',
     'x-api-key': 'YOUR_KEY_HERE',
     'anthropic-version': '2023-06-01'
   }
   ```
   > ⚠️ For production use, route API calls through a backend to keep your key secure.

## License

MIT — feel free to fork, remix, and explore.
