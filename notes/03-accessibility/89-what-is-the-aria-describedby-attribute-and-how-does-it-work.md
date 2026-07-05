# What Is the aria-describedby Attribute, and How Does It Work?

<aside>
✨

**Big idea:** **`aria-describedby`** points to **one or more elements** whose text becomes the **description** of the current element. It's the perfect way to attach **help text**, **error messages**, **format hints**, or **tooltip-like context** to a form field or button. Unlike `aria-label`, it doesn't replace the name — it **adds extra info**.

</aside>

## 💬 What Is `aria-describedby`?

- Takes one or more **`id` references**, space-separated.
- The referenced text is announced **after** the element's name and role.
- Used for **secondary, supporting information** — not the primary label.
- The referenced text is **visible on screen** (unless intentionally hidden with CSS).

## 🧪 Example — Form Hint

```html
<label for="password">Password</label>
<input
  type="password"
  id="password"
  aria-describedby="pwd-hint"
/>
<p id="pwd-hint">Must contain at least 8 characters, including a number.</p>
```

Screen reader announces: **"Password, edit text, Must contain at least 8 characters, including a number."**

## 🚨 Example — Inline Error Message

```html
<label for="email">Email</label>
<input
  type="email"
  id="email"
  aria-describedby="email-error"
  aria-invalid="true"
/>
<p id="email-error" role="alert">Please enter a valid email address.</p>
```

The field's accessible *name* is still "Email," but the *description* now includes the error — read after the field is focused.

## 🔗 Multiple Descriptions

You can reference more than one ID. Useful when help text and error text are both relevant:

```html
<input
  id="username"
  aria-describedby="username-hint username-error"
/>
<p id="username-hint">3–20 characters, letters and numbers only.</p>
<p id="username-error">Usernames must be unique.</p>
```

Order is preserved — hints are announced before errors.

## ⚖️ `aria-labelledby` vs `aria-describedby`

| Aspect | `aria-labelledby` | `aria-describedby` |
| --- | --- | --- |
| Provides | The accessible **name** | The accessible **description** |
| When announced | **First** — it's what the element IS | **After** the name and role |
| Replaces other labeling? | Yes — overrides native `<label>` | No — adds extra info |
| Typical use | Dialog titles, region names, complex labels | Help text, hints, errors, tooltips |

## 🎯 Best Practices

- Keep descriptions **short and informative**.
- Reference elements that are **visible on screen** — don't hide help text with `display: none` (you hide it from screen readers too).
- Use **`aria-invalid="true"`** alongside `aria-describedby` for error states so screen readers know something is wrong.
- For **dynamic errors** (appearing after submit), add `role="alert"` or `aria-live="polite"` to the message so it's announced immediately.
- One element can be both **labelled** by something and **described** by something else — they don't conflict.

## ⚠️ Common Mistakes

- Using `aria-describedby` as the **only** label — it's the description, not the name.
- Pointing to an `id` that **doesn't exist**.
- Stuffing huge paragraphs of text in the description — long announcements frustrate screen-reader users.
- Using **`title`** for help text — it appears only on mouse hover, invisible to keyboard/voice/touch users.
- Forgetting to pair with **`aria-invalid`** when describing an error.

## 🧠 Quick Self-Check

**1. `aria-describedby` is used to provide…**

- [ ]  The element's accessible name
- [x]  **An accessible description — secondary, supporting info**
- [ ]  An ARIA role
- [ ]  A CSS class

**2. Which is its value?**

- [ ]  A string of text
- [x]  **One or more space-separated `id`s of existing elements**
- [ ]  A URL
- [ ]  A boolean

**3. When is the description announced by a screen reader?**

- [ ]  Before the element's role
- [x]  **After the element's name and role**
- [ ]  Only on click
- [ ]  Never — it's only for sighted users

## ✅ Key Takeaways

- **`aria-describedby`** adds an accessible **description** to an element.
- Takes **one or more space-separated `id`s** referring to existing on-page elements.
- Used for **help text, hints, errors, and tooltips** — not for the main name.
- Announced **after** the element's name and role.
- Pair with **`aria-invalid="true"`** for error states; use **`role="alert"`** for messages that appear dynamically.

---

<aside>
➡️

**Next chapter →** When the `alt` attribute is needed, and what good alt text looks like.

</aside>
