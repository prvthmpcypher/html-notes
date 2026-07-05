# What Is Voice Recognition Software Used For?

<aside>
✨

**Big idea:** **Voice recognition software** lets users **operate a computer by speaking** — moving the cursor, clicking, dictating text, navigating the web — entirely hands-free. Used by people with motor impairments, RSI, and anyone who'd rather talk than type. Your code makes this easier by using **semantic HTML with meaningful labels** and **predictable element names**.

</aside>

## 🎙️ What Is Voice Recognition Software?

- Software that **converts spoken commands and dictation into computer input**.
- Users can:
    - **Dictate text** ("Open document. Write to whom it may concern, comma…")
    - **Move the cursor / click** by element name ("Click Submit. Tab. Type my name.")
    - **Navigate the web** ("Go to freecodecamp dot org. Click Forum.")
    - **Switch apps**, **control the OS**, **scroll**, **scroll to top**.

## 👥 Who Uses Voice Recognition?

- People with **motor impairments** (spinal injury, MS, ALS, cerebral palsy).
- People with **RSI** or **carpal tunnel syndrome**.
- People with **temporary injuries** (broken arm, post-surgery).
- Anyone in **eyes-busy or hands-busy contexts** (driving, cooking).
- **All users** via assistants like Siri, Alexa, Google Assistant, Cortana.

## 🧰 Common Voice Tools

| Tool | Platform | Notes |
| --- | --- | --- |
| **Voice Control** | macOS / iOS | Built-in; full computer + dictation |
| **Voice Access** | Android / Windows 11 | Built-in |
| **Dragon NaturallySpeaking** | Windows (commercial) | Industry standard for power users |
| **Talon Voice** | macOS / Windows / Linux | Popular open-source/community tool |
| **Siri / Google Assistant / Alexa** | Mobile / smart speaker | Conversational shortcuts |

## 🎯 What Voice Users Need from Your Site

Voice tools usually let users say **"Click [name]"** to interact with a control. So **what gets spoken** must match **what's visible**:

- Buttons and links must have **clear, unique, visible text labels**.
- **Avoid duplicate labels** ("Click Read More" — which one?).
- For icon-only buttons, add **`aria-label`** or visually-hidden text so a name exists.
- **Don't hide control labels behind hover** — voice users can't hover.
- Use **native HTML elements** (`<button>`, `<a>`, `<input>`) — they expose proper accessible names by default.
- Make sure **the visible label is part of the accessible name** (WCAG 2.5.3 — Label in Name).

### 🚫 Anti-pattern

```html
<!-- Voice user says "Click Save" — but the accessible name is something else -->
<button aria-label="Persist changes to disk">Save</button>
```

### ✅ Better

```html
<button>Save</button>
<!-- or if you need extra context: -->
<button aria-label="Save changes">Save</button>
```

Voice tool says "Click Save" → matches the visible label → works.

## 🧠 Quick Self-Check

**1. Voice recognition software primarily helps users with…**

- [ ]  Low vision
- [x]  **Motor impairments or anyone who can't / shouldn't type**
- [ ]  Color blindness
- [ ]  Deafness

**2. Which is the WCAG "Label in Name" rule?**

- [ ]  Every link must have a `title` attribute
- [x]  **The visible label of a control should be part of its accessible name**
- [ ]  All labels must be in uppercase
- [ ]  Links must use the word "Link" in their label

**3. Which makes a voice user's life easier?**

- [ ]  Icon-only buttons with no text
- [ ]  Two buttons both labeled "Click here"
- [x]  **Unique, visible text labels on every button and link**
- [ ]  Hidden navigation revealed only on hover

## ✅ Key Takeaways

- **Voice recognition** = controlling a computer by speaking — dictation, navigation, and clicking.
- Used by people with motor impairments, RSI, temporary injuries, and assistants like Siri/Alexa.
- Make every interactive element have a **clear, unique, visible text label**.
- Follow **WCAG 2.5.3 (Label in Name)** — the visible text should be part of the accessible name.
- Use **native HTML controls** — they get accessible names for free.
- Never hide labels behind hover or rely on icons without an `aria-label`.

---

<aside>
➡️

**Next chapter →** Common accessibility auditing tools — your testing toolkit.

</aside>
