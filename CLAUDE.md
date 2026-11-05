# Instructions pour l'IA

Ce fichier est lu automatiquement par Claude Code (et par les autres outils via `AGENTS.md`).
La méthode complète est dans `GUIDE.md`. Les commandes `/cadrer`, `/debut`, `/tache`, `/fin`, `/livrer` et `/retro` appliquent ses checklists.

## Au début de chaque session
1. Lis `PROJECT.md` (objectif, terminé, périmètre), `NEXT.md` (état, prochaine action) et `DECISIONS.md` (choix déjà faits).
2. Si `PROJECT.md` n'est pas rempli, propose de faire le cadrage (`/cadrer`) et ne produis rien d'autre.
3. Si `recettes/` contient une recette pour ce type de projet, lis-la.

## Rôles
L'utilisateur décide et valide. Toi, tu proposes, produis, vérifies et documentes.
Il peut aussi remplir les fichiers lui-même : respecte ce qu'il a écrit, complète-le sans le réécrire.

## Façon de travailler
- **Périmètre** : reste dans la tâche en cours et dans le périmètre de `PROJECT.md`. Une idée hors périmètre, c'est une ligne dans « Plus tard » de `NEXT.md`, pas du travail en plus. Signale-la.
- **Plan d'abord** pour toute tâche qui touche plusieurs fichiers ou un choix d'architecture. Attends la validation. Les petites modifications évidentes se font directement.
- **Petits pas** : des diffs de moins de 200 à 300 lignes. Au-delà, propose de découper la tâche.
- **Vérifie avant de dire « fini »** avec la commande « Vérifier » de la section Projet. Si tu ne peux pas vérifier, dis-le explicitement et explique comment l'utilisateur peut le faire.
- **Aucune nouvelle dépendance**, aucun nouveau service ni compte sans accord explicite.
- **Choix structurant** : présente 2 options et leurs compromis, laisse l'utilisateur trancher, puis ajoute une entrée dans `DECISIONS.md`.
- **Explique simplement** ce que tu as fait. Chaque notion nouvelle pour l'utilisateur va dans `GLOSSAIRE.md`.
- Ne remplis jamais seul les rubriques de décision de `PROJECT.md` (Pourquoi, Définition de terminé, Hors périmètre) : propose des formulations, l'utilisateur valide.

## Git
- Ne commite **jamais** sur `main`, sauf le commit de cadrage initial (`chore: cadrer le projet`) et seulement à la demande de l'utilisateur.
- Ne fais **jamais** de merge, de `push --force`, de `reset --hard` ni de réécriture d'historique.
- Une tâche = une branche `type/nom-court` (`feat`, `fix`, `docs`, `refactor`, `test`, `chore`, `exp`).
- Commits petits et fréquents, au format Conventional Commits en français : `type: description à l'impératif`, moins de 70 caractères.
- N'ajoute que les fichiers liés à la tâche : vérifie `git status` avant chaque commit, jamais de `git add -A` à l'aveugle.
- Tu peux pousser la branche de la tâche. La pull request est relue et fusionnée par l'utilisateur.
- Aucun secret dans le dépôt. Ne lis pas `.env` ; les noms de variables vont dans `.env.example`.

## Projet
<!-- À remplir au cadrage, à partir de « Comment ça marche concrètement » de PROJECT.md. -->
- **Type :**
- **Où vit le travail :**
- **Installer :**
- **Lancer :**
- **Vérifier :**
- **Livrer :**
- **Conventions propres au projet :**

## Erreurs à ne pas refaire
<!-- Une ligne chaque fois que l'IA répète une erreur. Ce fichier devient ton manuel de management. -->
-
