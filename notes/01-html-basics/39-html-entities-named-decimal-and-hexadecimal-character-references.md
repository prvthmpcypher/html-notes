# HTML Entities — Named, Decimal & Hexadecimal Character References

<aside>
✨

**Big idea:** HTML entities (a.k.a. **character references**) let you display **reserved characters** like `<`, `>`, `&`, `"`, and special symbols (©, €, Ω) as **text** — without the browser interpreting them as HTML. They come in three flavors: **named**, **decimal numeric**, and **hexadecimal numeric**.

</aside>

## 🔣 What Is an HTML Entity?

- An **HTML entity** (also called a **character reference**) is a set of characters used to represent a **reserved character** in HTML.
- Needed because some characters — like `<`, `>`, `&`, `"` — have **special meaning** in HTML and would otherwise be parsed as code.

### 🚫 The Problem

```html
<p>This is an <img /> element</p>
```

This won't show `This is an <img /> element` on the page. The HTML parser sees `<img />` and tries to render an **actual image element**.

### ✅ The Fix

```html
<p>This is an &lt;img /&gt; element</p>
```

Now the page literally shows `This is an <img /> element`, because `&lt;` and `&gt;` are entity codes for `<` and `>`.

## 🔤 1. Named Character References

- Start with **`&`**, end with **`;`**.
- Use a **human-readable name** in between.
- Easiest to read and remember.

```html
&lt;   &gt;   &amp;   &quot;   &apos;
```

| Entity | Renders as | Meaning |
| --- | --- | --- |
| `&lt;` | `<` | Less-than sign |
| `&gt;` | `>` | Greater-than sign |
| `&amp;` | `&` | Ampersand |
| `&quot;` | `"` | Double quote |
| `&apos;` | `'` | Single quote / apostrophe |
| `&copy;` | © | Copyright |
| `&reg;` | ® | Registered trademark |
| `&nbsp;` | (space) | Non-breaking space |

## 🔢 2. Decimal Numeric References

- Start with **`&#`**, followed by one or more **decimal digits**, ending with **`;`**.
- Each character has a unique decimal Unicode code point.

```html
&#60;   <!-- < -->
&#62;   <!-- > -->
&#169;  <!-- © copyright -->
&#174;  <!-- ® registered trademark -->
```

## 🔢 3. Hexadecimal Numeric References

- Start with **`&#x`**, followed by one or more **hex digits** (`0–9`, `A–F`), ending with **`;`**.
- Same code points as decimal, just written in **base 16**.

```html
&#x3C;     <!-- < -->
&#x3E;     <!-- > -->
&#x20AC;   <!-- € euro symbol -->
&#x03A9;   <!-- Ω Greek capital Omega -->
```

## 🎯 Three Forms, Same Character

All three of these render `<`:

```html
&lt;     <!-- named -->
&#60;    <!-- decimal -->
&#x3C;    <!-- hexadecimal -->
```

<aside>
💡

Prefer **named references** when one exists — they're easier to read. Fall back to numeric (decimal or hex) for characters without a named entity (rare emoji, niche symbols, etc.).

</aside>

## 📦 Common Useful Entities

| Symbol | Named | Decimal | Hex |
| --- | --- | --- | --- |
| `<` | `&lt;` | `&#60;` | `&#x3C;` |
| `>` | `&gt;` | `&#62;` | `&#x3E;` |
| `&` | `&amp;` | `&#38;` | `&#x26;` |
| `"` | `&quot;` | `&#34;` | `&#x22;` |
| © | `&copy;` | `&#169;` | `&#xA9;` |
| ® | `&reg;` | `&#174;` | `&#xAE;` |
| € | `&euro;` | `&#8364;` | `&#x20AC;` |
| Ω | `&Omega;` | `&#937;` | `&#x3A9;` |

## 🧠 Quick Self-Check

**1. What is an HTML entity (character reference)?**

- [ ]  A set of Google fonts.
- [ ]  A group of images and captions.
- [ ]  A set of characters used to represent JavaScript code.
- [x]  **A set of characters used to represent a reserved character in HTML.**

**2. What are the three types of character references?**

- [ ]  Named, Roman and Hexadecimal numeric character references.
- [ ]  Octal, Named and Binary character references.
- [x]  **Named, Decimal numeric, and Hexadecimal numeric character references.**
- [ ]  Asymmetric, Decimal numeric, and Hexadecimal numeric character references.

**3. Which of the following is the correct syntax for a named character reference?**

- [x]  **`&amp;`**
- [ ]  `;amp;`
- [ ]  `&amp>>`
- [ ]  `&amp&`

## ✅ Key Takeaways

- HTML entities let you display **reserved characters** as plain text.
- All three forms start with **`&`** and end with **`;`**.
- **Named** (`&lt;`) — easiest to read.
- **Decimal numeric** (`&#60;`) — `&#` + decimal digits.
- **Hexadecimal numeric** (`&#x3C;`) — `&#x` + hex digits.
- Always escape `<`, `>`, and `&` when showing them as literal text.
- Use entities for symbols too: © (`&copy;`), ® (`&reg;`), € (`&euro;`).

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 10 is created.)

</aside>
