I need a BigQuery query against our GCP billing export. Here's the schema:

TABLE: finops.gcp_billing_export
- usage_start_time TIMESTAMP
- service.description STRING
- sku.description STRING
- project.id STRING
- labels ARRAY<STRUCT<key STRING, value STRING>>
- cost FLOAT64
- credits ARRAY<STRUCT<amount FLOAT64, name STRING>>

I want net cost (cost minus credits) for the current month, broken down by:
1. The Kubernetes namespace, found in the `k8s_namespace` label key
2. Filtered to GKE services only (service.description LIKE "%Kubernetes%")
3. Sorted by net cost, descending, top 25

Show me the query. Then list every assumption you made about my schema
that I should double-check before running it.
