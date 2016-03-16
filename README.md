#Clutter

## Description

Un petit utilitaire qui parcourt tout les fichiers d'un répertoire pour en trouver les lignes "TODO" et les afficher en format markdown dans le fichier README du projet.
Clutter est prévu pour fonctionner avec **Github**, mais avec quelques modification, il peut fonctionner avec n'importe quelle plateforme graphique de versionnage.

## Elements requis

* python 2.7
* Un peu de bon sens

## Usage

Pour utiliser Clutter, placez dans votre fichier README deux balises [Clutter] telles que:

    [Clutter]
    [/Clutter]
    
Ensuite, exécutez le script clutter.py à l'aide de la commande 

    python clutter.py
    
Clutter lira alors l'ensemble des fichiers présents dans le répertoire (et les sous-répertoires) dans lequel il se trouve à la recherche de ligne de commentaires contenant la mention "TODO".  
L'ensemble des élements trouvés par le script seront alors mis en page et placé entre les deux balises Clutter du fichier README comme définies plus haut.

## Clutter et GIT

Il est conseillé de lancer Clutter avant chacun de vos commit **git**. 
Pour cela, placez clutter.py dans le dossier .git/hooks de votre projet. Renommez le "pre-commit" et rendez-le exécutable. 

Il sera ainsi exécuté à chaque fois que vous réaliserez un commit, permettant ainsi de garder le README à jour en toute circonstance.

