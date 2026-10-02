---
name: doc-html
description: >
  Generate world-class, single-file interactive HTML technical documentation,
  architecture reports, and research whitepapers. Features dual-theme support (Dark/Light),
  instant bilingual LTR/RTL switching (English/Persian with strict persian-writing standards),
  persistent Acrobat/ChatGPT-style catalog sidebar navigation, reading progress indicator (e.g. 2/5),
  colorful syntax-highlighted and copiable code blocks, responsive layouts (mobile, tablet, desktop),
  HTML/CSS architecture grids, Mermaid.js diagrams, interactive test labs,
  referenced citations with 1-click copy, two-pane Git-style diff viewer, and
  strict anti-hallucination ground-truth enforcement.
metadata:
  version: 1.1.0
  author: Digital Sign SDK & Antigravity Team
  license: MIT
  tags:
    - documentation
    - html
    - responsive
    - bilingual
    - rtl
    - persian
    - vazirmatn
    - syntax-highlighting
    - dark-mode
    - sidebar-catalog
    - diff-viewer
    - anti-hallucination
---

# `doc-html`: Standalone HTML Documentation Generator Skill

## 1. Overview & Core Philosophy

The `doc-html` skill teaches AI agents how to generate **modern, responsive, single-file, interactive HTML documentation** for software projects, cryptographic audits, API specifications, and architectural whitepapers.

### The Seven Inviolable Pillars
1. **Self-Contained & Zero Build Step:** The output must open directly in any browser (Chrome, Safari, Firefox, Edge on Windows, Mac, Linux, iOS, Android) via `file://` or HTTP without needing Node.js, Webpack, or a static site generator.
2. **Dual-Theme Engine (Dark / Light):** Smooth CSS variable-based transitions between a deep slate/midnight dark theme and a crisp light theme, persistent in `localStorage`.
3. **Zero-Reload Bilingual & RTL/LTR Switcher:** Seamless instantaneous language switching (e.g., English LTR and Persian RTL) using pure CSS `data-lang` filtering.
4. **Persistent Catalog Navigation & Progress:** Adobe Acrobat / ChatGPT-style sidebar catalog that stays accessible on all screen sizes, with scrollspy and a dynamic reading progress indicator (e.g., `Section 2 of 7` / `بخش ۲ از ۷` + top progress bar).
5. **Strict Persian Typography & Terminology Standard:** Strict adherence to `persian-writing` (Vazirmatn font, ZWNJ, Persian numerals, «گیومه», no bureaucratic tells). Crucially, **established industry terms must remain in English** (`Secure Enclave`, `KeyStore`, `WebAuthn`, `Passkeys`, `TPM 2.0`) rather than forced, unnatural translations.
6. **Colorful Syntax Highlighting & 1-Click Copy:** Powered by Highlight.js CDN with language badges, synchronized dark/light code themes, and animated visual copy feedback.
7. **Anti-Hallucination & Ground-Truth Enforcement:** If a requested API, feature, or security capability does not exist in verified source code, standards, or web documentation, the agent **MUST NOT invent or hallucinate it**. It must explicitly state: *"Nothing found / Not supported in current standards"*.

---

## 2. Anti-Hallucination & Ground-Truth Rule (Mandatory)

> [!CAUTION]
> **Strict Verification Before Claiming:**
> When asked whether a library, browser, or OS supports a cryptographic primitive, hardware backing, or API method:
> 1. Check verified source code or official W3C / RFC / vendor specifications.
> 2. **If a concept or feature does NOT exist, explicitly state: *"No evidence or support found in current specifications"*.**
> 3. **DO NOT invent fake parameters** (e.g., do NOT invent `crypto.subtle.generateKey({ hardwareProtected: true })` or pretend WebCrypto connects to biometric hardware).
> 4. Disclose exact limitations: Clearly delineate software in-memory emulation versus genuine silicon hardware enforcement.

---

## 3. Bilingual Terminology & Persian Rules

