# Print Nightmare 

 Il s’agit d’un exploit qui permettait à un pirate d’exécuter du code à distance sur la machine cible, avec le niveau d’accès le plus élevé. Cela lui offrait de nombreuses possibilités de nuire : installer des programmes, modifier ou voler des données, créer ou supprimer des utilisateurs. Selon Microsoft, la vulnérabilité d’exécution de code à distance se produit lorsque le service Spouleur d’impression Windows exécute de manière incorrecte des opérations sur les fichiers privilégiés.
 
 Comment s'en protéger ? 
La première chose à faire est de désactiver le service File d’attente d’impression si votre ordinateur n’a pas d’imprimante. Si vous possédez une imprimante, nous vous recommandons la procédure suivante :

* Accédez à Modifier la stratégie de groupe.
* Allez ensuite dans Configuration de l’ordinateur.
* Cliquez sur Modèles d’administration.
* Sélectionnez Imprimantes.
* Maintenant, nous désactivons Autoriser le gestionnaire de travaux d’impression à accepter les connexions client.
* Et c’est tout, avec cette procédure, vous protégerez votre ordinateur de la vulnérabilité Print Nightmare.
