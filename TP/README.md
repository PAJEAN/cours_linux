# Travaux pratiques: Initiation aux commandes Unix/Linux (distribution Ubuntu)

Ce TP constitue le guide de survie en territoire Linuxien. Il vous permettra d'acquérir le savoir et les compétences indispensables à l'informaticien que vous êtes. Fais chauffer le moteur Marcel !

## Mise en place

* Ouvrez un terminal (*Ctrl + Alt + T*).
* Placez vous dans le répertoire *~/Documents* (si le dossier n'existe pas le créer).
* Télécharger l'archive compressée à l'adresse suivante: https://github.com/PAJEAN/cours_linux/archive/master.zip
* Décompresser l'archive *.zip* obtenue puis la supprimer.
* Placez vous dans le répertoire *~/Documents/cours_linux-master/TP/*.
* Télécharger la commande **tree** et **cowsay** à l'aide du gestionnaire de paquets **apt** puis utiliser la commande **tree** à la racine du répertoire *TP* (le gestionnaire *apt* est disponible pour les distributions dérivées de Debian comme Ubuntu, sur Mac vous pouvez télécharger le gestionnaire de paquets *Homebrew*).
* Modifier le nom du fichier *lanceleau_de_la_riviere* par *lancelot_du_lac*.
* Créer un répertoire *Personnages* puis les sous-répertoires suivants: *Arthur*, *Perceval* et *Lancelot_du_lac*.
* Déplacer les fichiers *arthur*, *perceval* et *lancelot_du_lac* dans leur répertoire Personnages correspondant.

## Les processus

* Afficher la liste de tous vos processus en cours d'exécution.
* Exécuter la commande sleep 6000 en **arrière plan** et vérifier qu'elle est bien en cours d'exécution.
* Tuer la commande lancée précédemment.

## Manipuler les fichiers

* Concaténer les fichiers *citation_1.txt* et *citation_2.txt* dans un fichier *citations.txt* puis supprimer les fichiers *citation_1.txt* et *citation_2.txt*.
* Compter le nombre de mots présents dans le fichier *vocabulaire.txt*.
* Compter le nombre de colonnes dans le fichier *episodes.tsv*.
* Compter le nombre de fichiers *.txt* dans le répertoire *Missive*.
* Elle est où la poulette ? À quelle ligne apparaît précisément le mot "poulette" dans le fichier *vocabulaire.txt*.
* Créer une commande qui recherche un terme dans le fichier *vocabulaire.txt*. Lorsque le terme en paramètre n’existe pas alors afficher dans la console "Word not found".

## Les filtres
* Afficher toutes les citations d’Arthur dans le fichier *citations.txt*.
* Créer un fichier *citations.txt* dans le répertoire Arthur contenant toutes les citations d’Arthur. Utiliser une opération de redirection.
* Quel est la majuscule la plus utilisée dans le fichier *citations.txt*.
* Trouver tous les épisodes qui commencent par le pronom "Le" à partir du fichier *episodes.tsv*.
* Minifier toutes les majuscules dans le fichiers *episodes.tsv*.
* Lister uniquement les noms des épisodes du livre 2 à partir du fichier *episodes.tsv*.
* Lister uniquement les noms des épisodes qui ne sont pas du livre 2 à partir du fichier *episodes.tsv*.
* Trier dans l’ordre alphabétique uniquement les noms des épisodes du fichier *episodes.tsv*.
* Trier les épisodes (sans tenir compte de la première ligne) par livre, tome et épisode (délimiter avec $'\t' http://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#ANSI_002dC-Quoting) du fichier *episodes.tsv*.
* A partir notamment de la commande **pwd**, afficher uniquement le nom du répertoire dans lequel vous vous trouvez.
* Afficher tous les mots de taille 6 contenant un palindromes au sein du fichier *vocabulaire.txt*.


## Les missives

* Affichez à la suite les fichiers *arthur*, *lancelot_du_lac* et *perceval* respectivement localisés dans leur répertoire *Personnages*.
* À partir de l’affichage précédent, affichez uniquement les majuscules.
* À partir de l’indice précédent, décodez le fichier *Missives/missives_1.txt*.
* Afficher les épisodes du livre 4 listés dans le fichier *episodes.tsv*, substituer la chaîne de caractère “Les ” par une chaîne de caractères vide et afficher la première lettre de chaque nom d’épisode.
* Utilisez l’indice précédent pour décoder missive_2.txt.
* Créez un fichier *missive_3.txt* au sein du répertoire *Missives* et ajouter les lignes suivantes:

`Abricot\nRhubarbe\nTomate\nHaricot\nUgli\nRaisin`

* Affichez uniquement la première lettre de chaque ligne du fichier *missive_3.txt*.

## Bonus

* À partir de la commande suivante extraire la valeur du champs "value".

`wget -q -O - https://api.chucknorris.io/jokes/random`

* Appliquer le résultat à la commande cowsay de la façon suivante:

`cowsay $(x)`

où x est la commande précédente.

# Auteur

Pierre-Antoine Jean (IMT Mines Alès).