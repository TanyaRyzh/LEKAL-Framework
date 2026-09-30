# Domain Stage

## Purpose

The purpose of the **Domain Stage** is to build enough domain understanding to reason about the product correctly before product shaping begins.

A product idea usually exists within a domain that has its own:

- terminology;
- actors;
- entities;
- processes;
- lifecycle patterns;
- rules and conventions;
- regulations or standards;
- external systems;
- operational constraints.

Some of this knowledge may already be available from the client.

Some may require research.

Without sufficient domain context, downstream product analysis may be based on incorrect assumptions, misuse domain terminology, overlook important constraints, or propose product behavior that does not fit the environment in which the product must operate.

The Domain Stage therefore creates a structured domain knowledge base that can be used by the Consultant and downstream analytical work.

The goal is not to become a domain expert or produce an exhaustive industry study.

The goal is to understand the parts of the domain that are materially relevant to the product.

---

# Objective

The objectives of the Domain Stage are to:

- identify which parts of the domain are relevant to the product;
- establish a shared vocabulary;
- understand important domain actors and their responsibilities;
- identify important domain entities and relationships;
- understand common domain processes and lifecycle patterns;
- identify relevant regulations, standards, conventions, and operational constraints;
- identify external systems, institutions, or infrastructure relevant to the domain;
- distinguish established domain knowledge from assumptions and uncertain information;
- provide sufficient domain context for the Shape Stage.

The Domain Stage should reduce the risk of making product decisions based on an incomplete or incorrect understanding of the surrounding domain.

---

# Input

The primary input is the:

**Idea Document**

The Idea Document establishes the initial product context and helps determine which areas of the domain are relevant enough to investigate.

Additional input may include:

- materials provided by the client;
- existing product documentation;
- domain documentation;
- regulations and standards;
- public documentation;
- industry materials;
- documentation of relevant external systems;
- other reliable sources of domain knowledge.

The Domain Stage should investigate only information that is reasonably relevant to the product context established during the Idea Stage.

---

# Domain Knowledge vs Product Truth

The Domain Stage describes the environment in which the product exists.

It does not define the product itself.

This distinction is fundamental.

A pattern may be:

- common in the domain;
- required by regulation;
- supported by an external system;
- used by competitors;
- considered industry practice;

without automatically becoming a product requirement.

For example:

```text
Domain Knowledge

"Systems in this domain commonly support X."

does not mean:

Product Decision

"This product must support X."
```

Domain knowledge may influence downstream product decisions, but those decisions must be made explicitly in the appropriate Stage.

The Agent must not silently convert common domain practices into:

- Product Scope;
- Capabilities;
- Product Rules;
- Requirements;
- technical constraints.

Where the relevance of a domain finding to the product is uncertain, preserve the finding as domain context rather than turning it into product truth.

---

# Focus Areas

The Domain Stage investigates only the Focus Areas relevant to the specific product.

Not every project requires every Focus Area.

---

## 1. Domain Terminology

Identify terminology required to understand and discuss the domain correctly.

For each important term, determine:

- what it means;
- whether the meaning is standardized or context-dependent;
- whether similar terms have materially different meanings;
- whether terminology differs between actors, markets, jurisdictions, or systems.

Avoid creating a generic industry glossary.

Include terminology that materially supports understanding of the product context.

---

## 2. Domain Actors

Identify actors that play important roles in the surrounding domain.

Actors may include:

- individuals;
- organizations;
- professional roles;
- regulators;
- service providers;
- intermediaries;
- institutions;
- external systems.

For relevant actors, understand:

- their role in the domain;
- their responsibilities;
- important relationships with other actors;
- where they participate in relevant domain processes.

Domain Actors are not automatically Product Actors.

The Shape and downstream Stages determine which actors actually participate in the product.

---

## 3. Domain Entities and Relationships

Identify important objects, records, resources, or concepts that exist in the domain.

For relevant entities, understand:

- what the entity represents;
- who creates or owns it where relevant;
- important relationships with other entities;
- important lifecycle characteristics;
- terminology or identifiers associated with it.

