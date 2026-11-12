# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- **Plane Integration**: Added global reusable workflow [`.github/workflows/plane-sync.yml`](.github/workflows/plane-sync.yml) to synchronize GitHub Issues, Issue Comments, Pull Requests, and Commits (`PROJ-123` / `fixes PROJ-123`) with self-hosted Plane (`https://plane.goover.dev`) via Plane REST API v1.
- **Starter Workflow Template**: Added [`workflow-templates/plane-sync.yml`](workflow-templates/plane-sync.yml) and [`workflow-templates/plane-sync.properties.json`](workflow-templates/plane-sync.properties.json) for 1-click setup across all `gOOvER` repositories.

### Fixed
- **Plane Integration**: Added automatic resolution for `PLANE_PROJECT_ID` (accepting short Project IDs like `GGE`, project names, full Plane URLs, UUIDs, or automatic repo-name matching) and `PLANE_WORKSPACE_SLUG` normalization, plus `workflow_dispatch` connection check support to prevent `404 Page not found` errors on non-UUID project identifiers.
