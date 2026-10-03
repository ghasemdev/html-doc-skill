---
name: doc-html
description: >
  Generate world-class, single-file interactive HTML technical documentation,
  architecture reports, and research whitepapers. Features dual-theme support (Dark/Light),
  instant bilingual LTR/RTL switching (English/Persian with strict persian-writing standards),
  persistent Acrobat/ChatGPT-style catalog sidebar navigation, reading progress indicator,
  strictly LTR colorful syntax-highlighted code blocks, standardized API documentation tables,
  inline review and commenting system with JSON export for AI and embedded HTML persistence,
  1-click PDF export, header version selector with changelog history, responsive mobile layout,
  content-aware modularity, and strict anti-hallucination ground-truth enforcement.
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
    - review-comments
    - pdf-export
    - versioning
    - anti-hallucination
---

# `doc-html`: Standalone HTML Documentation Generator Skill

## 1. Overview & Core Philosophy

The `doc-html` skill teaches AI agents how to generate **modern, responsive, single-file, interactive HTML documentation** for software projects, cryptographic audits, API specifications, and architectural whitepapers.

### The Nine Inviolable Pillars
1. **Self-Contained & Zero Build Step:** The output must open directly in any browser (Chrome, Safari, Firefox, Edge on Windows, Mac, Linux, iOS, Android) via `file://` or HTTP without needing Node.js, Webpack, or a static site generator.
2. **Dual-Theme Engine (Dark / Light):** Smooth CSS variable-based transitions between a deep slate/midnight dark theme and a crisp light theme, persistent in `localStorage`.
3. **Zero-Reload Bilingual & RTL/LTR Switcher:** Seamless instantaneous language switching (e.g., English LTR and Persian RTL) using pure CSS `data-lang` filtering.
4. **Persistent Catalog Navigation & Progress:** Adobe Acrobat / ChatGPT-style sidebar catalog that collapses smoothly into a responsive drawer on mobile/tablet, with scrollspy and a dynamic reading progress indicator (e.g., `Section 2 of 7` / `بخش ۲ از ۷` + top progress bar).
5. **Strictly Left-to-Right (LTR) Code Blocks:** Regardless of whether the document is in RTL (Persian) or LTR (English) mode, **all code blocks, inline snippets, file paths, and syntax blocks MUST always be LTR (`direction: ltr !important; text-align: left !important;`)**.
6. **Standardized API Documentation Tables:** Comprehensive, structured API endpoint documentation with HTTP method badges, parameters table (Name, Type, Required, Description, Example), JSON request/response previews, and status/error tables.
7. **Interactive Review & Comments with AI Export & HTML Embedding:** Built-in review system allowing readers/reviewers to select text or target sections, write feedback, export comments as structured JSON for AI code refinement, and embed comments directly into the downloaded HTML file for offline sharing.
8. **1-Click PDF Export with Print Stylesheet:** Header PDF export button triggering clean print layouts where navigation bars, sidebars, and control buttons are hidden, page breaks are optimized, and backgrounds are preserved.
9. **Header Version Selector & Changelog History:** Clean version dropdown (`v2.0.0`, `v1.2.0`, `v1.0.0`) in the header paired with a version history modal/drawer detailing changelogs (no bulky Git diff clutter).

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

### 4.2 Persian Orthography Rules (`persian-writing` Compliance)
1. **Font Family:** **Vazirmatn** (weights 300 to 900) via Google Fonts.
2. **Line Height:** Must be `1.8` to `1.85` for Persian text.
3. **Never Letter-Space Persian:** `letter-spacing: normal !important;` (tracking tears apart Arabic/Persian cursive connections).
4. **Half-Space (نیم‌فاصله / ZWNJ, U+200C):** Enforce on all prefixes, plurals, and compound words: `می‌شود`، `سخت‌افزاری`، `نرم‌افزاری`، `کلیدهای`، `ذخیره‌سازی`، `رمزنگاری`، `آسیب‌پذیری`.
5. **Persian Characters Only:** `ی` (U+06CC) and `ک` (U+06A9) — never Arabic `ي` or `ك`.
6. **Persian Numerals & Punctuation:** `۰ ۱ ۲ ۳ ۴ ۵ ۶ ۷ ۸ ۹` in Persian prose; Persian comma `،`؛ semicolon `؛`؛ quotes in `«گیومه»`.
7. **Ban Bureaucratic Verbs:** Replace `می‌باشد` with `است`؛ replace `می‌گردد` with `می‌شود`؛ replace `می‌نماید` با `می‌کند`. Ban `لازم به ذکر است` and `در راستای`.
8. **Ban AI Tropes:** No em dashes (`—`) in Persian sentences; ban artificial triad clichés (`سریع، آسان و امن`).

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

