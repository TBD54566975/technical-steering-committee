# 2024-07-05

## Agenda

- Assign roles
- Announcements
  - Highlight any upcoming milestones that need our attention
- Agree on agenda
- tbDEX / Web5 Spec Conformance (_Frank_)
  - **Goal**: Drive awareness of proposed efforts
  - **Proposal**: Complete audit of tbDEX spec conformance and create remediation plan
- Rust Core Update (_Kendall_)
  - **Goal**: Drive awareness of progress and updates on Rust Core WG efforts
- Call for clarifications

## Attendance

TSC: Frank, Gabe, Henry, Neal, Leo, Kirah, Kendall

Observers: None

## Notes

- Assign roles
  - Facilitator: Frank Hinek
  - Note taker: Leo Ribeiro
- Announcements
  - Re-iterate TBD PFI readiness by end of month
- tbDEX Spec / Web5 Conformance
  - There's an increased challenge to keep our specs and test vectors up to date
  - Jiyoon raised that the PFI focused team are focused on keeping tbdex-/web5-go updated with spec changes
  - We agreed on opening up issues in all the repos when we have a change
  - We need to make sure to open issues if we dont have tests for something
  - Neal raised that test vectors must be automated in CI, instead individuals pulling down specs and testing each SDK language locally
    - Leo and Neal to design the solution here
    - Suggestion: prioritize tbdex and work backwards
    - Gabe can work on web5 spec vectors in parallel
    - Critical that the Kotlin and Go SDKs are aligned based on upcoming delivery milestones
- Rust Core
  - Lots of progress: web5 and tbDEX Rust SDKs are well underway and Kotlin bindings have been tested with happy path tests
  - Multiple integrations tests have been done with the Rust-backed SDKs and PFIs (PFI exemplar, proto PFI, TBD PFI)
  - We have comprehensive integration but there are tons of corners to fine tune to make it better, also bugs to work through
  - tldr: the core functionality there, POC is in place
  - Target architectures for bindings include: macOS aarch64 (Apple Silicon), macOS x64_64 (Intel mac), Ubuntu Linux amd64, and Alpine Linux amd64
  - Intent is to improve build systems through automation
  - We have targeted kotlin as the first language, Swift is our next one in the queue, but can consider swapping Swift for another lanague
  - JavaScript/TypeScript support will require a different approach using WASM
  - Biggest discussion now: How do we have a good transitioning plan to move current state to use rust? What is going to be the effort,
    are we going to achieve the proper deadlines timeline?
- Clarifications
  - Frank and Gabe to review the issues that need to be created for both specs and sdks
  - Leo and Neal to help with the test suite automation design, along with needed SDK DRIs
