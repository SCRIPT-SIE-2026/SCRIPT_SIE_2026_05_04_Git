# Travailler localement avec Git

Durant cette étape, on passera en revue les commandes de base de Git et on réalisera nos premiers commits.

## Les commandes de base

> Les commandes fournies ici peuvent, pour la plupart, être réalisées à l'aide de l'interface graphique de `VS Code`.

- Initialiser le suivi Git dans un dossier :

    ```bash
    git init
    ```

- Suivre l'état d'un dépôt :

    ```bash
    git status
    ```

- Ajouter un fichier au suivi :

    ```bash
    git add mon_fichier.txt
    ```

- Faire un commit :

    ```bash
    git commit -m "Description du commit"
    ```

- Voir l'historique des commits :

    ```bash
    git log
    ```

    Ou, pour une vision plus compacte :

    ```bash
    git log --pretty=oneline
    ```

- Annuler votre dernier commit :

    ```bash
    git reset --soft HEAD~1
    ```

    > Vous pouvez remplacer `1` par un entier positif pour annuler autant de derniers commits que souhaité. Par exemple, `git reset --soft HEAD~5` annulera vos 5 derniers commits.

## Exercices

1. Créer un fichier texte et faire son premier commit.
2. Réaliser diverses modifications et enchaîner les commits.
3. Introduire volontairement une erreur et essayer de la corriger.
4. Introduire un fichier binaire et réaliser un commit.
5. Exclure des fichiers du suivi de Git.

    > Réfléchir à de bonnes pratiques.

## Remarques

- Il existe des guides/conventions ([voir ici](https://www.conventionalcommits.org/en/v1.0.0/#specification), [ou là](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)) encadrant la rédaction des commits. Cette convention relève plutôt des bonnes pratiques informatiques.

## Bonnes pratiques

...
