---

# 2) `docs/STACK.md`

```md
# Stack

## Recommended production stack

### Frontend
- Next.js
- TypeScript
- Tailwind CSS
- Tremor for charts and KPI cards

### Auth / User / Billing
- Clerk
- Supabase
- Stripe or Clerk billing flow depending on final setup

### Backend
Two valid paths:

#### Path A — TypeScript-first
- Next.js API routes / server actions
- Trigger.dev for long-running jobs
- LangGraph.js if you want JS agent orchestration

#### Path B — Hybrid
- Next.js frontend
- Python services for agent and analysis layer
- LangGraph Python
- Trigger.dev or queue worker to schedule jobs

## My recommendation

For this product, the strongest version is:

- Next.js frontend
- Supabase database
- Trigger.dev for jobs
- Python microservice for trend analysis and agent logic
- LangGraph for multi-step workflow orchestration

That gives cleaner separation between UI and analysis.

## Core data sources

### Required
- YouTube Data API
- Google Trends / pytrends
- youtube-transcript-api

### Optional later
- YouTube Analytics API for a user’s own connected channel
- browser-use for live page validation
- official Google Trends API where practical

## Libraries and roles

### UI
- Tremor: charts, dashboard cards, simple analytics layout
- shadcn/ui or custom components for forms and app shell

### Data / analysis
- pytrends: related queries, related topics, rising signals
- youtube-transcript-api: transcript fetch and topic extraction
- analytix: own-channel analytics for connected creator accounts

### Agent layer
- LangGraph: stateful analysis workflows
- browser-use: live YouTube inspection and qualitative validation

### Job orchestration
- Trigger.dev: recurring scans, retries, alerts, long-running jobs

## Database tables to expect

- users
- searches
- niches
- niche_scores
- tracked_channels
- tracked_keywords
- video_snapshots
- transcript_snapshots
- trend_snapshots
- alerts
- watchlists
- generated_ideas

## Deployment

### Frontend
- Vercel or similar

### Background / agent layer
- Trigger.dev cloud or self-hosted jobs
- Python service on Railway, Fly.io, Render, or Cloud Run

### Database
- Supabase Postgres

## Why this stack

This product needs:
- dashboard UI
- recurring scans
- structured scoring
- transcript processing
- stateful multi-step research
- future alerting

So it should be built as a **SaaS analytics app with an agent layer**, not as a pure browser bot.