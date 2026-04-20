# Diligence Bridge

This document defines how TriTrap can support controlled review without turning the public repository into a deployment manual or proof archive.

The public repo is the front door. Controlled diligence is the review room.

---

## Purpose

The diligence bridge exists to avoid two bad outcomes:

- publishing private operational material
- asking qualified reviewers to rely only on public prose

It creates a third state:

```text
reviewable under control
```

---

## Access Classes

| Access class | Description | Material type |
| --- | --- | --- |
| Public | Safe for repository publication. | Architecture, protocol concepts, synthetic examples, claim boundaries. |
| Controlled review | Available only under appropriate review conditions. | Redacted proof summaries, bounded validation results, selected maintainer records. |
| Maintainer-only | Not provided through public review. | Raw proof archives, runtime paths, keys, verifier internals, topology, service definitions, operational commands. |

---

## Review Package Shape

A controlled diligence package may include:

- claim-to-evidence mapping
- accepted-run summary
- rejected-run summary
- divergence rejection summary
- incomplete-evidence rejection summary
- stale or replay rejection summary
- execution-mode comparison summary
- residual-risk notes

The package should label each item by evidence class and disclosure boundary.

---

## What Reviewers Can Ask

Qualified reviewers may ask:

- Which claims are public architecture only?
- Which claims have synthetic examples?
- Which claims have controlled private evidence?
- Which claims are not made?
- Which validation cases demonstrate refusal?
- Which failure domains are separated?
- Which risks remain deployment-dependent?

The public repo should route these questions to the correct evidence class without publishing private mechanics.

---

## What Is Not Provided Publicly

The diligence bridge does not publish:

- raw proof packages
- raw hashes unless intentionally released
- private paths
- node identities
- service definitions
- operational commands
- keys or secrets
- private verifier source
- deployment runbooks

---

## Review Standard

The correct standard is controlled confidence, not public reproducibility.

A reviewer should be able to understand the architecture publicly and evaluate stronger evidence through controlled review without receiving the keys to reproduce the private runtime.
