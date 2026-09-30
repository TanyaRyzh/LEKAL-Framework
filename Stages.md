# LEKAL Stages

LEKAL transforms a vague product idea into buildable product scope through a sequence of analytical Stages.

Each Stage performs a distinct transformation of product knowledge.

LEKAL contains:

- **Core Stages** — the default analytical path;
- **Optional Stages** — used when a specific project requires their output;
- **Validation checkpoints** — human activities that validate or change product knowledge but are not separate Stages.

---

# Core Flow

```text
Raw Idea
↓
Idea Stage
↓
Idea Document
↓
Domain Stage
↓
Domain Document
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
Interaction v1
↓
Consultant Review
↓
Interaction v2
↓
Client Validation
↓
Behavior v3 Document + Interaction v3
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

# Optional Stages

Optional Stages are not required for every LEKAL project.

They are introduced when the project requires the additional type of product knowledge they produce.

```text
Shape v2
└── Estimation*

Requirements
└── Design*
```

`*` = Optional Stage.

An Optional Stage does not become part of the Core Flow merely because it is used on a particular project.

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

## Stage 2 — Domain

### Purpose

Build the minimum domain understanding required to reason about the product correctly before product shaping begins.

The **Domain Stage** prepares the Consultant and downstream analytical Stages to work with the product in its actual domain context.

The Stage may identify and structure:

- domain terminology;
- important domain concepts;
- typical actors and responsibilities;
- important domain entities and relationships;
- common processes;
- common lifecycle patterns;
- relevant regulations or standards;
- common operational constraints;
- common industry practices;
- external systems or institutions relevant to the domain;
- other domain knowledge required to understand the product context.

The purpose is not to produce an exhaustive industry study.

The purpose is to establish enough shared domain knowledge to prevent downstream product analysis from being based on incorrect assumptions or missing domain context.

### Domain Knowledge vs Product Truth

The **Domain Document** describes contextual knowledge about the domain.

It does not define the product.

A pattern, process, rule, actor, object, or convention may be common in the domain without being applicable to the specific product.

Domain knowledge must therefore remain distinguishable from product-specific decisions.

A common domain pattern must not silently become:

- a product Capability;
- a product Rule;
- a requirement;
- a scope decision;
- a technical constraint.

Product-specific decisions are made in downstream Stages.

### Input

**Idea Document**

The Idea Document establishes the product context and determines which domain areas are relevant enough to investigate.

### Output

**Domain Document**

The Domain Document contains the domain knowledge required to support downstream product analysis.

Its primary immediate consumer is the **Shape Stage**.

### Core Question

> What do we need to understand about this domain before we can reason about the product correctly?

---

## Stage 3 — Shape

### Purpose

Transform the **Idea Document**, informed by relevant domain knowledge, into a validated product and business hypothesis.

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

When important information is uncertain, the Consultant determines whether that uncertainty can be reduced through analysis or research.

Where appropriate, the Consultant:

- identifies the gap;
- develops hypotheses or alternatives;
- gathers relevant evidence;
- compares options;
- analyzes tradeoffs, risks, and conditions;
- produces a recommendation or candidate set;
- returns the result for validation.

Domain knowledge may inform this analysis but must not automatically become product truth.

### Target Market

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

Primary input:

- **Idea Document**

Contextual input:

- **Domain Document**

### First Output

**Shape v1 Document**

The **Shape v1 Document** represents the Consultant's analyzed product and business hypothesis before external validation.

### External Validation

The Consultant visualizes and reviews the proposed Shape with the client or relevant decision-makers.

External Validation may:

- confirm hypotheses;
- reject hypotheses;
- correct product direction;
- change Target Market assumptions;
- change MVP scope;
- resolve assumptions;
- introduce new information;
- expose missing product concerns.

The Agent cannot simulate External Validation.

### Final Output

**Shape v2 Document**

The **Shape v2 Document** incorporates actual validation findings and represents the validated product hypothesis used by the next Stage.

### Core Question

> What product should exist, for whom, in what market, why, and within what validated scope?

---

## Optional Stage — Estimation*

### Purpose

Produce an early implementation estimate when the project requires information about expected effort, cost, timeline, team, or delivery range.

**Estimation is optional.**

It becomes available after Shape because **Shape v2** establishes a validated product hypothesis and scope sufficient for an early estimate.

Estimation does not require the complete downstream product definition produced by Structure, Behavior, Requirements, Design, or Solutions.

Consequently, the estimate must reflect the level of uncertainty that exists at this point in the lifecycle.

The Stage may estimate, where relevant:

- implementation effort;
- delivery range;
- approximate cost;
- team composition;
- major implementation areas;
- major uncertainty drivers;
- assumptions affecting the estimate;
- risks affecting cost or timeline.

Estimation must distinguish known scope from assumptions.

It must not manufacture implementation certainty that does not yet exist.

### Input

**Shape v2 Document**

Relevant upstream Documents remain available as supporting context.

### Output

**Estimation Document**

### Core Question

> What is the likely implementation effort, cost, and delivery range for the currently validated product scope?

---

## Stage 4 — Structure

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

During analysis, Capabilities may be internally classified as:

- Validated;
- Derived.

This classification supports analytical traceability and does not need to appear as a dedicated field in the final Structure Document.

Capabilities may receive a proposed functional priority:

- High;
- Medium;
- Low.

Priority represents relative functional importance.

It does not redefine Product Stage or release scope established during the **Shape Stage**.

### Product Scope Coverage

The Structure Stage should make the identified functional space explicit.

Relevant identified Capabilities should receive an explicit scope decision rather than disappearing from the Structure merely because they are not included in the current Product Stage or release.

Where applicable, Structure should distinguish between:

- functionality included in the current scope;
- functionality explicitly excluded from the current scope;
- other scope categories established by the product context.

The absence of a Capability should not be the only signal that it is outside the current scope.

This makes deliberate exclusions distinguishable from functionality that was simply missed.

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

### Input

**Shape v2 Document**

Relevant Domain knowledge remains available as supporting context where necessary.

### First Output

**Structure v1 Document**

The **Structure v1 Document** is the Agent's proposed functional decomposition.

It may deliberately include reasonably justified Derived Capabilities so that the Consultant can evaluate them rather than having potentially necessary functionality silently omitted.

### Consultant Review

The Consultant reviews the proposed functional WBS.

During review, the Consultant may:

- remove unnecessary Capabilities;
- reject Derived Capabilities;
- add missing Capabilities;
- merge or split Capabilities;
- rename Capabilities;
- move Capabilities between Functional Areas;
- reorganize optional groupings;
- correct actor responsibility;
- change priorities;
- correct scope decisions;
- resolve assumptions;
- identify new structural questions.

The purpose of the review is not to approve the Agent's decomposition.

The purpose is to produce the best functional Structure for the product.

### Final Output

**Structure v2 Document**

The Consultant incorporates review findings and produces the **Structure v2 Document**.

Structure v2 represents the reviewed functional WBS and becomes the primary input to the **Behavior Stage**.

### Core Question

> What functional mechanisms must exist for this product to work, and what is their scope?

---

## Stage 5 — Behavior

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

Functional Flow is one behavioral representation, not the mandatory representation for every mechanism.

### Behavioral Organization

The **Behavior Document** is normally organized by Functional Area to support Consultant Review.

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

Relevant upstream Documents and artifacts remain available as supporting context.

### First Output

**Behavior v1 Document**

The **Behavior v1 Document** is the Agent's proposed behavioral model.

It provides analytical material for human review and visualization.

### Consultant Review and Visualization

The Consultant reviews the **Behavior v1 Document** while visualizing relevant behavior in Miro or another suitable visual workspace.

Visualization is an analytical activity rather than mechanical transcription.

During review, the Consultant may:

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

The Consultant may substantially change the Agent's proposal.

### Final Output

**Behavior v2 Document**

The Consultant incorporates Consultant Review findings and produces the **Behavior v2 Document**.

Behavior v2 represents the Consultant-reviewed behavioral model.

Reviewed behavioral diagrams and other artifacts created or updated during Consultant Review form part of Behavior v2.

Behavior v2 becomes the primary input to the **Interaction Stage**.

### Core Question

> How does the product behave?

---

## Stage 6 — Interaction

### Purpose

Transform the reviewed **Behavior v2** into a visual interaction artifact that makes important product behavior easier to understand, discuss, and validate with the client.

The **Interaction Stage** does not attempt to design the complete product interface.

Its purpose is to provide enough interface representation for important behavioral decisions to become concrete.

The Agent selects the parts of Behavior where visualization materially improves understanding and represents them through a small, coherent set of low-fidelity wireframes.

The wireframes are a communication and validation artifact.

They are not a complete UX specification.

The Stage should prefer a small number of informative screens over exhaustive interface coverage.

### Input

The primary input is the complete Consultant-reviewed **Behavior v2**, including its reviewed behavioral diagrams and other artifacts.

Relevant upstream Documents may be used where additional context is required.

Behavior v2 is authoritative.

The Interaction Stage must preserve established product behavior and scope.

Items explicitly marked Out of Scope must not be introduced.

### Interaction Selection

The Agent identifies behavioral areas where interface representation would materially help the client understand, validate, or challenge the proposed product.

Priority may be given to behavior that:

- represents the core product experience;
- is product-specific;
- involves meaningful State changes;
- involves several actors;
- depends on important entity relationships;
- contains important recovery behavior;
- is difficult to understand from behavioral artifacts alone;
- contains decisions likely to require client validation.

Generic interface behavior does not require visualization merely for coverage.

The key selection question is:

> Would visualizing this behavior make it materially easier for the client to understand, validate, or challenge the proposed product behavior?

If not, the behavior does not require a wireframe merely for completeness.

### Lightweight Interaction Structure

The Agent establishes enough shared interaction structure to make the selected wireframes coherent.

This may include:

- a basic application shell;
- lightweight navigation;
- relevant entity hierarchy;
- recurring page structure;
- actor-specific context where necessary.

This structure is provisional.

It exists to support behavioral understanding.

It does not define the final information architecture, navigation system, or UX.

### First Output

**Interaction v1**

Interaction v1 is the Agent's proposed low-fidelity visual representation of selected parts of Behavior v2.

It should:

- represent selected behavioral flows;
- use understandable screens or views;
- provide sufficient product context;
- remain coherent across related screens;
- show important actor differences where relevant;
- show important actions, States, transitions, or system responses where necessary to understand the Behavior;
- avoid unnecessary interface detail;
- avoid expanding into complete UX design.

The Agent may make reasonable lightweight interaction decisions where necessary to create understandable wireframes.

Such decisions are proposals for Consultant Review.

They do not silently become authoritative product requirements.

### Consultant Review

The Consultant reviews Interaction v1 against Behavior v2.

The Consultant evaluates whether the artifact:

- represents the intended Behavior correctly;
- visualizes the behavioral areas that most benefit from interface representation;
- provides enough context for client discussion;
- introduces unnecessary interface assumptions;
- contains misleading or confusing representations;
- omits behavioral areas that should be visualized;
- reveals gaps or contradictions in Behavior v2.

The Consultant may substantially change the Agent's proposal.

The Consultant may modify the visual artifact directly where this is more efficient.

### Consultant-Reviewed Output

**Interaction v2**

The Consultant produces Interaction v2 based on the review.

Interaction v2 represents the Consultant-reviewed visual interpretation of Behavior v2.

It should be suitable for client validation together with Behavior v2.

It does not need to be a complete UX specification or polished UI.

### Client Validation

The Consultant reviews the following package with the client or relevant decision-makers:

```text
Behavior v2
+
Interaction v2
```

Behavior and Interaction are validated together because visualizing product behavior may make product decisions easier to understand and challenge.

Client Validation may:

- confirm product behavior;
- change product behavior;
- expose missing behavior;
- confirm or challenge the visual representation;
- reveal misunderstood user workflows;
- change assumptions;
- introduce new information.

The Agent cannot simulate Client Validation.

### Client-Validated Outputs

After Client Validation, the Consultant incorporates accepted feedback into both artifacts where required.

The Consultant produces:

**Behavior v3 Document**

and

**Interaction v3**

Behavior v3 represents client-validated product behavior.

Interaction v3 represents the client-validated visual interpretation of that behavior.

The pair:

```text
Behavior v3 Document
+
Interaction v3
```

becomes the primary input to the **Requirements Stage**.

### Core Question

> Which parts of the product behavior need to be made visual so they can be understood and validated with the client?

---

## Stage 7 — Requirements

### Purpose

Transform client-validated behavioral and interaction knowledge into precise product requirements.

The **Requirements Stage** defines exactly how the system must behave in material cases.

It expands validated product knowledge into specification-level detail.

Depending on the product, this may include:

- Functional Requirements;
- detailed Scenarios;
- exact Rules;
- Fields and Validation;
- constraints;
- Roles and Permissions;
- Alternative Scenarios;
- Negative Scenarios;
- error behavior;
- detailed State Transition Rules;
- Acceptance Criteria;
- functional edge cases;
- System Messages;
- Notifications;
- Non-Functional Requirements;
- Glossary.

The Stage should preserve the product behavior established in **Behavior v3** and use **Interaction v3** as validated visual context.

Interaction v3 is not treated as a complete UX specification.

### Requirements vs Solutions

Requirements define what the system must do and the conditions under which the behavior is correct.

Requirements do not define technical implementation unless a technical constraint is itself part of the validated product requirement.

Technical architecture, storage, implementation data models, APIs, infrastructure, and implementation choices belong to the **Solutions Stage**.

### Upstream Gaps

Requirements analysis may expose inconsistencies or missing information in upstream artifacts.

Such findings should be traced to the earliest Stage responsible for that type of product knowledge rather than silently invented inside Requirements.

### Input

Primary inputs:

- **Behavior v3 Document**;
- **Interaction v3**.

Relevant upstream Documents remain available as supporting product context.

### Output

**Requirements Document**

### Core Question

> Exactly how must the system behave in material cases?

---

## Optional Stage — Design*

### Purpose

Transform validated product behavior, interaction context, and precise Requirements into a complete product UX/UI design when the project requires a design deliverable.

**Design is optional.**

The earlier **Interaction Stage** deliberately visualizes only the parts of product behavior required for understanding and client validation.

Design is different.

When Design is included in the project, this is where the product interface is designed comprehensively.

Depending on the project, the Stage may define:

- complete information architecture;
- navigation;
- screens and views;
- actor-specific experiences;
- complete functional interaction coverage;
- action placement and availability;
- representation of States and progress;
- system feedback;
- validation and error states;
- confirmations;
- destructive interactions;
- recovery interactions;
- boundary and terminal states;
- detailed interaction patterns;
- layout;
- responsive behavior;
- components and variants;
- visual hierarchy;
- typography;
- visual language;
- accessibility considerations;
- other UX/UI decisions required by the project.

Design must preserve validated Behavior and Requirements.

It may elaborate interface decisions that were intentionally left unresolved during Interaction.

Design must not silently redefine product behavior or Requirements.

### Input

Primary inputs:

- **Behavior v3 Document**;
- **Interaction v3**;
- **Requirements Document**.

Relevant upstream Documents and artifacts remain available where necessary.

### Output

**Design Artifact**

The exact form and depth of the Design Artifact depend on the project and delivery context.

### Core Question

> How should the validated and specified product work through its complete user interface?

---

## Stage 8 — Solutions

### Purpose

Transform precise product Requirements into implementation-oriented solution decisions.

The **Solutions Stage** determines how the required product behavior can be implemented technically.

Depending on the product, this may include:

- system architecture;
- application components;
- APIs;
- integrations;
- technical data models;
- storage;
- external services;
- authentication approach;
- infrastructure;
- deployment;
- technical constraints;
- technology selection;
- implementation tradeoffs.

Potential technologies identified during the **Shape Stage** are candidates, not predetermined implementation decisions.

The **Solutions Stage** evaluates implementation choices against the actual product Structure, Behavior, and Requirements.

When the optional **Design Stage** has been performed, relevant Design decisions also become input to Solutions where they create implementation constraints or materially affect the technical solution.

### Input

Required primary input:

- **Requirements Document**.

When available and relevant:

- **Design Artifact**.

Relevant upstream product artifacts remain available where required.

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

## Idea → Domain

**Idea Stage** determines:

> What do we know about the idea?

**Domain Stage** determines:

> What do we need to understand about the surrounding domain?

Idea establishes the initial product context.

Domain builds the contextual knowledge required to reason about that product correctly.

Domain knowledge is context, not product truth.

---

## Domain → Shape

**Domain Stage** determines:

> What is generally true or relevant in the surrounding domain?

**Shape Stage** determines:

> What should be true for this specific product?

Domain provides context.

Shape uses that context together with the Idea to establish and validate product-specific hypotheses.

A common domain pattern does not become a product decision without product-specific justification.

---

## Shape → Structure

**Shape Stage** determines:

> What product should exist and what validated value must it deliver?

**Structure Stage** determines:

> What functional mechanisms must exist for that product to work?

Shape defines product direction, Target Market, value, and validated scope.

Structure decomposes that product into a functional WBS, discovers implied functionality, and makes functional scope decisions explicit.

---

## Shape → Estimation*

**Shape Stage** determines the validated product hypothesis and scope.

**Estimation Stage**, when required, determines:

> What is the likely implementation effort, cost, and delivery range at the current level of product definition?

Estimation does not make the product definition more complete.

It evaluates the currently known product and makes uncertainty in the estimate explicit.

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

> Which parts of that behavior need to be made visual so they can be understood and validated?

Behavior defines product logic.

Interaction does not replace or comprehensively redesign that logic as UX.

It selectively translates important behavioral decisions into low-fidelity interface representations for Consultant Review and Client Validation.

---

## Interaction → Requirements

Interaction creates the visual part of a combined client-validation package.

After Consultant Review:

```text
Behavior v2
+
Interaction v2
```

are validated together with the client.

The Consultant then produces:

```text
Behavior v3
+
Interaction v3
```

**Requirements Stage** determines:

> Exactly how must the system behave in material cases?

Requirements transform client-validated product knowledge into precise implementation-independent specification.

---

## Requirements → Design*

When Design is required:

**Requirements Stage** determines:

> What exactly must the system do?

**Design Stage** determines:

> How should that complete required behavior work through the user interface?

Requirements define precise expected system behavior.

Design turns validated and specified product knowledge into a complete UX/UI solution.

Design is not required for the Core Flow to continue.

---

## Requirements → Solutions

**Requirements Stage** determines:

> What exactly must the system do?

**Solutions Stage** determines:

> How should it be implemented technically?

Solutions may proceed directly from Requirements when a separate Design deliverable is not required.

When Design is performed, relevant Design decisions become additional input to Solutions.

---

# Human and Agent Responsibilities

LEKAL combines machine analysis with human product judgment.

The Agent is particularly useful for:

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
- selecting behavioral areas that benefit from visualization;
- producing initial low-fidelity interaction proposals;
- preserving traceability between Stages.

The Consultant is responsible for:

- product judgment;
- evaluating whether proposed functionality is actually necessary;
- rejecting plausible but irrelevant functionality;
- resolving ambiguous product meaning;
- challenging priorities;
- synthesizing information;
- visual reasoning;
- selecting and challenging behavioral representations;
- recognizing patterns and inconsistencies during visualization;
- reviewing and correcting Agent-generated proposals;
- making or facilitating product decisions;
- conducting real validation with clients and decision-makers;
- incorporating Consultant Review findings into reviewed artifacts;
- incorporating Client Validation findings into client-validated artifacts.

Human review is not merely quality control over Agent output.

It is part of the analytical process.

The Agent does not replace external validation.

The Agent must not manufacture client decisions, Consultant decisions, research findings, or validation outcomes.

---

# Document and Artifact Lifecycle

Some Stages require more than one version of the same Document or artifact because Agent generation, Consultant Review, and Client Validation represent different states of product knowledge.

## Idea

```text
Raw Idea
↓
Idea Stage
↓
Idea Document
```

---

## Domain

```text
Idea Document
↓
Domain Stage
↓
Domain Document
```

The Domain Document provides contextual knowledge for Shape.

It does not become product truth merely because it describes common domain practice.

---

## Shape

```text
Idea Document
+
Domain Document
↓
Shape Stage
↓
Shape v1 Document
↓
External Validation
↓
Shape v2 Document
```

The distinction between Shape v1 and Shape v2 represents pre-validation and post-validation product knowledge.

---

## Estimation*

When required:

```text
Shape v2 Document
↓
Estimation Stage
↓
Estimation Document
```

Estimation is a branch from the validated Shape.

It does not replace or block continuation into Structure.

---

## Structure

```text
Shape v2 Document
↓
Structure Stage
↓
Structure v1 Document
↓
Consultant Review
↓
Structure v2 Document
```

Structure v1 is the Agent's proposal.

The Consultant incorporates review findings and produces Structure v2.

---

## Behavior

```text
Structure v2 Document
↓
Behavior Stage
↓
Behavior v1 Document
↓
Consultant Review + Visualization
↓
Behavior v2 Document
```

Behavior v1 is the Agent's proposal.

The Consultant performs the analytical review and produces Behavior v2.

Reviewed behavioral diagrams and other review artifacts form part of Behavior v2.

---

## Interaction

```text
Behavior v2 Document
↓
Interaction Stage
↓
Interaction v1
↓
Consultant Review
↓
Interaction v2
```

Interaction v1 is the Agent's proposal.

The Consultant performs the review and produces Interaction v2.

Interaction v2 is intentionally not a complete UX specification.

---

## Client Validation

```text
Behavior v2 Document
+
Interaction v2
↓
Client Validation
↓
Consultant incorporates accepted feedback
↓
Behavior v3 Document
+
Interaction v3
```

Behavior and Interaction are deliberately validated together.

Client feedback may change either or both artifacts.

The Consultant produces the client-validated versions.

The Agent does not independently create Behavior v3 or Interaction v3.

---

## Requirements

```text
Behavior v3 Document
+
Interaction v3
↓
Requirements Stage
↓
Requirements Document
```

Requirements convert client-validated product knowledge into precise specification.

---

## Design*

When required:

```text
Behavior v3 Document
+
Interaction v3
+
Requirements Document
↓
Design Stage
↓
Design Artifact
```

Design is an optional downstream branch.

Its absence does not prevent the Core Flow from continuing to Solutions.

---

## Solutions

Without Design:

```text
Requirements Document
↓
Solutions Stage
↓
Solutions Document
```

When Design is performed:

```text
Requirements Document
+
Design Artifact
↓
Solutions Stage
↓
Solutions Document
```

Solutions translate specified product behavior and, where relevant, Design constraints into technical implementation decisions.

---

# Complete LEKAL Flow

```text
Raw Idea

    ↓

