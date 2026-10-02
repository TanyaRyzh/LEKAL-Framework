# Requirements Stage

## Purpose

The Requirements Stage transforms validated product behavior and interaction
knowledge into a precise, implementation-ready, and testable product
specification.

By the beginning of the Requirements Stage, the product's functional scope,
behavioral model, and interaction model have already been established and
validated.

Requirements do not redesign the product.

Requirements define the expected product behavior and constraints with
sufficient precision for implementation, verification, future UAT, and
downstream technical design.

The primary functional hierarchy is:

Journey
└── Scenario
    └── Acceptance Criteria

Cross-cutting requirements may be represented separately where consolidation
makes the specification substantially easier to understand, review, maintain,
or reuse.

---

## Objective

Produce a Requirements Document that:

- converts validated product behavior into precise and testable requirements;
- incorporates validated Interaction decisions that materially affect expected
  product behavior;
- covers all known in-scope Journeys and relevant Scenarios;
- provides sufficient detail for implementation;
- defines sufficient Acceptance Criteria for verification;
- preserves traceability between validated product knowledge, Requirements,
  implementation, and future UAT;
- consolidates cross-cutting requirements where doing so improves clarity and
  consistency;
- identifies material unresolved product decisions rather than hiding them;
- avoids technical implementation decisions that belong to Solutions.

---

## Input

The Requirements Stage uses the accumulated validated product knowledge.

Primary inputs are:

- Behavior v3;
- Interaction v3;
- Structure v2, including established IN / OUT scope decisions;
- established scope decisions;
- established constraints and assumptions;
- Out of Scope decisions;
- relevant validated product decisions from previous Stages.

Other upstream product knowledge may be used where necessary to correctly
interpret the current validated product model.

Behavior is authoritative for product behavior.

Interaction provides validated context for how important behavior is
represented to users.

Requirements must preserve the validated product model rather than derive a
new one.

---

## Core Principles

### 1. Requirements Specify Established Product Behavior

Requirements make validated product behavior precise.

They may refine the specification of established behavior where additional
detail is necessary for implementation or verification.

They must not silently:

- introduce new product scope;
- change Actor responsibilities;
- change permissions;
- change Rules;
- change State logic;
- change established workflows;
- change recovery behavior;
- contradict validated Interaction;
- resolve missing product decisions by assumption.

When specification exposes a missing or contradictory product decision, that
is an upstream gap rather than permission to invent an answer.

---

### 2. Requirements Preserve Product Structure

Requirements should preserve the product structure established by previous
Stages rather than introduce an unrelated requirements taxonomy.

The primary hierarchy is:

Journey
└── Scenario
    └── Acceptance Criteria

A Journey groups related product behavior around a meaningful user or system
objective.

A Scenario describes concrete user or system behavior within that Journey.

Acceptance Criteria define observable conditions used to determine whether the
required Scenario behavior has been implemented correctly.

The hierarchy may be refined where necessary for specification clarity, but
refinement must preserve established product meaning.

---

### 3. Precision Is Driven by Implementation and Verification Needs

Requirements should contain enough detail to remove material ambiguity for
implementation and verification.

Precision does not mean documenting every possible fact about the product.

Include detail when its absence would require an implementation or verification
decision that should instead be defined as product behavior.

Do not add detail merely because a requirements template permits it.

---

### 4. Requirements Remain Product-Level

Requirements define:

> what behavior or result the product must provide and the conditions it must
> satisfy.

They may define product-visible:

- entities;
- attributes;
- fields;
- values;
- relationships;
- constraints;
- validation;
- Rules;
- States;
- permissions;
- observable responses;
- required outcomes.

Requirements do not prescribe technical implementation unless an established
constraint already mandates it.

Technical architecture, storage models, service decomposition, APIs,
infrastructure, deployment, implementation mechanisms, and technology
selection belong to Solutions.

---

### 5. Interaction Informs Requirements Without Becoming Design

Interaction provides validated context for how product behavior is represented
and accessed.

Requirements should preserve Interaction decisions that materially affect
expected product behavior or implementation.

This may include:

- interaction context;
- navigation behavior;
- information hierarchy;
- available actions;
- Actor-specific interaction modes;
- representation of important States;
- continuation and recovery behavior;
- system feedback;
- relationships between overview and detail.

Requirements should not convert incidental low-fidelity visual choices into
mandatory product behavior.

