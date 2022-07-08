## CI/CD Pipeline

A continuous integration and continuous deployment (CI/CD) pipeline is a series of steps that must be performed in order to deliver a new version of software.

There are 5 essential stages in  a CI/CD pipeline irrespective of the tool used for configuring the pipeline :

1. **The trigger** - An automated pipeline is triggered automatically when a code commit is made in the repository.
2. **Code checkout** - Once the pipeline is triggered, the source code is checked out from the source control repository.
3. **Code Quality Analysis** - In this stage, we integrate a static code analyser such as SonarQube in the pipeline, which would check the source code against a set of predefined rules to ensure that the code is not of substandard quality.
4. **Build** - Once the code quality is ensured, the pipeline progresses to the build stage where the source  code is merged with its dependencies to build a runnable instance of the software that can be potentially shipped to the end user. Failure to pass the build stage indicates a major fundamental project misconfiguration which should be addressed immediately.
5. **Deploy** - This is the stage where the final runnable instance is deployed to particular environment. Once this stage is completed, the pipeline has finished execution successfully.


## Github Actions

Github actions is a continuous integration and continuous delivery platform that automates build, test and deploy pipeline. A Github action workflow is configured to be triggered when an event occurs in the repository (Eg. A pull request being created)

![Screenshot](../img/GitHub_Actions.png)

* A **workflow** is a configurable automated process that will run one or more jobs. Workflows are defined by a YAML file checked in to your repository and will run when triggered by an event in your repository, or they can be triggered manually, or at a defined schedule.

<p align="center">
  <img src="../img/Workflow-Designs-Dependent-Workflows.png" alt="Screenshot"/>
</p>

* An **event** is a specific activity in a repository that triggers a workflow run. For example, activity can originate from GitHub when someone creates a pull request, opens an issue, or pushes a commit to a repository. You can also trigger a workflow run on a schedule, by posting to a REST API, or manually.
* A **job** is a set of steps in a workflow that execute on the same runner. Each step is either a shell script that will be executed, or an action that will be run. Steps are executed in order and are dependent on each other. Since each step is executed on the same runner, you can share data from one step to another. For example, you can have a step that builds your application followed by a step that tests the application that was built.
* A **runner** is a server that runs your workflows when they're triggered. Each runner can run a single job at a time. GitHub provides Ubuntu Linux, Microsoft Windows, and macOS runners to run your workflows.
* An **action** is a custom application for the GitHub Actions platform that performs a complex but frequently repeated task. Use an action to help reduce the amount of repetitive code that you write in your workflow files.

## Jenkins

Jenkins is an open source tool with plugin built for continuous integration purpose. The principle functionality of Jenkins is to keep a track of version control system and to initiate and monitor a build system if changes occur.Jenkins is free but requires a dedicated server.

<p align="center">
  <img src="../img/jenkins.png" alt="Screenshot"/>
</p>


* Once the Jenkins server is up and running, pipeline jobs can be created using the Jenkins Web UI. 
* In the job, mention the source control repository URL from which the source code needs to be pulled.
* Next, mention the trigger that would start the pipeline. The most common way is to use web-hooks.Web hooks allow interaction between web-based applications through the use of custom callbacks. We can also use the Poll SCM option. This option does is that it continuously queries the VCS, based on a predefined schedule, for new changes.
* In the next step, write the build commands based on which the artifact should be built.
* Once all the necessary configurations are completed, the pipeline is ready to use for deployments.