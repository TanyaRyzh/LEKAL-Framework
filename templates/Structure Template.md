# Structure Document

## Status

**Project:** <Project Name>  
**Input:** **Shape v2 Document**  
**Stage:** **Structure Stage**  
**Document Version:** v1 | v2  
**Structure Status:** Proposed | Reviewed  

---

## 1. Functional Structure

### 1.1 <Functional Area>

**Responsibility:**  
<Short description of the functional responsibility represented by this area.>

**Actors:**  
<Relevant actors, if useful for understanding the area.>

#### <Capability Group>

| Capability | Classification | Priority | Actor | Rationale / Notes |
|---|---|---|---|---|
| <Capability> | Validated / Derived | Must / Should / Could | <Actor> | <Rationale, dependency, uncertainty, or other relevant note> |
| <Capability> | Validated / Derived | Must / Should / Could | <Actor> | |
| <Capability> | Validated / Derived | Must / Should / Could | <Actor> | |

#### <Capability Group>

| Capability | Classification | Priority | Actor | Rationale / Notes |
|---|---|---|---|---|
| <Capability> | Validated / Derived | Must / Should / Could | <Actor> | |
| <Capability> | Validated / Derived | Must / Should / Could | <Actor> | |

---

### 1.2 <Functional Area>

**Responsibility:**  
<Short description of the functional responsibility represented by this area.>

**Actors:**  
<Relevant actors, if useful.>

| Capability | Classification | Priority | Actor | Rationale / Notes |
|---|---|---|---|---|
| <Capability> | Validated / Derived | Must / Should / Could | <Actor> | |
| <Capability> | Validated / Derived | Must / Should / Could | <Actor> | |

> Use Capability Groups only where they improve understanding.  
> A Functional Area may contain a flat capability list when grouping adds no value.

---

## 2. Structural Dependencies

Include only dependencies that materially affect functional Structure, completeness, or priority.

| Capability | Depends On | Why It Matters |
|---|---|---|
| <Capability> | <Capability / condition> | <Functional reason> |
| <Capability> | <Capability / condition> | <Functional reason> |

Do not include technical implementation dependencies.

---

## 3. Validated Scope Coverage

Map the validated MVP scope from the **Shape v2 Document** to the proposed Structure.

| Validated Scope Item | Structure Representation | Coverage | Notes |
|---|---|---|---|
| <Shape capability / scope item> | <Functional Area → Capability> | Covered / Transformed / Gap | |
| <Shape capability / scope item> | <Functional Area → Capability> | Covered / Transformed / Gap | |

### Coverage Summary

**Covered:** <number>  
**Transformed:** <number>  
**Gap:** <number>

### Unresolved Gaps

- <Gap and required action>
- <Gap and required action>

If no unresolved gaps remain:

`No unresolved validated scope gaps.`

---

## 4. Functional Completeness Review

### <Functional Area>

**Actors covered:**  
<Yes / No + relevant finding>

**Start of work covered:**  
<Yes / No + relevant finding>

**Return to existing work covered:**  
<Yes / No + relevant finding>

**Lifecycle sufficiently represented:**  
<Yes / No + relevant finding>

**Necessary management capabilities covered:**  
<Yes / No + relevant finding>

**Important recovery / continuation capabilities covered:**  
<Yes / No + relevant finding>

**Hidden broad capabilities:**  
<None or capability requiring further decomposition>

**Missing or questionable capabilities:**  
<None or findings>

---

### <Functional Area>

**Actors covered:**  
<...>

**Start of work covered:**  
<...>

**Return to existing work covered:**  
<...>

**Lifecycle sufficiently represented:**  
<...>

**Necessary management capabilities covered:**  
<...>

**Important recovery / continuation capabilities covered:**  
<...>

**Hidden broad capabilities:**  
<...>

**Missing or questionable capabilities:**  
<...>

---

## 5. Product-Level Completeness Review

### Primary JTBD

| JTBD | Functional Support | Status | Notes |
|---|---|---|---|
| <JTBD> | <Relevant Functional Areas / Capabilities> | Supported / Gap | |
| <JTBD> | <Relevant Functional Areas / Capabilities> | Supported / Gap | |

### Value Proposition

| Value Proposition | Functional Support | Status | Notes |
|---|---|---|---|
| <Value proposition item> | <Relevant capabilities> | Supported / Gap | |

### MVP Value Loop

**Value Loop:**  
<Short representation of the validated end-to-end value loop>

**Functional Support:**  
<Functional Areas / capabilities supporting the loop>

**Can the loop reach its meaningful outcome?**  
Yes / No

**Can important negative paths return to the loop where necessary?**  
Yes / No

**Known gaps:**  
<None or findings>

---

## 6. Derived Capabilities Review

Use this section to make agent-generated scope expansion easy to challenge during consultant review.

| Derived Capability | Priority | Functional Rationale | Consultant Decision |
|---|---|---|---|
| <Capability> | Must / Should / Could | <Why it appears necessary> | Pending / Accept / Reject / Transform |
| <Capability> | Must / Should / Could | <Why it appears necessary> | Pending / Accept / Reject / Transform |

For **Structure v1 Document**, Consultant Decision may remain `Pending`.

For **Structure v2 Document**, all material Derived capabilities should have an explicit decision or remain clearly identified as unresolved.

---

## 7. Assumptions and Open Questions

### Assumptions

- <Assumption affecting functional Structure>
- <Assumption affecting priority or capability existence>

### Open Questions

- <Question that may change Structure>
- <Question requiring consultant or client decision>

Do not include detailed behavioral questions that belong to the **Concepts Stage**.

---

## 8. Consultant Review

> Complete when producing the **Structure v2 Document**.

### Accepted

- <Accepted Functional Area / capability / decomposition decision>

### Removed

- <Capability removed from Structure and why>

### Added

- <Capability added during consultant review and why>

### Transformed

- <Capability / group merged, split, renamed, or moved>

### Priority Changes

| Capability | v1 Priority | v2 Priority | Reason |
|---|---|---|---|
| <Capability> | <Priority> | <Priority> | <Reason> |

### Remaining Structural Questions

- <Question>
- <Question>

---

## 9. Structure Validation

### Structure Review

- Functional Areas represent coherent responsibilities: Yes / No
- Capability decomposition is sufficiently deep: Yes / No
- Derived capabilities have functional rationale: Yes / No
- Priorities have been reviewed: Yes / No
- Important dependencies are represented: Yes / No
- Validated Scope Coverage is complete: Yes / No
- Functional Completeness review is complete: Yes / No
- Primary JTBD are functionally supported: Yes / No
- MVP value loop can reach its meaningful outcome: Yes / No
- Structure remains above Concepts / Requirements detail: Yes / No

### Structural Gaps

<None or unresolved structural gaps>

### Ready for Concepts Stage

**Yes / No**

### Structure Status

**Proposed / Reviewed**