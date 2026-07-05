# HTML Basics — What Is HTML, the Page Skeleton & Element Anatomy

<aside>
🌐

**Big idea:** **HTML** is the **markup language** that describes the **content** and **structure** of every webpage. The browser reads HTML and renders text, headings, images, links, and forms — it's the **skeleton** that everything else (CSS, JavaScript) hangs onto.

</aside>

## 🌐 What Is HTML?

- **HTML** = **H**yper**T**ext **M**arkup **L**anguage.
- It's a **markup language** (not a programming language) used to describe the *content* and *structure* of a web page.
- The browser reads HTML and renders it into what you actually see — text, headings, images, links, forms, etc.

<aside>
💡

Think of HTML as the **skeleton** of a webpage. CSS is the *skin & clothes*, JavaScript is the *muscles & nervous system*.

</aside>

## 🧱 The Basic Page Skeleton

Every HTML document follows this structure:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>My First Page</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
    <p>This is my first webpage.</p>
  </body>
</html>
```

| Part | Role |
| --- | --- |
| `<!DOCTYPE html>` | Tells the browser "this is HTML5" |
| `<html>` | Root element — wraps the whole document |
| `<head>` | Metadata (title, charset, links to CSS) — *not* shown on the page |
| `<body>` | Visible content — what the user actually sees |

## 🔤 Headings — `h1` to `h6`

- HTML has **6 levels** of headings, from most important (`h1`) to least (`h6`).
- Use **one `h1` per page** (usually the page title).
- Use the rest in *logical hierarchy* — don't skip levels just for styling.

```html
<h1>Page Title</h1>
<h2>Section</h2>
<h3>Sub-section</h3>
<h4>Smaller sub-section</h4>
<h5>Even smaller</h5>
<h6>Smallest</h6>
```

<aside>
⚠️

Don't pick a heading just because it *looks* the right size — that's CSS's job. Pick based on **meaning & hierarchy**.

</aside>

## 📝 Paragraphs & Plain Text

- `<p>` wraps a block of text — a paragraph.
- Browsers automatically add space above and below paragraphs.

```html
<p>HTML is the foundation of every webpage on the internet.</p>
<p>Each paragraph sits on its own line by default.</p>
```

## 🧰 Anatomy of an HTML Element

Most elements have **three parts**:

```html
<p>I am a paragraph.</p>
```

- **Opening tag** → `<p>`
- **Content** → `I am a paragraph.`
- **Closing tag** → `</p>` (note the **forward slash** `/`)

Tags always sit between `<` and `>` (angle brackets). The tag name (`p`, `h1`, `img`...) goes in between.

<aside>
💡

HTML tag names are **case-insensitive** — `<P>` works — but the convention is **lowercase**.

</aside>

## 🧩 Common Tags at a Glance

| Tag | Purpose |
| --- | --- |
| `<h1>` – `<h6>` | Headings |
| `<p>` | Paragraph |
| `<a>` | Anchor (link) |
| `<img>` | Image (void element) |
| `<ul>` / `<ol>` | Unordered / Ordered list |
| `<li>` | List item |
| `<div>` | Generic block container |
| `<span>` | Generic inline container |
| 
`` | Line break (void) |
| `<hr>` | Horizontal rule (void) |

## 🪆 Nesting Elements

Elements can contain other elements — that's how structure is built.

```html
<section>
  <h2>About Me</h2>
  <p>I'm learning <strong>web development</strong>.</p>
</section>
```

- Always **close tags in the reverse order** they were opened (think *first opened, last closed*).
- Bad nesting can break the layout or how assistive tech reads your page.

## ✅ Key Takeaways

- HTML defines **content + structure**, not styling or behavior.
- Every page has a `<!DOCTYPE html>` + `<html>` + `<head>` + `<body>`.
- Use **one `h1`** per page; keep heading levels in **logical order**.
- Most elements have an **opening + closing** tag wrapping content.
- Tag names are **lowercase by convention**, even though HTML is case-insensitive.
- Nest tags properly — open-close them like brackets.

---

<aside>
➡️

**Next chapter →** *Dig deeper into how tags & attributes actually work — opening vs closing tags, void elements like **`<img>`**, and how **`src`** / **`alt`** behave.* (Link will be added when chapter 2 is created.)

</aside>
