# Cloud AWS

## Abstract
Scalabilité, élasticité, fiabilité, flexibilité, pay as you go, IaaS, PaaS…Autant de mots qui sont fortement liés au Cloud.

Le cloud AWS fournit un grand nombre de services d'infrastructure, notamment de la puissance de calcul, des options de stockage, des fonctions de mise en réseau et des bases de données. Chaque service est disponible à la demande et en quelques secondes, et la tarification se fait selon votre utilisation.

## Lieu et dates
SOFTEAM, mardi 30 octobre 2018

## Notes
AWS est le service de cloud d'Amazon, depuis 2006.
Concurrents : Microsoft Azure, Google Cloud Platform
62% de PDM


### Infra Vs Cloud
- Infra : peu de licences, mais beaucoup de maintenance, besoin de locaux, mettre en place la redondance, difficile de provisionner l'évolution des besoins, scalabilité difficile
- Cloud : plus besoin de deviner les capacités, meilleure scalabilité, agilité, moins de couts de maintenance


### Modeles de déploiement
- Cloud public : AWS, Azue, GCP
- Cloud privé : cloud dans une entreprise
- Community cloud : similaire
- Hybrid cloud : une partie privée, une partie publique


### Sécurité
Contraintes de localisation des données, par exemple données qu'on ne veut pas stocker aux US -> le cloud peut être vu comme un frein pour les données critiques

AWS garantit que ses données et son infrastructure sont sécurisés, mais le client a la responsabilité de l'encryptage des données sensibles.


### Différents niveaux de service
- IaaS : Infrastructure as a Service, on demande un serveur au provider
- Paas : Platform as a Service, on délègue l'approvisionnement de toute l'infrastructure
- SaaS : Software as a service, tout un service est fourni. Ex: Dropbox, Office 365


### Localisation des serveurs
Régions : 4 en Europe, il faut voir s'il y a des contraintes réglementaires dans la région choisie
Dans les Régions, il y a des Availability Zones : datacenters assez éloignés, pour gérer les problèmes d'infrastructure qui peuvent survenir. Au moins 2 par région, 3 à Paris.
Edge locations : serveur réservés au caching

### Types de services proposés
#### Compute
- AMI (Amazon Machine Image) : créer une image à partir d'un disque et la démarrer. Pour créer un serveur identique à partir d'une image qui contient toutes les dépendances, créer un post de développeur contenant tous les outils nécessaires...
- Instances : VM pour héberger les serveurs, postes...
- Load Balancers : Classic, Application ou Elastic, s'interfacent avec des instances
- Auto-Scaling : définir les règles pour l'évolution de l'architecture, horizontale (ajouter des instances en cas de charge élevée par exemple, couper des instances la nuit...) ou verticale (changer la configuration d'une machine, par exemple augmenter ou diminuer la RAM, le CPU...)

Plus de 60 types d'instance EC2, avec différents types (génériques, compute optimized, stockage...).

EBS (Elastic Block Service) : disques SSD ou HDD, de 1Gb à 16 Tb, avec la possibilité de faire des snapshots (que l'on peut monter sur une autre instance)

Lambda : exécuter une fonction, sur une instance, puis l'espace pris par cette fonction est libéré, avec un cout abordable (gratuit pour le premier million d'appels par mois, puis 0.20$ par million.

Elastic Container Service : pour utiliser Docker

#### Stockage
- S3 (Simple Storage Service) : bucket illimité de stockage, avec des objets clé/valeur de 5To max. On paie l'espace consommé. Peut héberger un site web statique. Existence d'un mode Infrequent Access si on accède rarement aux données (moins cher), possibilité de se limiter à une zone, forte garantie contre la perte de données. Possible de l'utiliser pour de l'archivage, plus lent (accès sous 3 à 5 heures, sur demande) mais moins cher.
- EFS : disque partagé par plusieurs serveurs
- AWS Sorage Gateway : pour du cloud privé par exemple
- Snowball envoyer des disques vers un datacenter

#### Database
- RDS (Relational Database Services) : héberger une BDD en PaaS (Amazon Aurora, Oracle, PostgreSQL, MariaDB, SQL Server...). On ne gère pas l'infrastructure. Pour migrer les données : Amazon DMS (copier et convertir les données vers le cloud).

Aurora utilise PostgreSQL ou MySQL, avec des meilleures performances (respectivement x3 et x10 selon Amazon)

- Amazon DynamoDB : base NoSQL, event driven programming pour s'interfacer avec Lambda
- Amazon Redshift, pour les data warehouses (en Paas)

#### Networking
- VPC : pour créer un espace logique isolé et dédié, faire des connexions VPN avec les datacenters de notre entreprise
- CloudFront : mise en cache sur des Edge locations
- Route 53 : pour l'enregistrement DNS, achat de noms de domaines sur Amazon, avec 5 routing policies (simple, geographical, par latence, failover, par poids)
- 3 types de load balancers
- Queing, notifications (email, http...)

#### Developer tools
CodeStar, CodeCommit, CodeBuild, CodeDeploy, CodePipeline, X-Ray