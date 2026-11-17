# Hi, I'm Tyler Clark 👋

**AI Solutions Engineer | Multi-Agent Orchestration · MCP & API Integrations · Workflow Automation | Shipping with Claude Code | Sales Veteran 10 Yrs**

I spent 10 years in sales, 7 of them leading teams, so I know where a business loses hours to manual work. Now I build the AI systems that take that work away: multi-agent systems where specialist agents report to a supervisor, integrations that plug agents into the tools a team already uses (Slack, HubSpot, Gmail, Google, Notion, Postgres), and automations backed by SQL and a real data model, built to save measurable time. A person stays in control of anything that matters.

What I bring that most builders don't: a decade across the table from customers and executives. I scope the real problem before I build, and I can explain the solution to the people who sign off on it.

I ship everything with [Claude Code](https://claude.com/claude-code) as my daily workflow (plus Cursor and Grok), and I own the product, architecture and security decisions myself.

| At a glance | |
|---|---|
| **Shipped and public** | 4 production projects, 3 with live demos, 2 in daily use by real people |
| **Engineering volume** | 200+ merged pull requests and 1,000+ automated tests across the public repos, CI on every change |
| **AI in production** | Multi-agent orchestration (supervisor and specialists, a critic loop), evals that gate CI, run tracing, held-out test sets, fact guards, prompt-injection defense, model racing and fallbacks |
| **Integrations built** | HubSpot (OAuth 2.0), Slack (bot and signed approvals), Gmail, Google Calendar and Google OAuth, Notion, GitHub, Figma, Gemini, Claude, OpenAI, RDAP, RSS, n8n, signed webhooks, REST APIs, and MCP servers in my daily workflow |
| **Data and security** | Postgres row-level security tested against a real database, least-privilege database roles, nonce CSP, SSRF-safe fetching, audit logs |

**Try them:** [Benchmark](https://benchmark-qypb.onrender.com) · [Dialed Kitchen](https://dialed-kitchen.vercel.app) · [DEVELOP](https://wellness-tracker-virid.vercel.app) (each has a one-tap demo, no sign-up)

---

## Roles I'm built for

| Role (also called) | What I bring | See it in |
|---|---|---|
| **AI Engineer** (Applied AI, LLM Engineer) | Production AI features with structured output, validation, evals and cost limits | [Handoff Triage](https://github.com/saltylvn/handoff-triage), [DEVELOP](https://github.com/saltylvn/wellness-tracker) |
| **AI + Automation Engineer** (Internal AI Engineer) | Automations that save measurable time, backed by SQL and a real data model | [Benchmark](https://github.com/saltylvn/benchmark-ai), [Dialed Kitchen](https://github.com/saltylvn/dialed-kitchen) |
| **AI Workflow Engineer** (AI Agent Engineer, Agentic AI Engineer) | Supervisor and specialist agents with approval gates, guards and traces | [Benchmark](https://github.com/saltylvn/benchmark-ai), Atlas (private) |
| **Software Engineer** (Full-stack, Product Engineer) | Next.js, TypeScript, Python and Postgres apps in daily use, with 1,000+ tests and CI on every change | [Dialed Kitchen](https://github.com/saltylvn/dialed-kitchen), [DEVELOP](https://github.com/saltylvn/wellness-tracker) |
| **Forward Deployed Engineer** (Agent Deployment Engineer) | Scoping a customer's real problem, then building and deploying the agent into their tools | [Benchmark](https://github.com/saltylvn/benchmark-ai), [Handoff Triage](https://github.com/saltylvn/handoff-triage) |
| **Solutions Engineer** (AI Solutions, Implementation) | 10 years with customers and executives, plus the integrations to back it up: OAuth, webhooks, CRM and Slack | [Handoff Triage](https://github.com/saltylvn/handoff-triage) |
| **GTM Engineer** (Revenue / RevOps Engineer) | CRM automation, enrichment and routing with a person approving the risky calls | [Handoff Triage](https://github.com/saltylvn/handoff-triage) (HubSpot, RDAP, Slack) |

---

## For engineers: where to look in the code

| What you want to judge | Read this |
|---|---|
| Agent design: one pure, tested function that runs 11 checks | [benchmark-ai/src/agents/coordinator.ts](https://github.com/saltylvn/benchmark-ai/blob/main/src/agents/coordinator.ts) |
| Supervisor, specialists and a Critic that rejects and retries plans | [benchmark-ai/src/orchestrator/supervisor.ts](https://github.com/saltylvn/benchmark-ai/blob/main/src/orchestrator/supervisor.ts) |
| A guard that stops a model from changing any fact in a draft | [benchmark-ai/src/providers/guard.ts](https://github.com/saltylvn/benchmark-ai/blob/main/src/providers/guard.ts) |
| Property tests on 300 random portfolios (they found two real bugs) | [benchmark-ai/tests/coordinator.properties.test.ts](https://github.com/saltylvn/benchmark-ai/blob/main/tests/coordinator.properties.test.ts) |
| OAuth 2.0 with token refresh and encrypted tokens | [handoff-triage/src/triage/adapters/hubspot.py](https://github.com/saltylvn/handoff-triage/blob/main/src/triage/adapters/hubspot.py) |
| HMAC-signed webhooks and approval clicks | [handoff-triage/src/triage/infra/signature.py](https://github.com/saltylvn/handoff-triage/blob/main/src/triage/infra/signature.py) |
| Idempotency and crash recovery in five layers | [handoff-triage/src/triage/pipeline.py](https://github.com/saltylvn/handoff-triage/blob/main/src/triage/pipeline.py) · [decision 0003](https://github.com/saltylvn/handoff-triage/blob/main/docs/decisions/0003-layered-idempotency.md) |
| Retries, backoff and rate limits | [handoff-triage/src/triage/infra/retry.py](https://github.com/saltylvn/handoff-triage/blob/main/src/triage/infra/retry.py) |
| Multi-tenant Postgres: row-level security, composite foreign keys, hashed invite tokens | [dialed-kitchen/supabase/migrations/…_households.sql](https://github.com/saltylvn/dialed-kitchen/blob/main/supabase/migrations/20261023000000_households.sql) |
| Tests that sign in as different users on real Postgres and try to break isolation | [dialed-kitchen/supabase/tests](https://github.com/saltylvn/dialed-kitchen/tree/main/supabase/tests) |
| SSRF-safe fetching, with the address check inside the DNS lookup | [dialed-kitchen/lib/server/safeFetch.ts](https://github.com/saltylvn/dialed-kitchen/blob/main/lib/server/safeFetch.ts) |
| Structured AI output: JSON schema, Zod validation, injection-aware prompt | [dialed-kitchen/lib/ai/receiptFromImage.ts](https://github.com/saltylvn/dialed-kitchen/blob/main/lib/ai/receiptFromImage.ts) |
| Hedged model racing that took AI replies from 12.5 s to about 2 s | [wellness-tracker/lib/ai/modelChain.ts](https://github.com/saltylvn/wellness-tracker/blob/main/lib/ai/modelChain.ts) |
| Least-privilege database logins for an agent (one function each) | [wellness-tracker/supabase/migrations/…_coach_access.sql](https://github.com/saltylvn/wellness-tracker/blob/main/supabase/migrations/20261116000000_coach_access.sql) |

---

## AI agents and workflows

### [Benchmark](https://github.com/saltylvn/benchmark-ai) · [live demo](https://benchmark-qypb.onrender.com)

**An AI agent team for construction project managers.** Every weekday at 6:00 a Coordinator agent runs 11 checks across every job, trade and PM (sub insurance, permits, long-lead orders, buyer selections, loan draws, closing dates, workload) and drafts the follow-ups: a Slack nudge, a vendor order, a construction-loan draw request to the lender. A named person approves each one in a phone-first app before anything goes out. Code computes every date and dollar; a language model may only reword, behind a guard that rejects any change to a fact.

[![Benchmark overview: sources, TypeScript agents (Coordinator with 11 checks, supervisor team, critic), a versioned snapshot and fact guard, the Flask service with its approval queue, REST API and security, then a named PM approves before Slack, email drafts and signed webhooks; the app on iPad and iPhone; 157 tests and 300 property-test portfolios](https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/benchmark-linkedin.jpg)](https://github.com/saltylvn/benchmark-ai)

<table>
  <tr>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/today-phone.jpg" alt="Today: 8 things blocked and 16 follow-ups already drafted"><br><sub>Today</sub></td>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/draw-request-phone.jpg" alt="A drafted construction-loan draw request waiting for approval"><br><sub>Loan draw to approve</sub></td>
    <td width="50%" align="center"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/ipad-queue.jpg" alt="The approval queue on iPad in two columns"><br><sub>Approval queue on iPad</sub></td>
  </tr>
</table>

- **Architecture:** two layers on purpose. TypeScript agents decide and export one versioned snapshot; a Python Flask service reads it and handles people, sign-in, approvals and integrations. A drift test fails if the UI could show a plan the agents didn't make.
- **Integrations:** Slack bot with an audit log and two locks before any send · Google and Slack OAuth with an email allowlist · bearer-token automation API · HMAC-signed webhooks with retries and a delivery log · n8n templates that verify the signature · GitHub Actions cron for the 8:00 brief · deployed on Render.
- **Quality:** 157 tests in TypeScript and Python, 300 random-portfolio property tests, nonce CSP and CSRF tokens, CodeQL and dependency audits in CI.

`TypeScript` `Node 20` `Python` `Flask` `gunicorn` `Slack API` `Google OAuth` `OpenAI (optional)` `n8n` `HMAC webhooks` `GitHub Actions` `Render` `PWA`

### [Handoff Triage](https://github.com/saltylvn/handoff-triage)

**A human-in-the-loop workflow that triages a company's contact form across four systems.** Gemini reads each message, RDAP enriches it, HubSpot and Slack get updated, and anything unsure or risky waits for a person. On 70 held-out messages it handled **84.3%** without a person at **96.6%** correct, sent **all 4** sensitive messages to a person, and costs about **$0.33 per 1,000 messages**. It has also run live on HubSpot and Slack test accounts, including a real approval click. It is one LLM step inside a deterministic workflow, on purpose: fixed steps are easier to test, audit and trust.

[![Handoff Triage connected to Gemini, RDAP, HubSpot and Slack, with its six workflow steps, results on 70 held-out messages, a pending Slack approval and the tools it is built with](https://github.com/saltylvn/handoff-triage/raw/main/docs/assets/overview.png)](https://github.com/saltylvn/handoff-triage)

<table>
  <tr>
    <td width="50%"><a href="https://github.com/saltylvn/handoff-triage#readme"><img src="https://github.com/saltylvn/handoff-triage/raw/main/docs/assets/integrations-security.png" alt="Integrations: HubSpot OAuth 2.0 in six steps, a signed Slack approval click, a retry budget, and an API log of Gemini, RDAP, HubSpot and Slack calls"></a><br><sub><b>Integrations:</b> HubSpot OAuth, signed Slack approvals, retries and an API log</sub></td>
    <td width="50%"><a href="https://github.com/saltylvn/handoff-triage#readme"><img src="https://github.com/saltylvn/handoff-triage/raw/main/docs/assets/reliability.png" alt="Reliability: six failure scenarios such as duplicate webhooks, crashes and lost replies, each handled, and a retry timeline from 503 to 429 to 200"></a><br><sub><b>Reliability:</b> one record and one message, even when things fail</sub></td>
  </tr>
</table>

- **Reliability:** a durable SQLite queue separates fast webhook replies from slow work · five layers against duplicates · retries with backoff that respect rate limits · a one-command failure demo that injects a rate limit, a lost reply, a replayed webhook and a double-clicked approval.
- **Safety and audit:** HubSpot tokens encrypted at rest · signed webhooks and approval clicks · append-only audit log · LLM output validation and prompt-injection defense · a $250,000 deal is held for approval even at full model confidence.
- **Quality:** 100-example eval with held-out results · 83 tests at 95% coverage · strict mypy · Docker with a start-up test in CI.

`Python 3.13` `FastAPI` `Pydantic` `httpx` `SQLite` `Google Gemini` `HubSpot API` `Slack API` `RDAP` `Docker` `uv` `pytest` `mypy (strict)` `ruff` `GitHub Actions`

---

## Full-stack apps in daily use

### [DEVELOP](https://github.com/saltylvn/wellness-tracker) · [live demo](https://wellness-tracker-virid.vercel.app)

**A wellness tracker for weight, workouts and nutrition, with an AI coach agent running on a Raspberry Pi 5 at home.** Log a meal by photo or description and Gemini estimates calories and macros; plan and log lifting and cardio; track weight against a goal. Every morning the Pi agent writes a coaching note, and twice a week it recommends workouts with links from seven allowlisted fitness publishers.

[![DEVELOP in dark mode: the Weight tab, the Coach window and the Fitness tab on iPhone, with the live demo and repository links, four proof numbers and the tech stack, including the Raspberry Pi agent](https://github.com/saltylvn/wellness-tracker/raw/main/docs/linkedin/DEVELOP-project-cover-4x3.png)](https://github.com/saltylvn/wellness-tracker)

<table>
  <tr>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/wellness-tracker/raw/main/docs/screens/weight.png" alt="Weight tab: start, current and target weight with a progress bar, a weigh-in chart and the projected goal date"><br><sub>Weight</sub></td>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/wellness-tracker/raw/main/docs/screens/fitness.png" alt="Fitness tab on a lifting day: two priority lifts with PRs and the day's exercises with logged sets"><br><sub>Fitness</sub></td>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/wellness-tracker/raw/main/docs/screens/coach.png" alt="The Coach window: today's note with yesterday vs plan, the week so far, today's focus and thumbs up or down"><br><sub>AI coach</sub></td>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/wellness-tracker/raw/main/docs/screens/nutrition.png" alt="Nutrition tab: food streak, week strip, calorie ring and macro goals"><br><sub>Nutrition</sub></td>
  </tr>
</table>

[![DEVELOP architecture: the app (iPhone PWA to Next.js on Vercel with a per-request CSP nonce, Server Components, Server Actions and an AI route, to Supabase Postgres and Auth, and Gemini) and the coach agent (a Raspberry Pi 5 running Python on systemd timers, stats in code, Gemini and a checker, two single-function database logins); CI on both](https://github.com/saltylvn/wellness-tracker/raw/main/docs/linkedin/DEVELOP-architecture.png)](https://github.com/saltylvn/wellness-tracker#how-its-built)

- **The coach agent:** code computes every number and the model only writes the words; a checker rejects any note with a number the code didn't produce, medical advice, links or markup. The model picks articles by number and code inserts the real links, so it never writes a URL. Two database logins that can each call exactly one function, a privacy filter that sends only weekly totals, and a sandboxed systemd service on a hardened Pi (key-only SSH, LAN-only firewall).
- **AI in the app:** photo and text nutrition estimates with JSON-schema output; hedged model racing took replies from **12.5 s to about 2 s**; a 40-a-day per-person limit taken atomically in Postgres.
- **Data and security:** row-level security on all 18 tables, 33 versioned migrations written to deploy safely, invite-only sign-up enforced by a Postgres trigger, Google sign-in with PKCE, strict nonce CSP, protected `main`, Actions pinned to commit SHAs.
- **Quality:** 421 tests, including every database rule on a real Postgres (PGlite), and a performance test that fails if a page needs more than two database round trips. 100+ merged pull requests.

`Next.js 16` `React 19` `TypeScript` `Tailwind CSS v4` `Supabase (Postgres, Auth, RLS)` `Google Gemini` `Python 3.13` `systemd` `Raspberry Pi 5` `Vitest` `PGlite` `pytest` `Vercel` `GitHub Actions` `CodeQL` `Dependabot`

### [Dialed Kitchen](https://github.com/saltylvn/dialed-kitchen) · [live demo](https://dialed-kitchen.vercel.app)

**An iPhone-first grocery price book, meal planner and recipe box that my household uses every day.** It plans the week, builds the grocery list with an estimated cost, and compares prices across six stores by unit price. Scan a receipt and Gemini logs a whole trip's prices at once, after you review them.

[![Dialed Kitchen overview: an iPhone app that compares six stores, reads receipts with AI, and plans the week, with six engineering areas (multi-tenant Postgres, application security, production AI, data correctness, testing, delivery), the request flow and the tech stack](https://github.com/saltylvn/dialed-kitchen/raw/main/docs/images/dialed-kitchen-overview.png)](https://github.com/saltylvn/dialed-kitchen)

[![Four real screens: the Grocery tab with its Price book button and list, the price book comparing stores, one item's latest price at every store with its trend, and the week's meal plan with calories and this week's groceries](https://github.com/saltylvn/dialed-kitchen/raw/main/docs/images/dialed-kitchen-screens.png)](https://github.com/saltylvn/dialed-kitchen)

- **Multi-tenant Postgres:** households with row-level security on all 16 tables, composite foreign keys so rows can't point at another household, column-level grants and 60+ check constraints. Prices and best prices are computed from history, never stored.
- **Security:** invite-only sign-up with a waitlist, admin approval and invite codes stored only as SHA-256 hashes; SSRF-safe recipe import that closes DNS rebinding; nonce CSP; CodeQL and secret scanning.
- **Production AI:** receipts and recipe photos read by Gemini with a JSON schema, every reply validated with Zod, a free-model fallback chain, and photos stripped of GPS data and never stored.
- **Quality:** 422 tests, 159 of them on real Postgres signing in as different users · WCAG AA contrast enforced by a test · 48 architecture decision records · 60 merged pull requests.

`Next.js 16` `React 19` `TypeScript (strict)` `Tailwind CSS v4` `Supabase (Postgres, Auth, RLS)` `Google Gemini` `Zod` `Vitest` `PGlite` `Vercel` `GitHub Actions` `CodeQL` `Dependabot`

---

## Private work (happy to walk through it)

- **Atlas:** a personal chief of staff run by a team of agents with one job each, in a supervisor (hierarchical) pattern: a Chief of Staff routes work to eight specialists that brief me twice a day, sort Gmail by rules (headers only), plan the week, track renewals and condense the news. Each agent has its own eval suite (nine in all), and CI fails the build if any suite drops below its threshold; every run leaves a step-by-step trace. **Ask Atlas** is a RAG feature with hybrid search (Postgres full-text plus pgvector embeddings, fused) where Claude answers only from the retrieved passages, with sources. A laptop Mission Control shows every agent's status, cost, errors and a live map of the orchestration. Nothing leaves without me: drafts open in my own Mail or Messages app. Connected to Gmail, Google Calendar, Notion, GitHub, Figma and RSS feeds. Next.js, Supabase, pgvector, Claude, Gemini, web push, Siri capture, Vercel. 60 merged pull requests.
- **Raspberry Pi 5 home server:** Pi-hole ad blocking plus the DEVELOP coach agent above. Swappable LLM interface, six eval scenarios including a prompt-injection attempt (first-try pass rate from 50% to 100% over four rounds), 89 tests, and a systemd sandbox that scores 1.1 on `systemd-analyze security`.

---

## How I work

- **Code decides, models phrase.** Dates, dollars, routing and permissions are deterministic and tested; a model writes or classifies inside guard rails, and its output is validated like any other untrusted input.
- **Agents draft, a person approves.** My agent systems never send on their own: outbound actions wait in an approval queue and land in an audit trail.
- **Measure it.** Evals that gate CI, held-out test sets, property tests, run traces, latency numbers and cost per message, reported with their caveats.
- **Scope with numbers.** Start from a vague business problem, agree what success looks like (hours saved, steps removed, cost per run), then build to that.
- **Rules live where they can't be bypassed.** Row-level security, triggers and single-purpose database roles, tested against a real Postgres.
- **Ship small and documented.** A branch and pull request per change, CI that blocks merging, preview deploys, decision records, and a living spec (`CLAUDE.md`) updated in the same pull request as the code.

---

## Skills

**AI engineering:** multi-agent orchestration (supervisor, critic, specialists) · human-in-the-loop approvals · RAG (hybrid full-text and pgvector search) · structured output with JSON schema · evals and observability (CI-gated eval suites, run traces) · property-based testing · fact guards and output checkers · prompt-injection defense · model racing and fallbacks · Google Gemini · Claude · OpenAI

**Integrations and APIs:** MCP · HubSpot · Slack (bot, interactivity, webhooks) · Gmail · Google Calendar · Google OAuth (PKCE) · Notion · GitHub · Figma · OAuth 2.0 with token refresh · HMAC-signed webhooks · REST APIs · bearer-token automation APIs · RDAP · RSS · n8n

**Back end and data:** Python · FastAPI · Flask · Pydantic · TypeScript · Node · PostgreSQL (row-level security, triggers, `SECURITY DEFINER` functions, migrations) · Supabase · SQLite · pgvector

**Front end:** Next.js 16 · React 19 (Server Components, Server Actions) · Tailwind CSS · installable PWAs for iPhone, iPad and desktop

**Security:** nonce-based CSP · CSRF protection · SSRF-safe fetching · least-privilege database roles · encrypted tokens · secret scanning · host hardening (systemd sandboxing, SSH, firewall)

**Delivery:** GitHub Actions · CodeQL · Dependabot · Docker · Vercel · Render · Raspberry Pi and systemd · Vitest · pytest · mypy (strict) · ruff · ESLint

**Shipping with AI coding agents:** Claude Code (daily) · Cursor · Grok
