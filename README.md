# Template to build and deploy an API in Konnect
The template of the OAS (OpenAPI Specification) is located in `mon-api/openapi.yaml`

When the Developer commits this repo, a pipeline is executed to publish the API in Konnect - Development environment for Kong Gateway, Catalog and Developer Portal

## Platform Team
The Platform Team controls and enforces the governance & security by adding policies in the CI pipeline. See policies enforcement in `platform/`. The policies have the `platform-repo-managed` Kong Gateway flag

## API Lifecycle
During the commit, a PR is created to deploy the API in the Development environment. The API Owner merges the PR to deploy the API in a Development environment

`Promote API to Konnect Environments` is the  Git worflow that promotes the API from Development to Test and Test to Production

## Country
The PR is executed for `environment: FRANCE_DEV`. Adapt it for other countries