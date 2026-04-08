# Repositories to Use

This project is not based on one perfect repo. It should be assembled from strong foundations.

## Core repos

### 1. browser-use/browser-use
Role:
- browser automation
- live site validation
- qualitative YouTube page inspection

Use for:
- checking competitor pages
- validating trends on real YouTube search pages
- manual-style web navigation through agent steps

Do not use as:
- the whole backend

---

### 2. langchain-ai/langgraph
Role:
- stateful agent orchestration
- multi-step research flows
- branching logic
- memory and checkpoints

Use for:
- niche analysis workflow
- scoring workflow
- transcript + trend + competitor synthesis

---

### 3. GeneralMills/pytrends
Role:
- Google Trends access layer

Use for:
- related queries
- related topics
- rising terms
- interest over time
- YouTube-oriented trend checks where relevant

Warning:
- unofficial API
- should be treated as useful but not fully guaranteed

---

### 4. jdepoix/youtube-transcript-api
Role:
- transcript and subtitles extraction

Use for:
- topic extraction
- transcript summarization
- repeated talking-point detection
- content angle clustering

Warning:
- YouTube can rate limit or change behavior

---

### 5. parafoxia/analytix
Role:
- YouTube Analytics API SDK

Use for:
- connected user’s own channel analytics
- creator dashboard
- report exports

Do not use for:
- universal competitor analytics across all channels without user auth

---

### 6. triggerdotdev/trigger.dev
Role:
- long-running jobs
- retries
- queues
- recurring scans
- alert workflows

Use for:
- scheduled niche scans
- trend refreshes
- watchlist updates
- alert generation

---

### 7. adrianhajdin/saas-template
Role:
- SaaS shell

Use for:
- auth structure
- billing structure
- dashboard layout foundation
- quick app setup

---

### 8. tremorlabs/tremor-npm
Role:
- charts and analytics components

Use for:
- KPI cards
- trend charts
- score visualizations
- watchlist analytics tables

## Reference repos

### Nayak578/Youtube-Trend-Analyzer
Useful for:
- trend-analysis product reference
- summary + prediction style reference
- layout ideas

### ShankarK2009/AI-YouTube-Trends-Finder
Useful for:
- niche trend workflow reference
- automation logic reference
- idea for short-cycle trend scraping workflow

## Final recommendation

Use this repo mix:

- SaaS shell: adrianhajdin/saas-template
- UI analytics layer: tremorlabs/tremor-npm
- agent orchestration: langchain-ai/langgraph
- browser actions: browser-use/browser-use
- jobs: triggerdotdev/trigger.dev
- trends: GeneralMills/pytrends
- transcripts: jdepoix/youtube-transcript-api
- own-channel analytics: parafoxia/analytix