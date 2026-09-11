# LEKAL 3 — Structure

## Goal

Transform the validated **Shape v2 Document** into a coherent functional structure of the product.

During the **Structure Stage**, the consultant decomposes the product into Functional Areas, identifies the capabilities required within each area, and develops the key functional flows between users and the system.

The result should show how the product works as a connected system at a functional level, while remaining above detailed requirements and technical implementation.

---

## Objective

Create a functional model of the product that:

- represents the complete end-to-end product flow;
- decomposes the product into meaningful Functional Areas;
- identifies the user-visible capabilities required within each Functional Area;
- describes the key functional flows between actors and the system;
- captures key rules, data constraints, states and decisions where they materially define the functional structure;
- shows how Functional Areas connect to each other;
- identifies structural assumptions and open questions;
- provides a stable basis for the **Requirements Stage**.

---

## Input

The primary input is the validated **Shape v2 Document**.

The consultant may also use:

- validation findings from the **Shape Stage**;
- existing product materials;
- relevant client-provided materials;
- supporting information required to understand the validated product scope.

The **Structure Stage** must not use an unvalidated **Shape v1 Document** as the validated basis for product structure.

---

## Core Structure Principle

The **Structure Stage** defines how the validated product scope is organized into a working functional system.

The primary decomposition is:

**Product Flow → Functional Areas → Capabilities → Functional Flows**

The decomposition should be driven by how users move through the product and how the system supports their goals.

Do not begin from screens, database entities, APIs, services, or technical components.

A Functional Area should represent a meaningful functional responsibility within the product.

A capability should represent something an actor can meaningfully do or achieve within that Functional Area.

A Functional Flow should show how an actor and the system interact to realize a significant capability or connected group of capabilities.

The purpose of the **Structure Stage** is not to exhaustively specify behavior. It should provide enough functional detail to understand how the product works and to expose missing connections, responsibilities, states, rules and flows before detailed requirements are written.

---

## Focus Areas

### 1. High-Level Product Flow

Start with the complete end-to-end product flow derived from the validated **Shape v2 Document**.

The flow should show:

- where the primary user journey starts;
- the major user actions;
- major system transitions;
- interactions between relevant participants;
- important successful and negative/recovery paths;
- the meaningful product outcome.

The High-Level Product Flow acts as the backbone for the rest of the **Structure Stage**.

It should remain high-level and must not become a detailed use case.

---

### 2. Functional Areas

Decompose the High-Level Product Flow into meaningful Functional Areas.

Each Functional Area should:

- have a clear functional responsibility;
- support a meaningful part of the product flow;
- contain a coherent group of capabilities;
- have understandable boundaries relative to other Functional Areas.

Functional Areas should be derived from product behavior rather than from UI screens or technical architecture.

Cross-cutting concerns do not automatically require separate Functional Areas. Keep them cross-cutting when that better represents the product structure.

---

### 3. Capabilities

For each Functional Area, identify the capabilities required for that area to support its part of the product flow.

Capabilities should preferably be expressed from the actor's perspective.

For example:

- User can create a project.
- User can edit own project.
- Client can execute an acceptance scenario.
- Vendor can resolve a reported issue.

Capabilities should be sufficiently decomposed to expose meaningful product behavior.

Avoid capabilities that are so broad that important functional behavior remains hidden.

At the same time, do not decompose capabilities into individual UI controls or low-level system operations.

---

### 4. Functional Flows

Develop the key Functional Flows required to realize the identified capabilities.

A Functional Flow should describe the interaction between an actor and the system from initiation to a meaningful result.

Where relevant, include:

- actor action;
- system response;
- system validation or decision;
- subsequent actor action;
- successful result;
- important alternative or negative path;
- return or recovery point.

Not every capability requires an independent Functional Flow.

Capabilities may participate in the same flow when they form one connected interaction.

Functional Flows should be detailed enough to reveal missing behavior and structural gaps, but should not become exhaustive requirements or use cases.

---

### 5. Key Rules, Data and States

Capture rules, data constraints, states and decisions when they materially define the functional structure or affect a Functional Flow.

Examples include:

- data required to perform a capability;
- important uniqueness or structural constraints;
- states required for a flow to continue;
- transitions between meaningful product states;
- permissions or ownership rules that change available actions;
- limits that materially affect product behavior.

