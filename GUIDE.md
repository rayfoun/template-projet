# Guide : comment utiliser ce template

Lis ce guide en entier une fois. Ensuite, tu n'y reviens que pour les checklists.

## Les 6 principes

1. **Écris-le, ne le retiens pas.** Objectif, décisions, prochaine action : tout vit dans le dépôt. Ta tête sert à réfléchir, pas à stocker.
2. **Un seul projet actif.** Les autres attendent dans `IDEES.md` (voir « Avant le projet »).
3. **Petit et fini bat grand et ambitieux.** Une v1 moche qui marche vaut mieux qu'une v3 imaginée.
4. **La prochaine action est toujours écrite.** Tu ne quittes jamais une session sans elle.
5. **Tu décides, l'IA exécute.** Tu dois pouvoir expliquer en quelques phrases tout ce que tu livres.
6. **Ce qui se répète deux fois devient un modèle** : une recette, un script ou une commande.

## Les fichiers

| Fichier | Rôle | Quand tu l'écris | Temps |
|---|---|---|---|
| `PROJECT.md` | Le cadrage, ta boussole quand tu doutes | Une fois au début, rarement ensuite | 45 min |
| `NEXT.md` | Où j'en suis, prochaine action, tâches, « Plus tard » | À la fin de **chaque** session | 5 min |
| `DECISIONS.md` | Les choix faits et pourquoi | À chaque choix non évident | 2 min |
| `GLOSSAIRE.md` | Ce que tu as dû comprendre | À chaque notion nouvelle | 1 min |
| `RETRO.md` | Le bilan, même en cas d'abandon | À la clôture | 20 min |
| `README.md` | Pour les autres : quoi, installer, lancer | À la fin (milestone M3) | 20 min |
| `CLAUDE.md` | Les règles pour l'IA | Au cadrage, puis à chaque erreur répétée de l'IA | 5 min |
| `notes/` | Recherches, brouillons, comparatifs, spikes internes | Quand tu en as besoin | — |
| `recettes/` | Ce que tu as appris à faire pour un type de projet | Après une rétro | — |

## Trois façons de travailler (tu peux en changer à chaque session)

- **Seul** : tu suis les checklists de ce guide et tu remplis les fichiers à la main.
- **Avec Claude Code** : tu tapes la commande indiquée à côté de chaque checklist (`/cadrer`, `/debut`, `/tache`, `/fin`, `/livrer`, `/retro`). L'IA applique **exactement** la même checklist, puis tu relis.
- **Avec une autre IA** (ChatGPT, Cursor…) : dis-lui « Lis `CLAUDE.md` et applique la checklist *X* de `GUIDE.md` ».

Les fichiers sont la seule source de vérité. Les commandes ne sont que des raccourcis.

---

## Phase 0 : avant le projet, l'idée

Une idée n'est pas un projet. Elle va dans `IDEES.md`, un fichier unique dans un dépôt séparé `lab`. Une ligne par idée :

```markdown
- 2026-11-05 · Agent qui trie mes factures · pourquoi ça m'excite : apprendre LangGraph
```

**Choisir le prochain projet**, seulement quand le projet actif est livré, en pause ou abandonné. Note chaque idée de 1 à 3 sur ces critères :

| Critère | Question |
|---|---|
| Envie | En aurai-je encore envie dans 2 semaines ? |
| Apprentissage | Est-ce que j'apprends quelque chose de précis ? |
| Faisabilité | Une v1 tient-elle en 2 à 4 semaines de soirées ? |

Le meilleur total gagne. Si rien ne dépasse 6/9, fais un **spike**.

**Spike** : un test rapide (nouveau modèle, nouvelle lib), limité à 2 à 4 h, dans `lab/spikes/AAAA-MM-JJ-nom/`. Pas de cadrage. À la fin, tu écris 5 lignes de conclusion dans un `CONCLUSION.md`. Ce template n'est **pas** fait pour les spikes.

---

