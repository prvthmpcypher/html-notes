# SVGs — Scalable Vector Graphics for Icons, Logos & Crisp Visuals

<aside>
✨

**Big idea:** **Raster images** (PNG, JPG) store color data per pixel — they pixelate when you scale them up. **SVGs** are **vector** images that store **paths and equations**, so they scale to any size without losing quality. Bonus: SVG data is **XML**, so you can drop it straight into HTML and change colors with attributes or CSS.

</aside>

## 🖼️ Raster vs Vector — The Core Difference

| Type | How it stores data | Scales well? | Examples |
| --- | --- | --- | --- |
| **Raster** | Color value for **each pixel** | ❌ Pixelates / blurs when scaled up | PNG, JPG, WEBP, AVIF, GIF |
| **Vector** | **Paths, lines, points & equations** | ✅ Scales to any size, no quality loss | SVG |
- Try resizing a PNG to 5× its original size — you'll see jagged pixels.
- Scale an SVG to fullscreen — still crisp.

## 🖍️ What Is an SVG?

- **SVG** = **S**calable **V**ector **G**raphic.
- A vector format that stores its data as **XML** — plain text that looks a lot like HTML.
- Two superpowers:
    1. ✅ Drop it **directly into HTML** using the `<svg>` element — no separate file needed.
    2. ✅ **Programmatically change colors, strokes, sizes** with attributes or CSS.

## 😊 A Simple Smiley SVG

```html
<svg width="100" height="100" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <circle cx="50" cy="50" r="45" stroke="black" stroke-width="4" fill="yellow" />
  <circle cx="35" cy="40" r="5" fill="black" />
  <circle cx="65" cy="40" r="5" fill="black" />
  <path d="M35 65 Q50 80 65 65" stroke="black" stroke-width="4" fill="transparent" />
</svg>
```

Change `fill="yellow"` to `fill="red"` and the face turns red — no image editor required.

## 🧩 Basic SVG Building Blocks

| Element | Purpose |
| --- | --- |
| `<svg>` | Container that sets up the drawing canvas (`width`, `height`, `viewBox`) |
| `<circle>` | Draws a circle (`cx`, `cy`, `r`) |
| `<rect>` | Draws a rectangle (`x`, `y`, `width`, `height`) |
| `<line>` | Draws a straight line (`x1`, `y1`, `x2`, `y2`) |
| `<path>` | Draws complex shapes from a `d` (data) attribute |
| `<text>` | Renders text inside the SVG canvas |

Common styling attributes: **`fill`**, **`stroke`**, **`stroke-width`**, **`opacity`**, **`transform`**.

<aside>
💡

The **`viewBox`** sets the SVG's internal coordinate system. Pair it with `width` and `height` on the outer `<svg>` to control how big the drawing is rendered — without distorting the artwork.

</aside>

## 🌟 More Icon Examples

```html
<!-- Star Icon -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="gold" xmlns="http://www.w3.org/2000/svg">
  <path d="M12 2L14.9 8.6L22 9.3L17 14.1L18.3 21.2L12 17.8L5.7 21.2L7 14.1L2 9.3L9.1 8.6L12 2Z"/>
</svg>

<!-- Heart Icon -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="crimson" xmlns="http://www.w3.org/2000/svg">
  <path d="M12 21.35L10.55 20.03C5.4 15.36 2 12.28 2 8.5C2 6 4 4 6.5 4C8 4 9.5 4.8 10.5 6.09C11.5 4.8 13 4 14.5 4C17 4 19 6 19 8.5C19 12.28 15.6 15.36 10.45 20.04L12 21.35Z"/>
</svg>

<!-- Checkmark Icon -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="green" xmlns="http://www.w3.org/2000/svg">
  <path d="M20.29 5.71L9 17L3.71 11.71L5.12 10.29L9 14.17L18.88 4.29L20.29 5.71Z"/>
</svg>
```

Change the `fill` to any named color (`red`, `blue`, `purple`...) and the icon updates instantly.

## ✅ When to Reach for SVG

- **Icons** — social media icons, UI icons, bullet points. (Font Awesome, Heroicons, Lucide all ship SVGs.)
- **Logos** — scale perfectly from favicon size to full-screen hero banners.
- **Illustrations** with sharp geometry — charts, diagrams, badges.
- **Anything that needs to stay crisp** at multiple sizes or on **retina/HiDPI** screens.

## ⚠️ When *Not* to Use SVG

- **Photographs** — they have millions of pixels of detail; vectors aren't the right model. Use **WEBP** or **AVIF** instead.
- **Highly detailed, painterly art** — the SVG file would explode in size and complexity.

## 🧠 Quick Self-Check

**1. What is a raster image?**

- [ ]  An image which stores paths, lines, points, and curves.
- [x]  **An image which stores color data for each pixel.**
- [ ]  All images are raster images.
- [ ]  An image which is easily scalable.

**2. What is a vector image?**

- [x]  **An image which stores paths, lines, points, and curves.**
- [ ]  An image which stores color data for each pixel.
- [ ]  All images are vector images.
- [ ]  An image which is not easily scalable.

**3. How does an SVG store data?**

- [ ]  As pixels.
- [ ]  As binary.
- [ ]  As hexadecimal.
- [x]  **As XML.**

## ✅ Key Takeaways

- **Raster images** = pixels (PNG, JPG); **vector images** = math (SVG).
- SVGs **scale infinitely** with no quality loss — perfect for icons & logos.
- SVG data is **XML**, so it lives happily inside HTML and is editable with CSS / JS.
- Use SVG for icons, logos, illustrations, charts. Use raster for photos.
- Common SVG elements: `<svg>`, `<circle>`, `<rect>`, `<line>`, `<path>`, `<text>`.
- Style them with `fill`, `stroke`, `stroke-width`, `opacity`, `transform`.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 17 is created.)

</aside>
