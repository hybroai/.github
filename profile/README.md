<div align="center">
  <a href="https://hybro.ai">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/hybroai/hybro/main/assets/logo-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/hybroai/hybro/main/assets/logo-light.svg">
      <img src="https://raw.githubusercontent.com/hybroai/hybro/main/assets/logo-dark.svg" alt="Hybro AI" width="420">
    </picture>
  </a>

  <p>
    <strong>An open interoperability layer for AI agents &amp; robots.</strong><br />
    Connect independently built agents, run them together, and stay in control of what executes.
  </p>

  <p>
    <a href="https://hybro.ai"><img src="https://img.shields.io/badge/hybro.ai-111111?style=for-the-badge" alt="hybro.ai"></a>
    <a href="https://opensource.org/licenses/Apache-2.0"><img src="https://img.shields.io/badge/Apache%202.0-orange?style=for-the-badge" alt="Apache 2.0"></a>
    <a href="https://discord.gg/2S5pCKzUmJ"><img src="https://img.shields.io/badge/Discord-5865F2?logo=discord&logoColor=white&style=for-the-badge" alt="Discord"></a>
    <a href="https://x.com/HybroAI"><img src="https://img.shields.io/badge/X-000000?logo=x&logoColor=white&style=for-the-badge" alt="X"></a>
    <a href="https://www.linkedin.com/company/hybroai"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white&style=for-the-badge" alt="LinkedIn"></a>
  </p>
</div>

---

## What is Hybro?

Hybro is open-source interoperability infrastructure for AI agents. It lets local and remote agents communicate, collaborate, and execute multi-step work over the [Agent2Agent (A2A) protocol](https://a2a-protocol.org/), while you authorize, inspect, and record what runs.

Think of Hybro as a **self-hosted control plane** for agent collaboration: sources decide the steps; Hybro runs, gates, and records them.

<p align="center">
  <img src="https://raw.githubusercontent.com/hybroai/hybro/main/assets/screenshots/chat-demo.gif" alt="Hybro room chat coordinating multiple agents" width="760">
</p>

## Start here

| Goal | Project |
|---|---|
| Run the Hybro platform (UI, API, MCP, bundled agents) | [`hybro`](https://github.com/hybroai/hybro) |
| Make any agent speak A2A (frameworks, CLIs, local coding agents) | [`a2a-adapter`](https://github.com/hybroai/a2a-adapter) |
| Bring robots onto A2A | [`a2a-robots`](https://github.com/hybroai/a2a-robots) |
| Inspect and debug A2A agents | [`a2a-agent-inspector`](https://github.com/hybroai/a2a-agent-inspector) |

### Try Hybro in one command

```bash
curl -fsSL https://hybro.ai/install.sh | sh
hybro
```

Then open [http://localhost:3000](http://localhost:3000). Details: [hybro README](https://github.com/hybroai/hybro#getting-started).

### Wrap an agent with A2A Adapter

```bash
pip install a2a-adapter
# or: uv tool install a2a-adapter
```

```python
from a2a_adapter import CallableAdapter, serve_agent

async def my_agent(inputs: dict) -> str:
    return f"Echo: {inputs['message']}"

serve_agent(CallableAdapter(func=my_agent, name="Echo Agent"), port=9000)
```

Docs: [a2a-adapter README](https://github.com/hybroai/a2a-adapter).

## Open-source projects

- **[hybro](https://github.com/hybroai/hybro)** — Open interoperability platform for AI agents: rooms, streaming, MCP, and one-container deploy.
- **[a2a-adapter](https://github.com/hybroai/a2a-adapter)** — SDK + CLI to serve LangGraph, LangChain, CrewAI, n8n, Claude Code, Codex, Pi, OpenClaw, and more as A2A servers.
- **[a2a-robots](https://github.com/hybroai/a2a-robots)** — A2A adapters for robots.
- **[a2a-agent-inspector](https://github.com/hybroai/a2a-agent-inspector)** — Tools for inspecting A2A agent cards and behavior.
- **[hybro-hub](https://github.com/hybroai/hybro-hub)** — Earlier hub for local and remote agent connectivity.

## Community

- Website: [hybro.ai](https://hybro.ai)
- Discord: [Join](https://discord.gg/2S5pCKzUmJ)
- X: [@HybroAI](https://x.com/HybroAI)
- Contact: [info@hybro.ai](mailto:info@hybro.ai)

Contributions are welcome. Start with issues and PRs on the project you care about; each repo has its own contributing guide.
