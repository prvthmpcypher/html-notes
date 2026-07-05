# <u>, <s> & <ruby> — Annotations, Strikethrough & East Asian Pronunciation

<aside>
✨

**Big idea:** Three semantic helpers for special text annotations. **`<u>`** marks **non-textual annotations** (like spelling errors). **`<s>`** marks text that's **no longer accurate or relevant**. **`<ruby>`** (with `<rt>` + `<rp>`) shows **pronunciation hints**, typically above East Asian characters.

</aside>

## ∄ The `<u>` Element — Unarticulated Annotation

- Stands for **"unarticulated annotation"**.
- Represents inline text with **non-textual annotation** applied.
- Default styling: **black underline** below the text.
- Common uses:
    - Marking **spelling errors** (like a word processor's red squiggle).
    - Highlighting **proper names** in Chinese text (per HTML spec).
    - Other annotations that can't be conveyed in words alone.

```html
<p>
  You can use the unarticulated annotation element to highlight
  <u>inccccort</u> <u>spling</u> <u>issses</u>.
</p>
```

<aside>
⚠️

In **HTML4**, `<u>` was used for **styling** (just an underline). In **HTML5**, it's **semantic** — use it only for annotations, **not for decoration**. For purely visual underlines, use CSS (`text-decoration: underline;`).

</aside>

## ✂️ The `<s>` Element — Strikethrough

- Represents text that's **no longer accurate or relevant**.
- Default styling: **strikethrough** line through the text.
- Common uses:
    - Cancelled events.
    - Discontinued products.
    - Outdated information that you want to leave visible.

```html
<p><s>Tomorrow's hike will be meeting at noon.</s></p>

<p>Due to unforeseen weather conditions, the hike has been canceled.</p>
```

<aside>
⚠️

Don't use `<s>` to show **document edits** — use **`<del>`** (deleted text) and **`<ins>`** (inserted text) for that. They're specifically designed for change tracking and can include `cite` and `datetime` attributes.

</aside>

## 🎌 The `<ruby>` Element — Pronunciation Annotations

- Represents small text shown **above (or beside)** the main text.
- Most commonly used to show the **pronunciation of East Asian characters** (Japanese furigana, Chinese pinyin, Korean ruby).
- Works with two companion elements:

| Element | Role |
| --- | --- |
| `<ruby>` | The container wrapping main text + annotation |
| `<rt>` | **Ruby Text** — the pronunciation / annotation itself |
| `<rp>` | **Ruby Parenthesis** — fallback parentheses for browsers that don't support ruby |

```html
<ruby> 明日 <rp>(</rp><rt>Ashita</rt><rp>)</rp> </ruby>
```

- Supported browsers display **Ashita** as a small annotation above **明日**.
- Browsers without ruby support fall back to **明日 (Ashita)** — the `<rp>` parentheses ensure it still reads sensibly.

### More ruby examples

```html
<!-- Chinese with Pinyin -->
<ruby> 你好 <rp>(</rp><rt>nǐ hǎo</rt><rp>)</rp> </ruby>

<!-- Japanese furigana -->
<ruby> 漢字 <rp>(</rp><rt>かんじ</rt><rp>)</rp> </ruby>
```

## ⚖️ The Three at a Glance

| Element | Semantic meaning | Default look | Typical use |
| --- | --- | --- | --- |
| `<u>` | Non-textual annotation | Underline | Spelling errors, proper names |
| `<s>` | No longer accurate / relevant | Strikethrough | Cancelled events, outdated info |
| `<ruby>`  • `<rt>`  • `<rp>` | Pronunciation / translation annotation | Small text above main text | East Asian pronunciation guides |

## 🎨 When to Use CSS Instead

- **Plain underline for design** (e.g., styled link, decorative emphasis) → CSS `text-decoration: underline;`.
- **Plain strikethrough for design** (e.g., crossed-out price tags) → CSS `text-decoration: line-through;`.
- Reach for `<u>`/`<s>` only when the visual carries **semantic meaning**.

## ⚠️ Common Mistakes

- ❌ Using `<u>` purely as a decorative underline — it carries semantic meaning now.
- ❌ Using `<s>` for document edits — use `<del>` and `<ins>` for tracked changes.
- ❌ Forgetting `<rp>` in a `<ruby>` block — you lose the fallback rendering on older browsers.
- ❌ Confusing the `<u>` element with HTML4's purely decorative use.

## 🧠 Quick Self-Check

**1. What is the `u` element used for?**

- [ ]  It's used to display subscripts in chemical formulas.
- [ ]  It's used to represent user input in HTML forms.
- [x]  **It's used to represent inline text that has non-textual annotation applied.**
- [ ]  It's used to italicize text in HTML.

**2. What is the `s` element used for?**

- [x]  **It's used to represent when text is no longer accurate or relevant.**
- [ ]  It's used to create navigational aides on websites.
- [ ]  It's used to represent copyright information on pages.
- [ ]  It's used to represent captions for images.

**3. What is the `ruby` element typically used for?**

- [ ]  It's used to write ruby applications.
- [ ]  It's used to create list items on a page.
- [ ]  It's used to apply an underline for text.
- [x]  **It's used to show the pronunciation of East Asian characters.**

## ✅ Key Takeaways

- **`<u>`** → non-textual annotation (e.g., spelling errors). **Not** for decoration — use CSS for that.
- **`<s>`** → text that's no longer accurate or relevant. **Not** for document edits — use `<del>` / `<ins>` for those.
- **`<ruby>`** + **`<rt>`** + **`<rp>`** → pronunciation or translation annotations, primarily for East Asian typography.
- The `<rp>` element provides **fallback parentheses** for browsers that don't support ruby annotations.
- All three are **semantic** in HTML5 — use them when the meaning matches, not just for the visual style.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
