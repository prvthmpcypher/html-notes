# The target Attribute — Where Links Open (_self, _blank, _parent, _top)

<aside>
✨

**Big idea:** The **`target`** attribute on `<a>` tells the browser **where to open the link**. Four main values to remember (all underscore-prefixed): **`_self`** (current tab, default), **`_blank`** (new tab), **`_parent`** (break out of the current iframe to its parent), **`_top`** (break out all the way to the topmost tab).

</aside>

## 🎯 What Is the `target` Attribute?

- Used on **anchor elements** (`<a>`) to tell the browser **where to open** the linked URL.
- Default value: **`_self`** — i.e., open in the current tab.

```html
<a href="https://freecodecamp.org" target="_blank">Visit freeCodeCamp</a>
```

This link opens the freeCodeCamp homepage in a **new browser tab**.

## 4️⃣ The Four Main `target` Values

| Value | Where the link opens |
| --- | --- |
| **`_self`** | **Current** browsing context — same tab/window. This is the **default**. |
| **`_blank`** | **New** browsing context — usually a new tab (sometimes a new window). |
| **`_parent`** | The **parent** of the current context — useful to escape an iframe back into its host page. |
| **`_top`** | The **topmost** browsing context — escapes **all** nested frames, opens in the full tab. |

<aside>
💡

Each value is **preceded by an underscore** (`_self`, not `self`). Without it, the browser treats the value as the **name of a window/frame** to target.

</aside>

## 🔍 Visualizing `_parent` vs `_top`

Imagine a page with an `<iframe>` that itself contains another `<iframe>`:

```
Top window
└── Your website
    └── iframe A
        └── iframe B  ← link clicked here
```

Clicking a link inside **iframe B**:

- `target="_self"` → opens **inside iframe B**.
- `target="_parent"` → opens **inside iframe A** (one level up).
- `target="_top"` → opens **in the full browser tab** (escape all the way out).
- `target="_blank"` → opens in a **brand-new tab**.

## 🧪 The Fifth (Experimental) Value

- **`_unfencedTop`** is part of the **experimental FencedFrame API**.
- You probably won't need it yet — it's only relevant inside fenced frames.

## ✅ Practical Tips

- For **external links**, `target="_blank"` is common so users don't lose your site.
- When using `target="_blank"`, also add **`rel="noopener noreferrer"`** for security and privacy:

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Open example</a>
```

- **`noopener`** prevents the new page from accessing `window.opener` (tabnabbing protection).
- **`noreferrer`** also strips the `Referer` header.
- For **internal links**, the default `_self` is almost always what you want — users expect navigation in the same tab.

<aside>
♿

If you open links in a new tab, consider adding visible text or an icon (↗️) so users know what to expect — surprise tabs are an accessibility annoyance.

</aside>

## 🧠 Quick Self-Check

**1. How many current target values are there to choose from?**

- [ ]  2
- [x]  **4** (`_self`, `_blank`, `_parent`, `_top`)
- [ ]  3
- [ ]  1

**2. Where will a link with `target="_blank"` open?**

- [x]  **In a new window or tab.**
- [ ]  In the same window or tab.
- [ ]  On your second monitor.
- [ ]  On Camperchan's computer.

**3. What is the default behavior when you do not set a target?**

- [ ]  Opens in a new window or tab.
- [ ]  Opens in the parent context.
- [x]  **Opens in the same window or tab.**
- [ ]  Does not open.

## ✅ Key Takeaways

- `target` tells the browser **where to open the link** from an `<a>` element.
- Four main values: **`_self`** (default, same tab), **`_blank`** (new tab), **`_parent`** (parent frame), **`_top`** (topmost tab).
- All values are **underscore-prefixed**.
- A 5th value, **`_unfencedTop`**, exists for the experimental FencedFrame API.
- When using `_blank`, pair with **`rel="noopener noreferrer"`** for security.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 20 is created.)

</aside>
