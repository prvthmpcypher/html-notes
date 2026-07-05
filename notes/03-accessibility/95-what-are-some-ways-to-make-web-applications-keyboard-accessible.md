# What Are Some Ways to Make Web Applications Keyboard Accessible?

<aside>
✨

**Big idea:** Every action a mouse user can do, a **keyboard user must also be able to do**. That means: every interactive element is reachable by **Tab**, has a **visible focus ring**, supports the **expected keyboard shortcuts**, and never **traps focus**. Native HTML gets you most of the way; ARIA + handlers cover the rest.

</aside>

## ⌨️ Why Keyboard Accessibility?

- **Screen-reader users** drive primarily with the keyboard.
- **Motor-impaired users** may use switches, voice, or alternative pointers — all of which emit keyboard-equivalent events.
- **Power users** prefer keyboard shortcuts.
- **WCAG 2.1.1 (Keyboard)** requires that **all functionality** be available via keyboard.

## 🔑 The Four Pillars

### 1️⃣ Everything reachable with Tab

- Use **native interactive elements** (`<button>`, `<a href>`, `<input>`, `<select>`, `<textarea>`, `<summary>`) — they're keyboard-reachable by default.
- For custom widgets, add **`tabindex="0"`** to make them tabbable.
- Avoid **`tabindex` values greater than 0** — they break the natural DOM order.
- Use **`tabindex="-1"`** for elements that should receive focus programmatically but not via Tab.

### 2️⃣ Visible focus indicators

- Browsers add a focus ring by default. **Never remove it without replacing it.**
- Style focus visibly:

```css
:focus-visible {
  outline: 2px solid #2563eb;
  outline-offset: 2px;
}
```

- `:focus-visible` shows focus only for keyboard users — mouse clicks don't show the ring on most browsers.

### 3️⃣ Logical tab order

- **DOM order should match visual order.** If they don't, keyboard users get confused.
- Don't rely on CSS `order` (Flexbox) or `grid-area` to reorder content — those don't change tab order.
- Test with **Tab key** — you should always know where focus will land next.

### 4️⃣ Expected keyboard shortcuts per widget

Follow the **ARIA Authoring Practices Guide** for custom widgets:

| Widget | Expected keys |
| --- | --- |
| **Button** | Enter, Space |
| **Link** | Enter |
| **Checkbox** | Space |
| **Radio group** | Arrows to move; Space to select |
| **Tabs** | Arrows to switch; Enter/Space to activate (or auto-activate on focus) |
| **Menu / combobox** | Arrows, Enter, Esc |
| **Slider** | Arrows, PageUp/PageDown, Home/End |
| **Dialog (modal)** | Esc closes; Tab cycles **inside** the dialog; focus returns to trigger on close |

## 🚪 Don't Trap Focus

- Inside a modal, **focus must stay inside** until the user dismisses it (focus trap).
- Outside a modal, **focus must never be trapped**. The user must always be able to Tab past your widget.
- Provide an **Escape** key to close any modal, dialog, or expanded menu.

## 🔗 Skip Links

- A **skip link** lets keyboard users jump past the navigation directly to main content.
- The first focusable element on the page should be a hidden-until-focused link:

```html
<a class="skip-link" href="#main">Skip to main content</a>
...
<main id="main">...</main>
```

```css
.skip-link {
  position: absolute;
  left: -9999px;
}
.skip-link:focus {
  position: static;
}
```

## ⚠️ Common Mistakes

- **Removing `outline`** without a replacement focus style.
- Using `<div>` or `<span>` as a button without `tabindex`, keyboard handlers, or a proper `role`.
- Forgetting `Enter` and `Space` handlers on custom buttons.
- Modals that **don't trap focus inside** while open (Tab escapes to the page behind).
- Modals that **trap focus forever** — no way to close with Esc.
- Carousels that auto-advance without a **pause control**.
- Hover-only menus that can't be opened via keyboard.

## 🧪 How to Test

1. Hide the mouse — unplug it or use the touchpad disable shortcut.
2. **Tab** through your page from the top.
3. Can you reach every link, button, input, video control?
4. Does **focus stay visible** at every step?
5. Does **DOM order match visual order**?
6. Inside dialogs, does **Esc close** them and **Tab cycle inside**?
7. Open **DevTools → Accessibility → Show Tab Stops** to visualize the order.

## 🧠 Quick Self-Check

**1. WCAG 2.1.1 requires that…**

- [x]  **All functionality must be available via keyboard**
- [ ]  Every page must have a hamburger menu
- [ ]  Every site must support touch gestures
- [ ]  Every link must have a `title` attribute

**2. Which `tabindex` value should you generally avoid?**

- [ ]  `0`
- [ ]  `-1`
- [x]  **Positive numbers like `1`, `2`, `3` (they break natural order)**
- [ ]  None — all values are fine

**3. When a modal closes, focus should return to…**

- [ ]  The top of the page
- [ ]  The first link on the page
- [x]  **The element that opened the modal**
- [ ]  Wherever the browser chooses

## ✅ Key Takeaways

- All interactive functionality must work via **keyboard alone** (WCAG 2.1.1).
- Use **native HTML controls** — they're keyboard-accessible by default.
- Keep **visible focus styles** (`:focus-visible`), **logical tab order**, and **predictable keyboard shortcuts**.
- For modals: **trap focus inside, Esc to close, return focus to the trigger** on close.
- Add a **skip link** so users can bypass repetitive nav.
- Test by unplugging the mouse and Tab-ing through your page.

---

<aside>
➡️

**Next chapter →** HTML Accessibility Review — the recap sheet for everything you've just learned.

</aside>
