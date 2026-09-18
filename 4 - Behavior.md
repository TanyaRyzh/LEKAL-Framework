# LEKAL 4 — Behavior

## Goal

Transform the reviewed **Structure v2 Document** into a coherent behavioral model of the product.

The **Structure Stage** determines:

> What functional mechanisms exist?

The **Behavior Stage** determines:

> How does the product behave?

For significant functionality from the **Structure v2 Document**, analyze where relevant:

- who participates in the behavior;
- what triggers it;
- what actors can do;
- how the system responds;
- what decisions or conditions affect behavior;
- what information is required or produced;
- what meaningful states exist;
- what causes state transitions;
- which actions are available in different states;
- how changes affect related objects and aggregate state;
- what happens on important negative paths;
- how recovery works where necessary;
- how behavior connects across Functional Areas;
- which meaningful product behaviors must be observable.

The result of the agent's analysis is the **Behavior v1 Document**.

The consultant reviews the proposed behavioral model, visualizes it where useful, corrects logic, removes unnecessary detail, adds missing behavior, resolves inconsistencies, and produces the **Behavior v2 Document**.

The **Behavior v2 Document** becomes the reviewed behavioral model and the primary input to the **Interaction Stage**.

---

## Objective

Produce a behavioral model rich enough that the consultant can understand and challenge how the product works without having to invent the basic behavior from scratch.

The **Behavior Stage** should:

- transform functional Capabilities into coherent behavioral mechanisms;
- identify meaningful actors, triggers, conditions, responses, and outcomes;
- model meaningful lifecycle States and transitions;
- identify actions available in different States where relevant;
- identify important Rules and functional Data;
- represent important negative and recovery behavior;
- identify consequences of changes to related product objects;
- maintain behavioral consistency across Functional Areas;
- identify structural problems exposed by behavioral analysis;
- identify meaningful product behavior that must be observable;
- provide a stable behavioral basis for interaction modeling.

The **Behavior Stage** should not define:

- screens or page layouts;
- navigation structure;
- visual hierarchy;
- detailed UI interaction;
- exhaustive field requirements;
- exhaustive validations;
- exact error messages;
- complete permission specifications;
- technical architecture;
- APIs or implementation details.

These belong to later Stages.

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

The **Structure v2 Document** defines the functional mechanisms and priorities used by the **Behavior Stage**.

The **Behavior Stage** must not silently redesign that Structure.

If behavioral analysis reveals that the Structure is materially incomplete or incorrect, record the structural issue explicitly rather than hiding it inside the behavioral model.

---

## Output

The **Behavior Stage** produces two versions of the same Document type.

### Behavior v1 Document

The **Behavior v1 Document** is the agent's proposed behavioral model.

It contains, where relevant:

- behavior mapped to Capabilities from the **Structure v2 Document**;
- actors and responsibilities;
- triggers and Preconditions;
- behavioral flows;
- States and State Transitions;
- transition permissions;
- actions available in different States;
- important decisions and status calculations;
- alternative and negative behavior;
- recovery behavior;
- behaviorally important Rules;
- functional Data;
- consequences and recalculation behavior;
- connections between behavioral mechanisms;
- observability and analytics behavior;
- assumptions;
- Open Questions;
- identified Structural Gaps.

Not every behavioral mechanism requires every representation.

The **Behavior v1 Document** is an analytical proposal.

It must not present uncertain behavior as confirmed product fact.

---

### Behavior v2 Document

The consultant reviews the **Behavior v1 Document** and produces the **Behavior v2 Document**.

During review, the consultant may:

- correct behavior;
- remove unnecessary behavior;
- add missing behavior;
- split or combine behavioral mechanisms;
- change actor responsibilities;
- correct triggers and Preconditions;
- change Rules;
- correct States or transitions;
- correct action availability;
- add missing consequences or recalculation behavior;
- add missing negative paths;
- add or remove recovery behavior;
- change the chosen behavioral representation;
- resolve assumptions;
- add Open Questions;
- identify missing Structure Capabilities;
- return structural problems to the **Structure Stage** where necessary.

The purpose of review is not to preserve the agent's proposal.

The purpose is to produce a coherent model of how the product should behave.

