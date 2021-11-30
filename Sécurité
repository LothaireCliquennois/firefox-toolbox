*Sauf si spécifié les commandes à éditer ou supprimer sont accessibles via about:config dans la barre d’adresses du navigateur. 
Lisez et validez l’avertissement si c’est la première fois que vous visitez cet outil embarqué de Firefox. 
N’appliquez pas les commandes qui ne vous correspondent pas par rapport à leur description.
Bien évidemment, vous aurez déjà commencé par configurer les paramètres introduits sur Firefox 67 par défaut de protection renforcée contre le pistage introduites avec Firefox dans les paramètres classiques.
Beaucoup plus de choses ici ! Le plus complet pour aller encore plus loin sera ici : https://privacytools.io/
Toutes les commandes pour Firefox ont été testées (ou presque).
Néanmoins vous devrez être nettement plus attentifs, car cela peut casser la compatibilité avec pas mal de sites.*

**Désactivation de la télémétrie et les rapports d’erreurs** *collecte de données pour améliorer le navigateur*
Avec toutes ces commandes, vous effectuez la première partie d’une démarche contre le recueil de données par Mozilla.
La deuxième partie concerne les rapports d’erreurs. 
Tout ce que je vous indique ici est dans le cas où vous souhaitez désactiver complètement l’envoi de données à Mozilla. 
L’inverse de ce qui est indiqué ci-dessous active ces envois.
Je ne vous recommande pas de modifier qu’une partie, soit vous activez la télémétrie à 100 %, soit vous la désactivez à 100 %.

```browser.newtabpage.activity-stream.feeds.telemetry``` :  mettez à ```false```
```browser.newtabpage.activity-stream.telemetry``` :  mettez à ```false``` 
```browser.ping-centre.telemetry``` mettez à ```false``` 
```toolkit.telemetry.bhrPing.enabled``` : mettez à ```false``` 
```toolkit.telemetry.enabled``` : mettez à ```false``` 
```toolkit.telemetry.firstShutdownPing.enabled``` : mettez à ```false``` 
```toolkit.telemetry.hybridContent.enabled``` : mettez à ```false``` 
```toolkit.telemetry.newProfilePing.enabled``` : mettez à ```false``` 
```toolkit.telemetry.reportingpolicy.firstRun```: mettez à ```false``` 
```toolkit.telemetry.shutdownPingSender.enabled``` : mettez à ```false``` 
```toolkit.telemetry.unifiedv : mettez à ```false```
```toolkit.telemetry.updatePing.enabled``` : mettez à ```false```
```app.normandy.enabled``` : mettez à ```false```
```app.normandy.first_run``` : mettez à ```false```
```app.normandy.remotesettings.enabled``` : mettez à ```false```
```app.normandy.dev_mode``` : mettez à ```false```
```beacon.enabled``` : mettez à ```false```
--- --- --- 
```browser.tabs.crashreporting.includeurl``` : mettez à ```false```
```browser.tabs.crashreporting.requestemail``` : mettez à ```false```
```browser.tabs.crashreporting.sendreport``` : mettez à ```false```
```datareporting.policy.datasubmissionenabled``` : mettez à ```false```
```datareporting.policy.datasubmissionpolicybypassnotification``` : mettez à ```false```
```dom.ipc.plugins.flash.subprocess.crashreporter.enabled``` : mettez à ```false```
```dom.ipc.plugins.reportcrashurl``` : mettez à ```false```
```dom.ipc.report.processhangs``` : mettez à ```false```
```dom.ipc.tabs.createkillhardcrashreports``` : mettez à ```false```
```dom.reporting.enabled``` : mettez à ```false```
```dom.reporting.featurepolicy.enabled``` : mettez à ```false```
```dom.reporting.header.enabled``` : mettez à ```false```
```dom.reporting.testing.enabled``` : mettez à ```false```
```dom.webcomponents.shadowdom.report_usage``` : mettez à ```false```
```extension.webcompat-reporter.enabledv : mettez à ```false```
```image.mem.debug-reporting``` : mettez à ```false```
```layout.css.report_errors``` : mettez à ```false``` (pas vraiment un point de télémétrie, il permet simplement d’empêcher la transmission d’erreurs dans le code de la page à la console de diagnostic intégrée au navigateur)
```memory.dump_reports_on_oom``` : mettez à ```false```
```security.ssl.errorreporting.automatic``` : mettez à ```false```
```security.ssl.errorreporting.enabled``` : mettez à ```false```
```services.sync.prefs.sync.browser.crashreports.unsubmittedcheck.autosubmit2``` : mettez à ```false```

