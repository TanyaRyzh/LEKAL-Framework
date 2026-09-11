# LEKAL 4 — Concepts

## Goal

Transform the reviewed **Structure v2 Document** into a behavioral model of the product's functional concepts.

The **Structure Stage** determines:

> What functional mechanisms exist?

The **Concepts Stage** determines:

> How does each significant functional mechanism work?

For every relevant capability from the **Structure v2 Document**, analyze:

- who initiates the interaction;
- what triggers it;
- what the actor does;
- how the system responds;
- what decisions or validations affect the flow;
- what information is required or produced;
- what meaningful states exist;
- what changes those states;
- what happens on important negative paths;
- how the actor recovers where recovery is necessary;
- how the concept connects to other concepts.

The result of the agent's analysis is the **Concepts v1 Document**.

The consultant reviews the proposed behavioral model, corrects logic, removes unnecessary detail, adds missing behavior, resolves structural inconsistencies, and produces the **Concepts v2 Document**.

The **Concepts v2 Document** becomes the primary source for visual modeling and the input to the **Requirements Stage**.

---

## Objective

Produce a **Concepts Document** that explains the behavior of the significant functional mechanisms identified in the **Structure v2 Document**.

The Document should provide enough behavioral information for the consultant to:

- understand how the product works;
- visualize the functional model in Miro or another suitable workspace;
- challenge the proposed behavior;
- discover missing interactions;
- discover inconsistent responsibilities;
- discover missing negative or recovery paths;
- identify missing rules or states;
- identify dependencies between concepts;
- prepare the product model for detailed Requirements.

The consultant should not need to invent the basic behavior of every capability from scratch during visualization.

The **Concepts Stage** should produce a rich analytical model that the consultant can review, reorganize, correct, and simplify.

---

## Input

Primary input:

- reviewed **Structure v2 Document**.

Additional inputs may include:

- validated **Shape v2 Document** for context and traceability;
- Structure review findings;
- existing product materials;
- relevant research from previous Stages;
- supporting project information.

The **Structure v2 Document** defines the functional decomposition and priorities used by the **Concepts Stage**.

The **Concepts Stage** must not silently redesign that Structure.

If behavioral analysis reveals that the Structure is materially incomplete or incorrect, record the structural issue explicitly rather than hiding it inside a concept.

---

## Output

The **Concepts Stage** produces two versions of the same Document type.

### Concepts v1 Document

The **Concepts v1 Document** is the agent's proposed behavioral model.

It contains, where relevant:

- concepts mapped to capabilities from the **Structure v2 Document**;
- actors;
- triggers;
- preconditions;
- Actor/System Functional Flows;
- alternative and negative flows;
- recovery behavior;
- structurally important rules;
- data required or produced by the interaction;
- meaningful states;
- state transitions;
- dependencies and connections between concepts;
- assumptions;
- open questions;
- identified structural gaps.

The **Concepts v1 Document** is an analytical proposal.

It must not present uncertain behavior as confirmed product fact.

---

### Concepts v2 Document

The consultant reviews the **Concepts v1 Document** and produces the **Concepts v2 Document**.

During this review, the consultant may:

- correct Functional Flows;
- remove unnecessary behavior;
- add missing behavior;
- split concepts;
- merge concepts;
- change actor responsibilities;
- correct triggers and preconditions;
- change rules;
- correct states or transitions;
- add missing negative paths;
- add or remove recovery behavior;
- resolve assumptions;
- add open questions;
- identify missing Structure capabilities;
- return structural problems to the **Structure Stage** where necessary.

The purpose of the review is not to preserve the agent's behavioral model.

The purpose is to produce a coherent model of how the product should function.

The **Concepts v2 Document** becomes the reviewed behavioral model used for visualization and detailed Requirements.

---

## Core Concepts Principle

The primary transformation is:

**Functional WBS → Functional Concepts → Behavioral Model**

