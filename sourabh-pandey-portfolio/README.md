# Sourabh Pandey — Personal Branding Portfolio

A premium, responsive, static nine-page portfolio for Sourabh Pandey, presented as an **IGBC Accredited Professional (profile-stated)**. Every HTML file is standalone and includes its own identical inline design system, shared navigation/footer markup, and vanilla-JavaScript interactions. There is no framework, build step, backend, external project CSS/JS or deployment. **Not deployed.**

## Open locally

1. Keep the full `sourabh-pandey-portfolio/` folder together.
2. Double-click `index.html` in a modern browser.
3. Open any other `.html` page directly, or use the in-page navigation.

No local server or internet connection is required to render the site. External profile/program/company links require internet access; email links open a configured mail client. The copy-email button uses Clipboard API when available and a local fallback, with an honest status message if browser permissions prevent copying. `404.html` is a standalone error page; without a server it does not automatically intercept missing files.

## Structure

```text
sourabh-pandey-portfolio/
├── index.html             Home and three-second signature intro
├── about.html             Profile and evidence limits
├── experience.html        Evidence-led timeline
├── projects.html          Activity/study filter and project disclosures
├── expertise.html         Source-linked professional context
├── certifications.html    IGBC AP credential context
├── insights.html          Summary of accessible LinkedIn activity
├── contact.html           Public professional links and copy-email action
├── 404.html               Standalone not-found page
├── README.md              Sources, project guide and editing notes
├── CONFIRM.md             Missing facts and asset confirmations
└── images/
    ├── commercial-interior-study.svg
    ├── green-building-study.svg
    └── workplace-light-study.svg
```

The SVGs are original, generic editorial illustrations. They are not photographs, project images or representations of work by Sourabh or FocusOn Interiors. No authorized portrait or official IGBC badge was supplied, so the site uses SP initials and a neutral inline-SVG leaf/shield badge. See `CONFIRM.md` before replacing either.

## Implementation and design

- HTML5 + CSS3 + vanilla JavaScript only; every page contains its own inline `<style>` and `<script>`. All nine pages share byte-identical CSS and JavaScript; the common header/footer components are repeated inline. The home page alone includes the signature loader markup.
- Exact requested color tokens (`--green-900`, `--green-600`, `--green-400`, `--green-50`, `--white`, `--ink`, `--muted`, `--border`, `--red`), system typography, responsive card grids, 20px card corners, light sections and dark green hero/footer.
- Sticky glass header with an opaque fallback, active-page state, keyboard-operable animated mobile menu, Escape close and visible focus indicators. No-JavaScript mobile navigation remains available.
- A single `IntersectionObserver` reveals elements once and unobserves them. A single passive scroll listener is throttled through `requestAnimationFrame`. Hover/reveal motion uses opacity and transform; the loader’s required SVG stroke drawing is the one intentional `stroke-dashoffset` exception. Reduced-motion preferences are honored.
- Vanilla-JS project/activity filters, accessible result count, defensive null checks, copy-email feedback and dynamic year with static 2026 fallback.
- Unique titles and descriptions, Open Graph text metadata, inline SVG favicon, semantic landmarks, one `<h1>` per page, image dimensions/alt text, lazy-loaded below-fold illustrations and relative internal links. No canonical or live URL is invented.
- No form, private phone/address, unverified client, fabricated project, invented experience date, statistic, testimonial or award.

## Home loader

`index.html` displays the vector “Sourabh Pandey” lettering, then “IGBC Certified” with a green check and red underline. It fades in over about 0.3 s, draws the custom SVG paths from about 0.3–2.05 s, reveals the subtitle from 1.9 s, and exits by about 3.0 s. The JavaScript timer is 3000 ms (maximum intended duration 3.5 s); CSS independently fades the loader and releases scroll at 3 s if JS does not run. The first visit and refresh play it; when session storage is available, in-session navigation back to Home and browser back/forward skip it. If storage is blocked, the full intro may replay. Reduced-motion users see a static version for about one second. Unsupported SVG stroke animation switches to per-letter cursive fallback; the page remains usable if JavaScript is disabled.

The outline paths are decorative script glyphs adapted from the open-source **Allura** typeface; they are not a reproduction of Sourabh’s real signature. No font is downloaded at runtime. Source: <https://github.com/google/fonts/tree/main/ofl/allura>. License: <https://github.com/google/fonts/blob/main/ofl/allura/OFL.txt>.

