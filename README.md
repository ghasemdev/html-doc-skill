# `doc-html` — Modern Interactive HTML Documentation Skill

[![GitHub Release](https://img.shields.io/github/v/release/ghasemdev/html-doc-skill?color=38bdf8&label=Release)](https://github.com/ghasemdev/html-doc-skill/releases)
[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-34d399?logo=github)](https://ghasemdev.github.io/html-doc-skill/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A production-grade, publishable AI coding assistant skill for generating **gorgeous, single-file, interactive HTML technical documentation, API specifications, architecture whitepapers, and dynamic research reports**.

🌐 **Live Interactive Demo:** [https://ghasemdev.github.io/html-doc-skill/](https://ghasemdev.github.io/html-doc-skill/)

---

## 🌟 What's New in v2.0.0

- 🔤 **Strictly Left-to-Right (LTR) Code Blocks:**
  All `<pre>`, `<code>`, `.code-container` blocks, headers, file paths, and JSON payloads are strictly enforced to render LTR (`direction: ltr !important; text-align: left !important; unicode-bidi: isolate;`), preserving code readability even in Persian RTL mode.
- 📡 **Standardized API Documentation Tables:**
  Rigid, high-readability API endpoint documentation structure:
  - Top API title & business description.
  - HTTP method badge (`POST`, `GET`, `PUT`, `DELETE`) with high-contrast pill + Endpoint URL with 1-click copy.
  - Parameters Table: Parameter Name, Type, Placement/Required, Description, Example.
  - Syntax-highlighted JSON Request & Response blocks (strictly LTR).
  - Status & Error Codes Table: HTTP Status, Error Code Key, Description & Mitigation.
- 📄 **1-Click PDF Export with Dedicated Print Stylesheet:**
  Header PDF button triggers `window.print()` with `@media print` rules that hide navigation rails, sidebars, interactive controls, and comment dialogs, ensuring pixel-perfect vector printing and page breaks.
- 💬 **Interactive Review & Comments System (AI Export & HTML Embed):**
  - **Inline Feedback:** Highlight text or click section `💬` buttons to record architectural notes and change requests.
  - **JSON Export for AI:** Export review notes as structured JSON formatted specifically for AI agents to process edits.
  - **Persistent HTML Embedding:** Embed all recorded comments directly into an internal `<script id="docEmbeddedComments" type="application/json">` tag and download an updated `.html` file. Sharing or emailing the file preserves all comments for any recipient without external databases!
- 🏷️ **Header Version Selector & Changelog Modal:**
  Clean version dropdown in the top navbar (`v2.0.0`, `v1.2.0`, `v1.0.0`) with a dedicated Changelog History modal (replacing bulky split-diff viewers).
- 📱 **Mobile & Drawer Responsiveness Best Practices:**
  Catalog sidebar automatically adapts on mobile to `width: min(85vw, 300px);` with touch-friendly targets (≥44px), backdrop dismiss, safe-area insets (`env(safe-area-inset)`), and touch-scrolling responsive tables.
- 🎯 **Context-Aware Modularity & Discretion:**
  Strict rule forbidding forced or irrelevant modules (no fake API tables if not an API doc, no Mermaid if no sequence needed, no broken fake images, no toy simulators unless genuinely educational).

---

## 🌟 Key Features

- 📑 **Persistent Catalog Sidebar Navigation (Adobe Acrobat / ChatGPT Style)**:
  - Collapsible slide-out catalog drawer with backdrop for mobile, tablet, and desktop.
  - Scrollspy active section highlighting for frictionless document navigation.
- ⏱️ **Reading Progress Indicator**:
  - Slim top progress bar and dynamic counter pill (e.g. `Section 2 of 11` / `بخش ۲ از ۱۱`).
- 🌓 **Dual-Theme System (Dark / Light)**: Fluid CSS variable transitions with persistent `localStorage` memory and synced code themes.
- 🌐 **Zero-Reload Bilingual Engine (English & Persian)**: Pure CSS `data-lang` filtering with instant LTR/RTL layout switching without page reload.
- 🚫 **Strict Prohibition of Phonetic Transliteration ("Fingilish")**:
  - Proper nouns, browser engines (`Safari`, `Chrome`), OS names (`Android`, `iOS`, `Windows`, `macOS`), and hardware (`Secure Enclave`, `KeyStore`) remain in Latin characters; no awkward phonetic transliterations (e.g. no «سافاری» or «وب‌کریپتو»).
- 🖋️ **Persian Typography Excellence (`persian-writing` Certified)**:
  - Bundled/Linked with **Vazirmatn** font (weights 300 to 900).
  - Proper line-height (1.85) to prevent clipped dots and ascenders.
  - Strict Half-Space (نیم‌فاصله / ZWNJ) enforcement.
  - Zero bureaucratic verbs (`است` instead of `می‌باشد`).
  - Persian numerals (`۰۱۲۳۴۵۶۷۸۹`) in prose and «گیومه» quotation marks.
- 🎨 **Colorful Syntax Highlighting (Highlight.js CDN)**:
  - Pre-configured for JavaScript, TypeScript, Kotlin, Swift, Python, Go, Rust, JSON, and Bash.
  - Synchronized dark (`Atom One Dark`) and light (`Atom One Light`) themes.
  - 1-click copy buttons with animated feedback (`✓ Copied!` / `✓ کپی شد!`).
- 🔗 **References & Standards with 1-Click Citation Copy**:
  - Verified W3C, RFC, and vendor specifications with instant clipboard copy.
- 🛡️ **Anti-Hallucination Ground-Truth Enforcement**:
  - Mandate to state "Nothing found / Not supported" when a feature or API does not exist; zero hallucinated parameters.
- 📊 **Interactive Charts & Data Visualizations (Chart.js CDN)**:
  - Responsive charts with automatic color palette re-theming on Dark/Light toggle.
- 📐 **Diagrams & Architecture Visuals**:
  - Responsive **HTML/CSS architecture comparison cards** (eliminating SVG coordinate flipping bugs in RTL mode).
  - Optional **Mermaid.js** CDN support for sequence diagrams, state machines, and workflows.

---

## 📂 Directory Structure

```
html-doc-skill/
├── SKILL.md                          # Authoritative skill instructions for AI agents (v2.0.0)
├── README.md                         # Publication & user documentation
├── index.html                        # GitHub Pages root entrypoint (Live Interactive Demo)
├── .nojekyll                         # GitHub Pages static asset bypass
├── examples/
│   └── remote-compose-architecture-and-usecases.html # Interactive bilingual showcase
└── resources/
    └── starter-template.html         # Boilerplate clean starter HTML template (v2.0.0)
```

---

## 🚀 How to Use & Install

### Installation for Antigravity (`agy` CLI)
Copy this directory into your global skills or project workspace:

```bash
# Global installation (available to all projects)
cp -r html-doc-skill ~/.gemini/antigravity-cli/skills/

# Or project-level installation
cp -r html-doc-skill .skills/
```

### Prompting the Agent
Simply ask your AI assistant:
> *"Generate an interactive HTML documentation file using the `doc-html` skill for our payment gateway API and microservice architecture. Include standardized API tables, bilingual English/Persian text, strictly LTR code blocks, and the inline review feature."*

---

## 📜 License

MIT License — free for open-source and commercial use.  
Typography powered by [Vazirmatn](https://github.com/rastikerdar/vazirmatn) (SIL Open Font License).  
Syntax highlighting powered by [Highlight.js](https://highlightjs.org) (BSD 3-Clause).