A capability in the **Structure v2 Document** tells us that functionality exists.

A concept explains what that functionality means behaviorally.

For example:

```text
Structure:

Registration
Classification: Validated
Priority: Must
```

may become:

```text
Concept:

Registration

Actor:
User

Trigger:
User chooses to create an account.

Functional Flow:

Actor                         System

Enter email and password
                              Validate provided data
                              Check email availability
                              Send confirmation code

Enter confirmation code
                              Validate confirmation code
                              Create account
                              Establish authenticated session
                              Open product

Result:
User has a confirmed account and can access the product.
```

The **Concepts Stage** should reveal enough behavior to understand the mechanism.

It should not attempt to produce a complete Requirements specification.

---

## Concept Selection

Not every capability requires the same amount of behavioral modeling.

Analyze concepts according to their significance and priority.

### Must

Must capabilities require behavioral analysis unless the capability is trivial and completely represented inside another concept.

### Should

Should capabilities should normally be analyzed when they are part of the intended product behavior represented by the current Structure.

### Could

Could capabilities may be analyzed at a lighter level when detailed modeling would not materially help current product understanding.

Do not spend equal analytical effort on every capability merely for formatting consistency.

---

## Concept Boundaries

A Concept should represent one coherent functional mechanism.

A Concept may correspond to:

- one capability;
- several tightly connected capabilities;
- part of a capability when the capability contains materially different behavior.

Do not force a one-to-one mapping between capabilities and Concepts.

For example:

```text
Password Recovery
```

may be one Concept even if Structure contains several supporting capabilities.

At the same time:

```text
Manage Project
```

should not become one giant Concept if creation, editing, deletion, and access represent materially different behavior.

Use behavioral coherence to determine Concept boundaries.

Every significant capability from the **Structure v2 Document** must either:

- be represented by a Concept; or
- be explicitly mapped into another named Concept.

No significant capability should silently disappear.

---

## Functional Flow

The primary representation of Concept behavior is an Actor/System Functional Flow.

Prefer:

| Actor | System |
|---|---|
| <Actor action> | |
| | <System response> |
| | <Validation / decision> |
| <Next actor action> | |
| | <State change / result> |

The Functional Flow should expose meaningful interaction rather than every UI operation.

Represent, where relevant:

- trigger;
- actor action;
- system response;
- validation or decision;
- meaningful data exchange;
- state change;
- result.

Avoid UI-level steps such as:

```text
Click button.
Open modal.
Display spinner.
Close popup.
```

unless the interaction itself has functional meaning.

Avoid implementation steps such as:

```text
Call API.
Insert database record.
Publish Kafka event.
```

unless the technical behavior has already become a validated functional constraint.

Technical design belongs to the **Solutions Stage**.

---

## Main Flow

For each significant Concept, identify the primary successful path.

The Main Flow should answer:

> How does the actor normally achieve the intended result?

The flow should begin from a meaningful trigger and end at a meaningful functional result.

Do not stop at an arbitrary intermediate system state.

For example, if the job is to regain account access, the flow should not stop at:

```text
Password reset email sent.
```

when the meaningful result is:

```text
User successfully establishes a new password and can access the account.
```

---

## Alternative and Negative Flows

Identify alternative or negative behavior when it materially changes the Concept.

Examples include:

- invalid input;
- unavailable or duplicate data;
- expired access;
- insufficient permissions;
- rejected action;
- failed scenario;
- missing prerequisite;
- invalid state;
- cancelled operation.

Do not attempt to enumerate every theoretical edge case.

Include a negative path when it:

- prevents the Main Flow from completing;
- creates a meaningful product state;
- requires user action;
- affects another actor;
- requires recovery;
- changes the resulting behavior.

---

## Recovery

A negative path is not necessarily complete when the system reports failure.

When the actor's original JTBD still requires completion, determine whether a recovery path is necessary.

Ask:

