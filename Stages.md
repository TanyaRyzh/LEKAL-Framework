# LEKAL Stages

LEKAL transforms a vague product idea into buildable product scope through a sequence of analytical Stages.

Each Stage performs a distinct transformation of product knowledge.

The output of one Stage becomes the primary input to the next.

```text
Raw Idea
↓
Idea Stage
↓
Idea Document
↓
Shape Stage
↓
Shape v1 Document
↓
External Validation
↓
Shape v2 Document
↓
Structure Stage
↓
Structure v1 Document
↓
Consultant Review
↓
Structure v2 Document
↓
Behavior Stage
↓
Behavior v1 Document
↓
Consultant Review + Visualization
↓
Behavior v2 Document
↓
Interaction Stage
↓
Wireframes v1
↓
Client Validation
↓
Behavior v3 Document + Wireframes v2
↓
Requirements Stage
↓
Requirements Document
↓
Solutions Stage
↓
Solutions Document
↓
Buildable Product Scope
```

---

## Stage 1 — Idea

### Purpose

Turn a raw product idea into structured product context.

The **Idea Stage** focuses on understanding the idea before attempting to design, evaluate, or decompose the product.

The Stage gathers and structures:

- problem context;
- users and stakeholders;
- expected outcomes;
- constraints;
- existing solutions;
- core interaction;
- assumptions;
- open questions.

The goal is not to solve product uncertainty prematurely.

The goal is to make the initial idea explicit enough for meaningful product analysis.

### Input

- Raw Idea
- Client-provided information
- Existing supporting materials where available

### Output

**Idea Document**

### Core Question

> What do we actually know about the product idea?

---

## Stage 2 — Shape

### Purpose

Transform the **Idea Document** into a validated product and business hypothesis.

The **Shape Stage** analyzes the product from several perspectives:

- Customer Segments;
- Target Market;
- Jobs to Be Done;
- Value Proposition;
- Revenue Streams;
- Competitors and Alternatives;
- Product Stages and Scope;
- Integrations;
- Constraints;
- Potential Tech Stack.

The Stage does not merely document known information.

When important information is uncertain, the consultant determines whether that uncertainty can be reduced through analysis or research.

Where appropriate, the consultant:

- identifies the gap;
- develops hypotheses or alternatives;
- gathers relevant evidence;
- compares options;
- analyzes tradeoffs, risks, and conditions;
- produces a recommendation or candidate set;
- returns the result for validation.

Target Market establishes the market context in which the product is expected to operate.

Where relevant, it may include:

- target geography or markets;
- local, regional, or international market scope;
- primary product language;
- expected localization needs;
- regional conventions;
- market-specific regulatory, legal, or operational conditions.

These findings inform Product Scope, Constraints, Integrations, and downstream functional analysis where relevant.

### Input

**Idea Document**

### First Output

**Shape v1 Document**

The **Shape v1 Document** represents the consultant's analyzed product and business hypothesis before external validation.

### Validation

The consultant visualizes and reviews the proposed Shape with the client or relevant decision-makers.

External validation may:

- confirm hypotheses;
- reject hypotheses;
- correct product direction;
- change Target Market assumptions;
- change MVP scope;
- resolve assumptions;
- introduce new information;
- expose missing product behavior.

The agent cannot simulate external validation.

### Final Output

**Shape v2 Document**

The **Shape v2 Document** incorporates actual validation findings and represents the validated product hypothesis used by the next Stage.

### Core Question

> What product should exist, for whom, in what market, why, and within what validated scope?

---

## Stage 3 — Structure

### Purpose

Transform the validated **Shape v2 Document** into a functional Work Breakdown Structure of the product.

The **Structure Stage** determines what functional mechanisms must exist for the validated product to operate coherently.

The Stage does not merely reorganize Capabilities explicitly named in Shape.

It performs Functional Discovery to identify Capabilities implied by:

- validated product behavior;
- actor responsibilities;
- functional object lifecycles;
- continuation of existing work;
- management of existing work;
- important recovery needs;
- dependencies;
- the complete product value loop;
- cross-cutting product responsibilities implied by the validated product context.

The primary decomposition is:

```text
Product
↓
Functional Areas
↓
Capabilities
```

Capability Groups may be used optionally when they improve readability, but they are not a required level of decomposition.

During analysis, Capabilities are internally classified as:

- Validated;
- Derived.

This classification supports analytical traceability and does not need to appear as a dedicated field in the final **Structure Document**.

Capabilities receive a proposed functional priority:

- High;
- Medium;
- Low.

Priority represents relative functional importance.

It does not redefine Product Stage or release scope established during the **Shape Stage**.

### Product Readiness

The **Structure Stage** also reviews whether the validated product context creates cross-cutting functional responsibilities that may not naturally emerge from the core value loop.

Relevant concerns may include, where applicable:

- privacy and consent;
- account and personal-data lifecycle;
- Target Market and localization needs;
- legal or regulatory interaction;
- product limits or quotas;
- user preferences;
- other cross-cutting product responsibilities.

This is not a generic product checklist.

A Capability is added only when the specific product context creates a justified functional responsibility.

Examples of possible findings may include:

```text
Manage cookie preferences
Delete own account
Change interface language
```

These are examples, not mandatory product functionality.

### Input

**Shape v2 Document**

### First Output

**Structure v1 Document**

The **Structure v1 Document** is the agent's proposed functional decomposition.

It may deliberately include reasonably justified Derived Capabilities so that the consultant can evaluate them rather than having potentially necessary functionality silently omitted.

### Consultant Review

The consultant reviews the proposed functional WBS.

During review, the consultant may:

- remove unnecessary Capabilities;
- reject Derived Capabilities;
- add missing Capabilities;
- merge or split Capabilities;
- rename Capabilities;
- move Capabilities between Functional Areas;
- reorganize optional groupings;
- correct actor responsibility;
- change priorities;
- resolve assumptions;
- identify new structural questions.

The purpose of the review is not to approve the agent's decomposition.

The purpose is to produce the best functional Structure for the product.

### Final Output

**Structure v2 Document**

The **Structure v2 Document** represents the reviewed functional WBS and becomes the primary input to the **Behavior Stage**.

### Core Question

> What functional mechanisms must exist for this product to work?

---

## Stage 4 — Behavior

### Purpose

Transform the reviewed **Structure v2 Document** into a coherent behavioral model of the product.

The **Behavior Stage** determines how the significant functional mechanisms identified during Structure actually behave.

For relevant functionality, the Stage analyzes:

- actors;
- triggers;
- Preconditions;
- actor actions;
- system responses;
- meaningful decisions and conditions;
- alternative and negative behavior;
- recovery;
- important Rules;
- functionally important Data;
- meaningful States;
- State Transitions;
- actions available in different States;
- change consequences;
- invalidation and recalculation behavior;
- connections between behavioral mechanisms;
- meaningful product behavior that must be observable.

### Behavioral Representation

The **Behavior Stage** does not require every mechanism to use the same representation.

Depending on the behavior, appropriate representations may include:

- Actor/System Functional Flow;
- State Machine;
- State Transition Matrix;
- Actions Matrix;
- Decision Table;
- Status Calculation;
- Rules;
- functional Data model;
- relationship model;
- other suitable behavioral representations.

The representation should expose the mechanism clearly with the least unnecessary duplication.

For example:

```text
State Machine
→ What lifecycle States exist?

Transition Matrix
→ Who can move the object between those States?

Actions Matrix
→ What can actors do while the object is in each State?

Status Calculation
→ How is aggregate State derived?
```

Functional Flow is therefore one behavioral representation, not the mandatory representation for every mechanism.

### Behavioral Organization

The **Behavior Document** is normally organized by Functional Area to support consultant review.

Functional Areas are organizational containers.

They are not behavioral boundaries.

Behavioral mechanisms may cross Functional Areas where the product behavior requires it.

### Cross-Cutting Behavior

The **Behavior Stage** defines how cross-cutting Capabilities discovered during Structure actually work.

Depending on the product, this may include behavior related to:

- Terms acceptance;
- Privacy Policy presentation;
- consent and preferences;
- account lifecycle;
- localization preferences;
- limits and quotas;
- other product-wide functional mechanisms.

The **Behavior Stage** does not invent these mechanisms merely because they are common.

Their existence must be justified by upstream product context or Structure.

### Limits and Consequences

When validated limits or quotas exist, the **Behavior Stage** determines their behavioral effect.

A numeric limit alone is not sufficient.

The Stage determines, where relevant:

