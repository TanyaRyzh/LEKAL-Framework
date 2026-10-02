# LEKAL 3 — Structure

## Goal

Transform the validated product direction into a complete functional decomposition of the product.

The **Structure Stage** answers:

> What functional capabilities does this product contain?

The result is a functional Work Breakdown Structure:

```text
Product
└── Functional Area
    └── Capability
```

Structure establishes the relevant product feature space before detailed behavioral analysis begins.

It identifies:

- coherent Functional Areas;
- meaningful Capabilities;
- current product scope;
- intentionally excluded functionality that is relevant to the product feature space;
- relative functional importance;
- preliminary relative size.

The Structure Stage does not define in detail how functionality behaves.

Detailed behavioral analysis belongs to the **Behavior Stage**.

---

# Objective

Create a functional decomposition broad and complete enough that later Stages do not need to rediscover basic product functionality.

The Structure Stage should:

- identify coherent Functional Areas;
- identify meaningful Capabilities within each Functional Area;
- preserve validated functionality from the current authoritative Shape;
- discover functionality implied by validated product context;
- represent relevant current and intentionally excluded functionality;
- distinguish Scope from functional Priority;
- assign preliminary relative Size;
- identify important structural gaps;
- preserve Open Questions that may materially change the functional Structure;
- verify that the resulting Structure supports the validated product value loop.

The Structure Stage should not define:

- detailed Actor/System flows;
- detailed business rules;
- exhaustive validations;
- field-level requirements;
- detailed state behavior;
- UI behavior;
- screen structure;
- technical implementation.

These belong to later Stages.

---

# Input

The primary input is the current authoritative **Shape**.

The current Shape represents validated product direction and scope.

Supporting upstream materials may also be used when relevant, including:

- **Idea Document**;
- **Domain artifacts**;
- validation findings;
- research produced during earlier Stages;
- explicit upstream scope decisions;
- other authoritative pre-Structure project materials.

The current authoritative Shape is the starting point for functional decomposition.

It is not assumed to contain a complete list of product functionality.

Earlier upstream artifacts provide context but must not silently override later validated product decisions.

Downstream artifacts must not be used to construct Structure.

---

# Output

The output of the Structure Stage is a functional WBS:

```text
Product
└── Functional Area
    └── Capability
```

Each Capability is described through:

```text
ID
Functional Area
Capability
Description
Scope
Priority
Preliminary Size
```

The Structure artifact should primarily contain the functional model.

Analytical controls used to produce the Structure do not need to be reproduced as separate reports.

Only material Structural Gaps and Open Questions need to be preserved alongside the WBS.

---

# Core Functional Model

## Functional Areas

A **Functional Area** represents a coherent product responsibility.

Examples:

```text
Account & Access
Project Management
Team Management
Guest Access
UAT Preparation
UAT Execution
Feedback
```

Functional Areas should not be based primarily on:

- screens;
- pages;
- database entities;
- APIs;
- services;
- technical components.

A Functional Area describes a meaningful functional responsibility of the product.

Functional Areas should be broad enough to group related functionality but specific enough to preserve meaningful product responsibilities.

---

## Capabilities

A **Capability** represents a meaningful functional ability provided by the product.

Examples:

```text
Account Registration
Password Recovery
Project Creation
Member Invitation
Guest Access Revocation
Scenario Execution
Feedback Classification
Language Selection
```

Capabilities should represent meaningful functional intentions rather than UI actions or technical operations.

Avoid overly broad Capabilities such as:

```text
Manage Projects
Manage Users
Handle UAT
```

when they hide materially different functional intentions.

Also avoid trivial decomposition such as:

```text
Click Save
Open Modal
Close Popup
Press Back
```

The goal is functional decomposition.

---

# Capability Granularity

A Capability should be sufficiently narrow to remain a useful functional unit for later behavioral analysis.

Split a Capability when it contains materially different functional intentions that may have different:

- Scope;
- Priority;
- lifecycle;
- relative Size;
- behavioral responsibility.

For example:

```text
Password Recovery
Password Change
```

may be preferable to:

```text
Password Management
```

when the two functions represent independent product capabilities.

Likewise:

```text
Journey Creation
Journey Editing
Journey Archiving
```

may be preferable to:

```text
Journey Management
```

when those lifecycle operations represent meaningful product decisions.

However, do not mechanically decompose every object into CRUD operations.

A separate Capability requires product-specific functional meaning.

---

# Feature Space

Structure represents more than the list of functionality currently being built.

It represents the **relevant product feature space**.

This may include:

- functionality currently included in product scope;
- functionality explicitly considered and excluded;
- meaningful alternatives that were rejected;
- functionality deliberately deferred;
- nearby functional alternatives whose exclusion is important to preserve.

This allows Structure to distinguish:

> We forgot this functionality.

from:

> We considered this functionality and intentionally excluded it.

The feature space must remain product-specific.

Structure is not an unlimited backlog of everything the product could theoretically contain.

---

# Scope

Every Capability has an explicit Scope:

```text
IN
OUT
```

## IN

`IN` means the Capability belongs to the current product scope.

It does not mean the Capability is fully specified or technically designed.

---

## OUT

`OUT` means the Capability belongs to the relevant product feature space but is intentionally excluded from the current product scope.

An OUT Capability may represent:

- an explicitly rejected option;
- deferred functionality;
- a meaningful alternative to an IN Capability;
- a product decision whose exclusion should remain visible.

OUT functionality remains inside its natural Functional Area.

Do not create separate functional areas based on Scope.

For example:

```text
Account & Access

Account Registration              IN
Google Registration / Login       OUT
Apple Registration / Login        OUT
```

Scope and Functional Area describe different dimensions.

---

# Scope Discipline

Functional Discovery does not mean adding generic product functionality.

Do not add a Capability merely because:

- similar products have it;
- it is common SaaS functionality;
- it appears on a generic product-readiness checklist;
- a competitor supports it;
- it is technically possible;
- it might be useful someday.

Every Capability must have a product-specific reason to belong to the relevant feature space.

A Capability may be justified by:

- validated product behavior;
- validated Target Market;
- validated Constraint;
- actor responsibility;
- functional object lifecycle;
- continuation;
- recovery;
- value loop;
- product-readiness concern;
- another justified Capability;
- an explicitly considered product alternative.

If the rationale cannot be explained, the Capability should not be silently added.

---

# Functional Priority

Every Capability receives a functional Priority:

```text
High
Medium
Low
```

Priority describes the relative functional importance of the Capability within the product.

Priority does not define Scope.

These are independent dimensions.

An OUT Capability may still have High or Medium functional importance while being intentionally excluded from the current product scope.

---

## High

A Capability is **High** priority when it is central or important to intended product operation.

Typical reasons include:

- directly supports a primary JTBD;
- directly supports the validated value loop;
- enables an important actor responsibility;
- is necessary to start or continue core product work;
- supports a critical negative or recovery path;
- another important Capability cannot operate coherently without it.

Removing a High Capability would materially damage intended product operation or value delivery.

---

## Medium

A Capability is **Medium** priority when it provides meaningful product functionality but is not central to the primary value loop.

Its absence may:

- create noticeable friction;
- limit collaboration;
- reduce usability;
- make some product situations inconvenient;
- remove useful supporting behavior;

without fundamentally preventing the primary product outcome.

---

## Low

A Capability is **Low** priority when it is secondary, supporting, convenience-oriented or reasonably deferrable.

Its absence does not materially prevent the primary product outcome.

Low does not mean unnecessary.

It means the Capability has lower relative functional importance than High or Medium functionality.

---

## Priority Principle

Priority must be based on product-specific functional reasoning.

Consider:

- primary JTBD;
- Value Proposition;
- validated value loop;
- actor responsibilities;
- lifecycle continuity;
- recovery;
- functional dependencies;
- product constraints;
- consequence of omission.

Do not assign Priority merely because a Capability is common in similar products.

