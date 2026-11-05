---
description: Entrer dans une session de travail (état Git, NEXT.md, choix de la tâche, branche)
---

Applique la checklist « Entrer » de `GUIDE.md`.

1. Vérifie l'état Git : branche courante, modifications non commitées, retard sur le distant. Signale tout ce qui n'est pas propre et propose quoi en faire, sans rien supprimer.
2. Lis `PROJECT.md`, `NEXT.md` et `DECISIONS.md`.
3. Si `NEXT.md` est vide, périmé ou ne correspond pas aux derniers commits (`git log --oneline -10`), reconstitue l'état à partir de l'historique, propose-moi une version à jour de `NEXT.md` et attends ma validation.
4. Donne-moi en 5 lignes maximum :
   - où on en est (milestone, tâches faites) ;
   - la prochaine action ;
   - les blocages notés ;
   - les jours restants dans la timebox.
5. Propose la tâche du jour (celle de la prochaine action, sauf raison de faire autrement), le nom de sa branche, et une phrase qui dit ce que « fini » veut dire pour cette session.
6. Après mon accord : reviens sur `main`, mets-la à jour, puis crée la branche.
