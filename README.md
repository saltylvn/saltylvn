# Hi, I'm Tyler Clark 👋

**Solutions Engineering | Building AI Agents & Workflows | Automation, APIs & Integrations | Strategic Tech Support Analyst | Former Sales Leader & Business Partner**

I build AI workflows, integrations and full-stack apps, from idea to working product, with [Claude Code](https://claude.com/claude-code) as my AI pair programmer. I own the product decisions, test with real services and devices, and ship in small pull requests with automated tests. Based in Lehi, Utah.

## Projects

| Project | What it is | Highlights |
| --- | --- | --- |
| [**Human-in-the-Loop Triage**](https://github.com/saltylvn/human-in-the-loop-triage) | AI workflow that triages contact form messages across Gemini, HubSpot and Slack | Asks a person before risky actions; handled 84% of 70 held-out synthetic messages alone at 97% correct; HubSpot OAuth, signed webhooks, five layers against duplicates, append-only audit log; run live on test accounts; 83 tests |
| [**Dialed Kitchen**](https://github.com/saltylvn/dialed-kitchen) · [live](https://dialed-kitchen.vercel.app) | Meal planning, recipes and grocery price tracking for a couple | Plans the week and builds the grocery list with an estimated cost; Gemini reads recipe photos and estimates nutrition; RLS on all 12 tables; SSRF-safe link import; 281 tests (103 against real Postgres); 24 decision records |
| [**DEVELOP**](https://github.com/saltylvn/wellness-tracker) · [live](https://wellness-tracker-virid.vercel.app) | Wellness tracker for food, lifting, cardio and weight | AI calorie and macro estimates from a photo in under 3 seconds (down from 12.5 s); swipe-to-log workouts; RLS on all 13 tables; strict CSP; 232 tests; CI, CodeQL and a protected `main`; one-click demo |

## Tools I use

**AI and automation:** Python · FastAPI · Google Gemini · n8n · HubSpot and Slack APIs · OAuth 2.0 · Webhooks · LLM evals

**Full-stack:** Next.js 16 · React 19 · TypeScript · Tailwind CSS · Supabase (Postgres, auth, row-level security) · Vitest

**Delivery:** GitHub Actions · Docker · Vercel
