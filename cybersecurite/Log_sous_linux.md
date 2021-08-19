# Les fichiers de logs sur un système de type Linux

## Les principaux fichiers et leurs emplacements

De base les fichiers avec les logs sont sous /var/log

Pour les afficher par ordre anti-chronologique, tapez :
``` ls -lrt /var/log ```

Sachant que par défaut les logs sont surtout dans le fichier /var/log/messages voir /var/log/syslog

Pour voir en temps réel les derniers événements d'un fichier de log, utilisez la commande tail -f. 

Exemple : ```tail -f /var/log/syslog```

Syslog est un protocole définissant un service de journaux d'événements. Il collecte les logs de différents programmes et services dont ceux du kernel.

/var/log/messages lui contient des messages systèmes globaux, y compris ceux écrit lors du démarrage du système.




## Moyens de les parcourir efficacement

### Rotation des logs

Les fichiers de logs vont vivre tout au long de l'utilisation de la machine. Leur taille va donc augmenter au fur et à mesure, en ajoutant les nouvelles entrées aux logs plus anciens. Pour éviter de se retrouver avec des fichiers trop volumineux et pour faciliter la recherche dans les fichiers de logs, une rotation est mise en place nativement. La rotation des logs consiste à compresser et archiver les logs les plus anciens. Les fichiers auront alors des noms de type *.1.log, *.2.log ou bien *log.2.gz s'ils sont compressés. Cette rotation est effectuée par une tâche cron. La configuration de la rotation des logs se fait dans le fichier

```/etc/logrotate.conf```


### Swatch 

L'utilitaire swatch peut surveiller un fichier de log et réaliser une action s'il voit passer un mot-clé.

Exemple de fichier de configuration /root/.swatchrc :
```
#
# A appeler avec la ligne suivante :
#
# swatch --config-file=/root/.swatchrc --tail-file=/var/log/auth.log
#

watchfor        /FAILED/
               echo red
               #mail addresses=alex\@localhost,subject=Alerte AUTH
               exec /usr/bin/zenity --error --text "$_"

watchfor        /Successful/
               echo green
```               


### Le Serveur de log

On peut être amené à créer un serveur de log si on possède plusieurs serveurs dont on souhaite centraliser les log, par mesure de sécurité ou par commodité (facilité de consultation, d'archivage, etc...)




## Sources

https://fr.wikibooks.org/wiki/Le_syst%C3%A8me_d%27exploitation_GNU-Linux/Les_fichiers_journaux_syslog
