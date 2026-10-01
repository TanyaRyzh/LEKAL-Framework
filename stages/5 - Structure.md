# LEKAL 3 — Structure

## Goal

Transform the validated **Shape v2 Document** into a complete functional decomposition of the product.

The **Structure Stage** answers:

> What functional mechanisms must exist for this product to work?

The result is a functional Work Breakdown Structure:

```text
Product
↓
Functional Areas
↓
Capabilities
```

The **Structure Stage** identifies what functionality exists, who needs it, and how important it is.

It does not define in detail how that functionality behaves.

Detailed behavioral analysis belongs to the **Behavior Stage**.

The agent produces the **Structure v1 Document**.

The consultant reviews the proposed Structure, removes unnecessary functionality, adds missing functionality, corrects decomposition and actor responsibility, and adjusts priorities.

The reviewed result becomes the **Structure v2 Document**.

The **Structure v2 Document** is the primary input to the **Behavior Stage**.

---

## Objective

Create a functional decomposition broad and complete enough that later Stages do not need to rediscover basic product functionality.

The **Structure Stage** should:

- identify coherent Functional Areas;
- identify meaningful Capabilities within each Functional Area;
- preserve validated functionality from the **Shape v2 Document**;
- discover functionality implied by validated product behavior;
- discover cross-cutting and product-readiness functionality required by the specific product context;
- identify relevant actors for each Capability;
- assign proposed functional priorities;
- identify important structural dependencies;
- expose material Structural Gaps;
- preserve assumptions and Open Questions that may change the functional Structure;
- verify that the resulting Structure supports the validated product value loop.

The **Structure Stage** should not define:

- detailed Actor/System flows;
- detailed business rules;
- exhaustive validations;
- field-level requirements;
- detailed state behavior;
- UI behavior;
- technical implementation.

These belong to later Stages.

---

# Input

Primary input:

**Shape v2 Document**

The **Shape v2 Document** represents validated product direction and scope.

Supporting materials may also be used when relevant, including:

- **Idea Document**;
- existing project materials;
- validation findings;
- research produced during earlier Stages.

The **Shape v2 Document** is the starting point for functional decomposition.

It is not assumed to contain a complete list of product functionality.

---

# Output

## Structure v1 Document

The agent produces a proposed **Structure v1 Document**.

The **Structure v1 Document** contains the proposed functional WBS and material findings necessary for consultant review.

The proposal may deliberately be broader than the final Structure.

When there is reasonable functional justification for a potentially necessary Capability, prefer proposing it for consultant review rather than silently omitting it.

The agent must distinguish internally between functionality validated during Shape and functionality derived during Structure analysis.

This distinction supports analysis but does not need to appear as a dedicated field in the **Structure Document**.

---

## Structure v2 Document

After Consultant Review, the reviewed result becomes the **Structure v2 Document**.

The consultant may:

- accept or reject proposed Capabilities;
- remove unnecessary functionality;
- add missing functionality;
- merge or split Capabilities;
- rename Capabilities;
- move Capabilities between Functional Areas;
- merge or split Functional Areas;
- correct actor responsibility;
- change priorities;
- resolve assumptions;
- add or resolve structural Open Questions.

The purpose of Consultant Review is not to preserve the agent's proposal.

The purpose is to produce the best functional Structure for the product.

The **Structure v2 Document** becomes the primary input to the **Behavior Stage**.

---

# Core Functional Model

The default decomposition is:

```text
Product
↓
Functional Areas
↓
Capabilities
```

---

## Functional Areas

A Functional Area represents a coherent product responsibility.

Examples:

```text
Account & Authentication
Project Workspace
Scenario Preparation
Client Access
UAT Execution
```

Functional Areas should not be based primarily on:

- screens;
- pages;
- database entities;
- APIs;
- services;
- technical components.

A Functional Area describes a meaningful functional responsibility of the product.

---

## Capabilities

A Capability represents something meaningful an actor can accomplish through the product.

Examples:

```text
Register with email and password
Recover account password
Delete own account
Create project
View project list
Invite member
Edit scenario
Provide guest access
Change interface language
Manage cookie preferences
Retest scenario
```

Prefer meaningful actor intentions over UI or implementation actions.

Avoid overly broad Capabilities such as:

```text
Manage Projects
Manage Users
Handle UAT
```

when they hide several distinct functional intentions.

Also avoid decomposing functionality into trivial UI actions.

---

## Optional Grouping

Capability Groups are not a required level of functional decomposition.

If a Functional Area contains many Capabilities, temporary or presentational grouping may be used to improve readability.

