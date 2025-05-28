# GOV.UK Search API v2 Dataform

## What's in this repo

This repo contains:

- [`definitions/`](definitions/): Google Dataform SQLX pipeline definitions for processing and transforming GA4 data into Google Verex AI Search datasets
- [`workflow_setting.yaml`](workflow_settings.yaml): Google Dataform workflow settings that apply to all pipelines

### What's not in this repo

Terraform definitions for dataform resources used to provision corresponding workflow and release configurations - [alphagov/govuk-infrastructure/blob/main/terraform/deployments/search-api-v2/dataform.tf](https://github.com/alphagov/govuk-infrastructure/blob/main/terraform/deployments/search-api-v2/dataform.tf).

## Usage

Install the [Dataform CLI](https://cloud.google.com/dataform/docs/use-dataform-cli) for local development.

Currently no [Dataform Workspace](https://cloud.google.com/dataform/docs/workspaces) is established for Google Cloud Console based pipeline development - all development is performed locally before pushing progressively into each environment/branch. Each Search API v2 GCP project/environment has a seperate Dataform Release configuration which maps onto the corresponding branch (i.e. `integration`, `staging` etc.).

## Documentation

See the [Google Dataform documentation](https://cloud.google.com/dataform/docs/overview).

## Team

GOV.UK Search team looks after this repo. If you're inside GDS, you can find us in [#govuk-search](https://gds.slack.com/channels/govuk-search)
