*Sauf si spécifié les commandes à éditer ou supprimer sont accessibles via ```about:config``` dans la barre d’adresses du navigateur. 
Lisez et validez l’avertissement si c’est la première fois que vous visitez cet outil embarqué de Firefox. 
N’appliquez pas les commandes qui ne vous correspondent pas par rapport à leur description.*

**Réservé à ceux qui ont un accès à internet plutôt lent ou facturées à l’usage :**
Sur les navigateurs de nos jours, une fonction du nom de prédiction de chargement des pages web est mis en place. Celui-ci permet ainsi de charger plusieurs pages s’affichant dans votre résultat de recherche, de manière à ce qu’une fois que vous cliquiez dessus, le chargement soit quasi instantané.

```network.prefetch-next``` : passez à ```false```.

```network.dns.disableprefetch``` : passer à ```true```. 

```network.predictor.enable-prefetch``` : passer à ```false```

```network.predictor.enabled``` : passer à ```false```

```network.predictor.enable-hover-on-ssl``` : passer à ```false```

```network.predictor.doing-tests``` : passer à ```false```

```network.predictor.cleaned-up``` : passer à ```true```

**Optimisation de la gestion des requêtes DNS :**
Maintenant que vous savez ce qu’est un serveur DNS (sous réserve d’avoir lu le n°6 de la page dédiée au bon sens)...
Un autre point à ce sujet nécessite d’être traité : les caches des requêtes DNS de votre navigateur, en plus de celui de votre système d'exploitation. 
En effet, Firefox créé une base de données de toutes les adresses IP qu’il a demandé de sorte à accélérer la navigation. 
Le nombre de requêtes effectuées par jour varie énormément en fonction des habitudes que vous avez.
Les valeurs ci-dessous sont celles préconisées sur différents sites, mais n’hésitez pas à les modifier. 
La première correspond au nombre de requêtes différentes sauvegardées, et à leur date d’expiration. 
La ligne 2 et 3 doivent être de même valeur pour éviter les problèmes.

```network.dnsCacheEntries``` -> 2000

```network.dnsCacheExpiration``` -> 14400

```network.dnsCacheExpirationGracePeriod``` -> 14400

**Si vous n’utilisez pas de proxy (utilisation de Firefox avec un FAI en accès direct) :** 

Il est possible d’empêcher Firefox d’essayer de détecter automatiquement les paramètres de connexion. 
Cela permet toujours la navigation web par un proxy à travers le navigateur (proxy web utilisés pour contourner un accès limité dans une entreprise ou une école notamment)

Pour ce faire : Trois traits en haut à droite ==> Paramètres ==> Onglet général ==> Paramètres réseau (configurer la façon dont Firefox se connecte à Internet). 
Cliquez ainsi sur "pas de proxy". 

Vous pouvez profiter d’être ici pour activer le "DNS via HTTPS" cela ne mange pas de pain. 
N’oubliez pas d’appuyer sur OK pour valider (habitude à prendre en général quoi qu'il arrive)...



**Réglage du cache « précédent/suivant » :** 
Ces réglages désactivent le système de cache de Firefox qui accélère l’affichage des pages suivantes et précédentes, gros consommateur de mémoire. 
Cela force le rechargement de la page, et a l’avantage de réactualiser son contenu à l’écran. 

La deuxième commande réduit la quantité de pages vers lesquelles vous pouvez retourner en arrière.

Dans les paramètres classiques de Firefox : onglet général, décocher « Utiliser les paramètres de performance recommandés », 

Vous pouvez ainsi régler le « nombre maximum de processus de contenu » à une valeur adaptée à la quantité de mémoire vive que vous possédez sur votre machine. Il est possible d’aller encore plus loin en augmentant la valeur de dom.ipc.processcount au-delà de 8, tout en restant raisonnable au niveau de la valeur.

```browser.sessionhistory.max_total_viewers``` : mettez ```0```

```browser.sessionhistory.max_entries``` : mettez ```5``` (par exemple, à modifier en fonction de la nécessité de retourner encore plus en arrière ou en avant.)

**Réglage du cache de navigation web :**

Par défaut, Firefox a la fâcheuse tendance de sauvegarder beaucoup trop d’éléments de pages web. Cela engendre un espace utilisé et un accès au niveau disque tous les deux importants. De mon expérience personnelle, sur des machines raisonnablement performantes, la différence est là. Mes recommandations sont de désactiver le cache disque et d’augmenter le cache en RAM.

Pour ce faire, il convient de suivre ces étapes à la lettre :

    1) Vérifiez que la commande ```browser.cache.memory.enable``` est à ```true``` (changez le cas échéant)
    
    2) Vérifiez que la commande ```browser.cache.disk.enable``` est à ```false``` (changez le cas échéant)
    
    3) Si vous avez changé quoi que ce soit, fermez et réouvrez Firefox.
    
    4) Vérifiez que la commande ```browser.cache.memory.capacity``` existe.
    
