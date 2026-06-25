# MambaHire — Resume & LinkedIn Optimization Service

MambaHire is a done-for-you resume and LinkedIn rewriting service targeting job seekers in the 2026 market. Clients fill out an intake questionnaire, you use Claude to produce an ATS-optimized resume and LinkedIn profile, review the output, and deliver polished documents within 48 hours. No design skills required. Labor cost per client is roughly 20–30 minutes of your time.

---

## Getting Started — Actionable Steps

### Step 1: Build your Claude system prompt
Save this as a Project instruction in Claude:

> You are an elite resume writer, LinkedIn strategist, and ATS optimization specialist with deep knowledge of how LinkedIn's 2026 AI hiring assistant, semantic entity mapping, and recruiter search algorithms work. You think like a hiring manager, a technical recruiter, and a personal brand consultant simultaneously.
>
> BEFORE DOING ANYTHING ELSE
> Search the web for the most current LinkedIn optimization best practices, algorithm updates, and recruiter behavior research from the past 6 months. Prioritize sources from career strategy publications, LinkedIn's own engineering blog, and staffing industry analysts. Use what you find to inform every recommendation — cite your sources.
>
> When I upload a LinkedIn profile PDF or resume, automatically do the following without asking for confirmation:
>
> Step 1 — Web research first
> Search the web for the most current LinkedIn optimization best practices, algorithm updates, and recruiter behavior research from the past 6 months. Prioritize sources from career strategy publications, LinkedIn's own engineering blog, and staffing industry analysts. Use what you find to inform every recommendation — cite your sources.
>
> Step 2 — Score the profile
> Display a row of 4 metric cards at the top of the output showing:
> - Current score (out of 100)
> - Projected score after all changes (out of 100)
> - Number of critical and high-impact upgrades
> - Estimated time to complete all changes
>
> Step 3 — Ranked upgrade list
> Display every recommended change as an interactive expandable card widget. Each card must include:
> - A numbered circle color-coded by tier: red = critical, orange = high, blue = medium, green = polish
> - A short title summarizing the change
> - A tier badge (Critical, High, Medium, Polish)
> - When expanded: why it matters in 2026 (grounded in research, not generic advice), the source that backs it up, and the exact copy-paste text ready to drop into LinkedIn with a one-click copy button
> - Where exactly to find the field or setting in LinkedIn's UI
>
> Rules for the copy-paste content:
> - Write all text in first person as me, not as a template
> - No placeholders except [Name] in outreach messages
> - Estimate any numbers that strengthen the copy (ticket volumes, revenue, team sizes, percentages) — flag estimated numbers so I can verify
> - Post drafts must sound like a real person, not a career coach — short paragraphs, no buzzwords, no explicit "what do you think" endings
>
> Resume (if requested):
> Build a downloadable .docx file with a dark sidebar, light text, teal accent color on company names and dividers, bold name treatment at the top of the sidebar. ATS-safe — all content in plain flowing text inside a table, no graphics or text boxes. After building, render to image and visually inspect before delivering. Fix any issues before presenting the file.
>
> Tone:
> Direct. No cheerleading. Treat me as someone who understands their field. Every recommendation needs a reason grounded in how LinkedIn's current algorithm actually works.

### Step 2: Build a 10-question Google Form intake questionnaire
Questions to include:
1. Current job title
2. Target job title and industry
3. Years of experience in your field
4. List your top 5 professional achievements (with numbers if possible)
5. List your core technical and soft skills
6. Highest level of education
7. Are you open to relocation? (yes / no / remote only)
8. Upload your current resume (Google Drive link or attach)
9. Paste 2–3 job descriptions you're targeting
10. Anything else we should know about your career goals?

### Step 3: Create a Fiverr listing
- Title: "I will rewrite your resume and optimize it for ATS systems"
- Start at $75 per resume to build reviews fast
- Raise price to $150 after your first 5 reviews
- Raise to $249 after 15 reviews (matching the site pricing)

### Step 4: Get your first testimonials
Post a free offer in 3 places: LinkedIn, a Facebook job seeker group, and a subreddit like r/resumes or r/jobs. Offer 2–3 free rewrites in exchange for honest feedback and permission to use the result as a before/after example.

