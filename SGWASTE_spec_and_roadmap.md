# SGWASTE — Product Spec & Roadmap

> *A scroll-based website that makes Singaporeans feel curious and hopeful about waste — through the life stories of everyday products and a visual timeline of Singapore's environmental journey.*

---

## Part 1: Product Spec (PRD)

### Problem Statement

Singaporeans are largely disengaged from the environmental impact of their daily waste — not because they are malicious, but because the system does not require them to care. Unlike Japan and Korea, Singapore has no mandatory waste segregation policy, removing the friction that builds habitual awareness. Government statistics exist (NEA publishes annual waste data) but they are abstract, dry, and disconnected from individual behaviour. The result: recycling rates have stagnated, and Semakau Landfill — Singapore's only landfill — is projected to reach capacity by 2035. The problem is not information; it is emotional distance.

---

### Goals

1. **Spark curiosity** — At least one product story should make a visitor stop and say "I did not know that."
2. **Make the abstract feel real** — Communicate the Semakau 2035 deadline in a way that feels urgent and personal, not preachy.
3. **Build a strong portfolio piece** — Demonstrate data storytelling, UI/UX design, and frontend development skills to recruiters and lecturers.
4. **Create a neutral reference** — Provide the most accessible, visual summary of Singapore's government waste policy timeline currently available online.
5. **Respect the visitor's time** — Full experience completable in under 5 minutes. No sign-ups. No friction.

---

### Non-Goals

1. **Not a campaign or petition site.** No email capture, no calls to donate or share. This is informational, not activist.
2. **Not tracking live data.** Content is manually curated and updated. No real-time API integration in v1.
3. **Not comprehensive.** Curated to 5 hyper-Singaporean everyday products — not an exhaustive waste database.
4. **Not a mobile app (v1).** Web-first. App is a future consideration once the core experience is validated.
5. **Not a B2B or school tool.** Not designing for classroom deployment or institutional licensing.

---

### Target Users

**Primary — Curious Young Singaporean (16–35)**
Digitally fluent. Scrolls Instagram and TikTok. Cares loosely about environmental issues but has not converted that into behaviour. Does not want to be lectured. Responds to aesthetics, humour, and surprising facts. Likely finds the site via social share or school/friend recommendation.

**Secondary — Student Researcher**
Secondary school or polytechnic student doing a report or project on Singapore's environment. Needs credible, structured information quickly. Values the government timeline most.

**Tertiary — Portfolio Viewer (Recruiter / Lecturer)**
Evaluating the maker's product thinking, design sensibility, and technical execution. Reads the site as both a product and a demonstration of craft.

---

### User Stories

**As a curious young Singaporean,**
I want to see the real journey of the bubble tea cup I throw away every day, so that I can feel a genuine connection to the waste I create — not just read a statistic.

**As a curious young Singaporean,**
I want to understand what Semakau Landfill is and why it matters to me personally, so that a distant environmental problem becomes something real and close.

**As a student researcher,**
I want to browse a clear, neutral timeline of Singapore's government waste policies over the last 10 years, so that I can quickly understand what has been done and reference it in my report.

**As a student researcher,**
I want the last 6 months of policy developments to be highlighted separately, so that my research is current without having to dig through press releases.

**As a portfolio viewer,**
I want to experience a site that feels considered, beautiful, and opinionated, so that I can assess the maker's design and product thinking at a glance.

---

### Requirements

#### P0 — Must Have (MVP cannot ship without these)

