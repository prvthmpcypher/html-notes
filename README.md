<p align="center"><img src="assets/logo.svg" alt="HTML Notes" width="700"/></p>


<p align="center">
  <a href="https://x.com/poorvithmp07"><img src="https://img.shields.io/badge/follow-@poorvithmp07-8B7FD6?style=for-the-badge&logo=x&logoColor=white" alt="Follow on X"/></a>
  &nbsp;
  <a href="https://linkedin.com/in/poorvithmp"><img src="https://img.shields.io/badge/connect-poorvithmp-C8A97E?style=for-the-badge&logo=linkedin&logoColor=white" alt="Connect on LinkedIn"/></a>
</p>


# HTML Notes

Self-written notes on HTML — from the page skeleton to semantic markup to a full accessibility deep-dive (ARIA, screen readers, keyboard navigation). Written in my own words while learning, with a review sheet closing out each section.

## Structure

```
html-notes/
├── 01-html-basics/     ← boilerplate, attributes, entities, media, links, paths
├── 02-semantic-html/   ← why semantics matter, heading hierarchy, semantic tags
└── 03-accessibility/   ← ARIA, screen readers, WAI-ARIA, keyboard navigation
```

## Contents

| Section | Topics |
|---|---|
| **HTML Basics** | 23 notes — [browse](notes/01-html-basics/) |
| **Semantic HTML** | 14 notes — [browse](notes/02-semantic-html/) |
| **Accessibility** | 20 notes — [browse](notes/03-accessibility/) |

### Full topic list


<details>
<summary><b>HTML Basics</b> (23 topics)</summary>

- [HTML Basics — What Is HTML, the Page Skeleton & Element Anatomy](notes/01-html-basics/31-html-basics-what-is-html-the-page-skeleton-and-element-anatomy.md)
- [Understanding HTML Attributes — Tags, Void Elements & src/alt](notes/01-html-basics/32-understanding-html-attributes-tags-void-elements-and-src-alt.md)
- [HTML Attributes Deep Dive — href, src, alt & Boolean Attributes](notes/01-html-basics/33-html-attributes-deep-dive-href-src-alt-and-boolean-attributes.md)
- [The <link> Element — Stylesheets, Fonts & Favicons](notes/01-html-basics/34-the-link-element-stylesheets-fonts-and-favicons.md)
- [The HTML Boilerplate — DOCTYPE, <html>, <head> & <body>](notes/01-html-basics/35-the-html-boilerplate-doctype-html-head-and-body.md)
- [UTF-8 Character Encoding — What It Is & Why Every HTML File Needs It](notes/01-html-basics/36-utf-8-character-encoding-what-it-is-and-why-every-html-file-needs-it.md)
- [<div> vs <section> — Grouping Content & Why Semantics Matter](notes/01-html-basics/37-div-vs-section-grouping-content-and-why-semantics-matter.md)
- [IDs vs Classes — Naming, Targeting & Styling HTML Elements](notes/01-html-basics/38-ids-vs-classes-naming-targeting-and-styling-html-elements.md)
- [HTML Entities — Named, Decimal & Hexadecimal Character References](notes/01-html-basics/39-html-entities-named-decimal-and-hexadecimal-character-references.md)
- [The <script> Element — Embedding & Linking JavaScript in HTML](notes/01-html-basics/40-the-script-element-embedding-and-linking-javascript-in-html.md)
- [Meta Description & SEO — How HTML Helps You Get Found](notes/01-html-basics/41-meta-description-and-seo-how-html-helps-you-get-found.md)
- [Open Graph Tags — Controlling How Links Look on Social Media](notes/01-html-basics/42-open-graph-tags-controlling-how-links-look-on-social-media.md)
- [Audio & Video Elements — Embedding Sound and Video in HTML](notes/01-html-basics/43-audio-and-video-elements-embedding-sound-and-video-in-html.md)
- [Optimizing Media Assets — Size, Format & Compression](notes/01-html-basics/44-optimizing-media-assets-size-format-and-compression.md)
- [Image Licenses — Copyright, Fair Use, Creative Commons & Public Domain](notes/01-html-basics/45-image-licenses-copyright-fair-use-creative-commons-and-public-domain.md)
- [SVGs — Scalable Vector Graphics for Icons, Logos & Crisp Visuals](notes/01-html-basics/46-svgs-scalable-vector-graphics-for-icons-logos-and-crisp-visuals.md)
- [Replaced Elements — When HTML Content Comes From Outside CSS](notes/01-html-basics/47-replaced-elements-when-html-content-comes-from-outside-css.md)
- [The <iframe> Element — Embedding Videos, Maps & External Pages](notes/01-html-basics/48-the-iframe-element-embedding-videos-maps-and-external-pages.md)
- [The target Attribute — Where Links Open (_self, _blank, _parent, _top)](notes/01-html-basics/49-the-target-attribute-where-links-open-self-blank-parent-top.md)
- [File Paths — Absolute vs Relative Paths & URLs](notes/01-html-basics/50-file-paths-absolute-vs-relative-paths-and-urls.md)
- [File Paths — Slashes, Single Dot & Double Dot Explained](notes/01-html-basics/51-file-paths-slashes-single-dot-and-double-dot-explained.md)
- [Link States — :link, :visited, :hover, :focus, :active & the LVHFA Order](notes/01-html-basics/52-link-states-link-visited-hover-focus-active-and-the-lvhfa-order.md)
- [HTML Basics Review](notes/01-html-basics/53-html-basics-review.md)

