# Structure of a Sprint

## The first week of a Project

### Before starting the project
[Discuss and start writing the Team Agreements](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/team-agreements/). Update these documents with any process decisions made throughout the project

[Working Agreement](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/team-agreements/working-agreements/)

[Definition of Ready](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/team-agreements/definition-of-ready/)

[Definition of Done](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/team-agreements/definition-of-done/)

[Estimation](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/core-expectations/)

[Set up the repository/repositories](https://neoito-hub.github.io/code-with-engineering-playbook/source-control/#creating-a-new-repository)

Decide on repository structure/s

Add [README.md](https://neoito-hub.github.io/code-with-engineering-playbook/resources/templates/), [LICENSE](https://neoito-hub.github.io/code-with-engineering-playbook/SPRINT-STRUCTURE/resources/templates/LICENSE), [CONTRIBUTING.md](https://neoito-hub.github.io/code-with-engineering-playbook/resources/templates/CONTRIBUTING/), .gitignore, etc

[Build a Product Backlog](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/backlog-management/readme/)

Set up a project in your chosen project management tool (ex. Azure DevOps)

[INVEST](https://en.wikipedia.org/wiki/INVEST_\(mnemonic\)) in good User Stories and Acceptance Criteria

[Non-Functional Requirements Guidance](https://neoito-hub.github.io/code-with-engineering-playbook/design/design-patterns/non-functional-requirements-capture-guide/)
### Day 1
[Plan the first sprint](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/core-expectations/)

Agree on a sprint goal, and how to measure the sprint progress

Determine team capacity

Assign user stories to the sprint and split user stories into tasks

Set up Work in Progress (WIP) limits

[Decide on test frameworks and discuss test strategies](https://neoito-hub.github.io/code-with-engineering-playbook/automated-testing/)

Discuss the purpose and goals of tests and how to measure test coverage

Agree on how to separate unit tests from integration, load and smoke tests

Design the first test cases

[Decide on branch naming](https://neoito-hub.github.io/code-with-engineering-playbook/source-control/naming-branches/)

[Discuss security needs and verify that secrets are kept out of source control](https://neoito-hub.github.io/code-with-engineering-playbook/continuous-delivery/secrets-management/recipes/azure-devops/secrets-per-branch/)
### Day 2
[Set up Source Control](https://neoito-hub.github.io/code-with-engineering-playbook/source-control/)

Agree on [best practices for commits](https://neoito-hub.github.io/code-with-engineering-playbook/source-control/#commit-best-practices)

[Set up basic Continuous Integration with linters and automated tests](https://neoito-hub.github.io/code-with-engineering-playbook/continuous-integration/)

[Set up meetings for Daily Stand-ups and decide on a Process Lead](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/core-expectations/)

Discuss purpose, goals, participants and facilitation guidance

Discuss timing, and how to run an efficient stand-up

[If the project has sub-teams, set up a Scrum of Scrums](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/effective-organization/scrum-of-scrums/)
### Day 3
[Agree on code style](https://neoito-hub.github.io/code-with-engineering-playbook/code-reviews/) and on [how to assign Pull Requests](https://neoito-hub.github.io/code-with-engineering-playbook/code-reviews/pull-requests/)

[Set up Build Validation for Pull Requests (2 reviewers, linters, automated tests)](https://neoito-hub.github.io/code-with-engineering-playbook/code-reviews/) and agree on [Definition of Done](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/team-agreements/definition-of-done/)

[Agree on a Code Merging strategy](https://neoito-hub.github.io/code-with-engineering-playbook/source-control/merge-strategies/) and update the [CONTRIBUTING.md](https://neoito-hub.github.io/code-with-engineering-playbook/resources/templates/CONTRIBUTING/)

[Agree on logging and observability frameworks and strategies](https://neoito-hub.github.io/code-with-engineering-playbook/observability/)
### Day 4
[Set up Continuous Deployment](https://neoito-hub.github.io/code-with-engineering-playbook/continuous-delivery/)

Determine what environments are appropriate for this solution

For each environment discuss purpose, when deployment should trigger, pre-deployment approvers, sing-off for promotion.

[Decide on a versioning strategy](https://neoito-hub.github.io/code-with-engineering-playbook/source-control/component-versioning/)

Agree on how to [Design a feature and conduct a Design Review](https://neoito-hub.github.io/code-with-engineering-playbook/design/design-reviews/)
### Day 5
Conduct a Sprint Demo

[Conduct a Retrospective](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/core-expectations/)

Determine required participants, how to capture input (tools) and outcome

Set a timeline, and discuss facilitation, meeting structure etc.

[Refine the Backlog](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/backlog-management/readme/)

Determine required participants

Update the [Definition of Ready](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/advanced-topics/team-agreements/definition-of-ready/)

Update estimates, and the [Estimation](https://neoito-hub.github.io/code-with-engineering-playbook/agile-development/core-expectations/) document

[Submit Engineering Feedback for issues encountered](https://neoito-hub.github.io/code-with-engineering-playbook/engineering-feedback/)
