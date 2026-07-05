# What Is the Purpose of WAI-ARIA, and How Does It Work?

<aside>
✨

**Big idea:** **WAI-ARIA** (Web Accessibility Initiative – Accessible Rich Internet Applications) is a set of **roles, states, and properties** you add to HTML to make **custom widgets** (tabs, dialogs, comboboxes, tree views) understandable to assistive tech. **First rule of ARIA: don't use ARIA if a native HTML element already does the job.**

</aside>

## 🏛️ What Is WAI-ARIA?

- A W3C specification, maintained by the **Web Accessibility Initiative (WAI)** at the W3C.
- Adds three categories of attributes to HTML:

| Category | Example | Purpose |
| --- | --- | --- |
| **Roles** | `role="dialog"` | What kind of UI is this? |
| **States** | `aria-expanded="true"` | Current condition (changes over time) |
| **Properties** | `aria-label="Close"` | Relationships / metadata (mostly static) |

These attributes don't change visuals — they update the **accessibility tree** the browser exposes to screen readers, voice tools, and other assistive software.

## 🎯 Why ARIA Exists

- HTML has great built-in semantics for common things (`<button>`, `<a>`, `<input>`, `<select>`).
- But there are many UI patterns HTML doesn't natively express — **tabs**, **accordions**, **autocomplete**, **tree views**, **toolbars**, **live regions**.
- ARIA fills that gap so custom widgets can still announce themselves correctly to assistive tech.

## 📜 The Five Rules of ARIA

From the official **"Using ARIA"** guide — internalize these:

1. **Don't use ARIA if a native HTML element exists.** `<button>` > `<div role="button">`.
2. **Don't change native semantics** unless you really must. Don't write `<h1 role="button">`.
3. **All interactive ARIA controls must be usable with the keyboard.** Roles imply behaviors — you must implement them.
4. **Don't use `role="presentation"` or `aria-hidden="true"`** on focusable elements — focus will land on something invisible to a screen reader.
5. **All interactive elements must have an accessible name.** That's a label, ARIA label, or labelled-by reference.

## 🧩 A Quick Example

### ❌ Without ARIA (custom widget, broken)

```html
<div class="toggle" tabindex="0">Notifications</div>
```

Screen reader: "Notifications" — *what is it? A heading? A clickable thing? Is it on or off?*

### ✅ With ARIA

```html
<button type="button" aria-pressed="false">Notifications</button>
```

Screen reader: "Notifications, toggle button, not pressed."

Notice we **switched to a native `<button>`** and used a single ARIA state — rule #1.

## ⚠️ Common ARIA Mistakes

- **`<div role="button">`** — use `<button>`.
- **`role="link"` on a `<span>`** — use `<a href>`.
- **`aria-label` that doesn't match visible text** — breaks WCAG "Label in Name."
- **`aria-hidden="true"`** on a focusable element — focus lands on "nothing."
- **No keyboard handler** for a `role="button"` div.
- **Overusing ARIA** — too many roles can drown a screen reader in noise.

## 🛠️ Where to Learn the Patterns

- **ARIA Authoring Practices Guide (APG)** — official patterns for dialogs, comboboxes, menus, etc.
- **MDN ARIA reference**.
- **Inclusive Components** (Heydon Pickering) — implementation-focused, accessible component recipes.

## 🧠 Quick Self-Check

**1. What does WAI-ARIA stand for?**

- [ ]  Web Accessibility Initiative for Animated Rich Apps
- [x]  **Web Accessibility Initiative – Accessible Rich Internet Applications**
- [ ]  Web Authoring Interface for Accessibility
- [ ]  World Accessibility Internet Annotation

**2. According to the first rule of ARIA, what should you do first?**

- [ ]  Add ARIA to every element
- [x]  **Use a native HTML element if one already exists for the job**
- [ ]  Hide all decorative elements with `aria-hidden`
- [ ]  Add `role="presentation"` to every `<div>`

**3. ARIA primarily changes which of the following?**

- [ ]  The visual appearance of an element
- [x]  **What the browser exposes to assistive technology (the accessibility tree)**
- [ ]  The page's HTML markup
- [ ]  The CSS box model

## ✅ Key Takeaways

- **WAI-ARIA** = a way to communicate UI semantics to assistive tech via **roles**, **states**, and **properties**.
- **First rule of ARIA: don't use ARIA when a native HTML element will do.**
- All interactive ARIA controls must be **keyboard-usable** and have an **accessible name**.
- ARIA changes the **accessibility tree** — never the visual rendering.
- For complex widgets, follow the patterns in the **ARIA Authoring Practices Guide (APG)**.

---

<aside>
➡️

**Next chapter →** ARIA roles — the most important ARIA attribute.

</aside>
