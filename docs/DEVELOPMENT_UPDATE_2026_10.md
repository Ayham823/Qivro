# Qivro — October 2026 development update

Source reviewed for this update on **October 17, 2026**. This is a public engineering overview of ongoing local development. It does not announce a production launch or establish release acceptance.

## Recent engineering work

| Area | Work present in the local source | Current boundary |
| --- | --- | --- |
| Map discovery | Viewport/radius queries, reviewed building links, MapLibre presentation, cluster handling, and explicit loading/selection state | Development and pilot contracts; production rollout remains separate |
| Owner workflows | Listing readiness, owner insights, command-center views, and property context in messaging | Cross-service behavior requires coordinated review |
| Shared living | Room offerings, roommate discovery, household/consent contracts, and transaction-workspace foundations | Ongoing implementation; fixtures are synthetic rather than market evidence |
| Privacy and consent | Public-location response boundaries, monitoring-data filtering, and AI-training consent/retention contracts | Coverage and rollout checks remain part of release review |
| AI assistance | Grounded property answers, comparison/viewing-question contracts, and reviewed spatial-scene contracts | Backend remains the authorization and provider gateway; external providers require configuration |
| Administration | Trust-evidence review and reviewed-building-link workflows in the independent operator application | Privileged access remains enforced by the backend |
| Native client | Marketplace-read adapters, search models, email-verification alignment, and contract checks | Development foundation; Xcode/device acceptance is separate |
| Delivery | Source/migration inventory, feature-readiness tooling, and isolated backup/restore verification | Source checks do not prove a live deployment or a successful production restore |

## Repository boundaries

The workspace has **six independent product repositories**: customer frontend, backend API, AI service, infrastructure, admin application, and native client. Cross-project architecture and operating guidance belong to workspace documentation.

```text
Customer web / Admin / Native client
                  |
              Backend API
             /     |      \
      PostgreSQL  Redis   AI service
                          |
                  Configured providers
```

Clients consume backend contracts. They do not directly access databases or model providers. Browser and operator applications keep independent dependency and delivery lifecycles.

## How to interpret this update

- **Source present** means implementation files and associated tests/contracts exist in the reviewed local source.
- **Source review** and **test execution** are distinct. A feature list is not a claim that every path passed an acceptance test.
- Code updates are submitted for review separately from the public showcase. A branch or draft pull request is not a deployment.
- Database schema changes require forward migrations and rollout review. They are not applied as part of publishing this overview.
- No production customer data, credentials, internal logs, or database exports are included here.

For an overview of the existing product evidence, see [the main README](../README.md) and [project status](PROJECT_STATUS.md).
