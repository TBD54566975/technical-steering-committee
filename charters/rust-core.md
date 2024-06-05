# Rust Core Working Group Charter

**Start Date**: June 6th 2024

**End Date**: Unknown

**DRI**: Kendall Weihe

## Motivation and Background

This working group intends to streamline and standardize the implementations of the open standards presented by the web5 and tbdex Working Groups. By implementing the open standards, the Rust Core Working Group enables the runtime execution of the web5 and tbdex standards. 

To date, we have implemented web5 and tbdex across many languages, and all in isolation. All implementations support the same general set of features, but no two implementation is identical. The lack of consistency across implementations has caused many undesired consequences which include, but are not limited to:

- Weak interoperability assurances
- Bike-shedding
- Inconsistent naming creates a barrier for cross-language (or higher-level) collaboration
- Building developer guides at https://developer.tbd.website/ which span many languages is inefficient
- Contributors who span multiple languages have increased cognitive overhead
- Excessive maintenance burden for dense solutions such as did:dht
- Ad hoc documentation comments can lead to a lack of quality
- Test vectors are a challenge to create across implementations with different function signatures
- Lack of codified governance has led to production-impacting bugs

The motivation of the Rust Core Working Group is to streamline the implementations of web5 and tbdex from a single starting place to alleviate the above consequences. Rust is uniquely qualified for the matter for cross-language bindings because of the available open source tooling with WASM & UniFFI. 

## Scope



Out of scope:
- Specification definitions
- Developer experiences beyond the scope defined in the API Design

In scope:
- web5 & tbdex specs
- Codification of an API Design conceptualized across all target implementation languages
- Implementation of the API Design in target languages

## Deliverables

Enumeration of work products for the group. Be as detailed as possible. 

Make sure to classify the deliverables accordingly (e.g. specification, SDK, research report, etc.). Assign DRIs for each deliverable as necessary. Deliverables should each have clear "acceptance criteria" so we know how to measure their completeness.

### [Deliverable 1] – [Type]

**Description**:

**DRI**:

**Scope of Work**:

**Timeline/Milestones**:

**Exit Criteria**:

## Success Criteria

How will we determine whether this group has achieved its objectives?

## Coordination

Will this group interact with other working groups? Other functions (Compliance, Legal, DevRel, OSPO, etc.). What resources will you require?

## Communication

How will this group organize itself and its work (which GitHub repos, projects, communication channels, etc.)? 

How will progress be reviewed and reported to the TSC or other stakeholders? Include the frequency of reviews and the format of progress reports.