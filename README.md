# Levelpath

Levelpath is an AI-native procurement platform that unifies intake and orchestration, strategic sourcing, contract lifecycle management, supplier management, third-party risk management, invoice automation, and category pipeline reporting into a single enterprise system. The product is built around AI agents that run sourcing events and generate RFPs, scan contract repositories to answer questions and flag risk, monitor supplier compliance signals, and process invoices.

Backed by Battery Ventures, Menlo Ventures, and Redpoint Ventures — https://www.levelpath.com

## API posture

Levelpath is a **closed enterprise platform with no public developer program**. As of the 2026-07-19 enrichment pass:

- No developer portal, API reference, getting-started guide, OpenAPI/Swagger definition, GraphQL schema, or AsyncAPI document is published.
- No first-party SDKs or CLI on npm, PyPI, or any other public registry.
- No public pricing, changelog, roadmap, or webhook documentation.
- No `/.well-known/` discovery documents. `app.levelpath.com` is an SPA that returns its `index.html` with HTTP 200 for every unmatched path, so `/.well-known/*` there are soft-404s, not documents.
- No `security.txt`, responsible-disclosure page, or bug bounty program.
- `api.levelpath.com` resolves but returns HTTP 403 — an API surface exists, gated.
- The Atlassian Statuspage lists a dedicated **APIs** component, confirming a production API behind the customer login.

Integrations (SAP, Ariba, Coupa, Oracle, NetSuite, Docusign, Ironclad, OneTrust, Slack, Microsoft Teams) are delivered through the platform rather than a documented public API.

## Artifacts

| Artifact | Method | Notes |
|---|---|---|
| `llms/levelpath-llms.txt` | searched | Real `llms.txt` published at `levelpath.com/llms.txt`, saved verbatim |
| `lifecycle/levelpath-lifecycle.yml` | searched | Atlassian Statuspage + 9 components, incl. an APIs component |
| `conformance/levelpath-conformance.yml` | searched | SOC 2 Type II, AES-256 at rest; API-level standards unverifiable |
| `security/levelpath-trust-center.yml` | searched | Vanta-hosted trust center, SOC 2 Type II, Zero Data Retention for AI |
| `security/levelpath-domain-security.yml` | probed | TLS 1.3, no HSTS, no DNSSEC, no CAA, SPF + DMARC (p=quarantine) |
| `well-known/levelpath-well-known.yml` | searched | Negative result — no discovery documents published |