### Code Block Layout
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
  <pre><code class="language-javascript">// Always LTR
export async function authenticate(token) {
  return await verifyToken(token);
}</code></pre>
</div>
```

---

## 6. Standardized API Documentation Specification

When the document includes API specifications (REST, RPC, or internal SDKs), follow this **strict hierarchical structure**:

1. **API Title & Description (Top):** Purpose of the endpoint and business context.
2. **HTTP Method & URL Bar:** High-contrast method badge (`GET`, `POST`, `PUT`, `DELETE`, `PATCH`) alongside the full endpoint path.
3. **Parameters Table:**
   - Parameter Name (`نام پارامتر`)
   - Type (`نوع` — e.g. `string`, `integer`, `boolean`, `object`)
   - Placement / Required (`موقعیت / الزامی` — e.g. `Path (Required)`, `Query (Optional)`, `Body (Required)`)
   - Description (`توضیحات`)
   - Example (`مثال`)
4. **Request & Response Body JSON Samples:** Strictly LTR formatted JSON with syntax highlighting.
5. **Errors & Status Codes Table:**
   - HTTP Status Code (`کد وضعیت`)
   - Error Key / Code (`کد خطا`)
   - Description & Resolution (`توضیحات و راهکار`)

### API Section HTML Pattern
```html
<div class="api-endpoint-card">
  <!-- 1. Description -->
  <div class="api-meta">
    <h3 class="api-title">
      <span data-lang="en">Submit Remote Drawing Batch</span>
      <span data-lang="fa">ارسال دسته دستورات گرافیکی ریموت</span>
    </h3>
    <p class="api-description">
      <span data-lang="en">Ingests binary serialized RemoteCompose draw commands for hardware rendering.</span>
      <span data-lang="fa">دریافت و پردازش دسته بایت‌های باینری دستورات گرافیکی ریموت کامپوز جهت رندر بلادرنگ سخت‌افزاری.</span>
    </p>
  </div>

  <!-- 2. Method + URL -->
  <div class="api-url-bar">
    <span class="http-badge post">POST</span>
    <code class="endpoint-url">/api/v2/remote-compose/render-batch</code>
    <button class="btn-copy-sm" onclick="copyText('/api/v2/remote-compose/render-batch', this)">📋</button>
  </div>

  <!-- 3. Parameters Table -->
  <h4 class="api-subheading">
    <span data-lang="en">Parameters</span>
    <span data-lang="fa">پارامترهای ورودی</span>
  </h4>
  <div class="table-responsive">
    <table class="api-table">
      <thead>
        <tr>
          <th><span data-lang="en">Parameter</span><span data-lang="fa">نام پارامتر</span></th>
          <th><span data-lang="en">Type</span><span data-lang="fa">نوع</span></th>
          <th><span data-lang="en">Required</span><span data-lang="fa">الزامی</span></th>
          <th><span data-lang="en">Description</span><span data-lang="fa">توضیحات</span></th>
          <th><span data-lang="en">Example</span><span data-lang="fa">نمونه</span></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><code>session_token</code></td>
          <td><span class="type-tag string">string</span></td>
          <td><span class="req-tag required">Required</span></td>
          <td>
            <span data-lang="en">Cryptographic device session identifier</span>
            <span data-lang="fa">شناسه رمزشده نشست دستگاه متصل</span>
          </td>
          <td><code>"tok_sec_9941a"</code></td>
        </tr>
      </tbody>
    </table>
  </div>

  <!-- 4. JSON Request/Response -->
  <div class="json-grid">
    <div class="code-container">
      <div class="code-header">
        <span class="code-lang-badge json">JSON Request</span>
        <button class="btn-copy" onclick="copyCode(this)">📋 <span class="copy-text">Copy</span></button>
      </div>
      <pre><code class="language-json">{
  "document_id": "doc_99182",
  "canvas_width": 1080,
  "canvas_height": 1920
}</code></pre>
    </div>

    <div class="code-container">
      <div class="code-header">
        <span class="code-lang-badge json">JSON Response (200 OK)</span>
        <button class="btn-copy" onclick="copyCode(this)">📋 <span class="copy-text">Copy</span></button>
      </div>
      <pre><code class="language-json">{
  "status": "SUCCESS",
  "rendered_ops": 42,
  "render_latency_ms": 1.4
}</code></pre>
    </div>
  </div>

  <!-- 5. Errors Table -->
  <h4 class="api-subheading">
    <span data-lang="en">Error Codes & Responses</span>
    <span data-lang="fa">کدهای خطا و وضعیت</span>
  </h4>
  <div class="table-responsive">
    <table class="api-table error-table">
      <thead>
        <tr>
          <th><span data-lang="en">Status</span><span data-lang="fa">کد وضعیت</span></th>
          <th><span data-lang="en">Error Code</span><span data-lang="fa">کد خطا</span></th>
          <th><span data-lang="en">Description</span><span data-lang="fa">توضیحات خطا</span></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><span class="status-badge s400">400 Bad Request</span></td>
          <td><code>INVALID_PAYLOAD</code></td>
          <td>
            <span data-lang="en">Malformed binary envelope or unsupported schema version.</span>
            <span data-lang="fa">ساختار باینری نامعتبر یا نسخه ناشناخته شمای ریموت کامپوز.</span>
          </td>
        </tr>
        <tr>
          <td><span class="status-badge s401">401 Unauthorized</span></td>
          <td><code>EXPIRED_SESSION</code></td>
          <td>
            <span data-lang="en">Device session signature expired or revoked.</span>
            <span data-lang="fa">امضای نشست معتبر نیست یا منقضی شده است.</span>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
