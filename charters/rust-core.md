# Rust Core Working Group Charter

**Start Date**: June 6th 2024

**End Date**: Unknown

**DRI**: Kendall Weihe

## Motivation and Background

This working group will streamline and standardize the implementations of the open standards presented by the web5 and tbdex Working Groups.

🚧 image: web5 & tbdex WGs feed into rust code which feeds into kt and swift 🚧

SDKs for web5 and tbdex have been implemented across TypeScript ([web5-js](https://github.com/TBD54566975/web5-js/) & [tbdex-js](https://github.com/TBD54566975/tbdex-js/)), Kotlin ([web5-kt](https://github.com/TBD54566975/web5-kt/) & [tbdex-kt](https://github.com/TBD54566975/tbdex-kt/)), Swift ([web5-swift](https://github.com/TBD54566975/web5-swift/) & [tbdex-swift](https://github.com/TBD54566975/tbdex-swift/)), Golang ([web5-go](https://github.com/TBD54566975/web5-go/) & [tbdex-go](https://github.com/TBD54566975/tbdex-go/)), and Dart ([web5-dart](https://github.com/TBD54566975/web5-dart/) & [tbdex-dart](https://github.com/TBD54566975/tbdex-dart/)). Streamlining the implementation's for web5 and tbdex by implementing "core" logic in Rust, and then binding the solution into the target language, offers many benefits. The benefits of Rust Core include but are not limited to:

- Strong interoperability assurances.
- Reduce maintenance burden for particularly dense feature sets (ex. did:dht).
- Serve as a Schelling Point for matters of implementation governance.
- Contain a convenient location for a historical record of decisions-made.

Rust is uniquely qualified as the solution to a core implementation which is deployed cross-platform because of open source tooling availability through WASM and UniFFI. Furthermore, Rust has a broad array of open source support, and Rust has the unique feature of memory safety (relative to alternatives such as C).

## Scope

The comprehensive implementations of the web5 and tbdex specifications across Rust, Kotlin and Swift are within the scope of this Working Group. Alongside of each implementation, documentation comments ("doc comments"), test vectors & integrations, example usages, and CI/CD solutions (eg. security analysis, test automation, artifact version & publication, etc.) are all within scope of this Working Group. 

The Rust Core Working Group will make an intentional effort to prioritize matters of security and performance. Furthermore, with regards to API design & developer experience (DX), this Working Group will prioritize first and foremost modularity and extensibility, over DX convenience, in order to limit the liklihood of introducing breaking changes to consumers of the delivered SDKs.

The Rust Core Working Group is not concerned with the definitions of the web5 and tbdex specifications, both of which are the concerns of the respective Working Group. However, the Rust Core Working Group will offer valuable feedback mechanisms to the web5 and tbdex Working Groups and so although the web5 and tbdex specifications are not within the scope of this Working Group, a considerable amount of cross-Working Group collaboration is to be expected (see [Coordination](#coordination) and [Communication](#communication) below).

The Rust Core Working Group codifies a standard API Design (🚧 link to APID deliverables 🚧) which is implemented across all supported language implementations (Rust, Kotlin and Swift), but any additional API features or design characteristics are not within the scope of this Working Group. Each implementation must support the standard API Design as a baseline implementation, but does not exclude the possibility of additional features.

## Deliverables

🚧 more detailed diagram including APID & UniFFI bindings 🚧 

### [Deliverable 1]: web5 API Design (APID) 

**Description**: The *web5 APID* is a language-independent codified API Design which serves to act as a baseline of features for implementations. The APID is primarily considered to be a deliverable for internal usage, but does not exclude the possibility of external consumption.

**DRI**: Kendall Weihe.

**Scope of Work**:

- Custom DSL which is conceptually compatible with all target languages.
- Codification of the API Design using the Custom DSL.
- Example usages.
- Doc comments inline for the API Design .
- Test vector resources.

**Timeline/Milestones**: Unknown???

**Exit Criteria**: Comprehensive feature coverage for the web5 specification, codified in the Custom DSL, committed to source code.

### [Deliverable 2]: web5 Rust Implementation

**Description**: Rust implementation of the [web5 API Design (APID)](🚧), intended for public consumption.

**DRI**: Kendall Weihe.

**Scope of Work**:

- Full conformance to [web5 API Design (APID)](🚧).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Rust project.

### [Deliverable 3]: web5 UniFFI Binding

**Description**: Rust crate which utilizes [UniFFI](https://github.com/mozilla/uniffi-rs) in conjunction with the [web5 Rust Implementation](🚧) to create Kotlin and Swift binded code, which feed into [web5 Kotlin Implementation](🚧) and [web5 Swift Implementation](🚧). This deliverable is intended primarily for internal purposes but does not exclude the possibility of public consumption.

**DRI**: Kendall Weihe.

**Scope of Work**:

- UDL file with comprehensive feature coverage from [web5 Rust Implementation](🚧).
- Successful binding executions for Kotlin & Swift.

**Timeline/Milestones**: ???

**Exit Criteria**: Successful binding executions, over the comprehensive set of features from [web5 Rust Implementation](🚧), for Kotlin and Swift.

### [Deliverable 4]: web5 Kotlin Implementation

**Description**: Kotlin implementation of web5 by wrapping [web5 UniFFI Binding](🚧) as to be conformant to the [web5 API Design (APID)](🚧), intended for public consumption.

**DRI**: Neal Roessler.

**Scope of Work**:

- Utilization of the output of the [web5 UniFFI Binding](🚧).
- Full conformance to [web5 API Design (APID)](🚧).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Kotlin project.

### [Deliverable 5]: web5 Swift Implementation

**Description**: Swift implementation of web5 by wrapping [web5 UniFFI Binding](🚧) as to be conformant to the [web5 API Design (APID)](🚧), intended for public consumption.

**DRI**: Kirah Sapong.

**Scope of Work**:

- Utilization of the output of the [web5 UniFFI Binding](🚧).
- Full conformance to [web5 API Design (APID)](🚧).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Swift project.

### [Deliverable 6]: tbdex API Design (APID) 

**Description**: The *tbdex APID* is a language-independent codified API Design which serves to act as a baseline of features for implementations. The APID is primarily considered to be a deliverable for internal usage, but does not exclude the possibility of external consumption.

**DRI**: Kendall Weihe

**Scope of Work**:

- Custom DSL which is conceptually compatible with all target languages.
- Codification of the API Design using the Custom DSL.
- Example usages.
- Doc comments inline for the API Design.
- Test vector resources.

**Timeline/Milestones**: Unknown???

**Exit Criteria**: Comprehensive feature coverage for the tbdex specification, codified in the Custom DSL, committed to source code.

### [Deliverable 7]: tbdex Rust Implementation

**Description**: Rust implementation of the [tbdex API Design (APID)](🚧), intended for public consumption.

**DRI**: Diane Huxley.

**Scope of Work**:

- Full conformance to [tbdex API Design (APID)](🚧).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Rust project.

### [Deliverable 8]: tbdex UniFFI Binding

**Description**: Rust crate which utilizes [UniFFI](https://github.com/mozilla/uniffi-rs) in conjunction with the [tbdex Rust Implementation](🚧) to create Kotlin and Swift binded code, which feed into [tbdex Kotlin Implementation](🚧) and [tbdex Swift Implementation](🚧). This deliverable is intended primarily for internal purposes but does not exclude the possibility of public consumption.

**DRI**: Kendall Weihe.

**Scope of Work**:

- UDL file with comprehensive feature coverage from [tbdex Rust Implementation](🚧).
- Successful binding executions for Kotlin & Swift.

**Timeline/Milestones**: ???

**Exit Criteria**: Successful binding executions, over the comprehensive set of features from [tbdex Rust Implementation](🚧), for Kotlin and Swift.

### [Deliverable 9]: tbdex Kotlin Implementation

**Description**: Kotlin implementation of tbdex by wrapping [tbdex UniFFI Binding](🚧) as to be conformant to the [tbdex API Design (APID)](🚧), intended for public consumption.

**DRI**: Neal Roessler.

**Scope of Work**:

- Utilization of the output of the [tbdex UniFFI Binding](🚧).
- Full conformance to [tbdex API Design (APID)](🚧).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Kotlin project.

### [Deliverable 10]: tbdex Swift Implementation

**Description**: Swift implementation of tbdex by wrapping [tbdex UniFFI Binding](🚧) as to be conformant to the [tbdex API Design (APID)](🚧), intended for public consumption.

**DRI**: Kirah Sapong.

**Scope of Work**:

- Utilization of the output of the [tbdex UniFFI Binding](🚧).
- Full conformance to [tbdex API Design (APID)](🚧).
- Comprehensive integration of test vectors (from APID).
- Comprehensive documentation comments (from APID).
- CI/CD implementations for security analysis, test automation, and crate publication.

**Timeline/Milestones**: ???

**Exit Criteria**: Full implementation of *Scope of Work* as a Swift project.

## Success Criteria

How will we determine whether this group has achieved its objectives?

## Coordination

Will this group interact with other working groups? Other functions (Compliance, Legal, DevRel, OSPO, etc.). What resources will you require?

---

Representatives to attend web5 (???) and tbdex (Diane) Working Groups

## Communication

How will this group organize itself and its work (which GitHub repos, projects, communication channels, etc.)? 

How will progress be reviewed and reported to the TSC or other stakeholders? Include the frequency of reviews and the format of progress reports.