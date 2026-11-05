---
description: Sortir d'une session proprement (commit wip, NEXT.md, docs, push)
---

Applique la checklist « Sortir » de `GUIDE.md`. Ce rituel est non négociable, même si rien n'est fini.

1. Si des modifications ne sont pas commitées sur la branche de la tâche, commite-les. Utilise `wip: <où on en est>` si c'est incomplet, ou le bon type si c'est fini. Jamais sur `main`.
2. Réécris dans `NEXT.md` :
   - la date et le milestone en cours ;
   - **Prochaine action** : précise et physique, avec le fichier, la fonction ou l'étape exacte. Elle doit être faisable fatigué, sans réfléchir ;
   - **Où j'en suis** : 2 phrases ;
   - **Blocages / questions ouvertes** ;
   - les tâches cochées ou ajoutées, et les idées pour « Plus tard ».
3. Vérifie que les décisions prises et les notions découvertes pendant la session sont dans `DECISIONS.md` et `GLOSSAIRE.md`. Ajoute ce qui manque.
4. Si j'ai corrigé la même erreur de l'IA plusieurs fois pendant la session, propose une ligne pour « Erreurs à ne pas refaire » dans `CLAUDE.md`.
5. Commite la documentation (`docs: mettre à jour NEXT.md`), puis pousse la branche.
6. Montre-moi le nouveau `NEXT.md` en 5 lignes pour que je le valide.
