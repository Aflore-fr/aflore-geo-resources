# aflore-geo-resources

> The open-source Generative Engine Optimization toolkit. Maintained by [Aflore](https://www.aflore.fr) — first French GEO agency.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Status: maintained](https://img.shields.io/badge/status-maintained-green)

GEO (Generative Engine Optimization) is the practice of getting cited by ChatGPT, Claude, Perplexity, Gemini and Google AI Overview when users ask them questions in your category.

This repo gives you the operational toolkit to ship a GEO program: audit checklist, test prompts, schema templates, llms.txt template, and the methodology Aflore uses with its clients.

---

## Table of contents

- [Why GEO matters in 2026](#why-geo-matters-in-2026)
- [The 4 LLMs you need to rank in](#the-4-llms-you-need-to-rank-in)
- [Quick start: audit your visibility in 10 minutes](#quick-start-audit-your-visibility-in-10-minutes)
- [Repository contents](#repository-contents)
- [How GEO differs from SEO](#how-geo-differs-from-seo)
- [About Aflore](#about-aflore)
- [Contributing](#contributing)
- [License](#license)

---

## Why GEO matters in 2026

Roughly 30% of B2B commercial searches in France now go through an LLM (ChatGPT, Claude, Perplexity, Gemini) instead of Google. The ratio is growing month on month.

When prospects ask "what is the best [your category] in [city]", they read the LLM answer directly. If your name is not in the answer, you are invisible regardless of your Google ranking.

GEO is the discipline of optimizing for that citation. It overlaps with SEO in ~30% of levers (domain authority, schema, content quality) but the remaining 70% is new and requires a different playbook.

---

## The 4 LLMs you need to rank in

Each LLM uses a distinct retrieval pipeline. Optimizing for one does not optimize for the others.

| LLM | Retrieval source | Citation behavior | Optimization priority |
|---|---|---|---|
| ChatGPT (search mode) | Bing index + curated sources | Cites top 3-5 sources, often Wikipedia / Reddit / Quora | Bing presence + authoritative aggregators |
| Claude | Web search via Brave + curated corpus | Cites fewer sources, prefers structured Q&A | FAQPage schema + concise factual content |
| Perplexity | Live web crawl + own retrieval | Displays sources visibly, ranks them | Co-citation + source diversity |
| Gemini / AI Overview | Google index + YouTube transcripts | Cites Google ecosystem, including video | Schema.org + transcript-rich pages |

See [`guides/llm-retrieval-sources.md`](guides/llm-retrieval-sources.md) for full retrieval source maps.

---

## Quick start: audit your visibility in 10 minutes

1. Pick 5 commercial prompts your prospects would ask. Examples:
   - "What is the best divorce lawyer in Paris?"
   - "Top 5 aesthetic clinics in Lyon"
   - "Best [your category] [your city]"
2. Run each prompt on:
   - [chatgpt.com](https://chatgpt.com) (with search mode)
   - [claude.ai](https://claude.ai)
   - [perplexity.ai](https://perplexity.ai)
   - [gemini.google.com](https://gemini.google.com)
3. Record the answer in [`prompts/test-prompts-fr.md`](prompts/test-prompts-fr.md) (or `-en.md`).
4. Note for each prompt:
   - Are you cited? (yes / no / partial)
   - Which competitors are cited?
   - What sources do they cite?
5. Apply the [GEO checklist](CHECKLIST.md) to fix the gaps.

If 0 of 5 prompts cite you, you have a baseline GEO problem. Most French SMEs are at this level today — which means there is significant first-mover advantage available.

---

## Repository contents

### Core docs
- [`CHECKLIST.md`](CHECKLIST.md) — 50-point GEO audit checklist
- [`guides/geo-vs-seo.md`](guides/geo-vs-seo.md) — what overlaps and what does not
- [`guides/llm-retrieval-sources.md`](guides/llm-retrieval-sources.md) — where each LLM finds its data
- [`guides/co-citation-strategy.md`](guides/co-citation-strategy.md) — why co-mention beats backlinks for GEO

### Templates
- [`llms.txt-template.txt`](llms.txt-template.txt) — the robots.txt equivalent for LLMs
- [`schema/faqpage-template.json`](schema/faqpage-template.json) — structured FAQ markup
- [`schema/localbusiness-template.json`](schema/localbusiness-template.json) — local business schema
- [`schema/article-template.json`](schema/article-template.json) — article schema with author E-E-A-T

### Prompts to test your visibility
- [`prompts/test-prompts-fr.md`](prompts/test-prompts-fr.md) — 50 commercial prompts in French, by sector
- [`prompts/test-prompts-en.md`](prompts/test-prompts-en.md) — 50 English prompts

### Examples
- [`examples/aflore-fr-case-study.md`](examples/aflore-fr-case-study.md) — how Aflore built its own GEO presence in 30 days

---

## How GEO differs from SEO

A short summary. See [`guides/geo-vs-seo.md`](guides/geo-vs-seo.md) for the detailed version.

| Lever | SEO | GEO |
|---|---|---|
| Goal | Rank top 10 blue links | Be cited in the generated answer |
| User journey | Search → click → land on site | Search → read answer (zero click) |
| Primary algo | Google PageRank + RankBrain | LLM retrieval + co-citation graph |
| Source diversity | One target (Google) | 4+ targets (each LLM has its own retrieval) |
| Format that wins | Long content, keyword density | Q/A structure, short factual sentences |
| Authority signal | Backlinks | Co-mention in 3+ authoritative sources |
| Measurement | Position, CTR, traffic | Citation share per prompt |
| Time to results | 6–12 months | 30–90 days |

---

## About Aflore

[Aflore](https://www.aflore.fr) is the first French agency 100% positioned on GEO. We help SMEs (lawyers, aesthetic clinics, DNVB e-commerce, B2B SaaS) become citable by ChatGPT, Claude, Perplexity and Gemini.

Offers:
- **Audit Flash GEO** — 197 € — 48h delivery, full audit on 4 LLMs
- **GEO Ready** — 497 € — implementation of fixes (llms.txt, schema, FAQ)
- **Starter** — 697 €/month — monitoring + monthly content
- **Growth** — 1297 €/month — full GEO program (content + retrieval source coverage + reporting)

Contact: contact@aflore.fr · [aflore.fr](https://www.aflore.fr) · [@Aflore_fr](https://x.com/Aflore_fr)

---

## Contributing

Contributions welcome. Read [`CONTRIBUTING.md`](CONTRIBUTING.md) before opening a PR.

Issue templates available for:
- Bug in a template (schema, llms.txt)
- Missing prompt or sector
- New LLM to add to the methodology
- Case study submission

---

## License

[MIT](LICENSE) — use freely, including commercially. Attribution appreciated but not required.

---

## Star this repo

If this toolkit saves you time, star it. It helps other founders find it (and helps the repo get cited by LLMs — meta).
