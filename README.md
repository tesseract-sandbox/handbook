# Tesseract engineering handbook

## Service owners

Ask the owner before changing a system; they also approve access to it (see [Access policy](access-policy.md)).

| Service or system | Team | Owner |
|---|---|---|
| auth-service | Platform | Ishan Sinha |
| api-gateway | Infra | Dhruv Pendharkar |
| infra repo (terraform, runbooks) | Infra | Dhruv Pendharkar |
| Grafana (staging and prod dashboards) | Infra | Dhruv Pendharkar |
| prod read replica (`pg-prod-ro`) | Infra | Dhruv Pendharkar and Hamilton Park (both approve) |
| web-app | Product engineering | Karthik Valluri |
| ml-platform and the retrain pipeline | ML Platform | Karthik Valluri |

## How we work

- [Access policy](access-policy.md): asking for access to a repo, dashboard or database.
- [Customer data exports](customer-data-exports.md): when a customer asks for their data as a file.
- Staging signing keys rotate every two weeks: runbook in `infra/docs/runbooks/rotate-staging-keys.md`.

## Current migrations

- auth-service is moving from custom OAuth2 to OIDC. Epic [SBX-1](https://tesseract-sandbox.atlassian.net/browse/SBX-1), design doc in Drive
  ([Auth OIDC Migration - Design Doc](https://docs.google.com/document/d/1q1jUX_Fpo9L9UgbMBY5AtQXO-c3-9IVgF18GeswQz6Q/edit)). Ask in #auth-migration on Slack.