| # | Requirement | Acceptance Criteria |
|---|-------------|---------------------|
| 1 | **Hero section** with a strong, Singaporean opening hook | Copy is specific to SG (not generic climate messaging). Visitor understands the site's purpose within 5 seconds. |
| 2 | **5 product life story sections** — hawker styrofoam box, bubble tea cup, Shopee cardboard box, NTUC plastic bag, e-waste (old phone) | Each shows: origin → common disposal behaviour → actual destination → decomposition timeline → scale reveal (block → town level). |
| 3 | **Semakau 2035 moment** — dedicated section, not buried in product cards | "Singapore has one landfill. It fills up in 2035." Presented as a standalone, memorable beat. |
| 4 | **Government timeline** — 10-year journey (2015–2025), last 6 months visually highlighted | Neutral framing. Milestones sourced from NEA, MSE, and official press releases. Dates and policy names accurate. |
| 5 | **Footer: What you can actually do** — 2–3 real, actionable options for Singaporeans right now | Must include: blue recycling bins, e-waste drop-off points (e.g. StarHub/M1 collection), food waste composting options. No preachy framing. |
| 6 | **Mobile responsive** | Site reads cleanly on 375px width (iPhone SE) through 1440px desktop. |
| 7 | **Free hosting** | Deployed on Vercel or Netlify. Zero ongoing cost. |
| 8 | **Cute, warm visual style** | Consistent illustration or icon style. Not clinical. Not guilt-inducing. Feels more like an exhibit than a report. |

#### P1 — Nice to Have (high-value fast follows)

| # | Requirement | Notes |
|---|-------------|-------|
| 1 | **Smooth scroll animations** | Products fade/slide in as visitor scrolls. Adds delight without adding complexity. |
| 2 | **Shareable stat cards** | Each product generates a screenshot-optimised card (e.g. "Did you know your bubble tea cup takes 500 years to decompose?") suitable for Instagram Stories. |
| 3 | **Product jump navigation** | Small sticky nav or pill buttons so visitors can jump to a specific product without scrolling through all. |
| 4 | **Dark mode** | Toggleable. Useful for portfolio presentation in a dark room. |

#### P2 — Future Considerations (design with these in mind, don't build now)

| # | Requirement | Notes |
|---|-------------|-------|
| 1 | **Personal waste calculator** | User inputs weekly habits, gets personalised annual impact. Requires form logic + state management. |
| 2 | **App version** | React Native. Reuses content and design system from web. Post-validation only. |
| 3 | **Community sightings** | Users can submit photos of waste in their area. Requires backend + moderation. |
| 4 | **NEA API integration** | Pull live recycling rate data. Requires checking if NEA exposes a public API. |

---

### Success Metrics

Since this is a student portfolio project with an educational purpose, metrics are qualitative-first:

| Metric | Target | How to Measure |
|--------|--------|----------------|
| Time on site | > 2 minutes average | Google Analytics (free) |
| Portfolio impact | Referenced or praised in ≥ 1 interview or showcase | Self-tracked |
| Organic sharing | ≥ 1 screenshot or link shared without prompting | Social monitoring |
| Completion rate | > 40% of visitors scroll past 80% of the page | Scroll depth via Analytics |
| Bounce rate | < 60% within first 10 seconds | Analytics |

---

### Open Questions

| Question | Who resolves it | Blocking? |
|----------|-----------------|-----------|
| What are the exact annual recycling rates by material (plastic, paper, glass) from 2015–2025? | Anton (NEA data research) | Yes — needed before timeline is built |
| What are the 5–6 most significant government waste policy milestones in the last 6 months? | Anton (MSE/NEA press releases) | Yes — core to timeline section |
| What illustration style? Flat vector, isometric, or hand-drawn? | Anton (design decision) | Yes — sets the visual direction for everything |
| Will there be any form of analytics / tracking? | Anton | No — can add post-launch |
| Does NEA publish open data via an API? | Anton (tech research) | No — P2 feature |

---

### Tech Stack Recommendation (Free, Student-Friendly)

| Layer | Recommendation | Cost |
|-------|----------------|------|
| Frontend | HTML/CSS/JS (vanilla) or Next.js | Free |
| Animations | GSAP (free tier) or CSS scroll animations | Free |
| Icons/Illustrations | Undraw, Flaticon, or custom SVGs | Free |
| Hosting | Vercel | Free |
| Analytics | Google Analytics 4 | Free |
| Domain | `.vercel.app` subdomain or cheap `.sg` domain (~$20/yr) | Free / Low |

