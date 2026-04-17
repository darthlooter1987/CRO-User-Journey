# CRO Reporting Product Mock-up Brief

<!-- Paste your brief below this line -->

The goal of the dashboard is not passive reporting. It must function as a decision engine. The user should be able to understand, in under 10 seconds:
1. which landing page or variant is performing best,
2. whether the result is reliable,
3. why it is winning or underperforming,
4. what action to take next.

The mock-up should feel like a premium 2026 SaaS product: clean, structured, spacious, elegant, data-dense but not cluttered, optimized for fast scanning and confident decision-making. Use modern product analytics patterns similar to best-in-class B2B SaaS interfaces. The design should be desktop-first but responsive. Use a polished card-based layout, sticky top bar, left sidebar navigation, strong typography hierarchy, soft dividers, subtle shadows, rounded corners, clear metric grouping, and strong visual distinction between summary information and deep analysis.

GENERAL PRODUCT CONTEXT

This dashboard is for a landing page creation platform. A user can:
- create multiple landing pages for one product,
- assign those pages to different campaign purposes,
- use pages in paid traffic or organic traffic,
- create variants of an existing page,
- split traffic between variants,
- compare performance,
- decide whether to scale a winner, keep testing, or replace a weak page.

The system must support both:
1. single landing pages with no experiment attached,
2. landing pages inside live or completed A/B tests.

IMPORTANT ANALYTICAL LOGIC

The UI must reflect the following logic very clearly:

1. A single landing page with no tested alternative must never be called a “winner”.
A page is only a winner if it has outperformed another page in a structured comparison.

2. Single landing pages should use a Performance Status model, not an Experiment Status model.
Performance Status options:
- Strong
- Average
- Weak
- Needs data

3. A/B tested pages should use an Experiment Status model.
Experiment Status options:
- Winner
- Losing
- Inconclusive
- Not enough data

4. Every landing page must have a Traffic Context tag:
- Paid
- Organic
- Mixed

5. Traffic context must influence metric emphasis:
- Paid pages should visually prioritize spend efficiency and revenue efficiency metrics.
- Organic pages should visually prioritize engagement and lead quality metrics.
- Mixed pages should show both, but still keep the interface readable.

6. The interface should be designed around decision clarity, not metric overload.
Do not show everything at once. Use progressive disclosure:
- immediate summary above the fold,
- analytical detail below,
- deeper breakdowns collapsed or secondary.

DESIGN 3 DISTINCT SCREENS

SCREEN 1: ALL LANDING PAGES VIEW

Purpose:
A portfolio-level dashboard where users can scan all created landing pages and quickly identify:
- what exists,
- what type of page each one is,
- whether it is paid, organic, or mixed,
- whether it is part of a test,
- whether it is performing strongly,
- which pages deserve attention.

Layout:
- sticky top navigation
- left sidebar
- filter and search bar at top of content area
- main inventory area using either a rich table or card-grid hybrid
- clean spacing and high readability
- ability to scan many pages quickly

Top navigation should include:
- product/workspace selector
- global search
- notifications icon
- user avatar/menu

Left sidebar should include:
- Dashboard
- Landing Pages
- Experiments
- Analytics
- Templates
- Settings

At the top of this screen include:
- page title: “Landing Pages”
- optional subtitle: “Track performance, compare variants, and identify what to scale”
- search bar
- date range selector
- filter controls
- primary action button: “Create Landing Page”

Add a filter row with:
- Product filter
- Page type filter
- Traffic context filter
- Campaign filter
- Experiment state filter
- Performance status filter
- Device filter
- Source/channel filter
- Date range picker

Landing page inventory entries should include these fields:
- landing page name
- product name
- page type tag
- traffic context tag
- channel/source tags
- campaign name
- status badge
- experiment badge
- sessions
- conversion rate
- conversions
- revenue or lead value
- last updated time
- quick action menu

Supported page types:
- Awareness
- Conversion
- Differentiation
- Loyalty
- Lead Capture
- Product Education
- Retargeting
- Other

Supported traffic tags:
- Paid
- Organic
- Mixed

Supported experiment state tags:
- No test
- Live test
- Completed test
- Paused test

Status behavior:
- if no experiment exists, show Performance Status:
  Strong / Average / Weak / Needs data
- if experiment exists, show Experiment Status:
  Winner / Losing / Inconclusive / Not enough data

