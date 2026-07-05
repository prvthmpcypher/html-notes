# When Is the alt Attribute Needed, and What Are Some Examples of Good Alt Text?

<aside>
✨

**Big idea:** Every **`<img>`** element must have an **`alt` attribute**. If the image carries meaning, write a short, specific description of what it shows. If the image is purely decorative, use an **empty alt (`alt=""`)** so screen readers skip it. The `alt` is your image's voice.

</aside>

## 🖼️ When Is `alt` Required?

- **Always** — every `<img>` must have an `alt` attribute.
- The **value** depends on whether the image is **meaningful** (needs a description) or **decorative** (use `alt=""`).

### Empty alt for decorative images

```html
<!-- A swirl divider that's just decoration -->
<img src="/img/swirl.png" alt="" />
```

With `alt=""`, screen readers **skip the image entirely** — perfect for purely visual flourishes.

### Missing alt is worse

```html
<!-- ❌ No alt at all — screen reader announces the file name -->
<img src="/img/swirl.png" />
```

Some screen readers will literally read **"image swirl dot png"** — unhelpful and noisy.

## 📝 Writing Good Alt Text

Good alt text answers: **"If the image disappeared, what would the user need to know?"**

### Rules of thumb

- **Be specific** — say what's actually shown, not generic.
- **Be concise** — aim for one sentence; under ~125 characters when possible.
- **Avoid "image of" or "picture of"** — screen readers already announce "image."
- **Skip redundant info** — if a caption already explains the image, keep alt short or empty.
- **Match context** — the same image can need different alt text on different pages.

## ✅ Examples — Good Alt Text

```html
<!-- Product photo -->
<img src="chair.jpg" alt="Walnut Eames lounge chair with black leather cushions" />

<!-- Profile/avatar -->
<img src="jane.jpg" alt="Jane Doe smiling at the camera" />

<!-- Informational diagram -->
<img src="plant-anatomy.svg"
     alt="Diagram of a flower with petals, stamen, pistil, and sepals labeled." />

<!-- Logo (the brand IS the meaning) -->
<img src="acme-logo.svg" alt="Acme Corp" />

<!-- Decoration -->
<img src="corner-flourish.png" alt="" />
```

## ❌ Examples — Bad Alt Text

```html
<!-- Useless: just says "image" -->
<img src="chair.jpg" alt="image" />

<!-- Redundant "picture of" -->
<img src="chair.jpg" alt="picture of a chair" />

<!-- Filename garbage -->
<img src="IMG_4032.jpg" alt="IMG_4032.jpg" />

<!-- Keyword-stuffed for SEO (Google penalizes this) -->
<img src="chair.jpg" alt="chair walnut leather modern furniture best chair buy chair" />

<!-- Decorative image with verbose alt -->
<img src="swirl.png" alt="Decorative swirl illustration line graphic" />
```

## 🔗 Linked Images and Buttons with Icons

If an image is **inside a link** with no other text, the `alt` becomes the link's accessible name:

```html
<a href="/cart">
  <img src="cart-icon.svg" alt="Shopping cart" />
</a>
```

If the image is an icon **next to text**, mark the icon decorative so the text doesn't get duplicated:

```html
<a href="/cart">
  <img src="cart-icon.svg" alt="" />
  Cart
</a>
```

## 🖥️ Other Elements That Need Alt Text

- **`<area>`** elements inside an `<map>` use `alt`.
- **`<input type="image">`** uses `alt` for the button label.
- **`<svg>`** uses `<title>` (and optionally `<desc>`) plus `role="img"` for meaningful graphics, or `aria-hidden="true"` for decorative ones.
- **`<figure>` + `<figcaption>`** is the right pattern for images with longer captions.

## 🧠 Quick Self-Check

**1. Which is required on every `<img>` element?**

- [ ]  `title`
- [x]  **`alt`**
- [ ]  `width`
- [ ]  `loading`

**2. What value should the `alt` attribute have on a purely decorative image?**

- [ ]  Don't include `alt` at all
- [ ]  `alt="decoration"`
- [x]  **`alt=""` (empty)**
- [ ]  `alt="image"`

**3. Which is the BEST alt text for a photo of a walnut lounge chair?**

- [ ]  `"image"`
- [ ]  `"chair chair chair best chair"`
- [ ]  `"picture of chair"`
- [x]  **`"Walnut Eames lounge chair with black leather cushions"`**

## ✅ Key Takeaways

- **Every `<img>` needs an `alt` attribute** — always.
- Meaningful image → **short, specific description** of what's shown.
- Decorative image → **`alt=""`** so screen readers skip it.
- Skip phrases like "image of" or "picture of" — screen readers already announce "image."
- For SVGs, use `<title>` + `<desc>` + `role="img"` (or `aria-hidden="true"` for decoration).
- Match context — the same image may need different alt text on different pages.

---

<aside>
➡️

**Next chapter →** Writing good link text and why it matters for accessibility.

</aside>
