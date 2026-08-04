# World Air Quality Index (WAQI)

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

World Air Quality Index REST API providing real-time air quality data, AQI readings, pollutant measurements, and station data for 12,000+ monitoring stations worldwide.

**Website:** https://waqi.info/ | https://aqicn.org/

**API Documentation:** https://aqicn.org/json-api/doc/

**API Base URL:** https://api.waqi.info

**GitHub:** https://github.com/waqi-dev-community

## Overview

The WAQI API delivers real-time air quality index data from a global network of monitoring stations. Data covers major pollutants including PM2.5, PM10, NO2, CO, SO2, and Ozone, with support for city-level queries, geo-location-based lookups, and 3-8 day forecasts.

## Authentication

API access requires a free token obtained from the [Air Quality Open Data Platform](https://aqicn.org/data-platform/token/). The token is passed as a query parameter (`token`) with each request.

## Key Endpoints

- **City Feed:** `GET /feed/{city}/` - Real-time AQI for a named city or station
- **Geo-localized Feed:** `GET /feed/geo:{lat};{lng}/` - AQI by coordinates
- **IP-based Feed:** `GET /feed/here/` - AQI based on caller IP location
- **Station Search:** `GET /search/?keyword={keyword}` - Search for stations or cities
- **Map Queries:** Tile-based map data for AQI visualization

## Rate Limits

- Default: 1,000 requests per second per token
- Custom quotas available on request

## Pricing

Free for non-commercial use. Commercial use requires a written agreement with the WAQI project team.

## Resources

- [Plans & Pricing](plans/waqi-plans-pricing.yml)
- [Rate Limits](rate-limits/waqi-rate-limits.yml)
- [FinOps](finops/waqi-finops.yml)
- [APIs.json](apis.yml)
