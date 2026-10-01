# Interaction Stage

## Purpose

The Interaction Stage translates the validated behavioral model of the product
into a low-fidelity visual interaction model.

Its purpose is to make important product behavior tangible enough to understand,
discuss, challenge, and validate before detailed Requirements and Design.

Interaction does not define the complete product interface.

---

## Objective

The objective of this Stage is to establish a coherent interaction hypothesis
for the product and visualize the parts of product behavior where visual
representation materially improves understanding.

The Stage should answer:

> How does the user interact with the important parts of the product behavior?

---

## Input

Primary input:

- **Behavior v2**

Supporting inputs:

- Structure v2
- Shape v2
- Domain
- Idea
- relevant project materials

Behavior v2 is the authoritative source for product behavior.

---

## Output

The output of this Stage is:

**Interaction v1 Artifact**

After Consultant Review:

**Interaction v2 Artifact**

After Client Validation:

**Interaction v3 Artifact**

Interaction is a visual artifact rather than a Document.

---

## Core Principles

### Behavior Is Authoritative

Interaction represents product behavior.

It must not independently change:

- product scope;
- actor responsibilities;
- Rules;
- permissions;
- State logic;
- workflows;
- recovery behavior;
- other established product behavior.

If creating a coherent interaction requires changing the behavioral model, this
indicates an upstream issue rather than an Interaction decision.

---

### Interaction Is Selective

Interaction does not attempt to visualize the entire product.

Not every:

- Capability;
- actor;
- action;
- State;
- transition;
- Rule;
- error;
- recovery path;
- data element

requires a visual representation.

The selection criterion is:

> Would visualizing this behavior make it materially easier to understand,
> discuss, challenge, or validate?

If not, it normally does not need to be represented in Interaction.

---

### Interaction Is a Coherent Model

Interaction should not be a collection of unrelated screens.

Before individual wireframes are created, establish the smallest coherent
interaction model necessary to represent the selected behavior.

This may include:

- product context;
- navigation model;
- entity hierarchy;
- page or view model;
- recurring interaction patterns;
- actor context;
- relationships between parent and child entities.

The interaction model may introduce provisional interface structure where
necessary to represent Behavior coherently.

These decisions are interaction hypotheses and are subject to Consultant and
Client Validation.

---

### Interaction Is Low Fidelity

Interaction communicates structure and behavior, not final interface design.

The artifact should optimize for:

- speed of thinking;
- clarity;
- discussion;
- restructuring;
- direct modification during Consultant Review.

Visual fidelity is not an objective of this Stage.

---

## Focus Areas

### Product Context

Represent enough context for a user to understand where they are and what they
are interacting with.

This may include:

- major product areas;
- important entities;
- entity hierarchy;
- parent-child relationships;
- actor context.

---

### Navigation

Represent the navigation necessary to understand the selected interaction model.

The goal is not to define complete information architecture.

Navigation should be detailed only as far as necessary to understand how users
reach and move between important product contexts.

---

### Core Interaction

Prioritize interaction that is:

- central to product value;
- product-specific;
- multi-step;
- state-dependent;
- actor-dependent;
- structurally unusual;
- difficult to understand from textual Behavior alone;
- important for client discussion or validation.

---

### States and System Feedback

Represent States and system feedback when they materially affect how users
understand or continue an interaction.

This may include representative:

- state changes;
- success feedback;
- failure feedback;
- blocked behavior;
- recovery;
- empty conditions;
- boundary conditions.

A separate representation is not required for every possible State.

---

### Actor Differences

Represent actor-specific interaction where different responsibilities,
permissions, entry points, or available actions materially change the
interaction.

Do not duplicate the same interaction solely to achieve actor coverage.

---

## Process

### 1. Understand the Behavioral Model

Review Behavior v2 and identify the product behavior relevant to interaction.

Understand:

- actors;
- important flows;
- States and transitions;
- Rules;
- recovery;
- functional Data;
- entity relationships;
- available actions;
- important system responses.

---

### 2. Identify Visualization Candidates

Identify behavior that may benefit materially from visual representation.

Pay particular attention to:

- core product behavior;
- important entity relationships;
- multi-step interaction;
- state-dependent interaction;
- actor differences;
- recovery;
- unusual product mechanics;
- areas likely to require client discussion.

---

### 3. Select Interaction Scope