### 3.1 Strict Prohibition of Phonetic Transliteration (No "Fingilish" / عدم آوانگاری نام‌های خاص)
> [!CAUTION]
> **Never phonetically transliterate English technology, browser, OS, hardware, vendor, or cryptographic terms into Persian script.**
> Writing phonetic approximations (e.g. «سافاری» for Safari, «کروم» for Chrome, «وب‌کریپتو» for Web Crypto) is strictly prohibited. It creates awkward, unsearchable, and unprofessional text.
> **All proper nouns, vendor brands, browser engines, operating systems, hardware modules, and cryptographic APIs MUST be written in their standard English / Latin form.**

#### Terminology Enforcement Matrix

| Category | ❌ Strict Ban (Phonetic Transliteration) | ✅ Mandatory Standard Form |
| :--- | :--- | :--- |
| **Browsers** | سافاری، کروم، فایرفاکس، اج، وب‌کیت | `Safari`, `Chrome`, `Firefox`, `Edge`, `WebKit` |
| **Operating Systems** | اندروید، آی‌او‌اس، ویندوز، مک، لینوکس | `Android`, `iOS`, `Windows`, `macOS` / `Mac`, `Linux` |
| **Security Hardware** | انکلاو، انکلاو امن، کی‌استور، استرانگ‌باکس، تی‌پی‌ام | `Secure Enclave`, `Android KeyStore`, `StrongBox`, `TPM 2.0` |
| **Web & Crypto APIs** | وب‌کریپتو، وب‌اتن، وب‌آتن، پس‌کی | `Web Crypto API`, `WebAuthn`, `Passkeys` |
| **Biometric Sensors** | فیس‌آیدی، تاچ‌آیدی، ویندوز هلو | `Face ID`, `Touch ID`, `Windows Hello` |
| **Architecture & Memory** | رم، حافظه رم، هیپ، دامپ رم | `RAM`, `حافظه RAM`, `Heap`, `Memory Dump` / `دامپ RAM` |
| **Tech Companies** | اپل، گوگل، مایکروسافت، موزیلا | `Apple`, `Google`, `Microsoft`, `Mozilla` |
| **Languages & Runtimes** | جاوااسکریپت، تایپ‌اسکریپت، کاتلین، سوئیفت | `JavaScript`, `TypeScript`, `Kotlin`, `Swift` |

### 3.2 Persian Orthography Rules (`persian-writing` Compliance)
1. **Font Family:** **Vazirmatn** (weights 300 to 900) via Google Fonts.
2. **Line Height:** Must be `1.8` to `1.85` for Persian text.
3. **Never Letter-Space Persian:** `letter-spacing: normal !important;` (tracking tears apart Arabic/Persian cursive connections).
4. **Half-Space (نیم‌فاصله / ZWNJ, U+200C):** Enforce on all prefixes, plurals, and compound words: `می‌شود`، `سخت‌افزاری`، `نرم‌افزاری`، `کلیدهای`، `ذخیره‌سازی`، `رمزنگاری`، `آسیب‌پذیری`.
5. **Persian Characters Only:** `ی` (U+06CC) and `ک` (U+06A9) — never Arabic `ي` or `ك`.
6. **Persian Numerals & Punctuation:** `۰ ۱ ۲ ۳ ۴ ۵ ۶ ۷ ۸ ۹` in Persian prose; Persian comma `،`؛ semicolon `؛`؛ quotes in `«گیومه»`.
7. **Ban Bureaucratic Verbs:** Replace `می‌باشد` with `است`؛ replace `می‌گردد` with `می‌شود`؛ replace `می‌نماید` with `می‌کند`. Ban `لازم به ذکر است` and `در راستای`.
8. **Ban AI Tropes:** No em dashes (`—`) in Persian sentences; ban artificial triad clichés (`سریع، آسان و امن`).

---

## 4. UI Architecture & Color System

