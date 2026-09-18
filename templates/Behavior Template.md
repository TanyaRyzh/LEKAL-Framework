# Behavior Document

## Status

**Project:** <Project Name>  
**Input:** **Structure v2 Document**  
**Stage:** **Behavior Stage**  
**Document Version:** v1 | v2  
**Behavior Status:** Proposed | Reviewed  

---

# 1. Behavioral Model

Organize the behavioral model by Functional Area from the **Structure v2 Document**.

Functional Areas are used to make the Document easier to review.

They are not behavioral boundaries.

A Behavioral Mechanism may:

- represent one Capability;
- combine several closely connected Capabilities;
- represent part of a Capability;
- connect behavior across several Functional Areas.

Behavioral boundaries should follow behavior.

For every Behavioral Mechanism, include only the representations and supporting information that materially help explain how it works.

Do not reproduce the same behavior in several representations unless the duplication materially improves understanding.

---

## 1.1 <Functional Area>

**Responsibility:**  
<Functional responsibility inherited from Structure>

---

### <Behavioral Mechanism>

**Structure Mapping:**

- <Capability>
- <Capability>

**Priority:**  
High / Medium / Low

**Actors:**

- <Actor>
- <Actor>

Include Actors only when useful for understanding the mechanism.

**Trigger:**  
<Meaningful trigger, when relevant>

**Preconditions:**

- <Meaningful condition>
- <Meaningful condition>

Include Preconditions only when they materially affect behavior.

---

#### Behavioral Representation

Choose the representation or combination of representations that best explains the mechanism.

Possible representations include:

- Functional Flow;
- State Machine;
- State Transition Matrix;
- Actions Matrix;
- Decision Table;
- Status Calculation;
- Rules;
- Data;
- other suitable behavioral representation.

Do not include representations that add no useful information.

---

##### Functional Flow

Use when sequence and Actor/System interaction are necessary to understand the behavior.

| Actor | System |
|---|---|
| <Actor action> | |
| | <System response> |
| | <Decision / validation, when relevant> |
| <Actor action> | |
| | <State change / meaningful result> |

**Result:**  
<Meaningful functional outcome>

Do not stop at an intermediate system response when the intended functional outcome has not yet been reached.

---

##### State Machine

Use when lifecycle States are central to understanding the behavior.

```text
<State>
↓
<State>
├── <State>
└── <State>
```

**States:**

| State | Meaning |
|---|---|
| <State> | <Functional meaning> |
| <State> | <Functional meaning> |

Do not create a State Machine when States do not materially affect behavior.

---

##### State Transition Matrix

Use when it is important to understand who or what may cause lifecycle transitions.

| From | To | <Actor> | <Actor> | System |
|---|---|---|---|---|
| <State> | <State> | Yes / No | Yes / No | Yes / No |
| <State> | <State> | Yes / No | Yes / No | Yes / No |

Use this representation for State Transitions.

Do not use it to describe unrelated actions that do not represent lifecycle transitions.

---

##### Actions Matrix

Use when available actions materially depend on the current State.

| Action | <State> | <State> | <State> |
|---|---|---|---|
| <Action> | Yes / No / Conditional | Yes / No / Conditional | Yes / No / Conditional |
| <Action> | Yes / No / Conditional | Yes / No / Conditional | Yes / No / Conditional |

Where an action changes already evaluated or completed content, describe its behavioral consequences.

**Action Consequences:**

| Action | Consequence |
|---|---|
| <Action> | <State reset / invalidation / recalculation / other consequence> |
| <Action> | <Consequence> |

---

##### Decision / Status Calculation

Use when system behavior or aggregate State depends on several conditions or related objects.

| Condition | Result |
|---|---|
| <Condition> | <Result> |
| <Condition> | <Result> |

or:

| Related Object States | Calculated State |
|---|---|
| <Combination / condition> | <State> |
| <Combination / condition> | <State> |

Include only the level of logic necessary to understand the behavioral mechanism.

---

#### Alternative / Negative Behavior

Include only behavior that materially changes the mechanism.

##### <Negative / Alternative Case>

**Condition:**  
<What causes this behavior>

**Behavior:**  
<What happens>

**Outcome:**  
<Meaningful outcome>

Do not enumerate theoretical edge cases.

---

#### Recovery

Include only when a negative condition prevents the intended outcome and productive behavior must continue.

**Recovery From:**  
<Negative State / condition>

**Responsible Actor:**  
<Actor>

**Recovery Behavior:**  
<How productive behavior resumes>

**Returns To:**  
<Behavioral Mechanism / State / flow>

Recovery should reconnect to meaningful product behavior rather than terminate at failure visibility.

---

#### Rules

Include only Rules necessary to understand behavior.

