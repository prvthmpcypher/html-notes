# The <link> Element — Stylesheets, Fonts & Favicons

<aside>
✨

**Big idea:** The `<link>` element connects your HTML page to **external resources** — stylesheets, fonts, and favicons. It lives inside `<head>`, never renders visible content itself, and uses two key attributes: **`rel`** (what kind of resource) and **`href`** (where it lives).

</aside>

## 🔖 What Is the `<link>` Element?

- A **void element** (no closing tag) used to **link external resources** to your HTML document.
- Most commonly used for **external CSS stylesheets**, but also for **fonts**, **favicons**, and **prefetch/preconnect hints**.
- Always placed **inside the `<head>` element**.

```html
<link rel="stylesheet" href="./styles.css" />
```

## 🔑 Key Attributes — `rel` & `href`

| Attribute | What it does |
| --- | --- |
| `rel` | **Relationship** between the linked resource and the HTML document (e.g. `stylesheet`, `icon`, `preconnect`) |
| `href` | **Location** (URL or path) of the external resource |

<aside>
💡

The `./` in `href="./styles.css"` means **"look in the current folder"**. You'll explore more path syntax (`../`, absolute vs relative) in a later chapter on file paths.

</aside>

## 🎨 Linking an External Stylesheet

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Examples of the link element</title>
  <link rel="stylesheet" href="./styles.css" />
</head>
```

- **Best practice:** keep HTML and CSS in **separate files**.
- The `<link>` element pulls in your CSS instead of writing styles directly in the HTML document.

## 🔤 Linking Google Fonts

Professional codebases often have **multiple `<link>` elements** pulling in fonts, icons, and stylesheets. Here's an example using *Playwrite CU*:

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Playwrite+CU:wght@100..400&display=swap"
  rel="stylesheet"
/>
```

<aside>
⚡

**`rel="preconnect"`** tells the browser to **open an early network connection** to the URL in `href`. This shaves milliseconds off loading external resources like fonts.

</aside>

- **Google Fonts** = free, open-source custom fonts you can use in any project. Pick the fonts you want and Google hands you the exact HTML + CSS snippet to drop in.

## 🌟 Linking a Favicon

```html
<link rel="icon" href="favicon.ico" />
```

- A **favicon** (short for **fav**orite **icon**) is a small icon shown in the **browser tab** next to the page title — and in bookmarks, history, and tab thumbnails.
- Most sites use a favicon to display their **brand icon**.

## 📐 Common `rel` Values at a Glance

| `rel` value | What it links |
| --- | --- |
| `stylesheet` | External CSS file |
| `icon` | Favicon / browser-tab icon |
| `preconnect` | Early connection hint for a domain |
| `preload` | Tell the browser to fetch a resource early |
| `manifest` | Web App Manifest (PWA metadata) |
| `alternate` | Alternate version (e.g. RSS feed, other language) |

## 🧠 Quick Self-Check

**1. What is the role of the `<link>` element in HTML?**

- [ ]  It specifies the content type of the linked resource.
- [ ]  It determines the visibility of the linked resource on the webpage.
- [ ]  It defines the font size of the linked resource when displayed.
- [x]  **It is used to link to external resources like stylesheets and site icons.**

**2. What is the role of the `rel` attribute inside the `<link>` element?**

- [ ]  It is used to indicate the language of the linked document.
- [x]  **It is used to specify the relationship between the linked resource and the HTML document.**
- [ ]  It is used to define the media type of the linked document.
- [ ]  It is used to determine the size of the linked document.

**3. What is a favicon?**

- [ ]  A type of JavaScript file used to enhance website functionality.
- [ ]  A type of font used to style text on a website.
- [x]  **A small icon typically displayed in the browser tab next to the site title.**
- [ ]  A security feature used to prevent cross-site scripting attacks.

## ✅ Key Takeaways

- `<link>` is a **void element** that connects your HTML to external resources.
- It always lives inside **`<head>`** and is invisible to the page itself.
- Two essential attributes: **`rel`** (relationship type) and **`href`** (location).
- Most common use: **`rel="stylesheet"`** for external CSS.
- Also used for **favicons** (`rel="icon"`), **fonts**, and **performance hints** like `preconnect` and `preload`.
- Keep HTML and CSS in separate files — it's a best practice for maintainability and clarity.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 5 is created.)

</aside>
