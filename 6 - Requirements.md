# Requirements Stage

The goal of this stage is to transform the reviewed product and interaction knowledge into a complete, implementation-ready and testable specification.

By the beginning of the Requirements Stage, the product behavior and interaction model have already been defined and reviewed.

The purpose of this stage is not to redesign the product or determine how it should be technically implemented.

The purpose is to describe the expected product behavior with sufficient precision for implementation, verification, and future UAT.

Requirements should preserve the product structure established by the previous Stages rather than introduce an unrelated requirements taxonomy.

The primary functional hierarchy is:

```text
Journey
└── Scenario
    └── Acceptance Criteria
```

Cross-cutting requirements may be represented separately when doing so makes them substantially easier to read, review, approve, or reuse.

## Objective

Produce a Requirements Document that:

- converts reviewed product behavior into precise and testable requirements;
- incorporates the reviewed Interaction artifact;
- covers all in-scope Journeys and Scenarios;
- defines sufficient detail for implementation;
- defines Acceptance Criteria for verification;
- consolidates cross-cutting requirements where this improves review and usability;
- preserves traceability between product behavior, interaction, requirements, and future UAT;
- avoids making technical implementation decisions that belong to the Solutions Stage.

## Input

The Requirements Stage uses the accumulated reviewed product knowledge.

Primary inputs include:

- Idea Document;
- Domain Document;
- Shape Document;
- Structure Document;
- reviewed Behavior Document and behavioral artifacts;
- reviewed Interaction artifact;
- explicit scope decisions;
- assumptions and constraints;
- Out of Scope decisions;
- relevant Consultant decisions produced during previous Stages.

The Requirements Stage must use the current reviewed product knowledge rather than obsolete pre-review versions.

## Focus Areas

### 1. Functional Requirements

Functional requirements describe the expected behavior of the product in sufficient detail for implementation and verification.

They are organized primarily as:

```text
Journey
└── Scenario
    └── Acceptance Criteria
```

A Journey groups related product behavior around a meaningful user or system objective.

A Scenario describes a concrete interaction or system behavior within that Journey.

Depending on the Scenario, its requirements may include:

- actors;
- trigger;
- preconditions;
- expected flow;
- system responses;
- relevant fields and attributes;
- required/optional fields;
- input constraints and validation;
- business rules;
- state-dependent behavior;
- permissions;
- alternative flows;
- negative flows;
- error handling;
- resulting state;
- relevant system feedback;
- references to corresponding Interaction views;
- other information required to implement the Scenario unambiguously.

Not every Scenario requires every element.

Do not add sections mechanically when they provide no useful information.

#### Acceptance Criteria

Each Scenario must contain sufficient Acceptance Criteria to determine whether the implemented behavior satisfies the requirement.

Acceptance Criteria should:

- be observable or otherwise verifiable;
- cover the expected successful behavior;
- cover materially relevant alternative and negative behavior;
- include important boundary conditions where applicable;
- reflect relevant permissions and state-dependent behavior;
- correspond to the behavior actually required by the Scenario.

Acceptance Criteria are intended to support implementation verification and later UAT.

### 2. Roles and Permissions

Consolidate roles and permissions when a centralized representation makes the authorization model easier to understand and review.

This may include:

- role definitions;
- role descriptions;
- permission matrix;
- access restrictions;
- relevant actor distinctions.

Individual Scenarios may reference the centralized permission model rather than reproduce it in full.

Scenario-specific authorization behavior should remain in the Scenario where necessary for understanding or implementation.

### 3. System Messages

Consolidate user-facing system messages when centralized review makes their wording and usage easier to validate.

For each relevant message, define as applicable:

- trigger or condition;
- context;
- message text;
- variables/placeholders;
- relevant actor;
- resulting interaction where necessary.

System Messages should correspond to actual behavior defined by the requirements and Interaction artifact.

Do not invent messages merely to populate the section.

### 4. Notifications

Define notifications that the product is required to send.

For each notification, define as applicable:

- trigger;
- recipient;
- channel;
- timing;
- conditions;
- message/template;
- variables/placeholders;
- duplicate-prevention or delivery rules where product behavior requires them.

Notification behavior must remain consistent with the corresponding functional requirements.

### 5. Non-Functional Requirements

Identify non-functional requirements that materially constrain the expected product.

Consider relevant areas such as:

- performance;
- availability and reliability;
- security;
- privacy and data protection;
- accessibility;
- scalability;
- compatibility;
- supported platforms and environments;
- localization;
- retention and deletion;
- auditability;
- logging and observability;
- backup and recovery;
- regulatory or compliance requirements.

Do not invent arbitrary numerical targets or constraints.

When a relevant NFR cannot yet be determined, record the unresolved requirement or required decision rather than fabricating a value.

Only include categories relevant to the product.

### 6. Glossary

Maintain a consolidated glossary of product terminology required to interpret the Requirements Document consistently.

The glossary should use terminology established by the reviewed upstream product knowledge.

The Requirements Stage is not responsible for repeating Domain research.

Add or clarify terminology when specification work reveals that precise interpretation is necessary.

## Process

### Phase 1 — Requirements Generation

#### 1. Read Accumulated Reviewed Product Knowledge

Read the relevant upstream Documents and artifacts.

Pay particular attention to:

- in-scope functionality;
- Actors;
- Journeys;
- Scenarios;
- states and transitions;
- business rules;
- permissions;
- interaction decisions;
- validation behavior;
- system feedback;
- error and recovery behavior;
- explicit Out of Scope decisions.

Do not derive requirements from a single upstream artifact in isolation.

#### 2. Build Requirements Coverage

Create an internal coverage model connecting the reviewed product knowledge to the requirements that must be produced.

At minimum, verify coverage across:

```text
In-Scope Functionality
×
Actors
×
Journeys
×
Scenarios
×
States
×
Relevant Interaction
```

The purpose is not to create requirements mechanically for every combination.

The purpose is to prevent reviewed product behavior from disappearing during specification.

#### 3. Build the Journey and Scenario Structure

Organize the functional specification using the product's established Journey and Scenario structure.

Do not create an unrelated functional decomposition merely because a traditional requirements template uses one.

Where upstream knowledge does not yet have sufficient decomposition for specification, the Agent may refine the requirement structure without changing established product meaning.

Do not silently introduce new product scope.

#### 4. Specify Each Scenario

For each Scenario, determine what information is necessary to make it implementation-ready and testable.

Specify relevant:

```text
Actor / context
Trigger
Preconditions
Flow
Fields and constraints
Validation
Business rules
State-dependent behavior
Alternative behavior
Negative behavior
System feedback
Resulting state
Acceptance Criteria
```

Use only the elements relevant to that Scenario.

Keep information close to the Scenario when doing so makes the requirement easier to understand and implement.

Do not extract information into separate requirement categories merely for taxonomic purity.

#### 5. Produce Acceptance Criteria

Derive Acceptance Criteria from the required Scenario behavior.

Acceptance Criteria must be sufficiently concrete to verify the implementation.

Ensure that important successful, alternative, negative, state-dependent, permission-dependent, and boundary behavior is represented where relevant.

Do not simply repeat the Scenario flow in different wording.

#### 6. Consolidate Cross-Cutting Requirements

After functional requirements have been specified, consolidate information that is substantially easier to review or approve together.

This may include:

```text
Roles & Permissions
System Messages
Notifications
NFR
Glossary
```

The reason for consolidation is usability of the Requirements Document, not classification for its own sake.

Do not create additional cross-cutting sections unless they materially improve review, approval, consistency, or reuse.

#### 7. Separate Requirements from Solutions

Review the specification for premature implementation decisions.

Requirements should define:

> what behavior or result the system must provide and the conditions it must satisfy.

The Requirements Stage may specify product-visible entities, fields, values, constraints, validation, and relationships when they are necessary to define expected behavior.

It should not prescribe technical persistence models merely because those product concepts will eventually require storage.

For example:

```text
Requirement:
Journey Title is required and must not exceed the defined maximum length.
```