The **Behavior v2 Document** becomes the reviewed behavioral model and the primary input to the **Interaction Stage**.

---

## Core Behavior Principle

The primary transformation is:

**Functional Structure → Behavioral Model**

A Capability in the **Structure v2 Document** tells us that functionality exists.

The **Behavior Stage** explains how that functionality behaves.

The behavioral model should expose the mechanism with enough precision to reason about:

- actors;
- lifecycle;
- decisions;
- actions;
- consequences;
- recovery;
- relationships with other behavior.

It should not attempt to produce a complete Requirements specification.

---

## Behavior Organization

The **Behavior Document** should normally be organized by Functional Area to make consultant review easier.

Recommended organization:

```text
Functional Area
↓
Behavioral Mechanisms
↓
Relevant behavioral representations
```

Functional Areas are organizational and review containers.

They are not behavioral boundaries.

A behavioral mechanism may:

- correspond to one Capability;
- combine several tightly connected Capabilities;
- represent part of a Capability;
- connect Capabilities from several Functional Areas.

Behavioral boundaries should follow behavior.

Document organization should follow consultant review workflow.

Do not duplicate the same behavior under several Functional Areas merely because it affects several parts of the product.

---

## Behavior Selection and Depth

Not every Capability requires the same amount of behavioral modeling.

Use the High / Medium / Low priority from the **Structure v2 Document** as one input when determining analytical depth.

### High

High-priority Capabilities normally require sufficient behavioral analysis to understand how the mechanism works and how it affects the core product.

### Medium

Medium-priority Capabilities should be analyzed when their behavior materially affects product coherence, supporting workflows, actors, or other mechanisms.

### Low

Low-priority Capabilities may be modeled more lightly when deeper analysis would not materially improve current product understanding.

Priority is not the only criterion.

A lower-priority Capability may require substantial behavioral analysis when it:

- has a complex lifecycle;
- changes another object's behavior;
- introduces important Rules;
- creates privacy, legal, or regulatory behavior;
- affects several Functional Areas;
- creates important negative or recovery behavior.

Do not spend equal analytical effort on every Capability merely for formatting consistency.

---

## Behavioral Boundaries

A behavioral mechanism should represent one coherent piece of product behavior.

Use behavioral coherence rather than Structure hierarchy to determine boundaries.

Several Capabilities may be modeled together when their behavior is inseparable.

A single Capability may require several behavioral representations when it contains materially different behavior.

Every significant Capability from the **Structure v2 Document** must be behaviorally represented or explicitly accounted for.

No significant Capability should silently disappear.

---

## Representation Selection

There is no mandatory primary representation for product behavior.

Choose the representation that exposes the mechanism clearly with the least unnecessary duplication.

Possible representations include:

- Actor/System Functional Flow;
- State Machine;
- State Transition Matrix;
- Actions Matrix;
- Decision Table;
- Status Calculation Table;
- Rules;
- functional Data model;
- relationship model;
- other structured behavioral representation appropriate to the mechanism.

Several representations may be combined when they answer different behavioral questions.

For example:

```text
State Machine
→ What lifecycle States exist?

Transition Matrix
→ Who can move the object between those States?

Actions Matrix
→ What can actors do while the object is in each State?

Status Calculation
→ How is an aggregate State derived from related objects?
```

Do not create an Actor/System Functional Flow merely because the template contains one.

Do not create a State Machine merely because an object exists.

Do not reproduce the same behavioral rule in several representations unless the duplication materially improves understanding.

The representation is a tool for analysis, not a required artifact shape.

---

## Actor/System Functional Flow

Use an Actor/System Functional Flow when sequence and interaction are necessary to understand the behavior.

Prefer:

| Actor | System |
|---|---|
| <Actor action> | |
| | <System response> |
| | <Decision / validation> |
| <Next actor action> | |
| | <State change / result> |

Flows are particularly useful when behavior involves:

- a meaningful sequence of actor and system actions;
- handoffs between actors;
- system decisions during an interaction;
- recovery paths;
- interactions whose order matters.

