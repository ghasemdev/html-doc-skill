---
name: doc-html
description: >
  Generate world-class, single-file interactive HTML technical documentation,
  API specifications, architecture reports, and research whitepapers. Features dual-theme support (Dark/Light),
  instant bilingual LTR/RTL switching (English/Persian with strict persian-writing standards),
  persistent Acrobat/ChatGPT-style catalog sidebar navigation, reading progress indicator,
  strictly LTR colorful syntax-highlighted code blocks, standardized API documentation tables,
  coordinate drag-and-drop commenting on API specs with slide-out review drawer, JSON export for AI,
  and embedded HTML persistence, 1-click PDF export via html2pdf.js, real multi-version navigation
  with archive banners, flawless zero-overflow mobile layout, context-aware modularity, and strict anti-hallucination ground-truth enforcement.
metadata:
  version: 2.0.0
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
    - api-docs
    - coordinate-comments
    - review-drawer
    - pdf-export
    - multi-versioning
    - anti-hallucination
---

# `doc-html`: Standalone HTML Documentation Generator Skill

## 1. Overview & Core Philosophy

The `doc-html` skill teaches AI agents how to generate **modern, responsive, single-file, interactive HTML documentation** for software projects, cryptographic audits, API specifications, and architectural whitepapers.

### The Nine Inviolable Pillars
1. **Self-Contained & Zero Build Step:** The output opens directly in any browser via `file://` or HTTP without needing Node.js or static site generators.
2. **Dual-Theme Engine (Dark / Light):** Smooth CSS variable-based transitions between midnight dark and crisp light themes, persistent in `localStorage`.
3. **Zero-Reload Bilingual & RTL/LTR Switcher:** Seamless instantaneous language switching (e.g., English LTR and Persian RTL) using pure CSS `data-lang` filtering.
4. **Persistent Catalog Navigation & Progress:** Adobe Acrobat / ChatGPT-style sidebar catalog that collapses into a responsive off-canvas drawer on mobile (`width: min(85vw, 290px)`), with active scrollspy and a reading progress indicator.
5. **Strictly Left-to-Right (LTR) Code Blocks:** In both RTL (Persian) and LTR (English) modes, **all code blocks, inline snippets, file paths, and syntax blocks MUST always be LTR (`direction: ltr !important; text-align: left !important; unicode-bidi: isolate;`)**.
6. **Standardized API Documentation Tables:** Comprehensive, structured API endpoint documentation with HTTP method badges, parameters table (Name, Type, Placement/Required, Description, Example), strictly LTR JSON request/response previews, and status/error tables.
7. **Coordinate Drag & Drop Commenting on API Specs:** Reviewers can drag a comment pin bubble onto any $(x, y)$ coordinate or click directly on API tables/code to leave a numbered pin. Clicking the toolbar `💬` icon slides out a review drawer displaying all comments, pin coordinates, "Jump to Pin" focus triggers, JSON export for AI, and embedded HTML persistence.
8. **1-Click PDF Export via 3rd-Party Library (`html2pdf.js`):** Client-side A4 PDF export with progress toast and automated page-break avoidance (`break-inside: avoid`).
9. **Real Multi-Version Navigation:** Live routing between documentation releases (`v2.0.0`, `v1.2.0`, `v1.0.0`) with prominent archive alert banners on older versions.

---

## 2. Content-Aware Modularity & Discretion (Mandatory)

> [!IMPORTANT]
> **Context-Aware Selection — Do NOT Force Unrelated Sections:**
> Before generating an HTML document, the AI agent **MUST evaluate the document topic and user prompt** to determine which components are appropriate:
> 
> 1. **Do NOT force API Documentation tables** if the document is an architectural whitepaper, research summary, or algorithmic guide without HTTP/RPC endpoints.
> 2. **Do NOT force Mermaid.js diagrams** if there is no genuine sequence, state-machine, or workflow to depict.
> 3. **Do NOT invent or include broken `<img>` tags** if real image URLs or assets do not exist. Use CSS architecture grids, structured metric cards, or clean SVG graphics instead.
> 4. **Do NOT add toy interactive simulators / playgrounds** if they do not add tangible technical depth to the subject matter.
> 5. **Include only modules that provide genuine technical value** to the reader.

