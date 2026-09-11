# Structure Document

**Status:** <Draft / Ready for external review / Validated>  
**Project:** <project>  
**Input:** **Shape v2 Document**  
**Stage:** **Structure Stage**

---

## 1. High-Level Product Flow

Describe the complete end-to-end functional flow of the product.

The flow should include the primary successful path and important negative or recovery paths required to reach the meaningful product outcome.

### Primary Flow

1. <Actor action>
2. <System response>
3. <Next action / transition>
4. ...
5. <Meaningful product outcome>

### Important Negative / Recovery Flows

#### <Negative or Recovery Flow>

`<Trigger> → <State / action> → <Recovery> → <Return to flow> → <Outcome>`

---

## 2. Functional Areas

| Functional Area | Responsibility | Primary Actors | Part of Product Flow |
|---|---|---|---|
| <Area> | <What this area owns> | <Actors> | <What part of the High-Level Product Flow it supports> |

---

## 3. Functional Area Structure

### 3.1 <Functional Area>

#### Purpose

<What functional responsibility this area has within the product.>

#### Actors

- <Actor>
- <Actor>

#### Capabilities

- <Actor> can <capability>.
- <Actor> can <capability>.
- <Actor> can <capability>.

#### Functional Flows

##### <Flow Name>

**Actor:** <Actor>  
**Trigger:** <What starts the flow>

**Flow:**

1. <Actor action>
2. <System response>
3. <System validation / decision, if structurally relevant>
4. <Actor action / system transition>
5. <Meaningful result>

**Alternative / Negative Flows:**

- `<Condition> → <system behavior / resulting state / return point>`
- `<Condition> → <system behavior / resulting state / return point>`

##### <Another Flow Name>

**Actor:** <Actor>  
**Trigger:** <What starts the flow>

**Flow:**

1. ...
2. ...

**Alternative / Negative Flows:**

- ...

#### Key Rules, Data and States

Include only rules, data constraints, states and decisions that materially affect the functional structure or Functional Flows.

##### Rules

- <Structurally important rule>
- <Ownership / permission rule>
- <Limit or constraint affecting the flow>

##### Data

| Data / Concept | Structurally Relevant Constraints |
|---|---|
| <Field / entity / concept> | <Constraint> |

##### States

`<State> → <State> → <State>`

or:

| State | Meaning | Possible Next States |
|---|---|---|
| <State> | <Meaning> | <States> |

Include these subsections only where they are relevant to the Functional Area.

#### Connections

- Receives <information / state / result> from <Functional Area>.
- Provides <information / state / result> to <Functional Area>.
- <Event / action> causes transition to <Functional Area>.

#### Boundaries

- Owns: <responsibility>.
- Does not own: <responsibility belonging elsewhere>.
- <Additional boundary where clarification is useful>.

#### Assumptions and Open Questions

**Assumptions**

- <Assumption>

**Open Questions**

- <Open question>

Include only material assumptions and open questions relevant to this Functional Area.

---

### 3.2 <Functional Area>

Repeat the same structure where applicable.

---

## 4. Cross-Area Connections

Describe how the Functional Areas form one connected product.

### Cross-Area Flow

```text
<Functional Area>
        │
        └── <transition> ──> <Functional Area>
                                  │
                                  ├── <result> ──> <Functional Area>
                                  │
                                  └── <negative result> ──> <Recovery Area / Flow>
```

### Connection Rules

- <Required relationship between areas>
- <Ownership transition>
- <State or information required for transition>
- <Recovery connection>
- <Completion dependency>

---

## 5. Structure Consistency Review

### Product Flow

- <Does the structure support the complete High-Level Product Flow?>
- <Can the primary JTBD reach its meaningful outcome?>
- <Are important negative and recovery paths complete?>

### Functional Coverage

- <Are all validated MVP capabilities represented?>
- <Does each capability belong to an appropriate Functional Area?>
- <Are any capabilities missing, duplicated or unnecessarily broad?>

### Functional Area Boundaries

- <Are responsibilities clear?>
- <Are there overlaps?>
- <Are cross-area dependencies understandable?>

### Shape Alignment

- <How the structure supports the primary JTBD>
- <How the structure supports the Value Proposition>
- <Whether any functionality has been added beyond the validated Shape>

### Structure / Requirements Boundary

- <Any details intentionally deferred to the Requirements Stage>
- <Any areas that may already contain unnecessary requirements-level detail>

### Structure / Solutions Boundary

- <Any technical decisions intentionally deferred to the Solutions Stage>
- <Any technical assumptions that materially affect Structure>

---

## 6. Assumptions and Open Questions

Capture cross-product structural uncertainty that does not belong to one Functional Area.

### Assumptions

- <Assumption>

### Open Questions

- <Open question>

---

## 7. Structure Validation

**Status:** <Not started / Ready for external review / In review / Validated>

### Validation Scope

Review:

- High-Level Product Flow;
- Functional Areas;
- capabilities;
- Functional Flows;
- important negative and recovery paths;
- key rules and states;
- Functional Area responsibilities and boundaries;
- cross-area connections;
- assumptions and open questions.

### Validation Findings

Leave empty until actual external validation has been performed.

- <Confirmed>
- <Correction>
- <Decision>
- <Rejected assumption>
- <New information>

### Changes After Validation

Leave empty until actual external validation has been performed.

- <Change made to the Structure Document based on validation>

### Remaining Open Questions

- <Open question remaining after validation>

---

## Structure Status

**Structure Document:** <Draft / Ready for external review / Validated>  
**Ready for Requirements Stage:** <Yes / No>

The **Structure Document** may be used as the validated input to the **Requirements Stage** only after external validation has been performed and the resulting feedback has been incorporated.