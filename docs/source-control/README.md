Improve code quality by enforcing reviews before merging into main branches
Improve traceability of features and fixes through a clean commit history
 
### Creating a new repository
When creating a new repository, the team should agree on the following:
 
* Agree on the branch, release and merge strategy
* Define the merge strategy.
* Lock the default branch and merge using pull requests (PRs)
* Agree on branch naming (e.g. user/your_alias/feature_name)
* Establish branch/PR policies
* For public repositories the default branch should contain the following files:
    1.  LICENSE
    2.  README.md


### Contributing to an existing branch
When working on an existing project, git clone the repository and ensure you understand the team's branch, merge and release strategy

### Commit Best Practices

* Make small commits. This makes changes easier to review, and if we need to revert a commit, we lose less work.
* Commit complete and well tested code. Never commit incomplete code, get in the habit of testing your code before committing.
* Write meaningful and easy to understand commit messages.

A good commit message should answer these questions:

* Why is it necessary? It may fix a bug, add a feature, improve performance, or just be a change for the sake of correctness
* How does it address the issue? For short, obvious changes, this can be omitted
* What effects does this change have? In addition to the obvious ones, this may include benchmarks, side effects etc.
* What limitations does the current code have?

How to write a great commit message:

1. Separate subject from body with a blank line - If the change is simple enough to understand from a single lined commit message, this can be omitted.
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line. A properly formed Git commit subject line should always be able to complete the following sentence:
> If applied, this commit will your subject line here.
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

### Naming Branches
When contributing to existing projects, look for and stick with the agreed branch naming convention.In the beginning of a new project the team agrees on the project conventions including the branch naming strategy.

Here's an example of a branch naming convention:

> user alias/feature/bug/hotfix/Issue/Ticket ID/Subtask ID_title
