# DevelopmentConexus Engineering Protocols

Canonical home for **organization-wide engineering collaboration protocols** that operationalize, but do not redefine, the DevelopmentConexus Engineering Method.

## Authority map

```text
developmentconexus-ops/conexus-methodology/METHOD.md
→ canonical reasoning/decision method

CHALLENGER-REVIEW-PROTOCOL.md
→ proposed independent challenger collaboration protocol; authority after ratification

profiles/FABLE.md
→ proposed current Fable realization profile; effective after protocol ratification

consuming repository AGENTS.md + canonical project authorities
→ project-specific read order, status, architecture and execution gates
```

The Method remains the higher reasoning authority. This repository deliberately does not copy its decision core.

## Why this repository exists

Repeated cross-repository work exposed a real failure class: every new Lead/Fable session was re-specifying who is authority, how an adversarial review works, what counts as a material finding, whether research is allowed, how Round 2 is admitted and where Fable returns its result.

The fix is one provider-neutral protocol plus replaceable challenger profiles—not larger prompts in every project.

## Files

- [`CHALLENGER-REVIEW-PROTOCOL.md`](CHALLENGER-REVIEW-PROTOCOL.md) — proposed protocol v1.0.0; pending independent review + operator ratification.
- [`profiles/FABLE.md`](profiles/FABLE.md) — proposed Fable profile v1.0.0; effective only with the ratified parent protocol.
- [`AGENTS.md`](AGENTS.md) — bootstrap and repository boundary.

## Adoption gate

Do **not** adopt this protocol into consuming repositories while its status is `PROPOSED`. First complete independent challenger review, Lead confrontation and explicit operator ratification; then change the protocol/profile status to `ACCEPTED`.

## Consuming `AGENTS.md` contract

A consuming repository's `AGENTS.md` is a **small bootstrap/router**, not a methodology, status ledger, roadmap, architecture authority or copy of organization-wide standards.

Repositories SHOULD converge on this structural contract while preserving their own authority paths and safety rails:

```text
1. scope / bootstrap role
2. fresh-session read order
3. organizational standards consumed + versions
4. repository authority / program routing
5. stable repository safety rails
6. verification / Git rules
```

The section contents are intentionally repository-specific. Standardization means the same routing semantics, not identical `AGENTS.md` files.

### Normal work

Do not load challenger material into every session.

```text
repository AGENTS.md
→ canonical Method or declared local availability mirror
→ repository router/current authority
→ exact task authority/evidence
→ task
```

### Independent challenger work

Only when independent challenger review is required or deliberately invoked:

```text
repository AGENTS.md
→ canonical Method or declared local availability mirror
→ repository router/current authority
→ exact accepted authority/evidence needed to form an independent view
→ CHALLENGER-REVIEW-PROTOCOL.md
→ applicable challenger profile (for example profiles/FABLE.md)
→ candidate/dialogue LAST
```

A candidate/dialogue is review input, never an earlier authority source. This ordering exists to reduce anchoring and confirmation bias.

### Consumed versions

Each consuming repository SHOULD declare the organizational versions it has deliberately adopted, for example:

```text
DevelopmentConexus Engineering Method: 1.0.0
Challenger Review Protocol: 1.0.0
Fable Profile: 1.0.0
```

Do not silently treat moving `main` as an implicit behavior update. A newer organizational version becomes effective for a consuming repository only when that repository deliberately adopts it through its normal governance.

After ratification, stable protocol/profile releases SHOULD be identifiable by Git version/tag so consumers can name the adopted version without packages, submodules or sync infrastructure.

### Mirror policy

A frequently consumed Method mirror MAY remain local when the repository already declares it as an availability copy rather than a fork.

The challenger protocol and provider profiles SHOULD remain canonical cross-repository reads by default because they are conditional inputs. Do not create local copies merely for convenience.

A local protocol/profile mirror is justified only when the execution environment cannot reliably read the canonical repository at bootstrap. Any such mirror must:

- identify the canonical repository/path and consumed version;
- be explicitly non-independent authority;
- be replaced from canonical bytes rather than locally reinterpreted;
- fail visibly when freshness cannot be established if exact version parity matters.

Do not add sync infrastructure until this exception is a real repeated consumer.

## Adoption by a consuming repository

Once this protocol is ratified, a consuming repository SHOULD make only the smallest `AGENTS.md` integration necessary:

- preserve its existing repository-specific read order, authority owners and safety rails;
- declare the consumed Method / Challenger Protocol / profile versions;
- conditionally route challenger work to the central protocol/profile;
- keep candidate/dialogue input after independent authority reconstruction;
- remove duplicated local Fable/challenger instructions only when the central canonical documents cover the same semantics exactly.

Repository-specific authority still determines **what is true about that product**. The challenger protocol determines only **how independent challenge is performed**.

## Default task handoff after adoption

Once adopted, a task-specific handoff should contain only what changes for that review, for example:

```text
Review <candidate> under DevelopmentConexus Challenger Review Protocol v1.0.0 using Fable Profile v1.0.0.
Focus: <task-specific risks/questions>.
Return the canonical challenger output in chat.
```

The handoff should not repeat the protocol.
