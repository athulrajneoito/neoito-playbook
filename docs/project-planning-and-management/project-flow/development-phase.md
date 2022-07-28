
III) Development Phase

**Environment: Dev**

**12.3 Development (Dev team, TL, PM, Solution Architect)**

1) PM to conduct daily scrum meeting and task assignment
   1) The duration of scrum meeting must not exceed 15-20 mins
   1) Each developer updates their status in the format 
- What I did yesterday.
- What I plan to do today.
- Blockers, if any.
  1) Any technical discussions are to be conducted as separate meetings between the concerned parties outside the scrum.
1) Project Monitoring
   1) PM to track the progress of the project daily to avoid blockers and delay
1) Weekly status reports by the PM to the delivery manager and clients (Project status)
1) Developers complete the tasks, complete unit testing using QA test cases (refer 12.7) and raise a pull request (PR).
1) Developers to maintain Tech-spec document


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Development  |PM, Dev, TL|Approved SDD, User stories, UI designs|Pull request after development |Approved SDD, User stories, UI designs|TL/PM|<p>Status Report</p><p></p>|
*ISO Document  at stage 12.3* 

- Status Report

**12.4 Code Review (TL, Dev)**

- The PR submitted by each developer will be reviewed by either the TL or another team member, as decided by the architect.
- Review comments may be added by the reviewer, which then should be corrected and resubmitted by the developer.
- TL/peer team members will approve the PR after verifying the above step. 
- Approved pull requests will be merged and deployed to the QA environment with the confirmation from TL.


|Stage|Participants|Input|Output|Prerequisite|Approving Authority|ISO Documents|
| :- | :- | :- | :- | :- | :- | :- |
|Code Review |Dev, TL|PR Request |Code deployed to QA env|Task completed by the developer as per business requirement|TL|<p>NA</p><p></p>|
*ISO Document  at stage 12.4* (Not identified)