La valeur ```-1``` correspond à une gestion automatique par rapport à votre quantité de RAM. 
Sur beaucoup de configurations testées, cela équivaut à plus ou moins 32Mo de RAM. 
C’est beaucoup trop conservatif à mon avis, surtout dans un monde où les onglets ouverts ne se comptent plus sur les doigts d’une main.
Vous pouvez tester plusieurs valeurs, je recommande dans un premier temps de doubler la valeur à l’entier près.

    5) Une nouvelle fois, fermez et réouvrez Firefox.
    
    6) Si tout s’est bien passé, en visitant la page about:cache, vous devriez voir affiché la quantité que vous avez entré auparavant. A la ligne storage disk location, vérifiez la présence de la mention none.
Dans certains cas il peut rester également le cache de navigation hors connexion, en fonction de votre configuration de Firefox il peut résider activé. Il convient de passer browser.cache.offline.capacity à 0 et browser.cache.offline.enable à false.

**Chargement des images différencié :**
En complément de la gestion du délai du premier rendu d’une page...
Vous pouvez faire en sorte que les images quand vous passez dessus. Cela s’appelle le lazy-load, modèle pertinent sur des sites comportant beaucoup d’images, économise de la bande passage, et redéfinit les priorités de sorte que le code HTML/CSS soit chargé et rendu avant les images. L’interrupteur à basculer à true est à cette adresse : dom.image-lazy-loading.enabled

**Désactivation des extensions embarquées dans Firefox (de base):**
Les versions récentes de Firefox intègrent nativement des éléments comme Pocket, qu’on le veuille ou non. Toutefois, il est aisé d’empêcher leur chargement (il semblerait que cela ne les désinstalle pas) afin d’optimiser la consommation de RAM et de réduire le temps de chargement du navigateur.

```reader.parse-on-load.enabled``` : mettez à ```false``` 

```reader.parse-on-load.force-enabled``` : mettez à ```false``` 

```browser.pocket.enabled``` : mettez à ```false``` 

```loop.enabled``` mettez à ```false``` 

**Rendu des pages :** 
Il s'agit du temps qu'attendra Firefox avant de faire un premier affichage de la page s'il n'a pas reçu toutes les données nécessaire à l'affichage de celle-ci.
(dans la manipulation, 2000 millisecondes, soit 2 secondes). 
Bien entendu, Firefox affichera toujours immédiatement la page s'il a reçu les données en moins de 2 secondes.
Sans ce réglage, Firefox va faire plusieurs "rendus" de la page pendant la réception des données, consommant plus de CPU que nécessaire. 
Contrairement à une astuce qui circule beaucoup, il n'est pas du tout recommandé de mettre ce paramètre à zéro. 

Cela force Firefox à faire un rendu de la page alors qu'il n'a même rien reçu, ralentissant l’ordinateur, et pire encore, consommant inutilement sur batterie. 
Selon moi il convient de fixer la valeur à 0 seulement si vous possédez un ordinateur performant et que vous le savez.
Par défaut la valeur est de 5ms (depuis 2016), ce qui, peu importe la machine est un réglage bien trop aggressif.

Créez une nouvelle "valeur nombre" si elle n’existe pas déjà nommée ```nglayout.initialpaint.delay``` et attribuez la valeur ```2000```.

**Désactivation de la restauration de l’activité en cas de plantage :** 

```browser.sessionstore.resume_from_crash``` est la ligne responsable de cette fonctionnalité du navigateur.
Elle permet normalement de restaurer tous les onglets dans le cas où Firefox planterait.
Il suffit de la passer à ```false``` pour désactiver cette sécurité, permettant de libérer quelques ressources. 