does not imply:

```text
Solution:
journeys.title VARCHAR(...) NOT NULL
```

Likewise, a requirement that repeated processing must not create duplicate results does not itself prescribe a particular idempotency implementation.

Technical architecture, storage models, service decomposition, APIs, infrastructure, and implementation mechanisms belong to the Solutions Stage unless an existing constraint already mandates them.

#### 8. Perform Requirements Review

Before presenting the Requirements Document for human review, verify:

**Coverage**

- every in-scope Journey is represented;
- relevant Scenarios are represented;
- reviewed Behavior has not disappeared;
- reviewed Interaction decisions affecting implementation are represented;
- relevant alternative, negative, recovery, and boundary behavior is covered.

**Consistency**

- terminology is consistent;
- roles and permissions do not contradict individual Scenarios;
- System Messages correspond to defined states/events;
- Notifications correspond to defined triggers;
- Acceptance Criteria agree with Scenario behavior;
- equivalent rules do not contradict each other.

**Testability**

- requirements can be objectively verified;
- Acceptance Criteria have observable outcomes;
- ambiguous adjectives such as "fast", "convenient", "secure", or "user-friendly" are not used as substitutes for requirements;
- undefined implementation assumptions are not presented as requirements.

**Stage Boundary**

- implementation choices have not leaked unnecessarily into Requirements;
- unresolved product decisions are identified rather than silently converted into technical assumptions.

Correct obvious defects before presenting the Requirements Document.

### Phase 2 — Consultant Review & Refinement

#### 9. Consultant Reviews the Requirements

The Consultant reviews the actual Requirements Document.

The Consultant may:

- correct requirements;
- add missing scenarios;
- remove unnecessary requirements;
- clarify rules;
- modify Acceptance Criteria;
- adjust requirement decomposition;
- correct cross-cutting requirements;
- identify upstream gaps;
- identify premature Solution decisions.

The Agent must not simulate Consultant Review.

#### 10. Refine the Requirements Document

Apply Consultant findings to the existing Requirements Document.

Preserve unaffected valid work.

Do not regenerate the complete specification merely because part of it requires correction.

Repeat Consultant Review and refinement as necessary.

#### 11. Resolve Upstream Gaps

If specification exposes missing or contradictory product knowledge:

1. identify the gap;
2. identify the earliest Stage responsible for establishing it;
3. determine whether unaffected Requirements work can continue;
4. record the issue;
5. return the material decision to the appropriate Stage or human reviewer where necessary.

Do not silently invent missing product behavior merely to complete the Requirements Document.

## Output

The output of the Requirements Stage is a **Requirements Document** containing, where applicable:

```text
Glossary

Roles & Permissions

System Messages

Notifications

Non-Functional Requirements

Functional Requirements
    Journey
        Scenario
            detailed requirements
            Acceptance Criteria
```

The exact ordering of sections may be adjusted for readability.

A section should not exist merely because the template permits it.

## Completion Criteria

The Requirements Stage is Complete when:

- all known in-scope Journeys are covered;
- relevant Scenarios are specified;
- each Scenario contains sufficient detail for implementation;
- relevant fields, constraints, validation, rules, states, permissions, errors, and outcomes are specified where necessary;
- Acceptance Criteria are sufficient to verify required behavior;
- relevant cross-cutting requirements are consolidated where doing so improves review or reuse;
- Roles and Permissions are internally consistent;
- System Messages correspond to defined product behavior;
- Notifications have defined triggers, recipients, channels, and content where applicable;
- applicable NFRs have been specified or material unresolved NFR decisions are explicitly recorded;
- terminology is consistent;
- the Requirements Document is consistent with reviewed Behavior and Interaction knowledge;
- no known in-scope behavior has disappeared during specification;
- technical implementation decisions have not been introduced unnecessarily;
- material upstream gaps are resolved or explicitly recorded;
- actual Consultant Review has occurred;
- required refinement has been completed;
- the Consultant determines that the Requirements Document is sufficiently complete for downstream Solutions work.
