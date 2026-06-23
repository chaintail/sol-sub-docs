# X Thread — Post C ("Canada's Stablecoin Subscription Layer")

**How to use:** copy each tweet block below into X, one per tweet, in order. Attach the suggested image (in this repo) where noted. The final tweet links to the full memo. Char counts are approximate and exclude the image; links count as 23 chars on X.

**Full post (final-tweet link):** https://blog.vellum.network/posts/canada-stablecoin-subscriptions/

**Accuracy guardrails baked in:** CADD is *planned, not live* on Solana (never implies a shipped integration); the program is a standalone audited program (not a Token-2022 extension, no protocol change); no real company logos implied as integrators; the LIVE / ANNOUNCED / HYPOTHETICAL honesty is the throughline.

---

### Tweet 1 — hook  · 📎 attach `c1.png` (hero)

Two things happened in Canada in 2026 that nobody has connected yet.

Solana shipped programmable subscriptions. Canada got its own regulated stablecoin.

Together they sketch a CAD-native billing rail — enforced by code, not by a support queue.

Nobody's built it. 🧵

---

### Tweet 2 — the primitive  · _(no image)_

June 3: an audited Solana program went live that lets you sign ONCE to authorize bounded pulls from your own wallet — capped by amount, period, and destination, revocable anytime.

Not a promise. Code enforces every pull. "Cancel anytime" becomes a property of the rail.

---

### Tweet 3 — the other half + honesty  · 📎 attach `c2.png` (LIVE / ANNOUNCED / HYPOTHETICAL status graphic)

The other half: CADD — Canada's first regulated CAD stablecoin. Launched May 4, backed by Shopify, Wealthsimple, Shakepay, National Bank & ATB.

Live on Base, Ethereum, Tempo. On Solana? Planned, not live.

That gap is the whole opportunity. 👇 (what's real vs. not)

---

### Tweet 4 — connector  · 📎 attach `c3.png` (3 archetypes triptych)

Three shapes of authorization, three Canadian use cases. Match the tool to the job 👇

---

### Tweet 5 — archetype 1  · _(no image)_

1/ Subscription boxes (think Shopify).

Publish a plan once: $40/mo, immutable terms, your treasury as the locked destination. Customer signs once.

You pull monthly for a fraction of a cent — not ~3% card fees. And no card to expire = no involuntary churn.

---

### Tweet 6 — archetype 2  · _(no image)_

2/ Contractor invoicing.

Amounts vary, so not a fixed plan — a recurring delegation: "up to $6k per 30 days, expires at contract end."

Pull the real amount each cycle. Periods go down to the second, so metered usage billing works too. Pull-based settlement, not chase-based.

---

### Tweet 7 — archetype 3  · _(no image)_

3/ AI-agent budgets.

Give an agent your card, you trust the agent. Give it a fixed allowance — "up to $1,200, expires in 12 months" — and you trust the cap.

The program rejects anything over it, no matter how confused the agent gets. Spending limits for software.

---

### Tweet 8 — the honest catches  · _(no image)_

The honest catches:

• CADD isn't on Solana yet — build on USDC, eat the FX for now
• No scheduler — someone off-chain still has to fire each pull
• Open question: will CADD's Solana mint even be compatible with the program's token rules?

Stating these is the point. Most coverage won't.

---

### Tweet 9 — the opportunity  · 📎 attach `c4.png` ("Stripe Billing for Solana" closer)

Walk back through those holes — the biggest isn't a protocol problem. It's a missing company.

The billing-ops layer: crank the pulls, retry & dun, receipts from on-chain events, a dashboard. "Stripe Billing for Solana." Suspiciously well-shaped for a small Canadian team.

---

### Tweet 10 — close + link  · _(blog link renders its own card)_

The rail is live. The gap is documented in embarrassing detail. Superteam Canada funds exactly this kind of build. Nobody has claimed it.

Full deep-dive — what's live vs. announced vs. hypothetical, the three archetypes, the holes:

https://blog.vellum.network/posts/canada-stablecoin-subscriptions/

---
---

## Bonus — standalone announce tweet for Post A (Permissioned Pulls)
*Post A is an article, not a thread. One tweet for reach:*  · 📎 attach `a1.png` (hero)

New piece: **Permissioned Pulls** — Solana's new authorization layer for subscriptions & allowances.

The 3 account types, the full pull-gate sequence, the u64::MAX "unlimited approval" paradox, and an honest list of what it deliberately doesn't do.

https://blog.vellum.network/posts/permissioned-pulls/