### 4.1 CSS Custom Properties
```css
:root, [data-theme="dark"] {
  --bg-base: #0a0f1d;
  --bg-surface: #10172a;
  --bg-surface-elevated: #172036;
  --bg-surface-hover: #1f2c4a;
  --border-subtle: rgba(255, 255, 255, 0.08);
  --border-strong: rgba(255, 255, 255, 0.16);
  --text-main: #f1f5f9;
  --text-muted: #94a3b8;
  --text-dim: #64748b;
  --primary: #38bdf8;
  --primary-glow: rgba(56, 189, 248, 0.18);
  --primary-dark: #0284c7;
  --accent: #818cf8;
  --success: #34d399;
  --success-bg: rgba(52, 211, 153, 0.12);
  --warning: #fbbf24;
  --warning-bg: rgba(251, 191, 36, 0.12);
  --danger: #f87171;
  --danger-bg: rgba(248, 113, 113, 0.12);
  --code-bg: #070b14;
  --code-border: #1e293b;
  --badge-bg: rgba(56, 189, 248, 0.12);
  --link-color: #38bdf8;
  --link-hover: #7dd3fc;
  --shadow: 0 10px 30px -10px rgba(0, 0, 0, 0.5);
}

[data-theme="light"] {
  --bg-base: #f8fafc;
  --bg-surface: #ffffff;
  --bg-surface-elevated: #f1f5f9;
  --bg-surface-hover: #e2e8f0;
  --border-subtle: rgba(0, 0, 0, 0.08);
  --border-strong: rgba(0, 0, 0, 0.16);
  --text-main: #0f172a;
  --text-muted: #475569;
  --text-dim: #64748b;
  --primary: #0284c7;
  --primary-glow: rgba(2, 132, 199, 0.15);
  --primary-dark: #0369a1;
  --accent: #6366f1;
  --success: #059669;
  --success-bg: rgba(5, 150, 105, 0.1);
  --warning: #d97706;
  --warning-bg: rgba(217, 119, 6, 0.1);
  --danger: #dc2626;
  --danger-bg: rgba(220, 38, 38, 0.1);
  --code-bg: #f8fafc;
  --code-border: #cbd5e1;
  --badge-bg: rgba(2, 132, 199, 0.1);
  --link-color: #0284c7;
  --link-hover: #0369a1;
  --shadow: 0 10px 25px -10px rgba(0, 0, 0, 0.08);
}
```

### 4.2 Distinct Inline Linking
Inline links must be clearly distinguishable from surrounding text:
```css
/* Inline links with distinct accent color and subtle underline */
a.doc-link, p a, li a:not(.nav-item) {
  color: var(--link-color);
  text-decoration: underline;
  text-decoration-thickness: 1.5px;
  text-underline-offset: 3px;
  font-weight: 500;
  transition: color 0.15s ease, text-decoration-color 0.15s ease;
}
a.doc-link:hover, p a:hover, li a:not(.nav-item):hover {
  color: var(--link-hover);
  text-decoration-color: var(--primary);
}
```

---

## 5. Acrobat/ChatGPT-Style Catalog Sidebar & Reading Progress

### 5.1 Top Reading Progress Bar
A fixed 3px progress bar at the top of the viewport indicating scroll completion:
```html
<div id="scrollProgressBar" style="position: fixed; top: 0; left: 0; height: 3px; background: linear-gradient(90deg, var(--primary), var(--accent)); width: 0%; z-index: 1000; transition: width 0.1s ease;"></div>
```

### 5.2 Section Counter ("2 of 7" / "بخش ۲ از ۷")
A pill in the navbar or floating header updated by Scrollspy:
```html
<span class="progress-pill">
  <span data-lang="en">Section <strong id="progressIndexEn">1</strong> of 7</span>
  <span data-lang="fa">بخش <strong id="progressIndexFa">۱</strong> از ۷</span>
</span>
```

### 5.3 Sidebar Catalog Navigation
The document layout is divided into a sidebar rail and a main content area:
- **On Desktop:** Sidebar displays a collapsible list of all sections, with active highlighting on scroll (Scrollspy).
- **On Tablet & Mobile:** Collapses into a floating TOC button (`📑 Contents`) that opens an off-canvas drawer with smooth backdrop blur.

```html
<!-- Mobile Drawer Backdrop -->
<div id="sidebarBackdrop" class="sidebar-backdrop" onclick="toggleSidebar()"></div>

<!-- Catalog Sidebar -->
<aside id="catalogSidebar" class="catalog-sidebar">
  <div class="sidebar-header">
    <div class="sidebar-title">
      <span>📑</span>
      <span data-lang="en">Document Catalog</span>
      <span data-lang="fa">فهرست موضوعی</span>
    </div>
    <button class="btn-close-sidebar" onclick="toggleSidebar()">✕</button>
  </div>
  <nav class="sidebar-nav">
    <a href="#verdict" class="sidebar-link active" onclick="closeSidebarOnMobile()">
      <span class="sidebar-num">01</span>
      <span data-lang="en">Executive Verdict</span>
      <span data-lang="fa">حکم و چکیده فنی</span>
    </a>
    <a href="#matrix" class="sidebar-link" onclick="closeSidebarOnMobile()">
      <span class="sidebar-num">02</span>
      <span data-lang="en">Browser Architecture</span>
      <span data-lang="fa">ماتریس موتور مرورگرها</span>
    </a>
    <!-- Additional section links... -->
  </nav>
</aside>
```

