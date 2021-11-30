**Consommation RAM : Firemin sous Windows** disponible ici (https://www.rizonesoft.com/downloads/)
Ce logiciel permet d’empêcher Firefox de dépasser une quantité de RAM donnée. 
Fini les fuites de consommation de mémoire vive par votre navigateur. 
Même si la gestion de la RAM de Firefox a évolué avec les années, elle est toujours loin d’être parfaite. 
Il y a plein de cas de figure dans lequel l’usage de ce logiciel me semble pertinent. 
L’utilisation de son navigateur sans jamais le fermer pendant des jours, l’ouverture d’une quantité d’onglets importante, et l’usage sur des machines avec peu de mémoire vive (inférieur à 4Go) pour éviter d’utiliser la swap sont trois cas où Firemin peut vous aider. 
Le site continent beaucoup d’informations au sujet de ce soft, notamment sa genèse, et pourquoi il ne produit pas d’effet placebo inutile. 
Il existe également une autre version générique qui peut également servir pour d’autres applications sur laquelle vous souhaitez borner la consommation de RAM.


**Accélération BDD : SpeedyFox** disponible ici (https://crystalidea.com/speedyfox)
Ce logiciel permet d’alléger les bases de données SQLite que Firefox (et autres) utilise. 
Le démarrage des applications qui utilisent de telles bases de données prend du temps et la vitesse globale est affectée. 
C'est un problème très courant et il se produit en grande partie à cause de la fragmentation des bases de données. 
Avec le temps, les bases de données SQLite ralentissent considérablement. 
SpeedyFox est capable de résoudre ce problème en un seul clic, sans réduire la quantité de données présente dans les bases de données. 
Ce boost de vitesse d’exécution et de chargement des pages sera surtout ressenti sur un navigateur servant beaucoup, ou dont l’installation est datée. 
C’est l’un des rares logiciels de ce genre qui a lui aussi survécu à l’épreuve du temps, et qui présente encore un intérêt en 2021.

**Bloqueur de nuisances : uBlock Origin** disponible dans le magasin d’extensions Firefox.
Probablement le meilleur bloqueur de pubs à ce jour, et ce pour deux raisons. 
La première, c’est la neutralité des listes de filtrage des nuisances par rapport à Adblock qui autorise certaines publicités soi-disant non intrusives. 
La deuxième raison concerne les ressources nécessaires, nettement en dessous de celles d’Adblock. 
Disponible ici : (https://addons.mozilla.org/fr/firefox/user/11423598/) vous aurez également une vue sur les autres outils de Raymond Hill, l'éditeur de l'extension.

**Complément à uBlock Origin : Decentraleyes ou LocalCDN** (fork de Decentraleyes). Page de l’extension ici pour la première et là pour la seconde. 
Extension de Firefox qui a pour but de protéger encore un peu plus du pistage lié aux diffuseurs de contenus « gratuits », centralisés, appelés aussi CDN. 
Le principe ici est gagnant-gagnant puisque des requêtes sont évitées et assurées localement à la place, accélérant le chargement de certaines pages web. 
Disponible ici (https://addons.mozilla.org/fr/firefox/user/6937656/) ou ici (https://addons.mozilla.org/fr/firefox/user/15698979/)

**Le cas NoScript** : cette extension est selon moi très controversée, et ce pour une simple raison ; elle est redoutable, trop redoutable. 
Vous n’imaginez pas toute la protection que cette extension peut apporter. 
Mozilla eux-mêmes ont beaucoup appris grâce à la communauté autour de NoScript. 
Etant plus jeune je l’ai beaucoup utilisé, à l’époque où il n’y avait pas vraiment de bloqueur de nuisances compétent sur le marché. 
C’est probablement l’une des plus vieilles extensions de Firefox à exister (de mémoire c’est 2004, mais qu’importe elle est toujours maintenue à l’heure actuelle…)
Il nécessite une configuration « au feeling » dont je ne peux tout simplement pas verbaliser la méthodologie (je n'en ai que de très vagues souvenirs d'ailleurs)
Une terminologie qui n'est digérable que par une certaine catégorie de personnes. 
Toutefois si vous voulez y jeter un coup d'oeil je partage le lien de l’extension ici (https://addons.mozilla.org/fr/firefox/user/143/)

**Le cas HTTPS Everywhere** : cette extension n’a AUCUN intérêt depuis Firefox 83.
Il embarque un paramètre que vous trouverez dans Paramètres ==> Vie privée et sécurité ==> Mode HTTPS uniquement ==> cocher Activer le mode HTTPS uniquement dans toutes les fenêtres.
Notez que ceci ne vous empêche en aucun cas d’accéder à des pages commençant par HTTP. 
Firefox tentera de surclasser la connexion en HTTPS quoi qu’il arrive et vous signalera s’il n’y arrive pas.
Le cas des extensions visant à vous protéger des liens visités : Pour être honnête, il n’y a pas meilleure protection que la réflexion avant de cliquer. 
Je partage quand même le lien ici https://addons.mozilla.org/fr/firefox/user/5474073/)
La raison est simple : si l'extension citée plus haut est d'une inutilité importante, Privacy Badger pourrait être l'alternative interactive à un bloqueur de nuisances.


Toutefois il existe des solutions permettant de vous donner une idée de la réputation du site, et si vous devriez cliquer ou pas. 
J’en ai testé deux. **Wot (Web Of Trust)** étant l’une d’entre elles, un projet qui a su faire ses preuves avec le temps. 
Ses résultats sont plutôt bons, mais pas forcément infaillibles. 
Par contre si vous lisez la page Wikipédia de cette extension, vous remarquerez que son histoire n’est pas toute rose. 
Plus d'informations ici (https://addons.mozilla.org/fr/firefox/user/18970/)

Une autre alternative serait **Bitdefender TrafficLight**, disponible ici (https://addons.mozilla.org/fr/firefox/addon/trafficlight)
Vous l’aurez compris, l’extension est gérée par une grosse firme (la société roumaine éditant une suite de sécurité du même nom), et d’un autre côté sa licence est un peu trouble. 
A un endroit j’ai même pu lire « GNU GPL2 », néanmoins cela reste à prendre avec des pincettes. A vous de voir.

**Mozilla Firefox édite aussi des extensions**, dont certaines dédiées à la sécurité (isolation de profiles de navigation notamment)  des thèmes officiels, ainsi que de quoi en créer par la suite.
C'est également par là que vous obtenez l'accès aux services de Firefox (dont ceux payants).
Egalement : la porte d'entrée pour tester la version "pre-release alpha" qui semblee t-il est encore plus frais que Nightly.
Accès ici : https://addons.mozilla.org/fr/firefox/user/4757633/

Pour résumer ce chapitre : 
Bien sûr, il y a des extensions pour tout (orthographe, changer d’User-Agent, accepter les cookies automatiquement, gérer les onglets, et même faire le café…) 
En revanche, les extensions restent à votre discrétion, mais n’en abusez pas ! 
Evitez aussi les extensions axées optimisation, c’est superflu et pouvant également vous amener à l'effet inverse !