- Can the actor correct the problem?
- Can the actor retry?
- Can another actor resolve the blocking condition?
- Can the process return to the Main Flow?
- Does the product need to preserve progress while the problem is resolved?

Example:

```text
Scenario fails
↓
Issue reported
↓
Vendor resolves issue
↓
Scenario becomes available for retest
↓
Client retests
↓
Scenario passes
```

The **Concepts Stage** should represent the recovery mechanism when it is necessary to achieve the validated product outcome.

---

## Actors and Responsibilities

For every Concept identify relevant actors.

Determine:

- who initiates the Concept;
- who may participate later;
- who owns decisions;
- who receives the result;
- whether responsibility passes between actors.

Do not assume that all authenticated users have the same functional responsibility.

If actor permissions materially change the behavior of a Concept, represent that difference.

Detailed permission matrices belong to the **Requirements Stage** unless they are necessary to understand the Concept.

---

## Preconditions

Capture preconditions when they materially determine whether a Concept can begin.

Examples:

```text
User is authenticated.

Project exists.

User is Project Owner.

Client has valid project access.

Scenario is in Failed state.
```

Do not use Preconditions to reproduce the entire upstream product flow.

Only include conditions necessary to understand the Concept.

---

## Rules

Capture rules when they materially define the behavior of a Concept.

Examples:

- email must be unique;
- only Project Owner can remove members;
- project cannot exceed the MVP member limit;
- failed scenario can create an issue;
- resolved issue enables retest;
- UAT cannot be completed while required scenarios remain unresolved.

Rules at this Stage should explain the behavioral model.

Do not attempt to specify:

- every validation rule;
- every exact field constraint;
- every error message;
- every permission combination;
- every edge case.

Those belong to the **Requirements Stage**.

---

## Data

Capture data when it is necessary to understand the Concept.

Focus on functional information rather than schemas.

Example:

```text
Project creation requires:

- Project Name
- Owner
```

or:

```text
Issue contains:

- related Scenario;
- description;
- status;
- reporter;
- evidence, when provided.
```

Do not define:

- database tables;
- API payloads;
- storage models;
- exact data types;
- technical schemas.

These belong to later specification or **Solutions Stage**.

---

## States

Identify meaningful states when behavior depends on them.

Examples:

```text
Scenario:
Draft → Ready → Passed
              → Failed → Retest → Passed
```

or:

```text
Issue:
Open → Resolved
```

A state belongs in the **Concepts Stage** when it:

- changes available actor actions;
- changes system behavior;
- represents meaningful lifecycle progress;
- enables or blocks another Concept;
- is necessary to understand recovery or completion.

Do not invent formal state machines for objects whose states do not materially affect behavior.

---

## State Transitions

For meaningful states determine:

- what triggers the transition;
- which actor may cause it;
- whether the system may cause it;
- what capability becomes available or unavailable afterward.

The purpose is to understand functional behavior.

Exact transition rules and exhaustive invalid transitions belong to the **Requirements Stage**.

---

## Concept Connections

Concepts must not be analyzed as isolated islands.

For each Concept determine:

- what must exist before it can begin;
- what information or state it consumes;
- what information or state it produces;
- which Concepts may follow;
- which Concept receives responsibility next;
- where negative paths lead;
- where recovery reconnects to the product flow.

Example:

```text
Create Project
↓
Invite Project Member
↓
Member gains Project Access
↓
Member can Open Project
```

or:

```text
Fail Scenario
↓
Report Issue
↓
Resolve Issue
↓
Retest Scenario
↓
Complete UAT
```

Connections should normally be represented through Concept relationships and flows.

A separate integration diagram is not required.

---

## Cross-Concept Consistency

After Concepts have been analyzed individually, perform a separate consistency pass across the complete behavioral model.

Check:

