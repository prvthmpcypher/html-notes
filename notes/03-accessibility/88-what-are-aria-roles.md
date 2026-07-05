# What Are ARIA Roles?

<aside>
✨

**Big idea:** An **ARIA role** tells assistive tech **what kind of UI an element is** — a button, a dialog, a navigation, a tab. The role overrides or supplies the element's implicit semantics. Use roles sparingly: if a native HTML element already has the right role baked in, use it instead.

</aside>

## 🎭 What Is an ARIA Role?

- A **role** is an attribute (`role="..."`) that **identifies what an element is** to the accessibility tree.
- Every interactive element should have **one role** — either implicit (from the HTML tag) or explicit (from `role`).
- Roles tell screen readers and other assistive tech how to **announce and interact** with the element.

## 📦 Categories of ARIA Roles

| Category | Examples | Used for |
| --- | --- | --- |
| **Landmark** | `banner`, `main`, `navigation`, `contentinfo`, `complementary`, `search`, `form` | Top-level page regions |
| **Widget** | `button`, `link`, `checkbox`, `slider`, `tab`, `tabpanel`, `dialog`, `menu`, `menuitem` | Interactive controls |
| **Document structure** | `heading`, `list`, `listitem`, `table`, `row`, `cell`, `article`, `figure` | Content structure |
| **Live region** | `alert`, `status`, `log`, `timer` | Content that updates dynamically |
| **Window** | `dialog`, `alertdialog` | Modal / overlay windows |
| **Abstract** | `widget`, `composite`, `input` | Don't use directly — ARIA uses them internally |

## 📠 Native Elements Already Have Roles

Most HTML elements have an **implicit role**. Adding `role` is redundant or harmful in these cases:

| Element | Implicit role |
| --- | --- |
| `<button>` | button |
| `<a href="...">` | link |
| `<input type="checkbox">` | checkbox |
| `<nav>` | navigation |
| `<main>` | main |
| `<header>` (page-level) | banner |
| `<footer>` (page-level) | contentinfo |
| `<aside>` | complementary |
| `<dialog>` | dialog |

So `<nav role="navigation">` is redundant. `<button role="button">` is redundant. **Just use the native element.**

## 🔨 When You'd Actually Add a Role

- You're stuck with a non-semantic element (rare but real — e.g., overriding a third-party widget).
- You're building a **custom composite widget** that has no native HTML equivalent (e.g., `role="tablist"` + `role="tab"` + `role="tabpanel"`).
- You're marking a **live region** (`role="alert"`, `role="status"`).
- You're patching legacy code where switching elements would be too invasive.

### Example — tabs widget

```html
<div role="tablist" aria-label="Account settings">
  <button role="tab" aria-selected="true" aria-controls="profile" id="tab-profile">
    Profile
  </button>
  <button role="tab" aria-selected="false" aria-controls="billing" id="tab-billing">
    Billing
  </button>
</div>
<div role="tabpanel" id="profile" aria-labelledby="tab-profile">...</div>
<div role="tabpanel" id="billing" aria-labelledby="tab-billing" hidden>...</div>
```

## ⚠️ Common Mistakes

- **Adding a role just because** — `<button role="button">` is noise.
- **Wrong role for the element** — `<a role="button">` confuses keyboard users; use `<button>`.
- **No keyboard support** — a `role="button"` div needs Enter + Space handlers, focus, and `tabindex`.
- **Mixing landmark roles with the wrong elements** — e.g., `<footer role="navigation">`.
- **Using abstract roles** — like `role="widget"` or `role="input"` — these are internal to the ARIA spec.

## 🧠 Quick Self-Check

**1. What does an ARIA role do?**

- [ ]  It styles the element with a special look
- [x]  **It tells assistive tech what kind of UI the element is**
- [ ]  It removes the element from the DOM
- [ ]  It adds JavaScript event handlers automatically

**2. Which is the LEAST useful place to add an ARIA role?**

- [x]  **On a native `<button>` to say `role="button"`**
- [ ]  On a custom tablist made from `<div>`s
- [ ]  On a `<div>` representing an `alert` live region
- [ ]  On a custom modal with `role="dialog"`

**3. Which is a landmark role?**

- [ ]  `button`
- [ ]  `tab`
- [x]  **`navigation`**
- [ ]  `checkbox`

## ✅ Key Takeaways

- An ARIA role identifies **what an element is** for assistive tech.
- Most HTML elements have an **implicit role** — don't redundantly add `role`.
- Use roles for **custom widgets** (tabs, dialogs, treeviews), **landmarks** when needed, and **live regions**.
- Always provide **keyboard support and accessible names** alongside any interactive role.
- Don't use **abstract roles** (`widget`, `composite`, `input`).

---

<aside>
➡️

**Next chapter →** The `aria-label` and `aria-labelledby` attributes.

</aside>
