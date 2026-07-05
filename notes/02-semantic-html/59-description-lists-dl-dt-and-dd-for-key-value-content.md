# Description Lists — <dl>, <dt> & <dd> for Key–Value Content

<aside>
✨

**Big idea:** A **description list** pairs a **term** with one or more **details** — perfect for glossaries, FAQs, recipes, specs, and any **key–value** content. Three elements work together: **`<dl>`** (the list), **`<dt>`** (the term), **`<dd>`** (the description).

</aside>

## 📖 What Is a Description List?

- A semantic list of **term–description pairs**.
- Built from three elements:
    - **`<dl>`** — **d**escription **l**ist (container).
    - **`<dt>`** — **d**escription **t**erm (the key).
    - **`<dd>`** — **d**escription **d**etails (the value).
- Default rendering: terms aligned left, descriptions slightly **indented**.

## 📘 Example — A Mini Glossary

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
  <dt>JS</dt>
  <dd>JavaScript</dd>
</dl>
```

- Two acronyms with their expansions.
- Browser indents each `<dd>` to visually separate it from its `<dt>`.

## 🍪 Example — A Recipe (Ingredient → Amount)

```html
<dl>
  <dt>Flour</dt>
  <dd>2 cups</dd>
  <dt>Sugar</dt>
  <dd>1/2 cup</dd>
  <dt>Vegetable Oil</dt>
  <dd>2 tablespoons</dd>
</dl>
```

Each ingredient is the **term**, each measurement is the **detail** — a clean key–value structure.

## 🧩 The Three Elements

| Element | Stands for | Role |
| --- | --- | --- |
| `<dl>` | Description list | Container wrapping the whole list |
| `<dt>` | Description term | The **key** — the term being described |
| `<dd>` | Description details | The **value** — description, definition, or related info |

## 🔁 Multiple Terms or Multiple Details

You're **not limited to one `<dt>` + one `<dd>`** per pair.

### One term, multiple details

```html
<dl>
  <dt>JavaScript</dt>
  <dd>A programming language for the web.</dd>
  <dd>Standardized by ECMA International as ECMAScript.</dd>
</dl>
```

### Multiple terms, one shared description

```html
<dl>
  <dt>JS</dt>
  <dt>JavaScript</dt>
  <dd>The programming language of the web.</dd>
</dl>
```

## 📈 Great Use Cases

- 📖 **Glossaries** — terms and definitions.
- 🛒 **Product specifications** — spec name + value.
- ❓ **FAQs** — question + answer.
- 📛 **Contact info** — label + value (Email, Phone, Address…).
- 🔖 **Metadata** — "Author", "Published", "Tags", etc.
- 🍳 **Recipes** — ingredient + amount.

<aside>
💡

If your data fits the shape **"label → related value"**, a description list is usually the most semantic choice — better than a `<ul>` with custom formatting or a table with one row.

</aside>

## ⚠️ Common Mistakes

- ❌ Using `<dl>` for ordered or unordered lists — use `<ol>`/`<ul>` instead.
- ❌ Forgetting that the **order matters**: `<dt>` first, then its `<dd>`(s).
- ❌ Wrapping each pair in `<div>` or `<li>` — description lists have their own grammar; don't nest with the wrong containers.
- ❌ Using `<dt>`/`<dd>` outside a `<dl>`. They must live inside a `<dl>` to be valid.

## 🧠 Quick Self-Check

**1. Which HTML tag is used to define an entire description list?**

- [ ]  `dt`
- [ ]  `dd`
- [x]  **`dl`**
- [ ]  `li`

**2. Which HTML tag is used to represent a term in a description list?**

- [ ]  `dl`
- [x]  **`dt`**
- [ ]  `dd`
- [ ]  `li`

**3. Which HTML tag is used to define or provide more details about a term in a description list?**

- [ ]  `dl`
- [ ]  `dt`
- [x]  **`dd`**
- [ ]  `li`

## ✅ Key Takeaways

- A **description list** is for **term → description** (key–value) content.
- Three elements: **`<dl>`** (container), **`<dt>`** (term), **`<dd>`** (details).
- A single `<dt>` can have multiple `<dd>`s; multiple `<dt>`s can share one `<dd>`.
- Browsers indent `<dd>` by default to visually separate it from its `<dt>`.
- Use it for **glossaries, FAQs, specs, contact info, metadata, recipes** — anywhere you have key–value pairs.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
