# THE BLIND CENTER DIGITAL CAMPUS
## Codex Master Build Package for a Static GitHub Pages Website

**Version:** 1.0  
**Prepared for:** Beaufort County Association for the Blind and Visually Impaired  
**Public-facing name:** The Blind Center  
**Primary address:** 221 North Harvey Street, Washington, North Carolina 27889  
**Deployment target:** GitHub Pages  
**Development environment:** Local machine in a Git-synchronized repository  
**Primary implementation assistant:** Codex  
**Purpose:** Replace and modernize the existing website using the architecture, language, accessibility principles, content system, page copy, workflows, and design system in this document.

---

# 0. HOW CODEX SHOULD USE THIS FILE

Treat this file as the master requirements document and primary source of truth for the new website.

Build a production-quality, mobile-first, static website that:

- Can be developed locally.
- Is committed to a GitHub repository.
- Builds successfully in GitHub Actions.
- Deploys to GitHub Pages.
- Uses relative-path-safe URLs.
- Is usable without JavaScript for essential content.
- Meets WCAG 2.2 AA at minimum.
- Is especially comfortable for visitors with blindness, low vision, reduced contrast sensitivity, limited dexterity, cognitive fatigue, and age-related changes in vision.
- Can be maintained by nontechnical staff through Markdown, MDX, YAML, JSON, or simple data files.
- Does not require a traditional server or database for launch.
- Can later be migrated to a headless CMS without rewriting the visual system.

## 0.1 Preferred static stack

Use one of these options, in this order:

1. **Astro + TypeScript + accessible vanilla CSS**
2. Eleventy + Nunjucks/Liquid + vanilla CSS
3. Jekyll only if the existing repository is already Jekyll-based

For a new build, use Astro because it supports static generation, Markdown content collections, reusable components, excellent performance, and GitHub Pages deployment.

Do not use Next.js unless it is configured for a fully static export and no server features are required.

## 0.2 Required implementation behavior

- Create semantic HTML landmarks: `header`, `nav`, `main`, `aside`, `footer`.
- Include a visible-on-focus “Skip to main content” link.
- Use proper heading order.
- Use native elements before ARIA.
- Do not create custom buttons from `div` elements.
- Do not hide important information inside hover-only interactions.
- Do not use carousels.
- Do not use auto-advancing sliders.
- Do not autoplay audio.
- Respect `prefers-reduced-motion`.
- Allow browser text enlargement to at least 200% without loss of content.
- Support keyboard navigation throughout.
- Use large tap targets of at least 44 by 44 CSS pixels.
- Maintain strong focus indicators.
- Use descriptive links. Avoid repeated “Learn More” links without context.
- Do not depend on color alone to communicate meaning.
- Do not publish invented hours, prices, eligibility rules, staff names, statistics, or program promises.
- Use clearly labeled content placeholders where operational facts still require confirmation.

## 0.3 Decisions already resolved

- Do not present ENCight Gardens as a current property or active program. The property was sold.
- Professionals located on campus are independent service providers. The Blind Center provides space but does not supervise, manage, employ, affiliate with, or direct their clinical or professional services.
- A social worker is available on campus twice per week, subject to current scheduling and agency availability.
- The Community Innovation Hub and Community Solutions Lab are planned for 2027.
- The public-facing educational destination is called **The Discovery Center**.
- The educational division is called **ENCight Academy**.
- Membership is called **Friends of The Blind Center**.
- The building should be described as **The Blind Center Community Center**, not merely an office.
- The homepage must give immediate prominence to emergency replacement eyeglasses.
- The website must be organized around visitor goals rather than the organization chart.

---

# 1. EXECUTIVE VISION

## 1.1 What this website is

The Blind Center Digital Campus is the online extension of a community institution. It should not feel like a small nonprofit brochure, a medical portal, or a government-service directory.

It should combine the confidence and depth of:

- A university extension program
- A Smithsonian-style discovery destination
- A community center
- A practical resource navigator
- An accessible learning platform
- A professional commons
- A membership organization
- A transparent nonprofit institution

The visitor should feel invited to explore, but never forced to explore when immediate help is needed.

## 1.2 Digital mission

Help people discover the knowledge, tools, skills, services, support, and community they need to:

- Protect and understand vision.
- Adapt to vision changes.
- Obtain eyeglasses when cost or emergency creates a barrier.
- Live more independently.
- Use technology with confidence.
- Build healthier lives.
- Support a family member or friend.
- Find the correct community resource.
- Learn throughout life.
- Participate in community.
- Volunteer or give.
- Connect with independent professionals located on campus.

## 1.3 Desired visitor responses

A successful visit should produce one or more of these thoughts:

- I belong here.
- I am not alone.
- I understand this better.
- There is a practical next step.
- I can do this.
- I know where to ask for help.
- I trust this organization.
- I want to return.

## 1.4 Four public pillars

### Discover

Discovery Journeys, Discovery Guides, eye-health education, research spotlights, stories, resources, and topic collections.

### Learn

ENCight Academy, workshops, classes, Community Learning Kitchen, Technology Discovery Lab, and the ENCight Experience Apartment.

### Connect

Friends of The Blind Center, Volunteer Center, Community Resource Network, events, support groups, and Professional Services on Campus.

### Build

The Professional Commons, partnerships, university collaborations, Community Innovation Hub, and Community Solutions Lab.

## 1.5 Brand voice

The voice must be:

- Warm
- Calm
- Knowledgeable
- Practical
- Respectful
- Hopeful
- Evidence-aware
- Plain-language
- Community-centered
- Professional without being corporate

Avoid:

- Pity
- Savior narratives
- Fear-based fundraising
- Unexplained medical jargon
- Talking about people as diagnoses
- Overpromising
- Infantilizing language
- Treating accessibility as a special feature
- Statements that imply every service is directly provided by The Blind Center

## 1.6 Editorial principles

Every page should answer:

1. What do I need to know?
2. Why does it matter?
3. What can I do today?
4. Where should I go next?

Every substantive educational page should also support:

- Print
- Large-text reading
- Future audio narration
- Future downloadable PDF
- Related resources
- Related classes
- A clear next step

---

# 2. AUDIENCES AND PRIMARY JOURNEYS

## 2.1 Person needing immediate help

Common situations:

- Glasses are broken, lost, or unusable.
- Cost prevents obtaining eyeglasses.
- Vision has suddenly or gradually changed.
- Mail, medicine labels, bills, or forms are difficult to read.
- Technology has become frustrating.
- The person does not know which agency or service to contact.

Primary journey:

`Home → Need Help Today → Start Here or Eyewear Center → Request Assistance`

## 2.2 Person who is blind or has low vision

Common goals:

- Stay in the current home.
- Read independently.
- Cook, shop, travel, work, or volunteer.
- Use a smartphone or computer.
- Find support or community.
- Compare devices before purchasing.

Primary journey:

`Home → Discovery Journey → Discovery Center / ENCight Academy / Resource Network`

## 2.3 Family member or caregiver

Common goals:

- Understand vision loss.
- Help without taking over.
- Improve lighting and safety.
- Find support and referrals.
- Communicate respectfully.
- Reduce isolation.

Primary journey:

`Home → I’m Supporting Someone → Caregiver Discovery Center → Related guides/classes`

## 2.4 Parent, teacher, or family with a child

Common goals:

- Understand healthy vision development.
- Respond to a failed screening.
- Support school success.
- Learn about screen use, eye safety, nutrition, and glasses.
- Find resources for a child who is blind or has low vision.

Primary journey:

`Home → Children & Families → Guides / Services / Academy`

## 2.5 Donor or supporter

Common goals:

- Understand impact.
- Trust stewardship.
- Make a gift.
- Become a member.
- Donate glasses.
- Recycle aluminum cans.
- Volunteer.
- Leave a legacy gift.

Primary journey:

`Home → Support → Giving path → Confirmation / continued relationship`

## 2.6 Professional

Common goals:

- Refer a person.
- Find educational resources.
- Lease an office or use a hot desk.
- Reserve meeting space.
- Join a collaborative effort.
- Locate an independent provider on campus.

Primary journey:

`Home → Professionals → Commons / Services on Campus / Referral`

---

# 3. SITE MAP AND ROUTES

## 3.1 Primary navigation

Use these top-level labels:

1. Home
2. Start Here
3. Discover
4. Learn
5. Services
6. Community
7. Professionals
8. Support
9. Visit
10. About

Utility links:

- Get Help
- Calendar
- Become a Friend
- Donate
- Search
- Member Login

For the initial static build, “Member Login” may link to an explanatory page describing future member features. Do not create a fake authentication system.

## 3.2 Route plan

