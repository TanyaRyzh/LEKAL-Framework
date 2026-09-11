# LEKAL 3 — Structure

## Goal

Transform the validated **Shape v2 Document** into a coherent functional structure of the product.

The consultant decomposes the validated product hypothesis into Functional Areas, capabilities, key Functional Flows, structurally relevant rules, data and states, and connections between parts of the product.

The **Structure Stage** describes how the product works as a connected functional system.

It operates above detailed requirements and below product-level scope.

---

## Objective

Create a validated functional structure that defines:

- the complete end-to-end Product Flow;
- meaningful Functional Areas;
- user-visible capabilities within those areas;
- key Functional Flows between actors and the system;
- key rules, data constraints, states and decisions where they materially define the structure;
- connections and dependencies between Functional Areas;
- explicit assumptions and open questions;
- traceability from validated MVP scope to the resulting Structure.

The resulting **Structure Document** should provide a stable functional basis for the **Requirements Stage**.

---

## Input

Primary input:

**Shape v2 Document**

The **Shape v2 Document** must already contain the validated product hypothesis.

Additional inputs may include:

- findings from Shape validation;
- client materials;
- supporting project information;
- other evidence required to understand the validated product behavior.

Do not use an unvalidated **Shape v1 Document** as the validated basis for the **Structure Stage**.

Do not restart product framing or redefine the validated product hypothesis unless a contradiction or structural problem requires returning a decision for validation.

---

## Core Structure Principle

The primary decomposition model is:

**Product Flow → Functional Areas → Capabilities → Functional Flows**

The decomposition should be driven by how users move through the product and how the product supports their jobs.

Do not begin decomposition from:

- screens;
- pages;
- database entities;
- APIs;
- services;
- technical components;
- implementation architecture.

A Functional Area represents a meaningful functional responsibility within the product.

A capability represents a meaningful ability or outcome available to an actor.

A Functional Flow describes how an actor and the system interact to achieve a meaningful result.

The Structure must contain enough detail to expose:

- missing capabilities;
- missing transitions;
- unclear responsibilities;
- important states;
- structurally significant rules;
- broken recovery paths;
- gaps between Functional Areas.

The **Structure Stage** must not expand into exhaustive behavioral requirements or technical implementation.

---

## Focus Areas

### 1. High-Level Product Flow

Describe the complete end-to-end functional flow of the validated product.

The flow should show:

- where the user job begins;
- the major user actions;
- major system responses and transitions;
- participating actors;
- the primary successful path;
- important negative or unresolved states;
- required recovery paths;
- the meaningful product outcome.

The High-Level Product Flow is the backbone of the Structure.

It is not a detailed use case.

Do not stop the flow merely because:

- a failure was recorded;
- an issue was created;
- a participant was notified;
- information became visible;
- another participant became able to act.

If the validated Job to Be Done requires resolution, acceptance, completion, confirmation, delivery or another meaningful final state, the functional structure must support reaching that state.

---

### 2. Functional Areas

Divide the product into meaningful Functional Areas.

Each Functional Area should:

- own a coherent functional responsibility;
- contain related capabilities;
- support a meaningful part of the Product Flow;
- have understandable boundaries;
- connect to other Functional Areas where required.

Functional Areas should be derived from product behavior.

Do not automatically create a Functional Area for every:

- feature;
- screen;
- entity;
- integration;
- technical component;
- cross-cutting concern.

If one Functional Area becomes so broad that its capabilities represent several materially different responsibilities or user flows, consider whether it should be decomposed further.

---

### 3. Capabilities

For each Functional Area, identify the meaningful capabilities available to its actors.

Prefer actor-oriented capability statements.

For example:

- User can create a project.
- User can edit own project.
- User can invite a project member.
- Client can execute an acceptance scenario.
- Vendor can return a failed scenario for retest.

Capabilities should be sufficiently decomposed to reveal the actual functional structure.

Avoid capabilities that are so broad that they hide several materially different user actions or flows.

Also avoid decomposing capabilities into individual UI controls or low-level implementation operations.

---

### 4. Functional Flows

Develop Functional Flows for significant capabilities or connected groups of capabilities.

A Functional Flow should normally show:

1. what triggers the flow;
2. the actor;
3. the actor action;
4. the system response;
5. structurally relevant validation or decision;
6. subsequent action or transition;
7. meaningful result.

Include important alternative, negative and recovery paths where they affect the functional structure.

