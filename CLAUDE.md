# Portfolio — Claude Context

This file gives Claude persistent context about this project.
Update it whenever decisions are made, preferences are set, or scope changes.

---

## Project Overview

**Type:** Personal portfolio / CV website
**Owner:** Rayyan Abzal
**File:** Single-file `index.html` — no build step, no dependencies
**Purpose:** Showcase projects, CV/experience, and act as a contact point for employers/collaborators

---

## Design Theme

**Batman / Batcave / Gotham City noir**

- Background: near-black `#020204` with cold blue tint
- Primary accent: Batman yellow `#f5c842` — used for all highlights, glows, interactive states
- Typography: Georgia serif (editorial/gothic) for headings; Courier New monospace for labels/nav (Batcomputer feel); system-ui for body
- **No external dependencies** — no CDN fonts, no frameworks, pure HTML/CSS/JS

### Active atmospheric effects (do not remove):
- Canvas rain (300 blue-tinted drops, wind-angled)
- Random lightning flash overlay (~every 8–12s)
- Bat Signal pulsing radial glow in hero
- Gotham SVG skyline with gothic spires + lit windows at hero bottom
- 4 flying bat silhouettes looping across the hero
- CRT scanline texture overlay (body::after)
- Glitch animation on hero name (every 7.5s, RGB chromatic aberration)
- Typewriter effect on hero subtitle on load
- Custom yellow cursor dot + ring with smooth lag

---

## Real Content (from CV)

**Personal:**
- Email: rayyanabzal@gmail.com
- Location: Auckland, NZ (36.8485° S, 174.7633° E)
- Status: Seeking Junior Software Engineer Internship / Graduate role

**Education:**
- AUT — BEng (Hons) Software Engineering, Minor in AI — Mar 2023–Present
- Techtorium NZIIT — NZ Diploma Software Development Level 6 — 2021
- Techtorium NZIIT — NZ Diploma Information Systems Level 5 — 2020
- Selwyn College, Auckland — 2016–2019

**Work Experience:**
- Country Road — Sales Consultant (Part-time) — Aug 2025–Present
- Heartland Bank — Hardship Officer (Full-time) — Dec 2023–Mar 2024
- Heartland Bank — Customer Service Business Consultant (Full-time) — Aug 2022–Mar 2023
- Zara — Operations Team Member (Casual) — Apr 2022–Aug 2022
- Macpac — Retail Team Member (Part-time) — Mar 2019–Oct 2019

**Projects:**
1. Fragrance Product Intelligence SaaS — Founder & Lead Dev — Nov 2025–Present
2. Delta Gaming — SaaS Business Owner — 2020–2022
3. Predictive ML Model — AUT coursework

**Skills (real):** Python, Java, SQL, R, C++, C# | ASP.NET, REST APIs, HTML/CSS, Android Studio | Git/GitHub, Azure, CI/CD, MVC | ML, Data Analysis, Predictive Modelling

- GitHub: https://github.com/RayyanAbzal
- LinkedIn: https://www.linkedin.com/in/rayyan-a-832a20213

---

## Structure

```
index.html          # Everything — all HTML, CSS, JS in one file
CLAUDE.md           # This file
```

Sections (in order):
1. `#hero` — Full-viewport intro, skyline, bat signal, typewriter
2. `#about` — Bio + skill chips
3. `#projects` — 3-column card grid (stacks to 1 on mobile)
4. `#experience` — Work Experience timeline (Country Road, Heartland Bank ×2, Zara, Macpac)
5. `#education` — Education timeline (AUT, Techtorium ×2, Selwyn College)
6. `#contact` — Social links + contact form

---

## Coding Conventions

- All CSS uses `var(--*)` custom properties — edit variables at the top of `<style>` to retheme
- Scroll reveal: add class `rev` (+ `d1`–`d4` for stagger delay) to any element
- Section structure: `.wrap` > `.s-head` > content
- Buttons: `.btn.btn-bat` (yellow filled) or `.btn.btn-ghost` (outlined)
- Skill chips: `<span class="chip">` inside `.chips` inside `.skill-grp`
- Project cards: `.proj-card` — include `.top-bar` div as first child for the hover sweep animation
- Timeline items: `.tl-item` inside `.timeline`

---

## Preferences & Rules

- **No external dependencies** — keep everything inline in `index.html`
- **Do not remove atmospheric effects** — rain, lightning, bats, skyline, glitch are core to the theme
- **Single file only** — resist splitting into multiple files unless explicitly asked
- **Mobile responsive** — breakpoints at 920px and 600px; test both
- **Custom cursor** — hidden on touch devices automatically
- **Yellow glow** — interactive elements should have subtle `box-shadow: 0 0 Npx rgba(245,200,66,0.X)` on hover
- Keep the footer credit "Gotham's Finest Developer" — it's intentional flavour

---

## Future Ideas (not yet built)

- [ ] Add a 4th project card
- [ ] Photo/avatar in the About section
- [ ] PDF CV download button in hero
- [ ] Dark/light toggle (would need full theme rework)
- [ ] Testimonials / recommendations section
- [ ] Blog or writing section

---

## Changelog

| Date | Change |
|---|---|
| 2026-03-22 | Initial build — clean dark editorial theme |
| 2026-03-22 | Redesigned to Batman/Batcave/Gotham noir theme with rain, lightning, bat signal, skyline, flying bats, glitch, typewriter |
| 2026-03-22 | Removed lightning effect and nav bat logo per user request |
| 2026-03-22 | Populated all real CV content — bio, skills, 3 real projects, 5 experience items, real email |
| 2026-03-22 | Glitch animation reduced from every 7.5s to every 30s (was too distracting) |