```

---

## 7. Interactive Review & Comments System (AI Export & HTML Embedding)

Documents generated by `doc-html` include a client-side **Review & Comments System**:
1. **Interactive Commenting:** Readers can select text to leave an inline note OR click a comment icon on any section.
2. **Export Comments as JSON:** Generates a structured JSON file formatted specifically for AI agents (specifying section title, selected text, reviewer comments, and timestamps).
3. **Embed Comments in HTML:** Allows downloading the document as a new `.html` file with the comments embedded in an internal `<script id="docEmbeddedComments" type="application/json">` tag. When emailed or shared, any recipient opens the file and immediately sees the reviewer comments!

### Embedded JSON Schema
```json
[
  {
    "id": "c_1728038912",
    "sectionId": "api-section",
    "sectionTitle": "Remote Drawing Batch API",
    "selectedText": "Cryptographic device session identifier",
    "comment": "Ensure we clarify whether this token is refreshed via WebAuthn or standard bearer token.",
    "author": "Security Reviewer",
    "createdAt": "2026-10-03T12:00:00Z"
  }
]
```

### Core Functions Required in Document JS
- `openAddCommentModal(sectionId, selectedText)`
- `saveComment(sectionId, selectedText, commentText, author)`
- `exportCommentsAsJSON()`: triggers download of `review-comments.json`.
- `embedCommentsAndDownloadHTML()`: serializes all current comments into the DOM script tag and triggers download of `<filename>-with-comments.html`.

---

## 8. 1-Click PDF Export & Print Stylesheet

Add an **Export PDF** button in the header toolbar (`window.print()`). Pair this with `@media print` rules:

```css
@media print {
  /* Hide interactive / non-content elements */
  header,
  .catalog-sidebar,
  .sidebar-backdrop,
  .btn-control,
  .btn-copy,
  .comment-drawer,
  .add-comment-btn,
  #scrollProgressBar,
  .modal-overlay {
    display: none !important;
  }

  /* Page styling */
  body {
    background: #ffffff !important;
    color: #000000 !important;
    font-size: 11pt;
  }

  .main-content {
    margin: 0 !important;
    padding: 0 !important;
    max-width: 100% !important;
    width: 100% !important;
  }

  /* Prevent awkward page cuts */
  .card,
  .api-endpoint-card,
  .code-container,
  table,
  figure {
    break-inside: avoid;
    page-break-inside: avoid;
  }

  /* Preserve colors */
  * {
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
  }
}
```

---

## 9. Header Version Selector & Version History Modal

Instead of clunky Git-diff sidebars, provide a **Header Version Dropdown** and an interactive **Version History Modal**:

```html
<!-- Version Selector in Header -->
<div class="version-selector-wrap">
  <select id="docVersionSelect" class="version-select" onchange="switchVersion(this.value)">
    <option value="2.0.0" selected>v2.0.0 (Latest)</option>
    <option value="1.2.0">v1.2.0</option>
    <option value="1.0.0">v1.0.0</option>
  </select>
  <button class="btn-icon" onclick="openVersionHistoryModal()" title="View Changelog">📜</button>
