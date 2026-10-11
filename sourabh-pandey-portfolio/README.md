# Sourabh Pandey — Personal Branding Portfolio

Eight complete static HTML pages using HTML5, inline CSS and vanilla JavaScript. Designed in green, white and charcoal with rounded glass cards, editorial white sections, restrained red accents and an offline SVG signature intro. **Not deployed.**

## Open locally

1. Keep the entire `sourabh-pandey-portfolio/` folder together.
2. Double-click **`index.html`** in a modern browser.
3. Use the navigation or open any other HTML page individually.

No framework, package installation, build, server, database or internet connection is needed to render the site. Professional external links require internet access. Email links open a configured mail client. Clipboard access varies by browser; the Copy email action includes a legacy file-opening fallback and a truthful manual-copy message if permission is denied.

The custom `404.html` opens independently. With no server or deployment, it does not automatically intercept missing file URLs.

## Structure

```text
sourabh-pandey-portfolio/
├── index.html
├── about.html
├── experience.html
├── projects.html
├── expertise.html
├── highlights.html
├── contact.html
├── 404.html
├── README.md
├── CONTENT-TO-CONFIRM.md
└── assets/
    └── editorial-office.webp
```

Credentials are consolidated into **`highlights.html#certification`**. Research references are at **`highlights.html#source-notes`**. The earlier standalone Certifications page is superseded by this eight-page structure.

Every page includes its own full document, inline `<style>` and `<script>`, responsive rules, header and footer. `assets/` contains images only. There are no separate project CSS/JS files, remote fonts, scripts, runtime includes or build dependencies. The primary visual asset is a local optimized WebP (approximately 176 KB).

## Implemented design and interactions

- Exact requested dark/green design variables, system typography, 22px rounded cards, translucent fills, subtle static glows, backdrop blur/saturation and WebKit equivalents. `@supports not` supplies opaque fallbacks.
- White sections break up the dark layout. Red is limited to navigation hover underlines, the signature subtitle underline, and a small 404 accent.
- Hero with SP avatar, profile-stated IGBC badge, **View Projects** and **Contact Me** actions. No generated or stock face impersonates Sourabh.
- Neutral inline leaf credential badge in the hero, About, credential card, Contact and footer. It is explicitly portfolio UI, not an official logo or verification seal.
- Sticky glass header, active-page indicator, animated mobile hamburger, Escape closing, close-on-link, keyboard focus trap and focus restoration. No-JavaScript mobile navigation remains visible.
- Filterable professional-work grid with **All entries**, **Professional activity**, and **Architectural studies**. Counts announce changes accessibly. Illustrations are not claimed as completed projects.
- Working mailto and LinkedIn links, copy-email feedback, no fake form or private contact details.
- IntersectionObserver entrance effects with card staggering; hover/press feedback; small requestAnimationFrame-throttled hero-glow scroll movement; reduced-motion support.
- Unique page titles/descriptions, Open Graph text metadata, inline SVG favicon, semantic landmarks, one H1 per page, visible focus rings, lazy-loaded non-critical imagery and local relative paths.
- Copyright year updated by JavaScript with a static 2026 fallback. No fictional canonical URL or deployed Open Graph image address.

## Signature intro

`index.html` only:

- **0.0–0.3 s:** dark screen with faint green glow.
- **0.3–2.0 s:** “Sourabh Pandey” draws using inline vector glyph outlines and `stroke-dashoffset`, then fills with a white/green gradient.
- **1.9–2.6 s:** “IGBC Certified” blur/fades in with a small green check and restrained red underline.
- **2.6–3.0 s:** overlay fades/slides away.

A 3000 ms JavaScript timer dismisses it and releases scroll. CSS independently hides the overlay and releases scrolling at approximately 3 seconds even if the timer fails. Browser scheduling can introduce minor timing variation. Normal visits and reloads replay the intro; same-tab navigation from inner pages suppresses it. Back/forward restores dismiss it. When session storage is denied, the full intro may replay on navigation rather than relying on unavailable state.

Reduced-motion users see the text statically for approximately one second, without drawing or parallax. If SVG stroke CSS is unsupported, per-letter text fading is used. If JavaScript is disabled, the loader stays hidden and the page/navigation remain usable.

The signature uses inline outlines derived from **Allura**, an open-source SIL OFL script face. No font file is downloaded at runtime. It is decorative lettering of the name, **not a claim to reproduce Sourabh’s real handwritten signature**. Source and license are included below.

## Research record and verified facts

Research checked: **11 October 2026**.

### URLs

1. Supplied primary professional reference:
   https://in.linkedin.com/in/sourabh-pandey-igbc-ap%C2%AE-545631265
2. Official credential program reference:
   https://www.igbc.in/igbc-ap
