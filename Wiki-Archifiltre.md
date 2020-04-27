# Bienvenue sur le wiki Archifiltre 📃 

L’objectif d’ArchiFiltre est de proposer à tout utilisateur de fichiers bureautiques un outil de visualisation d’arborescences complètes afin de pouvoir les appréhender rapidement en vue de les décrire, les organiser, les trier et aussi les enrichir en apportant de la contextualisation et de la qualification aux documents.

[[images/0_page-garde.png]]

# Sommaire : 
#### 1. Installer Archifiltre et charger mon répertoire
#### 2. Utiliser les fonctionnalités d'Archifiltre    
  2.1 Repérer les données sur le répertoire étudié    
  2.2 Visualiser et naviguer dans un répertoire    
  2.3 Utiliser les fonctionnalités    
  2.4 Utiliser les exports    
#### 3. Mener une opération d'audit et de collecte
  3.1 Je souhaite étudier la structure d’une arborescence   
  3.2 Je souhaite faire des recommandations techniques sur une arborescence  
  3.3 Je souhaite faire des préconisations à partir d’Archifiltre    
  3.4 Je souhaite trouver facilement des éliminables _(en cours)_    
  3.5 Je souhaite faire du tri à partir d’Archifiltre _(à venir)_     
  3.6 Je souhaite faire du traitement de masse _(à venir)_    
  3.7 Je souhaite rédiger un bordereau d’élimination _(à venir)_        
  3.8 Je souhaite organiser un Cleaning-Day à partir d’Archifiltre _(à venir)_ 
#### 4. Traiter un fonds d'archives électroniques
  4.1 Je souhaite faire un versement vers ADAMANT (SAE Archives nationales) _(en cours)_    
  4.2 Je souhaite faire un versement vers un autre SAE (As@lae ...) _(à venir)_    

## Wiki utilisateur

### 1. Installer Archifiltre et charger mon répertoire

Vous pouvez télécharger gratuitement l'outil Archifiltre en cliquant sur ce lien : https://archifiltre.fabrique.social.gouv.fr

Choisissez la version que vous désirez installer (la dernière version est automatiquement sélectionnée) et choississez votre explorateur (Windows ; Linux ou Mac). Cliquez ensuite sur "Découvrir l'application". Le téléchargement d'Archifiltre va se lancer automatiquement.

Le fichier s'enregistre sous le nom "Archifiltre.exe". Double-cliquez pour lancer l'exécution de l'outil. Il n'y a pas d'installation à faire, Archifiltre s’exécute immédiatement !

> **Attention :** Il est possible que votre système d'exploitation ou votre antivirus vous demande si ce programme est sûr, il n'y a pas d'inquiétude à avoir, le logiciel est sans danger, vous pouvez forcer l'installation. 

Lorsque Archifiltre est lancé, pour visualiser votre répertoire, il suffit de réaliser un glisser-déposer.

[[images/1-1_glisser-deposer.png]]

Votre répertoire commence à être chargé dans Archifiltre. Profitez-en pour lire les quelques astuces en bas de la page et découvrir les nouvelles fonctionnalités de la version en cliquant sur le lien "quoi de neuf ?"
 
[[images/1-2_chargement.png]]

> **Attention :** Plus votre arborescence est volumineuse, plus il y a de métadonnées à charger. La visualisation de l’arborescence peut pendre quelques minutes voire même de nombreuses minutes en fonction des volumes de fichiers et de la puissance de votre ordinateur.

Votre ordinateur a planté pendant votre session de travail ? Il possible de restaurer votre travail en relançant Archifiltre et en cliquant sur "Recharger la session précédente". Vous retrouverez votre travail là où il s'est arrêté.

[[images/1-3_recharger.png]]

***

### 2. Utiliser les fonctionnalités d'Archifiltre
#### 2.1 Repérer les données sur l'arborescence

* La zone des métadonnées :   
[[images/2-1-1_zone-metadonnee.png]]      
Elle permet de connaître pour un dossier (ou pour un fichier), son poids, son hash (son empreinte), la dernière date de modification la plus ancienne et la dernière de modification la plus récente (quand il s'agit d'un répertoire). Les métadonnées de dates du dossier se retrouvent dans la frise chronologique en dessous.    
_Peut être utile comme critère de recherche dans un audit (recherche des dossiers clos et anciens)._

* Les dates des répertoires :    
[[images/2-1-2_dates-repertoires.png]]    
Moyenne : valeur moyenne de la date de dernière modification pour l’ensemble des fichiers du répertoire sélectionné. Cela équivaut à calculer la moyenne d’âge des fichiers. Cette valeur n’est pas toujours très intéressante : elle peut être faussée quand quelques fichiers présentent des dates très anciennes (ou à l’inverse très récentes) alors que la majorité ont des dates relevant de la même période. Dans ce cas, ils faussent la valeur de la moyenne.    
Médiane : la moitié des fichiers ont une date antérieure à la valeur médiane, la moitié une date supérieure.
   
