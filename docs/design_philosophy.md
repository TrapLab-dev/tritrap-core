# Design Philosophy

TriTrap is built around a small set of engineering principles.

This document is not a manifesto. It states the public design posture that guides the architecture.

---

## Deny by Default

Execution should require authority.

TriTrap treats uncontrolled execution as the wrong default for high-consequence AI workflows.

A workload should pass through scoped authorization before execution.

---

## Evidence Over Trust

Execution should produce reviewable evidence.

TriTrap favors receipt-style evidence, bounded proof artifacts, and verifier outcomes over informal trust in a completed run.

If evidence is missing, incomplete, or inconsistent, the system should not treat that as success.

---

## Fail Closed

Uncertainty should not silently become acceptance.

When authority, identity, integrity, completeness, or lane agreement cannot be verified, the public-safe default is rejection.

This principle is reflected in the `reject_on_divergence` arbitration posture.

---

## Role Separation

Authorization, execution, and verification should not be collapsed into one indistinct path.

TriTrap separates Gate, execution lane, verification, permit, receipt, and arbitration concepts so that each responsibility can be reasoned about.

---

## Policy Before Assumption

Acceptance should follow policy.

TriTrap uses permits, execution modes, and arbitration policies to define how a workload should be handled.

The system should not rely on vague confidence or unstated fallback behavior.

---

## Human Authority

Automation should remain subordinate to governed authority.

TriTrap is designed to support controlled execution, review, and rejection. It does not treat autonomous completion as the highest goal.

---

## Disclosure Discipline

Public documentation should make the architecture reviewable without making the private deployment directly replicable.

This means separating public posture from private proof, private topology, verifier internals, keys, paths, service definitions, and operational commands.

