# Website Audit — Dr. Rajesh Kumar

**Site:** https://rajtaya.github.io/Rkumar/
**Repository:** Rajtaya/Rkumar (public, GitHub Pages, branch `main`)
**Audited:** 1 November 2026
**Working branch for the redesign:** `redesign/academic-portfolio` (original preserved on `main`)

---

## 1. Technology & structure (as-is)

| Aspect | Finding |
|---|---|
| Stack | Pure HTML5 + inline `<style>`. No JS, no framework, no build step. |
| Files | `index.html` (single 870-line page, ~43 KB), `README.md`, `papers/complexity-of-finite-state-turing-machine-2026.pdf`. |
| Hosting | GitHub Pages, served straight from `main`. Deploy = push. ~1 min to go live. |
| Navigation | None. Single long scrolling page with an in-page table of contents only. |
| Responsive | Only the infobox stacks on mobile (`@media max-width:768px`). All `.wikitable` tables will overflow horizontally on phones. |
| SEO | `<title>` only. **No** meta description, canonical, Open Graph, Twitter cards, favicon, `sitemap.xml`, `robots.txt`, or structured data. |
| Accessibility | Decorative avatar has no alt text; many links are `href="#"` placeholders; contrast generally OK; no skip-link; no landmarks beyond `<div>`s. |

**Verdict:** The foundation is clean and dependency-free (good), but the page is a single undifferentiated document with no real navigation, no discoverability, and no mobile table strategy.

---

## 2. CRITICAL — the site impersonates Wikipedia

This is the headline finding and it dominates everything else.

The entire page is skinned as a **fake Wikipedia article**:
- `<title>`: "Rajesh Kumar (computer scientist) - Wikipedia"
- Wikipedia "W" logo, "The Free Encyclopedia" wordmark, and nav (Main page / Contents / Random article…)
- Article / Talk / Read / Edit / View history tab bar
- Infobox styled as a Wikipedia infobox, lead paragraph written in third person ("Kumar specialises in…")
- Footer: *"This page was last edited on 19 October 2026 · Content is available under Creative Commons Attribution-ShareAlike 4.0 License · About Wikipedia…"*
- Wikipedia-style category links ("Living people", "1984 births", …)

**Why this is critical, not cosmetic:**
1. **Credibility damage.** To any academic, collaborator, or journal editor who knows what a real Wikipedia URL looks like (`en.wikipedia.org`), a self-hosted page dressed as a Wikipedia article reads as *fabricated authority* — the opposite of the credibility the brief wants to build. A genuine faculty profile is far more trustworthy than a fake encyclopedia entry.
2. **Impersonation.** It reproduces the Wikimedia Foundation's name, logo, wording, and CC-license footer on a page that is not Wikipedia. That is trademark/identity misuse.
3. **It undermines the whole brief.** Phases 2–13 all assume a genuine personal academic website.

**Proposed correction:** Remove the Wikipedia theme entirely and rebuild as a genuine, modern academic/faculty personal website (clean typography, real top navigation, multi-section layout) under Dr. Kumar's own identity. This is the core of the redesign.

---

## 3. HIGH — content accuracy & research integrity

The brief explicitly forbids inventing or overstating credentials and asks for careful review of indexing claims. These are the issues found:

