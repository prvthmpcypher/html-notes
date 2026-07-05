# Open Graph Tags — Controlling How Links Look on Social Media

<aside>
✨

**Big idea:** **Open Graph (OG) tags** are `<meta>` elements that control how your page **previews on social media** — Facebook, LinkedIn, X, Slack, Discord, and more. Set `og:title`, `og:type`, `og:image`, and `og:url` and your shared links go from plain URLs to rich, click-worthy cards.

</aside>

## 🔗 What Is the Open Graph Protocol?

- A standard (originally from Facebook) that lets you control how your **website's content appears** when shared on social platforms.
- Set via a collection of `<meta>` elements inside the **`<head>`** of your HTML document.
- Used by Facebook, LinkedIn, X (Twitter), Pinterest, Slack, Discord, iMessage — basically every link-previewing platform.

## 🔑 The 4 Most Important OG Properties

Four OG properties cover the **vast majority of use cases**:

| Property | What it sets |
| --- | --- |
| `og:title` | The **title** shown on the link preview card |
| `og:type` | The **kind** of content (e.g. `website`, `article`, `video`, `music`) |
| `og:image` | The **preview image** displayed on the card |
| `og:url` | The **canonical URL** the preview should point to |

### 1️⃣ `og:title`

```html
<meta content="freeCodeCamp.org" property="og:title" />
```

- `property="og:title"` → declares this as the Open Graph title.
- `content="..."` → the title text shown in the social card.

### 2️⃣ `og:type`

```html
<meta property="og:type" content="website" />
```

Common values: `website`, `article`, `video.movie`, `music.song`, `book`, `profile`.

### 3️⃣ `og:image`

```html
<meta
  content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
  property="og:image"
/>
```

- High-quality, well-proportioned images perform best.
- **Facebook recommendation:** use at least **1200 × 630 px** for best display on high-resolution devices; minimum **600 × 315 px**.

### 4️⃣ `og:url`

```html
<meta property="og:url" content="https://www.freecodecamp.org" />
```

The canonical URL the preview links back to.

## 🧩 A Complete Example — The Big Four in `<head>`

```html
<head>
  <meta charset="UTF-8" />
  <title>freeCodeCamp.org</title>
  <meta name="description" content="Learn to code — for free." />

  <!-- Open Graph -->
  <meta property="og:title" content="freeCodeCamp.org" />
  <meta property="og:type" content="website" />
  <meta property="og:image"
        content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png" />
  <meta property="og:url" content="https://www.freecodecamp.org" />
</head>
```

## 📦 Other Useful OG Properties

| Property | What it sets |
| --- | --- |
| `og:description` | Short summary shown under the title |
| `og:locale` | Language/region (e.g. `en_US`, `pt_BR`) |
| `og:site_name` | Overall site name (e.g. "freeCodeCamp") |
| `og:audio` | Audio file URL |
| `og:video` | Video file URL |

<aside>
💡

For X (Twitter), there's a parallel set of **Twitter Card meta tags** (`twitter:card`, `twitter:title`, `twitter:image`). X will fall back to OG tags if no Twitter-specific tags are set.

</aside>

## 📈 How OG Tags Affect SEO

- **Directly?** They aren't ranking signals — search engines don't rank you higher because you set them.
- **Indirectly?** Strong previews → higher **click-through rates** on social shares → more traffic → stronger engagement signals → better SEO over time.
- They also improve **brand consistency** and **shareability**, which keeps users coming back.

## 🧪 Test Your Tags

Most platforms provide a **link debugger** so you can preview how your page will look:

- Facebook Sharing Debugger
- LinkedIn Post Inspector
- X Card Validator
- [OpenGraph.xyz](http://OpenGraph.xyz) (works for any URL)

## 🧠 Quick Self-Check

**1. What are open graph properties used for?**

- [ ]  For embedding interactive multimedia content directly into web pages.
- [x]  **To set how your website's content will be seen on different social media platforms.**
- [ ]  For generating dynamic pop-up advertisements on websites.
- [ ]  For encrypting sensitive data transmitted between web servers and users' browsers.

**2. What does `property="og:title"` do in the meta element?**

- [ ]  It automatically adjusts the font size and style of the webpage title based on user preferences.
- [ ]  It directs the browser to display a specific emoticon or emoji as the title of the webpage.
- [ ]  It causes the webpage to play a specific audio file when the title is displayed in the browser tab.
- [x]  **It specifies the title of your web page content when it is shared on social media platforms.**

**3. What does `property="og:type"` do in the meta element?**

- [ ]  It selects the page's default font style.
- [ ]  It triggers a pop-up advertisement when the webpage is loaded.
- [x]  **It specifies the type of content used for your web page when it is shared on social media platforms.**
- [ ]  It changes the webpage's background color based on the user's time zone.

## ✅ Key Takeaways

- Open Graph tags are `<meta>` elements that control **social media link previews**.
- The **four essential properties**: `og:title`, `og:type`, `og:image`, `og:url`.
- Use **high-quality images** — at least **1200 × 630 px** for best display.
- They don't directly improve SEO but **boost click-through rates** on shared links.
- Test your tags with Facebook/LinkedIn/X debuggers before pushing to production.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 13 is created.)

</aside>
