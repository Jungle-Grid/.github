<div align="center">
  <a href="https://junglegrid.dev">
    <img src="./assets/junglegrid-logo.png" alt="Jungle Grid logo" width="128">
  </a>

  <h1>Jungle Grid</h1>

  <p><strong>The execution layer for AI workloads and agents.</strong></p>

  <p>
    <a href="https://junglegrid.dev"><img alt="Jungle Grid website" src="https://img.shields.io/badge/Website-junglegrid.dev-111827?style=for-the-badge"></a>
    <a href="https://junglegrid.dev/docs"><img alt="Jungle Grid docs" src="https://img.shields.io/badge/Docs-Read_the_docs-2563eb?style=for-the-badge"></a>
    <a href="https://github.com/Jungle-Grid/mcp-server"><img alt="Jungle Grid MCP server" src="https://img.shields.io/badge/MCP-Server_repo-7c3aed?style=for-the-badge"></a>
    <a href="https://discord.com/invite/kpJqxXFFCs"><img alt="Join the Jungle Grid Discord" src="https://img.shields.io/badge/Discord-Join-5865f2?style=for-the-badge&logo=discord&logoColor=white"></a>
    <a href="https://x.com/jungle_grid"><img alt="Follow Jungle Grid on X" src="https://img.shields.io/badge/X-@jungle__grid-000000?style=for-the-badge&logo=x"></a>
    <a href="mailto:run@junglegrid.dev"><img alt="Email Jungle Grid" src="https://img.shields.io/badge/Email-run@junglegrid.dev-16a34a?style=for-the-badge"></a>
  </p>
</div>

---

Jungle Grid lets developers and AI agents run inference, training, fine-tuning, and batch workloads without manually managing GPUs, regions, providers, pods, or infrastructure settings.

Submit workload intent. Jungle Grid handles placement, routing, execution, lifecycle tracking, logs, retries and recovery, and artifact retrieval across available GPU capacity.

## What Jungle Grid Does

Jungle Grid turns AI workload intent into managed execution:

- Classifies workload type and execution requirements.
- Routes jobs across available GPU capacity.
- Tracks job state, logs, failures, retries, and artifacts.
- Gives developers one control plane across portal, CLI, API, and MCP entry points.

```text
Intent -> Routing -> GPU placement -> Execution -> Logs -> Artifacts
```

## Built For Developers And Agents

Jungle Grid is designed for teams building systems that need real compute without exposing every infrastructure decision to the caller.

- Developers can submit and monitor jobs without becoming GPU operations engineers.
- AI agents can estimate, launch, inspect, cancel, and retrieve results from workload runs.
- Internal tools can connect to a workload execution layer instead of directly managing provider-specific GPU primitives.

## Ways To Use Jungle Grid

| Surface | Use it for |
| --- | --- |
| Portal | Submit workloads, inspect jobs, review logs, and retrieve outputs from the web. |
| CLI | Run and automate jobs from local development, CI, and terminal workflows. |
| API | Integrate Jungle Grid into products, internal platforms, and backend services. |
| MCP | Give AI agents a controlled interface for estimating, submitting, tracking, and cancelling workloads. |

## Open Source And MCP

MCP is one major integration surface for Jungle Grid, enabling agent-facing compute workflows through MCP-compatible clients.

- [Jungle Grid MCP Server](https://github.com/Jungle-Grid/mcp-server) exposes tools for estimating, submitting, tracking, cancelling, reading logs, and retrieving artifacts.
- The hosted MCP endpoint connects agent workflows to the Jungle Grid API while keeping scheduling, routing, billing, and artifact storage in the platform layer.

## Get Started

- Visit [junglegrid.dev](https://junglegrid.dev) for the product overview.
- Read the [Jungle Grid docs](https://junglegrid.dev/docs) for setup and integration guides.
- Join the [Discord community](https://discord.com/invite/kpJqxXFFCs) for questions and updates.
- Contact the team at [run@junglegrid.dev](mailto:run@junglegrid.dev).
