---
description: Réaliser une tâche de NEXT.md (plan, petits pas, vérification, commits)
argument-hint: "<la tâche, ou rien pour la prochaine action>"
---

Applique la checklist « Faire la tâche » de `GUIDE.md`.

Tâche : $ARGUMENTS
(Si c'est vide, prends la prochaine action de `NEXT.md`.)

1. Vérifie qu'on est sur une branche dédiée à la tâche, pas sur `main`. Sinon, propose d'en créer une.
2. Reformule la tâche en une phrase avec son critère de réussite. Si elle dépasse 90 min ou reste floue, propose de la découper et mets à jour `NEXT.md`.
3. Si elle touche plusieurs fichiers ou un choix d'architecture : propose un plan en étapes numérotées, en précisant les fichiers touchés, et attends ma validation. Sinon, avance directement.
4. Exécute par petits pas. Après chaque étape qui marche :
   - lance la commande « Vérifier » de `CLAUDE.md` ;
   - fais un commit au bon format ;
   - explique en une ou deux phrases ce qui a été fait.
5. Pendant le travail :
   - une idée hors tâche va dans « Plus tard » de `NEXT.md` ;
   - une notion nouvelle va dans `GLOSSAIRE.md` ;
   - un choix non évident : propose 2 options, puis une entrée dans `DECISIONS.md` ;
   - si tu bloques ou tournes en rond, arrête-toi et dis-le plutôt que d'insister.
6. Quand le critère de réussite est atteint :
   - montre-moi un résumé du diff : ce qui change, pourquoi, comment je vérifie ;
   - coche la tâche dans `NEXT.md` et commite ;
   - pousse la branche et crée la pull request avec `gh pr create`, en donnant le lien ;
   - demande-moi un « ok » pour fusionner. Après mon « ok » seulement : `gh pr merge --squash --delete-branch`, puis `git switch main` et `git pull`.
