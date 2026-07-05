# Heading Hierarchy — Why h1→h6 Order Matters for A11y & SEO

<aside>
✨

**Big idea:** Headings (`<h1>`–`<h6>`) are the **outline** of your page. Use them in **logical order** — never skip a level for styling reasons. Proper hierarchy makes pages **navigable for screen readers**, **rankable for search engines**, and **predictable for browsers**.

</aside>

## 🔢 The Six Heading Levels

- HTML provides **six heading elements**: `<h1>` (most important) through `<h6>` (least important).
- The number represents the **heading level** — not a font size.
- Treat your page like a text document: titles, sections, sub-sections.

## 🌟 The Rules of Structural Hierarchy

### 1️⃣ Start with a single `<h1>`

- `<h1>` is your **top-level heading** — usually the page title.
- You'll **rarely have more than one** `<h1>` per page.
- It should generally come **before all other content**.

### 2️⃣ Use `<h2>` for major sections

- `<h2>` is your **subheading** — always **after** the `<h1>`.
- You **can have many** `<h2>` elements to delineate different sections.

### 3️⃣ Never skip levels going down

- `<h3>` always comes after an `<h2>`. **Never jump from `<h1>` directly to `<h3>`.**
- Same rule applies to `<h4>`, `<h5>`, `<h6>`.

### ✅ Correct

```html
<section>
  <h1>freeCodeCamp</h1>
  <h2>Learn Front-End Development</h2>
  <h2>Learn Back-End Development</h2>
</section>
```

### ❌ Incorrect — `<h3>` appears before any `<h2>`

```html
<section>
  <h1>freeCodeCamp</h1>
  <h3>Introduction to HTML</h3>
  <h2>Learn Front-End Development</h2>
</section>
```

### ❌ Incorrect — using `<h1>` just for big text inside a paragraph

```html
<article>
  <p>
    Here is some
    <h1>Large Text</h1>
  </p>
</article>
```

Pick headings by **meaning**, not by how they look. **Use CSS for font size.**

## 🎯 Why Hierarchy Matters

### ♿ Accessibility

- Screen readers let users **jump between headings** to navigate a page.
- If you skip `<h2>` and use `<h3>` after `<h1>`, a screen-reader user may think they **missed something important**.
- Proper hierarchy = a clean, predictable outline.

### 🔍 SEO

- Search engines parse heading structure to understand **what your page is about** and which sections matter most.
- Malformed structure → worse rankings on relevant searches.

### 🖥️ Browser Compatibility

- Severely broken hierarchy can make your HTML **technically invalid**.
- When that happens, browsers **guess** how to interpret your markup — and their guesses may not match what you intended.

## 📂 Mental Model — Treat It Like a Book

A book's structure:

- **Book title** → `<h1>`
- **Chapter** → `<h2>`
- **Section in a chapter** → `<h3>`
- **Sub-section** → `<h4>`
- ...and so on.

If you saw a book with Chapter 1 jumping straight to a sub-section without naming the chapter — confusing, right? Same logic on the web.

## ✅ Do / ❌ Don't

| ✅ Do | ❌ Don't |
| --- | --- |
| Use **one** `<h1>` per page | Use multiple `<h1>`s for big banners |
| Step down one level at a time (`h2` → `h3` → `h4`) | Skip levels (`h1` → `h3`) |
| Use **many** `<h2>`s for major sections | Pick a heading because of its **default size** |
| Style headings with **CSS** | Use `<h1>` inline inside a `<p>` for emphasis |
| Audit your outline before shipping | Assume the browser will figure it out |

## 🧠 Quick Self-Check

**1. Why is structural hierarchy important?**

- [ ]  Accessibility
- [ ]  SEO
- [ ]  So browsers know what we mean
- [x]  **All of the above**

**2. Which heading element must precede an `<h3>` element?**

- [ ]  `h5`
- [x]  **`h2`**
- [ ]  `h6`
- [ ]  `h4`

**3. How should you create larger text on your page?**

- [ ]  Use any element you want, and style it with CSS.
- [ ]  Use an `h1` because it already has large text.
- [ ]  Use a `span` element.
- [x]  **Use the correct structural element, and style it with CSS.**

## ✅ Key Takeaways

- Headings `<h1>`–`<h6>` define your page's **outline** — from most to least important.
- Use **one** `<h1>` per page; use multiple `<h2>`s for sections.
- **Never skip levels** going down (`<h1>` → `<h3>` is a bug).
- Pick headings by **meaning**, not **font size** — style with CSS.
- Proper hierarchy boosts **accessibility**, **SEO**, and **browser compatibility**.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
