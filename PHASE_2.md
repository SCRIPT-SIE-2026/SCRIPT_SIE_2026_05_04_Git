# Comprendre les branches

*An english version of this document is available [here](PHASE_2_eng.md).*

Par défaut, vos commits sont créés sur la branche principale de votre projet, nommée `main` ou `master`.
Une branche est un pointeur vers un commit.
Il est possible de créer d'autres branches et de basculer vers celles-ci afin de tester une fonctionnalité avant de l'intégrer à votre branche principale, par exemple.

> `Git Graph` ([ici](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)) est une extension de VS Code qui peut vous permettre de mieux visualiser vos branches.

## Commandes associées

- Lister les branches locales du dépôt :

    ```bash
    git branch
    ```

    Variante pour lister toutes les branches locales et distantes :

    ```bash
    git branch -a
    ```

- Basculer d'une branche à l'autre :

    ```bash
    git switch votre_nouvelle_branche
    ```

    **Attention** : pour basculer vers une branche, cette dernière doit exister. Vous pouvez ajouter l'option `-c` pour créer une nouvelle branche et basculer vers celle-ci :

    ```bash
    git switch -c votre_nouvelle_branche
    ```

    > Vous pouvez aussi utiliser les commandes `git checkout votre_nouvelle_branche` et `git checkout -b votre_nouvelle_branche` pour faire la même chose.

- Fusionner deux branches :

    ```bash
    git merge votre_nouvelle_branche
    ```

## Exercices

1. Sur la branche `main`, en décomposant ces étapes en plusieurs commits, créer un fichier texte et y ajouter quelques lignes.
2. Créer une nouvelle branche, ajouter une nouvelle ligne à votre fichier et faire un commit.
3. Réaliser une fusion de cette nouvelle branche depuis votre branche principale.
4. Annuler votre fusion.
5. Faire un commit sur votre branche principale, procéder à une nouvelle fusion et résoudre les conflits éventuels.

> Réfléchir à de bonnes pratiques.

## Questions et remarques

- Comment naviguer entre les branches sans forcément devoir faire un commit lors d'un travail en cours ?

    > git stash

- Comment copier seulement un fichier d'une autre branche dans ma branche actuelle ?

    > git restore --source=<autre_branche> chemin/vers/le/fichier

    Ou :

    > git checkout <autre_branche> -- chemin/vers/le/fichier

- Il est possible de naviguer entre différents commits :

    > git checkout <commit_sha>

## Expérimentations bonus

- `git rebase` permet aussi de fusionner deux branches.
- `git cherry-pick` permet d'intégrer un commit depuis une autre branche.

## Bonnes pratiques

...