### Step 5: Prove the workflow, then bundle
Once you can reliably deliver a polished resume in under 30 minutes, add the LinkedIn rewrite to your offer. Upsell clients who ordered just the resume ($249) into the full bundle ($499). The bundle is your highest-margin offer because the LinkedIn rewrite takes less time than the resume once you have the client's background.

### Optional quality check
Run the finished resume through **jobscan.co** (free tier available). Paste the resume + one of the client's target job descriptions. Aim for 75%+ match score before delivering.

---

## Claude Prompt — Generate Client Audit HTML

Use this prompt in your MambaHire Claude project after completing a LinkedIn audit.
It will generate a fully branded, interactive HTML deliverable ready to send to the client.

---

After completing the LinkedIn audit analysis, generate a single downloadable HTML file as the client deliverable. Build it to the following exact specifications:

**File naming:** `MambaHire_LinkedIn_Audit_[ClientFirstName]_[ClientLastName].html`

---

### BRANDING

- Business name: MambaHire
- Analyst name: Charles Spivey
- Website: mambahire.com
- Email: bspivey212@gmail.com
- CTA text: "Leave Us a Review"
- Logo: A square pill with rounded corners containing the letters "MH" — no external image files, built in pure CSS/HTML

---

### COLOR PALETTE

**Dark mode (default):**
```
--bg:      #0A0D12
--bg2:     #111620
--bg3:     #181E2A
--bg4:     #1E2535
--border:  #252E42
--border2: #2E3A52
--accent:  #4F9CF9
--accent2: #38BDF8
--text1:   #F1F5F9
--text2:   #94A3B8
--text3:   #64748B
--text4:   #475569
--red:     #EF4444
--orange:  #F97316
--blue:    #3B82F6
--green:   #22C55E
--gold:    #F59E0B
```

**Light mode (activated by toggle — matches mambahire.com marketing site):**
```
--bg:      #FFFFFF
--bg2:     #F4F6FA
--bg3:     #EDF0F5
--bg4:     #E2E7EF
--border:  rgba(28,43,74,0.10)
--border2: rgba(28,43,74,0.18)
--accent:  #1C2B4A
--accent2: #2A3F6A
--text1:   #1C2B4A
--text2:   #3D4F6B
--text3:   #6B7A8D
--text4:   #8A98A8
--red:     #C0392B
--orange:  #D4651A
--blue:    #1C2B4A
--green:   #1E7A4A
--gold:    #C9A96E
```

Font: Inter (load from Google Fonts)

---

### LAYOUT STRUCTURE

Build the file as a single self-contained HTML file with all CSS and JS inline. Structure:

1. **Sticky header** — MH logomark (CSS-only pill, gradient fill in dark / navy in light), "MambaHire" wordmark, "Resume & LinkedIn Optimization" subtext, analyst name + audit date on the right, light/dark mode toggle button on the far right
2. **Hero section** — client full name (large), current job title and company, 4 score cards in a row
3. **Dimension score bars** — 2-column grid of labeled progress bars showing scores per category
4. **Alert banner** — gold-bordered callout with the honest assessment summary
5. **Expandable cards** — full ranked upgrade list (see Card Specs below)
6. **Footer** — MH logo, mambahire.com link, email link, analyst credit, "Leave Us a Review" CTA button

---

### SCORE CARDS (row of 4)

Display these four metrics pulled from the audit:
- Current Score (out of 100) — colored red if below 60, gold if 60–79, green if 80+
- Target Score (out of 100) — always green
- Number of Critical Gaps — red
- Estimated Time to Complete — blue/accent

---

### CARD SPECS

Each upgrade recommendation is an expandable card. Cards must include:

- A numbered circle, color-coded: red = Critical, orange = High, blue = Medium, green = Polish
- A short title
- A tier badge (Critical / High / Medium / Polish) matching the circle color
- A chevron (▾) that rotates 180° when the card is open
- Card body (hidden until clicked) containing:
  - **Why it matters** — paragraph grounded in 2026 research
  - **Source** — italicized citation with left border accent
  - **One or more copy blocks** — each with a pre-formatted text block and a "📋 Copy" button
  - **Where to find it** — small note with 📍 prefix showing exact LinkedIn UI path
  - **Flag notes** — styled callout (⚑) for any numbers the client should verify

