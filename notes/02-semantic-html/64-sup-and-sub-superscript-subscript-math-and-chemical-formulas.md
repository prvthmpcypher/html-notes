# <sup> & <sub> — Superscript, Subscript, Math & Chemical Formulas

<aside>
✨

**Big idea:** **`<sup>`** raises text above the baseline (exponents, ordinals, footnote markers). **`<sub>`** lowers text below the baseline (chemical formulas, variable indices, footnotes). They're **semantic** — use them when the position carries meaning, not just for style. For visual-only effects, use **CSS**.

</aside>

## 🔝 The `<sup>` Element — Superscript

- Displays text **above the normal baseline** in smaller type.
- A **superscript** is any symbol or letter printed above the line of text.
- Use it when the raised position carries **typographic meaning**.

```html
<p>2<sup>2</sup> (2 squared) is 4.</p>
```

Renders as: 2² (2 squared) is 4.

### Common uses

- **Exponents / powers** — `2<sup>2</sup>`, `x<sup>n</sup>`
- **Ordinal numbers** — `1<sup>st</sup>`, `2<sup>nd</sup>`, `3<sup>rd</sup>`
- **Superior lettering** (abbreviations) — `M<sup>gr</sup>` for *Monseigneur*
- **Footnote markers** — `...some claim.<sup>1</sup>`

### Example — superior lettering

```html
<p>
  Monseigneur is often written as <strong>M<sup>gr</sup></strong>.
</p>
```

## 🔟 The `<sub>` Element — Subscript

- Displays text **below the normal baseline** in smaller type.
- Use it when the lowered position carries **meaning**.

```html
<p>CO<sub>2</sub></p>
```

Renders as: CO₂

### Common uses

- **Chemical formulas** — `H<sub>2</sub>O`, `CO<sub>2</sub>`, `C<sub>6</sub>H<sub>12</sub>O<sub>6</sub>`
- **Mathematical variable subscripts** — `x<sub>1</sub>`, `a<sub>n</sub>`
- **Footnote references** in certain academic styles
- **Isotope notation** in chemistry/physics

## ⚖️ `<sup>` vs `<sub>` at a Glance

| Aspect | `<sup>` (Superscript) | `<sub>` (Subscript) |
| --- | --- | --- |
| Position | **Above** the baseline | **Below** the baseline |
| Font size | Smaller | Smaller |
| Common uses | Exponents, ordinals, footnote markers | Chemical formulas, variable indices |
| Typical example | 2², 1ˢᵗ | H₂O, x₁ |

## 🎨 When to Use CSS Instead

If you want to **raise or lower text purely for visual styling** — with no semantic meaning — reach for CSS:

```css
.tiny-baseline {
  vertical-align: super;
  font-size: 0.75em;
}
```

<aside>
💡

**Quick test:**

- Does the **position** carry meaning (exponent, isotope, ordinal)? → Use `<sup>` or `<sub>`.
- Is it **decorative**? → Use CSS (`vertical-align`, `font-size`).
</aside>

## 🧩 More Examples

```html
<!-- Math: exponent -->
<p>Einstein: E = mc<sup>2</sup>.</p>

<!-- Ordinal number -->
<p>The 21<sup>st</sup> century began in 2001.</p>

<!-- Footnote marker -->
<p>Most experts agree.<sup>1</sup></p>

<!-- Chemistry: water -->
<p>H<sub>2</sub>O is essential for life.</p>

<!-- Chemistry: glucose -->
<p>Glucose: C<sub>6</sub>H<sub>12</sub>O<sub>6</sub></p>

<!-- Variable indices in math -->
<p>The sequence x<sub>1</sub>, x<sub>2</sub>, ..., x<sub>n</sub> converges.</p>
```

## ⚠️ Common Mistakes

- ❌ Using `<sup>` / `<sub>` purely for **decoration** — use CSS instead.
- ❌ Swapping them — chemicals use `<sub>` (CO₂), exponents use `<sup>` (x²).
- ❌ Forgetting that they affect **line-height** in dense paragraphs — use sparingly in body copy.
- ❌ Typos like `<sutp>` or `<sul>` — those aren't real elements.

## 🧠 Quick Self-Check

**1. What is the primary use of the superscript element in HTML?**

- [ ]  To display text in a different color.
- [ ]  To show text in a smaller font size.
- [x]  **To display text as a superscript above the normal line of text.**
- [ ]  To underline text.

**2. Which of the following is an example of using the superscript element correctly?**

- [ ]  `<p>2<sub>2</sub> (2 squared) is 4.</p>`
- [x]  **`<p>2<sup>2</sup> (2 squared) is 4.</p>`**
- [ ]  `<p>2<sul>2</sul> (2 squared) is 4.</p>`
- [ ]  `<p>2<sutp>2</sutp> (2 subscript) is 4.</p>`

**3. What should be used instead of the `sup` element when text is raised purely for visual or styling purposes?**

- [ ]  The `sub` element.
- [x]  **CSS**
- [ ]  The `strong` element.
- [ ]  The `em` element.

## ✅ Key Takeaways

- **`<sup>`** = superscript (raised, smaller). Used for exponents, ordinals, footnote markers, superior lettering.
- **`<sub>`** = subscript (lowered, smaller). Used for chemical formulas, variable indices, isotopes.
- Both are **semantic** — they convey meaning about the position, not just style.
- For **purely visual** effects, use CSS (`vertical-align`, `font-size`).
- Common pairs: **CO₂** uses `<sub>`, **E = mc²** uses `<sup>`.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
