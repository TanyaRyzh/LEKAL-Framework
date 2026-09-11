# LEKAL 3 — Structure

## Goal

Transform the validated **Shape v2 Document** into a complete functional decomposition of the product.

The **Structure Stage** determines what functional capabilities must exist for the validated product scope to work as a coherent product.

The Stage does not describe detailed behavior of those capabilities.

Instead, it builds a functional Work Breakdown Structure (WBS):

**Product → Functional Areas → Capability Groups → Capabilities**

The Structure should go beyond simply reorganizing capabilities explicitly named in the **Shape v2 Document**.

It should actively discover capabilities that are implied by:

- validated product behavior;
- actor responsibilities;
- functional object lifecycles;
- continuation of user work;
- management of existing work;
- important negative and recovery paths;
- dependencies between parts of the product.

The result of the agent's analysis is the **Structure v1 Document**.

The consultant then reviews the proposed Structure, removes unnecessary functionality, corrects decomposition, adds missing capabilities, adjusts priorities, and produces the **Structure v2 Document**.

The **Structure v2 Document** becomes the input to the **Concepts Stage**.

---

## Objective

Produce a functional decomposition that gives the consultant a broad and sufficiently complete map of what the product needs to do before detailed functional behavior is analyzed.

The Structure should answer:

> What functional capabilities make up this product?

It should allow the consultant to review the complete functional landscape rather than rediscover basic product functionality manually.

The **Structure Stage** should identify:

- Functional Areas;
- Capability Groups where useful;
- validated capabilities;
- functionally implied capabilities;
- capability priorities;
- capability dependencies where structurally important;
- assumptions and open questions affecting the decomposition.

The **Structure Stage** should not define:

- detailed Actor/System flows;
- detailed business rules;
- exhaustive validations;
- field-level requirements;
- UI behavior;
- technical implementation.

These belong to later Stages.

---

## Input

Primary input:

- validated **Shape v2 Document**.

Additional inputs may include:

- validation findings;
- existing product materials;
- relevant research from previous Stages;
- supporting project information.

The **Shape v2 Document** is the validated product boundary from which Structure begins.

The **Structure Stage** must not silently redefine the validated product direction.

---

## Output

The **Structure Stage** produces two versions of the same Document type.

### Structure v1 Document

The **Structure v1 Document** is the agent's proposed functional decomposition.

It contains:

- Functional Areas;
- Capability Groups where useful;
- Validated capabilities;
- Derived capabilities;
- capability priorities;
- rationale for Derived capabilities where necessary;
- important structural dependencies;
- assumptions and open questions;
- validated scope coverage;
- functional completeness findings.

The **Structure v1 Document** is deliberately allowed to be broader than the final Structure.

When uncertainty exists between:

- omitting a potentially necessary capability; and
- explicitly proposing it for consultant review;

prefer explicit proposal when there is a reasonable functional justification.

The capability must be marked as Derived rather than presented as validated fact.

---

### Structure v2 Document

The consultant reviews the **Structure v1 Document** and produces the **Structure v2 Document**.

During this review, the consultant may:

- remove unnecessary capabilities;
- reject unjustified Derived capabilities;
- add missing capabilities;
- merge capabilities;
- split capabilities;
- rename capabilities;
- move capabilities between Functional Areas;
- reorganize Capability Groups;
- correct actor responsibility;
- change priorities;
- resolve assumptions;
- add new open questions.

The purpose of this review is not to preserve the agent's decomposition.

The purpose is to produce the best functional Structure for the product.

The **Structure v2 Document** is the reviewed functional decomposition and becomes the primary input to the **Concepts Stage**.

---

## Core Structure Principle

The primary decomposition is:

**Validated Product Scope → Functional Areas → Capability Groups → Capabilities**

Capability Groups are optional.

Use them when they make a Functional Area easier to understand.

Do not create artificial hierarchy merely to make the Structure deeper.

Example:

```text
Account & Authentication

├── Registration
├── Authentication
│   ├── Login
│   └── Logout
├── Password Management
│   ├── Forgot Password
│   └── Change Password
└── Profile
    └── View Profile
```

Another Functional Area may require no intermediate grouping:

```text
Source Materials

├── Add Source Materials
├── View Source Materials
└── Remove Source Materials
```

The Structure should represent meaningful functional decomposition rather than screens, technical components, or implementation architecture.

---

## Functional Discovery Principle

The **Structure Stage** is not a transcription exercise.

Capabilities explicitly named in the **Shape v2 Document** are the starting point, not necessarily the complete functional model.

For every Functional Area, investigate the functional mechanisms required for the validated product behavior to work coherently.

Ask:

1. What responsibility does this Functional Area represent?
2. Which actors interact with it?
3. What validated capabilities belong here?
4. What functional objects or processes exist here?
5. How does each object or process begin?
6. How does an actor find or access existing work later?
7. How does an actor continue existing work?
8. What may need to be viewed?
9. What may need to be changed?
10. What may need to be removed, closed, revoked, cancelled, repeated, or otherwise managed?
11. What actor-specific management actions are required?
12. What meaningful lifecycle transitions exist?
13. What happens when the normal path cannot continue?
14. What recovery capability may be necessary?
15. What supporting capability is required for another validated capability to remain usable?
16. What must exist before responsibility can pass to another Functional Area?

These questions are analytical prompts, not a mandatory CRUD checklist.

Do not automatically create Create / View / Edit / Delete capabilities for every object.

Every capability must have a product-specific functional reason for existing.

---

## Capability Classification

Every capability in the **Structure v1 Document** must be classified as either:

- `Validated`
- `Derived`

### Validated

A Validated capability directly represents behavior already established in the **Shape v2 Document**.

Example:

```text
Create Project — Validated
```

---

### Derived

A Derived capability was not explicitly defined in the **Shape v2 Document**, but analysis indicates that it may be necessary or strongly implied by the validated product behavior.

Example:

```text
Forgot Password — Derived

Rationale:
A vendor who loses authentication credentials needs a recovery mechanism to regain access to existing project work.
```

Derived does not mean approved.

The purpose of the classification is to allow the agent to propose potentially necessary functionality without silently expanding validated scope.

The consultant may accept, reject, transform, or reprioritize Derived capabilities during review.

---

## Priorities

Every capability in the **Structure v1 Document** must receive a proposed priority.

Use:

- `Must`
- `Should`
- `Could`

### Must

The capability is necessary for the validated MVP value loop, primary JTBD, essential actor responsibility, required recovery path, or basic operability of another Must capability.

Without it, the MVP cannot coherently deliver the validated outcome.

### Should

The capability materially improves the completeness or usability of the MVP but the validated value loop can still function without it.

Its absence creates meaningful friction, limitation, or operational inconvenience rather than breaking the core product outcome.

### Could

The capability is useful or logically related but is not required for the validated MVP to work coherently.

It can be deferred without materially damaging the core value loop.

---

Priority must be based on product necessity rather than how common a feature is.

Do not classify a capability as Must merely because similar products normally have it.

When assigning priority, consider:

- primary JTBD;
- Value Proposition;
- validated MVP value loop;
- actor ability to complete meaningful work;
- lifecycle continuity;
- recovery requirements;
- dependencies;
- validated constraints;
- consequences of omission.

For Derived capabilities, priority is also a hypothesis.

Example:

```text
Forgot Password
Classification: Derived
Priority: Should

Rationale:
Account recovery is necessary for continued use by an existing user, but it does not prevent the first end-to-end MVP value loop from being executed.
```

The consultant may change any proposed priority when producing the **Structure v2 Document**.

---

## Focus Areas

### 1. Functional Areas

Identify meaningful areas of functional responsibility.

A Functional Area should:

- represent a coherent product responsibility;
- contain related capabilities;
- have understandable actor involvement;
- support a meaningful part of the validated product behavior.

Do not define Functional Areas primarily from:

- screens;
- pages;
- database entities;
- APIs;
- services;
- technical components.

If one Functional Area contains materially different responsibilities, consider splitting it.

Do not split areas merely to increase granularity.

---

### 2. Capability Groups

Within a Functional Area, introduce Capability Groups when several capabilities represent one recognizable responsibility or lifecycle.

Example:

