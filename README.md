# Electra

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Electra is a European operator of ultra-fast electric-vehicle charging, headquartered at 104 rue de Richelieu in the 2nd arrondissement of Paris and led by co-founder and CEO Aurelien de Meaux. It designs, finances, installs and operates its own DC fast-charging stations rather than reselling someone else's hardware, advertising 770+ live stations with 68 more under construction, charge rates up to 400 kW, and a target of 2,200 stations / 15,000 charge points across Europe by 2030. Its own pricing and station pages cover France, Belgium, Spain, Italy, Germany, Austria, the Netherlands and Switzerland, with city hubs in Paris, Lyon, Marseille, Brussels, Antwerp, Liege, Milan, Bologna, Turin, Madrid, Barcelona and Zurich. The commercial surface is consumer- and fleet-facing: a mobile app, an Electra+ subscription that cuts up to 0.20 EUR/kWh, an RFID charging card, Autocharge and Plug&Charge, and a fleet dashboard at business.go-electra.com. It is a Serena portfolio company and has raised a 160 MEUR round, a 304 MEUR Series B and a 433 MEUR debt facility. Electra publishes NO developer portal, NO API documentation, NO OpenAPI, NO llms.txt, NO MCP server and NO A2A agent card — every one of those was probed and missed on 2026-08-17. What it does run, and what almost nobody looking at the marketing site would find, is a real machine-readable API: a live Open Charge Point Interface implementation in the Charge Point Operator role at https://ocpi.go-electra.com/ocpi/cpo, serving BOTH OCPI 2.1.1 and OCPI 2.2.1 concurrently. Its version-negotiation endpoints answer anonymously with HTTP 200 and enumerate the full module inventory — cdrs, commands, credentials, locations, sessions, tariffs and tokens, with SENDER/RECEIVER roles declared on the 2.2.1 surface — while every data module itself returns HTTP 401 with `WWW-Authenticate: Token realm="Application"`, OCPI's own bilateral token scheme. That is a documented open industry standard, fully implemented, discoverable without credentials and readable only with a roaming agreement; its production use is evidenced by the 180+ e-mobility service provider cards Electra's own help centre lists as accepted at its chargers.

**Areas:** Company · Climate Tech · EV Charging · Energy · Mobility · OCPI · Roaming · Charge Point Operator · Electric Vehicles · Fast Charging · Charging Sessions · Tariffs

## Electra on APIs.io

Everything profiled for Electra is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/go-electra/](https://apis.io/providers/go-electra/)** — or go straight to one of the APIs or properties below.

### APIs (1)

- [Electra OCPI CPO API](https://apis.io/apis/go-electra/go-electra-ocpi-cpo-api/) — Electra's Open Charge Point Interface implementation in the Charge Point Operator role — the roaming interface an e-mobility service provider calls to read…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [go-electra](https://apis.io/servers/go-electra/go-electra/)

#### Examples (3)

Example requests and responses.

- [Go Electra Ocpi Cpo 2.1.1 Endpoints](https://apis.io/examples/go-electra/go-electra-ocpi-cpo-2.1.1-endpoints/)
- [Go Electra Ocpi Cpo 2.2.1 Endpoints](https://apis.io/examples/go-electra/go-electra-ocpi-cpo-2.2.1-endpoints/)
- [Go Electra Ocpi Cpo Versions](https://apis.io/examples/go-electra/go-electra-ocpi-cpo-versions/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Go Electra Authentication](https://apis.io/security/go-electra/go-electra-authentication/)
- [Go Electra Domain Security](https://apis.io/security/go-electra/go-electra-domain-security/)
- [Go Electra Trust Center](https://apis.io/security/go-electra/go-electra-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Go Electra Plans Pricing](https://apis.io/plans/go-electra/go-electra-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Go Electra Rate Limits](https://apis.io/rate-limits/go-electra/go-electra-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.go-electra.com/)
- [Pricing](https://www.go-electra.com/en/price/)
- [Sign up](https://business.go-electra.com/register)
- [Support](https://intercom.help/go-electra/en/)
- [Blog](https://www.go-electra.com/en/newsroom/all-categories/)
- [Trust centre](https://trust.go-electra.com/)
- [Terms of service](https://www.go-electra.com/en/tos/)
- [Privacy policy](https://www.go-electra.com/en/privacy/)

## API Evangelist rating

**Kin Score 31.4** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 6.5 |
| Contract governance | 18.2 |
| Operational transparency | 0.0 |
| Developer ergonomics | 19.0 |
| Access clarity | 77.6 |

**Agent readiness 9.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 24.6** — Energy & Utilities

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/go-electra/](https://apis.io/providers/go-electra/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Electra: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/go-electra/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
