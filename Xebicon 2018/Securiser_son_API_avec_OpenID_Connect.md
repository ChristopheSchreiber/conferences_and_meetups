# Sécuriser son API avec OpenID Connect

## Abstract
Nous entrons progressivement dans l’ère du temps réel et toutes les technologies nécessaires sont désormais à portée de mains, mais comment s’y prendre ? Quelles technologies choisir ? Nous allons vous montrer aujourd’hui comment créer facilement une application temps-réel qui scale ! Notre Stack ? Kubernetes, Google Container Engine, React, Redux et RethinkDB.

## Speakers
Damien Baron & Jérémy Pinsolle, développeurs back/cloud

## Notes
But : identifier la personne ou l'application connectée au service

Nouvelle norme, ne remplace pas OAuth2, a pour but de regrouper, préciser et compléter OAuth2

OAuth2 : authentification

OIDC : authentification + identification

Authentification = acess token

Identification = identity token (JWT, Json Web Token)

JWT : String en base 64 contenant :
- header: quand, par qui, expiration
- claims: infos supplémentaires (nom, mail, roles...)
- signature: vérifie l'intégrité du token

Utilisation
- côté client : Java, JS...
- serveur : AWS, Azure, Google Identity, Facebook, Keycloak, Auth0 (PaaS)