The purpose is to understand the domain model sufficiently for product analysis.

The Domain Stage does not define the product's technical data model.

---

## 4. Domain Processes

Identify common domain processes that are materially relevant to the product idea.

For each relevant process, understand:

- participating actors;
- major steps;
- important handoffs;
- important inputs and outputs;
- important decisions;
- dependencies;
- common exceptions where they materially affect understanding.

The goal is not to document every possible operational process.

The goal is to understand the processes the proposed product may interact with, support, replace, or change.

---

## 5. Domain Lifecycles

Identify important lifecycle patterns where domain objects or processes move through meaningful states.

Examples may include:

- application lifecycles;
- order lifecycles;
- approval lifecycles;
- transaction lifecycles;
- document lifecycles;
- membership or accreditation lifecycles.

Where relevant, understand:

- major states;
- important transitions;
- actors responsible for transitions;
- terminal states;
- common recovery or reversal patterns.

These lifecycles provide domain context.

They do not automatically define Product States.

---

## 6. Regulations and Standards

Identify regulations, standards, or formal rules that may materially affect the product context.

Where relevant, determine:

- what the rule or standard governs;
- which actors or activities it applies to;
- under what conditions it applies;
- whether applicability depends on geography, market, product type, or business model;
- which source establishes the rule.

Distinguish:

```text
Regulatory requirement
```

from:

```text
Common industry practice
```

and from:

```text
Product decision
```

Do not convert a potentially relevant regulation into a product requirement before its applicability to the product has been established.

---

## 7. External Systems and Institutions

Identify external systems, services, platforms, institutions, or infrastructure that are materially relevant to the domain.

For each relevant item, understand:

- its role in the domain;
- which actors interact with it;
- what information or operations it provides;
- whether interaction with it is mandatory, common, or optional;
- relevant constraints or dependencies.

This analysis provides context for downstream integration decisions.

An external system being common in the domain does not automatically mean that the product must integrate with it.

---

## 8. Domain Constraints and Conventions

Identify domain-specific conditions that materially constrain how products or processes operate.

These may include:

- operational conventions;
- timing constraints;
- identity or verification conventions;
- standard identifiers;
- record-keeping expectations;
- market conventions;
- jurisdiction-specific practices;
- dependencies on physical-world processes.

Separate mandatory constraints from common practices wherever possible.

---

# Research

Domain analysis may require external research.

Research should be driven by the product context rather than by an attempt to document the entire domain.

Before researching, determine:

1. what domain knowledge is missing;
2. why it matters for understanding the product;
3. what type of source could answer the question.

Prefer authoritative sources where available, particularly for:

- regulation;
- standards;
- formal terminology;
- official processes;
- external system behavior.

Industry sources, professional materials, competitor information, and other secondary sources may be used to understand common practices and patterns.

When sources disagree, preserve the disagreement rather than manufacturing certainty.

When reliable information cannot be established, record the uncertainty explicitly.

---

# Process

## Step 1 — Read the Idea Document

Read the complete Idea Document and available supporting materials.

Identify:

- the apparent product domain;
- domain areas directly involved in the idea;
- terminology requiring clarification;
- actors or entities requiring domain understanding;
- processes the product appears to interact with;
- potentially relevant regulatory or operational context;
- explicit domain assumptions;
- important knowledge gaps.

Do not begin with a generic domain checklist.

Begin with the product context.

---

## Step 2 — Define Domain Research Scope

Determine which domain areas require investigation.

Prioritize areas where missing knowledge could materially affect:

- interpretation of the Idea;
- Shape hypotheses;
- Product Scope;
- Target Market;
- actor understanding;
- Constraints;
- Integrations;
- downstream product analysis.

Exclude domain areas that have no meaningful relationship to the product.

---

## Step 3 — Gather Domain Knowledge

Use available project materials and, where necessary, external research to investigate the selected domain areas.

For each important finding, distinguish between:

- established information;
- common patterns or practices;
- source-specific information;
- assumptions;
- unresolved questions.

Preserve source context where it matters.

---

## Step 4 — Build the Domain Model

