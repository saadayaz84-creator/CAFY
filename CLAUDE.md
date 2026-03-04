# CAFY Website — CLAUDE.md
# Version: 3.0 (Final Merged)

## Always Do First
- **Invoke the `frontend-design` skill** before writing any frontend code, every session, no exceptions.
- Read this entire file before touching a single line of code.

---

## Project Overview
A premium single-page website for **CAFY** — an AI content automation service.
Single `index.html` file. Tailwind CSS via CDN. Vanilla JavaScript only. No frameworks.

---

## Brand Identity
- **Name:** CAFY
- **Tagline:** Content Creation on Autopilot
- **Sub-tagline:** Create more, manage less.
- **Owner:** Muhammad Saad — AI Content Automation Specialist
- **LinkedIn:** https://www.linkedin.com/in/muhammadsaad-contentautomation/

### Colors (Never use default Tailwind palette)
- Background: `#080808`
- Surface elevated: `#111111`
- Surface floating: `#1a1a1a`
- Border subtle: `#222222`
- Accent primary: `#00d4ff` (cyan glow)
- Accent secondary: `#7b61ff` (purple)
- Text primary: `#f5f5f5`
- Text secondary: `#888888`
- Text muted: `#444444`

### Typography
- **Headings:** Plus Jakarta Sans (Google Fonts) — tight tracking `-0.03em`, bold weight
- **Body:** Inter (Google Fonts) — `1.7` line-height, regular weight
- Never use the same font for headings and body

---

## Brand Assets
- Always check the `brand_assets/` folder before designing
- If logo exists, use it — never use a placeholder where real assets exist
- If color palette file exists, use exact values — do not invent brand colors

---

## Target Audience
Marketing Managers, Agency Owners, Coaches, Brand Founders in USA/UK/UAE.
They are **not technical.** Speak in results and outcomes, never AI jargon.
Every line of copy should answer: "What's in it for me?"

---

## Site Sections — Build Exactly These, In This Order

### 1. Navigation
Add a sticky top nav bar with:
- Left: CAFY logo/name
- Right nav links: `Free Audit` | `ROI Calculator` | `Services` | `Our Stack`
  - All are smooth scroll anchor links to their respective section IDs
- Far right: a "Get Free Audit" button
  - Style: `1px solid #00d4ff` border, transparent background, `#00d4ff` text
  - `border-radius: 8px` | `padding: 8px 20px` | font-size: 14px
  - On click: smooth scroll to `#free-audit`
- Background: `rgba(8,8,8,0.85)` with `backdrop-filter: blur(12px)`
- Bottom border: `1px solid #222222`
- `position: sticky` | `top: 0` | `z-index: 100`

---

### 2. Hero Section
- Large bold headline: "Scale Your Content. Cut Your Costs. Run on Autopilot."
- Subheadline: 1-2 lines in plain English explaining what CAFY does
- Three CTA buttons stacked/grouped:
  - Primary: "Calculate Your ROI" → smooth scroll to `#calculator`
  - Secondary: "Work With Me" → smooth scroll to `#services`
  - **NEW** Third button (full-width, cyan filled): "Get Your Free Content Audit →"
    - Background: `#00d4ff` | Color: `#000000` | Bold | Height: 52px
    - On click: smooth scroll to `#free-audit`
    - Margin top: 12px from the first two buttons
- Below all three buttons, add two trust lines:
  ```
  Line 1: "Free audit delivered to your inbox in under 10 minutes. No calls required."
  Font: 12px | Color: rgba(245,245,245,0.3) | text-align: center | margin-top: 10px

  Line 2: "Helping creators and brands scale content without large teams."
  Font: 13px | Color: rgba(245,245,245,0.4) | text-align: center | margin-top: 6px
  ```
- Subtle animated background: layered radial gradients with slow drift animation
- Optional: particle or glow effect — nothing distracting, purely atmospheric

---