Lorsque les deux barres moyenne et médiane sont proches, cela signifie que le dossier présente une homogénéité des dates de dernière modification : elles sont rapprochées dans le temps, et il y a très peu de documents qui s’écartent de cette période.    
Les deux petites barres noires permettent par ailleurs de situer les dates extrêmes du répertoire sélectionné par rapport à l’ensemble de l’arborescence étudiée.    
> **Attention :** la métadonnée de dernière modification correspond normalement à la date de dernier enregistrement du fichier. Cette métadonnée n’est toutefois pas toujours fiable. Il arrive qu’elle soit modifiée lorsque le fichier est ouvert (par exemple pour les mails) alors même que ce fichier n’a pas été modifié.    

* Le Hash (empreintes) :   
[[images/2-1-3_empreintes.png]]     
Le hash est le résultat d'un calcul informatique qui attribue à un élément un code. Ce code est attribué en hashant (d'où le nom) l'ensemble de l'élément (données, métadonnées). Ainsi, un document ne peut avoir qu'un code unique (comme un code génétique). Si deux documents sont identiques, ils auront le même code. Si un document est modifié (même d'une seule virgule), son code est également modifié. Prenons un exemple cité sur Wikipédia, avec un hash calculé sur une phrase :     
"Et l’unique cordeau des trompettes marines" => 8747e564eb53cb2f1dcb9aae0779c2aa    
En modifiant un caractère, l'empreinte change radicalement :    
"Et l’unique cordeau des trompettes marinEs" => c802e1bd9b5f2b0d244bbc982f5082b3    
_Peut être utile lors de la recherche de doublons. Un csv avec empreintes peut-être édité depuis Archifiltre. Si l'on recherche dans ce csv deux hash identiques, alors on a la certitude d'avoir trouvé deux purs doublons._

* La zone d’informations sur le répertoire :      
[[images/2-1-4_entete.png]]     
Elle permet de connaître le nombre de dossiers, de fichiers et la volumétrie totale. Il est également possible de donner un nom à l’analyse Archifiltre en cliquant sur « Nom du projet ».    
_Peut être utile pour appréhender, dans un premier temps, l’arborescence._

#### 2.2 Visualiser et naviguer dans un répertoire

* La barre d’outils de visualisation :      
[[images/2-2-1_boutons.png]]    
**Retour à la racine** : permet de revenir à la visualisation initiale et "macro" du répertoire.    
**Code couleur** :   
_Type_ : l’affichage du répertoire se fait selon le volume. La visualisation n’est plus celle de Windows mais une visualisation pondérée selon le poids des dossiers/fichiers.
_Dates_ : l’affichage de la taille des éléments est toujours pondéré selon le poids des dossiers. En revanche, le classement des fichiers et les couleurs attribuées aux fichiers et aux dossiers sont réalisés selon les métadonnées de dates. Le classement se fait du plus ancien (en foncé) au plus récent (en clair).        
**Affichage** :     
_Volume_ : c’est l’option de visualisation qui est activée par défaut. Elle permet de voir votre arborescence selon une pondération par volume/poids de vos dossiers.    
*_Nombre_* : C’est une solution alternative pour visualiser votre arborescence. L’ordre affiché du répertoire reste le même, mais la pondération se fait selon le nombre de fichiers. Un dossier avec de nombreux fichiers, même peu volumineux, apparaîtra plus grand qu’un dossier contenant peu de fichiers mais volumineux.

* La navigation dans le répertoire :    
[[images/2-2-2_navigation-repertoires.png]]   
Vous pouvez naviguer dans le répertoire avec votre souris. En cliquant sur un dossier ou sur un fichier, les données propres à l’élément s’affichent dans la zone des métadonnées, mais aussi en bas de la visualisation avec la taille de l’objet mais aussi le pourcentage de l’espace qu’il occupe au sein du répertoire total. Si vous souhaitez naviguer plus profondément dans l’arborescence, il suffit de double-cliquer sur le dossier et un zoom pondérera à nouveau selon la nouvelle visualisation. Si vous souhaitez analyser plus en détail l’objet, il est possible d’ouvrir le dossier ou le fichier sélectionné en cliquant sur la loupe à côté du nom de l’objet.

* La visualisation des fichiers et typologies :     
[[images/2-2-3_couleurs-fichiers.png]]     
Au plus bas de votre répertoire, vous visualisez les fichiers. Des codes couleurs ont été attribués aux fichiers selon leur nature. Ils reprennent en partie  les couleurs utilisés par les logiciels de bureautique : rouge foncé (pdf), rouge clair (présentations de type Powerpoint), vert (tableurs), bleu clair (messageries), bleu foncé (traitement de texte), violet clair (images), violet foncé (vidéo), rose (fichiers audio) et gris (tous les autres formats y compris dossiers compressés, formats particuliers)