- when the limit is evaluated;
- what action becomes unavailable or blocked;
- what the actor can do next;
- how the product behaves when capacity becomes available again.

The Stage also analyzes the consequences of changing objects that already participate in product progress.

This may include:

- invalidating existing results;
- resetting States;
- recalculating parent States;
- recalculating aggregate progress;
- requiring another actor to repeat work.

### Observability and Analytics

After the core behavioral model is established, the **Behavior Stage** performs an observability review.

The key question is:

> Which meaningful product behaviors must be observable?

The Stage may identify:

- meaningful analytics events;
- event triggers;
- relevant non-sensitive parameters;
- product funnels or value-loop sequences.

Analytics is not treated as a generic user Capability unless analytics functionality is actually exposed to an actor.

Instrumentation should follow meaningful product behavior rather than arbitrary UI actions.

Analytics behavior must remain consistent with the product's privacy and consent decisions.

### Structural Gaps

Behavioral analysis may expose missing or incorrectly decomposed Capabilities in the **Structure v2 Document**.

Such Structural Gaps must be explicit rather than silently hidden inside the behavioral model.

### Input

**Structure v2 Document**

### First Output

**Behavior v1 Document**

The **Behavior v1 Document** is the agent's proposed behavioral model.

It provides analytical material for human review and visualization.

### Consultant Review and Visualization

The consultant reviews the **Behavior v1 Document** while visualizing relevant behavior in Miro or another suitable visual workspace.

Visualization is an analytical activity rather than mechanical transcription.

During review, the consultant may:

- reorganize behavior for review;
- challenge behavioral boundaries;
- choose different representations;
- correct Functional Flows;
- correct State Machines;
- correct State Transition Matrices;
- correct Actions Matrices;
- challenge status calculations;
- identify missing consequences;
- identify missing behavior;
- remove unnecessary behavior;
- identify inconsistent responsibilities;
- check relationships spatially;
- discover missing handoffs;
- challenge Rules and Data;
- identify Structural Gaps;
- identify additional assumptions and Open Questions.

The consultant may substantially change the agent's proposal.

### Final Output

**Behavior v2 Document**

The **Behavior v2 Document** incorporates Consultant Review findings and represents the reviewed behavioral model.

It becomes the primary input to the **Interaction Stage**.

### Core Question

> How does the product behave?

---

## Stage 5 — Interaction

### Purpose

Transform the reviewed behavioral model in the **Behavior v2 Document** into an interaction model of the product.

The **Behavior Stage** establishes how the product behaves independently of a particular interface representation.

The **Interaction Stage** determines how users interact with that behavior through the product interface.

The Stage translates behavioral mechanisms into an understandable interaction structure.

Depending on the product, this may include:

- screens or views;
- navigation;
- information hierarchy;
- placement and availability of actions;
- representation of meaningful States;
- representation of system feedback;
- representation of negative and recovery behavior;
- relationships between views;
- user movement through important product flows;
- wireframes.

The Stage must preserve the behavior established in the **Behavior v2 Document**.

It must not silently invent or change core product behavior merely to make an interface convenient.

At the same time, interaction modeling is analytical rather than decorative.

Creating wireframes may expose:

- missing navigation;
- unclear information hierarchy;
- missing system feedback;
- inaccessible actions;
- unclear State representation;
- missing interaction steps;
- contradictions in behavior;
- behavior that cannot be represented coherently through the interface.

These findings must be resolved rather than hidden by the wireframe.

### Input

**Behavior v2 Document**

### First Output

**Wireframes v1**

**Wireframes v1** represent the consultant-proposed interaction model before client validation.

They should be editable working artifacts rather than static presentation images where practical.

Wireframes are not expected to define visual design.

Their purpose is to make product interaction concrete enough to review and validate.

### Client Validation

The consultant reviews the proposed interaction model with the client or relevant decision-makers.

The validation surface includes:

- **Behavior v2 Document**;
- **Wireframes v1**.

Client Validation may:

- confirm product behavior;
- change product behavior;
- expose missing behavior;
- confirm or change interaction structure;
- change navigation;
- change information hierarchy;
- change action availability or presentation;
- expose misunderstood user workflows;
- resolve assumptions;
- introduce new information.

The agent cannot simulate Client Validation.

### Final Outputs

Client Validation produces two updated artifacts where necessary:

**Behavior v3 Document**