### 3. Problem Section
- Headline: "Sound Familiar?"
- 3 pain point cards with icons:
  1. "Spending 15+ hours/week writing scripts, captions, and posts"
  2. "Paying expensive freelancers for slow, inconsistent results"
  3. "Posting less than you should because production takes too long"
- Each card: icon + bold title + 2-sentence description
- Dark elevated card surface with subtle cyan border glow on hover

---

### 4. How It Works
- Headline: "From Chaos to Autopilot in 3 Steps"
- 3 numbered steps with connecting visual element between them:
  1. **Audit** — We analyze your content workflow and find the bottlenecks
  2. **Build** — We design a custom AI automation system for your brand
  3. **Scale** — You publish more, spend less, and focus on growth
- Each step: large number, bold title, 2-3 sentence description
- Horizontal layout on desktop, vertical on mobile

---

### 5. FREE CONTENT AUDIT — LEAD CAPTURE (NEW — HIGH PRIORITY)
Section ID: `free-audit`

This is a lead generation section. It must be visually prominent and impossible to miss.
It sits between "How It Works" and the ROI Calculator.

#### Section Header:
```
Label: "FREE CONTENT AUDIT"
Style: 12px, uppercase, letter-spacing: 0.15em, color: #00d4ff

H2: "Find Out Exactly What's Killing Your Content Growth"
Style: Plus Jakarta Sans, bold, large (same scale as other H2s)

Subtext:
"Drop your LinkedIn URL below. Our AI analyzes your content, identifies your exact
pain points, and sends you a personalized report — in under 10 minutes."
Style: 16px, color: #888888, max-width: 600px, centered
```

#### Layout:
Two-column grid on desktop (50% / 50%), single column on mobile.
Section padding: match other sections. Max-width: 1200px, centered.

#### LEFT COLUMN — Benefits:

Heading: `"What's Inside Your Free Audit"` — 20px, white, semibold

Five items with cyan checkmark icons (✓ in `#00d4ff`):
```
✓  Your 3 biggest content bottlenecks — backed by data from your actual posts
✓  The content gaps your competitors are exploiting right now
✓  Why your engagement doesn't match your reach — and the exact fix
✓  A 30-day content upscale roadmap tailored to your niche
✓  What your fully automated content system would look like
```
Each item: `display: flex`, `align-items: flex-start`, `gap: 12px`
Text: 15px, `#888888`, `line-height: 1.6`. Spacing between items: 16px.

Below checklist — add a mock "Sample Report" preview card:
```
Container:
  background: rgba(0,212,255,0.03)
  border: 1px solid rgba(0,212,255,0.15)
  border-radius: 12px
  padding: 20px
  margin-top: 32px

Contents:
  - Small label: "SAMPLE REPORT PREVIEW" — 10px, #00d4ff, uppercase, letter-spacing
  - Title: "CAFY CONTENT AUDIT" — 14px, white, semibold
  - Three lines of blurred placeholder text: filter: blur(4px)
  - A fake progress bar at 70% fill in #00d4ff, labeled "Content Gap Score"
  - Corner badge: "Example Only" — small, cyan pill

Purpose: Makes the offer feel tangible. Prospect sees what they'll receive.
```

#### RIGHT COLUMN — The Form:

Form container:
```
background: #111111
border: 1px solid rgba(0,212,255,0.2)
border-radius: 16px
padding: 36px
box-shadow: 0 0 60px rgba(0,212,255,0.05)
```

