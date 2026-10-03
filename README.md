# `doc-html` — Modern Interactive HTML Documentation Skill

[![GitHub Release](https://img.shields.io/github/v/release/ghasemdev/html-doc-skill?color=38bdf8&label=Release)](https://github.com/ghasemdev/html-doc-skill/releases)
[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-34d399?logo=github)](https://ghasemdev.github.io/html-doc-skill/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

An agentic AI skill for generating **responsive, single-file, interactive HTML technical documentation, API specifications, and architecture whitepapers**.

🌐 **Live Demo:** [https://ghasemdev.github.io/html-doc-skill/](https://ghasemdev.github.io/html-doc-skill/)  
📜 **Release Notes:** See [CHANGELOG.md](CHANGELOG.md) for detailed version history.

---

## ⚡ Core Capabilities

- 📑 **ChatGPT/Acrobat-Style Catalog Sidebar:** Persistent desktop rail and smooth mobile off-canvas drawer with reading progress indicator.
- 🔤 **Strictly Left-to-Right (LTR) Code Blocks:** All `<pre>`, `<code>`, and JSON snippets stay LTR in both RTL (Persian) and LTR (English) modes.
- 📡 **Standardized API Tables:** Structured endpoints with HTTP badges (`POST`, `GET`), parameter tables, JSON schemas, and error code tables.
- 📍 **Coordinate Drag & Drop Commenting:** Drag and drop comment pins at $(x, y)$ coordinates across sections with a slide-out review drawer.
- 📥 **Export to AI & Embedded HTML:** Download reviewer comments as structured JSON for AI iteration, or embed directly into downloadable HTML.
- 🔀 **Real Version Navigation:** Seamless routing between documentation versions (`v2.0.0`, `v1.2.0`, `v1.0.0`) with archived banners.
- 🌓 **Dual-Theme Engine (Dark/Light):** Fluid CSS variable transitions persistent in `localStorage`.
- 🌐 **Zero-Reload Bilingual Engine:** Instant English/Persian switching adhering to `persian-writing` typography (Vazirmatn, ZWNJ, no Fingilish).
- 📱 **Mobile First & No Horizontal Overflow:** Clean compact mobile toolbar, touch targets (≥44px), and responsive tables.
- 🎯 **Context-Aware Modularity:** Intelligent component inclusion — no forced or irrelevant APIs, diagrams, or simulators.

---

## 📂 Repository Structure

```
html-doc-skill/
├── SKILL.md                          # Authoritative AI agent skill instructions
├── README.md                         # Quick reference & documentation
├── CHANGELOG.md                      # Complete version changelog history
├── index.html                        # GitHub Pages root entrypoint (v2.0.0)
├── resources/
│   └── starter-template.html         # Clean boilerplate starter template
└── examples/
    ├── remote-compose-architecture-and-usecases.html # Full showcase (v2.0.0)
    ├── v2.0.0/remote-compose.html    # Version 2.0.0 release
    ├── v1.2.0/remote-compose.html    # Version 1.2.0 archived release
    └── v1.0.0/remote-compose.html    # Version 1.0.0 baseline release
```

---

## 🚀 Installation & Usage

### Install in Antigravity (`agy` CLI)
```bash
# Global installation (all projects)
cp -r html-doc-skill ~/.gemini/antigravity-cli/skills/

# Or project-level
cp -r html-doc-skill .skills/
```

### Prompting Example
> *"Generate interactive HTML documentation using the `doc-html` skill for our payment gateway API. Include standardized API tables, bilingual support, strictly LTR code blocks, and coordinate review comments."*

---

## 📜 License

MIT License — free for open-source and commercial use.