For example:

```text
Account & Authentication

Registration
- Register with email and password

Password Management
- Recover account password
- Change password
```

Such grouping is a presentation aid rather than a mandatory WBS level.

Do not create artificial hierarchy merely for consistency.

---

# Capability Classification

During analysis, distinguish between two sources of functionality.

## Validated

A Validated Capability directly represents functionality established in the **Shape v2 Document**.

Example:

```text
Shape:
Vendor can create a project.

Structure:
Create project
```

---

## Derived

A Derived Capability is not explicitly stated in the **Shape v2 Document**, but is discovered during functional analysis as necessary or strongly implied.

Example:

```text
Shape:
Vendor can create projects.

Derived Structure:
View project list
Open project
```

because the vendor must be able to return to existing work.

Another example:

```text
Shape:
Owner can invite a member.

Derived Structure:
Accept invitation
```

because an invitation must lead to actual project participation.

A Derived Capability may also be discovered from validated product context rather than directly from another Capability.

For example, Target Market, regulatory context, privacy needs, or other validated Shape information may imply functional mechanisms such as:

```text
Change interface language
Manage cookie preferences
Delete own account
```

when those mechanisms are materially required by the specific product context.

Derived does not mean approved.

It means:

> The Capability was discovered during Structure analysis and has a product-specific functional justification.

The consultant may:

- accept it;
- reject it;
- transform it;
- reprioritize it.

Validated / Derived classification is primarily an analytical control.

It does not need to appear in the final **Structure Document** unless useful for a specific case.

---

# Functional Priority

Every proposed Capability receives a functional priority:

- High;
- Medium;
- Low.

Priority describes the relative functional importance of the Capability within the product Structure.

It does not redefine Product Stage or release scope established during the **Shape Stage**.

---

## High

A Capability is High priority when it is central or important to intended product operation.

Typical reasons include:

- directly supports a primary JTBD;
- directly supports the validated value loop;
- enables an important actor responsibility;
- is necessary to start or continue core product work;
- supports a critical negative or recovery path;
- another important Capability cannot operate coherently without it.

Removing a High Capability would materially damage the intended product experience or value delivery.

---

## Medium

A Capability is Medium priority when it provides meaningful product functionality but is not central to the primary value loop.

Its absence may:

- create noticeable friction;
- limit collaboration;
- reduce usability;
- make some product situations inconvenient;
- remove useful supporting behavior;

without fundamentally breaking the primary product outcome.

---

## Low

A Capability is Low priority when it is secondary, supporting, convenience-oriented, or reasonably deferrable.

Its absence does not materially prevent the primary product outcome.

Low does not mean unnecessary.

It means the Capability has lower relative functional importance than High or Medium functionality.

---

## Priority Principle

Priority must be based on product-specific functional reasoning.

Do not assign priority merely because a Capability is common in similar products.

Consider:

- primary JTBD;
- Value Proposition;
- validated MVP value loop;
- actor responsibilities;
- lifecycle continuity;
- recovery;
- functional dependencies;
- product constraints;
- consequence of omission.

Priorities proposed in the **Structure v1 Document** are hypotheses.

The consultant may change them during review.

---

# Functional Discovery

The **Shape v2 Document** defines validated product direction.

It does not necessarily enumerate every Capability required for the product to operate coherently.

The **Structure Stage** must therefore perform Functional Discovery.

The core principle is:

> Shape wording is the starting point for functional decomposition, not the complete functional model.

For each Functional Area, analyze what functionality must surround validated behavior so that actors can actually perform meaningful work.

In addition to analyzing the core product flow, review whether the validated product context creates cross-cutting functional responsibilities that are not naturally discovered from the primary value loop.

---

## Actor Lens

For each actor, ask:

- What must this actor be able to start?
- What must this actor be able to access?
- What must this actor be able to continue?
- What must this actor be able to see?
- What must this actor be able to change?
- What responsibilities does this actor own?
- What happens when responsibility passes to another actor?

This helps identify functionality hidden by broad Shape statements.

---

## Functional Object Lens

For important functional objects, ask:

- How is the object created or introduced?
- How is it found later?
- How is it opened or viewed?
- Can it change?
- Can it be removed, revoked, archived, or otherwise stop being active?
- Who can perform those actions?
- What other functionality depends on the object?

Examples of functional objects may include:

```text
Account
Project
Journey
Scenario
Invitation
Guest Access
Feedback
```

These questions are analytical prompts.

They are not a mandatory CRUD checklist.

Do not add operations that have no product-specific reason to exist.

---

