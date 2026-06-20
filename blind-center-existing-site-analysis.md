# The Blind Center Existing Website Analysis and Redesign Outline

Analysis date: 2026-06-20  
Primary site: https://theblindcenter.org/  
Requested pages reviewed:

- https://theblindcenter.org/
- https://theblindcenter.org/home/
- https://theblindcenter.org/about/
- https://theblindcenter.org/donate/
- https://theblindcenter.org/resources/
- https://theblindcenter.org/programs/
- https://theblindcenter.org/events/
- https://theblindcenter.org/holiday/
- https://theblindcenter.org/contact/
- https://theblindcenter.org/volunteer/
- https://theblindcenter.org/job-opportunities/

## Methodology

This is a source-and-content audit of the live WordPress site. I reviewed public HTML, WordPress REST page data, page metadata, navigation links, forms, image attributes, loaded assets, and event API output. Automated browser and axe-style rendered auditing were not available in this session, so the accessibility section should be treated as a strong source-level audit plus a checklist for later manual validation in desktop/mobile browsers and screen readers.

## Executive Summary

The current site communicates a useful mission and has core nonprofit pages in place: programs, resources, events, donation, volunteer, jobs, holiday event, and contact. The organization is positioned as a Washington, North Carolina nonprofit serving blind and visually impaired people through independent living support, assistive technology, education, activities, and community programs.

The new version should clarify the mission faster, consolidate duplicate home pages, reduce stale content, and make the site much more accessible by default. This is especially important because the primary audience includes blind, low-vision, older, disabled, volunteer, donor, and community-service users. The current site has an accessibility toolbar, but the redesign should not rely on a toolbar as the main accommodation strategy.

Most important redesign decisions:

1. Make `/` the only home page and retire or redirect `/home/`.
2. Replace stale events output with a clean current-events model and an archive for past events.
3. Rewrite several pages for clarity, simpler reading level, consistent capitalization, and fewer grammar issues.
4. Replace generic image alternative text with descriptive alt text or decorative null alt where appropriate.
5. Build accessibility into the design system: high contrast, large text, keyboard focus, semantic headings, labels, skip links, reduced motion, and clear form instructions.
6. Provide contact alternatives beyond phone, including email and accommodation request paths.
7. Decide whether `/shop/` is active commerce or placeholder content; it is linked from the header but was not included in the requested page list.

## Current Platform and Technical Observations

The site is WordPress using Beaver Builder, Beaver Builder theme, WooCommerce, Gravity Forms, The Events Calendar / Events Calendar Pro, Event Tickets, Yoast SEO, an accessibility-light plugin, GoDaddy tooling, and newsletter subscribe components.

Observed technical load:

| Page | HTML Size | CSS Links | Script Tags | Image Tags |
| --- | ---: | ---: | ---: | ---: |
| `/` | 114.2 KB | 36 | 56 | 8 |
| `/home/` | 161.6 KB | 56 | 102 | 9 |
| `/about/` | 109.5 KB | 36 | 56 | 7 |
| `/donate/` | 113.7 KB | 36 | 56 | 8 |
| `/resources/` | 111.0 KB | 36 | 56 | 6 |
| `/programs/` | 131.2 KB | 36 | 56 | 7 |
| `/events/` | 156.3 KB | 48 | 96 | 9 |
| `/holiday/` | 110.9 KB | 36 | 56 | 6 |
| `/contact/` | 121.7 KB | 40 | 73 | 5 |
| `/volunteer/` | 154.2 KB | 40 | 73 | 6 |
| `/job-opportunities/` | 123.1 KB | 36 | 56 | 7 |

Performance implications:

- The current site loads a large amount of WordPress plugin CSS/JS on nearly every page.
- Events and form pages are especially heavy.
- A static rebuild can be much lighter if it avoids unused WooCommerce, builder, and events assets.
- If forms/events/commerce are still needed, load those scripts only on relevant pages.

Visual system observed:

- Main fonts: Poppins and Jost.
- Frequent colors in compiled CSS include black, white, light blue `#6bb2e2`, orange `#dd6420`, grays, and some red/yellow accents.
- The current design appears to use large hero images, blue/orange accent colors, card-like content blocks, and repeated footer layout.
- Several images use generic alt text such as "The Blind Center."

## Current Information Architecture

Primary navigation:

- Home
- About
- Donate
- Resources
- Programs
- Events
- Holiday
- Contact
- Volunteer
- Job Opportunities

Other linked or discoverable paths:

- `/shop/` with placeholder products and "Crafts Above the Rest"
- `/privacy/`
- `/terms-of-service/`
- event detail pages for 2023 past events
- vendor application PDF: `/wp-content/uploads/2023/04/Super-Early-vendor-application.pdf`
- RSS, comments feed, iCal feed

Recommended new navigation:

- Home
- Programs
- Resources
- Events
- Volunteer
- Donate
- About
- Contact

Recommended secondary/footer navigation:

- Job Opportunities
- Holiday Market
- Shop, only if real and maintained
- Privacy Policy
- Terms of Service

Rationale:

- "Donate" and "Volunteer" should stay prominent as primary conversion actions.
- "Holiday" is better framed as a seasonal event or campaign, not a permanent top-level peer unless it is a major annual destination.
- "Job Opportunities" is useful but should not compete with service, donor, and volunteer tasks in the main nav.
- The site should support direct task paths: get help, find programs, donate, volunteer, attend events, contact staff.

## Audience and User Needs

Primary audiences:

- Blind and visually impaired community members seeking services.
- Low-vision and older adults who need readable, simple, low-friction pages.
- Family members and caregivers seeking help.
- Donors looking for credibility and impact.
- Volunteers looking for ways to serve.
- Job/service applicants.
- Event attendees and vendors.
- Community partners and referral agencies.

Core tasks:

- Understand what The Blind Center does.
- Learn who qualifies for services and how to start.
- Contact the center by phone, email, form, or in person.
- Find programs and registration information.
- Donate money or goods.
- Volunteer and request accommodations.
- Find current events and holiday market information.
- Apply for jobs or service positions.

## Brand and Messaging Notes

Current repeated themes:

- Educate and empower.
- Support blind and visually impaired people.
- Independence, safe haven, assistive technology, independent living skills.
- Washington, North Carolina / Eastern North Carolina.
- More than 40 years of community service.
- Inclusive support regardless of socioeconomic status, religion, race, gender, or age.

Messaging improvements:

- Use consistent capitalization: avoid mixed strings such as "eDUCATE" and "oUR".
- Replace duplicate or near-duplicate mission/approach paragraphs with a clear mission, services summary, and next step.
- Put the most important user action above the fold: "Get help", "Donate", "Volunteer", or "Contact us".
- Avoid jargon where possible. Explain "blind and visually impaired" in plain language, but keep the explanation concise.
- Add credibility signals: 501(c)(3), years served, location, programs, community partners, stories/testimonials if available.

## Page-by-Page Current Content and Redesign Outline

### Home: `/`

Current metadata:

- Title: "Blind and Visually Impaired Support | New Home"
- Description: "Experience Blind and Visually Impaired Support with The Blind Center. Embrace independence and joy."
- WordPress page ID: 1247
- Modified: 2026-03-09

Current content:

- Hero headline around "Educate and Empower" and blind/visually impaired support.
- States The Blind Center is a nonprofit in Eastern North Carolina.
- Mentions 40+ years of classes on independent living, technology, finance, cooking, arts, and more.
- Includes sections explaining blindness/visual impairment, approach, mission, and programs.
- CTAs include "Learn More" and "View Our Upcoming Events."

Current issues:

- Duplicate or overlapping content with `/home/`.
- Inconsistent capitalization in headings.
- Mission and approach sections are very similar.
- "Upcoming Events" CTA points to a page with no future published events.
- Two h1-like sections are present in source structure.

Recommended redesign:

- Make this the canonical home page.
- Above the fold: organization name, one plain-language mission statement, location, and three CTAs: "Get Help", "Donate", "Volunteer".
- Add a "How We Help" section with 4-6 service cards: assistive technology, independent living skills, programs/classes, eyewear/resources, social connection, community events.
- Add "Start Here" section for clients and caregivers.
- Add "Support the Center" section for donors and volunteers.
- Add current events only if maintained; otherwise show a simple "Upcoming events will be announced soon" block plus contact/signup.
- Add footer with address, phone, email, hours if confirmed, newsletter, and legal links.

### Legacy Home: `/home/`

Current metadata:

- Title: "Blind and Visually Impaired Support | The Blind Center"
- Description: "Empower and educate the blind with The Blind Center. Discover resources for thriving lives. Join us for support."
- WordPress page ID: 9
- Modified: 2023-08-30

Current content:

- Older home page with donate CTA.
- Event calendar module shows zero upcoming events and latest past events from April, May, and November 2023.
- Includes a stronger mission statement than the new home page: education, safe haven, assistive technology resources, independent living skills training, and personal goals.
- Includes "What does blind and visually impaired mean?" and "Our Approach."

Current issues:

- Competes with `/` as another home.
- Event module dominates early content despite no future events.
- Heavier than `/`, with more scripts and CSS.
- Some past event content looks stale.

Recommended redesign:

- 301 redirect `/home/` to `/`.
- Migrate the stronger mission language into the new home page after copy cleanup.
- Do not keep duplicate home content.

### About: `/about/`

Current metadata:

- Title: "About | Non-Profit Organization by The Blind Center"
- Description: "Discover non-profit organization services at The Blind Center. Supporting our North Carolina community years of experience."
- WordPress page ID: 11
- Modified: 2023-04-25

Current content:

- "Building Futures" page.
- States The Blind Center is a North Carolina 501(c)(3).
- Serves people regardless of socioeconomic status, religion, race, gender, or age.
- Established by local community members over 40 years ago.
- Administered by a Board of Directors and maintains client representation through Beaufort County Association for the Blind and Visually Impaired.

Current issues:

- Very short for a trust-building About page.
- Board details are general; no names, photos, or governance specifics.
- The relationship between "The Blind Center" and "Beaufort County Association for the Blind" should be clarified.

Recommended redesign:

- Tell a concise origin story.
- Clarify legal name, DBA/brand name, service area, and 501(c)(3) status.
- Include mission, vision, values, and service philosophy.
- Add leadership/board section if approved.
- Add accessibility/inclusion statement.
- Add CTA: "Contact us", "Explore programs", "Support our work."

### Donate: `/donate/`

Current metadata:

- Title: "Donate | Support the Blind by The Blind Center"
- Description: "Support the visually impaired with The Blind Center. Donate today and help those in need."
- WordPress page ID: 13
- Modified: 2023-04-18

Current content:

- "Show Your Support."
- Explains that donations support education and independence.
- Mentions monetary and non-monetary donations.
- Lists accepted items: tin cans, sneakers, cars, boats, trailers.
- Mentions glass recycling.
- Tells visitors to come by the center or reach out.

Current issues:

- The page says "Donate" but does not present a clear donation form or payment path in extracted content.
- Non-cash donation instructions need specifics: accepted condition, drop-off hours, pickup options, tax receipts.
- "For almost 40 years" conflicts with "over 40 years" elsewhere.

Recommended redesign:

- Lead with impact and a clear donation action.
- Provide donation options: one-time, monthly, in-kind, vehicle/boat/trailer, recycling, planned giving if applicable.
- Add exact instructions: address, hours, who to contact, receipt/tax information, accepted/not accepted items.
- Include trust signals: 501(c)(3), secure payment, how funds are used.
- Add donor FAQ.

### Resources: `/resources/`

Current metadata:

- Title: "Resources | Work Readiness by The Blind Center"
- Description: "Discover Work Readiness resources at The Blind Center. Enhance your skills and access essential services today!"
- WordPress page ID: 1172
- Modified: 2026-03-09

Current content:

- Introduces Beaufort County Association for the Blind's resource pages.
- Describes intake, needs assessment, and referral to services.
- Mentions emergency eyewear, paperwork, accommodations, social worker access, and services.
- Service list includes eyewear, technical support, educational training, life skills, and job training.
- Provides address, phone, and emails: admin@theblindcenter.org and info@theblindcenter.org.

Current issues:

- Reads like an internal instruction manual rather than a public resource page.
- The page has no h1 in source audit.
- Dense text should be broken into task-focused sections.
- Intake and privacy expectations should be clearer.

Recommended redesign:

- Title page as "Get Help and Resources."
- Start with "Need support? Here is how to begin."
- Use step cards:
  1. Contact or visit.
  2. Complete intake with assistance if needed.
  3. Discuss needs and goals.
  4. Connect with services or referrals.
- Provide service categories with eligibility, wait time, costs, and contact.
- Add a clear accommodation statement.
- Add downloadable/printable intake information only if accessible.

### Programs: `/programs/`

Current metadata:

- Title: "Programs | Assistive Technology by The Blind Center"
- Description: "Explore Assistive Technology with The Blind Center. Boost your independence through our innovative programs."
- WordPress page ID: 19
- Modified: 2026-03-09

Current content:

- "Making a Difference."
- Explains support for independence and community participation.
- Program offerings include cooking class, health/wellness programming, exercise, DEEP diabetes course, yoga/meditation, healthier living, try-it workshops, weaving, printing, science of well-being, basket weaving, technology lab, and open craft studios.
- CTA: "Contact Us To Register."

Current issues:

- Programs are valuable but presented as a long text list.
- Some offerings need current status, schedule, cost, eligibility, and registration path.
- "NEW PROGRAM!!" may be outdated.
- Some punctuation and copy issues.

Recommended redesign:

- Use program cards grouped by category:
  - Independent Living and Technology
  - Health and Wellness
  - Creative Studios
  - Community and Recreation
  - Work Readiness / Job Training
- Each program card should include: summary, audience, schedule/status, cost if any, registration/contact.
- Add "Request a Program" or "Suggest a Workshop" CTA if the center wants community input.
- Add accessible calendar/sign-up integration only if maintained.

### Events: `/events/`

Current metadata:

- Title: "Events from April 25, 2023 - November 24, 2023 | The Blind Center"
- No useful meta description found.
- Public events API returned zero future published events for 2026-06-20 through 2028-06-20.

Current content:

- "Mark Your Calendar."
- Describes fundraising events for blind and visually impaired people in Eastern North Carolina.
- Event search and calendar views.
- Shows "0 events found" and latest past events:
  - Kris Kringle Holiday Village, November 24, 2023
  - Rock-A-Thon, May 20, 2023
  - Greenhouse Grand Opening dedication and Ceremony, April 25, 2023
- CTA: "Purchase a Ticket" anchor.

Current issues:

- The page appears stale because the public API has no future events and the page title references 2023.
- Events search is heavy and unnecessary if there are no current events.
- "Purchase a Ticket" may be misleading without active tickets.

Recommended redesign:

- If events are actively maintained: use a simple accessible event list with date, time, location, cost, registration/tickets, and accommodation info.
- If not actively maintained: replace with "No upcoming events are scheduled" plus newsletter/contact CTA.
- Keep past events in an archive section or separate page.
- Add event accessibility fields: wheelchair access, transit/parking, service animals, audio/visual accommodations, food/allergen notes, contact for accommodation requests.

### Holiday: `/holiday/`

Current metadata:

- Title: "Holiday | Kris Kringle Christmas Village by The Blind Center"
- Description: "Discover the Kris Kringle Christmas Village at The Blind Center. Festive fun and unique holiday shopping await!"
- WordPress page ID: 1195
- Modified: 2026-03-09

Current content:

- Kris Kringle Christmas/Holiday Village vendor and volunteer recruitment.
- Mentions crafters, artisans, small business owners, hot cocoa, decorations, carolers, smores, vendors, setup/cleanup volunteers.
- Vendor application PDF link.
- "Job Positions" section seeking an organizer.

Current issues:

- The page does not show a date, time, year, location, deadline, or vendor fee in the main text.
- Event naming alternates between Christmas Village and Holiday Village.
- The vendor application PDF is from 2023 and may be outdated.
- Page has no h1 in source audit.

Recommended redesign:

- Retitle as "Kris Kringle Holiday Village."
- Make year-specific content explicit: date, time, location, vendor deadline, cost, organizer contact.
- Archive old vendor PDFs; provide an accessible HTML vendor application or current PDF with tagged accessibility.
- Separate attendee, vendor, performer, and volunteer information.
- Add "Request accommodations for the event."

### Contact: `/contact/`

Current metadata:

- Title: "Contact | Contact Information by The Blind Center"
- Description: "Discover The Blind Center's Contact Information. Reach out today for inquiries and support."
- WordPress page ID: 23
- Modified: 2021-06-12

Current content:

- "Let's Discuss."
- Address: 221 N. Harvey St., Washington, North Carolina, 27889.
- Gravity Forms contact form with name, phone, email, message, and honeypot.
- Phone appears in global header/footer: (252) 946-6208.
- Footer email: director@theblindcenter.org.

Current issues:

- Page should include all contact methods in one place: phone, email, address, hours, parking/transit if possible.
- Form should include accommodation-related topic or message prompt.
- Need confirmation behavior and error handling review.
- Contact page has an iframe, likely map-related, which should have a clear accessible name/title.

Recommended redesign:

- Include contact cards: Call, Email, Visit, Send a Message.
- Include hours, holiday closures, accessibility/access instructions, and parking.
- Add "Need an accommodation?" copy and contact path.
- Ensure form labels, errors, required fields, and success messages are accessible.

### Volunteer: `/volunteer/`

Current metadata:

- Title: "Volunteer | Volunteer Opportunities byThe Blind Center"
- Description: "Join Volunteer Opportunities at The Blind Center. Make a difference today!"
- WordPress page ID: 15
- Modified: 2021-06-12

Current content:

- "Be a Part of Change."
- Describes equal opportunity for volunteers.
- Opportunities: gift shop, administrative assistant, lunches, crafters, fundraisers, gardening, program assistants, handyman help, recycling, events.
- Long Gravity Forms volunteer application.
- Form includes accommodation needs, references, experience, preferences, skills, travel distance, disability question, transport question, and background check note.

Current issues:

- Very long form may be difficult for screen-reader, cognitive, and mobile users.
- Some option text contains typos: "Eommunity", "Epecial", "Msic."
- Duplicate "Volunteer at The Center!" heading appears.
- Need privacy/background-check explanation before collecting detailed data.
- Need save-and-resume or alternative application path if form is long.

Recommended redesign:

- Page top should explain volunteer paths and time commitment.
- Use opportunity cards and a short "I'm interested" starter form.
- Keep full application available as step two, or split into sections.
- Clearly explain background check, transportation, references, and accommodation support.
- Ensure the form supports keyboard completion, fieldsets/legends, accessible errors, and progress indication.

### Job Opportunities: `/job-opportunities/`

Current metadata:

- Title: "Resource Development Coordinator | Job Opportunities"
- Description: "Apply now to be a Resource Development Coordinator at The Blind Center. Make a difference today!"
- WordPress page ID: 1184
- Modified: 2026-03-09

Current content:

- Three AmeriCorps/VISTA-style opportunities:
  - Resource Development Coordinator
  - Program Site Developer
  - Culinary Program Developer
- Each includes long descriptions, responsibilities/qualifications/benefits.
- CTAs include "See More" and "Send Resume."
- Application email: director@theblindcenter.org.

Current issues:

- No h1 in source audit.
- "See More" buttons are ambiguous.
- Bullet characters are misencoded in extracted content.
- Jobs may be stale; no posting date, closing date, status, location, compensation/stipend detail, or application deadline.
- Email-based application is fine but should include subject line requirements consistently.

Recommended redesign:

- Use a current/open/closed jobs model.
- Each job card: title, status, location, type, deadline, summary, apply action.
- Expand details with accessible disclosure controls.
- Add equal opportunity and accommodation statement.
- If no jobs are open, show that clearly and invite newsletter signup.

