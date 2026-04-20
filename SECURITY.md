# Security Policy

TriTrap publishes architecture, protocol concepts, and public runtime posture.

This repository does not publish private deployment mechanics, live evidence archives, runtime paths, keys, service definitions, verifier internals, or node topology.

---

## Reporting Security Concerns

Report concerns that affect the public architecture, protocol descriptions, repository contents, or disclosure boundary.

Useful reports include:

- unclear public/private boundaries
- protocol wording that appears to overclaim live implementation behavior
- documentation that could enable unintended replication
- repository content that appears to expose private operational details
- inconsistencies in public maturity labels

Do not submit requests for private proof material, deployment scripts, internal verifier source, keys, live topology, node addresses, or operational commands.

---

## Public Scope

The public security posture covers:

- permit-governed execution concepts
- Gate and lane role separation
- verification and arbitration concepts
- fail-closed evidence handling
- public evidence model
- public maturity labels
- non-disclosure boundaries

The public repository is intended to be reviewable without being directly replicable.

---

## Private Operational Scope

Private operational material remains outside this repository.

That includes live deployment records, private evidence packages, runtime scripts, service definitions, local verifier internals, topology, key material, and maintainer-only audit records.

The absence of those materials from this repository is intentional.

---

## Claim Discipline

Security review should preserve the distinction between:

- architecture and protocol concepts
- public runtime posture
- private operational evidence
- deployment-specific implementation details

If a public document blurs those boundaries, treat it as a documentation issue.
