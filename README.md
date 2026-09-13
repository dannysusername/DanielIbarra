# Daniel Ibarra — Portfolio

**It's live — just open it in your browser:**

### 👉 https://portfoliosite-f324a95ed6cd.herokuapp.com/

A single-page portfolio: who I am, the projects I've built, my stack, and how to reach me. No install, nothing to download — the link above is the whole thing.

---

## About me

Hello! My name is Daniel Ibarra. I am a student at Florida International University pursuing a Bachelor of Science in Computer Science, with an expected graduation in Summer 2027. My main experience is in Java, Spring, PostgreSQL, HTML, CSS, and JavaScript. I love building things that are useful for myself and others, so I have dabbled in tons of other languages and technologies.

My main focus is to become a backend software engineer, with a goal of working at SpaceX because their goal of going to Mars fascinates me. I am specializing in backend web development using Java, Spring, PostgreSQL, and CI/CD. I have built multiple Spring Boot applications and deployed them on Heroku.

I enjoy all sorts of outdoor and indoor activities like sailing, hiking, and swimming. I like building home automation projects for my family using Raspberry Pis.

## What it is

A self-contained personal portfolio for Daniel Ibarra, a backend developer and computer-science student. One page, with:

- **About** — short intro and a profile card.
- **Skills** — animated proficiency meters (Java, Python, JavaScript, PostgreSQL) plus categorized tech chips grounded in real project work.
- **Projects** — Aviary, Deadhead, RapidAid, Compass, and Pit Stop, each with its app icon, description, tech tags, and live + GitHub links.
- **Certifications** — each credential with a verify link.
- **Work experience** — each job with its logo (linked to the company's LinkedIn), plus an "open to opportunities" panel.
- **Education** — FIU and Christopher Columbus High School, each linked to its LinkedIn page.
- **Contact** — email, GitHub, LinkedIn, and a downloadable résumé.

The top nav collapses to a hamburger menu on screens under 900px, so it reads well on mobile.

## Featured projects

| Project | What it is | Live | Code |
|---|---|---|---|
| **Aviary** | Aircraft maintenance & flight-hours tracker for general-aviation owners | [open](https://aviarist-d300b0c36379.herokuapp.com/login) | [repo](https://github.com/dannysusername/Aviary) |
| **Deadhead** | Charter trip optimizer: the cheapest way to fly a week of client trips | [open](https://deadhead-planner-71dc1c210944.herokuapp.com/login) | [repo](https://github.com/dannysusername/Deadhead) |
| **RapidAid** | Disaster-relief aid-matching app with AI request categorization | [open](https://main.d2h3lh72uw4b1b.amplifyapp.com) | [repo](https://github.com/dannysusername/RapidAId) |
| **Compass** | School task tracker that parses syllabus PDFs into a calendar | [open](https://dannibar-compass-44cf6055d5e3.herokuapp.com/) | [repo](https://github.com/dannysusername/Compass) |
| **Pit Stop** | Team capstone: collaborative car maintenance tracker with vehicle sharing | [open](https://pitstop-8463842bfa02.herokuapp.com) | [repo](https://github.com/team-PitStop/PitStop) |

---

## Editing

The design source is **[Portfolio.dc.html](Portfolio.dc.html)**, a Claude Design canvas: markup with inline styles, a `<helmet>` style block, and a small component script run by the design tool. Browsers can't run that file directly, so the page actually served is **[index.html](index.html)**, generated from it:

```bash
npm run export     # runs career-sync's export_portfolio.py
```

- **Never hand-edit `index.html`.** Change `Portfolio.dc.html`, then re-export.
- **Certifications, work experience, and education** are generated from the career-sync registry: `sync_profile.py` writes them into the canvas between `career-sync` markers.
- **Assets** — images in [images/](images/), résumé at [Daniel_Ibarra_CV.pdf](Daniel_Ibarra_CV.pdf) (a copy of the approved résumé).

**Preview locally:**

```bash
npm install
npm start          # http://localhost:5050
```

## Deployment

Hosted on **Heroku** as a static site: `npm start` runs [serve](https://github.com/vercel/serve) on the port Heroku assigns. No build step.

| Environment | App | URL |
|---|---|---|
| Production | `portfoliosite` (eco dyno) | https://portfoliosite-f324a95ed6cd.herokuapp.com/ |

- **Deploy:** export, commit, then `git push heroku main` (remote `https://git.heroku.com/portfoliosite.git`).
- ⚠️ Eco dynos sleep when idle, so the first visit after a quiet spell takes a few seconds.

---

© Daniel Ibarra — personal project.
