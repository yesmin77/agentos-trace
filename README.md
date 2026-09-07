# AgentOS Trace

A Binance Agent OS skill that traces every step before any trade.

Most agents jump from chat to an order.
AgentOS Trace does not.

Path:

CONNECT → MARKET → ACCOUNT → SCORE → VERDICT → APPROVE → RECEIPT

## Why

I did not want another bot that talks like a trader.
I wanted to see whether Agent OS can refuse a bad request.

This skill uses official MCP:

https://agent.binance.com/mcp/agentic

It reads live market data and the agentic sub-account, scores Market / Capital / Human proof, then says NO TRADE or proposes a $10 BTCUSDT spot order. It waits for Approve.

## Setup

### A. Wire Agent OS
Claude → Customize → Connectors → Binance Agent OS.
Leave Withdrawal off.
Market + Account are enough to trace.

### B. Load the skill
Customize → Skills → create `trace`.
Paste `SKILL.md` from this repo.

### C. Prove the connector
New chat:

Read BTCUSDT from Agent OS. Do not place any order.

If the model guesses a web price, reconnect.

### D. Run the trace

Run AgentOS Trace. Do not place any order.

### E. Two passes
First pass: revenge + needed money → NO TRADE
Second pass: test + trading money → propose $10, then wait.
Do not type Approve unless you want a live $10 spot order.

## Scoring
Each proof 0-2. Total under 4 = NO TRADE. Total 4+ = propose $10.

## Disclaimer
Not financial advice. Control demo for the Binance Agent OS Mini Hackathon.