</details>

<details>
<summary><b>Semantic HTML</b> (14 topics)</summary>

- [Why Semantic HTML Matters — Meaning, Accessibility, SEO & DX](notes/02-semantic-html/54-why-semantic-html-matters-meaning-accessibility-seo-and-dx.md)
- [Heading Hierarchy — Why h1→h6 Order Matters for A11y & SEO](notes/02-semantic-html/55-heading-hierarchy-why-h1-h6-order-matters-for-a11y-and-seo.md)
- [Presentational vs Semantic HTML — Why <font>, <center> & <big> Are Dead](notes/02-semantic-html/56-presentational-vs-semantic-html-why-font-center-and-big-are-dead.md)
- [<i> vs <em> — Idiomatic Text vs Emphasis (and When to Use CSS Instead)](notes/02-semantic-html/57-i-vs-em-idiomatic-text-vs-emphasis-and-when-to-use-css-instead.md)
- [<b> vs <strong> — Bring-Attention-To vs Strong Importance](notes/02-semantic-html/58-b-vs-strong-bring-attention-to-vs-strong-importance.md)
- [Description Lists — <dl>, <dt> & <dd> for Key–Value Content](notes/02-semantic-html/59-description-lists-dl-dt-and-dd-for-key-value-content.md)
- [Block & Inline Quotes — <blockquote>, <q> & <cite>](notes/02-semantic-html/60-block-and-inline-quotes-blockquote-q-and-cite.md)
- [<abbr> — Abbreviations, Acronyms & Initialisms in HTML](notes/02-semantic-html/61-abbr-abbreviations-acronyms-and-initialisms-in-html.md)
- [The <address> Element — Contact Info, tel: & mailto: Links](notes/02-semantic-html/62-the-address-element-contact-info-tel-and-mailto-links.md)
- [The <time> Element — Machine-Readable Dates with datetime & ISO 8601](notes/02-semantic-html/63-the-time-element-machine-readable-dates-with-datetime-and-iso-8601.md)
- [<sup> & <sub> — Superscript, Subscript, Math & Chemical Formulas](notes/02-semantic-html/64-sup-and-sub-superscript-subscript-math-and-chemical-formulas.md)
- [<code> & <pre> — Representing Computer Code in HTML](notes/02-semantic-html/65-code-and-pre-representing-computer-code-in-html.md)
- [<u>, <s> & <ruby> — Annotations, Strikethrough & East Asian Pronunciation](notes/02-semantic-html/66-u-s-and-ruby-annotations-strikethrough-and-east-asian-pronunciation.md)
- [Semantic HTML Review](notes/02-semantic-html/67-semantic-html-review.md)

