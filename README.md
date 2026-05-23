# TriTrap
TriTrap is a governed execution architecture for controlled artificial intelligence inference workloads.
This repository is the invention/protocol/public architecture layer for TriTrap.
It is not the sole proof source for the current canonical live runtime, which must be grounded in canonical node docs, live service/source records, and dated execution evidence outside this repository.
The framework introduces mechanisms for:

• permit-based execution authorization
• controlled inference environments
• multi-lane execution validation
• policy-defined verification of computation outcomes
• governed compute commitment
• transaction-bound telemetry concepts

---

## Architecture

<img width="1024" height="1536" alt="FIG1_architecture" src="figures/FIG1_architecture.png" />
FIG.1 illustrates the high-level execution model of the TriTrap architecture, where a Gate node authorizes and dispatches workloads to separate execution lanes whose outputs are validated through a verification layer.

---
## Design Principles
TriTrap is built around several architectural principles:

• **Deny-by-default execution** — workloads require explicit authorization before execution.

• **Lane separation** — execution lanes operate as separate execution domains to allow comparative validation.

• **Policy-defined verification** — outputs are validated through reproducible verification mechanisms.

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

- [Documentation Index](docs/README.md) - reviewer navigation
- [Current Runtime Status](docs/current_runtime_status.md) - public maturity labels and runtime posture
- [Evidence Model](docs/evidence_model.md) - proof package concepts, hash-chain evidence, and fail-closed validation
- [Non-Disclosure Boundary](docs/non_disclosure_boundary.md) - what the public repo may disclose and what remains private
- [Runtime Maturity Matrix](docs/runtime_maturity_matrix.md) - public-safe maturity summary
- [Public Audit Checklist](docs/public_audit_checklist.md) - publication review checklist
- [Execution Modes](docs/execution_modes.md) - latency, assurance, and evidence tradeoffs
- [Controlled Validation Backbone](docs/controlled_validation_backbone.md) - public-safe validation cases and evidence classes
- [Proof Slice Example](docs/proof_slice_example.md) - synthetic governed-run example
- [Claim Boundary](docs/claim_boundary.md) - public claims, non-claims, and withheld material
- [Claim-to-Evidence Matrix](docs/claim_to_evidence_matrix.md) - mapping claims to evidence classes
- [Limitations](docs/limitations.md) - known limits and failure conditions
- [Threat Model](docs/threat_model.md) - public threat posture
- [Technical Due Diligence](docs/technical_due_diligence.md) - reviewer shortcut
- [Diligence Bridge](docs/diligence_bridge.md) - controlled review without public replication
- [One Page Brief](docs/one_page_brief.md) - fast, public-safe summary
- [Contact and Review](docs/contact_and_review.md) - reviewer and partner routing
- [Public Roadmap](docs/public_roadmap.md) - public-safe documentation direction
- [Brand and Domain Boundary](docs/brand_and_domain_boundary.md) - domain and brand routing
- [Use Cases](docs/use_cases.md) - grounded application areas
- [Partner Overview](docs/partner_overview.md) - integration and evaluation framing
- [Design Philosophy](docs/design_philosophy.md) - sober engineering principles
- [Security Policy](SECURITY.md) - responsible disclosure and repository scope
- [Notice](NOTICE.md) - review-only / all-rights-reserved posture unless separately licensed

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
│  ├─ README.md
│  ├─ overview.md
│  ├─ terminology.md
│  ├─ current_runtime_status.md
│  ├─ evidence_model.md
│  ├─ non_disclosure_boundary.md
│  ├─ runtime_maturity_matrix.md
│  ├─ public_audit_checklist.md
│  ├─ execution_modes.md
│  ├─ controlled_validation_backbone.md
│  ├─ proof_slice_example.md
│  ├─ claim_boundary.md
│  ├─ claim_to_evidence_matrix.md
│  ├─ limitations.md
│  ├─ threat_model.md
│  ├─ technical_due_diligence.md
│  ├─ diligence_bridge.md
│  ├─ one_page_brief.md
│  ├─ contact_and_review.md
│  ├─ public_roadmap.md
│  ├─ brand_and_domain_boundary.md
│  ├─ use_cases.md
│  ├─ partner_overview.md
│  └─ design_philosophy.md
│
├─ .github/
│  ├─ ISSUE_TEMPLATE/
│  └─ PULL_REQUEST_TEMPLATE.md
│
├─ figures/
│  ├─ FIG1_architecture.png
│  ├─ FIG2_permit_structure.png
│  ├─ FIG3_operational_flow.png
│  ├─ FIG4_multilane_execution.png
│  └─ FIG5_receipt_verification.png
│
├─ NOTICE.md
├─ SECURITY.md
└─ README.md
```

## Status

Invention/protocol architecture repository.
