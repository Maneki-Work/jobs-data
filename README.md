# Maneki — Web3 Jobs Data

Live data from [maneki.work](https://www.maneki.work), the Web3 job board that aggregates every open crypto and blockchain role from top companies' career pages — normalized, deduplicated, and with stale listings removed within 24 hours.

## What's in this repo

- **[`sample.json`](./sample.json)** — the 100 most recent active jobs, refreshed nightly. Full schema, real data: enough to evaluate quality and structure.
- **[`meta.json`](./meta.json)** — live statistics for the full dataset (total active jobs, freshness counts, salary coverage) + schema reference, refreshed nightly.

## Schema (per job)

`id`, `title`, `company`, `company_slug`, `logo_url`, `location`, `remote`, `work_mode`, `seniority`, `skills[]`, `job_url` (direct application link), `posted_at`, `scraped_at`, `salary_min/max/currency/period`, `salary_offers_equity`, `maneki_url`, `company_url`

All fields are normalized: seniority buckets, work mode (remote/hybrid/onsite), extracted salaries, canonical company slugs, no duplicates.

## Want the full dataset or API access?

The complete catalogue (~2,700 active jobs, nightly refresh) and programmatic access are available for **partners, researchers and agent builders**.

📧 **[team@maneki.work](mailto:team@maneki.work)** — tell us your use case. We're especially interested in AI agents, job-search tools, and labor-market research.

## Free live feeds

- **RSS**: [maneki.work/feed.xml](https://www.maneki.work/feed.xml) — latest 50 jobs, hourly
- **For LLMs/agents**: [maneki.work/llms.txt](https://www.maneki.work/llms.txt) — live counts and structured site map
- Every job page exposes `JobPosting` JSON-LD

---

*Maneki is independent and self-funded. Listings come from public company career pages only — no sponsored roles, no recruiter spam.*
