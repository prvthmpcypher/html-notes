# What Are the Roles of the aria-label and aria-labelledby Attributes?

<aside>
✨

**Big idea:** `aria-label` and `aria-labelledby` both give an element an **accessible name** when a native label isn't possible. **`aria-label`** holds the label **text directly** in the attribute. **`aria-labelledby`** points to **one or more existing elements** on the page whose visible text becomes the label.

</aside>

## 🏷️ Why Accessible Names Matter

Every interactive element (button, link, input, region) needs an **accessible name** so screen readers can announce it and voice users can target it. Native HTML often gives this for free (`<label>`, the text inside `<button>`). When it doesn't, ARIA fills the gap.

## 📝 `aria-label` — Direct Text

- Holds the label as a **string value**.
- Visible to **assistive tech only** — not rendered on screen.
- Best for **icon-only buttons** or any control without visible text.

```html
<button aria-label="Close dialog">
  <svg aria-hidden="true">...</svg>
</button>
```

Screen reader announces: **"Close dialog, button."**

### When to reach for `aria-label`

- Icon-only buttons (close, search, menu).
- Links where the link text alone is ambiguous (e.g., a card link wrapping just an image).
- Inputs without a visible label (rare — prefer a real `<label>` when possible).

## 🔗 `aria-labelledby` — Reference Another Element

- Points to **one or more `id`s** of elements on the page whose text becomes the label.
- The referenced text is **visible on screen** — keeping label and visible text in sync.
- Multiple IDs can be combined, **space-separated**, to compose a richer label.

```html
<h2 id="section-title">Pricing</h2>
<section aria-labelledby="section-title">
  ...
</section>
```

Screen reader announces the section as: **"Pricing, region."**

### Combining multiple references

```html
<button id="delete">Delete</button>
<span id="item-name">Invoice #1234</span>

<button aria-labelledby="delete item-name">
  ✖
</button>
```

Accessible name becomes **"Delete Invoice #1234."**

## ⚖️ `aria-label` vs `aria-labelledby`

| Aspect | `aria-label` | `aria-labelledby` |
| --- | --- | --- |
| Stores | **A string** of text | **One or more element IDs** |
| Visible on screen? | No — attribute value only | Yes — references visible elements |
| Best for | Icon-only buttons, hidden context | Regions, dialogs, fieldsets, complex composed names |
| Maintenance risk | Can drift from visible text | Stays in sync with the visible label |

## 📜 Priority — Which Wins?

The browser computes an accessible name with this priority:

1. **`aria-labelledby`** (highest)
2. **`aria-label`**
3. **Native labeling** (`<label>`, `<button>` text content, `alt`, `title` last-resort)

So `aria-labelledby` overrides `aria-label`, which overrides the native text.

## ⚠️ Common Mistakes

- Using `aria-label` on a control that **already has visible text** that's clear — unnecessary.
- `aria-label` text that **doesn't match** the visible label — breaks WCAG 2.5.3 (Label in Name).
- `aria-labelledby` pointing to an `id` that **doesn't exist** or **isn't unique**.
- Pointing to an element with **`display: none`** — the text is still used as the name but invisible to users.
- Using `aria-label` on **non-interactive** elements where it has no effect (e.g., on a plain `<p>`).

## 🧠 Quick Self-Check

**1. `aria-label` provides…**

- [ ]  A reference to another element's text
- [x]  **A label as a string value, visible to assistive tech only**
- [ ]  A CSS class
- [ ]  A keyboard shortcut

**2. `aria-labelledby` accepts as its value…**

- [ ]  Plain text
- [ ]  A CSS selector
- [x]  **One or more space-separated `id`s of elements whose text becomes the label**
- [ ]  An HTML fragment

**3. Which has the HIGHEST priority when the browser builds the accessible name?**

- [ ]  `<label>` element
- [ ]  `aria-label`
- [x]  **`aria-labelledby`**
- [ ]  `title` attribute

## ✅ Key Takeaways

- Both attributes give an element an **accessible name** when native labeling isn't enough.
- **`aria-label`** = string text, invisible on screen — best for icon-only controls.
- **`aria-labelledby`** = references one or more `id`s; stays in sync with visible text.
- Priority: **`aria-labelledby`** > **`aria-label`** > native HTML labeling.
- Don't let `aria-label` drift from the visible text — it breaks the WCAG "Label in Name" rule.

---

<aside>
➡️

**Next chapter →** The `aria-hidden` attribute — hiding things from assistive tech.

</aside>