Organize the gathered knowledge into a coherent representation of the relevant domain.

Depending on the product, this may include:

- glossary;
- actor map;
- entity relationship overview;
- process overview;
- lifecycle model;
- regulatory context;
- external ecosystem;
- domain constraints.

Do not create an artifact merely because the methodology lists it.

Use only representations that materially improve domain understanding.

---

## Step 5 — Review Relevance

Review each significant domain finding against the product context.

Ask:

> Does understanding this materially improve our ability to reason about the product?

Remove irrelevant detail.

The Domain Document should provide useful context rather than become an encyclopedia.

---

## Step 6 — Separate Context from Product Decisions

Review the Domain Document for accidental product definition.

Check whether any domain finding has silently been transformed into:

- required Product Scope;
- a Capability;
- a Product Rule;
- an integration requirement;
- a technical solution.

Where this has happened without product-specific justification, return the statement to domain context.

---

## Step 7 — Identify Open Questions

Record important questions that could not be resolved through available information or research.

An Open Question should be retained when its answer could materially affect downstream product analysis.

Do not create Open Questions for insignificant domain details.

---

## Step 8 — Produce the Domain Document

Create the Domain Document using the relevant sections of the template.

The document should be:

- product-relevant;
- concise enough to be usable;
- sufficiently detailed to support Shape;
- explicit about uncertainty;
- clear about the difference between domain knowledge and product decisions.

---

# Output

The output of the Domain Stage is:

**Domain Document**

The Domain Document provides the contextual knowledge required for product analysis.

Its primary immediate consumer is the **Shape Stage**.

The Domain Document does not define Product Scope.

---

# Domain Document Template

```md
# [Product Name] — Domain

## Domain Overview

[Short explanation of the domain context relevant to the product.]

## Terminology

| Term | Meaning | Notes |
|---|---|---|

## Domain Actors

### [Actor]

**Role in the Domain**

...

**Responsibilities**

- ...

**Relevant Relationships**

- ...

## Domain Entities

### [Entity]

**Description**

...

**Important Relationships**

- ...

**Lifecycle Notes**

- ...

## Domain Processes

### [Process]

**Purpose**

...

**Actors**

- ...

**High-Level Flow**

1. ...
2. ...
3. ...

**Important Conditions / Exceptions**

- ...

## Domain Lifecycles

### [Lifecycle]

[Suitable lifecycle representation.]

## Regulations and Standards

### [Regulation / Standard]

**Applies To**

...

**Relevant Domain Rule**

...

**Source / Evidence**

...

**Product Relevance**

[Known relevance, possible relevance, or not yet established.]

## External Systems and Institutions

### [System / Institution]

**Role in the Domain**

...

**Relevant Interactions**

- ...

**Constraints / Dependencies**

- ...

## Domain Constraints and Conventions

### [Constraint / Convention]

...

## Common Domain Patterns

### [Pattern]

...

**Status**

Common practice / convention / observed pattern / other.

**Product Relevance**

Not automatically a product requirement.

## Open Questions

- ...
```

Sections that are not relevant to the product may be omitted.

Additional representations may be used when they materially improve domain understanding.

---

# Completion Criteria

The Domain Stage is complete when:

- the domain areas materially relevant to the product have been identified;
- terminology required for downstream analysis is sufficiently understood;
- important domain actors and entities are understood where relevant;
- important domain processes and lifecycles are understood where relevant;
- relevant regulations, standards, external systems, and constraints have been investigated to the level necessary for product analysis;
- important uncertainty is explicit;
- common domain practices have not been silently converted into product requirements;
- irrelevant domain detail has been excluded;
- the Domain Document provides enough context to begin Shape without relying on major unstated domain assumptions.

The Domain Stage does not require exhaustive domain knowledge.

Completion means:

> enough domain understanding to reason about this product correctly.

---

# Stage Boundary

The **Domain Stage** determines:

> What is generally true or relevant in the surrounding domain?

The **Shape Stage** determines:

> What should be true for this specific product?

Domain provides context.

Shape makes product-specific hypotheses and decisions.

The boundary should remain explicit throughout the methodology.