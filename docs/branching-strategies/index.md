# Branching Strategies

A branching strategy is essential because it allows teams to work on different features or bug fixes in parallel without interfering with each other's work. a well-designed branching strategy helps teams work more efficiently, reduces the risk of errors and conflicts, and ensures that code changes are properly managed and reviewed.

There are many branching strategies and the best strategy for a particular project depends on its size, complexity, and development process.

## GitHub flow
GitHub Flow is a simplified branching strategy often used for continuous deployment. It involves using a single branch - typically called main or master - and creating feature branches for new changes. Once the feature is complete, it is merged back into the main branch and then deployed to production

### Steps

1. **Create a new feature branch**: Start by creating a new branch from the main branch for the new feature or enhancement that you are working on.

1. **Make changes and commit**: Work on the feature branch and make the necessary changes. Once you are satisfied with the changes, commit them to the feature branch.

1. **Open a pull request:** Once the changes are committed, open a pull request to merge the changes into the main branch. This allows other team members to review the changes and provide feedback.

1. **Review and test:** Team members review the pull request and test the changes to ensure that they are stable and do not cause issues.

1. **Merge changes**: If the changes are approved, merge them into the main branch. Once the changes are merged, they become part of the main branch and are available for deployment.

1. **Deploy to production**: Once the changes are merged, they can be deployed to production. This can be done automatically or manually, depending on the needs of the project.

1. **Delete the feature branch**: Once the changes have been merged into the main branch, the feature branch can be deleted to keep the repository clean and organized.

This is most suitable for small to medium-sized projects with a small team.


## Gitflow

Gitflow involves creating two main branches - develop and master - and using feature, release, and hotfix branches to manage changes and releases.

### Branch Types
1. **Develop Branch:** This is the main branch where ongoing development work takes place. Developers create feature branches from the develop branch to work on new features or enhancements.

1. **Feature Branches:** These branches are created from the “develop” branch and are used to develop new features or enhancements. Once the feature is complete, it is merged back into the “develop” branch.

1. **Release Branches:** These branches are created from the develop branch and are used to prepare the code for a new release. The release branch is used to stabilize the code and ensure that it is ready for release. Once the release is complete, the branch is merged back into both the main branch and the “develop” branch.

1. **Master Branch:** This is the main branch where the stable code is stored. It should only contain code that has been fully tested and is ready for production use.

1. **Hotfix Branches:** These branches are created from the master branch and are used to fix critical bugs or issues that need to be addressed immediately. Once the fix is complete and tested, the branch is merged back into both the master branch and any release branches that are affected.

### Steps

1. **Create the main branches:** The first step is to create the two main branches - the master branch and the develop branch. The master branch contains the stable production-ready code, while the develop branch contains the latest development code.

1. **Create a feature branch:** When a new feature or enhancement is needed, create a feature branch from the develop branch. This branch will contain the changes for the new feature.

1. **Develop the feature:** Work on the feature branch and make the necessary changes. Once the feature is complete, test it thoroughly to ensure that it works as expected.

1. **Merge the feature branch into the develop branch:** Once the feature is complete and tested, merge the feature branch into the develop branch. This will add the new feature to the latest development code.

1. **Create a release branch:** When it is time to prepare for a new release, create a release branch from the develop branch. This branch will contain the code for the upcoming release.

1. **Test and stabilize the release:** Work on the release branch and test it thoroughly to ensure that it is stable and ready for release. If any issues are found, fix them on the release branch.

1. **Merge the release branch into the master branch:** Once the release is stable and ready for release, merge the release branch into the master branch. This will make the new release available to users.

1. **Create a hotfix branch:** If any critical issues are found in the released code, create a hotfix branch from the master branch. This branch will contain the changes needed to fix the issue.

1. **Test and stabilize the hotfix:** Work on the hotfix branch and test it thoroughly to ensure that it fixes the issue and does not introduce any new problems.

1. **Merge the hotfix branch into the master branch:** Once the hotfix is stable and tested, merge the hotfix branch into the master branch. This will make the fixed code available to users.

1. **Merge the hotfix branch into the develop branch:** Finally, merge the hotfix branch into the develop branch to ensure that the fix is included in future releases.


## Keeping Git history Clean


### Rebase instead of Pull

When you pull changes from a remote branch, Git performs a merge between the local and remote branches. This creates a new merge commit that represents the combination of the two branches. In order to keep your Git history linear and avoid unnecessary merge commits, you can use the git pull --rebase command instead.

1. **Fetch the latest changes:** Start by fetching the latest changes from the remote repository using the following command:

    ```
    git fetch origin
    ```

2. **Checkout the branch to be rebased:** Check out the branch that you want to rebase. This is typically your feature branch.
    ```
    git checkout feature-branch
    ```

3. **Perform the rebase:** Use the following command to perform the rebase:
    ```
    git pull --rebase origin target-branch
    ```
This command will fetch the latest changes from the remote target-branch, then apply the changes from your local feature-branch on top of them, creating a new linear history without any merge commits.
4. **Resolve conflicts:** If there are any conflicts between the two branches, Git will prompt you to resolve them. You can use a merge tool or manually edit the files to resolve the conflicts.
5. **Continue the rebase:** Once you have resolved any conflicts, continue the rebase process using the following command:
    ```
    git rebase --continue
    ```
This command will apply the next set of changes in the feature branch onto the target branch.
6. **Repeat steps 4 and 5:** If there are any further conflicts, repeat steps 4 and 5 until the rebase is complete.
7. **Push the changes:** Finally, push the changes to the remote repository using the following command:
    ```
    git push -f origin feature-branch
    ```

Note that the -f flag is required to force the push, since the commit history has been rewritten during the rebase process.
However, be careful when rebasing shared branches, as it can cause conflicts and make it difficult for other developers to work on the same codebase concurrently.

### Squash Merging

A squash merge is a Git merging technique that allows you to combine multiple commits into a single, more concise commit. 

1. **Squash your commits:** Once you are ready to merge your changes, squash your commits into a single commit using the following command:
    ```
    git merge --squash feature-branch
    ```
This will merge the changes from the feature branch into the main branch as a single commit, without creating a merge commit.
1. **Commit the changes:** After squashing your commits, commit the changes to the main branch using the following command:
    ```
    git commit -m "Your commit message here"
    ```
This commit message should summarize the changes that you have made in the feature branch.

Squash merging can help keep your Git history clean and organized by reducing the number of unnecessary commits, making it easier to read and understand the history of your project.









