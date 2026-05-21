# Silsilah Keluarga: Bani Raukhan – Rafi

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?logo=github)](https://your-username.github.io/bani-raukhan-rafi/)

Interactive D3.js family tree dashboard for the Bani Raukhan – Rafi family lineage. Built with a Javanese *Kraton & Sogan* aesthetic.

## Features

- 🌳 **Collapsible D3.js Tree** — Top-down hierarchical layout with smooth transitions
- 🔍 **Live Name Search** — Highlights matching members and expands their ancestor chain
- 🔭 **Zoom & Pan** — Mouse wheel / pinch-to-zoom, drag to pan the canvas
- 📱 **Mobile-First** — Responsive layout optimized for 1080×1920 portrait screens
- ✿ **Status Indicators** — Deceased (greyed + ✿ symbol) and divorced (⌇ dashed border) visual cues
- 🏅 **Founder Highlight** — Gold-framed root couple node
- 🎯 **Recenter Button** — Snap back to the founder node at any time

## Controls

| Button | Action |
|--------|--------|
| `+` / `−` | Zoom in / out |
| `🎯` | Recenter to founder |
| `⊞` | Expand all branches |
| `⊟` | Collapse all branches |
| `🔍` | Search by name |

## Deployment to GitHub Pages

1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Set source to **Deploy from branch: `main` / `root`**
4. Your site will be live at `https://<username>.github.io/<repo>/`

> **Important:** Both `index.html` and `bani_raukhan_rafi_tree_d3_visual_reparse.json` must be in the **same directory** at the repository root.

## Data Schema

```json
{
  "id": "root",
  "nama": "RAUKHAN - RAFI",
  "jenis": "founder_couple",
  "generation_from_founder": 0,
  "pasangan": [{ "nama": "RAFI" }],
  "children": [
    {
      "id": "1",
      "nomor_silsilah": "1",
      "nama": "SLAMET",
      "meninggal": true,
      "pasangan": [{ "nama": "MARSIAH", "meninggal": true, "cerai": false }],
      "children": [ ... ]
    }
  ]
}
```

## Tech Stack

- **D3.js v7** — Tree layout, zoom, transitions
- **Tailwind CSS** (CDN) — Utility layout for the shell
- **Vanilla CSS** — Custom Javanese design system
- **Google Fonts** — Cinzel (serif titles) + Plus Jakarta Sans (body text)
- No build step required — pure static HTML

## License

Family data is private. Code released under MIT.