Do not attempt to define every field validation, error message, edge case or business rule during the **Structure Stage**.

Detailed behavior belongs to the **Requirements Stage**.

---

### 6. Connections Between Functional Areas

Identify how Functional Areas connect to each other.

For each important connection, determine:

- what information, state or result moves between the areas;
- what event or action causes the transition;
- which area owns the responsibility before and after the transition;
- whether another area depends on the result.

The complete set of Functional Areas and their connections must support the High-Level Product Flow without unexplained gaps.

---

### 7. Assumptions and Open Questions

During decomposition, explicitly capture structural uncertainty.

Examples include:

- unclear ownership of a capability;
- unresolved access model;
- uncertain state transition;
- unclear boundary between Functional Areas;
- missing decision required to complete a flow;
- alternative ways to organize product behavior.

Do not silently resolve client-specific uncertainty.

Where analysis can reduce uncertainty, analyze the alternatives and record the resulting hypothesis or recommendation.

Where client or decision-maker input is required, retain the issue as an explicit open question for validation.

---

## Process

### Step 1 — Review the validated Shape

Review the **Shape v2 Document** and identify:

- primary users and participants;
- primary JTBD;
- Value Proposition;
- validated MVP scope;
- complete value loop;
- important recovery paths;
- constraints;
- relevant assumptions and open questions.

Do not restart the **Shape Stage**.

Use the validated Shape as the product boundary for Structure.

---

### Step 2 — Build the High-Level Product Flow

Describe the complete functional journey through the product.

Verify that the flow reaches the meaningful outcome defined by the relevant JTBD.

Include important negative and recovery paths required to reach that outcome.

Do not stop at intermediate states such as:

- failure recorded;
- issue created;
- notification sent;
- information made visible;
- another participant able to act.

If additional product behavior is required to reach the meaningful outcome, continue the flow until that outcome can be reached.

---

### Step 3 — Identify Functional Areas

Group the High-Level Product Flow into coherent Functional Areas.

For each proposed area, check:

- What functional responsibility does it own?
- Which part of the High-Level Product Flow does it support?
- Which actors interact with it?
- What should explicitly belong elsewhere?

Avoid creating areas solely because a feature exists in the scope.

---

### Step 4 — Identify Capabilities

For each Functional Area:

1. Identify the relevant actors.
2. Identify what each actor must be able to do.
3. Express those actions as meaningful capabilities.
4. Check whether the capabilities are sufficient to support that area's part of the High-Level Product Flow.
5. Decompose capabilities that hide materially different user behavior.
6. Merge capabilities that represent unnecessarily granular implementation or UI actions.

---

### Step 5 — Develop Functional Flows

For each significant capability or connected group of capabilities:

1. Identify the initiating actor and trigger.
2. Describe the actor's action.
3. Describe the system response.
4. Add material validations or decisions.
5. Continue the interaction until a meaningful result is reached.
6. Identify important alternative or negative paths.
7. Identify how the actor returns to or continues the flow where recovery is required.

Use the flows to discover missing capabilities and structural gaps.

When a missing capability is discovered, add it to the relevant Functional Area and update affected flows.

---

### Step 6 — Capture Key Rules, Data and States

While developing the flows, capture only rules, data and states that materially affect the functional structure.

Ask:

- Does this rule change what the actor can do?
- Does this data constraint affect the flow?
- Is this state required to understand what happens next?
- Does ownership or permission change available actions?
- Is this decision necessary to understand the structure?

If not, defer it to the **Requirements Stage**.

---

### Step 7 — Connect Functional Areas

Review transitions between Functional Areas.

Verify that:

- outputs from one area can become valid inputs to another;
- ownership is understandable;
- required states are preserved;
- no part of the High-Level Product Flow disappears between areas;
- recovery paths reconnect to the appropriate flow;
- completion depends on the correct preceding states and outcomes.

---

### Step 8 — Perform Structure Consistency Review

Review the complete proposed structure against the validated **Shape v2 Document**.

Check:

- Does every primary JTBD have a complete functional path?
- Does the structure support the validated Value Proposition?
- Is every MVP capability represented?
- Are important negative and recovery paths represented?
- Can the user reach the meaningful outcome of the product?
- Are there unexplained gaps between Functional Areas?
- Are any Functional Areas overlapping without a clear reason?
- Are any capabilities duplicated?
- Are any capabilities unsupported by the validated Shape?
- Has detailed requirements work entered Structure unnecessarily?
- Have technical implementation decisions entered Structure prematurely?