---

## 6. References Section with 1-Click Copy Links

Every technical document must conclude with a structured references block. Each reference entry features a 1-click button that copies the citation / URL to the clipboard with animated confirmation:

```html
<section id="references">
  <h2 class="section-title">
    <span class="number">08</span>
    <span data-lang="en">Authoritative References & Standards</span>
    <span data-lang="fa">مراجع و استانداردهای معتبر</span>
  </h2>
  <div class="references-list">
    <div class="ref-card">
      <div class="ref-info">
        <span class="ref-tag">W3C Recommendation</span>
        <h4 class="ref-title">Web Cryptography API (W3C Standard)</h4>
        <p class="ref-url">https://www.w3.org/TR/WebCryptoAPI/</p>
      </div>
      <button class="btn-copy-ref" onclick="copyCitation('https://www.w3.org/TR/WebCryptoAPI/', this)">
        <span>🔗</span> <span class="copy-ref-text" data-lang="en">Copy Link</span><span class="copy-ref-text" data-lang="fa">کپی لینک</span>
      </button>
    </div>
  </div>
</section>
```

---

## 7. Version History & Two-Pane Visual Diff Viewer

To show how specifications evolve between revisions without losing context, provide a **Two-Pane Diff Viewer** mode (like Git split diff):

```html
<section id="version-history">
  <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 16px;">
    <h2 class="section-title">
      <span class="number">09</span>
      <span data-lang="en">Version History & Diff Mode</span>
      <span data-lang="fa">تاریخچه نسخه‌ها و نمایش مقایسه (Diff)</span>
    </h2>
    <div class="diff-toggle-bar">
      <button class="btn-control" id="diffViewBtn" onclick="toggleDiffMode()">
        <span>⚖️</span>
        <span data-lang="en">Toggle Visual Diff</span>
        <span data-lang="fa">نمایش مقایسه تغییرات (Diff)</span>
      </button>
    </div>
  </div>

  <div id="diffViewer" class="diff-viewer-container" style="display: none;">
    <div class="diff-header">
      <div class="diff-pane-title old-ver">v1.0.0 (Baseline)</div>
      <div class="diff-pane-title new-ver">v1.1.0 (Current)</div>
    </div>
    <div class="diff-body">
      <div class="diff-line del">
        <span class="diff-prefix">-</span>
        <span>Safari WebCrypto places CryptoKey inside Secure Enclave by default.</span>
      </div>
      <div class="diff-line add">
        <span class="diff-prefix">+</span>
        <span>Safari WebCrypto runs in WebProcess RAM; Secure Enclave is accessed ONLY via WebAuthn.</span>
      </div>
    </div>
  </div>
</section>
```

---

## 8. Colorful Code Blocks & Highlight.js

Every code snippet must include:
- Synchronized dark/light stylesheets (`Atom One Dark` / `Atom One Light`).
- Filename header with a colorful language badge (`JS`, `Kotlin`, `Swift`, `Python`, `Go`, `Rust`, `Bash`).
- Accessible 1-click copy button with instant feedback (`✓ Copied!` / `✓ کپی شد!`).

```html
<div class="code-container">
  <div class="code-header">
    <div style="display: flex; align-items: center; gap: 8px;">
      <span class="code-lang-badge js">JavaScript</span>
      <span>auth_service.js</span>
    </div>
    <button class="btn-copy" onclick="copyCode(this)">
      <span>📋</span> <span class="copy-text" data-lang="en">Copy</span><span class="copy-text" data-lang="fa">کپی کد</span>
    </button>
  </div>
  <pre><code class="language-javascript">// Code here...</code></pre>
</div>
```

---

---