- Does the result of one Concept satisfy the Preconditions of the next?
- Are the same functional objects described consistently?
- Are actor responsibilities consistent between Concepts?
- Are states named and interpreted consistently?
- Does one Concept require data that no previous Concept produces?
- Does one Concept assume a capability that does not exist in the **Structure v2 Document**?
- Does a negative path lead somewhere meaningful?
- Can recovery return to the intended value loop?
- Can the same object accidentally reach contradictory states?
- Does one Concept allow behavior another Concept implicitly forbids?
- Are there missing transitions between Functional Areas?

Do not consider Concepts complete merely because every individual Concept looks reasonable in isolation.

---

## Structural Gap Detection

Behavioral analysis may reveal that the **Structure v2 Document** is incomplete.

Examples:

- a flow requires a capability that does not exist;
- an actor needs an action not represented in Structure;
- recovery requires an additional functional mechanism;
- a lifecycle cannot complete using the existing capability set;
- two capabilities should actually be separated;
- a capability is too broad to model coherently.

When this occurs:

1. identify the structural gap;
2. explain why the missing capability or structural change is necessary;
3. record the proposed change;
4. do not silently modify validated Structure as if the change were already approved.

Minor structural corrections may be incorporated during consultant review.

Material changes to MVP scope must return to the appropriate validation decision.

---

## Behavioral Uncertainty

Missing behavioral information does not automatically require asking the client.

When behavior is uncertain:

1. check existing project information;
2. determine whether behavior follows logically from validated Structure;
3. research when external facts can reduce uncertainty;
4. compare reasonable behavioral options;
5. propose a recommendation where appropriate;
6. mark unresolved assumptions or open questions.

Do not invent certainty.

Do not stop analysis merely because some details are unknown.

---

## Concepts / Requirements Boundary

The **Concepts Stage** explains:

> How does the functional mechanism work?

The **Requirements Stage** specifies:

> Exactly how must the system behave in all material cases?

Concepts should capture enough detail to understand:

- actor behavior;
- system responsibility;
- significant decisions;
- meaningful rules;
- important data;
- meaningful states;
- negative behavior;
- recovery;
- connections.

Requirements should later define:

- exact field requirements;
- exhaustive validations;
- exact constraints;
- detailed permissions;
- complete alternative scenarios;
- exact error behavior;
- detailed business rules;
- acceptance criteria;
- detailed state transition rules;
- precise system responses.

If Concepts become a complete specification, the Stage has gone too far.

If Concepts contain only capability names and one-line descriptions, the Stage has not gone far enough.

---

## Concepts / Solutions Boundary

The **Concepts Stage** must remain implementation-independent unless a technical constraint has already been validated.

Do not define:

- APIs;
- endpoints;
- database models;
- queues;
- services;
- frameworks;
- infrastructure;
- deployment;
- storage implementation;
- detailed integration architecture.

These belong to the **Solutions Stage**.

External systems may be referenced when they are functionally relevant.

Example:

```text
System imports requirements from Jira.
```

is acceptable as functional behavior.

Detailed Jira API interaction belongs to the **Solutions Stage**.

---

## Process

### Step 1 — Review the Structure v2 Document

Review:

- Functional Areas;
- Capability Groups;
- capabilities;
- capability classification;
- priorities;
- actors;
- dependencies;
- assumptions;
- open questions.

Use the **Shape v2 Document** when necessary to preserve product intent, JTBD, Value Proposition, and MVP boundaries.

---

### Step 2 — Create Concept Inventory

Map significant capabilities to proposed Concepts.

For every capability determine:

- whether it requires its own Concept;
- whether it belongs inside another Concept;
- whether several capabilities form one coherent Concept;
- whether the capability is too broad and exposes a structural problem.

Prioritize behavioral depth according to Must / Should / Could priority.

Do not begin detailed modeling until every significant capability has an intended Concept representation.

---

### Step 3 — Analyze the Main Flow

For every significant Concept identify:

- actor;
- trigger;
- preconditions;
- primary actor actions;
- system responses;
- important decisions;
- meaningful result.

