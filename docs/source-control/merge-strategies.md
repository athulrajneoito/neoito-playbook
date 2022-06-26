# Merge strategies
## Approach for non-linear commit history
Merging topic into main

```
  A---B---C topic
 /         \
D---E---F---G---H main

git fetch origin
git checkout main
git merge topic

```

## Two approaches to achieving a linear commit history
### Rebase the topic branch before merging it into the main
Before merging the `topic` into the `main`, we rebase the `topic` with the `main` branch: 

```
          A---B---C topic
         /         \
D---E---F-----------G---H main

git checkout main
git pull
git checkout topic
git rebase origin/main

```

create a PR topic --> main and approve using the squash merge option
### Rebase the topic branch before squash merges into the main
[Squash merging](https://docs.microsoft.com/en-us/azure/devops/repos/git/merging-with-squash?view=azure-devops) is a merge option that allows you to condense the Git history of topic branches when you complete a pull request. Instead of adding each commit on the `topic` to the history of `main`, a squash merge takes all the file changes and adds them to a single new commit on `main`.

```
          A---B---C topic
         /
D---E---F-----------G---H main
```

Create a PR topic --> main and approve using the squash merge option
