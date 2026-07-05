# File Paths — Slashes, Single Dot & Double Dot Explained

<aside>
✨

**Big idea:** Three little symbols power every file path you'll ever write. **`/`** (or `\` on Windows) is the **path separator**. **`.`** (single dot) means **"this folder"**. **`..`** (double dot) means **"go up one folder"**. Chain them with the separator and you can navigate anywhere in your project.

</aside>

## 🔀 The Three Key Path Symbols

| Symbol | Name | Meaning |
| --- | --- | --- |
| `/` or `\` | Path separator | Marks the break between folder/file names |
| `.` | Single dot | **The current directory** |
| `..` | Double dot | **The parent directory** (one level up) |

## ➖ 1. The Slash — Path Separator

- Marks where one folder/file name ends and the next begins.
- **Forward slash (`/`)** on macOS, Linux, and **on the web everywhere**.
- **Backslash (`\`)** on Windows file paths (but URLs still use `/`).

```
naomis-files/    → a single folder literally named "naomis-files"
naomis/files/    → a "files" folder inside a "naomis" folder
```

<aside>
💡

In web URLs and HTML attributes (`src`, `href`), **always use forward slashes**, even on Windows. Browsers don't speak backslash.

</aside>

## · 2. The Single Dot — Current Directory

- **`.`** = **"start from here, the folder I'm in"**.
- Often used to make a path *explicitly* relative.

```
./favicon.ico       → file named favicon.ico in the current folder
./images/logo.png   → logo.png inside an "images" subfolder
```

Writing `./favicon.ico` and `favicon.ico` usually behaves the same way, but the leading `./` makes it **unambiguous that this is a relative path**.

## ·· 3. The Double Dot — Parent Directory

- **`..`** = **"go up one level"**.
- Chain them to climb multiple levels: `../../` goes up two folders.

```
../styles.css            → styles.css in the parent folder
../../shared/util.js     → go up two folders, then into "shared"
```

## 🌲 Walkthrough — Following a File Tree

```
my-app/
├─ public/
│  ├─ favicon.ico
│  ├─ index.html
├─ src/
│  ├─ index.css
│  ├─ index.js
```

We're inside **`public/index.html`**. How do we link to:

| Target | Path from `public/index.html` | Why |
| --- | --- | --- |
| `favicon.ico` | `./favicon.ico` | Same folder — single dot |
| `src/index.css` | `../src/index.css` | Up one to `my-app`, then into `src` |
| `src/index.js` | `../src/index.js` | Same trick — up, then sideways |

## 🔀 Mental Model — "Walk the Tree"

Reading a relative path is like giving directions:

- Start where the current file is.
- For each `../`, **step up one folder**.
- For each `folderName/`, **step into that folder**.
- The last piece is the **file you're after**.

## ⚠️ Common Mistakes

- ❌ Mixing slashes: don't write `\` in a URL — use `/`.
- ❌ Forgetting the leading `/` for **site-root** paths (e.g., `/public/styles.css` means "from the site root", not "from current folder").
- ❌ Using too few `..` and ending up in the wrong directory — always count folders carefully against your file tree.
- ❌ Assuming `./` and `/` are the same — the first is *current folder*, the second is *site root*. Very different.

## 🧠 Quick Self-Check

**1. Which option is an absolute path?**

- [ ]  `/public/styles.css`
- [ ]  `./script.js`
- [ ]  `../src/nav.html`
- [x]  **`https://freecodecamp.org`**

**2. Which option is a relative path to the current directory?**

- [ ]  `/public/styles.css`
- [x]  **`./script.js`**
- [ ]  `../src/nav.html`
- [ ]  `https://freecodecamp.org`

**3. Which option is a relative path to the parent directory?**

- [ ]  `/public/styles.css`
- [ ]  `./script.js`
- [x]  **`../src/nav.html`**
- [ ]  `https://freecodecamp.org`

## ✅ Key Takeaways

- **`/`** (forward slash) is the universal **path separator** in web URLs and Unix paths; Windows uses `\` for files but URLs still use `/`.
- **`.`** = current folder; **`..`** = parent folder (one level up).
- `./file` is an explicit relative reference; `../file` goes up one level.
- Chain double dots to navigate multiple levels: `../../`.
- Paths starting with `/` are **absolute from the site root** — not relative.
- A path starting with `https://` (or another protocol) is an **absolute URL**.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 22 is created.)

</aside>
