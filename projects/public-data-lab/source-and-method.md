# Source and method

Source: NYC Open Data dataset **311 Service Requests from 2020 to Present**, dataset identifier `erm2-nwe9`. The City describes each row as a service request with fields such as complaint type, responding agency, and location. This portfolio sample requests only a limited set of non-location, non-free-text fields.

- Dataset information: https://catalog.data.gov/dataset/311-service-requests-from-2010-to-present
- NYC dataset update notes: https://www.nyc.gov/opendata/news/all-news/311-Service-Requests-Updates
- Exact API query is linked in `case-study.md` and the dashboard.
- Sample: latest 1,200 Jan 2025 records in descending creation time at extraction. It is a convenience sample.
- Reproduce: open the NYC Open Data API endpoint in the case study, request the same selected fields and date filter, then apply descending `created_date` order and the recorded row limit. The live dataset can change, so later extracts may differ.
- No city targets, SLA compliance, employer data, or causal claims are inferred.
