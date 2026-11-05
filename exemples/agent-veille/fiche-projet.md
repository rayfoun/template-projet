# Fiche projet

- **Nom du projet :** agent-veille
- **Date de début :** 2026-11-01
- **Statut :** cadrage

## Objectif
Un agent qui, chaque matin, lit mes sources d'information (flux RSS), garde ce qui correspond à mes centres d'intérêt, en fait un résumé court et me le livre sous forme d'un digest lisible en 5 minutes. Pour moi seul, afin de rester informé sans passer des heures à trier.

## Contexte
Projet d'apprentissage : tester la méthode (cadrer, produire avec l'IA, documenter, livrer) sur un petit agent complet. L'agent appelle un modèle d'IA via API pour filtrer et résumer.

## Livrable attendu
- Un script/programme qui s'exécute en une commande et produit `output/digest-AAAA-MM-JJ.md`.
- Une exécution automatique quotidienne (GitHub Actions ou cron).
- Un README expliquant l'installation et l'usage.
- Livraison cible : v1.0.0 sous 2 semaines.

## Critères de « terminé »
- [ ] La commande unique génère un digest à partir d'au moins 5 sources configurables (fichier `sources.yml`)
- [ ] Chaque article retenu a un titre, un résumé de 2 à 3 phrases et un lien
- [ ] Les articles déjà vus ne reviennent pas dans les digests suivants
- [ ] Mes centres d'intérêt se règlent dans un fichier de configuration, sans toucher au code
- [ ] L'exécution quotidienne automatique fonctionne 5 jours de suite
- [ ] Je sais expliquer en quelques phrases comment l'agent décide de garder ou d'écarter un article
- [ ] Le coût d'API d'une exécution est mesuré et inférieur à un seuil que je fixe (ex. 0,10 €)

## Contraintes
- Python, pour rester simple.
- Clé d'API dans `.env`, jamais dans Git.
- Coût maîtrisé : limiter le nombre d'articles envoyés au modèle.

## Hors périmètre
- Interface web, application mobile.
- Envoi par e-mail ou messagerie (possible en v2).
- Multi-utilisateurs.

## Risques et inconnues
| Risque / inconnue | Impact | Plan B ou action |
|---|---|---|
| Flux RSS indisponible ou mal formé | Digest incomplet | Ignorer la source et le consigner dans un log |
| Coût d'API qui dérive | Budget dépassé | Plafond d'articles par exécution, mesure du coût |
| Résumés inexacts | Perte de confiance | Toujours afficher le lien source ; relire un échantillon |
| Je ne comprends pas le fonctionnement d'un agent | Livrable subi | Phase « Comprendre » + glossaire avant de produire |

## Ressources
- Documentation de l'API du modèle utilisé
- Liste de mes sources (à lister en phase 1)