A Functional Flow may support several closely related capabilities.

Not every capability requires a completely independent flow.

Do not stop a Functional Flow at an intermediate state when further product behavior is required to reach the validated user outcome.

---

### 5. Key Rules, Data and States

Capture rules, data constraints, states and decisions when they materially affect the functional structure or Functional Flows.

Examples may include:

- ownership;
- permissions;
- uniqueness;
- structurally important limits;
- required relationships;
- meaningful object states;
- state transitions;
- conditions required to continue a flow;
- conditions required to complete a process.

Include only what is necessary to understand how the functional structure works.

Do not attempt to define:

- every field validation;
- every error message;
- every edge case;
- exhaustive business rules;
- complete state machines;
- technical data models.

Those details belong primarily to the **Requirements Stage** or **Solutions Stage**.

---

### 6. Connections Between Functional Areas

Functional Areas must form one connected product.

For each important connection, determine:

- what information, state or result moves between areas;
- what event or action causes the transition;
- which Functional Area owns the responsibility before the transition;
- which Functional Area owns it after the transition;
- what state or condition is required for the transition;
- where recovery paths reconnect to the primary Product Flow.

Do not allow functionality to disappear between Functional Areas.

Outputs from one area that are required by another must have a clear connection.

---

### 7. Validated Scope Coverage

The **Structure Stage** must preserve the validated MVP scope from the **Shape v2 Document**.

Before the Structure can pass consistency review, verify every validated MVP capability from the **Shape v2 Document** against the proposed Structure.

For every validated MVP capability, identify:

- the Functional Area that owns it;
- the capability or Functional Flow that represents it;
- whether it is fully represented;
- whether it has been intentionally transformed into a broader Structure capability;
- whether a gap remains.

A validated MVP capability must not disappear during structural decomposition.

If several Shape capabilities are combined into one broader Structure capability, their relationship must remain traceable.

If decomposition reveals that a validated MVP capability should be removed, materially changed or moved outside MVP, do not silently change the validated scope.

Make the proposed scope change explicit and return it for validation.

Do not conclude that MVP coverage is complete from the overall Product Flow or Functional Area list alone.

Verify coverage capability by capability.

---

### 8. Assumptions and Open Questions

Capture structural uncertainty explicitly.

When an uncertainty is discovered:

- determine whether it can be resolved through available information or analysis;
- resolve it where possible;
- retain unresolved client-specific or decision-dependent uncertainty as an assumption or open question.

Do not present unresolved assumptions as confirmed product behavior.

Structural uncertainty should not prevent useful decomposition where reasonable hypotheses can support continued work.

---

## Process

### Step 1 — Review the Validated Shape

Review the **Shape v2 Document**.

Identify:

- primary users and actors;
- Jobs to Be Done;
- Value Proposition;
- validated MVP scope;
- complete value loop;
- important negative and recovery paths;
- constraints;
- assumptions;
- open questions.

Create an explicit inventory of the validated MVP capabilities that must remain traceable through Structure.

Do not restart the **Shape Stage**.

---

### Step 2 — Build the High-Level Product Flow

Translate the validated product hypothesis into a complete functional flow.

Identify:

- starting condition;
- actors;
- major actions;
- major system transitions;
- successful path;
- important negative states;
- recovery paths;
- meaningful final outcome.

Verify that the flow reaches the outcome promised by the relevant Jobs to Be Done.

Do not stop at an intermediate state merely because another participant can continue manually.

---

### Step 3 — Identify Functional Areas

Group product responsibilities into meaningful Functional Areas.

For each Functional Area, determine:

- its purpose;
- the part of the Product Flow it supports;
- its actors;
- what responsibility it owns;
- what responsibility belongs elsewhere.

Do not create Functional Areas directly from screens or technical architecture.

Review broad Functional Areas and determine whether they hide several materially different responsibilities or user flows that should be separated.

---

### Step 4 — Identify Capabilities

Within each Functional Area:

1. identify the actors;
2. identify what each actor must be able to do;
3. express those abilities as meaningful capabilities;
4. check whether the capabilities are sufficient to support the relevant part of the Product Flow;
5. decompose capabilities that are too broad;
6. combine capabilities that are unnecessarily granular.

Compare the resulting capabilities against the validated MVP capability inventory.

Do not allow validated MVP behavior to disappear because it was absorbed into an overly broad capability.

---

