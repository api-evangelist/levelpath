# Levelpath

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
