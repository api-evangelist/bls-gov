# Bureau of Labor Statistics (bls-gov)

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
