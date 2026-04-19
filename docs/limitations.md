# Limitations

TriTrap is designed around governed execution, role separation, verification, and fail-closed evidence handling.

Those strengths do not remove every risk. This document states public limitations directly.

---

## Latency and Cost

Multi-lane execution can increase latency and compute cost.

Fast mode may reduce latency by using a single lane, but it provides less comparative assurance than verified or critical modes.

Verified, critical, and audit modes may require more compute, more evidence handling, and more review overhead.

---

## Shared Failure Modes

Multi-lane comparison does not guarantee correctness if all lanes share the same flaw.

Examples include:

- the same model error across lanes
- the same dependency bug across lanes
- the same prompt or workload ambiguity across lanes
- the same flawed verification policy

Role separation improves detection of divergence. It does not prove universal correctness.

---

## Permit Dependency

TriTrap depends on permit integrity.

If permit generation, validation, scope definition, or expiration handling is weak, the execution boundary is weakened.

Permit-governed execution must be paired with disciplined permit policy.

---

## Verification Policy Quality

Verification is only as strong as the policy being applied.

Weak policies can allow weak conclusions.

For high-consequence workloads, unresolved divergence should fail closed unless a deterministic permit policy explicitly defines another outcome.

---

## Evidence Completeness

Evidence packages support reviewability only when required proof material is present and internally consistent.

Incomplete evidence should not be treated as success.

The public evidence model describes the contract. It does not publish private evidence archives.

---

## Public Proof Limits

Synthetic proof examples are useful for explaining behavior, but they are not private operational evidence.

Redacted examples can improve public credibility, but excessive detail can expose private mechanics.

The public repo therefore prioritizes reviewable structure over raw operational disclosure.

---

## Implementation Variation

Different deployments may implement receipt storage, evidence capture, lane configuration, arbitration, retention, and audit behavior differently.

Protocol compatibility does not imply identical deployment mechanics.

Public documentation should preserve that distinction.
