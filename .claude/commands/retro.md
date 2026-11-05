---
description: Clôturer le projet (RETRO.md, statut, améliorations du template)
---

Applique la checklist « Phase 5 : clôturer » de `GUIDE.md`. Elle vaut aussi pour une pause ou un abandon.

1. Rassemble les faits :
   - `PROJECT.md` (timebox, terminé) ;
   - `NEXT.md` (Plus tard, blocages) ;
   - `DECISIONS.md` ;
   - `git log` (nombre de sessions, durée réelle).
2. Pose-moi les questions de `RETRO.md` une par une, puis rédige-le avec **mes** réponses. Ajoute tes observations sous un intertitre « Observations de l'IA », séparé de mes réponses.
3. Mets à jour le statut dans `PROJECT.md`. Si le projet passe « en pause », vérifie que `NEXT.md` permettra de reprendre sans réfléchir.
4. Pour « Ce que je change dans mon système », propose des modifications concrètes à faire dans le **dépôt template** : `GUIDE.md`, `CLAUDE.md`, modèles, et une recette si ce type de projet en est à sa 2e occurrence. Rédige-les pour que je n'aie plus qu'à les copier.
5. Commite sur une branche `docs/retro`, ouvre la pull request et fusionne après mon « ok ». Si le projet est livré ou abandonné, propose ensuite d'archiver le dépôt (`gh repo archive`) et attends mon accord.