* Le fil d'Ariane    
[[images/2-2-4_fil-ariane.png]]    
Il permet de suivre le chemin d’accès jusqu’au dossier ou fichier que l’on étudie. On peut copier le chemin d'accès en sélectionnant le niveau du chemin d'accès désiré et en cliquant sur le petit icône apparaissant.   
_Peut être utile lors de l'enrichissement pour réaliser un lien (dans un tag ou une description) entre deux documents. Les deux unités peuvent être enrichies par les chemins permettant de faire un lien intellectuel entre les deux.

* La carte :     
[[images/2-2-5_map.png]]    
Elle vous permet de savoir où vous êtes dans l’arborescence lorsque vous naviguez au sein de celle-ci. Lorsque l’on descend à plusieurs sous-niveaux, la carte vous permet de vous resituer dans l’arborescence.     
_Peut être utile lors de l’audit ou du traitement afin d’orienter son niveau d’analyse. Lorsqu’on étudie une partie infinitésimale de l’arborescence, mieux vaut ne pas s’y attarder._  

#### 2.3 Utiliser les fonctionnalités

* La barre de chargement du calcul d’empreintes :    
[[images/2-3-1_empreintes.png]]           
_Plus le répertoire comporte un nombre élevé de fichiers plus le calcul est long. Lorsque le calcul est disponible, l’export csv avec empreintes et le rapport d’audit peuvent être générés._

* Renommer un répertoire ou un fichier :      
[[images/2-3-2_renommage.png]]    
Vous pouvez le réaliser en cliquant dans cette zone. Le renommage n’est effectif que dans Archifiltre. En renommant, vous attribuez un nouveau nom à l’objet tout en conservant l’ancien nom (visible entre parenthèses en dessous). La visualisation d'un renommage dans Archifiltre est notifié par un liseré bleu clair. 
_Peut être utile dans le cadre d’une proposition de modification de l’arborescence ou bien lors du traitement d’un fonds électronique._    

* L’ouverture d'un item :    
[[images/2-3-3_item.png]]     
L'icône de dossier ou de fichier avec une loupe permet d’ouvrir directement l’objet pour pouvoir le consulter (il faut que le lien entre Archifiltre et le répertoire ne soit pas rompu). 

* Le tag :      
[[images/2-3-4_tags.png]]    
Le tag permet d’appliquer à un dossier ou à un fichier une information. Cette information s’ajoute à la bibliothèque des tags. **Attention**, lorsqu'on applique un tag sur un dossier, le tag s’applique à l’ensemble des dossiers et fichiers contenus dans ce dossier. Lorsqu’un tag est appliqué, il se visualise par un liseré bleu foncé sur le haut de l'item.    
_Peut être utile dans le cadre d’un audit en appliquant des actions à réaliser (à éliminer, à archiver, à transférer…) ou dans le cadre du traitement en appliquant une action, un thème d'indexation à un dossier ou faire un rapprochement intellectuel (type répertoire méthodique)._

* Le tag "A supprimer" :     
[[images/2-3-5_tag-supp.png]]    
Ce tag est un tag automatisé qui permet d'appliquer l'action "A supprimer" à un élément ou à un ensemble d'éléments d'un répertoire.
Vous retrouverez la liste des éléments tagués "A supprimer" dans l'export CSV pour en faire une liste d'éliminables à valider suivant la réglementation (la liste peut être jointe à un bordereau d'élimination).
>*Attention :* Lors de l'export RESIP les items ayant le tag "A supprimer" ne sont pas exportés. Ainsi, il ne sont pas chargés dans le SAE.

* La bibliothèque de tags :    
[[images/2-3-6_bibliotheque.png]]    
Elle permet de retrouver l’ensemble des tags qui ont été appliqués dans l'arborescence analysée. Cette bibliothèque permet de réutiliser les tags et de les appliquer en appuyant sur le « + » mais aussi de les comptabiliser en nombre et en volumétrie concernée (zone grisée à l'arrière) pour se représenter le volume d'éléments qu'ils concernent. Il est possible également de supprimer un tag appliqué en cliquant sur la corbeille.    
Il est possible de renommer un tag depuis la bibliothèque en cliquant dessus.    
_Peut être utile pour un retour d’audit sur le nombre de dossiers éliminables, la volumétrie…_

