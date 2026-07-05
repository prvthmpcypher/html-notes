# Optimizing Media Assets — Size, Format & Compression

<aside>
✨

**Big idea:** Three levers control how fast your images load: **size** (match the rendered dimensions), **format** (prefer modern formats like WEBP / AVIF over PNG / JPG), and **compression** (squeeze every byte without ruining quality). Get all three right and your pages feel ⚡ fast.

</aside>

## 🗜️ The Three Levers for Image Optimization

| Lever | Goal |
| --- | --- |
| **Size** | Match the rendered dimensions — don't ship a 1920×1080 image to display at 640×480 |
| **Format** | Use modern, more efficient formats (WEBP, AVIF) when possible |
| **Compression** | Reduce file size with the right algorithm (lossless vs lossy) |

## 📏 1. Size — Match the Rendered Resolution

- Resolution is written **width × height in pixels** (e.g., **640×480**).
- Scale your image to **match the size at which it's displayed** — not your camera's native resolution.
- Shipping a 1920×1080 image to render at 640×480 forces users to download data they'll never see.
- Smaller resolution → **smaller file** → **faster page**.

<aside>
💡

For responsive pages, you can serve **different image sizes for different screens** using the `srcset` and `sizes` attributes on `<img>` (covered in later lessons).

</aside>

## 🖼️ 2. Format — Pick the Right File Type

| Format | Compression | Best for |
| --- | --- | --- |
| **PNG** | Lossless | Graphics with sharp edges, transparency |
| **JPG / JPEG** | Lossy | Photographs (legacy) |
| **WEBP** | Lossless *and* lossy | Modern replacement for PNG/JPG — smaller files |
| **AVIF** | Lossy (modern) | Newest, often even smaller than WEBP |
| **GIF** | Lossless (palette-limited) | Short animations (mostly replaced by WEBP/MP4) |
| **SVG** | Vector (text-based) | Icons, logos, illustrations — scales to any size |

Unless you must support very old browsers, **prefer WEBP or AVIF** over PNG and JPG. They're generally **30–50% smaller** at similar visual quality.

## 🗜️ 3. Compression — Lossless vs Lossy

### 🔒 Lossless compression

- **Preserves all original image data.** You can decompress and get the **exact original back**.
- Re-saving doesn't degrade quality.
- Examples: **PNG**, **WEBP (lossless mode)**, **GIF**.
- Tools: **pngcrush**, **OptiPNG**, **ZopfliPNG**.

### 🔓 Lossy compression

- **Permanently discards data** to shrink the file.
- Each re-save discards a little more → **quality degrades over time**.
- Examples: **JPG**, **WEBP (lossy mode)**, **AVIF**.
- Trade-off: way smaller files, but you can't recover the original.

<aside>
⚠️

**Always keep an unedited master copy** of lossy images. Re-saving a JPG five times produces visibly worse results than saving once at the right quality from the master.

</aside>

## 🧩 A Quick Optimization Checklist

- ✅ Resize the image to the **exact rendered dimensions** (or 2× for retina screens).
- ✅ Convert to a **modern format** (WEBP or AVIF) when possible.
- ✅ Run it through a **compressor** (pngcrush, MozJPEG, Squoosh, ImageOptim).
- ✅ For icons/logos → use **SVG** instead of bitmap formats.
- ✅ Set explicit **`width`** and **`height`** in HTML to avoid layout shift.

## 🧠 Quick Self-Check

**1. How should you scale, or size, your images?**

- [ ]  Your images should be smaller than the rendered size on the page.
- [ ]  Your images should be larger than the rendered size on the page.
- [x]  **Your images should be the same scale as the rendered size on the page.**
- [ ]  It doesn't matter, use whatever size you'd like.

**2. Which of the following is NOT a valid image file type?**

- [x]  **TS**
- [ ]  PNG
- [ ]  JPG
- [ ]  WEBP

**3. Which file format uses lossy compression, meaning re-saving or re-compressing it degrades image quality?**

- [ ]  WEBP
- [ ]  PNG
- [x]  **JPG**
- [ ]  GIF

## ✅ Key Takeaways

- Three optimization levers: **size**, **format**, **compression**.
- Always scale images to **match their rendered dimensions** — don't waste bandwidth.
- Prefer **WEBP** or **AVIF** over PNG / JPG for modern browsers.
- **Lossless** (PNG, WEBP lossless) preserves all data; **lossy** (JPG, WEBP lossy, AVIF) discards data permanently for smaller files.
- Keep an unedited **master copy** of lossy files — each re-save degrades quality further.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 15 is created.)

</aside>