Visual styling, detailed layout, component design, spacing, and other complete
interface decisions belong to Design unless they materially define required
product behavior.

---

### 6. Completeness Means Behavioral Coverage, Not Document Volume

A complete Requirements Document preserves all known in-scope behavior needed
for implementation and verification.

Completeness is not measured by:

- number of pages;
- number of requirements;
- number of Acceptance Criteria;
- number of sections;
- number of fields in a template.

A concise specification can be complete.

A large specification can still contain material gaps.

---

## Focus Areas

### 1. Functional Requirements

Functional Requirements describe expected product behavior in sufficient
detail for implementation and verification.

They are organized primarily as:

Journey
└── Scenario
    └── Acceptance Criteria

Depending on the Scenario, specification may include:

- Actor or context;
- trigger;
- preconditions;
- expected flow;
- system responses;
- relevant fields and attributes;
- required and optional data;
- constraints;
- validation;
- Rules;
- State-dependent behavior;
- permissions;
- alternative behavior;
- negative behavior;
- error handling;
- recovery behavior;
- resulting State;
- relevant system feedback;
- relevant Interaction context.

Not every Scenario requires every element.

Information should remain close to the Scenario when doing so makes the
behavior easier to understand, implement, and verify.

---

### 2. Acceptance Criteria

Each Scenario must contain sufficient Acceptance Criteria to determine whether
the implemented behavior satisfies the Requirement.

Acceptance Criteria should:

- be observable or otherwise objectively verifiable;
- cover expected successful behavior;
- cover materially relevant alternative behavior;
- cover materially relevant negative behavior;
- include important boundary conditions where applicable;
- reflect relevant permissions;
- reflect relevant State-dependent behavior;
- reflect relevant recovery behavior;
- correspond to the behavior actually required by the Scenario.

Acceptance Criteria should not merely repeat the Scenario flow in different
words.

Acceptance Criteria define verification conditions.

They are not intended to become a complete QA test suite.

---

### 3. Fields and Validation

Where product-visible data is necessary to define expected behavior,
Requirements should specify relevant:

- meaning;
- required or optional status;
- allowed values;
- format;
- constraints;
- uniqueness;
- defaults;
- editability;
- State-dependent availability;
- validation behavior;
- user-visible error behavior.

Only specify constraints that are established or necessary product decisions.

Do not invent arbitrary limits, formats, defaults, or validation Rules merely
because they are common implementation practices.

If a material constraint is necessary but unresolved, record the unresolved
decision.

---

### 4. Roles and Permissions

Roles and permissions may be consolidated when a centralized representation
makes the authorization model easier to understand and review.

This may include:

- role definitions;
- role descriptions;
- permission matrix;
- access restrictions;
- relevant Actor distinctions.

Individual Scenarios may reference the centralized authorization model rather
than reproduce it in full.

Scenario-specific authorization behavior should remain in the Scenario where
necessary for understanding or implementation.

The centralized model and Scenario behavior must remain consistent.

---

### 5. States and Recovery

Requirements should specify State-dependent behavior where States affect what
the product or Actor can do.

Where relevant, Requirements should make clear:

- applicable State;
- available actions;
- transition conditions;
- resulting State;
- invalid transitions;
- recovery behavior;
- invalidation or recalculation behavior;
- consequences of relevant structural or behavioral changes.

Requirements do not need to reproduce the complete behavioral State model in
every Scenario.

State behavior may be centralized or referenced where doing so remains clear
and unambiguous.

---

### 6. System Messages

User-facing System Messages may be consolidated when centralized review makes
their wording and usage easier to validate.

For each relevant message, define as applicable:

- trigger or condition;
- context;
- message text;
- variables or placeholders;
- relevant Actor;
- resulting interaction where necessary.

System Messages must correspond to actual required product behavior.

Do not invent messages merely to populate the section.

---

### 7. Notifications

Define Notifications the product is required to send.

For each relevant Notification, define as applicable:

- trigger;
- recipient;
- channel;
- timing;
- conditions;
- message or template;
- variables or placeholders;
- duplicate-prevention or delivery Rules where product behavior requires them.

Notification behavior must remain consistent with corresponding Functional
Requirements.

Do not introduce Notifications merely because they may be useful.

---

### 8. Non-Functional Requirements

Define Non-Functional Requirements that materially constrain the expected
product.

Relevant areas may include:

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

Only relevant categories should be included.

