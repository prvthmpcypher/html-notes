# Replaced Elements — When HTML Content Comes From Outside CSS

<aside>
✨

**Big idea:** A **replaced element** is an HTML element whose **content is loaded from an external resource** — not from your HTML or CSS. Think `<img>`, `<iframe>`, `<video>`, `<embed>`. You can style their **position and layout**, but you can't reach inside and restyle their actual content.

</aside>

## 🔄 What Is a Replaced Element?

- A **replaced element** is an element whose **content is determined by an external resource** rather than by your HTML/CSS.
- The browser **replaces** the element's box with whatever the external object is — an image, an embedded site, a video, etc.
- CSS can style the **container** (position, size, filters, borders), but **cannot modify the content** that fills it.

## 🖼️ Example 1 — `<img>`

```html
<img src="example-img-url" alt="Descriptive text goes here">
```

- The `<img>` element is **replaced** by the actual image fetched from `src`.
- You can style the image's **position, size, opacity, border, filter**, etc.
- You **can't** change the pixels inside the image with CSS.

## 📺 Example 2 — `<iframe>` (YouTube)

```html
<iframe
  width="400"
  height="200"
  src="https://www.youtube.com/embed/u43gJJrVa1I?si=BoDW_puFsy8OEr_Z"
  title="Professional Cloud Architect Certification Course – Pass the Exam! (YouTube video)"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  referrerpolicy="strict-origin-when-cross-origin"
  allowfullscreen
></iframe>
```

- The `<iframe>` is **replaced** by a YouTube video player.
- Don't worry about `referrerpolicy` and `allowfullscreen` for now — they're covered in the iframe workshop.

## 🗺️ Example 3 — `<iframe>` (Map)

```html
<iframe
  title="Map of the Royal Observatory, Greenwich, London"
  width="300"
  height="200"
  src="https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&amp;layer=mapnik"
></iframe>
```

- The iframe is **replaced** by an embedded OpenStreetMap.
- You can size and position the iframe with CSS, but you **cannot** style the map's internal markers, controls, or text — those belong to the embedded site.

## 🚫 What CSS *Cannot* Do to Replaced Element Content

If an `<iframe>` embeds a site that has its own `<h1>`, your CSS:

- ❌ Cannot change the `<h1>`'s **font size**.
- ❌ Cannot change its **color**.
- ❌ Cannot change its **text** or **layout**.

<aside>
⚠️

Replaced elements are **isolated containers**. CSS in your page never reaches into the external resource. This is also why iframes have their **own scrollbars, fonts, and CSS context** — they're effectively a separate document.

</aside>

## 📦 Common Replaced Elements

| Element | What it embeds |
| --- | --- |
| `<img>` | An external image |
| `<iframe>` | Another HTML document (site, YouTube, map…) |
| `<video>` | A video file |
| `<audio>` | An audio file |
| `<embed>` | Generic external content (PDFs, Flash legacy, etc.) |
| `<object>` | Another external resource (similar to `embed`) |

## 🔀 Sometimes-Replaced Elements

A few elements **become replaced under specific conditions**:

```html
<input type="image" alt="Descriptive text goes here" src="example-img-url">
```

- `<input type="image">` is a **replaced element** (the input is replaced by an image).
- `<input type="text">`, `<input type="email">`, etc. are **not** replaced elements.

## 🎨 What CSS *Can* Do

For a replaced element, CSS can typically style:

- `width`, `height`, `max-width`, `min-height`
- `margin`, `padding`, `border`
- `position`, `top`, `left`, `transform`, `z-index`
- `opacity`, `filter`, `box-shadow`, `border-radius`
- `object-fit`, `object-position` (for `<img>`/`<video>` content cropping/alignment)

What CSS **cannot** do: change the **internal content** of the replaced element.

## 🧠 Quick Self-Check

**1. What can you style in a replaced element?**

- [ ]  The font size.
- [x]  **The layout or positioning.**
- [ ]  The color of specific text.
- [ ]  Everything.

**2. What is a replaced element replaced with?**

- [x]  **An external object.**
- [ ]  Another element.
- [ ]  Some CSS.
- [ ]  Assembly.

**3. Which of these is a replaced element?**

- [ ]  `h1`
- [ ]  `p`
- [x]  **`iframe`**
- [ ]  `a`

## ✅ Key Takeaways

- A **replaced element** has content loaded from an **external resource** — not from your HTML/CSS.
- Common ones: **`<img>`**, **`<iframe>`**, **`<video>`**, **`<audio>`**, **`<embed>`**, **`<object>`**.
- CSS can style the **container** (size, position, filters), but **not the content** inside.
- iframes are isolated documents — your CSS can't reach inside them.
- `<input type="image">` is a replaced element; other `<input>` types are not.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 18 is created.)

</aside>
