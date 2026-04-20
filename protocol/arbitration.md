# Verification and Arbitration Protocol

The Verification Layer evaluates execution receipts produced by one or more lanes.

Its purpose is to determine the accepted output for a workload.

---

## Responsibilities

The verification layer must:

• collect receipts from execution lanes  
• verify receipt authenticity  
• compare execution outcomes  
• determine accepted result  

---

## Receipt Verification

For each receipt:

1. Verify lane signature
2. Confirm permit reference
3. Validate output hash integrity

---

## Arbitration

Arbitration determines whether one or more lane receipts support an accepted output.

The default public-safe policy is **reject_on_divergence**.

If lane outputs diverge and the permit does not specify a deterministic arbitration policy, the result is rejected.

This default preserves TriTrap's fail-closed posture.

---

## Agreement Criteria

Receipts are considered in agreement when:

1. each receipt is authentic
2. each receipt references the same permit
3. each receipt references the same authorized workload
4. each receipt reports an output that satisfies the permit's verification policy

Agreement is not assumed from receipt presence alone.

---

## Public Arbitration Policies

Permits may define deterministic arbitration policies.

Public protocol examples include:

| Policy | Behavior |
| --- | --- |
| reject_on_divergence | Reject if required lane outputs do not match the permit's verification rule. |
| strict_match | Accept only if all required lane outputs match exactly. |
| majority_accept | Accept the majority result only when the permit explicitly allows majority resolution. |
| weighted_lane | Prefer a designated lane only when the permit explicitly defines lane weighting. |
| manual_review | Hold the result for maintainer or reviewer action. |

The public repository describes policy semantics, not private verifier implementation.

---

## Divergence Handling

When required lanes disagree:

1. the verification layer records the divergence where implemented
2. the accepted output is withheld unless a deterministic permit policy resolves the conflict
3. the default outcome is rejection
4. private operational evidence remains outside this repository

The verification policy is defined in the permit.

---

## Output Resolution

After arbitration completes:

• accepted output is returned to the client
• verification result may be recorded
• receipts may be archived for auditing where the deployment implements durable receipt archival
