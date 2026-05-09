# Jungle Grid

**The execution layer for AI workloads and agents.**

Jungle Grid lets developers submit AI workloads by intent - inference, training, fine-tuning, and batch jobs - without manually choosing GPUs, regions, providers, pods, or infrastructure settings.

Instead of asking developers to think like cloud infrastructure engineers, Jungle Grid lets them say what they want to run. The platform handles placement, routing, execution, logs, lifecycle tracking, and recovery across available GPU capacity.

Website: https://junglegrid.dev  
Docs: https://junglegrid.dev/docs

---

## What is Jungle Grid?

Jungle Grid is a GPU orchestration platform built for AI teams, developers, and agents.

Modern AI workloads are hard to run because developers often have to answer low-level infrastructure questions before they can even execute a job:

- Which GPU should I pick?
- Is this model too large for the available VRAM?
- Which provider has capacity right now?
- What happens if the node fails?
- How do I track logs and job state?
- How does my AI agent run real workloads safely?

Jungle Grid abstracts that complexity.

Developers describe the workload, and Jungle Grid handles the execution layer underneath.

---

## Core idea

Traditional GPU platforms start with hardware:

> Pick a GPU.  
> Pick a region.  
> Configure a pod.  
> Manage execution yourself.

Jungle Grid starts with workload intent:

> Run this inference job.  
> Fine-tune this model.  
> Execute this batch workload.  
> Let my agent submit and monitor this job.

Jungle Grid then decides how and where the workload should run.

---

## What Jungle Grid handles

Jungle Grid provides:

- Workload-first job submission
- Intent-based workload classification
- GPU fit checks based on workload requirements
- Routing across available compute capacity
- Provider-aware placement
- Managed job execution
- Job lifecycle tracking
- Live and historical logs
- Retry and recovery behavior
- Artifact handling
- CLI-based developer workflow
- API/service integration
- MCP integration for AI agents

---

## Supported workload types

Jungle Grid is designed for AI workloads such as:

- Inference
- Training
- Fine-tuning
- Batch jobs
- Model evaluation
- Data processing
- Agent-triggered compute tasks

---

## Why Jungle Grid exists

AI development is moving toward agents, automation, and workload-level execution.

But most compute platforms still expose infrastructure-first primitives. That means developers and agents still need to think about GPU types, pod management, regions, capacity failures, and operational details.

Jungle Grid exists to make compute feel closer to an execution layer:

```text
Intent -> Routing -> GPU placement -> Execution -> Logs -> Results
```

The goal is simple:

Developers and agents should submit workloads, not manage GPU infrastructure.

---

## Quick start

Install and authenticate with the Jungle Grid CLI:

```bash
npx @jungle-grid/cli@latest login
```

This command runs the Jungle Grid CLI without requiring a global install and starts the login flow.

Check your authenticated user:

```bash
npx @jungle-grid/cli@latest whoami
```

This command confirms that the CLI is connected to your Jungle Grid account.

Submit an inference workload:

```bash
npx @jungle-grid/cli@latest submit \
  --workload inference \
  --model-size 7 \
  --image pytorch/pytorch:2.4.0-cuda12.1-cudnn9-runtime \
  --name chat-infer
```

This command submits an inference job, tells Jungle Grid the approximate model size, provides the container image to run, and gives the job a readable name.

Check jobs:

```bash
npx @jungle-grid/cli@latest jobs
```

This command lists your submitted workloads.

Check the status of a specific job:

```bash
npx @jungle-grid/cli@latest status <job-id>
```

This command shows the current lifecycle state of a submitted job.

---

## CLI workflow

The Jungle Grid CLI is built around a simple loop:

```text
login -> submit workload -> inspect status -> view logs -> collect results
```

The CLI lets developers interact with Jungle Grid from their terminal without manually managing GPU servers or provider dashboards.

---

## MCP for agents

Jungle Grid includes an MCP layer so AI agents can submit and monitor workloads from inside agent workflows.

This allows agentic systems to move from planning to execution.

Instead of only suggesting that a workload should run, an agent can use Jungle Grid to:

- Estimate a workload
- Submit a job
- Monitor job state
- Retrieve logs
- Track completion
- Reason over execution results

This makes Jungle Grid useful as an execution backend for AI coding agents, internal automation agents, research agents, and developer tools.

---

## Example use cases

Jungle Grid can be used for:

- Running model inference without managing GPUs
- Testing AI workloads across available capacity
- Running batch processing jobs
- Triggering compute from an AI agent
- Fine-tuning models
- Building developer tools that need GPU-backed execution
- Creating automation workflows that require real compute
- Abstracting GPU complexity away from end users

---

## Platform architecture

At a high level, Jungle Grid includes:

```text
Developer / Agent
      |
      v
CLI / API / MCP
      |
      v
Jungle Grid Orchestrator
      |
      v
Scheduler and Routing Layer
      |
      v
GPU Capacity Providers / Nodes
      |
      v
Workload Execution
      |
      v
Logs, Status, Artifacts, Results
```

The platform is built around separating workload intent from infrastructure execution.

---

## Core components

### Orchestrator

The orchestrator receives jobs, validates workload intent, tracks lifecycle state, and coordinates execution.

### Scheduler

The scheduler evaluates workload requirements, available capacity, GPU fit, provider health, and execution constraints.

### Node agent

The node agent connects compute nodes to Jungle Grid and allows workloads to run on available GPU capacity.

### Provider integrations

Jungle Grid can route workloads across compatible GPU capacity providers instead of locking execution into one provider model.

### CLI

The CLI gives developers a simple terminal interface for login, submission, inspection, and job tracking.

### MCP server

The MCP server allows AI agents and MCP-compatible tools to interact with Jungle Grid as an execution layer.

---

## Why not just rent a GPU?

Renting a GPU gives you hardware.

Jungle Grid gives you an execution workflow.

With raw GPU rentals, you often still need to:

- Choose the GPU manually
- Check VRAM fit yourself
- Configure the environment
- Handle provider capacity issues
- Track job state
- Manage logs
- Retry failed jobs
- Build agent integration yourself

Jungle Grid is designed to sit above that layer.

The goal is not simply to expose GPUs.

The goal is to make AI workload execution easier, safer, and more automated.

---

## Jungle Grid is for

- AI developers
- ML engineers
- AI startups
- Agent builders
- Developer tool companies
- Research teams
- Infrastructure teams
- Builders who need GPU execution without GPU operations overhead

---

## Current focus

Jungle Grid is currently focused on:

- Reliable workload submission
- Inference execution
- CLI and API workflows
- Live logs and job lifecycle visibility
- MCP-based agent execution
- Provider-aware routing
- Improving cold-start and execution reliability
- Making GPU-backed jobs easier for developers to run

---

## Public repositories

This GitHub organization will host public developer-facing Jungle Grid projects, including:

- CLI tools
- MCP server examples
- SDKs
- Workload templates
- Example jobs
- Integration guides
- Community resources

Core platform services may remain private while the system is under active development.

---

## Documentation

Read the docs here:

https://junglegrid.dev/docs

The docs cover:

- Getting started
- CLI usage
- Job submission
- Provider setup
- API usage
- MCP integration
- Workload examples

---

## Community and support

For questions, feedback, or early access:

Website: https://junglegrid.dev  
Docs: https://junglegrid.dev/docs  
Email: support@junglegrid.dev

For security issues, please do not open a public issue. Email:

security@junglegrid.dev

---

## One-line summary

Jungle Grid lets developers and agents run AI workloads by intent, while the platform handles GPU placement, routing, execution, logs, and recovery.