</div>

<!-- Version History Modal -->
<div id="versionHistoryModal" class="modal-overlay" onclick="closeModalOnBackdrop(event, this)">
  <div class="modal-box">
    <div class="modal-header">
      <h3>
        <span data-lang="en">Version Changelog History</span>
        <span data-lang="fa">تاریخچه نسخه‌ها و تغییرات</span>
      </h3>
      <button class="btn-close-modal" onclick="closeVersionHistoryModal()">✕</button>
    </div>
    <div class="modal-body changelog-timeline">
      <div class="changelog-entry current">
        <div class="changelog-badge">v2.0.0 · Current</div>
        <p class="changelog-date">2026-10-03</p>
        <ul class="changelog-list">
          <li>Standardized API Documentation table pattern.</li>
          <li>Strict Left-to-Right (LTR) code blocks across all languages.</li>
          <li>Integrated client-side review notes with JSON export and HTML embed.</li>
          <li>1-Click PDF Export.</li>
        </ul>
      </div>
      <!-- Older versions... -->
    </div>
  </div>
</div>
```

---

## 10. Mobile Responsiveness Best Practices

Follow these rules for flawless mobile display:

1. **Drawer Sizing:** On mobile, the sidebar drawer must have `width: min(85vw, 300px);` so it never exceeds screen bounds.
2. **Touch Targets:** All interactive buttons (`btn-control`, hamburger, close buttons) must have a touch area of at least **44x44px**.
3. **Safe Area Insets:** Support notch devices with `padding-top: env(safe-area-inset-top);` and `padding-bottom: env(safe-area-inset-bottom);`.
4. **Responsive Tables:** Wrap every table in `<div class="table-responsive">` with `overflow-x: auto; -webkit-overflow-scrolling: touch;`.
5. **No Horizontal Body Overflow:** `overflow-x: hidden;` on `body` and `html`. Code blocks handle their own horizontal scrolling.
6. **Breakpoints System:**
   - **Desktop:** `> 1024px` (Sidebar persistent rail)
   - **Tablet:** `769px - 1024px` (Sidebar off-canvas, 2-column cards)
   - **Mobile:** `<= 768px` (Sidebar off-canvas drawer, 1-column cards, compact header controls)
   - **Small Mobile:** `<= 480px` (Adjust hero title font to `clamp(1.5rem, 5vw, 2rem)`)

---

## 11. Generation Checklist

Before delivering an HTML documentation file using `doc-html`:

- [ ] **Content-Aware Modularity:** Evaluated whether API docs, diagrams, or simulators genuinely belong in this document; omitted unneeded sections.
- [ ] **Anti-Hallucination:** Every API parameter, hardware claim, and factual statement is backed by real specs or marked as "Not Supported / Nothing Found".
- [ ] **No "Fingilish" Transliteration:** Proper nouns, brands, browsers, OS, and APIs are written in standard English (`Safari`, `Chrome`, `Android`, `iOS`, `Secure Enclave`, `KeyStore`, `WebAuthn`).
- [ ] **Code Blocks Always LTR:** All `<pre>`, `<code>`, and code container headers are strictly LTR in both English and Persian modes.
- [ ] **Standard API Tables (if applicable):** HTTP method badge, URL, parameters table (Name, Type, Required, Description, Example), JSON request/response, and status/error table.
- [ ] **PDF Export Button:** Header button triggers `window.print()` with clean `@media print` styling hiding UI toolbars.
- [ ] **Review & Comments Feature:** Readers can add notes, export review comments as JSON for AI, and embed comments into downloadable HTML.
- [ ] **Header Version Selector:** Clean version dropdown + version changelog modal (no diff slider).
- [ ] **Catalog Sidebar:** Persistent on desktop, off-canvas drawer on mobile (`min(85vw, 300px)`), with active section highlighting on scroll.
- [ ] **Reading Progress:** Top horizontal progress bar + dynamic `Section X of Y` badge working properly.
- [ ] **Bilingual & RTL:** Dual `data-lang` spans with zero-reload switcher; Vazirmatn font with line-height 1.85, ZWNJ, and no bureaucratic verbs.
- [ ] **100% Mobile & Touch Responsive:** Verified on mobile (360px), tablet (768px), and desktop (1280px).
