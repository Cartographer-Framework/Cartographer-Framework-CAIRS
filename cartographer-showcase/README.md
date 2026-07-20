# Cartographer — Portfolio Showcase

Static portfolio site for four interactive MITRE ATLAS threat-intelligence views extracted from the Cartographer red-teaming framework.

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

## Setup — data

```
data/
  atlas_ttp.json               ← required by mitigations + severity
  atlas_mitigations.json       ← required by mitigations
  tactics_gallery_file.json    ← required by tactics
  remediation_categories.json  ← required by remediations
  severity_categories.json     ← required by severity
```

