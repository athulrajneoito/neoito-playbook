# Backlog Management 

This section has links directing you to best practices for managing Product and Sprint backlogs. After reading through the best practices you should have a basic understanding for managing both product and sprint backlogs, how to create acceptance criteria for user stories, creating a definition of done and definition of ready for user stories and the basics around estimating user stories.



- [Product Backlog](https://scrumguides.org/scrum-guide.html#product-backlog)
- [Sprint Backlog](https://scrumguides.org/scrum-guide.html#sprint-backlog)
- [Acceptance Criteria](acceptance-criteria/README.md)
- [Definition of Done](https://scrumguides.org/scrum-guide.html#increment)
- [Definition of Ready](https://www.scrum.org/resources/blog/walking-through-definition-ready)
- [Estimation Basics in Agile](https://www.scrum.org/resources/blog/what-scrum-says-about-estimates)



# *External Feedback*
Various stakeholders can provide feedback to the working product during a project, beyond any formal review and feedback sessions required by the organization. The frequency and method of collecting feedback through reviews varies depending on the case, but a couple of good practices are:

- Capture each review in the backlog as a separate user story.
- Standardize the tasks that implement this user story.
- Plan for a review user story per Epic / Feature in your backlog proactively.
# Minimalism Slices
## Always deliver your work using minimal valuable slices
- Split your work item into small chunks that are contributed in incremental commits.
- Contribute your chunks frequently. Follow an iterative approach by regularly providing updates and changes to the team. This allows for instant feedback and early issue discovery and ensures you are developing in the right direction, both technically and functionally.
- Do NOT work independently on your task without providing any updates to your team.
### Example
Imagine you are working on adding UWP (Universal Windows Platform) application building functionality for existing continuous integration service which already has Android/iOS support.
#### **Bad approach**
After six weeks of work you created PR with all required functionality, including portal UI (build settings), backend REST API (UWP build functionality), telemetry, unit and integration tests, etc.
#### **Good approach**
You divided your feature into smaller user stories (which in turn were divided into multiple tasks) and started working on them one by one:

- As a user I can successfully build UWP apps using current service
- As a user I can see telemetry when building the apps
- As a user I have the ability to select build configuration (debug, release)
- As a user I have the ability to select target platform (arm, x86, x64)
- ...

You also divided your stories into smaller tasks and sent PRs based on those tasks. E.g. you have the following tasks for the first user story above:

- Enable UWP platform on backend
- Add build button to the UI (build first solution file found)
- Add select solution file dropdown to the UI
- Implement unit tests
- Implement integration tests to verify build succeeded
- Update documentation