### Shop: `/shop/` Linked but Not in Requested List

Current metadata:

- Title: "Shop | Shop for Blinds by The Blind Center"
- Heading: "Crafts Above the Rest"
- Products are placeholder products priced at $100 or $110.

Current issues:

- Header includes "Start shopping."
- Product names are placeholder content.
- This undermines credibility if the shop is not ready.

Recommended decision:

- If the shop is real: rename products, add real photos, descriptions, shipping/pickup, return policy, and accessible checkout testing.
- If the shop is not real: remove from header/nav and noindex or redirect until ready.

## Global Components

### Header

Current:

- Donation link and phone number in top area.
- Main nav repeated for desktop/mobile.
- "Start shopping" appears as a linked element.

Recommended:

- Include skip link before header.
- Use one semantic `nav` with accessible mobile disclosure.
- Keep phone number visible.
- Make primary actions distinct: Donate and Get Help/Contact.
- Avoid duplicated menu IDs in desktop/mobile markup.

### Footer

Current:

- Contact info: 221 N. Harvey St., Washington, NC 27889; phone; director email.
- Quicklinks repeat main nav.
- Newsletter subscribe with name/email.
- Copyright currently says 2023.
- GoDaddy badge appears.

Recommended:

- Update copyright year automatically.
- Add accessible newsletter labels and privacy note.
- Include organization legal name and nonprofit status.
- Include privacy/terms.
- Include social links only if maintained.
- Avoid generic footer heading repetition that adds noise to screen-reader navigation.

### Newsletter

Current:

- Name and email fields are present on most pages.
- Source audit indicates placeholder-dependent labels.
- Submit link/button appears as `#` in some extracted output.

Recommended:

- Use real `label` elements for name and email.
- Make the form optional and brief.
- Provide accessible success/error messages.
- Include privacy/consent text.

## Content Cleanup Backlog

High priority:

- Consolidate `/` and `/home/`.
- Remove stale event/ticket messaging or update events.
- Decide whether `/shop/` is real.
- Update holiday event year/date/application.
- Review all job postings for current status.
- Rewrite home mission/approach to remove duplication.
- Add missing h1s on Resources, Holiday, and Job Opportunities.

Medium priority:

- Fix capitalization and grammar across headings.
- Clarify relationship between The Blind Center and Beaufort County Association for the Blind.
- Add hours and direct service intake instructions.
- Update footer year and global contact info.
- Replace generic image alt text.
- Convert PDF-only vendor application into accessible HTML or tagged PDF.

Low priority:

- Add testimonials or client stories if permissions are available.
- Add board/staff profiles if approved.
- Add partner logos or referral resources.

## Accessibility, Hearing, and Visual Accommodation Review

### Current Positive Signals

- The site uses `lang="en-US"`.
- A skip-to-content link exists.
- Most content images have an `alt` attribute.
- Gravity Forms contact/volunteer forms include visible labels for many fields.
- Events Calendar search fields include some labels/ARIA.
- The site includes an accessibility toolbar with options such as heading marking, background color, zoom, font size, readable font, contrast modes, underline links, and marked links.

### Current Accessibility Risks

Source-level issues found:

- Some pages have no h1: Resources, Holiday, Job Opportunities.
- Some page h1s appear to wrap too much body copy, not just a clear page title.
- Root page appears to have more than one h1-style major heading.
- Menu item IDs are duplicated across desktop/mobile menus.
- Newsletter fields are not properly labeled; they rely on placeholders.
- Many pages contain empty links, likely icons, lazy image placeholders, or builder elements.
- Several links/buttons are ambiguous: "Learn More", "See More", "Donate", "Submit" without enough context in repeated areas.
- Many images use generic alt text such as "The Blind Center."
- No `prefers-reduced-motion` handling was found in page source, while animation CSS is loaded.
- Event and form pages load many scripts, which increases the chance of keyboard/focus and mobile performance issues.
- The accessibility toolbar adds its own heading and controls; this can help some users but can also add extra navigation noise.