3. Secondary indexed activity/reaction reference:
   https://www.linkedin.com/in/jalaram-plywood-and-laminates-62635b3b4/
4. Allura font source:
   https://github.com/google/fonts/tree/main/ofl/allura
5. Allura license:
   https://github.com/google/fonts/blob/main/ofl/allura/OFL.txt

### Independently verified program facts

- The Indian Green Building Council (IGBC) publishes the **IGBC Accredited Professional** program.
- Its AP examination concerns green-building design and construction knowledge and is not based on a single rating system.
- Its official page describes awarding the IGBC Accredited Professional certificate to successful candidates.
- That general program page does **not** independently verify Sourabh’s award, issue date or current validity.
- An individual credential and a building/project certification are different claims; the site makes no verified project-certification claim.

### Supplied / profile-stated identity, not independently verified award facts

- The user supplied the name **Sourabh Pandey** and IGBC AP identity.
- Direct access to the LinkedIn reference returned **HTTP 403**, including during the final revision. The full biography, employment record, qualifications and photos could not be inspected.
- The main site marks individual credential status as **profile-stated**. The exact user-requested loader text “IGBC Certified” is retained; the certification card clarifies precise program wording and evidence limits.

### Secondary evidence only

A search-indexed LinkedIn reaction/activity excerpt attributed a vendor invitation to **“SOURABH PANDEY IGBC AP®”**, naming **FocusOn Interiors** and describing commercial fit-out vendor partnerships, structured work orders, clear scope, transparent relationships, Delhi-NCR/Gurugram/Bengaluru/Mumbai and pan-India outreach. It supplied `sourabh.pandey@focusoninterior.in` for vendor registration.

This is a limited secondary excerpt, not an accessible original post or verified employment record. No exact post date, job title, tenure, personal project assignments or present employment status has been inferred. The listed cities are outreach locations, not a confirmed residence or career history. No company website was guessed from the email domain. No unrelated same-name search results were adopted.

See **`CONTENT-TO-CONFIRM.md`** for every material missing fact and asset request. No awards, project values, years of experience, client names, skill percentages, testimonials, ratings or formal recognitions have been fabricated.

## Edit content

Because there is deliberately no template engine, shared changes must be made in all eight HTML files.

- **Colors/components:** edit the CSS variables and the `FINAL DESIGN SYSTEM` section within each page’s `<style>`. Base layout rules precede this section in the same inline block.
- **Navigation/footer:** change the same markup on all pages; preserve relative paths and the page-specific `aria-current="page"`.
- **Biography and timeline:** replace only with approved, sourced text. Confirm dates and roles before adding timeline entries.
- **Expertise:** add a competency only when source evidence or Sourabh’s confirmation supports it. Do not infer services from the IGBC suffix.
- **Projects:** cards have `data-category="activity"` or `data-category="study"`. If verified delivered projects are supplied, add an appropriate category and a matching `data-filter` button. Keep initial result-count text accurate. Source-rich projects can later receive independent `project-name.html` pages with their own complete inline CSS/JS.
- **Contact:** email appears in the Contact page, shared footer and copy handler. Update all copies together. Add a `tel:` link or city only if supplied and approved for publication.
- **Credentials:** update `highlights.html#certification` and the repeated badge components only with authentic evidence. Do not present the program page as individual verification.
- **Intro:** inline SVG paths and their gradient are in the homepage loader. Keep the exact required text, accessible SVG label, fallback lettering and subtitle aligned when editing.

## Replace portrait, imagery and badge

### Portrait

No authorized real portrait was available. The homepage, About and Contact deliberately use SP initials.

Once Sourabh supplies an authorized real image:

1. Remove the background from that real photo; retain natural facial features and skin tones.
2. Save a transparent optimized `assets/sourabh-portrait.webp` or `.png` (no generated face).
3. Replace the homepage `.avatar`, About `.profile-mark`, and Contact `.contact-avatar` with an `<img>` using relative `src`, correct width/height and accurate alt text.
4. Use `object-fit: contain` over the existing glass/glow treatment. Avoid cropping off the head or stretching the image. Lazy-load non-hero portraits.
5. Recheck mobile cropping and accessibility. Remove placeholder notes only after this replacement is genuine and approved.

### Architectural image

`assets/editorial-office.webp` is an original AI-generated architectural concept, not a named real project or Sourabh’s delivered/design work. A second project-grid study shows a detail of the same illustration; it is not a second claimed project. Captions and alt text identify the illustration. No measured sustainability performance or material certifications are asserted.

To replace it with real project photography, first establish image reuse rights, client permission, project association and accurate captions. Keep dimensions/aspect ratio stable, optimize the local file and preserve lazy loading below the fold. Never remove illustrative disclaimers without evidence that the replacement depicts verified work.

### Official badge

