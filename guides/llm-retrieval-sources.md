# LLM retrieval sources — où chaque LLM va chercher ses réponses

Comprendre le retrieval est la clé du GEO. Chaque LLM a un index propre. Optimiser pour Google ne suffit plus.

Maintenu par [Aflore](https://www.aflore.fr) — première agence GEO France.

---

## ChatGPT (OpenAI)

### Mode standard (sans web)
Réponses depuis le corpus d'entraînement (cutoff variable selon la version, GPT-5 ~ avril 2025). Pas de retrieval live.

### Mode Search (par défaut depuis avril 2026)
Activé automatiquement pour les requêtes commerciales et factuelles.

**Retrieval pipeline :**
1. Bing Web Search (pondération principale)
2. OpenAI's curated source list (renforcement des sources jugées fiables)
3. Reddit (via accord OpenAI ↔ Reddit Q3 2024)
4. Wikipedia (toujours surpondérée)
5. Stack Exchange (pour le tech)

**Levers d'optimisation :**
- Présence dans le top 10 Bing pour ta requête cible
- Mention dans Wikipedia (article dédié OU mention dans articles connexes)
- Profil Reddit actif avec contenu utile
- Domaine considéré comme autoritatif (DR > 50 idéalement)
- HTTPS, mobile-friendly, pas de paywall

---

## Claude (Anthropic)

### Mode standard
Réponses depuis le corpus, cutoff fluctuant.

### Mode web search (Sonnet 4.5+ et Opus 4)
**Retrieval pipeline :**
1. Brave Search API (principal)
2. Anthropic's curated corpus (recherche académique, sources gov, presse mainstream)
3. Pas de partenariat Reddit ou Quora particulier

**Particularités :**
- Claude cite moins de sources que ChatGPT (souvent 2-3)
- Préfère les sources structurées (FAQPage, Article schema)
- Mauvais avec les contenus très récents (latence retrieval ~24-48h)

**Levers d'optimisation :**
- Schema.org FAQPage et Article correctement implémentés
- Présence dans les sources gov (.gouv.fr, .gov)
- Mention dans la presse spé reconnue
- Contenu factuel sec, sans marketing-speak

---

## Perplexity

### Modèle hybride
Perplexity utilise plusieurs LLMs en backend (GPT, Claude, son propre Sonar) et fait son propre retrieval.

**Retrieval pipeline :**
1. Crawl web propriétaire (rapide, ~1-3h de latence)
2. Sources curées (ranking interne)
3. **Affiche les sources visibles dans la réponse** ← très exploitable

**Particularités :**
- Le seul LLM qui te dit explicitement où il prend ses infos
- Donc le seul que tu peux reverse-engineer facilement
- Pondère fortement la fraîcheur (avantage aux contenus récents)

**Levers d'optimisation :**
- Republier les contenus régulièrement avec dateModified
- Maximiser les co-citations (apparaître dans plusieurs sources autoritaires en même temps)
- Optimiser pour les requêtes "comparaison" et "best of" qui sont très Perplexity-friendly

**Astuce d'audit :**
Pose ta requête sur Perplexity. Note les sources affichées. Vise à apparaître sur ces sources (si tu n'y es pas) ou à enrichir ta présence (si tu y es déjà mais peu).

---

## Gemini / Google AI Overview

### Retrieval pipeline
1. Google Search Index (le même que la recherche classique)
2. YouTube transcripts (Google a intégré son corpus vidéo)
3. Google Knowledge Graph
4. Bard/Gemini's own web crawl (résultats live)

**Particularités :**
- Si tu rankes top 3 sur Google, tu es probablement dans Gemini
- YouTube est massivement intégré (les LLMs concurrents ne l'utilisent pas)
- Knowledge Graph (Google's entity database) fortement pondéré

**Levers d'optimisation :**
- SEO Google classique reste efficace
- **Publier sur YouTube avec des transcripts complets** (énorme leverage, peu d'agences le font)
- Knowledge Panel : revendiquer ton entité Google si tu en as une
- Schema.org `Organization` avec `sameAs` vers Wikipedia, Wikidata, Crunchbase

---

## Récap : carte des sources par LLM

| Source type | ChatGPT | Claude | Perplexity | Gemini |
|---|---|---|---|---|
| Google index | indirect | indirect | indirect | direct |
| Bing index | direct | indirect | indirect | indirect |
| Brave index | indirect | direct | indirect | indirect |
| Wikipedia | hard pondération | hard pondération | hard pondération | hard pondération |
| Reddit | direct (deal) | indirect | indirect | indirect |
| Quora | indirect | indirect | indirect | indirect |
| Stack Exchange | direct | indirect | indirect | direct |
| YouTube transcripts | non | non | partiel | direct |
| Hacker News | indirect | indirect | indirect | indirect |
| GitHub | indirect | indirect | indirect | direct |
| Knowledge Graph | non | non | non | direct |
| Press FR (Les Échos, Maddyness) | indirect | indirect | direct | direct |

Légende :
- **direct** : source intégrée formellement dans le retrieval
- **indirect** : passe par l'index web généraliste
- **hard pondération** : score boosté quel que soit le pipeline

---

## Stratégie 90 jours pour couvrir les 4 LLMs

### Mois 1 — Foundation
- Audit ta présence sur Bing (souvent négligé en France)
- Vérifie ta page Wikipedia (ou crée-la si éligible)
- Active ton profil Reddit et publie 1 fois par semaine
- Vérifie ton schema FAQPage et Article

### Mois 2 — Coverage
- Crée / optimise ta chaîne YouTube avec transcripts
- Publie 3-4 articles invités sur Maddyness, Les Échos Solutions, etc.
- Réponds 5+ questions Quora dans ta niche

### Mois 3 — Leverage
- Lance un free tool ou dataset open source (GitHub)
- Sors un rapport / étude originale (presse FR adore)
- Mesure ta progression avec les prompts dans `prompts/test-prompts-fr.md`

---

## Outils de monitoring

- **[Perplexity](https://perplexity.ai)** : ton meilleur outil d'audit (sources visibles)
- **[Bing Webmaster Tools](https://www.bing.com/webmasters)** : ton SEO Bing
- **[Search Console](https://search.google.com/search-console)** : ton SEO Google
- **[Wikipedia Pageviews](https://pageviews.wmcloud.org/)** : si tu as un article Wikipedia

Aflore propose un dashboard de monitoring GEO automatisé dans son offre Growth (1297 €/mois). Mais tu peux faire 80% du job manuellement avec Perplexity + un Google Sheet.