Fields in order:
```
1. Full Name or Brand Name
   type="text" | placeholder="e.g. John Smith or Acme Agency" | required

2. LinkedIn Profile or Page URL
   type="url" | placeholder="https://linkedin.com/in/yourprofile" | required
   Help text below: "We only read public post data. We never store credentials."

3. Your Industry / Niche
   <select> required
   Options:
   - Select your niche... (disabled selected default)
   - Personal Brand / Creator
   - Marketing & Advertising Agency
   - SaaS / Tech Company
   - E-commerce / Product Brand
   - Consulting / Coaching
   - Real Estate
   - Finance / Fintech
   - Healthcare / Wellness
   - Other

4. Primary Content Goal
   <select> required
   Options:
   - Select a goal... (disabled selected default)
   - Grow my audience and followers
   - Generate more leads and clients
   - Build authority in my niche
   - Increase engagement on my posts
   - Scale content without spending more time
   - All of the above

5. Biggest Content Frustration Right Now
   <textarea> rows="4" required
   placeholder="e.g. I post consistently but nothing grows.
                Or: I never have time to create content every week..."

6. Email Address
   type="email" | placeholder="your@email.com" | required
   Help text below: "Your report arrives within 10 minutes. No spam, ever."
```

Field styling (apply to ALL inputs, selects, textareas):
```css
width: 100%;
background: rgba(245,245,245,0.04);
border: 1px solid #222222;
border-radius: 8px;
padding: 12px 16px;
color: #f5f5f5;
font-size: 14px;
font-family: Inter;
outline: none;
transition: border-color 0.2s ease, box-shadow 0.2s ease;

/* Focus state */
border-color: #00d4ff;
box-shadow: 0 0 0 3px rgba(0,212,255,0.1);
```
Labels: `13px, #888888, margin-bottom: 6px, font-weight: 500`
Space between fields: `20px`

Submit Button:
```
Text: "Analyze My Content → Get Free Report"
width: 100% | height: 52px
background: #00d4ff | color: #000000 | font-weight: bold | font-size: 15px
border-radius: 8px | border: none | cursor: pointer | margin-top: 8px
transition: background 0.2s ease, transform 0.2s ease

Hover: background #00b8d9, transform: translateY(-1px)
Active: transform: translateY(0)
```

#### Form Submission JavaScript:
```javascript
// Place inside the main <script> tag at bottom of body

const auditForm = document.getElementById('audit-form');
const auditFormContainer = document.getElementById('audit-form-container');
const auditSuccess = document.getElementById('audit-success');

// Replace with real n8n URL when automation is ready
// Set to empty string for now — form works visually without a backend
const N8N_WEBHOOK_URL = "";

auditForm.addEventListener('submit', async function(e) {
  e.preventDefault();

  const submitBtn = auditForm.querySelector('button[type="submit"]');
  submitBtn.disabled = true;
  submitBtn.textContent = "Analyzing your content...";
  submitBtn.style.background = "#00b8d9";

  const payload = {
    name: auditForm.querySelector('[name="audit-name"]').value,
    linkedin_url: auditForm.querySelector('[name="audit-linkedin"]').value,
    niche: auditForm.querySelector('[name="audit-niche"]').value,
    content_goal: auditForm.querySelector('[name="audit-goal"]').value,
    frustration: auditForm.querySelector('[name="audit-frustration"]').value,
    email: auditForm.querySelector('[name="audit-email"]').value,
    submitted_at: new Date().toISOString(),
    source: "cafy_website_free_audit"
  };

  try {
    if (N8N_WEBHOOK_URL) {
      await fetch(N8N_WEBHOOK_URL, {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(payload)
      });
    }
  } catch (err) {
    // Fail silently — always show success state
    console.error("Webhook error:", err);
  }

  // Show success state regardless
  auditFormContainer.style.display = "none";
  auditSuccess.style.display = "block";
  showAuditProgressSteps(payload.name, payload.email);
});

function showAuditProgressSteps(name, email) {
  // Update dynamic text in success state
  document.getElementById('audit-success-name').textContent = name;
  document.getElementById('audit-success-email').textContent = email;

  // Animate the 4 steps with delays
  const steps = document.querySelectorAll('.audit-step');
  const delays = [0, 2500, 5000, 7500];

  steps.forEach((step, index) => {
    setTimeout(() => {
      step.querySelector('.step-dot').classList.add('step-complete');
      step.querySelector('.step-text').style.color = "#f5f5f5";
    }, delays[index]);
  });

  // Show final message after all steps
  setTimeout(() => {
    document.getElementById('audit-final-msg').style.display = "block";
  }, 9000);
}
```

