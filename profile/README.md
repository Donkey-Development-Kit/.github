<h1 align="center">🫏 Donkey Development Kit</h1>

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

> **Alpha, pre-release** (`v0.1.0.dev1`) — not yet published to PyPI. Install from source:

```bash
git clone https://github.com/Donkey-Development-Kit/donkey-development-kit.git
cd donkey-development-kit/python
pip install -e ".[llm,langgraph]"   # base + raw client + one framework
```

Then head to the [SDK repo](https://github.com/Donkey-Development-Kit/donkey-development-kit) for usage and the [demos](https://github.com/Donkey-Development-Kit/donkey-development-kit-demos) to see it in action.

---

<sub>Unofficial &amp; independent — not affiliated with, endorsed by, or supported by Salesforce or MuleSoft. “Agent Fabric”, “MuleSoft”, “Anypoint”, and “Omni Gateway” are Salesforce trademarks. Licensed under Apache-2.0.</sub>