| # | Severity | Finding | Proposed correction |
|---|---|---|---|
| 3.1 | High | **Blanket indexing claim:** "15 research papers in journals indexed in UGC CARE, Scopus, and SCI" (stated in lead + publications intro). The journals listed (IJARCSSE, IJCSMC, IJSCE, IJRCS, Advanced Research Int'l Pub. House, Blue Eyes, etc.) are **not** SCI/SCIE-indexed and most are not Scopus-indexed; several are widely regarded as predatory. The claim is not supportable as written. | Remove the blanket "indexed in UGC CARE, Scopus and SCI" sentence. State indexing **per journal, only where independently verified**, else mark "Indexing not independently verified." (See INFORMATION_REQUIRED.md.) |
| 3.2 | High | **Publication #13 "One-Way Tape Deterministic PDA" in *REDVET – Revista electrónica de Veterinaria* (2023).** A computer-science paper in a **veterinary** journal is a classic hijacked/predatory-journal signature. (Flagged previously; kept by owner.) | Recommend removing, or clearly labelling it and dropping any indexing claim. **Owner decision required** — see INFORMATION_REQUIRED.md. |
| 3.3 | High | **#14 is a conference paper in the journal table.** Row 14 is explicitly "National Conference … (NC DAIFC-2026)" yet sits in the journal/publisher table (published in IJRCS special issue). The brief flags exactly this. | Split publications into **Journal Articles / Conference Papers / Books & Chapters**; place #14 under Conference Papers (or clearly mark it a conference-proceedings special issue). |
| 3.4 | High | **ORCID vs site mismatch.** The ORCID record (`0000-0002-7897-5495`, confirmed his) lists only **3 unique works** (2026 CSIT; 2019 IJITEE; 2019 IJECE). 12 of the 15 are not discoverable via ORCID. | Keep all verified records, but treat ORCID-listed ones as the independently verifiable core; add the rest to ORCID over time. Do not claim ORCID verification for papers not on it. |
| 3.5 | Medium | **"h-index of 1"** is stated inline. The brief says show metrics only if verified from the live profile, with a retrieval date. | Remove the inline h-index. Only show Scholar metrics (citations / h / i10 + date) once a real Google Scholar URL is supplied. |
| 3.6 | Medium | **Software-development portfolio authorship.** The site claims an extensive full-stack stack (NestJS, Next.js, Prisma, React Native, etc.) and the brief wants a Projects page of real repos. The `Rajtaya` GitHub repos (College ERP, UEMS, Namankan, …) appear to be **Aryan TechLabs / family builds**, not clearly Dr. Kumar's personal authored work. | **Owner decision required:** which projects may be legitimately presented as his own, and at what framing (e.g. "led/supervised" vs "developed"). Do not fabricate a portfolio. |

---

## 4. HIGH — privacy (brief Phase 9)

| # | Severity | Finding | Proposed correction |
|---|---|---|---|
| 4.1 | High | **Exact date of birth exposed** ("3 August 1984", repeated in infobox, lead, and Early-life). Brief Phase 9 says remove exact DOB. | Remove DOB. Keep professional identity only. |
| 4.2 | Medium | **Birthplace / "1984 births" / "Living people" categories** add personal data with no professional value. | Remove the Wikipedia category block entirely. |
| 4.3 | Medium | "Website" field in the infobox actually contains the **email** (`rajtaya@kuk.ac.in`), mislabeled. | Label email as email; add real profile URLs as the web presence. |

> Note: no phone number or home address is present in `index.html` (good — earlier CV versions had them).

---

## 5. MEDIUM — broken / placeholder links & dead ends

| # | Finding | Correction |
|---|---|---|
| 5.1 | ~40 links are `href="#"` placeholders (Google Scholar, ResearchGate, CRM Jat College, Kurukshetra University, and nearly every inline term). | Wire real URLs where they exist; otherwise remove the link and keep plain text. Collect missing URLs in INFORMATION_REQUIRED.md. |
| 5.2 | ORCID is the **only** working external link. | Build a proper "Profiles" block: ORCID (live), Google Scholar, ResearchGate, GitHub, institutional email — real URLs only. |
| 5.3 | No GitHub link anywhere, despite the dev-portfolio emphasis. | Add once authorship framing is confirmed (§3.6). |

---

## 6. MEDIUM — inconsistent / incorrect terminology & data

| # | Finding | Correction |
|---|---|---|
| 6.1 | **Affiliating university conflict:** `index.html` says CRM Jat College is under **Guru Jambheshwar University of Science & Technology (GJUST), Hisar**; `README.md` says **Chaudhary Ranbir Singh University (CRSU), Jind**. Both cannot be current. | Confirm the correct current affiliating university (see INFORMATION_REQUIRED.md) and use it consistently. |
| 6.2 | **ORCID typo in README** (`0000-0002-789X-5495`) vs correct `0000-0002-7897-5495` in `index.html`. | Fix README. |
| 6.3 | **Counts drift:** README says "13 publications / 18 workshops"; `index.html` shows 15 publications / 31 workshops. | Use one source of truth; make counts match the tables. |
| 6.4 | **Current vs former roles blurred.** "Assistant Professor & Head" is shown as current; UCK (2009–2010) and DCSA KUK (2010–2014) are former. NAAC Coordinator / Exam Superintendent / NEP Science Coordinator are listed without "current vs past" framing. | Timeline with explicit durations; separate current responsibilities from past ones (brief Phase 5 & 8). |
| 6.5 | Research interests under-weight the stated **primary** direction. Brief wants Theoretical CS / Automata / Computational Complexity / Formal Verification **primary**, with SBSE/GA/ML as *additional*. Current list mixes them flat and omits Multi-Pushdown Systems / bounded reachability. | Re-organize research into Primary areas + "Current Research Directions" (clearly labelled as ongoing, not proven). |

---

## 7. LOW — design / UX

- No real site navigation; everything is one scroll.
- "RK" monogram avatar instead of a photo (brief: use a real photo when supplied; placeholder otherwise — **do not** generate a fake photo).
- Tables are information-dense and will not reflow on mobile.
- Serif Wikipedia typography; the redesign should use a clean, restrained academic palette and type system.
- No dark-mode handling (optional).

---

## 8. Proposed redesign (maps to brief phases)

1. **Scrap the Wikipedia skin** → genuine faculty site: sticky top nav, hero, section layout. *(Critical fix §2.)*
2. **Homepage** — hero (name, title, institution, tagline, profile links, photo placeholder), ~120-word bio (consistent voice), then concise linked sections.
3. **Research** — Primary areas (Automata Theory, Computational Complexity, Formal Verification) + Additional (SBSE, GA/Metaheuristics, AI/ML) + a clearly-labelled "Current Research Directions" (Multi-Pushdown Systems, bounded reachability).
4. **Publications** — split Journal / Conference / Books & Chapters; per-item indexing only where verified; fix §3.1–3.4.
5. **Career & Teaching** — timeline with durations; courses list.
6. **Projects** — only legitimately-attributable work, correctly framed (§3.6).
7. **Technical expertise** — grouped categories, evidence-based, no percentage bars.
8. **Contributions** — books, FDPs/workshops, lectures, refresher courses, admin roles.
9. **Privacy** — strip DOB, birthplace, categories (§4).
10. **SEO & a11y** — full meta/OG/canonical, `sitemap.xml`, `robots.txt`, JSON-LD `Person`/`ProfilePage`, semantic landmarks, alt text, skip link.
11. **QA** — mobile/tablet/desktop, link check, DOI check, console/validation, then `WEBSITE_FINAL_REPORT.md`.

**Nothing in this plan is implemented yet.** Per the brief, implementation proceeds after you confirm direction and the open decisions in `INFORMATION_REQUIRED.md`. No change will be deployed without your approval; the original remains on `main`.