Quick actions on each row/card:
- View dashboard
- Open experiment
- Create variant
- Duplicate page
- Pause
- Archive

Use realistic dummy rows such as:
- Omega 2X – Conversion LP – Paid – Meta Ads – Strong
- Omega 2X – Comparison LP – Paid – Google Ads – Live Test / Inconclusive
- Omega 2X – Loyalty LP – Email / Organic – Strong
- Kids Multivitamin – Awareness LP – Mixed – Weak
- Sleep Support – Lead Capture LP – Organic – Needs data

Add a small summary strip above the inventory with high-level totals:
- total landing pages
- live experiments
- strong performers
- weak performers
- pages needing data

SCREEN 2: SINGLE LANDING PAGE ANALYTICS VIEW

Purpose:
Detailed analytics for one landing page that is either:
- a standalone page,
- or a specific page that may later become part of a test.

This screen should answer:
- Is this page performing well?
- Is it above or below target?
- Where are users dropping off?
- Is traffic high enough to trust the data?
- Should the user create a test or change the page?

Top of page:
- breadcrumb navigation
- landing page name
- product name
- campaign name
- page type tag
- traffic context tag
- channel/source tags
- current status badge
- date range selector
- compare-to-previous-period toggle
- primary actions:
  - Create Variant
  - Duplicate Page
  - Export Report

At the very top, include a hero summary area with:
- page title
- short performance summary sentence
- status badge
- support sentence explaining why status was assigned

Example summary copy:
- “Performance is Strong”
- “Conversion rate is above target and CTA engagement is healthy”
- “Traffic volume is still limited, so results should be treated cautiously”

The top KPI row should use large metric cards. For a generic page include:
- Sessions
- Unique visitors
- Conversion rate
- Total conversions
- Revenue or lead value
- Bounce rate
- CTA click-through rate
- Average time on page
- Scroll depth

Each KPI card should contain:
- metric name
- large current value
- percent change vs previous period
- small sparkline
- tooltip/info icon

For paid pages, add a second emphasized KPI row or insert paid metrics higher on the page:
- Spend
- CPC
- CPA
- ROAS
- Revenue per visit
- Cost per landing page view

For organic pages, emphasize:
- Bounce rate
- Scroll depth
- CTA CTR
- Time on page
- Returning visitor rate
- Assisted conversions or lead completion quality

Include a dedicated Performance Status card.
This card should clearly show:
- status badge: Strong / Average / Weak / Needs data
- benchmark comparison
- short plain-language explanation
- data sufficiency note
- suggested next action

Example content:
- Status: Strong
- Benchmark: 4.8% conversion rate vs 3.5% target
- Reason: “This page is converting above target and has above-average CTA engagement”
- Data note: “Traffic volume is sufficient for directional confidence”
- Suggested action: “Create a variant to test a stronger hero section”

Below the KPI area, add these major sections:

1. PERFORMANCE TREND SECTION
Show line charts for:
- sessions over time
- conversion rate over time
- revenue or lead value over time
- bounce rate over time
Use a clean chart style and allow date-range toggles such as:
- 7D
- 30D
- 90D
- custom

2. FUNNEL SECTION
Display a visual funnel for this landing page:
- Sessions
- CTA Clicks
- Form Starts
- Form Completions
- Purchases / Leads Submitted
Show:
- counts at each step
- conversion percentages between steps
- largest drop-off point highlighted
- short note such as:
  “Biggest drop occurs between Form Start and Form Completion”

3. BEHAVIOR INSIGHTS SECTION
Display cards or small charts for:
- Bounce rate
- Scroll depth
- Average time on page
- CTA CTR
- Exit rate
- Form abandonment rate
- Repeat visit rate
Show short interpretation snippets:
- “High bounce despite healthy CTR may indicate message mismatch below the fold”
- “Scroll depth is weak on mobile users”

4. SEGMENT BREAKDOWN SECTION
Make this expandable/collapsible.
Break down performance by:
- Device
- Source
- Campaign
- Geography
- New vs Returning
For each segment, show:
- sessions
- conversion rate
- conversions
- bounce rate
- revenue / leads
The default state should be collapsed to avoid clutter.

