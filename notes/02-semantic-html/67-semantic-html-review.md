# Semantic HTML Review

<aside>
📚

**Recap sheet** for the entire **Semantic HTML** module. Use this as your before-the-quiz cheat sheet; deeper write-ups live in each chapter.

</aside>

## 🎯 1. Why Semantic HTML Matters

- **Semantics** = the **meaning** of an element.
- Benefits: **accessibility**, **SEO**, **developer experience**.
- Non-semantic: `<div>`, `<span>` — use only as styling/scripting hooks.

## 🔢 2. Heading Hierarchy

- Six levels: `<h1>` (most important) → `<h6>`.
- **One `<h1>`** per page; multiple `<h2>`s for sections.
- **Never skip levels** going down (`<h1>` → `<h3>` is a bug).
- Pick by **meaning**, not size — style with CSS.

## ⚰️ 3. Presentational vs Semantic

- **Presentational HTML** (`<font>`, `<center>`, `<big>`) is **deprecated**.
- Use semantic elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`) + CSS for style.

## 📦 4. Generic Containers

- `<div>` = block, no semantics; `<section>` = thematic block with a heading.
- Reach for the most meaningful element first; fall back to `<div>` only when nothing better fits.

## ✏️ 5. Text Emphasis & Importance

| Look | Different/set-apart | Important/emphasized |
| --- | --- | --- |
| Italic | `<i>` (idiomatic / foreign / term) | `<em>` (changes sentence meaning) |
| Bold | `<b>` (bring attention to) | `<strong>` (urgent / critical) |

For visual-only italic/bold, use **CSS** (`font-style`, `font-weight`).

## 🔣 6. Abbreviations — `<abbr>`

- Marks abbreviations, acronyms, initialisms.
- Add `title="Full form"` for a hover tooltip.
- `<acronym>` is deprecated — use `<abbr>` for everything.

## 📖 7. Description Lists

- `<dl>` (list) + `<dt>` (term) + `<dd>` (description).
- Perfect for glossaries, FAQs, specs, recipes, metadata.
- One `<dt>` can have multiple `<dd>`s; multiple `<dt>`s can share a `<dd>`.

## 💬 8. Quotations — `<blockquote>`, `<q>`, `<cite>`

- `<blockquote>` = long quote (block); `<q>` = short inline quote (browser auto-adds quotation marks).
- Both accept the **`cite` attribute** with a URL.
- The **`<cite>` element** marks the **title** of a referenced work — different from the `cite` attribute.

## 📧 9. Contact Info — `<address>`

- For author/business contact info inside a section. Not for any postal address inside text.
- Pair with `href="tel:+..."` and `href="mailto:..."` for clickable phone/email.

## ⏰ 10. Dates & Times — `<time>`

- Visible text is human-readable; **`datetime`** attribute is **ISO 8601** for machines.
- Forms: `YYYY`, `YYYY-MM-DD`, `HH:MM`, `YYYY-MM-DDTHH:MM:SSZ`, `PT45M`.

## 🔣 11. Math & Chemistry — `<sup>`, `<sub>`

- `<sup>` = exponents, ordinals, footnote markers (E = mc², 1ˢᵗ).
- `<sub>` = chemical formulas, variable subscripts (H₂O, x₁).

## 💻 12. Code — `<code>` & `<pre>`

- `<code>` = inline code (monospace, no whitespace preserved).
- `<pre>` = preformatted block (preserves spaces & newlines).
- For multi-line: `<pre><code>...</code></pre>`.
- Related: `<kbd>` (keyboard input), `<samp>` (program output), `<var>` (variable).

## 📝 13. Annotations — `<u>`, `<s>`, `<ruby>`

- `<u>` = non-textual annotation (e.g. spelling errors).
- `<s>` = no longer accurate (cancelled, discontinued). Don't use for tracked edits — use `<del>`/`<ins>`.
- `<ruby>` + `<rt>` + `<rp>` = pronunciation annotations (East Asian typography).

## 🧠 Quick Self-Check

**1. Which element has NO semantic meaning?**

- [ ]  `nav`
- [x]  **`div`**
- [ ]  `article`
- [ ]  `footer`

**2. Which element marks text whose absence would change the sentence's meaning?**

- [ ]  `<i>`
- [ ]  `<b>`
- [x]  **`<em>`**
- [ ]  `<u>`

**3. What does the `cite` attribute on `<blockquote>` hold?**

- [ ]  The title of a referenced work
- [ ]  An ID for CSS targeting
- [x]  **A URL pointing to the source of the quote**
- [ ]  The author's name

## ✅ Things to remember

- **HTML for meaning. CSS for style.** Never reach for a tag because of how it looks.
- The semantic landmarks `<header>`, `<nav>`, `<main>`, `<footer>`, `<aside>` give screen readers and search engines a clear page outline.
- The italic pair: `<i>` (set apart) vs `<em>` (emphasis). The bold pair: `<b>` (attention) vs `<strong>` (importance).
- Use **`<dl>`** for any key→value content.
- Use **`<time datetime="...">`** so machines can read dates accurately.

---

<aside>
➡️

Next up: **HTML Forms & Tables** — how to collect input and present tabular data accessibly.

</aside>
