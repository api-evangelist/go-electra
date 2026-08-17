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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Electra is a European operator of ultra-fast electric-vehicle charging, headquartered in Paris and
led by co-founder and CEO Aurelien de Meaux. It designs, finances, installs and operates its own DC
fast-charging stations — 770+ live with 68 more building, up to 400 kW — across France, Belgium,
Spain, Italy, Germany, Austria, the Netherlands and Switzerland, with a stated target of 2,200
stations / 15,000 charge points in Europe by 2030.

**API surface.** Electra publishes no developer portal, no API documentation, no OpenAPI, no
GraphQL, no MCP server and no A2A agent card — all probed and missed on 2026-08-17. It does run one
real machine-readable API: an Open Charge Point Interface (OCPI) implementation in the Charge Point
Operator role at `https://ocpi.go-electra.com/ocpi/cpo`, serving OCPI 2.1.1 and 2.2.1 concurrently.
Version negotiation answers anonymously with HTTP 200 and enumerates all seven modules (cdrs,
commands, credentials, locations, sessions, tariffs, tokens) with SENDER/RECEIVER roles on 2.2.1;
every data module returns HTTP 401 with `WWW-Authenticate: Token realm="Application"`, OCPI's own
bilateral token scheme. Access follows a commercial roaming agreement — there is no signup, no
sandbox and no self-service credential.

Sector: climate-tech.

Source: portfolio company of [serena](https://github.com/api-evangelist/serena) — https://www.go-electra.com/
