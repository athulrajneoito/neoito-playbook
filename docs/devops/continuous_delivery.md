**Continuous Delivery(CD)** takes the Continuous Integration concept further to also test deployments of the integrated code base on a replica of the environment it will be ultimately deployed on. This enables us to learn early about any unforeseen operational issues that arise from our changes as quickly as possible and also learn about gaps in our test coverage.


Continuous Delivery is a small build cycle with short sprints, where the aim is to keep the code in a deployable state at any given time. This does not mean the code or project is 100% complete, but the feature sets that are available are vetted, tested, debugged and ready to deploy, although you may not deploy at that moment.

The focus and key here is to keep the code base at a deployable state. This is the standard everyday project that goes out to the public or is consumer facing. In today’s world, you cannot afford to release a bug-riddled project, so smaller sprints allow for quicker turn times to identify bugs and therefore quicker time in fixing those bugs, creating a much more stable code base early on. This is our preferred method of working.


## General Guidance
### Define a Release Strategy
It's important to establish a common understanding between the Dev Lead and application stakeholder(s) around the release strategy / design during the planning phase of a project. This common understanding includes the deployment and maintenance of the application throughout its SDLC.


### Release Strategy Principles

* Parties in charge of deployments to each environment, as well as in charge of the release.
* An asset and configuration management strategy.
* An enumeration of the environments available for acceptance, capacity, integration, and user acceptance testing, and the process by which builds will be moved through these environments.
* A description of the processes to be followed for deployment into testing and production environments, such as change requests to be opened and approvals that need to be granted.
* A discussion of the method by which the application’s deploy-time and runtime configuration will be managed, and how this relates to the automated deployment process.
* Description of the integration with any external systems. At what stage and how are they tested as part of a release? How does the technical operator communicate with the provider in the event of a problem?
* A disaster recovery plan so that the application’s state can be recovered following a disaster. Which steps will need to be in place to restart or redeploy the application should it fail.
* Production sizing and capacity planning: How much data will your live application create? How many log files or databases will you need? How much bandwidth and disk space will you need? What latency are clients expecting?
* How the initial deployment to production works.
* How fixing defects and applying patches to the production environment will be handled.
* How upgrades to the production environment will be handled, including data migration. How will upgrades be carried out to the application without destroying its state.


### Application Release and Environment Promotion
Your release manifestation process should take the deployable build artifact created from your commit stage and deploy them across all cloud environments, starting with your test environment.

The test environment (often called Integration) acts as a gate to validate if your test suite completes successfully for all release candidates. This validation should always begin in a test environment while inspecting the deployed release integrated from the feature / release branch containing your code changes.


### Modeling your Release Pipeline
It's critical to model your test and release process to establish a common understanding between the application engineers and customer stakeholders. Specifically aligning expectations for how many cloud environments need to be pre-provisioned as well as defining sign-off gate roles and responsibilities.

![Screenshot](../img/example_release_flow.png)

## The First Deployment

The very first deployment of any application should be showcased to the customer in a production-like environment (UAT) to solicit feedback early. The UAT environment is used to obtain product owner sign-off acceptance to ultimately promote the release to production.

Criteria for a production-like environment

* Runs the same operating system as production.
* Has the same software installed as production.
* Is sized and configured the same way as production.
* Mirrors production's networking topology.
* Simulated production-like load tests are executed following a release to surface any latency or throughput degradation.


## Blue-Green Deployments

Blue/green deployments provide releases with near zero-downtime and rollback capabilities by running two identical instances of a production environment called Blue and Green.
Only one of these environments accepts live production traffic at a given time.


<p align="center">
  <img src="../img/bg3-1.jpg" alt="Screenshot"/>
</p>
 
Blue and green take turns to play the role of production. Only one of the environments is live at any given time. Say, for instance, that blue is active. In that case, it receives all the production traffic. Meanwhile, green acts as a staging area, where we can deploy and test the next version that needs to go live.

Migrating users to the new application version is as simple as changing the router configuration to direct all traffic to the Blue environment.

This technique **simplifies rollback scenarios** as we can simply switch the router back to Green.
This ability to simply roll traffic back to the operational environment is a key benefit of blue/green deployments. You can roll back to the blue environment at any time during the deployment process. Impaired operation or downtime is minimized because impact is limited to the window of time between green environment issue detection and shift of traffic back to the blue environment. Additionally, impact is limited to the portion of traffic going to the green environment, not all traffic. If the blast radius of deployment errors is reduced, so is the overall deployment risk.