## Phase 1 et 2 : démarrer un projet (≈ 1 h 30) · `/cadrer`

- [ ] Créer le dépôt depuis le template, nom `AAAA-nom-du-projet`, **privé** : sur GitHub avec **Use this template**, ou en une commande `gh repo create AAAA-nom-du-projet --template rayfoun/template-projet --private --clone`. Puis l'ouvrir dans VS Code.
- [ ] Régler le dépôt pour n'autoriser que « Squash and merge » et supprimer les branches fusionnées : `gh repo edit --enable-squash-merge --enable-merge-commit=false --enable-rebase-merge=false --delete-branch-on-merge` (ou Settings → General → Pull Requests).
- [ ] Regarder dans `recettes/` s'il existe une recette pour ce type de projet.
- [ ] Remplir `PROJECT.md` (45 min). Les consignes sont dans le fichier.
- [ ] **Test de sortie** : si la définition de terminé ne s'écrit pas, c'est encore une idée. Retour en Phase 0 ou spike.
- [ ] Découper dans `NEXT.md` :
  - 3 à 5 milestones (M0 Squelette, M1 Le cœur, M2 Robuste, M3 Utilisable) ;
  - des tâches de 30 à 90 min pour M0 et M1 au moins ;
  - chaque inconnue de la rubrique « Risques » devient une tâche *comprendre* en M0.
- [ ] Remplir la section **Projet** de `CLAUDE.md` à partir des réponses de « Comment ça marche concrètement ».
- [ ] Écrire la **prochaine action** dans `NEXT.md`.
- [ ] Commiter le cadrage sur une branche `docs/cadrage` (`docs: cadrer le projet`), pull request, relecture, fusion. Même le cadrage passe par une PR : `main` ne reçoit jamais de commit direct.
- [ ] Bloquer les sessions des 2 prochaines semaines dans ton agenda.

**Une bonne tâche** commence par un verbe, a un résultat vérifiable et tient en une session.
Mauvais : « Faire l'agent ». Bon : « Écrire la fonction qui extrait le montant d'un PDF + 3 tests ».
Si une tâche te fait hésiter avant de la commencer, elle est trop grosse : découpe-la encore.

---

## Phase 3 : la boucle de session

### Entrer (5 min) · `/debut`

- [ ] `git status` est propre ? Revenir sur `main` et faire `git pull`.
- [ ] Lire `NEXT.md` : la prochaine action te dit quoi faire.
- [ ] Choisir **une** tâche et créer sa branche : `git switch -c feat/nom-court`.
- [ ] Écrire en une phrase ce que « fini » veut dire pour cette session.

### Faire la tâche (60 à 120 min) · `/tache <la tâche>`

- [ ] Si la tâche touche plusieurs fichiers ou un choix d'architecture : **plan d'abord**, validé avant d'exécuter.
- [ ] Avancer par petits pas. Commit dès qu'un morceau marche (toutes les 20 à 40 min).
- [ ] Vérifier avec la commande « Vérifier » de `CLAUDE.md` avant de dire que c'est fini.
- [ ] Une idée nouvelle surgit ? Une ligne dans « Plus tard » de `NEXT.md`, puis tu reviens à ta tâche.
- [ ] Une notion nouvelle ? Une ligne dans `GLOSSAIRE.md`. Un choix non évident ? Une entrée dans `DECISIONS.md`.
- [ ] Bloqué plus de 20 min ? Écrire le problème dans `NEXT.md`, puis découper, demander à l'IA ou changer de tâche.
- [ ] Tâche finie : cocher la tâche dans `NEXT.md`, push, pull request vers `main`, **relire le diff entier**, puis « Squash and merge ». Tu fusionnes toi-même sur GitHub, ou tu dis « ok » à l'IA qui fusionne pour toi.

### Sortir (5 min, non négociable, même si rien n'est fini) · `/fin`

