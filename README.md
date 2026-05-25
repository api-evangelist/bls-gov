# Bureau of Labor Statistics (bls-gov)

The U.S. Bureau of Labor Statistics (BLS) is the principal federal statistical agency responsible for measuring labor market activity, working conditions, price changes, and productivity in the U.S. economy. BLS operates the Public Data API at `api.bls.gov`, providing programmatic JSON access to published historical time series across more than 75 surveys — including the Consumer Price Index (CPI), Producer Price Index (PPI), Employment Situation (CES), Local Area Unemployment Statistics (LAUS), Quarterly Census of Employment and Wages (QCEW), Occupational Employment and Wage Statistics (OEWS), Employment Cost Index (ECI), Productivity, Import/Export Price Indexes, and Census of Fatal Occupational Injuries (CFOI).

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/bls-gov/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=government-api-evangelist&utm_content=repo)

## Tags

- Federal Government, Labor Statistics, Economic Data, Consumer Price Index, Producer Price Index, Employment, Unemployment, Wages, Productivity, Open Data, Time Series

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Access Tiers

| Tier | Daily Queries | Series per Request | Years per Query | Calculations | Catalog | Annual Averages |
|---|---|---|---|---|---|---|
| v1 (unregistered) | 25 | 25 | 10 | No | No | No |
| v2 (registered, free) | 500 | 50 | 20 | Yes | Yes | Yes |

