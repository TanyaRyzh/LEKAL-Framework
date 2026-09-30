# Interaction Stage

The goal of this stage is to make the reviewed product behavior easier to understand, discuss, and validate by representing key parts of it through low-fidelity interface wireframes.

At this point, the product behavior has already been defined and reviewed by the Consultant.

The Interaction Stage does not attempt to design the complete product interface.

Its purpose is to help the Consultant communicate important product behavior visually before detailed Requirements and full UX/UI design are produced.

The Agent translates selected parts of the reviewed Behavior into a small, coherent set of wireframes that show how important flows, entities, actions, states, and actor experiences may appear through an interface.

The wireframes are a communication and validation artifact.

They are not a complete UX specification and are not expected to cover every screen, action, state, validation rule, error, CRUD operation, or interaction detail in the product.

The stage is performed in two phases:

1. **Interaction Generation** — the Agent creates Interaction v1 from the Consultant-reviewed Behavior.
2. **Consultant Review** — the Consultant reviews and modifies the proposal and produces Interaction v2.

Interaction v2 is reviewed with the client together with Behavior v2.

Client feedback is then incorporated by the Consultant into Behavior v3 and Interaction v3 before the Requirements Stage.

---

## Objective

The objective of the Interaction Stage is to create enough visual context to make important product behavior concrete and understandable during client validation.

The stage should:

- identify the parts of the reviewed Behavior that benefit most from visual representation;
- translate those parts into clear low-fidelity wireframes;
- show how key actors experience important product flows;
- make important product entities, relationships, actions, and states easier to understand;
- provide enough interface context for the client to understand what the proposed behavior would mean in practice;
- help reveal misunderstandings or missing decisions that are difficult to notice in behavioral models alone;
- reduce the amount of interface visualization the Consultant needs to create manually;
- produce a visual artifact that can be reviewed and modified by the Consultant before client validation.

The Interaction Stage should prefer a small number of informative screens over exhaustive interface coverage.

A screen should exist because it helps explain or validate an important part of the product behavior, not merely because a possible interface state exists.

---

## Input

The primary input to the Interaction Stage is the latest Consultant-reviewed **Behavior v2**.

The Agent must use Behavior v2 as authoritative product knowledge.

The input may include:

- the Behavior v2 Document;
- reviewed behavioral diagrams and other artifacts that form part of Behavior v2;
- relevant upstream Documents where additional context is required;
- established scope boundaries, constraints, and Out of Scope decisions.

The Agent should not reinterpret or independently redesign established Behavior decisions.

Where multiple representations exist, the latest Consultant-reviewed version is authoritative.

Items explicitly marked Out of Scope must not be introduced into the interaction proposal.

---

## Focus Areas

### Key Behavioral Flows

Identify the flows where visual representation would materially improve understanding or client validation.

Priority should be given to flows that:

- represent the core product experience;
- contain important product-specific behavior;
- involve meaningful state transitions;
- involve multiple actors;
- contain important recovery behavior;
- depend on relationships between product entities;
- are difficult to understand from text or behavioral diagrams alone;
- contain decisions that the client is likely to need to validate.

Generic interface behavior does not require visualization unless it is important to the product decision being discussed.

### Product Context

Wireframes should provide enough surrounding interface context for the represented behavior to make sense.

Where relevant, show:

- the current product area;
- the current entity or working context;
- important parent-child relationships;
- the actor's available actions;
- relevant status or progress;
- enough navigation or hierarchy to understand where the user is.

The purpose is not to define the complete information architecture or navigation model.

Only the context necessary to understand the represented behavior is required.

### Screens and Views

Use complete, understandable screens or views as the primary review unit.

A wireframe should represent a meaningful user context rather than an isolated behavioral concept.

Several related behavioral decisions may be represented on the same screen.

Likewise, the Agent should not create separate screens for every possible state when the difference can be understood from a smaller number of representative views.

The artifact should remain easy to review as a product experience rather than becoming a catalogue of system states.

### Actors

Where actors experience materially different parts of a flow, represent those differences where they are important to understanding the Behavior.

Separate actor experiences do not need to be exhaustively designed.

Only the experiences required to explain the selected behavioral flows should be included.

### Actions, States, and Feedback

Represent actions, states, and system responses when they are important to understanding the selected behavior.

The Agent may show:

- important available actions;
- meaningful state changes;
- relevant system feedback;
- recovery actions;
- important consequences;
- progress or completion where relevant.

The Interaction Stage does not require visual coverage of every success message, validation error, blocked action, confirmation, boundary state, or alternative path.

Such details may be defined later through Requirements and full Design unless they are necessary to understand or validate the Behavior.

---

## Process

# Phase 1 — Interaction Generation

## 1. Read Behavior v2

The Agent reviews the complete Consultant-reviewed Behavior v2 and its relevant artifacts.

The Agent must understand the established:

- actors;
- product entities and relationships;
- key flows;
- actions;
- states and transitions;
- recovery behavior;
- rules and constraints;
- scope boundaries.

The purpose of this step is to understand the reviewed Behavior, not to redefine it.

## 2. Select Behavior to Visualize

The Agent identifies the parts of Behavior v2 where wireframes would provide meaningful additional value during client validation.

The Agent should ask internally:

**Would visualizing this behavior make it materially easier for the client to understand, validate, or challenge the proposed product behavior?**

If the answer is no, the behavior does not need a wireframe merely for coverage.

The Agent should aim for the smallest set of screens that provides sufficient visual context for the important behavioral decisions.

There is no required number of screens.

The number should follow the complexity of the product and the needs of client validation.

## 3. Define a Lightweight Interaction Skeleton

Before producing individual wireframes, the Agent establishes enough shared interaction structure to keep the selected screens coherent.

This may include:

- a basic application shell;
- a lightweight navigation concept;
- relevant entity hierarchy;
- recurring page structure;
- basic actor-specific context.

This structure is provisional.

It exists to make the wireframes understandable and internally consistent.

It is not intended to define the final UX architecture.

## 4. Build Interaction v1

The Agent creates a low-fidelity editable visual artifact in the designated design tool.

Interaction v1 should:

- represent the selected behavioral flows;
- use clear, understandable screens or views;
- provide sufficient product context;
- remain consistent across related screens;
- represent important actor differences where relevant;
- show important actions and states required to understand the behavior;
- avoid unnecessary visual detail;
- avoid solving interaction problems that are not necessary for behavioral validation.

The Agent should make reasonable lightweight interaction decisions where necessary to create understandable wireframes.

These decisions are proposals for review, not new authoritative product requirements.

The Agent should not stop for ordinary interface ambiguity.

Where a fundamental contradiction in Behavior v2 makes meaningful visualization impossible, the Agent should identify the contradiction rather than silently invent new product behavior.

## 5. Self-Review Interaction v1

Before presenting Interaction v1, the Agent reviews the artifact for its intended purpose.

The Agent checks whether:

- the selected wireframes cover the important behavioral areas that benefit from visualization;
- each screen has understandable user and product context;
- related screens form coherent flows;
- the artifact is small enough to remain practical for review;
- important actor differences are visible where necessary;
- the wireframes do not contradict Behavior v2;
- Out of Scope functionality has not been introduced;
- generic interface states have not expanded the artifact without providing meaningful validation value;
- the artifact has not accidentally become a complete UX specification.

The Agent corrects obvious problems before presenting Interaction v1.

---

# Phase 2 — Consultant Review

## 6. Consultant Reviews Interaction v1

The Consultant reviews the visual artifact.

The Consultant evaluates whether the wireframes:

- represent the intended Behavior correctly;
- make important flows easier to understand;
- provide enough context to discuss the product with the client;
- visualize the right behavioral decisions;
- omit behavioral areas that would benefit from visualization;
- introduce unnecessary interface detail;
- introduce interaction assumptions that should not yet be made;
- contain confusing or misleading representations;
- reveal gaps or problems in Behavior v2.

The Consultant may change the wireframes directly when doing so is more efficient than further Agent refinement.

## 7. Produce Interaction v2

Based on the review, the Consultant produces Interaction v2.

Interaction v2 represents the Consultant-reviewed visual interpretation of Behavior v2.

It should be suitable for client validation together with Behavior v2.

Interaction v2 does not need to be a complete UX specification or polished UI.

Its purpose is to make the proposed product behavior concrete enough for a productive client discussion.

---

# Client Validation

Behavior v2 and Interaction v2 are reviewed with the client as one validation package.

The client validates the proposed product behavior using both:

- the behavioral model;
- the visual representation of key flows.

Feedback may affect either or both artifacts.

After client validation, the Consultant incorporates the accepted feedback and produces:

- **Behavior v3** — client-reviewed Behavior;
- **Interaction v3** — client-reviewed Interaction.

Behavior v3 and Interaction v3 become input to the Requirements Stage.

---

## Output

The primary output of the Interaction Stage is a Consultant-reviewed low-fidelity visual artifact: **Interaction v2**.

The artifact typically consists of a small set of editable wireframes representing the behavioral flows where visual context materially improves understanding and validation.

The artifact is expected to provide:

- representative screens or views;
- key behavioral flows;
- enough product and user context to understand those flows;
- important actor differences where relevant;
- important actions, states, and transitions where relevant;
- a lightweight and internally coherent interaction skeleton.

The artifact is not expected to provide:

- complete screen coverage;
- complete information architecture;
- complete navigation design;
- exhaustive CRUD coverage;
- exhaustive error, validation, confirmation, and boundary states;
- final interaction patterns;
- visual design;
- design system;
- production-ready UI.

Those concerns are handled downstream using the validated Behavior, Interaction, and Requirements.

---

## Completion Criteria

The Interaction Stage is complete when:

- the important parts of Behavior v2 that benefit from visual representation have been identified;
- those parts are represented through a manageable set of understandable wireframes;
- the wireframes provide enough context to discuss the proposed behavior with the client;
- the artifact does not contradict established Behavior;
- unnecessary exhaustive UX coverage has been avoided;
- Out of Scope functionality has not been introduced;
- the Consultant has reviewed Interaction v1;
- the Consultant has produced Interaction v2;
- Behavior v2 and Interaction v2 are ready to be reviewed with the client together.

The Interaction Stage does not require a complete UX or final UI.

Full UX/UI design is performed downstream after the product behavior has been validated and Requirements have been defined.