**Do Not Track** *demander aux sites web de ne pas vous pister*
Qu’on se le dise, la majorité des éditeurs de sites web n’en ont rien à cirer. 
L’activer ne mange pas de pain, elle n’a pas cassé de sites pendant mes tests. J’ai cependant entendu des cas où des sites ne passaient pas avec ceci.
privacy.trackingprotection.enabled : passez à true

**Désactiver l’OCSP** (encore une technique pour faire fuir votre trafic vers Google*
Si vous allez observer about:networking#dns il est possible que vous tombiez de requêtes provenant de ocsp.pki.goog en quantité importante. Elles ne sont pas là par hasard : elles sont sensées sécuriser la navigation en ayant le contrôle des certificats des sites visités. Selon pas mal d’experts, c’est encore un moyen de tracker ce que vous faites sur la toile. 
Vous voulez en avoir le cœur net ? Visitez ce fameux oscp.pki.goog et vous comprendrez à qui appartient ce service. Plus d’infos ici. 
Il vous suffira de passer security.ocsp.enabled et security.ocsp.get.enabled toutes deux à false.


**Désactiver le safebrowsing** *Google gouverne encore et toujours le monde*
Le safebrowsing était issu d’un partenariat entre Google et Firefox. Pour Google, il s’agissait d’un merveilleux moyen de collecter des informations sur votre navigation. Même pris en charge désormais directement par Mozilla, il y a lieu de désactiver cette fonctionnalité, sans état d’âme.
https://www.dsfc.net/logiciel-libre/firefox-logiciel-libre/firefox-aurait-coupe-les-ponts-avec-google-pas-vraiment/
Il se base sur trois commandes facilement compréhensibles : browser.safebrowsing.malware.enabled , browser.safebrowsing.phishing.enabled et geo.enabled. Vous passez ça à false, et les ponts avec Google commencent à être rompus ! 

**Désactiver le stockage des applications utilisant le mode offline**
Pour la vie privée, il convient d’éviter laisser des données hors connexion stockées sur votre machine sans aucune raison, alors que vous n’utilisez pas le service en question.
```offline-apps.allow_by_default``` : passer à ```false```
```browser.offline-apps.notify``` : passer à ```false```
```browser.cache.offline.enable``` : passer à ```false```
```browser.cache.offline.capacity ```: passer à  ```0```
```network.manage-offline-status``` : passer à ```false``` (empêche la mise hors connexion en cas de coupure réseau).

**Désactiver la détection automatique des portails captifs**
Avec Firefox 52.0 une nouvelle fonction est apparue, la détection automatique de portails captifs d'accès Wi-Fi, vous savez ceux qui vous redirigent vers une page spéciale en général d'authentification afin de vous connecter à Internet.
Si cette fonction est sans doute bien utile pour les itinérants et/ou ceux qui se connectent souvent hors de chez eux via leur appareil portable, il n'est pas contre d'aucune utilité pour une utilisation domestique.
Or, l'une des conséquences de cette fonction est la connexion quasi permanente de Firefox à un serveur aléatoire de cloudfront.net
Pour désactiver cette fonction, et donc la connexion quasi permanente qui y est liée, passez 
network.captive-portal-service.enabled à false.

**Télémétrie de Firefox via Amazon AWS** 
Dans Firefox il y a le fichier pingsender.exe qui scrute régulièrement l'IP 50.112.45.104 port 443, propriétaire Amazon.
Pingsender est une nouvelle manière d'envoyer les données de télémétrie à la fermeture de Firefox plutôt qu'à son prochain lancement, ce qui permet aux données d'être analysées plus rapidement.
Présent depuis que le recueil des données de télémétrie, il y a plusieurs solutions pour empêcher la communication de ce composant.
Il est à noter que certains forks de Firefox ne le possèdent pas, comme Waterfox (et possiblement d'autres
    1) La ligne ```toolkit.telemetry.shutdownpingsender.enabled``` à passer à ```false```, normalement déjà faite si vous avez désactivé la télémétrie plus haut.
    2) Le fichier hosts de votre système d’exploitation :