#### Success State HTML (hidden by default, shown after submit):
```html
<!-- Add this inside the form column, hidden initially -->
<div id="audit-success" style="display:none; text-align:center; padding: 20px;">

  <!-- Animated checkmark (CSS drawn SVG) -->
  <svg class="audit-checkmark" ...>...</svg>

  <h3 style="font-size:22px; color:#f5f5f5; font-weight:600; margin-top:20px;">
    Your audit is being generated!
  </h3>

  <p style="font-size:15px; color:#888888; margin-top:12px; line-height:1.6;">
    We're analyzing <strong id="audit-success-name" style="color:#f5f5f5;"></strong>'s content right now.<br>
    Your personalized report will land in
    <strong id="audit-success-email" style="color:#00d4ff;"></strong>
    within the next 10 minutes.
  </p>

  <!-- 4 animated progress steps -->
  <div style="margin-top:28px; text-align:left; max-width:320px; margin-inline:auto;">
    <div class="audit-step">
      <span class="step-dot"></span>
      <span class="step-text" style="color:#444444;">Fetching your content data</span>
    </div>
    <div class="audit-step">
      <span class="step-dot"></span>
      <span class="step-text" style="color:#444444;">Analyzing posting patterns</span>
    </div>
    <div class="audit-step">
      <span class="step-dot"></span>
      <span class="step-text" style="color:#444444;">Identifying content gaps</span>
    </div>
    <div class="audit-step">
      <span class="step-dot"></span>
      <span class="step-text" style="color:#444444;">Building your 30-day roadmap</span>
    </div>
  </div>

  <!-- Final message — shown after all steps complete -->
  <div id="audit-final-msg" style="display:none; margin-top:24px;">
    <p style="font-size:14px; color:#888888;">Check your inbox! While you wait:</p>
    <a href="#services"
       style="display:inline-block; margin-top:12px; padding:10px 24px;
              border:1px solid #00d4ff; color:#00d4ff; border-radius:8px;
              font-size:14px; text-decoration:none;">
      See How We Build Systems →
    </a>
  </div>

</div>
```

Step dot CSS:
```css
.audit-step {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 14px;
}
.step-dot {
  width: 18px;
  height: 18px;
  border-radius: 50%;
  border: 2px solid #333;
  flex-shrink: 0;
  transition: all 0.3s ease;
}
.step-dot.step-complete {
  background: #00d4ff;
  border-color: #00d4ff;
  /* Add a checkmark via ::after pseudo element */
}
.step-dot.step-complete::after {
  content: "✓";
  font-size: 11px;
  color: #000;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}
```

#### Below the two-column section (full width, centered):
```
Three trust signals in a row:

🔒 No login required    ⚡ Report ready in 10 min    ✉️ Delivered to your inbox

Style: flex, gap: 48px, justify-content: center, margin-top: 48px
Font: 13px | Color: rgba(245,245,245,0.35)
Icon + text on same line, small gap between them
```

---

### 6. Content ROI Calculator (Section ID: `calculator`)
Keep all existing calculator logic and layout exactly as is.

One change only — update the CTA button text:
```
Old: "Want These Numbers? Let's Talk"
New: "Get These Results — Let's Talk"
```
Button still scrolls to footer/contact.

---

### 7. THE STACK — AI Tools Section (NEW)
Section ID: `our-stack`

#### Section Header:
```
Label: "THE STACK" — 12px, uppercase, letter-spacing: 0.15em, color: #00d4ff
H2: "The AI Tools Powering Your System"
Subtext: "We don't use one tool. We combine the best AI in the world
          into one seamless pipeline built around your brand."
Style: 16px, #888888, max-width: 600px, centered
```

