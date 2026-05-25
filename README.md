# basecamp · design system v0.1

Direction C — **Block / Retro**. Cool gray base, JetBrains Mono + Arial Black, indigo primary accent, magenta secondary, 2–4px radius, subtle grain.

## Files

```
basecamp/
├── index.html               ← hub / overview
├── Design System.html       ← full component library (22 sections)
├── Marketing Landing.html   ← public front door
├── App Shell.html           ← three-column notes editor
├── Dashboard.html           ← KPI tiles + activity + widget shelf
├── Design Directions.html   ← archive — original A/B/C exploration
│
├── tokens.css               ← color, type, spacing, grain, theme switching
├── components.css           ← every primitive (buttons, inputs, cards…)
│
├── tokens.json              ← Tokens Studio for Figma import
└── README.md                ← this file
```

Open `index.html` to start.

## Hosting on Netlify

1. Drag this whole folder onto [Netlify Drop](https://app.netlify.com/drop).
2. Done. You'll get a `*.netlify.app` URL.

## Bringing it into Figma

1. Install the **Tokens Studio for Figma** plugin.
2. Open the plugin → settings → **Import** → paste or upload `tokens.json`.
3. Both modes (Dark + Light) will appear as themes in the plugin, with all colors / typography / spacing / radii as Figma variables.
4. For the layouts themselves, host this folder on Netlify (above), then use the **html.to.design** Figma plugin and paste each page URL.

## Theming

Theme toggle lives in the top-right of every page. Choice persists in `localStorage` as `basecamp-theme`.

To change a token value: edit `tokens.css` (one of the `--d-*` or `--l-*` lines). Every page picks it up automatically.

## Accent rules

- `--acc` (indigo `#6A76FB`) — primary. Default highlight, active states, focus rings.
- `--acc-2` (magenta `#C839C5`) — secondary. Used sparingly: pinned items, featured tiles, "now playing" markers.
- `--success` (green `#67F86F` / `#1D7A25`) — positive deltas, "online" status, autosaved indicator.
- `--danger` (coral `#FD6F6B`) — destructive actions, errors.
- `--warn` (yellow `#FFFA71` / `#D97706`) — pending, scheduled, caution.
- `--info` (teal `#20C5C6` / `#0E8A8B`) — informational banners.

One accent per screen, ideally. The rest is neutral grays.
