# Maneki Web3 & Crypto Jobs Dataset

An openly-licensed, continuously-updated dataset of live **Web3, crypto and
blockchain job postings**, aggregated from company career pages and normalized
into one clean schema.

- **2,514** active jobs · **914** with published salary
- Last updated: `2026-11-25` (refreshed daily)
- Landing page & docs: https://www.maneki.work/data

## What's here

| File | Description |
|------|-------------|
| `sample.json` | The 100 most recent active jobs (rotates daily) |
| `meta.json` | Aggregate stats (counts, salary coverage, freshness) + field schema |

The **full dataset and API** are available for partners, researchers and agent
builders — email team@maneki.work with your use case. Live feeds:
[RSS](https://www.maneki.work/feed.xml) · [llms.txt](https://www.maneki.work/llms.txt) ·
[MCP server](https://www.maneki.work/agents).

## Schema

Each record: `id, title, company, company_slug, logo_url, location, remote,
work_mode, seniority, skills, job_url, posted_at, scraped_at, salary_min,
salary_max, salary_currency, salary_period, salary_offers_equity, maneki_url,
company_url`.

## License

Released under [**CC BY 4.0**](https://creativecommons.org/licenses/by/4.0/).
Free to use, share and build on — commercially too — **with attribution**.
Please credit Maneki with a link:

> Data: Maneki Web3 Jobs Dataset (maneki.work), CC BY 4.0

See `LICENSE` for details.
