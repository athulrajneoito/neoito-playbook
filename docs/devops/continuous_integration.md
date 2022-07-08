We encourage engineering teams to make an upfront investment during Sprint 0 of a project to establish an automated and repeatable pipeline which continuously integrates code and releases system executable(s) to target cloud environments. Each integration should be verified by an automated build process to surface any errors across the developer team.

We encourage teams to implement the CI/CD pipelines before any service code is written for customers, which usually happens in Sprint 0(N). This way, the engineering team can develop and test their work in isolation without impacting other developers and promote a consistent devops workflow throughout the engagement.

**Continuous Integration(CI)** is the engineering practice of frequently committing code in a shared repository, ideally several times a day, and performing an automated build on it. These changes are built with other simultaneous changes to the system, which enables early detection of integration issues between multiple developers working on a project. Build breaks due to integration failures are treated as the highest priority issue for all the developers on a team and generally work stops until they are fixed.
This approach leads to significantly reduced integration problems and allows a team to develop cohesive software more rapidly.


## Goals
* Continuous integration automation is an integral part of the software development lifecycle intended to reduce build integration errors and maximize velocity across a dev crew.

* A robust build automation pipeline will:

* Accelerate team velocity
* Prevent integration problems
* Avoid last minute chaos during release dates
* Provide a quick feedback cycle for system-wide impact of local changes
* Separate build and deployment stages
* Measure and report metrics around build failures / success(s)
* Increase visibility across the team enabling tighter communication
* Reduce human errors, which is probably the most important part of automating the builds


## Continuous integration tools

### Source control version management

Probably the most important foundational pillar of continuous integration is source control version management. It is used to communicate and resolve editing conflicts between multiple developers working in the same codebase. Source control version management comes in a variety of tools, the most popular being Git and Subversion. Fot most of our projects, we use GitHub and GitLab as the source control version management tool.

### Static Code Analysis
Static code analysis tools find code defects by examining the code without executing the program. As such, static code analysis has become an essential part of CI because:   

1. It is very efficient in identifying hundreds of types of defects such as concurrency, data flow, dynamic memory, and numerical defects.
2. It finds defects early in the development cycle, that is, as soon as code is written or modified.
3. It verifies compliance with coding standards such as MISRA C®, MISRA C++, JSF++, and custom naming conventions.
4. It finds security vulnerabilities and checks for adherence with security standards such as CERT® C, CERT C++, ISO 17961, and MISRA C:2012 Amendment 1.
5. By using formal methods, it can prove the absence of overflow, divide-by-zero, out-of-bounds array access, and other run-time errors.

SonarQube, Codacy etc are examples of Static Code Analysis tools.

### Automated testing
Most serious software projects include an additional code base that is not explicitly responsible for the business product and features. This secondary code base is a test suite and acts as a set of assertions that assures the primary code base is working correctly without bugs.  During development, these tests are run by developers to validate that new code has not caused any regression on existing features. These test cases can also be run by extraneous tools to automate this validation process. CI service products will automatically run the test cases for a project on user-specified events. Generally, when a developer pushes code using the version control system an event will trigger the full test suite to run automatically.