- [ ] Commiter ce qui existe, même incomplet : `wip: extraction OK, reste le format européen`.
- [ ] Mettre à jour `NEXT.md` :
  - **Prochaine action** : précise et physique. Pas « continuer l'extraction » mais « gérer les virgules dans `parse_amount()`, le test existe déjà dans `test_parse.py` ».
  - **Où j'en suis** : 2 phrases.
  - **Blocages / questions ouvertes.**
- [ ] Vérifier que `DECISIONS.md` et `GLOSSAIRE.md` sont à jour.
- [ ] `git push`.

**La règle d'or** : la prochaine action doit être si claire que tu pourrais la commencer fatigué, un dimanche soir, sans réfléchir.

### Chaque semaine (15 min)

- [ ] Relire `NEXT.md` : le milestone avance-t-il ? Les tâches sont-elles encore assez petites ?
- [ ] Relire la timebox de `PROJECT.md`. À 80 % du temps, tout ce qui ne sert pas la définition de terminé part dans « Plus tard ».
- [ ] Deux semaines sans progrès : décider pause ou abandon (Phase 5). Un choix, pas une fatalité.

---

## Git : les règles fixes

1. **`main` marche toujours.** On ne travaille jamais directement dessus.
2. **Une tâche = une branche** : `feat/…`, `fix/…`, `docs/…`, `exp/…`.
3. **Un commit = une chose qui marche**, ou une sauvegarde `wip` de fin de session. Si le message a besoin d'un « et », fais deux commits.
4. **Une branche finie = une pull request**, même seul. C'est là que tu relis ce que l'IA a produit. L'IA peut fusionner, mais seulement après ton « ok » explicite pour cette PR.
5. **Squash and merge** : les `wip` disparaissent et `main` reste propre.

Format des messages : `type: ce que ça fait`, à l'impératif, en moins de 70 caractères.

| Type | Quand | Exemple |
|---|---|---|
| `feat` | Nouvelle fonctionnalité | `feat: extraire le montant des factures` |
| `fix` | Correction | `fix: gérer les PDF sans texte` |
| `refactor` | Réorganisation, même comportement | `refactor: séparer lecture et écriture` |
| `test` | Tests | `test: couvrir les montants avec virgule` |
| `docs` | Documentation, `NEXT.md`, décisions | `docs: mettre à jour la prochaine action` |
| `chore` | Configuration, dépendances | `chore: ajouter pytest` |
| `exp` | Expérience, benchmark, notebook | `exp: comparer 3 modèles sur 20 cas` |
| `wip` | Sauvegarde de fin de session | `wip: regex OK, reste le format européen` |

Le cycle d'une tâche, à la main :

```bash
git switch main && git pull
git switch -c feat/nom-court
# ... travail ...
git add -p                      # relire chaque morceau avant de l'ajouter
git commit -m "feat: ..."
git push -u origin feat/nom-court
gh pr create --fill                     # ou sur GitHub : « Compare & pull request »
# relire le diff sur GitHub, puis :
gh pr merge --squash --delete-branch    # ou le bouton « Squash and merge »
git switch main && git pull
```

**Filets de sécurité**

- Les secrets vont dans `.env` (ignoré par Git) ; seuls les noms de variables vont dans `.env.example`.
- Un secret a été commité ? **Le révoquer immédiatement** chez le fournisseur, puis nettoyer l'historique.
- Paniqué ? `git stash` met tout de côté, `git log --oneline` montre où tu es, `git reflog` retrouve presque tout. Rien n'est perdu tant que c'est commité.

---

## Phase 4 : livrer · `/livrer`

