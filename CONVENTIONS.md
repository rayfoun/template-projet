# Conventions Git

## Dépôt
- Un projet = un dépôt, **privé par défaut**. Nom : `AAAA-nom-du-projet`.
- `main` est toujours propre et fonctionnel. On ne travaille jamais directement dessus.

## Branches
Une tâche (issue) = une branche : `feat/court-nom`, `fix/court-nom`, `docs/court-nom`.

## Commits
Petits et fréquents. Format : `type: description courte à l'impératif`
Types : `feat`, `fix`, `docs`, `refactor`, `test`, `chore`.

## Pull requests
Toujours, même seul : c'est le point où je relis ce que l'IA a produit avant de fusionner.
Chaque PR référence son issue (`Closes #12`).

## Issues et jalons
Une issue = une petite tâche délégable (modèle dans `.github/ISSUE_TEMPLATE/`).
Un *milestone* GitHub par phase ou par livrable.

## Livraison
Checklist `03-livrables/checklist-livraison.md` cochée, puis tag `v1.0.0` + release GitHub.

## Secrets
Jamais dans Git. Clés dans `.env` (ignoré), noms de variables dans `.env.example`.
Si un secret a été commité par erreur : le révoquer immédiatement, puis nettoyer l'historique.
