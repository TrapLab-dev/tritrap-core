# Current Runtime Status

TriTrap is a governed edge-runtime architecture for controlled dispatch, lane execution, verification, and fail-closed evidence handling.

This repository documents public architecture, protocol concepts, and runtime posture. It is not the sole source of live-runtime proof and does not publish private deployment mechanics.

---

## Runtime Posture

TriTrap has advanced beyond architecture-only framing into a governed runtime posture with defined roles, evidence discipline, and fail-closed validation behavior.

The public runtime model is composed of:

- Gate role
- execution lane role
- verification lane role
- scoped dispatch
- receipt and event identity discipline
- evidence package generation
- comparative verification
- governed compute commitment concepts
- transaction-bound telemetry concepts
- fail-closed handling for incomplete or invalid evidence

Private node identities, service definitions, network topology, runtime paths, and deployment scripts are intentionally withheld.

---

## Maturity Labels

TriTrap uses conservative status labels for public documentation.

**PROVEN** means behavior has dated evidence or verified maintainer records.

**STAGED** means the workflow or control exists in an approval or deployment path but is not being presented as complete public proof.

**WITHHELD** means details exist privately but are intentionally not published because they would expose deployment mechanics, verifier internals, topology, or evidence package contents.

**PLANNED** means the direction is identified but not represented as completed behavior.

---

## Current Public Maturity Summary

| Area | Public status | Public description |
| --- | --- | --- |
| Gate-controlled dispatch | PROVEN | Workload flow is governed by an authorization point before lane execution. |
| Separated lane roles | PROVEN | Execution and verification roles are separated for comparison and arbitration. |
| Evidence package model | PROVEN | Runtime evidence is captured into bounded proof packages with verification metadata. |
| Hash-chain evidence discipline | PROVEN | Evidence records are validated against ordered integrity expectations. |
| Fail-closed verifier behavior | PROVEN | Missing or inconsistent proof material is rejected rather than accepted silently. |
| Governed compute commitment | STAGED | Public docs describe the concept that expensive or specialized compute should be committed only under explicit authorization. Private implementation evidence is withheld. |
| Transaction-bound telemetry | STAGED | Public docs describe telemetry as evidence that should bind activity to a governed transaction. Private implementation evidence is withheld. |
| Recurring runtime operation | STAGED | Recurring operation is part of the hardening direction, with private operational details withheld. |
| Status and audit visibility | STAGED | Runtime status and audit posture are part of the hardening direction, with private commands withheld. |
| Retention policy | STAGED | Evidence retention is treated as a controlled operational policy, not a public implementation recipe. |
| Hardware-backed lane internals | WITHHELD | The public repo does not disclose lane hardware, topology, or deployment mechanics. |
| Private verifier internals | WITHHELD | The public repo describes verification posture without publishing copyable verifier implementation details. |

---

## Public Claim Boundary

This repository may state that TriTrap defines and exercises governed dispatch, lane execution, verification, and evidence validation concepts.

This repository must not be read as publishing:

- private node names
- private host addresses
- service unit internals
- operational scripts
- proof package contents
- private verifier internals
- runtime filesystem paths
- cryptographic material
- deployment mechanics

TriTrap's public posture is maturity without replicability.