The flow should begin from a meaningful trigger and end at a meaningful functional result.

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
Publish event.
```

Technical design belongs to the **Solutions Stage**.

---

## States

Identify meaningful States when behavior depends on them.

A State is useful when it:

- changes available actor actions;
- changes system behavior;
- represents meaningful lifecycle progress;
- enables or blocks another behavior;
- affects related objects;
- is necessary to understand recovery or completion.

Do not invent formal State Machines for objects whose States do not materially affect behavior.

Where States are important, define their functional meaning consistently across the behavioral model.

---

## State Machines

Use a State Machine when the lifecycle of an object is central to understanding its behavior.

A State Machine should show:

- meaningful States;
- valid lifecycle progression;
- important branches;
- important recovery or terminal States.

It should answer:

> What meaningful States can this object move through?

A State Machine does not need to contain every actor permission or every content-editing consequence.

Use other representations when those questions are better expressed separately.

---

## State Transition Matrix

Use a State Transition Matrix when it is important to understand who or what may cause a State Transition.

Example:

| From | To | Owner | Member | Guest | System |
|---|---|---|---|---|---|
| <State> | <State> | Yes / No | Yes / No | Yes / No | Yes / No |

The matrix should answer:

> Who may initiate or cause this transition?

Do not use the transition matrix to describe unrelated actions that do not themselves represent lifecycle transitions.

---

## Actions Matrix

Use an Actions Matrix when available actions depend materially on the current State.

Example:

| Action | State A | State B | State C |
|---|---|---|---|
| Edit | Yes | Yes | No |
| Delete | Yes | Conditional | No |
| Archive | Yes | Yes | No |

The matrix should answer:

> What may be done to this object while it is in this State?

Actions may include structural or content changes that do not directly represent State Transitions.

When an action changes already evaluated or completed content, determine whether it:

- invalidates existing results;
- resets child States;
- resets the object's own State;
- triggers recalculation of related States;
- affects aggregate progress.

Represent those consequences explicitly.

---

## Decisions and Status Calculations

Use a Decision Table or Status Calculation Table when system behavior is derived from several conditions or related objects.

Examples include:

- aggregate Journey status derived from Scenario States;
- Scenario status derived from Acceptance Criterion States;
- overall UAT completion derived from Journey or Scenario completion;
- action availability derived from actor + State + ownership;
- limits or quotas determining whether an action remains available.

The representation should make the decision logic understandable without prematurely specifying implementation.

---

## Alternative and Negative Behavior

Identify alternative or negative behavior when it materially changes the mechanism.

Examples include:

- invalid input;
- duplicate or unavailable data;
- expired access;
- insufficient permissions;
- missing prerequisite;
- invalid State;
- limit reached;
- rejected action;
- failed execution;
- cancelled operation.

Do not enumerate every theoretical edge case.

Represent a negative path when it:

- prevents the intended outcome;
- creates a meaningful State;
- requires actor action;
- affects another actor;
- requires recovery;
- materially changes what happens next.

---

## Recovery

A negative result is not necessarily the end of product behavior.

When the original JTBD still requires completion, determine whether recovery is necessary.

Ask:

- Can the actor correct the problem?
- Can the actor retry?
- Can another actor resolve the blocking condition?
- Can the process return to productive behavior?
- Does the product need to preserve progress while the problem is resolved?
- Does recovery change or reset related States?

Recovery should reconnect to the meaningful product outcome where the validated value loop requires it.

---

## Actors and Responsibilities

For relevant behavior determine:

- who initiates it;
- who may participate;
- who owns decisions;
- who receives the result;
- whether responsibility passes between actors;
- whether the System itself causes behavior.

Do not assume that all authenticated users have the same responsibility.

When permissions are essential to understanding behavior, represent them at the level necessary for behavioral reasoning.

Exhaustive authorization specification belongs to the **Requirements Stage**.

---

## Preconditions

Capture Preconditions when they materially determine whether behavior can begin.

Examples:

```text
User is authenticated.

Project exists.

User owns the Project.

Guest Access is active.

