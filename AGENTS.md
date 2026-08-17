# DevelopmentConexus Engineering Protocols — Agent Instructions

## Start here

For any work in this repository, read in this order:

1. `developmentconexus-ops/conexus-methodology/METHOD.md` — canonical DevelopmentConexus Engineering Method.
2. `CHALLENGER-REVIEW-PROTOCOL.md` — canonical organizational challenger-collaboration protocol.
3. the applicable profile under `profiles/` when a named challenger/tool is used.
4. `README.md` only as a repository/adoption map.

## Authority boundary

- The **DevelopmentConexus Engineering Method** owns how engineering is reasoned about and decided.
- `CHALLENGER-REVIEW-PROTOCOL.md` owns only the mechanics and invariants of independent challenger collaboration.
- `profiles/*` specialize transport/tool realization and MUST NOT redefine the Method or generic challenger protocol.
- Consuming repositories continue to own their product architecture, current status, read order, decision authority, implementation gates and safety rails.

No document in this repository may turn a challenger, reviewer, model, score, platform or research source into requirement/acceptance authority by convenience.

## Editing rule

A material change to `CHALLENGER-REVIEW-PROTOCOL.md` requires explicit operator ratification and must itself be reasoned about under the current DevelopmentConexus Engineering Method.

A profile change may be bounded when it changes only transport/tool mechanics. If it changes reviewer independence, authority, admission, output semantics, escalation or ratification, treat it as a protocol-level material change.

Do not duplicate `METHOD.md` here. Cite it.

## Repository rule

Keep this repository small. Do not add product-specific workflow, repository status, implementation plans, sync machinery, CI frameworks, prompt libraries, scorecards or provider-specific ceremony without a demonstrated cross-repository failure class or current consumer.
