# Vijevira

Independent software projects — real-time multiplayer games, peer-to-peer tools, and self-hosted SaaS.

Everything here is live and deployed. No demos, no screenshots-only repos.

---

## Projects

| Project | What it is | Live |
|---|---|---|
| **Zyvora** | Jira-like project management — Kanban, sprints, timeline, multi-tenant RBAC, real-time collaboration | [zyvora.endra.in](https://zyvora.endra.in) |
| **WatchTower** | Monitors pages, RSS feeds, and JSON APIs; delivers to Discord, Slack, and Telegram via a 3-stage job pipeline | [watchtower.wasmer.app](https://watchtower.wasmer.app) |
| **BlindShare** | Zero-persistence P2P sharing — files, text, code, secrets, view-once media, screen share. Nothing touches a server | [blindshare.in](https://blindshare.in) |
| **BlindParty** | P2P watch party, video call, and group chat over a full WebRTC mesh | [party.blindshare.in](https://party.blindshare.in) |
| **Chhakkadi** | Real-time platform for 3 Indian trick-taking card games, with bot AI and an Android build | [chhakkadi.endra.in](https://chhakkadi.endra.in) |
| **Cabo** | Multiplayer Cabo card game, 2–15 players, edge-native | [cabo.endra.in](https://cabo.endra.in) |
| **Cuff the Bluff** | Liar's Dice for up to 15 players with probability-based bot AI | [cuffthebluff.endra.in](https://cuffthebluff.endra.in) |
| **Splendor** | Full Splendor board game, 2–12 players, procedural SVG art and synthesized audio — zero external assets | [splendor.endra.in](https://splendor.endra.in) |

---

## How These Are Built

Most projects here share a few common choices:

- **Edge-native multiplayer** — one Cloudflare Durable Object per game room, holding stateful WebSocket connections at the edge with no database to operate.
- **Peer-to-peer where it matters** — BlindShare and BlindParty move data directly between browsers over WebRTC, so payloads never reach a server.
- **Job queues over cron loops** — BullMQ pipelines with staged workers, backoff retries, and per-attempt delivery logs.
- **TypeScript throughout**, with React and Vite on the frontend, Node.js and Fastify on the backend, PostgreSQL and Redis for state.

---

## About

Maintained by Vijendra Kumar.

[vijevira.in](https://vijevira.in) · [LinkedIn](https://www.linkedin.com/in/vijevira) · [vijevira@engineer.com](mailto:vijevira@engineer.com)