Scenario is Ready to Test.
```

Do not use Preconditions to reproduce the entire upstream product flow.

---

## Rules

Capture Rules when they materially define behavior.

Rules may describe:

- who may perform an action;
- when an action is available;
- what condition must be satisfied;
- what happens when a limit is reached;
- what happens when content changes;
- when a result becomes invalid;
- when another object's State must be recalculated;
- what acceptance or consent is required before behavior can continue.

Do not attempt to specify every validation, field constraint, error message, or edge case.

Those belong to the **Requirements Stage**.

---

## Data

Capture Data when it is necessary to understand behavior.

Focus on functional information rather than schemas.

For example:

```text
Feedback:

- related Scenario;
- related Acceptance Criterion, when applicable;
- type;
- text;
- author;
- attachments.
```

or:

```text
Guest Access:

- Project;
- guest email;
- access token;
- status.
```

Do not define:

- database tables;
- API payloads;
- exact data types;
- storage models;
- technical schemas.

---

## Change Consequences and Recalculation

Behavioral analysis must consider what happens when actors change objects that already participate in product progress or calculated State.

For important edit, delete, archive, restore, or similar actions, ask:

- Does existing execution or progress remain valid?
- Does a child object need to reset?
- Does the current object need to reset?
- Does a parent object's State need to be recalculated?
- Does overall progress need to be recalculated?
- Does another actor need to repeat an action?

Example:

```text
Acceptance Criterion structural change
↓
Acceptance Criterion execution result may become invalid
↓
Scenario progress is recalculated
↓
Journey progress is recalculated
```

Do not assume that CRUD-like actions are behaviorally isolated.

When they affect existing product state, model the consequences.

---

## Limits and Quotas

When the **Structure v2 Document**, **Shape v2 Document**, or validated product context establishes limits or quotas, define their behavioral effect.

Examples may include:

- maximum number of Projects;
- maximum number of Project Members;
- usage or resource limits;
- other product-specific quotas.

For each relevant limit determine:

- what is being limited;
- when the limit is evaluated;
- what action becomes unavailable or blocked;
- how the actor understands why the action cannot continue;
- whether removing an existing object or resource makes the action available again;
- whether the limit differs by product stage, account type, role, or other validated condition.

A numeric limit alone is not a complete behavioral model.

Do not invent limits that have not been established or justified upstream.

---

## Terms, Privacy, and Consent Behavior

Where the validated product context requires Terms acceptance, Privacy Policy presentation, consent, or preference management, define the relevant behavior.

Analyze, where applicable:

- when Terms or Privacy information is presented;
- whether explicit acceptance is required;
- what happens when required acceptance is not provided;
- what version or decision must be recorded functionally;
- whether updated Terms require renewed acceptance;
- whether optional consent may be refused without blocking unrelated product use;
- whether users can later change optional preferences;
- what behavior depends on those preferences.

Distinguish:

- mandatory conditions required to use the product;
- informational legal notices;
- optional consent;
- user-controlled preferences.

Do not assume that every legal or privacy document requires explicit consent.

Do not invent legal requirements.

When legal interpretation is unresolved, represent the product decision as an assumption or Open Question requiring appropriate validation.

---

## Cross-Area Behavior

Behavior must not be analyzed as isolated Functional Areas.

For each significant mechanism determine:

- what must exist before it can begin;
- what State or Data it consumes;
- what State or Data it produces;
- what other behavior follows;
- where responsibility moves;
- what related objects are affected;
- where negative behavior leads;
- where recovery reconnects;
- what must be recalculated after changes.

Functional Areas may organize the **Behavior Document**, but cross-area behavior must remain explicit.

---

## Behavioral Consistency

After individual mechanisms have been analyzed, perform a consistency pass across the complete behavioral model.

Check:

- Do outputs satisfy downstream Preconditions?
- Are actors and responsibilities consistent?
- Are functional objects described consistently?
- Are States named and interpreted consistently?
- Are transitions compatible with available actions?
- Does one mechanism require Data that no previous behavior produces?
- Does behavior assume a Capability absent from the **Structure v2 Document**?
- Do negative paths lead somewhere meaningful?
- Can recovery return to the intended value loop?
- Can the same object reach contradictory States?
- Do edit/delete/archive actions invalidate or recalculate related progress correctly?
- Are parent and child State calculations consistent?
- Are limits enforced consistently wherever the limited action can occur?
- Are consent and preference decisions respected by dependent behavior?

Do not consider the behavioral model complete merely because each individual mechanism looks reasonable in isolation.

---

## Structural Gap Detection

Behavioral analysis may reveal that the **Structure v2 Document** is incomplete or incorrect.

Examples:

- behavior requires a Capability that does not exist;
- an actor needs an action not represented in Structure;
- recovery requires another functional mechanism;
- a lifecycle cannot complete using existing Capabilities;
- a cross-cutting responsibility has no Capability;
- a Capability is too broad to model coherently;
- Structure represents a product object or responsibility incorrectly.

When this occurs:

1. Identify the Structural Gap.
2. Explain why the Structure is insufficient.
3. Record the proposed correction.
4. Do not silently modify the reviewed **Structure v2 Document** as if the change were already approved.

Minor structural corrections may be incorporated during consultant review according to the methodology.

Material changes to validated product scope must return to the appropriate upstream decision.

---

## Behavioral Uncertainty

Missing behavioral information does not automatically require asking the client.

When behavior is uncertain:

1. Check existing project information.
2. Determine whether behavior follows logically from validated upstream Documents.
3. Research when external facts can reduce uncertainty.
4. Compare reasonable behavioral options.
5. Analyze implications and trade-offs.
6. Propose a recommendation where appropriate.
7. Mark unresolved assumptions or Open Questions.

Do not invent certainty.

Do not stop analysis merely because some details are unknown.

---

## Observability and Analytics

After the core behavioral model is established, perform a separate observability pass.

Ask:

> Which meaningful product behaviors must be observable?

Analytics is not modeled as a generic user Capability unless the product actually exposes analytics functionality to an actor.

Instead, identify meaningful events from already-defined behavior.

Candidate events may include:

- completion of important value-loop steps;
- creation or deletion of important functional objects;
- meaningful State Transitions;
- start and completion of important workflows;
- important recovery behavior;
- product activation or adoption milestones;
- changes to relevant preferences or consent;
- reaching product limits where analytically useful.

For each meaningful event determine, where useful:

- event name;
- trigger;
- relevant non-sensitive parameters;
- relationship to the product value loop or analytical question.

Prefer meaningful events over low-level interaction telemetry.

For example:

```text
project_created
guest_access_opened
scenario_testing_started
acceptance_criterion_failed
scenario_ready_for_retest
uat_completed
```

are generally more behaviorally meaningful than:

```text
button_clicked
modal_opened
tab_changed
```

unless the low-level interaction itself answers a specific product question.

Analytics parameters may describe behavioral context such as:

- actor role;
- pseudonymous object identifier;
- previous State;
- new State;
- creation source;
- feedback type;
- language;
- consent status;
- limit type.

Do not send user-generated content, unnecessary personal information, or sensitive product data merely because it is available.

Examples of information that should normally not be used as analytics parameters include:

- email addresses;
- names;
- Project titles;
- Journey or Scenario content;
- Acceptance Criterion text;
- Feedback text;
- attachment names;
- client-provided content.

Analytics instrumentation must respect the consent and privacy behavior defined for the product.

The observability pass is an analytical control.

Only useful analytics findings need to appear in the **Behavior Document**.

---

## Behavior / Interaction Boundary

The **Behavior Stage** explains:

> How does the product behave?

The **Interaction Stage** determines:

> How does the user interact with that behavior through the product interface?

The **Behavior Stage** may define:

- actors;
- triggers;
- Preconditions;
- functional sequences;
- States;
- transitions;
- available actions;
- Rules;
- Data;
- negative behavior;
- recovery;
- consequences;
- behavioral connections.

The **Interaction Stage** may later define:

- screens or views;
- navigation;
- information hierarchy;
- where actions are available;
- how States are represented to the user;
- how system feedback is presented;
- wireframes and interaction structure.

Do not design screens merely to explain behavior.

At the same time, the behavioral model must contain enough information for the **Interaction Stage** to represent the product without inventing core product logic.

---

## Behavior / Requirements Boundary

The **Behavior Stage** explains:

> How does the functional mechanism work?

The **Requirements Stage** specifies:

> Exactly how must the system behave in all material cases?

The **Behavior Stage** should capture enough detail to understand:

- actor behavior;
- system responsibility;
- significant decisions;
- meaningful Rules;
- important Data;
- meaningful States;
- action availability;
- negative behavior;
- recovery;
- consequences;
- connections.

The **Requirements Stage** should later define:

- exact field requirements;
- exhaustive validations;
- exact constraints;
- detailed permissions;
- complete alternative scenarios;
- exact error behavior;
- detailed business rules;
- acceptance criteria;
- exhaustive transition rules;
- precise system responses.

If the **Behavior Document** becomes a complete specification, the Stage has gone too far.

If it contains only Capability names and one-line descriptions, it has not gone far enough.

---

## Behavior / Solutions Boundary

The **Behavior Stage** must remain implementation-independent unless a technical constraint has already been validated.

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

Detailed technical interaction belongs to the **Solutions Stage**.

---

## Process

### Step 1 — Review the **Structure v2 Document**

Review:

- Functional Areas;
- Capabilities;
- priorities;
- actors;
- dependencies;
- assumptions;
- Open Questions.

Use the **Shape v2 Document** when necessary to preserve:

- product intent;
- Target Market;
- JTBD;
- Value Proposition;
- MVP boundaries;
- Product Stages / Scope;
- Constraints.

---

### Step 2 — Build Behavioral Inventory

For each Functional Area, identify the significant behavioral mechanisms that need to be understood.

For every significant Capability determine:

- whether it requires independent behavioral analysis;
- whether it belongs inside another behavioral mechanism;
- whether several Capabilities form one coherent mechanism;
- whether the Capability is too broad and exposes a Structural Gap.

Use High / Medium / Low priority as an input to analytical depth.

Do not begin by forcing every Capability into the same template.

---

### Step 3 — Select Behavioral Representations

For each mechanism determine which representation or combination of representations best exposes its behavior.

Consider:

- Functional Flow;
- State Machine;
- State Transition Matrix;
- Actions Matrix;
- Decision Table;
- Status Calculation;
- Rules;
- Data;
- relationships.

Use only representations that add information.

Avoid duplicating the same behavior across several artifacts.

---

### Step 4 — Analyze Core Behavior

Analyze, where relevant:

- actors;
- triggers;
- Preconditions;
- actor actions;
- system responses;
- decisions;
- meaningful results.

Where sequence matters, model the flow from trigger to meaningful outcome.

Where sequence does not materially add knowledge, use a more appropriate representation.

---

### Step 5 — Analyze States, Transitions, and Actions

For objects with meaningful lifecycle behavior:

1. Identify meaningful States.
2. Identify valid lifecycle progression.
3. Identify who or what can cause relevant transitions.
4. Identify actions available in each State.
5. Identify actions that become unavailable.
6. Identify consequences of changes to already evaluated or completed objects.

Use separate representations where this improves clarity.

---

### Step 6 — Analyze Alternative, Negative, and Recovery Behavior

Identify material deviations from intended behavior.

For each relevant negative condition determine:

- what causes it;
- what the system does;
- what the actor can do;
- whether work stops;
- whether another actor becomes responsible;
- whether recovery is required;
- where recovery reconnects.

If recovery requires functionality absent from the **Structure v2 Document**, record a Structural Gap.

---

### Step 7 — Analyze Rules, Data, Limits, and Consequences

Capture behavioral Rules and functional Data necessary to understand the mechanism.

Review validated limits and quotas.

For actions that change existing product content or Structure, determine whether related execution results, States, or aggregate progress must be invalidated or recalculated.

Do not expand into exhaustive Requirements.

---

### Step 8 — Analyze Consent, Legal, and Preference Behavior

For relevant Capabilities and validated product concerns, analyze:

- Terms acceptance;
- Privacy Policy presentation;
- optional consent;
- preference management;
- language or localization preferences;
- account lifecycle and deletion behavior;
- other cross-cutting behavior discovered during Structure.

Do not assume that every concern requires the same behavior.

Do not invent legal requirements.

---

### Step 9 — Connect Behavior Across Functional Areas

Determine:

- prerequisites;
- produced and consumed information;
- responsibility handoffs;
- State dependencies;
- parent/child relationships;
- continuation paths;
- recovery paths;
- recalculation chains.

Ensure the behavioral model supports the complete validated value loop.

---

### Step 10 — Perform Behavioral Consistency Review

Review the complete behavioral model.

Look for:

- missing Preconditions;
- inconsistent actors;
- inconsistent States;
- missing Data;
- impossible handoffs;
- disconnected behavior;
- duplicated responsibility;
- contradictory Rules;
- missing recovery;
- inconsistent action availability;
- missing invalidation or recalculation behavior;
- hidden Structural Gaps.

Resolve clear behavioral inconsistencies.

Record structural problems separately.

---

### Step 11 — Verify Structure Coverage

Internally map every significant Capability from the **Structure v2 Document** to the behavioral model.

Determine whether it is:

- Covered;
- Combined;
- Gap.

No significant Structure Capability should silently disappear.

This is an analytical control.

Do not reproduce a complete coverage matrix in the **Behavior Document** unless it contains material information useful for review.

---

### Step 12 — Perform Observability and Analytics Review

Review the completed behavioral model and identify which meaningful behaviors must be observable.

Define useful:

- analytics events;
- triggers;
- non-sensitive parameters;
- funnel or value-loop relationships where relevant.

Check that analytics behavior respects privacy and consent decisions.

Do not instrument every possible UI action by default.

---

### Step 13 — Produce **Behavior v1 Document**

Create the **Behavior v1 Document**.

Organize it primarily by Functional Area for consultant review.

For each significant behavioral mechanism include only the representations and supporting information that materially explain its behavior.

The Document may contain:

- Structure Mapping;
- Priority;
- Actors;
- Trigger;
- Preconditions;
- Functional Flow;
- State Machine;
- Transition Matrix;
- Actions Matrix;
- Decision or Status Calculation;
- Alternative / Negative Behavior;
- Recovery;
- Rules;
- Data;
- Consequences;
- Connections;
- Analytics Events;
- Assumptions;
- Open Questions.

Also include material:

- Structural Gaps;
- cross-area consistency findings;
- behavioral Open Questions;
- review status.

Do not add empty sections merely for template consistency.

Stop after producing the **Behavior v1 Document**.

Consultant Review must not be simulated.

---

### Step 14 — Consultant Review and Visualization

The consultant reviews the **Behavior v1 Document** and visualizes behavior in Miro or another suitable workspace where visual representation improves analysis.

Visualization is an analytical activity.

It is not mechanical transcription of the **Behavior v1 Document**.

During review, the consultant may:

- reorganize behavior for review;
- challenge behavioral boundaries;
- choose different representations;
- correct Functional Flows;
- correct State Machines;
- correct transition permissions;
- correct Actions Matrices;
- challenge status calculations;
- identify missing consequences;
- identify missing behavior;
- remove unnecessary behavior;
- check relationships spatially;
- discover missing handoffs;
- discover duplicated responsibility;
- challenge Rules and Data;
- identify Structural Gaps;
- identify assumptions and Open Questions;
- compare the model against their own product understanding.

The consultant may reject or substantially change the agent's proposal.

The purpose of the agent output is to provide analytical material for human synthesis, not to replace it.

---

### Step 15 — Produce **Behavior v2 Document**

After actual Consultant Review findings are available:

1. incorporate accepted review decisions;
2. correct behavioral boundaries;
3. update behavioral representations;
4. update actors and responsibilities;
5. update States, transitions, and actions;
6. update negative and recovery behavior;
7. update Rules and Data;
8. update limits and consequences;
9. update cross-area connections;
10. update analytics findings where behavior changed;
11. update assumptions and Open Questions;
12. record unresolved Structural Gaps;
13. repeat Structure Coverage;
14. repeat Behavioral Consistency Review;
15. produce the **Behavior v2 Document**.

The **Behavior v2 Document** is the consultant-reviewed behavioral model.

It becomes the primary input to the **Interaction Stage**.

---

## Recommended Behavior Document Format

The **Behavior Document** should be organized for consultant review rather than around a mandatory repeated Concept template.

Recommended high-level structure:

```text
Status

