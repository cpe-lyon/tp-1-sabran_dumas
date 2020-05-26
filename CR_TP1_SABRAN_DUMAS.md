# TP 1 : Installation d’Ubuntu Server et prise en main du shell
### SABRAN Raphael & DUMAS Maxime


# Exercice 2 - Prise en main de l’interpréteur
## Manuel
### Question 1
A l’aide du manuel, identifiez le rôle de la commande which
> La commande `which` permet de localiser une commande ou un binaire en cherchant la commande exécutable dans les dossiers spécifiques.

### Question 2
Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercher
le terme option dans la page de manuel de which ?
> La commande permettant de  rechercher un mot clé dans les pages du manuel est :  `man -k mot-clé`.

### Question 3
Comment quitte-t-on le manuel ?
> La touche `q`permet de sortir du manuel.

### Question 4
Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la
première page de la section 6 ; de quoi parle cette section ?
> La première page de chaque section (par exemple : `man 6 intro`) correspond à la page d'introduction de la section. On retrouve le nom de la section, une brève description, les notes de l'auteur et le colophon (références).
> La section 6 parle des jeux et programmes drôles accessibles sur le système.

## Navigation dans l’arborescence des fichiers

> cd : revient au dossier $HOME (dossier de l’utilisateur)
> cd chemin : va dans le dossier spécifié par chemin
> cd .. : remonte dans le dossier parent
> cd - : revient au dossier dans lequel on était précédemment
> ls : lister les répertoires et fichiers.
> pwd : afficher le répertoire où l'on se trouve exactement

> touch : créer un fichier.
> mkdir : créer un dossier.

### Question 5/6
Essayez d’accéder au dossier /root ; que se passe-t-il ?
Essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez
> il est impossible d’accéder au dossier /root car nous n'avons pas les permissions.
> On utilise donc la commande `sudo`.
> En tapant `sudo cd /root`, nous avons une erreur car `cd` n'est pas un programme mais une commande alors que `sudo` permet d'éxécuter un programme en mode admin. 

### Question 8/9/10/11
Revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis
Dossier1 ; que se passe-t-il ?
> La commande `rm` ne permet pas d’effacer le fichier si nous sommes dans le dossier parent, il faut être dans le dossier concerné pour le supprimer.
Quelle commande permet de supprimer un dossier ?
> Pour supprimer un dossier VIDE on peut utiliser la commande `rmdir`. Elle ne fonctionne pas si un dossier contient un fichier.
Comment supprimer en une seule commande Dossier2 et son contenu ?
> Pour supprimer un dossier ainsi que ses fichiers, on utilise la commande `rm -r Nom_du_dossier`.

## Commandes importantes
### Question 1
Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?
>On peut utiliser la commande `date` pour afficher l'heure. La commande `time` permet de determiner le temps d'execution d'une commande.

### Question 2
Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire
sur les fichiers commençant par un point ?
> `ls` : affiche la liste des dossiers.
> `la` : affiche la liste des dossiers et des dossiers cachés.

### Question 3
Où se situe le programme ls ?
> La commande `ls` se situe dans /usr/bin.

### Question 4
Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande ? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.
> Il n'existe pas d'entrée de manuel pour ll.

### Question 5
Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?
> la commande `ls /bin` permet de visualiser l'ensemble des fichiers contenus dans bin.

### Question 6
Que fait la commande ls .. ?
> la commande `ls ..` permet de visualiser l'ensemble des fichiers contenus dans le dossier parent.

### Question 7
Quelle commande donne le chemin complet du dossier courant ?
> la commande `pwd` permet d'afficher le chemin complet du dossier courant.

### Question 8/9
Que fait la commande echo 'yo' > plop exécutée 2 fois ?
> la commande `echo 'yo' > plop` permet de créer le fichier plop si il n'existe pas et écrit 'yo' dedans. En la faisant une deuxieme fois, il ecrase le fichier plop et en recréer un autre avec 'yo' dedans.
Que fait la commande echo 'yo' >> plop exécutée 2 fois ?
> la commande `echo 'yo' >> plop` permet, dans le fichier plop, d'écrire à la fin du fichier 'yo' vu qu'il existe.

### Question 10
A quoi sert la commande file ? Essayez la sur des fichiers de types différents.
> la commande `file` permet d'afficher le type du fichier demandé.

### Question 11
Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier
avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi :
qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?
> la commande `cat` permet de visualiser le contenu d'un fichier.
> la commande `ln` permet de créer un lien/raccourci physique entre 2 fichiers (`ln toto titi`).
> Lors de la modification du fichier toto, on modifie aussi le contenu de titi.
> En écrasant toto, titi n'est pas affecté. 

### Question 12
Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le
contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle
conséquence cela a-t-il sur tutu ?
> la commande `ln -s` permet de créer un lien/raccourci symbolique entre 2 fichiers (`ln -s titi tutu`).
> Lors de la modification du fichier tutu, on modifie aussi le contenu de titi et inversement.
> En écrasant tutu, titi n'est pas affecté mais en écrasant titi, tutu est aussi écrasé. En effet, le contenu du fichier lié symboliquement correspond au chemin du fichier original.
> Le contenu du fichier n'est pas enregistré au même endroit que les noms des fichiers.

