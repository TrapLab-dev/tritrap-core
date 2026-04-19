# Proof Slice Example

This document provides a public-safe synthetic proof slice.

It demonstrates the shape of a governed TriTrap run without publishing private evidence, live node names, runtime paths, proof archives, verifier internals, keys, topology, or operational commands.

The values below are illustrative and are not copied from private runtime evidence.

---

## Scenario

Mode: `verified`

Arbitration policy: `strict_match`

Default fallback: `reject_on_divergence`

Workload: synthetic prompt classification

Expected behavior: two independent lane receipts support the same accepted output.

---

## Synthetic Request

```text
request_id: example-request-001
mode: verified
permit_id: example-permit-001
workload_ref: synthetic-workload-alpha
verification_policy: strict_match
```

---

## Synthetic Lane Receipts

```text
receipt_id: example-receipt-lane-a
permit_id: example-permit-001
lane_role: execution_lane
workload_ref: synthetic-workload-alpha
output_ref: synthetic-output-match
receipt_status: complete
```

```text
receipt_id: example-receipt-lane-b
permit_id: example-permit-001
lane_role: verification_lane
workload_ref: synthetic-workload-alpha
output_ref: synthetic-output-match
receipt_status: complete
```

---

## Verification Result

```text
verification_result: accepted
reason: required lane receipts are authentic, permit-bound, workload-bound, and output-equivalent under strict_match
accepted_output_ref: synthetic-output-match
evidence_boundary: public synthetic example
```

---

## Divergence Example

If the same request produced different output references:

```text
lane_a_output_ref: synthetic-output-one
lane_b_output_ref: synthetic-output-two
verification_result: rejected
reason: lane outputs diverged under strict_match
fallback_policy: reject_on_divergence
```

The result is rejected because the permit did not define a deterministic policy that accepts divergent outputs.

---

## Public Interpretation

This proof slice demonstrates:

- permit-bound execution
- independent lane receipts
- output comparison
- deterministic arbitration
- fail-closed rejection on unresolved divergence

This proof slice does not disclose:

- private node names
- private runtime paths
- private proof packages
- private verifier internals
- key material
- deployment topology
- operational commands