Do not invent arbitrary numerical targets or constraints.

When a material NFR cannot yet be determined, record the unresolved requirement
or required decision rather than fabricating a value.

---

### 9. Glossary

Maintain a consolidated glossary where precise terminology is necessary for
consistent interpretation of the Requirements Document.

The Glossary should use terminology established by validated upstream product
knowledge.

The Requirements Stage does not repeat Domain research.

Terms should be added or clarified when specification reveals that precise
interpretation is necessary.

---

## Process

### 1. Establish Requirements Coverage

Before detailed specification, establish coverage between validated product
knowledge and the Requirements that must represent it.

At minimum, consider:

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

Also consider where relevant:

- Rules;
- permissions;
- alternative behavior;
- negative behavior;
- recovery;
- validation;
- constraints.

The purpose is not to create Requirements mechanically for every possible
combination.

The purpose is to prevent validated product behavior from disappearing during
specification.

---

### 2. Establish the Journey and Scenario Structure

Organize Functional Requirements using the product's established Journey and
Scenario structure.

Refine decomposition where necessary to make the specification usable, but do
not change established product meaning or silently introduce new scope.

Avoid unrelated functional decomposition created solely to fit a generic
requirements template.

---

### 3. Specify Scenario Behavior

For each in-scope Scenario, determine what information is necessary to make the
expected behavior implementation-ready and testable.

Specify only relevant elements.

Keep information close to the Scenario when this improves understanding and
implementation.

Do not extract information into separate categories merely for taxonomic
purity.

---

### 4. Define Acceptance Criteria

Derive Acceptance Criteria from the required Scenario behavior.

Acceptance Criteria must be sufficiently concrete to verify implementation.

Cover materially relevant:

- successful behavior;
- alternatives;
- negative behavior;
- State-dependent behavior;
- permission-dependent behavior;
- recovery;
- validation;
- boundary conditions.

Do not simply repeat the Scenario flow.

---

### 5. Consolidate Cross-Cutting Requirements

After Functional Requirements are sufficiently understood, consolidate
information that is substantially easier to review, approve, maintain, or
reuse together.

This may include:

- Roles & Permissions;
- System Messages;
- Notifications;
- Non-Functional Requirements;
- Glossary.

Consolidation exists for specification usability and consistency.

Do not create cross-cutting sections for classification alone.

---

### 6. Check Coverage

Verify that:

- every known in-scope Journey is represented;
- relevant Scenarios are represented;
- validated Behavior has not disappeared;
- validated Interaction decisions affecting expected behavior or
  implementation are represented;
- materially relevant alternative behavior is covered;
- materially relevant negative behavior is covered;
- recovery behavior is covered where applicable;
- important boundary conditions are covered.

---

### 7. Check Consistency

Verify that:

- terminology is consistent;
- roles and permissions agree with Scenario behavior;
- State behavior is internally consistent;
- System Messages correspond to defined product behavior;
- Notifications correspond to defined triggers;
- Acceptance Criteria agree with Scenario behavior;
- equivalent Rules do not contradict each other;
- cross-cutting Requirements do not contradict local Scenario Requirements;
- Requirements remain consistent with validated Behavior and Interaction.

---

### 8. Check Testability

Verify that:

- Requirements can be objectively verified;
- Acceptance Criteria have observable outcomes;
- materially ambiguous behavior has been resolved or explicitly identified;
- vague qualities are not used as substitutes for Requirements;
- implementation assumptions are not presented as established product
  Requirements.

---

### 9. Check Stage Boundaries

Verify that:

- no new product scope has been silently introduced;
- missing product decisions have not been silently invented;
- Interaction has not been redesigned;
- low-fidelity visual choices have not been unnecessarily converted into
  mandatory Requirements;
- technical implementation decisions have not been introduced unnecessarily;
- unresolved product decisions remain explicit.

---

## Upstream Gaps

Requirements work may reveal missing, ambiguous, or contradictory product
knowledge.

When this occurs:

1. identify the unresolved product question;
2. identify the earliest Stage responsible for establishing it;
3. identify the affected Requirements;
4. determine whether unaffected specification can continue;
5. resolve the product decision at the appropriate methodological level before
   treating it as established Requirements.

Do not silently invent missing product behavior merely to make the
Requirements Document appear complete.

A localized upstream gap does not necessarily invalidate unrelated
Requirements work.

---

## Consultant Review

