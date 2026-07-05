# <abbr> — Abbreviations, Acronyms & Initialisms in HTML

<aside>
✨

**Big idea:** **`<abbr>`** marks up an **abbreviation, acronym, or initialism** so browsers, screen readers, and search engines know it's a shortened form. Add a **`title`** attribute with the **expanded version** and users get a tooltip on hover.

</aside>

## 🔤 What Counts as an Abbreviation?

An **abbreviation** is any shortened form of a word or phrase — like **"Dr"** for *Doctor*.

Two common subtypes:

| Type | Definition | Examples |
| --- | --- | --- |
| **Acronym** | Formed from initial letters and **pronounced as a word** | GUI ("goo-ee"), NASA, LASER, SCUBA |
| **Initialism** | Formed from initial letters and **pronounced letter-by-letter** | HTML, CSS, FBI, URL, API |

Both are abbreviations. The difference is **how you say them out loud**.

## 🏷️ The `<abbr>` Element

Use `<abbr>` to mark up any abbreviation that benefits from extra context.

```html
<p><abbr>HTML</abbr> is the foundation of the web.</p>
```

- By itself, `<abbr>` doesn't change the look of the text — it's a **semantic hint**.
- Screen readers may announce abbreviations differently when they're marked up.
- Search engines get extra context about technical terms on your page.

## 🏷️ Add a `title` Attribute for the Full Form

The **`title`** attribute is **optional but recommended** — it holds the **expanded form** of the abbreviation.

```html
<p><abbr title="HyperText Markup Language">HTML</abbr> is the foundation of the web.</p>
```

- On hover, the browser shows a **tooltip** with the expanded form.
- Browsers may also style the element with a **dotted underline** or **small caps**.
- The text must be a **human-readable expansion**, not a URL or code.

<aside>
♿

Tooltips from `title` aren't available to keyboard or touch-only users. For critical context, **spell out the full term in the surrounding text** at least once on the page.

</aside>

## ✅ Best Practices

- **Spell it out the first time.** When introducing an abbreviation, mention the full form at least once — then use the abbreviation throughout.
- Use `<abbr>` for abbreviations that **might be unclear** to your audience.
- Pair with `title="..."` whenever the expansion would help — especially for jargon.
- Don't over-mark common abbreviations (like "USA" or "OK") that everyone already knows.
- Keep your `title` text **human-readable** — just the expansion, no extra commentary.

## 🧩 Real-World Examples

```html
<!-- Initialism with expansion -->
<p>
  Many APIs return data as
  <abbr title="JavaScript Object Notation">JSON</abbr>.
</p>

<!-- Acronym -->
<p>
  <abbr title="Self-Contained Underwater Breathing Apparatus">SCUBA</abbr>
  diving has its own jargon.
</p>

<!-- Domain-specific term -->
<p>
  Make sure your
  <abbr title="Hypertext Transfer Protocol Secure">HTTPS</abbr>
  certificate is valid.
</p>

<!-- Abbreviation without an expansion (still semantic) -->
<p>The package will arrive on <abbr>Wed</abbr>.</p>
```

## ⚠️ Common Mistakes

- ❌ Using `<abbr>` for **every** abbreviation — too much noise.
- ❌ Adding overly long or salesy `title` text — keep it to the plain expansion.
- ❌ Relying on hover tooltips alone for critical information.
- ❌ Using `<acronym>` — it's **deprecated**. `<abbr>` covers both acronyms and initialisms.

## 🧠 Quick Self-Check

**1. Which HTML element is used to indicate an abbreviation or acronym?**

- [x]  **`abbr`**
- [ ]  `acronym`
- [ ]  `abbrev`
- [ ]  `acron`

**2. What is the primary purpose of the `abbr` element?**

- [ ]  To style text as an abbreviation.
- [x]  **To indicate an abbreviation or acronym and provide additional information.**
- [ ]  To shorten the content of a webpage.
- [ ]  To improve search engine rankings.

**3. What attribute can be used within the `abbr` element to provide the full form of an acronym or abbreviation?**

- [ ]  `explain`
- [ ]  `description`
- [x]  **`title`**
- [ ]  `fullform`

## ✅ Key Takeaways

- `<abbr>` marks up an **abbreviation**, **acronym**, or **initialism** semantically.
- **Acronyms** = pronounced as a word (NASA). **Initialisms** = pronounced letter-by-letter (HTML).
- Add a **`title="..."`** with the full expansion so users get a hover tooltip and assistive tech gets context.
- The old `<acronym>` tag is **deprecated** — use `<abbr>` for everything.
- Spell out the expansion at least once in text — don't rely on tooltips alone for critical info.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
