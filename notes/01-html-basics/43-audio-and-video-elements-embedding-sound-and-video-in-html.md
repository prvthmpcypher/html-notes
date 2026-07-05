# Audio & Video Elements — Embedding Sound and Video in HTML

<aside>
✨

**Big idea:** `<audio>` and `<video>` let you embed sound and video directly into a webpage — no plugins needed. They share a familiar attribute family: `src`, `controls`, `loop`, `muted`, `autoplay`. Use `<source>` children for multi-format support, and use `poster` (video only) to show a preview image while the file loads.

</aside>

## 🎧 The `<audio>` Element

- Embeds **sound** in an HTML document.
- Supports common formats: **MP3**, **WAV**, **OGG**.

### Basic syntax

```html
<audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3"></audio>
```

⚠️ Nothing visible appears — the audio is loaded but no player is shown.

### Add the `controls` attribute to show a player

```html
<audio
  src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3"
  controls
></audio>
```

- `controls` is a **boolean attribute** — its presence enables built-in play / pause / volume controls.

## 🎥 The `<video>` Element

- Embeds **video** in an HTML document.
- Supports common formats: **MP4**, **OGG**, **WEBM**.

```html
<video
  src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
  loop
  controls
  muted
  width="400"
></video>
```

Most audio attributes work on `<video>` too — plus a few of its own.

## 🎛️ Common Attributes (Shared by `<audio>` & `<video>`)

| Attribute | Type | What it does |
| --- | --- | --- |
| `src` | string | URL/path to the media file |
| `controls` | boolean | Show built-in play/pause UI |
| `loop` | boolean | Restart automatically when finished |
| `muted` | boolean | Start the media in a muted state |
| `autoplay` | boolean | Start playing as soon as the page loads |
| `preload` | `none`/`metadata`/`auto` | Hint how much of the file to load upfront |

<aside>
⚠️

Most browsers will **only allow `autoplay` if the media is also `muted`**  (or the user has interacted with the page). This is to protect users from surprise sound.

</aside>

### `<video>`-only attributes

| Attribute | What it does |
| --- | --- |
| `poster` | Image shown **while the video is downloading** or before the user hits play |
| `width` / `height` | Set the displayed size of the video |
| `playsinline` | Play inline on iOS (don't auto-fullscreen) |

```html
<video
  src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
  loop
  controls
  muted
  poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
  width="400"
></video>
```

## 📦 Multiple Formats with `<source>`

Different browsers support different formats. Use `<source>` children and the browser picks the **first one it understands**.

### Audio

```html
<audio controls>
  <source src="audio.ogg" type="audio/ogg" />
  <source src="audio.wav" type="audio/wav" />
  <source src="audio.mp3" type="audio/mpeg" />
</audio>
```

### Video

```html
<video
  controls
  width="400"
  poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
>
  <source
    src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
    type="video/mp4"
  />
  <source
    src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.webm"
    type="video/webm"
  />
  Your browser does not support the video tag.
</video>
```

<aside>
💡

Text placed **inside** `<audio>` or `<video>` (after the `<source>` children) is **fallback content** — shown only when the browser can't play any of the formats. Great place for a friendly "Your browser does not support video" message.

</aside>

## 📊 Audio vs Video Cheat Sheet

| Feature | `<audio>` | `<video>` |
| --- | --- | --- |
| Common formats | MP3, WAV, OGG | MP4, OGG, WEBM |
| `controls`, `loop`, `muted`, `autoplay` | ✅ | ✅ |
| `poster` image | ❌ | ✅ |
| `width` / `height` | ❌ (audio has no visible size) | ✅ |
| Multi-format `<source>` | ✅ | ✅ |

## 🧠 Quick Self-Check

**1. What attribute allows the audio to start in a muted state?**

- [ ]  `mute`
- [ ]  `quiet`
- [ ]  `pause`
- [x]  **`muted`**

**2. Which attribute lets you see the play and pause buttons?**

- [ ]  `loop`
- [x]  **`controls`**
- [ ]  `details`
- [ ]  `muted`

**3. What is the purpose of the `poster` attribute in the video element?**

- [ ]  To set the video source.
- [ ]  To control the video playback.
- [x]  **To display an image while the video is downloading.**
- [ ]  To mute the video.

## ✅ Key Takeaways

- `<audio>` embeds sound (MP3, WAV, OGG); `<video>` embeds video (MP4, OGG, WEBM).
- Without **`controls`**, the player UI is hidden — add it to make playback visible.
- Boolean attributes: **`controls`**, **`loop`**, **`muted`**, **`autoplay`** (autoplay usually requires `muted`).
- Use `<source>` children for **multi-format fallback**; place text inside for **fallback content**.
- `<video>` adds **`poster`**, **`width`/`height`**, and **`playsinline`** on top of the shared attributes.

---

<aside>
➡️

**Next chapter →** *Up next — the freeCodeCamp lesson that follows this one.* (Link will be added when chapter 14 is created.)

</aside>
