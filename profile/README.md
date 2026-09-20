<h1 align="center">🫏 Donkey Development Kit</h1>

<p align="center">
  <strong>Takes the donkey work out of AI development.</strong>
</p>

<p align="center">
  An independent Python SDK for consuming <a href="https://www.mulesoft.com/">MuleSoft</a> Agent Fabric governance —
  typed refusals, budgets, OpenTelemetry spans, and correlation IDs — <em>without adopting Mule</em>.
</p>

---

## What is DDK?

DDK lets your AI application benefit from **Agent Fabric governance** without pulling the Mule runtime into your stack. It speaks the governance contract natively from Python:

- 🚦 **Typed refusals** — governance decisions arrive as structured, catchable types, not opaque errors.
- 💰 **Budgets** — enforce spend and usage limits before a call is made.
- 🔭 **OpenTelemetry spans** — every governed call is traced end to end.
- 🔗 **Correlation IDs** — follow a request across services and logs.

## Repositories

| Repo | What it is |
|------|------------|
| [**donkey-development-kit**](https://github.com/Donkey-Development-Kit/donkey-development-kit) | The core Python SDK — typed refusals, budgets, OTel spans, correlation IDs. |
| [**donkey-development-kit-demos**](https://github.com/Donkey-Development-Kit/donkey-development-kit-demos) | Runnable scenario and presentation demos, companion to the SDK. |

## Get started

```bash
git clone https://github.com/Donkey-Development-Kit/donkey-development-kit.git
cd donkey-development-kit/python
pip install -e ".[llm,langgraph]"   # base + raw client + one framework
```

Then head to the [SDK repo](https://github.com/Donkey-Development-Kit/donkey-development-kit) for usage and the [demos](https://github.com/Donkey-Development-Kit/donkey-development-kit-demos) to see it in action.
