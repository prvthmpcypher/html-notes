# UTF-8 Character Encoding — What It Is & Why Every HTML File Needs It

<aside>
✨

**Big idea:** **UTF-8** is the universal character encoding for the web. Setting `<meta charset="UTF-8">` in your `<head>` guarantees that every character — from `é` and `ñ` to 中文, عربي, ひらがな, and 😀 — renders correctly on the page.

</aside>

## 🔤 What Is UTF-8 Character Encoding?

- **UTF-8** = **U**CS **T**ransformation **F**ormat — **8**-bit.
- A **standardized character encoding** widely used on the web (used by **~98% of all websites**).
- **Character encoding** = the method computers use to **store characters as data**.
- All text on a webpage is a **sequence of characters stored as one or more bytes**.

<aside>
💡

A **byte** is a unit of data made of **8 bits** (binary digits — each a `0` or `1`). UTF-8 stores each character in **1 to 4 bytes**.

</aside>

## 🌐 Why UTF-8?

- Supports **every character in the Unicode character set** — including:
    - All writing systems and languages (English, Hindi, Mandarin, Arabic, Cyrillic…)
    - Mathematical and technical symbols
    - Emojis 🎉💯
- Backward-compatible with **ASCII** (the original 7-bit English-only encoding).
- Without the right encoding, characters like `é`, `ñ`, or `€` may show up as **mojibake** (e.g. `CafÃ©` instead of `Café`).

## 🧩 Setting UTF-8 in HTML

Add this `<meta>` element inside `<head>`:

```html
<meta charset="UTF-8" />
```

The **`charset`** attribute is what tells the browser which encoding to use.

### Full example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Examples of the UTF-8 encoding</title>
  </head>
  <body>
    <p>Café</p>
  </body>
</html>
```

Thanks to `charset="UTF-8"`, the **`é`** in *Café* displays correctly.

<aside>
✅

**Best practice:** include `<meta charset="UTF-8">` in **every new HTML project**. Place it as the **first child of `<head>`**, before any text-containing tags like `<title>`.

</aside>

## 🔍 Bits, Bytes & Encoding — The Mental Model

| Term | Meaning |
| --- | --- |
| **Bit** | A single binary digit — `0` or `1` |
| **Byte** | **8 bits** grouped together — the basic unit of data |
| **Character encoding** | The mapping between **characters** (like `A`, `é`, 中) and the **bytes** that represent them |
| **Unicode** | The universal character set — a catalog of every character across human languages and symbols |
| **UTF-8** | The most popular **encoding** of Unicode — 1–4 bytes per character |

## 🧠 Quick Self-Check

**1. Which attribute is used to set the UTF-8 character encoding for HTML documents?**

- [ ]  `pattern`
- [ ]  `content`
- [x]  **`charset`**
- [ ]  `lang`

**2. What is character encoding?**

- [x]  **A method computers use to store characters as data.**
- [ ]  A way to compress text files.
- [ ]  It determines the font used to display text on a screen.
- [ ]  It refers to the process of converting spoken language into written text.

**3. How many bits are inside of a byte?**

- [ ]  1
- [ ]  3
- [ ]  37
- [x]  **8**

## ✅ Key Takeaways

- **UTF-8** = the universal web character encoding — supports every Unicode character.
- A **byte** is **8 bits**; UTF-8 uses **1–4 bytes** per character.
- Set it with **`<meta charset="UTF-8">`** as the first thing inside `<head>`.
- Without it, accented and non-Latin characters can display as garbled text (mojibake).
- Include this `<meta>` tag in **every** new HTML project — it's part of the boilerplate.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 7 is created.)

</aside>
