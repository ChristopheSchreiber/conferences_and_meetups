# Architecturer son application mobile pour la durabilité

## Abstract
TODO

## Speaker
Jean-Christophe Pastant

## Notes
Une architecture n'a pas besoin d'être complexe pour être réussie.

Une bonne architecture :
- orientée vers le besoin fonctionnel
- pragmatique (construite pour le présent)
- code lisible et cohérent

Une architecture pérenne:
- robuste dans le temps face aux petites modifications
- évolutive pour permettre de grosses modifications

Structurer en couches :
- séparer les responsabilités (affichage, réseau...)
- réfléchirau rôle de chaque classe
- être plus ouvert aux changements

Exemple :
- Données : DB, webservices, cache
- Métier : règles business
- UI : layout, i18n, formattage...

Dépendances: UI -> Métier -> Données

Objets métier : faire des objets simples, orientés sur le métier

UI : passer aussi des objets métier, créer des petits composants réutilisables pour regrouper le traitement liés à un concept métier, exposer une API métier

Métier : smart components : encapsuler la logique métier, dans des composants facilement testables

Données : construire de petits objets pour avoir des APIs simples, en encapsulant le code complexe

Providers : rassemblent les repositories nécessaires pour exécuter une action, en chainant les appels

Injection de dépendances : pour garder les couches indépendantes et rendre le code testable

Test unitaires : si les écrire et difficile, revoir l'architecture pour rendre le code testable
