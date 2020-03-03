# Bienvenue sur le wiki Archifiltre

Archifiltre est un logiciel destiné à aider les archivistes et les producteurs de documents bureautiques à appréhender des arborescences complètes de fichiers pour les traiter.    

# Sommaire : 
1. Installer Archifiltre et charger mon répertoire
2. Utiliser les fonctionnalités d'Archifiltre
3. Mener une opération d'audit et de collecte
4. Traiter un fonds d'archives électroniques

## Wiki utilisateur

### 1. Installer Archifiltre et charger mon répertoire

Vous pouvez télécharger gratuitement l'outil Archifiltre en cliquant sur ce lien : https://archifiltre.fabrique.social.gouv.fr

Choisissez la version que vous désirez installer (la dernière version est automatiquement sélectionnée) et choississez votre explorateur (Windows ; Linux ou Mac). Cliquez ensuite sur "Découvrir l'application". Le téléchargement d'Archifiltre va se lancer automatiquement.

Le fichier s'enregistre sous le nom "Archifiltre.exe". Double-cliquez pour lancer l'exécution du logiciel. Il n'y a pas d'installation à faire, Archifiltre s’exécute immédiatement !

> **Attention :** Il est possible que votre système d'exploitation ou votre antivirus vous demande si ce programme est sûr, il n'y a pas d'inquiétude à avoir, le logiciel est sans danger, vous pouvez forcer l'installation. 

Lorsque Archifiltre est lancé, pour visualiser votre répertoire, il suffit de réaliser un glisser-déposer.

[[images/image2.png]]

Votre répertoire commence à être chargé dans Archifiltre. Profitez-en pour lire les quelques astuces en bas de la page et découvrir les nouvelles fonctionnalités de la version en cliquant sur le lien "quoi de neuf ?"
 
[[images/image5.png]]

> **Attention :** Plus votre arborescence est volumineuse, plus il y a de métadonnées à charger. La visualisation de l’arborescence peut pendre quelques minutes. 
***

### 2. Utiliser les fonctionnalités d'Archifiltre

01. Renommer un répertoire ou un fichier en cliquant dans cette zone. Le renommage n’est effectif que dans Archifiltre. En renommant, vous attribuer un nouveau nom à l’objet tout en conservant l’ancien nom (visible entre parenthèse en dessous). 
L’icône de dossier ou de fichier avec une loupe permet d’ouvrir directement l’objet pour pouvoir le consulter (il faut que le lien entre Archifiltre et le répertoire ne soit pas rompu). 
Peut être utile dans le cadre d’une proposition de modification de l’arborescence ou bien lors du traitement d’un fonds électronique.

02. Le tag permet d’appliquer à un dossier ou à un fichier une information. Cette information s’ajoute à la bibliothèque des tags (voir n°5). Attention, lorsque l’on applique un tag sur un dossier, le tag s’applique à l’ensemble des dossiers et fichiers contenu dans ce dossier. Lorsqu’un tag est appliqué il se visualise par un liseré bleu sur le haut du dossier (ex : au-dessus du numéro 11)
Peut être utile dans le cadre d’un audit en appliquant des actions à réaliser (à éliminer, à archiver, à transférer…) ou dans le cadre du traitement en appliquant une action à un dossier (ISAD-G)