- [ ] Chaque critère de la définition de terminé de `PROJECT.md` est vérifié, et coché.
- [ ] Ce qui est prévu dans « Qu'est-ce que je livre ? » de `PROJECT.md` existe.
- [ ] La commande « Vérifier » de `CLAUDE.md` passe sur `main`.
- [ ] Je sais expliquer en quelques phrases comment ça marche, et `GLOSSAIRE.md` couvre les notions clés.
- [ ] `README.md` est rempli : quoi, installer, lancer, un exemple de résultat. Lisible en 5 minutes.
- [ ] Aucun secret ni donnée sensible dans le dépôt, historique compris. `.env.example` est à jour.
- [ ] Tag et release : `git tag v1.0.0 && git push --tags`, puis une release GitHub avec 3 lignes de notes.
- [ ] Optionnel : une démo (capture, GIF ou courte vidéo) dans le README.

Coupe le périmètre, pas la qualité minimale. Une fonctionnalité de moins, oui. Un README absent, non.

## Phase 5 : clôturer (20 min, même pour un abandon) · `/retro`

- [ ] Remplir `RETRO.md` et choisir un statut :
  - **Livré** : la définition de terminé est cochée. Une v2 éventuelle sera un **nouveau** cadrage.
  - **En pause** : bonne idée, mauvais moment. `NEXT.md` est ultra précis pour la reprise.
  - **Abandonné** : tu as appris ce que tu voulais, ou l'envie est partie. Ce n'est pas un échec, c'est une décision.
- [ ] Mettre à jour le statut dans `PROJECT.md`.
- [ ] Reporter dans le **dépôt template** ce qui doit l'améliorer (voir « Faire évoluer le template »).
- [ ] Archiver le dépôt sur GitHub si le projet est livré ou abandonné.

Un projet clôturé proprement ne pèse plus sur ta tête. C'est ce qui libère la place pour le suivant.

---

## Quand ça coince

| Situation | Protocole |
|---|---|
| « Je ne sais plus où j'en étais » | Lire `NEXT.md`, puis `git log --oneline -10`. Si `NEXT.md` est vide ou périmé, le réécrire **avant** de coder (ou `/debut`, qui le reconstitue). |
| « Il y a trop de choses » | Une seule question : quelle est la plus petite chose qui fait avancer le milestone actuel ? Fais-la. Le reste va dans « Plus tard ». |
| « Je suis embrouillé » | Arrête de produire. Écris en 5 lignes dans `notes/` comment ça devrait marcher. Si tu n'y arrives pas : spike d'1 h, puis une décision dans `DECISIONS.md`. |
| « Je ne sais pas si c'est la bonne approche » | 30 min pour comparer 2 options, puis tu choisis, tu notes dans `DECISIONS.md` et tu avances. Un choix réversible ne mérite pas plus. |
| « L'IA tourne en rond » | `git restore .`, nouvelle conversation, tâche plus petite, avec un exemple d'entrée et de sortie attendues. Si c'est une erreur répétée, une ligne dans `CLAUDE.md`. |
| « Je n'ai pas envie » | Règle des 15 minutes : un minuteur, et seulement la prochaine action. Si c'est toujours non, rituel de sortie et repos, sans culpabilité. |
| « Je n'y ai pas touché depuis 2 semaines » | Session de reprise de 30 min : lire `PROJECT.md` et `NEXT.md`, relancer le projet, choisir une tâche minuscule. Ou décider pause / abandon. |
| « Un nouveau projet me tente » | Une ligne dans `IDEES.md`. Si l'envie tient 2 semaines, clôture d'abord le projet actuel, même par un abandon. |

---

## Faire évoluer le template

Ce template est volontairement minimal : il ne prévoit aucun type de projet à l'avance. Il grandit avec tes vrais projets.

- **Recettes** : quand tu as fait **deux** projets du même type (N8N, agent, app web, data…), extrais ce qui s'est répété dans `recettes/<type>.md` du dépôt template. Le format est dans `recettes/README.md`.
- **Erreurs de l'IA** : une erreur qui revient dans tous les projets passe du `CLAUDE.md` du projet à celui du template.
- **Le guide lui-même** : chaque rubrique « Ce que je change dans mon système » de `RETRO.md` se traduit par une modification ici. On fait ces modifications dans le dépôt template, avec une branche et une pull request comme pour n'importe quel projet.