The current green leaf icon is an original neutral inline SVG, not a fabricated IGBC mark. Use an official asset **only if supplied with appropriate permission**, named `assets/igbc-ap-badge.svg` or `.png`. Keep its aspect ratio and official artwork unchanged. Retain a text label and do not imply verification, endorsement or project certification. Never invent a seal, credential ID or validity date.

## QA completed

Chromium/Playwright tests using direct `file://` opening:

- All eight pages load independently and include their own inline CSS/JS; no external project stylesheet/script dependencies.
- One H1, working internal files/fragments, image loading and no page JavaScript errors.
- No horizontal overflow at **320, 390, 768, 1024, 1440 and 1920 px**.
- All-page mobile menu toggle, Escape closing, Tab/Shift+Tab focus wrapping and focus restoration.
- Project category filters and correct visible-card counts.
- Copy-email success through the file-opening fallback.
- Homepage 3-second timing, refresh replay, scroll locking/release, inner-page skip and one-second reduced-motion presentation.
- No-JavaScript loader invisibility and mobile navigation availability.
- CSS fallback hides the loader and restores scrolling even with JavaScript timers deliberately disabled.
- Automated axe-core WCAG 2 A/AA and WCAG 2.1 AA desktop and mobile scans on all eight pages: **zero reported violations after contrast fixes**.

Automated checks are not a certification of accessibility. Real-device, screen-reader and additional browser review remain recommended. LinkedIn or other external references may require login or restrict access; current external reachability and mailbox delivery are not guaranteed.

## Allura attribution and license

The following license accompanies the source script lettering used to create the inline SVG outlines. No binary font is shipped in the assets directory.

```text
Copyright 2010 The Allura Project Authors (https://github.com/googlefonts/allura)

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
http://scripts.sil.org/OFL


-----------------------------------------------------------
SIL OPEN FONT LICENSE Version 1.1 - 26 February 2007
-----------------------------------------------------------

PREAMBLE
The goals of the Open Font License (OFL) are to stimulate worldwide
development of collaborative font projects, to support the font creation
efforts of academic and linguistic communities, and to provide a free and
open framework in which fonts may be shared and improved in partnership
with others.

The OFL allows the licensed fonts to be used, studied, modified and
redistributed freely as long as they are not sold by themselves. The
fonts, including any derivative works, can be bundled, embedded,
redistributed and/or sold with any software provided that any reserved
names are not used by derivative works. The fonts and derivatives,
however, cannot be released under any other type of license. The
requirement for fonts to remain under this license does not apply
to any document created using the fonts or their derivatives.

DEFINITIONS
"Font Software" refers to the set of files released by the Copyright
Holder(s) under this license and clearly marked as such. This may
include source files, build scripts and documentation.

"Reserved Font Name" refers to any names specified as such after the
copyright statement(s).

"Original Version" refers to the collection of Font Software components as
distributed by the Copyright Holder(s).

"Modified Version" refers to any derivative made by adding to, deleting,
or substituting -- in part or in whole -- any of the components of the
Original Version, by changing formats or by porting the Font Software to a
new environment.

"Author" refers to any designer, engineer, programmer, technical
writer or other person who contributed to the Font Software.

PERMISSION & CONDITIONS
Permission is hereby granted, free of charge, to any person obtaining
a copy of the Font Software, to use, study, copy, merge, embed, modify,
redistribute, and sell modified and unmodified copies of the Font
Software, subject to the following conditions:

1) Neither the Font Software nor any of its individual components,
in Original or Modified Versions, may be sold by itself.

2) Original or Modified Versions of the Font Software may be bundled,
redistributed and/or sold with any software, provided that each copy
contains the above copyright notice and this license. These can be
included either as stand-alone text files, human-readable headers or
in the appropriate machine-readable metadata fields within text or
binary files as long as those fields can be easily viewed by the user.

3) No Modified Version of the Font Software may use the Reserved Font
Name(s) unless explicit written permission is granted by the corresponding
Copyright Holder. This restriction only applies to the primary font name as
presented to the users.

4) The name(s) of the Copyright Holder(s) or the Author(s) of the Font
Software shall not be used to promote, endorse or advertise any
Modified Version, except to acknowledge the contribution(s) of the
Copyright Holder(s) and the Author(s) or with their explicit written
permission.

5) The Font Software, modified or unmodified, in part or in whole,
must be distributed entirely under this license, and must not be
distributed under any other license. The requirement for fonts to
remain under this license does not apply to any document created
using the Font Software.

TERMINATION
This license becomes null and void if any of the above conditions are
not met.

DISCLAIMER
THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL THE
COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL, OR CONSEQUENTIAL
DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF THE USE OR INABILITY TO USE THE FONT SOFTWARE OR FROM
OTHER DEALINGS IN THE FONT SOFTWARE.

```
