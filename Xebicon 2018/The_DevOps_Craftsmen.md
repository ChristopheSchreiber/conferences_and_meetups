# The DevOps Craftsmen

## Abstract
Le contexte bancaire complexifie la marge de manœuvre pour mettre en place une démarche Devops : régulateurs, protection des données, ségrégation prod/dev, processus de validation sécurisé... Tout pourrait paraître contradictoire avec un concept de collaboration étroite entre les dev et les ops.

Nous allons vous présenter comment nous sommes devenus Devops, avons rendu l’ownership aux développeurs sur le pipeline de livraison en production sans sacrifier les aspects de sécurité et par la même occasion, avons réduit les coûts de livraisons.

Dans la deuxième partie de la conférence nous vous présenterons comment nous avons évité la catastrophe en mettant une bonne dose de Craftmanship dans le setup Devops.

## Speaker
Igor Lovich & Wilfried Willisek Faucounau
 
## Notes
Contexte: au départ, 3 grosses applications monolithiques, longues à livrer mais infra simple à gérer pour les ops

Maintenant : microservices (environ 60), résilient, faciles à builder, livrables rapidement, mais beaucoup de build à gérer, beaucoup de versions, dur à gérer pour les Ops

Challenge de faire ces changements dans une banque : pas d'accès aux images Docker publiques, contraintes de sécurité, contraintes des régulateurs, séggrégation dev/prod...

DevOps = mindset de collaboration entre Devs et Ops

Pour le mettre en place:
- améliorer boucle de feedback (monitoring, alerting, builds...)
- automatiser tout ce qui peut l'être (build, déploiement, monitoring...)
- responsabiliser les équipes

Pour parvenir à changer le mindset :
- passage en feature teams, dans le cadre de l'Agilité à l'échelle
- chapters :regroupements de communautés (ex: les testeurs)
- outils de communication : bannir les emails, utilisation de Symphony (similaire à Slack)
- colocalisation, les équipes sontsur3 sites
- organisation de BBL, meetups, hackaton

Guidelines & best practices:
- interdiction des taches manuelles, pas de checklists, procédures...
- Ops en mode craftsmanship (tests, clean code...)
- taches Ops pour les Devs (maintenir les environnements, responsables de leurs microservices...)

Il faut fournir aux Devs les outils pour réaliser ces taches, avec des wrappers simplifiant les APIs existantes, un générateur d'application...

Les conventions de nommage doivent être respectées pour identifier facilement le repo, les jobs Jenkins (générés automatiquement), les certificats... Permet aussi de faciliter les déploiements à partir de règles de nommage des branches.

Plus de 350 repositories à suivre, cela amène des contraintes => création d'outils opensource (GitHub Crawler & CI-Droid)

Développement d'un dashboard pour suivre pour chaque service, la version déployée sur chaque environnement et le hash Git correspondant, redéployer des versions...

Le monitoring se fait grâce à des index Elasticsearch, des dashboards Kibana sont créés pour exploiter ces données.

Applications des mêmes attentes en terme de qualité sur le code de l'outillage que sur le code des features

