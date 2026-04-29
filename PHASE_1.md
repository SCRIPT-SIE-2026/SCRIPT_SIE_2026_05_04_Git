# Travailler localement avec Git

*An english version of this document is available [here](PHASE_1_eng.md).*

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

    > Vous pouvez remplacer `1` par un entier positif pour annuler autant de commits récents que souhaité. Par exemple, `git reset --soft HEAD~5` annulera vos 5 derniers commits.

## Exercices

1. Créer un fichier texte et faire son premier commit.
2. Réaliser diverses modifications et enchaîner les commits.
3. Introduire volontairement une erreur et essayer de la corriger.
4. Introduire un fichier binaire et réaliser un commit.
5. Exclure des fichiers du suivi de Git.

    > Réfléchir à de bonnes pratiques.

## Remarques

### Les messages de commit

Il existe des guides/conventions ([voir ici](https://www.conventionalcommits.org/en/v1.0.0/#specification), [ou là](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)) encadrant la rédaction des commits. Cette convention relève plutôt des bonnes pratiques informatiques.

En général, on peut se référer à ces conseils simples :

- privilégier un message court (50 caractères maximum) ;
- donner du contexte si besoin ;
- séparer les changements.

> Puis-je comprendre ce que fait ce commit juste avec son message de commit ?

Le formalisme le plus répandu est le suivant :

```bash
type: court résumé
```

Les types souvent utilisés sont les suivants :

```yaml
add: ajout d'un nouveau fichier
feat: ajout de fonctionnalité
fix: correction de bug
docs: documentation
refactor: changement sans impact fonctionnel
test: ajout/modification de tests
wip: (work in progress) dédié aux branches de développement
chore: changements relatifs à la configuration de votre dépôt
```

> &#x1F4A1; Un bon message de commit va de pair avec un bon regroupement/découpage de vos modifications dans votre commit.

Un exemple simple, j'ai ajouté une nouvelle section à un document : 

```yaml
feat: add new section "Chapter 1: Were Ross and Rachel on a break ?"
```

## Bonnes pratiques

...
