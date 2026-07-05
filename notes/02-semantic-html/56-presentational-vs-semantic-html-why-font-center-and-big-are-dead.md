# Presentational vs Semantic HTML — Why <font>, <center> & <big> Are Dead

<aside>
✨

**Big idea:** **Presentational HTML** (`<font>`, `<center>`, `<big>`…) describes how content *looks*. **Semantic HTML** (`<header>`, `<nav>`, `<section>`…) describes what content *is*. The old presentational tags are **deprecated** — use semantic elements for structure and let **CSS** handle appearance.

</aside>

## 📜 Presentational HTML — Old-School Appearance Tags

- **Focuses on the appearance and style** of content.
- Used heavily in early HTML — things like `<center>`, `<big>`, `<font>`.
- **Deprecated** today: outdated, accessibility-hostile, and harder to maintain.
- They mix **what content is** with **how it looks** — violating separation of concerns.

### ⚰️ The Deprecated Trio

#### `<font>`

Set font size and color directly in HTML.

```html
<font size="5" color="blue">This text is blue and large.</font>
```

- `size` ranged from **1–7** (default `3`).
- Both color and size **should now be set with CSS** — don't use `<font>`.

#### `<center>`

Centers content horizontally inside its container.

```html
<center>
  This text is centered.
  <p>HTML is awesome.</p>
</center>
```

- Replace with **CSS** (`text-align: center;`, flexbox, or grid).

#### `<big>`

Makes the enclosed text one level bigger than surrounding text.

```html
<p>
  This text has a normal font size.
  <big>This text is larger.</big>
  Some other text.
</p>
```

- Replace with CSS (`font-size`).

<aside>
⚠️

These tags **still render** in modern browsers, but they're **deprecated**. Don't reach for them — they hurt accessibility, SEO, and maintainability.

</aside>

## 🎯 Semantic HTML — The Modern Way

- **Describes the content** of each element.
- **Easier to read, understand, and maintain.**
- **Helps search engines** parse what your page is about.
- **Critical for accessibility** — screen readers rely on semantic landmarks.

### Common semantic elements

| Element | What it represents |
| --- | --- |
| `<header>` | Header of a document or section |
| `<nav>` | A section with navigation links |
| `<main>` | The main, unique content of the page |
| `<section>` | A group of related content (usually with a heading) |
| `<article>` | Self-contained content (blog post, news article) |
| `<aside>` | Tangential content (sidebars, callouts) |
| `<footer>` | Footer of a document or section |
| `<figure>` / `<figcaption>` | Illustrations, diagrams, code samples with a caption |

### Example — a header with navigation

```html
<header>
  <nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Products</a>
    <a href="#">Contact</a>
  </nav>
</header>
```

The **purpose of each element is obvious** from the markup — no class-name hunting required.

## ⚖️ Presentational vs Semantic at a Glance

| Aspect | Presentational HTML | Semantic HTML |
| --- | --- | --- |
| Focus | **Appearance** | **Meaning / structure** |
| Examples | `<font>`, `<center>`, `<big>` | `<header>`, `<nav>`, `<article>`, `<section>` |
| Status | **Deprecated** | Recommended |
| Accessibility | Poor | Strong |
| SEO | Weak | Strong |
| Maintainability | Hard — styling mixed with markup | Easy — styling lives in CSS |

## 🔄 Modernize Your Markup — Quick Wins

| ❌ Old (presentational) | ✅ Modern (semantic + CSS) |
| --- | --- |
| `<font color="red">!</font>` | `<span style="color:red">!</span>` (or a class) |
| `<center>...</center>` | CSS: `text-align: center;` / flex / grid |
| `<big>...</big>` | CSS: `font-size: 1.25rem;` |
| Navigation in `<div class="nav">` | `<nav>...</nav>` |
| Page header in `<div class="top">` | `<header>...</header>` |

## 🧠 Quick Self-Check

**1. Which of the following best describes the difference between presentational and semantic HTML?**

- [ ]  Presentational HTML focuses on content structure, while semantic HTML focuses on appearance.
- [x]  **Semantic HTML focuses on content structure, while presentational HTML focuses on appearance.**
- [ ]  There is no difference between presentational and semantic HTML.
- [ ]  Both focus on style, but presentational HTML is more modern.

**2. Which of the following is an example of presentational HTML?**

- [ ]  Using the `header` element to define a header.
- [ ]  Using the `nav` element to define a navigation section.
- [ ]  Using the `article` element to define independent content.
- [x]  **Using the `center` element to center the content.**

**3. Which of the following is an example of semantic HTML?**

- [ ]  Using `<font color="red">` to make text red.
- [ ]  Using the `center` element to center the content.
- [x]  **Using the `nav` element to represent a navigation section.**
- [ ]  Using the `big` element to make text bigger.

## ✅ Key Takeaways

- **Presentational HTML** describes *appearance* — `<font>`, `<center>`, `<big>` are all **deprecated**.
- **Semantic HTML** describes *meaning* — `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, etc.
- Modern rule: **HTML for structure, CSS for style.**
- Semantic markup improves **accessibility**, **SEO**, **maintainability**, and **collaboration**.
- If you're tempted to reach for an old presentational tag, ask: *"What does this content mean?"* — then pick a semantic element and style it with CSS.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
