# The <iframe> Element — Embedding Videos, Maps & External Pages

<aside>
✨

**Big idea:** **`<iframe>`** = **inline frame**. It lets you embed external content — YouTube videos, maps, other web pages, or even raw HTML — directly inside your page. Use **`src`** to point to a URL, **`srcdoc`** to embed HTML inline, and **`allow`** to control what the embedded content can do.

</aside>

## 🖼️ What Is the `<iframe>` Element?

- **iframe** = **i**nline **frame**.
- An **inline element** used to **embed other HTML content** directly within your page.
- That "other content" can be:
    - A **video** (YouTube, Vimeo, or any video host).
    - A **map** (Google Maps, OpenStreetMap).
    - Another **web page** or **HTML document**.
    - A snippet of **raw HTML** (via `srcdoc`).

## 📺 Embedding a YouTube Video

```html
<iframe
  width="400"
  height="400"
  src="https://www.youtube.com/embed/PkZNo7MFNFg?si=-UBVIUNM3csdeiWF"
  title="Learn JavaScript - Full Course for Beginners (YouTube video)"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  referrerpolicy="strict-origin-when-cross-origin"
  allowfullscreen
></iframe>
```

| Attribute | What it does |
| --- | --- |
| `src` | URL of the page or resource you want to embed |
| `width` / `height` | Dimensions of the iframe in pixels |
| `title` | Accessible name read by screen readers — **always include one** |
| `allow` | **Allowlist** of features the embedded content can use (autoplay, clipboard-write, fullscreen…) |
| `allowfullscreen` | Boolean — lets the embedded content go fullscreen |
| `referrerpolicy` | Controls what referrer info is sent to the embedded resource |

<aside>
♿

Always add a `title` attribute — it's how screen readers announce what's inside the iframe.

</aside>

## 🔒 The `allow` Attribute — An Allowlist

- An **allowlist** defines exactly what the embedded content **can or can't do**.
- Items can be **separated by semicolons or spaces** (you can mix both).

```html
allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
```

Common allow values:

- **`autoplay`** — allow auto-playing media
- **`clipboard-write`** — allow writing to the user's clipboard
- **`encrypted-media`** — allow DRM playback
- **`fullscreen`** — allow fullscreen mode
- **`picture-in-picture`** — allow PiP video
- **`gyroscope`**, **`accelerometer`** — device-motion sensors

## 🗺️ Embedding a Map (OpenStreetMap)

```html
<h1>A Map from Openstreetmap.org Embedded with the iframe Element</h1>

<iframe
  width="425"
  height="350"
  src="https://www.openstreetmap.org/export/embed.html?bbox=3.006134033203125%2C6.150112578753815%2C3.6357879638671875%2C6.749850810550778&amp;layer=mapnik"
  title="Map of Lagos area, Nigeria"
  style="border: 1px solid black"
></iframe>
<br />
<small>
  <a href="https://www.openstreetmap.org/#map=11/6.4501/3.3210">
    View Larger Map
  </a>
</small>
```

The iframe is replaced by an interactive OpenStreetMap — try zooming in and out!

## 🧾 Embedding Raw HTML — `srcdoc`

If you want to embed direct HTML **without pointing at a URL**, use **`srcdoc`** instead of `src`:

```html
<iframe srcdoc="<h2>Hello from inside an iframe!</h2><p>This HTML lives in the parent page.</p>"></iframe>
```

- `src` → load content from a **URL**.
- `srcdoc` → load content from a **string of HTML** you supply.
- If both are set, **`srcdoc` wins** (and the browser only falls back to `src` if `srcdoc` is unsupported).

## ✅ Best Practices

- ✅ Always include a meaningful **`title`** for accessibility.
- ✅ Use **`loading="lazy"`** on offscreen iframes for a performance boost (defer load until they're scrolled near).
- ✅ Use **`allow`** to restrict embedded content to only the features it needs.
- ✅ Use **`sandbox`** to lock down untrusted embeds (disables scripts, forms, popups by default).
- ⚠️ Be careful **embedding sites you don't control** — they can change at any time and may track users.
- ⚠️ Some sites **block themselves from being iframed** with `X-Frame-Options` or `Content-Security-Policy: frame-ancestors`.

## 🧠 Quick Self-Check

**1. What does iframe mean?**

- [ ]  International frame.
- [ ]  Inline form.
- [x]  **Inline frame.**
- [ ]  Inline form element.

**2. Which attribute of the `iframe` element specifies the location of what you want to embed?**

- [x]  **`src`**
- [ ]  `url`
- [ ]  `frameborder`
- [ ]  `cross-origin`

**3. Which attribute of the `iframe` element do you use instead of `src` if you want to embed direct HTML?**

- [ ]  `html`
- [ ]  `document`
- [ ]  `srcweb`
- [x]  **`srcdoc`**

## ✅ Key Takeaways

- **`<iframe>`** = inline frame — embeds external content inside your page.
- **`src`** = URL to embed; **`srcdoc`** = raw HTML to embed.
- Use **`width`**, **`height`**, **`title`**, **`allow`**, **`allowfullscreen`**, **`referrerpolicy`** to configure behavior.
- The **`allow`** attribute is an **allowlist** — features can be separated by `;` or spaces.
- Always provide a **`title`** for accessibility.
- Embed videos (YouTube/Vimeo/any host), maps, other pages, or direct HTML.
- Use **`loading="lazy"`** and **`sandbox`** for performance and security where appropriate.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 19 is created.)

</aside>