Functional Area

    Behavioral Mechanism

        Structure Mapping
        Priority

        Relevant behavioral representations:
            Functional Flow
            and/or
            State Machine
            and/or
            Transition Matrix
            and/or
            Actions Matrix
            and/or
            Decision / Status Calculation

        Relevant supporting information:
            Actors
            Preconditions
            Rules
            Data
            Negative Behavior
            Recovery
            Consequences
            Connections
            Assumptions
            Open Questions

Functional Area

    Behavioral Mechanism
    ...

Analytics / Observability

Structural Gaps

Cross-Area Behavioral Consistency

Open Questions

Behavior Validation

Behavior Status
```

Include only sections and representations that add meaningful behavioral information.

Do not fill the Document with:

```text
N/A
None
Not applicable
```

merely for formatting consistency.

---

## Success Criteria

The **Behavior Stage** is successful when:

- every significant Capability from the **Structure v2 Document** is behaviorally represented;
- behavioral boundaries reflect coherent product behavior;
- High-priority Capabilities have sufficient behavioral analysis;
- representation is selected according to the mechanism rather than template convention;
- meaningful sequential behavior reaches functional outcomes;
- actor and system responsibilities are clear;
- material decisions and conditions are visible;
- important negative behavior is represented;
- necessary recovery returns to meaningful product behavior;
- important Rules are visible;
- functionally important Data is visible;
- meaningful States are represented where needed;
- relevant State Transitions are understood;
- State-dependent actions are represented where needed;
- changes that invalidate or recalculate related progress are represented;
- relevant limits and quotas have defined behavioral consequences;
- relevant consent, Terms, Privacy, and preference behavior is understood;
- behavior connects coherently across Functional Areas;
- the complete behavioral model supports the validated MVP value loop;
- primary JTBD can reach their meaningful outcomes;
- actors, States, Rules, and functional objects remain consistent across the model;
- Structural Gaps discovered during behavioral analysis are explicit;
- significant Structure Capabilities are Covered, Combined, or explicitly identified as Gap;
- meaningful product behavior has been reviewed for observability;
- analytics findings respect privacy and consent behavior;
- the model contains enough information for the **Interaction Stage** to model the interface without inventing core product behavior;
- the model has not drifted into detailed Requirements;
- the model has not drifted into technical Solutions;
- the **Behavior v1 Document** has undergone real Consultant Review;
- consultant findings have been incorporated into the **Behavior v2 Document**;
- Behavioral Consistency has been repeated after material changes;
- the **Behavior v2 Document** is sufficiently coherent for the **Interaction Stage**.

---

## Failure Conditions

The **Behavior Stage** has failed or remains incomplete when:

- the **Behavior Document** merely repeats Capability names from the **Structure v2 Document**;
- significant Capabilities have no behavioral representation;
- every Capability is forced into the same behavioral template;
- Actor/System Functional Flow is treated as mandatory when another representation explains the mechanism better;
- States are modeled without considering relevant transitions or available actions;
- available actions contradict lifecycle States;
- changes to already evaluated content ignore necessary invalidation or recalculation;
- meaningful sequential behavior stops before the actor reaches its functional result;
- actor and system responsibilities are unclear;
- negative behavior is ignored when it materially affects the product;
- failure is treated as an endpoint when recovery is necessary for the original JTBD;
- Functional Areas are treated as hard behavioral boundaries;
- behavior is modeled independently without checking cross-area connections;
- one mechanism requires information or State that no other behavior produces;
- actor responsibilities contradict one another across the model;
- States are inconsistent across the model;
- validated limits exist but their behavioral effect is undefined;
- relevant consent, Terms, Privacy, or preference Capabilities exist but their behavior is undefined;
- meaningful analytics are omitted where product behavior must be observable;
- analytics instrumentation contradicts privacy or consent behavior;
- behavioral analysis exposes a Structural Gap and silently changes the reviewed Structure to hide it;
- every theoretical edge case is modeled regardless of relevance;
- detailed Requirements replace behavioral modeling;
- UI design replaces behavioral modeling;
- technical architecture replaces behavioral modeling;
- the **Behavior v1 Document** is treated as reviewed without actual Consultant Review;
- visualization is treated as mechanical transcription rather than analytical review;
- consultant corrections are not incorporated;
- the **Behavior v2 Document** remains too shallow or inconsistent to begin the **Interaction Stage**.