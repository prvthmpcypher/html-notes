# Link States — :link, :visited, :hover, :focus, :active & the LVHFA Order

<aside>
✨

**Big idea:** Links have **five interactive states** — `:link`, `:visited`, `:hover`, `:focus`, `:active`. Each one tells the user something important (clickable? already visited? being hovered? being activated?). Always write them in the **LVHFA** order so later states aren't accidentally overridden by earlier ones.

</aside>

## 🔗 The Five Link States

| State | Triggered when… |
| --- | --- |
| **`:link`** | Default — the link hasn't been visited yet |
| **`:visited`** | The user has already visited the linked page |
| **`:hover`** | The user's cursor is hovering over the link |
| **`:focus`** | The link is focused (e.g., by Tab key) — critical for keyboard accessibility |
| **`:active`** | The link is being clicked / activated **right now** |

## 1️⃣ `:link` — Default State

Base styling for any unvisited link. By default, blue + underlined.

```html
<a href="https://freecodecamp.org" target="_blank">Visit freeCodeCamp</a>
```

Think of `:link` as the **foundation styles** — the other states build on top.

## 2️⃣ `:visited` — Already Visited

Applies when the user has visited the target URL before. By default, browsers turn these **purple**.

```css
a:visited {
  color: brown;
}
```

Useful for showing users **which docs they've already read** or **which sites they trust**.

<aside>
🔒

For privacy reasons, **only a limited set of properties** can be changed in `:visited` (mainly `color`, `background-color`, `border-color`). You can't, for example, swap an image or change `display`.

</aside>

## 3️⃣ `:hover` — Mouse Over

Applies when a pointer hovers over the link — a clear visual signal that this thing is clickable.

```css
a:hover {
  color: red;
}
```

## 4️⃣ `:focus` — Keyboard / Programmatic Focus

Applies when the link is focused (clicking the empty page area then pressing **Tab** moves focus to the next link).

```css
a:focus {
  color: green;
}
```

<aside>
♿

**Never remove focus styles** without replacing them. Keyboard users navigate by Tab, and they need to see where they are. The default outline isn't pretty — style it, don't kill it.

</aside>

## 5️⃣ `:active` — Being Clicked

Applies *while* the link is being activated (mouse button down, finger pressed, Enter held). Usually brief.

```css
a:active {
  color: black;
}
```

Gives instant feedback that **"yes, your click was registered."**

## 📜 The LVHFA Order Matters

Write your link rules in this exact order:

```css
a:link    { color: blue;   }
a:visited { color: purple; }
a:hover   { color: red;    }
a:focus   { color: green;  }
a:active  { color: black;  }
```

A handy mnemonic:

<aside>
🧠

**LoVe HAte** → :**L**ink → :**V**isited → :**H**over → :**A**ctive *(or LVHFA if you include :focus, slotted between hover and active).*

</aside>

### Why the order?

CSS uses **source order** for rules of equal specificity. If you write `:hover` before `:visited`, the visited color will *override* your hover color — because both rules apply when the user hovers over an already-visited link. The LVHFA order makes sure **later interactions override earlier states**.

## 🧩 Mini Pattern — Accessible Link Styling

```css
a:link {
  color: #1d4ed8;
  text-decoration: underline;
}

a:visited {
  color: #6b21a8;
}

a:hover {
  color: #b91c1c;
}

a:focus {
  outline: 2px solid #2563eb;
  outline-offset: 2px;
}

a:active {
  color: #000;
}
```

## 🧠 Quick Self-Check

**1. What is the default state of a link?**

- [x]  **`:link`**
- [ ]  `:visited`
- [ ]  `:hover`
- [ ]  `:active`

**2. Which state applies while a user is clicking the link?**

- [ ]  `:link`
- [ ]  `:visited`
- [ ]  `:hover`
- [x]  **`:active`**

**3. In what order should you style your links?**

- [ ]  visited, link, active, hover.
- [ ]  link, active, hover, visited.
- [ ]  hover, active, link, visited.
- [x]  **link, visited, hover, active.** (LVHA; insert `:focus` between hover and active for the full LVHFA)

## ✅ Key Takeaways

- Five link states: **`:link`**, **`:visited`**, **`:hover`**, **`:focus`**, **`:active`**.
- `:link` = default; `:visited` = already-visited (purple by default).
- `:hover` = mouse over; `:focus` = keyboard focus; `:active` = currently being clicked.
- Write them in **LVHFA** order (LoVe HAte mnemonic) so later interactions win.
- For privacy, only a few properties can be styled in `:visited` — mainly colors.
- Never strip `:focus` outlines without replacing them — it breaks keyboard accessibility.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 23 is created.)

</aside>