#### Grid Layout:
```
Desktop: 5 columns, gap: 16px
Tablet (768px–1024px): 3 columns
Mobile (<768px): 2 columns
```

#### Tool Card HTML structure (repeat for each tool):
```html
<div class="tool-card" data-description="[DESCRIPTION TEXT]">
  <img src="[LOGO_URL]" alt="[NAME]" width="36" height="36"
       style="object-fit:contain; margin:auto; display:block;" />
  <p class="tool-name">[NAME]</p>
  <span class="tool-category">[CATEGORY]</span>
  <p class="tool-desc">[DESCRIPTION]</p>
</div>
```

#### Tool Card CSS:
```css
.tool-card {
  background: rgba(245,245,245,0.02);
  border: 1px solid #222222;
  border-radius: 12px;
  padding: 24px 16px;
  text-align: center;
  cursor: pointer;
  transition: border-color 0.25s ease, background 0.25s ease, box-shadow 0.25s ease;
}
.tool-card:hover {
  border-color: rgba(0,212,255,0.4);
  background: rgba(0,212,255,0.04);
  box-shadow: 0 0 24px rgba(0,212,255,0.08);
}
.tool-card img {
  filter: grayscale(80%) opacity(0.7);
  transition: filter 0.25s ease;
}
.tool-card:hover img {
  filter: grayscale(0%) opacity(1);
}
.tool-name {
  font-size: 13px;
  color: #f5f5f5;
  font-weight: 600;
  margin-top: 12px;
}
.tool-category {
  display: inline-block;
  font-size: 10px;
  color: #00d4ff;
  background: rgba(0,212,255,0.1);
  border-radius: 20px;
  padding: 3px 10px;
  margin-top: 6px;
}
.tool-desc {
  font-size: 12px;
  color: #888888;
  line-height: 1.5;
  margin-top: 10px;
  opacity: 0;
  max-height: 0;
  overflow: hidden;
  transition: opacity 0.2s ease, max-height 0.3s ease;
}
.tool-card:hover .tool-desc {
  opacity: 1;
  max-height: 100px;
}
```

#### Tools Data (render all 12 cards):
```
1.  Name: n8n
    Category: Automation
    Logo: https://n8n.io/favicon.ico
    Description: The backbone of every system we build. Connects all tools — when content is approved, n8n triggers writing, image generation, scheduling, and publishing automatically. Zero manual steps.

2.  Name: Make
    Category: Automation
    Logo: https://www.make.com/favicon.ico
    Description: Visual workflow automation between apps. We use Make to build multi-step content pipelines that run without any manual triggers.

3.  Name: Freepik AI
    Category: Image AI
    Logo: https://www.freepik.com/favicon.ico
    Description: On-brand visuals at scale. Thumbnails, social graphics, and branded imagery generated automatically — no design team needed.

4.  Name: Higgsfield AI
    Category: Video AI
    Logo: https://higgsfield.ai/favicon.ico
    Description: Cinematic AI video from images and scripts. Produces high-quality video ads and social clips that look like full production shoots.

5.  Name: Kling AI
    Category: Video AI
    Logo: https://klingai.com/favicon.ico
    Description: Realistic motion video from text or image prompts. Powers short-form content for Reels, TikTok, and YouTube Shorts at scale.

6.  Name: HeyGen
    Category: Video AI
    Logo: https://www.heygen.com/favicon.ico
    Description: AI avatar videos with realistic lip-sync. Talking-head explainers and demos — without cameras or studios.

7.  Name: Pika Labs
    Category: Video AI
    Logo: https://pika.art/favicon.ico
    Description: Turns text and images into dynamic short video clips. Repurposes blog posts and tweets into scroll-stopping content in minutes.

8.  Name: ElevenLabs
    Category: Voice AI
    Logo: https://elevenlabs.io/favicon.ico
    Description: Ultra-realistic AI voiceovers in any language. Professional narration for videos, podcasts, and reels — no recording studio required.

9.  Name: Claude AI
    Category: Writing AI
    Logo: https://www.anthropic.com/favicon.ico
    Description: Long-form writing, brand voice calibration, and content planning. Posts, scripts, and captions that sound like your brand — not a robot.

10. Name: ChatGPT
    Category: Writing AI
    Logo: https://openai.com/favicon.ico
    Description: Rapid ideation and bulk content generation. The fast creative layer for high-volume output and content repurposing.

11. Name: Publer
    Category: Publishing
    Logo: https://publer.io/favicon.ico
    Description: Multi-platform auto-publishing across LinkedIn, Instagram, Twitter, and more. Posts go live at optimal times without manual effort.

12. Name: Canva AI
    Category: Design AI
    Logo: https://www.canva.com/favicon.ico
    Description: AI-assisted graphic design at scale. Auto-generates branded post templates and resizes content for every platform automatically.
```

