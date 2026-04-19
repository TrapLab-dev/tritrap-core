# Documentation Index

This index gives reviewers a clean path through the TriTrap public repository.

The public repo is intended to be reviewable without exposing private deployment mechanics, live proof archives, verifier internals, topology, keys, paths, or operational commands.

---

## Start Here

- [Overview](overview.md) - architecture overview and figure walkthrough
- [One Page Brief](one_page_brief.md) - fast public-safe summary
- [Problem Statement](problem_statement.md) - original problem framing
- [Terminology](terminology.md) - shared vocabulary

---

## Architecture

- [Gate](../architecture/gate.md) - Gate role and responsibilities
- [System Model](../architecture/system_model.md) - role model and execution flow

---

## Protocol

- [Protocol README](../protocol/README.md) - protocol layer summary
- [Gate Protocol](../protocol/gate_protocol.md) - request authorization and routing
- [Permit Protocol](../protocol/permit.md) - permit structure and validation
- [Lane Execution](../protocol/lane_execution.md) - lane responsibilities
- [Receipt Protocol](../protocol/receipt.md) - receipt contract
- [Arbitration](../protocol/arbitration.md) - agreement, divergence, and fail-closed defaults

---

## Runtime Posture

- [Current Runtime Status](current_runtime_status.md) - public maturity labels and runtime posture
- [Evidence Model](evidence_model.md) - evidence package concepts and fail-closed validation
- [Execution Modes](execution_modes.md) - speed, assurance, and audit tradeoffs
- [Proof Slice Example](proof_slice_example.md) - synthetic governed-run example
- [Runtime Maturity Matrix](runtime_maturity_matrix.md) - public-safe maturity summary

---

## Trust and Defensibility

- [Non-Disclosure Boundary](non_disclosure_boundary.md) - public/private disclosure split
- [Public Audit Checklist](public_audit_checklist.md) - publication review checklist
- [Claim Boundary](claim_boundary.md) - claims, non-claims, withheld, and not implemented
- [Limitations](limitations.md) - known limits and failure modes
- [Threat Model](threat_model.md) - public threat posture
- [Technical Due Diligence](technical_due_diligence.md) - reviewer shortcut
- [Security Policy](../SECURITY.md) - responsible disclosure and repository scope

---

## Pitch and Partner Context

- [Use Cases](use_cases.md) - grounded application areas
- [Partner Overview](partner_overview.md) - integration and evaluation framing
- [Design Philosophy](design_philosophy.md) - engineering principles
