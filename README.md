# Bureau of Labor Statistics (bls-gov)

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

The U.S. Bureau of Labor Statistics (BLS) is the principal federal statistical agency responsible for measuring labor market activity, working conditions, price changes, and productivity in the U.S. economy. BLS operates the Public Data API at api.bls.gov, providing programmatic JSON access to published historical time series across more than 75 surveys — including the Consumer Price Index (CPI), Producer Price Index (PPI), Employment Situation (CES), Local Area Unemployment Statistics (LAUS), Quarterly Census of Employment and Wages (QCEW), Occupational Employment and Wage Statistics (OEWS), Employment Cost Index (ECI), Productivity, Import/Export Price Indexes, and Census of Fatal Occupational Injuries (CFOI). Version 1 is open without registration; Version 2 requires a free registration key and provides higher daily limits, more series per request, longer year ranges, catalog metadata, statistical calculations, and annual averages.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bls-gov/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bls-gov/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Federal Government
- Labor Statistics
- Economic Data
- Consumer Price Index
- Producer Price Index
- Employment
- Unemployment
- Wages
- Productivity
- Open Data
- Time Series

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### BLS Public Data API

The BLS Public Data API is the agency's public REST + JSON service for retrieving published historical time series across every BLS program. v1 is open and unauthenticated with smaller daily limits and per-request caps; v2 requires a free registration key and unlocks 500 queries per day, up to 50 series per request, up to 20 years per query, optional catalog metadata, net/percent-change calculations, and annual averages. All requests return a uniform JSON envelope with status, responseTime, and Results.series, where each series carries data points keyed by year and period (M01–M12 for monthly, Q01–Q04 for quarterly, S01–S03 for semi annual, A01 for annual, M13 for annual averages).

- **Human URL:** [https://www.bls.gov/developers/home.htm](https://www.bls.gov/developers/home.htm)
- **Base URL:** `https://api.bls.gov/publicAPI/v2`

#### Tags

- Labor Statistics
- Employment
- Unemployment
- Consumer Price Index
- Producer Price Index
- Economic Data
- Time Series
- Open Data

#### Properties

- [Documentation](https://www.bls.gov/developers/home.htm)
- [Documentation](https://www.bls.gov/developers/api_signature_v2.htm)
- [Getting Started](https://www.bls.gov/developers/api_FAQs.htm)
- [Registration](https://data.bls.gov/registrationEngine/)
- [Terms of Service](https://www.bls.gov/developers/termsOfService.htm)
- [Signature Examples](https://www.bls.gov/developers/api_sample_code.htm)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/bls-gov/refs/heads/main/openapi/bls-public-data-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/bls-gov/refs/heads/main/json-schema/bls-time-series-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](https://raw.githubusercontent.com/api-evangelist/bls-gov/refs/heads/main/json-structure/bls-time-series-structure.json)
- [JSON-LD](https://raw.githubusercontent.com/api-evangelist/bls-gov/refs/heads/main/json-ld/bls-gov-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Ruleset](https://raw.githubusercontent.com/api-evangelist/bls-gov/refs/heads/main/rules/bls-public-data-api-rules.yml)
- [Data A P I](https://api.bls.gov/publicAPI/v2/timeseries/data/)
- [Data A P I](https://api.bls.gov/publicAPI/v2/surveys)
- [Data A P I](https://api.bls.gov/publicAPI/v2/timeseries/popular)
- [Rate Limits](rate-limits/bls-gov-rate-limits.yml)
- [Plans](plans/bls-gov-plans-pricing.yml)
- [Fin Ops](finops/bls-gov-finops.yml)
- [Examples](examples/bls-get-unemployment-rate-example.json)
- [Examples](examples/bls-list-surveys-example.json)
- [Vocabulary](vocabulary/bls-gov-vocabulary.yml)
- [Postman Collection](collections/bls-public-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bls-public-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.bls.gov/)
- [Developer](https://www.bls.gov/developers/)
- [Documentation](https://www.bls.gov/developers/home.htm)
- [Registration](https://data.bls.gov/registrationEngine/)
- [Terms of Service](https://www.bls.gov/developers/termsOfService.htm)
- [Contact Us](https://www.bls.gov/contact/)
- [LinkedIn](https://www.linkedin.com/company/bureau-of-labor-statistics)
- [Twitter](https://twitter.com/BLS_gov)
- [Facebook](https://www.facebook.com/BLSgov)
- [YouTube](https://www.youtube.com/user/blsgov)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
