# Concepts Document

## Status

**Project:** <Project Name>  
**Input:** **Structure v2 Document**  
**Stage:** **Concepts Stage**  
**Document Version:** v1 | v2  
**Concepts Status:** Proposed | Reviewed  

---

## 1. Concept Map

Map significant capabilities from the **Structure v2 Document** to Concepts.

| Functional Area | Structure Capability | Priority | Concept | Coverage |
|---|---|---|---|---|
| <Functional Area> | <Capability> | Must / Should / Could | <Concept> | Covered / Combined / Gap |
| <Functional Area> | <Capability> | Must / Should / Could | <Concept> | Covered / Combined / Gap |

### Coverage Summary

**Covered:** <number>  
**Combined:** <number>  
**Gap:** <number>

### Unresolved Gaps

- <Capability not yet represented>
- <Capability not yet represented>

If no unresolved gaps remain:

`No unresolved Structure coverage gaps.`

---

## 2. Functional Concepts

### 2.1 <Functional Area>

---

### <Concept Name>

**Structure Mapping:**  
- <Capability>
- <Capability>

**Priority:**  
Must / Should / Could

**Actors:**  
- <Actor>
- <Actor>

**Trigger:**  
<What starts the Concept>

**Preconditions:**  
- <Condition>
- <Condition>

Include only meaningful preconditions.

---

#### Main Functional Flow

| Actor | System |
|---|---|
| <Actor action> | |
| | <System response> |
| | <Validation / decision> |
| <Next actor action> | |
| | <State change / result> |

**Result:**  
<Meaningful functional outcome>

---

#### Alternative / Negative Flows

##### <Alternative / Negative Flow Name>

**Condition:**  
<What causes the alternative path>

| Actor | System |
|---|---|
| <Actor action, when relevant> | |
| | <System response> |
| <Next action, when relevant> | |
| | <Result> |

**Outcome:**  
<What happens after this path>

---

##### <Alternative / Negative Flow Name>

**Condition:**  
<...>

**Outcome:**  
<...>

Do not enumerate theoretical edge cases.

Include only behavior that materially changes the Concept, blocks the Main Flow, creates a meaningful state, affects another actor, or requires recovery.

---

#### Recovery

Include this section only when a negative path requires functional recovery.

**Recovery From:**  
<Negative state / blocked flow>

**Responsible Actor:**  
<Actor>

**Recovery Flow:**

| Actor | System |
|---|---|
| <Action> | |
| | <Response> |
| <Action> | |
| | <Recovered state / return point> |

**Returns To:**  
<Concept / Main Flow step / product flow>

---

#### Rules

Include only Rules necessary to understand the behavior of this Concept.

- <Rule>
- <Rule>
- <Rule>

Do not define exhaustive validation or detailed Requirements here.

---

#### Data

Include only data that is functionally important to understanding the Concept.

| Data | Purpose / Meaning | Required |
|---|---|---|
| <Data item> | <Why it matters> | Yes / No |
| <Data item> | <Why it matters> | Yes / No |

Do not define technical schemas, database fields, API payloads, or exact data types.

---

#### States

Include only states that materially affect behavior.

| State | Meaning | Available / Blocked Behavior |
|---|---|---|
| <State> | <Meaning> | <Relevant behavior> |
| <State> | <Meaning> | <Relevant behavior> |

##### State Transitions

| From | Trigger | Actor / System | To | Result |
|---|---|---|---|---|
| <State> | <Trigger> | <Actor/System> | <State> | <Meaningful result> |

Do not create a formal state model where states do not materially affect behavior.

---

#### Connections

**Depends On:**  
- <Concept / capability / meaningful condition>

**Produces / Enables:**  
- <Concept / capability / meaningful state>

**Responsibility Handoff:**  
<Describe when responsibility moves to another actor or Functional Area, when relevant>

**Recovery Connection:**  
<Where negative behavior reconnects to another Concept, when relevant>

---

#### Assumptions

- <Assumption>

---

#### Open Questions

- <Question>

---

### <Concept Name>

**Structure Mapping:**  
<...>

**Priority:**  
<...>

**Actors:**  
<...>

**Trigger:**  
<...>

**Preconditions:**  
<...>

#### Main Functional Flow

| Actor | System |
|---|---|
| <Action> | |
| | <Response> |

**Result:**  
<...>

#### Alternative / Negative Flows

<Only when relevant>

#### Recovery

<Only when relevant>

#### Rules

<Only when relevant>

#### Data

<Only when relevant>

#### States

<Only when relevant>

#### Connections

<Only when relevant>

#### Assumptions

<Only when relevant>

#### Open Questions

<Only when relevant>

---

## 3. Structural Gaps

Use this section when behavioral analysis reveals that the **Structure v2 Document** is incomplete or incorrectly decomposed.

