# Design Stage

## Purpose

The purpose of the **Design Stage** is to transform validated product behavior, interaction context, and precise Requirements into a complete product UX/UI design.

The Stage is optional.

It is used when the project requires a complete interface design rather than only the low-fidelity visual validation produced during the **Interaction Stage**.

The distinction between Interaction and Design is fundamental:

```text
Interaction
=
visualize selected product behavior
to support understanding and validation

Design
=
design the complete product interface
required for implementation
```

The Interaction Stage deliberately does not attempt to define the complete user experience.

The Design Stage does.

It determines how the validated and specified product should work through its user interface while preserving the product behavior established upstream.

---

# Objective

The objectives of the Design Stage are to:

- establish the complete information architecture required by the product;
- define complete navigation;
- represent all relevant user-facing functionality;
- define actor-specific experiences where required;
- determine how actions are exposed through the interface;
- represent meaningful product States and progress;
- define system feedback;
- define validation and error experiences;
- define destructive and recovery interactions;
- cover relevant empty, blocked, boundary, and terminal states;
- establish consistent interaction patterns;
- define responsive behavior where required;
- establish visual hierarchy and visual language;
- define reusable interface components where appropriate;
- produce a coherent design artifact suitable for implementation.

The Design Stage should make the complete required interface explicit without redefining validated product behavior.

---

# Input

The primary inputs are:

- **Behavior v3 Document**;
- **Interaction v3**;
- **Requirements Document**.

Relevant upstream Documents and artifacts remain available as supporting context.

### Behavior v3

Behavior v3 defines the client-validated behavioral model.

Design must preserve:

- actors;
- Rules;
- States;
- State Transitions;
- action availability;
- consequences;
- recovery behavior;
- relationships;
- other validated behavioral mechanisms.

### Interaction v3

Interaction v3 provides client-validated visual context.

It may establish useful:

- interaction concepts;
- product structure;
- page concepts;
- visual representations;
- navigation hypotheses;
- behavioral representations through UI.

Interaction v3 is not assumed to provide complete UX coverage.

Design may extend, reorganize, or elaborate it where necessary while preserving the validated product meaning.

### Requirements

The Requirements Document defines precise expected system behavior.

Design must represent user-facing Requirements completely enough for implementation.

Design must not silently change Requirements merely to simplify the interface.

---

# Design vs Interaction

The **Interaction Stage** asks:

> Which parts of product behavior need to be made visual so they can be understood and validated with the client?

The **Design Stage** asks:

> How should the complete validated and specified product work through its user interface?

Interaction is selective.

Design is comprehensive within the defined design scope.

Interaction prioritizes validation value.

Design prioritizes complete and coherent product usage.

Interaction may intentionally omit:

- generic screens;
- repetitive states;
- secondary actions;
- complete navigation;
- detailed validation;
- detailed error behavior;
- responsive behavior;
- final component behavior;
- visual polish.

Design must address these where they are required by the product.

Interaction artifacts may therefore be reused as starting points, but they must not be mistaken for completed Design.

---

# Design Authority

Design may make UX/UI decisions necessary to represent validated product behavior.

These may include:

- information architecture;
- navigation structure;
- page organization;
- action placement;
- information hierarchy;
- interaction patterns;
- layout;
- component selection;
- presentation of States;
- presentation of progress;
- feedback mechanisms;
- responsive behavior;
- visual hierarchy.

These decisions must remain consistent with upstream product knowledge.

Design must not independently change:

- Product Scope;
- actor responsibilities;
- functional Rules;
- State logic;
- permissions;
- validated workflows;
- Acceptance Criteria;
- other product behavior defined upstream.

If good UX appears to require changing validated product behavior, this is an **Upstream Gap or Conflict**, not merely a Design decision.

---

# Focus Areas

## 1. Information Architecture

Define how user-facing product information and functionality are organized.

This may include:

- primary product areas;
- entity hierarchy;
- page hierarchy;
- relationships between views;
- grouping of functionality;
- actor-specific access to product areas.

Information architecture should reflect the actual product model rather than arbitrary screen grouping.

---

## 2. Navigation

Define how users move through the product.

Depending on the product, this may include:

- global navigation;
- contextual navigation;
- entity navigation;
- breadcrumbs;
- tabs;
- links between related objects;
- entry and exit points;
- return paths.

Navigation should allow actors to understand:

- where they are;
- what they can access;
- how they can continue their work.

---

## 3. Screen and View Coverage

Identify and design the screens or views required to support the complete user-facing product scope.

Coverage should follow validated product behavior and Requirements.

Do not create screens merely to satisfy a generic screen checklist.

Conversely, do not omit required functionality merely because it was not visualized during Interaction.

---

## 4. Actions

Define how available actions are represented through the interface.

For relevant actions, determine:

- where the action is available;
- when it is available;
- how it is presented;
- what context is required;
- what happens after the action;
- how unavailable actions are handled where relevant.

Action availability must remain consistent with Roles, Permissions, Rules, and States.

---

## 5. States and Progress

Define how meaningful product States are represented to users.

Where relevant, determine:

- State visibility;
- progress representation;
- available actions by State;
- transition feedback;
- parent and child status representation;
- blocked States;
- terminal States.

The interface should make important product behavior understandable without exposing unnecessary internal system mechanics.

---

## 6. Forms and Data Entry

Design user interaction with fields and structured data.

Where relevant, define:

- field organization;
- required and optional fields;
- input controls;
- validation presentation;
- dependencies between fields;
- default values;
- editing behavior;
- save behavior;
- cancellation behavior;
- unsaved changes behavior.

Field behavior must remain consistent with Requirements.

---

## 7. System Feedback

Define how the interface communicates the result of user and system actions.

This may include:

- success feedback;
- warnings;
- errors;
- progress indicators;
- loading States;
- confirmations;
- informational messages;
- system status.

Feedback should make important consequences visible without producing unnecessary interruption.

---

## 8. Alternative and Negative States

Design relevant non-happy-path experiences.

These may include:

- validation errors;
- permission restrictions;
- unavailable actions;
- failed operations;
- expired access;
- missing data;
- unavailable external services;
- rejected operations;
- other product-specific negative outcomes.

Coverage should follow actual Requirements and Behavior rather than generic error-state enumeration.

---

## 9. Empty, Boundary, and Terminal States

Represent meaningful situations where normal content or actions are unavailable.

Depending on the product, these may include:

- first-use States;
- empty collections;
- completed processes;
- archived objects;
- reached limits;
- blocked workflows;
- deleted or unavailable resources;
- other meaningful boundary conditions.

The interface should make the user's available next action clear where one exists.

---

## 10. Destructive Actions and Recovery

Define interaction patterns for actions with significant consequences.

Where relevant, determine:

- whether confirmation is required;
- what information must be shown before confirmation;
- whether the action is reversible;
- what recovery path exists;
- how the result is communicated.

The level of protection should correspond to the consequence of the action.

---

## 11. Actor-Specific Experience

Where actors have materially different responsibilities or permissions, ensure that the Design represents those differences coherently.

This may affect:

- available product areas;
- navigation;
- visible information;
- available actions;
- workflow entry points;
- status presentation.

Do not create separate experiences where actor differences do not materially require them.

---

## 12. Responsive Behavior

Where required by the product, define how the interface behaves across relevant viewport sizes or device classes.

This may include:

- layout adaptation;
- navigation changes;
- component behavior;
- content prioritization;
- interaction changes.

Responsive Design should follow actual target platforms established upstream.

Do not automatically design every product for every possible device.

---

## 13. Components and Patterns

Identify reusable interface patterns and components where they improve consistency and implementation.

These may include:

- buttons;
- inputs;
- dialogs;
- tables;
- cards;
- navigation elements;
- status indicators;
- notifications;
- recurring entity representations;
- other product-specific components.

Repeated behavior should use consistent patterns unless there is a product reason for variation.

---

## 14. Visual Design

Where visual design is part of the project scope, establish the visual language required for the product.

This may include:

- visual hierarchy;
- typography;
- spacing;
- iconography;
- component styling;
- visual States;
- brand application;
- other relevant visual principles.

The required level of visual detail depends on the project and agreed Design scope.

---

## 15. Accessibility

Consider accessibility requirements relevant to the product, Target Market, platform, and project constraints.

Where applicable, this may affect:

- contrast;
- keyboard interaction;
- focus behavior;
- semantic hierarchy;
- input labeling;
- error communication;
- non-color State representation;
- assistive technology support.

Accessibility requirements should reflect actual product context and applicable standards rather than an unsupported generic compliance claim.

---

# Process

## Step 1 — Read Validated Product Knowledge

Read the complete:

- Behavior v3 Document;
- Interaction v3;
- Requirements Document.

Use relevant upstream artifacts where additional context is required.

Understand:

- actors;
- product scope;
- functional areas;
- entities;
- behavioral mechanisms;
- States;
- Rules;
- permissions;
- scenarios;
- Acceptance Criteria;
- known constraints;
- existing Interaction decisions.

Do not treat Interaction v3 as complete interface coverage.

---

## Step 2 — Establish Design Scope

Determine what must be designed for the project.

Identify:

- Product Stage or release;
- actors included;
- platforms included;
- relevant user-facing functionality;
- required visual fidelity;
- relevant responsive requirements;
- known brand or design constraints.

Design must remain within validated Product Scope.

---

## Step 3 — Establish Information Architecture

Define the product's user-facing structure.

Determine:

- primary areas;
- entity hierarchy;
- page or view hierarchy;
- relationships between areas;
- actor-specific access where relevant.

Use validated product structure and behavior as the basis.

---

## Step 4 — Define Navigation

Define the navigation required to move through the established information architecture and product workflows.

Ensure that important user journeys have coherent:

- entry points;
- continuation paths;
- contextual movement;
- return paths;
- exits.

---

## Step 5 — Establish Design Coverage

Map relevant Requirements and Behavior to the interface.

Identify which screens, views, States, and interaction patterns are required.

Interaction v3 may provide part of this coverage.

Add the missing interface coverage required for a complete Design.

Avoid both:

- missing required product behavior;
- unnecessary screen proliferation.

---

## Step 6 — Design Core Experiences

Design the primary user-facing product experiences first.

Establish recurring patterns before expanding them across secondary functionality.

Ensure consistency between:

- product structure;
- navigation;
- entity hierarchy;
- actor responsibilities;
- States;
- actions.

---

## Step 7 — Design Detailed Interaction

Expand the Design to cover relevant:

- forms;
- actions;
- States;
- system feedback;
- validations;
- alternative scenarios;
- negative scenarios;
- destructive actions;
- recovery;
- empty States;
- boundary States;
- terminal States.

Use Requirements as the behavioral authority.

---

## Step 8 — Define Reusable Patterns

Identify recurring interaction and visual patterns.

Create or reuse components where appropriate.

Maintain consistency unless different behavior is intentionally required.

---

## Step 9 — Apply Visual Design

Where required by project scope, develop the interface from structural UX into the required visual fidelity.

Apply:

- hierarchy;
- typography;
- spacing;
- components;
- visual States;
- branding;
- other relevant visual decisions.

---

## Step 10 — Review Coverage and Consistency

Review the Design against Behavior v3 and Requirements.

Check:

- required functionality is represented;
- actors have the correct access and actions;
- important States are represented;
- Rules and permissions are preserved;
- negative and recovery behavior is represented where necessary;
- recurring interaction patterns are consistent;
- navigation is coherent;
- the Design has not silently changed product behavior.

---

