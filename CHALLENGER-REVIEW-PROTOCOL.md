# DevelopmentConexus Independent Challenger Review Protocol

**Version:** 1.0.0  
**Status:** PROPOSED — PENDING INDEPENDENT REVIEW  
**Authority:** organizational engineering collaboration standard  
**Scope:** DevelopmentConexus engineering work using an independent challenger, human or agentic  
**Reasoning authority:** `developmentconexus-ops/conexus-methodology/METHOD.md`  
**Compatible method baseline:** DevelopmentConexus Engineering Method v1.0.0

## Objective

Obtain **independent adversarial signal with minimum ceremony**: challenge material engineering decisions deeply enough to escape local maxima, hidden assumptions and agreement theater without creating a second authority, review bureaucracy or provider-specific process.

This protocol operationalizes challenger collaboration. It does **not** redefine the DevelopmentConexus Engineering Method, product architecture, repository authority, acceptance criteria or implementation workflow.

---

## 1. Authority model

Three roles are conceptually distinct:

```text
Lead
→ performs the primary analysis/design
→ owns technical confrontation and consolidation

Challenger
→ independently attacks the candidate
→ produces evidence, counterarguments and findings
→ never becomes decision/acceptance authority by being the reviewer

Ratifier
→ the human/operator or other authority designated by the consuming repository
→ ratifies the final candidate when ratification is required
```

The same person/tool MAY fill multiple mechanical roles only when the consuming repository permits it, but a review claimed as **independent** must preserve actual independence sufficient for the claim.

Normative laws:

```text
review != authority
severity != requirement
score != requirement
reference platform behavior != requirement
challenger agreement != ratification
Lead preference != dismissal of evidence
```

Accepted repository authority remains the baseline for execution. Discovery/challenge may question it only through explicit material evidence and the applicable Decision Loop.

---

## 2. Admission and proportionality

Use an independent challenger when required by the DevelopmentConexus Engineering Method or by the consuming repository, and whenever the expected decision-quality gain justifies the review cost.

The Method's current floor applies especially to decisions that create/move authority or trust boundaries, have external/irreversible effects, or bind multiple repositories.

Do not turn this floor into universal ceremony.

Review depth scales with:

```text
materiality
irreversibility
uncertainty
blast radius
novelty of the failure class
```

A bounded package should remain bounded. Do not force one microdecision per review. Split only when a sub-question has materially independent owner/authority, blocks the rest, or contains a contradiction requiring its own Decision Loop.

---

## 3. Independence before candidate anchoring

The challenger MUST reconstruct enough current authority and problem context to form an independent view **before treating the Lead's decomposition or preferred solution as the frame of the problem**.

Default read shape:

```text
consuming repository AGENTS/read order
→ canonical DevelopmentConexus Method
→ current project authority/status
→ exact accepted authority relevant to the question
→ material evidence/current external facts when needed
→ THEN the candidate/dialogue to challenge
```

If a candidate is encountered first, it remains input, never authority.

The challenger should ask, implicitly or explicitly:

> If the Lead had proposed the opposite structure, what would the current authority and evidence still force us to conclude?

A review that only checks whether the candidate is internally tidy is insufficient when the material question is whether the candidate is the right structure at all.

---

## 4. Canonical collaboration flow

For a material package, the default flow is:

```text
1. Lead independent analysis
2. NON-AUTHORITATIVE candidate/dialogue package when useful
3. compact task-specific challenger handoff
4. Challenger independent adversarial review
5. Lead technical confrontation/classification
6. Round 2 ONLY for surviving material contradiction
7. consolidated candidate
8. ratification by the repository-designated authority
9. only then durable authority/status update when applicable
```

The candidate/review may live only in chat when durable provenance would add no decision value. A repository file is not required merely to make the process look formal.

No implementation or authority mutation is implied by a review.

---

## 5. Challenger review obligations

The challenger applies the DevelopmentConexus Engineering Method proportionally and attacks the candidate rather than paraphrasing it.

For material decisions, challenge at least the dimensions that can falsify the decision:

```text
root cause vs symptom
Global Maximum vs local maximum
essential vs accidental complexity
YAGNI / overengineering / foreseeable retrofit
owner / authority / boundary
mechanism becoming hidden authority
missing or invented consumer
trust / external-effect / recovery exposure when applicable
public/durable contract consequences when applicable
technology/provider overfit when applicable
proof strategy / falsifiability
reopen conditions
hardest plausible future change supported by current evidence
```

The challenger MUST articulate the **strongest serious counterargument** to the preferred candidate.

The challenger SHOULD try credible alternatives, including a structurally simpler alternative and, when evidence supports it, a materially different structure outside the Lead's initial option set.

Do not manufacture alternatives for symmetry when only one is credible.

---

## 6. Research behavior

Current authority is the execution baseline; it is **not an inquiry boundary**.

The challenger SHOULD research when a material conclusion depends on facts that are unstable, uncertain, provider/framework-specific, externally standardized or likely to hide a better alternative.

Evidence preference:

```text
current repository/source evidence for repository claims
primary/official external sources for unstable external facts
current library/framework documentation for technology behavior
Context7 or equivalent current-doc tooling when available and materially useful
real runtime/probes when documentary evidence cannot prove the claim
```

References provide evidence and alternatives. They do not create requirements.

Forbidden inference:

```text
Factory/Mitra/Mastra/<platform> has X
→ therefore DevelopmentConexus must build X
```

A new capability still requires current consumer, risk, defect class or accepted product objective under the Method.

Research should stop when evidence is sufficient for the claim. Do not perform broad market surveys to decorate a review.

---

## 7. Material finding classification

A challenger observation becomes a **material finding** only when it can materially affect correctness, authority, boundary, trust, persistent/public meaning, external effect, recovery/temporal correctness, user-observable contractual behavior or hard-to-reverse structure.

A material finding should identify:

```text
Finding ID
→ implicated authority/invariant/assumption
→ evidence or counterexample
→ why the consequence is material
→ required correction or routing, if known
```

Classify reviewer output before acting on it:

### A. Defect against existing authority

The candidate contradicts an accepted invariant/decision or fails to realize a required property.

→ correct the candidate or reopen the smallest implicated authority if the authority itself is invalidated.

### B. Material new evidence against existing authority

Evidence may invalidate the accepted structure.

→ return to the applicable Decision Loop; do not smuggle the change in as a review correction.

### C. Proposed new requirement/capability

Not required by current authority/evidence.

→ classify through `MUST DECIDE / DEFER SAFELY / REJECT` or the consuming repository's equivalent; reviewer enthusiasm does not admit it.

### D. Preference / wording / polish / equivalent realization

Does not change a material property.

→ may be adopted opportunistically; MUST NOT force Round 2 or block ratification.

### E. Unknown

Evidence is insufficient.

→ preserve Unknown; route a focused research/probe question when the unknown is load-bearing.

Reviewer-provided severity labels are evidence metadata at most. They never create authority.

---

## 8. Canonical challenger output

Default output is compact and uses this semantic structure:

```text
VERDICT
READY_FOR_CONSOLIDATION
| MATERIAL_REVISION_REQUIRED
| BLOCKED_BY_LOAD_BEARING_UNKNOWN

MATERIAL FINDINGS
NONE
or
F-01 — <finding>
  Implicates: <authority/invariant/assumption>
  Evidence: <deciding evidence/counterexample>
  Material consequence: <why it matters>
  Correction/routing: <bounded correction or Decision Loop>

STRONGEST COUNTERARGUMENT
<best serious argument against the candidate>

MUST / DEFER / REJECT DIVERGENCES
<only actual classification divergences; NONE is valid>

ROUND 2
REQUIRED | NOT_REQUIRED
Reason: <material reason>
```

Equivalent compact formatting is acceptable if semantic fields are preserved.

Default exclusions:

```text
no numeric review score
no arbitrary quality threshold
no severity theater
no restatement of the whole candidate
no generic best-practice checklist dump
no requirement invented from reviewer preference
```