---

## 3. Anti-Hallucination & Ground-Truth Rule (Mandatory)

> [!CAUTION]
> **Strict Verification Before Claiming:**
> When asked whether a library, browser, or OS supports a cryptographic primitive, hardware backing, or API method:
> 1. Check verified source code or official W3C / RFC / vendor specifications.
> 2. **If a concept or feature does NOT exist, explicitly state: *"No evidence or support found in current specifications"*.**
> 3. **DO NOT invent fake parameters** (e.g., do NOT invent `crypto.subtle.generateKey({ hardwareProtected: true })` or pretend WebCrypto connects to biometric hardware).
> 4. Disclose exact limitations: Clearly delineate software in-memory emulation versus genuine silicon hardware enforcement.

---

## 4. Bilingual Terminology & Persian Rules

### 4.1 Strict Prohibition of Phonetic Transliteration (No "Fingilish" / عدم آوانگاری نام‌های خاص)
> [!CAUTION]
> **Never phonetically transliterate English technology, browser, OS, hardware, vendor, or cryptographic terms into Persian script.**
> Writing phonetic approximations (e.g. «سافاری» for Safari, «کروم» for Chrome, «وب‌کریپتو» for Web Crypto) is strictly prohibited.
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

### 4.2 Persian Orthography Rules (`persian-writing` Compliance)
1. **Font Family:** **Vazirmatn** (weights 300 to 900) via Google Fonts.
2. **Line Height:** Must be `1.8` to `1.85` for Persian text.
3. **Never Letter-Space Persian:** `letter-spacing: normal !important;`.
4. **Half-Space (نیم‌فاصله / ZWNJ, U+200C):** Enforce on all prefixes, plurals, and compound words: `می‌شود`، `سخت‌افزاری`، `نرم‌افزاری`، `کلیدهای`، `ذخیره‌سازی`.
5. **Persian Characters Only:** `ی` (U+06CC) and `ک` (U+06A9) — never Arabic `ي` or `ك`.
6. **Persian Numerals & Punctuation:** `۰ ۱ ۲ ۳ ۴ ۵ ۶ ۷ ۸ ۹` in Persian prose; Persian comma `،`؛ semicolon `؛`؛ quotes in `«گیومه»`.
7. **Ban Bureaucratic Verbs:** Replace `می‌باشد` with `است`؛ replace `می‌گردد` with `می‌شود`؛ replace `می‌نماید` با `می‌کند`. Ban `لازم به ذکر است` and `در راستای`.

---

## 5. Strictly LTR Code Blocks & Syntax Highlighting

> [!IMPORTANT]
> **Code Blocks Must ALWAYS Be Left-to-Right (LTR):**
> Even when the page direction is switched to RTL (`dir="rtl"`), all code snippets, terminal commands, JSON bodies, and code block headers **must remain strictly LTR**.

```css
/* Mandatory LTR rule for all code containers */
.code-container,
pre,
code,
.code-header,
.endpoint-url,
.json-preview {
  direction: ltr !important;
  text-align: left !important;
  unicode-bidi: isolate;
}
```

---

## 6. Standardized API Documentation Specification

Follow this **strict hierarchical structure** when documenting endpoints:
1. **API Title & Business Description (Top):** Purpose of the endpoint and business context.
2. **HTTP Method & URL Bar:** High-contrast method badge (`GET`, `POST`, `PUT`, `DELETE`, `PATCH`) alongside the full endpoint path with copy button.
3. **Parameters Table:** Parameter Name, Type, Placement/Required, Description, Example.
4. **Request & Response Body JSON Samples:** Strictly LTR formatted JSON with syntax highlighting.
5. **Errors & Status Codes Table:** HTTP Status Code, Error Key/Code, Description & Mitigation.