## Step 11 — Identify Upstream Gaps

If Design exposes missing, contradictory, or unusable upstream product behavior, record the issue explicitly.

Examples may include:

- missing State transitions;
- contradictory permissions;
- impossible workflow;
- unclear ownership;
- missing recovery behavior;
- incomplete Requirements;
- conflicting Acceptance Criteria.

Do not silently solve upstream product problems through interface invention.

Resolve the issue in the earliest responsible Stage or obtain the required Consultant decision.

---

## Step 12 — Produce the Design Artifact

Produce the complete Design Artifact at the fidelity required by the project.

The artifact should provide enough interface definition for its intended downstream use.

---

# Output

The output of the Design Stage is:

**Design Artifact**

The Design Artifact represents the complete UX/UI definition required by the project.

Its exact form may depend on:

- product type;
- target platform;
- required fidelity;
- delivery context;
- implementation needs.

The primary Design workspace may be Figma or another appropriate design environment.

The Design Artifact is not automatically a Document.

---

# Design Artifact Structure

The exact artifact structure should follow the product rather than a mandatory page taxonomy.

Where relevant, the Design Artifact may contain:

```text
Foundations / Shared Patterns

Application Structure

Navigation

Core Product Areas

Actor-Specific Experiences

Forms and Data Entry

States and Progress

System Feedback

Alternative / Negative States

Empty / Boundary / Terminal States

Destructive / Recovery Interactions

Responsive Variants

Components

Visual Design
```

These are possible organizational areas, not mandatory sections.

The artifact should be organized so that:

- the product can be understood coherently;
- related screens and States can be reviewed together;
- recurring patterns are recognizable;
- implementation-relevant behavior can be traced where necessary.

---

# Coverage

Unlike the Interaction Stage, the Design Stage is expected to provide complete interface coverage for the agreed Design scope.

However:

```text
Complete interface coverage
≠
one screen for every possible system State
```

Coverage should be achieved through reusable interaction patterns and components where possible.

A separate screen or variant is required only when the difference is materially relevant to:

- behavior;
- user understanding;
- implementation;
- review.

Do not turn the Design Artifact into a visual test matrix.

---

# Upstream Conflicts

Design may reveal that validated product behavior is difficult, contradictory, or impossible to represent coherently.

This is valuable analytical information.

The Design Stage must distinguish between:

```text
UX/UI Decision
```

and:

```text
Product Decision
```

The Agent or Designer may make the first within the Design Stage.

The second must be resolved through the appropriate upstream product process.

Design must not hide product uncertainty behind a visually plausible interface.

---

# Completion Criteria

The Design Stage is complete when:

- the agreed Design scope is covered;
- the required information architecture is defined;
- navigation is coherent;
- required user-facing functionality is represented;
- relevant actor-specific differences are represented;
- meaningful actions and States are represented;
- required validation, feedback, negative behavior, and recovery are represented;
- relevant empty, boundary, and terminal States are handled;
- recurring interaction patterns are consistent;
- responsive behavior is defined where required;
- visual design is developed to the agreed fidelity;
- relevant accessibility considerations are addressed;
- the Design remains consistent with Behavior v3 and Requirements;
- significant upstream gaps are resolved or explicitly recorded;
- the Design Artifact is sufficiently complete for its intended downstream use.

The Design Stage does not require every theoretical interface permutation to be drawn separately.

Completion means:

> the complete required product interface is defined sufficiently for the purpose for which Design was requested.

---

# Stage Boundary

The **Interaction Stage** determines:

> Which parts of product behavior need to be made visual so they can be understood and validated with the client?

The **Requirements Stage** determines:

> Exactly how must the system behave in material cases?

The **Design Stage** determines:

> How should that validated and specified product work through its complete user interface?

The **Solutions Stage** determines:

> How should the product be implemented technically?

Design owns the complete UX/UI solution.

It does not own Product Scope, product behavior, or technical architecture.