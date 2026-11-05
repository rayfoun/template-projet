# <Nom du projet>

<!--
Le cadrage du projet. Une page maximum, 45 min.
C'est ta boussole : quand tu doutes, tu la relis. Les commentaires comme celui-ci
sont des consignes : tu peux les supprimer au fur et à mesure.
Avec Claude Code : /cadrer remplit ce fichier avec toi en te posant des questions.
-->

- **Statut :** cadrage
<!-- cadrage | en cours | livré | en pause | abandonné -->
- **Dépôt :** AAAA-nom-du-projet

## Pitch
<!-- Une phrase : ce que ça fait, pour qui.
Ex. : « Un agent qui lit mes mails de factures et remplit un Google Sheet, pour moi. » -->

## Pourquoi
<!-- UNE raison principale : apprendre X, résoudre un vrai problème Y, portfolio.
Elle t'aide à trancher quand tu hésites sur le périmètre. -->

## Définition de terminé (v1)
<!-- 3 à 5 critères VÉRIFIABLES : quelqu'un d'autre pourrait les cocher sans te demander.
Ex. : « Je lance une commande, l'agent traite 10 mails, le Sheet a 10 lignes justes. »
Mauvais : « L'agent marche bien. »
Si tu n'arrives pas à écrire cette rubrique, c'est encore une idée : retour à IDEES.md ou spike. -->
- [ ]
- [ ]
- [ ]

## Hors périmètre v1
<!-- Tout ce que tu ne feras PAS. Aussi important que la rubrique précédente.
Ex. : interface web, multi-utilisateur, déploiement cloud, envoi par mail. -->
-

## Comment ça marche concrètement
<!-- Ces 3 questions remplacent les « types de projet » : elles s'appliquent à tout
(app, workflow N8N, agent, analyse de données…). Les réponses alimentent la section
« Projet » de CLAUDE.md. Si tu ne sais pas, note 2 options et fais-en une tâche de M0. -->

**Où vit le travail ?**
<!-- Ex. : code dans src/ · workflows N8N exportés en JSON dans workflows/ · prompts dans prompts/ · notebooks/ -->

**Comment je sais que ça marche ?**
<!-- La vérification, la plus automatique possible.
Ex. : `uv run pytest` · exécution du workflow avec fixtures/exemple.json · script qui rejoue 15 cas dans evals/ -->

**Qu'est-ce que je livre, et à qui ?**
<!-- Ex. : tag v1.0.0 + README · JSON importable + liste des credentials à créer · rapport Markdown -->

**Stack et accès**
<!-- Langage, outils, modèle d'IA, où ça tourne (local, cloud, instance N8N…).
Les comptes, clés et accès nécessaires (leurs NOMS seulement, les valeurs vont dans .env).
Choisis ce que tu connais, sauf si apprendre la techno est le but. -->

## Timebox
<!-- Ex. : 3 semaines × 3 sessions de 2 h. À 80 % du temps, tu coupes le périmètre. -->
- **Début :** AAAA-MM-JJ
- **Fin visée :** AAAA-MM-JJ
- **Rythme :** N sessions de N h par semaine

## Milestones
<!-- 3 à 5. Le détail des tâches vit dans NEXT.md. Adapte les noms au projet. -->
- **M0 Squelette** : environnement qui tourne, un « hello world » de bout en bout
- **M1 Le cœur** : la fonctionnalité principale, en version moche, sur un cas réel
- **M2 Robuste** : erreurs gérées, vérifications sur les cas clés
- **M3 Utilisable** : README, une façon simple de lancer, démo

## Risques et inconnues
<!-- Ce que tu ne sais pas encore faire ou ce qui peut mal tourner.
Chaque inconnue devient une tâche « comprendre » en M0 (avec une note dans notes/). -->
| Risque / inconnue | Impact | Action |
|---|---|---|
| | | |

## Ressources
<!-- Liens, docs, contacts utiles. -->
-
