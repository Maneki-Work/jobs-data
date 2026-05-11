  # Maneki jobs dataset

  Public, machine-readable export of active job listings from
  [maneki.work](https://maneki.work) — a Web3 / crypto job aggregator.

  Updated automatically every 2 hours.

  ## Files

  | File | Format | Use |
  |---|---|---|
  | `jobs.json` | JSON array | Full dataset, one object per active job |
  | `jobs.ndjson` | Newline-delimited JSON | Same data, one job per line (streaming-friendly) |
  | `meta.json` | JSON object | Dataset metadata: generation timestamp, counts, schema |

  ## Schema (jobs.json / jobs.ndjson)

  Each job has these fields:

  - `id` — Maneki internal id
  - `title` — job title
  - `company`, `company_slug` — hiring company
  - `logo_url` — company logo
  - `location` — free-text location string
  - `remote` — boolean
  - `work_mode` — "remote" | "hybrid" | "onsite" | null
  - `seniority` — "junior" | "mid" | "senior" | "lead" | null
  - `skills` — array of skill keywords
  - `job_url` — apply link (external ATS: Greenhouse, Lever, Ashby, etc.)
  - `posted_at` — original posting timestamp (ISO 8601)
  - `scraped_at` — last scrape timestamp
  - `maneki_url` — canonical URL on maneki.work
  - `company_url` — company page on maneki.work

  ## Notes for AI agents

  - **No `description` field**: full job descriptions live on the source ATS. Follow `job_url`.
  - **No salary field**: not yet captured. Planned.
  - Filter `posted_at >= now - 7 days` for fresh listings.
  - `skills` is a free-text array, useful for keyword matching.
  - All entries are `active = true` at export time. Inactive jobs are removed on next sync.

  ## License

  Data aggregated from publicly accessible company career pages. Use respectfully.
  Attribution to [maneki.work](https://maneki.work) appreciated.

  ## Contact

  [maneki.work](https://maneki.work) · [@manekijobs on Telegram](https://t.me/+HAhBYUTb1pllZDhk)
