
# Git Commands Guide

## Creating a Branch
To create a new branch:
```zsh
git checkout -b MY_BRANCH
```


## Pushing a Local Branch to Remote
To push your local branch to the remote repository:

- **First time**:
    ```zsh
    git push origin -u MY_BRANCH
    ```
- **Subsequent times**:
    ```zsh
    git push
    ```

## Tracking a Remote Branch
To track a remote branch:

1. Update local references to remote repository, and view all remote branches:
    ```zsh
    git fetch --prune
    git branch -r
    ```
2. Check out the remote branch and create a corresponding local branch:
    ```zsh
    git checkout -b MY_BRANCH origin/MY_BRANCH
    ```

## Merging a Branch
To merge when you are on the local branch:

```zsh
git checkout main
git pull origin main
git merge MY_BRANCH
git push origin HEAD:main
git branch -d MY_BRANCH
git push origin -d MY_BRANCH
``` 
Explanation:
1. Switch to the `main` branch
2. Pull the latest changes from the remote `main` branch into your local `main` branch
3. Merge your branch (`MY_BRANCH`) into the local `main` branch
4. Push the latest commit of the local `main` branch to the remote `main` branch
5. It is now safe to delete the branch locally...
6. ... and remotely


## Force gitignore
git rm --cached YOUR_FILE