5. RECOMMENDATIONS SECTION
Display an AI-style insight card with 3–5 plain-language findings.
Example:
- “Mobile conversion rate is 28% lower than desktop”
- “Paid traffic from Meta generates high click volume but weaker completion rate”
- “The CTA is attracting clicks, but the form step is causing major abandonment”

6. NEXT ACTION SECTION
Provide action-oriented cards/buttons:
- Create Variant
- Improve Form
- Review Mobile Layout
- Launch A/B Test
- Export Report

7. EMPTY OR LOW-DATA STATES
If the page has little traffic:
- show muted charts
- display grey “Needs data” badge
- replace strong conclusions with cautious copy
- include CTA: “Share traffic to gather enough data”

SCREEN 3: EXPERIMENT / A-B TEST COMPARISON VIEW

Purpose:
This is the most important screen. It must allow the user to determine very quickly:
- which variant is leading,
- how large the uplift is,
- whether the result is trustworthy,
- what changed between variants,
- what to do next.

This screen must feel like a true decision surface.

Top of page:
- breadcrumb navigation
- experiment name
- product
- page type
- traffic context
- start date
- status: Live / Completed / Paused
- control variant name
- number of variants
- primary actions:
  - Adjust Traffic Split
  - Pause Test
  - Declare Winner
  - Create New Variant
  - Export Report

Above the fold, the design must immediately show:

1. EXPERIMENT SUMMARY CARD
Include:
- experiment name
- experiment status badge
- leading variant
- uplift vs control
- confidence level
- total sessions
- days running
- sample size adequacy
- recommended action

Possible statuses:
- Winner
- Losing
- Inconclusive
- Not enough data

Examples:
- “Variant B is leading by +14.2% with 93% confidence”
- “Result remains inconclusive due to insufficient sample size”
- “Variant C is underperforming against control”

2. SIDE-BY-SIDE VARIANT COMPARISON
Do not use tabs. All major variants must be visible side by side.
For each variant card show:
- variant name
- label: Control / Variant B / Variant C
- page thumbnail preview
- traffic share %
- sessions
- conversion rate
- conversions
- revenue / lead value
- bounce rate
- CTA CTR
- average time on page
- scroll depth
- uplift vs control
- confidence badge
- status badge

The leading variant should be visually highlighted with:
- stronger border
- status color
- subtle glow or emphasis
- “Leading” tag

3. UPLIFT + CONFIDENCE MODULE
This block should clearly explain:
- uplift %
- confidence %
- whether current traffic is enough
- whether the test should continue
- estimated reliability
Example:
- “Variant B shows +12.8% uplift over control”
- “Confidence: 91%”
- “Current sample is close to the minimum threshold”
- “Recommendation: continue until 95% confidence or 10,000 sessions”

4. TRAFFIC SPLIT MODULE
Show:
- split allocation per variant
- clear percentage bars
- editable-looking UI controls
Examples:
- A: 50%
- B: 50%
or
- A: 40%
- B: 40%
- C: 20%

5. COMPARISON FUNNEL SECTION
Show side-by-side mini funnels for each variant:
- Sessions
- CTA Clicks
- Form Starts
- Form Completions
- Purchases / Leads Submitted
Highlight:
- where one variant is outperforming another
- biggest drop-off differences

6. TIME TREND SECTION
Overlay lines for each variant on shared charts:
- conversion rate over time
- sessions over time
- revenue / leads over time
- bounce rate over time
Purpose:
- show whether the winner is stable
- reveal novelty spikes
- reveal reversals over time

7. VARIANT DIFFERENCE PANEL
This section is essential.
It should answer:
“What changed between these versions?”
Include:
- side-by-side preview thumbnails
- list of edited components
- tags for changed elements
Supported change tags:
- Headline
- Hero image
- CTA copy
- CTA color
- Button position
- Social proof
- Offer
- Pricing
- Form length
- Layout
- Testimonial placement
- Other

Also include a written summary like:
- “Variant B uses a shorter headline, higher-contrast CTA, and simplified form”

8. SEGMENT WINNER BREAKDOWN
Show whether a variant wins differently by segment:
- Mobile
- Desktop
- Paid source
- Geography
- New vs Returning
For each segment show:
- winning variant
- conversion rate
- uplift
- confidence
This section can be lower on the page.

9. RECOMMENDATION + NEXT ACTION PANEL
This must be blunt and useful.
Examples:
- “Declare Variant B winner and shift 100% traffic”
- “Continue test; confidence still below threshold”
- “Pause Variant C; it underperforms across all major segments”
- “Create a new variant based on B and test form length”

