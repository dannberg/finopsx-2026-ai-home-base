We had a BigQuery cost anomaly this week. Details:
- Service: BigQuery, account 4421 (Data Engineering)
- Time period: Apr 28 – May 2
- Expected weekly spend: $4,200
- Actual spend: $11,800 (+181%)
- Suspected cause: New ETL pipeline deployed Apr 27; doing full table
  scans against a 14 TB table

I need two pieces of communication:

1. A 4-sentence Slack message for #data-engineering. Direct, peer tone,
   no acronym-explaining. Include the suspected cause and ONE specific
   ask: someone please review the ETL's query plan and confirm whether
   the full scans are intentional.

2. A short paragraph for our CFO's weekly digest. Lead with dollar
   impact, no service names if avoidable, what's been done to investigate,
   our timeline for resolution. Should not require the reader to know
   what BigQuery is.

For each version, end with one follow-up question that audience is
likely to ask but I haven't pre-empted in the message.
