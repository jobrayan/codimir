# Codimir — AI Context Framework (SDK, Client, CLI)

[![npm version](https://img.shields.io/npm/v/@codimir/core?color=green)](https://www.npmjs.com/package/@codimir/core)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![Docs](https://img.shields.io/badge/docs-What%20is%20Codimir-blue)](./docs/WHAT_IS_CODIMIR.md)

Codimir is the **Context Framework for AI↔AI workflows**.  
It provides a **unified SDK, client, and CLI** so you can integrate Codimir tickets, context capsules, and reference graphs directly into your apps (Next.js, Vue, Node, or anywhere else).

---

## 🚀 Installation

Codimir is published on npm under `@codimir/*`.

### Using npm
```bash
npm install @codimir/core
```

### Using yarn
```bash
yarn add @codimir/core
```

### Using pnpm
```bash
pnpm add @codimir/core
```

---

## ✨ Features

- **Context Capsules** — structured tickets with story, references, artifacts, signals  
- **Reference Graph API** — link tickets ↔ code ↔ PRs ↔ datasets ↔ tests  
- **Cross-framework support** — usable in Next.js, Vue, and Node.js environments  
- **CLI tooling** — generate, share, and sync capsules from the terminal  
- **SDK client** — interact with Codimir servers or self-hosted backends  

---

## 🧩 Usage Examples

### Next.js / React
```tsx
import { CodimirClient } from "@codimir/core";

const client = new CodimirClient({ apiKey: process.env.CODIMIR_API_KEY });

export default async function Page() {
  const ticket = await client.tickets.create({
    title: "Add AI-to-AI workflow",
    description: "Codimir should record agent handoff references",
  });
  return <pre>{JSON.stringify(ticket, null, 2)}</pre>;
}
```

### Vue
```ts
import { CodimirClient } from "@codimir/core";

const client = new CodimirClient({ apiKey: import.meta.env.VITE_CODIMIR_KEY });

client.tickets.list().then(console.log);
```

### CLI
```bash
npx codimir ticket:create "Fix failing E2E tests"
```

---

## 📌 To-Do Roadmap

- [ ] **Semantic versioning + automated releases**  
  - Configure GitHub Actions + semantic-release to auto-publish new versions to npm  
  - Sync releases with **codimir.com** deployments  
  - Add AI bot to announce new versions in Discord channels  

- [ ] **Develop core modules**  
  - [ ] `@codimir/cli` — CLI for ticket & capsule management  
  - [ ] `@codimir/core` — SDK client for Node.js, Next.js, Vue, etc.  
  - [ ] `@codimir/react` — React hooks & providers  
  - [ ] `@codimir/vue` — Vue composables  

- [ ] **Integration with Codimir Cloud**  
  - Ensure OSS packages stay aligned with hosted services on [codimir.com](https://codimir.com)  

- [ ] **Context Graph extensions**  
  - Add adapters for GitHub, Jira, Slack, and ChatGPT plugin ecosystem  

---

## 📖 Documentation

- [What is Codimir?](./docs/WHAT_IS_CODIMIR.md) — overview of context framework  
- [API Reference](./docs/API.md) — SDK + CLI usage docs (coming soon)  
- [Contributing](./docs/CONTRIBUTING.md) — guidelines for contributors  

---

## 🤖 Release Workflow

- **Semantic Release** — automatically version & publish to npm registry  
- **Discord Bot** — notifies channels when new versions go live  
- **CI/CD** — GitHub Actions test, lint, build, and release pipeline  

---

## 📜 License

Codimir is open-source under the [MIT license](./LICENSE).  
© 2025 Jobrayan, Inc. All rights reserved.

---

> **Codimir**: the missing context layer that makes AI not just an autocomplete, but a true collaborator.
