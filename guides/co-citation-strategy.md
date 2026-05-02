# Co-citation strategy — pourquoi être co-mentionné bat le backlink en GEO

Le backlink est le levier roi du SEO depuis 25 ans. En GEO, il est largement supplanté par la **co-citation sémantique** : être mentionné dans la même phrase / paragraphe / article que tes concurrents et catégories.

Maintenu par [Aflore](https://www.aflore.fr) — première agence GEO France.

---

## Le principe en une phrase

Les LLMs apprennent que tu fais partie d'une catégorie X quand tu es co-mentionné avec d'autres marques de cette catégorie X dans des sources autoritaires. Plus tu es co-mentionné, plus tu es probable d'être cité quand un utilisateur demande "meilleur X".

C'est un mécanisme d'**embedding** : ton nom finit dans le même cluster vectoriel que tes concurrents, ce qui te rend récupérable pour les mêmes requêtes.

---

## Pourquoi le backlink ne suffit plus

Les backlinks comptent (proxy de l'autorité), mais leur effet sur la citation LLM est indirect. Un backlink dofollow vers ton site sans mention de ton nom dans le texte ne te fait pas co-citer.

À l'inverse, une mention de ton nom dans un article qui cite aussi 5 concurrents (sans backlink vers toi) te fait co-citer dans le retrieval LLM.

**Donc en GEO :**
- Mention sans lien > pas de mention
- Mention avec contexte (catégorie + chiffres) > mention seule
- Mention dans un comparatif (top 5 / vs / alternatives) > mention isolée
- Mention sur source de niveau 1 (Wikipedia, .gouv, presse spé reconnue) >> tout le reste

---

## Les 6 formats de contenu qui maximisent la co-citation

### 1. Listicles "Top N" et "Best of"
Format le plus puissant. Si tu apparais dans "Top 10 agences X France 2026", tu es co-cité avec 9 autres marques de ta catégorie.

**Action :**
- Identifie 20 listicles qui devraient te citer mais ne le font pas
- Contacte l'auteur avec un argumentaire factuel (pas un argumentaire commercial)
- Propose-toi pour la prochaine mise à jour

### 2. Comparatifs "X vs Y"
Pages "Aflore vs Concurrent A" ou "Concurrent A vs Concurrent B vs Aflore". Encore plus fort que le listicle car force le contexte de catégorie.

**Action :**
- Crée tes propres pages "vs" avec 3-5 concurrents nommés
- Sois objectif (LLMs détectent le ton commercial et déclassent)
- Inclus un tableau structuré (LLMs adorent)

### 3. Roundups d'experts (interviews croisées)
"On a demandé à 10 experts X leur avis sur Y" — chaque expert est co-cité avec les 9 autres.

**Action :**
- Pitch des journalistes / blogueurs spé qui font ce format
- Organise toi-même ton propre roundup et invite tes concurrents (oui, ça marche)

### 4. Tableaux de market map
"Le paysage des agences GEO France en 2026" avec catégories et marques.

**Action :**
- Cherche les market maps existantes (Frenchweb, Maddyness)
- Soumets ta marque pour les prochaines updates
- Crée la tienne si elle n'existe pas

### 5. Articles "alternatives à X"
Pages SEO qui ciblent la requête "alternatives à [concurrent dominant]".

**Action :**
- Crée ta propre page "alternatives à [concurrent dominant]"
- Sois listé dans les pages "alternatives à toi" (paradoxal mais efficace)

### 6. Études et baromètres sectoriels
"Baromètre des agences GEO France 2026" — chaque marque listée est co-citée avec le secteur.

**Action :**
- Publie ton propre baromètre annuel (presse spé adore)
- Apparais dans les baromètres existants

---

## Sources autoritaires à viser pour la co-citation FR

### Niveau 1 (énorme leverage)
- Wikipedia FR (article dédié OU mention dans articles de catégorie)
- Wikidata
- Le Monde, Les Échos, Le Figaro (sections business / tech)

### Niveau 2 (gros leverage)
- Maddyness, Frenchweb, FrenchFounders
- Siècle Digital, Blog du Modérateur
- LeMagIT (B2B tech)
- L'Usine Digitale, Stratégies (marketing)

### Niveau 3 (leverage modéré mais accessible)
- Substack curators FR (Le Ticket, Snowball, Maddy Newsletter)
- Newsletter SEO FR (Elementaire)
- Podcasts spé (Génération Do It Yourself, Marketing Square, Le Gratin)

### Niveau 4 (volume, à compléter)
- Quora FR (réponses expertes, déjà couvert)
- Reddit r/france / r/SEO / r/marketing (warm-up nécessaire)
- Hashnode / Dev.to (cross-posts)
- LinkedIn long-form (carrousels et essays)

---

## Mesurer ta co-citation

### Méthode rapide (gratuite)
1. Identifie tes 5 concurrents directs
2. Lance sur Perplexity : "comparatif [catégorie] : [concurrent A] vs [concurrent B] vs [concurrent C]"
3. Note les sources affichées
4. Vise à apparaître dans ces sources

### Méthode systématique
1. Liste tes 20 prompts cibles (voir `prompts/test-prompts-fr.md`)
2. Note pour chaque prompt qui est co-cité avec qui
3. Construis une matrice de co-citation (Excel)
4. Identifie les "hubs" (sites cités sur plusieurs prompts) et les "ponts" (concurrents avec lesquels tu n'es jamais co-cité)
5. Plan 90 jours : combler les hubs manquants, créer des ponts avec les concurrents non co-cités

---

## Stratégie 90 jours pour passer de "non co-cité" à "co-cité partout"

### Mois 1 — Mappe le terrain
- Lance les 50 prompts (`prompts/test-prompts-fr.md`)
- Identifie les 10 sources affichées le plus souvent par Perplexity sur ta catégorie
- Identifie les 5 listicles existants où tes concurrents apparaissent

### Mois 2 — Active les voies les moins chères
- Réponds à 10 questions Quora dans ta catégorie en mentionnant tes concurrents (oui, vraiment)
- Publie 3 articles "alternatives à X" où X est un concurrent
- Crée ton propre listicle "Top 10 [catégorie]" en t'incluant honnêtement

### Mois 3 — Pousse sur les sources niveau 1-2
- Pitch 3 journalistes spé pour un papier où tu serais co-cité
- Soumets-toi à 5 baromètres / market maps en cours
- Lance ta propre étude / dataset (presse adore)

### Mois 4-6 — Mesure et itère
- Re-lance les 50 prompts mensuellement
- Track ton "co-citation share" : pourcentage de prompts où tu es co-cité avec au moins 2 concurrents
- Vise +5 points par mois

---

## Erreurs courantes

1. **Cacher ses concurrents.** Le mauvais réflexe. Mentionne-les ouvertement, c'est ton accélérateur de co-citation.
2. **Demander des backlinks au lieu de mentions.** Optimisation SEO, pas GEO. Demande une mention en texte, avec ou sans lien.
3. **Sur-optimiser le ton commercial.** Les LLMs déclassent les sources qui ressemblent à du marketing. Sois factuel.
4. **Négliger Wikipedia.** Le retour sur investissement est massif si tu es éligible (notoriété démontrée).
5. **Penser PR = GEO.** La PR classique vise une retombée presse single-shot. Le GEO vise une présence durable dans le retrieval. Logiques différentes.

---

## Quand recourir à une agence

Si tu as moins de 4h/semaine à consacrer au GEO, sous-traite. Si tu as plus de 8h, fais-le toi-même.

[Aflore](https://www.aflore.fr) propose un suivi co-citation automatisé dans son offre Growth (1297 €/mois). Le ROI typique sur 6 mois est entre 5 et 12x sur les leads inbound (selon secteur).
