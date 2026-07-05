# The <script> Element — Embedding & Linking JavaScript in HTML

<aside>
✨

**Big idea:** The `<script>` element is how you bring **JavaScript** into an HTML page — either by writing code inline between the tags or, far more commonly, by linking to an **external `.js` file** with the `src` attribute. The second approach follows the **separation of concerns** principle: HTML for structure, CSS for style, JavaScript for behavior.

</aside>

## 📜 What Is the `<script>` Element?

- Used to **embed executable code** in an HTML document.
- Almost always used for **JavaScript** — the language that adds **interactivity** to web pages.
- Common uses: interactive games, image sliders, form validation, fetching data, animations.

## 🧪 Inline JavaScript

You can write JavaScript directly between the opening and closing tags:

```html
<body>
  <script>
    // alert("Welcome to freeCodeCamp");
  </script>
</body>
```

Uncomment the `alert(...)` line and a popup appears when the page loads. The `//` at the start makes the line a **JavaScript comment** — it's ignored by the browser.

<aside>
⚠️

Inline scripts work, but they **mix HTML and JS** in one file. For anything beyond a tiny demo, keep your JavaScript in a **separate file**.

</aside>

## 🔗 Linking to an External JavaScript File

Use the **`src`** attribute (short for *source*) to point to an external `.js` file:

```html
<script src="path-to-javascript-file.js"></script>
```

- `src` → the **location** of the JavaScript file (URL or file path).
- The closing `</script>` is **required**, even when `src` is used and the tag has no inline content.

## 🧱 Why External JS — Separation of Concerns

**Separation of concerns** is a design principle: **split your program into distinct sections, each handling one concern.**

| Layer | Concern | Lives in |
| --- | --- | --- |
| **HTML** | Content & structure | `.html` |
| **CSS** | Style & presentation | `.css` |
| **JavaScript** | Behavior & interactivity | `.js` |

Keeping them in separate files makes your code:

- ✅ **Easier to read** and maintain.
- ✅ **Reusable** — the same `.js` file can be loaded across multiple pages.
- ✅ **Cacheable** by browsers — faster subsequent loads.
- ✅ **Easier to debug** — tooling, linters, and editors work better on dedicated files.

## 📜 Where to Put `<script>`

There are a few common spots, each with trade-offs:

| Placement | Behavior |
| --- | --- |
| End of `<body>` | Loads after HTML — the simplest "safe" default |
| In `<head>` with `defer` | Downloads in parallel, executes after HTML is parsed |
| In `<head>` with `async` | Downloads in parallel, executes as soon as it's ready (order not guaranteed) |

<aside>
💡

You'll meet `defer` and `async` in later lessons. For now, just remember: put `<script>` at the **bottom of `<body>`** or use `defer` so your script doesn't try to run before the HTML it depends on exists.

</aside>

## 🧠 Quick Self-Check

**1. Which attribute is used to link to an external JavaScript file?**

- [ ]  The `div` attribute.
- [ ]  The `defer` attribute.
- [ ]  The `async` attribute.
- [x]  **The `src` attribute.**

**2. What is separation of concerns?**

- [ ]  It's about making sure everyone on the team has their own clear responsibilities.
- [x]  **A design principle where you separate your programs into distinct sections and have each section address a separate concern.**
- [ ]  The act of combining all aspects of a program into a single module for simplicity.
- [ ]  It involves dividing up tasks among team members without considering how they might overlap or affect each other.

**3. Which of the following is the correct syntax for linking to an external JavaScript file?**

- [ ]  `<script div="path-to-javascript-file.js"></script>`
- [ ]  `<script alt="path-to-javascript-file.js"></script>`
- [x]  **`<script src="path-to-javascript-file.js"></script>`**
- [ ]  `<script defer="path-to-javascript-file.js"></script>`

## ✅ Key Takeaways

- `<script>` embeds **executable code** (usually JavaScript) into an HTML page.
- JavaScript adds **interactivity** — games, sliders, form validation, dynamic content.
- For anything beyond a tiny demo, **link an external `.js` file** with `<script src="..."></script>`.
- The closing `</script>` tag is **always required**, even with `src`.
- **Separation of concerns:** HTML for content, CSS for style, JS for behavior — keep them in separate files.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 11 is created.)

</aside>
