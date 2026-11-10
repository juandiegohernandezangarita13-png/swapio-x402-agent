# ⚡ Swap.io x402 Autonomous Agent Client & Live Demo

> **Superteam Earn Bounty Submission:** Make a video about our x402 Feature with Swap.io  
> **Prize Pool:** $500 USDC (1st: $200, 2nd: $125, 3rd: $80 + 30% code demo bonus)  
> **Developer:** Juan Diego Hernandez ([@juandiegohernandezangarita13-png](https://github.com/juandiegohernandezangarita13-png))  
> **Settlement Wallet (EVM / Base / USDC):** `0xc49a22a14b02189c5fd640809c5800ca5168be9e`  

---

## 🚀 Overview

Autonomous AI trading agents and DeFi bots face a fundamental bottleneck when using Web2 financial APIs:
* **Forced monthly subscriptions** ($100–$500/mo) regardless of whether the agent executes 1 trade or 10,000.
* **Credit card KYC friction** that autonomous code cannot navigate.
* **Leaked static API keys** leading to catastrophic drained accounts.

**Swap.io's x402 protocol** completely solves this by enabling native, machine-to-machine **pay-per-query liquidity routing on Solana**. 

---

## 🔄 The x402 Execution Loop

```
1. Agent queries quote  --->  GET https://hermes.swap.io/v1/quote
2. Gateway returns challenge <---  HTTP 402 Payment Required (0.0001 USDC)
3. Agent settles on Solana  --->  Broadcasts micro-transaction (<400ms finality)
4. Gateway unlocks route <---  HTTP 200 OK (Executable Raydium/Jupiter route)
```

---

## 💻 Repository Contents

1. **[`demo.html`](./demo.html):** Interactive dark-mode Web3 architecture simulator running a real-time terminal simulation of the HTTP 402 handshake.
2. **[`agent_client.py`](./agent_client.py):** Production-ready Python client demonstrating the autonomous HTTP 402 challenge negotiation loop with Swap.io's Hermes API.
3. **[`PITCH_SCRIPT_X402.md`](./PITCH_SCRIPT_X402.md):** 90-second technical pitch script & storyboard.
4. **[`SUBMISSION_X_AND_EARN.md`](./SUBMISSION_X_AND_EARN.md):** Complete 5-tweet submission thread for Twitter/X tagging `@swapdotio` and `@Superteam`.

---

## 🛠️ Quickstart

Run the client simulation locally:

```bash
python agent_client.py
```

Open `demo.html` in any web browser to view the interactive live terminal simulator.
