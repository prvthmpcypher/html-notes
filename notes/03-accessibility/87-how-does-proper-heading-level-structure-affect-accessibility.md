# How Does Proper Heading Level Structure Affect Accessibility?

<aside>
✨

**Big idea:** Headings (`<h1>`–`<h6>`) are the **table of contents** of your page. Screen-reader users navigate **by heading**, so a clean, logical hierarchy is essential — never skip levels and never pick a heading because of how it looks.

</aside>

## 🔢 Headings Are Landmarks

- Screen readers offer a **headings list** that lets users **jump straight to a section**.
- Roughly **70% of screen-reader users** use heading navigation as their primary way to scan a page (WebAIM survey).
- A page with no headings — or with broken hierarchy — is like a book with no chapter titles.

## 📐 The Hierarchy Rules

1. **One `<h1>`** per page — the unique page title.
2. **`<h2>`** for major sections.
3. **`<h3>`** for subsections within `<h2>`, and so on down to `<h6>`.
4. **Never skip a level going down** (`<h1>` → `<h3>` is a bug).
5. You **may** "jump back up" — finishing an `<h3>` and starting a new `<h2>` is fine.
6. Pick headings by **meaning**, not visual size. Style with CSS.

### ✅ Correct

```html
<h1>Recipe: Apple Pie</h1>
  <h2>Ingredients</h2>
  <h2>Instructions</h2>
    <h3>Prepare the crust</h3>
    <h3>Make the filling</h3>
  <h2>Notes</h2>
```

### ❌ Incorrect — skipped level

```html
<h1>Recipe: Apple Pie</h1>
  <h3>Ingredients</h3>   <!-- jumps from h1 to h3 -->
```

### ❌ Incorrect — used for font size

```html
<p>Tip: <h2>buy fresh apples</h2></p>
```

## ♿ Why It Matters for Accessibility

- A screen-reader user pressing **H** moves to the next heading. **Skipped levels suggest missing content.**
- A clear outline helps users **build a mental model** of the page in seconds.
- Search engines also use headings to **summarize and rank** the page (SEO bonus).
- Browsers' built-in **Reader Mode** depends on heading structure for clean rendering.

## 🛠️ How to Audit Your Headings

- Open **DevTools → Accessibility tree**, or use the **WAVE** browser extension — both reveal the heading outline.
- The **HeadingsMap** extension (Chrome/Firefox) shows a live outline of any page.
- Use **`document.querySelectorAll('h1,h2,h3,h4,h5,h6')`** in the console to inspect order.
- Lighthouse flags **"Heading elements are not in a sequentially-descending order."**

## 🧠 Quick Self-Check

**1. How many `<h1>` elements should a page typically have?**

- [ ]  None
- [x]  **One**
- [ ]  Three to five
- [ ]  As many as you want

**2. Which heading sequence is INCORRECT?**

- [ ]  `<h1>` → `<h2>` → `<h2>` → `<h3>`
- [ ]  `<h1>` → `<h2>` → `<h3>` → `<h2>` (jumping back up is allowed)
- [x]  **`<h1>` → `<h3>` (skipping `<h2>`)**
- [ ]  `<h1>` → `<h2>` → `<h3>` → `<h4>`

**3. About what percentage of screen-reader users navigate primarily by headings?**

- [ ]  5%
- [ ]  25%
- [x]  **~70%**
- [ ]  100%

## ✅ Key Takeaways

- Headings are **navigation landmarks** for screen-reader users.
- Use **one `<h1>`** per page; sequential `<h2>`–`<h6>` under it.
- **Never skip levels** going down. **Don't use headings for font size** — style with CSS.
- Audit with the **accessibility tree**, **HeadingsMap**, **WAVE**, or **Lighthouse**.
- Good heading structure also boosts SEO and Reader Mode rendering.

---

<aside>
➡️

**Next chapter →** Best practices for tables and accessibility.

</aside>