The **Behavior v3 Document** incorporates behavioral changes resulting from Client Validation.

It represents client-validated product behavior.

**Wireframes v2**

**Wireframes v2** incorporate validated interaction changes.

They represent the client-validated interaction model.

The pair:

```text
Behavior v3 Document
+
Wireframes v2
```

becomes the primary input to the **Requirements Stage**.

### Core Question

> How does the user interact with the defined product behavior?

---

## Stage 6 — Requirements

### Purpose

Transform the client-validated behavioral and interaction models into precise product requirements.

The **Requirements Stage** defines exactly how the system must behave in material cases.

It expands the behavioral and interaction models into specification-level detail.

Depending on the product, this may include:

- detailed scenarios;
- exact business rules;
- field requirements;
- validations;
- constraints;
- permissions;
- alternative scenarios;
- error behavior;
- detailed State Transition Rules;
- acceptance criteria;
- data requirements;
- functional edge cases.

The Stage should preserve the product behavior established in the **Behavior v3 Document** and the validated interaction model represented by **Wireframes v2**, while removing ambiguity required for implementation.

The **Requirements Stage** may identify inconsistencies or missing information in upstream artifacts.

Such findings should be traced to the earliest Stage responsible for that type of product knowledge rather than silently invented inside Requirements.

### Input

Primary inputs:

- **Behavior v3 Document**;
- **Wireframes v2**.

### Output

**Requirements Document**

### Core Question

> Exactly how must the system behave in material cases?

---

## Stage 7 — Solutions

### Purpose

Transform precise product Requirements into implementation-oriented solution decisions.

The **Solutions Stage** determines how the required product behavior can be implemented technically.

Depending on the product, this may include:

- system architecture;
- application components;
- APIs;
- integrations;
- data models;
- storage;
- external services;
- authentication approach;
- infrastructure;
- deployment;
- technical constraints;
- technology selection;
- implementation tradeoffs.

Potential technologies identified during the **Shape Stage** are candidates, not predetermined implementation decisions.

The **Solutions Stage** evaluates implementation choices against the actual product Structure, Behavior, Interaction Model, and Requirements.

### Input

**Requirements Document**

### Output

**Solutions Document**

### Core Question

> How should this product be implemented?

---

# Stage Boundaries

Each LEKAL Stage represents a distinct transformation of product knowledge.

The Stages should not collapse into one another.

When a downstream Stage exposes missing information, identify the earliest Stage responsible for producing that type of knowledge.

Do not solve every discovered problem in the Stage where it happens.

---

## Idea → Shape

**Idea Stage** determines:

> What do we know about the idea?

**Shape Stage** determines:

> What product hypothesis follows from that information?

Idea gathers and structures context.

Shape analyzes it and establishes validated product direction, including relevant market context.

---

## Shape → Structure

**Shape Stage** determines:

> What product should exist and what validated value must it deliver?

**Structure Stage** determines:

> What functional mechanisms must exist for that product to work?

Shape defines product direction, Target Market, value, and validated scope.

Structure decomposes that product into a functional WBS and discovers implied functionality.

---

## Structure → Behavior

**Structure Stage** determines:

> What functional mechanisms exist?

**Behavior Stage** determines:

> How does the product behave?

Structure identifies Capabilities.

Behavior models the mechanisms, lifecycle, Rules, consequences, recovery, and relationships that make those Capabilities work.

---

## Behavior → Interaction

**Behavior Stage** determines:

> How does the product behave?

**Interaction Stage** determines:

> How does the user interact with that behavior through the product interface?

Behavior defines product logic independently of a specific interface representation.

Interaction transforms that logic into screens, views, navigation, information hierarchy, available actions, State representation, system feedback, and wireframes.

The **Interaction Stage** is not merely visualization of Behavior.

It creates a different type of product knowledge: the interaction model.

---

## Interaction → Requirements

**Interaction Stage** determines:

> How does the user interact with the defined product behavior?

**Requirements Stage** determines:

> Exactly how must the system behave in material cases?

Interaction produces client-validated behavior and interaction artifacts.

Requirements turn them into precise implementation-independent specification.

---

## Requirements → Solutions

**Requirements Stage** determines:

> What must the system do?

**Solutions Stage** determines:

> How should the system implement it?

Requirements remain implementation-independent where possible.

Solutions make technical decisions.

---

# Human and Agent Responsibilities

