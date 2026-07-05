# File Paths — Absolute vs Relative Paths & URLs

<aside>
✨

**Big idea:** A **path** says **where a file lives**. **Absolute paths** start from the root and spell out every folder. **Absolute URLs** add a protocol (`https://`, `file://`) and (for web resources) a domain. **Relative paths** describe location *relative to the current file* — they're shorter, portable, and ideal for links inside your own site.

</aside>

## 📍 What Is a Path?

- A **path** is a string that **specifies the location** of a file or directory in a file system.
- In web development, paths let you link to **resources**: images, stylesheets, scripts, other web pages.
- Two main flavors: **absolute** and **relative**.

## 🏠 Absolute Paths

- A **complete link to a resource**.
- Starts from the **root directory**, includes every folder along the way, ends with the filename + extension.
- The **root directory** is the top-level folder in the hierarchy (e.g., `/` on macOS/Linux, `C:\` on Windows).

```html
<p>
  Read more on the
  <a href="/Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/about.html">
    About Page
  </a>
</p>
```

This path drills down: root → `Users` → `user` → `Desktop` → `fCC` → `script-code` → `absolute-vs-relative-paths` → `pages` → `about.html`.

## 🌐 Absolute URLs

An **absolute URL** is a complete address that includes:

- The **protocol** (`http://`, `https://`, `file://`).
- The **domain name** (for web resources).
- The **path** to the file.
- The **filename + extension**.

```html
<a href="https://design-style-guide.freecodecamp.org/img/fcc_secondary_small.svg">
  View fCC Logo
</a>
```

Breakdown:

| Part | Value |
| --- | --- |
| Protocol | `https` |
| Domain | `design-style-guide.freecodecamp.org` |
| Filename | `fcc_secondary_small.svg` |

### Absolute URL on a local file

When you open a local HTML file in the browser, the address bar shows the **`file://`** protocol:

```
file:///Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/about.html
```

- Protocol: `file://`
- Path: `/Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/`
- Filename: `about.html`

## 📍 Relative Paths

- A **relative path** describes a file's location **relative to the current file's directory**.
- **No protocol, no domain** — just the path from where you are.
- Shorter, more flexible, and **portable** — moves cleanly with your site.

```html
<p>
  Read more on the
  <a href="about.html">About Page</a>
</p>
```

If `contact.html` and `about.html` are in the **same folder**, you just write the filename. The browser figures out the rest.

### Common relative path syntax

| Syntax | What it means |
| --- | --- |
| `about.html` | Same folder as the current file |
| `./about.html` | Same folder (explicit form) |
| `pages/about.html` | Inside the `pages` subfolder |
| `../about.html` | One folder up from current |
| `../../about.html` | Two folders up |
| `/about.html` | From the **site root** (server-relative) |

## ⚖️ When to Use Which

| Situation | Best choice |
| --- | --- |
| Linking to a resource on **another website** | **Absolute URL** (with `https://`) |
| Linking within **your own site** | **Relative path** |
| Linking from a fixed local location | **Absolute path** |
| Local testing without internet | **Relative path** |
| Keeping code clean & easy to maintain | **Relative path** |

<aside>
💡

**Rule of thumb:** use **relative paths** by default for anything inside your own project. Reach for an **absolute URL** only when you're linking to a different site.

</aside>

## 🧠 Quick Self-Check

**1. What are the two types of paths?**

- [ ]  Resolute and absolute paths.
- [ ]  Absolute and ultimate paths.
- [ ]  Relative and unique paths.
- [x]  **Absolute and relative paths.**

**2. How do you link to a resource available only on the internet?**

- [x]  **Absolute URL.**
- [ ]  Absolute path.
- [ ]  Relative path.
- [ ]  Both relative and absolute paths.

**3. Which protocol is used for an absolute URL on a local machine?**

- [ ]  `http://`
- [ ]  `https://`
- [x]  **`file://`**
- [ ]  `localhost`

## ✅ Key Takeaways

- A **path** points to a file's location in a file system.
- **Absolute path** = full path from the root directory.
- **Absolute URL** = absolute path + protocol (+ domain for web resources).
- **Relative path** = path relative to the current file's folder — short, portable, ideal for internal links.
- Use `.` for current folder and `..` to go up one level.
- Prefer **relative paths** for resources inside your own project; use **absolute URLs** to link to external sites.
- Local files in the browser use the **`file://`** protocol.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 21 is created.)

</aside>
