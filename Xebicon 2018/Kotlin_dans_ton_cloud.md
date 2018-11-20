# Kotlin dans ton cloud

## Abstract
Kotlin est un excellent langage , mais comment le propulser sur son provider cloud favori ?

Que ce soit sur AWS ou GCP cette Konférence vous montrera les techniques, astuces et avantages du langage pour des déploiements en mode IaaS, PaaS et bien sur Serverless.

Nous montrerons également, comment Kotlin permet d'écrire du code "propre" tout en minimisant le vendor lock-in.

## Speakers
Benjamin Lacroix & Paul-Guillaume Déjardin

## Notes
Pourquoi Kotlin ?
- Plus élégant que Java, plus simple que Scala, concis et intéropérable, techno stable.
- Null safety
- Immutabilité
- Concision, avec les data class par exemple
- Extensions
- coroutines, default values pour paramètres...

### Google Cloud Platform
Google fournit de la doc pour utiliser Kotlin sur GCP (Google Cloud Platform). GCP demande un WAR et tourne avec Java 8.

Pour écrire les fonctions : Ktor. Pour les lancer: AppEngine.

Isolation du code spécifique au cloud provider avec les extensions.

### Amazon Web Services
AWS demande un fat jar (code de l'appli + ses dépendances) et tourne avec Java 8. Déploiement avec Serverless.

Serverless & JVM: cold start (environ 1s à chaque appel de la Lambda), mais perfs similaires à Go (et plus constantes que les langages dynamiques)

### Microsoft Azure
Ne gère que Maven, pas Gradle. Java n'est qu'en preview.

Il faut créer un fat jar et plusieurs fichiers de conf (host.json, local.settings.json, build.gradle). Il faut dans le répertoire de resources un répertoire correspondant au nom de la fonction.

### Autre
- Kotlin fonctionne avec Docker (Ktor, Spring Boot...)
- Peut tourner sur iOs grâce à Kotlin Native
