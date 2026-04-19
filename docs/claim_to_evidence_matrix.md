# Claim-to-Evidence Matrix

This matrix binds strong public TriTrap claims to evidence classes.

It is designed to prevent claim drift. It does not publish private deployment mechanics, live proof archives, verifier internals, topology, keys, paths, or operational commands.

---

## Evidence Classes

| Evidence class | Meaning | Public handling |
| --- | --- | --- |
| PUBLIC_ARCHITECTURE | Architecture or protocol behavior described in this repository. | Public. |
| PUBLIC_SYNTHETIC | Synthetic example that demonstrates shape or expected behavior. | Public, but not live evidence. |
| PRIVATE_CONTROLLED_EVIDENCE | Dated or bounded operator evidence available only through controlled review. | Withheld unless deliberately redacted. |
| WITHHELD_OPERATIONAL | Real or relevant operational material that is not safe to publish. | Withheld. |
| NOT_CLAIMED | A statement the public repo does not make. | Explicitly excluded. |
| PLANNED | Identified future hardening or validation direction. | Public as future work only. |

---

## Matrix

| Claim | Public statement | Evidence class | Validation type | Status | Reviewer access | Disclosure boundary | Residual risk |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TriTrap separates authorization, execution, and verification responsibilities. | Gate, lane, and verification roles are described as distinct responsibilities. | PUBLIC_ARCHITECTURE | Role-model review | PROVEN | Public | No topology or runtime identity details. | Public docs do not prove every private deployment shape. |
| Execution is permit-scoped. | Workloads are authorized before dispatch under bounded authority concepts. | PUBLIC_ARCHITECTURE + PRIVATE_CONTROLLED_EVIDENCE | Protocol review and controlled evidence review | PROVEN | Public concept, private validation | No live permits, paths, keys, or commands. | Public repo does not independently prove every live permit decision. |
| Receipts provide reviewable execution evidence. | Lanes produce receipt-style evidence for verification and arbitration. | PUBLIC_ARCHITECTURE + PRIVATE_CONTROLLED_EVIDENCE | Receipt contract review | PROVEN | Public concept, private validation | No raw receipt records. | Public examples show shape, not live evidence. |
| Divergent lane outputs should not be silently accepted. | Default public arbitration posture is `reject_on_divergence`. | PUBLIC_ARCHITECTURE + PUBLIC_SYNTHETIC + PRIVATE_CONTROLLED_EVIDENCE | Arbitration review and negative-case validation | PROVEN | Public rule, private validation | No private arbitration traces. | Public repo does not expose every policy implementation. |
| Invalid or incomplete evidence fails closed. | Missing, inconsistent, or unverifiable evidence is treated as invalid. | PUBLIC_ARCHITECTURE + PRIVATE_CONTROLLED_EVIDENCE | Negative-case validation | PROVEN | Public rule, private validation | No verifier internals or proof archives. | Public repo does not prove all deployment failure paths. |
| Multi-lane execution increases comparative assurance. | Verified and critical modes can compare outputs across lanes. | PUBLIC_ARCHITECTURE | Mode and limitation review | PROVEN | Public | No hardware, model, or deployment details. | Agreement is not universal correctness. Shared failure modes remain. |
| Lane independence is meaningful only when failure domains differ. | The public repo treats independence as a design requirement, not a universal guarantee. | PUBLIC_ARCHITECTURE + PLANNED | Failure-domain review | STAGED | Public posture, private testing when available | No lane stack disclosure. | Independence must be validated per deployment. |
| Runtime evidence exists outside the public repo. | The public repository is not the sole proof source. | WITHHELD_OPERATIONAL + PRIVATE_CONTROLLED_EVIDENCE | Controlled diligence review | WITHHELD | Controlled review only | No raw packages, hashes, paths, or commands. | Public confidence has a deliberate proof ceiling. |
| Synthetic proof slice demonstrates behavior shape. | The proof slice is synthetic and does not claim to be live evidence. | PUBLIC_SYNTHETIC | Documentation example review | PROVEN | Public | No operational artifact disclosure. | It proves structure, not runtime enforcement. |
| Public docs are not a deployment manual. | Operational mechanics remain withheld. | NOT_CLAIMED | Boundary review | PROVEN | Public | No service definitions or runbooks. | Some reviewers will require private diligence to assess implementation. |
| Latency and cost differ by execution mode. | Fast, verified, critical, and audit modes trade latency for assurance. | PUBLIC_ARCHITECTURE + PLANNED | Mode review and measured-envelope review | STAGED | Public shape, private measurements | No raw benchmarks unless intentionally released. | Public docs do not publish deployment-specific timing. |

---

## Use Rule

Any strong public claim should map to this matrix or be weakened before publication.

If a claim requires private evidence, the public repo should identify the evidence class and disclosure boundary rather than expose the evidence itself.