</details>

<details>
<summary><b>Accessibility</b> (20 topics)</summary>

- [What Are Large Text or Braille Keyboards, and Who Uses Them?](notes/03-accessibility/68-what-are-large-text-or-braille-keyboards-and-who-uses-them.md)
- [What Is Accessibility?](notes/03-accessibility/78-what-is-accessibility.md)
- [What Are Screen Magnifiers Used For?](notes/03-accessibility/79-what-are-screen-magnifiers-used-for.md)
- [What Are Alternative Pointing Devices Such as Trackballs, Joysticks, and Touchpads Used For?](notes/03-accessibility/80-what-are-alternative-pointing-devices-such-as-trackballs-joysticks-and-touchpads-used-for.md)
- [What Is Voice Recognition Software Used For?](notes/03-accessibility/81-what-is-voice-recognition-software-used-for.md)
- [What Are Screen Readers, and Who Uses Them?](notes/03-accessibility/82-what-are-screen-readers-and-who-uses-them.md)
- [What Is the Purpose of WAI-ARIA, and How Does It Work?](notes/03-accessibility/83-what-is-the-purpose-of-wai-aria-and-how-does-it-work.md)
- [What Are Best Practices for Tables and Accessibility?](notes/03-accessibility/84-what-are-best-practices-for-tables-and-accessibility.md)
- [Why Is It Important for Inputs to Have an Associated Label?](notes/03-accessibility/85-why-is-it-important-for-inputs-to-have-an-associated-label.md)
- [What Are Some Common Accessibility Auditing Tools to Use?](notes/03-accessibility/86-what-are-some-common-accessibility-auditing-tools-to-use.md)
- [How Does Proper Heading Level Structure Affect Accessibility?](notes/03-accessibility/87-how-does-proper-heading-level-structure-affect-accessibility.md)
- [What Are ARIA Roles?](notes/03-accessibility/88-what-are-aria-roles.md)
- [What Is the aria-describedby Attribute, and How Does It Work?](notes/03-accessibility/89-what-is-the-aria-describedby-attribute-and-how-does-it-work.md)
- [What Are the Accessibility Benefits for Good Link Text, and What Are Examples of Good Link Text?](notes/03-accessibility/90-what-are-the-accessibility-benefits-for-good-link-text-and-what-are-examples-of-good-link-text.md)
- [What Is the aria-hidden Attribute, and How Does It Work?](notes/03-accessibility/91-what-is-the-aria-hidden-attribute-and-how-does-it-work.md)
- [What Are the Roles of the aria-label and aria-labelledby Attributes?](notes/03-accessibility/92-what-are-the-roles-of-the-aria-label-and-aria-labelledby-attributes.md)
- [When Is the alt Attribute Needed, and What Are Some Examples of Good Alt Text?](notes/03-accessibility/93-when-is-the-alt-attribute-needed-and-what-are-some-examples-of-good-alt-text.md)
- [What Are Good Ways to Make Audio and Video Content Accessible?](notes/03-accessibility/94-what-are-good-ways-to-make-audio-and-video-content-accessible.md)
- [What Are Some Ways to Make Web Applications Keyboard Accessible?](notes/03-accessibility/95-what-are-some-ways-to-make-web-applications-keyboard-accessible.md)
- [HTML Accessibility Review](notes/03-accessibility/96-html-accessibility-review.md)

</details>


## How to use this

- **HTML Basics** and **Semantic HTML** each end with a review file — use it to self-test.
- **Accessibility** is written as a Q&A set (mirroring how it's taught in most a11y curricula) — read a few a day rather than all at once, it sticks better that way.

## References

See [REFERENCES.md](REFERENCES.md) for the sources consulted while writing these notes, especially the Accessibility section.

## License

Released under the [MIT License](LICENSE).
