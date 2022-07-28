
IV) QA Phase (to run in parallel to the Dev phase)

**12.5 Test Plan (QA)**

Estimated Time - 2 Hours 

- A detailed document that outlines the test strategy, objectives, schedule, estimation, deliverables, and resources needed to undertake software product testing for that particular sprint.
- Test planning is done right after sprint kickoff.
- The test plan document consists of the following: 
  - in-scope items (including test environments and test devices)
  - out-of-scope items and 
  - Entry-exit criteria: Entry and exit criteria are the requirements which must be met before and after a specific process.
- This test plan document is to be approved by the PM before starting test cases



|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Test Plan|QA|User stories added to the current sprint|Approved test plan|Sprint kickoff|PM|<p>Test plan document</p><p></p>|
*ISO Document  at stage 12.5* 

1. Test plan document - QA

**12.6 Test Case Design, Creation and Approval (QA, BA)**

Estimated Time - 25 Hours for a sprint

- Creates test cases by analyzing the requirements.
- Identification of smoke, regression and negative scenarios.
- Detailed test cases and test scenarios are prepared for both functionality and user experience aspects for the user stories included in the current sprint.
- The test case document has to be reviewed and approved by the BA in conformation with the edge cases and test case coverage.



|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Test case design, creation and Approval|QA, BA|User stories added to the current sprint, Test plan document|BA approved test case document|Sprint kickoff|PM, BA|<p>Test case document </p><p></p>|
*ISO Document  at stage 12.6* 

Test Case document - QA

**12.7 Unit Testing using QA Test Cases (Dev)**
**
`	`Estimated Time - 4 Hours

- The PM shares the approved test cases with the dev team before the completion of dev.
- Each developer unit tests his/her own output using the approved test cases.
- The developer clears any issues found during unit tests and submits PR. 


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Unit Testing|Dev|Approved unit test cases|PR after Unit Test|Completion of development task|NA|<p>NA</p><p></p>|
*ISO Document  at stage 12.7 (Not identified)*

**12.8 Deployment to QA env** 

- The TL merges the pull requests after review
- The latest updates will be pushed to the QA env and TL confirms the same with the team.


**Environment: QA**

**12.9 Smoke Test (QA)**

Estimated Time - 30 Minutes

- QA performs smoke tests on the deployed updates and determines whether or not the deployed build is stable. 
- If any blocker issues are caught in smoke testing, the dev team will be informed after bug creation in the PM tool.
- The dev team fixes the blocker issues on priority and submits PR 
- TL deploys the PR to the QA server once again for bug retest.
- The QA performs a smoke test to ensure the update is stable.


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Smoke test|QA, TL, Dev|Deployment to QA|Updates ready for functional testing|Unit testing|PM|<p>NA</p><p></p>|

**12.10 Functional Test (QA)** 

Estimated Time -  24 Hours

- QA tests the basic functionality, negative cases and edge cases of the build thoroughly. 
- Bugs are raised in the PM tool in the following format:
  - Description of bug
  - Criticality
  - Steps to Reproduce
  - Actual Result
  - Expected Result
- The TL will assign bugs to the corresponding developer based on the priority. If the TL is unsure, he/she can confirm the priority with the PM.
- The developer will fix the bug and submit PR after their unit test.
- TL deploys the PR to the QA server once again for bug retest.


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Functional Test|QA, TL, PM|Deployment to QA|Bug report|Smoke test passed|PM|<p>Test Case and result</p><p></p>|
*ISO Document  at stage 12.10*

- Test case and results

**12.11 Integration Testing** (QA, TL, PM)

Estimated Time 8 Hours

- The QA tests whether the updated components and system interfaces work together. 
- Bugs are raised in the PM tool in the following format:
  - Description of bug
  - Criticality 
  - Steps to Reproduce
  - Actual Result
  - Expected Result