```text
/
├── /start-here/
├── /who-we-help/
├── /discover/
│   ├── /discover/journeys/
│   ├── /discover/vision/
│   ├── /discover/healthy-living/
│   ├── /discover/independent-living/
│   ├── /discover/technology/
│   ├── /discover/children-families/
│   ├── /discover/caregivers/
│   ├── /discover/community/
│   ├── /discover/life-skills/
│   ├── /discover/guides/
│   ├── /discover/research/
│   └── /discover/stories/
├── /learn/
│   ├── /learn/encight-academy/
│   ├── /learn/courses/
│   ├── /learn/workshops/
│   ├── /learn/community-learning-kitchen/
│   └── /learn/experience-apartment/
├── /services/
│   ├── /services/community-eyewear-center/
│   ├── /services/emergency-glasses/
│   ├── /services/request-assistance/
│   ├── /services/community-resource-network/
│   └── /services/professional-referrals/
├── /community/
│   ├── /community/friends/
│   ├── /community/volunteer/
│   ├── /community/events/
│   ├── /community/dining-in-the-dark/
│   └── /community/stories/
├── /professionals/
│   ├── /professionals/commons/
│   ├── /professionals/hot-desks/
│   ├── /professionals/offices/
│   ├── /professionals/meeting-rooms/
│   ├── /professionals/services-on-campus/
│   ├── /professionals/directory/
│   └── /professionals/innovation-hub/
├── /support/
│   ├── /support/donate/
│   ├── /support/monthly-giving/
│   ├── /support/legacy-giving/
│   ├── /support/eyeglass-donations/
│   ├── /support/aluminum-recycling/
│   ├── /support/sponsorships/
│   └── /support/corporate-giving/
├── /visit/
│   ├── /visit/plan-your-visit/
│   ├── /visit/campus-map/
│   ├── /visit/accessibility/
│   ├── /visit/facility-rentals/
│   └── /contact/
├── /about/
│   ├── /about/our-story/
│   ├── /about/mission-vision-values/
│   ├── /about/history/
│   ├── /about/leadership/
│   ├── /about/board/
│   ├── /about/strategic-vision/
│   ├── /about/impact/
│   ├── /about/transparency/
│   ├── /about/careers/
│   └── /about/press/
├── /accessibility/
├── /privacy/
├── /terms/
├── /search/
├── /member/
└── /404.html
```

## 3.3 Build priority

### Launch group A

- Home
- Start Here
- Who We Help
- Community Eyewear Center
- Emergency Glasses
- Discovery Center
- ENCight Academy
- Community Resource Network
- Friends of The Blind Center
- Volunteer Center
- Ways to Give
- Legacy Giving
- Professional Commons
- Professional Services on Campus
- Visit
- Contact
- Accessibility
- About
- Transparency

### Launch group B

- Major Discovery Center landing pages
- Community Learning Kitchen
- ENCight Experience Apartment
- Facility Rentals
- Events
- Forms
- Stories

### Expansion group

- Full Discovery Guide library
- Research Spotlights
- Discovery Meals
- Member portal
- Discovery Passport
- Video library
- Podcast network
- AI assistant
- Community Innovation Hub and Community Solutions Lab in 2027

---

# 4. STATIC REPOSITORY BLUEPRINT

Use this recommended structure:

```text
the-blind-center/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── public/
│   ├── favicon.svg
│   ├── robots.txt
│   ├── images/
│   │   ├── home/
│   │   ├── discovery/
│   │   ├── services/
│   │   ├── community/
│   │   ├── professionals/
│   │   └── about/
│   ├── documents/
│   └── social/
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── accessibility/
│   │   ├── cards/
│   │   ├── forms/
│   │   ├── layout/
│   │   ├── navigation/
│   │   ├── search/
│   │   └── sections/
│   ├── content/
│   │   ├── config.ts
│   │   ├── guides/
│   │   ├── stories/
│   │   ├── research/
│   │   ├── courses/
│   │   ├── events/
│   │   ├── professionals/
│   │   └── resources/
│   ├── data/
│   │   ├── navigation.ts
│   │   ├── site.ts
│   │   ├── social.ts
│   │   └── forms.ts
│   ├── layouts/
│   │   ├── BaseLayout.astro
│   │   ├── PageLayout.astro
│   │   ├── GuideLayout.astro
│   │   ├── CourseLayout.astro
│   │   └── StoryLayout.astro
│   ├── pages/
│   ├── styles/
│   │   ├── reset.css
│   │   ├── tokens.css
│   │   ├── global.css
│   │   ├── components.css
│   │   └── print.css
│   └── utils/
├── astro.config.mjs
├── package.json
├── tsconfig.json
├── README.md
└── LICENSE
```

## 4.1 GitHub Pages path configuration

The build must support either:

- A custom domain at the repository root, or
- A project path such as `https://organization.github.io/repository-name/`

In Astro, set the `site` and `base` values through environment variables or repository configuration.

Example:

```js
import { defineConfig } from 'astro/config';

export default defineConfig({
  site: process.env.SITE_URL || 'https://example.org',
  base: process.env.BASE_PATH || '/',
  output: 'static',
  trailingSlash: 'always'
});
```

All internal links and assets must use Astro’s base-aware mechanisms. Do not hardcode root-relative paths that fail under a GitHub project subdirectory.

## 4.2 GitHub Actions deployment

Use an official Pages deployment workflow. Example:

```yaml
name: Deploy Astro to GitHub Pages

on:
  push:
    branches: [main]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: pages
  cancel-in-progress: true

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 22
          cache: npm
      - run: npm ci
      - run: npm run build
        env:
          SITE_URL: ${{ vars.SITE_URL }}
          BASE_PATH: ${{ vars.BASE_PATH }}
      - uses: actions/upload-pages-artifact@v3
        with:
          path: ./dist

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy
        id: deployment
        uses: actions/deploy-pages@v4
```

---

# 5. DESIGN SYSTEM

## 5.1 Visual concept

The design should feel:

- Calm
- Warm
- Institutional
- Contemporary
- Trustworthy
- Spacious
- Tactile
- Community-centered
- More like a discovery campus than a clinic

Avoid:

- Hospital blue as the dominant color
- Excessive gradients
- Very pale text
- Animated decoration
- Crowded dashboards
- Tiny cards
- Generic disability icons
- Eye close-ups as hero images
- Stock photos in which one person is passively “helped” by another

## 5.2 Color palette

Use CSS custom properties. Confirm final colors against actual logo assets when available.

```css
:root {
  --color-ink: #17221d;
  --color-text: #223029;
  --color-muted: #4b5d54;
  --color-background: #fbfcf8;
  --color-surface: #ffffff;
  --color-surface-soft: #f1f5ee;
  --color-border: #c8d2cb;

  --color-primary: #174c3c;
  --color-primary-hover: #0f382c;
  --color-primary-contrast: #ffffff;

  --color-accent: #b5482d;
  --color-accent-hover: #8f361f;
  --color-accent-contrast: #ffffff;

  --color-gold: #8a6418;
  --color-gold-soft: #f7edce;

  --color-info: #174c6b;
  --color-info-soft: #e6f2f7;

  --color-success: #24683f;
  --color-success-soft: #e7f3ea;

  --color-warning: #7b4b00;
  --color-warning-soft: #fff0c7;

  --color-error: #8d1c1c;
  --color-error-soft: #fdeaea;

  --focus-ring: #ffbf47;
}
```

Do not use color values without testing contrast. Text must meet WCAG AA contrast at the final rendered size and weight.

## 5.3 Typography

Preferred font stack:

```css
:root {
  --font-sans: "Atkinson Hyperlegible", "Inter", "Segoe UI", Arial, sans-serif;
  --font-serif: "Source Serif 4", Georgia, serif;
}
```

Do not distribute font files in the repository unless properly licensed. Prefer system-safe loading or approved web-hosted fonts. The site must remain usable if external fonts fail.

Typography scale:

```css
:root {
  --text-xs: 0.875rem;
  --text-sm: 1rem;
  --text-base: clamp(1.125rem, 1.05rem + 0.2vw, 1.25rem);
  --text-lg: clamp(1.25rem, 1.1rem + 0.5vw, 1.5rem);
  --text-xl: clamp(1.5rem, 1.2rem + 1vw, 2rem);
  --text-2xl: clamp(2rem, 1.5rem + 2vw, 3rem);
  --text-3xl: clamp(2.5rem, 1.7rem + 3vw, 4.5rem);
}
```

Body text:

- Minimum 18 px on mobile
- Preferred 19–20 px on desktop
- Line height 1.65–1.8
- Maximum reading width 68 characters
- Left aligned
- Never fully justified

## 5.4 Spacing

```css
:root {
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.5rem;
  --space-6: 2rem;
  --space-7: 3rem;
  --space-8: 4rem;
  --space-9: 6rem;

  --radius-sm: 0.35rem;
  --radius-md: 0.75rem;
  --radius-lg: 1.25rem;

  --shadow-sm: 0 1px 2px rgb(0 0 0 / 0.08);
  --shadow-md: 0 8px 24px rgb(0 0 0 / 0.10);
}
```

## 5.5 Complete baseline CSS

