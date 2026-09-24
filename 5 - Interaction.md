# Interaction Stage

The goal of this stage is to transform accumulated product knowledge
into a usable interaction model that shows how users interact with the
product.

At this point, the product scope, structure, and behavior have already
been defined. The Interaction Stage determines how that behavior is
exposed to users through the interface: how users navigate the product,
access actions, understand system states and feedback, and move through
product flows.

The Interaction Stage does not merely visualize previously defined
behavior.

Building an interaction model is an analytical activity itself. It may
require new decisions about information architecture, navigation, screen
structure, action placement, representation of states, transitions
between experiences, and other interaction-level concerns.

The Agent is expected to make these decisions and produce a concrete
interaction proposal rather than stop whenever the upstream artifacts do
not prescribe an exact interface.

The stage is performed in two phases:

1.  **Interaction Generation** --- the Agent independently produces a
    complete reviewable interaction proposal.
2.  **Consultant Review & Refinement** --- the Consultant reviews the
    proposal visually and iteratively refines it with the Agent until
    the interaction model is considered sufficient.

------------------------------------------------------------------------

## Objective

The objective of the Interaction Stage is to define how users interact
with the product behavior established during previous Stages.

The stage should:

-   transform accumulated product knowledge into a coherent interaction
    model;
-   define the information architecture of the product;
-   define navigation between product areas and hierarchy levels;
-   determine how users access available actions;
-   determine how system states and state changes are represented to
    users;
-   define interaction for primary, alternative, recovery, and
    destructive flows where applicable;
-   represent differences between actor experiences where necessary;
-   identify and resolve interaction-level gaps that become visible only
    when the product is represented as an interface;
-   provide a concrete visual artifact that can be reviewed by the
    Consultant;
-   ensure that the interaction proposal covers the relevant product
    behavior rather than only illustrating the primary happy path.

The result should be sufficiently concrete for a reviewer to understand
how the product would actually be used.

------------------------------------------------------------------------

## Input

The Interaction Stage uses accumulated product knowledge produced and
validated during previous Stages.

The input may include:

-   **Idea Document**
-   **Shape Document**
-   **Structure Document**
-   **Behavior Document**
-   reviewed behavioral artifacts, including:
    -   Functional Flows;
    -   State Machines;
    -   Transition Matrices;
    -   Actions Matrices;
    -   other relevant visual artifacts;
-   decisions, constraints, assumptions, and scope boundaries
    established during previous Stages.

The Agent must treat reviewed upstream artifacts as product knowledge,
not merely as reference material.

When information exists in multiple representations, the Agent must use
the latest reviewed version.

Items explicitly marked Out of Scope must not be introduced into the
interaction model.

------------------------------------------------------------------------

## Focus Areas

### Information Architecture

Determine how product information and functionality are organized from
the user's perspective.

Define:

-   major product areas;
-   hierarchy between entities and views;
-   grouping of related information and actions;
-   relationships between parent and child contexts;
-   how users understand where they are in the product.

### Navigation

Determine how users move through the product.

Consider:

-   entry points;
-   navigation between major product areas;
-   navigation between hierarchy levels;
-   returning to previous or parent contexts;
-   direct access to relevant entities where appropriate;
-   differences in navigation between actors or experiences.

Navigation should allow users to understand both their current context
and the available next destinations.

### Screens and Views

Determine which screens, views, panels, dialogs, or other interaction
surfaces are required to expose the defined product behavior.

A separate screen should not be created merely because a separate
behavioral concept exists.

Likewise, behavior must not be omitted merely because it does not belong
to the primary user journey.

### Actions

Represent the actions available to each actor.

This includes, where applicable:

-   create;
-   view;
-   edit;
-   delete;
-   archive;
-   state-changing actions;
-   management actions;
-   destructive actions;
-   recovery actions;
-   actions available only in particular states or to particular actors.

Action placement should reflect the user's current context and expected
workflow.

### States and System Feedback

Determine how relevant system and entity states are communicated to
users.

Consider:

-   current status;
-   progress;
-   completion;
-   blocked actions;
-   errors;
-   validation;
-   consequences of actions;
-   successful operations;
-   state changes;
-   invalidated or recalculated results;
-   user-visible confirmation of successful operations where the
    resulting state does not make success self-evident;
-   boundary and terminal states where applicable, such as exhausted
    attempts, expired or invalid access, reached limits, or other states
    that change what the user can do next.

For each user-initiated action, the interaction model should make the
outcome understandable to the user. Where applicable, this includes the
system response, user-visible feedback, resulting state or navigation,
and a recovery or exit path for unsuccessful outcomes.

Internal behavioral explanations should not automatically become
permanent UI text.

Internal scope, implementation, methodology, or delivery terminology
should not appear in user-facing interface copy unless it is genuinely
part of the user's product model.

The interaction model should communicate information at the moment and
location where it is useful to the user.

### Confirmations and Consequences

Actions with significant, destructive, irreversible, or
state-invalidating consequences should have an appropriate interaction
pattern.

