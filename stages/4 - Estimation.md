# Estimation Stage

## Purpose

The purpose of the **Estimation Stage** is to produce an early implementation estimate for the validated product scope.

The Stage is optional.

It is used when the client or project requires an understanding of likely:

- implementation effort;
- delivery timeline;
- cost;
- team composition;
- major implementation risks.

The Estimation Stage runs after the current authoritative validated **Shape**.

At this point, the product direction and scope have been validated, but detailed Structure, Behavior, Requirements, Design, and Solutions may not yet exist.

The estimate therefore represents the expected implementation effort based on the level of product knowledge currently available.

It is not a delivery commitment.

The goal is to provide enough estimation information to support decisions such as:

- whether the product is economically feasible;
- whether the proposed scope fits available constraints;
- whether scope should be reduced or changed;
- what approximate budget may be required;
- what approximate delivery range may be expected;
- what team may be required;
- whether further product definition is necessary before a more precise estimate can be produced.

---

# Objective

The objectives of the Estimation Stage are to:

- translate the validated product scope into estimable implementation areas;
- identify the major work required to implement the product;
- estimate implementation effort at an appropriate level of detail;
- derive an approximate delivery range;
- derive an approximate cost range where relevant;
- identify likely team composition;
- identify major assumptions affecting the estimate;
- identify major uncertainty drivers;
- identify implementation risks that may materially affect effort, cost, or timeline;
- communicate the confidence and limitations of the estimate explicitly.

The Estimation Stage should provide useful decision-making information without pretending that detailed implementation knowledge already exists.

---

# Input

The primary input is:

the current authoritative validated **Shape artifact**

Relevant upstream materials may also be used as supporting context:

- **Idea Document**;
- **Domain Document**;
- client-provided materials;
- validated external constraints;
- known delivery constraints;
- available technical information where it already exists.

The validated Shape defines the product scope being estimated.

The Estimation Stage must not silently expand that scope.

---

# Estimation Principle

The level of estimation precision must correspond to the level of product definition available.

At the Estimation Stage, LEKAL does not yet have detailed:

- functional decomposition;
- behavioral models;
- Requirements;
- Design;
- technical Solutions.

Therefore, the estimate necessarily contains uncertainty.

The Stage must not hide this uncertainty behind artificially precise numbers.

For example:

```text
Estimated delivery:
4–6 months
```

is generally more appropriate than:

```text
Estimated delivery:
127 working days
```

when the available product definition does not support that level of precision.

Precision should be earned by information.

---

# Scope Basis

The estimate must have an explicit scope basis.

Identify:

- Product Stage or release being estimated;
- functionality included in that scope;
- functionality explicitly excluded from that scope;
- important assumptions required to estimate the scope;
- known constraints affecting implementation.

If the Shape Document contains several Product Stages, the estimate must clearly identify which Stage or Stages are included.

Do not silently estimate the entire future product when only the MVP or another specific Product Stage is requested.

---

# Focus Areas

## 1. Estimation Scope

Establish exactly what is being estimated.

Identify:

- target Product Stage;
- major product capabilities or product areas known from Shape;
- relevant integrations;
- important platform requirements;
- relevant market or localization requirements;
- known regulatory or operational constraints;
- other material implementation concerns already established upstream.

The purpose is to create an explicit boundary around the estimate.

---

## 2. Implementation Areas

Decompose the validated scope into implementation areas sufficiently detailed for estimation.

These are estimation units.

They are not a substitute for the future **Structure Stage**.

Implementation areas may represent, for example:

- major product capabilities;
- user-facing product areas;
- backend functionality;
- integrations;
- authentication;
- administration;
- notifications;
- analytics;
- infrastructure;
- platform work;
- other significant implementation concerns.

The decomposition should be detailed enough to reason about effort without pretending that the complete functional WBS already exists.

---

## 3. Complexity Drivers

For each significant implementation area, identify factors likely to affect implementation effort.

These may include:

- number and complexity of actors;
- complex workflows;
- State-heavy behavior;
- permissions;
- integrations;
- third-party dependencies;
- external APIs;
- data migration;
- regulatory requirements;
- localization;
- security requirements;
- performance expectations;
- platform requirements;
- unknown technical constraints;
- unusual product behavior.

