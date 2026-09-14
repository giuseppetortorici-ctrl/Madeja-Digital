# MADEJA — Master Reference Document

**The single source of truth for everything Madeja.**
Portable — reference from any project, any environment, any conversation.

> Last consolidated: **2026-09-14** (Pricing restructure — Madeja Pro €59 base + Madeja Voice €99 add-on; old 4-tier structure retired)
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
| **B2B Persona** | **Vera** — AI reputation assistant who speaks to the *restaurant owner* (weekly report, review auto-response) |
| **B2C Persona** | **Milo** — voice agent (Vapi + Twilio) + web chatbot for the owner's *customers* (24/7 bookings + FAQ) |
| **Domain** | madeja.digital |
| **App** | app.madeja.digital (Lovable frontend) |
| **Founded** | 2026 (rebranded from FabricAI → TelarAI → Madeja, Feb 2026) |
| **Founder** | Giuseppe Tortorici — solo technical founder |
| **Location** | Spain (Spanish-first, expanding to LATAM + Romance markets) |
| **Stage** | Production, revenue-generating, bootstrapped & profitable |
| **Capital raised** | €0 (bootstrapped) |
| **Team size** | 1 (founder) |
| **Pricing** | €59/month (Pro) + €99/month optional Voice add-on |
| **Active workflows** | ~31 (post Sep-14 simplification) |
| **Live API endpoints** | ~15 (restaurant ops + Lovable infra) |
| **AI personas** | 2 (Vera B2B, Milo B2C) |
| **Verticals live** | 1 (Restaurants) — Fashion vertical deactivated Sep 14 2026 |
| **Target market size** | ~80,000 restaurants in Spain |

### Elevator Pitch

> **Madeja is the reputation and booking operations platform for Spanish restaurants.** €59/month covers a live review-intelligence dashboard, weekly branded PDF report, automatic responses to Google/TripAdvisor/TheFork/ElTenedor reviews in the owner's tone, a booking sheet with SMS confirmations, and a Milo web chatbot for customer FAQs. Add Madeja Voice at €99/month and Milo answers your phone 24/7 with 300 booking minutes included.

### One-Liner (Spanish)

> *"Mientras tú estás en servicio, Madeja lleva tu reputación y coge las reservas."*

### Founder Framing (use for pitches)

Giuseppe is a **bootstrapped, already-profitable technical founder**. The ask is not capital — it is **network, pilots, and mentors**. (Confirmed strategic framing, Apr 2026.)

---

## 2. Brand Identity

