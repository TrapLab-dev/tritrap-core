# Non-Disclosure Boundary

This repository publishes the TriTrap architecture, protocol concepts, public verification posture, and maturity framing.

It does not publish the private operational material required to reproduce a live deployment.

---

## Public Repository Scope

The public repository may contain:

- architecture diagrams
- protocol descriptions
- role definitions
- permit concepts
- receipt concepts
- verification concepts
- arbitration concepts
- public evidence model
- public maturity labels
- fail-closed behavior
- operator authority principles

The public repository is intended to communicate what TriTrap is and why the model matters without exposing the private deployment pattern.

---

## Private Operational Scope

The following material is intentionally withheld:

- exact node names
- LAN addresses
- host topology
- service scripts
- system service definitions
- runtime paths
- private verifier internals
- raw proof tarballs
- raw evidence hashes unless explicitly published
- key material
- deployment commands
- retention implementation details
- private audit commands
- operational timing details

These items belong in private operator records, controlled evidence packages, or internal deployment repositories.

---

## Claim Discipline

Public documentation should use disciplined language.

Use:

- architecture defines
- protocol describes
- runtime posture includes
- evidence model supports
- verifier contract rejects
- current public status is

Avoid:

- publishing private deployment instructions
- implying that public docs are the sole live proof source
- claiming every possible embodiment is currently live
- exposing node topology or runtime paths
- releasing proof package internals by default

---

## Status Labels

Public docs should use conservative status labels:

- **PROVEN** for behavior backed by dated evidence or verified operator records
- **STAGED** for controlled workflows not being represented as complete public proof
- **WITHHELD** for real but private operational details
- **PLANNED** for known future hardening direction

These labels prevent overclaiming while still showing maturity.

---

## Public Position

TriTrap is a governed edge-runtime architecture for controlled dispatch, lane execution, verification, and fail-closed evidence handling.

The public repository shows the architecture, protocol posture, and maturity model.

The private system records hold deployment mechanics and dated proof.