Complexity should be based on known product context rather than generic assumptions.

---

## 4. Effort

Estimate the implementation effort required for the defined scope.

The estimation method may depend on:

- project type;
- available information;
- delivery model;
- expected team;
- client needs.

The methodology may use:

- effort ranges;
- person-days;
- person-weeks;
- person-months;
- another suitable effort unit.

The chosen unit must remain consistent throughout the estimate.

Where meaningful uncertainty exists, use ranges rather than single-point estimates.

---

## 5. Team Composition

Identify the likely roles required to implement the estimated scope.

Depending on the product, this may include:

- frontend development;
- backend development;
- mobile development;
- QA;
- UX/UI design;
- DevOps;
- product or business analysis;
- technical leadership;
- other specialist roles.

Do not add roles merely because they are common in software teams.

Include roles justified by the estimated product and delivery model.

Where the exact team structure is uncertain, provide a reasonable candidate configuration rather than presenting it as established fact.

---

## 6. Delivery Range

Translate implementation effort into an approximate delivery range.

Delivery time is not identical to total effort.

Consider:

- parallel work;
- team composition;
- dependencies;
- sequencing;
- external dependencies;
- review and testing;
- integration work;
- known delivery constraints.

The result should normally be expressed as a range.

---

## 7. Cost

When cost estimation is required, derive the expected cost from:

- estimated effort;
- team composition;
- known or assumed rates;
- relevant external costs.

Separate known values from assumed values.

If rates are unknown, the Stage may provide:

- effort without cost;
- a cost formula;
- cost scenarios based on different rate assumptions.

Do not invent client rates.

---

## 8. Assumptions

Record assumptions that materially affect the estimate.

Examples may include:

- expected behavior of an external API;
- reuse of an existing authentication service;
- availability of client-provided content;
- absence of complex migration;
- expected platform support;
- expected Design availability;
- assumed technical approach where necessary for estimation.

An assumption should be recorded when changing it could materially change the estimate.

Do not create an exhaustive list of trivial assumptions.

---

## 9. Uncertainty

Identify areas where insufficient product or technical knowledge materially reduces estimation confidence.

For each significant uncertainty, determine:

- what is unknown;
- why it matters;
- which part of the estimate it affects;
- whether further analysis could reduce it.

Do not silently compensate for major uncertainty by increasing every estimate.

Make uncertainty visible.

---

## 10. Risks

Identify known risks that could materially affect:

- effort;
- delivery;
- cost;
- team composition.

Relevant risks may include:

- external dependency risk;
- technical feasibility risk;
- regulatory uncertainty;
- integration uncertainty;
- unknown legacy systems;
- performance requirements;
- scope ambiguity;
- dependencies on client decisions or materials.

Risks should be specific to the product.

Avoid generic project-management risk lists.

---

# Process

## Step 1 — Read the Current Validated Shape

Read the complete current authoritative validated **Shape artifact** and relevant upstream context.

Identify:

- Product Stage being estimated;
- included scope;
- Out of Scope items;
- actors;
- major product mechanisms;
- integrations;
- constraints;
- Target Market implications;
- known technical candidates;
- important assumptions;
- unresolved questions.

Use validated Shape information as the estimation baseline.

---

## Step 2 — Establish Estimation Scope

Define the exact boundary of the estimate.

Explicitly state:

- what Product Stage is estimated;
- what major functionality is included;
- what known functionality is excluded.

If the requested estimation scope is unclear in a way that could materially change the result, the uncertainty must be resolved before producing the final estimate.

---

## Step 3 — Create Estimation Breakdown

Decompose the scope into implementation areas.

The breakdown should be detailed enough to estimate meaningful units of work but should not attempt to perform the complete Structure Stage.

Each implementation area should be traceable to validated product scope.

Do not introduce speculative future functionality merely to make the estimate appear complete.

---

## Step 4 — Identify Complexity Drivers

For each implementation area, identify the characteristics most likely to affect implementation effort.

Use available product and domain information.

Do not assume detailed behavior that has not yet been defined.

Where missing behavior materially affects the estimate, record the uncertainty.

---

## Step 5 — Estimate Effort

Estimate implementation effort for each area using the selected estimation unit.