10. DECLARE WINNER MODAL STATE
Include a button and modal mock-up for:
- Declare Winner
When opened, show options:
- Send 100% traffic to winner
- Archive losing variants
- Create follow-up test from winner
- Keep historical reporting accessible

VISUAL AND UX RULES

1. The interface must use a modern premium SaaS style:
- soft neutral background
- white or lightly tinted cards
- clean typography hierarchy
- subtle borders
- rounded corners
- spacious layout
- restrained accent colors
- no clutter

2. Make status extremely easy to read.
Use visual hierarchy to make these instantly obvious:
- strong / weak / needs data
- winner / inconclusive / losing
- uplift %
- confidence %
- next recommended action

3. Use progressive disclosure.
Above the fold:
- answer first
Below the fold:
- analysis and diagnosis
Lower sections:
- segment and detailed breakdowns

4. Avoid overcomplicated data visualization.
Prefer:
- KPI cards
- clean line charts
- small bar charts
- mini funnels
- comparison tables
Avoid:
- noisy pie charts
- excessive legends
- complex statistical visualizations
- cluttered dashboards with too many colors

5. Use plain-language explanations next to metrics.
The mock-up should feel usable by a marketer, not only an analyst.

6. Side-by-side comparison is mandatory for experiments.
Do not hide variants behind tabs.

7. Use realistic empty states and edge states:
- No traffic yet
- Needs data
- Inconclusive test
- Paused test
- Single page with no test

REQUIRED METRICS TO SHOW ACROSS THE PRODUCT

Core traffic and conversion:
- Sessions
- Unique visitors
- Conversion rate
- Total conversions
- Revenue
- Lead value
- Revenue per visit

Engagement and behavior:
- Bounce rate
- CTA click-through rate
- Average time on page
- Scroll depth
- Exit rate
- Form abandonment rate
- Returning visitor rate

Paid media:
- Spend
- CPC
- CPM
- CPA
- ROAS
- Cost per landing page view
- Conversion value

Experiment analysis:
- Uplift %
- Confidence level
- Sample size adequacy
- Traffic split %
- Days running
- Statistical status
- Winning variant
- Stability over time

DATA MODEL / MOCK DATA EXPECTATIONS

Use realistic dummy data throughout the mock-up. Do not use placeholder nonsense like “1234”.
Create plausible data that looks like real landing page performance.

Examples:
Single page example:
- Sessions: 18,420
- Unique visitors: 15,976
- Conversion rate: 4.7%
- Conversions: 866
- Bounce rate: 38.4%
- CTA CTR: 12.9%
- Avg time on page: 1m 42s
- Scroll depth: 64%
- Spend: $6,900
- CPA: $7.97
- ROAS: 3.6x

Experiment example:
Control A:
- Sessions: 8,240
- Conversion rate: 4.2%
- Conversions: 346
- Revenue: $18,900
Variant B:
- Sessions: 8,115
- Conversion rate: 4.8%
- Conversions: 389
- Revenue: $21,200
- Uplift vs control: +14.3%
- Confidence: 92%
- Traffic split: 50/50

COPY TONE

All labels and helper text should be concise, product-like, and clear.
Avoid jargon-heavy explanations.
Use direct language such as:
- “Performance is Strong”
- “Variant B is leading”
- “Result is inconclusive”
- “Traffic is too low to declare a winner”
- “Mobile users are dropping off at the form step”
- “Create a variant to test a stronger headline”

COMPONENTS TO INCLUDE

Make sure the mock-up visibly includes:
- top nav
- sidebar
- page inventory cards or rows
- filter bar
- date picker
- KPI cards
- status cards
- experiment summary card
- side-by-side variant cards
- trend charts
- funnel cards
- behavior insight cards
- segmented breakdown table
- recommendations card
- next action card
- traffic split control UI
- variant difference panel
- export/report button
- create variant button
- declare winner button
- pause test button
- archive action
- empty state / low data state card

TECHNICAL DELIVERY EXPECTATION

Generate this as a static HTML/CSS mock-up, not a functioning analytics product.
The objective is to create a visually convincing product prototype that clearly communicates:
- dashboard hierarchy,
- decision-first UX,
- performance status vs experiment status logic,
- paid vs organic context,
- A/B testing workflow,
- and clear actionability.

