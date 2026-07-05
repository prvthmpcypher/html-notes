# What Are Screen Magnifiers Used For?

<aside>
✨

**Big idea:** A **screen magnifier** zooms a portion of the screen so users with **low vision** can see it clearly. Most operating systems include one built in. Your job as a developer: build pages that **reflow** when zoomed up to 400%, and never break layouts at higher zoom levels.

</aside>

## 🔍 What Is a Screen Magnifier?

- Software that **enlarges part of the screen** so users with low vision can read it.
- Provides a movable **lens** or **fullscreen zoom** that follows the cursor or focused element.
- May add features like **inverted colors**, **high contrast**, **focus highlighting**, and **smooth tracking**.

## 👥 Who Uses Magnifiers?

- **Low-vision users** who can see text but only when enlarged.
- People with conditions like **macular degeneration**, **diabetic retinopathy**, **glaucoma**, or **cataracts**.
- **Older adults** with age-related vision decline.
- Anyone with **temporary eye strain** or working in poor lighting.

## 🧠 Common Screen Magnifiers

| Magnifier | Platform | Notes |
| --- | --- | --- |
| **Magnifier** | Windows | Built-in; Win + `+`/`–` to zoom |
| **Zoom** | macOS | Built-in; Ctrl + scroll or pinch-zoom |
| **ZoomText** | Windows (commercial) | Adds screen-reader features too |
| **Magnification** | Android | Triple-tap to zoom; accessibility shortcut |
| **Zoom** | iOS | Triple-tap with three fingers |
| **Browser zoom** | All browsers | Ctrl + `+` / `–` — most-used "magnifier" of all |

## 🎯 What Magnifier Users Need from Your Site

- **Responsive layout** — content must reflow when zoomed; **no horizontal scrolling** at 320 px width (WCAG 1.4.10).
- Support **up to 400% browser zoom** without losing functionality (WCAG 1.4.4).
- Use **relative units** (`rem`, `em`, `%`) instead of fixed `px` everywhere — text scales properly.
- **Don't lock the viewport** with `user-scalable=no` or `maximum-scale=1` — that prevents mobile zoom.
- Keep **focus indicators visible and big enough** to find with a magnifier lens.
- Keep **related controls grouped visually** so a single magnified view captures them together.

## 🚫 Common Anti-Patterns

```html
<!-- ❌ Disables pinch-zoom on mobile -->
<meta name="viewport"
      content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">

<!-- ✅ Lets users zoom freely -->
<meta name="viewport"
      content="width=device-width, initial-scale=1">
```

Other things to avoid:

- Fixed-pixel text that doesn't grow on zoom.
- Tiny click targets that vanish at 400% zoom.
- Overlays/sticky bars that eat too much screen space when magnified.
- Important info revealed only on hover — a magnifier lens may not include the trigger.

## 🧠 Quick Self-Check

**1. A screen magnifier helps users with…**

- [ ]  Color blindness
- [x]  **Low vision**
- [ ]  Hearing loss
- [ ]  No disability — it's a developer tool

**2. WCAG requires that a page must remain functional up to what browser zoom level?**

- [ ]  150%
- [ ]  200%
- [x]  **400%**
- [ ]  1000%

**3. Which `<meta name="viewport">` line is BAD for accessibility?**

- [ ]  `<meta name="viewport" content="width=device-width, initial-scale=1">`
- [x]  **`<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no">`**
- [ ]  `<meta name="viewport" content="width=device-width">`
- [ ]  `<meta name="viewport" content="initial-scale=1">`

## ✅ Key Takeaways

- A **screen magnifier** zooms part of the screen for low-vision users.
- Most OSes (Windows, macOS, iOS, Android) ship one; the **browser's own zoom** is the most common magnifier.
- Your site must **reflow gracefully up to 400% zoom** with no horizontal scrollbar at 320 px.
- Use **relative units** (`rem`/`em`/`%`) and **never disable mobile pinch-zoom**.
- Keep focus indicators visible, click targets large, and important info **not hidden behind hover**.

---

<aside>
➡️

**Next chapter →** Voice recognition software — how spoken input shapes accessible UI.

</aside>