Prefer ranges when uncertainty is meaningful.

Document significant assumptions that influence individual estimates.

Combine individual estimates into an overall implementation effort range.

---

## Step 6 — Determine Team

Determine a reasonable team configuration capable of implementing the estimated scope.

Consider:

- required skills;
- opportunities for parallel work;
- dependencies between implementation areas;
- expected delivery model.

The proposed team is an estimation assumption unless already established by the project.

---

## Step 7 — Estimate Delivery Range

Translate effort and team assumptions into an approximate delivery range.

Account for meaningful sequencing and dependencies.

Do not calculate delivery duration by simply dividing total effort by the number of people.

---

## Step 8 — Estimate Cost

If required, calculate the cost range using known or explicitly assumed rates.

Keep:

- effort;
- rates;
- external costs;
- resulting cost

traceable.

If reliable rates are unavailable, do not manufacture a monetary estimate.

---

## Step 9 — Analyze Uncertainty and Risks

Review the estimate for factors that could materially change it.

Identify:

- major assumptions;
- major unknowns;
- implementation risks;
- areas where later LEKAL Stages may significantly change the estimate.

Where possible, explain what additional information would reduce uncertainty.

---

## Step 10 — Produce the Estimation Document

Create the **Estimation Document**.

The document should make it possible to understand:

- what was estimated;
- what was not estimated;
- how the estimate was derived;
- expected effort;
- expected team;
- expected delivery range;
- expected cost where relevant;
- important assumptions;
- major uncertainty;
- major risks.

The estimate should be useful for decision-making without implying unsupported precision.

---

# Output

The output of the Estimation Stage is:

**Estimation Document**

The Estimation Document represents an early estimate based on the validated product knowledge available after Shape.

It does not replace a detailed delivery estimate produced after later product-definition or technical-design work.

---

# Estimation Document Template

```md
# [Product Name] — Estimation

## Estimation Summary

**Estimated Scope**

[Product Stage / release]

**Estimated Effort**

[Range]

**Estimated Delivery**

[Range]

**Estimated Cost**

[Range / Not Estimated]

**Proposed Team**

[Summary]

**Estimation Confidence**

[Description]

---

## Scope

### Included

- ...

### Out of Scope

- ...

---

## Estimation Breakdown

| Implementation Area | Scope | Complexity | Effort | Notes |
|---|---|---|---|---|
| | | | | |

---

## Team

| Role | Allocation / Involvement | Notes |
|---|---|---|
| | | |

---

## Delivery

**Estimated Delivery Range**

...

**Key Dependencies**

- ...

**Sequencing Considerations**

- ...

---

## Cost

| Cost Component | Basis | Estimate |
|---|---|---|
| | | |

**Total Estimated Cost**

...

---

## Assumptions

- ...

---

## Uncertainties

| Uncertainty | Impact | What Would Reduce It |
|---|---|---|
| | | |

---

## Risks

| Risk | Potential Impact | Notes |
|---|---|---|
| | | |

---

## Estimate Limitations

- ...
```

---

# Completion Criteria

The Estimation Stage is complete when:

- the estimation scope is explicit;
- the estimate is based on validated Shape scope;
- included and excluded functionality are distinguishable;
- the product has been decomposed into meaningful estimation areas;
- significant complexity drivers have been considered;
- implementation effort has been estimated;
- likely team composition has been identified where required;
- an approximate delivery range has been produced where required;
- cost has been estimated where required and sufficient rate information exists;
- major assumptions are explicit;
- major uncertainty is visible;
- major estimation risks are explicit;
- the precision of the estimate does not exceed the precision supported by available product knowledge.

The Estimation Stage does not require detailed Requirements or a technical Solution.

Completion means:

> enough estimation confidence to support the decision for which the estimate was requested.

---

# Stage Boundary

The **Shape Stage** determines:

> What product should exist and within what validated scope?

The **Estimation Stage** determines:

> What is the likely implementation effort, cost, team, and delivery range for that scope at the current level of product definition?

The **Structure Stage** determines:

> What functional mechanisms must exist for that product to work?

Estimation does not replace Structure.

It creates a decision-support estimate from the validated Shape while explicitly preserving the uncertainty that exists before detailed product definition.