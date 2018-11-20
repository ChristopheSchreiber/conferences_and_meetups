# Comment j'ai développé un jeu vidéo avec des outils de développement web ?

## Abstract
Par curiosité, puis par passion, j'ai développé un jeu vidéo à l'aide des outils et frameworks habituellement utilisés dans des applications web.

Pas commun dites-vous ? Revenons ensemble sur la manière dont je m'y suis pris, les choix techniques et ce qui les a faits évoluer, les challenges et les compétences développées au cours de cette aventure.

## Speakers
Alexandre Dergham, développeur fullstack

## Notes
Architectur
- Jeu : appli web en Angular 5
- Editeur de niveau en React
- Back: NodeJS
- BDD
- BabylonJS pour le rendu 3D

Composants Angular encapsulés dans des modules, qui reposent sur des services :
- ScreensModule : gestion des écrans du jeu
- SceneDisplayModule: affichage de la scène 3D
- GameModule: moteur de jeu

Méthodologie : TDD et refactoring, TDD s'applique très bien sur les algos déterministes

Challenges techniques :
- gestion du son et des évènements dans une appli web => utilisation de RxJS
- ajout et réutilisation de contenu => utilisation du design pattern strategy
- injection de dépendance => éviter les dépendances cycliques avec des dépendances runtime avec l'injecteur Angular
- Parseurs pour le game design => Ascii art, par exemple pour modéliser l'arbre de compétences
- level design => en JSON
- gestion de la mise à jour du modèle => Zone.js, réagir aux intéractions de l'utilisateur
- migration AngularJS vers Angular 5 => passage de Gulp à Webpack, de ES6 à Typescript...

## Conclusion
- Outils plutôt bien adaptés aux besoins
- Beaucoup de compétences techniques acquises, réutilisables en mission
- Compétences en 3D, musique...