* La description :      
[[images/2-3-7_description.png]]    
Elle permet d’ajouter à un dossier ou à un fichier des informations. La visualisation de l'ajout d'une description se fait avec un liseré bleu sur l'item enrichi.
_Peut être utile dans le cadre d’un audit, pour justifier un sort final. La description peut être utilisée dans le cadre du traitement en tant que « Présentation du contenu » (ISAD-G) ou « scope content » (balise de l'EAD)._

#### 2.4 Utiliser les exports

[[images/2-4-1_enregistrement.png]]    
* Le bouton "Enregistrer" permet de sauvegarder le travail réalisé dans Archifiltre. L’enregistrement génère un fichier à l’extension JSON. Ce fichier peut être chargé dans Archifiltre en faisant le glisser-déposer. Le chargement du fichier est alors très rapide, quelle que soit la taille de l’arborescence puisque les métadonnées ont déjà été analysées une fois. Ce fichier JSON comporte également tous les enrichissements (renommages, tags et descriptions) que vous avez pu inscrire dans votre analyse.
_Peut être utilisé comme outil de dialogue avec un service pour faire des propositions de tri ou de dialogue avec vos collègues/votre responsable dans le cadre d'un traitement._ 

[[images/2-4-2_exports.png]]    
* Le bouton « Exporter » permet de regrouper les métadonnées récupérées et générées dans Archifiltre sous un autre format. Il est possible d’exporter :    
Au format csv
Au format csv avec empreintes    
A un format exploitable par le logiciel RESIP (développé par le programme VITAM) 
Au format METS (Metadata Encoding and Transmission Standard)
Il est également possible de générer un rapport d’audit automatique    

> _Le bouton « Fermer » permet de quitter l’analyse en cours et de revenir à l’écran d’accueil d’Archifiltre afin de charger un nouveau répertoire. En cas d'erreur, il est possible d'ouvrir à nouveau Archifiltre et de charger le répertoire sur lequel on travaillait et de restaurer l'ensemble de son travail._

***
### 3. Mener une opération d’audit et de collecte
Le génie d’Archifiltre vous permet de réaliser tous vos souhaits, il ne reste plus qu’à le choisir !

#### 3.1 Je souhaite étudier la structure d’une arborescence

**Cas 1 – Une arborescence mal pensée**
[[images/3-1-1-1_structure-volumine.png]]

La visualisation d’Archifiltre étant pondérée par le poids des dossiers, la visualisation du répertoire peut permettre en quelque secondes de constater que le répertoire n’est pas construit dans une logique fonctionnelle ni organisationnelle. Ici, on peut constater un dysfonctionnement dès le deuxième niveau du répertoire.

**Que faire ?** Analysez le répertoire en ayant connaissance de l’organigramme et des grandes fonctions de la structure. Par exemple, si on analyse le répertoire d’un service d’archives, il ne sera pas difficile d’y retrouver dès les premiers niveaux, ses grandes missions : collecte, classement, conservation, communication avec quelques dossiers liés à tous les services : gestion du personnel, documentation…
La visualisation à plat et pondérée doit permettre de dégager l’organisation du service et proposer a minima, un répertoire au deuxième niveau.

> **Attention :** Ce cas fonctionne dans le cas où l’arborescence est essentiellement constituée de fichiers bureautique. Si un dossier comporte plusieurs fichiers volumineux (type multimédia) alors la visualisation peut être faussée. Pour s’en assurer il est important d’essayer une visualisation pondérée selon le nombre (II.10).

**Cas 2 – Des doublons de répertoires au sein de l’arborescence**
[[images/3-1-1-2_structure-redondante.png]]

Avant d’entrer plus en détail dans un répertoire, il est important d’en étudier sa structure par sa visualisation. Ici, il n’est pas difficile de voir que l’arborescence présente quatre fois une structuration similaire. Pour qu’un tel résultat apparaisse dans la visualisation globale du répertoire, il y a deux possibilités : soit il y a un classement sériel (type chronologique, géographique…) soit il y a des dossiers similaires créés à des endroits différents et qui comportent plus ou moins les mêmes fichiers (puisque la visualisation est pondérée par poids).

**Que faire ?** Pour déterminer plus précisément la situation à laquelle on est confronté, il est inévitable de rentrer plus en profondeur dans l’analyse de ces dossiers. Dans cet exemple, des dossiers et des fichiers de mêmes noms ont été retrouvés. Pour déterminer si les dossiers sont de véritables doublons, un récolement doit être réalisé. Pour cela, chaque dossier doit être intégré, à son niveau le plus haut, dans Archifiltre. En faisant un export csv, nous obtenons le récolement. (à réaliser ici quatre fois). En établissant les différences via les csv, il est possible de déterminer avec exactitude quel dossier est le plus complet, quels dossiers manquent, quels dossiers disposent des dernières versions etc. 

> **Attention :** Réaliser un dé-doublonnage est plus compliqué qu’il n’y paraît. Dans cet exemple, il faut déterminer les différences entre ces quatre arborescences : Où sont les fichiers définitifs ? Est-ce qu’on retrouve l’intégralité des fichiers dans la plus grosse arborescence ? Quelle arborescence fait référence ? Un logiciel de dé-doublonnage va supprimer les fichiers sans déterminer une logique de tri. La visualisation de doublons impose donc un travail de réflexion en amont et de choix d'évaluation en fonction de la connaissance du contexte. 

**Cas 3 – Une arborescence chronologique**
[[images/3-1-1-3_structure-chrono.png]]

La visualisation d’ensemble d’une arborescence (par poids ou par nombre) peut donner les premières clefs d’analyse et d’audit. Toutefois, certains bureaux peuvent être amenés à avoir une production sérielle, qui peut être classée de façon chronologique. A plus ou moins grande échelle, tous les bureaux ont une partie d’arborescence sérielle. Le chrono-courrier d’un secrétariat, les dossiers de gestion annuelle d’un bureau des ressources humaines, le registre d’entrée ou d’élimination du bureau des archives etc. 

**Que faire ?** Pour une analyse du répertoire à échelle macro, la visualisation pondérée n’apporte aucune plus-value. En revanche, il est possible de s’appuyer sur l’ensemble des métadonnées pour aborder l’arborescence d’une autre manière. Lorsqu’un répertoire a une date de dernière modification qui remonte à plusieurs années, on peut considérer alors que ce dossier est clos. A l’instar du papier, il est possible de débuter l’évaluation. 

> **Attention :**  Bien qu’il soit simple et efficace, le classement chronologique ne peut être utilisé que partiellement.

**Cas 4 – Visualiser l’arborescence par nombre de fichiers**    

_Visualisation par poids :_    
[[images/3-1-1-4_structure-volume.png]]

Étudier une arborescence contenant des fichiers volumineux n’est pas pertinente avec la pondération par poids. De fait, plus un fichier est volumineux, plus sa visualisation au sein de l’arborescence est importante. Si le volume par poids peut être un indicateur de tri, il n’est pas forcément un bon indicateur dans un audit ou une opération de collecte. Avec la pondération par poids, notre arborescence ci-dessous, nous oriente vers une priorisation du tri du premier et du deuxième dossier au premier niveau. 

**Que faire ?**

_Visualisation par nombre :_     
[[images/3-1-1-4_structure-nombre.png]]

Si l’on utilise la visualisation par nombre (exemple ci-dessus), les indicateurs sont totalement différents. Ce changement de visualisation offre une nouvelle grille d’analyse de l’arborescence. Dans ce deuxième exemple, on constate que le troisième dossier dispose d’une arborescence complexe et d’une profondeur dépassant les 15 niveaux.

> **Attention :** Ces indicateurs ne sont que des éléments d'analyse pour appréhender le répertoire. Lorsque nous sommes confrontés à un archivage à réaliser, nous quantifions toujours ce qu'il y a à traiter pour définir notre plan d'action et adapter nos méthodes de travail selon le volume. Nous n'allons pas traiter de la même manière l'archivage d'une armoire, d'un local ou d'un service entier. Cette capacité d'adaptation de l'archiviste, se transpose ici, en électronique, avec la visualisation par poids et par volume. 

#### 3.2 Je souhaite faire des recommandations techniques sur une arborescence

**S’appuyer sur le rapport d’audit**

Lorsqu’on génère un rapport d’audit automatiquement depuis Archifiltre, de nombreuses données sont analysées et structurées. 

_1 Les chiffres clés sur l’arborescence :_

Dans cette première partie, il s’agit de faire un état des lieux de l’arborescence du service audité : le nombre de dossiers, le nombre de fichiers, la taille de l’arborescence, les dates extrêmes, le nom du fichier le plus long, le chemin d’accès le plus long et le nombre de niveaux de profondeur maximum.
L’objectif de cette première partie est de donner, à une échelle macro, les premiers problèmes de l’arborescence. 

_2 Répartition des éléments par types d’extension_

Cette rubrique a pour objectif de pondérer l’arborescence selon les types de fichiers produits. Cette indication n’est qu’un élément d’orientation pour un audit. Par exemple, la présence en masse de fichiers de type tableur peut indiquer la conservation d’un grand nombre de fichiers de suivi ou d’export de logiciels. Une présence très importante de fichiers de type média peut indiquer une utilisation non appropriée ou abusive du réseau commun.

_3 Top 5 des répertoires/dossiers le plus anciens_

Dans cette partie est mise en avant, les dossiers dont les dernières dates de modification sont les plus anciennes du répertoire. Cette information peut être une orientation pour collecter ou éliminer réglementairement ces dossiers.

_4 Top 5 des répertoires/dossiers les plus volumineux_

A l’instar des archives papier, la volumétrie reste toujours un premier indicateur pour approcher un fonds à évaluer, collecter, traiter.

_5, 6 et 7 Les redondances_

Dans ces deux parties, sont renseignés les éléments en redondance au sein du répertoire avec une estimation du volume et de la quantité que cela représente.

**Etudier les chemins d’accès**

Le chemin d’accès d’un fichier ou d’un répertoire est la chaîne de caractères décrivant la position du fichier ou du répertoire dans le système. En d’autres termes, le chemin d’accès, l’ensemble des niveaux en partant du disque dur ou serveur, jusqu’au fichier. Le fil d’Ariane dans Archifiltre est une partie du chemin d’accès. 

_Pourquoi faut-il étudier les chemins d’accès ?_ 

Pour des raisons techniques, les chemins d’accès ne peuvent dépasser 256 caractères dans un environnement Windows. 
Cette limite peut vite être atteinte avec une arborescence trop profonde. Elle peut également être vite atteinte à cause du nommage d’un fichier. 
Quand la limite des 256 caractères est dépassée, les fichiers ne s'affichent plus dans Windows, et ils 

Par exemple un fichier situé à un niveau 4, peut vite devenir bloquant s’il est mal nommé.

> J://Direction/Archives/0_Procédures-et-doc/Textes/loi n 78-753du 17 juillet 1978 portant diverses mesures d'amélioration des relations entre l'administration et le public et diverses dispositions d'ordre administratif social et fiscal

Dans cet exemple, le fichier a simplement été enregistré sans être renommé. Le chemin d’accès atteint déjà 235 caractères sur 256.

_Pourquoi faut-il surveiller la longueur des chemins d’accès de mon répertoire ?_

Un fichier dont le chemin d’accès dépasse le cadre maximal ne peut plus être consulté ni même déplacé. De même, lorsqu’on souhaite déplacer des dossiers, le transfert peut être bloqué en raison de chemins d’accès trop longs.

_Comment identifier l’ensemble de mes chemins d’accès trop longs ?_

Pour connaître l’ensemble des chemins d’accès trop longs, il faut réaliser un export csv. Dans l’export csv, une colonne est consacrée au nombre de caractères du chemin d’accès. Si on applique un filtre, il est possible de demande au tableur de ressortir l’ensemble des chemins d’accès dépassant le nombre de 256.
 
 _Comment y remédier ?_

Il n’y a pas d’autre solutions que le renommage. Selon les situations, il peut être fait en masse ou manuellement. Il est également possible de supprimer des niveaux intermédiaires inutiles. 

**Etudier les profondeurs de l’arborescence**

Comme expliqué dans la rubrique ci-dessus, plus il y aura de profondeur dans l’arborescence plus le chemin d’accès est allongé. En outre, plus l’utilisateur doit naviguer dans l’arborescence plus le risque de perte de l’information est importante.

_Quelle profondeur d’arborescence doit-on conseiller ?_

Il est conseillé de ne pas dépasser plus de dix niveaux de profondeurs. Il est important de transposer sa pratique électronique à celle du papier. Qui ouvrirait plus de dix dossiers à la suite pour accéder à sa feuille ? Une arborescence trop profonde n’est pas fonctionnelle. Le risque est que l’utilisateur copie les documents ailleurs dans l’arborescence voire ne retrouve pas les documents en question.

_Comment identifier les différentes profondeurs de mon arborescence ?_

Pour connaître la valeur des niveaux de profondeur de mon arborescence, il faut réaliser un export csv. Dans l’export csv, une colonne est consacrée à la profondeur de l’arborescence. Si on applique un filtre, il est possible de demander au tableur de ressortir l’ensemble des niveaux de profondeur dépassant le chiffre 10.

#### 3.3 Je souhaite faire des préconisations à partir d’Archifiltre

Comme chaque projet, il est important de définir le cadre d’action et le rôle de chaque personne. Dans un projet d’audit ou de préconisation sur une arborescence, il est indispensable de définir les attentes et les besoins du service. De fait, si l’archiviste s’engage à fournir un livrable contenant l’ensemble des préconisations (problèmes, solutions, points forts, points faibles), le service audité doit également s’impliquer dans le plan d’action et le calendrier défini en amont. 

##### **Première étape : faire une analyse macro de l’arborescence**

Archifiltre permet de connaître l’ensemble des métadonnées de l’arborescence en un seul coup d’œil. 

Sans même naviguer au sein de l’arborescence, il est déjà possible de dégager des pistes de réflexions, d’orientation pour nos préconisations.

L’indice de la volumétrie de l’arborescence: on peut mettre en relief ce chiffre avec celui d’autres services, calculer son pourcentage d’occupation de l’espace serveur. 

Les métadonnées de dates peuvent également donner une orientation. Le fichier le plus ancien date de 1980 et la date moyenne se situe à 2010 et la médiane à 2000. On peut d’ores-et-déjà estimer que des dossiers sont clos et peuvent être sûrement archivés ou éliminés.

L’indication du nombre de fichiers et de dossiers peut être parlante si l’on dispose de moyens de comparaison. Si on ne dispose pas de moyens de comparaison, on peut faire le ratio nombre de fichiers / nombres de dossiers. Ici : 104812/7721=13,5. Cette information est purement théorique, mais une arborescence où le ratio descend à moins de dix fichiers, on peut de suite savoir qu’il y a un problème d’organisation. L’arborescence est trop ramifiée et l’information perdue.

##### **Deuxième étape : proposer un rapport d’audit**

Pour débuter un rapport d’audit, il faut dans un premier s’appuyer sur le rapport d’audit généré automatiquement par Archifiltre. C’est un format texte et modifiable, il peut être complété et modifié sur sa forme. 

L’audit généré automatiquement réalise des préconisations essentiellement techniques. C’est au tour de l’archiviste de l’agrémenter d’éléments d’analyse plus approfondie.  

**Cas 1 – Proposer des améliorations de règles de nommage**

Dans cet exemple, le fil d’Ariane visualisé dans Archifiltre permet de voir l’ensemble du chemin d’accès jusqu’au fichier. On peut voir de nombreuses redondances. En les identifiant par des codes couleurs, il est facile de faire comprendre au service qu’il n’est pas utile de reprendre les informations du niveau supérieur. Chaque niveau dans l’arborescence doit avoir une information complémentaire, sinon son existence n’est pas utile.

En retravaillant très peu l’arborescence (en renommage et en déplacement), il est possible de montrer au service que le chemin d’accès peut être fortement réduit et plus explicite. Avec l’exemple ci-dessous, il est possible de réduire la longueur de chemin d’accès de 46% : 

\PREST\5 - SUIVI DES MARCHES et des CONVENTIONS\2 - MARCHES et CONVENTIONS\Section MOBILIERS DEMENAGEMENTS MANUTENTION\MARCHE DEMENAGEMENTS\Marché 2017-2021 ORGANIDEM\1 - Prépa DCE + procd\Analyse candidatures et offres\Compléments offres\3 réponses\2 NASSE DEMECO\2ème Réponse Groupe Nasse\2ème réponse Groupe Nasse\Cas pratiques - destruction mobilier, garde meuble Rectifié 22 decembre 2016.xlsx

PREST\5_Marchés-et-conventions\2_Suivi\1_Section-déménagements-manutention\1_2017-2021\1_DCE_procédures\1_Candidatures_et_offres\1_Compléments\3_Réponses\2_Nasse-demeco\1_2e_réponse\20161222_cas-pratique-déménagement 

**Cas 2 – Proposer des pistes de réorganisation de l’arborescence**

La fin de la deuxième étape est l’occasion de lancer une réflexion sur la construction de l’arborescence et les choix qui ont été faits.

Dans chaque arborescence, il y a des cas que l’on voit revenir systématiquement et qui sont toujours sources de problèmes et qui doivent attirer notre attention.

* Les dossiers personnels

Ces dossiers ont une logique d’organisation personnelle, souvent peu utilisés par les collaborateurs. Les dossiers sont souvent sources de redondances de fichiers ou de versioning (les versions intermédiaires dans le dossier perso et la version finale sur le serveur commun).

* Les dossiers thématiques

Prenons l’exemple des dossiers de ressources humaines. Les services ont tendance à classer par thématiques :
RH > Recrutement > Contractuel > Non-abouti > Monsieur X ; Madame X ; Madame Y ; …

Or la durée d’utilité administrative de ces dossiers est de 5 ans. Il est donc utile de créer un niveau pour réaliser un classement chronologique, facilitant ainsi le traitement.

RH > Recrutement > Contractuel > Non-abouti > 2019 (Monsieur X ; Madame Y) ; 2020 (Madame X) ; …

> **Attention :** Faire des préconisations engage l’archiviste à fournir un travail en amont de toutes actions. Il est important de s’assurer de l’implication du service et de travailler par étapes. Restructurer une arborescence prend beaucoup de temps aux deux acteurs. Il faut procéder par étapes. Par exemple, définir et établir une arborescence de premier niveau puis fignoler par étapes/niveaux.

### 4. Traiter un fonds d'archives électroniques
#### 4.1 Je souhaite faire un versement vers ADAMANT (SAE Archives nationales)

L'ensemble des enrichissements possibles avec Archifiltre restent virtuels, le versement à étudier n'est pas impacté. Tous les enrichissements qui sont réalisés dans Archifiltre peuvent être transformés au format [SEDA](https://francearchives.fr/de/article/88482501)
et ainsi être intégré dans un SAE [ADAMANT](http://www.archives-nationales.culture.gouv.fr/archiver-les-donnees-numeriques-adamant)

**Préparer le versement**

Comme pour le papier, un versement électronique demande une préparation avant son traitement et versement final. Les principaux éléments de préparation du versement vont être d'ordre technique.    

[[images/4-1-1_ZIP.png]]

Le premier élément à vérifier est de savoir si le versement contient des éléments qui peuvent être bloquants.    
Tout d'abord, il est important de vérifier si le versement est composé de répertoires compressés (zip, 7z, rar…). Ils doivent être décompressés pour être traités (sinon, leur contenu n'est pas affiché dans Archifiltre). La présence de répertoires compressés peut être bloquant pour le SAE. Outre le blocage, il est important de décompresser les répertoires car le contenu compressé peut modifier fortement le contenu du versement dans sa globalité et donc son analyse.    
Pour identifier les objets compressés présents dans le versement, on peut exporter un récolement csv de l’arborescence depuis Archifiltre. Dans ce cas, il faut filtrer la colonne "extension" en sélectionnant uniquement les formats de compression (.zip, .7z, .rar). La liste de l'ensemble des éléments compressés et leur chemin d'accès sont ainsi renseignés.

[[images/4-1-2_CSV.png]]

Le deuxième élément, identique dans la pratique, est de vérifier l'existence ou non de fichiers vides (de l'ordre de 0 à 1 octet) et les fichiers systèmes (ayant pour extensions .ini, .tmp, tumbs.db, .Ink, .DS_Store).    
La même méthode peut être utilisée pour identifier ces éléments, avec le récolement csv, en filtrant les colonnes "poids" et "extension".

Enfin, le troisième élément tient dans le nommage du fichier. L'ensemble des fichiers ou dossiers ayant un point dans leur nommage, autre que pour l'extension, seront bloqués dans le SAE. Il convient donc de corriger manuellement depuis l'explorateur windows en retirant le signe de ponctuation.

**Enrichir depuis Archifiltre**

Il est possible d'enrichir le versement en ajoutant des métadonnées au versement. A l'instar des instruments de recherche rédigés dans la feuille de style SOSIE, nous ajoutons des éléments d'informations, de contextualisation à des ensembles d'archives. Ces informations sont catégorisées et standardisées par la norme ISAG (G) et au format SEDA.  

_Modification de l'intitulé_    
Par défaut, Archifiltre reprend comme intitulé le titre du fichier/répertoire. En cas de modification, le titre d'origine est conservé comme métadonnée et rappelé dans Archifiltre en-dessous du nouveau titre. Lors de l'export pour le SAE, les informations d'origine et les modifications sont conservées.    

[[images/4-1-3_renommage.png]]

_Tag : action et liens_    
Le tag peut être utilisé pour décrire les actions (mot action), mais aussi un sort de traitement (qui seront à exploiter depuis ReSIP).    
Le tag peut être également utilisé pour réaliser un lien intellectuel entre plusieurs éléments dans l'arborescence. Cette utilisation du tag revient à la méthodologie de la rédaction d'un répertoire méthodique.    
>**Attention** : le tag est à utiliser avec parcimonie. Au format SEDA, le tag ne remplit pas la balise "Keyword", propre aux actions. Actuellement, le tag renseigne le champ des indexations thématiques.

_Tag : A supprimer_    
Lors de l'export pour le SAE, les items ayant le tag "A supprimer" ne sont pas exportés depuis Archifiltre. Ainsi, il ne sont pas chargés dans le SAE.

_Description_    
Le champ "Description" peut être utilisé lorsqu'on souhaite décrire l'objet par une phrase ou ajouter un commentaire (signaler une information par exemple). Cette information est celle de la présentation du contenu.

**Enrichir depuis RESIP**    

L'ensemble du traitement du versement ne peut être complètement réalisé depuis Archifiltre. Pour le finaliser, il convient d'utiliser [ReSIP](https://www.programmevitam.fr/pages/ressources/resip/) développé par le programme [VITAM](https://www.programmevitam.fr/).    

Pour établir le lien entre Archifiltre et ReSIP, il faut réaliser l'export "ReSIP" depuis Archifiltre. 

[[images/4-1-3_resip.png]]

Il convient ensuite d'importer cet export dans ReSIP. Les principales actions à mener dans ReSIP vont être la description de l'en-tête du versement, les règles d'accès (au niveau du versement ou de l'item) et la modification des dates extrêmes (si des métadonnées sont modifiées par la consultation du document, par exemple).    

Pour éclaircir la méthodologie et l'interopérabilité entre Archifiltre et ReSIP, a été créé par l'équipe Archifiltre un logigramme pour traiter un versement bureautique.

[[images/4-1-3_logigramme2.png]]

#### 4.2 Je souhaite faire un versement vers un autre SAE (As@lae, ...)


***
## Autres wiki et documentation sur Archifiltre :

### [Wiki de développement](https://github.com/SocialGouv/archifiltre/wiki/Wiki-de-d%C3%A9veloppement)

### [Historique](https://github.com/SocialGouv/archifiltre/wiki/Historique)
***
