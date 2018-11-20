# Deno, le nouveau NodeJS qui inverse la tendance ?

## Abstract
Le créateur de NodeJS, Ryan Dahl, a décidé de créer un nouveau runtime pour Javascript : Deno. Son but ? Eliminer les erreurs et maladresses de son grand frère. Découvrez ce qui se cache derrière ainsi que la vision de son créateur.

## Speaker
Maxime Pichou, développeur back/cloud

## Notes
### NodeJS et son créateur
Deno présenté à la JS Conf Berlin en juin 2018.
NodeJS a été créé en 2009, pour utiliser côté back
Utilise NPM pour la gestion des dépendances

### Les erreurs de NodeJS
- Un seul repository centralisé pour les modules
- Trop de dépendances vers les modules
- Trop de boilerplate pour gérer les dépendances
- Build system : utilise GYP (Generate Your Project) depuis 2012, n'est pas passé à GN (Generate Ninja) qui est beaucoup plus rapide (x20)
- le fichier index.js, ajoute de la complexité dans le chargement de modules
- require sans extension
- ne meurt jamais sur les uncaught errors
- applis non sécurisées par défaut

### Les ambitions de Deno
- Support natif de Typescript 3.0
- Sécurité en mode sandbox
- Moteur V8
- Gestion des dépendances simplifiées
- Support de await au plus haut niveau
- Compatibilité avec les navigateurs
- Meurt sur les Uncaught errors

### Langages utilisés
- Typescripyt
- Rust
- C++
- Python

### Avancement
Très jeune, pas beaucoup de fonctionnalités terminées, une release par semaine, pas de date de sortie

Sécurité : on doit passer une option pour autoriser la création de fichier, l'accès au réseau...
Modules : import par URL (sans NPM), mais incompatible avec CommonJS, compatible avec l'import ESM ou AMD
Await : pas besoin d'encapsuler dans un async (pas encore implémenté)

### Roadmap
- TCP Server
- Lister les dépendances
- Public API (IO, setTimeout)
- Binding infrastructure entreV8 et libdeno
- await au plus haut niveau

### Conclusion
Beaucoup plus sécurisé, utilise Typescript, meilleure gestion des dépendances, buid system GN...
Mais incompatible avec NodeJS, gestion des dépendances adaptées sur les gros projets ?, gestion des droits trop binaire