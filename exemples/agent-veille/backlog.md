# Backlog : issues à créer dans GitHub

Un milestone par phase. Une issue = une petite tâche, une branche, une pull request.

## Milestone 1 — Comprendre (phase 2)
- [ ] **Recherche :** qu'est-ce qu'un agent ? Boucle observer / décider / agir, outils, limites. Résumé dans `01-recherche/` + termes dans le glossaire.
- [ ] **Recherche :** comparer 2-3 façons de lire des flux RSS en Python. Consigner le choix dans le journal de décisions.
- [ ] **Recherche :** comment appeler un modèle d'IA par API (clé, appel simple, coût par appel).

## Milestone 2 — Produire le noyau (phase 3)
- [ ] Initialiser le projet Python (dépendances, `.env.example`, structure dans `02-production/`)
- [ ] Lire les sources listées dans `sources.yml` et récupérer les articles
- [ ] Mémoriser les articles déjà vus (fichier ou base simple)
- [ ] Filtrer les articles selon mes centres d'intérêt (appel au modèle)
- [ ] Résumer chaque article retenu en 2-3 phrases
- [ ] Générer le digest Markdown dans `output/`
- [ ] Ajouter un plafond d'articles et mesurer le coût par exécution
- [ ] Tests de base (sources vides, flux cassé, doublon)

## Milestone 3 — Automatiser et livrer (phases 3 et 5)
- [ ] Planifier l'exécution quotidienne (GitHub Actions ou cron)
- [ ] Rédiger le README (installation, configuration, usage)
- [ ] Dérouler la checklist de livraison
- [ ] Tag `v1.0.0` + release
- [ ] Remplir `04-docs/bilan.md` et reporter les améliorations dans le dépôt modèle

## Idées v2 (hors périmètre pour l'instant)
Envoi par e-mail, score de pertinence, regroupement par thème, mémoire de mes retours (« plus de ça »).
