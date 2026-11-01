# Website Final Report — Dr. Rajesh Kumar

**Date:** 1 November 2026
**Branch:** `redesign/academic-portfolio` (original preserved on `main`)
**Status:** Built and QA-passed locally. **Not deployed** — awaiting your review and approval to merge to `main`.

---

## 1. What changed, in one line

The site was a **fake-Wikipedia article**. It is now a **genuine, modern, multi-page academic faculty website** under Dr. Rajesh Kumar's own identity — faster, mobile-responsive, accessible, SEO-ready, and with corrected, honestly-framed content.

## 2. Pages created

| Page | Purpose |
|---|---|
| `index.html` | Homepage — hero (photo, name, role, tagline, actions), bio, primary research, selected publications, selected projects, teaching, contact. |
| `research.html` | Primary areas (Automata Theory, Computational Complexity, Formal Verification), additional/applied interests, and a clearly-labelled **Current research directions** (multi-pushdown systems, bounded reachability — marked ongoing/unpublished). |
| `publications.html` | Full list split into **Journal articles / Conference papers / Books & chapters**, with an honest indexing note. |
| `projects.html` | Software built through **Aryan TechLabs**, split into institutional software and tools; public repos linked, private deployments marked. |
| `profile.html` | Career timeline, courses taught, technical expertise by area, workshops/FDPs/conferences, invited lectures, refresher courses, administrative service. |

## 3. Files modified / created

**New:** `research.html`, `publications.html`, `projects.html`, `profile.html`, `assets/styles.css`, `assets/site.js`, `assets/favicon.svg`, `assets/rajesh-kumar.jpg`, `assets/rajesh-kumar-square.jpg`, `sitemap.xml`, `robots.txt`, `WEBSITE_AUDIT.md`, `INFORMATION_REQUIRED.md`, `WEBSITE_FINAL_REPORT.md`, `.claude/launch.json`.
**Rewritten:** `index.html` (from Wikipedia skin → academic homepage), `README.md`.
**Kept:** `papers/complexity-of-finite-state-turing-machine-2026.pdf` (now linked as full text).

## 4. Issues resolved (from WEBSITE_AUDIT.md)

| Audit item | Resolution |
|---|---|
| §2 Wikipedia impersonation (Critical) | **Removed entirely.** New identity, nav, layout, typography; no Wikipedia logo, tabs, CC footer, or categories. |
| §3.1 Blanket "indexed in UGC CARE, Scopus & SCI" | **Removed.** Indexing shown per journal only where verifiable; an explicit note states so. ORCID-listed papers flagged. |
| §3.2 REDVET paper #13 | **Kept at your instruction**, presented as a journal article with **no** indexing claim. |
| §3.3 Conference paper in journal table (#14) | **Moved** to a dedicated Conference papers section. |
| §3.4 ORCID vs site mismatch | 2026 CSIT + two 2019 papers labelled "Listed on ORCID"; ORCID linked. |
| §3.5 "h-index of 1" inline | **Removed.** No metrics shown until a verified Scholar profile is supplied. |
| §3.6 Dev-portfolio authorship | Framed honestly as **Aryan TechLabs** (your company); prototypes vs production distinguished. |
| §4.1–4.3 Privacy (DOB, birthplace, categories, mislabeled "website") | **DOB, birthplace, and all Wikipedia categories removed.** Email labelled as email; profiles block added. |
| §5 Broken `href="#"` links | **Zero** dead `#` links remain; real URLs wired (ORCID, email, public repos); unknown ones shown as clearly-marked "link pending". |
| §6.1 University conflict | **GJUS&T, Hisar** used consistently; README's CRSU reference removed. |
| §6.2 README ORCID typo | Fixed (`0000-0002-7897-5495`). |
| §6.3 Count drift | Counts now match the tables. |
| §6.4 Current vs former roles | Timeline with durations; current role marked. |
| §6.5 Research under-weighting TCS | Research reorganised: TCS primary, SBSE/GA/AI additional, bounded-reachability as current direction. |
| §7 Design / no nav / table overflow | New design system, sticky nav, dark mode; publications/workshops use reflowing list layouts (no horizontal scroll on mobile). |

## 5. Design & build

- **Stack:** plain HTML5 + one shared CSS file + ~1 KB vanilla JS. No framework, no build step. Site works with JS disabled.
- **Type:** IBM Plex Serif / Sans / Mono (Google Fonts). **Palette:** cool paper, slate-navy ink, academic garnet accent; full light + dark mode (auto + manual toggle, remembered).
- **SEO:** per-page `<title>` + meta description + canonical + Open Graph/Twitter; `sitemap.xml`; `robots.txt`; JSON-LD `ProfilePage`/`Person` on the homepage; semantic landmarks.
- **Accessibility:** skip link, keyboard focus styles, `aria-current`, labelled nav/toggles, alt text on the photo, `prefers-reduced-motion` respected.

## 6. Test results (local, served at :4510)

- All 5 pages return HTTP 200; all CSS/JS/image/PDF assets 200.
- **No console errors** on any page.
- Responsive verified at mobile (375 px) and desktop: hero photo aspect fixed, mobile menu opens, tables/lists reflow with no horizontal scroll.
- Dark mode verified and persists across pages.
- No leftover `href="#"` placeholder links.
- External DOI `10.11591/csit.v7i2.p196-202` resolves (→ iaesprime.com). ORCID link live.

## 7. Still needs your input (see INFORMATION_REQUIRED.md)

Non-blocking — the site is complete and correct without them, and each is an easy later fill-in:
- **Google Scholar / ResearchGate URLs** (currently shown as "link pending"). With a verified Scholar URL I can add citation/h-index/i10 metrics with a retrieval date.
- Confirm the **Head of Department appointment year** (timeline currently says "July 2014 – present" for the combined role).
- Any **indexing evidence** you want cited per journal.
- A LinkedIn URL, if you want one linked.

## 8. Deployment instructions

Nothing is live yet. When you approve:

```bash
cd Rkumar
git checkout main
git merge redesign/academic-portfolio
git push origin main
```

GitHub Pages will rebuild in ~1 minute at https://rajtaya.github.io/Rkumar/.
Prefer a safer review first? I can push the branch and open a pull request so you can read the diff before anything reaches `main`.

*(The `.claude/launch.json` is only a local preview helper; harmless to keep or delete.)*
