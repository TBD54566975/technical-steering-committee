# 2024-07-05

## Agenda

- Assign roles
- Announcements
  - Highlight any upcoming milestones that need our attention
- Agree on agenda
- tbDEX Spec Conformance (_Frank_)
  - **Goal**: Drive awareness of proposed efforts
  - **Proposal**: Complete audit of tbDEX spec conformance and create remediation plan
- Web5 Spec Conformance (_Frank_)
  - **Goal**: Drive awareness of proposed efforts
  - **Proposal**: Complete audit of Web5 spec conformance and create remediation plan
- Call for clarifications

## Attendance

TSC: Frank, Gabe, Henry, Neal, Leo, Kirah, Kendall

Observers: None

## Notes

- Assign roles
  - Facilitator: Frank Hinek
  - Note taker: Leo Ribeiro
- Announcements
- tbDEX Spec / Web5 Conformance
  - There's an increased challenge to keep our specs and test vectors up to date
  - Jiyoon raised in the PFI side are going to be primarily focused on go
  - We agreed on opening up issues in all the repos when we have a change
  - We need to make sure to open issues if we dont have tests for something
  - Tests must be automated in CI, instead of pulling everything locally
    - Leo and Neal to design the solution here
    - Suggestion: prioritize tbdex and works backwards
    - Specially with kotlin and go, the client sdks in these two languages must be aligned
    - Gabe can work in web5 in parallel
- Rust Core
  - Lots of progress, we are at the point where rust sdk are ready for web5, we have kotlin bindings tested with happy path tests
  - We have various integrations, we have happy path tests for PFI
  - We have comprehensive integration but there are tons of corners to fine tune to make it better, also bugs to work through
  - tldr: the core functionality there, POC is made
  - Different targets too: macos, ubuntu, alpine etc.
  - We are trying to automate the build systems
  - We have targeted kotlin as the first language, swift is our next one in the queue, but maybe we should switch to go
  - With javascript/typescript it will be a very different thing with wasm bindings etc
  - Biggest discussion now: How do we have a good transitioning plan to move current state to use rust? What is going to be the effort, are we going to achieve the proper deadlines timeline?
- Clarifications
  - Frank and Gabe to review the issues that need to be created for both specs and sdks
  - Leo and Neal to help with the test suite automation design, along with needed SDKs leads
  - On the CashApp implementation:
    - Its like a hosted wallet, on cloud
    - Rather than have the client polling, webhooks are the way to go
