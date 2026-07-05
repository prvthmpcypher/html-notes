# <code> & <pre> — Representing Computer Code in HTML

<aside>
✨

**Big idea:** **`<code>`** marks up **inline code snippets** — a single-line bit of code inside flowing text. **`<pre>`** preserves **whitespace and line breaks** so multi-line code displays exactly as written. The classic combo for code blocks: **`<pre><code>...</code></pre>`**.

</aside>

## 💻 The `<code>` Element — Inline Code

- A **semantic** element for **short code snippets** inside text.
- Default styling: **monospaced font** (e.g., Courier, Menlo).
- Best for **single-line** examples in technical articles, documentation, README files, and tutorials.

```html
<p>
  To set the text color to blue in CSS, use the following code:
  <code>color: blue;</code>
</p>
```

The browser knows the wrapped text is **code**, not regular prose. Screen readers and search engines benefit, and you get a nice monospace font for free.

## 📋 The `<pre>` Element — Preformatted Text

- A **block-level** element that preserves **whitespace and line breaks exactly as written**.
- Normally, HTML collapses runs of spaces and ignores extra newlines — `<pre>` overrides that.
- Renders in a **monospaced font** by default.

```html
<pre>
Line 1
    Indented line 2
  Indented line 3
</pre>
```

All the spaces and line breaks above show up **exactly** in the browser.

## 🧩 The Classic Combo — `<pre><code>` for Code Blocks

For **multi-line code samples**, wrap a `<code>` inside a `<pre>`:

```html
<pre>
  <code>
    body {
      color: red;
    }
  </code>
</pre>
```

Why both?

- **`<pre>`** → preserves the formatting (indentation, line breaks).
- **`<code>`** → keeps the semantic meaning ("this content is code").

<aside>
⚠️

The browser displays **whatever spacing is in your HTML source**. Indenting the code inside `<pre>` adds extra leading spaces in the output. Trim them if you don't want them showing.

</aside>

## ⚖️ `<code>` vs `<pre>` at a Glance

| Aspect | `<code>` | `<pre>` |
| --- | --- | --- |
| Layout | **Inline** | **Block** |
| Preserves whitespace? | No (collapses like normal HTML) | **Yes** — exact spacing & newlines |
| Default font | Monospace | Monospace |
| Semantic meaning | "This is code" | "Preserve formatting" |
| Used for | Single-line snippets in text | Multi-line text where whitespace matters |

## 📦 When to Use Which

- **Single-line, inline** → use `<code>` alone.
- **Multi-line code block** → wrap a `<code>` in a `<pre>`.
- **Preformatted non-code text** (ASCII art, poetry with specific spacing) → use `<pre>` without `<code>`.

## 🧩 Real-World Examples

```html
<!-- Inline code -->
<p>
  Install dependencies with <code>npm install</code> before running the app.
</p>

<!-- Variable name in text -->
<p>
  Set <code>process.env.NODE_ENV</code> to <code>"production"</code> for builds.
</p>

<!-- Multi-line block: CSS rule -->
<pre><code>.btn {
  padding: 0.5rem 1rem;
  border-radius: 4px;
}</code></pre>

<!-- Multi-line block: JavaScript -->
<pre><code>function greet(name) {
  return `Hello, ${name}!`;
}</code></pre>
```

## ⚠️ Common Mistakes

- ❌ Putting multi-line code inside just **`<code>`** without `<pre>` — the browser will collapse all whitespace.
- ❌ Indenting code inside `<pre>` for source readability — it shows up as extra leading spaces in the output.
- ❌ Using `<code>` only for **font styling** — if it's not actually code, reach for CSS instead.
- ❌ Forgetting to **escape angle brackets** (`<`, `>`) in code samples — use `&lt;` and `&gt;` so the browser doesn't try to render them as tags.

## 🔗 Bonus — Related Elements

- **`<kbd>`** — keyboard input, e.g. <kbd>Ctrl</kbd> + <kbd>C</kbd>.
- **`<samp>`** — sample output from a program.
- **`<var>`** — a variable in a mathematical or programming expression.

These pair nicely with `<code>` for richer technical content.

## 🧠 Quick Self-Check

**1. What is the `code` element used for?**

- [ ]  It's used to create hyperlinks to other web pages.
- [ ]  It's used to format text with bold or italic styles.
- [x]  **It's used to represent short snippets of code inside text.**
- [ ]  It's used to embed images and multimedia files.

**2. What is the preformatted text (`pre`) element used for?**

- [ ]  It's used to apply CSS styles to text.
- [ ]  It's used to create tables and structured layouts.
- [x]  **It's used to represent preformatted text.**
- [ ]  It's used to insert hyperlinks and email addresses.

**3. What is the default styling for the `code` element?**

- [x]  **Monospaced font.**
- [ ]  Italic text with a colored background.
- [ ]  Bold text with a larger font size.
- [ ]  Underlined text with a fixed-width font.

## ✅ Key Takeaways

- **`<code>`** = inline, short code snippets — monospace font by default.
- **`<pre>`** = preformatted block, preserves whitespace and newlines exactly.
- For multi-line code blocks, use **`<pre><code>...</code></pre>`** — layout from `<pre>`, meaning from `<code>`.
- Watch indentation inside `<pre>` — it shows up exactly as written.
- Escape `<` and `>` with `&lt;` and `&gt;` when displaying HTML inside code blocks.
- Related semantic helpers: **`<kbd>`**, **`<samp>`**, **`<var>`**.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