## Research record

Research checked **11 October 2026**. The supplied LinkedIn profile is the identity anchor, but direct access returned HTTP 403. Public search results and official references were used cautiously; unrelated same-name professionals were excluded. Full research URLs:

1. Supplied primary profile: <https://in.linkedin.com/in/sourabh-pandey-igbc-ap%C2%AE-545631265>
2. Official IGBC Accredited Professional program: <https://igbc.in/igbc-ap>
3. FocusOn Interiors website: <https://focusoninteriors.com/>
4. Secondary indexed LinkedIn activity context: <https://www.linkedin.com/in/jalaram-plywood-and-laminates-62635b3b4/>
5. Allura vector-lettering source: <https://github.com/google/fonts/tree/main/ofl/allura>
6. Allura SIL Open Font License: <https://github.com/google/fonts/blob/main/ofl/allura/OFL.txt>

### Evidence and limitations

- The supplied profile name and IGBC AP identity are represented as **profile-stated**, not independently verified. The supplied LinkedIn page returned HTTP 403, so its biography, jobs, education, credential record, photos and post history could not be reviewed.
- A search-indexed LinkedIn activity excerpt associated the wording “SOURABH PANDEY IGBC AP” with a FocusOn Interiors vendor-partner invitation in the commercial fit-out context. The text refers to structured work orders, clear scope, professional partner relationships and multi-market outreach. This does not verify Sourabh’s current employment, designation, tenure, individual duties or project delivery; the original post URL and date were unavailable.
- `sourabh.pandey@focusoninterior.in` appeared in that public vendor-registration excerpt. It is included as a public professional contact with an explicit note that current ownership/availability has not been confirmed. No personal phone or address is included.
- FocusOn Interiors’ public site is linked as an organizational resource only. The site does not call the company a verified current employer.
- IGBC’s official page explains the general AP examination/program, including green-building design and construction knowledge. That general page is not individual credential verification and does not establish Sourabh’s award date or active status.
- No personally attributable project, client, education record, career dates, other credential, outcome, rating or testimonial was sufficiently supported. The site leaves these blank rather than guessing.

## Editing guide

Because each page is intentionally standalone, copy edits to shared components must be repeated across all nine HTML files. Keep CSS and JavaScript identical between pages.

- **Shared colors/layout:** edit `:root` tokens and the same inline `<style>` block in every HTML file.
- **Header/footer:** update the repeated markup in every page. The active navigation state is assigned by the inline script based on the current filename.
- **Profile facts:** add only after checking a primary source and, where appropriate, getting Sourabh’s approval. Keep uncertain claims in `CONFIRM.md`, not in the public biography.
- **Projects:** add a personal case study only when project attribution, Sourabh’s role, dates, client/publication permissions and supporting photos/outcomes are confirmed. Update the project filter categories and accessible count.
- **Insights:** add a concise original summary with a direct source link and published date only when the post/article is available. Never reproduce full posts.
- **Contact:** change the repeated public email only after confirming ownership/availability. No phone or personal address is included.
- **Portrait:** use only a real image provided with permission; do not generate or substitute a face. Keep transparent cut-out retouching natural, crop responsibly and use meaningful alt text.
- **Badge:** replace the neutral inline badge only with an official IGBC asset supplied with permission. Do not invent certificate IDs, expiry dates or official seals.
- **Live SEO:** add canonical/absolute Open Graph URLs only when the final domain is confirmed.

## QA completed

- `html-validate`: all nine HTML files pass with no errors or warnings; PostCSS parses the inline stylesheet on every page.
- Node syntax checks pass for the shared inline scripts. Static checks confirm exactly nine pages, one `<h1>` per page, identical CSS/JS, exact design tokens, complete relative links/fragments, local image paths, dimensions and descriptive alt text, and no external project CSS/JS.
- DOM interaction checks were run on all nine pages using `file://`: active navigation, mobile menu open/Escape close, project filters and result announcements, copy-email feedback, and home-loader initialization.
- Loader checks cover the 3-second normal timer, one-second reduced-motion timer, first-visit display, refresh replay, same-session Home skip and back/forward skip.

The files are intended to open directly as `file://` documents. A graphical browser was not available for pixel-level layout review, so check the 320px viewport, touch targets and screen-reader behavior in your target browser before publishing. Automated checks do not replace real-device, browser and accessibility review.
