# Data Schema

This document describes the basic data schema used by the starter prototype.

Tables

1) regions (sample_data/regions.csv)
- region_id (string) - unique region identifier
- region_name (string)
- latitude (float)
- longitude (float)

2) prices (sample_data/prices.csv)
- date (ISO date)
- region_id (string) - FK -> regions.region_id
- crop (string) - e.g., rice, maize
- market (string) - market name
- price_usd_per_ton (float)

3) production (sample_data/production.csv)
- date (ISO date)
- region_id (string)
- crop (string)
- production_tons (float)
- area_ha (float)

Notes
- All PII is omitted in the sample data.
- Dates use YYYY-MM-DD format.
- In production, store raw landing data (S3), then write curated Parquet/Delta to a data lake.