Where confirmation is required, the user should be informed about the
relevant consequence as part of that interaction rather than through
unrelated permanent interface text.

### Actor Experiences

Where actors have materially different goals, permissions, workflows, or
product contexts, the Interaction Stage may define separate experiences
for them.

The Agent should not force different actors into the same interaction
model merely because they operate on the same underlying entities.

### Interaction-Level Decisions

Upstream Stages intentionally do not define every interface decision.

The Interaction Agent is expected to make reasonable decisions about
matters such as:

-   information hierarchy;
-   navigation;
-   grouping;
-   action placement;
-   screen boundaries;
-   representation of progress;
-   representation of relationships;
-   presentation of states and system feedback;
-   interaction patterns.

These decisions become new product knowledge created during the
Interaction Stage.

------------------------------------------------------------------------

## Process

The Interaction Stage consists of two phases.

# Phase 1 --- Interaction Generation

## 1. Read Accumulated Product Knowledge

The Agent reviews all relevant upstream Documents and reviewed visual
artifacts.

The Agent must understand:

-   actors;
-   product entities;
-   relationships;
-   available actions;
-   permissions;
-   states and transitions;
-   rules;
-   primary flows;
-   alternative flows;
-   recovery behavior;
-   destructive behavior;
-   constraints;
-   Out of Scope boundaries.

The Agent should analyze this information internally.

A separate textual analysis, ambiguity report, or proposed interaction
plan is not required before generation.

## 2. Build an Interaction Coverage Model

Before or while constructing the interaction proposal, the Agent must
ensure that the proposal is not limited to a single narrative or happy
path.

The Agent should account for relevant combinations of:

-   actors;
-   entities;
-   actions;
-   states;
-   transitions;
-   permissions;
-   creation and management operations;
-   destructive operations;
-   recovery flows;
-   alternative flows;
-   successful outcomes and resulting states;
-   validation failures and business-rule blocks;
-   boundary and terminal states where applicable.

For relevant user-initiated actions, the Agent should trace the complete
interaction outcome:

**action → system response → user-visible feedback → resulting state or
navigation**

Where an action can fail or be blocked, the Agent should also account
for the applicable recovery or exit path.

The purpose of this step is not to create another large deliverable.

Its purpose is to prevent known product behavior from disappearing
simply because it is not required by the primary walkthrough.

## 3. Make Interaction Decisions

Where upstream knowledge does not prescribe an exact interaction
solution, the Agent should make a reasonable proposal.

Ordinary interaction ambiguity is not a reason to stop and ask the
Consultant.

The preferred behavior is:

**make a reasonable proposal → visualize it → bring it to review**

The Agent should stop before generation only when a fundamental upstream
contradiction or missing decision makes a meaningful interaction
proposal impossible.

## 4. Build Interaction v1

The Agent creates a low-fidelity visual interaction proposal in the
designated design tool.

The proposal should be sufficiently complete to review:

-   product information architecture;
-   navigation;
-   relevant screens and views;
-   actor-specific experiences;
-   primary flows;
-   alternative and recovery flows where relevant;
-   state-dependent behavior;
-   available actions;
-   confirmations;
-   system feedback;
-   successful action outcomes where they are not otherwise
    self-evident;
-   relevant error, blocked, boundary, and terminal states;
-   recovery or exit paths where applicable;
-   progress and completion where relevant.

The purpose of Interaction v1 is not visual polish.

Its purpose is to make the proposed interaction model concrete enough to
inspect, challenge, and change.

## 5. Perform Coverage and Consistency Review

Before presenting Interaction v1 to the Consultant, the Agent performs a
self-review against the accumulated product knowledge and the
interaction proposal itself.

### Coverage Review

The Agent checks whether known in-scope behavior has an interaction
representation.

The review should specifically look for omissions caused by following
only the primary narrative, including:

-   missing create/edit/delete operations;
-   missing management functionality;
-   missing actor-specific actions;
-   missing state-dependent actions;
-   missing confirmations;
-   missing recovery paths;
-   missing navigation;
-   missing blocked/error states where relevant;
-   missing successful outcomes or user-visible confirmation where
    success is not otherwise clear;
-   missing boundary or terminal states where they affect the user's
    next available action;
-   known behavior that exists upstream but cannot be reached through
    the proposed interface.

For relevant user-initiated actions, the Agent should verify the
complete outcome chain:

**action → system response → user-visible feedback → resulting state or
navigation**

For unsuccessful outcomes, the Agent should verify that the user has an
understandable recovery or exit path where one exists.

### Consistency Review

The Agent reviews repeated interaction patterns across the artifact.

Equivalent actions, states, and controls should use a consistent
interaction pattern unless established product behavior requires a
difference.

The review should pay particular attention to repeated patterns such as:

-   authentication and credential inputs;
-   validation and error handling;
-   unavailable or blocked actions;
-   confirmations;
-   destructive actions;
-   success feedback;
-   navigation;
-   recovery patterns.

