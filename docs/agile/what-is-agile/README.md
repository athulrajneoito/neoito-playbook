#**What is Agile Development?**

Agile development is a term used to describe iterative software development. Iterative software development shortens the DevOps lifecycle by executing against work in smaller increments, usually called ***sprints***. Sprints are typically 1-4 weeks long. Agile development is often contrasted with traditional or waterfall development, where larger projects are planned upfront and executed against that plan.

Delivering production quality code every sprint requires the Agile development team to account for the accelerated pace. All coding, testing, and quality verification must be done each and every sprint. Unless a team is properly set up, the results can fall short of expectations. While these disappointments offer great learning opportunities, wouldn't it be better to learn some key lessons before getting started?

Here is some key success factors for Agile development teams:

- Diligent backlog refinement
- Integrate early and often
- Minimize technical debt

## **→ Diligent backlog refinement**
An Agile development team works off of a backlog of requirements, often called *user stories*. The backlog is prioritized so the most important user stories are at the top. The product owner owns the backlog and adds, changes, and reprioritizes user stories based on the customer's needs.

One of the biggest drags on an Agile team's productivity is a poorly defined backlog. A team cannot be expected to consistently deliver high-quality software each sprint unless they have clearly defined requirements.

The product owner's job is to ensure that in every sprint, the engineers have clearly defined user stories to work with. The user stories at the top of the backlog should always be ready for the team to execute. This is called backlog refinement. Keeping a backlog ready for an Agile development team requires effort and discipline. Fortunately, it's well worth the investment.

When refining the backlog, there are some key considerations to remember.

1. Refining user stories is often a long-lead activity. Elegant user interfaces, beautiful screen designs, and customer delighting solutions all take time and energy to create. Diligent product owners refine user stories 2-3 sprints in advance. They account for design iterations and customer reviews. They work to ensure every user story is something the Agile team is proud to deliver to the customer.
1. A user story is not refined unless the team says it is. The team needs to review the user story and agree it's ready to work on. If a team has not seen the user story until day 1 of a sprint, that's a big red flag.
1. User stories further down the backlog can remain ambiguous. Don't waste time refining lower priority items. Stay intently focused on the top of the backlog.

## **→Integrate early and often**
Continuous Integration and continuous delivery (CI/CD) sets your team up for the fast pace of Agile development. As soon as possible, automate the build, test, and deployment pipelines. This should be one of the first things a team sets up when starting a new project.

With automation, the team will avoid slow, error-prone, and time-intensive manual deployment processes. Since teams release every sprint, there just isn't time to do this manually.

CI/CD also influences your software architecture. It ensures you deliver buildable and deployable software. When implementing a difficult-to-deploy feature, teams become aware immediately as the build and deployments fail. CI/CD forces a team to fix deployment issues as they occur, ensuring the product is always ready to ship.

There are some key CI/CD activities that are critically important to effective Agile development.

1. **Unit testing**. Unit tests are the first defense against human error. Unit tests should be considered part of coding and checked in with the code. Executing unit tests should be part of every build. Failed unit tests mean a failed build.
1. **Build automation**. The build system should automatically pull code and tests directly from source control when builds execute.
1. **Branch and build policies**. Configure branches and build policies to build automatically as the team checks code into a specific branch.
1. **Deploy to an environment**. Set up a release pipeline that automatically deploys built projects to an environment that mimics production.
## **→Minimize technical debt**
With personal finances, it's easier to stay out of debt than to dig out from under it. The same rule applies to technical debt. Technical debt includes anything the team must do to deploy production-quality code and keep it running in production. Examples are bugs, performance issues, operational issues, accessibility, and others.

Keeping on top of technical debt requires courage. There are many pressures to delay fixing bugs. It feels good to work on features and ignore debt. Unfortunately, somebody must pay the technical debt sooner or later. Just like financial debt, technical debt becomes harder to pay off the longer it exists. A smart product owner works with their team to ensure there is time to pay off technical debt every sprint. Balancing technical debt reduction with feature development is a difficult task. Fortunately, there are some straightforward techniques for creating productive, customer-focused teams.
