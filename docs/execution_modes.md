# Execution Modes

TriTrap defines different execution postures for different trust, cost, and latency requirements.

This document describes public execution modes. It does not publish private deployment topology, live service configuration, verifier internals, runtime paths, keys, or operational commands.

---

## Mode Summary

| Mode | Lane posture | Verification posture | Typical use |
| --- | --- | --- | --- |
| fast (conceptual) | Single lane | Minimal receipt validation | Low-latency work where speed matters most. |
| verified | Two or more lanes | Output comparison required | Workloads that require stronger assurance. |
| critical | Multiple required lanes | Strict arbitration and fail-closed behavior | High-consequence workloads. |
| audit | Configurable lanes | Extended evidence capture where implemented | Review, demonstration, or controlled audit runs. |

---

## Fast Mode
Fast mode is a conceptual posture. The public repository does not claim fast mode is implemented or publicly proven for the current canonical runtime.


Fast mode favors latency.

In fast mode, a workload may run through a single execution lane with receipt validation.

This mode can reduce compute cost and response time, but it provides less comparative assurance than multi-lane modes.

Fast mode should not be represented as equivalent to multi-lane verification.

---

## Verified Mode

Verified mode favors comparative assurance.

In verified mode, two or more lanes may execute the same authorized workload and return receipts for comparison.

If required lane outputs diverge, the default public-safe behavior is rejection unless the permit defines an explicit arbitration policy.

---

## Critical Mode

Critical mode favors fail-closed assurance.

In critical mode, multiple lanes may be required, arbitration rules should be explicit, and unresolved divergence should reject the result.

This mode is intended for cases where confidence is more important than minimizing latency or compute cost.

---

## Audit Mode

Audit mode favors reviewability.

In audit mode, the system may capture extended evidence where implemented. This can support demonstrations, controlled review, or public-safe examples.

Audit mode should still preserve the non-disclosure boundary. Public examples should use synthetic or redacted proof material rather than private operational evidence.

---

## Tradeoff Principle

TriTrap does not treat every workload as having the same assurance requirement.

Execution mode selection is a policy decision:

- fast mode (conceptual) reduces latency and comparative assurance
- verified mode increases assurance and compute cost
- critical mode prioritizes strict rejection on unresolved divergence
- audit mode prioritizes reviewable evidence boundaries

The permit or governing policy should define the required execution mode.