## Lifecycle Lens

For important product work and functional objects, ask:

```text
How does it begin?
↓
How does it continue?
↓
How does it change?
↓
How does it end or stop being active?
↓
How does it reach a meaningful outcome?
```

Identify Capabilities required at important lifecycle transitions.

The lifecycle review should include actor-owned objects such as accounts where their creation, continued existence, or termination materially affects the product.

---

## Continuation Lens

Products must support not only starting work but returning to it.

Ask:

- How does the actor find existing work?
- How does the actor reopen it?
- How does the actor understand current state?
- How does the actor continue from where work stopped?

This is especially important for persistent objects and multi-session workflows.

---

## Recovery Lens

For important negative outcomes, ask:

- What happens when the normal path fails?
- Does the actor still need to reach the original outcome?
- What Capability allows work to recover?
- Does another actor need to intervene?
- Can the process return to the primary value loop?

Do not stop functional decomposition at failure visibility when the validated JTBD requires resolution.

---

## Value Loop Lens

Review the complete validated MVP value loop.

Ask:

- Can every meaningful step actually happen?
- Can responsibility move between actors?
- Can actors return to unfinished work?
- Can important negative paths recover?
- Can the product reach the validated final outcome?

A functional decomposition is incomplete if the value loop stops before the meaningful outcome established during Shape.

---

## Product Readiness Lens

Core product flows do not necessarily reveal all functional mechanisms required for a real product to operate in its validated context.

Review the product for cross-cutting concerns that may create user-facing or actor-facing Capabilities.

Relevant concerns may include, where applicable:

- privacy and consent;
- account and personal-data lifecycle;
- target-market and localization needs;
- legal or regulatory interaction;
- product limits or quotas;
- user preferences;
- other cross-cutting responsibilities implied by the validated product context.

For each relevant concern, ask:

1. Does the **Shape v2 Document**, Target Market, Constraint, actor model, data usage, or product scope make this concern relevant?
2. Does addressing the concern require an actor to perform or control something through the product?
3. Does the product need a functional mechanism to support that responsibility?
4. If so, is the mechanism already represented by an existing Capability?
5. If not, propose a Derived Capability.

Examples may include:

```text
Manage cookie preferences
Delete own account
Change interface language
```

These are examples of possible findings, not mandatory product functionality.

Do not automatically add standard SaaS capabilities.

A Product Readiness concern belongs in the functional Structure only when the specific product context creates a justified functional responsibility.

Technical, operational, or organizational concerns that do not create product functionality should remain Constraints or belong to later Stages rather than being forced into the WBS.

---

# Scope Discipline

Functional Discovery does not mean adding generic product functionality.

Do not add a Capability merely because:

- similar products have it;
- it is common SaaS functionality;
- it appears on a generic product-readiness checklist;
- it seems professionally complete;
- a competitor supports it;
- it might be useful someday.

Every Derived Capability must have a product-specific reason based on at least one of:

- validated product behavior;
- validated Target Market or market-specific need;
- validated Constraint;
- actor responsibility;
- functional object lifecycle;
- continuation;
- recovery;
- value loop;
- product-readiness concern that creates a functional responsibility;
- another justified Capability.

If the rationale cannot be explained, do not silently add the Capability.

---

# Structural Uncertainty

Not every uncertainty needs to be solved during the **Structure Stage**.

If functional need is clear but detailed behavior is unknown:

> Include the Capability and defer behavioral analysis to the **Behavior Stage**.

If the Capability itself is plausible but insufficiently justified:

> Record it as an Open Question rather than treating it as established Structure.

If the decision materially changes validated product scope:

> Make the uncertainty explicit and return it for appropriate validation.

If only detailed behavior is unknown:

> Do not solve it during Structure merely because the question has been discovered.

---

# Structural Dependencies

Analyze functional dependencies when they materially affect:

- completeness;
- priority;
- actor ability to continue work;
- the product value loop.

Example:

```text
Invite member
↓
Accept invitation
↓
Member can access project
```

If a High Capability depends on another Capability, review whether the dependency should also receive High priority.

Do not model technical dependencies during the **Structure Stage**.

Examples of technical dependencies that belong later:

- API calls;
- databases;
- queues;
- storage;
- authentication providers;
- infrastructure components.

---

# Validated Scope Coverage

Before completing the **Structure v1 Document**, verify that functionality validated in the **Shape v2 Document** has not disappeared.

For each validated MVP capability, determine whether it is:

- Covered;
- Transformed;
- Gap.

Covered means it has a clear representation in Structure.

