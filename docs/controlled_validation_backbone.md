# Controlled Validation Backbone

This document defines the public-safe shape of TriTrap controlled validation.

The purpose is to move review from wording to bounded evidence classes without publishing private proof material. This document does not include live evidence packages, raw hashes, runtime paths, node identities, service definitions, keys, commands, or verifier internals.

---

## Validation Goal

TriTrap validation should demonstrate acceptance and refusal, with refusal weighted first.

Positive validation can show that a governed run completes under the expected policy.

Negative validation shows that the system rejects invalid, stale, incomplete, divergent, or unverifiable material instead of accepting it silently.

---

## Core Validation Cases

| Case | Purpose | Expected public outcome | Evidence class |
| --- | --- | --- | --- |
| Accepted governed run | Show that an authorized workload can produce bounded receipts and a governed result. | Accepted under matching policy and complete evidence. | PRIVATE_CONTROLLED_EVIDENCE |
| Rejected bad authority | Show that invalid or missing authority does not dispatch as valid work. | Rejected. | PRIVATE_CONTROLLED_EVIDENCE |
| Rejected divergence | Show that required lane disagreement does not silently become success. | Rejected under `reject_on_divergence`. | PRIVATE_CONTROLLED_EVIDENCE |
| Rejected incomplete evidence | Show that missing required proof material invalidates the result. | Rejected. | PRIVATE_CONTROLLED_EVIDENCE |
| Rejected stale or replayed material | Show that stale or replayed evidence is not treated as fresh authority. | Rejected. | PRIVATE_CONTROLLED_EVIDENCE |
| Mode contrast | Show that fast, verified, critical, and audit modes trade latency, cost, and assurance. | Bounded comparison without private timing disclosure. | PRIVATE_CONTROLLED_EVIDENCE |

---

## Negative Proof Principle

A TriTrap validation set is not mature if it contains only successful runs.

The minimum controlled validation backbone should include refusal cases for:

- invalid authority
- expired or stale material
- mismatched workload identity
- divergent lane outputs under strict policy
- missing lane receipt
- incomplete evidence package
- verifier rejection

These cases are more important than a polished happy path because they test the fail-closed posture under pressure.

---

## Repeatable Review Harness

A controlled review harness should be able to reproduce bounded case outcomes for qualified review without exposing private internals.

The public-safe harness contract is:

1. Select a validation case.
2. Execute or replay the case under controlled conditions.
3. Produce a bounded result summary.
4. Identify the evidence class.
5. Preserve the disclosure boundary.

The public repository may describe this contract. It should not publish the private harness, private data, runtime paths, operational commands, service definitions, or verifier internals.

---

## Failure-Domain Review

Multi-lane comparison is stronger when lanes differ in meaningful failure domains.

Controlled validation should record whether lanes differ by relevant factors such as runtime stack, model family, parser path, configuration path, receipt generation path, or policy handling path.

If meaningful failure-domain separation is not established for a given deployment, the public claim should remain limited to divergence detection and comparative assurance, not universal correctness.

---

## Public Interpretation

This backbone is not a public release of private proof material.

It defines what controlled validation should prove, what proof classes exist, and where public review stops.
