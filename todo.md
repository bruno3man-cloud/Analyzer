# TODO

## Phase 1 — Repository and app shell
- [ ] Add basic README and docs
- [ ] Choose frontend base
- [ ] Set up Next.js app
- [ ] Set up Tailwind
- [ ] Set up Tremor
- [ ] Set up auth
- [ ] Set up Supabase
- [ ] Add dashboard shell

## Phase 2 — Core data connections
- [ ] Connect YouTube Data API
- [ ] Build basic keyword search
- [ ] Build recent video fetch flow
- [ ] Build basic channel fetch flow
- [ ] Connect pytrends
- [ ] Add related queries fetch
- [ ] Add related topics fetch
- [ ] Add interest-over-time checks
- [ ] Connect youtube-transcript-api
- [ ] Store transcript snapshots

## Phase 3 — Analysis engine
- [ ] Create niche expansion service
- [ ] Create competitor snapshot service
- [ ] Create transcript theme extractor
- [ ] Create trend signal normalizer
- [ ] Create first scoring formula
- [ ] Create AI explanation generator
- [ ] Create idea generation output

## Phase 4 — Product pages
- [ ] Dashboard page
- [ ] Niche Finder page
- [ ] Trend Radar page
- [ ] Competitor Analyzer page
- [ ] Idea Lab page
- [ ] Watchlists page

## Phase 5 — Persistence
- [ ] Save searches
- [ ] Save results
- [ ] Save tracked keywords
- [ ] Save tracked channels
- [ ] Save niche scores
- [ ] Save generated ideas

## Phase 6 — Jobs and alerts
- [ ] Add Trigger.dev
- [ ] Create scheduled niche refresh job
- [ ] Create watchlist refresh job
- [ ] Create alert generation job
- [ ] Create stale-data refresh job

## Phase 7 — Agent layer
- [ ] Add LangGraph workflow
- [ ] Build niche analysis graph
- [ ] Build transcript + trend synthesis step
- [ ] Build competitor reasoning step
- [ ] Build final recommendation step

## Phase 8 — Browser validation
- [ ] Add browser-use
- [ ] Validate live YouTube search pages
- [ ] Validate competitor channel pages
- [ ] Add optional qualitative enrichment step

## Phase 9 — Polish
- [ ] Improve scoring explanations
- [ ] Add empty states
- [ ] Add loading states
- [ ] Add export options
- [ ] Add pricing page
- [ ] Add onboarding

## First implementation order

Build in this order:

1. app shell
2. niche input
3. YouTube ingest
4. trends enrichment
5. transcript enrichment
6. scoring
7. summary + ideas
8. save results
9. watchlists
10. recurring jobs

## Rule for scope

If a feature does not directly improve:
- niche discovery
- trend detection
- competitor clarity
- content idea quality

do not add it to MVP.