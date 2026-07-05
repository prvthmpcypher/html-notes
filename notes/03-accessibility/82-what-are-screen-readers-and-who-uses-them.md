# What Are Screen Readers, and Who Uses Them?

<aside>
✨

**Big idea:** A **screen reader** is software that reads digital content **out loud** (or to a braille display) and lets users **navigate** with the keyboard. Used primarily by **blind and low-vision users**, but also by many people with dyslexia, ADHD, or temporary visual impairments. Your semantic HTML is what makes a screen reader's job possible.

</aside>

## 🔊 What Is a Screen Reader?

- A **screen reader** is assistive software that **converts on-screen content into speech or braille**.
- It reads the **accessibility tree** — a structured representation the browser builds from your HTML.
- Users navigate with **keyboard shortcuts**, not a mouse — by headings, links, landmarks, forms, etc.

## 👥 Who Uses Screen Readers?

- **Blind users** — primary users; rely on a screen reader for almost all digital interaction.
- **Low-vision users** — combine a screen reader with magnification.
- **Deafblind users** — use a screen reader paired with a **refreshable braille display**.
- **Users with cognitive differences** (dyslexia, ADHD) — often prefer to listen while reading.
- **Anyone hands-busy or eyes-busy** — drivers, cooks, parents, multitaskers.

## 🧰 Common Screen Readers

| Screen reader | Platform | Notes |
| --- | --- | --- |
| **NVDA** | Windows | Free & open source — very popular |
| **JAWS** | Windows | Long-standing commercial reader, common in enterprise |
| **VoiceOver** | macOS / iOS | Built into every Apple device — turn on with ⌘ + F5 |
| **TalkBack** | Android | Built into every Android device |
| **Narrator** | Windows | Built into Windows 10/11 |
| **Orca** | Linux | Default on most distributions |

## 🗺️ How They Navigate

Users typically jump by **landmark** instead of reading linearly:

- Heading list (H key in NVDA) → outline of the page.
- Landmarks list → `<header>`, `<nav>`, `<main>`, `<footer>`.
- Links list, forms list, buttons list.
- Tab key → next focusable element.

That's why your **semantic HTML structure is the UI** for screen reader users.

## 🛠️ What Helps a Screen Reader

- **Semantic elements** (`<nav>`, `<main>`, `<button>`, `<h1>`–`<h6>`).
- **Meaningful link text** ("Download report" — not "click here").
- **`alt` text** on images that carry meaning.
- **Labels** on form fields.
- **Logical reading order** — DOM order should match visual order.
- **ARIA** roles/attributes only when native HTML can't express the meaning.

## 🚫 What Hurts a Screen Reader

- Wrapping everything in `<div>`s and `<span>`s.
- Skipping heading levels.
- Empty alt text on meaningful images, or missing alt entirely.
- Decorative-only icons announced as text.
- Auto-playing audio that drowns out the reader.

## 🧠 Quick Self-Check

**1. A screen reader converts page content into…**

- [ ]  Larger text
- [x]  **Speech or braille output**
- [ ]  Captions on video
- [ ]  CSS animation

**2. Which is the free, open-source screen reader for Windows?**

- [ ]  JAWS
- [x]  **NVDA**
- [ ]  VoiceOver
- [ ]  TalkBack

**3. Which of these helps screen readers the most?**

- [ ]  Wrapping nav links in `<div>`s
- [ ]  Using `<h1>` for any large text
- [x]  **Using semantic elements like `<nav>`, `<main>`, and proper heading levels**
- [ ]  Removing focus outlines

## ✅ Key Takeaways

- A screen reader converts on-screen content into **speech or braille**.
- Common ones: **NVDA**, **JAWS**, **VoiceOver**, **TalkBack**, **Narrator**, **Orca**.
- Users **navigate by structure** (headings, landmarks, links) — your semantic HTML *is* their UI.
- The single biggest improvement you can make for screen readers: **use the right semantic element**.

---

<aside>
➡️

**Next chapter →** Large text and braille keyboards — physical input devices for low-vision and deafblind users.

</aside>
