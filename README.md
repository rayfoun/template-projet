# Méthode projet

Dépôt modèle à dupliquer pour chaque nouveau projet.

**Principe : moi = décisions et validation. IA / automatisation = production, recherche, rédaction.**
La structure sert à garder le contrôle et la compréhension, pas à faire le travail.

## Les 5 phases

| # | Phase | Qui | Dossier | Sortie |
|---|-------|-----|---------|--------|
| 1 | Cadrer | Moi | `00-cadrage/` | Fiche projet validée |
| 2 | Comprendre | IA pilotée par moi | `01-recherche/` | Synthèse que je sais reformuler |
| 3 | Produire | IA + automatisation | `02-production/` | Travail relu et validé |
| 4 | Documenter (en continu) | IA rédige, je valide | `04-docs/` | Journaux, glossaire |
| 5 | Livrer et clôturer | Moi | `03-livrables/` | Livrable + bilan |

## Structure

```
.
├── PROMPT_DEMARRAGE.md      # À coller au début de chaque session IA
├── CONVENTIONS.md           # Règles Git (branches, commits, tags)
├── CLAUDE.md                # Lu automatiquement par les outils d'IA
├── exemples/                # Projets d'essai pré-remplis (à copier, pas à garder)
├── .github/                 # Modèles d'issues et de pull requests
├── 00-cadrage/
│   └── fiche-projet.md      # LA source de vérité du projet
├── 01-recherche/            # Notes, synthèses, comparatifs
├── 02-production/           # Le travail en cours (code, contenu, etc.)
├── 03-livrables/
│   └── checklist-livraison.md
└── 04-docs/
    ├── journal-de-bord.md
    ├── journal-de-decisions.md
    ├── glossaire.md
    └── bilan.md
```

## Démarrer un nouveau projet

1. Sur GitHub, cliquer sur **Use this template** (après avoir activé *Template repository* dans les paramètres du dépôt).
2. Nommer le dépôt `YYYY-nom-du-projet`.
3. Remplir `00-cadrage/fiche-projet.md` (15 à 30 min).
4. Lancer une session IA avec `PROMPT_DEMARRAGE.md`.
5. Travailler en suivant `CONVENTIONS.md`.

## Règles d'or

- Pas de fiche projet validée, pas de production.
- Si je ne peux pas expliquer la solution en quelques phrases, la phase 2 n'est pas finie.
- Tout ce qui se répète plus de deux fois devient un script, un modèle ou une automatisation.
- Je relis tout ce que produit l'IA avant de le valider.
- Je documente au fil de l'eau, pas à la fin.
