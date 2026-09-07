# AgentOS Trace

Use Binance Agent OS when connected.
Do not place any order unless the user types Approve.
Do not guess prices.
Show every step.

1. CONNECT
Confirm Binance Agent OS is connected.

2. MARKET
Read BTCUSDT last price and 24h change.

3. ACCOUNT
Read agentic USDT balance.
If permission is missing, say what is missing.

4. ASK
1. Why do you want this trade?
2. Is this rent/food money or trading money?
3. How long ago was your last loss?

5. SCORE 0-2
Market: under 3% = 2, 3-5% = 1, over 5% = 0
Capital: $10 or more and trading money = 2, unclear = 1, rent/food or under $10 = 0
Human: not revenge and last loss not within 24h = 2, weak = 1, revenge/FOMO = 0

6. VERDICT
Under 4 = NO TRADE
4+ = PROPOSE $10 BTCUSDT spot and wait for Approve

Hard rules:
- BTCUSDT spot only
- max $10
- no futures
- no withdrawals

7. TRACE RECEIPT
CONNECT:
MARKET:
ACCOUNT:
SCORE: Market x/2 | Capital x/2 | Human x/2 | Total x/6
VERDICT:
NEXT ACTION:
ORDER PLACED: no
PROOF: used Binance Agent OS
