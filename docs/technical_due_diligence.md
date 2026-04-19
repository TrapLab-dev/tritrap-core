# Technical Due Diligence

This document gives reviewers a concise public map of TriTrap claims, boundaries, and evidence posture.

It is intended for a fast technical review. It does not publish private deployment mechanics, live proof archives, verifier internals, topology, keys, paths, or operational commands.

---

## What TriTrap Is

TriTrap is a governed execution architecture for controlled dispatch, lane execution, verification, arbitration, and fail-closed evidence handling.

It separates authorization, execution, and verification responsibilities so inference work can be governed and reviewed.

---

## What Is Publicly Established

The public repository establishes:

- architecture roles and protocol concepts
- permit-scoped execution model
- receipt-style evidence model
- arbitration and divergence handling concepts
- default fail-closed public posture
- public execution modes
- public evidence model
- disclosure boundary
- synthetic proof slice showing expected behavior
- claim-to-evidence classes for public, private, withheld, and planned material
- controlled validation case requirements without publishing private artifacts

---

## What Is Withheld

The following are intentionally outside the public repo:

- live evidence packages
- private proof archives
- private verifier internals
- service definitions
- topology and node identities
- runtime paths
- key material
- deployment commands
- operational timing and audit outputs
- private validation harnesses and raw controlled-review artifacts

Withholding these details is part of the public security posture.

---

## What Is Not Claimed

The public repo does not claim:

- to be a complete deployment manual
- to prove every live runtime detail by itself
- that every lane is hardware-backed
- that all deployments have identical evidence storage
- that multi-lane execution proves universal correctness
- that private evidence has been published
- that every planned hardening item is complete

---

## How Failure Is Handled Publicly

TriTrap's public posture is fail-closed.

Invalid permits, missing evidence, inconsistent evidence, unverifiable receipts, or unresolved lane divergence should not be accepted silently.

The default public arbitration behavior is `reject_on_divergence` unless the permit defines a deterministic policy that resolves the conflict.

---

## What To Review First

Recommended review order:

1. [Claim Boundary](claim_boundary.md)
2. [Claim-to-Evidence Matrix](claim_to_evidence_matrix.md)
3. [Controlled Validation Backbone](controlled_validation_backbone.md)
4. [Limitations](limitations.md)
5. [Threat Model](threat_model.md)
6. [Arbitration Protocol](../protocol/arbitration.md)
7. [Execution Modes](execution_modes.md)
8. [Proof Slice Example](proof_slice_example.md)
9. [Runtime Maturity Matrix](runtime_maturity_matrix.md)
10. [Diligence Bridge](diligence_bridge.md)
11. [Non-Disclosure Boundary](non_disclosure_boundary.md)

---

## Review Questions

A reviewer should be able to answer:

- What does TriTrap claim?
- What does it not claim?
- What is public?
- What is withheld?
- What is staged or planned?
- Which evidence class supports each claim?
- Which validation cases prove refusal rather than acceptance?
- What happens when lanes disagree?
- What happens when evidence is incomplete?
- What risks remain?

If a question requires private operational records, the public repo should identify the boundary rather than expose the records.
