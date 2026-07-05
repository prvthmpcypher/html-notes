# The <time> Element — Machine-Readable Dates with datetime & ISO 8601

<aside>
✨

**Big idea:** **`<time>`** marks up a **specific moment** (time, date, or duration). Pair it with a **`datetime`** attribute in **ISO 8601** format so browsers, search engines, and calendars can read it. Humans see a friendly string; machines see a precise timestamp.

</aside>

## ⏰ What Is the `<time>` Element?

- A semantic element used to represent a **specific moment in time** — a clock time, calendar date, datetime, or duration.
- The text between the tags is **what humans see**.
- The **`datetime`** attribute is **what machines read**.

```html
<p>The reservations are for <time datetime="20:00">20:00</time></p>
```

## 🏷️ The `datetime` Attribute

- Translates the human-readable text into a **machine-readable format**.
- Helps with:
    - 🔍 **Search engines** (rich results, event snippets).
    - 📅 **Calendars and assistive tech** parsing dates/times.
    - ✅ **Date math and sorting** by tooling that consumes the page.
- The value must be a **valid year, month, time, local date, global date, or duration** — always per ISO 8601.

## 📆 ISO 8601 in 90 Seconds

**ISO 8601** is the international standard for writing dates and times. Common shapes:

| Format | Means | Example |
| --- | --- | --- |
| `YYYY` | Year | `2024` |
| `YYYY-MM` | Year and month | `2024-06` |
| `YYYY-MM-DD` | Full date | `2024-06-15` |
| `HH:MM` | Time (24-hour) | `20:00` |
| `HH:MM:SS` | Time with seconds | `20:00:30` |
| `YYYY-MM-DDTHH:MM:SS` | Local datetime | `2024-06-15T15:00:00` |
| `YYYY-MM-DDTHH:MM:SSZ` | UTC datetime (`Z`) | `2024-06-15T15:00:00Z` |
| `PnYnMnDTnHnMnS` | Duration (period) | `PT2H30M` = 2 h 30 min |

<aside>
💡

The **capital `T`** in `2024-06-15T15:00` is the **separator** between the date and the time — not a timezone marker. A trailing **`Z`** would mark UTC.

</aside>

## 📅 Example — A Calendar Date

```html
<p>
  The graduation will be on
  <time datetime="2024-06-15T15:00">June 15</time>
</p>
```

- Humans read: **"June 15"**.
- Machines read: **June 15, 2024 at 15:00 local time**.

## 🧩 More Real-World Examples

```html
<!-- Just a year -->
<p>Founded in <time datetime="1999">1999</time>.</p>

<!-- A specific date -->
<p>Released on <time datetime="2024-09-12">September 12th</time>.</p>

<!-- A datetime in UTC -->
<p>
  Live demo starts at
  <time datetime="2024-11-01T18:00:00Z">6 PM UTC on Nov 1</time>.
</p>

<!-- A duration (period) -->
<p>
  The talk is
  <time datetime="PT45M">45 minutes</time> long.
</p>

<!-- Inside a blog post -->
<article>
  <h2>Why I love HTML</h2>
  <p>Posted on <time datetime="2024-05-20">May 20, 2024</time>.</p>
</article>
```

## ✅ When to Use `<time>`

- **Events** (meetups, concerts, releases).
- **Publication dates** (blog posts, news articles).
- **Appointments** and bookings.
- **Deadlines**.
- **Durations** (talk length, video length).

## ⚠️ Common Mistakes

- ❌ Using a non-ISO format inside `datetime` (e.g. `15/06/2024` or `Jun 15, 2024`). Always use ISO 8601 in the attribute.
- ❌ Forgetting the **`T`** between date and time (`2024-06-15 15:00` is **not** valid).
- ❌ Putting the **time zone in the visible text** but forgetting to encode it in `datetime` (use `Z` for UTC or `+HH:MM`/`-HH:MM` offsets).
- ❌ Reusing `<time>` for relative phrases like "sometime next week" — it needs a specific moment.

## 🧠 Quick Self-Check

**1. What does the `datetime` attribute in the `time` element help with?**

- [ ]  It formats text in bold.
- [x]  **It translates dates and times into a machine-readable format.**
- [ ]  It adds color to the text.
- [ ]  It creates hyperlinks to other pages.

**2. What is the correct format for the `datetime` attribute value according to ISO 8601?**

- [x]  **`YYYY-MM-DDTHH:MM:SS`**
- [ ]  `DD-MM-YYYY HH:MM`
- [ ]  `MM-DD-YYYY HH:MM AM/PM`
- [ ]  `YYYY/MM/DD HH:MM:SS`

**3. What does the capital `T` in the ISO 8601 datetime value represent?**

- [ ]  The time zone.
- [x]  **The separator between date and time.**
- [ ]  The title of the document.
- [ ]  The temperature.

## ✅ Key Takeaways

- `<time>` marks up a **specific moment** — time, date, datetime, or duration.
- The **visible text** is human-friendly; the **`datetime`** attribute is machine-readable.
- `datetime` values follow **ISO 8601**: `YYYY`, `YYYY-MM`, `YYYY-MM-DD`, `HH:MM`, `YYYY-MM-DDTHH:MM:SS`, `PT45M`, etc.
- The capital **`T`** separates the date from the time — a trailing **`Z`** marks UTC.
- Use `<time>` for events, publication dates, appointments, deadlines, and durations — it boosts SEO and accessibility.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when the next chapter is created.)

</aside>
