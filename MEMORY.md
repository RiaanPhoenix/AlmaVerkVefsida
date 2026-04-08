# MEMORY.md — AlmaVerkVefsida Project

> Living document. Update this whenever meaningful work happens.

---

## Project Overview

**Client:** Alma Verk  
**Project name:** AlmaVerkVefsida  
**Repo:** `git@github.com:RiaanPhoenix/AlmaVerkVefsida.git`  
**Local path:** `/home/claw/.openclaw/workspace-worker-two/almaverk/`  
**Language:** Icelandic (`lang="is"`)  
**Stack:** Plain HTML/CSS/JS — single-page, no framework, no build step  
**Status:** Early prototype — functional but placeholder data throughout

---

## What Exists (as of 2026-03-28)

### Single file: `index.html`
A complete single-page marketing website for Alma Verk, an Icelandic earthworks/excavation company.

#### Sections (top to bottom)
| ID | Section | Notes |
|----|---------|-------|
| — | `<nav>` | Fixed top nav, becomes opaque on scroll via JS |
| `#top` | Hero | Full-viewport hero with background image (Unsplash), headline, two CTA buttons |
| — | Strip | Orange CTA bar with phone number |
| `#um-okkur` | About | Two-column grid: image + text + stats (15+ yr, 500+ verk, 100%, 24h) |
| `#thjonusta` | Services | 3-column grid of 6 service cards with inline SVG icons |
| — | Dark CTA | Full-width dark section with quote prompt |
| `#verkin` | Portfolio | CSS grid gallery, 5 placeholder items with Unsplash images |
| — | Process | 4-step dark process section |
| `#samband` | Contact | Two-column: contact info + form (non-functional, `onsubmit="return false;"`) |
| — | Footer | 3-column footer with nav links |

#### Design tokens
```
--accent:  #F0542D  (orange-red)
--dark:    #1a1a1a
--mid:     #2e2e2e
--light:   #f5f5f5
--gray:    #767676
--white:   #ffffff
```

#### Fonts
- **Raleway** — headings, nav, labels (Google Fonts)
- **Lato** — body copy (Google Fonts)

#### Logo
SVG triangle with orange lightning-bolt inset. Text: `ALMA VERK`.

---

## Placeholder / TODO Items

These are things that need real content before going live:

- [ ] **Phone number** — currently `555 1234` (fake). Replace with real number.
- [ ] **Email** — currently `info@almaverk.is`. Confirm this is live.
- [ ] **Hero background image** — Unsplash URL (`photo-1504307651254-35680f356dfd`). Needs real photo.
- [ ] **About image** — Unsplash URL (`photo-1581094794329-c8112a89af12`). Needs real photo.
- [ ] **Portfolio images** — All 5 are Unsplash placeholders. Needs real project photos.
- [ ] **Portfolio captions** — Placeholder project names (Reykjavík, Kópavogur, Garðabær, etc.). Confirm real projects.
- [ ] **Stats** — 15+ ára, 500+ verk, 100% ánægðir, 24h svartími. Confirm with client.
- [ ] **Contact form** — Currently does nothing (`return false`). Needs backend or mailto/Formspree hookup.
- [ ] **"Sjá fleiri verk"** button — links to `#samband`. Should probably link to a real gallery or just removed.
- [ ] **Favicon** — None set.
- [ ] **OG/meta tags** — No description, og:image, or twitter card tags.
- [ ] **Typo** — "Efnisflutnigur" (should be "Efnisflutningur") — appears in service card and footer.
- [ ] **Mobile nav** — `.nav-links` hidden on mobile (`display:none`) with no hamburger menu. Needs mobile nav solution.

---

## Git History

| Commit | Message |
|--------|---------|
| `e69acb6` | `feat: initial Alma Verk prototype landing page` |

One commit. Clean working tree. Branch: `main`. Tracking `origin/main`.

---

## Decisions & Notes

- **2026-03-28** — Project set up. Single `index.html` prototype committed. Memory file created to track progress.
- Design is dark/bold with orange accent — fits the heavy machinery / industrial sector well.
- All content is in Icelandic. Keep it that way unless client requests otherwise.
- No dependencies, no package.json — keep it that way unless complexity warrants a build step.

---

## Known Issues

1. **Typo:** "Efnisflutnigur" → should be "Efnisflutningur" (service card + footer link)
2. **Mobile nav:** No hamburger — users on mobile have no nav access
3. **Contact form:** Non-functional
4. **External font/image deps:** Site won't load properly offline (Google Fonts + Unsplash)

---

## Next Steps (suggested)

1. Fix the "Efnisflutningur" typo
2. Add mobile hamburger nav
3. Wire up contact form (Formspree or mailto fallback)
4. Replace Unsplash images with real Alma Verk photos
5. Add favicon and meta/OG tags
6. Confirm/correct placeholder stats and contact details

---

*Last updated: 2026-03-28*