## 9. Visual Media: Images, Diagrams & Interactive Charts

### 9.1 Interactive Charts (Chart.js CDN)
When presenting metrics, benchmarks, timelines, or progression data:
- Load Chart.js CDN (`https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js`).
- Wrap canvas in a responsive container with fixed height (e.g. `height: 320px; position: relative;`).
- **Theme Synchronization:** When the user toggles Dark/Light theme, update the chart's colors (`ticks.color`, `grid.color`, `tooltip`) dynamically and call `chart.update()`.

```html
<div class="chart-container" style="position: relative; height: 320px; width: 100%;">
  <canvas id="metricChart"></canvas>
</div>
<script>
  let myChart;
  function initChart(theme) {
    const isDark = theme === 'dark';
    const textColor = isDark ? '#94a3b8' : '#475569';
    const gridColor = isDark ? 'rgba(255, 255, 255, 0.06)' : 'rgba(0, 0, 0, 0.06)';
    // create or update Chart instance...
  }
</script>
```

### 9.2 Diagrams: Mermaid.js & Architecture Grids
- **Mermaid.js CDN:** Load `https://cdnjs.cloudflare.com/ajax/libs/mermaid/10.9.0/mermaid.min.js` for sequence diagrams, state machines, and flowcharts. Initialize with `mermaid.initialize({ startOnLoad: true, theme: currentTheme === 'dark' ? 'dark' : 'neutral' });`.
- **CSS Architecture Grids:** For bilingual (LTR/RTL) architecture comparisons, prefer responsive HTML/CSS Grid cards over raw SVG text, as SVG text coordinate inversion under `dir="rtl"` causes layout truncation.

### 9.3 Responsive Figures, Images & Pure JS Lightbox
- Wrap images in semantic `<figure class="doc-figure">` with `<figcaption>` containing bilingual captions.
- Images must have `max-width: 100%; height: auto; border-radius: var(--radius); border: 1px solid var(--border-subtle);`.
- In dark mode, apply `filter: brightness(0.9) contrast(1.05);` to reduce eye strain.
- **Lightbox Preview:** Include a simple, zero-dependency click-to-zoom modal:
```html
<!-- Lightbox Modal -->
<div id="imageLightbox" class="lightbox-modal" onclick="closeLightbox()">
  <img id="lightboxImg" src="" alt="Enlarged view">
</div>
<script>
  function openLightbox(src) {
    const lb = document.getElementById('imageLightbox');
    document.getElementById('lightboxImg').src = src;
    lb.classList.add('active');
  }
  function closeLightbox() {
    document.getElementById('imageLightbox').classList.remove('active');
  }
  document.addEventListener('keydown', (e) => { if (e.key === 'Escape') closeLightbox(); });
</script>
```

---

## 10. Generation Checklist

Before delivering an HTML documentation file using `doc-html`:

- [ ] **Anti-Hallucination:** Every API parameter, hardware claim, and factual statement is backed by real specs or marked as "Not Supported / Nothing Found".
- [ ] **No "Fingilish" Transliteration:** Proper nouns, brands, browsers, OS, and APIs are written in standard English (`Safari`, `Chrome`, `Android`, `iOS`, `Secure Enclave`, `KeyStore`, `WebAuthn`).
- [ ] **Catalog Sidebar:** Persistent on desktop, off-canvas drawer on mobile, with active section highlighting on scroll.
- [ ] **Reading Progress:** Top horizontal progress bar + dynamic `Section X of Y` badge working properly.
- [ ] **Bilingual & RTL:** Dual `data-lang` spans with zero-reload switcher; Vazirmatn font with line-height 1.85, ZWNJ, and no bureaucratic verbs.
- [ ] **Distinct Links:** All inline hyperlinks have distinct colors and underlines.
- [ ] **Visual Media & Charts:** Responsive charts (Chart.js / SVG), diagrams (Mermaid / CSS Grid), and zoomable figures included where relevant.
- [ ] **Copiable Code:** Highlight.js colorful highlighting with 1-click copy buttons and animated feedback.
- [ ] **References & Diff:** Reference section with copy buttons + Version History / Diff viewer included.
- [ ] **100% Responsive:** Verified on mobile (360px), tablet (768px), and desktop (1280px).

