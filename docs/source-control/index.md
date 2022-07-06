# Source Control
There are many options when working with Source Control. Github, Gitlab, bitbucket etc. For Public projects, Github can be used.
## Goal
- Following industry best practices to work in geo-distributed teams encourages contributions.
- Improve code quality by enforcing reviews before merging into main branches
- Improve traceability of features and fixes through a clean commit history

## General Guidance
Consistency is important, so agree to the approach as a team before starting to code. Treat this as a design decision, so include a design proposal and review, in the same way as you would document all design decisions
## Creating a new repository
When creating a new repository, the team should at least do the following

- Agree on the **branch**, **release,** and **merge strategy**
- Define the merge strategy ([linear or non-linear](../source-control/merge-strategies.md))
- Lock the default branch and merge using [pull requests (PRs)](../pull-requests/index.md)
- Agree on [branch naming](./naming-branches.md) (e.g. user/your\_alias/feature\_name)
- Establish [branch/PR policies](../pull-requests/index.md)
- For public repositories the default branch should contain the following files:
  - LICENSE
  - README.md
  - CONTRIBUTING.md
## Contributing to an existing repository
When working on an existing project, git clone the repository and ensure you understand the team's branch, merge and release strategy (e.g. through the project [CONTRIBUTING.md file](https://blog.github.com/2012-09-17-contributing-guidelines/))