- The TL will assign bugs to the corresponding developer based on the priority. If the TL is unsure, he/she can confirm the priority with the PM.
- The developer will fix the bug and submit PR after the unit test.
- TL deploys the PR to the QA server once again for bug retest.
- Integration and functional testing run in parallel.


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Integration Test|QA, TL, PM|Deployment to QA|Bug report|Smoke test passed|NA|<p>Test Case and result</p><p></p>|
*ISO Document  at stage 12.11*

- Test case and results

**12.12 Regression Testing** (QA, BA, TL, PM)

Estimated Time 8 Hours

- The QA tests to ensure that a recent update hasn't harmed existing functionality and is working properly. 
- Regression tests are done based on the regression suite created by the QA and BA. 
- Bugs are raised in the PM tool in the following format:
  - Description of bug
  - Criticality
  - Steps to Reproduce
  - Actual Result
  - Expected Result
- The TL will assign bugs to the corresponding developer based on the priority. If the TL is unsure, he/she can confirm the priority with the PM.
- The developer will fix the bug and submit PR after the unit test.
- TL deploys the PR to the QA server once again for bug retest.




|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Regression Test|QA, BA, TL, PM|Deployment to QA|Bug report |Functional/Integration tests passed|PM|<p>Test Case and result</p><p></p>|
*ISO Document  at stage 12.12*

- Test case and results

**12.13 Bug Retesting and Sign off** (QA, Dev, PM)

- The QA retests the bug tickets which are redeployed after bug fixes. 
- The QA conducts integration testing along with a retest if needed based on the bug.
- If bugs are found in this stage, the cycle of bug creation, bug fixes, QA deployments and retests repeat. 
- Once all bugs as per priority are found to be cleared, the QA signs off to the PM for staging deployment.



|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Bug retesting and sign off to UAT|QA, Dev, PM|Bug Fixes|QA Sign off for staging deployment|Smoke, functional, integration, regression tests|QA, PM|<p>Test Case and result</p><p></p>|
*ISO Document  at stage 12.13*

- Test case and results

**12.14 Internal Demo** (QA, PM, Dev, BA)

- QA performs the demo of the features completed in the current sprint to PM and BA along with the Dev team.
- If any bugs are discovered during the demo they shall be fixed in the QA environment and submitted for retest.
- Multiple internal demos could be conducted during a sprint as per the discretion of the PM.



|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Internal Demo|QA, PM, Dev, BA|User stories completed in the current sprint|Approval for staging deployment|User stories completed in the current sprint|` `PM|<p>??</p><p></p>|
*ISO Document  at stage 12.14*

- ??

**Environment: Staging/UAT**

**12.14 Staging Deployment & Testing** (QA, Dev, PM, BA, Architect (critical bug))

Estimated Time 8 Hours (If Applicable to the project)

- Staging environment is a replication of the production environment. 
- The updates signed off by the QA in the QA env are deployed to the staging server by the TL.
- On completion of staging deployment, the TL notifies the same to the QA and the PM.
- In this environment, functional, integration, and regression tests are performed. 
- If bugs are found in this stage:
  - Criticality: Low to High - the cycle of bug creation, bug fixes in dev env, followed by QA deployment and retests repeat.
  - Criticality (Blocker issue) Highest - the bug has to be fixed in the staging environment with the approval of the PM and architect. This is retested in the same environment by the QA.
- Once the QA confirms that the staging is stable, the BA runs a UAT in the staging environment.


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Staging Deployment|QA, Dev, PM, BA|Updates deployed in staging server|Staging environment ready for UAT|Sign off from QA env|QA, PM, Architect (critical bug)|<p>Test Case and result</p><p></p>|
*ISO Document  at stage 12.14*

- Test case and results


**12.15 Backlog Refinement for next sprint** 

Please follow steps as in Section **11.1** **Product Backlog Refinement**


**12.16 UI Designs for next sprint**

Please follow steps as in Section **11.2** **UI Designs for first sprint**


**12.17 UAT** (QA, PM, BA, Client)

