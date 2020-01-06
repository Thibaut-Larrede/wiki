Cette page compile les causes des erreurs classiques remontées dans Sentry, ainsi que les versions des correctifs apportés, si ils ont lieu d'être.

# Erreurs

## Non-Error exception captured with keys ([exemple](https://sentry.fabrique.social.gouv.fr/incubateur/archifiltre/issues/1884))

Version : 2.0

Cause : Une valeur inattendue est reçue à un emplacement du code. Semble être une erreur lié directement au code, à investiguer.

## Cannot read property 'progress' of undefined ([exemple](https://sentry.fabrique.social.gouv.fr/incubateur/archifiltre/issues/2177))
Version: 2.0
Cause : Erreur lors dans le code de gestion de la progression des empreintes. N'a peut-être aucun impact sur l'affichage, mais il faudrait quand même investiguer.

## EXCEPTION_ACCESS_VIOLATION_WRITE ([exemple](https://sentry.fabrique.social.gouv.fr/incubateur/archifiltre/issues/2218))

Version: 2.0

Cause: Erreur de droits d'écriture sur un dossier. A investiguer, mais il semble dans l'exemple qu'Archifiltre essaie d'interagir avec un dossier DropBox.

## Range Error: The value "8057368521" is invalid for option "size" ([exemple](https://sentry.fabrique.social.gouv.fr/incubateur/archifiltre/issues/2213))

Version: 2.0

Cause: On essaie d'interagir avec un fichier trop gros (pas vraiment de précision là dessus, à investiguer). Il semblerait que la valeurs soit supérieure à 4Go, ce qui pourrait être une piste pour le problème.

## Command failed: %windir%\System32\REG.exe QUERY HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography /v MachineGuid

Version: 2.0

Cause: Le problème semble lié à l'exécution d'un build 32 bits sur une machine 64 bits. A creuser.

## ENOTDIR: not a directory ([exemple](https://sentry.fabrique.social.gouv.fr/incubateur/archifiltre/issues/2180))

Version: 2.0

Cause: Un fichier est identifié en tant que dossier par Archifiltre. Il n'arrive donc pas à l'ouvrir correctement.  Cause à identifier.