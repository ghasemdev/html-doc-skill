# Changelog

All notable changes to the `doc-html` documentation skill and its reference implementations will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [2.0.0] — 2026-10-03

### Added
- **Coordinate Drag & Drop Commenting:** Readers can drag a comment pin onto any $(x, y)$ coordinate in the API specification section or click anywhere to drop a pin.
- **Slide-Out Comment Drawer:** Replaced modals with a slide-out drawer displaying all comments, coordinates, "Jump to Pin" focus triggers, JSON AI export, and HTML file persistence.
- **Client-Side PDF Generation via `html2pdf.js`:** Integrated 3rd-party library `html2pdf.js` for 1-click A4 PDF export with page-break management and progress indicator.
- **Real Multi-Version Navigation:** Full cross-version routing (`v2.0.0`, `v1.2.0`, `v1.0.0`) with dedicated document versions and archived version alert banners.
- **Standardized API Specification Hierarchy:**
  - Endpoint title and business description at the top.
  - High-contrast HTTP method badges (`POST`, `GET`, `PUT`, `DELETE`) with 1-click URL copy.
  - Parameters table (Name, Type, Placement/Required, Description, Example).
  - Strictly LTR JSON Request and Response syntax-highlighted blocks.
  - HTTP Status and Error Codes table (Status, Error Code, Description, Resolution).
- **Strictly LTR Code Blocks:** All `<pre>`, `<code>`, `.code-container`, headers, and JSON previews are strictly forced to Left-to-Right (`direction: ltr !important; text-align: left !important; unicode-bidi: isolate;`), even when the document is switched to Persian RTL mode.
- **Mobile Responsiveness Overhaul:**
  - Fixed horizontal scroll bug on mobile viewports (scaled `#remoteComposeCanvas`, container constraints).
  - Compact mobile top navbar with icon buttons and hidden subtitle pills.
  - Responsive catalog sidebar drawer (`width: min(85vw, 300px)`).
  - Safe-area insets (`env(safe-area-inset)`).
  - Horizontal touch-scrolling for all tables (`table-responsive`).
- **Context-Aware Modularity Rule:** AI agents must not force irrelevant components (APIs, Mermaid, broken images, or toy simulators) if not appropriate for the document topic.

### Removed
- **Split Diff Viewer:** Removed the bulky two-pane Git diff viewer in favor of clean version navigation and changelogs.

---

## [1.2.0] — 2026-05-18

### Added
- SIMD-accelerated RPN math evaluation engine.
- Nano-binary envelope parser and dynamic memory compaction.
- Wear OS 5 standalone display controller integration.

---

## [1.1.0] — 2026-02-12

### Added
- Visual Chart.js benchmarks with dynamic dark/light theme switching.
- Responsive HTML/CSS architecture grids replacing SVG text in RTL.
- Pure JS zoomable image lightbox modal.

---

## [1.0.0] — 2025-11-10

### Added
- Initial release of `doc-html` skill.
- Dual-theme engine (Dark/Light) with `localStorage` memory.
- Zero-reload bilingual switcher (English / Persian) with Vazirmatn typography.
- Persistent Adobe Acrobat / ChatGPT-style catalog sidebar navigation.
- Highlight.js colorful syntax highlighting with 1-click copy buttons.
- Anti-hallucination ground-truth enforcement.
