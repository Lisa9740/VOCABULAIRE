# SUID sous linux

Un répertoire avec un file owner et un groupe lit, écrit, et exécute les permissions, mais pour les autres il lit et exécute seulement . Il y a en fait 3 permissions en plus.
Les permissions spéciaux ajoute un quatrième niveau d'accès s'ajoutant déja aux utilisateur, group et autres

=> SUID (Set owner User ID up on execution) est un type de permission spécial assigné à un fichier (script ou application) sous linux. Il permet d'avoir les permissions du file owner
plutôt que les permissions de la personne qui a lancer le programme. Quand le SUID est activé sur un exécutable, l'utilisateur qui éxecute le fichier dispose des 
même droits que le propriétaire.

```valeur octale : 4000, valeur symbolique : s ```

## Cas d'activation du SUID

``` sudo chmod +4000 $(which chown) ```

``` ls -l $(which chown) ```

``` -rwsr-xr-x. 1 root root 62792 10 jun  2014 /usr/bin/chown ```

## Sécurité

Mettre un fichier, et surtout un programme, en Setuid (SUID) ou Setgid (Set User Group ID) n'est pas anodin car cela court-circuite le système de protection. Ainsi la commande chmod ug+s /bin/bash donne les droits root à toute
personne qui ouvre un terminal ou qui lance l'interpréteur de commande bash