Transformed means the Shape capability was legitimately decomposed or represented differently.

Gap means validated functionality has no adequate representation.

Resolve or explicitly record material Gaps before completing the proposed Structure.

---

# Functional Completeness

Validated Scope Coverage and Functional Completeness are different checks.

Validated Scope Coverage asks:

> Did we lose anything that was validated during Shape?

Functional Completeness asks:

> Did we discover the surrounding functionality required for the validated product to operate coherently in its validated context?

A Structure may have perfect Scope Coverage and still be functionally incomplete.

For each Functional Area, review:

- actors;
- start of work;
- return to existing work;
- functional object lifecycle;
- management responsibilities;
- continuation;
- important negative paths;
- recovery;
- connections to the rest of the value loop.

At product level, additionally review whether cross-cutting product-readiness concerns create missing functional responsibilities.

---

# Analysis vs Document Content

The analysis performed during the **Structure Stage** is broader than the information that needs to appear in the **Structure Document**.

The agent must perform relevant analytical controls, including:

- Validated Scope Coverage;
- Functional Discovery;
- Product Readiness review;
- Functional Completeness;
- dependency analysis;
- JTBD support review;
- Value Proposition support review where relevant;
- MVP value-loop review.

These checks exist to improve the quality of the functional Structure.

They do not need to be reproduced as detailed analytical reports in the **Structure Document**.

The **Structure Document** should contain primarily:

- Functional Areas;
- Capabilities;
- Actors;
- Priority;
- useful Comments;
- material Structural Gaps;
- material structural Open Questions;
- concise validation status.

Only material findings from analytical checks should be persisted.

Do not turn the **Structure Document** into a report describing every analytical step performed by the agent.

---

# Process

## Step 1 — Review Shape v2 Document

Read the complete **Shape v2 Document**.

Understand:

- primary actors;
- Target Market and material market-specific needs;
- primary JTBD;
- Value Proposition;
- validated MVP scope;
- MVP value loop;
- constraints;
- relevant assumptions and Open Questions.

Create an internal inventory of validated MVP functionality.

---

## Step 2 — Identify Functional Areas

Group product responsibilities into coherent Functional Areas.

Functional Areas should represent product responsibilities rather than screens, entities, or technical components.

Avoid premature detailed decomposition.

---

## Step 3 — Build Initial Capability Inventory

Identify Capabilities directly supported by the **Shape v2 Document**.

Internally distinguish these as Validated.

Do not assume this inventory is complete.

---

## Step 4 — Perform Functional Discovery

For every Functional Area, apply the relevant discovery lenses:

- Actor Lens;
- Functional Object Lens;
- Lifecycle Lens;
- Continuation Lens;
- Recovery Lens;
- Value Loop Lens.

At product level, also apply the Product Readiness Lens to identify cross-cutting functional responsibilities that may not belong naturally to an existing core flow.

Add justified Derived Capabilities where necessary.

Do not add generic functionality without product-specific rationale.

---

## Step 5 — Review Decomposition Depth

Check whether each Capability represents a meaningful functional intention.

Split overly broad Capabilities when they hide distinct actor intentions.

Merge trivial or artificial decomposition.

Use optional grouping only when it materially improves readability.

---

## Step 6 — Assign Actors

Identify the actor or actors responsible for each Capability.

Actor responsibility should describe who performs or owns the functional action.

Do not use technical components as actors.

---

## Step 7 — Assign Functional Priority

Assign:

- High;
- Medium;
- Low.

Base priority on product-specific functional importance.

Do not use Structure priority to redefine validated Product Stage scope.

---

## Step 8 — Check Structural Dependencies

Identify dependencies that materially affect completeness or priority.

Do not document every dependency.

Persist only material findings.

---

## Step 9 — Verify Validated Scope Coverage

Check every validated MVP capability from the **Shape v2 Document**.

Ensure each is:

- Covered;
- Transformed;
- or explicitly identified as a Gap.

Do not require the complete coverage matrix to appear in the **Structure Document** unless it contains material findings useful for review.

---

## Step 10 — Review Functional Completeness

Review every Functional Area using the discovery lenses.

Check whether basic functionality still needs to be rediscovered by a later Stage.

Pay particular attention to:

- return to existing work;
- actor handoffs;
- lifecycle continuation;
- functional object termination;
- negative paths;
- recovery;
- end-to-end value-loop completion.

Review the product as a whole using the Product Readiness Lens.

Check whether the validated context creates cross-cutting functional responsibilities that are absent from the proposed Structure.

---

## Step 11 — Verify Product-Level Support

