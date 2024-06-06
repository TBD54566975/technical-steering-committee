# Rust Core Working Group Charter <!-- omit in toc -->

**Start Date**: June 6th 2024

**End Date**: Unknown

**DRI**: Kendall Weihe (@KendallWeihe)

- [Motivation and Background](#motivation-and-background)
- [Scope](#scope)
- [Deliverables](#deliverables)
  - [web5](#web5)
    - [\[Deliverable 1\]: web5 API Design (APID)](#deliverable-1-web5-api-design-apid)
    - [\[Deliverable 2\]: web5 Rust Implementation](#deliverable-2-web5-rust-implementation)
    - [\[Deliverable 3\]: web5 UniFFI Binding](#deliverable-3-web5-uniffi-binding)
    - [\[Deliverable 4\]: web5 Kotlin Implementation](#deliverable-4-web5-kotlin-implementation)
    - [\[Deliverable 5\]: web5 Swift Implementation](#deliverable-5-web5-swift-implementation)
  - [tbdex](#tbdex)
    - [\[Deliverable 6\]: tbdex API Design (APID)](#deliverable-6-tbdex-api-design-apid)
    - [\[Deliverable 7\]: tbdex Rust Implementation](#deliverable-7-tbdex-rust-implementation)
    - [\[Deliverable 8\]: tbdex UniFFI Binding](#deliverable-8-tbdex-uniffi-binding)
    - [\[Deliverable 9\]: tbdex Kotlin Implementation](#deliverable-9-tbdex-kotlin-implementation)
    - [\[Deliverable 10\]: tbdex Swift Implementation](#deliverable-10-tbdex-swift-implementation)
- [Success Criteria](#success-criteria)
- [Coordination](#coordination)
- [Communication](#communication)

## Motivation and Background

This working group will streamline and standardize the implementations of the open standards presented by the web5 and tbdex Working Groups.

![High-Level](./high-level.png)

SDKs for web5 and tbdex have been implemented across TypeScript ([web5-js](https://github.com/TBD54566975/web5-js/) & [tbdex-js](https://github.com/TBD54566975/tbdex-js/)), Kotlin ([web5-kt](https://github.com/TBD54566975/web5-kt/) & [tbdex-kt](https://github.com/TBD54566975/tbdex-kt/)), Swift ([web5-swift](https://github.com/TBD54566975/web5-swift/) & [tbdex-swift](https://github.com/TBD54566975/tbdex-swift/)), Golang ([web5-go](https://github.com/TBD54566975/web5-go/) & [tbdex-go](https://github.com/TBD54566975/tbdex-go/)), and Dart ([web5-dart](https://github.com/TBD54566975/web5-dart/) & [tbdex-dart](https://github.com/TBD54566975/tbdex-dart/)). Streamlining the implementation's for web5 and tbdex by implementing "core" logic in Rust, and then binding the solution into the target language, offers many benefits. The benefits of Rust Core include but are not limited to:

- Strong interoperability assurances.
- Reduce maintenance burden for particularly dense feature sets (ex. did:dht).
- Serve as a Schelling Point for matters of implementation governance.
- Contain a convenient location for a historical record of decisions-made.

Rust is uniquely qualified as the solution for a cross-platform core implementation because of open source tooling availability through WASM and UniFFI. Furthermore, Rust has a broad array of open source support, and Rust has the unique feature of memory safety (relative to alternatives such as C).

## Scope

The comprehensive implementations of the web5 and tbdex specifications across Rust, Kotlin and Swift are within the scope of this Working Group. Alongside of each implementation, documentation comments ("doc comments"), test vectors, example usages, and CI/CD solutions (eg. security analysis, test automation, artifact version & publication, etc.) are all within scope of this Working Group. 

The Rust Core Working Group will make an intentional effort to prioritize matters of security and performance. Furthermore, with regards to API design & developer experience (DX), this Working Group will prioritize first and foremost modularity and extensibility, over DX convenience, in order to limit the liklihood of introducing breaking changes to consumers of the delivered SDKs.

The Rust Core Working Group is not concerned with the definitions of the web5 and tbdex specifications, both of which are the concerns of the respective Working Group. However, the Rust Core Working Group will offer valuable concrete feedback to the web5 and tbdex Working Groups. Although the web5 and tbdex specifications are not within the scope of this Working Group, a considerable amount of cross-Working Group collaboration is to be expected (see [Coordination](#coordination) and [Communication](#communication) below).

The Rust Core Working Group codifies a standard API Design ([web5 APID](#deliverable-1-web5-api-design-apid) & [tbdex APID](#deliverable-6-tbdex-api-design-apid)) which is implemented across all supported language implementations (Rust, Kotlin and Swift), but any additional API features or design characteristics are not within the scope of this Working Group. Each implementation must support the standard API Design as a baseline implementation, but does not exclude the possibility of additional features.

The Rust Core Working Group will codify itself across the following GitHub repos:

- web5: https://github.com/TBD54566975/web5-rs/
  - [[Deliverable 1]: web5 API Design (APID)](#deliverable-1-web5-api-design-apid)
  - [[Deliverable 2]: web5 Rust Implementation](#deliverable-2-web5-rust-implementation)
  - [[Deliverable 3]: web5 UniFFI Binding](#deliverable-3-web5-uniffi-binding)
  - [[Deliverable 4]: web5 Kotlin Implementation](#deliverable-4-web5-kotlin-implementation)
  - [[Deliverable 5]: web5 Swift Implementation](#deliverable-5-web5-swift-implementation)
  - RFCs for historical tracking of significant decisions
- tbdex: https://github.com/TBD54566975/tbdex-rs/
  - [[Deliverable 6]: tbdex API Design (APID)](#deliverable-6-tbdex-api-design-apid)
  - [[Deliverable 7]: tbdex Rust Implementation](#deliverable-7-tbdex-rust-implementation)
  - [[Deliverable 8]: tbdex UniFFI Binding](#deliverable-8-tbdex-uniffi-binding)
  - [[Deliverable 9]: tbdex Kotlin Implementation](#deliverable-9-tbdex-kotlin-implementation)
  - [[Deliverable 10]: tbdex Swift Implementation](#deliverable-10-tbdex-swift-implementation)
  - RFCs for historical tracking of significant decisions

## Deliverables

![Deliverables](./deliverables.png)

### web5

#### [Deliverable 1]: web5 API Design (APID)

**Description**: The *web5 APID* is a language-independent codified API Design which serves to act as a baseline of features for implementations. The APID is primarily considered to be a deliverable for internal usage, but does not exclude the possibility of external consumption.

**DRI**: Kendall Weihe (@KendallWeihe).

**Scope of Work**:

- Custom DSL which is conceptually compatible with all target languages.
- Codification of the API Design using the Custom DSL.
- Example usages.
- Doc comments inline for the API Design .
- Test vector resources.

**Timeline/Milestones**: Unknown???

**Exit Criteria**: Comprehensive feature coverage for the web5 specification, codified in the Custom DSL, committed to source code.

#### [Deliverable 2]: web5 Rust Implementation

**Description**: Rust implementation of the [[Deliverable 1]: web5 API Design (APID)](#deliverable-1-web5-api-design-apid), intended for public consumption.

**DRI**: Kendall Weihe (@KendallWeihe).

**Scope of Work**:

- Full conformance to [[Deliverable 1]: web5 API Design (APID)](#deliverable-1-web5-api-design-apid).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Rust project.

#### [Deliverable 3]: web5 UniFFI Binding

**Description**: Rust crate which utilizes [UniFFI](https://github.com/mozilla/uniffi-rs) in conjunction with the [[Deliverable 2]: web5 Rust Implementation](#deliverable-2-web5-rust-implementation) to create Kotlin and Swift binded code, which feed into [[Deliverable 4]: web5 Kotlin Implementation](#deliverable-4-web5-kotlin-implementation) and [[Deliverable 5]: web5 Swift Implementation](#deliverable-5-web5-swift-implementation). This deliverable is intended primarily for internal purposes but does not exclude the possibility of public consumption.

**DRI**: Kendall Weihe (@KendallWeihe).

**Scope of Work**:

- UDL file with comprehensive feature coverage from [[Deliverable 2]: web5 Rust Implementation](#deliverable-2-web5-rust-implementation).
- Successful binding executions for Kotlin & Swift.

**Timeline/Milestones**: ???

**Exit Criteria**: Successful binding executions, over the comprehensive set of features from [[Deliverable 2]: web5 Rust Implementation](#deliverable-2-web5-rust-implementation), for Kotlin and Swift.

#### [Deliverable 4]: web5 Kotlin Implementation

**Description**: Kotlin implementation of web5 by wrapping [[Deliverable 3]: web5 UniFFI Binding](#deliverable-3-web5-uniffi-binding) as to be conformant to the [[Deliverable 1]: web5 API Design (APID)](#deliverable-1-web5-api-design-apid), intended for public consumption.

**DRI**: Neal Roessler (@nitro-neal).

**Scope of Work**:

- Utilization of the output of the [[Deliverable 3]: web5 UniFFI Binding](#deliverable-3-web5-uniffi-binding).
- Full conformance to [[Deliverable 1]: web5 API Design (APID)](#deliverable-1-web5-api-design-apid).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Kotlin project.

#### [Deliverable 5]: web5 Swift Implementation

**Description**: Swift implementation of web5 by wrapping [[Deliverable 3]: web5 UniFFI Binding](#deliverable-3-web5-uniffi-binding) as to be conformant to the [[Deliverable 1]: web5 API Design (APID)](#deliverable-1-web5-api-design-apid), intended for public consumption.

**DRI**: Kirah Sapong (@kirahsapong).

**Scope of Work**:

- Utilization of the output of the [[Deliverable 3]: web5 UniFFI Binding](#deliverable-3-web5-uniffi-binding).
- Full conformance to [[Deliverable 1]: web5 API Design (APID)](#deliverable-1-web5-api-design-apid).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Swift project.

### tbdex

#### [Deliverable 6]: tbdex API Design (APID)

**Description**: The *tbdex APID* is a language-independent codified API Design which serves to act as a baseline of features for implementations. The APID is primarily considered to be a deliverable for internal usage, but does not exclude the possibility of external consumption.

**DRI**: Kendall Weihe (@KendallWeihe)

**Scope of Work**:

- Custom DSL which is conceptually compatible with all target languages.
- Codification of the API Design using the Custom DSL.
- Example usages.
- Doc comments inline for the API Design.
- Test vector resources.

**Timeline/Milestones**: Unknown???

**Exit Criteria**: Comprehensive feature coverage for the tbdex specification, codified in the Custom DSL, committed to source code.

#### [Deliverable 7]: tbdex Rust Implementation

**Description**: Rust implementation of the [[Deliverable 6]: tbdex API Design (APID)](#deliverable-6-tbdex-api-design-apid), intended for public consumption.

**DRI**: Diane Huxley (@diehuxx).

**Scope of Work**:

- Full conformance to [[Deliverable 6]: tbdex API Design (APID)](#deliverable-6-tbdex-api-design-apid).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Rust project.

#### [Deliverable 8]: tbdex UniFFI Binding

**Description**: Rust crate which utilizes [UniFFI](https://github.com/mozilla/uniffi-rs) in conjunction with the [[Deliverable 7]: tbdex Rust Implementation](#deliverable-7-tbdex-rust-implementation) to create Kotlin and Swift binded code, which feed into [[Deliverable 9]: tbdex Kotlin Implementation](#deliverable-9-tbdex-kotlin-implementation) and [[Deliverable 10]: tbdex Swift Implementation](#deliverable-10-tbdex-swift-implementation). This deliverable is intended primarily for internal purposes but does not exclude the possibility of public consumption.

**DRI**: Kendall Weihe (@KendallWeihe).

**Scope of Work**:

- UDL file with comprehensive feature coverage from [[Deliverable 7]: tbdex Rust Implementation](#deliverable-7-tbdex-rust-implementation).
- Successful binding executions for Kotlin & Swift.

**Timeline/Milestones**: ???

**Exit Criteria**: Successful binding executions, over the comprehensive set of features from [[Deliverable 7]: tbdex Rust Implementation](#deliverable-7-tbdex-rust-implementation), for Kotlin and Swift.

#### [Deliverable 9]: tbdex Kotlin Implementation

**Description**: Kotlin implementation of tbdex by wrapping [[Deliverable 8]: tbdex UniFFI Binding](#deliverable-8-tbdex-uniffi-binding) as to be conformant to the [[Deliverable 6]: tbdex API Design (APID)](#deliverable-6-tbdex-api-design-apid), intended for public consumption.

**DRI**: Neal Roessler (@nitro-neal).

**Scope of Work**:

- Utilization of the output of the [[Deliverable 8]: tbdex UniFFI Binding](#deliverable-8-tbdex-uniffi-binding).
- Full conformance to [[Deliverable 6]: tbdex API Design (APID)](#deliverable-6-tbdex-api-design-apid).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Kotlin project.

#### [Deliverable 10]: tbdex Swift Implementation

**Description**: Swift implementation of tbdex by wrapping [[Deliverable 8]: tbdex UniFFI Binding](#deliverable-8-tbdex-uniffi-binding) as to be conformant to the [[Deliverable 6]: tbdex API Design (APID)](#deliverable-6-tbdex-api-design-apid), intended for public consumption.

**DRI**: Kirah Sapong (@kirahsapong).

**Scope of Work**:

- Utilization of the output of the [[Deliverable 8]: tbdex UniFFI Binding](#deliverable-8-tbdex-uniffi-binding).
- Full conformance to [[Deliverable 6]: tbdex API Design (APID)](#deliverable-6-tbdex-api-design-apid).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Swift project.

## Success Criteria

The Rust Core Working Group will have achieved its objective if it delivers comprehensive implementations for the web5 and tbdex specifications, across Rust, Kotlin and Swift, as robust, extensible, performant, and secure artifacts for public consumption in highly available an reliable production environments.

## Coordination

The Rust Core Working Group will need to coordinate regularly with the web5 and tbdex Working Groups as a means of consuming the specification output of said Working Groups, and providing concrete feedback to said Working Groups which arise during implementation. The Rust Core Working Group will require the web5 and tbdex Working Groups to produce codified specification resources which enable implementation, and will provide concrete feedback in the form of meeting attendance, and the codified resources of open source development (Issue tickets, Pull Requests, comments, & RFCs).

In order to coordinate with the web5 and tbdex Working Groups, the Rust Core Working Group will elect the following individuals to represent the Rust Core Working Group within the respective Working Groups:

- web5: Neal Roessler (@nitro-neal)
- tbdex: Diane Huxley (@diehuxx)

The above individuals will be required to participate in the respective Working Group and bridge the gap between consumption of said Working Groups Deliverables, and concrete feedback.

## Communication

See [Scope](#scope) for description of GitHub repository makeup.

All productive work for the Rust Core Working Group will occur out in the open, on GitHub, for anyone to participate in.

The Rust Core Working Group will follow an RFC process, codified in the respective GitHub repository, for the matter of significant decision making, wherein Pull Requests will offer a place of communication among contributors to provide feedback.

The Rust Core Working Group will organize weekly meetings to synchronously communicate and coordinate current affairs, and each meeting will be summarized via note taking which is codified and committed to the respective GitHub repository.

The DRI of the Rust Core Working Group will attend the regular Technical Steering Committee meetings and act as the representative for the ongoings from the Rust Core Working Group.

As stated in [Coordination](#coordination), representatives from the Rust Core Working Group will attend the respective web5 and tbdex Working Group meetings to bridge the communication gap.