```css
/* reset.css */
*,
*::before,
*::after {
  box-sizing: border-box;
}

html {
  color-scheme: light;
  scroll-behavior: smooth;
}

@media (prefers-reduced-motion: reduce) {
  html {
    scroll-behavior: auto;
  }

  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

body {
  margin: 0;
}

img,
picture,
svg,
video {
  display: block;
  max-width: 100%;
}

button,
input,
select,
textarea {
  font: inherit;
}

button,
a {
  touch-action: manipulation;
}

/* global.css */
body {
  min-height: 100vh;
  background: var(--color-background);
  color: var(--color-text);
  font-family: var(--font-sans);
  font-size: var(--text-base);
  line-height: 1.7;
  text-rendering: optimizeLegibility;
}

a {
  color: var(--color-primary);
  text-decoration-thickness: 0.12em;
  text-underline-offset: 0.18em;
}

a:hover {
  color: var(--color-primary-hover);
}

a:focus-visible,
button:focus-visible,
input:focus-visible,
select:focus-visible,
textarea:focus-visible,
summary:focus-visible,
[tabindex]:focus-visible {
  outline: 4px solid var(--focus-ring);
  outline-offset: 4px;
}

h1,
h2,
h3,
h4 {
  color: var(--color-ink);
  font-family: var(--font-serif);
  line-height: 1.12;
  text-wrap: balance;
}

h1 {
  font-size: var(--text-3xl);
}

h2 {
  font-size: var(--text-2xl);
}

h3 {
  font-size: var(--text-xl);
}

p,
li {
  max-width: 68ch;
}

main:focus {
  outline: none;
}

.container {
  width: min(100% - 2rem, 76rem);
  margin-inline: auto;
}

.content-narrow {
  width: min(100%, 68ch);
}

.section {
  padding-block: var(--space-8);
}

.section--soft {
  background: var(--color-surface-soft);
}

.stack > * + * {
  margin-block-start: var(--space-5);
}

.cluster {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-4);
  align-items: center;
}

.grid {
  display: grid;
  gap: var(--space-5);
}

.grid--cards {
  grid-template-columns: repeat(auto-fit, minmax(min(100%, 18rem), 1fr));
}

.skip-link {
  position: absolute;
  z-index: 9999;
  top: 0;
  left: 0;
  padding: 0.8rem 1rem;
  background: var(--color-ink);
  color: #fff;
  transform: translateY(-150%);
}

.skip-link:focus {
  transform: translateY(0);
}

.button {
  display: inline-flex;
  min-height: 3rem;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 1.1rem;
  border: 2px solid transparent;
  border-radius: var(--radius-md);
  background: var(--color-primary);
  color: var(--color-primary-contrast);
  font-weight: 700;
  line-height: 1.2;
  text-align: center;
  text-decoration: none;
}

.button:hover {
  background: var(--color-primary-hover);
  color: var(--color-primary-contrast);
}

.button--accent {
  background: var(--color-accent);
}

.button--accent:hover {
  background: var(--color-accent-hover);
}

.button--secondary {
  border-color: var(--color-primary);
  background: transparent;
  color: var(--color-primary);
}

.button--secondary:hover {
  background: var(--color-primary);
  color: #fff;
}

.card {
  height: 100%;
  padding: var(--space-6);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  background: var(--color-surface);
  box-shadow: var(--shadow-sm);
}

.card:focus-within,
.card:hover {
  box-shadow: var(--shadow-md);
}

.card__link::after {
  position: absolute;
  inset: 0;
  content: "";
}

.alert {
  padding: var(--space-6);
  border-inline-start: 0.5rem solid var(--color-accent);
  border-radius: var(--radius-md);
  background: var(--color-warning-soft);
}

.prose blockquote {
  margin-inline: 0;
  padding-inline-start: var(--space-5);
  border-inline-start: 0.35rem solid var(--color-gold);
  font-family: var(--font-serif);
  font-size: var(--text-lg);
}

form {
  display: grid;
  gap: var(--space-5);
}

label,
legend {
  font-weight: 700;
}

input,
select,
textarea {
  width: 100%;
  min-height: 3rem;
  padding: 0.75rem;
  border: 2px solid var(--color-muted);
  border-radius: var(--radius-sm);
  background: #fff;
  color: var(--color-text);
}

textarea {
  min-height: 10rem;
  resize: vertical;
}

fieldset {
  padding: var(--space-5);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-md);
}

.help-text {
  color: var(--color-muted);
  font-size: var(--text-sm);
}

.error-message {
  color: var(--color-error);
  font-weight: 700;
}

.site-header {
  position: sticky;
  z-index: 100;
  top: 0;
  border-bottom: 1px solid var(--color-border);
  background: rgb(255 255 255 / 0.97);
}

.utility-nav {
  background: var(--color-ink);
  color: #fff;
}

.utility-nav a {
  color: #fff;
}

.hero {
  display: grid;
  min-height: min(44rem, 82vh);
  align-items: center;
  padding-block: var(--space-9);
  background:
    linear-gradient(90deg, rgb(23 34 29 / 0.88), rgb(23 34 29 / 0.42)),
    var(--hero-image, none) center / cover no-repeat;
  color: #fff;
}

.hero h1,
.hero p {
  color: #fff;
}

.breadcrumbs ol {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  padding: 0;
  list-style: none;
}

.breadcrumbs li:not(:last-child)::after {
  margin-inline-start: 0.5rem;
  content: "/";
}

.site-footer {
  padding-block: var(--space-8);
  background: var(--color-ink);
  color: #fff;
}

.site-footer a,
.site-footer h2,
.site-footer h3 {
  color: #fff;
}

@media (max-width: 48rem) {
  .section {
    padding-block: var(--space-7);
  }

  .desktop-only {
    display: none !important;
  }
}

/* print.css */
@media print {
  .site-header,
  .site-footer,
  .breadcrumbs,
  .no-print,
  .button,
  form {
    display: none !important;
  }

  body {
    background: #fff;
    color: #000;
    font-size: 12pt;
  }

  a {
    color: #000;
    text-decoration: underline;
  }

  main {
    width: 100%;
  }
}
```

## 5.6 Accessibility preferences

Do not override the user’s browser zoom. A site-based text size control may be offered as a convenience but must not replace correct scalable typography.

Optional preferences panel:

- Increase text size
- Increase spacing
- High contrast
- Reduce motion

Store preferences in local storage only after the user changes them. Do not create a mandatory accessibility widget that covers content.

---

# 6. GLOBAL COMPONENT BLUEPRINT

## 6.1 Header

Desktop:

```text
[Utility bar]
Get Help | Calendar | Become a Friend | Donate | Search | Member Login

[Primary bar]
Logo | Start Here | Discover | Learn | Services | Community |
Professionals | Support | Visit | About
```

Mobile:

- Logo
- Large “Get Help” button
- Clearly labeled Menu button
- Full-screen or large-sheet navigation
- Search
- Donate
- Close button
- No nested fly-out menus requiring precision pointer control

## 6.2 Hero

Required fields:

- Eyebrow, optional
- H1
- Supporting paragraph
- Primary CTA
- Secondary CTA
- Optional third CTA
- Background image with dark overlay or side-by-side image
- Never place small text directly over a complex photograph

## 6.3 Help cards

Each card:

- Clear title in first person
- One-sentence explanation
- Descriptive link
- Optional simple icon
- Entire card may be clickable only if keyboard and screen-reader behavior remains correct

Examples:

- I Need Glasses
- My Vision Has Changed
- I Want to Live Independently
- I Need Technology Help
- I’m Supporting Someone
- I Want to Learn
- I Want to Volunteer
- I Want to Give

## 6.4 Emergency callout

Must be prominent on the homepage and Eyewear Center page.

Use a high-contrast visual treatment but do not imply medical emergency treatment. Clarify that inventory cannot guarantee a prescription match.

## 6.5 Discovery cards

Fields:

- Title
- One-paragraph description
- Related audience tags
- Related guide count, optional
- CTA
- Image or illustration

## 6.6 Event cards

Fields:

- Date
- Time
- Title
- Location
- Short description
- Registration link
- Accessibility details
- Status: open, full, canceled, or completed

## 6.7 Story cards

Fields:

- Headline
- Excerpt
- Image
- Story type
- Privacy note where appropriate
- Link

## 6.8 Reusable CTA band

Examples:

- Need help deciding where to begin?
- Become a Friend of The Blind Center.
- Schedule a visit.
- Support the next discovery.
- Continue your journey.

## 6.9 Footer

Include:

- Public name and legal name
- Address
- Phone placeholder
- Email placeholder
- Hours placeholder
- Mission summary
- Primary destinations
- Donate
- Volunteer
- Friends membership
- Accessibility
- Privacy
- Terms
- Transparency
- Annual reports
- Newsletter
- Social links
- Copyright

---

# 7. HOMEPAGE WIREFRAME AND FINAL COPY

## 7.1 Section order

1. Header
2. Hero
3. How Can We Help Today?
4. Emergency glasses
5. Welcome to The Blind Center
6. Discovery destinations
7. Stories of Discovery
8. ENCight Academy
9. Upcoming events
10. Friends of The Blind Center
11. Ways to Give
12. Professional Commons
13. Visit
14. Newsletter
15. Footer

## 7.2 Hero copy

### Healthy Vision. Independent Living. Connected Community.

