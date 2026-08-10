# IDEAgent — Privacy-First, Self-Hosted AI for PyCharm

> ⚠️ **NOTICE:** This project is the official commercial platform for IDEAgent ([ideagent/IDEAgent](https://github.com/ideagent/IDEAgent)). We are not affiliated with the academic research paper or the repository hosted by declare-lab.

> **Your data never leaves your machine. You own your APIs. You own your context.**

IDEAgent is the first fully self-hosted, privacy-first AI agent system tightly integrated with PyCharm. It combines a purpose-built **MCP server**, a **RAG context engine**, and a smart **gateway** to deliver AI-powered coding assistance without any third-party data retention. All API keys are stored locally on the machines you control, and context is assembled on-device before being forwarded to your chosen AI provider.

---

## 🔒 Privacy First

- **We do not resell your APIs.** You bring your own API keys and they stay on your infrastructure.
- **No data retention on our side.** Everything runs on machines you control.
- **Context is assembled locally.** Only the context window you construct is sent to the AI provider, under _your_ agreement with that provider.
- **Data retention agreements are between API providers and end users.** IDEAgent is simply the delivery mechanism — transparent and auditable.

---

## 📦 The Five Packages

### 1. `mcp-server` — Model Context Protocol Server
The core server implementing the [Model Context Protocol](https://modelcontextprotocol.io). It exposes a well-defined API surface that IDE plugins and external tools use to query the context engine, manage tools, and orchestrate AI calls. Runs fully locally on your hardware or on a self-hosted server of your choice.

### 2. `rag-server` — Retrieval-Augmented Generation Server
A self-hosted RAG engine that indexes your codebase, documentation, and any additional knowledge sources you configure. It retrieves the most relevant context snippets for every AI request, dramatically improving answer quality without ever transmitting your full codebase to any third party.

### 3. `gateway` — Secure API Gateway
A lightweight proxy that sits between the IDE plugins and your AI provider(s). It enforces local authentication, rate limiting, and request shaping. Your API keys are stored and managed here — they are never exposed to the IDE plugins directly and never sent to any service other than the AI provider you explicitly configure.

### 4. `PyCharm IDEAgent Plugin` — JetBrains IDE Integration
The PyCharm plugin that surfaces all IDEAgent capabilities directly in the IDE. It connects to the local MCP server, streams AI responses inline, and provides code completion, refactoring suggestions, and project-aware chat — all with zero cloud dependency.

### 5. `PyCharm RAG File Watcher Plugin` — Real-Time Index Maintenance
A companion PyCharm plugin that watches your project files for changes and keeps the RAG index up to date in the background. When you save a file, rename a class, or add a module, the index is updated immediately so the AI always has the freshest view of your codebase.

---

## ⚖️ How IDEAgent Compares

| Feature | IDEAgent | Cloud-only assistants |
|---|---|---|
| API keys stored locally | ✅ | ❌ |
| Codebase stays on-device | ✅ | ❌ |
| Self-hosted RAG | ✅ | ❌ |
| Works with any LLM provider | ✅ | Limited |
| Fully offline (Ollama) | ✅ | ❌ |
| No vendor data retention | ✅ | Varies |
| PyCharm-native integration | ✅ | Partial |

---

## 🐛 Issues & Feature Requests

All five packages live in private repositories to protect implementation details. To report a bug or request a feature, please use the issue templates below — they route your report to the correct team:

- 🐛 **[Bug Report](https://github.com/ideagent/.github/issues/new?template=bug_report.yml)**
- 💡 **[Feature Request](https://github.com/ideagent/.github/issues/new?template=feature_request.yml)**
- ❓ **[Question / Support](https://github.com/ideagent/.github/issues/new?template=question.yml)**

---

## 📜 License & Contributing

Each package carries its own license. Please refer to the individual package documentation for details. Contributions, feedback, and ideas are welcome through the issue tracker above.

