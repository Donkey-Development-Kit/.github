<h1 align="center">🫏 Donkey Development Kit</h1>

<p align="center">
  <a href="https://pypi.org/project/donkey-kit/">
    <img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fpypi.org%2Fpypi%2Fdonkey-kit%2Fjson&query=%24.info.version&prefix=v&label=PyPI&logo=pypi&logoColor=white&color=blue&cacheSeconds=300" alt="PyPI version">
  </a>
  <a href="https://pypi.org/project/donkey-kit/">
    <img src="https://img.shields.io/pypi/pyversions/donkey-kit?logo=python&logoColor=white" alt="Supported Python versions">
  </a>
  <a href="https://github.com/Donkey-Development-Kit/donkey-development-kit/actions/workflows/ci.yml?query=branch%3Adevelop">
    <img src="https://img.shields.io/github/actions/workflow/status/Donkey-Development-Kit/donkey-development-kit/ci.yml?branch=develop&label=CI&logo=githubactions&logoColor=white" alt="CI status">
  </a>
  <a href="https://pepy.tech/projects/donkey-kit">
    <img src="https://img.shields.io/pepy/dt/donkey-kit?label=downloads" alt="Total downloads">
  </a>
  <a href="https://github.com/Donkey-Development-Kit/donkey-development-kit/blob/main/LICENSE">
    <img src="https://img.shields.io/pypi/l/donkey-kit?color=green" alt="License: Apache-2.0">
  </a>
  <a href="https://docs.donkey-kit.dev">
    <img src="https://img.shields.io/badge/docs-docs.donkey--kit.dev-0A7BBB?logo=readthedocs&logoColor=white" alt="Documentation">
  </a>
</p>

<p align="center">
  <a href="https://docs.donkey-kit.dev/frameworks/langgraph"><img src="https://img.shields.io/badge/LangGraph-1C3C3C?logo=langgraph&logoColor=white" alt="LangGraph"></a>
  <a href="https://docs.donkey-kit.dev/frameworks/adk"><img src="https://img.shields.io/badge/Google_ADK-4285F4?logo=google&logoColor=white" alt="Google ADK"></a>
  <a href="https://docs.donkey-kit.dev/frameworks/openai"><img src="https://img.shields.io/badge/OpenAI_Agents_SDK-412991" alt="OpenAI Agents SDK"></a>
  <a href="https://docs.donkey-kit.dev/frameworks/agent-framework"><img src="https://img.shields.io/badge/Microsoft_Agent_Framework-5E5E5E" alt="Microsoft Agent Framework"></a>
  <a href="https://docs.donkey-kit.dev/frameworks/anthropic"><img src="https://img.shields.io/badge/Anthropic-191919?logo=anthropic&logoColor=white" alt="Anthropic"></a>
  <a href="https://docs.donkey-kit.dev/frameworks/crewai"><img src="https://img.shields.io/badge/CrewAI-FF5A50?logo=crewai&logoColor=white" alt="CrewAI"></a>
  <a href="https://docs.donkey-kit.dev/frameworks/llamaindex"><img src="https://img.shields.io/badge/LlamaIndex-8A2BE2" alt="LlamaIndex"></a>
  <a href="https://docs.donkey-kit.dev/frameworks/strands"><img src="https://img.shields.io/badge/Strands_Agents-FF9900" alt="Strands Agents"></a>
  <a href="https://docs.donkey-kit.dev/telemetry"><img src="https://img.shields.io/badge/OpenTelemetry-425CC7?logo=opentelemetry&logoColor=white" alt="OpenTelemetry"></a>
</p>

<p align="center">
  <strong>Takes the donkey work out of AI development.</strong>
</p>

<p align="center">
  An independent, community-maintained Python SDK for consuming <strong>MuleSoft Agent Fabric</strong> capabilities:
  governed model and MCP tool access, Exchange publishing, user identity, and approvals from your own agent framework and IDE,
  <em>without adopting Mule</em>.
</p>

---

## What is DDK?

DDK connects your Python AI application to **MuleSoft Agent Fabric** while you keep your own framework and IDE, **without deploying or running the Mule runtime**. The gateway enforces policy; DDK makes its decisions visible and actionable in your code.

With **donkey-kit**, you can:

- 🔗 **Use governed models and MCP tools**: call models through the gateway, discover governed MCP servers in Exchange, and bind their tools to native framework objects.
- 📦 **Publish from code and CI**: scan agents and MCP servers, publish them to Exchange, and verify live tools and agent cards against what you published.
- 🔐 **Carry user identity and pause for approval**: forward on-behalf-of user tokens, gate tools with human-in-the-loop approvals, and handle the gateway's CIBA step-up decisions as typed outcomes.
- 🤝 **Serve A2A agents**: make your agent callable through the official `a2a-sdk`, with local simulated ingress and CLI tooling to expose it behind a gateway.
- 🚦 **React to typed refusals and pace usage**: catch structured governance exceptions, register refusal handlers and custom policy types, and use gateway-reported budget windows to slow down before hitting a limit.
- 🔭 **Trace and test governance**: OpenTelemetry GenAI spans, correlation IDs, cost attribution, a local gateway simulator, and a pytest conformance plugin help you observe calls and test refusal paths before production.

**Framework support is deliberately differentiated.** LangGraph and the OpenAI Agents SDK are conformance-tested adapters. Google ADK, Strands, Microsoft Agent Framework, Anthropic, CrewAI, and LlamaIndex provide native factories and `connection_kwargs()`, with framework-specific limitations documented in the [support matrix](https://docs.donkey-kit.dev/frameworks).

DDK consumes platform capabilities; it does not replace policy enforcement or ship a provisioning control plane. See the [feature overview](https://docs.donkey-kit.dev/feature-overview) and [verification ledger](https://github.com/Donkey-Development-Kit/donkey-development-kit/blob/main/docs/verified-apis.md) for shipped features, evidence, and remaining verification-gated surfaces.

## Repositories

| Repo | What it is |
|------|------------|
| [**donkey-development-kit**](https://github.com/Donkey-Development-Kit/donkey-development-kit) | The Python SDK and CLI: governed model and MCP tool access, Exchange publication, user identity, approvals, A2A serving, typed refusals, budget pacing, telemetry, and local testing. |
| [**donkey-development-kit-demos**](https://github.com/Donkey-Development-Kit/donkey-development-kit-demos) | Runnable scenario and presentation demos, companion to the SDK. |

## Get started

> **Alpha, published on PyPI.** See the [release notes](https://github.com/Donkey-Development-Kit/donkey-development-kit/releases/latest) for what's new. Requires Python 3.10 or newer.

```bash
pip install "donkey-kit[llm,langgraph]"   # base + raw client + one framework
```

Add `mcp` for governed tool binding, `a2a` for agent serving, or `cli,local` for command-line tooling and the simulator. The `all` extra includes these plus LangGraph and OpenTelemetry, not every framework; add your framework's extra separately.

Start with the [quickstart](https://docs.donkey-kit.dev/quickstart), choose your [framework](https://docs.donkey-kit.dev/frameworks), and explore the [demos](https://github.com/Donkey-Development-Kit/donkey-development-kit-demos). Registry, discovery, and publication operations need an Anypoint connected app with the [appropriate scopes](https://github.com/Donkey-Development-Kit/donkey-development-kit/blob/main/docs/scopes.md).

---

<sub>Unofficial & independent — not affiliated with, endorsed by, or supported by Salesforce or MuleSoft. “Agent Fabric”, “MuleSoft”, “Anypoint”, and “Omni Gateway” are Salesforce trademarks. Licensed under Apache-2.0.</sub>