Helping people protect, preserve, maximize, and adapt their vision while building lives of confidence, independence, and purpose.

Whether you are experiencing vision changes, caring for someone you love, looking for affordable eyeglasses, searching for trusted information, or wanting to support your community, welcome to The Blind Center.

You are in the right place.

Primary buttons:

- Start Here
- Need Glasses?
- Explore the Discovery Center

## 7.3 How Can We Help Today?

Choose the path that best matches what you need right now.

### I Need Glasses

Learn about free and subsidized eyeglasses, emergency replacement glasses, and donated eyewear available through The Blind Center and community partners.

CTA: **Get Help with Glasses**

### My Vision Has Changed

Find plain-language information, practical next steps, and support for understanding vision loss, low vision, and common eye conditions.

CTA: **Start My Journey**

### I Want to Live More Independently

Discover tools, techniques, classes, and resources for cooking, reading, organizing your home, managing medications, using technology, and staying connected.

CTA: **Explore Independent Living**

### I Need Technology Help

Learn about smartphones, screen readers, magnifiers, artificial intelligence, smart-home tools, and adaptive devices that can make everyday life easier.

CTA: **Visit the Technology Discovery Lab**

### I’m Supporting Someone

Find guidance for family members, caregivers, friends, and professionals who want to help while encouraging independence.

CTA: **Caregiver Resources**

### I Want to Learn

Explore ENCight Academy, Discovery Guides, workshops, healthy-living classes, and educational resources for every stage of life.

CTA: **Start Learning**

### I Want to Volunteer

Share your time, talents, and experience through the Welcome Center, Community Eyewear Center, events, classes, recycling, and community programs.

CTA: **Volunteer with Us**

### I Want to Support the Mission

Donate, become a Friend of The Blind Center, give eyeglasses, recycle aluminum cans, sponsor a program, or leave a legacy gift.

CTA: **Ways to Give**

## 7.4 Welcome section

### Welcome to The Blind Center

The Blind Center is more than a nonprofit office.

It is a community center, learning campus, discovery space, and connection point for people who are blind, have low vision, are experiencing changes in vision, or want to protect their eye health.

Our work brings together education, practical training, assistive technology, healthy living, community resources, professional partnerships, and compassionate support.

Every person’s journey is different.

Some visitors need eyeglasses today.

Some are learning how to use a phone after vision loss.

Some are caring for a parent.

Some want to understand diabetes and eye health.

Some are looking for friendship, classes, volunteer opportunities, or a place to belong.

Wherever you are starting, we are here to help you take the next step.

## 7.5 Discovery destinations

### Discover The Blind Center

#### Community Eyewear Center

Free and subsidized eyeglasses, emergency replacement glasses, donated eyewear, readers, sunglasses, and Lions Club partnerships.

CTA: **Visit the Eyewear Center**

#### Vision Discovery Center

Plain-language education about vision, eye health, common eye conditions, prevention, healthy aging, and practical next steps.

CTA: **Explore Vision Guides**

#### Technology Discovery Lab

Hands-on learning for smartphones, screen readers, magnifiers, artificial intelligence, smart-home tools, and adaptive technology.

CTA: **Explore Technology**

#### Community Learning Kitchen

Healthy cooking, adaptive kitchen skills, diabetes prevention, nutrition education, and meals that support healthy living.

CTA: **Learn in the Kitchen**

#### ENCight Experience Apartment

A hands-on model home where visitors can discover tools, lighting, organization, technology, and techniques that support independence at home.

CTA: **Tour the Apartment**

#### ENCight Academy

Classes, workshops, Discovery Guides, learning pathways, and educational programs designed to build confidence for life.

CTA: **Visit ENCight Academy**

## 7.6 Emergency glasses

### Need Help Today?

#### Free Walk-In Emergency Replacement Glasses

Sometimes you simply cannot wait.

If your glasses are broken, lost, or no longer usable, The Blind Center may be able to help you find a temporary replacement pair from our donated eyewear inventory.

We maintain community-donated eyeglasses, readers, and sunglasses that are cleaned, repaired when possible, organized, and redistributed through The Blind Center and Lions Club partnerships.

While we cannot guarantee an exact prescription match, many visitors are able to find a temporary pair that helps them continue reading, working, attending school, or carrying out daily activities while permanent replacement glasses are arranged.

CTA: **I Need Emergency Glasses**

#### Donate Your Used Eyeglasses

One pair of glasses can change someone’s life.

We accept used prescription eyeglasses, reading glasses, sunglasses, children’s glasses, and selected eyewear accessories. Donated glasses are cleaned, sorted, repaired when possible, and redistributed to people who need them.

CTA: **Donate Eyeglasses**

## 7.7 Stories

### Stories of Discovery

#### Finding the Way Home

When “Lucinda” first came to The Blind Center, she was legally blind, homeless, and without the documents needed to apply for housing or services after a robbery.

Over time, with support from a local social worker and The Blind Center team, Lucinda rebuilt her foundation. Birth certificates and identification were secured. Benefits and assistance were accessed. Job training opened new possibilities. Eventually, Lucinda moved into private housing and returned to independent living.

Her story reminds us that rebuilding a life rarely happens through one dramatic moment. It happens through small victories, steady support, and a community that refuses to give up.

Privacy label: **Name changed for privacy.**

CTA: **Read Stories of Discovery**

#### One Gift Changed Everything

“Tom” wanted to keep managing his own mail and bills, but declining vision made due dates and payment amounts difficult to read. Late fees began to add up.

Then the family of a community member donated a CCTV magnification machine. That gift allowed The Blind Center to help Tom read his mail, review bills, and continue managing his own affairs.

One family’s donation became another person’s independence.

CTA: **Share Your Story**

## 7.8 ENCight Academy

### Learn With Us

ENCight Academy is the educational home of The Blind Center.

Through classes, workshops, Discovery Guides, demonstrations, and future online learning, participants build practical skills for daily life.

Learn about:

- Vision and eye health
- Independent living
- Assistive technology
- Healthy cooking
- Diabetes and vision
- Home safety
- Caregiver support
- Community resources

CTA: **Start Learning**

## 7.9 Events

### Upcoming Experiences

There is always something happening at The Blind Center.

Join us for:

- Technology workshops
- Healthy cooking classes
- Support groups
- Volunteer opportunities
- Community events
- Discovery tours
- Professional programs
- Dining in the Dark
- Friends of The Blind Center gatherings

CTA: **View Community Calendar**

## 7.10 Friends membership

### Become a Friend of The Blind Center

#### Together, We See a Brighter Future

Friends of The Blind Center is a community of people who believe that vision care, lifelong learning, accessibility, and compassion make our entire community stronger.

Membership is open to everyone.

Free membership provides access to community updates and learning opportunities. Supporting memberships help sustain programs, expand the Discovery Center, provide emergency glasses, and build educational resources for the future.

Friends receive early access to Dining in the Dark fundraiser tickets before they are released to the public.

CTA: **Become a Friend**

## 7.11 Ways to Give

### Ways to Give

There are many ways to support The Blind Center.

- Give today
- Become a monthly donor
- Donate eyeglasses
- Recycle aluminum cans
- Volunteer
- Sponsor a program
- Become a corporate partner
- Leave a legacy gift

CTA: **Explore Ways to Give**

## 7.12 Professional Commons

### Work Where Community Happens

The Professional Commons provides office suites, hot-desk opportunities, meeting rooms, and recurring office time for independent professionals and organizations whose work strengthens the community.

Professionals located on campus operate independently while sharing a welcoming, accessible environment connected to education, community resources, and collaboration.

CTA: **Explore the Professional Commons**

## 7.13 Visit

### Visit The Blind Center

We look forward to welcoming you.

**The Blind Center**  
221 North Harvey Street  
Washington, North Carolina 27889

Visit us to learn about services, donate eyeglasses, attend a class, explore technology, volunteer, or discover the many resources available through the Community Center.

Buttons:

- Plan Your Visit
- Contact Us

## 7.14 Newsletter

### Never Miss a Discovery

Receive updates about classes, events, Discovery Guides, volunteer opportunities, stories, and ways to support The Blind Center.

CTA: **Subscribe**

---

# 8. START HERE PAGE

## Hero

### Everyone’s journey is different. You do not have to navigate yours alone.

Whether you have lived with vision loss your entire life, have noticed gradual changes over the years, recently received an eye diagnosis, or simply want to protect your eyesight, welcome to The Blind Center.

Vision changes for many reasons. Some people are born with visual impairments, while others experience changes because of aging, injury, eye disease, diabetes, genetics, or other health conditions.

No matter where you are on your journey, our mission is the same: to provide education, practical skills, resources, technology, and community that help people live healthy, confident, and independent lives.

You do not need to have all the answers today. We will help you take the next step.

## First, take a breath

It is normal to feel uncertain, frustrated, angry, anxious, or overwhelmed after vision changes or a diagnosis.

Vision loss changes how some tasks are completed, but it does not determine your value, your independence, or your future.

People who are blind or have low vision continue to work, travel, cook, volunteer, raise families, enjoy hobbies, learn technology, and participate fully in community life.

