# Working Locally with Git

During this step, we will review the basic Git commands and make our first commits.

## Basic Commands

> Most of the commands provided here can be run using the `VS Code` graphical interface.

- Initialize Git tracking in a folder:

    ```bash
    git init
    ```

- Check the status of a repository:

    ```bash
    git status
    ```

- Add a file to tracking:

    ```bash
    git add mon_fichier.txt
    ```

- Make a commit:

    ```bash
    git commit -m "Commit description"
    ```

- View the commit history:

    ```bash
    git log
    ```

    Or, for a more compact view:

    ```bash
    git log --pretty=oneline
    ```

- Undo your last commit:

    ```bash
    git reset --soft HEAD~1
    ```

    > You can replace `1` with a positive integer to undo as many recent commits as needed. For example, `git reset --soft HEAD~5` will undo your last 5 commits.

## Exercises

1. Create a text file and make your first commit.
2. Make several changes and create a sequence of commits.
3. Deliberately introduce an error and try to fix it.
4. Add a binary file and make a commit.
5. Exclude files from Git tracking.

    > Think about best practices.

## Notes

- There are guides/conventions ([see here](https://www.conventionalcommits.org/en/v1.0.0/#specification), [or here](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)) that define how commit messages should be written. This convention is more a matter of software engineering best practices.

## Best Practices

...