### Question 13
 Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et
reprendre le défilement à l’écran ?
> la commande `CTRL +S` permet d'interrompre le défilement et `CTRL + Q` permet de le reprendre.

### Question 14
Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les
lignes 10 à 20.
> la commande `head -5 /var/log/syslog` affiche les 5 premières lignes du fichier.
>  la commande `tail -5 /var/log/syslog` affiche les 5 denrières lignes du fichier.
> la commande `head -20 /var/log/syslog | tail -10` affiche les lignes 10 à 20 du fichier. En effet, on crée un pipe qui dans un premier temps prend les 20 premières lignes (head -20) mais doit prendre les 10 dernières (tail -10). Donc on peut afficher les lignes de 10 à 20 grâce à cette commande.

### Question 15
Que fait la commande dmesg | less ?
> la commande `dmseg | less` permet d'afficher page par page (`less`) le tampon des messages du noyau (`dmseg`).

### Question 16
Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page
de manuel de ce fichier ?
> le fichier `/etc/passwd` est une base de données donnant les utilisateurs qui peuvent se connecter au système.

### Question 17
Affichez seulement la première colonne triée par ordre alphabétique inverse
> la commande `sort -r /etc/passwd` permet de trier la première colonne par ordre alphabetique inverse.
> entre `sort` et `-r`, on peut specifier les colonnes (1ère colonne pour 0, 2eme colonne pour 1 ..) : +1 -2 par exemple va trier la 2eme colonne. 

### Question 18
Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seulement les utilisateurs connectés) ?
> la commande `getent passwd` permet de donnée l'ensemble des utilisateurs ayant un compte sur la machine (et qui ne sont pas forcément connectés).

### Question 19
Combien de pages de manuel comportent le mot-clé conversion dans leur description ?
> la commande `man -k` conversion nous indique dans quelle page du manuel est present le mot conversion. Dans notre cas, il y en a 4.

### Question 20
A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine
> la commande `find -name "passwd"` recherche tous les fichiers se nommant passwd.

### Question 21
Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier
~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null
> En modifiant la commande de la question précédente, on peut enregistrer la liste des fichiers trouvée dans un nouveau fichier par la commande :  `find -name "passwd" > ~/list_passwd_files.txt`.
> On peut aussi mettre les erreurs dans le fichier special `/dev/null` par la commande :  `find -name "passwd" 2> /dev/null`.

### Question 22
Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu
précédemment
> la commande `grep ll` dans notre dossier personnel tourne en boucle, il n'y a pas cet alias dans notre dossier personnel.

### Question 23
Utilisez la commande locate pour trouver le fichier history.log
> la commande `locate history.log` nous donne le chemin ou est localisé le fichier history.log. Son chemin est : /var/log/apt/history.log.

### Question 24
Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?
> Suite à la création d'un nouveau fichier (`touch coucou`), la commande 'locate coucou' ne fonctionne pas. En effet, la commande locate va chercher le chemin du fichier dans une base de données et non pas directement au sein de l'arborescence. Sachant que cette base de données est update toutes les 24h, il est normal de ne pas trouver notre nouveau fichier. On peut mettre à jour la base de données avec la commande `update db`.


# Exercice 3 - Decouverte de l'éditeur de texte nano

### Question 1
Copiez le fichier /var/log/syslog dans votre dossier personnel sous le nom log.txt, puis ouvrez-le avec
nano
> la commande `cp /var/log/syslog /home/ckali` permet de copier le fichier syslog et le coller dans le dossier ckali.
> Pour changer le nom du fichier, on utilise la commande `mv syslog log.txt`. Ainsi, le fichier syslog est renommé en log.txt.

### Question 2
Remplacez toutes les occurrences du mot kernel par le mot noyau
> On ouvre nano en tappant `nano` dans le shell.
> On utilise la commande `CTRL + \` pour modifier les termes que l'on souhaite.

### Question 3
Déplacer les 10 premières lignes à la fin du fichier
> On utilise la commande `CTRL + K` pour couper la ligne souhaité (qui est sauvegardé) puis `CTRL + U` pour la coller. On se deplace ensuite à la fin du fichier texte et on refait la commande `CTRL +U` pour copier la ligne.

### Question 4
Annulez cette action
>On utilise la commande `ALT + U` pour annuler l'action.

### Question 5
Enregistrez le fichier avant de quitter nano
> On enregistre le fichier avec `CTRL + O` et on quitte avec `CTRL + X`.

# Exercice 4 - Personnalisation du SHELL

### Question 4 
> On ajoute le code `[033[01;35m\]\A\[\033[00m\]` sur la ligne PS1 =  pour ajouter l'heure en magenta.
Les lignes commençant par `PS1=` indiquent la mise en forme de l’invite de commande