03. La description permet d’ajouter à un dossier ou à un fichier des informations.
Peut être utile dans le cadre d’un audit, pour justifier un sort final. La description peut être utilisée dans le cadre du traitement en tant que « présentation du contenu » (ISAD-G) ou « scope content » (Balise de la Description Archivistique Encodée).
04. La zone des métadonnées permet de connaître pour un dossier ou pour un fichier son poids, son hash, la dernière date de modification la plus ancienne et la dernière de modification la plus récente. Les métadonnées de dates du dossier se retrouvent dans la frise chronologique en dessous. L’Explication du hash se retrouve dans la partie III. 4.
Peut être utile comme critère de recherche dans un audit (recherche des dossiers clos et anciens).
05. La bibliothèque de tags permet de retrouver l’ensemble des tags qui ont été appliqués dans le répertoire. Cette bibliothèque permet de réutiliser les tags et de les appliquer en appuyant sur le « + » mais aussi de les comptabiliser en nombre et en volumétrie concernée. Il possible également de supprimer un tag appliqué en cliquant sur la corbeille.
Peut être utile pour un retour d’audit sur le nombre de dossier éliminable, la volumétrie…
06. La zone d’informations sur le répertoire permet de connaître le nombre de dossiers, de fichiers et la volumétrie totale. Il est également possible de donner un nom à l’analyse Archifiltre en cliquant sur « Nom du projet ».
Peut-être utile pour appréhender, dans un premier temps, l’aborescence.
07. Le bouton enregistrer permet de sauvegarder le travail réalisé dans Archifiltre. L’enregistrement génère un fichier à l’extension JSON. Ce fichier peut être chargé dans Archifiltre en faisant le glisser-déposer. Le chargement du fichier est très rapide, quelle que soit la taille de l’arborescence.
Peut être utilisé comme outil de dialogue avec un service (proposition 
08. Le bouton « Exporter » permet de regrouper les métadonnées récupérées et générées dans Archifiltre sous un autre format. Il est d’exporter :
* Au format csv (Voir III.4)
* Au format csv avec calcul d’empreintes (colonne en plus dans l’export, voir III.4)
* Au format exploitable par le logiciel RESIP (voir IV.)
* Au format METS (Metadata Encoding and Transmission Standard)
* Il est également possible de générer un rapport d’audit (voir III. 2)
09. Le bouton « Fermer » permet de quitter l’analyse en cours et de revenir à l’écran d’accueil d’Archifiltre afin de charger un nouveau répertoire.
10. La barre d’outils de visualisation dispose de plusieurs fonctionnalités :
* Retour à la racine : permet de revenir à la visualisation initiale du répertoire. 
* Type : l’affichage du répertoire se fait selon le volume. La visualisation n’est plus celle de Windows mais une visualisation pondérée selon le poids des dossiers.
* Dates : l’affichage du répertoire est toujours pondéré selon le poids des dossiers. En revanche le classement des fichiers et les couleurs attribuées aux fichiers et aux dossiers sont réalisés selon les métadonnées de dates. Le classement se fait du plus ancien (à gauche et en foncé) au plus récent (à droite, en clair). 
* Volume : c’est l’option de visualisation qui est activée par défaut. Elle permet de voir votre arborescence selon une pondération par volume/poids de vos dossiers.
* Nombre : C’est une solution alternative pour visualiser votre arborescence. L’ordre affiché du répertoire reste le même, mais la pondération se fait selon le nombre de fichiers. Un dossier avec de nombreux fichiers, même peu volumineux, apparaîtra plus grand qu’un dossier contenant peu de fichiers mais volumineux.
11. Vous pouvez naviguer dans le répertoire avec votre souris. En cliquant sur un dossier ou sur un fichier, les données propres à l’objet s’affichent dans la zone des métadonnées (01, 02,03, 04) mais aussi en bas de la visualisation avec la taille de l’objet mais aussi le pourcentage de l’espace qu’il occupe au sein du répertoire total. Si vous souhaitez naviguez plus profondément dans l’arborescence, il suffit de double-cliquer sur le dossier et un zoom en pondérant à nouveau selon la nouvelle visualisation. Si vous souhaitez analyser plus en détail l’objet, il est possible d’ouvrir le dossier ou le fichier sélectionné en cliquant sur la loupe à côté du nom de l’objet (01).
12. Au plus bas de votre répertoire, vous visualiser les fichiers. Des codes couleurs ont été attribués aux fichiers selon leur nature. Ils reprennent en partie  les couleurs utilisés par les logiciels de bureautique : vert (tableurs), bleu (traitement de texte), rouge (présentation ou pdf), bleu indigo (messagerie), violet (multimédia), gris (dossiers compressés, format particulier…) 
13. Cette zone permet de suivre le chemin d’accès jusqu’au dossier ou fichier que l’on étudie.
14. La barre de chargement permet de savoir l’avancé du calcul d’empreinte. Plus le répertoire comporte un nombre élevé de fichier plus le calcul est long. Lorsque le calcul est disponible, l’export csv et le rapport d’audit peuvent être générés (08)
15. La carte vous permet de savoir où vous êtes dans l’arborescence lorsque vous naviguez au sein de celle-ci. Lorsque l’on descend à plusieurs sous-niveaux, la carte vous permet de vous resituer dans l’arborescence. 
Peut-être utile lors de l’audit ou du traitement afin d’orienter son niveau d’analyse. Lorsqu’on étudie une partie infinitésimale de l’arborescence, mieux vaut ne pas s’y attarder.  

***
### 3. Mener une opération d’audit et de collecte
Le génie d’Archifiltre vous permet de réaliser tous vos souhaits, il ne reste plus qu’à le choisir !

#### Je souhaite étudier la structure d’une arborescence

**Cas 1 – Une arborescence mal pensée**
[[images/image4.png]]

La visualisation d’Archifiltre étant pondérée par le poids des dossiers, la visualisation du répertoire peut permettre en quelque secondes de constater que le répertoire n’est pas construit dans une logique fonctionnelle ni organisationnelle. Ici, on peut constater un dysfonctionnement dès le deuxième niveau du répertoire.

**Que faire ?** Analysez le répertoire en ayant connaissance de l’organigramme et des grandes fonctions de la structure. Par exemple, si on analyse le répertoire d’un service d’archives, il ne sera pas difficile d’y retrouver dès les premiers niveaux, ses grandes missions : collecte, classement, conservation, communication avec quelques dossiers liés à tous les services : gestion du personnel, documentation…
La visualisation à plat et pondérée doit permettre de dégager l’organisation du service et proposer a minima, un répertoire au deuxième niveau.

> **Attention :** Ce cas fonctionne dans le cas où l’arborescence est essentiellement constituée de fichiers bureautique. Si un dossier comporte plusieurs fichiers volumineux (type média) alors la visualisation peut être faussée. Pour s’en assurer il est important d’essayer une visualisation pondérée selon le nombre (II.10).

**Cas 2 – Des doublons de répertoires au sein de l’arborescence**
[[images/image8.png]]

Avant d’entrer plus en détail dans un répertoire, il est important d’en étudier sa structure par sa visualisation. Ici, il n’est pas difficile de voir que l’arborescence présente quatre fois une structuration similaire. Pour qu’un tel résultat apparaisse dans la visualisation globale du répertoire, il y a deux possibilités : soit il y a un classement sériel (type chronologique, géographique…) soit il y a des dossiers similaires créés à des endroits différents et qui comportent plus ou moins les mêmes fichiers (puisque la visualisation est pondérée par poids).

**Que faire ?** Pour déterminer plus précisément la situation à laquelle on est confronté, il est inévitable de rentrer plus en profondeur dans l’analyse de ces dossiers. Dans cet exemple, des dossiers et des fichiers de mêmes noms ont été retrouvés. Pour déterminer si les dossiers sont de véritables doublons, un récolement doit être réalisé. Pour cela, chaque dossier doit être intégré, à son niveau le plus haut, dans Archifiltre. Un export csv doit être réalisé quatre fois. Par différentiel, il possible de déterminer avec exactitude quel dossier est le plus complet, quel dossier manque, quel dossiers dispose des dernières versions etc. 

> **Attention :** Réaliser un dé-doublonnage est plus compliqué qu’il n’y paraît. Dans cet exemple, il faut déterminer les différences entre ces quatre arborescences : Où sont les fichiers définitifs ? Est-ce qu’on retrouve l’intégralité des fichiers dans la plus grosse arborescence ? Quelle arborescence fait référence ? Un logiciel de dé-doublonnage va supprimer les fichiers sans déterminer une logique de tri. La visualisation de doublons impose donc un travail de réflexion en amont. 

**Cas 3 – Une arborescence chronologique**
[[images/image7.png]]

La visualisation d’ensemble d’une arborescence (par poids ou par nombre) peut donner les premières clefs d’analyse et d’audit. Toutefois, certains bureaux peuvent être amenés à avoir une production sérielle, qui peut être classée de façon chronologique. A plus ou moins grande échelle, tous les bureaux ont une partie d’arborescence sérielle. Le chrono-courrier d’un secrétariat, les dossiers de gestion annuelle d’un bureau des ressources humaines, le registre d’entrée ou d’élimination du bureau des archives etc. 

**Que faire ?** Pour une analyse du répertoire à échelle macro, la visualisation pondérée n’apporte aucune plus-value. En revanche, il est possible de s’appuyer sur l’ensemble des métadonnées pour aborder l’arborescence d’une autre manière. Lorsqu’un répertoire à une date de dernière modification qui remonte à plusieurs années, on peut considérer alors que ce dossier est clos. A l’instar du papier, il est possible de débuter l’évaluation. 

> **Attention :**  Bien qu’il soit simple et efficace, le classement chronologique ne peut être utilisé que partiellement.

**Cas 4 – Visualiser l’arborescence par nombre de fichiers**
Par poids :
[[images/image10.png]]
Par nombre : 
[[images/image9.png]]

***
## Autres wiki et documentation sur Archifiltre :

### [Wiki de développement](https://github.com/SocialGouv/archifiltre/wiki/Wiki-de-d%C3%A9veloppement)

### [Historique](https://github.com/SocialGouv/archifiltre/wiki/Historique)
***
