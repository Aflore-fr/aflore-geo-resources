# GEO vs SEO — what overlaps, what diverges, what is brand new

Maintained by [Aflore](https://www.aflore.fr) — first French GEO agency.

---

## TL;DR

GEO and SEO share ~30% of levers. The remaining 70% requires a different toolkit. Treating GEO as "new SEO" is the most common mistake we see in 2026.

---

## What overlaps (the 30%)

These levers help both SEO and GEO. Do them.

| Lever | Why it works for SEO | Why it works for GEO |
|---|---|---|
| Domain authority (DR) | Google PageRank | LLMs weight authoritative domains in retrieval |
| Schema.org | Rich snippets in SERP | LLMs parse structured data more reliably |
| HTTPS, mobile-friendly, fast | Google ranking factors | LLM crawlers respect web standards |
| Quality content | Engagement, dwell time | LLMs cite well-written sources more |
| Backlinks (count + quality) | PageRank | Authority signal for LLM retrieval |
| Internal linking | Crawl, link equity | LLMs follow internal links during crawl |
| Sitemap.xml | Indexation | LLM crawlers use it too |
| E-E-A-T (author bio, dates, citations) | Google quality rater guidelines | LLMs prefer attributed content |
| Page titles + meta descriptions | CTR in SERP | Often the snippet LLM cites verbatim |
| Local NAP consistency | Local SEO | Local Q&A retrieval |

---

## What diverges (the 70%)

This is where most teams fail. The same content that ranks #1 on Google can be invisible on ChatGPT.

### 1. Goal: rank a link vs be cited in an answer
- **SEO :** the user clicks your link and lands on your page
- **GEO :** the user reads the LLM answer; your name appears (or not) without click

Implication: LLMs scan content for *citable atomic facts*. Your homepage marketing copy is hard to cite. A factual FAQ entry is easy to cite.

### 2. Algorithmic logic
- **SEO :** keyword matching, link graph, user signals
- **GEO :** retrieval scoring (BM25 + vector embedding), source ranking, contextual prompt-fit

Implication: keyword density helps SEO. For GEO, what matters is whether your content semantically matches the user's prompt vector.

### 3. Source diversity
- **SEO :** one target (Google)
- **GEO :** four+ targets (ChatGPT, Claude, Perplexity, Gemini), each with its own retrieval pipeline

Implication: Google #1 is one battle. GEO requires winning four parallel battles, each with different rules. See [`llm-retrieval-sources.md`](llm-retrieval-sources.md).

### 4. Format that wins
- **SEO :** long-form (1500-3000 words), keyword-dense, with internal links
- **GEO :** short factual sentences, Q/A blocks, numbered lists, comparison tables

Implication: a 3000-word SEO article is often a worse GEO asset than a focused 800-word FAQ page with 10 questions.

### 5. Authority signal
- **SEO :** backlinks (PageRank)
- **GEO :** co-citation (being mentioned in the same source as competitors)

Implication: a guest article that links to you without naming your brand has SEO value but minimal GEO value. A "top 10" that names you with no link has zero SEO value but high GEO value.

### 6. Measurement
- **SEO :** position, CTR, organic traffic
- **GEO :** citation share per prompt, retrieval source coverage, mention sentiment

Implication: your existing dashboards don't show GEO performance. You need to score yourself manually (see `prompts/test-prompts-fr.md`).

### 7. Time to results
- **SEO :** 6-12 months for a new site to rank competitive terms
- **GEO :** 30-90 days to start being cited (much faster because the competition is sparse)

Implication: GEO has a window of opportunity in 2026. The market will saturate by 2028.

### 8. Off-site footprint
- **SEO :** backlinks from authoritative domains
- **GEO :** mentions on the specific platforms each LLM crawls (Wikipedia, Reddit, Quora, Stack Exchange, GitHub, YouTube transcripts, podcast show notes)

Implication: a SEO PR campaign aims for "DR50 backlink". A GEO presence campaign aims for "Wikipedia mention + Reddit AMA + 5 podcast appearances + GitHub repo".

### 9. Content that compounds
- **SEO :** evergreen long-form
- **GEO :** structured atomic facts (each fact citable independently)

Implication: rewrite your 5000-word "ultimate guide" into 30 atomic FAQ entries. Each entry can be cited independently in different LLM contexts.

### 10. Risk profile
- **SEO :** algorithm updates can drop traffic 50%+ overnight (Google core updates)
- **GEO :** retrieval changes are smaller, more gradual, less catastrophic

Implication: GEO is a more stable channel once you're in. But it's also harder to leapfrog competitors quickly.

---

## What is brand new in GEO (no SEO equivalent)

These do not exist in SEO. They are pure GEO levers.

### 1. llms.txt
A robots.txt equivalent for LLMs. Tells crawlers which pages to prioritize and provides standalone facts ready to be cited. See [`../llms.txt-template.txt`](../llms.txt-template.txt).

### 2. Prompt-fit optimization
Crafting page content so it matches the structure of typical user prompts ("what is X", "best Y in Z", "how to A").

### 3. Co-citation engineering
Deliberate strategy to be mentioned in the same source as competitors (see [`co-citation-strategy.md`](co-citation-strategy.md)).

### 4. Multi-LLM monitoring
Tracking your citation share across 4+ LLMs simultaneously (no SEO tool covers this natively yet).

### 5. Retrieval source coverage
Mapping which sources each LLM crawls and ensuring you're present on each.

### 6. Hallucination correction
When an LLM cites incorrect facts about you, you have to actively counter-publish to correct the embedding (no SEO equivalent).

### 7. AI Overview claim
For Google, you can claim and dispute AI Overview citations (similar to Knowledge Panel claim).

---

## Migration checklist: from "SEO-only" to "SEO + GEO"

If your current presence is SEO-optimized, here's how to layer GEO on top in 90 days.

### Week 1-2: Audit
- [ ] Run the 50 prompts in `prompts/test-prompts-fr.md`
- [ ] Score yourself on `CHECKLIST.md`
- [ ] Map the sources Perplexity cites for your competitors

### Week 3-4: Foundation
- [ ] Publish `llms.txt` at your root
- [ ] Add FAQPage schema to your top 5 commercial pages
- [ ] Update Article schema on all blog posts with author E-E-A-T

### Week 5-6: Content restructure
- [ ] Identify your 5 best-performing SEO pages
- [ ] For each, add a 30-question FAQ block at the bottom
- [ ] Add a TL;DR paragraph at the top of each

### Week 7-8: Off-site coverage
- [ ] Activate / claim Wikipedia + Wikidata
- [ ] Set up Quora profile and answer 5 questions
- [ ] Set up Reddit account and engage in 3 subreddits

### Week 9-12: Co-citation push
- [ ] Pitch 5 journalists for "top X" inclusion
- [ ] Publish your own "alternatives to [competitor]" page
- [ ] Re-score the 50 prompts and measure progression

---

## Common questions

**Should I stop doing SEO?**
No. SEO still drives traffic and is foundational for GEO (most LLMs use Google or Bing as a retrieval source). Layer GEO on top.

**Will GEO replace SEO?**
Not by 2027. By 2030, probably yes for many B2B and B2C considered-purchase categories.

**Is GEO just LLMO / AEO / SGE-O?**
Yes, all these terms refer to the same discipline. We use "GEO" because it's the term that has the most adoption in the French market in 2026.

**Can I do GEO myself?**
Yes if you have ~8h/week and technical comfort. This repo is designed for self-service.

**When should I hire an agency?**
When your time is worth more than 1500 €/month and you cannot dedicate 8h/week. [Aflore](https://www.aflore.fr) starts at 197 € for an audit.
