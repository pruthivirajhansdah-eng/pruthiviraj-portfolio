# Public-data service-request analysis

## Question
What descriptive workflow signals appear in a bounded sample of NYC 311 service requests, and what would an analyst validate next?

## Source and extraction
NYC Open Data, “311 Service Requests from 2020 to Present,” dataset `erm2-nwe9`. The sample contains the latest 1,200 records returned for Jan 1–31, 2025, ordered by creation time descending at extraction. Selected fields: request key, created date, closed date, agency, complaint type, and status. Free text and location fields were not requested.

Source page: https://catalog.data.gov/dataset/311-service-requests-from-2010-to-present
API endpoint and query: https://data.cityofnewyork.us/resource/erm2-nwe9.json?%24select=unique_key%2Ccreated_date%2Cclosed_date%2Cagency%2Ccomplaint_type%2Cstatus&%24where=created_date+%3E%3D+%272025-01-01T00%3A00%3A00%27+AND+created_date+%3C+%272025-02-01T00%3A00%3A00%27&%24order=created_date+DESC&%24limit=1200

## Sample findings
- Records returned: 1200
- Records with a closure timestamp: 1198 (99.8% of this bounded sample)
- Median elapsed time from creation to closure among the 1198 records with both timestamps: 3.3 hours. This is not an SLA measure.
- The most frequent request category in this sample: **Noise - Residential** (277 records).

## Limitations
This is a convenience sample of recent records in one month, not a random or representative sample. The city dataset may be updated or corrected after extraction. Complaint categories and status are city-defined. “Closed” does not establish customer satisfaction or service quality. Elapsed time is descriptive and can be affected by agency-specific workflows and data-entry practices. No city service target is inferred.

## Analyst follow-up
Validate category definitions and timezone handling; compare a full-month query; profile missing closure timestamps by category and agency; speak with process owners about lifecycle states; and agree a meaningful target before describing performance. Do not directly compare this civic service dataset to enterprise IT support.