Below the grid:
```
"Every tool is selected based on your niche, platform, and goals.
 You don't need to know how any of this works — that's our job."

Font: 14px | Color: rgba(245,245,245,0.3) | text-align: center | margin-top: 40px
```

---

### 8. Services Section (Section ID: `services`)
Keep all existing service cards.

ADD below the "How We Work Together" H2:
```
"Most clients start with an Audit, move into a Build, then stay on retainer.
 Each step builds on the last."
Font: 15px | Color: #888888 | text-align: center | margin-bottom: 40px
```

ADD visual journey arrows between the 3 cards (desktop only, hidden mobile):
```
Between card 1 and card 2: a "→" in color rgba(0,212,255,0.4), font-size: 24px
Between card 2 and card 3: same
Position: centered vertically in the card row
Hidden via display:none below 768px
```

UPDATE Content Audit card — add 4th bullet point:
```
Existing:
✓ Full workflow analysis
✓ AI tool recommendations
✓ Prioritized action plan

Add:
✓ AI-powered niche content research — trending topics, content gaps & competitor angles
```

---

### 9. Footer CTA
Keep all existing content.

ADD second line below "No agencies. No large teams. Just smart systems.":
```
"Or start with a free audit — no commitment, no calls needed."
Font: 14px | Color: rgba(245,245,245,0.35) | margin-top: 4px
```

ADD second button below "Message Me on LinkedIn":
```
Text: "Get Free Content Audit"
Style: transparent bg, border: 1px solid #00d4ff, color: #00d4ff
Border-radius: 8px | Padding: 12px 28px | margin-top: 12px
On click: smooth scroll to #free-audit
```

ADD above the copyright line:

1. Nav links row:
```
[Free Audit]  [ROI Calculator]  [Services]  [Our Stack]
Font: 13px | Color: rgba(245,245,245,0.35) | Hover: #00d4ff
Display: flex | gap: 32px | justify: center | margin-bottom: 20px
Each is an anchor smooth scrolling to its section ID
```

2. Powered-by tools strip:
```
"Powered by" label — 11px muted text
Followed by 5 logos: n8n | HeyGen | ElevenLabs | Claude AI | Freepik AI
Logo height: 18px
filter: grayscale(100%) opacity(0.25)
Hover per logo: grayscale(0%) opacity(0.65), transition: 0.2s
Display: flex | align-items: center | gap: 20px | justify: center
margin-bottom: 20px
```

---

## Design Rules — Non Negotiable

### Depth & Layering
- Three surface levels: base `#080808` → elevated `#111111` → floating `#1a1a1a`
- Nothing should sit at the same visual z-plane — use shadows and borders to separate layers
- Shadows: never flat `shadow-md` — use layered, color-tinted shadows with low opacity
  - Example: `box-shadow: 0 1px 3px rgba(0,212,255,0.05), 0 8px 32px rgba(0,0,0,0.4)`

