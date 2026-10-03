# Vijevira

Independent software projects — real-time multiplayer games, peer-to-peer tools, and self-hosted SaaS.

Everything here is live and deployed.

---

## Projects

| Project | What it is | Live |
|---|---|---|
| **[Zyvora](https://github.com/vijevira/zyvora)** | Jira-like project management — Kanban, sprints, timeline, multi-tenant RBAC, real-time collaboration | [zyvora.endra.in](https://zyvora.endra.in) |
| **[WatchTower](https://github.com/vijevira/WatchTower)** | Monitors pages, RSS feeds, and JSON APIs; delivers to Discord, Slack, and Telegram via a 3-stage job pipeline | [watchtower.endra.in](https://watchtower.endra.in) |
| **[BlindShare](https://github.com/vijevira/BlindShare)** | Zero-persistence P2P sharing — files, text, code, secrets, view-once media, screen share. Nothing touches a server | [blindshare.in](https://blindshare.in) |
| **[BlindParty](https://github.com/vijevira/BlindParty)** | P2P watch party, video call, and group chat over a full WebRTC mesh | [party.blindshare.in](https://party.blindshare.in) |
| **[BlindChat](https://github.com/vijevira/BlindChat)** | End-to-end encrypted messenger — chats, photos, voice notes, and video encrypted in the browser, with P2P voice and video calls. Android in Play Store alpha | [chat.endra.in](https://chat.endra.in) · [Play Store](https://play.google.com/store/apps/details?id=in.endra.blindchat) |
| **[CronDeck](https://github.com/vijevira/CronDeck)** | Cron-as-a-service for HTTP jobs with full execution history, uptime monitors, heartbeats, and public status pages | [crondeck.cc.cd](https://crondeck.cc.cd) |
| **[Wishly](https://github.com/vijevira/Wishly)** | Automated birthday and anniversary wishes sent from your own WhatsApp, email, Telegram, Discord, or Slack | [wishly.cc.cd](https://wishly.cc.cd) |
| **[Chhakkadi](https://github.com/vijevira/Chhakkadi)** | Real-time platform for 3 Indian trick-taking card games, with bot AI and an Android app on Google Play | [chhakkadi.endra.in](https://chhakkadi.endra.in) · [Play Store](https://play.google.com/store/apps/details?id=in.endra.chhakkadi) |
| **[Cabo](https://github.com/vijevira/carbo-card-game)** | Multiplayer Cabo card game, 2–15 players, edge-native | [cabo.endra.in](https://cabo.endra.in) |
| **[Cuff the Bluff](https://github.com/vijevira/cuff-the-bluff)** | Liar's Dice for up to 15 players with probability-based bot AI | [cuffthebluff.endra.in](https://cuffthebluff.endra.in) |
| **[Splendor](https://github.com/vijevira/Splendor)** | Full Splendor board game, 2–12 players, procedural SVG art and synthesized audio — zero external assets | [splendor.endra.in](https://splendor.endra.in) |

---

## How These Are Built

Most projects here share a few common choices:

- **Edge-native multiplayer** — one Cloudflare Durable Object per game room, holding stateful WebSocket connections at the edge with no database to operate.
- **Peer-to-peer where it matters** — BlindShare and BlindParty move data directly between browsers over WebRTC, so payloads never reach a server. BlindChat encrypts every message on the device, so its server stores only ciphertext.
- **Job queues over cron loops** — BullMQ pipelines with staged workers, backoff retries, and per-attempt delivery logs.
- **TypeScript throughout**, with React and Vite on the frontend, Node.js and Fastify on the backend, PostgreSQL and Redis for state.

---

## About

Maintained by [Vijendra Kumar](https://github.com/vijevirat).

[vijevira.in](https://vijevira.in) · [LinkedIn](https://www.linkedin.com/in/vijevira) · [vijevira@engineer.com](mailto:vijevira@engineer.com)