- <Rule>
- <Rule>
- <Rule>

Rules may describe:

- actor responsibility;
- action availability;
- behavioral conditions;
- limits or quotas;
- invalidation behavior;
- recalculation behavior;
- required acceptance or consent;
- other behaviorally meaningful restrictions.

Do not define exhaustive validation or specification-level Rules.

---

#### Data

Include only Data necessary to understand the behavior.

| Data | Purpose / Meaning |
|---|---|
| <Data> | <Why the behavior needs it> |
| <Data> | <Why the behavior needs it> |

Do not define:

- database fields;
- API payloads;
- exact data types;
- technical schemas;
- implementation-specific structures.

---

#### Change Consequences

Include when editing, deleting, archiving, restoring, or otherwise changing an object affects existing product State or progress.

| Change | Direct Effect | Related Effect |
|---|---|---|
| <Change> | <Direct consequence> | <Recalculation / invalidation / reset> |
| <Change> | <Direct consequence> | <Related consequence> |

Example relationship:

```text
Child object changes
↓
Child execution result becomes invalid
↓
Parent State is recalculated
↓
Aggregate progress is recalculated
```

Do not include this section when changes have no meaningful behavioral consequences.

---

#### Connections

Include only relationships necessary to understand how this mechanism participates in the broader behavioral model.

**Depends On:**

- <Behavioral Mechanism / functional condition>

**Enables:**

- <Behavioral Mechanism / functional outcome>

**Responsibility Handoff:**  
<Actor handoff, when relevant>

**State / Recalculation Connection:**  
<Related behavior, when relevant>

**Recovery Connection:**  
<Where recovery continues, when relevant>

---

#### Assumptions

- <Assumption>

Include only when relevant.

---

#### Open Questions

- <Question>

Include only questions that materially affect behavior.

---

### <Behavioral Mechanism>

Repeat the structure above using only the representations relevant to this mechanism.

---

## 1.2 <Functional Area>

**Responsibility:**  
<Functional responsibility inherited from Structure>

### <Behavioral Mechanism>

...

---

# 2. Cross-Cutting Behavior

Use this section only for behavior that materially affects several Functional Areas and would be misleading or unnecessarily duplicated if placed inside a single Functional Area.

Possible examples include:

- consent and preferences;
- Terms acceptance;
- Privacy Policy behavior;
- localization preferences;
- product-wide limits;
- account lifecycle consequences;
- aggregate product State.

Do not create this section merely to collect generic product-readiness functionality.

Each item must originate from validated or structurally justified product behavior.

---

## <Cross-Cutting Behavioral Mechanism>

**Structure Mapping:**

- <Capability / Capabilities>

**Affected Functional Areas:**

- <Functional Area>
- <Functional Area>

Use the same representation-selection principle as in the main Behavioral Model.

Include only relevant:

- Functional Flow;
- State Machine;
- State Transition Matrix;
- Actions Matrix;
- Decision / Status Calculation;
- Alternative / Negative Behavior;
- Recovery;
- Rules;
- Data;
- Change Consequences;
- Connections;
- Assumptions;
- Open Questions.

---

# 3. Limits and Quotas

Include this section only when limits or quotas are established by upstream Documents or discovered as a material behavioral concern.

| Limit | Value / Condition | Evaluated When | Behavior When Reached | Becomes Available Again When |
|---|---|---|---|---|
| <Limit> | <Value / condition> | <Trigger> | <Blocked / unavailable behavior> | <Condition> |
| <Limit> | <Value / condition> | <Trigger> | <Behavior> | <Condition> |

Do not invent product limits.

A numeric limit alone is insufficient.

Its effect on product behavior must be understood.

---

# 4. Consent, Terms, Privacy, and Preferences

Include only mechanisms relevant to the product.

This section may cover behavior such as:

- Terms acceptance;
- Privacy Policy presentation;
- optional consent;
- cookie preferences;
- language preferences;
- renewed acceptance or consent;
- changing previously saved preferences.

Do not assume that every legal document requires explicit acceptance.

Do not invent legal requirements.

---

## <Mechanism>

**Trigger:**  
<When this behavior occurs>

**Required / Optional:**  
<Required / Optional / Informational>

**Behavior:**  
<Flow, decision table, Rules, or another appropriate representation>

**Recorded Information:**  
<Only functionally relevant information>

**Effect on Product Behavior:**  
<What becomes available, unavailable, enabled, disabled, etc.>

**Change / Renewal Behavior:**  
<When relevant>

**Assumptions / Open Questions:**

- ...

---

# 5. Analytics / Observability

Identify meaningful product behavior that must be observable.

Do not model analytics as a generic user Capability unless analytics functionality is actually exposed to an actor.

## Events