Tier colors:
- Critical: `#EF4444` (dark) / `#C0392B` (light)
- High: `#F97316` (dark) / `#D4651A` (light)
- Medium: `#3B82F6` (dark) / `#1C2B4A` (light)
- Polish: `#22C55E` (dark) / `#1E7A4A` (light)

---

### LIGHT/DARK MODE TOGGLE

- Button sits in the sticky header, far right
- Dark mode is the default
- Toggle shows ☀ "Light Mode" in dark mode, ☾ "Dark Mode" in light mode
- Clicking switches all CSS custom properties to the light palette defined above
- User preference is saved to localStorage and restored on next open
- Print styles always force light mode regardless of toggle state — dark backgrounds never print

---

### COPY BUTTONS

Every text block the client needs to paste into LinkedIn must have its own "📋 Copy" button. Rules:
- Button sits in the top-right corner of the copy block, absolute positioned
- On click: copies the pre block's innerText to clipboard, changes to "✓ Copied" in green for 2 seconds, then resets
- Each copy block gets a unique ID (c1, c2, c3a, c3b, etc.) for the JS to target
- Cards with multiple paste targets (e.g. 3 separate role descriptions) get one copy button per block

---

### JAVASCRIPT (all inline, no external dependencies)

- `toggle(headElement)` — opens/closes card body and rotates chevron
- `copyText(id, buttonElement)` — copies pre block text, shows "✓ Copied" feedback
- `toggleMode()` — switches light/dark, updates icon and label, saves to localStorage
- On page load: restore saved mode preference from localStorage

---

### RESPONSIVE

- Stack score cards to 2-column grid below 680px
- Stack dimension bars to single column below 680px
- Reduce header/section padding on mobile
- Footer stacks to single column on mobile, CTA left-aligned

---

### QUALITY RULES

- No external JS libraries — vanilla only
- No external CSS frameworks
- Google Fonts is the only external request (Inter)
- All content must be inside the single HTML file — no separate CSS or JS files
- Must open and work fully offline after first load (Google Fonts degrades gracefully to system sans-serif)
- Validate before delivering: confirm all pre block IDs have matching copyText calls, confirm card count matches audit item count, confirm toggle works in both directions

---

### POPULATE WITH AUDIT DATA

Fill in the following from the completed audit:
- Client name, title, company, location
- Current score, target score, critical gap count, time estimate
- Dimension scores (one bar per category audited)
- Alert banner text (the honest assessment)
- All expandable cards in ranked order with full copy-paste content, sources, and LinkedIn UI paths
- Any estimated numbers flagged with ⚑ for client verification

---

## Payment Setup

### Stripe (for direct sales from this site)
1. Create an account at stripe.com
2. In your Stripe dashboard, go to **Products → Payment Links**
3. Create three payment links:
   - "Resume Rewrite" — $249
   - "LinkedIn Rewrite" — $349
   - "Full Bundle" — $499
4. In `index.html`, replace the following placeholder hrefs with your real Stripe Payment Link URLs:
   - `href="#stripe-resume"` → Stripe link for Resume Rewrite
   - `href="#stripe-linkedin"` → Stripe link for LinkedIn Rewrite
   - `href="#stripe-bundle"` → Stripe link for Full Bundle

### Formspree (contact / free audit form)
Form is already connected: `https://formspree.io/f/mwvdvvgo`
Configure the email recipient at formspree.io/dashboard if not already set to bspivey212@gmail.com.

---

## Deployment

This site is GitHub Pages compatible — no build step, no dependencies. To deploy:
1. Push this folder to a GitHub repository
2. Go to Settings → Pages → Source: main branch, root folder
3. Your site will be live at `https://yourusername.github.io/your-repo-name`
4. When you have a real domain, point it to GitHub Pages or move the files to any static host (Netlify, Vercel, Cloudflare Pages)

---

## File Structure

```
MambaHire/
├── index.html       — full page HTML
├── css/
│   └── style.css    — all styles (no framework)
├── js/
│   └── main.js      — nav scroll, mobile drawer, reveal animations, stat counter
└── README.md        — this file
```
