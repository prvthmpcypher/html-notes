# What Are the Accessibility Benefits for Good Link Text, and What Are Examples of Good Link Text?

<aside>
✨

**Big idea:** **Link text must make sense on its own** — because screen-reader users often pull up a **list of every link on the page**, stripped of surrounding context. "Click here" and "read more" are useless in that list. Good link text describes the destination clearly and concisely.

</aside>

## 🔗 Why Link Text Matters

- Screen-reader users frequently scan a page by **opening a Links List** (NVDA: `Ins + F7`, VoiceOver: `Ctrl + Opt + U`).
- The list shows only the **link text** — no surrounding paragraph, no headings, no context.
- If many links say **"click here"** or **"read more"**, the user has no idea where each one leads.
- Good link text helps **everyone** — sighted users skimming the page, voice users ("Click Pricing"), and search engines.

## ✅ Good Link Text Patterns

### Describe the destination, not the action

```html
<!-- ✅ Clear destination -->
<p>For more details, visit our <a href="/pricing">pricing page</a>.</p>

<!-- ❌ Vague action -->
<p>For more details, <a href="/pricing">click here</a>.</p>
```

### Front-load the meaningful words

```html
<!-- ✅ Keyword first -->
<a href="/refund-policy">Refund policy details</a>

<!-- ❌ Filler first -->
<a href="/refund-policy">Click here for refund policy details</a>
```

### Use unique link text per destination

When multiple links say "Read more," the screen-reader links list shows **"Read more, Read more, Read more, ..."** — useless.

If you must reuse "Read more," add **`aria-label`** or **visually-hidden text** to differentiate:

```html
<a href="/post-1">
  Read more <span class="sr-only">about CSS Grid</span>
</a>
<a href="/post-2">
  Read more <span class="sr-only">about Flexbox</span>
</a>
```

Now the links list reads **"Read more about CSS Grid"** and **"Read more about Flexbox."**

## ❌ Patterns to Avoid

| Bad pattern | Why |
| --- | --- |
| `<a>click here</a>` | No destination info |
| `<a>read more</a>` (many in a row) | Indistinguishable in a links list |
| `<a>here</a>` / `<a>this</a>` | Pronoun salad — no meaning out of context |
| `<a>https://very-long-url-on-screen</a>` | Screen readers read every character; painful |
| Whole sentences as link text | Hard to scan in a links list |
| Link text styled to look like a button but using `<a>` without a clear label | Ambiguous role; missing accessible name |

## 🔊 What a Screen Reader Hears

```html
<a href="/pricing">Pricing</a>
<!-- "Pricing, link" -->

<a href="/pricing" target="_blank" rel="noopener">Pricing</a>
<!-- "Pricing, link, opens in new tab" (if you add the cue) -->

<a href="https://example.com">click here</a>
<!-- "Click here, link" — destination unclear -->
```

Some best practices to support that:

- For links that **open in a new tab**, add a **visual indicator** (icon or text "(opens in new tab)") so users aren't surprised.
- For **download links**, say so: `<a href="..." download>Annual report 2024 (PDF, 1.2 MB)</a>`.
- For **external links**, optionally append a short "(external)" hint if the destination domain matters.

## 🌐 SEO Bonus

Search engines treat link text as a **strong signal** of the destination's topic. Descriptive link text:

- Improves your destination page's rankings for the topic referenced.
- Provides anchor-text context that crawlers love.
- Encourages click-throughs because it's clearer.

## 🧠 Quick Self-Check

**1. Why does link text need to make sense on its own?**

- [ ]  It looks better visually
- [x]  **Because screen-reader users often browse a list of links stripped of surrounding context**
- [ ]  To save bandwidth
- [ ]  To satisfy CSS rules

**2. Which is the BEST link text for a page about your refund policy?**

- [ ]  `click here`
- [ ]  `learn more`
- [x]  **`Refund policy details`**
- [ ]  `this page`

**3. If multiple "Read more" links appear on the same page, the best fix is to…**

- [ ]  Remove the `<a>` tag
- [ ]  Style the links differently
- [x]  **Add visually-hidden text or `aria-label` so each link's accessible name is unique**
- [ ]  Put them all inside a `<button>`

## ✅ Key Takeaways

- Link text should **describe the destination**, not the action.
- Avoid **"click here"**, **"read more"**, and similar generics — they're useless in a links list.
- **Unique** link text per destination; differentiate repeats with visually-hidden text or `aria-label`.
- Indicate when a link **opens in a new tab** or downloads a file.
- Good link text helps **screen readers, voice users, sighted scanners, and SEO** — all at once.

---

<aside>
➡️

**Next chapter →** Making audio and video content accessible.

</aside>