| Structural Gap | Discovered During | Why Structure Is Insufficient | Proposed Change | Impact |
|---|---|---|---|---|
| <Missing / incorrect capability> | <Concept> | <Reason> | <Add / Split / Merge / Move / Reclassify> | <Minor / Material> |

### Structural Gap Decisions

For **Concepts v1 Document**:

| Structural Gap | Consultant Decision |
|---|---|
| <Gap> | Pending |

For **Concepts v2 Document**:

| Structural Gap | Consultant Decision |
|---|---|
| <Gap> | Accept / Reject / Transform / Return to Structure |

Material scope changes must not be silently absorbed into Concepts.

---

## 4. Cross-Concept Consistency Review

### Actors

- Actor responsibilities are consistent across Concepts: Yes / No
- Responsibility handoffs are clear: Yes / No
- Conflicting actor responsibilities found: <None / Findings>

### Preconditions and Outputs

- Concept outputs satisfy downstream Preconditions: Yes / No
- Missing prerequisite behavior: <None / Findings>
- Data required but never produced: <None / Findings>

### States

- State names are consistent across Concepts: Yes / No
- State meaning is consistent across Concepts: Yes / No
- Contradictory states or transitions: <None / Findings>

### Functional Objects

- Functional objects are used consistently: Yes / No
- Duplicated or conflicting ownership: <None / Findings>

### Negative and Recovery Paths

- Material negative paths have meaningful outcomes: Yes / No
- Required recovery paths exist: Yes / No
- Recovery reconnects to the intended value loop: Yes / No
- Dead-end flows: <None / Findings>

### Concept Boundaries

- Concepts represent coherent functional mechanisms: Yes / No
- Overly broad Concepts: <None / Findings>
- Artificially fragmented Concepts: <None / Findings>

### End-to-End Behavior

- Primary JTBD can reach meaningful outcomes: Yes / No
- Validated Value Proposition is behaviorally supported: Yes / No
- MVP value loop can complete: Yes / No

### Consistency Findings

- <Finding>
- <Finding>

---

## 5. Assumptions and Open Questions

### Cross-Concept Assumptions

- <Assumption affecting several Concepts>
- <Assumption>

### Cross-Concept Open Questions

- <Question affecting several Concepts>
- <Question>

Concept-specific assumptions and questions should remain with the relevant Concept.

---

## 6. Consultant Review and Visualization

> Complete when producing the **Concepts v2 Document**.

The consultant reviews the **Concepts v1 Document** while transferring the functional model into Miro or another suitable visual workspace.

### Accepted

- <Concept / flow / rule accepted>

### Removed

- <Behavior removed and why>

### Added

- <Behavior discovered during visualization>

### Transformed

- <Concept split / merged / reorganized>
- <Flow changed>
- <Responsibility changed>

### Structural Changes

- <Change to Structure discovered during review>

### Rules / States Changes

- <Rule or state corrected during review>

### Remaining Questions

- <Question>
- <Question>

---

## 7. Concept Review Decisions

Use this section to make the differences between **Concepts v1 Document** and **Concepts v2 Document** explicit.

| Concept | v1 Proposal | Consultant Decision | v2 Result |
|---|---|---|---|
| <Concept> | <Short summary> | Accept / Reject / Transform | <Final result> |
| <Concept> | <Short summary> | Accept / Reject / Transform | <Final result> |

Do not record every wording correction.

Capture only material behavioral decisions.

---

## 8. Concepts Validation

### Structure Coverage

- Every significant Structure capability is represented: Yes / No
- No capability silently disappeared: Yes / No
- Structure Coverage gaps resolved or explicit: Yes / No

### Behavioral Model

- Main Flows reach meaningful outcomes: Yes / No
- Actor/System responsibilities are clear: Yes / No
- Material negative paths are represented: Yes / No
- Required recovery paths are represented: Yes / No
- Important Rules are represented: Yes / No
- Functionally important Data is represented: Yes / No
- Meaningful States are represented: Yes / No
- Concept Connections are coherent: Yes / No

### Consistency

- Cross-Concept Consistency review is complete: Yes / No
- Actors are consistent: Yes / No
- States are consistent: Yes / No
- Functional objects are consistent: Yes / No
- Preconditions and outputs connect correctly: Yes / No
- No known dead-end recovery paths remain: Yes / No

### Stage Boundaries

- Concepts remain above detailed Requirements: Yes / No
- Concepts remain implementation-independent: Yes / No
- Structural Gaps are explicit rather than silently hidden: Yes / No

### Known Behavioral Gaps

<None or unresolved gaps>

### Known Structural Gaps

<None or unresolved gaps>

### Ready for Requirements Stage

**Yes / No**

### Concepts Status

**Proposed / Reviewed**