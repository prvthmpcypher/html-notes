# Why Is It Important for Inputs to Have an Associated Label?

<aside>
✨

**Big idea:** Every form input needs a **proper `<label>`** that's programmatically associated with it. The label tells screen readers what the field is for, **enlarges the click target** (clicking the label focuses the input), and helps **voice users** name the field. Placeholders are not labels — use both, never just one.

</aside>

## 🏷️ What a `<label>` Does

A `<label>` provides the **accessible name** for a form control. With it:

- 🔊 **Screen readers** announce "Email, edit text" instead of just "edit text."
- 👆 **Clicking the label focuses the input** — bigger target, easier on motor-impaired users.
- 🎙️ **Voice users** can say "Click Email."
- 🔍 **Browser autofill** uses labels to identify common fields like email, phone, address.

## 🛠️ Three Ways to Associate a Label

### 1️⃣ `for` + `id` (most flexible — most common)

```html
<label for="email">Email</label>
<input type="email" id="email" name="email" />
```

The `for` attribute must match the input's `id`. Label and input can be **anywhere** on the page.

### 2️⃣ Wrapping (implicit association)

```html
<label>
  Email
  <input type="email" name="email" />
</label>
```

No `for`/`id` needed — the input is inside the label.

### 3️⃣ `aria-label` or `aria-labelledby` (last resort)

```html
<input type="search" aria-label="Search the site" />
```

Only when **no visible label** is possible (e.g., a single icon-only search field). Visible labels are always preferable.

## 🚫 What's NOT a Label

- **`placeholder`** — disappears the moment the user starts typing, low contrast, often confused with default text. Always pair with a real label.
- **`title`** — appears on hover (mouse-only) and is invisible to most users.
- **Adjacent text** without `for`/`id` — visually associated isn't programmatically associated.
- **`name` attribute** — used for form submission, not for accessibility.

### ❌ Bad

```html
<!-- Placeholder pretending to be a label -->
<input type="email" placeholder="Email" />
```

### ✅ Good

```html
<label for="email">Email</label>
<input type="email" id="email" placeholder="name@example.com" />
```

## 🔘 Special Cases

- **Radio buttons / checkboxes:** each input needs its own label.

```html
<fieldset>
  <legend>Favorite color</legend>
  <label><input type="radio" name="color" value="red" /> Red</label>
  <label><input type="radio" name="color" value="blue" /> Blue</label>
</fieldset>
```

- **Grouped fields:** use `<fieldset>` + `<legend>` to label the group.
- **Required fields:** mark with `required` and indicate visually with text or `*` (don't rely on color alone).
- **Error messages:** link via `aria-describedby` so they're announced.

## 🧠 Quick Self-Check

**1. Which is the BEST way to associate a label with an input?**

- [ ]  Just put the label text next to the input visually
- [x]  **`<label for="…">` matched to the input's `id`, or wrapping the input inside `<label>`**
- [ ]  Using `placeholder`
- [ ]  Using `title`

**2. Why isn't `placeholder` a substitute for `<label>`?**

- [ ]  It can't hold multiple words
- [x]  **It disappears when typing, has poor contrast, and is treated as default text by many tools**
- [ ]  It only works on `<input type="text">`
- [ ]  Screen readers can't read it

**3. Which element groups related radio buttons or checkboxes with a shared label?**

- [ ]  `<group>`
- [x]  **`<fieldset>` + `<legend>`**
- [ ]  `<section>`
- [ ]  `<div>` with `aria-group`

## ✅ Key Takeaways

- Every form input needs a **programmatically associated `<label>`**.
- Use **`for` + `id`** (most flexible) or **wrap the input** inside the label.
- `placeholder`, `title`, and adjacent text are **NOT labels**.
- For groups of inputs, use **`<fieldset>` + `<legend>`**.
- Pair labels with `aria-describedby` for help text and error messages.
- Labels make forms easier for screen readers, voice users, motor-impaired users, and everyone with bigger click targets.

---

<aside>
➡️

**Next chapter →** Introduction to WAI-ARIA — when native HTML isn't enough.

</aside>
