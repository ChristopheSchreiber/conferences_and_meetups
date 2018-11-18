# Monitorer son application NodeJs dans un container

## Abstract
Sur l'un des tee-shirt Docker, il est écrit "The revolution will be containerized".

La révolution est en marche, mais comme pour toutes révolutions, elles laissent beaucoup de questions et de chaos.
Dans le cas de notre révolution, les outils pour la métrologie et les métriques évoluent. Pour Docker, il existe un outil appelé Prometheus qui remplit parfaitement ce rôle. Mais c'est au développeur d'envoyer les métriques (techniques, business).

Découvrez comment un développeur NodeJS peut envoyer ses métriques à Prometheus ainsi qu'un petit utilitaire que j'ai réalisé pour simplifier cette mise en place. 

## Notes