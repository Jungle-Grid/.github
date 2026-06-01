# CI/CD Roadmap

## Current CI Baseline

Jungle Grid public repositories should use pull request CI with least-privilege `GITHUB_TOKEN` permissions, dependency installation from lockfiles, no deployment credentials, and no secrets passed to forked pull requests.

The shared reusable workflows in this repository provide:

- Node/TypeScript PR CI for repositories with real package scripts.
- Static/example PR CI for documentation, shell, JSON, YAML, and configuration repositories.
- Verified secret scanning in PR CI through TruffleHog.

## Repository Coverage

- `.github`: organization standards, default community files, workflow templates, and reusable CI.
- `mcp-server`: npm package candidate/current package; CI should build and test before merge.
- `junglegrid-examples`: examples and documentation; CI should validate configuration files and shell examples.
- `forgegrid`: Next.js application; CI should run the real lint/build scripts before merge.

## CD Readiness

Production deployment and package publishing are intentionally not configured in this baseline. A release workflow should be added only after each repository has a documented release contract, required maintainers, rollback expectations, and scoped credentials.

Recommended future release paths:

- `mcp-server`: use a manual `workflow_dispatch` or tag-based npm publish workflow with npm provenance, an `NPM_TOKEN` scoped to `@jungle-grid/mcp`, protected environments, and required maintainer approval.
- `junglegrid-examples`: no deployment is needed unless examples are later published as documentation artifacts.
- `forgegrid`: define the hosting target, environment names, required secrets, preview behavior, production approval policy, and rollback plan before adding CD.
- `.github`: no deployment workflow is needed.
