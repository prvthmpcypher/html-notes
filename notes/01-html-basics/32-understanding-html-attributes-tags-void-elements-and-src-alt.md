# Understanding HTML Attributes — Tags, Void Elements & src/alt

<aside>
✨

**Big idea:** HTML describes a page's **content & structure** through *elements*. Most elements have **opening + closing tags** with content in between — but some (**void elements** like `<img>`) have only a start tag. **Attributes** sit inside the opening tag (`name="value"`) and tweak how the element behaves.

</aside>

## 🌐 What Role Does HTML Play on the Web?

- **HTML** = **H**yper**T**ext **M**arkup **L**anguage — a markup language for creating web pages.
- Everything you see on a website — paragraphs, headings, links, images, videos — is **HTML doing its job**.
- HTML represents a page's **content** and **structure** through *elements*.

```html
<h1>Main heading element</h1>

<p>I am a paragraph element.</p>
```

## 🧱 Elements, Tags & Content

- An **element** is the building block of HTML.
- Most elements have **three parts**:
    - **Opening tag** → `<p>`
    - **Content** → text or other elements
    - **Closing tag** → `</p>`
- The content sandwiched between the two tags is what the browser renders.

```html
<p>I love coding!</p>
```

## 🔚 Opening vs Closing Tags

- Both tags start with `<` and end with `>`.
- The **tag name** goes between the angle brackets.
- What makes a closing tag a *closing* tag → the **forward slash `/`** right after `<`.

```html
<p>   <!-- opening -->
</p>  <!-- closing -->
```

<aside>
💡

Tag names are **case-insensitive** — `<P>` and `<p>` both work — but **lowercase is the universally accepted convention**.

</aside>

## 🚫 Void Elements (No Closing Tag)

- Some elements have **no closing tag** and **no content**. These are called **void elements**.
- They only have a **start tag**.

```html
<img>
```

- You'll also see void elements written with a `/` before the `>`:

```html
<img />
```

<aside>
⚠️

Per the HTML spec, the trailing `/` in `<img />` **does not** mark it as self-closing — it's *unnecessary and has no effect*. But many formatters (e.g. Prettier) add it, so you'll see **both forms in the wild** — get comfortable with both.

</aside>

Common void elements: `<img>`, 
``, `<hr>`, `<input>`, `<meta>`, `<link>`.

## 🏷️ HTML Attributes

- An **attribute** is a special value placed inside an element's opening tag that **adjusts the element's behavior**.
- Format: `name="value"` inside the opening tag.

```html
<element attribute="value">content</element>
```

Attributes let you do things like:

- Point an image at a file (`src`)
- Describe an image for screen readers (`alt`)
- Make a link clickable to a URL (`href`)
- Add a CSS class (`class`)

## 🖼️ The `img` Element — `src` & `alt`

### `src` — *where* the image lives

The `src` attribute specifies the **location (URL or path)** of the image.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" />
```

### `alt` — *describe* the image

The `alt` attribute provides **short, descriptive text** for the image:

- Shown when the image fails to load.
- Read aloud by screen readers (huge for accessibility).
- Used by search engines to understand the image.

```html
<img
	src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"
	alt="Two tabby kittens sleeping together on a couch."
/>
```

<aside>
💡

If the `src` is broken, the browser shows the `alt` text instead. Try mistyping the URL — you'll see the description appear in place of the image.

</aside>

## 🧩 Is HTML Alone Enough?

It depends:

- ✅ **Small practice project** with just text & images → HTML alone might be fine.
- ❌ **Modern professional website** → you'll need **HTML + CSS + JavaScript**.

### 🏠 The Building Analogy

| Tech | Role in a building |
| --- | --- |
| **HTML** | Blocks, concrete, iron — the **structure & foundation** |
| **CSS** | Interior & exterior **design** — what makes it look good |
| **JavaScript** | **Electrical & plumbing** — interactivity & behavior |

## 🧠 Quick Self-Check

**1. What does HTML stand for?**

- [ ]  HyperText Maker Language
- [ ]  HyperText Marker Language
- [ ]  HyperText Markdown Language
- [x]  **HyperText Markup Language**

**2. Which of the following is the correct syntax for a closing tag?**

- [ ]  `<;p>`
- [ ]  `<p>`
- [x]  **`</p>`**
- [ ]  `<///p/>`

**3. Which of the following is a valid attribute used inside the `img` element?**

- [x]  **`src`**
- [ ]  `bold`
- [ ]  `closing`
- [ ]  `div`

## ✅ Key Takeaways

- HTML defines a page's **content & structure** using *elements*.
- Most elements = **opening tag + content + closing tag**. Closing tag has a `/`.
- **Void elements** (`<img>`, 
``, `<hr>`, `<input>`...) have **no closing tag** and **no content**.
- **Attributes** sit inside the opening tag as `name="value"` and tweak the element's behavior.
- For `<img>`: **`src`** = where the image is, **`alt`** = describe it (accessibility + fallback).
- HTML alone isn't enough for a real-world site — pair it with **CSS** (style) and **JavaScript** (interactivity).

---

<aside>
➡️

**Next chapter →** *Level up on attributes — master **`href`** + **`target`** for links, recap **`src`** / **`alt`**, and meet boolean attributes like **`checked`**, **`disabled`**, **`required`**.* (Link will be added when chapter 3 is created.)

</aside>
