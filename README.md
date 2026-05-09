# smolla-contracts

Shared contracts package containing domain event schemas, OpenAPI specifications, and DTOs consumed across Smolla services. No runtime; build-time only.

## Repository layout

```
dotnet/                  .NET classlib published as Smolla.Contracts (NuGet)
typescript/              TypeScript package published as @smolla/contracts (npm)
```

## Local development

```
# .NET
cd dotnet
dotnet build

# TypeScript
cd typescript
npm install
npm run build
```

## Workflows

- `ci.yml` — runs on every push and PR
- `deploy-prod.yml` — runs on push to `main`
- `deploy-staging.yml` — runs on push to `develop`
- `deploy-test.yml` — manual dispatch for shared test slot
- `release-please.yml` — opens release PRs based on conventional commits
- `sync-main-to-develop.yml` — back-merges hotfixes from `main` into `develop`

## Versioning

Managed by `release-please`; the canonical version lives in `version.txt` and is propagated to project files on each release.

## Licence

GNU Affero General Public License v3.0 — see [LICENSE](LICENSE).

Copyright (c) 2026 Adam Salisbury.

