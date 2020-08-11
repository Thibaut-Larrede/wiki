# Introduction

Lors du chargement d'une arborescence, archifiltre interagit avec le système de fichier, principalement lors du calcul des empreintes qui requiert la lecture intégrale des éléments présents. Ces interactions peuvent être très longues, notamment dans le cadre de la lecture d'un disque réseau, ou de tout types de documents distants, car la vitesse de lecture est limitée par la vitesse de la connexion réseau.

Afin de contourner ce problème, nous proposons un script qui peut s'exécuter directement sur un ordinateur distant. Si vous ne savez pas comment faire, le plus simple est de contacter votre DSI.

Nous proposons 2 scripts : un script bash pour les systèmes UNIX/LINUX, et un script Powershell pour les systèmes windows.

# Utilisation des scripts

## Windows

Récupérez le script Powershell [ici](https://raw.githubusercontent.com/SocialGouv/archifiltre/master/scripts/load-from-filesystem.ps1), puis exécutez-le :

```
load-from-filesystem.ps1 chemin-vers-le-dossier-a-charger > chemin-du-fichier-de-sortie
```

Un fichier d'export sera créé.

## Unix

Récupérez le script Bash [ici](https://raw.githubusercontent.com/SocialGouv/archifiltre/master/scripts/load-filesystem.sh), puis exécutez-le :

```
./load-filesystem.sh chemin-vers-le-dossier-a-charger > chemin-du-fichier-de-sortie
```

Un fichier d'export sera créé.

Si vous avez des problèmes de droits d'exécution, vous pouvez les ajouter avant de lancer le script :

```
chmod u+x ./load-filesystem.sh
```

# Contenu du fichier d'export

Le fichier d'export contient les informations suivantes :
- Le chemin absolu vers l'arborescence chargée
- Le type de système (UNIX/Windows)
- Le chemin absolu de chacun des fichiers de l'arborescence (sans prendre en compte les fichiers cachés)
- La taille de chacun des fichiers de l'arborescence
- La date de dernière modification de chacun des éléments de l'arborescence
- L'empreinte MD5 de chacun des éléments de l'arborescence