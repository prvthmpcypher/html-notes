# What Are Large Text or Braille Keyboards, and Who Uses Them?

<aside>
✨

**Big idea:** **Large-text keyboards** have oversized keys and high-contrast labels, helping users with **low vision or motor difficulties**. **Braille keyboards** use the 6-dot braille pattern for input and pair with **refreshable braille displays** for blind and deafblind users.

</aside>

## ⌨️ Large Text (Large Print) Keyboards

- Standard QWERTY layout, but with **oversized characters** printed on each key.
- Often use **high-contrast color schemes** (white on black, yellow on black, large black on white).
- Sometimes paired with **larger keys** themselves for easier targeting.

### Who uses them?

- **Low-vision users** who can still see the screen with magnification but struggle to find keys.
- **Older adults** with age-related vision decline.
- **Beginners or younger learners** for whom standard letters are too small.
- **Users with motor difficulties** who benefit from bigger keys (lower precision needed).

## ⠿ Braille Keyboards

- Use the **six-dot Braille cell** layout instead of QWERTY.
- Usually 8 input keys: 6 for the braille dots, plus space + backspace (or modifiers).
- Often called **"Perkins-style"** keyboards (after the Perkins Brailler typewriter).
- Many pair with a **refreshable braille display** — small pins raise and lower to form braille characters in real time.

### Refreshable braille display

- A row (or rows) of cells with electromechanical pins.
- Pins rise to form **braille letters**, refresh as the user moves through the text.
- Critical for **deafblind users** who can't use audio output.

### Who uses braille input?

- **Blind users** fluent in braille — many find it faster than dictation.
- **Deafblind users** who need a tactile-only workflow.
- **Students learning braille** to build literacy.

## 🌐 What This Means for Web Developers

The device that **types** doesn't directly change your code — but it does shape **how** users interact:

- **Form inputs** must be **fully keyboard-accessible** (no mouse-only widgets).
- **Focus indicators** must be visible and never removed.
- **Tab order** must be logical (DOM order matches visual order).
- **Don't trap focus** in modals without escape; provide a way out via Esc and a close button.
- **Provide skip links** ("Skip to main content") so braille/keyboard users don't have to step through every nav item every time.

## 🧠 Quick Self-Check

**1. Large-text keyboards primarily help users with…**

- [ ]  Deafness
- [x]  **Low vision or motor difficulty**
- [ ]  Color blindness
- [ ]  No disability — they're decorative

**2. A refreshable braille display works by…**

- [ ]  Reading text aloud
- [x]  **Raising and lowering pins to form braille characters in real time**
- [ ]  Showing larger text on screen
- [ ]  Translating text into pictures

**3. Which of these helps both braille and screen-reader users the most?**

- [ ]  Removing keyboard focus styles
- [ ]  Hiding navigation behind hover effects
- [x]  **Building a fully keyboard-accessible site with logical tab order**
- [ ]  Using pixel-only fixed widths

## ✅ Key Takeaways

- **Large-text keyboards** = oversized labels, high contrast, often larger keys — for low vision and motor difficulty.
- **Braille keyboards** use a 6-dot input layout; **refreshable braille displays** show braille via electromechanical pins.
- Deafblind users rely on **braille input + braille display** — text is their only channel.
- For developers: keep your site **fully keyboard-navigable**, with visible focus, logical tab order, and skip links.

---

<aside>
➡️

**Next chapter →** Alternative pointing devices like trackballs, joysticks, and touchpads.

</aside>
