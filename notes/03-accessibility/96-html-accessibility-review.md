# HTML Accessibility Review

<aside>
📚

**Recap sheet** for the entire **HTML Accessibility** module — skim it before the quiz. Each section links back to the deeper chapter.

</aside>

## ♿ 1. What Is Accessibility?

- **a11y** = making the web usable by everyone, including people with disabilities.
- Guided by **WCAG**'s **POUR** principles: **P**erceivable, **O**perable, **U**nderstandable, **R**obust.
- Conformance levels: **A**, **AA** (industry default), **AAA**.

## 🔊 2. Assistive Tech Overview

- **Screen readers** — NVDA, JAWS, VoiceOver, TalkBack, Narrator, Orca — read aloud or output to braille.
- **Large-text keyboards** — oversized labels for low-vision users.
- **Braille keyboards + refreshable braille displays** — 6-dot input, tactile output for blind/deafblind users.
- **Alternative pointing devices** — trackball, joystick, head-mouse, eye-tracker, sip-and-puff switch.
- **Screen magnifiers** — zoom part of the screen; built into every OS + browsers.
- **Voice recognition** — Voice Control, Voice Access, Dragon, Talon Voice — dictation + control.

## 🛠️ 3. Auditing Tools

- **Browser scanners**: axe DevTools, WAVE, Accessibility Insights.
- **Built-in**: Lighthouse, Chrome DevTools Issues panel, Firefox Accessibility Inspector.
- **CI**: `@axe-core/cli`, `pa11y`, `jest-axe`, `cypress-axe`, `playwright-axe`.
- Catch **~30–50%** of issues automatically. Manual testing is still required.

## 🔢 4. Heading Hierarchy

- **One `<h1>`** per page.
- Sequential `<h2>`–`<h6>` underneath. **Never skip levels** going down.
- Pick headings by **meaning**, not size.
- ~70% of screen-reader users navigate by headings.

## 📊 5. Accessible Tables

- Use `<table>` **only for tabular data**.
- Always include a **`<caption>`**.
- Use **`<th scope="col">`** and **`<th scope="row">`** for headers.
- Group rows with **`<thead>`**, **`<tbody>`**, **`<tfoot>`**.
- For complex tables: **`id` + `headers`** to link cells to multiple headers.

## 🏷️ 6. Form Labels

- Every input needs a **`<label>`** — via `for`+`id` or by wrapping.
- `placeholder` is **not** a label.
- Group radios/checkboxes inside **`<fieldset>` + `<legend>`**.
- Use **`aria-describedby`** for help text and errors; pair with **`aria-invalid="true"`**.

## 🏛️ 7. WAI-ARIA in One Page

| Attribute | Purpose |
| --- | --- |
| `role` | What kind of UI is this (button, dialog, navigation) |
| `aria-label` | Direct-string accessible name (icon-only buttons) |
| `aria-labelledby` | References one or more `id`s as the name |
| `aria-describedby` | References one or more `id`s as a description (hints, errors) |
| `aria-hidden="true"` | Hide from accessibility tree (decorative icons) |
| `aria-expanded`, `aria-pressed`, `aria-selected`, `aria-invalid`, `aria-live` | State attributes for custom widgets |

**First rule of ARIA**: don't use ARIA if a native HTML element will do.

## 🖼️ 8. Alt Text

- Every `<img>` needs an `alt` attribute.
- **Meaningful image** → short, specific description.
- **Decorative image** → `alt=""`.
- Avoid "image of" / "picture of" — screen readers already announce "image."

## 🔗 9. Link Text

- Describe the **destination**, not the action.
- Avoid "click here", "read more", "learn more."
- Make every link's accessible name **unique**.
- Mark links that open in a new tab or download a file.

## 🎥 10. Audio & Video

- **Captions** (same language + sound effects) — for deaf/HoH users.
- **Subtitles** — translation.
- **Transcripts** — full text next to the player.
- **Audio descriptions** — narration of visuals for blind users.
- Use HTML5 `<video>` with `<track kind="captions">`. **Never autoplay sound.**

## ⌨️ 11. Keyboard Accessibility

- Everything reachable by **Tab**.
- **Visible focus** (`:focus-visible`).
- **Logical tab order** (DOM order = visual order).
- Expected shortcuts per widget (Enter/Space for buttons, arrows for tabs, Esc for modals).
- **Trap focus inside modals** until closed; return focus to the trigger.
- Add a **skip link** to jump past repetitive nav.

## 🧠 Quick Self-Check

**1. What does WCAG stand for?**

- [ ]  Web Content Action Group
- [x]  **Web Content Accessibility Guidelines**
- [ ]  Web Communication Accessibility Guide
- [ ]  World Content Audit Group

**2. Which is NOT a typical assistive technology?**

- [ ]  Screen reader
- [ ]  Refreshable braille display
- [ ]  Voice recognition software
- [x]  **A pixel-perfect mouse**

**3. Inside a modal dialog, the Esc key should…**

- [ ]  Submit the form
- [x]  **Close the dialog and return focus to the element that opened it**
- [ ]  Toggle dark mode
- [ ]  Do nothing

## ✅ Things to remember

- **HTML semantics is the foundation** — ARIA fills the gaps native HTML can't express.
- Provide **alt text**, **labels**, **captions**, and **transcripts** for all media.
- Test with the **keyboard**, **screen reader**, **400% zoom**, and **automated tools** — in that order.
- A focus indicator must always be **visible**; tab order must be **logical**; modals must **trap focus**.
- Accessibility is not a checklist — it's a mindset that benefits **every** user.

---

<aside>
➡️

Next up: **CSS module** — begin with the fundamentals.

</aside>
