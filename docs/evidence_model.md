# Evidence Model

TriTrap treats runtime evidence as a governed output of execution, not as an informal log stream.

The public evidence model is designed to support verification, auditability, and fail-closed handling while keeping private operational mechanics out of the public repository.

---

## Evidence Goals

TriTrap evidence is intended to demonstrate:

- an authorized execution path existed
- role identity was preserved across the flow
- runtime events were captured in an ordered structure
- proof material can be checked for completeness
- tampering or omission can be detected
- invalid or incomplete evidence fails closed

This repository describes the evidence posture. It does not publish private proof archives or deployment-specific evidence paths.

---

## Public Evidence Concepts

TriTrap evidence packages may include these public concepts:

- summary verdict
- manifest records
- event records
- role-scoped execution records
- integrity hashes
- hash-chain validation
- verifier result
- package boundary

The exact private layout, file names, paths, hashes, command names, service names, and verifier implementation details are withheld.

---

## Verification Contract

A public-safe TriTrap evidence verifier should reject proof material when:

- a required summary is missing
- declared integrity values do not match observed content
- event ordering or hash-chain continuity is broken
- package sealing does not match the expected terminal event
- required role evidence is missing
- proof material is incomplete

This is the important public claim: invalid evidence is not accepted silently.

---

## Fail-Closed Principle

TriTrap evidence handling follows a fail-closed principle.

If authority, identity, ordering, integrity, or completeness cannot be verified, the evidence is treated as invalid.

The public repo may describe this principle. It should not publish enough implementation detail to allow a third party to clone the private verifier or deployment.

---

## Public Evidence Boundary

Safe public disclosures:

- evidence packages exist as bounded proof artifacts
- proof material is checked against a verifier contract
- hash-chain style integrity is used as a public concept
- missing or mismatched evidence fails closed

Withheld private details:

- raw proof packages
- raw evidence hashes unless intentionally released
- private paths
- private scripts
- service definitions
- key material
- node addresses
- verifier source internals
- retention mechanics