Manual validation still needed:

- Keyboard-only navigation order.
- Visible focus states.
- Mobile menu keyboard and screen-reader behavior.
- Screen reader reading order with VoiceOver/NVDA/JAWS.
- Color contrast after final visual design.
- Browser zoom at 200%, 300%, and 400%.
- Form error messaging and success confirmation.
- Event calendar controls and date picker accessibility.
- PDF accessibility for the vendor application.

### Blind and Screen-Reader User Requirements

Build requirements:

- Use semantic HTML landmarks: `header`, `nav`, `main`, `section`, `footer`.
- Provide a visible-on-focus skip link.
- One clear h1 per page.
- Headings must describe page structure and not be used for visual styling only.
- All forms need programmatic labels.
- Group checkbox/radio sets with `fieldset` and `legend`.
- Use descriptive link text: "Read about volunteer opportunities" instead of "Learn More."
- Avoid placing critical information only in images or PDFs.
- Use descriptive alt text for informative images and empty alt for decorative images.
- Provide accessible names for icon buttons and disclosure controls.
- Ensure focus moves predictably when opening/closing mobile menu, modals, accordions, or forms.
- Avoid auto-advancing carousels or provide pause/stop controls.

### Low-Vision and Visual Accommodation Requirements

Build requirements:

- Default body text should be at least 18px or a comfortable rem equivalent.
- Use generous line-height, strong contrast, and readable measure.
- Avoid text over busy images unless backed by a solid high-contrast overlay.
- Do not rely on color alone for status, errors, or required fields.
- Provide visible focus styles with at least 3:1 contrast against adjacent colors.
- Support browser zoom/reflow without horizontal scrolling at 320px width and 400% zoom.
- Use high-contrast color tokens from the start, not as a toolbar-only mode.
- Underline links in body copy or provide another persistent non-color indicator.
- Avoid thin font weights for small text.
- Keep phone numbers, addresses, dates, and event details in selectable text.

Suggested design tokens:

- Text: near black on white or very light background.
- Primary action: high-contrast blue or orange with white/near-black text only after contrast verification.
- Link style: underlined by default in content areas.
- Focus ring: thick, visible, and not clipped.
- Minimum touch target: 44px by 44px.

### Deaf and Hard-of-Hearing Accommodation Requirements

Current site does not appear to use audio or video content in the reviewed pages. Future site requirements:

- Any video must include accurate captions.
- Any audio-only content must include a transcript.
- Event pages should state whether ASL interpretation, CART captioning, assistive listening, or other accommodations are available by request.
- Provide non-phone contact paths for people who cannot or prefer not to call: email, form, and mailing/visit information.
- Do not use sound-only alerts in forms or interactions.
- If the site adds webinars, livestreams, or event recordings, include caption/transcript workflows before publishing.

### Cognitive, Motor, and Aging-Related Accommodation Requirements

Build requirements:

- Use plain-language section titles and short paragraphs.
- Break long forms into manageable sections.
- Provide clear required-field indicators and examples.
- Preserve entered form data after validation errors.
- Use large click/tap targets.
- Avoid timed interactions.
- Make error messages specific and placed near fields.
- Provide alternate ways to complete long volunteer or intake forms, such as call/email assistance.

### Accessibility Acceptance Checklist for New Site

Use this checklist before launch:

- Lighthouse/axe automated scan has no serious or critical issues.
- Every page has one h1 and logical heading order.
- All interactive controls are reachable and operable by keyboard.
- Focus is visible at all times.
- Forms have labels, grouped choices, accessible errors, and success messages.
- Images have useful alt text or decorative empty alt.
- PDFs are tagged and accessible, or HTML alternatives are provided.
- Pages work at 200% and 400% zoom.
- Mobile menu works with keyboard and screen reader.
- No content depends on hover only.
- Motion respects `prefers-reduced-motion`.
- Color contrast passes WCAG AA; key text and controls should aim for AAA where practical because of the audience.
- Videos/audio, if added, include captions/transcripts.
- Events include accommodation request instructions.