### Gradients & Texture
- Layer multiple radial gradients for depth
- Add subtle grain/texture via SVG noise filter
- Never flat solid backgrounds on hero or feature sections

### Animations
- Only animate `transform` and `opacity` — never `transition-all`
- Use spring-style easing: `cubic-bezier(0.34, 1.56, 0.64, 1)`
- Subtle hover lifts on cards: `transform: translateY(-4px)`
- Glow pulse on primary CTA button

### Interactive States
- Every clickable element needs: hover + focus-visible + active states
- No exceptions — buttons, cards, inputs, links

### Anti-Generic Rules
- Never use default Tailwind blue/indigo as primary color
- Never use generic stock-looking sections
- Reference aesthetic: Linear.app, Vercel.com, Resend.com
- Generous whitespace — nothing cramped
- Every section feels intentional, not templated

---

## Technical Rules
- Single `index.html` — all CSS in `<style>` tag in `<head>`, all JS in `<script>` tag before `</body>`
- Tailwind CSS via CDN: `<script src="https://cdn.tailwindcss.com"></script>`
- Google Fonts via CDN link in `<head>`
- No jQuery — vanilla JS only
- No Bootstrap, no React, no external UI libraries
- Smooth scroll: `scroll-behavior: smooth` on `html`
- Fully mobile responsive — mobile-first approach
- Calculator must update all outputs in real time on every input change
- Placeholder images if needed: `https://placehold.co/WIDTHxHEIGHT`
- Tool card logos: if any favicon fails to load, show tool name abbreviation as fallback text

---

## N8N Webhook Setup
The Free Audit form posts to an n8n webhook when the automation is ready.
For now, the webhook URL is an empty string — the form works fully without it.

```javascript
// In the main <script> tag — update this when n8n is ready
const N8N_WEBHOOK_URL = ""; // ← paste your n8n webhook URL here

// Payload structure (do not change — must match n8n workflow):
{
  name, linkedin_url, niche, content_goal,
  frustration, email, submitted_at, source
}
```

When automation is ready: paste webhook URL → save → done. No other changes needed.

---

## Screenshot & QA Workflow (For Claude Code Only)
- Always serve on localhost — never screenshot a `file:///` URL
- After building, take at minimum 2 screenshot passes
- Compare each pass: check spacing, font sizes, colors (exact hex), alignment, border-radius, shadows
- Fix all visible mismatches before marking done
- Check both desktop (1440px) and mobile (375px) views

---

## Mobile Responsiveness Rules
- Free Audit section: single column, full-width inputs, hide mock report card
- Tools grid: 2 columns on mobile
- Service journey arrows (→): `display: none` below 768px
- Section vertical padding: 80px mobile vs 120px desktop
- Hero third button: full width on mobile
- Nav: collapse to hamburger menu on mobile

---

## Final Section Order (Exact)
1. Navigation (sticky)
2. Hero
3. Problem Section
4. How It Works (3 Steps)
5. Free Content Audit ← `#free-audit`
6. ROI Calculator ← `#calculator`
7. The Stack ← `#our-stack`
8. Services ← `#services`
9. Footer CTA

---

## Copy Tone Rules
- Confident but not arrogant
- Results-focused — outcomes over features always
- Simple English — no AI jargon, no tech buzzwords
- Speak directly using "you" and "your"
- Short sentences, high impact
- Never use: "leverage", "utilize", "cutting-edge", "revolutionary"

---

## Hosting
GitHub repository → Vercel (auto-deploy on every push to main branch)
Live URL target: `cafy.vercel.app` or custom domain once purchased

---

## Hard Rules — Never Break These
- Do not add sections not listed above
- Do not use `transition-all` anywhere
- Do not use default Tailwind blue/indigo as primary
- Do not use flat shadows
- Do not stop after one screenshot pass
- Do not use the same font for headings and body
- Do not put prices on the services section
- Do not change the N8N_WEBHOOK_URL payload structure — it must stay consistent for when automation is connected