### Brand Name
- **Madeja** (Spanish for "skein" — a coil of yarn; metaphor for the woven threads of a restaurant's reputation and operations)
- Rebranded from *TelarAI* (Feb 25, 2026) and before that *FabricAI* (Feb 24, 2026)

### AI Personas — Two Voices, One Brand

Madeja deploys **two distinct personas** with different audiences and scopes. **Never conflate them** in any artifact (deck, copy, mockup, email, leaflet).

| Persona | Audience | Role | Surface |
|---------|----------|------|---------|
| **Vera** | The *owner* (B2B) | AI reputation assistant | `vera@madeja.digital`, weekly branded PDF report, Google/TripAdvisor/TheFork review auto-responses in the owner's tone, reputation alerts |
| **Milo — voice** | The owner's *customers* (B2C) | Phone agent for inbound bookings | Vapi + Twilio, dedicated ES phone number per restaurant, 24/7 reservations + FAQ + SMS confirmations |
| **Milo — web chatbot** | The owner's *customers* (B2C) | Public-facing web chat | Embedded chat widget on the restaurant's site — menu, hours, reservations, booking capture |

- Vera works **FOR** Madeja and helps the owner keep their reputation clean and their inbox quiet
- Vera **dispatches Milo** to handle customer-facing channels (voice + web chat)
- Both speak Spanish (primary) and English
- The owner-facing tagline *"Mientras tú estás en servicio, Vera trabaja por ti"* — Vera is the umbrella brand the owner hires; Milo is the customer-facing agent Vera dispatches.
- When describing voice/call/chat → Milo. When describing reviews, digest, and owner insights → Vera.

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
- **No AI content generation** — Madeja no longer produces marketing content (retired Sep 2026); focus is review intelligence + booking ops
- **No Virtual Try-On (VTO)** — exists in Moda Madrid B2C demo but NOT part of Madeja platform. Do not present as a Madeja feature.

---

## 3. Product & Offering

### Core Insight

Restaurant owners already do this work — checking reviews every morning, calling back missed bookings, replying to complaints between services. Madeja automates the loop end-to-end: reviews are collected, ranked, summarized, and answered; bookings are captured 24/7 on web or phone; the owner reads one weekly PDF instead of eleven browser tabs. Client invests ~5 minutes/day, gets the output of a part-time reputation manager plus a night receptionist.

### Madeja Pro — What's Included (€59/month)

#### Review Intelligence

| Capability | Description |
|------------|-------------|
| **Live dashboard** | Weekly refreshed scores across Google, TripAdvisor, TheFork, ElTenedor. Trend arrows, sentiment breakdown, most-mentioned dishes and complaints. |
| **Barrio benchmarking** | Compare your rating and review velocity against the top N restaurants in your Madrid barrio. Percentile ranking updated weekly. |
| **Weekly branded PDF report** | Delivered Monday 9AM to the owner. Executive summary, sentiment shift, competitor snapshot, action items — all in Madeja brand. |
| **Reputation monitor** | Daily 8AM silent scan across all review platforms. Alerts only when negative or new reviews appear — no digest fatigue. |
| **Vera — auto-response** | AI drafts + posts replies to Google Business Profile reviews in the owner's tone every 2h. Owner can review-and-approve or full-auto. |

#### Bookings & Customer Ops

| Capability | Description |
|------------|-------------|
| **Booking sheet** | Google Sheet backend, availability calendar, one-click confirmations, SMS to the customer via Twilio. |
| **Menu management** | Full CRUD API on menu items, prices, allergens, descriptions — updated once, propagated to chatbot + voice agent + review responses. |
| **Milo web chatbot** | Embeddable widget on the restaurant's site. Answers menu / hours / reservations / FAQ in Spanish or English. Captures bookings without staff involvement. |

### Madeja Voice — What's Included (€99/month add-on)

| Capability | Description |
|------------|-------------|
| **Dedicated ES phone number** | Local Spanish Twilio number provisioned per restaurant at onboarding. |
| **Milo voice agent** | Vapi-powered 24/7 phone answering — takes bookings, quotes hours, handles menu questions, escalates edge cases. |
| **300 voice minutes/month included** | Overage billed at **€0.30/minute**. |
| **SMS booking confirmations** | Customer receives confirmation text on booking; owner sees the booking land in the sheet. |

### One-Click Onboarding

New restaurant → Notion CRM entry + Google Sheet (menu + bookings) auto-scaffolded + website/Instagram scraped into brand context + Google Business Profile linked + (if Voice) Vapi assistant + Twilio number provisioned. Zero manual setup, no forms to fill in the app.

### What Madeja Does NOT Do

- No marketing content generation (no post scheduling, no ad copy, no image/video creation — the old "14 agents" suite was retired Sep 2026 with the pivot to review intelligence)
- No fashion vertical — that vertical was deactivated Sep 14 2026 to focus the platform
- No standalone chatbot / voice product for verticals other than restaurants
- No DIY automation platform (it's a finished product, not Zapier/n8n for end users)

---

## 4. Pricing & Plans

**Two-component pricing, decoupled to protect margin.** The base plan covers reputation + booking operations; the voice add-on is a metered utility for restaurants that want 24/7 phone answering.

### Madeja Pro — €59/month

Same price for every restaurant. No feature gating.

**Included:**
- Review Intelligence Dashboard with barrio-level benchmarking
- Weekly branded PDF report (Monday 9AM)
- Vera — Google Business Profile review auto-responder in owner's tone
- Reputation Monitor (TripAdvisor / TheFork / ElTenedor, daily 8AM)
- Milo web chatbot — customer FAQ + menu + booking widget
- Booking management (Google Sheet backend + SMS confirmations via Twilio)
- Menu / catalog management API
- One-click onboarding (Notion CRM + sheet + scrape + GBP link)
- No usage limits

### Madeja Voice — €99/month *(add-on, restaurants only)*

Requires an active Madeja Pro subscription. Available only for restaurant clients.

**Included:**
- Dedicated ES local phone number (Twilio)
- Milo voice agent (Vapi) — 24/7 inbound booking + FAQ
- **300 voice minutes/month included**
- SMS booking confirmations
- Overage: **€0.30/minute** beyond 300 min

**Why priced separately:** Voice runs €0.14–0.20/min all-in (Vapi + STT + LLM + TTS + Twilio ES). Bundling it into the base plan would sink margin — the split keeps Pro at ~85% gross margin and prices Voice honestly against usage.

### Old 4-tier structure — retired

The previous Free / Starter (€39–49) / Pro (€119–149) / Premium (€249–349) tiers were built to feature-gate a content-creation tool that no longer exists. Retired. Any surviving references in code (`Code: Check Limit`, `remaining_uses`, Pro/Premium filters) are dead paths pending cleanup.

### Payment

Stripe (currently deactivated in code, ready to reactivate). Direct-sales + manual onboarding during early access & capstone demo — everyone who onboards gets full access automatically. No contracts, cancel anytime once billing is live.

---

## 5. Business Model & Unit Economics

### Revenue Streams

1. **Primary — Monthly SaaS subscriptions (MRR)**
   - Pro: €59/month · Voice add-on: €99/month (restaurants only, ~40% attach expected)
   - Blended ARPA: **~€99/month**
   - Target: 100 paying clients by Q4 2026 = **~€9,900 MRR**
2. **Secondary — Voice overage** (metered, restaurants that exceed 300 min)
   - €0.30/min beyond bundle · thin margin (~50%) but expands with client volume
3. **Tertiary — Digital products & white-label**
   - PDF guides €12–27, prompt packs €15–47, mini-courses €47–97 (Q3 2026)
   - White-label Madeja for agencies, custom verticals, API access

### Unit Economics

| Metric | Pro only | Pro + Voice |
|--------|---------:|------------:|
| Monthly revenue | €59 | €158 |
| Monthly variable cost | €8–12 | €95–110 (voice at 300 min budget) |
| Gross margin | **~85%** | **~35%** at bundle, ~50% on overage |
| CAC | €30–50 | €30–50 |
| LTV (12-mo, 5% churn) | ~€708 | ~€1,896 |
| LTV/CAC | 14:1–24:1 | 38:1–63:1 |
| Payback | <1 month | <1 month |

### Cost Structure (Monthly Fixed)

| Item | Cost |
|------|------|
| n8n Cloud | ~€50 |
| OpenRouter (Claude API) | Variable — €0.01–0.05/call |
| OpenAI (images, GPT) | Variable — €0.05–0.50/asset |
| KIE.AI (video) | Variable — €0.10–0.30/video |
| Brevo (email, 10K/mo) | €25 |
| Google Workspace | €6 |
| Firecrawl (scraping) | €19 |
| Apify (scraping) | ~€24 |
| Stripe fees (when active) | 1.5% + €0.25/tx |
| **Total fixed** | **~€125/month** |
| **Variable per Pro client** | **~€8–12/month** |
| **Variable per Voice add-on** | **€0.14–0.20/min** (Vapi + STT + LLM + TTS + Twilio ES) + €1–6/mo number rental |

**Break-even:** 3 Pro clients (or 2 Pro + 1 Voice) covers all fixed infrastructure.

### ROI Projections

Assumes 40% of clients attach the Voice add-on → blended ARPA ~€99/month.

| Horizon | Clients | Blended ARPA | MRR | ARR | Monthly Profit | Gross Margin |
|---------|--------:|-------------:|-----:|-----:|---------------:|-------------:|
| 6 mo (conservative) | 30 | €90 | €2,700 | €32,400 | €1,900 | 70% |
| 12 mo (moderate) | 100 | €99 | €9,900 | €118,800 | €7,200 | 72% |
| 18 mo (aggressive) | 300 | €105 | €31,500 | €378,000 | €23,600 | 75% |

Assumptions: 5% monthly churn, 100% paid (no free tier), ~40% voice attach on restaurants, organic-only growth.

### Client ROI

| Capability | Without Madeja | With Madeja |
|------------|----------------|-------------|
| Daily manual review monitoring | 30 min/day owner time | Automated dashboard + PDF |
| Replying to Google reviews | 10 min per review, inconsistent tone | Auto-response in owner's tone |
| Reputation monitor (TripAdvisor, TheFork, ElTenedor) | €80–150/mo tools (Revinate/ReviewPro) | Included |
| Web booking system | €50–100/mo (OpenTable/Covermanager) | Included |
| Web chatbot for customers | €40–80/mo (Zendesk/Intercom) | Included |
| Part-time reservation staff (nights, weekends) | €800–1,500/mo | +€99 Voice add-on |
| Weekly performance report | 2 hrs manual per week or unavailable | Branded PDF, delivered Mon 9AM |
| **Total monthly value** | **€1,000–1,800+** in tools & time | **€59 (or €158 with Voice)** |

**Client payback: immediate** — first negative review auto-answered pays back the month.

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
2. **Restaurant-specialized AI** — System prompts dynamically assemble brand context, menu data, review history, and barrio competitor data before every LLM call. Vera and Milo are shaped by real Spanish restaurant operational patterns, not generic templates.
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
| Supported verticals | 1 (Restaurant) |
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

Spanish restaurant owners have three real jobs at once — cooking, running service, and running the business online. The online piece is what breaks first:

| Task | Reality Today | Cost / Consequence |
|------|---------------|--------------------|
| Monitoring reviews daily | Checked on phone during breaks, forgotten by shift's end | Late responses = lost credibility |
| Responding to Google reviews | Copy-pasted templates or nothing | Damage to rating over months |
| Cross-platform reputation (TripAdvisor, TheFork, ElTenedor) | Rarely checked | Prospective customers see stale info |
| Answering the phone during peak hours | Missed | Missed bookings = missed revenue |
| Understanding how you rank vs the barrio | Impossible without tooling | No signal, no strategy |
| Existing tools (Revinate/ReviewPro) | Enterprise pricing, English-first, no ES review platforms | Priced for hotel chains, not neighborhood restaurants |

**Result:** small-and-mid restaurants operate blind on reputation and lose bookings to the phone every night.

### Market Size

- **~15,000** restaurants in Madrid
- **~80,000** restaurants in Spain
- **~€100–200 median monthly spend** on reservation + review tools per restaurant (fragmented)
- **Whitespace:** no integrated ES-first reputation + booking + voice product exists at Madeja's price point

### Direct Competitors

| Competitor | What They Do | Madeja Advantage |
|-----------|-------------|------------------|
| **Revinate / ReviewPro** | Hospitality review intelligence | Enterprise pricing (€300+/mo), English-first, no barrio benchmarking, no ES voice agent |
| **Covermanager / OpenTable** | Restaurant booking systems | Booking only — no review ops, no AI response, no voice agent |
| **Trivec / Bookline** | Voice AI for restaurants | Voice only — no reputation stack, no dashboard, no benchmarking |
| **Google Business Profile alerts** | Free review notifications from Google | No response drafting, no cross-platform view, no benchmarking |
| **In-house junior + agency** | Manual monitoring + reply drafting | €800–1,500/mo staff + delayed responses, no 24/7 coverage |

### Indirect Competitors

| Category | Players | Why Madeja Wins |
|----------|---------|------------------|
| Automation platforms | Zapier, Make, n8n | Tools, not solutions — restaurants don't build |
| Chatbot builders | Intercom, Zendesk | Generic — no menu/booking context, no ES review integration |
| POS + booking bundles | Toast, TheFork | Booking only, no reputation ops |

### Competitive Moat

1. **Barrio benchmarking data** — 3–6 months of scraping across Madrid barrios is hard to replicate; every week our advantage widens
2. **Owner-tone auto-response** — reply drafts learn each restaurant's voice; competitors ship generic templates
3. **End-to-end integration** — reviews + bookings + voice in one system; nobody else covers all three for restaurants
4. **Spanish-first** — built for Spanish market, Spanish review platforms (TheFork, ElTenedor), Spanish restaurant culture
5. **Restaurant-specialized** — not "hospitality," not "SME general" — sharp focus on the vertical
6. **Asymmetric switching cost** — swapping means rebuilding review context, booking calendar, and voice agent

---

## 8. Go-To-Market Strategy

### Active Channels

| Channel | Strategy | Status |
|---------|----------|--------|
| **Direct sales — D2D Madrid barrios** | Founder walks target barrios with tablet demo of live dashboard | Active — primary channel |
| **Pizza Rosie live demo** | Show a prospect their neighbor's real dashboard, ask if they want theirs | Live case study |
| **LinkedIn prospecting** | Weekly automated scrape of restaurant owners in target barrios | Active |
| **Word of mouth** | Existing clients refer neighbor restaurants | Organic |

### Planned Channels (Q4 2026)

- Distribuidor partnerships (POS resellers, hospitality consultants — see Sales Playbook 90-day memory)
- Referral program — existing clients earn free months
- SEO blog on madeja.digital targeting restaurant-owner search intent
- WhatsApp Business outreach

### Sales Funnel

```
Discovery (D2D visit / LinkedIn / Referral)
    ↓
Live dashboard demo — prospect sees their real reviews, sentiment, and barrio ranking
    ↓
Onboarding (auto: sheet + scrape + GBP link + Notion CRM)
    ↓
First weekly PDF report delivered Monday 9AM — value proven within 7 days
    ↓
Optional: Voice add-on activated for restaurants with high call volume
    ↓
Retention: weekly report becomes owner ritual; switching cost compounds
```

---

## 9. Current Status & Traction

### Latest Health Check — September 14, 2026

**21/24 GREEN on the restaurant vertical.** Post platform-simplification: 71 workflows deactivated, ~31 active. Focus is restaurant ops + Bridge capstone scrapers + Lovable infra.

| Category | Status |
|----------|--------|
| Restaurant API endpoints | Green |
| Scheduled restaurant workflows | Green |
| Broken (Sep 14) | 3 — Apify credit refill + IF type-mismatch in Follow-up Sequence |

### What's Built and Working

- ~31 active workflows — restaurant vertical + Lovable infra (Stripe/checkout/auth/RGPD) + utils
- Restaurant onboarding — one call: Notion CRM + Google Sheet + website scrape + GBP link
- Full booking stack — web + SMS + optional voice (Vapi + Twilio)
- Review Intelligence — daily reputation monitor + auto-response (Vera) + weekly PDF digest
- Milo web chatbot — customer FAQ, menu, booking widget
- **Stripe deactivated pending direct-sales pipeline** — capstone / early access clients onboarded manually with full access
- **GDPR compliance** — consent, unsubscribe, data export/delete
- Error monitoring — all active workflows wired to error notification

### Development Velocity

| Period | Milestone |
|--------|-----------|
| Jan 2026 | Core platform (agents, chat, Notion CRM) |
| Feb 2026 | Lovable frontend, Stripe billing, PDF reports |
| Mar 2026 | Restaurant vertical, booking, voice agent, GDPR |
| Apr 2026 | Palomo Spain demos, cold outreach, system stabilization |
| Sep 2026 | **Pivot** — retire marketing agents, retire fashion vertical, refocus on restaurant review intelligence + booking |

**One developer built and then focused the equivalent of a 5-person engineering team's output in 8 months.**

---

## 10. Roadmap & Expansion

### Expansion Strategy

- **Horizontal (future verticals — after restaurant depth):** Restaurant (now) → Hotel → Salón / Peluquería → Clínica dental → other neighborhood service SMEs
- **Geographic:** Spain → LATAM → Portugal → Italy (Romance-language markets)
- **Product:** SaaS → White-label → API → Marketplace → Digital products

**Each new vertical reuses ~65% of existing infrastructure.**

### Product Roadmap (New Revenue Streams)

| Product | Build Time | Price | Target |
|---------|-----------|-------|--------|
| Google Review Auto-Responder | DONE | Included in Pro | All clients |
| Booking Confirmation Bot | BUILT | Included in Pro | Restaurants w/ Calendar |
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
- Shipped restaurant vertical solo (onboarding, review intelligence, voice booking, dashboard) in 8 months; pivoted focus from marketing-agent suite to review-intelligence SaaS Sep 2026
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
