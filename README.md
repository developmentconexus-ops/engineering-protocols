# DevelopmentConexus Engineering Protocols

Canonical home for **organization-wide engineering collaboration protocols** that operationalize, but do not redefine, the DevelopmentConexus Engineering Method.

## Authority map

```text
developmentconexus-ops/conexus-methodology/METHOD.md
→ canonical reasoning/decision method

CHALLENGER-REVIEW-PROTOCOL.md
→ canonical independent challenger collaboration protocol

profiles/FABLE.md
→ current Fable realization profile

consuming repository AGENTS.md + canonical project authorities
→ project-specific read order, status, architecture and execution gates
```

The Method remains the higher reasoning authority. This repository deliberately does not copy its decision core.

## Why this repository exists

Repeated cross-repository work exposed a real failure class: every new Lead/Fable session was re-specifying who is authority, how an adversarial review works, what counts as a material finding, whether research is allowed, how Round 2 is admitted and where Fable returns its result.

The fix is one provider-neutral protocol plus replaceable challenger profiles—not larger prompts in every project.

## Files

- [`CHALLENGER-REVIEW-PROTOCOL.md`](CHALLENGER-REVIEW-PROTOCOL.md) — normative protocol v1.0.0.
- [`profiles/FABLE.md`](profiles/FABLE.md) — Fable profile v1.0.0.
- [`AGENTS.md`](AGENTS.md) — bootstrap and repository boundary.

## Adoption by a consuming repository

A consuming repository SHOULD reference these canonical files from its own `AGENTS.md`; it SHOULD NOT copy the protocol locally by default.

Recommended routing:

```text
repository AGENTS.md
→ canonical DevelopmentConexus METHOD
→ repository-specific authority/read order
→ when independent challenger review applies:
   CHALLENGER-REVIEW-PROTOCOL.md
   → profiles/FABLE.md when Fable is the challenger
→ exact task authority/evidence
```

Repository-specific authority still determines **what is true about that product**. The challenger protocol determines only **how independent challenge is performed**.

### Local mirror exception

A local mirror is justified only when the execution environment cannot reliably read the canonical repository at bootstrap. Any mirror must:

- identify the canonical repository/path and protocol version;
- be explicitly non-independent authority;
- be replaced from canonical bytes rather than locally reinterpreted;
- fail visibly when freshness cannot be established if the consuming workflow depends on exact version parity.

Do not add sync infrastructure until this exception is a real repeated consumer.

## Default task handoff after adoption

Once adopted, a task-specific handoff should contain only what changes for that review, for example:

```text
Review <candidate> under the canonical DevelopmentConexus Challenger Review Protocol using the Fable profile.
Focus: <task-specific risks/questions>.
Return the canonical challenger output in chat.
```

The handoff should not repeat the protocol.
