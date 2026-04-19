# Public Audit Checklist

This checklist helps review TriTrap public documentation before publication.

The goal is to show maturity and credibility without publishing material that would make a private deployment directly replicable.

---

## Public Claim Boundary

Public documents should make clear that TriTrap is a governed execution architecture with controlled dispatch, independent lane roles, verification, and fail-closed evidence handling.

Public documents should not claim that this repository is the sole proof source for a live deployment.

Pass criteria:

- public claims are architecture-level or protocol-level unless clearly marked otherwise
- runtime posture is described without private deployment mechanics
- evidence concepts are described without private proof contents
- live proof remains tied to private operator records or controlled evidence packages

---

## Status Label Review

Use conservative status labels.

- **PROVEN** means behavior is backed by dated evidence or verified operator records
- **STAGED** means the workflow exists in a controlled path but is not presented as public proof
- **WITHHELD** means the detail exists privately but is intentionally not published
- **PLANNED** means the direction is identified but not represented as complete

Fail a document if it uses broad certainty or marketing language that exceeds the evidence boundary.

---

## Replicability Review

A public reader should be able to understand:

- what TriTrap does
- why governance matters
- how the roles relate
- what fail-closed evidence means
- how public maturity is described

A public reader should not receive enough information to recreate:

- private deployment topology
- private runtime operation
- private evidence archive layout
- private verifier internals
- private operational schedule
- private audit commands

---

## Evidence Language Review

Preferred language:

- evidence packages support verification
- invalid or incomplete evidence fails closed
- runtime evidence is captured into bounded proof artifacts
- private evidence archives are withheld

Avoid language that publishes raw proof material, private paths, command recipes, operational timing, key material, or service internals.

---

## Protocol Language Review

Protocol documents should preserve architecture coverage while avoiding overclaim.

Good qualifiers include:

- architecture-level contract
- deployment may vary
- where implemented
- public posture
- not the sole proof source

Review any wording that implies every deployment has the same storage behavior, hardware behavior, verifier implementation, or archival behavior.

---

## Final Review Question

Before publishing, ask:

Would this help a serious reviewer understand the system while still preventing direct reconstruction of the private implementation?

If not, tighten the disclosure boundary before publication.
