# World Air Quality Index (WAQI)

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
