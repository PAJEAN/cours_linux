# Travaux pratiques: Initiation aux commandes Linux

Ce TP constitue le guide de survie en territoire Linuxien. Il vous permettra d'acquérir le savoir et les compétences indispensables à l'informaticien que vous êtes.

**Certaines questions peuvent être résolues de plusieurs manières en employant une suite de commandes différentes. Aucun script ne doit être utilisé pour répondre à ces questions.**

## Mise en place

* Accéder au terminal.

### Si vous n'utilisez pas un environnement *online*:

* Placez vous dans le répertoire *~/Documents* (si le répertoire n'existe pas, le créer).
* Télécharger l'archive compressée à l'aide de l'une des commandes suivantes:

```
wget https://github.com/PAJEAN/cours_linux/archive/master.zip
```
ou

```
git clone https://github.com/PAJEAN/cours_linux.git
```

* Décompresser l'archive *.zip* obtenue.

```
unzip master.zip
```

* Placez vous dans le répertoire *~/Documents/cours_linux-master/TP/*.

### Si vous utilisez l'environnement *Replit*:
* Placez vous dans le répertoire */home/runner/courslinux/TP/*

### Si vous utilisez l'environnement *MyBinder*:
* Placez vous dans le répertoire *~/TP/*.

## Les processus

* Afficher la liste de tous vos processus en cours d'exécution.
* Exécuter la commande sleep 6000 en **arrière plan** et vérifier qu'elle est bien en cours d'exécution.
* Tuer la commande lancée précédemment.

## Manipuler les fichiers

* Lister tous les fichiers (y compris les fichiers cachés) et les répertoires. 
* Modifier le nom du fichier *lanceleau_de_la_riviere* par *lancelot_du_lac*.
* Créer un répertoire *Personnages* puis les sous-répertoires suivants: *Arthur*, *Perceval* et *Lancelot_du_lac*.
* Déplacer les fichiers *arthur*, *perceval* et *lancelot_du_lac* dans leur répertoire Personnages correspondant.
* Concaténer les fichiers *citation_1.txt* et *citation_2.txt* dans un fichier *citations.txt* puis supprimer les fichiers *citation_1.txt* et *citation_2.txt*.
    <details>
        <summary><i style="color:#aaa">Indice</i></summary> 
        <i>Redirections des flux E/S.</i>
    </details>
* Compter le nombre de mots présents dans le fichier *vocabulaire.txt*.
* Compter le nombre de colonnes dans le fichier *episodes.tsv* (le séparateur entre les colonnes est la tabulation).
    <details>
        <summary><i style="color:#aaa">Indice</i></summary> 
        <i>Une tabulation est symbolisée par le caractère <b>\t</b> et un saut de ligne par le caractère <b>\n</b>.</i>
    </details>
* Compter le nombre de fichiers *.txt* dans le répertoire *.missive*.
* Compter le nombre de fichiers et répertoires cachés au sein de */TP*.
* À quelle ligne apparaît précisément le mot "poulette" dans le fichier *vocabulaire.txt* (*Elle est où la poulette ?*).
* À partir de la commande *grep*, afficher dans la console "Word not found" lorsque le terme recherché n'existe pas dans le fichier *vocabulaire.txt*.
* Le fichier adresses_mail.txt contient des lignes vides. Afficher l'ensemble des adresses mail sans inclure les lignes vides.

## Les filtres
* Afficher toutes les citations d’Arthur dans le fichier *citations.txt*.
* Créer un fichier *citations.txt* dans le répertoire Arthur contenant toutes les citations d’Arthur. Utiliser une opération de redirection.
* Quel est la majuscule la plus utilisée dans le fichier *citations.txt*.
* Trouver tous les épisodes qui commencent par le pronom "Le" à partir du fichier *episodes.tsv*.
* Afficher uniquement les **noms des répertoires** fils de *TP/* en incluant les répertoires cachés.
    <details>
        <summary><i style="color:#aaa">Indice</i></summary> 
        <i>L'option -F de ls ajoute un indicateur aux entrées.</i>
    </details>
* Minifier toutes les majuscules dans le fichiers *episodes.tsv*.
* Lister uniquement les noms des épisodes du livre 2 à partir du fichier *episodes.tsv*.
* Lister uniquement les noms des épisodes qui ne sont pas du livre 2 à partir du fichier *episodes.tsv*.
* Trier dans l’ordre alphabétique uniquement les noms des épisodes du fichier *episodes.tsv*.
* Trier les épisodes (sans tenir compte de la première ligne) par livre, tome et épisode (délimiter avec l'option *-t$'\t'* http://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#ANSI_002dC-Quoting) du fichier *episodes.tsv*.
    <details>
        <summary><i style="color:#aaa">Indice</i></summary> 
        <i>L'option -k suivie d'un numéro de colonne permet de trier selon une colonne spécifique (l'option peut être employée plusieurs fois).</i>
    </details>
* A partir notamment de la commande **pwd**, afficher uniquement le nom du répertoire dans lequel vous vous trouvez.
* Afficher tous les mots de taille 6 contenant un palindromes au sein du fichier *vocabulaire.txt*.
    <details>
        <summary><i style="color:#aaa">Indice</i></summary> 
        <i>L’expression « (.)\1 » représente le motif « un caractère répété ».</i>
    </details>
* Afficher à partir du fichier adresses_mail.txt tous les noms de domaine et les trier dans l'ordre alphabétique.
* Afficher à partir du fichier adresses_mail.txt tous les noms d'extension et le nombre de fois qu'ils apparaissent.


## Les missives

* Afficher à la suite les fichiers *arthur*, *lancelot_du_lac* et *perceval* respectivement localisés dans leur répertoire *Personnages*.
* À partir de l’affichage précédent, afficher uniquement les majuscules.
* À partir de l’indice précédent, décoder le fichier *missives_1.txt* situé dans le répertoire caché *.missives*.
* Afficher les épisodes du livre 4 listés dans le fichier *episodes.tsv*, substituer la chaîne de caractère “Les ” par une chaîne de caractères vide et afficher la première lettre de chaque nom d’épisode.
* Utiliser l’indice précédent pour décoder missive_2.txt.
* Créer un fichier *missive_3.txt* au sein du répertoire *Missives* et ajouter les lignes suivantes:

`Abricot\nRhubarbe\nTomate\nHaricot\nUgli\nRaisin`

* Afficher uniquement la première lettre de chaque ligne du fichier *missive_3.txt*.

## Bonus

* À partir de la commande suivante extraire la valeur du champs "value".

`wget -q -O - https://api.chucknorris.io/jokes/random`

* Appliquer le résultat à la commande cowsay de la façon suivante:

`cowsay $(x)`

où x est la commande précédente. Si vous n'avez pas la commande cowsay, vous pouvez la télécherger à l'aide de votre gestionnaire de package (apt pour les distribution debian, Homebrew pour MacOs, etc.). Par exemple: `sudo apt install cowsay`.

# Auteur

Pierre-Antoine Jean (IMT Mines Alès).