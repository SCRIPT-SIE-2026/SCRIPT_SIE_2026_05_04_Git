# Outils supplémentaires

*An english version of this document is available [here](Extra_tools_eng.md).*

## Pre-commit

[Pre-commit](https://pre-commit.com/) est un petit utilitaire qui permet d'automatiser des actions sur votre dépôt avant de faire un commit.
Par exemple, il peut être utilisé pour effectuer des vérifications, homogénéiser le style du code ou encore éviter de committer des fichiers trop volumineux.

> ### Prérequis
> Pour l'utiliser, il vous faudra une installation fonctionnelle de Python.
> Nous vous conseillons fortement de procéder à l'installation de votre environnement Python via `miniforge`. Un guide est disponible sur cette page [GitHub](https://github.com/conda-forge/miniforge).

Vous pouvez installer pre-commit dans votre environnement Python à l'aide de la commande suivante :

```bash
pip install pre-commit
```

Le fonctionnement de pre-commit repose sur l'édition d'un fichier de configuration nommé `.pre-commit-config.yaml`, qui devra se trouver à la racine de votre dépôt Git (au même niveau que le fichier `.git`).

Voici un exemple minimaliste de ce type de fichier de configuration :

```yaml
# .pre-commit-config.yaml
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v3.2.0
    hooks:
    -   id: trailing-whitespace
    -   id: end-of-file-fixer
    -   id: check-yaml
    -   id: check-added-large-files
```

Il vous faudra ensuite appliquer cette configuration à votre dépôt en tapant la commande suivante :

```bash
pre-commit install
```

## Le pipeline CI/CD

Les plateformes d’hébergement de code comme GitHub et GitLab proposent des systèmes d’automatisation appelés pipelines CI/CD.

Un pipeline est une suite d’actions exécutées automatiquement lorsqu’un événement se produit dans votre dépôt (par exemple : un `push` ou une `pull request`).

Ces actions permettent notamment de :

* exécuter des tests automatiquement
* compiler du code (ou un document LaTeX)
* générer des fichiers appelés artefacts (par exemple un PDF)
* déployer une application ou un site web

> L’objectif est de vérifier automatiquement que le projet fonctionne et de produire des résultats sans intervention manuelle.

**Note** : Le déclenchement de ces services est souvent limité sur les comptes gratuits (temps de calcul, nombre de minutes, etc.).

Sur GitHub, ces automatisations sont appelées **GitHub Actions**. Elles se configurent via des fichiers `.yml` placés dans le dossier `.github/workflows/` du dépôt.

Voici un exemple de fichier nommé `latex.yml` permettant de compiler un document LaTeX à chaque `push` ou `pull request`, puis de publier le PDF comme artefact téléchargeable :

```yaml
# latex.yml
name: Build LaTeX PDF

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

permissions:
  contents: read

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - name: Compile LaTeX document
        uses: xu-cheng/latex-action@v3
        with:
          root_file: main.tex

      - name: Upload PDF artifact
        uses: actions/upload-artifact@v4
        with:
          name: compiled-pdf
          path: main.pdf
```

Une mise en œuvre de cet exemple est reprise dans ce [dépôt](https://github.com/SCRIPT-SIE-2026/SCRIPT_SIE_2026_05_04_Git_CICD).
