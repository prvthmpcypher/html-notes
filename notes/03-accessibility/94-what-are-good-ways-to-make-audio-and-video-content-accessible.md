# What Are Good Ways to Make Audio and Video Content Accessible?

<aside>
✨

**Big idea:** Audio and video are inaccessible by default — a deaf user can't hear the audio, a blind user can't see the video. Add **captions**, **transcripts**, **audio descriptions**, and **proper player controls** so the content works for everyone.

</aside>

## 🎧 The Four Main Accessibility Add-Ons

| Add-on | What it provides | For whom |
| --- | --- | --- |
| **Captions** | On-screen text of spoken words + important sounds | Deaf or hard-of-hearing users; noisy environments |
| **Subtitles** | On-screen text of spoken words in another language | Non-native speakers |
| **Transcripts** | Full text version of the audio (with optional time stamps) | Deafblind users (with braille), screen-reader users, search engines |
| **Audio descriptions** | Narration of visual events during gaps in dialogue | Blind / low-vision users |
| **Sign-language interpretation** | A signer in a corner of the video | Deaf users whose first language is a signed language |

## 📺 Captions vs Subtitles

- **Captions** → same language as the audio; include **sound effects** and **speaker names** ("[door slams]", "NARRATOR:"). For deaf/hard-of-hearing users.
- **Subtitles** → translation into another language. For hearing users who don't speak the audio language.

Both are typically provided as **WebVTT (`.vtt`)** files attached to a `<video>` via `<track>`.

### Adding captions to HTML5 video

```html
<video controls>
  <source src="talk.mp4" type="video/mp4" />
  <track
    kind="captions"
    src="talk-en.vtt"
    srclang="en"
    label="English"
    default
  />
  <track
    kind="subtitles"
    src="talk-es.vtt"
    srclang="es"
    label="Español"
  />
</video>
```

The `<track>` element supports `kind="captions"`, `"subtitles"`, `"descriptions"`, `"chapters"`, `"metadata"`.

### Sample WebVTT format

```
WEBVTT

00:00:01.000 --> 00:00:04.000
[applause]

00:00:04.500 --> 00:00:07.000
Thank you. Today we'll talk about accessibility.
```

## 📜 Transcripts

- A **full text version** of the audio/video published next to the player.
- Helps:
    - **Deafblind users** (with a braille display).
    - **Screen-reader users** who prefer text.
    - **All users** who skim or search.
    - **SEO** — search engines can index every word.
- Easy and cheap. Always provide one.

## 🎙️ Audio Descriptions

- Spoken narration that describes important **visual** information during gaps in dialogue.
- Required for content where the visuals carry meaning the audio doesn't (films, demos, charts).
- Two flavors:
    - **Standard** audio description — fits in dialogue gaps.
    - **Extended** — the video pauses to allow longer descriptions.
- Provide via `<track kind="descriptions">` or as a separate audio-described video file.

## 🎮 Accessible Player Controls

- Use the **native HTML5 player** with `controls` — it's keyboard-accessible by default.
- If you build a custom player:
    - **Keyboard support**: Space to play/pause, arrows to scrub, M to mute, F for fullscreen.
    - **Visible focus** rings on buttons.
    - **Labels** on every control (`aria-label`).
    - **`aria-pressed`** for toggle buttons (mute, captions on/off).
    - A **caption toggle** that's actually reachable.
- **Avoid autoplay with sound** — it drowns out screen readers and startles users.

## ⚠️ Common Mistakes

- **Auto-generated captions only** — YouTube's auto-captions can hit 80% accuracy on a good day. Always **review and correct** them.
- **No transcript at all** — cheap to add, huge benefit.
- **Captions burned into the video** — users can't turn them off, resize them, or restyle them.
- **Auto-playing audio** — disturbs screen-reader use and many users.
- **Tiny, unreachable caption toggle**.
- **No keyboard support** in a custom player.

## 🧠 Quick Self-Check

**1. What's the difference between captions and subtitles?**

- [ ]  None — they're the same
- [x]  **Captions include sound effects and speaker names (same language as audio); subtitles translate the dialogue**
- [ ]  Captions are for video, subtitles are for audio
- [ ]  Subtitles include sound effects; captions don't

**2. Which is the file format used by HTML5 `<track>` for captions?**

- [ ]  SRT
- [x]  **WebVTT (.vtt)**
- [ ]  MP3
- [ ]  CSS

**3. Audio descriptions help users who…**

- [x]  **Can't see the visuals (blind or low-vision)**
- [ ]  Are hard of hearing
- [ ]  Speak another language
- [ ]  Have RSI

## ✅ Key Takeaways

- Always provide **captions** (same-language text + sound effects) for deaf/hard-of-hearing users.
- Add **subtitles** for translation when relevant.
- Publish a **full transcript** next to every video/audio embed.
- Provide **audio descriptions** when visuals carry meaning the audio doesn't.
- Use the **native HTML5 player** or build a fully keyboard-accessible custom player with labeled controls.
- Never **autoplay sound** — it breaks screen-reader UX and surprises users.

---

<aside>
➡️

**Next chapter →** Making web applications keyboard-accessible.

</aside>
