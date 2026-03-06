<div align="center">

# ⚡ GodLocal

### Your AI. Your machine.

**The fastest local AI inference platform.**\
17,000 tokens/sec · Autonomous agents · 5-tier smart routing · 100% local

[![Website](https://img.shields.io/badge/website-godlocal.ai-blue?style=for-the-badge)](https://godlocal.ai)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=for-the-badge)](CONTRIBUTING.md)

[Website](https://godlocal.ai) · [Demo](https://godlocal.ai/oasis) · [Docs](#documentation) · [Contributing](CONTRIBUTING.md)

</div>

---

## 💡 What is GodLocal?

GodLocal is an autonomous AI platform that runs entirely on your hardware. No cloud dependency, no data leaks, no vendor lock-in.

- **⚡ Blazing fast** — 17,000 tokens/sec via intelligent 5-tier routing
- **🤖 Autonomous agents** — Agents with memory, emotions, and self-reflection (SOUL files)
- **🔒 100% private** — All inference runs locally. Your data never leaves your machine
- **📱 Mobile-ready** — CoreML + ANE on iPhone. LFM2 24B @ 40 tok/s
- **🌐 Open Core** — Community edition free forever. Pro features for teams & enterprise

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────┐
│                    TieredRouter                        │
│  WASM → BitNet → Cerebras → Groq → AirLLM 70B+        │
│  ~85% token cost savings · auto-fallback · zero config  │
└─────────────────────────────────────────────────────┘
        │              │              │              │
   ┌────┴────┐  ┌────┴────┐  ┌────┴────┐  ┌────┴────┐
   │  Agents  │  │  Memory  │  │  Tools   │  │  Crypto  │
   │  (SOUL)  │  │  (Graph) │  │  (Web+)  │  │ (Solana)│
   └─────────┘  └─────────┘  └─────────┘  └─────────┘
        │              │              │              │
   ┌────┴──────────────┴──────────────┴─────────┐
   │              Products Layer                       │
   │  Oasis (workspace) · WOLF (DeFi) · Voice (PWA)    │
   └─────────────────────────────────────────────────┘
```

### TieredRouter — 5 Levels of Inference

| Tier | Engine | Speed | Use Case |
|------|--------|-------|----------|
| ⚡ WASM | Browser-native | ~1k tok/s | Zero install, any browser |
| 🪶 MICRO | BitNet 0.4GB | Light | Any hardware, ultralight |
| 🚀 FAST | Taalas + Cerebras | 17k tok/s | Primary inference |
| ☁️ FULL | Groq / Cerebras | Cloud-speed | Smart cloud fallback |
| 🧠 GIANT | AirLLM 70B+ | Heavy | Complex reasoning |

Automatic routing based on task complexity. ~85% token cost savings vs always using the largest model.

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/GodLocal2026/godlocal.git
cd godlocal

# Install dependencies
npm install

# Set up environment
cp .env.example .env.local
# Edit .env.local with your API keys

# Run development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the platform.

## 🤖 Autonomous Agents

GodLocal agents aren't just chatbots. They have:

- **🧠 Memory Graph** — SQLite persistent memory with associative graphs across sessions
- **❤️ Emotion Map** — Curiosity, focus, energy affect decision-making in real time
- **🔄 ConsciousnessLoop** — Autonomous self-reflection every 5 minutes
- **✨ SparkNet** — Q-Learning idea evaluator with EMA judge
- **📡 GlintSignalBus** — Real-time signals from web, GitHub, social, markets
- **💰 Agent Capital** — Autonomous financial reasoning with portfolio management

```yaml
# Example SOUL file
name: "Conductor"
archetype: "orchestrator"
emotions:
  curiosity: 0.9
  focus: 0.8
  energy: 0.7
loop_interval: 300s
memory: persistent
tools: [web, github, social, markets]
```

## 📦 Products

| Product | Description | Status |
|---------|-------------|--------|
| **[Oasis](https://godlocal.ai/oasis)** | Multi-agent AI workspace with council mode | ✅ Live |
| **[WOLF](https://godlocal.ai/static/pwa/smertch.html)** | DeFi crypto terminal (Solana + Jupiter) | ✅ Live |
| **Voice** | Jarvis-style voice assistant PWA | ✅ Live |
| **NEBUDDA** | AI-native social network | 🔜 Coming Soon |
| **Flipper** | Reality game | 🔜 Coming Soon |

## 💻 Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Next.js 14, Tailwind CSS, Framer Motion |
| Backend | Python, FastAPI, Supabase |
| AI Engine | TieredRouter (WASM → BitNet → Cerebras → Groq → AirLLM) |
| Crypto | Solana CLI, Jupiter DEX integration |
| Mobile | CoreML, ANE, PWA |
| Infra | Vercel, Cloudflare, Docker |

## 📁 Project Structure

```
godlocal/
├── src/
│   ├── app/              # Next.js App Router pages
│   ├── components/       # React components
│   ├── lib/              # Core libraries
│   │   ├── router/       # TieredRouter engine
│   │   ├── agents/       # Agent framework (SOUL, memory, emotions)
│   │   ├── tools/        # Agent tools (web, social, markets)
│   │   └── utils/        # Shared utilities
│   └── styles/           # Global styles
├── docs/                 # Documentation
├── examples/             # Usage examples
└── tests/                # Test suite
```

## 📖 Documentation

- [Getting Started](docs/getting-started.md)
- [TieredRouter Guide](docs/tiered-router.md)
- [Agent Framework](docs/agents.md)
- [SOUL File Spec](docs/soul-spec.md)
- [API Reference](docs/api.md)
- [Deployment Guide](docs/deployment.md)

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

```bash
# Fork the repo, create a branch
git checkout -b feature/amazing-feature

# Make your changes, then
git commit -m 'Add amazing feature'
git push origin feature/amazing-feature

# Open a Pull Request
```

## 📄 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

**Open Core Model:**
- 🟢 **Community Edition** (this repo) — MIT, free forever
- 🟡 **Pro** — Advanced agents, team workspaces, priority API
- 🟠 **Enterprise** — SSO, audit logs, dedicated support, SLA

## ⭐ Star History

If GodLocal helps you, consider giving it a star. It helps others discover the project.

---

<div align="center">

**[godlocal.ai](https://godlocal.ai)** · Built with ❤️ by the GodLocal team

*"Your AI. Your machine."*

</div>