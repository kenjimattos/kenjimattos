<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://capsule-render.vercel.app/api?type=blur&amp;height=260&amp;color=0:0f2027%2C50:203a43%2C100:2c5364&amp;text=Kenji%20Mattos%20Kinoshita&amp;fontSize=48&amp;fontColor=ffffff&amp;desc=Full-stack%20developer%20%C2%B7%20LLMs%20and%20MCP%20servers%20in%20production&amp;descSize=16&amp;descAlignY=68" />
  <source media="(prefers-color-scheme: light)" srcset="https://capsule-render.vercel.app/api?type=blur&amp;height=260&amp;color=0:e6eef5%2C50:cfe0ea%2C100:b4cddd&amp;text=Kenji%20Mattos%20Kinoshita&amp;fontSize=48&amp;fontColor=2C5364&amp;desc=Full-stack%20developer%20%C2%B7%20LLMs%20and%20MCP%20servers%20in%20production&amp;descSize=16&amp;descAlignY=68" />
  <img alt="Kenji Mattos Kinoshita" src="https://capsule-render.vercel.app/api?type=blur&amp;height=260&amp;color=0:0f2027%2C50:203a43%2C100:2c5364&amp;text=Kenji%20Mattos%20Kinoshita&amp;fontSize=48&amp;fontColor=ffffff" />
</picture>

<div align="center">

<a href="https://www.linkedin.com/in/kenjimattos/">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white"/>
</a>
<a href="mailto:kenjimattos@gmail.com">
  <img src="https://img.shields.io/badge/-Email-2c5364?style=for-the-badge&amp;logo=gmail&amp;logoColor=white"/>
</a>
<a href="https://kenji-mattos.vercel.app">
  <img src="https://img.shields.io/badge/-Portfolio-0f2027?style=for-the-badge&amp;logo=vercel&amp;logoColor=white"/>
</a>

</div>

---

I ship complete products in **React, Next.js, TypeScript and Node.js**, with **generative AI in production** — LLMs wired into the product through the API, from the prompt to the error handling, an MCP server with its own authorization layer that a team queries every day, and LLM-driven code review in CI.

I am an economist by training, with 7 years in corporate financial planning before engineering. That is why I model the business rules before writing the solution, and why I gravitate towards systems where the logic is the hard part: access control, medical staffing, socioeconomic indicators.

---

## Selected work

### [`finance`](https://github.com/kenjimattos/finance) · TypeScript

Self-hosted credit-card spending manager on top of Brazilian Open Finance. TypeScript monorepo end to end — Express API, React SPA, one SQLite database per user with automatic migrations — plus fatura import from screenshots through Claude vision.

The part worth reading: transactions were silently changing value. The aggregator recycles transaction IDs, reposts pending rows with new dates and re-issues everything on reconnection. I keyed every row on a locally minted UUID and deduplicated on a hash of date, amount and merchant, so a full re-sync never destroys the categories, splits and overrides a user has built. The reasoning is written down in [`docs/`](https://github.com/kenjimattos/finance/tree/main/docs), and the business rules are covered by tests.

**Live demo:** `demo` / `demo` — link in the repo.

### [`sebrae-opp-snapshot`](https://github.com/kenjimattos/sebrae-opp-snapshot) · React 19 · Python

Territorial intelligence platform covering the 223 municipalities of Paraíba, built for Sebrae. Three layers: a React 19 SPA, a Fastify/MongoDB read API that resolves each indicator's status server-side from officially published thresholds, and a Python ETL consolidating 35 socioeconomic indicators from more than ten government sources.

The choropleth map is plain SVG generated from IBGE GeoJSON, with the lon/lat to viewBox projection written by hand rather than pulled from a mapping library. Averages drawn from fewer than 30 samples are withheld by the API instead of being rendered as a misleading number.

**562 commits. Live demo in the repo.**

### MCP server for Meta Business Insights · TypeScript *(production, private)*

Thirteen tools over the Meta Graph API — followers, page and Instagram insights, per-post performance, comment search — aggregated across an entire account portfolio, so a non-technical team can ask questions in natural language through Claude instead of navigating dashboards. A five-minute dashboard hunt became a thirty-second question.

The access token stays on the server, which is what makes installation trivial for people who do not work with credentials: add the connector, sign in with Google Workspace, done. As a side effect, revoking someone's access is deleting a line rather than rotating a secret that holds write access to everything. Implemented as an authorization server with dynamic client registration (RFC 7591), an email allowlist, and write permission separated from read. Runs on a Linux VPS under systemd and Caddy, with a daily systemd timer that replays missed runs after downtime — the Instagram API only exposes a 30-day follower window, so a skipped day is data that never exists.

---

## Stack

<img src="https://skillicons.dev/icons?i=ts,react,nextjs,nodejs,python,postgres,mongodb,tailwind,docker,linux,git,figma&perline=6&theme=light" />

**Also:** Model Context Protocol · Anthropic SDK · OpenRouter · Fastify · Express · Zod · Vitest · React Testing Library · Supabase · systemd · Caddy · Nginx · GitHub Actions

---

## Background

Economics degree (Mackenzie). Seven years in corporate FP&A, running a utility's business plan and a R$400M Opex budget. Nine years as a designer and art director, writing landing pages and HTML5 ad campaigns throughout. Engineering has been the centre of my work since 2024.

**CS50x** (Harvard/edX) — completed, with a Python/Flask final project.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white)](https://www.linkedin.com/in/kenjimattos/)

</div>

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,100:2c5364&height=120&section=footer)
