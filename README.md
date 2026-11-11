# Hi, I'm Tyler Clark 👋

**Solutions Engineering | Building AI Agents & Workflows | Automation, APIs & Integrations | Strategic Tech Support Analyst | Former Sales Leader & Business Partner**

I turn business problems into working software: AI agent teams, workflows with a person in the loop, API integrations and full-stack apps, from idea to deployed product. I build hands-on with AI coding agents ([Claude Code](https://claude.com/claude-code), Cursor, Grok) and own the product and architecture decisions myself. Years in sales leadership and technical support shape how I work: find the real problem with the people who have it, translate between business and technical teams, test against real services and devices, and ship in small pull requests with automated tests.

| What I build | Where to see it |
|---|---|
| **AI agent teams** | [Benchmark](https://github.com/saltylvn/benchmark-ai): agents check every construction job each morning and draft the follow-ups; a person approves each one |
| **AI workflows with a person in the loop** | [Human-in-the-Loop Triage](https://github.com/saltylvn/human-in-the-loop-triage): Gemini, HubSpot and Slack, with approvals, evals and an audit log |
| **API integrations** | OAuth 2.0 with token refresh, HMAC-signed webhooks, Slack bots, retries with backoff, idempotent writes |
| **Full-stack apps in daily use** | [Dialed Kitchen](https://github.com/saltylvn/dialed-kitchen) and [DEVELOP](https://github.com/saltylvn/wellness-tracker): Next.js, Supabase Postgres with row-level security, Gemini |

**Try them:** [Benchmark demo](https://benchmark-qypb.onrender.com) · [Dialed Kitchen demo](https://dialed-kitchen.vercel.app) · [DEVELOP demo](https://wellness-tracker-virid.vercel.app) (no sign-up for any of them)

---

## AI agents, workflows and integrations

### [Benchmark](https://github.com/saltylvn/benchmark-ai) · [live demo](https://benchmark-qypb.onrender.com) (tap **View the demo**; the free host takes about a minute to wake)

An AI agent team for construction project managers. Every weekday at 6:00 a Coordinator agent runs 11 checks across every home, trade and PM (sub insurance, permits, long-lead orders, buyer selections, loan draws, closing dates, workload), then drafts the follow-ups: a Slack nudge, a vendor order, a construction-loan draw request to the lender. A named person approves each one in a phone-first app before anything goes out. Code computes every date and dollar; a language model may only reword, behind a guard that rejects any change to a fact.

[![Benchmark overview: the morning workflow from a weekday schedule to the Coordinator agent and its checks, drafted follow-ups behind a fact guard, human approval, then Slack, email drafts to clients and lenders, and signed webhooks to n8n; the app on iPad and iPhone; 150+ tests and 300 random-portfolio property tests](https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/benchmark-linkedin.jpg)](https://github.com/saltylvn/benchmark-ai)

<table>
  <tr>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/landing-phone.jpg" alt="Landing page on a phone"><br><sub>Landing</sub></td>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/today-phone.jpg" alt="Today: 8 things blocked and 16 follow-ups already drafted"><br><sub>Today</sub></td>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/draw-request-phone.jpg" alt="A drafted construction-loan draw request waiting for approval"><br><sub>Loan draw to approve</sub></td>
    <td width="25%" align="center"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/today-phone-dark.jpg" alt="Today in dark mode"><br><sub>Dark mode</sub></td>
  </tr>
</table>

<table>
  <tr>
    <td width="50%"><a href="https://github.com/saltylvn/benchmark-ai#readme"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/ipad-queue.jpg" alt="The approval queue on iPad in two columns"></a><br><sub><b>Approval queue:</b> Approve or Later on every drafted follow-up</sub></td>
    <td width="50%"><a href="https://github.com/saltylvn/benchmark-ai#readme"><img src="https://github.com/saltylvn/benchmark-ai/raw/main/docs/images/screens/board-desktop.jpg" alt="Where every job stands: a board by stage with status, progress and what changed since yesterday"></a><br><sub><b>Job board:</b> every home by stage, and what changed since yesterday</sub></td>
  </tr>
</table>

**Highlights:** Coordinator agent with 11 checks, written as a pure, tested function · supervisor team whose Critic rejects and retries plans · fact guard on every model rewrite · Slack bot with an audit log and two locks before any send · Google and Slack OAuth with an allowlist · bearer-token automation API · HMAC-signed webhooks with retries, plus n8n templates · GitHub Actions cron for the 8:00 brief · nonce CSP and CSRF tokens · 150+ tests, including 300 random-portfolio property tests

**Tech stack:** TypeScript · Node 20 · Python · Flask · gunicorn · Slack API · Google OAuth · n8n · HMAC webhooks · REST · GitHub Actions · CodeQL · Dependabot · Render · PWA

### [Human-in-the-Loop Triage](https://github.com/saltylvn/human-in-the-loop-triage)

An AI workflow that triages a company's contact form across Gemini, RDAP, HubSpot and Slack, and asks a person before anything risky. On 70 held-out synthetic messages it handled **84.3%** alone at **96.6%** correct, sent **4 of 4** sensitive messages to a person, and costs about **$0.33 per 1,000 messages**. It has also run live on HubSpot and Slack test accounts, including a real approval click.

<table>
  <tr>
    <td width="50%"><a href="https://github.com/saltylvn/human-in-the-loop-triage#readme"><img src="https://github.com/saltylvn/human-in-the-loop-triage/raw/main/docs/assets/workflow.png" alt="Automation workflow: receive a signed webhook, classify with Gemini, enrich, route with plain rules, act in HubSpot and Slack, and log each decision; seven rules that send a message to a person"></a><br><sub><b>Workflow:</b> the AI supplies the facts, code decides what happens</sub></td>
    <td width="50%"><a href="https://github.com/saltylvn/human-in-the-loop-triage#readme"><img src="https://github.com/saltylvn/human-in-the-loop-triage/raw/main/docs/assets/integrations-security.png" alt="Integrations: HubSpot OAuth 2.0 in six steps, a signed Slack approval click, a retry budget, and an API log of Gemini, RDAP, HubSpot and Slack calls"></a><br><sub><b>Integrations and APIs:</b> HubSpot OAuth, signed Slack approvals, retries and an API log</sub></td>
  </tr>
  <tr>
    <td width="50%"><a href="https://github.com/saltylvn/human-in-the-loop-triage#readme"><img src="https://github.com/saltylvn/human-in-the-loop-triage/raw/main/docs/assets/architecture.png" alt="Architecture: contact form webhook to a FastAPI API, a SQLite queue and log, and a Python worker that calls Gemini, RDAP, HubSpot and Slack"></a><br><sub><b>Architecture:</b> a durable queue separates fast replies from slow work</sub></td>
    <td width="50%"><a href="https://github.com/saltylvn/human-in-the-loop-triage#readme"><img src="https://github.com/saltylvn/human-in-the-loop-triage/raw/main/docs/assets/reliability.png" alt="Reliability: six failure scenarios such as duplicate webhooks, crashes and lost replies, each handled, and a retry timeline from 503 to 429 to 200"></a><br><sub><b>Reliability:</b> one record and one message, even when things fail</sub></td>
  </tr>
</table>

**Highlights:** HubSpot OAuth 2.0 with encrypted tokens · HMAC-signed webhooks and approval clicks · five layers against duplicates · append-only audit log · prompt-injection defense · 100-example eval · 83 tests, 95% coverage · Docker

**Tech stack:** Python · FastAPI · Pydantic · httpx · SQLite · Google Gemini · HubSpot API · Slack API · RDAP · Docker · uv · pytest · mypy (strict) · ruff · GitHub Actions

---

## Full-stack apps

### [Dialed Kitchen](https://github.com/saltylvn/dialed-kitchen) · [live site](https://dialed-kitchen.vercel.app) (tap **Try the demo**)

An iPhone-first grocery price book, meal planner and recipe box that a couple uses every day. It plans the week, builds the grocery list with an estimated cost, and compares prices across stores. Scan a receipt and AI logs a whole trip's prices at once.

[![Dialed Kitchen overview: an iPhone app that compares six stores, reads receipts with AI, and plans the week, with six engineering areas (multi-tenant Postgres, application security, production AI, data correctness, testing, delivery), the request flow and the tech stack](https://github.com/saltylvn/dialed-kitchen/raw/main/docs/images/dialed-kitchen-overview.png)](https://github.com/saltylvn/dialed-kitchen)

[![Four real screens: the Grocery tab with its Price book button and list, the price book comparing stores, one item's latest price at every store with its trend, and the week's meal plan with calories and this week's groceries](https://github.com/saltylvn/dialed-kitchen/raw/main/docs/images/dialed-kitchen-screens.png)](https://github.com/saltylvn/dialed-kitchen)

**Highlights:** Gemini reads receipts and recipe photos and estimates nutrition · price book compares six stores by unit price · invite-only sign-up with a waitlist, admin approval and hashed invite codes · row-level security on all 16 tables · nonce CSP and SSRF-safe link import · 422 tests, 159 against real Postgres · 48 decision records · 57 merged pull requests

**Tech stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS · Supabase (Postgres, auth, row-level security) · Google Gemini · Zod · Vitest · PGlite · Vercel · GitHub Actions · CodeQL · Dependabot

### [DEVELOP](https://github.com/saltylvn/wellness-tracker) · [live demo](https://wellness-tracker-virid.vercel.app) (no sign-up)

A wellness tracker for weight, workouts and nutrition, now on **v2.0** and in daily use. Log a meal by photo or description and AI estimates calories and macros; plan and log lifting and cardio; track weight against a goal with a projected goal date.

[![DEVELOP v2.0: the Weight, Fitness and Nutrition tabs on iPhone, with 339 automated tests, 16 of 16 tables with row-level security, and about 2 second AI photo estimates](https://github.com/saltylvn/wellness-tracker/raw/main/docs/linkedin/DEVELOP-project-cover-4x3.png)](https://github.com/saltylvn/wellness-tracker)

<table>
  <tr>
    <td width="33%" align="center"><img src="https://github.com/saltylvn/wellness-tracker/raw/main/docs/screens/weight.png" alt="Weight tab: start, current and target weight with a progress bar, a weigh-in chart and the projected goal date"><br><sub>Weight</sub></td>
    <td width="33%" align="center"><img src="https://github.com/saltylvn/wellness-tracker/raw/main/docs/screens/fitness.png" alt="Fitness tab on a lifting day: two priority lifts with PRs and the day's exercises with logged sets"><br><sub>Fitness</sub></td>
    <td width="33%" align="center"><img src="https://github.com/saltylvn/wellness-tracker/raw/main/docs/screens/nutrition.png" alt="Nutrition tab: food streak, week strip, calorie ring and macro goals"><br><sub>Nutrition</sub></td>
  </tr>
</table>

[![DEVELOP architecture: iPhone PWA to Next.js on Vercel (proxy with a nonce CSP, Server Components and Server Actions, an AI route) to Supabase Postgres and Auth and Google Gemini, with CI, preview deploys, protected main and Dependabot](https://github.com/saltylvn/wellness-tracker/raw/main/docs/linkedin/DEVELOP-architecture.png)](https://github.com/saltylvn/wellness-tracker#how-its-built)

**Highlights:** AI photo estimates in about 2 seconds (down from 12.5 s) by racing models · Google or username and password sign-in, invite-only, with an admin view · row-level security on all 16 tables (28 policies) · strict CSP · 339 tests, including database rules on real Postgres · protected `main` · one-click demo

**Tech stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS · Supabase (Postgres, auth, row-level security) · Google Gemini · ZXing · Vitest · Vercel · GitHub Actions · CodeQL · Dependabot

---

## In progress

- **PM Bot** (private for now): a PM Bot orchestrator and six specialist agents for an IT delivery team, with n8n connecting Slack, Jira, ServiceNow, GitHub and Google Workspace.

---

## All tools

**AI coding agents:** Claude Code · Cursor · Grok

**Agent design:** multi-agent orchestration (supervisor, critic, specialists) · human approval gates · fact guards · property-based evals

**AI and automation:** Python · FastAPI · Flask · TypeScript · Node · Google Gemini · OpenAI · n8n · LLM evals · prompt-injection defense

**APIs and integrations:** HubSpot · Slack · GitHub · Google OAuth · OAuth 2.0 · RDAP · REST · HMAC-signed webhooks

**Full-stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS · Supabase (Postgres, auth, row-level security) · Zod · Vitest

**Delivery:** GitHub Actions · CodeQL · Dependabot · Docker · Vercel · Render · gunicorn

**Diagrams and docs:** Mermaid · SVG diagrams · architecture decision records
