A basic Git workflow is as follows; you can find more information on the specific steps below.

**Pull latest changes**
> git pull
 
**Start a new feature branch based on the develop branch**
> git checkout -b feature/123-add-git-instructions develop

**Edit files**
> add and commit the files 

**Git add file**
> git commit -m "meaningful commit message"

**Check your changes**
> git status
 
**Push the branch to the remote repository**
> git push --set-upstream origin feature/123-add-git-instructions


### Cloning
Whenever you want to make a change to a repository, you need to first clone it. Cloning a repository pulls down a full copy of all the repository data, so that you can work on it locally. This copy includes all versions of every file and folder for the project.

> git clone https://github.com/username/repo-name

You only need to clone the repository the first time. Before any subsequent branches you can sync any changes from the remote repository using git pull.


### Branching
To avoid adding code that has not been peer reviewed to the main branch (ex. develop) we typically work in feature branches, and merge these back to the main trunk with a Pull Request. It's even the case that often the main or develop branch of a repository are locked so that you can't make changes without a Pull Request. Therefore, it is useful to create a separate branch for your local/feature work, so that you can work and track your changes in this branch.
Pull the latest changes and create a new branch for your work based on the trunk (in this case develop).

> git pull

> git checkout -b feature/feature-name develop

At any point, you can move between the branches with **git checkout <branch>** as long as you have committed or stashed your work. If you forget the name of your branch use **git branch --all** to list all branches.


### Committing
To avoid losing work, it is good to commit often in small chunks. This allows you to revert only the last changes if you discover a problem and also neatly explains exactly what changes were made and why.

1. Make changes to your branch
2. Check what files were changed with git status command
3. Track the files you wish to include in the commit. To track all modified files:
> git add --all      
**Or to track only specific files:**     
> git add source-control/git-guidance/readme.md
4. Commit the changes to your local branch with a descriptive commit message
> git commit -m "add basic git instructions"


### Pushing
When you are done working, push your changes to a branch in the remote repository using:
> git push

The first time you push, you first need to set an upstream branch as follows. After the first push, the --set-upstream parameter and branch name are not needed anymore.
> git push --set-upstream origin feature/feature-name

Once the feature branch is pushed to the remote repository, it is visible to anyone with access to the code.

### Merging

We encourage the use of Pull Request to merge code to the main repository to make sure that all code in the final product is properly reviewed.
The Pull Request (PR) process in GitHub and other similar tools make it easy both to start a PR, review a PR and merge a PR.
 
**Merge Conflicts**   
If multiple people make changes to the same files, you may need to resolve any conflicts that have occurred before you can merge.

**Check out the develop branch and get the latest changes**
> git checkout develop
git pull
 
**Check out your branch**
> git checkout <your branch>
 
**Merge the develop branch into your branch**
> git merge develop
**If merge conflicts occur, above command will fail with a message telling you that there are conflicts to be solved**
**Find which files need to be resolved**
> git status
 
You can start an interactive process that will show which files have conflicts. Sometimes you removed a file, where it was changed in dev. Or you made changes to some lines in a file where another developer made changes as well. 
When editing conflicts occur, the process will automatically open Visual Studio Code where the conflicting parts are highlighted in green and blue, and you have make a choice:


* Accept your changes (current)
* Accept the changes from dev branch (incoming)
* Accept them both and fix the code (probably needed)
When this process is completed, make sure you test the result by executing build, checks, test to validate this merged result.

**Conclude the merge**
> git merge --continue
 
**Verify that everything went ok**
> git log

**push the changes to the remote branch**
> git push
If no other conflicts appear, the PR can now be merged, and your branch deleted. Use squash to reduce your changes into a single commit, so the commit history can be within an acceptable size.


### Stashing changes
**git stash** is super handy if you have uncommitted changes in your working directory, but you want to work on a different branch. You can run git stash, save the uncommitted work, and revert to the HEAD commit. You can retrieve the saved changes by running git stash pop:
 
> git stash    
…    
git stash pop
 
Or you can move the current state into a new branch:
> git stash branch "new_branch_to_save_changes"


### Recovering lost commits
 
If you "lost" a commit that you want to return to, for example to revert a git rebase where your commits got squashed, you can use **git reflog** to find the commit:

> git reflog     

Then you can use the reflog reference (HEAD@{}) to reset to a specific commit before the rebase:   
> git reset HEAD@{2}


## Managing Remotes
A local git repository can have one or more backing remote repositories. You can list the remote repositories using git remote - by default, the remote repository you cloned from will be called origin
> git remote -v


### Rolling back changes
Reverting and deleting commits
To "undo" a commit, run the following two commands: **git revert** and **git reset**. git revert creates a new commit that undoes commits while git reset allows deleting commits entirely from the commit history.

To delete the latest commit use HEAD~:
> git reset --hard HEAD~1

To delete commits back to a specific commit, use the respective commit id:
> git reset --hard "sha1-commit-id"
 
After you deleted the unwanted commits, push using force:
> git push origin HEAD --force

Interactive rebase for undoing commits:
> git rebase -i HEAD~N     

The above command will open an interactive session in an editor (for example vim) with the last N commits sorted from oldest to newest. To undo a commit, delete the corresponding line of the commit and save the file. Git will rewrite the commits in the order listed in the file and because one (or many) commits were deleted, the commit will no longer be part of the history.
Running rebase will locally modify the history, after this one can use force to push the changes to remote without the deleted commit.