## Proposed New Site Outline

### Home

- Hero: "The Blind Center" plus short mission.
- Primary CTAs: Get Help, Donate, Volunteer.
- "How We Help" services summary.
- "Start Here" client/caregiver path.
- Featured programs.
- Current events or no-events message.
- Donation/volunteer impact section.
- Contact/location strip.

### Programs

- Overview of program philosophy.
- Program categories with cards.
- Current schedule or "contact to register."
- Accessibility/accommodation notes.
- CTA: Register or ask about a program.

### Resources / Get Help

- How intake works.
- Services: eyewear, technical support, educational training, life skills, job training, referrals.
- What to bring / what to expect.
- Contact paths.
- Accessible downloadable resources only if maintained.

### Events

- Current event list.
- Past event archive.
- Event accessibility info.
- Newsletter signup for updates.

### Donate

- Donation impact.
- Monetary donation path.
- In-kind donations.
- Recycling/vehicle donations if active.
- Tax/receipt and drop-off details.
- FAQ.

### Volunteer

- Volunteer overview.
- Opportunity categories.
- Short interest form.
- Full application or application next step.
- Background check and accommodations information.

### About

- Mission and history.
- Who is served.
- Governance / board.
- Service area.
- Accessibility and inclusion statement.
- Contact/support CTAs.

### Contact

- Address, phone, emails, hours.
- Form.
- Map with accessible fallback address.
- Parking/transit/accessibility notes.
- Accommodation request route.

### Job Opportunities

- Current openings.
- Closed/no openings state.
- How to apply.
- Equal opportunity and accommodation statement.

### Holiday Market

- Seasonal landing page.
- Event year/date/time/location.
- Vendor, volunteer, performer, attendee sections.
- Current accessible application.
- Archive or redirect off-season.

## Recommended Development Approach for This Repository

This repository is currently a small static site with `index.html` and `styles.css`. A first rebuild can remain static if forms are handled by a service or linked externally.

Suggested file structure:

```text
/
  index.html
  about.html
  programs.html
  resources.html
  events.html
  donate.html
  volunteer.html
  contact.html
  jobs.html
  holiday.html
  privacy.html
  terms.html
  styles.css
  assets/
    images/
    documents/
```

Recommended build priorities:

1. Build shared header/footer and accessible navigation.
2. Build home, programs, resources, donate, volunteer, and contact first.
3. Add events with a simple maintainable data pattern.
4. Add jobs and holiday as content modules that can show active/inactive states.
5. Add forms only after deciding the backend/form service.

Static-site form options to decide:

- Keep Gravity Forms only if staying on WordPress.
- Use a static form provider for contact/volunteer/newsletter.
- Use mailto only for low-volume applications, but do not rely on mailto for primary contact forms.

## Open Questions for Stakeholders

- What is the legal organization name, and how should it relate to "The Blind Center" branding?
- What are current hours?
- Which email addresses should be public?
- Is the shop active or placeholder?
- Are donations accepted online today? If yes, through what processor?
- Are all listed programs currently active?
- What programs have fees, registration limits, or eligibility requirements?
- Are there upcoming events for 2026?
- Should old event pages remain indexed?
- Is the Kris Kringle page for 2026 active, and what are the current dates/deadlines?
- Are job opportunities current?
- Who receives contact, volunteer, vendor, and job inquiries?
- What accommodations can the center currently provide for events and services?

## Source URLs

- https://theblindcenter.org/
- https://theblindcenter.org/home/
- https://theblindcenter.org/about/
- https://theblindcenter.org/donate/
- https://theblindcenter.org/resources/
- https://theblindcenter.org/programs/
- https://theblindcenter.org/events/
- https://theblindcenter.org/holiday/
- https://theblindcenter.org/contact/
- https://theblindcenter.org/volunteer/
- https://theblindcenter.org/job-opportunities/
- https://theblindcenter.org/shop/
- https://theblindcenter.org/wp-json/wp/v2/pages
- https://theblindcenter.org/wp-json/tribe/events/v1/events