Idea Stage
    ↓
Idea Document

    ↓

Domain Stage
    ↓
Domain Document

    ↓

Shape Stage
    ↓
Shape v1 Document
    ↓
External Validation
    ↓
Shape v2 Document

    ├──────────────→ Estimation Stage*
    │                    ↓
    │               Estimation Document
    │
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
Interaction v1
    ↓
Consultant Review
    ↓
Interaction v2

    ↓

Client Validation

    ↓

Consultant incorporates accepted feedback

    ↓

Behavior v3 Document
+
Interaction v3

    ↓

Requirements Stage
    ↓
Requirements Document

    ├──────────────→ Design Stage*
    │                    ↓
    │               Design Artifact
    │                    │
    └────────────────────┤
                         ↓

                   Solutions Stage
                         ↓
                   Solutions Document

                         ↓

                 Buildable Product Scope
```

`*` = Optional Stage.

---

# LEKAL Transformation Model

At the highest level, LEKAL progressively transforms uncertainty into implementation-ready knowledge.

## Core Stages

| Stage | Transformation | Primary Output |
|---|---|---|
| Idea Stage | Raw Idea → Structured Context | **Idea Document** |
| Domain Stage | Product Context → Relevant Domain Knowledge | **Domain Document** |
| Shape Stage | Context + Domain Knowledge → Validated Product Hypothesis | **Shape v2 Document** |
| Structure Stage | Validated Product Hypothesis → Reviewed Functional Structure | **Structure v2 Document** |
| Behavior Stage | Functional Structure → Consultant-Reviewed Behavioral Model | **Behavior v2 Document** |
| Interaction Stage | Reviewed Behavioral Model → Consultant-Reviewed Visual Validation Artifact | **Interaction v2** |
| Requirements Stage | Client-Validated Product Knowledge → Precise Specification | **Requirements Document** |
| Solutions Stage | Precise Specification → Technical Solution | **Solutions Document** |

Between Interaction and Requirements, Client Validation transforms:

```text
Behavior v2 + Interaction v2
↓
Behavior v3 + Interaction v3
```

## Optional Stages

| Stage | Transformation | Primary Output |
|---|---|---|
| Estimation* | Validated Product Hypothesis → Early Delivery Estimate | **Estimation Document** |
| Design* | Validated Product + Specification → Complete UX/UI Solution | **Design Artifact** |

The Core transformation chain is:

```text
Context
↓
Domain Understanding
↓
Product Hypothesis
↓
Functional Structure
↓
Behavioral Model
↓
Visual Validation
↓
Client-Validated Product Knowledge
↓
Specification
↓
Technical Solution
```

Optional transformations are introduced when the project requires them:

```text
Product Hypothesis
↓
Estimation*
```

and:

```text
Client-Validated Product Knowledge
+
Specification
↓
Design*
```

Each Stage should reduce a different kind of uncertainty.

A new Stage should exist only when it represents a meaningful transformation in the type of product knowledge being produced.