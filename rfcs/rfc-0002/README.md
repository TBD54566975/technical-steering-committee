# RFC-0002 - Working Group Charters

## Summary

This RFC proposes both some suggestions on how to run Working Groups along with a template for Working Group charters to be used by the TSC to allow for the creation, and maintenance, of well-structured Working Groups. With this proposal, Working Groups are able to be formed with clear scopes-of-work, including work items with reasonable timelines, and accountability by assigning DRIs.

## Motivation

The TSC enables the creation of _Working Groups_ to achieve its technical goals in developing specifications, SDKs, and other software projects and initiatives. _Working Groups_ are created with a _charter_ which is designed to focus a group on a clear set of deliverables within a given time frame. _Charters_ can always be renewed, extended, or altered as needed. It is recommended to set realistic timelines and deliverables for each _Working Group_ while taking care to not over-extend the group.

## Detailed Design

In addition to the charter template below, we should adhere to the following processes in managing Working Groups and their charters:

* A Working Group’s charter must reach consensus in the TSC before being considered approved. 

* A Working Group shall be chartered for a limited set of time (e.g. a few months, a year) with clear deliverables. This enables a realistic scope of work and aids in our goal of having a public timeline.

* Charters should be as explicit as possible in describing deliverables and their acceptance criteria to promote a shared understanding of determining when a work item is to be considered complete.

* Working Groups shall share updates through the TSC via the Working Group DRI. Working Groups shall adhere to the TSC's recommendations on regular reviews (whether monthly, quarterly, or on another timeline).

* Working Group shall ensure that all activities are well-documented: keeping meeting minutes, decision logs, and transparent progress reports, which can all be facilitated through GitHub.

* Charters may be amended at any time through RFCs run through the TSC.

* Favor extending/amending charters instead of creating new Working Groups. New Working Groups should be created for distinct work items that would benefit from being given extra focus, direction, and freedom (e.g. Web5 vs tbDEX).

### Charter Template

This template is to be used as a starting point for Working Group charters. It can be extended and amended as necessary.

```
# [PROPOSED NAME] Working Group Charter

**Start Date**:
**End Date**:
**DRI**:

## Motivation and Background
Why is this working group necessary? What does it build upon? What does it enable? Is it related to other groups?

## Scope
What exactly is in scope and out of scope for the working group.

## Deliverables
Enumeration of work products for the group. Be as detailed as possible. 

Make sure to classify the deliverables accordingly (e.g. specification, SDK, research report, etc.). Assign DRIs for each deliverable as necessary. Deliverables should each have clera acceptance criteria" so we know how to measure their completeness.

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
```

### Drawbacks

**Overhead**: Working Groups / chartering could be seen as heavy handed. An alternative could be to have a set of work items approved by the TSC and not form working groups at all. This could lead to more overhead, slowing down decision-making and execution.

Counterpoint: Having a distinct set of responsibilities and deliverables can be a powerful driver of focused delivery and accountability.

**Flexibility**: Charters may limit the flexibility of Working Groups to pivot or adapt to new information or changing circumstances. A more flexible approach could allow for more dynamic and responsive project management.

Counterpoint: Having a straightforward process for charter amendment could limit this risk.

**Complexity in Coordination**: Managing multiple Working Groups with their own charters could create complexity in coordination, especially if there are interdependencies between groups. A more centralized approach might simplify coordination and reduce potential conflicts.

Counterpoint: This trades off giving more autonomy and flexibility to those closest to the work.

#### Alternative Approaches:

**Ad Hoc Teams**: Instead of formal Working Groups, form ad hoc teams for specific tasks or projects. These teams can be more flexible and nimble, adapting quickly to changes without the need for formal charters.

**Task Forces**: Establish task forces for urgent or high-priority initiatives. Task forces can have a narrow focus and short lifespan, providing a more agile approach to addressing specific issues.

**Centralized Management**: Centralize the management of work items under the TSC. This could streamline processes and reduce the overhead associated with multiple Working Groups.

## Prior Art

The proposed charter template was heavily influenced by the [W3C Charter Template](https://w3c.github.io/charter-drafts/charter-template.html) as well as the [DIF Charter Documents](https://github.com/decentralized-identity/org/tree/master/Org%20documents/WG%20documents).

## Unresolved Questions

1. How to operate a WG (tooling & meeting/comms norms).

A GitHub repo could be created per WG; though it could also be viable to track WGs via the TSC repository.

Similarly meetings/comms norms could be handled by each group, with common suggestions for async processes (like using GitHub issues and lableing to track work).

2. Handling participation.

Should we track who is participating in each working group? Or stick to a top level DRI for the Working Group and each of its deliverables? How do we handle changes over time?

3. Scope and Definitions.

What are the precise definitions and boundaries for terms such as "clear deliverables," "realistic timelines," and "accountability"? These terms need to be clearly defined and agreed upon to avoid ambiguity in the chartering process.

4. Process for Amendments.

How exactly will the process for amending charters work? What are the criteria for deciding whether to amend an existing charter or create a new Working Group?

5. Resource Allocation Details

How will resource allocation be managed and monitored? What are the criteria for allocating resources to different Working Groups, and how will changes in resource needs be handled?

6. Feedback Mechanism

What specific methods will be used to gather feedback from Working Group members and stakeholders? How will this feedback be utilized to improve the chartering process?

6. Coordination with Other Functions.

What are the detailed mechanisms for coordination between Working Groups and other functions (Compliance, Legal, DevRel, OSPO, etc.)? How will potential conflicts be managed?

7. Exit Criteria.

What are the detailed criteria for disbanding a Working Group or transitioning it into a different form? How will the decision-making process be structured to ensure clarity and fairness?

## Future Possibilities

* Room for automation/tooling to streamline these processes. 

* Promoting consistency across working groups via the TSC (e.g. shared infra/tooling across WGs., communication norms).

* Cross-domain work - encouraging and facilitating more collaboration between Working Groups on cross-cutting initiatives.
