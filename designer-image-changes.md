# Designer Image — Change Requests

Review of the uploaded images (`a1`–`a5`, `c1`–`c4`). **4 need a change, 1 optional.** The others (**a1, a5, c1, c3**) are clean — no changes.

Each change is a **text/label edit only** — the illustrations themselves are good.

---

## 🔴 Real fixes (accuracy)

### 1. `a3.png` — Accounts & PDA map
In the **SubscriptionAuthority PDA** box (top-left), the line currently reads:

> ~~Created per (owner, program)~~

Change it to:

> **Created per (user, mint)**

**Why:** the SubscriptionAuthority PDA is derived per *(user, token-mint)* pair — seeds `["SubscriptionAuthority", user, tokenMint]`. "program" is incorrect; "owner" is ambiguous (reads as the merchant). Everything else in a3 is accurate.

### 2. `a4.png` — Cap enforcement
This shows a **per-period** cap ($50/period). The revert label currently reads:

> ~~AmountExceedsLimit (300)~~

Change it to:

> **AmountExceedsPeriodLimit (400)**

**Why:** `AMOUNT_EXCEEDS_LIMIT (300)` is the *fixed / cumulative* cap error; the *per-period* cap returns `AMOUNT_EXCEEDS_PERIOD_LIMIT (400)`. (The live field guide was already corrected to match.)

---

## 🟡 Minor

### 3. `a2.png` — Authorization-model flow
The subscriber is labeled **"(paper wallet)."** In crypto, "paper wallet" specifically means printed cold-storage keys — not the intent here.

Change to: **"wallet"** (or **"user wallet"**).

### 4. `c2.png` — LIVE / ANNOUNCED / HYPOTHETICAL status board
The memo date reads **"May 13, 2026,"** but Post C states its data is "as of **June 9, 2026**." Align the date (use **June 9, 2026**, or the publish date).

---

## ⚪ Optional

### 5. `c4.png` — "Stripe Billing for Solana, built in Canada" vision stack
Great as-is. Only if it might be shared **standalone** (outside the post), consider adding a small caption/cue like **"the opportunity — not yet built"** so it can't be read as a shipped product. C1 and C2 already establish the hypothetical framing, so this is low priority.

---

## No changes needed
`a1.png` (hero), `a5.png` (card pre-auth analogy), `c1.png` (Post C hero), `c3.png` (archetype triptych).