## Choose a path

### I was recently diagnosed

Understand your diagnosis, prepare questions for your eye-care provider, and discover practical next steps.

CTA: **Understand Vision Changes**

### My vision has gradually changed

Explore lighting, magnification, adaptive techniques, technology, and training.

CTA: **Explore Independent Living**

### I need help paying for glasses

Learn about free and subsidized eyeglasses and emergency replacement options.

CTA: **Get Help with Glasses**

### I am supporting someone

Find caregiver guidance designed to encourage independence without taking over.

CTA: **Caregiver Discovery Center**

### I need help with technology

Explore smartphones, screen readers, magnification, artificial intelligence, and adaptive devices.

CTA: **Technology Discovery Lab**

### I want to protect my eyesight

Learn about eye examinations, nutrition, movement, diabetes, blood pressure, eye safety, and healthy aging.

CTA: **Healthy Vision Resources**

### I need another kind of resource

Use the Community Resource Network to find transportation, housing, benefits, healthcare, mental-health resources, employment assistance, and more.

CTA: **Community Resource Network**

## Not sure where to begin?

You do not need to know which program or agency you need.

Tell us what is happening. We will help you identify a useful next step.

CTA: **Request Assistance**

---

# 9. WHO WE HELP PAGE

## Every person’s journey is different. Every person deserves support.

The Blind Center serves people throughout every stage of life.

### Children and families

Healthy-vision habits, school success, nutrition, eye safety, screenings, low-vision resources, and family education.

### Teens and young adults

Technology, independence, college, careers, leadership, healthy living, and community participation.

### Adults

Independent living, assistive technology, employment resources, transportation, financial organization, healthy vision, and community.

### Older adults

Healthy aging, fall prevention, common eye conditions, medication organization, technology, transportation, and remaining at home.

### People who are blind or have low vision

Education, technology, adaptive techniques, resource navigation, community, and lifelong learning.

### People who recently experienced vision changes

Plain-language information, practical next steps, support, and opportunities to build new skills.

### Family members and caregivers

Guidance for supporting independence, improving safety, communicating respectfully, and finding resources.

### Healthcare and community professionals

Referral resources, educational materials, campus partnerships, meeting space, and professional collaboration.

### Volunteers and supporters

Meaningful ways to contribute time, skills, financial support, eyeglasses, recyclable aluminum, and community connections.

CTA: **Start Here**

---

# 10. DISCOVERY CENTER

## Landing-page hero

### Every discovery begins with curiosity.

Explore practical guides, inspiring stories, research summaries, classes, and community resources designed to help people live healthier and more independent lives.

Search prompt:

**What would you like to discover today?**

Suggested topics:

- Healthy vision
- Glaucoma
- Macular degeneration
- Cooking
- Technology
- Transportation
- Caregiving
- Children
- Artificial intelligence
- Reading mail
- Staying at home

## Discovery promise

The Discovery Center was created for people, not diagnoses.

Information should be:

- Evidence-aware
- Easy to understand
- Practical
- Accessible
- Hopeful
- Respectful
- Free to everyone

Learning should build confidence, not fear.

## Discovery method

- Discover
- Understand
- Experience
- Practice
- Thrive
- Share

## Discovery journeys

### I’m new to vision changes

Understand what is happening, what to expect, and what can help.

### I want to protect my eyesight

Explore eye examinations, healthy living, diabetes prevention, heart health, nutrition, safety, and healthy aging.

### I want to live more independently

Explore home organization, cooking, reading, medications, shopping, transportation, technology, and emergency planning.

### I want to learn about technology

Explore smartphones, computers, screen readers, magnification, artificial intelligence, OCR, smart-home tools, and wearables.

### I’m supporting someone I love

Explore caregiver communication, home safety, emotional adjustment, resources, and ways to encourage independence.

### I want to help a child

Explore development, school success, eye safety, nutrition, screen use, glasses, and family resources.

### I want healthier living

Explore nutrition, movement, sleep, stress, diabetes, blood pressure, and sustainable everyday habits.

### I want to find community

Explore events, support groups, volunteer opportunities, classes, membership, and stories.

## Major Discovery destinations

- Vision Discovery Center
- Healthy Living Discovery Center
- Independent Living Discovery Center
- Technology Discovery Lab
- Children & Families Discovery Center
- Caregiver Discovery Center
- Community Discovery Center
- Life Skills Discovery Center

---

# 11. DISCOVERY GUIDE CONTENT MODEL

Create a static content collection named `guides`.

Required frontmatter:

```yaml
title: "Understanding Glaucoma"
subtitle: "Protecting Vision from the Silent Thief of Sight"
slug: "understanding-glaucoma"
description: "Plain-language guidance about glaucoma, risk, diagnosis, treatment, and living well."
publishedDate: 2026-07-01
reviewDate: 2027-07-01
readingMinutes: 20
difficulty: "Beginner"
audiences:
  - adults
  - caregivers
  - professionals
topics:
  - glaucoma
  - eye-conditions
journeys:
  - new-to-vision-changes
  - protect-my-eyesight
featured: true
medicalReviewRequired: true
sources:
  - title: "Source title"
    organization: "Source organization"
    url: "https://..."
```

Guide body structure:

1. Why This Matters
2. What You Will Learn
3. Understanding the Topic
4. Real Life
5. Practical Solutions
6. Research Spotlight
7. Meet Someone Like You — clearly label as a fictional composite when not a real person
8. Experience It at The Blind Center
9. Questions to Ask a Professional
10. Myths and Facts
11. Take Action Today
12. One Thing to Remember
13. Explore More
14. Continue Discovering
15. Sources and review date

Initial guide inventory:

- How Your Eyes Work
- How We See
- Understanding Vision
- Protecting Healthy Vision
- Vision Throughout Life
- Understanding Cataracts
- Understanding Glaucoma
- Understanding Age-Related Macular Degeneration
- Understanding Diabetic Eye Disease
- Understanding Dry Eye Disease
- Nutrition for Healthy Eyes
- Prediabetes and Your Vision
- Diabetes and Healthy Vision
- Heart Health and Healthy Vision
- Organizing Your Home
- Reading Your Mail
- Managing Medications
- Adaptive Lighting
- Kitchen Safety
- Laundry with Confidence
- Choosing a Smartphone
- Screen Readers
- Magnification
- Artificial Intelligence for Everyday Life
- Helping Without Taking Over
- Making a Home Safer
- Children’s Vision Milestones
- School Success and Vision
- Technology for Children and Families

---

# 12. ENCIGHT ACADEMY PAGE

## Learning that builds confidence for life

### Discover. Learn. Practice. Thrive.

ENCight Academy is the educational division of The Blind Center. It brings together classes, workshops, demonstrations, future certificate programs, online learning, community lectures, and hands-on experiences into one lifelong-learning community.

Whether you are learning to use a smartphone, preparing healthier meals, understanding an eye condition, supporting a family member, or exploring a new interest, ENCight Academy provides practical education designed to improve everyday life.

Learning does not end with graduation. It continues throughout our lives.

## Educational philosophy

People learn best by doing.

Every course should combine practical instruction with opportunities to practice, ask questions, and build confidence.

The Academy does not simply teach information. It teaches skills, problem-solving, and independence.

## Learning model

### Discover

Understand why the subject matters.

### Learn

Build knowledge and explore practical options.

### Experience

Try real equipment, techniques, or healthy habits.

### Apply

Use the skill in everyday life.

### Share

Help another person learn.

## Areas of learning

- Vision and eye health
- Healthy living
- Independent living
- Technology
- Family and caregiving
- Community leadership
- Professional education

## Static launch approach

Public visitors may read course descriptions and selected introductory lessons.

Free Friends membership may later provide:

- Full course access
- Progress tracking
- Certificates
- Downloadable worksheets
- Saved content
- Discovery Passport

For the static launch, do not create fake progress tracking. Create clear informational pages and link registration to the configured membership/newsletter platform.

CTA buttons:

- Browse Courses
- View Workshops
- Become a Free Friend
- Attend an In-Person Class

---

# 13. COMMUNITY EYEWEAR CENTER

## Everyone deserves clear vision

The Community Eyewear Center helps connect individuals with free or subsidized eyeglasses, emergency replacement eyewear, donated readers and sunglasses, and community vision resources.

The Center also receives donated eyeglasses that are cleaned, inspected, organized, repaired when appropriate, and redistributed through The Blind Center and Lions Club partnerships.

## Emergency replacement glasses

If someone’s glasses are broken, lost, or no longer usable, The Blind Center may be able to help locate a temporary pair from the donated inventory.

Important language:

- Inventory varies.
- An exact prescription match cannot be guaranteed.
- Emergency glasses are temporary and do not replace a current eye examination or professionally prescribed eyewear.
- Confirm current walk-in hours before publishing them.
- Encourage visitors with sudden vision loss, severe eye pain, flashes, a sudden increase in floaters, or a curtain-like shadow to seek urgent professional eye care.

## Eyeglass donations

Accept, subject to current policy:

- Prescription eyeglasses
- Reading glasses
- Sunglasses
- Children’s glasses
- Cases and selected accessories
- Safety glasses in suitable condition

CTA buttons:

- Request Eyeglass Help
- Emergency Glasses
- Donate Eyeglasses
- Ask a Question

---

# 14. COMMUNITY RESOURCE NETWORK

## Helping you find the right resource at the right time

Life does not organize itself by agencies. It organizes itself by challenges.

A visitor may need transportation, housing, food assistance, benefits information, mental-health support, disability resources, healthcare, employment, or adaptive technology without knowing which organization provides it.

The Community Resource Network uses a “No Wrong Door” approach.

If The Blind Center provides the service, help the person begin.

If another organization is better equipped, help connect the person.

If the person does not know what is needed, help identify the next step.

## Resource pathways

- I need transportation.
- I need help paying for eyeglasses.
- I need food assistance.
- I need help at home.
- I need healthcare.
- I need disability resources.
- I need benefits information.
- I need housing.
- I need employment support.
- I need mental-health support.
- I am a veteran.
- I am supporting someone else.
- I do not know where to begin.

For launch, store resources in a maintainable JSON or Markdown collection with:

- Organization name
- Service area
- Counties
- Eligibility summary
- Contact information
- Website
- Accessibility notes
- Last verified date
- Resource categories
- Disclaimer

Do not imply endorsement. Add a notice that listings are informational, details may change, and visitors should confirm current eligibility and availability directly.

---

# 15. EXPERIENCE PAGES

## 15.1 ENCight Experience Apartment

### Discover a home designed for independence

The ENCight Experience Apartment is a hands-on learning environment where visitors can explore practical solutions that make everyday life safer, easier, and more enjoyable for people who are blind, have low vision, or want to age in place successfully.

Rather than displaying products on shelves, the apartment demonstrates how organization, technology, lighting, contrast, and adaptive techniques work together in a realistic home.

Rooms and topics:

- Kitchen
- Living room
- Bedroom
- Bathroom
- Medication management
- Laundry
- Home office
- Smart-home controls
- Emergency planning
- Lighting and contrast
- Fall prevention

CTA:

- Schedule a Tour
- Explore Independent Living Guides
- View Related Classes

## 15.2 Community Learning Kitchen

### Where healthy living becomes a hands-on experience

The Community Learning Kitchen brings together nutrition, cooking, vision health, diabetes prevention, independent living, and community.

Classes should focus on practical skills people can use at home:

- Healthy cooking
- Cooking with low vision
- Adaptive measuring
- Safe knife skills
- Reading labels
- Diabetes-friendly meals
- Budget-friendly meals
- Cooking for one or two
- Meal planning
- Discovery Meals

Core principle:

**No shame, no fad diets, and no impossible expectations. Make the next meal a little better than the last one.**

CTA:

- View Kitchen Classes
- Explore Discovery Meals
- Reserve a Group Program

## 15.3 Technology Discovery Lab

### Discover technology that makes everyday life easier

Topics:

- Smartphones
- VoiceOver and TalkBack
- Screen magnification
- Screen readers
- OCR and reading mail
- Artificial intelligence
- Smart speakers
- Smart-home controls
- Electronic video magnifiers
- Portable magnifiers
- Wearables
- Online safety

Core principle:

**Experience before investment.**

CTA:

- Request a Demonstration
- View Technology Guides
- Attend a Class

---

# 16. COMMUNITY AND MEMBERSHIP

## 16.1 Friends of The Blind Center

### Together, we see a brighter future

Friends of The Blind Center is a community of people who believe that vision care, lifelong learning, accessibility, and compassion make the entire community stronger.

Membership is open to everyone.

### Free Friend

Cost: $0

Collect:

- Name
- Email
- ZIP code
- Areas of interest, optional
- Communication preferences

Benefits:

- Discovery newsletter
- New class announcements
- Selected Academy resources
- Event information
- Future member features

### Supporting Friend

Suggested annual amount: $50, subject to approval.

Benefits may include:

- Early Dining in the Dark ticket access
- Member appreciation events
- Annual impact updates
- Optional recognition

### Family Friend

Suggested annual amount: $100, subject to approval.

Benefits may include:

- Household participation
- Family learning activities
- Early ticket access

### Community Builder

Suggested annual amount: $250 or more, subject to approval.

Benefits may include:

- Preview invitations
- Behind-the-scenes updates
- Selected Academy benefits

Do not promise benefits that have not been operationally approved.

CTA:

- Become a Free Friend
- Choose a Supporting Membership
- Learn About Dining in the Dark

## 16.2 Volunteer Center

### Change a life. Strengthen a community. Discover your purpose.

Volunteer opportunities may include:

- Welcome Center Ambassador
- Community Eyewear Center
- Discovery Center Guide
- Technology Mentor
- Community Learning Kitchen
- Event support
- Administrative assistance
- Photography and communications
- Fundraising
- Aluminum recycling
- Student service
- Corporate service
- Board or committee interest

Clearly state that some roles may require screening, orientation, training, or a background check.

CTA:

- Apply to Volunteer
- Explore Volunteer Roles
- Ask About Group Service

---

# 17. PROFESSIONALS

## 17.1 Professional Commons

### Work where community happens

The Professional Commons provides office suites, hot-desk opportunities, meeting rooms, one-time meeting space, and regular recurring office time for independent professionals and organizations.

Features may include:

- Private offices
- Hot desks
- Recurring office hours
- Meeting rooms
- Community setting
- Accessible location
- Shared professional connections
- Educational opportunities
- Referral relationships where appropriate

Do not publish pricing until approved.

CTA:

- Request Availability
- Reserve Meeting Space
- Ask About Recurring Office Time

## 17.2 Professional Services on Campus

### A community of professionals working alongside one another

The Blind Center Community Center is home to independent professionals and organizations whose work complements the mission of independence, accessibility, communication, advocacy, and well-being.

Required disclaimer:

> Professionals and organizations located on campus operate as independent service providers. They establish their own appointments, fees, policies, licensing, professional practices, and client relationships. The Blind Center provides office space but does not supervise, manage, direct, employ, or assume responsibility for their professional services.

Current categories may include:

- Independent disability evaluation and assessment
- Mental-health counseling
- Communication support
- Advocacy and self-determination
- Therapeutic services
- Social-work resource navigation

A social worker is available on campus two times per week, subject to the current provider’s schedule and eligibility rules.

Each provider entry should include:

- Practice name
- Provider name, when approved
- Service summary
- Independent-provider badge
- Contact information
- Scheduling instructions
- Accessibility details
- Link to provider site
- Last verified date

## 17.3 Community Innovation Hub

Label clearly:

**Planned for 2027**

Possible features:

- Roundtables
- Innovation showcases
- University partnerships
- Grant collaboratives
- Professional education
- Community problem-solving
- Community Solutions Lab

Do not present this as currently operating.

---

# 18. SUPPORT AND GIVING

## 18.1 Ways to Give

### Every gift helps someone discover greater independence

Generosity takes many forms.

A donated pair of glasses may help someone return to work.

A volunteer may help a senior learn to use a smartphone.

Aluminum cans may help support a community class.

A monthly gift may help provide emergency replacement glasses.

Giving paths:

- One-time gift
- Monthly giving
- Friends membership
- Eyeglass donation
- Aluminum-can recycling
- Memorial and tribute gifts
- Program sponsorship
- Corporate giving
- Volunteering
- Legacy giving

## 18.2 Legacy Giving

### Create opportunities that last for generations

A legacy gift allows a person’s values to continue strengthening lives.

Possible giving methods:

- Bequest in a will or trust
- Retirement-account beneficiary designation
- Life-insurance beneficiary designation
- Investment or transfer-on-death account
- Appreciated assets
- Real estate, subject to Gift Acceptance Policy
- Memorial gifts
- Named funds or endowment gifts, when approved

Required disclaimer:

> The Blind Center does not provide legal, tax, or financial advice. Donors should consult qualified professional advisors regarding their individual circumstances. Proposed noncash and restricted gifts are subject to the organization’s Gift Acceptance Policy and formal approval.

### Legacy Society

People who notify The Blind Center that they have included the organization in their estate plans may be invited to join the Legacy Society, with recognition only if desired.

CTA:

- Request a Confidential Conversation
- Download Legacy Information
- Contact Your Professional Advisor

---

# 19. FORMS FOR A STATIC GITHUB PAGES SITE

GitHub Pages does not process forms. Use a configurable external endpoint.

Approved options may include:

- Formspree
- Basin
- Getform
- Netlify Forms only if hosting changes
- Google Forms for low-risk simple forms
- A CRM or donor platform’s embedded form
- A secure third-party donation processor
- A secure event-registration platform

Do not store sensitive personal, health, benefits, or disability documentation in the GitHub repository.

## 19.1 Form configuration

Create `src/data/forms.ts`:

```ts
export const formEndpoints = {
  contact: import.meta.env.PUBLIC_CONTACT_FORM_ENDPOINT,
  assistance: import.meta.env.PUBLIC_ASSISTANCE_FORM_ENDPOINT,
  volunteer: import.meta.env.PUBLIC_VOLUNTEER_FORM_ENDPOINT,
  membership: import.meta.env.PUBLIC_MEMBERSHIP_FORM_ENDPOINT,
  rental: import.meta.env.PUBLIC_RENTAL_FORM_ENDPOINT,
  legacy: import.meta.env.PUBLIC_LEGACY_FORM_ENDPOINT,
  story: import.meta.env.PUBLIC_STORY_FORM_ENDPOINT,
  professional: import.meta.env.PUBLIC_PROFESSIONAL_FORM_ENDPOINT
};
```

If an endpoint is absent, show a clear alternate contact method instead of a broken form.

## 19.2 Request Assistance form

Fields:

- Name
- Phone
- Email
- Preferred contact method
- Contacting for self, family member, friend, client, or professional referral
- Help needed:
  - Eyeglasses
  - Broken glasses
  - Emergency temporary glasses
  - Vision changes
  - Technology
  - Independent living
  - Transportation
  - Community resources
  - Benefits information
  - Classes
  - Not sure where to begin
  - Other
- Open-text description
- Consent to contact
- Privacy notice

Do not request Social Security numbers, medical records, diagnoses, or sensitive documents through a general static form.

## 19.3 Volunteer application

Fields:

- Name
- Preferred name
- Address
- Phone
- Email
- Emergency contact
- Areas of interest
- Skills and experience
- Availability
- Estimated hours per month
- Why the person wants to volunteer
- Acknowledgment that selected roles may require screening
- Newsletter option
- Membership information option

## 19.4 Friends membership form

Fields:

- Membership level
- Name
- Organization, optional
- Address
- Phone
- Email
- Relationship or interest category
- Areas of interest
- Communication preferences
- Public recognition or anonymous
- Payment link shown only for paid memberships

## 19.5 Facility reservation form

Fields:

- Organization
- Primary contact
- Email
- Phone
- Event name
- Preferred and alternate dates
- Start and end time
- Attendance
- Space requested
- One-time or recurring
- Equipment
- Event description
- Mission/community benefit
- Billing contact
- Tax-exempt status, optional
- Policy acknowledgment
- Acknowledgment that request does not guarantee reservation

## 19.6 Donation form

Prefer a secure third-party processor.

Fields handled by processor:

- Amount
- One-time or monthly
- Designation
- Tribute
- Donor information
- Recognition preference
- Employer match
- Communication preferences

Never build raw credit-card processing into a static site.

## 19.7 Legacy inquiry form

Fields:

- Name
- Phone
- Email
- Preferred contact method
- Areas of interest
- Comments
- Confidentiality notice
- No-obligation notice

## 19.8 Share Your Story

Fields:

- Name
- Email
- Phone, optional
- Story title
- Story
- Relationship to The Blind Center
- Permission options
- Name display preference
- Photo upload only through an approved secure provider
- Consent and editorial-use statement

---

# 20. ABOUT AND TRUST PAGES

## 20.1 About

### Building a community where everyone can see possibility

The Beaufort County Association for the Blind and Visually Impaired is a nonprofit organization dedicated to helping people protect, preserve, maximize, and adapt their vision while living healthy, independent, and connected lives.

For many people, vision changes can feel overwhelming. Questions arise about work, school, reading, technology, independence, and the future. Others simply want to learn how to protect their eye health.

The Blind Center provides trusted information, practical training, supportive relationships, community connections, and opportunities that help people move forward with confidence.

Work areas include:

- Vision assistance
- Education
- Independent living
- Assistive technology
- Healthy living
- Community resource navigation
- Volunteer engagement
- Professional collaboration

## 20.2 Mission

The Beaufort County Association for the Blind and Visually Impaired exists to help individuals protect, preserve, maximize, and adapt their vision through education, practical training, assistive technology, community engagement, and compassionate support.

## 20.3 Vision

We envision a community where blindness, low vision, and vision loss never prevent someone from living a healthy, active, connected, and fulfilling life.

## 20.4 Values

- Dignity
- Independence
- Education
- Accessibility
- Community
- Innovation
- Stewardship
- Hope
- Partnership
- Respect

## 20.5 Leadership

### Leadership is a responsibility, not a position

Every decision should begin with:

**Will this improve the lives of the people and communities we serve?**

Leadership should emphasize:

- Listening
- Education
- Responsible stewardship
- Innovation
- Transparency
- Community partnership

Add actual leadership names and biographies only after approval.

## 20.6 Board

The volunteer Board provides governance, strategic direction, financial oversight, Executive Director support and evaluation, policy approval, fundraising leadership, and mission stewardship.

Add current Board names only from an approved source.

## 20.7 Strategic vision

Strategic priorities:

1. Protect and preserve healthy vision.
2. Build independence through lifelong learning.
3. Develop the ENCight Experience Apartment and hands-on learning.
4. Serve as a trusted front door to community resources.
5. Strengthen sustainability through giving, membership, rentals, professional space, and partnerships.
6. Expand statewide digital educational reach while remaining rooted in Beaufort County and Eastern North Carolina.
7. Develop the Community Innovation Hub and Community Solutions Lab in 2027.

## 20.8 Community impact

Do not invent counters.

Use CMS or data-file placeholders until verified metrics are supplied.

Possible categories:

- Eyeglasses distributed
- People served
- Classes
- Discovery Guides
- Volunteer hours
- Resource referrals
- Technology demonstrations
- Events
- Professional partners

## 20.9 Transparency

Include:

- Annual reports
- IRS Form 990
- Financial statements
- Strategic plan
- Governance policies
- Conflict of Interest Policy
- Articles of Incorporation
- IRS determination letter
- Donor privacy policy
- Gift Acceptance Policy
- Accessibility statement

---

# 21. ACCESSIBILITY STATEMENT COPY

## Accessibility is one of our core values

At The Blind Center, accessibility is more than a design standard. It is part of our mission.

We believe every person deserves equal access to information, education, services, technology, community life, and opportunity.

Our goal is to remove barriers whenever possible so every visitor feels welcomed, respected, and empowered.

## Digital commitment

We are committed to building and maintaining a website that is accessible to the widest possible audience.

We strive to provide:

- Clear and consistent navigation
- Logical heading structure
- Strong color contrast
- Readable typography
- Keyboard access
- Screen-reader compatibility
- Alternative text
- Descriptive links
- Accessible forms
- Captions and transcripts
- Plain language
- Responsive layouts
- Reduced-motion support

Accessibility is an ongoing commitment.

## Request help

If you experience a barrier or need information in another format, contact The Blind Center.

Add confirmed phone and email.

Ask the visitor to include:

- The page or resource
- The problem experienced
- The device or browser, if known
- The preferred way to receive the information

Do not promise a specific response time unless staff has approved it.

---

# 22. SEARCH

Use a client-side static search solution.

Preferred:

- Pagefind after build
- MiniSearch with a generated JSON index
- Fuse.js only for a small launch library

Search must cover:

- Pages
- Discovery Guides
- Courses
- Events
- Stories
- Research Spotlights
- Professionals
- Resources

Filters:

- Topic
- Audience
- Content type
- Journey
- Difficulty
- In-person or online
- County or service area for resources

Search prompt:

**What would you like to discover today?**

Provide suggested queries and a clear no-results path:

- Browse Discovery Journeys
- Request Assistance
- Contact The Blind Center

---

# 23. CONTENT COLLECTIONS

Create these collections:

## Guides

Educational long-form content.

## Stories

Human stories. Include privacy, consent, and real/composite status.

## Research Spotlights

Plain-language summaries answering:

- What was studied?
- What was found?
- Why does it matter?
- What can a person do?
- What are the limitations?
- Sources

## Courses

ENCight Academy offerings.

## Events

Calendar items.

## Professionals

Independent provider listings.

## Resources

Community-resource directory.

## Documents

Annual reports, policies, handouts, and downloads.

## Discovery Meals

Recipes with:

- Nutrition
- Budgeting
- Adaptive kitchen techniques
- Skills
- Why ingredients matter
- Dietary disclaimer
- Print view

---

# 24. SEO AND STRUCTURED DATA

Every page requires:

- Unique title
- Meta description
- Canonical URL
- Open Graph title and description
- Social image
- Correct H1
- Logical headings
- Descriptive internal links
- Image alt text
- Last updated date where relevant

Use JSON-LD where appropriate:

- `Organization`
- `NonprofitOrganization`
- `WebSite`
- `BreadcrumbList`
- `Article`
- `Event`
- `Course`
- `FAQPage`
- `LocalBusiness` only where accurate
- Do not use medical schema that suggests diagnosis or clinical service where none is provided

Organization data placeholders:

```json
{
  "@context": "https://schema.org",
  "@type": "NonprofitOrganization",
  "name": "Beaufort County Association for the Blind and Visually Impaired",
  "alternateName": "The Blind Center",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "221 North Harvey Street",
    "addressLocality": "Washington",
    "addressRegion": "NC",
    "postalCode": "27889",
    "addressCountry": "US"
  }
}
```

