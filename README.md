# Hi, I'm Tyler Clark 👋

**Solutions Engineering | Building AI Agents & Workflows | Automation, APIs & Integrations | Strategic Tech Support Analyst | Former Sales Leader & Business Partner**

I build AI workflows, integrations and full-stack apps, from idea to working product, with [Claude Code](https://claude.com/claude-code) as my AI pair programmer. I own the product decisions, test with real services and devices, and ship in small pull requests with automated tests.

## Projects

### [Human-in-the-Loop Triage](https://github.com/saltylvn/human-in-the-loop-triage)

An AI workflow that triages contact form messages across Gemini, HubSpot and Slack, and asks a person before risky actions. It handled 84% of 70 held-out synthetic messages alone at 97% correct, and has run live on test accounts.

[![Human-in-the-Loop Triage system map: contact form, API, database and worker, connected to Gemini, RDAP, HubSpot, Slack and a human approver](https://github.com/saltylvn/human-in-the-loop-triage/raw/main/docs/assets/system-map.png)](https://github.com/saltylvn/human-in-the-loop-triage)

**Highlights:** HubSpot OAuth · signed webhooks · five layers against duplicates · append-only audit log · 100-example eval · 83 tests

**Tech stack:** Python · FastAPI · Pydantic · httpx · SQLite · Google Gemini · HubSpot API · Slack API · RDAP · Docker · pytest · mypy · ruff · GitHub Actions

### [Dialed Kitchen](https://github.com/saltylvn/dialed-kitchen) · [live site](https://dialed-kitchen.vercel.app)

Meal planning, recipes and grocery price tracking for a couple. It plans the week and builds the grocery list with an estimated cost.

[![Dialed Kitchen overview: a meal planner, recipe box and grocery list, with its engineering areas and architecture](https://github.com/saltylvn/dialed-kitchen/raw/main/docs/images/dialed-kitchen-overview.png)](https://github.com/saltylvn/dialed-kitchen)

**Highlights:** Gemini reads recipe photos and estimates nutrition · RLS on all 12 tables · SSRF-safe link import · 281 tests (103 against real Postgres) · 24 decision records

**Tech stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS · Supabase (Postgres, auth, row-level security) · Google Gemini · Zod · Vitest · PGlite · Vercel · GitHub Actions · CodeQL

### [DEVELOP](https://github.com/saltylvn/wellness-tracker) · [live demo](https://wellness-tracker-virid.vercel.app) (no sign-up)

A wellness tracker for food, lifting, cardio and weight, with AI calorie and macro estimates from a photo.

[![DEVELOP on iPhone: the Fitness tab and the swipe-to-log weight and reps wheels](https://github.com/saltylvn/wellness-tracker/raw/main/docs/showcase/develop-fitness@2x.png)](https://github.com/saltylvn/wellness-tracker)

**Highlights:** photo estimates in under 3 seconds (down from 12.5 s) · swipe-to-log workouts · RLS on all 13 tables · strict CSP · 232 tests · protected `main` · one-click demo

**Tech stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS · Supabase (Postgres, auth, row-level security) · Google Gemini · ZXing · Vitest · Vercel · GitHub Actions · CodeQL

## All tools

**AI and automation:** Python · FastAPI · Google Gemini · n8n · HubSpot and Slack APIs · OAuth 2.0 · Webhooks · LLM evals

**Full-stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS · Supabase (Postgres, auth, row-level security) · Vitest

**Delivery:** GitHub Actions · Docker · Vercel
