# Brand and Domain Boundary

This document defines public domain and brand routing for TriTrap-related surfaces.

It does not define private infrastructure, DNS configuration, or deployment endpoints.

---

## Domain Roles

`traplab.dev` is the technical, project, reviewer, and lab-facing public surface.

Appropriate uses include:

- public project information
- reviewer orientation
- public-safe technical summaries
- controlled diligence routing
- public demo surfaces when intentionally approved

`mntdintel.com` is the outward business, brand, and operations identity surface.

Appropriate uses include:

- business identity
- partner outreach
- contact routing
- public-facing commercial positioning
- non-runtime organizational material

---

## Private Infrastructure Boundary

Private infrastructure endpoints are not public product endpoints.

The public repository should not document private service names, hostnames, local dashboards, local DNS records, runtime ports, private network layout, operator tools, or infrastructure access patterns.

If a public demo or reviewer endpoint is created later, it should be documented as a deliberately approved public surface, not as a leak from private infrastructure.

---

## Repository Rule

Public docs may refer to `traplab.dev` and `mntdintel.com` as routing concepts.

Public docs must not publish private DNS plans, private subdomain layouts, infrastructure configuration, tunnel configuration, or endpoint credentials.
