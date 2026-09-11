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
Concepts Stage
↓
Concepts v1 Document
↓
Consultant Review + Visualization
↓
Concepts v2 Document
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
- change MVP scope;
- resolve assumptions;
- introduce new information;
- expose missing product behavior.

The agent cannot simulate external validation.

### Final Output

**Shape v2 Document**

The **Shape v2 Document** incorporates actual validation findings and represents the validated product hypothesis used by the next Stage.

### Core Question

> What product should exist, for whom, why, and within what validated scope?

---

## Stage 3 — Structure

### Purpose

Transform the validated **Shape v2 Document** into a functional Work Breakdown Structure of the product.

The **Structure Stage** determines what functional parts must exist for the validated product to operate coherently.

The Stage does not merely reorganize capabilities explicitly named in Shape.

It performs Functional Discovery to identify capabilities implied by:

- validated product behavior;
- actor responsibilities;
- functional object lifecycles;
- continuation of existing work;
- management of existing work;
- important recovery needs;
- dependencies;
- the complete product value loop.

The primary decomposition is:

```text
Product
↓
Functional Areas
↓
Capability Groups
↓
Capabilities
```

Capability Groups are optional and are used only when they improve understanding.

Capabilities are classified as:

- Validated;
- Derived.

Capabilities also receive a proposed priority:

- Must;
- Should;
- Could.

### Input

**Shape v2 Document**

### First Output

**Structure v1 Document**

The **Structure v1 Document** is the agent's proposed functional decomposition.

It may deliberately include reasonably justified Derived capabilities so that the consultant can evaluate them rather than having potentially necessary functionality silently omitted.

### Consultant Review

The consultant reviews the proposed functional WBS.

During review, the consultant may:

- remove unnecessary capabilities;
- reject Derived capabilities;
- add missing capabilities;
- merge or split capabilities;
- rename capabilities;
- move capabilities between Functional Areas;
- reorganize Capability Groups;
- correct actor responsibility;
- change priorities;
- resolve assumptions;
- identify new structural questions.

The purpose of the review is not to approve the agent's decomposition.

The purpose is to produce the best functional Structure for the product.

### Final Output

**Structure v2 Document**

The **Structure v2 Document** represents the reviewed functional WBS and becomes the primary input to the **Concepts Stage**.

### Core Question

> What functional mechanisms must exist for this product to work?

---

## Stage 4 — Concepts

### Purpose

Transform the reviewed **Structure v2 Document** into a behavioral model of the product's functional concepts.

The **Concepts Stage** determines how the significant functional mechanisms identified during Structure actually work.

For relevant capabilities, the Stage analyzes:

- actors;
- triggers;
- preconditions;
- Actor/System Functional Flows;
- meaningful decisions and validations;
- alternative and negative behavior;
- recovery;
- important Rules;
- functionally important Data;
- meaningful States;
- State Transitions;
- dependencies and connections between Concepts.

The Stage also analyzes Concepts together rather than treating them as isolated mechanisms.

Cross-Concept Consistency checks whether:

- outputs satisfy downstream Preconditions;
- actor responsibilities remain consistent;
- states remain consistent;
- required data exists;
- handoffs are possible;
- negative paths have meaningful outcomes;
- recovery reconnects to the intended value loop.

Behavioral analysis may also expose missing or incorrectly decomposed capabilities in the **Structure v2 Document**.

Such Structural Gaps must be explicit rather than silently hidden inside Concept behavior.

### Input

**Structure v2 Document**

### First Output

**Concepts v1 Document**

The **Concepts v1 Document** is the agent's proposed behavioral model.

It provides rich analytical material for human review and visualization.

### Consultant Review and Visualization

The consultant reviews the **Concepts v1 Document** while transferring the functional model into Miro or another suitable visual workspace.

Visualization is an analytical activity rather than mechanical transcription.

During visualization, the consultant:

- absorbs product context;
- reorganizes information;
- challenges Concept boundaries;
- checks Actor/System behavior;
- discovers missing interactions;
- removes unnecessary behavior;
- identifies inconsistent responsibilities;
- checks relationships spatially;
- discovers missing handoffs;
- challenges Rules and States;
- identifies additional assumptions and open questions.

The consultant may substantially change the agent's proposal.

### Final Output

**Concepts v2 Document**

The **Concepts v2 Document** incorporates consultant findings and represents the reviewed behavioral model.

It becomes the primary input to the **Requirements Stage**.

### Core Question

> How does each significant functional mechanism work?

---

## Stage 5 — Requirements

### Purpose

Transform the reviewed behavioral model in the **Concepts v2 Document** into precise product requirements.

The **Requirements Stage** defines exactly how the system must behave in material cases.

It expands the functional model into specification-level detail.

Depending on the product, this may include:

- detailed scenarios;
- exact business rules;
- field requirements;
- validations;
- constraints;
- permissions;
- alternative scenarios;
- error behavior;
- detailed state transition rules;
- acceptance criteria;
- data requirements;
- functional edge cases.

The Stage should preserve the product behavior established during Concepts while removing ambiguity required for implementation.

### Input

**Concepts v2 Document**

### Output

**Requirements Document**

### Core Question

> Exactly how must the system behave?

---

## Stage 6 — Solutions

### Purpose

Transform validated functional Requirements into implementation-oriented solution decisions.

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

The **Solutions Stage** evaluates implementation choices against the actual product Structure and Requirements.

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

---

## Idea → Shape

**Idea Stage** determines:

> What do we know about the idea?

**Shape Stage** determines:

> What product hypothesis follows from that information?

Idea gathers and structures context.

Shape analyzes it.

---

## Shape → Structure

**Shape Stage** determines:

> What product should exist and what validated value must it deliver?

**Structure Stage** determines:

> What functional mechanisms must exist for that product to work?

Shape defines product direction and validated scope.

Structure decomposes that scope into a functional WBS and discovers implied functionality.

---

## Structure → Concepts

**Structure Stage** determines:

> What functional mechanisms exist?

**Concepts Stage** determines:

> How does each significant functional mechanism work?

Structure identifies capabilities.

Concepts models their behavior.

---

## Concepts → Requirements

**Concepts Stage** determines:

> How does the functional mechanism work conceptually?

**Requirements Stage** determines:

> Exactly how must the system behave in material cases?

Concepts creates a behavioral model.

Requirements turn that model into a precise specification.

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
- analyzing behavioral flows;
- checking coverage;
- checking consistency;
- identifying potential gaps;
- preserving traceability between Stages.

The consultant is responsible for:

- product judgment;
- evaluating whether proposed functionality is actually necessary;
- rejecting plausible but irrelevant functionality;
- resolving ambiguous product meaning;
- challenging priorities;
- synthesizing information;
- visual reasoning;
- recognizing patterns and inconsistencies during visualization;
- making or facilitating product decisions;
- conducting real validation with clients and decision-makers.

Human review is not merely quality control over agent output.

It is part of the analytical process.

---

# Document Lifecycle

Some Stages require more than one version of the same Document because analysis and review represent different states of product knowledge.

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

## Concepts

```text
Concepts v1 Document
↓
Consultant Review + Visualization
↓
Concepts v2 Document
```

The distinction represents agent-proposed behavioral analysis and consultant-reviewed behavioral synthesis.

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

Concepts Stage
    ↓
Concepts v1 Document
    ↓
Consultant Review + Visualization
    ↓
Concepts v2 Document

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
| Structure Stage | Validated Product Hypothesis → Functional WBS | **Structure v2 Document** |
| Concepts Stage | Functional WBS → Behavioral Model | **Concepts v2 Document** |
| Requirements Stage | Behavioral Model → Precise Specification | **Requirements Document** |
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
Specification
↓
Technical Solution
```

Each Stage should reduce a different kind of uncertainty.

A new Stage should exist only when it represents a meaningful transformation in the type of product knowledge being produced.