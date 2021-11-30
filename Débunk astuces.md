**Ici, j'essaie de lister les astuces pour Firefox déclarées comme inutiles**

Soit parce qu'elles fonctionnaient à un moment, plus maintenant.
Soit tout simplement car elles n'ont jamais fonctionnées aussi loin que je me souvienne...
(j'ai commencé à bricoler Firefox environ à la sortie de la version 3.0 à l'époque)
A terme, cette liste va finir par anfler, à terme tout ce qui sera dans les autres catégories se retrouvera ici.

```browser.cache.use_new_backend``` 
(Booléen, true). 
Cette commande est activée par défaut depuis Firefox 32.
niquement trouvable sur des tutoriels datant de 2013-2015. Plus d’infos ici. 

```config.trim_on_minimize``` 
(Booléen, true)
Cette commande est très controversée. 
Datant de l’époque de Firefox 3.0, elle ne semble plus fonctionner aujourd’hui. 
A l’époque, la ligne était déjà controversée. 
Pour résumer, la gestion de la mémoire vive tel que le nom de la commande l’entend est impossible. 
Voir ce lien datant de 2006-2008 pour plus de précisions. (en anglais)

```network.dns.disableipv6``` 
(Booléen, true)
Cette commande était pertinente dans un monde sans IPv6, qui est celui avec lequel j’ai grandi. Or, de nos jours, ce serait plutôt l’inverse qu’il faudrait faire, au risque de se priver de l’accès à pléthore de sites. Soit disant cela accélèrerait la connexion, mais cela est tellement contre-productif.

```browser.turbo.enabled```
(Booléen, true)
Cette commande permettait, dans les débuts de Firefox (à l’époque de Firebird), de compenser le temps que le navigateur mettait à se lancer, en le gardant en mémoire.
Si vous considérez que le lancement met déjà peu de temps à se lancer à chaud. 
Plus de contexte sur ce topic. 

```browser.tabs.remote.autostart```
(Booléen, true)
Depuis Firefox 68, cette commande n’a plus aucun effet.
Peu importe le réglage effectué par l’utilisateur, la valeur reviendra à true.

```browser.tabs.remote.force-enable``` 
(Booléen, true) 
Même remarque que la ligne du dessus.

```toolkit.cosmeticanimations.enabled``` 
(Booléen, false) 
Cette commande était effective à l’époque où l’interface de Firefox s’appelait Quantum. 
Depuis la nouvelle interface Proton, il semblerait que plus aucun effet soit ressenti.

```network.http.sendrefererheader``` 
(Nombre, 0) 
Cette commande permet normalement d’empêcher Firefox d’envoyer certains headers. 
Elle est tellement fonctionnelle qu’elle bloque l’accès à certains sites, principalement des CMS de forums.

```privacy.firstparty.isolate``` 
(Booléen, true) 
Cette commande a pour but de mettre en place des politiques d’isolement des cookies du domaine visité avec les autres, empêchant le suivi sur les autres domaines. 
Elle empêche également le fonctionnement de certains CMS de forums.

```plugin.scan.pid.all``` 
(Booléen, false) 
L’intérêt de cette commande est de désactiver la vérification de l’obsolescence des extensions. 
Lorsqu’une extension n’est plus maintenue, ou qu’une version de Firefox plus récente nécessite d’être installée pour continuer à recevoir les mises à jour des modules. 
L’impact sur les performances étant périodique et très minime, il convient de laisser ceci activé.

```network.http.max-connections``` 
(Nombre, varie d’un site à l’autre, parfois les informations sont même contradictoires) 
Cette commande semble avoir une valeur dorénavant une valeur suffisamment haute pour la plupart des usages. 
Si ce n’est pas le cas chez-vous augmentez-là, mais je crois que toutes ces infos à ce sujet que l’on trouve sont obsolètes…

```network.http.pipelining``` et ses commandes filles 
(activation + valeurs hautes) 
Ces commandes datent d’avant l’HTTP 2. 
Elles étaient déjà en cours d'obsolescence quand les arguments ont été extraits de mozillazine.
Elle présente un effet néfaste global de nos jours sur quasiment tous les sites que vous visiterez aujourd'hui.


