# TP 1 : Installation d’Ubuntu Server et prise en main du shell
### SABRAN Raphael & DUMAS Maxime


# Exercice 2 - Prise en main de l’interpréteur
## Manuel
### Question 1
> La commande 'which' permet de localiser une commande ou un binaire en cherchant la commande exécutable dans les dossiers spécifiques.

### Question 2
> La commande permettant de  rechercher un mot clé dans les pages du manuel est :  'man -k mot-clé'.

### Question 3
> La touche 'q' permet de sortir du manuel.

### Question 4
> La première page de chaque section (par exemple : man 6 intro) correspond à la page d'introduction de la section. On retrouve le nom de la section, une brève description, les notes de l'auteur et le colophon (références).
> La section 6 parle des jeux et programmes drôles accessibles sur le système.

## Navigation dans l’arborescence des fichiers

### Question 5/6
> il est impossible d’accéder au dossier /root car nous n'avons pas les permissions.
> On utilise donc la commande 'sudo'.
> En tapant 'sudo cd /root', nous avons une erreur car 'cd' n'est pas un programme mais une commande alors que 'sud'o permet d'éxécuter un programme en mode admin. 

### Question 8/9/10/11
> La commande 'rm' ne permet pas d’effacer le fichier si nous sommes dans le dossier parent, il faut être dans le dossier concerné pour le supprimer.
> Pour supprimer un dossier VIDE on peut utiliser la commande 'rmdir'. Elle ne fonctionne pas si un dossier contient un fichier.
> Pour supprimer un dossier ainsi que ses fichiers, on utilise la commande 'rm -r Nom_du_dossier'.

## Commandes importantes
### Question 1
>On peut utiliser la commande 'date' pour afficher l'heure. La commande 'time' permet de determiner le temps d'execution d'une commande.

### Question 2
> 'ls' : affiche la liste des dossiers.
> 'la' : affiche la liste des dossiers et des dossiers cachés.

### Question 3
> La commande 'ls' se situe dans /usr/bin.

### Question 4
> Il n'existe pas d'entrée de manuel pour ll.

### Question 5
> la commande 'ls /bin' permet de visualiser l'ensemble des fichiers contenus dans bin.

### Question 6
> la commande 'ls ..' permet de visualiser l'ensemble des fichiers contenus dans le dossier parent.

### Question 7
> la commande 'pwd' permet d'afficher le chemin complet du dossier courant.

### Question 8/9
> la commande 'echo 'yo' > plop' permet de créer le fichier plop si il n'existe pas et écrit 'yo' dedans. En la faisant une deuxieme fois, il ecrase le fichier plop et en recréer un autre avec 'yo' dedans.
> la commande 'echo 'yo' >> plop' permet, dans le fichier plop, d'écrire à la fin du fichier 'yo' vu qu'il existe.

### Question 10
> la commande 'file' permet d'afficher le type du fichier demandé.

### Question 11
> la commande 'cat' permet de visualiser le contenu d'un fichier.
> la commande 'ln' permet de créer un lien/raccourci physique entre 2 fichiers ('ln toto titi').
> Lors de la modification du fichier toto, on modifie aussi le contenu de titi.
> En écrasant toto, titi n'est pas affecté. 

### Question 12
> la commande 'ln -s' permet de créer un lien/raccourci symbolique entre 2 fichiers ('ln -s titi tutu').
> Lors de la modification du fichier tutu, on modifie aussi le contenu de titi et inversement.
> En écrasant tutu, titi n'est pas affecté mais en écrasant titi, tutu est aussi écrasé. En effet, le contenu du fichier lié symboliquement correspond au chemin du fichier original.
> Le contenu du fichier n'est pas enregistré au même endroit que les noms des fichiers.

### Question 13
> la commande 'CTRL +S' permet d'interrompre le défilement et 'CTRL + Q' permet de le reprendre.

### Question 14
> la commande 'head -5 /var/log/syslog' affiche les 5 premières lignes du fichier.
>  la commande 'tail -5 /var/log/syslog' affiche les 5 denrières lignes du fichier.
> la commande 'head -20 /var/log/syslog | tail -10' affiche les lignes 10 à 20 du fichier. En effet, on crée un pipe qui dans un premier temps prend les 20 premières lignes (head -20) mais doit prendre les 10 dernières (tail -10). Donc on peut afficher les lignes de 10 à 20 grâce à cette commande.

### Question 15
> la commande 'dmseg | less' permet d'afficher page par page ('less') le tampon des messages du noyau ('dmseg').

### Question 16
> le fichier '/etc/passwd' est une base de données donnant les utilisateurs qui peuvent se connecter au système.

### Question 17
> la commande 'sort -r /etc/passwd' permet de trier la première colonne par ordre alphabetique inverse.
> entre 'sort' et '-r', on peut specifier les colonnes (1ère colonne pour 0, 2eme colonne pour 1 ..) : +1 -2 par exemple va trier la 2eme colonne. 

### Question 18
> la commande getent passwd permet de donnée l'ensemble des utilisateurs ayant un compte sur la machine (et qui ne sont pas forcément connectés).

### Question 19
> la commande 'man -k' conversion nous indique dans quelle page du manuel est present le mot conversion. Dans notre cas, il y en a 4.

### Question 20
> la commande 'find -name "passwd"' recherche tous les fichiers se nommant passwd.

### Question 21
> En modifiant la commande de la question précédente, on peut enregistrer la liste des fichiers trouvée dans un nouveau fichier par la commande :  'find -name "passwd" > ~/list_passwd_files.txt'.
> On peut aussi mettre les erreurs dans le fichier special '/dev/null' par la commande :  'find -name "passwd" 2> /dev/null'.

### Question 22
> la commande 'grep ll' dans notre dossier personnel tourne en boucle, il n'y a pas cet alias dans notre dossier personnel.

### Question 23
> la commande 'locate history.log' nous donne le chemin ou est localisé le fichier history.log. Son chemin est : /var/log/apt/history.log.

### Question 24
> Suite à la création d'un nouveau fichier ('touch coucou'), la commande 'locate coucou' ne fonctionne pas. En effet, la commande locate va chercher le chemin du fichier dans une base de données et non pas directement au sein de l'arborescence. Sachant que cette base de données est update toutes les 24h, il est normal de ne pas trouver notre nouveau fichier. On peut mettre à jour la base de données avec la commande 'update db'.

# Exercice 3 - Decouverte de l'éditeur de texte nano

### Question 1
> la commande 'cp /var/log/syslog /home/ckali' permet de copier le fichier syslog et le coller dans le dossier ckali.
> Pour changer le nom du fichier, on utilise la commande 'mv syslog log.txt'. Ainsi, le fichier syslog est renommé en log.txt.

### Question 2
> On ouvre nano en tappant 'nano' dans le shell.
> On utilise la commande 'CTRL + \' pour modifier les termes que l'on souhaite.

### Question 3
> On utilise la commande 'CTRL + K' pour couper la ligne souhaité (qui est sauvegardé) puis 'CTRL + U' pour la coller. On se deplace ensuite à la fin du fichier texte et on refait la commande 'CTRL +U' pour copier la ligne.

### Question 4
>On utilise la commande 'ALT + U' pour annuler l'action.

### Question 5
> On enregistre le fichier avec 'CTRL + O' et on quitte avec 'CTRL + X'.

# Exercice 4 - Personnalisation du SHELL

### Question 4 
> On ajoute le code '[033[01;35m\]\A\[\033[00m\]' pour ajouter l'heure en magenta.
