# StarTECH DevOps - Présentation Octopus Deploy

Système de déploiement automatique et gestion de release.

Développé en C#.

Simplifier le déploiement des applications, sur des VM (Windows, Linux), sur le cloud (Azure, AWS)

Définir le process de déploiement : environnements, applications, rôle de l'utilisateur...

## Vocabulaire
- Octopus Server : master & agents
- Tentacules : agents installés sur chaque machine
- Users, Teams
- Environnements
- Lifecycles: workflow de déploiement, successions des étapes et environnements
- Project : application à déployer
- Process : flux de déploiement
- Release : une image de l'application
- Variables: configurations liées à l'environnement

## Flux typique

Dev -> Git -> Jenkins -> Repo d'artifact -> Octopus Deploy

## Fonctionnement
Le server communique avec les serveurs cibles par les tentacules

La Communication Server/Tentacules peut se faire suivant 2 modes :
- Listening tentacules: la tentacule écoute sur un port (serveur TCP), le serveur est un client TCP. Mode recommandé
- Polling tentacules: récupération sur le serveur régulièrement

Plusieurs rôles prédéfinis pour définir les taches qui peuvent être réalisées (environment manager, environment viewer, project contributor...). On peut en créer des spécifiques.

## Bénéfices
- S'intègre bien aux pipelines existants (Jenkins, TFS...). Permet de déclencher un déploiement après un build
- Permet de faire de la promotion de build entre environnements
- Déploiements répétables et continus
- Facilite les déploiements complexes grâces à des taches hautniveau pour Java, .Net, Node.js...
- Dashboard intuitif pour le suivi des déploiements
- Scalabilité: cluster de serveurs et load balancer, configuration partagée entre les noeuds

## Gestion
Octopus Manager : application qui gère le serveur (arrêt/démarrage du service, import/export des données...)

Dashboard : vue pour chaque projet, avec la version courante par environnement, déploiements en cours

Infrastructure : gestion des environnements, des tentacules

Sur les machines cible : Tentacule Manager pour gérer l'agent installé localement

Depuis le dashboard, on peut faire un healthcheck des agents

