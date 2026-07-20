# Cartographer — Portfolio Showcase

Static portfolio site for four interactive MITRE ATLAS threat-intelligence views extracted from the Cartographer red-teaming framework. No build step. No server. Deploys to Vercel in under a minute.

---

## Pages

| File | What it shows |
|------|--------------|
| `index.html` | Showcase landing page with card previews and setup instructions |
| `tactics.html` | 16-node radial graph of MITRE ATLAS tactics |
| `remediations.html` | 5-category fault-localization atlas with expandable radial |
| `mitigations.html` | 35 ATLAS mitigations × technique cross-reference radial |
| `severity.html` | 4-band severity atlas mapped to ATLAS tactics |

---

## Setup — add your data

Each page fetches JSON from `./data/`. Drop your exports from the Cartographer platform here:

```
data/
  atlas_ttp.json               ← required by mitigations + severity
  atlas_mitigations.json       ← required by mitigations
  tactics_gallery_file.json    ← required by tactics
  remediation_categories.json  ← required by remediations
  severity_categories.json     ← required by severity
```

If a file is missing, the page shows a clear empty state — it won't error or break other pages.

---

## Deploy on Vercel

1. Fork or clone this repo
2. Push to GitHub
3. Connect the repo in Vercel → **no build command**, publish directory is `/` (root)
4. Deploy — done

Data files are served with a 5-minute cache. Update a file, redeploy, and the view refreshes automatically.

---

## Local dev

```bash
# Any static file server works — e.g. Python's built-in:
python3 -m http.server 3000
# Then open http://localhost:3000
```

> **Note:** The pages fetch `./data/*.json` via `fetch()`. Browsers block cross-origin `file://` requests, so you need a local server rather than opening the HTML files directly.