Select the smallest coherent set of behavior necessary to make the interaction
model understandable and useful for validation.

Selection should be based on analytical value rather than coverage.

---

### 4. Establish the Interaction Model

Define the minimum interaction structure necessary to represent the selected
behavior coherently.

Determine, where relevant:

- product context;
- navigation;
- entity hierarchy;
- page or view structure;
- recurring interaction patterns;
- actor entry points.

Prefer reusable interaction patterns over independent solutions for individual
cases.

---

### 5. Create Representative Wireframes

Create low-fidelity wireframes that demonstrate the selected interaction model
and behavior.

A wireframe may represent:

- an important entry point;
- a core working context;
- an important entity;
- an actor-specific context;
- an important behavioral transition;
- recovery;
- another interaction that cannot be understood sufficiently from the primary
  representations.

Create only representations that add meaningful understanding.

---

### 6. Review Behavioral Consistency

Review the Interaction artifact against Behavior v2.

Verify that the interaction does not:

- introduce unsupported product behavior;
- contradict Rules;
- change actor responsibilities;
- change permissions;
- change State logic;
- change recovery behavior;
- silently expand scope.

Any conflict that requires a behavioral decision should be returned upstream.

---

### 7. Review Interaction Coherence

Review the artifact as a whole.

A reviewer should be able to understand, where relevant:

- where the user is;
- what they are interacting with;
- how related product entities are organized;
- how they reached the current context;
- what they can do;
- what important information is available;
- how important States or outcomes are represented;
- how they continue after an important action or transition.

The artifact should communicate one coherent interaction hypothesis rather than
a catalogue of examples.

---

## Consultant Review

Interaction v1 is reviewed and modified by the Consultant.

Consultant Review may:

- accept or reject interaction hypotheses;
- restructure navigation;
- restructure page or view organization;
- change representation of product entities;
- change interaction patterns;
- remove unnecessary representations;
- add missing representations;
- simplify the interaction model;
- resolve visual ambiguity.

Consultant Review must preserve the established behavioral model.

If the review reveals that Behavior itself must change, the issue is resolved
upstream rather than silently inside Interaction.

The result of Consultant Review is:

**Interaction v2 Artifact**

---

## Client Validation

Interaction v2 is validated together with Behavior v2.

Interaction provides a visual representation through which important behavioral
decisions can be understood, discussed, and challenged.

It does not replace Behavior.

Accepted validation feedback may result in changes to either or both artifacts.

The resulting validated artifacts are:

- **Behavior v3**
- **Interaction v3**

---

## Completion Criteria

Interaction is sufficiently complete when:

- the important behavior that benefits from visualization is represented;
- the representations form a coherent interaction model;
- important product context and navigation are understandable;
- important entity relationships are understandable;
- actor differences are represented where materially relevant;
- important States and system feedback are visible where they affect
  interaction;
- the artifact remains consistent with Behavior;
- the artifact can be efficiently reviewed and modified;
- additional representations would primarily increase coverage rather than
  improve understanding or validation.

Completeness means sufficient interaction clarity.

It does not mean complete interface coverage.

---

## Failure Conditions

Interaction has failed its purpose if it:

- attempts to visualize all product behavior;
- becomes a screen catalogue;
- becomes a visual Requirements specification;
- becomes a visual test matrix;
- creates representations primarily for coverage;
- creates a separate screen for every possible State;
- duplicates interaction solely for actor coverage;
- invents unsupported product behavior;
- silently changes Rules, permissions, States, workflows, or scope;
- produces isolated screens without a coherent interaction model;
- introduces detailed interface decisions that are not necessary for
  understanding the interaction;
- optimizes visual fidelity at the expense of reasoning and modification.

---

## Boundaries

### Behavior → Interaction

Behavior defines:

> How does the product behave?

Interaction determines:

> How should the important parts of that behavior be represented so the
> interaction can be understood and validated?

Interaction may propose interface structure.

It must not redefine product behavior.

---

### Interaction → Requirements

Interaction is not a detailed behavioral specification.

After Behavior and Interaction are validated, Requirements define the precise
expected product behavior required for implementation and testing.

---

### Interaction → Design

Interaction establishes a low-fidelity interaction hypothesis sufficient for
understanding and validation.

Design defines the complete UX/UI required for implementation.

Interaction focuses on:

> understanding and validating interaction.

Design focuses on:

> designing the complete product experience.