The initial Requirements v1 is an analytical proposal.

The Consultant reviews and refines the complete Requirements Document toward v2.
Independent review may challenge the working artifact during this refinement.
Findings are advisory; the Consultant accepts, rejects, defers, or resolves them upstream.

The Consultant may:

- correct Requirements;
- add missing Scenarios;
- remove unnecessary Requirements;
- clarify Rules;
- modify Acceptance Criteria;
- adjust requirement decomposition;
- correct cross-cutting Requirements;
- identify upstream gaps;
- identify premature Solution decisions;
- simplify over-specified areas;
- request additional precision where implementation or verification remains
  ambiguous.

Review should consider the Requirements Document as a coherent specification,
not only as isolated individual Requirements.

Findings should be incorporated without unnecessarily discarding unaffected
valid work.

Consultant Review may be repeated until the Requirements Document is
sufficiently complete and coherent for downstream work.

The Consultant completes Requirements v2, the authoritative input to Solutions.
Review does not create or approve a version. No separate post-Requirements
validation checkpoint or Requirements v3 is currently defined.

---

## Output

The output of the Requirements Stage is a **Requirements Document** containing,
where applicable:

Glossary

Roles & Permissions

System Messages

Notifications

Non-Functional Requirements

Functional Requirements
    Journey
        Scenario
            detailed Requirements
            Acceptance Criteria

The exact ordering may be adjusted for readability.

A section should not exist merely because the structure permits it.

---

## Completion Criteria

The Requirements Stage is Complete when:

- all known in-scope Journeys are covered;
- relevant Scenarios are specified;
- each Scenario contains sufficient detail for implementation;
- relevant fields, constraints, validation, Rules, States, permissions, errors,
  recovery behavior, and outcomes are specified where necessary;
- Acceptance Criteria are sufficient to verify required behavior;
- relevant cross-cutting Requirements are consolidated where doing so improves
  review, consistency, or reuse;
- Roles and Permissions are internally consistent;
- System Messages correspond to defined product behavior;
- Notifications have sufficient definition where applicable;
- applicable NFRs have been specified or material unresolved NFR decisions are
  explicitly recorded;
- terminology is consistent;
- Requirements are consistent with validated Behavior and Interaction;
- no known in-scope behavior has disappeared during specification;
- technical implementation decisions have not been introduced unnecessarily;
- material upstream gaps are resolved or explicitly recorded;
- actual Consultant Review has occurred;
- required refinement has been completed;
- the Consultant determines that the Requirements Document is sufficiently
  complete for downstream Solutions work.

---

## Failure Conditions

The Requirements Stage has failed when the resulting specification materially:

- invents product behavior not established upstream;
- loses known in-scope behavior;
- contradicts validated Behavior;
- contradicts validated Interaction without explicitly resolving the conflict;
- leaves implementation-dependent product decisions ambiguous;
- contains Acceptance Criteria that cannot meaningfully verify required
  behavior;
- treats a generic template as more authoritative than the product model;
- duplicates information so extensively that consistency becomes unreliable;
- converts incidental Interaction details into unnecessary mandatory behavior;
- introduces technical implementation decisions without an established
  constraint requiring them;
- hides unresolved product decisions behind assumptions;
- becomes a test-case catalogue instead of a product specification;
- becomes a technical Solution instead of Requirements.

---

## Stage Boundaries

### Requirements vs Behavior

Behavior defines:

> How does the product behave?

Requirements define:

> What exactly must the product do, under what conditions, so that its behavior
> can be implemented and verified?

Requirements make validated Behavior precise.

They do not independently redefine it.

### Requirements vs Interaction

Interaction defines:

> How is important product behavior represented so that users can understand
> and interact with it?

Requirements define the exact expected behavior and constraints behind that
interaction.

Interaction provides validated visual and interaction context.

Requirements do not turn Interaction into a complete UI specification.

### Requirements vs Design

Requirements define expected product behavior and constraints.

Design defines the complete UX/UI required to represent that behavior.

Requirements may constrain Design where product behavior requires it.

They should not make detailed visual design decisions unnecessarily.

### Requirements vs Solutions

Requirements define:

> What must be true of the product?

Solutions define:

> How should the product be technically implemented?

Requirements may establish product-visible data, constraints, validation,
relationships, and observable outcomes.

Solutions establish technical architecture, data storage, APIs, infrastructure,
services, technologies, and implementation mechanisms.