The purpose is not to enforce a universal UI convention. It is to
prevent the Agent from making contradictory interaction decisions for
equivalent situations without a product reason.

### User-Facing Language Review

The Agent checks interface copy for internal scope, implementation,
methodology, or delivery terminology that should not be exposed to
users.

Internal concepts may appear only when they are genuinely meaningful to
the user.

The Agent corrects obvious coverage, consistency, and language gaps
before presenting Interaction v1.

------------------------------------------------------------------------

# Phase 2 --- Consultant Review & Refinement

## 6. Consultant Reviews Interaction v1

The Consultant reviews the interaction proposal visually.

The primary review surface is the interaction artifact itself, not a
textual explanation produced by the Agent.

The Consultant evaluates whether the proposed interaction:

-   makes sense from the user's perspective;
-   exposes the necessary product behavior;
-   provides understandable navigation;
-   represents hierarchy appropriately;
-   places actions in sensible contexts;
-   communicates states and consequences clearly;
-   makes action outcomes and recovery paths understandable;
-   handles relevant boundary and terminal states;
-   uses repeated interaction patterns consistently where appropriate;
-   separates actor experiences where appropriate;
-   contains unnecessary interaction complexity;
-   misses expected functionality;
-   reveals new product questions or upstream gaps.

The Consultant may also identify preferable interaction solutions that
could not reasonably be determined from upstream knowledge alone.

## 7. Classify Significant Findings

Where useful, review findings may be distinguished as:

-   a problem in the proposed Interaction solution;
-   a missing Interaction decision;
-   an upstream Behavior gap;
-   an upstream Structure gap;
-   an upstream Shape gap;
-   a new methodology finding.

Not every visual correction requires formal classification.

Classification is primarily useful when a finding affects upstream
product knowledge or the LEKAL methodology.

## 8. Refine the Interaction Model

After Interaction v1 exists, the Consultant may give concrete change
requests directly to the Agent.

At this point, the Agent should treat explicit Consultant decisions as
authoritative unless they create a genuine contradiction with another
established product decision.

The refinement loop may include:

**Consultant Review** → targeted correction → updated interaction
artifact → review → further correction

The number of refinement iterations is not predetermined.

The Consultant may also modify the interaction artifact manually when
doing so is more efficient.

The purpose of refinement is to progressively shape the proposal into
the intended interaction model rather than repeatedly regenerate the
entire solution.

## 9. Resolve Upstream Gaps

If interaction work reveals a genuine missing upstream product decision,
that decision must be resolved at the appropriate level.

The Interaction Stage should not silently redefine established Shape,
Structure, or Behavior decisions.

However, discovering an upstream gap does not automatically invalidate
the entire Interaction proposal.

Unaffected parts of the interaction model may continue to be refined
while the relevant gap is resolved.

------------------------------------------------------------------------

## Output

The primary output of the Interaction Stage is a reviewed visual
interaction model.

For the current LEKAL workflow, this is typically a low-fidelity
editable Figma artifact containing the relevant interaction surfaces and
flows.

The artifact should capture:

-   information architecture;
-   navigation;
-   screens/views;
-   available actions;
-   actor-specific experiences;
-   representation of relevant states;
-   system feedback;
-   action outcomes and resulting states;
-   relevant boundary and terminal states;
-   confirmations and consequences;
-   primary flows;
-   relevant alternative and recovery flows;
-   interaction decisions created during the Stage.

A separate large textual **Interaction Document** is not required when
it would merely duplicate information that is better represented
visually.

Textual supporting artifacts may be introduced only where they provide
information that cannot be represented clearly in the visual interaction
model.

------------------------------------------------------------------------

## Completion Criteria

The Interaction Stage is complete when:

-   the accumulated in-scope product behavior has sufficient interaction
    coverage;
-   relevant actors can perform the actions defined for them;
-   primary flows can be followed through the interface;
-   relevant alternative, destructive, and recovery behavior has an
    interaction representation;
-   navigation between required product contexts is defined;
-   important states, consequences, and system feedback are represented;
-   relevant user actions have understandable outcomes, including
    success feedback where the result is not otherwise self-evident;
-   relevant unsuccessful outcomes provide a recovery or exit path where
    one exists;
-   boundary and terminal states that affect further interaction are
    represented;
-   repeated interaction patterns are internally consistent unless a
    product reason requires a difference;
-   user-facing copy does not expose internal scope, implementation,
    methodology, or delivery terminology without a user-facing reason;
-   known CRUD and management functionality has not been omitted simply
    because it falls outside the primary walkthrough;
-   the Consultant has reviewed the interaction model;
-   identified interaction problems have been resolved to an acceptable
    level;
-   significant upstream gaps discovered during review have been
    resolved or explicitly recorded;
-   the Consultant considers the interaction model sufficiently complete
    for downstream work.

Visual polish is not required for completion of the Interaction Stage.

If further work is required on visual language, layout refinement,
typography, components, design system, or other presentation-level
concerns, this may be handled by an optional downstream **Design
Stage**.
