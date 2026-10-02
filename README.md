# `doc-html` — Modern Interactive HTML Documentation Skill

A production-grade, publishable AI coding assistant skill for generating **gorgeous, single-file, interactive HTML technical documentation and architecture whitepapers**.

---

## 🌟 Key Features

- 📑 **Persistent Catalog Sidebar Navigation (Adobe Acrobat / ChatGPT Style)**:
  - Collapsible slide-out catalog drawer with backdrop for mobile, tablet, and desktop.
  - Scrollspy active section highlighting for frictionless document navigation.
- ⏱️ **Reading Progress Indicator**:
  - Slim top progress bar and dynamic counter pill (e.g. `Section 2 of 9` / `بخش ۲ از ۹`).
- 🌓 **Dual-Theme System (Dark / Light)**: Fluid CSS variable transitions with persistent `localStorage` memory and synced code themes.
- 🌐 **Zero-Reload Bilingual Engine (English & Persian)**: Pure CSS `data-lang` filtering with instant LTR/RTL layout switching without page reload.
- 🚫 **Strict Prohibition of Phonetic Transliteration ("Fingilish")**:
  - Proper nouns, browser engines (`Safari`, `Chrome`), OS names (`Android`, `iOS`, `Windows`, `macOS`), and hardware (`Secure Enclave`, `KeyStore`) remain in Latin characters; no awkward phonetic transliterations (e.g. no «سافاری» or «وب‌کریپتو»).
- 🖋️ **Persian Typography Excellence (`persian-writing` Certified)**:
  - Bundled/Linked with **Vazirmatn** font (weights 300 to 900).
  - Proper line-height (1.85) to prevent clipped dots and ascenders.
  - Strict Half-Space (نیم‌فاصله / ZWNJ) enforcement.
  - Zero bureaucratic tells (`است` instead of `می‌باشد`).
  - Persian numerals (`۰۱۲۳۴۵۶۷۸۹`) in prose and «گیومه» quotation marks.
- 🎨 **Colorful Syntax Highlighting with Library (Highlight.js CDN)**:
  - Pre-configured for JavaScript, TypeScript, Kotlin, Swift, Python, Go, Rust, and Bash.
  - Synchronized dark (`Atom One Dark`) and light (`Atom One Light`) themes.
  - Language badges on code blocks.
- 📋 **1-Click Copy with Animated Visual Feedback**:
  - Interactive copy button that copies clean code to clipboard.
  - Contextual feedback (`✓ Copied!` in English, `✓ کپی شد!` in Persian).
- 🔗 **References & Standards with 1-Click Citation Copy**:
  - Verified W3C, RFC, and vendor specifications with instant clipboard copy.
- 🔀 **Two-Pane Git-Style Visual Diff Viewer**:
  - Side-by-side semantic diff pane comparing baseline vs. audited releases with green/red line changes.
- 🛡️ **Anti-Hallucination Ground-Truth Enforcement**:
  - Mandate to state "Nothing found / Not supported" when a feature or API does not exist; zero hallucinated parameters.
- 📐 **Diagrams**:
  - Responsive **HTML/CSS architecture comparison cards** (eliminating SVG coordinate flipping bugs in RTL mode).
  - Optional **Mermaid.js** CDN support for sequence diagrams and state machines.
- ⚡ **Interactive Live Labs & Test Suites**:
  - Embedded live testing sandboxes directly inside the HTML page.
- 📱 **100% Mobile & Touch Responsive**:
  - Touch-scrolling tables, auto-reflowing card grids, and mobile-friendly navbars.

---

## 📂 Directory Structure

```
doc-html/
├── SKILL.md                          # Authoritative skill instructions for AI agents
├── README.md                         # Publication & user documentation
└── resources/
    └── starter-template.html         # Boilerplate clean starter HTML template
```

---

## 🚀 How to Use & Install

### Installation for Antigravity (`agy` CLI)
Copy this directory into your global skills or project workspace:

```bash
# Global installation (available to all projects)
cp -r doc-html ~/.gemini/antigravity/skills/

# Or project-level installation
cp -r doc-html .skills/
```

### Prompting the Agent
Simply ask your AI agent:
> *"Generate an interactive HTML documentation file using the `doc-html` skill covering our authentication architecture, with bilingual support and live test cases."*

---

## 📜 License

MIT License — free for open-source and commercial use.
Typography powered by [Vazirmatn](https://github.com/rastikerdar/vazirmatn) (SIL Open Font License).
Syntax highlighting powered by [Highlight.js](https://highlightjs.org) (BSD 3-Clause).
