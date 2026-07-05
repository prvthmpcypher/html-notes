# What Is the aria-hidden Attribute, and How Does It Work?

<aside>
✨

**Big idea:** **`aria-hidden="true"`** removes an element (and its subtree) from the **accessibility tree** — it's invisible to screen readers but still visible on screen. Useful for **decorative icons** and **purely visual filler**. Never use it on focusable elements — focus would land on something assistive tech can't see.

</aside>

## 🙈 What `aria-hidden` Does

- Boolean-ish attribute: `aria-hidden="true"` or `aria-hidden="false"`.
- When `true`, the element and **all its descendants** are removed from the **accessibility tree**.
- Screen readers, voice tools, and other assistive tech act as if the element doesn't exist.
- **CSS rendering is unaffected** — the element still shows on screen unless other CSS hides it.

```html
<button>
  <svg aria-hidden="true">...</svg>
  Save
</button>
```

Screen reader announces just **"Save, button"** — the decorative icon stays out of the way.

## 🎯 When to Use It

- **Decorative icons** that sit next to a text label.
- **Purely visual filler** (decorative SVGs, dividers).
- **Duplicate content** that's already announced elsewhere (e.g., a tooltip mirroring visible text).
- **Off-screen modals** while not active — hide the rest of the page so screen reader users stay in the modal.

## 🚫 When NOT to Use It

- **On focusable elements.** Focus can still land on a `tabindex` element marked aria-hidden — the user lands on "nothing."
- **On meaningful content.** Don't aria-hide a paragraph just to clean up screen-reader output — you're hiding information.
- **As a replacement for `hidden` or `display: none`.** Those hide the element from *everyone*. `aria-hidden` hides only from a11y tech.
- **On the root of a modal that you want screen readers to read.** That's the opposite of what you want.

## 🧑‍💻 Common Patterns

### Decorative SVG inside a button

```html
<button type="button">
  <svg aria-hidden="true" focusable="false">
    <path d="M12 5v14M5 12h14" />
  </svg>
  New file
</button>
```

### Hide background page when a modal opens

```html
<body>
  <main id="main" aria-hidden="true">...</main>
  <div role="dialog" aria-modal="true">...</div>
</body>
```

When the dialog closes, restore `aria-hidden="false"` (or remove it) on the main content.

## ⚖️ `aria-hidden` vs `hidden` vs `visibility: hidden` vs `display: none`

| Technique | Visible on screen? | In a11y tree? | Takes layout space? | Focusable? |
| --- | --- | --- | --- | --- |
| `aria-hidden="true"` | **Yes** | No | Yes | **Avoid — still possible** |
| `hidden` attribute | No | No | No | No |
| `display: none` | No | No | No | No |
| `visibility: hidden` | No | No | **Yes** | No |
| `opacity: 0` | No (transparent) | **Yes** | Yes | **Yes** |
| Visually-hidden CSS class | No | **Yes** | No (positioned off-screen) | Yes |

Pick the right tool for the job:

- Hide from **everyone** → `hidden` or `display: none`.
- Hide only from **screen readers**, keep visually → `aria-hidden="true"`.
- Hide only **visually**, expose to screen readers → visually-hidden CSS pattern.

## 🧠 Quick Self-Check

**1. `aria-hidden="true"` removes the element from…**

- [ ]  The DOM
- [x]  **The accessibility tree (it's invisible to screen readers but still rendered visually)**
- [ ]  The rendered page
- [ ]  CSS layout

**2. Which is a BAD use of `aria-hidden`?**

- [ ]  On a decorative SVG inside a labeled button
- [x]  **On a focusable interactive button**
- [ ]  On a tooltip that duplicates visible text
- [ ]  On a divider that's purely decorative

**3. Which CSS pattern hides visually but KEEPS the element in the accessibility tree?**

- [ ]  `display: none`
- [ ]  `aria-hidden="true"`
- [x]  **A visually-hidden / sr-only CSS class**
- [ ]  `hidden` attribute

## ✅ Key Takeaways

- **`aria-hidden="true"`** → hides from assistive tech but **still visible on screen**.
- Use on **decorative icons** and **content already announced elsewhere**.
- **Never** put it on a focusable element — focus would land on "nothing."
- Don't confuse with `hidden`, `display: none`, `visibility: hidden` (those hide visually too).
- For "visually hidden but screen-reader-visible" content, use a **visually-hidden CSS class** instead.

---

<aside>
➡️

**Next chapter →** The `aria-describedby` attribute — extra context for controls.

</aside>
