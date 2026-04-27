# Travailler localement avec Git

Durant cette étape, on passera en revue les commandes de base de Git et on réalisera nos premiers commits.

## Les commandes de bases

- Intialiser le suivi Git dans un dossier :

    ```bash
    git init
    ```

- Suivre l'état d'un dépot :

    ```bash
    git status
    ```

- Ajouter un fichier au suivi 

    ```bash
    git add mon_fichier.txt
    ```

- Faire un commit 

    ```bash
    git commit -m "Description du commit"
    ```

- Voir l'historique des commits
    ```bash
    git log
    ```
    ou pour une vision plus compacte
    ```bash
    git log --pretty=oneline
    ```

## Excercices 

1 - Créer un fichier texte et faire son premier commit
2 - Réaliser divers modifications et enchaîner les commits
3 - Introduire volontaire une erreur et essayer de la corriger 
4 - Introduire un fichier binaire et réaliser un commit  

## Bonus

- Il existe des guides/cenventions ([voir ici](https://www.conventionalcommits.org/en/v1.0.0/#specification), [ou là](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)) encadrant la rédaction des commits. Cette convention relève plutôt des bonnes pratiques informatiques.

