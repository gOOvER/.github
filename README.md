# 🌐 gOOvER's Global GitHub Configuration (`.github`)

This repository contains the default [Community Health Files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file), templates, and global development rules for all **[gOOvER](https://github.com/gOOvER)** repositories.

## 📁 Contents

| File / Folder | Purpose |
| :--- | :--- |
| [`FUNDING.yml`](FUNDING.yml) / [`.github/FUNDING.yml`](.github/FUNDING.yml) | Global Sponsor & Donation links for all repositories |
| [`SECURITY.md`](SECURITY.md) | Default security vulnerability reporting policy |
| [`SUPPORT.md`](SUPPORT.md) | Default support & help resources |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Default contribution guidelines |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Contributor Covenant Code of Conduct |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/) | Global Bug Report & Feature Request issue forms |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Global Pull Request template |
| [`.github/workflows/plane-sync.yml`](.github/workflows/plane-sync.yml) | Global reusable GitHub Action (`workflow_call`) to sync Issues, Comments, PRs & Commits to Plane (`https://plane.goover.dev`) |
| [`workflow-templates/`](workflow-templates/) | 1-Click GitHub Starter Workflow (**Plane Sync**) shown in **Actions → New workflow** across all `gOOvER` repositories |
| [`GEMINI.md`](GEMINI.md) & [`rules/`](rules/) | Global AI Agent rules & standards (`CHANGELOG.md`, versioning, funding) |

## 🔗 Using Plane Sync in Any Repository

1. In **Plane** (`https://plane.goover.dev`):
   - Create an API token under **Workspace Settings → API Tokens**.
   - Copy your **Workspace Slug** (from the URL `https://plane.goover.dev/<workspace-slug>/...`) and the target **Project ID** (UUID in **Project Settings**).
2. In your **GitHub Repository** (**Settings → Secrets and variables → Actions**):
   - `PLANE_API_KEY`: Your Plane API token
   - `PLANE_WORKSPACE_SLUG`: Your Plane workspace slug *(or pass via `with: plane_workspace_slug`)*
   - `PLANE_PROJECT_ID`: Target Plane project UUID *(or pass via `with: plane_project_id`)*
3. Add `.github/workflows/plane-sync.yml` (or select **Plane Sync (gOOvER)** directly under **Actions → New workflow**):

```yaml
name: Plane Sync

on:
  issues:
    types: [opened, edited, closed, reopened]
  issue_comment:
    types: [created]
  pull_request:
    types: [opened, reopened, ready_for_review, closed]
  push:
    branches: [main, master]

jobs:
  plane-sync:
    uses: gOOvER/.github/.github/workflows/plane-sync.yml@main
    with:
      plane_base_url: "https://plane.goover.dev"
    secrets:
      PLANE_API_KEY: ${{ secrets.PLANE_API_KEY }}
      PLANE_WORKSPACE_SLUG: ${{ secrets.PLANE_WORKSPACE_SLUG }}
      PLANE_PROJECT_ID: ${{ secrets.PLANE_PROJECT_ID }}
```