Build the Main Flow from trigger to meaningful outcome.

Do not stop at an intermediate system response when the actor's job remains incomplete.

---

### Step 4 — Analyze Alternative and Negative Flows

Identify material deviations from the Main Flow.

For each relevant negative path determine:

- what causes it;
- what the system does;
- what the actor can do;
- whether the process stops;
- whether recovery is required.

Do not enumerate theoretical edge cases without product relevance.

---

### Step 5 — Analyze Recovery

For negative states that block the original job, determine whether and how the actor returns to productive flow.

Identify:

- recovery capability;
- responsible actor;
- required state or action;
- resulting state;
- reconnection point.

If recovery requires functionality absent from the **Structure v2 Document**, record a Structural Gap.

---

### Step 6 — Identify Rules and Data

Capture behavioral rules and functional data necessary to understand the Concept.

Keep the level sufficient for functional reasoning.

Do not expand into exhaustive Requirements.

---

### Step 7 — Identify States and Transitions

Identify states only when they materially affect behavior.

For relevant states determine:

- how the object enters the state;
- what behavior becomes possible;
- what behavior becomes blocked;
- what causes transition to another meaningful state.

Keep detailed transition specification for the **Requirements Stage**.

---

### Step 8 — Connect Concepts

Determine how Concepts interact.

Review:

- prerequisites;
- produced information;
- consumed information;
- responsibility handoffs;
- state dependencies;
- continuation paths;
- recovery paths.

Ensure the behavioral model supports the complete validated value loop.

---

### Step 9 — Perform Cross-Concept Consistency Review

Review the complete behavioral model rather than individual Concepts.

Look for:

- missing prerequisites;
- inconsistent actors;
- inconsistent states;
- missing data;
- impossible handoffs;
- disconnected flows;
- duplicated responsibility;
- contradictory behavior;
- missing recovery;
- hidden structural gaps.

Resolve clear behavioral inconsistencies.

Record structural problems separately.

---

### Step 10 — Verify Structure Coverage

Map every significant capability from the **Structure v2 Document** to the Concepts model.

Use:

- `Covered`
- `Combined`
- `Gap`

### Covered

The capability has its own Concept.

### Combined

The capability is explicitly represented inside another named Concept.

### Gap

The capability is not adequately represented.

No significant Structure capability should silently disappear.

---

### Step 11 — Produce the Concepts v1 Document

Create the **Concepts v1 Document**.

For each significant Concept include only relevant sections:

- Structure Mapping;
- Priority;
- Actors;
- Trigger;
- Preconditions;
- Main Functional Flow;
- Alternative / Negative Flows;
- Recovery;
- Rules;
- Data;
- States;
- Connections;
- Assumptions;
- Open Questions.

Also include:

- Structure Coverage;
- Structural Gaps;
- Cross-Concept Consistency findings;
- review status.

Do not add empty sections merely for template consistency.

---

### Step 12 — Consultant Review and Visualization

The consultant reviews the **Concepts v1 Document** while transferring the functional model into Miro or another suitable visual workspace.

Visualization is an analytical activity.

It is not a mechanical export of the **Concepts v1 Document**.

During visualization, the consultant:

- absorbs the product context;
- reorganizes Concepts where necessary;
- challenges Functional Flows;
- checks whether actor/system interaction makes sense;
- notices missing behavior;
- identifies unnecessary behavior;
- checks relationships spatially;
- discovers missing handoffs;
- discovers duplicated responsibility;
- challenges Rules and States;
- identifies additional assumptions and open questions;
- compares the model against their own product understanding.

The consultant may reject or substantially change the agent's proposal.

The purpose of the agent output is to provide rich analytical material for this review, not to replace human synthesis.

---

### Step 13 — Produce the Concepts v2 Document

Incorporate consultant review findings into the **Concepts v2 Document**.

Update:

- Concept boundaries;
- Functional Flows;
- actors;
- negative paths;
- recovery;
- Rules;
- Data;
- States;
- Connections;
- assumptions;
- open questions;
- Structure Coverage;
- Structural Gaps.

Repeat Cross-Concept Consistency Review after material changes.

The **Concepts v2 Document** becomes the reviewed behavioral model.

It becomes the primary input to the **Requirements Stage**.

---

## Concepts Document Format

The recommended representation is:

```text
## <Functional Area>

### <Concept>

Structure Mapping:
<Capability / capabilities from Structure v2>

Priority:
Must | Should | Could

Actors:
<Relevant actors>

Trigger:
<Meaningful trigger>

Preconditions:
<Only meaningful preconditions>

#### Main Functional Flow

| Actor | System |
|---|---|
| <Action> | |
| | <Response> |
| | <Decision / validation> |
| <Action> | |
| | <Meaningful result> |

#### Alternative / Negative Flows

<Only material alternatives>

#### Recovery

<When required>

#### Rules

<Only behaviorally important rules>

#### Data

<Only functionally important information>

#### States

<Only meaningful states and transitions>

#### Connections

<Relevant upstream / downstream Concepts>

#### Assumptions

<Behavioral assumptions>

#### Open Questions

<Unresolved questions>
```

Include only sections relevant to the Concept.

Do not fill the Document with:

```text
N/A
None
Not applicable
```

when the section provides no value.

---

## Success Criteria

The **Concepts Stage** is successful when:

- every significant capability from the **Structure v2 Document** is represented;
- Concept boundaries reflect coherent functional behavior;
- Must capabilities have sufficient behavioral analysis;
- Main Flows reach meaningful functional outcomes;
- actor and system responsibilities are clear;
- material decisions and validations are visible;
- important negative paths are represented;
- necessary recovery paths return to meaningful product flow;
- important Rules are visible;
- functionally important Data is visible;
- meaningful States and transitions are represented;
- Concepts connect coherently to one another;
- the complete behavioral model supports the validated MVP value loop;
- primary JTBD can reach their meaningful outcomes;
- actor responsibilities remain consistent across Concepts;
- states and functional objects are used consistently;
- Structural Gaps discovered during behavioral analysis are explicit;
- every Structure capability is Covered, Combined, or explicitly marked as Gap;
- the model contains enough information for meaningful visual analysis;
- the model has not drifted into detailed Requirements;
- the model has not drifted into technical Solutions;
- the **Concepts v1 Document** has been reviewed by the consultant;
- consultant findings have been incorporated;
- Cross-Concept Consistency has been repeated after material changes;
- the **Concepts v2 Document** is sufficient input for the **Requirements Stage**.

---

## Failure Conditions

The **Concepts Stage** has failed or remains incomplete when:

- the Document merely repeats capability names from the **Structure v2 Document**;
- significant capabilities have no behavioral representation;
- one broad Concept hides materially different functional mechanisms;
- Functional Flows contain only vague summaries;
- Functional Flows stop before the actor reaches a meaningful result;
- actor and system responsibilities are unclear;
- negative paths are ignored when they materially affect the product;
- failure is treated as an endpoint when recovery is necessary for the original JTBD;
- concepts are modeled independently without checking their connections;
- one Concept requires information or state that no other Concept produces;
- actor responsibilities contradict one another across Concepts;
- states are inconsistent across Concepts;
- behavioral analysis exposes a structural gap and silently invents functionality to hide it;
- every theoretical edge case is modeled regardless of relevance;
- detailed Requirements replace behavioral modeling;
- UI design replaces functional behavior;
- technical architecture replaces functional behavior;
- **Concepts v1 Document** is treated as final without consultant review;
- visualization is treated as mechanical transcription rather than analytical review;
- consultant corrections are not incorporated;
- the **Concepts v2 Document** remains too shallow or inconsistent to begin the **Requirements Stage**.