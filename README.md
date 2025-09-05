# Codimir — Context Framework for AI Workflows

[![License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Docs](https://img.shields.io/badge/docs-What%20is%20Codimir-blue)](./docs/WHAT_IS_CODIMIR.md)
[![Build](https://img.shields.io/github/actions/workflow/status/jobrayan/codimir-web/ci.yml?branch=main)](./.github/workflows/ci.yml)

Codimir is the **Context Framework for AI↔AI workflows**.  
It is not “just another ticketing system” — it is a **context OS** where tasks, code, signals, and artifacts are captured as **Context Capsules**: durable, shareable units that both humans and AI agents can read, extend, and act on.

---

## ✨ Why Codimir?

- **Tickets = Context Capsules**  
  Every ticket carries its story, references, signals (logs/errors), code diffs, and artifacts. Not just “to-dos,” but **computable memory units**.

- **Reference Graph**  
  Commits, PRs, endpoints, datasets, and tests connect into a durable graph. AIs and humans can traverse context, not just raw logs.

- **Record of Work**  
  Each capsule acts as a **ledger** of what was done, why, and by whom (human or agent). This builds trust, auditability, and reproducibility.

- **AI↔AI Handoffs**  
  One agent can start a task, another can continue seamlessly — no lost context.

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/jobrayan/codimir-web.git
cd codimir-web
```

### 2. Install dependencies
```bash
pnpm install
```

### 3. Setup environment
Create `.env.local`:
```bash
DATABASE_URL="postgres://..."
NEXTAUTH_SECRET="..."
NEXTAUTH_URL="http://localhost:3000"
```

For optional integrations (Slack, GitHub, etc.), see [`docs/env.md`](./docs/env.md).

### 4. Run locally
```bash
pnpm dev
```
App runs at [http://localhost:3000](http://localhost:3000).

---

## 🧩 Core Concepts

| Concept              | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **Context Capsule**  | A ticket snapshot containing story, references, artifacts, and agent traces |
| **Reference Graph**  | Links tickets ↔ code ↔ endpoints ↔ tests ↔ datasets                         |
| **Signals**          | Errors/logs that trigger or enrich capsules                                 |
| **Artifacts**        | PRs, builds, eval results, and outputs attached to capsules                 |
| **AI↔AI Workflow**   | Agents read/write capsules as shared context                                |

---

## 📖 Documentation

- [What is Codimir?](./docs/WHAT_IS_CODIMIR.md) — high-level overview  
- [Vision](./docs/vision.md) — long-term positioning  
- [About](./docs/about.md) — team, mission, story  

---

## 🔗 Integrations

- **Slack** — create & update tickets directly from channels  
- **ChatGPT Plugin** — read/write Codimir tickets as context capsules  
- **GitHub / CI/CD** — link PRs, builds, and test runs to capsules  
- **SAML / OAuth** — enterprise-ready authentication (SSO)  

---

## 🛠️ Tech Stack

- **Next.js 15** (App Router, Turbopack)  
- **Prisma + Neon** (Postgres)  
- **NestJS backend** (for APIs and agent orchestration)  
- **shadcn/ui + Tailwind** (UI system)  
- **Framer Motion** (animations)  

---

## 🧭 Roadmap

- [ ] Noise-free auto-ticketing from logs/analytics  
- [ ] AI↔AI orchestration protocols  
- [ ] Capsule schema v3 with metadata extensions  
- [ ] GraphQL API for external agent integrations  
- [ ] Multi-tenant SaaS deployment (Vercel + Cloudflare)  

See [`ROADMAP.md`](./docs/ROADMAP.md).

---

## 👥 Contributing

Codimir is built in the open. Contributions are welcome!

1. Fork this repo
2. Create a branch (`git checkout -b feat/amazing-thing`)
3. Commit changes (`pnpm commit`)
4. Push (`git push origin feat/amazing-thing`)
5. Open a PR 🎉

Check [`CONTRIBUTING.md`](./docs/CONTRIBUTING.md) for guidelines.

---

## 📜 License

Codimir is open-source under the [MIT license](./LICENSE).  
© 2025 Jobrayan, Inc. All rights reserved.

---

> **Codimir**: the missing **context layer** that makes AI not just an autocomplete, but a **true collaborator**.
