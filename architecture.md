# Architecture

## Product shape

This should be built as:

**SaaS dashboard + analysis backend + agent orchestration layer**

Not as:
- only a browser bot
- only a scraper
- only an LLM wrapper

## High-level architecture

```text
User
  ↓
Next.js App
  ↓
API / App Backend
  ↓
Analysis Services
  ├─ YouTube Data API
  ├─ Google Trends / pytrends
  ├─ youtube-transcript-api
  ├─ browser-use
  └─ LLM / LangGraph
  ↓
Scoring + Summaries
  ↓
Supabase DB
  ↓
Dashboard / Watchlists / Alerts