---

## 7. Coordinate Drag & Drop Commenting & Slide-Out Drawer

Review and feedback on API specifications use a coordinate pin drop system:
1. **Draggable Pin Widget:** A sticky bar containing `📍 Drag Pin onto Section` with active Pin Mode toggle.
2. **Coordinate Pin Drop:** Dragging the bubble or clicking anywhere inside the API section drops a numbered pin at relative $(X\%, Y\%)$.
3. **Pin Input Modal:** Prompts for reviewer role/name and review feedback.
4. **Slide-Out Comment Drawer:** Clicking the top toolbar `💬` icon slides out a full-height drawer with:
   - List of all dropped pins with $(X\%, Y\%)$ coordinates.
   - `🎯 Jump to Pin` button that smoothly scrolls to the exact element and pulses the pin.
   - `📥 Export JSON (for AI)` downloading AI-ready structured review data.
   - `💾 Save & Embed in HTML` downloading an updated HTML file with comments permanently embedded inside `<script id="docEmbeddedComments" type="application/json">`.

---

## 8. 3rd-Party PDF Export (`html2pdf.js`)

Use client-side library `html2pdf.js` via CDN:
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
```

```javascript
function exportDocumentToPDF() {
  const element = document.querySelector('.main-content');
  const opt = {
    margin: [8, 8, 8, 8],
    filename: 'Technical-Documentation.pdf',
    image: { type: 'jpeg', quality: 0.98 },
    html2canvas: { scale: 1.5, useCORS: true, logging: false },
    jsPDF: { unit: 'mm', format: 'a4', orientation: 'portrait' },
    pagebreak: { mode: ['avoid-all', 'css', 'legacy'] }
  };
  html2pdf().set(opt).from(element).save();
}
```

---

## 9. Real Multi-Version Navigation

Provide real routing between versions:
- Place versions in `examples/v2.0.0/`, `examples/v1.2.0/`, `examples/v1.0.0/`.
- The version dropdown navigates between versions via `switchVersion(ver)`.
- Older archived versions display a top warning banner:
  `⚠️ You are viewing archived version v1.0.0. [Switch to Latest (v2.0.0)]`.

---

## 10. Mobile Responsiveness Best Practices (Zero-Overflow Guarantee)

To guarantee zero horizontal scroll bugs and optimal mobile UX:

1. **Top Navbar Mobile Compaction:**
   On screens $\le 768\text{px}$:
   - Hide subtitles and badges (`.brand-pill`, `.progress-pill`).
   - Hide text labels on control buttons (`.btn-label { display: none; }`).
   - Compact button sizes ($32\times32\text{px}$) with icon-only presentation.
   - Limit version select width to $65\text{px}$.
   - Ensure the entire header fits on a single line $\le 300\text{px}$.

2. **Zero Horizontal Overflow:**
   ```css
   html, body, .app-layout {
     overflow-x: hidden !important;
     max-width: 100vw !important;
     width: 100% !important;
     box-sizing: border-box;
   }
   .main-content {
     min-width: 0 !important;
     max-width: 100% !important;
     width: 100% !important;
     overflow-x: hidden !important;
     box-sizing: border-box !important;
   }
   ```

3. **Tables and Code Containers:**
   Wrap all tables in `.table-responsive` / `.table-container`:
   ```css
   .table-responsive, .table-container {
     width: 100% !important;
     max-width: 100% !important;
     overflow-x: auto !important;
     -webkit-overflow-scrolling: touch;
     box-sizing: border-box;
   }
   .code-container {
     min-width: 0 !important;
     max-width: 100% !important;
     width: 100% !important;
     overflow: hidden !important;
   }
   pre {
     min-width: 0 !important;
     max-width: 100% !important;
     overflow-x: auto !important;
     box-sizing: border-box;
   }
   ```

4. **Scalable Canvas:**
   ```css
   canvas {
     width: 100% !important;
     max-width: 400px !important;
     height: auto !important;
     box-sizing: border-box;
   }
   ```
