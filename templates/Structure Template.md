# Structure Document

**Status:** <Draft / Ready for external review / Validated>  
**Project:** <project>  
**Input:** **Shape v2 Document**  
**Stage:** **Structure Stage**

---

## 1. Functional Areas

- <Functional Area>
- <Functional Area>
- <Functional Area>

---

## 2. Functional Structure

### 2.1 <Functional Area>

#### Capabilities

- <Actor> can <capability>.
- <Actor> can <capability>.
- <Actor> can <capability>.
- <Actor> can <capability>.

---

#### <Capability / Functional Flow Name>

**Actor:** <Actor>

| Actor | System |
|---|---|
| <Actor action> | |
| | <System response> |
| | <Validation / decision> |
| <Next actor action> | |
| | <System response> |
| | <State change / result> |

##### Alternative / Negative Flows

- `<Condition> → <System behavior> → <Return point / result>`
- `<Condition> → <System behavior> → <Return point / result>`

##### Rules

- <Structurally relevant rule>
- <Validation>
- <Constraint>
- <Permission / ownership rule>
- <Limit>

##### States

`<State> → <State> → <State>`

##### Open Questions

- <Open question>

Include only sections that are relevant to this Functional Flow.

---

#### <Capability / Functional Flow Name>

**Actor:** <Actor>

| Actor | System |
|---|---|
| <Actor action> | |
| | <System response> |
| <Next actor action> | |
| | <System response / result> |

##### Alternative / Negative Flows

- <Alternative / negative flow>

##### Rules

- <Rule>

##### States

`<State> → <State>`

##### Open Questions

- <Open question>

---

### 2.2 <Functional Area>

#### Capabilities

- <Actor> can <capability>.
- <Actor> can <capability>.
- <Actor> can <capability>.

---

#### <Capability / Functional Flow Name>

**Actor:** <Actor>

| Actor | System |
|---|---|
| <Actor action> | |
| | <System response> |
| | <Validation / decision> |
| <Next actor action> | |
| | <System response / result> |

##### Alternative / Negative Flows

- <Alternative / negative flow>

##### Rules

- <Rule>

##### States

`<State> → <State>`

##### Open Questions

- <Open question>

---

## 3. Validated Scope Coverage

Map every validated MVP capability from the **Shape v2 Document** to the resulting Structure.

| Validated MVP Capability from Shape v2 Document | Functional Area | Structure Representation | Coverage |
|---|---|---|---|
| <Capability> | <Functional Area> | <Capability / Functional Flow> | <Covered / Transformed / Gap> |

Use:

- `Covered` — the validated capability is explicitly represented in the Structure.
- `Transformed` — the validated capability is represented through a different structural decomposition without losing the original validated behavior.
- `Gap` — the validated capability is not adequately represented.

Every validated MVP capability from the **Shape v2 Document** must appear in this table.

For every `Transformed` item, explain how the original validated behavior is represented.

Every `Gap` must be resolved or explicitly returned for validation.

Coverage does not by itself prove sufficient decomposition.

A validated capability represented only by a broad statement is not sufficiently structured when meaningful actor actions, system responses, validations, decisions, states or recovery behavior remain hidden.

---

## 4. Structure Consistency Review

### Capability Decomposition

- <Does every structurally significant capability have a Functional Flow or explicit representation within another named Functional Flow?>
- <Have complex capabilities been decomposed into meaningful actor actions and system responses?>
- <Are meaningful validations, decisions and state changes visible?>
- <Do any capability statements hide multiple materially different interactions?>
- <Are any capabilities unnecessarily granular?>

### Validated Scope Coverage

- <Has every validated MVP capability from the Shape v2 Document been traced to the Structure?>
- <Are there any unresolved Gaps?>
- <Do Transformed capabilities preserve the original validated behavior?>

### Functional Coverage

- <Can the identified capabilities support the relevant JTBD?>
- <Can users reach the meaningful outcomes defined in the Shape v2 Document?>
- <Are important negative and recovery paths represented?>
- <Is any functional mechanism required for the validated MVP missing?>

### Functional Areas

- <Does each capability belong to an appropriate Functional Area?>
- <Are any Functional Areas unnecessarily broad?>
- <Are any responsibilities duplicated or unclear?>

### Structure / Requirements Boundary

- <What detailed behavior is intentionally deferred to the Requirements Stage?>
- <Has enough functional behavior been captured to understand how each mechanism works?>

### Structure / Solutions Boundary

- <What technical decisions are intentionally deferred to the Solutions Stage?>
- <Has premature implementation design been avoided?>

---

## 5. Assumptions and Open Questions

Include only structural assumptions and open questions that do not belong to one specific Functional Flow.

### Assumptions

- <Assumption>

### Open Questions

- <Open question>

---

## 6. Structure Validation

**Status:** <Not started / Ready for external review / In review / Validated>

### Validation Findings

Leave empty until actual external validation has been performed.

- <Confirmed>
- <Correction>
- <Decision>
- <Rejected assumption>
- <New information>

### Changes After Validation

Leave empty until actual external validation has been performed.

- <Change>

### Remaining Open Questions

- <Open question>

---

## Structure Status

**Structure Document:** <Draft / Ready for external review / Validated>  
**Ready for Requirements Stage:** <Yes / No>