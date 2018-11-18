# Retours sur la conférence XebiCon 2017 - Agile Smells
Pour cette première conférence de la journée, j'ai assisté à un talk de Julien Rossignol sur les Agile Smells, ces signes qui indiquent que quelque chose de va pas dans l'équipe.
Cette conférence reprenait une partie des (très  bons) articles qu'il avait publiés sur le [blog de Xebia](https://blog.xebia.fr/2017/03/15/agile-agile-smells-management-visuel/) en début d'année 2017.

## Absence de management visuel
Pour rappel, le management visuel consiste à utiliser les murs du bureau pour faire apparaitre des informations sur la vie de l'équipe : ses tâches en cours, ses objectifs, ses problèmes éventuels, etc. Cela permet en un clin d'oeil à chaque personne passant dans l'openspace de connaitre ce sur quoi travaille l'équipe.
Pour Julien Rossignol, un bureau d'équipe Agile où les murs sont vierges de tout post-it, burnown chart ou autre est un signe important de dysfonctionnement, cela pouvant signifier :
* Une pression externe de la part du management, ce qui pousse l'équipe à cacher les informations pour se protéger
* Un manque de vision produit et des objectifs à plus ou moins long terme, ce qui a tendance  à entrainer une perte de motivation de l'équipe
* l'emploi d'outils numériques uniquement, ce qui peut ne pas convenir à tout le monde et mobilise moins les membres de l'équipe lors des cérémonies.
Julien fournit un exemple de management visuel efficace :
![Managemet visuel](https://www.christopheschreiber.fr/blog/wp-content/uploads/2017/11/management_visuel.jpg)

Julien conclue cette partie en énonçant les 3 caractéristiques d'un bon espace de travail :
* audibilité : chacun doit pouvoir parler et entendre le reste de l'équipe sans souci
* visibilité : tous les membres de l'équipe doivent se voir
* isolation : il faut pouvoir discuter sans déranger le reste de l'équipe

## Taskboard : les user stories restent dans la colonne In Progress
Julien nous a décrit pour illustrer son propos un exemple simple : puisque les tâches restent dans la colonne In Progress une fois le développement achevé, ce faute de validation, on ajoute une colonne Validation.
On s'aperçoit ensuite qu'il serait bon d'ajouter une colonne Review, puis Test, puis Deploy...
La multiplication des colonnes est à nouveau le signe de problèmes dans l'équipe :
* la nécessité d'une étape de validation peut indiquer que le PO n'est pas assez présent
* il n'y a pas de bonnes pratiques de test
* il n'y a pas d'esprit d'équipe, ce qui fait que les reviews trainent à être réalisées
* il n'y a pas de profil OPS, ce qui ralentit la partie déploiement

Cela a aussi des conséquences sur le déroulement du Sprint :
* il y a beaucoup de stories en cours
* les stories ont tendance à faire des allers-retours entre les colonnes (par exempke In Progress -> Validation -> In Progresss -> Validation...)
* ce sont en fait des files d'attente déguisées
* cela ne favorise pas la collaboration au sein de l'équipe, puisque l'on ne fait pas en sorte de désengorger la colonne In Progress

Face à ce problème, Julien préconise les solutions suivantes :
* supprimer les colonnes inutiles. 4 colonnes peuvent tout à fait suffir dans la majorité des cas : Ready | Todo | In Progress | Done
* limiter le travail en cours (à la manière de la méthode Kanban afin de favoriser l'esprit d'équipe. Les développeurs devront s'entraider pour pouvoir ajouter de nouvelles stories, en pratiquant le pair programming, la revue de code...
* avoir si possible des équipes pluridisciplinaires, afin que chacun puisse toucher à tous les types de sujets, même s'il n'est pas forcément un expert dans le domaine

## Retards au morning meeting
Un grand classique que chaque équipe Scrum a sans doute connu :-P
Le mauvais réflexe consiste à décaler l'horaire de début de cette réunion quotidienne afin que tout le monde puisse y assister. Au bout de quelques temps, on devra redécaller car il y aura de nouveaux retards. Cela revient à traiter les symptomes, pas le problème lui-même. Il s'agit souvent d'un signe de manque d'intérêt de l'équipe pour ce rituel matinal.
Julien propose à nouveau quelques pistes pour résoudre ce problème :
* veiller à maitriser la durée du meeting, en limitant le temps de parole de chaque interlocuteur et renvoyer les discussions hors du daily meeting
* revoir le format : au lieu de donner la parole à chaque membre de l'équipe à tour de rôle, on peut par exemple parcourir la liste des stories en cours, chaque personne concernée prenant la parole pour apporter sa contribution au sujet, ce qui évite les allers-retours et les redites entre plusieurs personnes.On peut éventuellement essayer d'effectuer ce meeting de façon plus informelle, hors de l'openspace, autour d'un café... Même si cela n'est pas vraiment efficace d'après l'expérience de Julien.
* revoir l'organisation du Sprint : se fixer moins d'objectifs et avoir des stories cohérentes par rapport à ceux-ci, limiter le work in progress, favoriser le pair programming...
* si vraiment ce meeting est vu comme inutile par l'équipe, on peut carrément le supprimer, si les membres n'ont rien à se dire et sont déjà au courant du travail effectué par chacun (en particulier dans les petites équipes)
 
 ## Perte d'attention lors des réunions
 * L'attention moyenne d'un adulte étant suivant des études de 52 minutes, des réunions trop longues ont des effets néfastes sur les participants, qui ont alors tendance à perdre leur attention et à sortir leur téléphone... Julien préconise donc un devoir de déconnexion pour s'assurer que chacun reste mobilisé.
 * Comme vu précédemment, il faut limiter la durée du daily meeting
 * Le Sprint Planning doit être préparé en affinant le backlog. Il faut aussi éviter de parler trop de technique et se concentrer sur le métier, avec des estimations rapides.
 * La Sprint Review doit être préparée, répétée, afin d'avoir une présentation efficace, avec aussi peu de slides que possibles. Il n'est pas nécessaire d'entrer dans tous les détails de ce qui a été fait, testé ou pas, etc.
 * Lors des Rétrospectives, il est préférable de se concentrer sur un ou deux problèmes plutôt que d'essayer de tout résoudre.
 
 ## Rétrospectives où les problèmes de remontent pas et/ou les actions sont vagues
 Il faut faire attention à la routine. Si peu de points sont remontés, cela peut signifier que tout va bien, que les développeurs ont oublié les problèmes rencontrés pendant le Sprint, ou bien qu'ils jugent la rétrospective inutile.
 
 Il faut contextualiser les rétrospectives visà-vis de ce qu'il s'est passé durant le Sprint, en utilisant des formats adaptés.
   * Affecter des rôles aux gens
   * Définir des vraies actions (qui doivent être SMART)
   * Evaluer la rétrospective, pour savoir l'équipe a jugé la réunion utile
 
 ## Backlog trop détaillé
 Si on se retrouve avec un très long backlog, très détaillé, on est proche de ce qu'on aurait dans un cycle en V, puisque l'on aura tendance à suivre le plan initial, perdant ainsi les avantages de l'Agilité. De plus, si on jette toutes ces tâches pour les remplacer par de nouvelles plus à jour compte-tenu de ce qui a déjà été réalisé et d'éventuelles nouvelles contraintes/besoins, on perd le travail d'étude et les analyses techniques effectuées, ce qui peut être frustrant.
 Julien conseille d'avoir un backlog organisé en pyramides :
 * des stories détaillées pour les 2 ou 3 prochaines itérations
 * des features à un niveau moins détaillé pour la release en cours
 * des epics peu détaillées pour les futures releases
 
 On affinera le backlog et le détail des user stories au fil des itérations.
 
 ## Rôles peu clairs
 L'exemple le plus fréquent est le rôle du Scrum Master, qui peut être dificile à cerner pour l'équipe. Cela dénote d'un problème dans la structuration de l'équipe, et peut mener à des conflits et des tensions.
 
 Il convient alors de redéfinir le rôle afin de le clarifier :
 * On peut utiliser la méthode Stop / Start / Continue pour indiquer ce qui va, ne va pas ou qu'on aimerait mettre en place
 * Build your own Scrum Master : voir avec l'équipe ce qu'ils attendent de ce rôle
 
 Un autre rôle qui peut générer des doutes est celui du référent technique. S'il est trop présent, cela peut nuire à l'équipe car les développeurs perdront leur motivation à cause de leur perte d'autonomie, du manque d'apprentissage...
 
 Il peut alors être intéressant que le référent fasse du pair programming avec les membres de l'équipe, qu'il répartisse les analyses pour que chacun participe à tour de rôle, voire même d'avoir un rôle de référent technique tournant, jusqu'à ce que l'équipe soit suffisamment mature pour pouvoir se passer de ce rôle.
 
 ## Différence entre Coach Agile et Scrum Master
 Le Coach Agile :
 * Observe l'équipe
 * n'échange qu'avec le Scrum Master
 * peut animer une communauté de Scrum Masters
 * co-anime les ateliers avec le Scrum Master
 
 Il y a donc un risque de perte de légitimité pour le Scrum Master. Cela peut être le signe d'efforts uniquement dirigé vers l'organisation et le management. Dans ce cas, on peut se demander si une organisation Agile est suffisante.
 
 En effet, il ne faut pas oublier la partie technique :
 * ajouter un Coach Craft pour améliorer les pratiques de développement
 * cela passe aussi par l'amélioration de design et de tests
 * il faut aussi améliorer l'outillage lorsque le delivery pose problème (Devops)
 
 ## Conclusion
 Il ne faut pas se contenter de suivre aveuglément une méthodologie et ses rituels, il faut s'adapter à l'équipe et au contexte du projet.
 Il faut mesurer l'efficacité du processus mis en place, par exemple le temps passé par une story dans une colonne, et revoir en rétrospective ce que l'on peut améliorer quand ces mesures font ressortir des problèmes.