Resolve structural inconsistencies before external validation where possible.

---

### Step 9 — Visualize the Structure

Transfer the proposed functional structure into a visual representation.

The visualization should make it possible to review:

- Functional Areas;
- capabilities within each area;
- key Functional Flows;
- important rules, states and decisions;
- connections between Functional Areas;
- important negative and recovery paths.

The visual representation is a working review artifact.

Its exact layout and notation may vary depending on the product and complexity.

---

## External Validation Boundary

The proposed **Structure Document** and its visual representation must be reviewed with the client or relevant decision-makers before the **Structure Stage** is complete.

External validation must confirm or correct:

- Functional Areas;
- capabilities;
- Functional Flows;
- responsibilities and boundaries;
- important rules and states;
- cross-area connections;
- assumptions and open questions.

External validation is a real consulting activity and must not be replaced by internal analysis.

---

## Step 10 — Validate the Structure

During external review:

1. Walk through the High-Level Product Flow.
2. Review each Functional Area.
3. Review the capabilities within each area.
4. Walk through the key Functional Flows.
5. Review important negative and recovery paths.
6. Confirm important rules, states and ownership boundaries.
7. Capture corrections, decisions, rejected assumptions and new information.
8. Resolve or retain open questions as appropriate.

---

## Step 11 — Finalize the Structure Document

Incorporate validation findings into the **Structure Document**.

Update affected:

- High-Level Product Flow;
- Functional Areas;
- capabilities;
- Functional Flows;
- rules and states;
- connections;
- assumptions and open questions.

Preserve unresolved uncertainty explicitly.

The validated **Structure Document** becomes the primary input to the **Requirements Stage**.

---

## Output

The output of the **Structure Stage** is the **Structure Document**.

The **Structure Document** contains:

- High-Level Product Flow;
- Functional Areas;
- capabilities;
- key Functional Flows;
- key rules, data and states where structurally relevant;
- connections between Functional Areas;
- assumptions and open questions;
- validation findings and resulting changes;
- validation status.

Before external validation, the **Structure Document** is a proposed functional structure and must not be treated as final.

After external validation and incorporation of the resulting decisions, the validated **Structure Document** becomes the input to the **Requirements Stage**.

---

## Success Criteria

The **Structure Stage** is complete when:

- the validated **Shape v2 Document** has been transformed into a coherent functional structure;
- the complete High-Level Product Flow is represented;
- meaningful Functional Areas are identified;
- Functional Areas have clear responsibilities and boundaries;
- relevant actors and their capabilities are represented;
- key Functional Flows are described;
- important negative and recovery paths are represented;
- structurally important rules, data constraints and states are captured;
- Functional Areas connect without unexplained gaps;
- every primary JTBD can reach its meaningful outcome through the proposed structure;
- the validated Value Proposition is supported by the structure;
- the validated MVP scope is represented without unnecessary scope expansion;
- detailed requirements and technical implementation have not been introduced prematurely;
- assumptions and open questions are explicit;
- external validation has been performed;
- validation findings have been incorporated into the **Structure Document**;
- no Failure Condition remains unresolved.

---

## Failure Conditions

The **Structure Stage** is not complete if:

- an unvalidated **Shape v1 Document** is used as the validated basis for Structure;
- the High-Level Product Flow is incomplete;
- a primary JTBD cannot reach its meaningful outcome;
- an important negative or recovery path required for the product outcome is missing;
- Functional Areas are derived primarily from screens or technical components rather than product behavior;
- Functional Areas have unclear or contradictory responsibilities;
- important capabilities required by the product flow are missing;
- capabilities remain so broad that materially different product behavior is hidden;
- Functional Flows stop at intermediate states when additional behavior is required to reach the meaningful outcome;
- there are unexplained gaps between Functional Areas;
- important structural rules, states or ownership decisions are missing;
- the structure introduces unsupported functionality outside the validated Shape without explicitly identifying it as a new hypothesis;
- the structure has expanded into exhaustive detailed requirements;
- technical implementation decisions are presented as part of functional structure without a product-level reason;
- material assumptions are presented as confirmed facts;
- external validation has not occurred;
- validation feedback has not been incorporated into the **Structure Document**.