# KitabisaKerja.id

Production-grade early-career opportunity platform and interactive ATS resume engine built for **KitabisaKerja.id**, an initiative focused on youth employment in Semarang, Central Java and remote work across Indonesia.

---

## Project Background & Context

This project was built to bring to life and technically validate a business pitch developed by my friends for a national youth career venture. 

According to data from the Central Statistics Agency (BPS Sakernas), Indonesia faces a **13.14% youth unemployment rate**. Most early-career jobseekers encounter a common structural barrier: entry-level job postings demanding 2 to 5 years of prior experience, opaque salary bands, and unvetted job listings that expose beginners to recruitment fee scams.

The team authored the business model, user surveys, and initial pitch presentation (archived in this repository as `KITABISAKERJA.ID.pdf`). I took on the engineering responsibility to turn their business deck into a real, functional, ready-to-launch digital product.

---

## Role & Technical Credentials

**Lead Software Engineer & Platform Architect**  
*Full ownership of frontend architecture, UI/UX engineering, motion systems, and platform delivery.*

- **Platform Architecture & Delivery:** Architected a self-contained, high-performance web platform containing the primary landing interface, opportunity discovery engine, employer inbound portal, and client-side ATS CV studio in a single, zero-build deployable bundle.
- **Brand Identity & Vector Engineering:** Designed the mathematical SVG vector brand mark (the 4-figure collaborative crest representing mutual support across orange, yellow, blue, and green quadrants) and the accompanying typography lockup based on Plus Jakarta Sans.
- **Client-Side ATS Resume Studio:** Engineered a real-time, interactive resume builder tailored for students and fresh graduates without formal employment history. Includes an automatic heuristic ATS compatibility score meter (evaluating contact completeness, action verb density, and section structuring) and a `@media print` CSS engine for 1-click PDF exports that parse cleanly in enterprise ATS systems (Workday, Greenhouse, Lever).
- **Opportunity Catalog & Filter Engine:** Implemented instant, zero-latency multi-attribute filtering across career tracks (Internship, Part-Time, Freelance) and locations (Semarang on-site/hybrid and Remote).
- **Motion Engineering (Framer Motion):** Integrated `window.Motion` to choreograph spring-physics hover states, staggered viewport reveals, and an `IntersectionObserver`-backed scroll-spy that synchronizes the active navbar indicator to the current section.
- **Performance & Compliance:** Enforced strict compliance with Indonesian Manpower Law No. 13/2003 (zero placement fees) and Personal Data Protection standards (UU PDP No. 27/2022). Zero external icon fonts or heavy UI dependencies—100% inline SVG for instant first contentful paint.

---

## Core System Architecture

```text
├── index.html                  # Main production application (HTML5, CSS3, Framer Motion)
├── kitabisakerja_website.html  # Standalone platform mirror
├── kitabisakerja_website.pdf   # Complete high-resolution visual export of the platform
├── KITABISAKERJA.ID.pdf        # Original team business strategy and pitch presentation
├── favicon.svg                 # Scalable vector favicon (collaborative crest)
├── favicon.ico                 # Legacy browser favicon
├── favicon-32x32.png           # Raster favicon (32x32)
├── favicon.png                 # Raster favicon (64x64)
├── apple-touch-icon.png        # Mobile bookmark / iOS icon (180x180)
├── logo.svg                    # Complete horizontal brand mark (SVG)
└── README.md                   # Engineering documentation & credentials
```

---

## Key Functional Modules

### 1. Curated Opportunity Catalog
- Direct display of beginner-friendly roles based in Semarang and remote.
- Strict transparent compensation display (hourly rates for retail/hospitality, monthly stipends for internships, project fees for freelance).
- Interactive role inspection modal with full responsibility and qualification breakdown.

### 2. Standalone ATS Resume Studio
- Structured fields for education, GPA, core technical skills, leadership, and project experience.
- Real-time ATS parsing heuristic score calculated dynamically in memory.
- Standard single-column layout optimized for automated parser extraction.
- Browser print-to-PDF pipeline that strips non-document UI during print calls.

### 3. Commercial Tiers & Transparency
- **Candidate Free:** Full role discovery, basic ATS template, direct application pipeline.
- **KitabisaKerja Pro:** Unlimited CV generation, advanced ATS templates, AI bullet-point action verb suggestions, and personalized recommendations at Rp 19.999/month or Rp 199.999/year (~Rp 16.667/month).
- **Enterprise / B2B:** Structured corporate talent intake portal for local companies and campus partnerships.

---

## Local Development

Serve the repository with any static file server:

```bash
# Using Python 3 built-in server
python3 -m http.server 3000

# Or using Bun / Node
npx serve . -p 3000
```

Open `http://localhost:3000` in your browser.

---

## Operational Specifications

- **Target Market:** University students, vocational graduates, and early-career jobseekers.
- **Geographic Base:** Headquartered in Semarang, Central Java, Indonesia.
- **Legal Safeguards:** Zero recruitment fees, verified corporate registrations, and structured candidate privacy.