- User Acceptance Testing has to be performed by the QA, BA, PM and the client in the staging environment. 
- Issues found follow the cycle of bug creation, bug fixes in dev env, followed by QA deployment and retests repeat. 
  - Retests of the bugs found in this stage have to be signed-off by only the QA.
- Once the QA confirms that the staging has passed UAT, the PM is notified and he/she informs the client that the updates are ready for client UAT.
- The client performs UAT and one of the following happens:
  - The client raises an issue which is a change request
    - The BA confirms with the client that the issue is a change request and schedules the request for future iterations.
    - The same will be updated as a product backlog item for future sprint.
  - The client raises an issue which is a bug or missed requirement-
    - The BA negotiates with the client to confirm the criticality of the issue. 
    - Critical issues: need to be addressed at the earliest and redeployed for client confirmation. 
    - Non-critical issues can be addressed in a future sprint with the confirmation of the client. The cycle of bug creation, bug fixes in dev env, followed by QA deployment and retests repeat.
  - UAT Passed- The client signs off for production release after they perform UAT.


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|UAT|QA, PM, BA, Client|QA sign off for UAT|Client Sign off for production release|Stable updates in staging server|Client|<p>Test Case and result, Change request document (if applicable), Decision analysis and resolution (if applicable)</p><p></p>|


*ISO Document  at stage 12.17*

1. Test case and results
1. Change request document (if applicable)
1. Decision analysis and resolution (if applicable)

**12.18 Production Deployment/Release**(PM, TL, QA)

- PM approves for production deployment.
- TL completes the production deployment from the staging server and notifies the team.
- TL creates a pre-production snapshot of the latest production server.
- QA runs a smoke test in the production server
  - Smoke test fails: Issue will be fixed in staging server, retested and redeployed to production, followed by a retest in production.
  - Smoke test passes: QA confirms the production server as stable.
- PM confirms the release with the client.
- Ideally, this marks the completion of a sprint.


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Production release|PM, TL, QA, Client|Client release for production release|App updated in production server ready for live users|Updates are stable in staging server|Client|<p>Test Case and result, Release notes, Status report</p><p></p>|
*ISO Document  at stage 12.18*

1. Test case result
1. Release notes
1. Status report

**13. Post-Production Support** 

- Client raises a critical production issue to the PM.
- PM, BA and TL gauge the criticality and impact of the issue.
- The issue could be categorized into either of the following:
  - Feature bug
    - BA negotiates with the client on the criticality of the bug.
    - Top priority issues will be reproduced by the team, fixed in dev env, tested, deployed in staging env retested and then deployed to production.
    - Non-critical issues could be added to the backlog as a future update with the confirmation of the client.
  - Technical, Deployment or high impact issue
    - Dev team fixes the issues in production 
    - TL creates an incident report and submits it to the PM and architect.
    - The PM confirms with the client that the issue is fixed and submits the incident report to the client and the delivery head.

|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Post Production Support|Client, PM, BA, QA, Dev,TL, Architect|Production issue|Stable product in the live environment or updated product backlog|NA|Client|<p>Change request, Incident report, Release notes?, CAPA</p><p></p>|
*ISO Document  at stage 12.13*

1. Change request
1. Incident report
1. Corrective and Preventive Action
1. Release notes?


**14. Project Closure**

\*\*to be completed\*\*

PS: 	

\*this doc will be supported by a detailed flowchart

**15. Deployment Management**

- The goal of deployment management is to get feature updates into live environments. It may also be involved in deploying components to test or staging environments.
- The following table shows the different environment switchings, with the requirements to be met for it, along with the approving authorities.


|**Environments**|**Requirements**|**Approving Authority**|
| :- | :- | :- |
|Dev - QA|Passed Unit testing |PM/BA|
|QA - Staging|Passed smoke, functional, integration and regression tests|QA Lead|
|Staging - Production|Passed UAT/Client Demo|Client|
