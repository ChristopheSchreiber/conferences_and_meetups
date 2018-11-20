# Modern Infrastructure

## Abstract
Vous avez beau avoir modernisé vos applications, les avoir rendu stateless, 12factor-compliant, etc., si vous n'avez pas l'infrastructure pour les déployer proprement et les gérer, votre bénéfice final sera fortement amoindri.

Cette conférence a pour but de vous faire ressortir avec une définition et une vision claires des principaux concepts qui caractérisent une infrastructure moderne. Nous y parlerons Configuration Management, infrastructure immuable, infra-as-Code, orchestration, self-healing, systèmes distribués, applications Cloud Native, Serverless ... et ce n'est qu'un avant goût !

## Speakers
Alexis "Horgix" Chotard

## Notes
Résilence, scalabilité, isolation

Beaucoup de VMs => beaucoup de conf, d'actions manuelles, d'erreurs => automatisation avrec des scripts shell

Scripts shell = peu maintenables => passage à des outils de configuration management (ex : Puppet), avec un agent sur la VM

- Automatiser setup de machines existantes
- Description textuelle
- Outillage pour comprendre la conf, prendre les actions et mettre les machines dans l'état attendu

Mais il faut toujours s'occuper du hardware (serveurs, disques, hyperviseur...) => le cloud permet de considérer ces points comme des commodités mises à disposition, location de ressources
=> Infrastructure as a Service (ex : AWS)

Plus scalable, plus rapide pour avoir une VM, SLAs, couts plus simples à planifier

Mais la manipulation de la console est manuelle et répétitive, à automatiser => utilisation des API des cloud providers => Infrasture as Code

Outils qui utilisent les APIs d'Amazon pour décrire les VM, liens réseaux... ex: Terraform

Pour éviter de devoir appliquer la conf sur chaque instance: faire une image d'une VM fonctionnelle, qui sera déployée en utilisant Ansible

Difficultés en cas d'erreur de conf dans Ansible ? Utiliser Packer pour configurer les instances
=> Immutable Infrastructure: ne rien changer au runtime et passer les images sur les environnements

Pour éviter de perdre les logs des VM supprimées : les stocker dans Elasticsearch plutôt que sur les instances, avec un dashboard pour s'y connecter
=> centralisation des logs

Pour avoir des VM localement pour ne pas dépendre de la connexion au réseau : utilisation de Vagrant. Mais les VM sont lourdes => utilisation de containers Docker

Même notion d'image, avec des outils pour les décrire et construire, stockées dans Docker Hub

Réutiliser les machines locales (serveurs) pour avoir la même chose avec OpenStack ? => orchestration de containers, avec Kubernetes

En utilisant les instances Kubernetes d'Amazon, plus besoin de Packer et Ansible, accès direct aux APIs Kubernetes

## Conclusion
Infra moderne :
- images immuables, que ça soit des VM ou des containters, sur le cloud ou non
- automatisation de A à Z, Infra as Code, tout versionner dans Git, CI/CD
- observable : logs centralisés, métriques
- outillage intelligent
- gain en sécurité
- Functions as a Service 