Register for a free v2 key at [data.bls.gov/registrationEngine](https://data.bls.gov/registrationEngine/).

## APIs

### BLS Public Data API

The BLS Public Data API is the agency's public REST + JSON service for retrieving published historical time series across every BLS program. All requests return a uniform JSON envelope with `status`, `responseTime`, and `Results.series`, where each series carries data points keyed by `year` and `period` (`M01`–`M12` for monthly, `Q01`–`Q04` for quarterly, `S01`–`S03` for semi-annual, `A01` for annual, `M13` for annual averages).

**Base URL:** `https://api.bls.gov/publicAPI/v2`

- [Documentation — Developers Home](https://www.bls.gov/developers/home.htm)
- [Documentation — API Signature v2](https://www.bls.gov/developers/api_signature_v2.htm)
- [Getting Started — API FAQs](https://www.bls.gov/developers/api_FAQs.htm)
- [Registration](https://data.bls.gov/registrationEngine/)
- [Terms of Service](https://www.bls.gov/developers/termsOfService.htm)
- [Sample Code](https://www.bls.gov/developers/api_sample_code.htm)
- [OpenAPI](openapi/bls-public-data-api-openapi.yml)
- [JSON Schema — Time Series](json-schema/bls-time-series-schema.json)
- [JSON Structure — Time Series](json-structure/bls-time-series-structure.json)
- [JSON-LD Context](json-ld/bls-gov-context.jsonld)
- [Spectral Rules](rules/bls-public-data-api-rules.yml)
- [Naftiko Capability — Time Series](capabilities/bls-public-data-time-series.yaml)
- [Naftiko Capability — Popular Series](capabilities/bls-public-data-popular-series.yaml)
- [Naftiko Capability — Surveys](capabilities/bls-public-data-surveys.yaml)

## Operations

| Method | Path | Operation | Purpose |
|---|---|---|---|
| POST | `/timeseries/data/` | `getMultipleTimeSeries` | Retrieve one or many series with optional calculations, catalog, and annual averages |
| GET | `/timeseries/data/{seriesId}` | `getSingleTimeSeries` | Retrieve a single series (supports `?latest=true`, `?startyear=`, `?endyear=`) |
| GET | `/surveys` | `listSurveys` | List every BLS survey with abbreviation and full name |
| GET | `/surveys/{surveyAbbreviation}` | `getSurveyDetails` | Inspect a single survey including capability flags |
| GET | `/timeseries/popular` | `getPopularSeries` | Top 25 most-requested series (optionally `?survey=` to scope) |

## Key Data Domains

- **Employment & Unemployment** — National, state, metro, and demographic unemployment (CPS/LN series, LAUS)
- **Payroll Employment** — Nonfarm payroll employment and earnings by industry (CES)
- **Consumer Price Index** — CPI-U, CPI-W, Chained CPI inflation measures (CU/CW/SU series)
- **Producer Price Index** — Producer prices by commodity and industry (PC/WP series)
- **Wages & Compensation** — Employment cost index (ECI), employer costs (ECEC), occupational wages (OEWS)
- **Productivity** — Labor productivity and unit labor cost (PR series)
- **Job Openings** — JOLTS series on openings, hires, and separations (JT)
- **Workplace Safety** — Census of Fatal Occupational Injuries (FA/CF) and Survey of Occupational Injuries and Illnesses (CD/CS)
- **Trade Prices** — Import/Export Price Indexes (EI)
- **Employment Projections** — Projected industry and occupational employment (EP)

## Common Series IDs

| Series ID | Description |
|-----------|-------------|
| `LNS14000000` | Unemployment Rate, 16 years and over (Seasonally Adjusted) |
| `LNS11300000` | Labor Force Participation Rate (Seasonally Adjusted) |
| `CES0000000001` | Total Nonfarm Employment (Seasonally Adjusted) |
| `CES0500000003` | Average Hourly Earnings, Private (Seasonally Adjusted) |
| `CUUR0000SA0` | CPI-U All Items (Not Seasonally Adjusted) |
| `CUSR0000SA0L1E` | CPI-U All Items Less Food and Energy (Seasonally Adjusted) |
| `JTS000000000000000JOR` | Job Openings Rate, Total Nonfarm |
| `PRS85006092` | Nonfarm Business Sector Labor Productivity |

## Artifacts

### OpenAPI Specifications

| Spec | Description |
|---|---|
| [bls-public-data-api-openapi.yml](openapi/bls-public-data-api-openapi.yml) | BLS Public Data API v2 — time series, surveys, popular series |

### JSON Schemas

| Schema | Description |
|---|---|
| [bls-time-series-schema.json](json-schema/bls-time-series-schema.json) | Time series payload schema with data points, catalog metadata, and calculations |

### JSON Structures

| Structure | Description |
|---|---|
| [bls-time-series-structure.json](json-structure/bls-time-series-structure.json) | Hierarchical structure documentation for BLS time series API responses |

### JSON-LD Contexts

| Context | Description |
|---|---|
| [bls-gov-context.jsonld](json-ld/bls-gov-context.jsonld) | Linked-data context mapping BLS concepts to schema.org, DCAT, and Dublin Core |

### Examples

| Example | Description |
|---|---|
| [bls-get-unemployment-rate-example.json](examples/bls-get-unemployment-rate-example.json) | POST request retrieving the national unemployment rate with calculations |
| [bls-list-surveys-example.json](examples/bls-list-surveys-example.json) | GET request listing all BLS survey programs |

### Spectral Rules

| Ruleset | Description |
|---|---|
| [bls-public-data-api-rules.yml](rules/bls-public-data-api-rules.yml) | Spectral linting rules enforcing BLS API conventions |

### Naftiko Capabilities

| Capability | Description |
|---|---|
| [bls-public-data-time-series.yaml](capabilities/bls-public-data-time-series.yaml) | Retrieve single- or multi-series BLS time series data |
| [bls-public-data-popular-series.yaml](capabilities/bls-public-data-popular-series.yaml) | Retrieve top-25 most-requested series, optionally scoped to one survey |
| [bls-public-data-surveys.yaml](capabilities/bls-public-data-surveys.yaml) | Discover and inspect BLS surveys |

### Vocabulary

| File | Description |
|---|---|
| [bls-gov-vocabulary.yml](vocabulary/bls-gov-vocabulary.yml) | Domain vocabulary covering BLS surveys, economic indicators, and data terminology |

### Plans

| File | Description |
|---|---|
| [bls-gov-plans-pricing.yml](plans/bls-gov-plans-pricing.yml) | Access tiers documented as API Commons Plans 0.1 (v1 anonymous, v2 registered free) |

### Rate Limits

| File | Description |
|---|---|
| [bls-gov-rate-limits.yml](rate-limits/bls-gov-rate-limits.yml) | Per-IP and per-key daily quotas and request-shape limits |

### FinOps

| File | Description |
|---|---|
| [bls-gov-finops.yml](finops/bls-gov-finops.yml) | FOCUS-aligned cost surface (BLS is no-cost; documented for completeness) |

## Tags

`Federal Government` · `Labor Statistics` · `Economic Data` · `Consumer Price Index` · `Producer Price Index` · `Employment` · `Unemployment` · `Wages` · `Productivity` · `Open Data` · `Time Series`

## Maintainers

**Kin Lane** — [kin@apievangelist.com](mailto:kin@apievangelist.com)
