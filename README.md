# Hi, I'm Eddie

Self-taught software engineer in Nairobi, building backends, full-stack products and cloud services. I run [The EWN](https://theewn.com), a small consulting studio doing custom software, AI integrations and architecture work for clients in the EU and Middle East.

My background is in mechanical engineering, which mostly shows up as a habit of drawing the system before building it.

**Usually working in:** Python (FastAPI) · Go (Gin) · TypeScript (React, Next.js) · MongoDB · Redis · Docker · AWS

---

## Featured projects

### [Nifty by Paragon](https://github.com/eddie-wainaina1/paragon)
Multi-tenant ed-tech platform for schools. Organizations register, admins manage users and classes, teachers publish content, students work through it.

- FastAPI + MongoEngine backend with role-based access across platform and organization roles
- Paystack subscriptions, SendGrid transactional email with HTML templates, ffmpeg video transcoding
- OpenTelemetry tracing for FastAPI, PyMongo and Redis
- Versioned data migrations, Redis caching and rate limiting
- Ships as separate containers via docker-compose, or a single image with nginx + uvicorn under supervisord

`React` `FastAPI` `MongoDB` `Redis` `Docker` `OpenTelemetry`

### [eblog](https://github.com/eddie-wainaina1/eblog)
Blog platform where an AI agent drafts the posts and a human decides what ships. A daily cron reads Google Trends, Claude writes a full draft, and it lands in an admin queue as `pending` until someone approves it.

- Next.js App Router, custom JWT auth, Markdown authoring with an admin dashboard
- SEO built in: OG/Twitter meta, JSON-LD, generated sitemap
- Deployed on Vercel with scheduled generation

`Next.js` `MongoDB` `Claude API` `Vercel`

### Maggie: e-commerce with M-Pesa payments
[Storefront](https://github.com/eddie-wainaina1/Maggie) · [API](https://github.com/eddie-wainaina1/maggiesb)

An online shop built end to end: a Next.js storefront and admin dashboard on the front, a Go API handling orders and money on the back.

**Storefront (Next.js)**
- Marketplace, cart, orders, and an admin dashboard for products, users and roles
- Clerk auth with role-based admin views, Redis-backed caching
- Product images stored in GridFS with AES-256 encryption at rest, served through signed URLs, plus a migration script that encrypted the existing images

**API (Go)**
- JWT auth with role-based middleware covering products, orders, invoices, payment reversals and reports
- M-Pesa STK push integration with callback handling (payment flow documented in the repo)
- Repository pattern over MongoDB with mocked collections; 20+ test files across handlers, auth and data layers

`Next.js` `React 19` `Go` `Gin` `MongoDB` `Redis` `M-Pesa` `Clerk`

---

## Private and client work

Most of what I build lives in private repos. Code isn't public, but here's what it does.

**Document-to-PDF conversion service (AWS Lambda)**
Converts Office documents to PDF using LibreOffice inside a Lambda container image. Started life as a FastAPI service on EC2 and was rearchitected for Lambda. Fonts are vendored into the image so builds don't depend on flaky downloads, converter logic is kept separate from the handler's I/O, and S3 object tags (not metadata) mark processed files so the trigger can't loop on its own output.
`Python` `AWS Lambda` `S3` `Docker` `LibreOffice`

**Algorithmic trading tools (MQL5 / Pine Script)**
Expert Advisors for MetaTrader 5 trading XAUUSD. One is a breakout scalper that detects ranges and flags and places stops at the structure boundary. Another is a smoothed Heiken Ashi strategy with trend, session and ATR filters, equity-based position sizing and a companion indicator. Prototyped in Pine Script, backtested, and iterated on drawdown rather than headline win rate.
`MQL5` `Pine Script`

<!-- TODO: add client projects here. Suggested format:
**Project name (client type, e.g. "EU fintech")**
One or two sentences on the problem and what you built. Name the hard part.
`Stack` `Tags`
-->

## Collaborations

<!-- TODO: list team or contributed repos here. Example:
**[org/repo](link)**: what the project is, and what you specifically owned (e.g. "built the vendor filtering and selection hooks used across the procurement UI").
-->

---

## Get in touch

[theewn.com](https://theewn.com) · <!-- TODO: LinkedIn URL --> · <!-- TODO: preferred contact email -->
