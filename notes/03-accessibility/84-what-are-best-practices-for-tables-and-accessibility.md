# What Are Best Practices for Tables and Accessibility?

<aside>
✨

**Big idea:** Use the table element **only for tabular data** — rows and columns of related information. Make every table accessible with a `<caption>`, proper `<th>` headers with `scope` attributes, and meaningful `<thead>`/`<tbody>` grouping. **Never use tables for layout.**

</aside>

## 📊 When to Use a Table

Use the `<table>` element only for **two-dimensional data** where rows and columns are meaningful — pricing grids, sports stats, schedules, financial reports.

**Don't** use tables for:

- Page layout (use CSS Grid / Flexbox instead).
- Single-column lists (use `<ul>`/`<ol>`).
- Key-value pairs (use `<dl>` description lists).

## 🧱 The Building Blocks

| Element | Purpose |
| --- | --- |
| **table** | The container |
| **caption** | Title/description of the table — first child of `<table>` |
| **thead** | Group of header rows |
| **tbody** | Group of data rows |
| **tfoot** | Group of footer rows (totals, summaries) |
| **tr** | A row |
| **th** | A header cell — boldfaced by default, announced as a header by screen readers |
| **td** | A data cell |

## ✅ A Fully Accessible Table

```html
<table>
  <caption>Monthly book sales by genre, 2024</caption>
  <thead>
    <tr>
      <th scope="col">Genre</th>
      <th scope="col">January</th>
      <th scope="col">February</th>
      <th scope="col">March</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Fiction</th>
      <td>120</td>
      <td>140</td>
      <td>135</td>
    </tr>
    <tr>
      <th scope="row">Non-fiction</th>
      <td>80</td>
      <td>95</td>
      <td>110</td>
    </tr>
  </tbody>
</table>
```

Key moves:

- **`<caption>`** describes what the table contains — screen readers announce this first.
- **`<th scope="col">`** tells assistive tech "this cell heads a column."
- **`<th scope="row">`** tells assistive tech "this cell heads a row."
- **`<thead>` / `<tbody>`** group rows logically.

## 🧰 More Advanced Markup

- **`scope="colgroup"` / `scope="rowgroup"`** for headers spanning multiple columns/rows.
- For very complex tables, link cells to multiple headers with **`id` + `headers`**:

```html
<th id="name">Name</th>
<th id="sales">Sales</th>
<td headers="name">Alice</td>
<td headers="sales">$1,200</td>
```

- **`<colgroup>` + `<col>`** can apply styling or semantic grouping to columns.

## 🚫 Anti-Patterns

- Using `<table>` for layout (legacy 1990s technique).
- Skipping `<caption>` — readers don't know what the table is about.
- Using `<td>` for header cells with bold styling instead of `<th>`.
- Forgetting `scope` — screen readers can't always infer the relationship.
- Nesting tables inside tables (confusing for assistive tech).
- Using `display: none` on important table content (it's hidden from screen readers too).

## 🧠 Quick Self-Check

**1. Which element gives a table its title/description?**

- [ ]  `<title>`
- [x]  **`<caption>`**
- [ ]  `<header>`
- [ ]  `<thead>`

**2. Which attribute marks whether a `<th>` heads a row or a column?**

- [ ]  `type`
- [x]  **`scope`**
- [ ]  `role`
- [ ]  `axis`

**3. When should you use a `<table>` for page layout?**

- [ ]  When you want a grid
- [ ]  When CSS feels too hard
- [x]  **Never — use CSS Grid / Flexbox instead. `<table>` is only for tabular data.**
- [ ]  When you have more than 5 columns

## ✅ Key Takeaways

- Tables are for **two-dimensional data**, not layout.
- Always include a **`<caption>`** as the first child.
- Use **`<th>` with `scope="col"` / `scope="row"`** to mark headers.
- Group rows with **`<thead>`**, **`<tbody>`**, **`<tfoot>`**.
- For complex tables, use **`id` + `headers`** to link data to headers.
- Don't nest tables, don't use `<td>` as a header, and never hide important rows with `display: none`.

---

<aside>
➡️

**Next chapter →** Why every input needs an associated label.

</aside>
