# Hi, I'm Tyler Clark 👋

**Solutions Engineering | Building AI Agents & Workflows | Automation, APIs & Integrations | Strategic Tech Support Analyst | Former Sales Leader & Business Partner**

I turn business problems into working solutions: AI agents and workflows, automations, API integrations and full-stack apps, from idea to working product. I work hands-on with AI agents such as [Claude Code](https://claude.com/claude-code), Cursor and Grok, choosing the right one for each job while I own the product decisions. My background in sales leadership and technical support shapes how I build: I work with teams and stakeholders to understand the real problem, translate between business and technical needs, test with real services and devices, and ship in small pull requests with automated tests.

| What I build | Where to see it |
|---|---|
| **AI workflows with a person in the loop** | [Human-in-the-Loop Triage](https://github.com/saltylvn/human-in-the-loop-triage): Gemini, HubSpot and Slack, with approvals, evals and an audit log |
| **API integrations** | OAuth 2.0 with token refresh, signed webhooks, retries with backoff, idempotent writes |
| **Full-stack apps in daily use** | [Dialed Kitchen](https://github.com/saltylvn/dialed-kitchen) and [DEVELOP](https://github.com/saltylvn/wellness-tracker): Next.js, Supabase Postgres with row-level security, Gemini |
| **Solution design** | [PM Bot](https://github.com/saltylvn/PMbot): agents, n8n automations and integrations for an IT delivery team |

---

## Workflows, integrations and APIs

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

## Solution design

### [PM Bot and the Solution Delivery Cockpit](https://github.com/saltylvn/PMbot)

A solution design for an IT delivery team: a PM Bot orchestrator and six specialist agents on a Next.js and Supabase cockpit, with **n8n** as the automation layer connecting Slack, Jira, ServiceNow, GitHub and Google Workspace. People keep the decisions that change scope, money, dates or a cutover. The package has 15 workflow and architecture diagrams, written as code in Mermaid, and a time-saved model.

[![Integration ecosystem: the Solution Delivery Cockpit connected to the n8n automation layer, Slack, Jira, ServiceNow, GitHub, Google Calendar, Gmail and Sheets, a language model and Supabase](https://github.com/saltylvn/PMbot/raw/main/assets/png/10-integration-ecosystem.png)](https://github.com/saltylvn/PMbot)

<table>
  <tr>
    <td width="50%"><a href="https://github.com/saltylvn/PMbot"><img src="https://github.com/saltylvn/PMbot/raw/main/assets/png/01-agent-map.png" alt="Agent map: PM Bot orchestrating intake, planning, risk, cutover, status and copilot agents, with human-in-the-loop handoffs"></a><br><sub><b>Agent map:</b> six agents and four human handoffs</sub></td>
    <td width="50%"><a href="https://github.com/saltylvn/PMbot"><img src="https://github.com/saltylvn/PMbot/raw/main/assets/charts/time-saved-weekly-by-automation.png" alt="Estimated staff time saved per week by automation, about 22 hours a week for the squad, an illustrative estimate"></a><br><sub><b>Time saved:</b> about 22 staff-hours a week (illustrative estimate)</sub></td>
  </tr>
</table>

**Tech stack:** n8n · Mermaid · Python (matplotlib) · Slack · Jira · ServiceNow · GitHub · Google Workspace · Next.js · Supabase

---

## In progress

**[LFG-optim](https://github.com/saltylvn/LFG-optim.)**: a local-first Python platform that shows where a team's time goes: a workload radar for open pull requests and review queues, pull request cycle-time analytics from a live GitHub connector, and an SE ops toolkit for demo prep and call summaries. Python 3.12 · mypy (strict) · ruff · pytest · GitHub Actions.

---

## All tools

**AI agents:** Claude Code · Cursor · Grok

**AI and automation:** Python · FastAPI · Google Gemini · n8n · LLM evals · prompt-injection defense

**APIs and integrations:** HubSpot · Slack · GitHub · RDAP · OAuth 2.0 · signed webhooks · REST

**Full-stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS · Supabase (Postgres, auth, row-level security) · Zod · Vitest

**Delivery:** GitHub Actions · CodeQL · Dependabot · Docker · Vercel

**Diagrams and docs:** Mermaid · architecture decision records
