# MADEJA — Master Reference Document

**The single source of truth for everything Madeja.**
Portable — reference from any project, any environment, any conversation.

> Last consolidated: **2026-04-24** (palette corrected same day — old blue replaced with current teal `#3DD5D0`)
> Maintainer: Giuseppe Tortorici
> If facts conflict with reality, trust current code/data and update this doc.
> **Canonical design tokens live in** [madeja_brand.py](../../.claude/skills/canvas-design/madeja_brand.py) — this doc mirrors that file, never overrides it.

---

## Table of Contents

1. [Quick Facts](#1-quick-facts)
2. [Brand Identity](#2-brand-identity)
3. [Product & Offering](#3-product--offering)
4. [Pricing & Plans](#4-pricing--plans)
5. [Business Model & Unit Economics](#5-business-model--unit-economics)
6. [Technology & Architecture](#6-technology--architecture)
7. [Market & Competition](#7-market--competition)
8. [Go-To-Market Strategy](#8-go-to-market-strategy)
9. [Current Status & Traction](#9-current-status--traction)
10. [Roadmap & Expansion](#10-roadmap--expansion)
11. [Founder & Contact](#11-founder--contact)
12. [Source Documents](#12-source-documents)

---

## 1. Quick Facts

| Field | Value |
|-------|-------|
| **Company** | Madeja |
| **AI Assistant** | Vera (AI marketing strategist) |
| **Domain** | madeja.digital |
| **App** | app.madeja.digital (Lovable frontend) |
| **Founded** | 2026 (rebranded from FabricAI → TelarAI → Madeja, Feb 2026) |
| **Founder** | Giuseppe Tortorici — solo technical founder |
| **Location** | Spain (Spanish-first, expanding to LATAM + Romance markets) |
| **Stage** | Production, revenue-generating, bootstrapped & profitable |
| **Capital raised** | €0 (bootstrapped) |
| **Team size** | 1 (founder) |
| **Pricing** | €39–349/month (Free tier available) |
| **Production workflows** | 41 |
| **Live API endpoints** | 23 |
| **AI agents** | 14 |
| **Verticals live** | 2 (Fashion, Restaurant) |
| **Target market size** | 300,000+ SMEs in Spain |

### Elevator Pitch

> **Madeja gives Spanish SMEs a complete AI marketing department — 14 specialized agents for €39–349/month instead of €5,000–15,000 for the equivalent human team.** Vera, the AI strategist, knows your brand, catalog, and competitors. You get the strategy and content; you just snap the photo and hit publish.

### One-Liner (Spanish)

> *"Un departamento de marketing completo en bandeja de plata — tú solo sacas la foto y le das a enviar."*

### Founder Framing (use for pitches)

Giuseppe is a **bootstrapped, already-profitable technical founder**. The ask is not capital — it is **network, pilots, and mentors**. (Confirmed strategic framing, Apr 2026.)

---

## 2. Brand Identity

### Brand Name
- **Madeja** (Spanish for "skein" — a coil of yarn; metaphor for the woven threads of a marketing system)
- Rebranded from *TelarAI* (Feb 25, 2026) and before that *FabricAI* (Feb 24, 2026)

### Bot / AI Persona
- **Vera** — the AI marketing strategist
- Works **FOR** Madeja, helps users with **THEIR** brand
- Speaks Spanish (primary) and English
- Sender identity: **vera@madeja.digital** (Google Workspace)

### Visual Identity

> ⚠️ **Use these colors — the earlier blue palette (`#2E86DE`, `#48C9F4`, `#0D1B2A`) is OUTDATED and must not be used.** The current brand uses a **teal accent (`#3DD5D0`)** on near-black navy backgrounds. Canonical source: `madeja_brand.py` in the `canvas-design` Claude skill.

**Backgrounds**
| Token | Hex | Use |
|-------|-----|-----|
| BG Primary | `#0D111A` | Page background, dark navy |
| BG Card | `#131B2A` | Cards, table headers |
| BG Card Hover | `#1A2436` | Card hover state |

**Accent (the brand color)**
| Token | Value | Use |
|-------|-------|-----|
| **Accent Teal** | **`#3DD5D0`** | Logo, CTAs, numbers, highlights (NOT body text) |
| Accent Dim | `rgba(61, 213, 208, 0.15)` | Glow backgrounds, hero gradient |
| Accent Glow | `rgba(61, 213, 208, 0.30)` | Card hover borders |

**Text**
| Token | Hex | Use |
|-------|-----|-----|
| Text Primary | `#F0F2F5` | Headings, primary body |
| Text Secondary | `#8B95A5` | Body text, descriptions |
| Text Muted | `#5A6577` | Labels, captions |
| Border | `#1E2A3A` | Card borders, dividers |

**Status**
| Token | Hex |
|-------|-----|
| Green (success) | `#34D399` |
| Red (error) | `#F87171` |
| Yellow (warning) | `#FBBF24` |

**Typography**
- **Headings / numbers:** Space Grotesk (400/500/600/700)
- **Body:** Inter (300–900)
- Full TYPO scale in `madeja_brand.py`

**Wordmark**
- Always lowercase: `madeja` (never `MADEJA` or `Madeja` in the wordmark)
- Logo file: `Madeja Logo New.png` (light bg) / `madeja-logo-processed.jpg` (dark bg)

### Design Philosophy — "Woven Systematic"

The textile metaphor governs visual communication:
- **Space** structured through the logic of the loom — an implied grid that governs everything
- **Color** operates as material, not decoration — raw fiber tones (charcoal, warm stone) anchor; a single accent emerges with the discipline of first dye
- **Typography** follows warp/weft logic — light strokes for structural text, bolder forms for expressive moments
- **Repeating elements** build density and rhythm the way threads accumulate into cloth
- **Result**: compositions that feel both open and precisely engineered

### Voice & Positioning

- **Sophisticated, clean, premium** — tech-meets-textile
- **Spanish-first** — built for Spanish business culture, not a US translation
- **Strategist, not tool** — Vera is a thinking partner, not a generic AI
- **"Brain, not hands"** — delivers strategy; client executes (photos, posting)
- **No AI product photography** — fashion brands need authentic images; AI product visuals hurt credibility
- **No Virtual Try-On (VTO)** — exists in Moda Madrid B2C demo but NOT part of Madeja platform. Do not present as a Madeja feature.

---

## 3. Product & Offering

### Core Insight

**80/20 split:** Vera provides **strategy and content** (80%); the client provides **execution** (20% — photos, publishing). Client invests ~30 minutes/week for output equivalent to a full marketing team.

### 14 AI Agents

#### Strategy Agents (All Plans)

| Agent | What It Delivers | Human Equivalent Cost |
|-------|-----------------|------------------------|
| **Trend Scout** | Weekly trend reports, seasonal analysis, emerging aesthetics | Market research analyst — €2,000/mo |
| **Copywriter** | Social posts, product descriptions, captions in brand voice | Copywriter — €1,500/mo |
| **Visual Creator** | Mood boards, color palettes, visual direction | Art director — €2,500/mo |
| **Content Calendar** | Monthly posting schedule — themes, copy, hashtags, timing | Social media manager — €1,200/mo |
| **Competitor Analyst** | Auto monitoring of competitor products, pricing, strategy | Competitive intelligence — €3,000/mo |
| **Product Describer** | SEO-optimized product narratives from catalog data | E-commerce specialist — €1,500/mo |
| **Community Manager** | Engagement strategies, comment templates, growth tactics | Community manager — €1,200/mo |
| **Email Strategist** | Campaign planning, subject lines, nurture sequences | Email marketing specialist — €1,800/mo |
| **Blog Writer** | Long-form SEO articles positioning brand as industry voice | Content writer — €1,500/mo |
| **Collection Designer** | Catalog DNA analysis, gap identification, new piece suggestions | Fashion consultant — €3,000/mo |

**Total equivalent hiring cost:** €19,200/month
**Madeja price:** €39–349/month (**96–99% cost savings**)

#### Creative Production Agents (Pro & Premium)

| Agent | Output | Technology |
|-------|--------|-----------|
| **Instagram Post Creator** | Professional image + caption + hashtags | gpt-image-1 + GPT-4.1 |
| **Video Creator** | Brand videos from text prompts | Kling AI via KIE.AI |
| **Product Video Creator** | Enhanced product showcase videos | gpt-image-1 + Kling |
| **TikTok Video Creator** | Vertical 9:16 videos with captions | Kling 2.6 + GPT-4.1 |
| **Email Campaign Sender** | Full email campaigns via Brevo | AI-generated + mass delivery |

#### Restaurant-Exclusive Features (Premium)

| Feature | Description |
|---------|-------------|
| **Voice Booking Agent** | Phone-based reservations via Vapi + Twilio |
| **Booking Management** | Web + phone booking, SMS confirmations, availability calendar |
| **Google Review Auto-Responder** | AI-drafted responses to Google Business reviews |
| **Menu Management API** | Full CRUD for menu items, prices, descriptions |
| **B2C Customer Chatbot ("Milo")** | Public-facing chat for customer inquiries |

### Always-On Automations (Included)

| Automation | Benefit |
|-----------|---------|
| **Catalog Intelligence** | One-time scrape at onboarding, then agents read from Google Sheet |
| **Lead Nurture** | Automatic Day 1/3/7 onboarding emails for new signups |
| **Weekly Performance Digest** | Monday 9AM per-company AI digest email |
| **Google Review Auto-Responder** | AI-drafted review responses (restaurants, every 2h) |
| **Reputation Monitor** | Daily 8AM reputation scan across review platforms |

### Research Reports (Async PDF)

5 on-demand report types delivered as branded PDFs:
trend analysis, competitor deep-dives, market positioning, content strategy, seasonal planning

### What Madeja Does NOT Do

- No AI-generated product photography (authenticity matters for fashion)
- No Virtual Try-On (VTO) — exists in separate demo, not platform
- No standalone text-to-image or text-to-video generators for clients
- No DIY automation platform (not Zapier/n8n for users — it's a finished product)

---

## 4. Pricing & Plans

| Plan | Price/mo | Agent Calls | Target Client | Key Features |
|------|----------|-------------|---------------|--------------|
| **Free** | €0 | 3 | Trial users | All 10 strategy agents, basic reports |
| **Starter** | €39–49 | 15 | Solo founders | Strategy + content planning |
| **Pro** | €119–149 | 50 | Growing brands | + Creative production + Email campaigns |
| **Premium** | €249–349 | 150 | Established businesses | + Voice booking + B2C chatbot + TikTok video |

**Payment:** Stripe (live, production). No contracts, cancel anytime.

---

## 5. Business Model & Unit Economics

### Revenue Streams

1. **Primary — Monthly SaaS subscriptions (MRR)**
   - Average revenue per account (ARPA): ~€120/month
   - Target: 100 paying clients by Q4 2026 = **€12,000 MRR**
2. **Secondary — Digital products** (lead generation + passive income)
   - PDF guides €12–27, prompt packs €15–47, mini-courses €47–97 (Q3 2026)
3. **Tertiary — Enterprise / white-label**
   - White-label Madeja for agencies, custom verticals, API access

### Unit Economics

| Metric | Value |
|--------|-------|
| Customer Acquisition Cost (CAC) | €30–50 (organic + cold outreach) |
| Monthly ARPA | ~€120 |
| Gross Margin | ~85% |
| LTV (12-month) | ~€1,440 |
| LTV/CAC Ratio | 29:1–48:1 |
| Payback Period | <1 month |
| Monthly infra cost per client | €15–20 |

### Cost Structure (Monthly Fixed)

| Item | Cost |
|------|------|
| n8n Cloud | ~€50 |
| OpenRouter (Claude API) | Variable — €0.01–0.05/call |
| OpenAI (images, GPT) | Variable — €0.05–0.50/asset |
| KIE.AI (video) | Variable — €0.10–0.30/video |
| Brevo (email, 10K/mo) | €25 |
| Twilio (SMS) | ~€0.05/SMS |
| Vapi (voice) | ~€0.10–0.30/call |
| Google Workspace | €6 |
| Firecrawl (scraping) | €19 |
| Stripe fees | 1.5% + €0.25/tx |
| **Total fixed** | **~€120/month** |
| **Variable per client** | **~€15–20/month** |

**Break-even:** 2 Starter clients OR 1 Pro client covers all fixed costs.

### ROI Projections

| Horizon | Clients | ARPA | MRR | ARR | Monthly Profit | Gross Margin |
|---------|---------|------|------|------|----------------|--------------|
| 6 mo (conservative) | 30 | €100 | €3,000 | €36,000 | €2,400 | 80% |
| 12 mo (moderate) | 100 | €120 | €12,000 | €144,000 | €10,000 | 83% |
| 18 mo (aggressive) | 300 | €140 | €42,000 | €504,000 | €36,000 | 86% |

Assumptions: 5% monthly churn, 70% Starter/Pro + 20% Premium + 10% Free, organic-only growth.

### Client ROI

| Capability | Without Madeja | With Madeja |
|-----------|----------------|-------------|
| Marketing strategy | €2,000/mo consultant | Included |
| Content calendar | €1,200/mo CM | Included |
| Copywriting | €1,500/mo freelancer | Included |
| Competitor monitoring | €3,000/mo agency | Included |
| Email campaigns | €500/mo tool + specialist | Included (Pro+) |
| Booking system | €100/mo + staff | Included (Premium) |
| Time investment | 20+ hrs/week | 30 min/week |
| **Total monthly value** | **€8,300+** | **€39–349** |

**Client payback: immediate** — first agent call delivers actionable value.

---

## 6. Technology & Architecture

### Platform Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    LOVABLE (Frontend)                     │
│         Web App — madeja.digital / app.madeja.digital     │
│    Onboarding Wizard │ Agent Chat │ Dashboard │ Billing   │
└────────────────────────┬────────────────────────────────┘
                         │ REST API (23 endpoints)
                         ▼
┌─────────────────────────────────────────────────────────┐
│              n8n ORCHESTRATION ENGINE                     │
│           41 Production Workflows                        │
│                                                          │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐              │
│  │ Agent    │  │ Booking  │  │ Billing  │              │
│  │ Gateway  │  │ System   │  │ Engine   │              │
│  │ (14 AI)  │  │ (Web +   │  │ (Stripe) │              │
│  │          │  │  Voice)  │  │          │              │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘              │
│       │              │              │                    │
│  ┌────┴──────────────┴──────────────┴────┐              │
│  │         SHARED SERVICES LAYER          │              │
│  │  Error Handling │ Email │ PDF │ Auth   │              │
│  └────────────────────────────────────────┘              │
└─────────────┬───────────┬───────────┬───────────────────┘
              │           │           │
    ┌─────────┴──┐  ┌─────┴────┐  ┌──┴──────────┐
    │  AI Layer  │  │  Data    │  │  External   │
    │            │  │  Layer   │  │  Services   │
    │ Claude 4.6 │  │ Notion   │  │ Stripe      │
    │ GPT-4.1    │  │ G.Sheets │  │ Brevo       │
    │ gpt-image-1│  │ Pinecone │  │ Twilio      │
    │ Kling AI   │  │ G.Drive  │  │ Vapi        │
    │ Tavily     │  │          │  │ Firecrawl   │
    └────────────┘  └──────────┘  └─────────────┘
```

### Key Technical Differentiators

1. **Multi-tenant by design** — Each company gets isolated data (Notion row, Google Sheet, Pinecone namespace). No cross-client leakage.
2. **Vertical-aware AI** — System prompts dynamically assemble brand context, catalog data, vertical-specific instructions, and competitor info before every LLM call. Fashion and restaurant agents speak different languages because they ARE different agents.
3. **Four-tier execution engine** — Chat Agent routes intelligently:
   - **Fast** (<5s): simple queries
   - **Conversational** (~15s): context-dependent strategy questions
   - **Voice sync** (~10s): real-time voice
   - **Async** (minutes): deep research/creative production, delivered via email
4. **Self-healing** — Error Trigger workflow catches all failures across 41 workflows, sends branded alert emails, logs for debugging.
5. **One-click onboarding** — New company → auto Google Sheet + auto scrape website/Instagram + auto provision Vapi voice agent (restaurants) + auto Drive folder + auto Notion CRM entry. Zero manual setup.

### Infrastructure Stats

| Metric | Value |
|--------|-------|
| Total workflows | ~200 (95 active) |
| Production workflows | 41 |
| API endpoints | 23 |
| Active credentials | 18 |
| AI models used | 5 (Claude Sonnet 4.6, GPT-4.1, GPT-4o, gpt-image-1, Kling 2.6) |
| Supported verticals | 2 (Fashion, Restaurant) |
| n8n version | 2.35.2 |
| n8n instance | giuseppetortorici.app.n8n.cloud |

### Tech Stack

- **Frontend:** Lovable (React) — madeja.digital
- **Orchestration:** n8n Cloud (self-hosted instance)
- **LLMs:** Claude Sonnet 4.6 (primary, via OpenRouter), GPT-4.1-mini (secondary)
- **Image gen:** gpt-image-1 (OpenAI)
- **Video gen:** Kling 2.6 (via KIE.AI)
- **Voice:** Vapi (voice agent) + Twilio (telephony)
- **Scraping:** Firecrawl (websites), Apify (social)
- **Data:** Notion (CRM), Google Sheets (catalogs/bookings), Pinecone (RAG vectors), Google Drive (assets)
- **Email:** Gmail (via vera@madeja.digital) for transactional, Brevo for campaigns
- **Payments:** Stripe (live)
- **Analytics:** custom dashboard via `/webhook/fab-analytics`

---

## 7. Market & Competition

### The Problem

Spanish PYMEs face a brutal marketing choice:

| Option | Monthly Cost | Reality |
|--------|-------------|---------|
| In-house marketing team | €5,000–15,000 | Unaffordable for 95% of SMEs |
| Marketing agency | €1,500–4,000 | Generic, slow, lock-in contracts |
| Freelance specialists | €800–2,500 each | Need 3–5 of them, coordination nightmare |
| DIY with ChatGPT | €20 | No brand context, no strategy, no execution |
| Do nothing | €0 | Invisible online, losing daily |

**Result:** 80% of Spanish fashion and restaurant SMEs have no coherent marketing strategy.

### Market Size

- **~15,000–20,000** fashion PYMEs in Spain
- **~80,000** restaurants in Spain
- **300,000+** total addressable SMEs across all target verticals
- **€3.6B** annual marketing services spend by Spanish SMEs

### Direct Competitors

| Competitor | What They Do | Madeja Advantage |
|-----------|-------------|------------------|
| **Metricool** | Social scheduling + analytics | No AI strategy, no content creation, no brand context |
| **Hootsuite / Buffer** | Social media management | Scheduling only |
| **Copy.ai / Jasper** | AI copywriting | Generic output, no brand context, no catalog |
| **ChatGPT / Claude (direct)** | General AI chat | No memory, no catalog, no multi-agent orchestration |
| **Marketing agencies** | Full-service | 10–50× more expensive, slower, lock-in |
| **Freelance marketers** | Specialist hire | Need 3–5, coordination overhead |

### Indirect Competitors

| Category | Players | Why Madeja Wins |
|----------|---------|------------------|
| Automation platforms | Zapier, Make, n8n | Tools, not solutions |
| CRM with AI | HubSpot, Salesforce | Enterprise pricing (€800+/mo) |
| Vertical SaaS | Toast, Shopify apps | Single-function, no marketing strategy |

### Competitive Moat

1. **Vertical depth** — sector-specific prompts trained on fashion/restaurant data patterns
2. **Integrated system** — not just copywriting OR scheduling OR analytics — all orchestrated
3. **Brand context persistence** — Vera remembers brand colors, catalog, competitors, voice across every interaction
4. **Spanish-first** — built for the Spanish market, in Spanish, understanding Spanish business culture
5. **Asymmetric switching cost** — easy for clients (free tier), hard for competitors (41-workflow orchestration)
6. **Network effects** — more clients per vertical = better trend data, better benchmarks

---

## 8. Go-To-Market Strategy

### Active Channels

| Channel | Strategy | Status |
|---------|----------|--------|
| **Cold outreach** | Daily automated emails to restaurants via Google Search + Firecrawl | Active — ~70 leads/week |
| **LinkedIn prospecting** | Weekly automated scrape of restaurant owners | Active |
| **Instagram** | @gius.tortorici — AI marketing tips, Vera demos | 2.6K followers, growing |
| **YouTube** | Long-form Vera avatar videos, podcast episodes | Weekly |
| **Digital products** | PDF guides on Gumroad — funnel to signups | Live (€12/guide) |
| **Word of mouth** | Existing clients refer others | Organic |

### Planned Channels (Q3–Q4 2026)

- Partnerships with Spanish business associations (CECOT, PIMEC)
- Webinars — "AI Marketing for Your PYME in 30 min/week"
- Referral program — existing clients earn free months
- SEO blog on madeja.digital
- WhatsApp Business outreach (Evolution API)

### Sales Funnel

```
Discovery (Instagram / YouTube / Cold Email / LinkedIn)
    ↓
Landing Page (madeja.digital)
    ↓
Free Registration (0 friction, no credit card)
    ↓
3 Free Agent Calls (experience value)
    ↓
Nurture Sequence (Day 1 / 3 / 7 automated emails)
    ↓
Upgrade to Starter / Pro / Premium (Stripe)
    ↓
Onboarding (auto: scrape + Drive + Notion)
    ↓
Weekly Value Delivery (calendar, reports, campaigns)
    ↓
Retention (Weekly Digest — continuous value)
```

---

## 9. Current Status & Traction

### Latest Health Check — April 23, 2026

**24/24 GREEN** — up from 19/24 (Apr 18). All scheduled workflows, API endpoints, and core features fully operational across both verticals.

| Category | Status |
|----------|--------|
| API Endpoints | 15/15 green |
| Scheduled Workflows | 9/9 green |
| Core Feature Tests | 8/8 pass (Fashion + Restaurant) |

### What's Built and Working

- 41 production workflows — tested, error-handled, GDPR-compliant
- 23 live API endpoints — 100% uptime on latest check
- 14 AI agents — all accessible via web chat
- 2 verticals — Fashion (primary) + Restaurant (secondary)
- Complete booking system — Web + Voice + SMS for restaurants
- **Stripe payments live** — three tiers, production credentials
- Automated lead generation — daily cold outreach + weekly LinkedIn
- Lead nurture — 3-email automated sequence
- Weekly per-company digest — Monday 9AM
- **GDPR compliance** — consent, unsubscribe, data export/delete
- Error monitoring — all 41 workflows wired to error notification

### Development Velocity

| Period | Milestone |
|--------|-----------|
| Jan 2026 | Core platform (agents, chat, Notion CRM) |
| Feb 2026 | Lovable frontend, Stripe billing, PDF reports |
| Mar 2026 | Restaurant vertical, booking, voice agent, Stripe live, GDPR |
| Apr 2026 | Palomo Spain demos, cold outreach, system stabilization |

**One developer built the equivalent of a 5-person engineering team's output in 4 months.**

---

## 10. Roadmap & Expansion

### Expansion Strategy

- **Horizontal (verticals):** Fashion → Restaurant → Hotel → E-commerce → Real Estate → Professional Services
- **Geographic:** Spain → LATAM → Portugal → Italy (Romance-language markets)
- **Product:** SaaS → White-label → API → Marketplace → Digital products

**Each new vertical reuses ~65% of existing infrastructure.**

### Product Roadmap (New Revenue Streams)

| Product | Build Time | Price | Target |
|---------|-----------|-------|--------|
| Google Review Auto-Responder | DONE | Included Pro/Premium | All clients |
| Booking Confirmation Bot | BUILT | Included Starter+ | Restaurants w/ Calendar |
| Cold Outreach Personalization | 1 day | €0.50–2/prospect or €299/mo | B2B services |
| AI Support Chatbot (RAG) | 3–5 days | Setup €500–2,000 + €99–299/mo | Any vertical |
| Hospitality Marketing Suite | 1–2 weeks | €49–249/mo | Hotels, restaurants |
| E-commerce Marketing Autopilot | 1 week | €49–249/mo | Shopify/WooCommerce |
| Real Estate Listing Intelligence | 2–3 weeks | €149–349/mo | Real estate agencies |

### Post-Investment Milestones (if raise)

| Timeline | Milestone | Target |
|----------|-----------|--------|
| Month 1–3 | Launch 3rd vertical (Hospitality) | 50 paying clients |
| Month 3–6 | WhatsApp integration, mobile app MVP | 150 paying clients |
| Month 6–9 | LATAM expansion (Mexico, Colombia) | 300 paying clients |
| Month 9–12 | White-label product for agencies | 500 paying clients |
| Month 12+ | Series A readiness | €50K+ MRR |

### Use of Funds (if raised)

| Priority | Allocation | Purpose |
|----------|-----------|---------|
| Engineering | 40% | +1 full-stack developer, scale infra |
| Sales & Marketing | 30% | Paid ads, content, partnerships |
| Operations | 15% | Legal, accounting, registration |
| Product | 15% | New verticals, WhatsApp, mobile |

> **Note on framing:** Giuseppe is already profitable. Capital is *an option*, not a need. Primary asks: network, pilots, mentors.

---

## 11. Founder & Contact

**Giuseppe Tortorici** — Founder & CEO
- Email: giuseppe.tortorici@gmail.com
- Brand email: vera@madeja.digital
- Platform: https://madeja.digital
- App: https://app.madeja.digital
- Instagram: @gius.tortorici
- WhatsApp / phone: +34 617 128 611

### Founder-Market Fit

- Technical founder who builds **and** understands marketing
- Shipped entire verticals solo (fashion + restaurant in 4 months)
- Deep understanding of Spanish SME market
- Academic validation (Master's project on AI marketing framework)

---

## 12. Source Documents

### In this folder (`C:/Users/giuse/Documents/Madeja/`)
- `Madeja.pdf` — branded overview PDF
- `Madeja._Tu_departamento_de_marketing_y_atención_al_cliente.mp4` — Spanish promo video
- `Madeja._Your_Marketing_&_Customer_Care_Department.mp4` — English promo video
- `madeja-restaurant-leaflet.png` — restaurant vertical leaflet
- `madeja-internal - TikTok - *.mp4` — 8 internal TikTok scripts/videos
- `Bases-Premios-Digital-Tourist-2026.pdf` / `Dossier-Premios-DT-26-vf.pdf` — competition materials

### In the n8n workflows project (`C:/Users/giuse/Documents/n8n workflows/`)
- `MADEJA_PLATFORM_OVERVIEW.md` — original investor-brief markdown (Apr 18, 2026)
- `madeja_investor_brief.html` / `.pdf` — investor brief
- `madeja-pitch-philosophy.md` — "Woven Systematic" design philosophy
- `madeja_report_philosophy.md` — client report design philosophy
- `madeja-leaflet-philosophy.md` — leaflet design notes
- `madeja-pitch-deck.pdf` — pitch deck
- `madeja-pitch-competition.pptx` + `-onepager.pdf` — GBO2026 competition submission
- `madeja-one-pager.pdf` — one-pager
- `madeja-infographic.pdf` — infographic
- `docs/madeja-flow-diagrams.md` — architecture diagrams

### In user-level memory (`~/.claude/projects/.../memory/`)
- `madeja-offering.md` — offering summary
- `madeja-config.md` — config/tech details
- `health-check-apr23.md` — latest health check
- `investor-brief-apr18.md` — investor briefing session notes

---

## How to Use This Document

This is the **canonical reference**. When info conflicts between docs, this one wins (and should be updated if reality has moved on).

**To update:** edit in place and bump the date at top. Keep sections atomic so sections can be lifted into pitches, proposals, or chat replies without rewriting.

**To reference from other environments:** the absolute path is `C:/Users/giuse/Documents/Madeja/MADEJA_MASTER.md`. On other machines, keep this folder synced (Dropbox / OneDrive / git / etc.) and the doc remains portable.

**To share externally:** strip sections 9–11 (current status, roadmap, contact) before sending to people outside the inner circle.