```text
Project Workspace

Project Management
- Create Project
- View Project
- Edit Project
- Delete Project

Project Access
- View Project List
- Open Project

Project Members
- Invite Member
- View Members
- Remove Member
```

Capability Groups are organizational tools.

They are not mandatory product entities and should not be invented when a flat capability list is clearer.

---

### 3. Capabilities

Capabilities describe meaningful things an actor can accomplish through the product.

Prefer actor-oriented capability names.

Examples:

```text
User can create a project.
User can view projects they participate in.
Project Owner can remove a project member.
Client can mark a UAT scenario as failed.
Vendor can mark an issue as resolved.
```

A capability should be:

- meaningful to product behavior;
- specific enough to represent one understandable responsibility;
- broad enough to avoid UI-level decomposition.

Avoid capabilities such as:

```text
Click Create button.
Open modal.
Enter field value.
Call API.
Store record in database.
```

These describe interaction or implementation details rather than functional Structure.

---

### 4. Functional Lifecycles

For important functional objects or processes, examine the lifecycle around validated capabilities.

Examples may include:

- account lifecycle;
- project lifecycle;
- membership lifecycle;
- source material lifecycle;
- UAT scenario lifecycle;
- issue lifecycle;
- acceptance lifecycle.

The lifecycle analysis is used to discover missing capabilities.

It is not necessary to document every lifecycle as a formal state model during the **Structure Stage**.

Detailed behavior and state transitions belong to the **Concepts Stage**.

---

### 5. Recovery and Continuation

Check whether users can continue meaningful work after common interruptions or negative states.

Examples may include:

- recovering account access;
- returning to an existing project;
- reopening unfinished work;
- resolving a failed UAT scenario;
- retesting after resolution;
- completing acceptance after a previous failure.

Recovery capabilities should be included when they are necessary for the original JTBD or validated value loop to reach its meaningful outcome.

Do not add generic recovery mechanisms without product-specific justification.

---

### 6. Dependencies

Capture dependencies only when they materially affect Structure or priority.

Example:

```text
Open Project
Depends on:
- Project exists
- User has project access
```

or:

```text
Retest Scenario
Depends on:
- Scenario previously failed
- Related issue has been resolved
```

Do not define technical dependencies during the **Structure Stage**.

---

### 7. Validated Scope Coverage

Create an explicit inventory of validated MVP capabilities from the **Shape v2 Document**.

Map every validated capability to the proposed Structure.

For each item determine:

- Functional Area;
- Capability or Capability Group representing it;
- coverage status.

Coverage statuses:

- `Covered`
- `Transformed`
- `Gap`

`Covered` means the validated behavior is explicitly represented.

`Transformed` means it has been decomposed or reorganized without losing its validated meaning.

`Gap` means the validated behavior is not adequately represented.

A validated capability must not silently disappear.

---

### 8. Functional Completeness

Validated Scope Coverage answers:

> Did we preserve everything already validated?

Functional Completeness answers:

> Did we discover enough surrounding functionality for the validated product to work coherently?

These are separate checks.

For each Functional Area ask:

- Can relevant actors begin their work?
- Can they find and return to existing work?
- Can they continue unfinished work?
- Can they perform necessary management actions?
- Is the relevant lifecycle sufficiently represented?
- Are important recovery capabilities present?
- Is a broad capability hiding several meaningful capabilities?
- Does another capability depend on functionality that does not exist in the Structure?
- Can responsibility pass coherently to the next Functional Area?

For the product as a whole ask:

- Can each primary JTBD reach its meaningful outcome?
- Does the validated Value Proposition have functional support?
- Can the complete MVP value loop finish?
- Can important negative paths return to that loop?
- Is anything required for basic operability missing?

Do not consider the Structure complete merely because every validated Shape capability appears somewhere in the hierarchy.

---

## Process

### Step 1 — Review the Shape v2 Document

Review:

- actors and users;
- primary JTBD;
- Value Proposition;
- validated MVP scope;
- Product Flow / value loop;
- negative and recovery paths;
- constraints;
- assumptions;
- open questions.

Create an explicit inventory of validated MVP capabilities.

Do not begin by mechanically converting Shape headings into Structure headings.

---

### Step 2 — Identify Functional Areas