LEKAL combines machine analysis with human product judgment.

The agent is particularly useful for:

- processing large amounts of context;
- maintaining breadth across the product;
- generating hypotheses;
- discovering implied functionality;
- systematically decomposing product scope;
- identifying lifecycle and recovery needs;
- analyzing behavioral mechanisms;
- proposing appropriate behavioral representations;
- checking coverage;
- checking consistency;
- identifying potential gaps;
- identifying observable product behavior;
- preserving traceability between Stages.

The consultant is responsible for:

- product judgment;
- evaluating whether proposed functionality is actually necessary;
- rejecting plausible but irrelevant functionality;
- resolving ambiguous product meaning;
- challenging priorities;
- synthesizing information;
- visual reasoning;
- selecting and challenging behavioral representations;
- recognizing patterns and inconsistencies during visualization;
- translating behavior into a coherent interaction model;
- making or facilitating product decisions;
- conducting real validation with clients and decision-makers.

Human review is not merely quality control over agent output.

It is part of the analytical process.

---

# Document and Artifact Lifecycle

Some Stages require more than one version of the same Document or artifact because analysis, review, and validation represent different states of product knowledge.

## Shape

```text
Shape v1 Document
↓
External Validation
↓
Shape v2 Document
```

The distinction represents pre-validation and post-validation product knowledge.

---

## Structure

```text
Structure v1 Document
↓
Consultant Review
↓
Structure v2 Document
```

The distinction represents agent-proposed functional decomposition and consultant-reviewed functional decomposition.

---

## Behavior

```text
Behavior v1 Document
↓
Consultant Review + Visualization
↓
Behavior v2 Document
```

The distinction represents agent-proposed behavioral analysis and consultant-reviewed behavioral synthesis.

---

## Interaction

```text
Behavior v2 Document
↓
Interaction Modeling
↓
Wireframes v1
↓
Client Validation
↓
Behavior v3 Document + Wireframes v2
```

The **Interaction Stage** deliberately validates behavior and interaction together.

Interaction modeling may expose product decisions that cannot be reliably validated from an abstract behavioral model alone.

Client feedback may therefore change both:

- the behavioral model;
- the interaction model.

The resulting **Behavior v3 Document** and **Wireframes v2** represent the client-validated basis for Requirements.

---

# Complete LEKAL Flow

```text
Raw Idea

    ↓

Idea Stage
    ↓
Idea Document

    ↓

Shape Stage
    ↓
Shape v1 Document
    ↓
External Validation
    ↓
Shape v2 Document

    ↓

Structure Stage
    ↓
Structure v1 Document
    ↓
Consultant Review
    ↓
Structure v2 Document

    ↓

Behavior Stage
    ↓
Behavior v1 Document
    ↓
Consultant Review + Visualization
    ↓
Behavior v2 Document

    ↓

Interaction Stage
    ↓
Wireframes v1
    ↓
Client Validation
    ↓
Behavior v3 Document
+
Wireframes v2

    ↓

Requirements Stage
    ↓
Requirements Document

    ↓

Solutions Stage
    ↓
Solutions Document

    ↓

Buildable Product Scope
```

---

# LEKAL Transformation Model

At the highest level, LEKAL progressively transforms uncertainty into implementation-ready knowledge.

| Stage | Transformation | Primary Output |
|---|---|---|
| Idea Stage | Raw Idea → Structured Context | **Idea Document** |
| Shape Stage | Structured Context → Validated Product Hypothesis | **Shape v2 Document** |
| Structure Stage | Validated Product Hypothesis → Functional Structure | **Structure v2 Document** |
| Behavior Stage | Functional Structure → Behavioral Model | **Behavior v2 Document** |
| Interaction Stage | Behavioral Model → Validated Interaction Model | **Behavior v3 Document** + **Wireframes v2** |
| Requirements Stage | Validated Behavior + Interaction → Precise Specification | **Requirements Document** |
| Solutions Stage | Precise Specification → Technical Solution | **Solutions Document** |

The resulting chain is:

```text
Context
↓
Product Hypothesis
↓
Functional Structure
↓
Behavioral Model
↓
Interaction Model
↓
Specification
↓
Technical Solution
```

Each Stage should reduce a different kind of uncertainty.

A new Stage should exist only when it represents a meaningful transformation in the type of product knowledge being produced.