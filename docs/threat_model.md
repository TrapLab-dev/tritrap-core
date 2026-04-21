# Threat Model

This document summarizes public threat considerations for TriTrap.

It describes classes of risk and expected posture without publishing private deployment mechanics, verifier internals, topology, keys, paths, or operational commands.

---

## Scope

The public threat model covers:

- permit misuse or forgery attempts
- malicious or faulty lanes
- compromised coordination roles
- replayed or stale execution material
- incomplete or tampered evidence
- verifier bypass attempts
- weak arbitration policy
- disclosure boundary failures

The public repo does not disclose private mitigations that would make a deployment easier to attack or reproduce.

---

## Threat Summary

| Threat | Public posture | Status |
| --- | --- | --- |
| Forged permit | Permit validation is a required control. Invalid authority should fail closed. | Mitigated by design, deployment-dependent. |
| Replay attempt | Permit scope, validity, and evidence identity should prevent stale material from being accepted silently. | Mitigated/detected by design, deployment-dependent. |
| Malicious lane | Comparative verification and arbitration can detect divergence or invalid receipts. | Detected where policies and evidence are sufficient. |
| Faulty lane | Divergent or invalid lane output should trigger rejection unless an explicit policy resolves it. | Detected where comparative verification is used. |
| Compromised Gate | A compromised authorization role is high impact and must be treated as a serious operational risk. | Not fully mitigated by public protocol alone. |
| Partial evidence submission | Missing required proof material should fail closed. | Mitigated by verifier contract. |
| Evidence tampering | Integrity and ordering checks should detect inconsistent evidence. | Detected where evidence model is implemented. |
| Verifier bypass | Verification must not be treated as optional in governed modes. | Deployment-dependent control. |
| Weak arbitration policy | Weak policy can produce weak assurance even if receipts exist. | Mitigated by explicit policy discipline. |
| Disclosure leakage | Public documentation can accidentally expose private deployment mechanics. | Mitigated by non-disclosure boundary and audit checklist. |

---

## Fail-Closed Expectations

The safest public default is rejection when required authority, identity, integrity, completeness, or lane agreement cannot be verified.

This is especially important for:

- forged or invalid permits
- stale or replayed material
- missing evidence
- broken evidence continuity
- lane divergence without an explicit policy
- verifier uncertainty

---

## Not Fully Solved by Architecture Alone

TriTrap does not claim that architecture alone solves:

- compromised deployment environments
- compromised key material
- identical model failures across multiple lanes
- flawed verification policy design
- every supply-chain dependency risk
- all denial-of-service conditions
- all deployment misconfigurations

These require operational controls outside the public protocol description.

---

## Review Guidance

A reviewer should ask:

1. What authority permits execution?
2. What evidence proves the authorized path?
3. What happens when evidence is incomplete?
4. What happens when lanes disagree?
5. What is public, withheld, staged, planned, or not implemented?

If an answer depends on private deployment details, the public repo should say so rather than expose those details.