The mock-up should look presentation-ready and investor-demo-ready.

Build a static high-fidelity HTML/CSS product mock-up for a premium landing page analytics platform. The interface must include three distinct screens: an all landing pages inventory view, a single landing page analytics view, and an A/B experiment comparison view. The product supports multiple landing pages per product and allows users to create variants, split traffic, compare performance, and decide which version to scale.

This is a decision engine, not a reporting dashboard. The interface must help a marketer identify which page is performing best and why in under 10 seconds. The mock-up should feel like a polished 2026 B2B SaaS product: clean, spacious, premium, minimal, highly legible, card-based, desktop-first, and suitable for a product demo.

Analytical logic:
- Do not label a single non-tested landing page as a winner.
- Standalone pages use Performance Status: Strong, Average, Weak, Needs data.
- Tested pages use Experiment Status: Winner, Losing, Inconclusive, Not enough data.
- Every page must have a Traffic Context tag: Paid, Organic, or Mixed.
- Paid traffic pages prioritize efficiency metrics such as spend, CPC, CPA, ROAS, and revenue per visit.
- Organic pages prioritize behavior and engagement metrics such as bounce rate, time on page, scroll depth, CTA CTR, and returning visitors.

Screen 1: All Landing Pages View
Include a sticky top nav, left sidebar, page title, search, date range picker, filters, summary strip, and a rich inventory table or card list. Each page entry must show landing page name, product, page type, campaign, traffic context, source tags, performance or experiment status badge, sessions, conversion rate, conversions, revenue or lead value, last updated, and quick actions. Include filters for product, page type, traffic context, campaign, device, source, status, experiment state, and date range. Include summary totals such as total pages, live experiments, strong performers, weak performers, and pages needing data.

Screen 2: Single Landing Page Analytics View
Include a breadcrumb, header with landing page name and tags, date controls, and action buttons. Add a top hero summary with a clear status badge and short plain-language explanation. Show KPI cards for sessions, unique visitors, conversion rate, conversions, revenue or lead value, bounce rate, CTA CTR, average time on page, and scroll depth. If traffic context is paid, also prominently show spend, CPC, CPA, ROAS, and revenue per visit. Add a dedicated Performance Status card explaining why the page is Strong, Average, Weak, or Needs data. Below that, add trend charts, a conversion funnel, behavior insight cards, segment breakdowns by device/source/geography/new-vs-returning, an AI-style recommendations card, and a next actions card. Include realistic low-data and no-data states.

Screen 3: Experiment Comparison View
Include a breadcrumb, experiment header, experiment status, start date, control variant, number of variants, and actions such as Adjust Traffic Split, Pause Test, Declare Winner, Create New Variant, and Export Report. Above the fold, show an Experiment Summary Card with leading variant, uplift, confidence, total sessions, days running, sample adequacy, and recommended action. Show all variants side by side without tabs. Each variant card must include a thumbnail, control/variant label, traffic share, sessions, conversion rate, conversions, revenue or lead value, bounce rate, CTA CTR, average time on page, scroll depth, uplift vs control, confidence, and status. Clearly highlight the leading variant visually. Add a dedicated uplift/confidence module, traffic split module, comparison funnel, over-time trend charts, a variant difference panel showing what changed, a segment winner breakdown, a blunt recommendation panel, and a declare winner modal state.

Required metrics:
Sessions, unique visitors, conversion rate, conversions, revenue, lead value, revenue per visit, bounce rate, CTA CTR, average time on page, scroll depth, exit rate, form abandonment rate, returning visitor rate, spend, CPC, CPM, CPA, ROAS, cost per landing page view, conversion value, uplift percentage, confidence level, sample size adequacy, traffic split percentage, days running, and winning variant.

Visual rules:
Use clean cards, strong typography hierarchy, spacious layout, subtle shadows, modern charts, restrained color use, and clear badge systems. Above the fold should answer the decision first. Deeper analytics should appear below. Use progressive disclosure. Avoid clutter, pie charts, or noisy dashboards. Use side-by-side comparison for experiments. Include plain-language helper text and realistic dummy data across all screens.

Use realistic examples like supplement, wellness, or ecommerce landing pages and populate the interface with believable performance data. This is a static HTML/CSS mock-up for presentation purposes, not a working application.