Confirm that the resulting Structure functionally supports:

- primary JTBD;
- validated Value Proposition;
- the complete MVP value loop;
- material functional responsibilities created by the validated Target Market and Constraints.

Record only material gaps or uncertainties in the **Structure Document**.

---

## Step 12 — Produce Structure v1 Document

Create the **Structure v1 Document** using the Structure template.

The primary artifact is the functional WBS:

```text
Functional Area
↓
Capability
↓
Actor + Priority + useful Comment
```

Do not reproduce internal analytical work unless it creates a material finding relevant to Consultant Review.

Stop after producing the **Structure v1 Document**.

Consultant Review must not be simulated.

---

## Step 13 — Consultant Review

The consultant reviews the proposed Structure.

The consultant may:

- accept;
- reject;
- add;
- remove;
- merge;
- split;
- rename;
- move;
- reprioritize;

functional elements.

The consultant may use Miro or another visual workspace during review.

The purpose of review is analytical synthesis, not approval of agent output.

---

## Step 14 — Produce Structure v2 Document

After actual Consultant Review findings are available:

1. incorporate accepted review decisions;
2. remove rejected functionality;
3. add discovered functionality;
4. apply decomposition changes;
5. apply actor changes;
6. apply priority changes;
7. repeat Validated Scope Coverage;
8. repeat Functional Discovery and Product Readiness review;
9. repeat Functional Completeness review;
10. repeat dependency and value-loop checks;
11. resolve or record remaining Structural Gaps and Open Questions;
12. produce the **Structure v2 Document**.

The **Structure v2 Document** becomes the primary input to the **Behavior Stage**.

---

# Recommended Structure Document Format

```text
Status

Functional Structure

    Functional Area

        Capability | Actors | Priority | Comment

    Functional Area

        Capability | Actors | Priority | Comment

Structural Gaps

Open Questions

Structure Validation

Structure Status
```

Comments should be included only when they provide useful information, such as:

- an important assumption;
- an unresolved structural choice;
- unusual actor responsibility;
- rationale necessary to understand a non-obvious Capability.

Do not fill Comments merely for formatting consistency.

---

# Success Criteria

The **Structure Stage** succeeds when:

- the product is decomposed into coherent Functional Areas;
- Functional Areas contain meaningful Capabilities;
- decomposition is sufficiently deep for the next Stage;
- validated Shape functionality remains traceable;
- Functional Discovery has been performed for every Functional Area;
- Product Readiness has been reviewed at product level;
- important implied functionality has been identified;
- justified cross-cutting functional responsibilities have been identified;
- Derived functionality has product-specific justification;
- actors are identified where useful;
- priorities have been proposed and reviewed;
- important lifecycle and continuation behavior is functionally represented;
- important recovery needs are functionally represented;
- material dependencies have been considered;
- primary JTBD are functionally supported;
- the complete validated MVP value loop is functionally supported;
- material functional implications of Target Market and Constraints are represented;
- Structural Gaps are explicit;
- structural Open Questions are explicit;
- the **Structure Document** contains the functional model rather than an unnecessary analytical report;
- the **Structure v1 Document** has undergone real Consultant Review before the **Structure v2 Document** is produced;
- the **Structure v2 Document** is sufficiently complete for the **Behavior Stage**.

---

# Failure Conditions

The **Structure Stage** fails when:

- the **Structure Document** merely transcribes the **Shape v2 Document**;
- Shape wording is assumed to be a complete functional model;
- obvious implied functionality is omitted;
- material cross-cutting functional responsibilities implied by the validated product context are omitted;
- generic SaaS functionality is added without product-specific justification;
- Product Readiness is treated as a mandatory generic feature checklist;
- Derived functionality is treated as validated fact;
- Functional Areas are based primarily on screens or technical components;
- artificial Capability Groups are created merely for hierarchy;
- broad Capabilities hide materially different actor intentions;
- Capabilities are decomposed into trivial UI actions;
- priority is based on convention rather than product need;
- Structure priority silently redefines validated Product Stage scope;
- important dependencies are ignored;
- Validated Scope Coverage is confused with Functional Completeness;
- the value loop stops before its validated meaningful outcome;
- detailed Actor/System flows are produced during Structure;
- detailed Requirements are produced during Structure;
- technical architecture is produced during Structure;
- internal analytical checks are unnecessarily reproduced as large reports in the **Structure Document**;
- the **Structure v1 Document** is treated as reviewed without actual Consultant Review;
- the **Structure v2 Document** remains so shallow that the **Behavior Stage** must rediscover basic product functionality.