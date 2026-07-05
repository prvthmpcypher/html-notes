# The HTML Boilerplate — DOCTYPE, <html>, <head> & <body>

<aside>
✨

**Big idea:** An **HTML boilerplate** is the ready-made skeleton every webpage starts with — `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>`. It guarantees your page is structured correctly, works across browsers, and includes the metadata browsers need to render it properly.

</aside>

## 🧱 What Is an HTML Boilerplate?

- A **boilerplate** is a ready-made template containing the basic structure every HTML document needs.
- Think of it as the **foundation of a house** — you don't pour the concrete every time you build a room.
- It **saves time** and **prevents common setup mistakes**.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1.0" />
    <title>freeCodeCamp</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
  </body>
</html>
```

## 🔨 Breaking Down the Boilerplate

### 1️⃣ `<!DOCTYPE html>`

```html
<!DOCTYPE html>
```

- Tells browsers **which version of HTML** you're using — in modern code, **HTML5**.
- Must be the **very first line** of the document.
- Without it, browsers may fall back to "quirks mode" and render the page incorrectly.

### 2️⃣ The `<html>` Element

```html
<!DOCTYPE html>
<html lang="en">
  <!-- All other elements go inside here -->
</html>
```

- The **root element** — wraps every other element on the page.
- The **`lang`** attribute declares the page's **primary language** (here, English). Important for screen readers, search engines, and translation tools.

### 3️⃣ `<head>` & `<body>`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <!-- Important metadata goes here -->
  </head>
  <body>
    <!-- Headings, paragraphs, images, etc. go inside here -->
  </body>
</html>
```

| Section | Purpose |
| --- | --- |
| `<head>` | Behind-the-scenes metadata — *not* shown on the page |
| `<body>` | Visible content — what users actually see |

## 🧠 Inside the `<head>`

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Document Title Goes Here</title>
  <link rel="stylesheet" href="./styles.css" />
</head>
```

| Element | What it does |
| --- | --- |
| `<meta charset="UTF-8">` | Sets the character encoding so all text characters render correctly |
| `<meta name="viewport" ...>` | Makes the page responsive on mobile devices |
| `<title>` | Text shown in the browser tab / window title |
| `<link rel="stylesheet">` | Connects external CSS files |

<aside>
💡

Metadata in `<meta>` elements also controls how sites like X (Twitter), LinkedIn, and Facebook **preview your page link**. You'll cover that in the Open Graph chapter.

</aside>

## 👁️ Inside the `<body>`

```html
<body>
  <h1>I am a main title</h1>
  <p>Example paragraph text</p>
</body>
```

- The `<body>` holds **everything visible** — headings, paragraphs, images, links, forms, you name it.

## ✨ Why Use a Boilerplate?

- ✅ Ensures pages are **structured correctly** and **cross-browser compatible**.
- ✅ Helps you **avoid common setup mistakes** (missing charset, viewport, etc.).
- ✅ Enforces **best practices** from line one.
- ✅ Gives you a **solid starting point** every time you spin up a new project.
- 💡 As you grow, you'll **customize your own boilerplate** with your favorite meta tags, scripts, and conventions.

## 🧠 Quick Self-Check

**1. Where would you set the character encoding for your page?**

- [ ]  A `meta` element in the `body`.
- [ ]  A `head` element in the `body`.
- [x]  **A `meta` element in the `head`.**
- [ ]  In the `DOCTYPE`.

**2. Where would you set the language for your page?**

- [x]  **In the opening `html` tag.**
- [ ]  A `meta` element in the `body`.
- [ ]  A `head` element in the `body`.
- [ ]  A `meta` element in the `head`.

**3. What purpose does a boilerplate serve?**

- [ ]  Provides a starting structure for your websites.
- [ ]  Ensures you are not missing any essential elements.
- [ ]  Allows you to get started writing the content of your page faster.
- [x]  **All of the above.**

## ✅ Key Takeaways

- A boilerplate = ready-made HTML skeleton: `<!DOCTYPE html>` + `<html>` + `<head>` + `<body>`.
- **`<!DOCTYPE html>`** declares HTML5 and must be the **first line**.
- **`<html lang="...">`** wraps everything and sets the page's primary language.
- **`<head>`** holds invisible metadata (`<meta>`, `<title>`, `<link>`).
- **`<body>`** holds everything users see.
- Using a boilerplate saves time, prevents mistakes, and bakes best practices into every project.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 6 is created.)

</aside>
