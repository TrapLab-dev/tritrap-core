# Runtime Maturity Matrix

This matrix summarizes TriTrap runtime maturity in public-safe terms.

It is intended for review and orientation. It does not publish private deployment mechanics, proof archives, verifier internals, topology, keys, paths, or operational commands.

---

## Status Labels

| Label | Meaning |
| --- | --- |
| PROVEN | Backed by dated evidence or verified maintainer records. |
| STAGED | Present in a controlled workflow or hardening path, but not presented as complete public proof. |
| WITHHELD | Real or relevant, but intentionally private. |
| PLANNED | Identified future hardening direction. |

---

## Public Maturity Summary

| Area | Public status | Public claim | Private evidence class |
| --- | --- | --- | --- |
| Gate authorization | PROVEN | Execution is governed through an authorization role before dispatch. | Withheld dated evidence and maintainer records. |
| Role separation | PROVEN | Gate, execution lane, and verification lane responsibilities are separated. | Withheld deployment records. |
| Scoped dispatch | PROVEN | Workloads are dispatched under bounded authority concepts. | Withheld runtime evidence. |
| Receipt concept | PROVEN | Lanes produce receipt-style evidence for verification and arbitration. | Withheld live receipt records. |
| Evidence package model | PROVEN | Runtime evidence is represented as bounded proof artifacts. | Withheld proof packages. |
| Hash-chain evidence model | PROVEN | Ordered integrity checking is part of the public evidence posture. | Withheld verifier outputs and private evidence. |
| Fail-closed behavior | PROVEN | Missing or inconsistent evidence is rejected rather than accepted silently. | Withheld canary and verifier records. |
| Governed compute commitment | STAGED | Expensive or specialized compute should be committed only under explicit governed authorization. | Withheld implementation records and controlled evidence. |
| Transaction-bound telemetry | STAGED | Telemetry should bind observed activity to a governed transaction rather than remain ambient. | Withheld implementation records and controlled evidence. |
| Recurring operation | STAGED | Recurring runtime operation is part of the hardening posture. | Withheld service records and timing details. |
| Status and audit visibility | STAGED | Runtime visibility is treated as a controlled operational requirement. | Withheld audit commands and outputs. |
| Retention posture | STAGED | Evidence retention is governed as an operational control. | Withheld retention procedure and archive details. |
| Hardware lane details | WITHHELD | Hardware and runtime specifics are not published in this repository. | Private deployment material. |
| Verifier internals | WITHHELD | The public verifier contract is described; implementation details remain private. | Private verifier source and maintainer records. |
| Public review process | PLANNED | Public documentation will continue to use conservative review gates. | Internal release review records. |

---

## Public Interpretation

The matrix shows public maturity posture, not a complete deployment recipe.

TriTrap can be reviewed as a governed architecture while private operational records remain controlled.
