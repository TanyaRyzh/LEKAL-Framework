# Solutions Stage

Transform the Consultant-refined Requirements v2 into a technical solution that can be used as the basis for implementation.

Depending on the product, the consultant may define:

- system structure
- components or modules
- domain and data models
- technical implementation of established states and lifecycles
- system interactions
- integrations
- data flows
- interface definitions
- technical decisions and constraints

Only artifacts that help explain, validate, or implement the solution should be created.

The purpose of this stage is to describe **how the system supports the required product behavior** without introducing unnecessary implementation detail.

**Output:** Solutions

---

## Input

Requirements v2 is the primary specification. Use validated Behavior v3,
Interaction v3, Structure v2, and established constraints where necessary to
interpret it. Design may provide additional context when available; it is
optional and is not a prerequisite for Solutions.

## Boundaries

Requirements define what must be true of the product. Solutions define the
technical mechanisms that satisfy those requirements.

Do not silently change scope, Actors, permissions, Rules, States, recovery, or
acceptance conditions. If technical analysis exposes a product gap or an
infeasible constraint, identify the affected requirement and return the
product decision to the responsible Stage and Consultant.

## Completion Criteria

- technical decisions support Requirements v2;
- relevant components, data, interfaces, integrations, and interactions are coherent;
- established constraints are respected;
- material assumptions, tradeoffs, risks, and unresolved questions are explicit;
- implementation does not require inventing material product behavior;
- the Consultant has reviewed and refined the proposed solution.

## Failure Conditions

- technical models contradict established behavior or Requirements;
- the solution silently redesigns the product;
- unnecessary architecture obscures implementation decisions;
- material uncertainty is presented as resolved;
- Design is treated as a mandatory prerequisite.
