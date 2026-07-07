# Real-Time-Fintech-Transaction-Monitoring-Pipeline

**Business Scenario**
**Company**: ModernPaymentsABC - a payment processor handling 500K+ transactions/day.

**Problem**: Fraud is rising, and overnight batch detection is too slow. The ops team needs real-time alerts for suspicious activity (velocity spikes, geo-anomalies), and compliance needs daily Suspicious Activity Reports (SARs).

**Your Role**: Senior Data Engineer building the end-to-end monitoring pipeline on Databricks.

**Learning Objectives**

By completing this lab, you will be able to:

- Ingest Streaming JSON with Auto Loader and capture malformed data using the Rescued Data Column.
- Implement Watermarked Deduplication to handle technical payment gateway retries.
- Perform Stream-Static Joins to enrich real-time events with customer and merchant reference data.
- Design a Rules Engine using Tumbling and Sliding windows for velocity detection.
- Build a Medallion Architecture that serves dual SLAs: real-time streaming alerts and batch Gold reporting.
- Optimize for Performance using Liquid Clustering.

**Architecture Overview**
- Bronze: Raw ingestion via Auto Loader + Watermarked Dedup.
- Silver: Enriched transactions + Real-time risk scoring & alerts.
- Gold: Aggregated merchant summaries and SAR pre-fill datasets.