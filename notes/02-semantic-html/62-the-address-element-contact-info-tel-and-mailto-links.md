# The <address> Element — Contact Info, tel: & mailto: Links

<aside>
✨

**Big idea:** **`<address>`** is the semantic home for **contact information** — mailing address, phone, email, social links — tied to a section of your page. Pair it with **`tel:`** for clickable phone numbers and **`mailto:`** for one-click email composing.

</aside>

## 📧 What Is the `<address>` Element?

- A semantic element used to represent **contact information** for a section on a web page.
- Versatile — great for business pages, author bios, footers, personal sites, FAQ contact blocks, and more.
- Prefer it over a generic `<div>` so screen readers, search engines, and other developers understand the content's purpose.

<aside>
⚠️

`<address>` is **only for contact info about the page or its author** — not for arbitrary postal addresses inside articles (like the address of a historic building). For arbitrary addresses, use `<p>` or another block element.

</aside>

## 🏢 A Full Example — Company Contact Block

```html
<address>
  <h2>Company Name</h2>
  <p>
    1234 Elm Street<br />
    Springfield, IL 62701<br />
    United States
  </p>
  <p>Phone: <a href="tel:+15555555555">+1 (555) 555-5555</a></p>
  <p>Email: <a href="mailto:contact@company.com">contact@company.com</a></p>
</address>
```

Three common ingredients:

- **Physical address** — lines separated by 
`` for readability.
- **Phone** — wrapped in an `<a>` with `href="tel:..."`.
- **Email** — wrapped in an `<a>` with `href="mailto:..."`.

## 📞 `tel:` Links — Tap to Call

- Set the `href` of an `<a>` to **`tel:`** followed by the phone number.
- Include the country code with a `+` for international compatibility.
- On phones (and many desktop apps), tapping the link **opens the dialer**.

```html
<a href="tel:+15555555555">+1 (555) 555-5555</a>
```

**Tips**

- Use **digits only after the `+`** — spaces, dashes, and parentheses are tolerated but cleaner without.
- Show a **formatted version** to the user (with spaces/dashes) and keep the `href` clean.

## 📧 `mailto:` Links — Open a New Email

- Set the `href` of an `<a>` to **`mailto:`** followed by an email address.
- Clicking opens the user's **default email client** with a new draft ready.

```html
<a href="mailto:contact@company.com">contact@company.com</a>
```

You can also pre-fill `subject` and `body`:

```html
<a href="mailto:hello@example.com?subject=Hi&body=I%20have%20a%20question">
  Send us a message
</a>
```

<aside>
⚠️

**Downside:** plain `mailto:` links are easily scraped by spammers, so emails published this way often attract junk mail. Consider a contact form, obfuscation (e.g., "hello [at] example [dot] com"), or a JavaScript-built link to mitigate.

</aside>

## 📦 What Can Go Inside `<address>`?

- The author's / company's name.
- Physical mailing address (`<p>` with 
`` separators).
- Phone (`tel:` link), email (`mailto:` link), website URL (`<a href="...">`).
- Social media handles or profile links.
- A link to the author's profile page on the same site.

```html
<address>
  Written by <a href="/authors/jane">Jane Doe</a>.<br />
  Reach out: <a href="mailto:jane@example.com">jane@example.com</a>
</address>
```

## ⚠️ Common Mistakes

- ❌ Putting **random postal addresses** inside `<address>` (use `<p>` instead).
- ❌ Using `<address>` for an **entire footer** when the footer also has unrelated content. Wrap only the contact-info portion.
- ❌ Forgetting the **`+` and country code** in `tel:` links.
- ❌ Exposing emails plainly with `mailto:` on high-traffic pages without spam protection.
- ❌ Wrapping `<address>` inside an `<address>` (nesting them is invalid).

## 🧠 Quick Self-Check

**1. What is the purpose of the `address` element?**

- [ ]  It's used to define a section for navigation links.
- [x]  **It's used to represent contact information for a section on a web page.**
- [ ]  It's used to set the font style for a section of the page.
- [ ]  It's used to group content for styling with CSS.

**2. What is the `mailto` link used for?**

- [ ]  It's used to link to a webpage.
- [ ]  It's used to create a file download link.
- [ ]  It's used to redirect to another website.
- [x]  **It's used to allow users to open a new email within their preferred email client.**

**3. What is a downside to using `mailto` links?**

- [x]  **These links are a target for spammers to send emails to users.**
- [ ]  These links automatically create a webpage.
- [ ]  These links enhance website SEO.
- [ ]  These links improve website loading speed.

## ✅ Key Takeaways

- `<address>` semantically marks up **contact info** for a page section or its author.
- Use it for business contact blocks, author bios, footers, personal sites — not for arbitrary postal addresses in articles.
- Make phone numbers tappable with **`href="tel:+..."`** (include country code).
- Make emails clickable with **`href="mailto:..."`** — optionally pre-fill `subject` and `body`.
- **Downside of `mailto:`**: spammers scrape exposed emails. Consider contact forms or obfuscation.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
