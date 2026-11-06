---
description: Cadrer un nouveau projet avec moi (PROJECT.md, découpage dans NEXT.md, section Projet de CLAUDE.md)
argument-hint: "[idée du projet en vrac]"
---

Applique avec moi la checklist « Phase 1 et 2 : démarrer un projet » de `GUIDE.md`.

Idée de départ (peut être vide) : $ARGUMENTS

Déroulé :
1. Lis `GUIDE.md` (sections Principes et Démarrer), `PROJECT.md` tel qu'il est (j'ai peut-être commencé à le remplir) et la liste de `recettes/`. Si une recette correspond, dis-le et utilise-la.
2. Si l'idée de départ est vide, demande-moi de la décrire en vrac.
3. Pose-moi des questions, 2 ou 3 à la fois, pour remplir chaque rubrique de `PROJECT.md`. Rubrique par rubrique :
   - Pourquoi, Définition de terminé, Hors périmètre : **tu ne décides pas**. Tu proposes des formulations, je valide.
   - Pousse-moi à rendre chaque critère de terminé vérifiable et la v1 petite. Si la timebox paraît irréaliste, dis-le.
   - « Comment ça marche concrètement » : si je ne sais pas répondre, propose 2 options avec leurs compromis.
4. Test de sortie : si la définition de terminé ne s'écrit pas, dis-le franchement et propose un spike à la place.
5. Découpe dans `NEXT.md` : milestones, tâches de 30 à 90 min (verbe + résultat vérifiable) pour M0 et M1 au moins. Chaque inconnue de « Risques » devient une tâche « comprendre » en M0.
6. Remplis la section « Projet » de `CLAUDE.md` (installer, lancer, vérifier, livrer). Ce qui n'est pas encore connu devient une tâche de M0.
7. Écris la prochaine action et mets la date dans `NEXT.md`.
8. Montre-moi un récapitulatif court. Après ma validation :
   - règle le dépôt GitHub avec la commande `gh repo edit` indiquée dans `GUIDE.md` (squash uniquement, suppression des branches fusionnées) ;
   - crée la branche `docs/cadrage`, commite `docs: cadrer le projet`, pousse et ouvre la pull request ;
   - fusionne seulement après mon « ok ».

Ne crée aucun fichier de production (code, workflow…) pendant le cadrage.
