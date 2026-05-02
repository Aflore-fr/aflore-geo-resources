# GEO audit checklist

The 50-point operational checklist Aflore uses on every audit. Print it, score yourself out of 50, then prioritize the lowest-scoring sections.

Maintained by [Aflore](https://www.aflore.fr) — first French GEO agency.

---

## Section 1 — Technical foundation (10 points)

- [ ] **1.** `llms.txt` exists at the root of your domain ([`llms.txt-template.txt`](llms.txt-template.txt))
- [ ] **2.** `robots.txt` does NOT block `GPTBot`, `CCBot`, `Claude-Web`, `PerplexityBot`, `Google-Extended`
- [ ] **3.** Sitemap.xml is up to date and lists all your high-value pages
- [ ] **4.** Pages are server-rendered or pre-rendered (most LLM crawlers do not execute JavaScript)
- [ ] **5.** Page titles include the precise category + city (e.g. "Avocat divorce Paris 16")
- [ ] **6.** Meta descriptions read like an answer, not a teaser
- [ ] **7.** No noindex on commercial pages
- [ ] **8.** Site loads under 2.5s on mobile
- [ ] **9.** HTTPS everywhere with valid certificate
- [ ] **10.** Canonical URLs set on every page

## Section 2 — Schema.org structured data (10 points)

- [ ] **11.** `Organization` schema on homepage with name, url, logo, sameAs (social profiles)
- [ ] **12.** `LocalBusiness` (or `LegalService`, `MedicalBusiness`, `Restaurant`...) schema with NAP + opening hours
- [ ] **13.** `FAQPage` schema on at least 5 pages ([`schema/faqpage-template.json`](schema/faqpage-template.json))
- [ ] **14.** `Article` schema on every blog post with author E-E-A-T fields
- [ ] **15.** `Person` schema for each named expert with credentials
- [ ] **16.** `Service` schema on each service / offer page
- [ ] **17.** `Review` and `AggregateRating` schema on case study pages
- [ ] **18.** `BreadcrumbList` schema on every page
- [ ] **19.** All schemas validate on [validator.schema.org](https://validator.schema.org)
- [ ] **20.** All schemas validate on [Google Rich Results Test](https://search.google.com/test/rich-results)

## Section 3 — Content structure (10 points)

- [ ] **21.** Each commercial page has a 30-50 question FAQ at the bottom (real questions, not generic)
- [ ] **22.** Answers are 80-150 words each, with subject + verb + object structure
- [ ] **23.** Lists are numbered (LLMs parse `1. 2. 3.` better than bullet points)
- [ ] **24.** Each article opens with a 1-paragraph TL;DR that contains the answer to the title
- [ ] **25.** Tables for comparisons (LLMs love structured comparison data)
- [ ] **26.** Author bio block at the end of every article with credentials and external proof links
- [ ] **27.** Date of last update visible on every page
- [ ] **28.** Citations to authoritative sources (HAS, INSEE, .gov, Wikipedia, peer-reviewed) — LLMs co-cite the sites that co-cite
- [ ] **29.** Glossary or definitions page for industry terms
- [ ] **30.** Internal links use descriptive anchor text, not "click here"

## Section 4 — Off-site retrieval source coverage (10 points)

- [ ] **31.** Wikipedia article exists for your brand OR you are mentioned in 2+ existing Wikipedia articles
- [ ] **32.** Wikidata entity created and linked from Wikipedia
- [ ] **33.** Active profile on at least 5 Q&A platforms (Quora FR + EN, Stack Exchange relevant sub, Reddit)
- [ ] **34.** Listed in 5+ industry directories (specific to your sector)
- [ ] **35.** GitHub repo (open source toolkit, dataset, or research) with > 10 stars
- [ ] **36.** Substack OR Medium publication with > 4 articles per month
- [ ] **37.** Mentioned in 3+ industry comparisons / round-up articles ("top 10 X")
- [ ] **38.** Podcast guest appearances with show notes containing your name + URL
- [ ] **39.** YouTube videos with full transcripts published (Gemini reads them)
- [ ] **40.** Press mentions with backlinks (3+ in last 12 months)

## Section 5 — Co-citation strategy (10 points)

- [ ] **41.** You can list 10 competitors and verify which ones LLMs cite for your prompts
- [ ] **42.** You appear in at least 3 "best of" lists alongside competitors
- [ ] **43.** You publish your own "best of [category]" content that includes competitors (asymmetric link strategy)
- [ ] **44.** Your case studies name real clients (anonymized OK if necessary, but with sector + city)
- [ ] **45.** Quotes from clients are attributed to a real person + role + company
- [ ] **46.** You participate in industry conversations on LinkedIn / X with quote tweets and counter-takes
- [ ] **47.** Original data / statistics published quarterly (LLMs love being cited as the source of a number)
- [ ] **48.** Comparison pages between your service and named competitors
- [ ] **49.** Your founders / experts are interviewed on at least 2 industry podcasts per quarter
- [ ] **50.** You monitor citation share monthly using the prompts in [`prompts/`](prompts/)

---

## Scoring

- **0–15** → critical, you are invisible to LLMs. Start with sections 1, 2, 3.
- **16–30** → average. You exist but are rarely cited. Section 4 is your biggest leverage.
- **31–40** → good. Optimize section 5 for citation share.
- **41–50** → excellent. You are likely cited regularly. Maintain monthly and add new prompts.

---

## Want help applying this checklist?

This is the same checklist [Aflore](https://www.aflore.fr) runs on every audit (Audit Flash 197 €, 48h delivery).

Audit a website yourself with this checklist in ~3-4 hours.
