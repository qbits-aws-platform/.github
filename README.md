# Qbits Platform Engineering
Enterprise-grade AWS data platform built to production standards.

## Architecture
Multi-account AWS organisation mirroring financial services 
patterns — separate ingest, process-storage, and egress layers 
across dev/test/pre-prod/production environments.

## Stack
- **IaC**: Terraform with remote state + DynamoDB locking
- **Auth**: AWS IAM Identity Center (SSO) with OIDC for CI/CD
- **Ingest**: Lambda · SQS · EventBridge · S3
- **Transform**: AWS Glue (PySpark) · Delta Lake
- **Serving**: Redshift Serverless · dbt · Athena
- **Governance**: SCPs · CloudTrail · AWS Config
- **CI/CD**: GitHub Actions with environment protection gates

## Repos
| Repo | Purpose |
|------|---------|
| [platform-infra](link) | Networking, OIDC, shared infrastructure |
| [do-aws-lakehouse-ingest](link) | S3 landing, Lambda ingest, SQS |
| [do-aws-lakehouse-process-storage](link) | Glue ETL, Redshift, Delta Lake |
