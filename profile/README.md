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
  <a href="https://github.com/Donkey-Development-Kit/donkey-development-kit/blob/develop/LICENSE">
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
  An independent, community-maintained Python SDK for consuming <strong>Agent Fabric</strong> capabilities —
  governed model access, governed tool access, and provisioning-as-code — from your own agent framework and IDE,
  <em>without adopting Mule</em>.
</p>

---

## What is DDK?

DDK lets your AI application consume **Agent Fabric** governance from Python — **without deploying or running the Mule runtime**. It speaks the governance contract natively:

- 🚦 **Typed refusals** — governance decisions arrive as structured, catchable types, not opaque errors.
- 💰 **Budgets** — enforce spend and usage limits before a call is made.
- 🔭 **OpenTelemetry spans** — every governed call is traced end to end.
- 🔗 **Correlation IDs** — follow a request across services and logs.

## Repositories

| Repo | What it is |
|------|------------|
| [**donkey-development-kit**](https://github.com/Donkey-Development-Kit/donkey-development-kit) | The core Python SDK — governed model & tool access, provisioning-as-code, typed refusals, budgets, OTel spans, correlation IDs. |
| [**donkey-development-kit-demos**](https://github.com/Donkey-Development-Kit/donkey-development-kit-demos) | Runnable scenario and presentation demos, companion to the SDK. |

## Get started

> **Alpha — published on PyPI.**

```bash
pip install "donkey-kit[llm,langgraph]"   # base + raw client + one framework
```

Then head to the [SDK repo](https://github.com/Donkey-Development-Kit/donkey-development-kit) for usage and the [demos](https://github.com/Donkey-Development-Kit/donkey-development-kit-demos) to see it in action.

---

<sub>Unofficial & independent — not affiliated with, endorsed by, or supported by Salesforce or MuleSoft. “Agent Fabric”, “MuleSoft”, “Anypoint”, and “Omni Gateway” are Salesforce trademarks. Licensed under Apache-2.0.</sub>