A consuming repository may require additional fields only when they change a real decision or proof obligation.

---

## 9. Lead technical confrontation

The Lead MUST classify each challenger finding against current authority/evidence instead of automatically accepting or dismissing it.

For each material disagreement, the Lead should be able to state:

```text
ACCEPT
→ finding is valid; candidate changes or Decision Loop is invoked

REJECT
→ finding conflicts with stronger authority/evidence or is not material
→ state the technical basis, not reviewer status

UNKNOWN
→ load-bearing evidence is insufficient
→ route focused research/probe

DEFER / REJECT SCOPE
→ proposed improvement is valid in general but not required now
→ preserve trigger/later owner when needed
```

Agreement theater is prohibited in both directions:

```text
"Fable found it, so add it"       = invalid
"the Lead designed it, so keep it" = invalid
```

The winner is the strongest authority/evidence/reasoning under the Method.

---

## 10. Round 2 admission

Round 2 is **not a normal step**. It exists only when a material contradiction survives the Lead confrontation.

Round 2 is REQUIRED when at least one is true:

```text
Lead rejects a material finding on substantive technical grounds and the challenger has relevant contrary evidence
current authority admits two materially different interpretations that change the decision
new evidence could invalidate the selected structure and has not been resolved
load-bearing Unknown can be narrowed by a focused challenger pass without requiring a separate probe
```

Round 2 is NOT justified by:

```text
wording
naming
format
polish
different but materially equivalent decomposition
reviewer request for more detail
numeric score
preference
non-blocking suggestion
```

Round 2 MUST be focused on the unresolved contradiction. Do not resend the entire problem unless the contradiction proves the original frame invalid.

A third round requires a newly surfaced material contradiction or evidence—not failure to reach social agreement.

---

## 11. Ratification and authority mutation

The challenger never self-ratifies the candidate.

When the consuming repository requires human/operator approval:

```text
challenger review
→ Lead consolidation
→ clearly identified consolidated candidate
→ explicit ratification
→ only then authority/status mutation
```

A review file, chat message, PR comment, model confidence or lack of objections is not implicit approval.

If the repository allows natural-language ratification such as `Aprovado`, the target candidate must be unambiguous from context.

When review uncovers a new material requirement, the final authority must record the resulting decision through the repository's normal Decision Loop; it must not cite “reviewer requested it” as the authority basis.

---

## 12. Review artifacts and transport

Transport and durable authority are separate concerns.

```text
chat
PR comment
review file
shared document
→ transport/provenance
-X-> authority by medium
```

Default behavior:

- challenger returns the review through its normal interactive transport;
- durable review files are optional and should exist only when they materially improve provenance, asynchronous handoff or later auditability;
- any persisted review/dialogue artifact MUST identify itself as non-authoritative unless a consuming repository explicitly ratifies content into an authority document;
- do not update `LEDGER`, decision registers, architecture authority or product code merely because a review completed.

The Lead must not assume that “review completed” means the challenger created a Git commit or PR comment. The handoff/profile defines the return channel.

---

## 13. Stop rule

Stop the challenger loop when:

```text
current authority is reconstructed sufficiently for the claim
credible alternatives were attacked
strongest counterargument is addressed
material findings are resolved/classified
load-bearing Unknowns are routed
no material contradiction remains
```

Do not continue reviewing to increase confidence cosmetically.

A review that finds `MATERIAL FINDINGS = NONE` is a valid successful result.

---

## 14. Reopen/change triggers for this protocol

Revisit this protocol when evidence shows that it:

- systematically creates agreement theater or anchoring rather than independent challenge;
- causes repeated review ceremony without decision-quality gain;
- fails to distinguish findings from new requirements;
- produces repeated cross-repository confusion about transport, authority or ratification;
- cannot support a materially new challenger class (e.g. automated continuous reviewer, multi-party formal assurance) without weakening the current invariants;
- conflicts with a future accepted amendment of the DevelopmentConexus Engineering Method.

Provider/tool changes alone normally belong in profiles, not this protocol.