Do not infer Priority mechanically from Scope.

---

# Preliminary Size

Every Capability receives a preliminary relative Size:

```text
XS
S
M
L
XL
```

Preliminary Size describes the apparent relative functional size and complexity of a Capability at the Structure Stage.

It is not:

- an implementation estimate;
- hours;
- days;
- story points;
- cost;
- delivery commitment.

Approximate interpretation:

```text
XS — trivial functional scope

S — small and relatively isolated Capability

M — moderate Capability with meaningful behavior or several conditions

L — substantial Capability involving multiple behaviors, states,
    responsibilities, relationships or recovery

XL — very large Capability with substantial functional complexity
     or a strong indication that further decomposition may be needed
```

Preliminary Size is intentionally rough.

Later Stages may reveal substantially different complexity.

Technical architecture must not be invented merely to assign Size.

An `XL` Capability should trigger a decomposition check:

> Is this truly one Capability, or are multiple meaningful functional intentions still hidden inside it?

---

# Functional Discovery

The authoritative Shape defines validated product direction.

It does not necessarily enumerate every Capability required for the product to operate coherently.

The Structure Stage must therefore perform **Functional Discovery**.

The core principle is:

> Shape is the starting point for functional decomposition, not the complete functional model.

For each Functional Area, analyze what functionality must surround validated product behavior so that actors can actually perform meaningful work.

Functional Discovery should use multiple analytical lenses.

---

# Actor Lens

For each actor, ask:

- What must this actor be able to start?
- What must this actor be able to access?
- What must this actor be able to continue?
- What must this actor be able to see?
- What must this actor be able to change?
- What responsibilities does this actor own?
- What happens when responsibility passes to another actor?

The Actor Lens is an analytical control.

Actors do not need to be persisted as a dedicated Structure field.

---

# Functional Object Lens

For important functional objects, ask:

- How is the object created or introduced?
- How is it found later?
- How is it opened or accessed?
- Can it change?
- Can it stop being active?
- Can it be removed, revoked or archived where relevant?
- Who is responsible for those actions?
- What other functionality depends on it?

These questions are analytical prompts.

They are not a mandatory CRUD checklist.

Do not add operations that have no product-specific reason to exist.

---

# Lifecycle Lens

For important product work and functional objects, ask:

```text
How does it begin?
↓
How does it continue?
↓
How does it change?
↓
How does it end or stop being active?
↓
How does it reach a meaningful outcome?
```

Identify Capabilities required at important lifecycle transitions.

Do not define detailed state machines during Structure.

---

# Continuation Lens

Products must support not only starting work but returning to it.

Ask:

- How does the actor find existing work?
- How does the actor reopen or access it?
- How does the actor understand that work already exists?
- How does the actor continue from where work stopped?

This is especially important for persistent objects and multi-session workflows.

---

# Recovery Lens

For important negative outcomes, ask:

- What happens when the normal path fails?
- Does the actor still need to reach the original outcome?
- What functional Capability enables recovery?
- Does another actor need to intervene?
- Can the process return to the primary value loop?

Do not stop functional decomposition at failure visibility when the validated product outcome requires recovery.

Detailed recovery behavior belongs to Behavior.

---

# Value Loop Lens

Review the complete validated product value loop.

Ask:

- Can every meaningful step actually happen?
- Can responsibility move between actors?
- Can actors return to unfinished work?
- Can important negative paths recover?
- Can the product reach the validated final outcome?

A functional decomposition is incomplete if the value loop stops before the meaningful outcome established upstream.

---

# Product Readiness Lens

Core product flows do not necessarily reveal all functional mechanisms required for a real product to operate in its validated context.

Review whether the product context creates cross-cutting functional responsibilities.

Relevant concerns may include, where applicable:

- privacy and consent;
- account lifecycle;
- personal-data lifecycle;
- localization;
- legal or regulatory interaction;
- product limits or quotas;
- user preferences;
- support;
- other cross-cutting responsibilities implied by the validated context.

For each relevant concern, ask:

1. Does the validated product context make this concern relevant?
2. Does addressing it require an actor to perform or control something through the product?
3. Does the product require a functional mechanism to support that responsibility?
4. Is that mechanism already represented by an existing Capability?
5. If not, does it justify an additional Capability?

Product Readiness is not a generic SaaS checklist.

Only product-specific functional responsibilities belong in Structure.

---

# Structural Dependencies

Consider functional dependencies when they materially affect:

- completeness;
- Priority;
- actor ability to continue work;
- the product value loop.

For example:

```text
Invite Member
↓
Member gains project access
↓
Member can participate in project work
```

Dependencies are primarily an analytical control.

They do not need to be persisted as a dedicated Structure field.

Do not model technical dependencies during Structure.

Technical dependencies include:

- API calls;
- databases;
- queues;
- storage;
- authentication providers;
- infrastructure components.

These belong to later Stages.

---

# Validated Scope Coverage

Before Structure is considered complete, verify that functionality established by the authoritative Shape has not disappeared.

For each validated functional element, determine whether it is:

```text
Covered
Transformed
Gap
```

## Covered

The validated functionality has a clear representation in Structure.

## Transformed

The validated functionality has been legitimately decomposed or represented differently.

## Gap

Validated functionality has no adequate representation.

Validated Scope Coverage is an analytical control.

A complete coverage matrix does not need to be part of the Structure artifact.

Material Gaps must be resolved or explicitly preserved.

---

# Functional Completeness

Validated Scope Coverage and Functional Completeness are different checks.

Validated Scope Coverage asks:

> Did we lose anything that was already validated?

Functional Completeness asks:

> Did we discover the surrounding functionality required for the validated product to operate coherently?

A Structure may have perfect Validated Scope Coverage and still be functionally incomplete.

For each Functional Area, review:

- actors;
- start of work;
- access;
- return to existing work;
- functional object lifecycle;
- management responsibilities;
- continuation;
- important negative paths;
- recovery;
- connections to the rest of the value loop.

At product level, additionally review cross-cutting Product Readiness responsibilities.

---

# Structural Uncertainty

Not every uncertainty needs to be solved during Structure.

If the functional need is clear but detailed behavior is unknown:

> Include the Capability and defer behavioral analysis to Behavior.

If the existence of the Capability itself is plausible but insufficiently established:

> Preserve it as an Open Question rather than silently treating it as product truth.

If a decision materially changes validated product direction or scope:

> Make the uncertainty explicit rather than silently changing the product.

If only detailed behavior is unknown:

> Do not solve it during Structure merely because the question has been discovered.

---

# Structural Gaps

A **Structural Gap** exists when functionality required by validated product truth or functional coherence has no adequate representation in Structure.

Examples may include:

- validated functionality disappeared during decomposition;
- an actor cannot continue required work;
- an important lifecycle has no functional continuation;
- a necessary recovery mechanism is absent;
- the validated value loop cannot reach its intended outcome.

Structural Gaps should be explicit.

Do not hide them by inventing product decisions.

---

# Analysis vs Artifact Content

The analysis performed during Structure is broader than the information persisted in the Structure artifact.

Relevant analytical controls include:

- Validated Scope Coverage;
- Functional Discovery;
- Product Readiness;
- Functional Completeness;
- dependency analysis;
- JTBD support review;
- Value Proposition support review;
- value-loop review.

These controls exist to improve the quality of the functional model.

They are not separate deliverables by default.

The Structure artifact should primarily contain:

- Functional Areas;
- Capabilities;
- concise Descriptions;
- Scope;
- Priority;
- Preliminary Size;
- material Structural Gaps;
- material Open Questions.

Do not turn Structure into a report describing every analytical step performed.

---

# Stage Boundary

Structure answers:

> What functional capabilities does this product contain?

Behavior answers:

> How does this product behave?

Requirements answer:

> What exactly must the product do?

Solutions answer:

> How will this product be technically implemented?

Structure must therefore stop before detailed behavioral specification.

Do not define:

- detailed actor/system sequences;
- complete states and transitions;
- exhaustive rules;
- exact validation behavior;
- detailed data rules;
- UI interactions;
- screen layouts;
- technical architecture.

A Capability may imply that behavior exists.

Structure does not need to define that behavior.

---

# Structure Lifecycle

The initial Structure is produced as **Structure v1**.

Structure v1 is a proposal.

It may deliberately be broader than the final Structure in order to expose relevant functional possibilities for Consultant Review.

The Consultant then reviews and refines Structure v1.

The Consultant may:

- accept or reject Capabilities;
- add missing Capabilities;
- remove unnecessary Capabilities;
- change Scope;
- change Priority;
- change Preliminary Size;
- merge or split Capabilities;
- rename Capabilities;
- move Capabilities between Functional Areas;
- merge or split Functional Areas;
- resolve Open Questions;
- correct Structural Gaps.

Independent review may challenge the working artifact during Consultant refinement.

Reviewer findings are advisory.

The Consultant decides which findings to:

- accept;
- reject;
- defer;
- treat as upstream issues.

The Consultant incorporates accepted findings and completes **Structure v2**.

Structure v2 is the authoritative Structure input to the **Behavior Stage**.

There is no separate Structure validation checkpoint and no automatic Structure v3.
Independent review does not create or approve a Structure version.

---

# Success Criteria

The Structure Stage succeeds when:

- the product is decomposed into coherent Functional Areas;
- Functional Areas contain meaningful Capabilities;
- decomposition is sufficiently deep for Behavior;
- validated Shape functionality remains represented;
- relevant IN functionality is explicit;
- relevant intentionally excluded functionality is explicit where useful;
- Scope is distinct from Priority;
- Priority reflects product-specific functional importance;
- Preliminary Size provides useful relative structural information;
- Functional Discovery has been performed;
- Product Readiness has been considered;
- important implied functionality has been identified;
- Derived functionality has product-specific justification;
- important lifecycle and continuation needs are functionally represented;
- important recovery needs are functionally represented;
- primary JTBD are functionally supported;
- the validated value loop is functionally supported;
- material implications of Target Market and Constraints are represented;
- Structural Gaps are explicit;
- Open Questions that may change Structure are explicit;
- the Structure artifact contains the functional model rather than an unnecessary analytical report;
- detailed behavior has not been prematurely specified;
- Structure v2 is sufficiently complete for Behavior to proceed without rediscovering basic product functionality.

---

# Failure Conditions

The Structure Stage fails when:

- Structure merely transcribes Shape;
- Shape wording is assumed to be the complete functional model;
- validated functionality disappears during decomposition;
- obvious implied functionality is omitted;
- material cross-cutting functional responsibilities are omitted;
- generic SaaS functionality is added without product-specific justification;
- Product Readiness is treated as a mandatory feature checklist;
- speculative functionality turns Structure into an unlimited backlog;
- OUT functionality is separated from its natural Functional Area merely because it is OUT;
- Scope and Priority are treated as the same concept;
- Functional Areas are based primarily on screens or technical components;
- broad Capabilities hide materially different functional intentions;
- Capabilities are decomposed into trivial UI actions;
- CRUD operations are added mechanically without product-specific meaning;
- Priority is based on convention rather than product need;
- Preliminary Size is presented as a delivery estimate;
- technical architecture is invented to estimate Size;
- `XL` Capabilities hide obvious functional decomposition;
- important functional dependencies are ignored;
- Validated Scope Coverage is confused with Functional Completeness;
- the value loop stops before its validated meaningful outcome;
- detailed Actor/System flows are produced during Structure;
- detailed Requirements are produced during Structure;
- UI design is produced during Structure;
- technical architecture is produced during Structure;
- internal analytical checks are unnecessarily reproduced as large reports;
- agent output is treated as Consultant-reviewed without actual Consultant Review;
- Reviewer findings are treated as automatic product truth;
- the final Structure remains so shallow that Behavior must rediscover basic product functionality.