---

## Part 2: Roadmap — Now / Next / Later

> Format: **Now/Next/Later** — best for a solo student builder. Avoids false precision on dates. Focuses on what's committed, what's planned, and what's directional.

---

### 🟢 NOW — Build the MVP (Weeks 1–2)

*Goal: A working, beautiful scroll experience for the core product stories. Something you can show people and get real feedback.*

| Item | Description | Status |
|------|-------------|--------|
| Project setup | Repo, Vercel deployment, basic file structure | Not Started |
| Design system | Choose illustration style, define colour palette, font pairing | Not Started |
| Hero section | Opening hook copy + layout. Anchor the SG context immediately. | Not Started |
| Product story: Hawker styrofoam box | Full life story — the most SG product on the list | Not Started |
| Product story: Bubble tea cup | Full life story | Not Started |
| Semakau 2035 section | Standalone, punchy beat — the emotional core of the site | Not Started |

**Why these first?** The Semakau moment + the two most relatable hawker-culture products give you a completable, shareable 60% of the site. You can get feedback before finishing.

---

### 🟡 NEXT — Complete + Launch (Weeks 3–4)

*Goal: Full experience live. All 5 products. Government timeline. Mobile polished. Shareable.*

| Item | Description | Status |
|------|-------------|--------|
| Product story: Shopee cardboard box | Full life story | Not Started |
| Product story: NTUC plastic bag | Full life story | Not Started |
| Product story: E-waste / old phone | Full life story | Not Started |
| Data research | Gather NEA stats (2015–2025 recycling rates, waste tonnage) | Not Started |
| Government timeline | Build the 10-year visual timeline. Highlight last 6 months. | Not Started |
| Footer: What you can do | 2–3 real, current SG options. Bloobox, e-waste bins, blue bins. | Not Started |
| Mobile responsive pass | Test on 375px, 768px, 1440px. Fix layout breaks. | Not Started |
| Soft launch | Share with 5–10 friends/classmates. Collect first reactions. | Not Started |

---

### 🔵 LATER — Polish + Extend (Month 2+)

*Goal: Turn a working site into a polished portfolio piece. Add delight. Explore next phase.*

| Item | Description | Priority |
|------|-------------|----------|
| Scroll animations | GSAP or CSS scroll-triggered reveals | High |
| Shareable stat cards | Screenshot-optimised cards for Instagram Stories | High |
| Product jump nav | Sticky pill navigation for direct product access | Medium |
| SEO + meta tags | Open Graph images, page title, description for sharing | Medium |
| Dark mode | Toggle for portfolio presentation aesthetics | Low |
| App exploration | Prototype one screen of the mobile app concept | Low |
| Personal waste calculator | User inputs habits, gets annual impact score | Low (v2) |

---

### Risk Register

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Data research takes too long (NEA stats hard to find) | Medium | High | Start data research in parallel with design. Use estimates if exact figures unavailable. |
| Illustration style takes too long to decide / execute | High | Medium | Pick one free resource (Undraw or Flaticon) and commit. Custom art is a P1, not P0. |
| Scope creep (adding products, features before launching) | High | High | Stick to 5 products. Everything else goes to LATER. |
| Government timeline is too dry | Medium | Medium | Use icons and short punchy copy — not full paragraphs. |

---

## Summary: The Three-Tool Logic

| Tool | What it did |
|------|-------------|
| 🧠 **Brainstorm** | Identified the real problem (motivation gap, not info gap), found the emotional core (Semakau 2035), defined the right tone (curious + cute, not preachy), scoped to scroll-first experience |
| 📋 **Spec** | Turned the ideas into structure — what to build, for whom, in what priority, with what success criteria |
| 🗺️ **Roadmap** | Sequenced the build into honest phases — what's committed NOW, what's planned NEXT, what's directional LATER |
