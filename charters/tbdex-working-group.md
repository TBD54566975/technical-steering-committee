# tbDEX Working Group Charter

**Start Date**: June 10, 2024

**End Date**: December 31, 2024

**DRI**: [Moe Jangda](https://github.com/mistermoe), [Jiyoon Koo](https://github.com/jiyoontbd)

## Motivation and Background

tbDEX is an open-source protocol that can be used to move value between N parties. It relies on Web5 primitives such as Decentralized Identifiers and Verifiable Credentials to enable secure, decentralized value exchanges without intermediaries.

This working group serves as a gathering place to discuss and improve the existing protocol and the resulting implementation(s), which will provide developers with the tools they need to build Participating Financial Institutions (PFIs) and Wallets that "speak" spec-conformant tbDEX.

## Scope

* Discussing, defining and implementing the tbDEX protocol specification that will best suit the needs of those who are using it in the real world
* Discussing how updates to Web5 libraries impact tbDEX implementation, and coming up with ways to adjust the tbDEX API as needed, or influence Web5 API surfaces, if necessary
* Discussing, defining and implementing transport specifications to send and receive tbDEX messages

## Deliverables

### 1. tbDEX Protocol Specification
Description: Develop and maintain the [tbDEX Protocol Specification](https://github.com/TBD54566975/tbdex/tree/main/specs/protocol)

#### Scope of Work:
- Specification outlining types of messages and common traits in messages (structure, signature generation etc.) used by PFIs and Wallets to interact with each other to exchange value
- Test vectors to achieve conformance across N implementations, if needed
- Incorporate interoperability components that currently lives in [tbDEX Interop Profile Specification](https://github.com/TBD54566975/tbdex/tree/main/specs/interop) into the protocol specificiation

### 2. tbDEX HTTP API Specification
Description: Develop and maintain the [tbDEX HTTP API Specification](https://github.com/TBD54566975/tbdex/tree/main/specs/http-api)

#### Scope of Work:
- Develop and maintain the [tbDEX HTTP API Specification](https://github.com/TBD54566975/tbdex/tree/main/specs/http-api) outlining how to use various transports to send and receive tbDEX messages

### 3. tbDEX SDKs
Description: Develop and maintain SDK implementations that conform to the tbDEX protocol and transport specifications

#### Scope of Work:
- SDKs in [Typescript](https://github.com/TBD54566975/tbdex-js), [Kotlin](https://github.com/TBD54566975/tbdex-kt), [Swift](https://github.com/TBD54566975/tbdex-swift), [Dart](https://github.com/TBD54566975/tbdex-dart), [Go](https://github.com/TBD54566975/tbdex-go), and [Rust](https://github.com/TBD54566975/tbdex-rs)

- SDKs shall demonstrate conformance to the test vectors defined by the tbDEX protocol and transport(s) specifications

- SDKs shall be well-documented according to each language's conventions, as well as being surfaced through the [developer site](https://developer.tbd.website/docs/)

- SDKs shall follow the guidance of the Rust Working Group in adopting a Rust core to limit developer overhead
  
## Success Criteria

### 1. tbDEX Protocol Specification
- A published versioned specification
- Test vectors to be consumed across multiple tbDEX SDK implementations

### 2. tbDEX HTTP API Specification
- A published versioned specification

### 3. tbDEX SDKs
- Across the aforementioned languages, feature completeness in accordance with the latest version of the tbDEX protocol and transport(s) specification's feature set and API
- Demonstrated interoperability via the tbDEX specifications' test suites

### Other goals
- Implement versioning process for each specification (ideally it's the same process across all specifications)
- Incorporate interoperability components that currently lives in [tbDEX Interop Profile Specification](https://github.com/TBD54566975/tbdex/tree/main/specs/interop) into the [tbDEX Protocol Specificiation](https://github.com/TBD54566975/tbdex/tree/main/specs/protocol)

## Coordination
This group favors document-driven coordination, documenting communications and decisions. The group will be facilitated via the Technical Steering Comittee and the set of repositories specific to each of the work items and deliverables listed above, making use of GitHub Issues and a common GitHub project for the entire Working Group's corpus.

The Working Group will closely collaborate with the Web5 Working Group to ensure alignment and support for the tbDEX protocol and requirements. Similarly, the Working Group will coordinate closely with the Rust Working Group for the uptake of a Rust Core throughout the tbDEX SDKs. Coordination will surface through the TSC, associated GitHub repositories, and communication tools (Slack, Discord).

## Communication
The working group will communicate primarily in a written manner via GitHub: filing issues and Requests for Comments (RFCs) directly to the respective GitHub repository, primarily within the [tbDEX GitHub repository](https://github.com/TBD54566975/tbdex).

The group will establish dedicated public and private communication channels as necessary (e.g., TBD Slack, TBD Discord) for real-time discussions and quick resolution of issues.

The Working Group DRI will coordinate weekly updates for each of the group's work items, with the respective DRIs of each work item, to share with the TSC.

## Decision making
DRIs of the working group are responsible for facilitating discussions to come to a consensus when possible. When consensus cannot be reached, the working group DRIs are responsible for making a decision.