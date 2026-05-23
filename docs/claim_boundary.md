# Claim Boundary

This document defines what the public TriTrap repository claims, what it does not claim, and what is intentionally withheld.

The goal is confident and constrained public documentation.

---

## Public Claims

TriTrap publicly claims the following architecture and protocol posture:

- governed execution through an authorization role
- separation between Gate, execution lane, and verification responsibilities
- permit-scoped dispatch
- receipt-style evidence concepts
- verification and arbitration concepts
- governed compute commitment concepts
- transaction-bound telemetry concepts
- fail-closed handling for invalid, incomplete, or divergent evidence
- public evidence package model
- public execution modes that trade latency for assurance
- public non-disclosure boundary for private deployment material

These claims are architecture-level, protocol-level, or public maturity claims unless a document explicitly states otherwise.

---

## Public Non-Claims

This repository does not claim:

- to be the sole source of live-runtime proof
- to publish a complete deployment recipe
- that every possible TriTrap embodiment is currently live
- that every lane is hardware-backed
- that every deployment stores receipts in the same way
- that every verification policy has the same assurance level
- that multi-lane execution removes all correctness risk
- that public synthetic examples are private operational evidence
- that private verifier internals are disclosed
- that public documentation publishes private telemetry implementation proof
- that public documentation publishes private accelerator or specialized-compute proof
- that specialized compute output is the default final response in every deployment

These are boundaries, not retreats. They keep the public repo accurate.

---

## WITHHELD vs NOT IMPLEMENTED

**WITHHELD** means a detail is intentionally not public because it belongs in private maintainer records, controlled evidence packages, or internal deployment material.

**NOT IMPLEMENTED** means a capability does not currently exist in the relevant implementation.

The public repository should not blur these terms.

Examples of material that may be **WITHHELD**:

- private evidence packages
- node topology
- runtime paths
- private verifier internals
- service definitions
- operational commands
- key material
- private telemetry artifacts
- specialized-compute receipts or evidence records

Examples of material that should be marked **NOT IMPLEMENTED** only when true:

- a planned feature with no current implementation
- an unsupported arbitration policy
- a deployment mode that has not been built
- an evidence retention behavior that does not exist

If public documentation cannot safely distinguish the two, it should use conservative wording and avoid overclaim.

---

## Evidence Boundary

Public examples may demonstrate protocol shape and verification behavior using synthetic or redacted material.

Private proof packages and live evidence records remain outside the public repo unless intentionally released through a controlled publication process.

The public repo can be reviewable without being directly replicable.

---

## Review Rule

Each public claim should answer:

1. What is being claimed?
2. Is it architecture, protocol, public maturity, or live evidence?
3. Is supporting detail public, withheld, staged, planned, or not implemented?
4. Does the wording preserve the non-disclosure boundary?

If a claim cannot answer those questions, it should be tightened before publication.
