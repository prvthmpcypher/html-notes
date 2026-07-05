# HTML Attributes Deep Dive — href, src, alt & Boolean Attributes

<aside>
✨

**Big idea:** **Attributes** are extra values placed inside an element's opening tag that **customize its behavior** — like where a link goes (`href`), what image to load (`src`), or whether a checkbox starts ticked (`checked`). Some attributes need a value, others (**boolean attributes**) just need to *be present*.

</aside>

## 🏷️ What Are Attributes, and How Do They Work?

- An **attribute** is a value placed **inside the opening tag** of an HTML element.
- It gives the element **extra information** or controls how it behaves.
- Basic syntax:

```html
<element attribute="value"></element>
```

- The attribute **name** is followed by an `=` and the **value in quotes**.
- The value can be a **string** or a **number**, depending on the attribute.

## 🔗 Links — `<a>` with `href` & `target`

<aside>
💡

The `<a>` element (the **anchor element**) creates a hyperlink. The text between `<a>` and `</a>` is the **clickable part**.

</aside>

```html
<a href="https://www.freecodecamp.org/news/" target="_blank">Visit freeCodeCamp</a>
```

- **`href`** → the **destination URL** of the link. Without it, the link does nothing.
- **`target="_blank"`** → opens the link in a **new browser tab**.

## 🖼️ Images — `<img>` with `src` & `alt`

```html
<img
	src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"
	alt="Two tabby kittens sleeping together on a couch."
/>
```

- **`src`** → the **location of the image file** (URL or path). **Required** — without it, no image loads.
- **`alt`** → short, descriptive text shown when the image fails or read aloud by screen readers. **Not required, but strongly recommended for accessibility.**

<aside>
♿

**Accessibility** = making sure everyone, including people with disabilities, can use and understand things like websites, apps, and physical spaces. `alt` text is one of the simplest accessibility wins you can add.

</aside>

## ✅ Boolean Attributes — Presence = True

Some attributes don't need a value — just **being present** turns the behavior on. These are called **boolean attributes**.

```html
<input type="checkbox" checked />
```

- `type="checkbox"` → tells the browser this is a checkbox input.
- `checked` → boolean attribute. **Present → checked. Absent → unchecked.** No value needed.

<aside>
⚠️

You *can* write `checked="checked"`, but you **do not write** `checked="true"`, `checked="on"`, or `checked="off"`. The presence of the attribute is what matters — not what's inside the quotes.

</aside>

### 📦 Common Boolean Attributes

| Attribute | What it does |
| --- | --- |
| `checked` | Checkbox or radio button starts selected |
| `disabled` | Element can't be interacted with |
| `readonly` | Input value can't be edited (but can be read & submitted) |
| `required` | Form field must be filled before submitting |
| `autofocus` | Element auto-focuses when the page loads |
| `hidden` | Element is hidden from rendering |

### Example — disabled input

```html
<input type="text" disabled>
```

The text input above is **greyed out and unclickable**. Remove the `disabled` attribute and it becomes editable.

## 🧠 Quick Self-Check

**1. Which of the following is an example of a boolean attribute?**

- [ ]  `src`
- [ ]  `href`
- [x]  **`disabled`**
- [ ]  `alt`

**2. What is the role of an attribute in HTML?**

- [x]  **Attributes provide additional information and help define the behavior for HTML elements.**
- [ ]  Attributes change the background color of an element.
- [ ]  Attributes change the font size of an element.
- [ ]  Attributes add JavaScript functionality to an element.

**3. Which of the following is the correct syntax for a boolean attribute?**

- [x]  **`<input type="checkbox" checked>`**
- [ ]  `<input type="checkbox" checked="on">`
- [ ]  `<input type="checkbox" checked="off">`
- [ ]  `<input type="checkbox" checked="isChecked">`

## ✅ Key Takeaways

- Attributes live **inside the opening tag** and follow `name="value"` syntax.
- **`href`** = link destination on `<a>` — required for a working link.
- **`target="_blank"`** = open link in a new tab.
- **`src`** = where to load the image from — required on `<img>`.
- **`alt`** = describe the image — optional but vital for accessibility.
- **Boolean attributes** (`checked`, `disabled`, `readonly`, `required`...) work by **presence**, not value — if the attribute is there, the behavior is on.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 4 is created.)

</aside>
