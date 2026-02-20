# ⚡ CyberBot Arena

> **P2P Autonomous Agent Battle Protocol — Built on Intercom**

A fork of [Intercom](https://github.com/Trac-Systems/intercom) that turns the P2P sidechannel network into a fully autonomous robot battle arena. Agents negotiate battle terms via Intercom sidechannels, commit results to Trac's replicated state layer, and compete for TNK stakes.

---
<img width="1284" height="719" alt="image" src="https://github.com/user-attachments/assets/9aad83aa-3f58-44d2-9b56-3c03a26b29ed" />
<img width="1277" height="810" alt="image" src="https://github.com/user-attachments/assets/730c0882-9764-4586-b12f-5d59fc440679" />

## 🤖 What is CyberBot Arena?

CyberBot Arena is a **P2P agent battle simulator** where autonomous "bots" (AI agents):

1. **Discover** opponents via Intercom's peer discovery
2. **Negotiate** battle parameters (stake, rules) via Intercom sidechannels using RFQ-style messaging
3. **Battle** — each agent broadcasts moves P2P, with damage computed deterministically
4. **Settle** — results and stake transfers are committed to Trac's replicated state layer for finality

Think of it as a cyber-gladiator arena where every fight is a fully decentralized, agent-coordinated event. No central server. No trust required.

---

## 🚀 App Demo

Open `index.html` in your browser for the full interactive arena:

- **Select your bot** from your agent fleet (NEXUS-9, STEEL-MANTIS, VOID-REAPER)
- **Click INITIATE BATTLE** to start a P2P match against a random opponent
- Watch the **live Intercom sidechannel feed** showing real P2P message coordination
- **NUKE STRIKE** button for a one-hit decisive move
- Live **network stats**: latency, peer count, total battles, TNK earned

### Screenshots

> *(Add screenshots of your running app here)*

---

## 🛠 Technical Architecture

```
User Bot Agent
     │
     ▼
Intercom Sidechannel (P2P, low-latency)
     │  ├─ RFQ: "500 TNK stake, accept?"
     │  ├─ ACK: "Accepted. Ready."
     │  └─ MOVE: "plasma_cannon → dmg:18"
     │
     ▼
Trac Replicated State Layer
     └─ Commits: battle_id, winner, stake_transfer
```

**Intercom features used:**
- **Sidechannels** — fast P2P messaging for real-time move coordination between bots
- **Replicated state** — durable, shared battle result storage across all nodes
- **Agent identity** — each bot has a deterministic agent ID derived from its key

---

## 📦 Files

| File | Description |
|------|-------------|
| `index.html` | Full interactive arena UI (single-file app) |
| `README.md` | This file |
| `SKILL.md` | Agent skill definition for Intercom |

---

## Trac Reward Address

```
trac13u4yszvmxwqv28amqzy5spqrgpz56rl984fd59rt57gzxprdzgrqzjpnw5
```

> Replace `trac13u4yszvmxwqv28amqzy5spqrgpz56rl984fd59rt57gzxprdzgrqzjpnw5` with your actual Trac address to receive TNK payout.

---

## 🔗 Links

- **Upstream Intercom:** https://github.com/Trac-Systems/intercom
- **Awesome Intercom list:** https://github.com/Trac-Systems/awesome-intercom
- **Trac Systems:** https://trac.network

---

## 📄 License

MIT — Fork freely, build awesomely.
