# Dr. Rajesh Kumar — Academic & Research Website

Personal academic website for **Dr. Rajesh Kumar**, Assistant Professor & Head, Department of Computer Science & Applications, CRM Jat College, Hisar, Haryana, India.

**Live:** https://rajtaya.github.io/Rkumar/

## About

A fast, accessible, mobile-responsive faculty website built with plain HTML5 + CSS (no build step, no framework). It presents research, publications, software projects, teaching, and professional service.

## Structure

```
Rkumar/
  index.html          # Homepage: hero, bio, research, selected publications, projects, teaching, contact
  research.html       # Research areas + current directions
  publications.html   # Full publications (journal / conference / books)
  projects.html       # Software projects (Aryan TechLabs)
  profile.html        # Career timeline, teaching, technical expertise, workshops, lectures, service
  assets/
    styles.css        # Design system (IBM Plex Serif/Sans/Mono; cool paper + garnet; light + dark)
    site.js           # Mobile nav + theme toggle (site works without JS)
    favicon.svg
    rajesh-kumar.jpg          # Hero portrait
    rajesh-kumar-square.jpg   # Social/OG image
  papers/             # Hosted full-text PDFs
  sitemap.xml  robots.txt
```

## Editing

### Via GitHub (quick)
1. Open the relevant `.html` file on GitHub → pencil (Edit) → commit. Live page updates in ~1 minute.

### Locally
```bash
git clone https://github.com/Rajtaya/Rkumar.git
cd Rkumar
open index.html
```

| What to change | Where |
|---|---|
| Add a publication | Add a `.pub` block in `publications.html` |
| Add a project | Add a `.card` in `projects.html` |
| Add a workshop / lecture | Add an `.event` in `profile.html` |
| Edit bio / hero | `index.html` (hero + About) |
| Colours / fonts | CSS variables at the top of `assets/styles.css` |

## Profile links

- **ORCID:** https://orcid.org/0000-0002-7897-5495
- **Email:** rajtaya@kuk.ac.in
- *Google Scholar / ResearchGate links: to be added (see `INFORMATION_REQUIRED.md`).*

## Notes

- Indexing is shown per journal only where independently verifiable.
- Software projects are production work built through Aryan TechLabs.
- See `WEBSITE_AUDIT.md`, `INFORMATION_REQUIRED.md`, and `WEBSITE_FINAL_REPORT.md` for the redesign record.

## Tech

Pure HTML5 + CSS3, minimal vanilla JS, Google Fonts (IBM Plex). Hosted on GitHub Pages.