Sur Windows : ```%SystemRoot%\system32\drivers\etc\hosts```
Sur Linux : ```/etc/hosts```


**Désactivation de protection contre les sites malveillants**
Ce système est soit-disant conçu pour vous protéger des sites malveillants. 
La liste des sites à éviter est fournie par Google et stockée dans le fichier ```urlclassifier3.sqlite``` de votre profil Firefox. 
Ce fichier pèse lourd pour une base de données et Firefox le consulte constamment pour vérifier toutes les adresses que vous visitez. 
Cela a un impact significatif sur les performances. 
Vous pouvez désactiver ce système pour améliorer les performances. (À ne faire seulement si vous savez ce que vous faites)
Pour le désactiver, il suffit de définir à false ```browser.safebrowsing.enabled``` et browser.safebrowsing.malware.enabled. 
Dans votre profil Firefox, supprimer également le fichier ```urlclassifier3.sqlite``` 
(ne pose aucun problème, fichier pouvant être recréé très facilement au besoin, c’est une base construite normalement au premier lancement du navigateur).

**Désactivation du WebRTC** *nécessaire pour le partage vocal, vidéo et P2P*
Ce tweak ne conviendra pas à tout le monde, car vous pouvez être amené à vous en servir si vous utilisez des sites de chat, de visioconférence, et autres plateformes dans le style. 
Sa désactivation a néanmoins un avantage : VPN ou pas, cette technologie peut révéler votre adresse IP publique via des requêtes appelées STUN.
Passer media.peerconnection.enabled à false permet de renforcer la protection, au détriment de l’incapacité de vous connecter à ce type de sites avec succès.
Pour être sûr qu’il ne va pas se réactiver, vous pouvez aussi modifier ceci : 

```media.peerconnection.turn.disable``` : passer à ```true```
```media.peerconnection.use_document_iceservers``` : passer à ```false```
```media.peerconnection.video.enabled``` : passer à ```false```
```media.peerconnection.identity.timeout``` : passer à ```1```

**Fluidifier le rendu d’images** *on touche à l’accélération graphique*
Catégorie un peu fourre-tout, à tester, car tout dépend de votre configuration matérielle.
D'expérience ces paramètres semblent surtout être valable pour les machines peu performantes.
```gfx.webrender.all``` et ```gfx.webrender.enabled``` sont les commandes à passer à true 
```layers.acceleration.disabled``` est à passer à ```false```
```layers.acceleration.draw-fps``` : passer à ```true``` *seulement si vous souhaitez afficher le taux d’images par seconde, à activer temporairement pour comparer*
```layers.acceleration.force-enabled``` : passer à true *semble ne pas faire bon ménage avec la deuxième ligne*
```gfx.direct2d.force-enabled``` : passer à true *valable uniquement sur Windows, API DirectX*
```gfx.filter.nearest.force-enabled``` : passer à ```true```
```stagefright.force-enabled```: passer à ```true```
```webgl.force-enabled``` : passer à ```true```


***Protection simple contre les sites de phishing/contrefaçons***
```network.idn_show_punycode``` à passer à true de toute urgence !
Pour corriger une faille de sécurité qui peut être corrigée depuis Firefox 62, mais dont la correction n’est toujours pas mise en place par défaut.
Maintenant vous avez plus d'infos ici : https://www.dsfc.net/browser/firefox/phishing-firefox-nest-plus-un-navigateur-pour-madame-michu/
