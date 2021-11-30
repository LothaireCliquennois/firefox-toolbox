**J'ai créé une valeur/chaîne de trop**

Vous avez créé une valeur au lieu d'une chaîne/chaîne au lieu d'une valeur ou encore vous avez mis un mauvais nom à la valeur/chaîne.
Si vous savez quelle valeur/chaîne : allez sur cette ligne et soit vous l’effacez, soit vous l’inversez, soit vous appuyez sur la flèche retour.
Le cas échéant vous avez hélas commis une erreur à éviter et le seul moyen est de réinstaller Firefox en le désinstallant complètement avec cette méthode (par exemple) en pensant bien à conserver ce que vous souhaitez conserver.

**Je veux sauvegarder mes bookmarks par sécurité (marques-pages)**
    1) Clic droit sur un marque page de la barre
    2) Organiser les marque-pages
    3) Importation et Sauvegarde
    4) Sauvegarder.
    
**Même chose pour les mots de passe (Lockwise anciennement, dépréciée en 2021)**
    1) Tapez about:logins dans la barre d'adresse de Firefox ==> lisez et validez l'avertissement éventuel.
    2) En haut à droite, cliquez sur les trois petits points ==> exporter les identifiants 
    3) Lisez et validez l’avertissement à propos des mots de passe qui seront stockés en clair.
    4) Choisissez l’emplacement où vous souhaitez les retrouver ==> validez.
    
**J'ai mal attribué une valeur/chaîne**
    1) Tapez about:config dans la barre d'adresse de Firefox ==> lisez et validez l'avertissement éventuel.
    2) Trouvez-la chaîne/valeur en question
    3) Clic droit sur la chaîne/valeur ==> Modifier
    4) Attribuez-lui la valeur appropriée (en référence, évitez de vous baser sur ce que vous trouverez en ligne, vous feriez mieux d'installer un Firefox)
    
**J'ai modifié la valeur d'une mauvaise valeur/chaîne**
Autrefois, dans about:config, il était possible de réinitialiser la valeur d’une chaîne, il semblerait que ceci ne soit plus possible. 
C’est pourquoi la seule solution est d’aller chercher la valeur par défaut sur un Firefox qui n’a pas été modifié. 
(encore une fois, soit sur le net, avec un taux d’exactitude aléatoire, soit sur une autre installation de Firefox **DE MÊME VERSION**).

**Je constate toujours des fuites de mémoire vive dont Firefox est responsable, même après les tweaks**
Il est possible de ponctuellement résoudre ce problème en allant sur l’un des outils de diagnostic embarqués à Firefox. 
Celui-ci est accessible ```via about:memory```
En dessous de la section nommée "Free Memory", cliquer sur "GC" puis sur "CC" et finalement sur "Minimise memory usage".

**Je constate toujours un usage CPU (processeur) important dont Firefox est responsable, même après les tweaks**
Dans ce cas, le problème peut se situer à plusieurs endroits :

    1) Chipset graphique trop peu performant ou pilotes manquant de maturité/pas à jour.
Une solution temporaire (à utiliser avec parcimonie) pourrait être de désactiver l’accélération graphique matérielle.
Toutefois mais si votre processeur central n’est pas suffisamment véloce, cela pourrait être encore pire ! 

    2) Modules complémentaires inutiles et/ou malicieux. 
    La meilleure manière d’en avoir le cœur net serait de cliquer sur les trois barres en haut à droite ==> "Aide" ==> "Mode de dépannage". 
Laissez-vous guider pour démarrer Firefox dans un mode où les extensions sont toutes désactivées.
Si Firefox semble plus performant, c’est qu’il faut faire le tri dans vos extensions.

    3) Profil de navigation problématique. 
Il conviendra de le réinitialiser. 
Pour ce faire, lorsque Firefox est fermé, avec la combinaison Windows + R ==> firefox.exe -P 
Et sous Linux Alt + F2 (valable pour certains environnements de bureau) ou directement en terminal , tapez firefox -P, 
Une fenêtre s’ouvrira vous permettant de gérer ainsi vos profils.

**Je souhaite accéder à l’arborescence (les répertoires) de mon profil Firefox**
Pour trouver votre profil Firefox, n’hésitez pas à suivre la documentation officielle accessible ici. 
La liste de l’ensemble des fichiers contenus et leur intérêt est également décrite. 

**Mon Firefox ne veut plus démarrer, ton tuto c’est de la merde**
Pas de panique ! (le taux de fiabilité de tout ce qui est listé sur ce dépôt est compris entre 98 et 100 %, échantillon de grande taille)
Il est possible de démarrer Firefox en mode sans échec de sorte à pouvoir continuer à expérimenter vos réglages personnalisés.
Ainsi, vous pourrez remettre certaines choses par défaut au besoin pour réussir à redémarrer Firefox correctement. 
Combinaison de touches Windows + R ==> C:\Program Files\Mozilla Firefox\firefox.exe" -safe-mode ==> Entrée
Sur Linux via Alt + F2 ou via un terminal ==> firefox -safe-mode

**Mon erreur n'est pas répertoriée**
Si votre erreur n'est pas répertoriée ou n'a pas été résolue :
Ce n’est pas grave, puisque vous savez dorénavant, en ayant lu la page principale, comment solliciter la communauté ou moi-même pour vous aider.
