# What Are Some Common Accessibility Auditing Tools to Use?

<aside>
✨

**Big idea:** Accessibility auditing tools **scan your pages for common a11y violations** — missing alt text, low contrast, broken keyboard focus, invalid ARIA, and so on. They catch the **easy wins automatically** but can never replace **manual testing with a keyboard, screen reader, and real users**.

</aside>

## 🛠️ Why Audit?

- Automated tools catch **~30–50% of accessibility issues**.
- They're great for **regression testing**, CI/CD pipelines, and quick spot checks.
- They **cannot** judge whether `alt` text is meaningful, whether headings make sense in context, or whether a focus order is logical — that's manual work.

## 🧰 Popular Auditing Tools

### Browser-extension scanners

| Tool | What it does |
| --- | --- |
| **axe DevTools** (Deque) | Industry-standard scanner; precise, low false-positive rate. Free + paid versions. |
| **WAVE** (WebAIM) | Visualizes issues directly on the page with icons. |
| **Accessibility Insights** (Microsoft) | Combines automated scans with guided manual tests (FastPass). |
| **SiteImprove** | Enterprise scanning across many pages. |

### Built into your browser

- **Lighthouse** (Chrome DevTools → Lighthouse tab) → automated a11y audit + score.
- **Chrome DevTools → Issues panel** → real-time warnings as you browse.
- **Firefox Accessibility Inspector** → shows the accessibility tree, contrast checks, simulates color-blindness.

### Command-line / CI tools

- **`@axe-core/cli`** — run axe from the terminal.
- **`pa11y`** — script-friendly audit runner.
- **`jest-axe`** — assertions inside unit tests.
- **`cypress-axe`** / **`playwright-axe`** — bake a11y checks into end-to-end tests.

### Targeted checkers

- **WebAIM Contrast Checker** — verify text-vs-background color contrast.
- **HTML Validator (W3C)** — bad markup often causes a11y bugs; valid HTML is a strong foundation.
- **Color Oracle** — desktop tool that simulates color-blindness.

## 🧪 What Tools Catch Well

- Missing **`alt`** attributes
- **Empty links/buttons** (no accessible name)
- **Low color contrast**
- **Invalid or duplicate ARIA**
- **Missing form labels**
- **Skipped heading levels**
- **Non-unique `id`** values
- Missing `lang` on `<html>`
- Inputs without associated `<label>`

## 🧤 What Tools Can't Catch

- Is the `alt` text **meaningful** or just "image"?
- Does the **focus order** match the visual order?
- Does a custom widget behave correctly when used with a screen reader?
- Are videos **really** captioned and audio-described?
- Does the page make sense with CSS disabled?
- Do animations cause discomfort (without `prefers-reduced-motion`)?

Manual testing is non-negotiable.

## 🧩 A Practical Audit Workflow

1. **Run axe or Lighthouse** for the obvious issues.
2. **Tab through the page** — can you reach every interactive element? In a logical order? With a visible focus ring?
3. **Turn on a screen reader** for 60 seconds and listen to your homepage.
4. **Zoom to 400%** — does anything break?
5. **Disable CSS** — does the raw HTML still make sense?
6. **Test with `prefers-reduced-motion`** turned on.
7. **Get real users involved** when possible — nothing beats lived experience.

## 🧠 Quick Self-Check

**1. Roughly what percentage of accessibility issues do automated tools catch?**

- [ ]  5–10%
- [x]  **About 30–50%**
- [ ]  90%
- [ ]  100%

**2. Which is a popular browser-extension auditor by Deque?**

- [x]  **axe DevTools**
- [ ]  WAVE
- [ ]  Lighthouse
- [ ]  WebAIM

**3. Which check requires manual testing (an automated tool can't do it)?**

- [ ]  Detecting missing `alt` attributes
- [ ]  Detecting low color contrast
- [x]  **Judging whether `alt` text is meaningful in context**
- [ ]  Detecting duplicate `id`s

## ✅ Key Takeaways

- Automated tools (**axe**, **WAVE**, **Lighthouse**, **Accessibility Insights**) catch the easy 30–50%.
- They're great in **CI/CD** (`jest-axe`, `cypress-axe`, `playwright-axe`).
- They **don't** judge meaning, context, focus order, or screen-reader experience.
- Always supplement with **manual keyboard testing**, **screen-reader use**, **400% zoom**, and ideally **real-user testing**.
- Valid HTML + semantic markup gets you most of the way there before you even run a scanner.

---

<aside>
➡️

**Next chapter →** How proper heading structure affects accessibility.

</aside>
