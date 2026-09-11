# LEKAL 4 — Requirements

The goal of this stage is to transform the validated product structure into detailed product requirements.

At this point, the product idea, business context, scope, product flow, and functional structure have already been defined and validated during the previous stages.

The consultant now uses this information to describe how the product should behave in sufficient detail for solution design and implementation.

---

# Objective

Define the expected product behavior and remove ambiguity from the product concepts established during the previous stages.

The objective of this stage is to establish:

- what users should be able to do
- how the product should behave in different scenarios
- what rules and conditions affect product behavior
- what data the product operates with
- what restrictions and validations apply
- how different parts of the product interact from a functional perspective
- what external interactions must be supported

The requirements describe **what the product must do**, without defining how the technical solution should implement it.

---

# Input

The stage uses the outputs of the previous LEKAL stages:

- **Idea**
- **Frame**
- **Structure**

The **Structure** document is the primary input.

It provides the High-Level Product Flow, Functional Areas, capabilities, and Functional Area Concepts that must now be decomposed into detailed product behavior.

The **Idea** and **Frame** documents provide additional context, including the original problem, customer needs, product scope, integrations, constraints, and decisions made during earlier stages.

---

# Focus Areas

During this stage, the consultant progressively decomposes the product structure into detailed requirements.

The analysis may include:

- user scenarios and use cases
- functional requirements
- business rules
- roles and permissions
- product and domain entities
- entity states and lifecycle rules
- validations and restrictions
- error and alternative behavior
- functional interactions between product areas
- requirements for interactions with external systems
- relevant non-functional requirements

The exact structure and organization of the requirements depend on the product and will be defined separately within the LEKAL methodology.

---

# Process

The consultant reviews the **Structure** document together with the relevant context from **Idea** and **Frame**.

The process follows a general sequence:

1. take each Functional Area and its concept as a basis for decomposition
2. identify the scenarios and behaviors that must be supported
3. define the requirements necessary to describe those behaviors
4. capture relevant rules, conditions, data, states, validations, and exceptions
5. define required functional interactions between different parts of the product and external systems
6. review the resulting requirements for gaps, contradictions, and ambiguity
7. capture remaining assumptions and open questions

Requirements should remain consistent with the validated product scope and structure.

If requirements analysis reveals missing functionality or requires changes to the previously agreed product structure or scope, these changes should be explicitly identified and resolved rather than silently introduced.

---

# Validation

The resulting requirements are reviewed with the client or relevant decision-makers.

The purpose of validation is to:

- confirm that the requirements correctly represent the expected product behavior
- confirm that all critical product scenarios are covered
- validate important business rules and restrictions
- identify missing or incorrect behavior
- resolve critical assumptions, contradictions, and open questions
- confirm changes to the previously agreed product scope or structure, if any

Validation may result in changes to the requirements or require revisiting decisions made during earlier LEKAL stages.

The consultant updates the requirements based on the validation results before proceeding to solution definition.

---

# Output

The output of this stage is **Requirements**.

Requirements contain the validated detailed description of the expected product behavior and provide the basis for technical solution definition.

The internal structure and format of Requirements are defined separately.

---

# Success Criteria

The stage is complete when:

- the product behavior is described in sufficient detail for solution definition
- all major Functional Areas are covered by requirements
- critical user scenarios are described
- relevant business rules, conditions, restrictions, and validations are captured
- required functional interactions are defined
- critical gaps and contradictions have been resolved
- the requirements remain consistent with the agreed product scope and structure
- the requirements have been reviewed and validated with the client or relevant decision-makers

Once these conditions are satisfied, the process can move to the next stage: **Solutions**.

## Failure Conditions

The stage is considered unsuccessful if the expected product behavior cannot be described with sufficient clarity to proceed to solution definition.

This may include situations where:

- critical product scenarios remain undefined
- major Functional Areas contain significant behavioral gaps
- important business rules or conditions remain unclear
- requirements contradict the agreed product scope or structure
- critical assumptions or contradictions remain unresolved after validation
- the client does not confirm the fundamental expected product behavior

In such cases, the consultant should return to the unresolved requirements or revisit the relevant previous LEKAL stage where necessary.