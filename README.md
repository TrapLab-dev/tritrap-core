# TriTrap
TriTrap is a governed execution architecture for deterministic artificial intelligence inference workloads.
This repository is the invention/protocol/public architecture layer for TriTrap.
It is not the sole proof source for the current canonical live runtime, which must be grounded in canonical node docs, live service/source records, and dated execution evidence outside this repository.
The framework introduces mechanisms for:

• permit-based execution authorization  
• controlled inference environments  
• multi-lane execution validation  
• deterministic verification of computation outcomes

---

## Architecture

<img width="1024" height="1536" alt="FIG1_architecture" src="https://github.com/user-attachments/assets/c80c29a5-c214-40ff-ab7a-b54efdfeee55" /> 
FIG.1 illustrates the high-level execution model of the TriTrap architecture, where a Gate node authorizes and dispatches workloads to independent execution lanes whose outputs are validated through a verification layer.

---
## Design Principles
TriTrap is built around several architectural principles:

• **Deny-by-default execution** — workloads require explicit authorization before execution.

• **Lane independence** — execution lanes operate independently to allow comparative validation.

• **Deterministic verification** — outputs are validated through reproducible verification mechanisms.

• **Separation of authorization and execution** — Gate nodes authorize workloads but do not perform inference.

---
## Core Concepts

TriTrap introduces a model where inference execution must be explicitly authorized and verified.

The system is built around four primary roles:

• Gate  
• Execution Lanes  
• Permit System  
• Verification Layer

---

## Public Runtime Posture

TriTrap's public repository documents architecture, protocol concepts, and runtime maturity posture without publishing private deployment mechanics.

Current public runtime documentation:

- [Current Runtime Status](docs/current_runtime_status.md) - public maturity labels and runtime posture
- [Evidence Model](docs/evidence_model.md) - proof package concepts, hash-chain evidence, and fail-closed validation
- [Non-Disclosure Boundary](docs/non_disclosure_boundary.md) - what the public repo may disclose and what remains private
- [Runtime Maturity Matrix](docs/runtime_maturity_matrix.md) - public-safe maturity summary
- [Public Audit Checklist](docs/public_audit_checklist.md) - publication review checklist
- [Security Policy](SECURITY.md) - responsible disclosure and repository scope

---

## Execution Model

1. Request arrives
2. Permit validated
3. Gate dispatches workload
4. Execution lanes perform inference
5. Receipts generated
6. Verification / arbitration

---
## Repository Structure

```
tritrap-core/
│
├─ architecture/
│  ├─ gate.md
│  └─ system_model.md
│
├─ protocol/
│  ├─ permit.md
│  ├─ receipt.md
│  ├─ gate_protocol.md
│  ├─ lane_execution.md
│  └─ arbitration.md
│
├─ docs/
│  ├─ overview.md
│  ├─ terminology.md
│  ├─ current_runtime_status.md
│  ├─ evidence_model.md
│  ├─ non_disclosure_boundary.md
│  ├─ runtime_maturity_matrix.md
│  └─ public_audit_checklist.md
│
├─ figures/
│  ├─ FIG1_architecture.png
│  ├─ FIG2_permit_structure.png
│  ├─ FIG3_operational_flow.png
│  ├─ FIG4_multilane_execution.png
│  └─ FIG5_receipt_verification.png
│
├─ SECURITY.md
└─ README.md
```

## Status

Invention/protocol architecture repository.
