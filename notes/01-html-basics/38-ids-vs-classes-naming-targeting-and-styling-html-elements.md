# IDs vs Classes — Naming, Targeting & Styling HTML Elements

<aside>
✨

**Big idea:** Use **`id`** to label a **single, unique** element (good for targeting one specific thing). Use **`class`** to label a **group** of elements that share styles or behavior. IDs are targeted in CSS with `#`, classes with `.`.

</aside>

## 🏷️ The `id` Attribute — Unique Identifier

- Adds a **unique identifier** to an HTML element.
- Should appear on **only one element per page**.
- Targeted in CSS with `#` and in JavaScript with `document.getElementById(...)`.

```html
<h1 id="title">Movie Review Page</h1>
```

### Targeting an `id` in CSS

```css
#title {
  color: red;
}
```

The **`#`** in front of `title` means "target the element whose `id` is `title`".

## 🚫 `id` Naming Rules

- ❌ **No spaces** allowed.
- ✅ Only **letters, digits, underscores (`_`), and dashes (`-`)**.
- ✅ Should be unique — don't reuse the same `id` on multiple elements.

```html
<!-- ❌ invalid — space inside the id -->
<h1 id="main heading">Main heading</h1>

<!-- ✅ valid alternatives -->
<h1 id="main-heading">Main heading</h1>
<h1 id="main_heading">Main heading</h1>
```

<aside>
⚠️

If an `id` contains a space, browsers treat the space as part of the name — your CSS and JavaScript selectors will silently fail to match.

</aside>

## 🏷️ The `class` Attribute — Reusable Label

- A **class** is a label you can apply to **as many elements as you want**.
- Values **can contain spaces** — a space separates **multiple class names**.
- Targeted in CSS with `.` and in JavaScript with `document.querySelectorAll('.classname')`.

```html
<div class="box"></div>
```

### Multiple classes on one element

```html
<div class="box red-box"></div>
```

The element has **two classes**: `box` and `red-box`.

### Full example — styling multiple elements

```html
<body>
  <div class="box red-box"></div>
  <div class="box blue-box"></div>
  <div class="box red-box"></div>
  <div class="box blue-box"></div>
</body>
```

```css
.box {
  width: 100px;
  height: 100px;
}

.red-box {
  background-color: red;
}

.blue-box {
  background-color: blue;
}
```

- Every box gets size from `.box`.
- Red and blue colors come from their second class.

## ⚖️ `id` vs `class` at a Glance

| Aspect | `id` | `class` |
| --- | --- | --- |
| Unique on the page? | ✅ Must be unique | ❌ Can repeat freely |
| Multiple per element? | One `id` per element | Multiple class names allowed |
| Spaces in value? | ❌ No spaces | ✅ Space separates multiple classes |
| CSS selector | `#name` | `.name` |
| JS selector | `getElementById('name')` | `querySelectorAll('.name')` |
| Best for | Targeting **one specific element** | Styling **groups of elements** |

## 🧩 When to Use Which

- Use **`id`** when you need to point at **exactly one element** (e.g. `id="main-nav"`, `id="hero-title"`).
- Use **`class`** when **many elements** should share styles or behavior (e.g. `.button`, `.card`, `.red-box`).

<aside>
💡

**Rule of thumb:** classes are for **reuse**, IDs are for **uniqueness**. When in doubt, reach for a class.

</aside>

## 🧠 Quick Self-Check

**1. When should you use an `id` versus a `class`?**

- [ ]  Use a class when you want a unique identifier that should only apply to one element.
- [x]  **Use an `id` when you need a unique identifier for a specific element, and use a `class` when you want to apply styles or behavior to multiple elements.**
- [ ]  Use an `id` when you want to style multiple elements consistently across different parts of your webpage.
- [ ]  Use an `id` when you want to apply styles that can be easily overridden by other styles in your CSS.

**2. What happens if you use the same `id` more than once in your HTML?**

- [x]  **It can lead to unwanted results and issues when trying to apply styles or targeting an element in JavaScript.**
- [ ]  The program will crash.
- [ ]  Nothing will happen.
- [ ]  There will be a popup alert message in the browser window.

**3. Which of the following is NOT a correct value for the `id` attribute?**

- [ ]  `id="heading"`
- [ ]  `id="main-heading"`
- [ ]  `id="main"`
- [x]  **`id="main heading"`** (spaces are not allowed)

## ✅ Key Takeaways

- **`id`** = unique label — **one element only**, no spaces, target with `#name` in CSS.
- **`class`** = reusable label — **any number of elements**, multiple classes allowed (space-separated), target with `.name` in CSS.
- `id` values may only contain **letters, digits, underscores, and dashes**.
- Use `id` to grab **one specific element**, use `class` to style or behave across **many elements**.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 9 is created.)

</aside>
