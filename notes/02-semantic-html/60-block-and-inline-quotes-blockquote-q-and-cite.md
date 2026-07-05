# Block & Inline Quotes — <blockquote>, <q> & <cite>

<aside>
✨

**Big idea:** HTML has dedicated elements for quoting other sources. Use **`<blockquote>`** for **long, standalone quotes**, **`<q>`** for **short inline quotes**, and **`<cite>`** to **name the work** being quoted. Both quote elements accept a **`cite` attribute** pointing to the source URL.

</aside>

## 💬 What Are HTML Quote Elements?

Three elements work together to mark up quoted content semantically:

| Element | Purpose |
| --- | --- |
| `<blockquote>` | **Extended quotations** — a standalone block of quoted content |
| `<q>` | **Short inline quotations** — a few quoted words inside a sentence |
| `<cite>` | The **title of a creative work** being referenced (book, article, song, film, paper, site…) |

All three are **semantic** — they help screen readers, search engines, and humans understand what's quoted from where.

## 🧱 `<blockquote>` — Extended Quotations

- For long quotes pulled from another source.
- Rendered slightly **indented** by default.
- Accepts a **`cite` attribute** with a URL pointing to the source.

```html
<blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
  "Can you imagine what it would be like to be a successful developer?
  To have built software systems that people rely upon?"
</blockquote>
```

<aside>
💡

The **`cite` attribute** is invisible to users but exposed to screen readers and search engines. Add it whenever you have a source URL.

</aside>

### Multi-paragraph block quote

Wrap each paragraph in `<p>` to keep them grouped under one quote:

```html
<blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
  <p>Build your projects. Show them to your friends. Build projects for your friends.</p>
  <p>Build your network. Help the people you meet along the way. What goes around comes around.</p>
  <p>It is not too late. Life is long.</p>
  <p>You will look back on this moment years from now and be glad you made a move.</p>
</blockquote>
```

All four paragraphs sit inside **one** `<blockquote>` — they belong to the same quotation.

## 📖 `<cite>` — Naming the Work

- The `cite` **element** is different from the `cite` **attribute**.
- `<cite>` marks up the **title** of a creative work being referenced.
- Common targets: books, articles, songs, films, websites, research papers.
- Browsers usually render `<cite>` in italics by default.

```html
<div>
  <blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
    Can you imagine what it would be like to be a successful developer?
    To have built software systems that people rely upon?
  </blockquote>
  <p>—Quincy Larson, <cite>How to Learn to Code and Get a Developer Job [Full Book]</cite>.</p>
</div>
```

Now the author and book title are **visible** to readers too.

## 📝 `<q>` — Inline Quotations

- For **short** quotes that live inside a surrounding paragraph.
- Most modern browsers **add quotation marks automatically** — don't write them yourself.
- Also supports the **`cite` attribute** for source URLs.

```html
<p>
  As Quincy Larson said,
  <q cite="https://www.freecodecamp.org/news/learn-to-code-book/">
    Momentum is everything.
  </q>
</p>
```

The browser typically renders this as: *As Quincy Larson said, "Momentum is everything."*

## ⚖️ `<blockquote>` vs `<q>`

| Aspect | `<blockquote>` | `<q>` |
| --- | --- | --- |
| Length | Long / extended | Short / a few words |
| Layout | **Block** — standalone, indented | **Inline** — part of a sentence |
| Quotation marks | Write them yourself if you want them | Browser adds them automatically |
| Multi-paragraph? | Yes — wrap each in `<p>` | No — single inline span |
| Supports `cite` attribute? | Yes | Yes |

## 🔗 `cite` Attribute vs `<cite>` Element

Easy to mix these up:

|  | **`cite` attribute** | **`<cite>` element** |
| --- | --- | --- |
| Where it lives | On `<blockquote>` / `<q>` | Anywhere a phrase needs a title |
| What it holds | A **URL** to the source | The **title** of a work |
| Visible to users? | No | Yes (usually italic) |
| Audience | Screen readers, search engines | Readers |

## 🧩 A Full Example, All Three Together

```html
<figure>
  <blockquote cite="https://example.com/article">
    <p>The best time to plant a tree was 20 years ago.
    The second best time is now.</p>
  </blockquote>
  <figcaption>—Chinese proverb, quoted in <cite>Wisdom of the Ages</cite></figcaption>
</figure>
```

- `<blockquote>` holds the quote and links the source URL.
- `<figcaption>` attributes it visually.
- `<cite>` names the referenced work.

## 🧠 Quick Self-Check

**1. Which HTML element is used for displaying extended quotations from other sources?**

- [ ]  `q`
- [x]  **`blockquote`**
- [ ]  `cite`
- [ ]  `p`

**2. What is the purpose of the `cite` element in HTML?**

- [ ]  To display inline quotations.
- [ ]  To specify the source URL of a quotation.
- [x]  **To mark up the title of a referenced creative work.**
- [ ]  To display extended quotations.

**3. Which HTML attribute is used to specify the source of a quotation in a block or inline quotation element?**

- [ ]  `href`
- [ ]  `src`
- [ ]  `title`
- [x]  **`cite`**

## ✅ Key Takeaways

- **`<blockquote>`** → long, standalone quotations. Wrap multi-paragraph content in `<p>` children.
- **`<q>`** → short inline quotes; browsers add quotation marks automatically.
- Both accept a **`cite` attribute** — the URL of the source (invisible to users, useful to bots & assistive tech).
- **`<cite>` element** — marks up the **title** of a creative work (book, article, song, film…).
- Don't confuse the `cite` **attribute** (URL) with the `<cite>` **element** (title of work).

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