Identify the major functional responsibilities required to support the validated MVP.

For every proposed Functional Area determine:

- its responsibility;
- relevant actors;
- validated behavior it supports.

Review whether any Functional Area is too broad or too fragmented.

---

### Step 3 — Build Initial Capability Inventory

Place validated capabilities from the **Shape v2 Document** into the appropriate Functional Areas.

Introduce Capability Groups where they improve clarity.

Mark these capabilities as:

`Validated`

Do not assume this initial inventory is functionally complete.

---

### Step 4 — Perform Functional Discovery

Analyze each Functional Area independently.

For every area:

1. identify important functional objects and processes;
2. examine their lifecycle;
3. identify how actors begin work;
4. identify how actors return to existing work;
5. identify necessary viewing and management capabilities;
6. identify actor-specific responsibilities;
7. identify important recovery and continuation mechanisms;
8. identify structural dependencies;
9. identify functionality implied by existing capabilities.

Add justified missing capabilities as:

`Derived`

Include a short rationale where the reason is not obvious.

Prefer exposing a reasonably justified Derived capability for consultant review over silently omitting a potentially material functional mechanism.

Do not add functionality solely because it is common in similar products.

---

### Step 5 — Review Decomposition Depth

Review every Functional Area and Capability Group.

Check whether:

- capabilities are too broad;
- one capability hides several materially different actor goals;
- multiple capabilities represent the same responsibility;
- a Functional Area should be split;
- Capability Groups improve or reduce clarity;
- important lifecycle actions are missing;
- the decomposition has drifted into UI or implementation detail.

Correct the Structure before continuing.

---

### Step 6 — Assign Priorities

Assign each capability:

- `Must`
- `Should`
- `Could`

Base priority on:

- validated MVP value loop;
- primary JTBD;
- Value Proposition;
- actor ability to complete meaningful work;
- functional dependencies;
- lifecycle continuity;
- recovery requirements;
- consequences of omission.

Do not use market convention as sufficient justification for priority.

For uncertain Derived capabilities, preserve the uncertainty rather than forcing false confidence.

---

### Step 7 — Check Dependencies

Identify structurally important capability dependencies.

Use dependencies to verify:

- capability ordering;
- missing prerequisite capabilities;
- priority consistency;
- lifecycle continuity.

If a Must capability depends on another capability, review whether the dependency must also be Must.

Do not model technical implementation dependencies.

---

### Step 8 — Verify Validated Scope Coverage

Map every validated MVP capability from the **Shape v2 Document** to the Structure.

Use:

- `Covered`
- `Transformed`
- `Gap`

Resolve every known `Gap` before producing the **Structure v1 Document**, or explicitly record why it remains unresolved.

---

### Step 9 — Perform Functional Completeness Review

Perform a separate completeness pass.

Review every Functional Area using the Functional Completeness questions.

Specifically search for capabilities that:

- were not explicitly stated in Shape;
- are necessary to operate an already validated capability;
- allow users to return to existing work;
- support an important lifecycle;
- support necessary management;
- recover from meaningful negative states;
- connect otherwise disconnected parts of the validated value loop.

Add justified Derived capabilities where necessary.

Repeat until no material known structural gap remains.

---

### Step 10 — Produce the Structure v1 Document

Create the **Structure v1 Document**.

The Document should primarily represent:

**Functional Areas → Capability Groups → Capabilities**

For each capability include:

- capability;
- classification: Validated / Derived;
- priority: Must / Should / Could;
- relevant actor where useful;
- rationale for Derived capability where necessary;
- important dependency where necessary;
- open question where necessary.

Also include:

- Validated Scope Coverage;
- assumptions and open questions;
- Structure review status.

Do not add detailed Functional Flows.

Do not add Actor/System interaction tables.

Do not specify detailed Rules or States.

Do not create technical architecture.

---

### Step 11 — Consultant Review

The consultant reviews the **Structure v1 Document**.

The review is an analytical activity, not an approval formality.

The consultant should challenge:

- whether every Functional Area is necessary;
- whether Functional Areas have correct boundaries;
- whether Capability Groups are useful;
- whether capabilities are missing;
- whether Derived capabilities are actually justified;
- whether unnecessary functionality has been proposed;
- whether capabilities should be merged or split;
- whether actor responsibilities are correct;
- whether priorities reflect the actual MVP;
- whether the Structure is sufficiently complete to begin concept modeling.

The consultant may freely remove, add, merge, split, rename, move, or reprioritize capabilities.

The agent must not treat **Structure v1 Document** as validated Structure.

---

### Step 12 — Produce the Structure v2 Document

Incorporate consultant review findings into the **Structure v2 Document**.

After changes:

- repeat Validated Scope Coverage;
- repeat Functional Completeness review;
- verify priority consistency;
- verify important dependencies;
- preserve unresolved assumptions and open questions.

The **Structure v2 Document** represents the reviewed functional WBS of the product.

It becomes the primary input to the **Concepts Stage**.

---

## Structure Document Format

The recommended core representation is:

```text
## <Functional Area>

### <Capability Group>

#### <Capability>

Classification: Validated | Derived  
Priority: Must | Should | Could  
Actor: <Actor, when useful>

Rationale:
<Required for Derived capabilities when not obvious>

Dependencies:
<Only structurally important dependencies>

Open Questions:
<Only questions affecting Structure>
```

For compact areas, table representation may be used:

| Capability | Classification | Priority | Actor | Rationale / Notes |
|---|---|---|---|---|
| Create Project | Validated | Must | Vendor | |
| View Project List | Derived | Must | Vendor | Required to return to existing project work |
| Edit Project | Derived | Should | Project Owner | |
| Delete Project | Derived | Could | Project Owner | Validate MVP necessity |

Use whichever representation makes the Structure easiest to review.

The hierarchy and functional meaning are more important than formatting consistency.

---

## Success Criteria

The **Structure Stage** is successful when:

- the validated **Shape v2 Document** has been decomposed into a coherent functional WBS;
- Functional Areas represent meaningful product responsibilities;
- Capability Groups are used only where they improve understanding;
- every validated MVP capability is traceable to the Structure;
- no validated capability silently disappears;
- Functional Discovery has been performed for every Functional Area;
- important implied capabilities have been identified;
- Derived capabilities are clearly distinguished from Validated capabilities;
- Derived capabilities have functional justification;
- capabilities are sufficiently decomposed to expose meaningful actor responsibilities;
- capabilities have proposed priorities;
- priorities are based on product necessity rather than convention;
- structurally important dependencies are visible;
- functional lifecycles have been considered;
- important recovery and continuation capabilities have been considered;
- Validated Scope Coverage and Functional Completeness have been reviewed separately;
- the Structure has not drifted into detailed Requirements or technical Solutions;
- the **Structure v1 Document** has been reviewed by the consultant;
- unnecessary functionality has been removed or deprioritized;
- missing functionality identified during consultant review has been incorporated;
- the **Structure v2 Document** represents the reviewed functional decomposition;
- the **Structure v2 Document** is sufficient input for the **Concepts Stage**.

---

## Failure Conditions

The **Structure Stage** has failed or remains incomplete when:

- the Structure merely reorganizes wording from the **Shape v2 Document**;
- Functional Areas are primarily screens, database entities, APIs, services, or technical components;
- the agent assumes capabilities explicitly named in Shape are the complete functional model;
- important implied capabilities are omitted merely because Shape did not name them;
- generic SaaS functionality is added without product-specific justification;
- Derived capabilities are presented as validated facts;
- capability hierarchy is artificially deep without improving functional understanding;
- capabilities are so broad that materially different responsibilities remain hidden;
- capabilities are decomposed into UI actions or implementation details;
- capability priorities are missing;
- priorities are based primarily on what similar products normally contain;
- a Must capability depends on an omitted prerequisite capability;
- a validated MVP capability disappears without an explicit decision;
- Validated Scope Coverage is confused with Functional Completeness;
- detailed Actor/System flows are produced instead of functional decomposition;
- detailed requirements are specified prematurely;
- technical architecture replaces functional Structure;
- **Structure v1 Document** is treated as final without consultant review;
- consultant corrections are not incorporated;
- the **Structure v2 Document** remains too shallow or inconsistent to begin the **Concepts Stage**.