Add phone, email, URL, logo, and social accounts only when confirmed.

---

# 25. PHOTOGRAPHY DIRECTION

Use authentic photography showing:

- People participating
- Hands using devices or preparing food
- Group learning
- Eyewear Center activity
- Technology demonstrations
- Community gatherings
- Volunteers
- Professional Commons
- Real spaces
- Details that communicate dignity and usefulness

Avoid:

- Pity
- Dark isolated portraits
- Hands reaching toward a helpless subject
- White-cane clichés on every page
- Eye close-ups
- Generic hospital imagery
- Images showing unapproved programs
- Images identifying clients without consent

Alt-text method:

- Describe relevant content and function.
- Do not begin with “image of.”
- Keep decorative images empty with `alt=""`.
- Do not repeat surrounding text.
- Describe race, disability, age, or gender only when contextually relevant and known.

---

# 26. SOCIAL MEDIA CONNECTION

The website is the permanent home of substantive content. Social media should lead visitors to it.

For every major page, create:

- Facebook post
- Instagram caption
- LinkedIn post when professionally relevant
- Story or short-video concept
- Social image
- UTM-tagged link

Launch content series:

1. New website
2. Start Here
3. Emergency glasses
4. Discovery Center
5. ENCight Academy
6. Community Learning Kitchen
7. Experience Apartment
8. Friends membership
9. Volunteer Center
10. Professional Commons
11. Ways to Give
12. Legacy Giving
13. Lucinda’s story
14. Tom’s story
15. First Research Spotlight
16. First Discovery Guide

---

# 27. MIGRATION FROM THE EXISTING WEBSITE

## 27.1 Inventory

Before replacing the site:

- Crawl existing URLs.
- Export page titles and descriptions.
- Identify downloadable documents.
- Identify forms and endpoints.
- Identify analytics.
- Identify donation links.
- Identify embedded calendars.
- Identify custom-domain and DNS settings.
- Record redirects.
- Archive the current site.

## 27.2 Content migration rules

- Preserve useful historical material.
- Remove duplicate or outdated pages.
- Replace older terminology with the approved naming system.
- Remove active references to ENCight Gardens.
- Correct independent-provider wording.
- Do not carry forward inaccessible PDFs without remediation.
- Do not migrate old “news” as active current content.
- Preserve annual reports and formal records with dates.

## 27.3 Redirects on GitHub Pages

GitHub Pages does not provide server redirects.

Options:

- Preserve old paths when possible.
- Create lightweight redirect HTML pages using canonical tags and immediate refresh only when necessary.
- Use domain-level redirect support if available through the DNS/CDN provider.
- Maintain a redirect manifest.

Example static redirect page:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Page moved</title>
  <link rel="canonical" href="/new-path/">
  <meta http-equiv="refresh" content="0; url=/new-path/">
</head>
<body>
  <p>This page has moved to <a href="/new-path/">the new page</a>.</p>
</body>
</html>
```

Use base-aware URLs.

---

# 28. QUALITY ASSURANCE

## Accessibility

- Keyboard test
- Screen-reader test
- 200% zoom
- 400% reflow where applicable
- High-contrast mode
- Reduced motion
- Form labels
- Error messages
- Focus order
- Focus visibility
- Skip link
- Alternative text
- Captions and transcripts
- Accessible document downloads

## Browsers

- Safari
- Firefox
- Chrome
- Edge
- iOS Safari
- Android Chrome

## User tasks

Test whether someone can:

- Find emergency eyeglasses.
- Request assistance.
- Find information about glaucoma.
- Find a technology class.
- Become a Friend.
- Volunteer.
- Make a donation.
- Ask about office space.
- Find independent professionals on campus.
- Find the address.
- Report an accessibility barrier.

## Performance

Targets:

- Lighthouse accessibility 100 where practical
- Performance 90 or above on representative pages
- Minimal client JavaScript
- Responsive images
- Lazy loading below the fold
- Font-display swap
- No layout shift from images
- No large autoplay video
- No third-party script without documented purpose

---

# 29. LAUNCH CHECKLIST

## Repository

- Main branch protected
- README complete
- License selected
- Build succeeds locally
- GitHub Action succeeds
- Pages environment configured
- Custom domain configured if applicable
- HTTPS active

## Content

- Operational facts confirmed
- Contact details confirmed
- Hours confirmed
- Board and leadership approved
- Donation links tested
- Forms tested
- Independent-provider disclaimer present
- 2027 projects labeled
- No ENCight Gardens references
- No invented statistics

## Accessibility

- Automated checks
- Manual keyboard test
- Screen-reader review
- Low-vision review
- Mobile review
- PDF review

## Analytics and privacy

Use a privacy-conscious analytics option such as:

- Plausible
- Cloudflare Web Analytics
- Simple Analytics
- GA4 only if organizational requirements justify it

Document cookies and third-party embeds.

## Launch day

- Publish
- Test homepage
- Test forms
- Test donation
- Test search
- Test mobile
- Send announcement
- Publish social campaign
- Monitor inquiries
- Log issues

---

# 30. POST-LAUNCH RHYTHM

Weekly:

- Add or update one Discovery Guide.
- Update events.
- Review forms.
- Check broken links.
- Promote one existing resource.

Monthly:

- Publish a Research Spotlight.
- Publish a Story of Discovery.
- Add Academy content.
- Review analytics and search terms.
- Refresh homepage features.

Quarterly:

- Accessibility review.
- Resource verification.
- Impact update.
- Membership and volunteer campaign.
- Review Discovery Journey gaps.

Annually:

- Annual report.
- Board and leadership update.
- Financial documents.
- Strategic update.
- Privacy and accessibility review.
- Full content audit.

---

# 31. DEFINITION OF DONE

A page is complete only when:

- Copy is approved.
- Route is assigned.
- Metadata is complete.
- Images are selected.
- Alt text is written.
- Links work.
- Forms work.
- Accessibility is tested.
- Mobile is tested.
- Print behavior is acceptable.
- Operational facts are confirmed.
- Page is deployed.

---

# 32. CODEX FIRST-RUN TASK LIST

Codex should perform these tasks in order:

1. Inspect the existing repository.
2. Identify the current framework and GitHub Pages deployment method.
3. Create a migration branch.
4. Preserve the current site in a tagged release or archive branch.
5. Choose Astro unless the existing static framework is clearly better to retain.
6. Install and configure the static build.
7. Configure GitHub Pages base paths.
8. Build global tokens and CSS.
9. Build header, utility navigation, mobile navigation, footer, breadcrumbs, buttons, cards, CTA bands, alert, and accessible form components.
10. Build the homepage using the copy in this document.
11. Build Start Here.
12. Build Community Eyewear Center and Emergency Glasses.
13. Build Discovery Center.
14. Build ENCight Academy.
15. Build Community Resource Network.
16. Build Friends, Volunteer, Ways to Give, Legacy Giving.
17. Build Professional Commons and Professional Services on Campus.
18. Build About, Accessibility, Contact, Visit, and Transparency.
19. Add static search.
20. Add forms only after endpoints are configured.
21. Add test content collections.
22. Run accessibility and performance checks.
23. Produce a migration report listing old URLs, new URLs, placeholders, and unresolved operational facts.
24. Open a pull request for review.
25. Do not merge until the organization approves the preview.

---

# 33. PLACEHOLDERS REQUIRING ORGANIZATIONAL CONFIRMATION

Codex must place these in a single editable data file and visibly mark unresolved values in development:

- Main phone
- Main email
- Current public hours
- Emergency-glasses walk-in hours
- Donation processor
- Newsletter provider
- Form endpoints
- Current Board names
- Current staff names
- Current event calendar
- Current rental rates
- Current membership dues and benefits
- Current provider directory
- Current social-worker schedule wording
- Current annual reports and financial documents
- Social media links
- Final logo files
- Final brand colors if established
- Custom domain
- Privacy-contact person
- Accessibility-contact person

Suggested data file:

```ts
export const site = {
  name: 'The Blind Center',
  legalName: 'Beaufort County Association for the Blind and Visually Impaired',
  address: {
    street: '221 North Harvey Street',
    city: 'Washington',
    state: 'NC',
    postalCode: '27889'
  },
  phone: 'TO_BE_CONFIRMED',
  email: 'TO_BE_CONFIRMED',
  hours: 'TO_BE_CONFIRMED',
  domain: 'TO_BE_CONFIRMED'
};
```

---

# 34. FINAL CREATIVE DIRECTION

The finished site should feel like entering a calm, welcoming institution that has carefully considered the needs of each visitor.

It should not feel:

- Flashy
- Crowded
- Clinical
- Governmental
- Childish
- Pity-based
- Overly donor-focused
- Like a collection of unrelated pages

It should feel:

- Useful
- Attractive
- Vision-friendly
- Calm
- Deeply organized
- Easy to scan
- Easy to enlarge
- Easy to navigate
- Rich in practical knowledge
- Trustworthy
- Alive with stories, classes, and discovery

The essential promise of the website is:

> **Wherever your journey begins, The Blind Center will help you discover a useful next step.**
