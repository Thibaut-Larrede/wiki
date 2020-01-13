Description des interactions avec le système de fichiers et des erreurs pouvant en résulter.

# Chargement de l'arborescence

## `fs.statSync()`

### Usage

`fs.statSync` est appelée récursivement sur les éléments du système de fichier. Elle permet de parcourir l'arborescence et d'obtenir la liste des enfants pour les dossiers, et la la taille et date de modification pour les fichiers.

### Erreurs possibles

- ENOENT : Le fichier ou dossier n'existe pas
- EACCES : L'utilisateur n'a pas les droits d'accès sur le fichier / dossier.

# Calcul des hashs

## `md5File.sync()`

### Usage

`md5File.sync` est appelée sur l'ensemble des fichiers afin de calculer leur empreinte.

### Erreurs possibles

- ENOENT : Le fichier n'existe pas. Peut se produire si le fichier a été déplacé entre le chargement et le calcul des empreintes.
- EACCES : L'utilisateur n'a pas les droits de lecture sur le fichier.
