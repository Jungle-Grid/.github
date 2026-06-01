<div align="center">
  <a href="https://junglegrid.dev">
    <img src="./profile/assets/junglegrid-logo.png" alt="Jungle Grid logo" width="112">
  </a>

  <h1>Jungle Grid GitHub Defaults</h1>

  <p><strong>Community health files, templates, and public profile content for Jungle Grid.</strong></p>

  <p>
    <a href="https://junglegrid.dev"><img alt="Jungle Grid website" src="https://img.shields.io/badge/Website-junglegrid.dev-111827?style=for-the-badge"></a>
    <a href="https://junglegrid.dev/docs"><img alt="Jungle Grid docs" src="https://img.shields.io/badge/Docs-Read_the_docs-2563eb?style=for-the-badge"></a>
    <a href="https://github.com/Jungle-Grid/mcp-server"><img alt="Jungle Grid MCP server" src="https://img.shields.io/badge/MCP-Server_repo-7c3aed?style=for-the-badge"></a>
    <a href="https://discord.com/invite/kpJqxXFFCs"><img alt="Join the Jungle Grid Discord" src="https://img.shields.io/badge/Discord-Join-5865f2?style=for-the-badge&logo=discord&logoColor=white"></a>
    <a href="mailto:run@junglegrid.dev"><img alt="Email Jungle Grid" src="https://img.shields.io/badge/Email-run@junglegrid.dev-16a34a?style=for-the-badge"></a>
  </p>
</div>

---

Jungle Grid is the execution layer for AI workloads and agents. Developers submit inference, training, fine-tuning, and batch jobs by intent; Jungle Grid handles placement, routing, execution, lifecycle tracking, logs, retries, recovery, and artifact retrieval across available GPU capacity.

This repository supports the Jungle Grid GitHub organization. It contains the public organization profile README, default community health files, issue templates, pull request templates, and reusable workflow templates shared across Jungle Grid repositories.

## Repository Contents

| Path | Purpose |
| --- | --- |
| `profile/README.md` | Public Jungle Grid organization profile shown on GitHub. |
| `profile/assets/` | Brand assets used by the organization profile and repository README. |
| `ISSUE_TEMPLATE/` | Default issue templates for organization repositories. |
| `.github/workflows/` | Reusable CI workflows for Jungle Grid projects. |
| `workflow-templates/` | Workflow templates available to organization repositories. |
| `SECURITY.md`, `SUPPORT.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md` | Default community health and contribution guidance. |

## Platform Positioning

Jungle Grid abstracts low-level GPU infrastructure decisions behind workload intent.

- Developers and agents submit what they need to run.
- The platform handles placement across available GPU capacity.
- Jobs can be launched and inspected through the portal, CLI, API, and MCP integrations.
- Execution state, logs, recovery, and artifacts are tracked by the platform layer.

## Public Profile

The organization profile lives in [`profile/README.md`](./profile/README.md). Keep it concise, platform-level, and developer-first. MCP should be presented as a major integration surface, not as the entire product.

## Links

- [Website](https://junglegrid.dev)
- [Docs](https://junglegrid.dev/docs)
- [MCP Server](https://github.com/Jungle-Grid/mcp-server)
- [Discord](https://discord.com/invite/kpJqxXFFCs)
- [X](https://x.com/jungle_grid)
- [Email](mailto:run@junglegrid.dev)