| Event | Trigger | Purpose / Behavioral Meaning |
|---|---|---|
| `<event_name>` | <Meaningful product behavior> | <Why this event is useful> |
| `<event_name>` | <Meaningful product behavior> | <Why this event is useful> |

Prefer events representing meaningful product behavior rather than low-level UI interaction.

---

## Event Parameters

| Parameter | Values / Example | Purpose |
|---|---|---|
| `<parameter>` | <Values / example> | <Behavioral context> |
| `<parameter>` | <Values / example> | <Behavioral context> |

Do not include unnecessary personal information, sensitive product data, or user-generated content.

Normally exclude:

- email addresses;
- names;
- Project titles;
- Journey or Scenario content;
- Acceptance Criterion text;
- Feedback text;
- attachment names;
- client-provided content.

Analytics must respect the consent and privacy behavior defined by the product.

---

## Product Funnel / Behavioral Sequence

Include only when useful.

```text
<Meaningful event>
↓
<Meaningful event>
↓
<Meaningful event>
↓
<Meaningful outcome>
```

---

# 6. Structural Gaps

Behavioral analysis may reveal that the **Structure v2 Document** is missing a Capability or contains an incorrect functional decomposition.

Record only material Structural Gaps.

| Structural Gap | Discovered During | Why Structure Is Insufficient | Proposed Direction |
|---|---|---|---|
| <Gap> | <Behavioral Mechanism> | <Reason> | <Add / Split / Merge / Move / Reconsider> |

Do not silently modify the reviewed **Structure v2 Document**.

If no material Structural Gaps remain:

`No unresolved Structural Gaps.`

---

# 7. Cross-Area Behavioral Consistency

Record only material results of the behavioral consistency review.

## Actors and Responsibilities

**Actor responsibilities are consistent:** Yes / No  
**Responsibility handoffs are coherent:** Yes / No

## Preconditions and Outcomes

**Behavioral outcomes satisfy downstream Preconditions:** Yes / No  
**Required functional inputs exist:** Yes / No

## Functional Objects

**Functional objects are used consistently:** Yes / No

## States and Actions

**State names and meanings are consistent:** Yes / No  
**Required State Transitions exist:** Yes / No  
**State-dependent actions are consistent:** Yes / No

## Change Consequences

**Required invalidation behavior is represented:** Yes / No  
**Required recalculation chains are represented:** Yes / No  
**Parent and child States remain consistent:** Yes / No

## Negative and Recovery Behavior

**Material negative behavior has meaningful outcomes:** Yes / No  
**Required recovery behavior exists:** Yes / No  
**Recovery reconnects to intended product behavior:** Yes / No

## Limits and Cross-Cutting Behavior

**Validated limits have defined behavioral consequences:** Yes / No  
**Relevant consent / preference behavior is represented:** Yes / No

## End-to-End Behavior

**Primary JTBD can reach meaningful outcomes:** Yes / No  
**Validated MVP value loop can complete:** Yes / No

## Material Findings

- <Finding>
- <Finding>

If no material consistency problems remain:

`No unresolved Cross-Area Behavioral Consistency issues.`

---

# 8. Open Questions

Include only Open Questions that affect several Behavioral Mechanisms or the behavioral model as a whole.

Mechanism-specific questions should remain inside the relevant mechanism.

- <Open Question>
- <Open Question>

If none remain:

`No unresolved behavioral Open Questions.`

---

# 9. Behavior Validation

**Significant Structure Capabilities behaviorally represented:** Yes / No  
**High-priority Capabilities sufficiently analyzed:** Yes / No  
**Behavioral boundaries reviewed:** Yes / No  
**Representations selected according to behavior:** Yes / No  
**Meaningful sequential behavior reaches functional outcomes:** Yes / No  
**Material alternative / negative behavior represented:** Yes / No  
**Required recovery behavior represented:** Yes / No  
**Important Rules represented:** Yes / No  
**Functionally important Data represented:** Yes / No  
**Meaningful States represented where required:** Yes / No  
**State-dependent actions represented where required:** Yes / No  
**Required invalidation / recalculation behavior represented:** Yes / No  
**Validated limits have defined behavioral consequences:** Yes / No  
**Relevant consent / Terms / Privacy / preference behavior represented:** Yes / No  
**Cross-Area Behavioral Consistency checked:** Yes / No  
**Structural Gaps explicit:** Yes / No  
**MVP value loop behaviorally complete:** Yes / No  
**Observability / Analytics reviewed:** Yes / No  
**Ready for Consultant Review:** Yes / No  
**Ready for Interaction Stage:** Yes / No

### Remaining Issues

<None or short description of material issues>

---

# 10. Behavior Status

**Proposed / Reviewed**