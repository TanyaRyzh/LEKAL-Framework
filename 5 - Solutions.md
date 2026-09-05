# LEKAL 5 — Solutions

The goal of this stage is to transform the validated product requirements into a technical solution that can be used as the basis for implementation.

At this point, the expected product behavior has already been described and validated during the Requirements stage.

The consultant now analyzes the requirements from a technical perspective and defines how the system should be structured to support them.

The purpose of this stage is not to document every implementation detail, but to create a sufficiently clear technical model of the system for development to begin.

---

# Objective

Define the technical shape of the system required to implement the validated product requirements.

The objective of this stage is to establish:

- what major technical components the system consists of
- how those components interact
- how important domain entities are represented
- how entity states and lifecycles are handled
- how data moves through the system
- how external systems and services interact with the product
- how key product scenarios are supported technically
- which important technical decisions and constraints affect implementation

The solution should explain **how the system is expected to support the defined product behavior** without prescribing unnecessary implementation details.

---

# Input

The primary input for this stage is the validated **Requirements** produced during LEKAL 4.

The consultant may also refer to the outputs of previous stages where additional product context is required:

- **Idea**
- **Frame**
- **Structure**

The Requirements define the expected product behavior.

The previous documents provide supporting context such as product scope, constraints, integrations, Functional Areas, and decisions made during earlier stages.

---

# Focus Areas

During this stage, the consultant translates product requirements into appropriate technical models.

Depending on the product and the complexity of the solution, the analysis may include:

### System Structure

Identify the major technical components, services, modules, or other structural elements required to support the product.

Define their primary responsibilities and relationships.

### Domain and Data Model

Define the important domain entities, their key characteristics, and relationships where this information is necessary for solution design.

### States and Lifecycles

Define states and transitions for entities with meaningful or complex lifecycles.

State diagrams may be used where they help clarify system behavior.

### System Interactions

Define how system components interact during important product scenarios.

Sequence diagrams or similar interaction models may be used where they help clarify the solution.

### Integrations

Define how the system interacts with external systems and services.

This may include:

- integration boundaries
- exchanged data
- interaction direction
- triggers
- dependencies
- relevant interface expectations

Detailed interface contracts may be defined where required.

### Data Flows

Define how important data enters, moves through, changes within, and leaves the system where this is necessary to understand the solution.

### Technical Decisions and Constraints

Capture important technical decisions, assumptions, limitations, and constraints that affect implementation.

---

# Process

The consultant reviews the validated Requirements and determines which technical models are necessary to describe the solution.

The process follows a general sequence:

1. identify the major technical responsibilities implied by the Requirements
2. define the high-level system structure required to support them
3. identify important domain entities and relationships
4. model states and lifecycles where relevant
5. model interactions for technically significant scenarios
6. define required integrations and data flows
7. capture important technical decisions, assumptions, and constraints
8. review the resulting solution for gaps, contradictions, and unnecessary complexity
9. verify that the solution covers the validated Requirements

The exact set of models and diagrams depends on the product.

Only artifacts that help explain, validate, or implement the solution should be created.

A diagram or model should not be produced solely because it is part of a particular notation or methodology.

---

# Validation

The resulting solution is reviewed with the relevant technical stakeholders.

Depending on the project, this may include:

- developers
- technical leads
- solution or system architects
- integration specialists
- infrastructure specialists
- other relevant technical experts

The purpose of validation is to:

- confirm that the proposed solution can support the Requirements
- validate major technical responsibilities and system boundaries
- review important interactions and data flows
- validate integration assumptions
- identify technical gaps or contradictions
- identify unnecessary complexity
- resolve critical technical assumptions and open questions

Technical validation may result in changes to the solution.

If technical analysis reveals a problem with the previously defined product behavior, scope, or requirements, the relevant earlier LEKAL stage should be revisited.

---

# Output

The output of this stage is **Solutions**.

Solutions contain the technical models and decisions required to describe how the validated product requirements should be implemented.

Depending on the product, Solutions may include:

- high-level system structure
- component or module models
- domain and data models
- state diagrams
- sequence diagrams
- integration models
- data flow diagrams
- interface definitions
- technical decisions
- technical constraints and assumptions

The exact structure and format of Solutions depend on the product and are defined separately.

Not every product requires every type of model or diagram.

---

# Success Criteria

The stage is complete when:

- the technical structure required to support the product is understood
- the validated Requirements are covered by the proposed solution
- major system responsibilities and boundaries are defined
- important domain entities and relationships are understood
- relevant states and lifecycles are defined
- technically significant interactions are described
- required integrations and important data flows are defined
- critical technical decisions, constraints, and assumptions are captured
- critical technical gaps and contradictions have been resolved
- the solution has been reviewed with the relevant technical stakeholders

Once these conditions are satisfied, the product definition is sufficiently detailed to proceed to implementation.

## Failure Conditions

The stage is considered unsuccessful if a coherent technical solution cannot be established based on the validated Requirements.

This may include situations where:

- important Requirements cannot be supported by the proposed solution
- major system responsibilities or boundaries remain unclear
- critical integrations cannot be defined
- technically significant interactions remain ambiguous
- critical technical constraints make the proposed product behavior infeasible
- major technical assumptions remain unresolved
- the relevant technical stakeholders cannot confirm the viability of the proposed solution

In such cases, the consultant should revise the solution or return to the relevant previous LEKAL stage where product or requirements decisions need to be reconsidered.