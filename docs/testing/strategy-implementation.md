# Strategy Implementation
### Stage 0: Development (Env)
Responsibility: 100% Dev lead/TL/Architect

Escalation Point: Dev Lead->PM

Dev lead/TL would be completely responsible for all the issues related to the development environment 
### Stage 1: QA (Env) 
Documents: QA Signoff & Test Summary

Responsibility: 100% QA

Escalation point: QA->PM, PM->Dev lead/TL/Architect
### Stage 2: UAT (Env)
Documents: Sign-off by PM.

Responsibility: 80% QA; 20% BA/PM

QA will be solely responsible for identifying all functionality issues as well as UI/UX issues and requirement gaps. 

BA/PM has a shared responsibility in identifying requirement gaps and UI/UX. performance before handing over to the client

Escalation point: PM
### Stage 3: Production (Env)
Responsibility: 15% client, 35% QA, 25% BA, 25%. PM.

If something goes wrong Production

1. Due to requirement gap- shared between client & BA

2. Missed Happy Path scenarios - QA & PM

3. Missed Edge scenarios - QA & BA

4. Environment and deployment - Dev lead, PM

5. Infrastructure – Architect, TL/Dev-lead 

### Stage 4: Post-production
Documents: RCA & Maintenance log for all bugs, Incident report for critical bags.

QA & Dev lead together to provide RCA

PM to provide Incident report & Maintenance log

Responsibility: 50% QA; 25% dev lead,15%. PM; 10% BA

![](images/Aspose.Words.e4d64546-c6d2-46ea-9993-efc42f6dccb5.003.png)