### Step 5 — Develop Functional Flows

For each significant capability or connected group of capabilities:

1. identify the trigger;
2. identify the actor;
3. describe the actor action;
4. describe the system response;
5. include structurally relevant validations or decisions;
6. continue through subsequent actions or transitions;
7. reach a meaningful result;
8. include important negative and recovery paths.

Use Functional Flows to discover:

- missing capabilities;
- missing states;
- missing transitions;
- unclear responsibilities;
- gaps between Functional Areas.

---

### Step 6 — Capture Key Rules, Data and States

For each Functional Area and Functional Flow, determine whether understanding the structure requires explicit:

- rules;
- data constraints;
- ownership;
- permissions;
- limits;
- states;
- transitions;
- completion conditions.

Capture only structurally relevant information.

Defer detailed behavioral specification to the **Requirements Stage**.

---

### Step 7 — Connect Functional Areas

Review the product across Functional Area boundaries.

Verify that:

- outputs from one area become valid inputs to the next;
- ownership is clear;
- important state is preserved;
- no part of the Product Flow disappears between areas;
- negative and recovery paths reconnect correctly;
- completion depends on the correct upstream states.

---

### Step 8 — Verify Validated Scope Coverage

Create a capability-level mapping from the validated MVP scope in the **Shape v2 Document** to the proposed Structure.

For every validated MVP capability, record:

- its Functional Area;
- its Structure capability or Functional Flow;
- its coverage status.

Use:

- `Covered`
- `Transformed`
- `Gap`

`Covered` means the validated capability is explicitly represented.

`Transformed` means the validated capability is represented through a broader or differently structured capability without losing the original product behavior.

`Gap` means the validated capability is not adequately represented.

Every `Transformed` item must remain traceable to its original validated behavior.

Every `Gap` must be resolved or explicitly returned for validation.

Do not mark validated scope coverage as complete while unresolved gaps remain.

---

### Step 9 — Structure Consistency Review

Review the proposed Structure as one connected product model.

Check:

#### Product Flow

- Does the Structure support the complete High-Level Product Flow?
- Can each primary Job to Be Done reach its meaningful outcome?
- Are important negative and recovery paths complete?

#### Validated Scope Coverage

- Has every validated MVP capability from the **Shape v2 Document** been checked individually?
- Is every validated MVP capability represented in a Functional Area?
- Is each capability traceable to a Structure capability or Functional Flow?
- Have transformed capabilities preserved the validated behavior?
- Are any validated capabilities missing?
- Have any scope changes been made without explicit validation?

#### Functional Coverage

- Are capabilities sufficiently decomposed?
- Are any capabilities unnecessarily broad?
- Are any capabilities duplicated?
- Does each capability belong to an appropriate Functional Area?

#### Functional Area Boundaries

- Are responsibilities clear?
- Are Functional Areas coherent?
- Are any Functional Areas hiding several materially different responsibilities?
- Are there overlaps?
- Are cross-area dependencies understandable?

#### Shape Alignment

- Does the Structure support the primary Jobs to Be Done?
- Does the Structure support the Value Proposition?
- Has validated MVP scope been preserved?
- Has functionality been added beyond the validated Shape without justification?

#### Structure / Requirements Boundary

- Has the Structure captured enough behavior to understand the functional mechanisms?
- Has it avoided exhaustive behavioral specification?
- Are detailed validations, error behavior and edge cases appropriately deferred?

#### Structure / Solutions Boundary

- Has the Structure avoided premature technical implementation?
- Are technical assumptions included only where they materially affect functional Structure?

Resolve discovered structural gaps where possible.

If resolving a gap requires changing validated product scope, surface it for validation instead of silently changing the product.

---

### Step 10 — Visualize the Structure

Transfer the proposed Structure into a visual representation suitable for review.

The visualization should make it possible to inspect:

- Functional Areas;
- capabilities;
- key Functional Flows;
- important rules, states and decisions;
- connections;
- negative and recovery paths.

The exact visual layout and notation are flexible.

The visual representation may organize information differently from the **Structure Document** where that improves readability, but it must preserve the same functional meaning.

---

## External Validation Boundary

The proposed **Structure Document** and its visual representation must be reviewed with the client or relevant decision-makers before the **Structure Stage** can be completed.

External validation should confirm or correct:

- High-Level Product Flow;
- Functional Areas;
- capabilities;
- Functional Flows;
- responsibilities;
- boundaries;
- structurally important rules and states;
- cross-area connections;
- assumptions;
- open questions;
- any proposed changes to validated MVP scope.

External validation is a real consulting activity.

It must not be replaced by internal analysis.

---

### Step 11 — Validate the Structure

Walk through the proposed Structure with the client or relevant decision-makers.

Review:

1. the complete Product Flow;
2. Functional Areas;
3. capabilities;
4. Functional Flows;
5. important negative and recovery paths;
6. key rules and states;
7. Functional Area responsibilities and boundaries;
8. cross-area connections;
9. assumptions and open questions;
10. any proposed scope changes discovered during decomposition.

Capture:

- confirmed structure;
- corrections;
- decisions;
- rejected assumptions;
- new information;
- required changes.

---

### Step 12 — Finalize the Structure Document

Incorporate validation feedback into the **Structure Document**.

Update all affected:

- Functional Areas;
- capabilities;
- Functional Flows;
- rules;
- data constraints;
- states;
- connections;
- assumptions;
- open questions;
- validated scope coverage.

Repeat the Structure Consistency Review after material changes.

The validated **Structure Document** becomes the primary input to the **Requirements Stage**.

---

## Output

Use the Structure template to create the **Structure Document**.

The **Structure Document** contains:

- High-Level Product Flow;
- Functional Areas;
- actors;
- capabilities;
- key Functional Flows;
- structurally relevant rules, data and states;
- connections and boundaries;
- validated MVP scope coverage;
- assumptions and open questions;
- validation findings;
- changes after validation;
- validation status.

Before external validation, the **Structure Document** represents the proposed functional structure.

After external validation and incorporation of feedback, it represents the validated functional structure and may be used as input to the **Requirements Stage**.

---

## Success Criteria

The **Structure Stage** is successful when:

- the validated **Shape v2 Document** has been transformed into a coherent functional Structure;
- the complete end-to-end Product Flow is represented;
- the primary successful path reaches a meaningful product outcome;
- important negative and recovery paths are represented;
- meaningful Functional Areas have been identified;
- Functional Area responsibilities and boundaries are understandable;
- relevant actors are identified;
- capabilities are sufficiently decomposed to expose the functional structure;
- key Functional Flows describe meaningful actor/system interaction;
- structurally important rules, data constraints and states are represented where necessary;
- connections between Functional Areas are clear;
- every validated MVP capability from the **Shape v2 Document** is traceable to the Structure;
- no validated MVP capability has been silently omitted during decomposition;
- every transformed validated capability remains traceable to its original behavior;
- no unresolved validated-scope gap remains hidden by the overall Product Flow or Functional Area structure;
- each primary Job to Be Done can reach its meaningful outcome;
- the Structure supports the validated Value Proposition;
- MVP scope has not been expanded unnecessarily;
- detailed requirements have not been prematurely specified;
- technical implementation has not been prematurely designed;
- material assumptions and open questions are explicit;
- external validation has been performed;
- validation feedback has been incorporated;
- no Failure Condition remains unresolved.

---

## Failure Conditions

The **Structure Stage** must not be considered complete if:

- an unvalidated **Shape v1 Document** was used as the validated basis;
- the High-Level Product Flow is incomplete;
- a primary Job to Be Done cannot reach its meaningful outcome;
- an important negative or recovery path required for the same job is missing;
- Functional Areas are primarily derived from screens or technical components;
- Functional Area responsibilities are unclear or materially overlapping;
- capabilities required to understand product behavior are missing;
- capabilities are so broad that materially different user actions or flows remain hidden;
- Functional Flows stop at intermediate states before the validated user outcome can be reached;
- connections between Functional Areas contain functional gaps;
- structurally important rules, states, ownership or transitions are missing;
- one or more validated MVP capabilities are missing from the Structure without an explicit validated scope change;
- validated scope coverage is claimed without capability-level traceability to the **Shape v2 Document**;
- a `Gap` in validated MVP coverage remains unresolved and is not explicitly returned for validation;
- a `Transformed` capability cannot be traced back to the validated product behavior it represents;
- validated scope has been silently removed or materially changed during decomposition;
- unsupported functionality has been added without justification;
- the Structure expands into exhaustive detailed requirements;
- technical implementation is prematurely designed;
- assumptions are presented as confirmed facts;
- required external validation has not occurred;
- validation feedback has not been incorporated into the final **Structure Document**.