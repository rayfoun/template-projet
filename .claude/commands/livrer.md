---
description: Livrer la v1 (vérifier la définition de terminé, README, secrets, tag)
---

Applique la checklist « Phase 4 : livrer » de `GUIDE.md`.

1. Vérifie qu'on est sur `main`, à jour, sans modification en cours, et que toutes les branches de tâches sont fusionnées.
2. Pour chaque critère de la définition de terminé de `PROJECT.md`, vérifie-le réellement (commande, exécution, lecture), puis dis : ✅ vérifié, ❌ échoue, ou ❓ à vérifier par moi, avec comment.
3. Vérifie que ce qui est prévu dans « Qu'est-ce que je livre ? » existe.
4. Lance la commande « Vérifier » de `CLAUDE.md`.
5. Cherche les secrets et données sensibles dans les fichiers **et dans l'historique Git**. Vérifie que `.env.example` est à jour.
6. Vérifie que le `README.md` est rempli : quoi, installer, lancer, exemple, comment ça marche. Signale les manques. Si c'est à rédiger, fais-le sur une branche `docs/readme`.
7. Pose-moi 2 ou 3 questions pour vérifier que je sais expliquer comment ça marche. Complète `GLOSSAIRE.md` si besoin.
8. Donne-moi la liste de ce qui reste. S'il ne reste rien : propose les 3 lignes de notes de release, puis, après mon accord, crée le tag `v1.0.0` et pousse-le.
9. Propose de passer à `/retro`.
