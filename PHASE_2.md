# Comprendre les branches

Par défaut, vos commits sont créer sur la branche principale de votre projet nommé `main`ou `master` 
Une branche est un pointeur vers un commit.
Il est possible de créer et basculer vers d'autres branches pour par exemple tester une fonctionnalité avant de l'intégrer à votre branche principale.

L'extension VSCode `Git Graph` [ici](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph) est un outil qui peut vous permettre de mieux visualiser vos branches.
## Commandes associées

- Lister les branches locales du dépôt :

    ```bash
    git branch
    ```
    variante pour lister toutes les branches locales et distantes:
    ```bash
    git branch -a
    ```    
- Basculer d'une branch à l'autre : 
    ```bash
    git switch votre_nouvelle_branche
    ````
    **Attention**: Pour basculer vers une branche cette dernier doit exister, vous pour ajouter l'option -c pour créer et basculer vers une nouvelle branche
    ```bash
    git switch -c votre_nouvelle_branche
    ````

- Fusionner deux branches
    ```bash
    git merge votre_nouvelle_branche
    ```

    

