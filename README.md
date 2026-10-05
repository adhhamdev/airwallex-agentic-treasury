# airwallex-agentic-treasury

**Problem**
Finance teams constantly face two linked pains:
1. Cash is short or multi-currency → which obligations to fund, convert, defer or escalate?
2. SaaS / vendor purchases need to stay within approved terms → how to enforce intent with real card controls?

**Solution**
A single-wallet agentic system built on Airwallex APIs that runs the Observe → Decide → Act → Reconcile loop:

1. Adaptive Treasury Controller
   - Continuously monitors balances, FX rates, upcoming obligations and reserve floors
   - Decides in real time: fund, convert (optimal FX), defer, or escalate to human
   - Clear policy layer + explicit human-in-the-loop for high-risk actions
   - Full audit trail of every decision and resulting transfer/conversion

2. Lightweight Intent-Bound Purchase Agent (same wallet)
   - Accepts a purchase intent (merchant, amount, category, validity window)
   - Issues / configures a virtual card with strict Airwallex controls (MCC, amount, time, currency)
   - Enforces the approved terms; rejects or escalates anything outside policy
   - Reconciles spend back into the treasury view

**Why this wins**
- Demonstrates real money movement (Global Accounts, FX, Transfers, Issuing) under realistic constraints
- Strong guardrails and escalation (the anti-pattern of “just give the LLM a card” is avoided)
- Dual value: treasury intelligence + spend control on one stack
- Highly demoable: change balance / rate / policy → agent behaves differently live
- Direct path to both open prizes and Visa-related awards via card controls

**Tech**
Airwallex sandbox (Developer MCP + REST), Claude for reasoning, explicit policy engine, virtual cards with controls, simulation endpoints for deposits/transfers/status.

**Next steps after acceptance**
Full working agent + live branching demo + short video by submission deadline.

**Status**
Idea phase - full implementation starts after acceptance.