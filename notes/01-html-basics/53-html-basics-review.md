# HTML Basics Review

<aside>
📚

**Recap sheet** for the entire **Basic HTML** module — skim this when you need a quick mental refresh before the quiz. Every section links back to the deeper chapter notes.

</aside>

## 🧱 1. What HTML Is

- **HTML** = **H**yper**T**ext **M**arkup **L**anguage — describes a page's **content & structure**.
- Browsers read HTML and render text, headings, images, links, forms.
- HTML is **structure**; CSS is **style**; JavaScript is **behavior**.

## 🧰 2. Elements, Tags & Attributes

- **Element** = opening tag + content + closing tag → `<p>Hi</p>`.
- **Void elements** have no content/closing tag → `<img>`, 
``, `<hr>`, `<meta>`, `<link>`, `<input>`.
- **Attributes** sit in the opening tag: `name="value"` (e.g. `src`, `alt`, `href`, `class`, `id`).
- **Boolean attributes** work by presence: `checked`, `disabled`, `readonly`, `required`.

## 🧱 3. The HTML Boilerplate

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Page Title</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>...</body>
</html>
```

- `<!DOCTYPE html>` → declares HTML5; must be first line.
- `<html lang>` → root element + page language.
- `<head>` → metadata; `<body>` → visible content.

## 🔤 4. UTF-8

- `<meta charset="UTF-8">` → tells the browser to use UTF-8 encoding.
- Covers every Unicode character (é, 中, ع, 😀). Place as first child of `<head>`.

## 🧩 5. HTML Fundamentals

- `<div>` = generic block container (no semantics); `<section>` = thematic group (semantic).
- **`id`** = unique label, no spaces, CSS `#name`.
- **`class`** = reusable label, multiple allowed, CSS `.name`.
- **HTML entities**: `&lt;` `&gt;` `&amp;` `&copy;` — three forms (named, decimal `&#60;`, hex `&#x3C;`).
- **`<script>`** loads JavaScript: prefer external file via `src`.

## 🔍 6. HTML & SEO

- `<meta name="description" content="...">` → snippet in search results.
- **Open Graph** tags control social previews: `og:title`, `og:type`, `og:image`, `og:url`.
- Image recommendation: 1200×630 px.

## 🎥 7. Audio & Video

- `<audio>` (MP3/WAV/OGG), `<video>` (MP4/OGG/WEBM).
- Boolean attrs: `controls`, `loop`, `muted`, `autoplay` (usually needs `muted`).
- Video-only: `poster`, `width`, `height`.
- Use `<source>` children for multi-format fallback.

## 🖼️ 8. Images & SVGs

- **Optimize**: match rendered size, use WEBP/AVIF, compress.
- **Lossy** (JPG, WEBP lossy) discards data per save; **lossless** (PNG) does not.
- **Image licenses**: default is *all rights reserved*; **CC0** = public domain; use Pixabay/Unsplash.
- **SVG** = vector graphic, stores paths as XML — scales infinitely, editable with CSS.

## 📺 9. iframe

- `<iframe>` embeds external content — videos, maps, other pages.
- Use `src` for URL, `srcdoc` for inline HTML.
- Always add `title` for accessibility, set `allow` for features.
- **Replaced elements** (`img`, `iframe`, `video`, `audio`) load content from outside CSS.

## 🔗 10. Links

- `<a href="...">` + **`target`** controls where it opens: `_self` (default), `_blank` (new tab), `_parent`, `_top`.
- For `_blank`, add `rel="noopener noreferrer"`.
- **Absolute path** starts from root; **relative path** is from current file. `./` = here, `../` = up one.
- **Link states (LVHFA)**: `:link`, `:visited`, `:hover`, `:focus`, `:active` — write in that order.

## 🧠 Quick Self-Check

**1. Which attribute is required on an `<img>` element?**

- [ ]  `alt`
- [x]  **`src`**
- [ ]  `title`
- [ ]  `width`

**2. Where does `<meta charset="UTF-8">` belong?**

- [ ]  Inside `<body>`
- [x]  **As the first child of `<head>`**
- [ ]  Outside `<html>`
- [ ]  Anywhere on the page

**3. Which order is correct for link-state CSS rules?**

- [ ]  hover, link, visited, active
- [ ]  visited, link, active, hover
- [x]  **link, visited, hover, active** (LVHA, with `:focus` between hover and active)
- [ ]  active, hover, visited, link

## ✅ Things to remember

- Pick **semantic elements** over `<div>` whenever the meaning fits.
- Use **lowercase tags**, **double-quote attributes**, and **close every non-void tag**.
- `<!DOCTYPE html>` + `<html lang>` + `<meta charset>` + `<meta viewport>` + `<title>` are the boilerplate non-negotiables.
- For any media, optimize **size → format → compression**.
- Use **`href="tel:"`** and **`href="mailto:"`** for clickable phone/email links.

---

<aside>
➡️

Next up: **Semantic HTML** chapters — pick the right element for the right meaning.

</aside>
