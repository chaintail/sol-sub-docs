# Designer Image Brief — Posts A & C

Artwork to accompany the two long-form Superteam Canada submission posts:

- **Post A — "Permissioned Pulls: Solana's New Authorization Layer for Subscriptions and Allowances"** (deep technical explainer)
- **Post C — "Canada's Stablecoin Subscription Layer: CADD, Solana Allowances, and the CAD-Native Billing Rail Nobody Has Built Yet"** (strategy memo)

Each post needs **one hero image** (top of post) plus **supporting diagrams/graphics**. Several pieces already exist in the field guide and can be reused as-is — those are marked **[REUSE]**. New pieces are marked **[NEW]**.

---

## Shared brand spec (applies to every image)

- **Aesthetic:** "field notes of a thinking machine" — hand-inked technical illustration on warm paper, like an engineer's notebook. Precise linework, not glossy. **Avoid generic crypto** (glowing 3D coins, neon, circuit-board clichés).
- **Palette (exact hex):**
  - Paper: `#faf8f3` / `#f3efe7`
  - Ink: `#211e1a` · soft ink `#58524a` · muted `#8b8478`
  - **Claude coral `#d97757`** (signature accent) · deep coral `#c05f3f` · soft coral `#e8916f`
  - **Teal `#14b8a6`** — used *sparingly*, a single "living pulse" accent only
  - Dark terminal `#0a0a0b` · warm white `#fafaf7`
- **Logo / motif:** the **"C-dot"** — an open "C" arc (warm-white or ink stroke) with a **coral dot at the opening**. Reference: the mark in the field guide (`docs/assets/claude-do-mark.svg`). The coral dot can recur as a small motif.
- **Typography (if any labels are baked in):** Inter (text) + JetBrains Mono (code/labels). **Prefer NO baked-in text** — labels are added in HTML/post layout. The one exception is a human-set share card.
- **Deliverables:** SVG where vector-capable; otherwise PNG @2x, background either transparent or matched to `#faf8f3`.
- **Consistency:** all images should feel like they belong to the same set as the field guide at https://fieldguide.claude.do — same ink-on-paper-with-coral language.

### Accuracy guardrails (read before drawing anything for Post C)
- **CADD (the Canadian-dollar stablecoin) is _planned, not live_ on Solana** as of this writing. Any Canada/CADD imagery must read as a **concept/vision**, never imply a shipped integration. Text-free art handles this cleanly — do **not** draw logos of real companies (Shopify, Wealthsimple, etc.) or imply they integrated.
- **No garbled/AI-looking text inside illustrations.** If a piece needs precise labels, leave space for them to be added in layout, or hand-letter cleanly.

---

## POST A — "Permissioned Pulls"

Thesis: Solana shipped an **authorization layer** — a bounded, revocable right to *pull* funds (capped by amount, period, destination), enforced on-chain at transfer time. Mental model: a **card pre-authorization, on-chain**.

### A1 — Hero **[REUSE]**
- **Purpose:** top-of-post hero; captures "bounded pull payment" in one image.
- **Existing asset:** the bounded-pull flow illustration (`hero-pulls` in the field guide): a wallet on the left with a **metered valve**, a measured stream of coral token-dots flowing right to a recipient, passing through a **hard "cap" gate** that visibly stops anything over the limit — with one stray dot **ricocheting off the cap** (the rejected over-pull). Ink linework on warm paper, coral tokens + cap line, a single teal tick on the valve.
- **Dimensions:** wide banner, ~**2:1** (e.g. 2400×1200). A 1200×630 crop should also read well (it doubles as the social card).

### A2 — Authorization-model flow **[REUSE]**
- **Purpose:** illustrate "sign once → the program enforces every pull" (the post's *life of a $5 pull* section).
- **Existing asset:** a two-phase flow diagram — **(1 · ONCE)** Subscriber signs `subscribe()` → creates the SubscriptionAuthority + Subscription PDAs; **(2 · EACH PULL)** Merchant/puller submits `transferSubscription()` → the program validates (cap · destination · expiry · cancellation) → **pass** (PDA signs the token CPI, tokens move) or **fail** (whole transaction reverts). On-brand boxes, coral arrows, pass/fail branch.
- **Dimensions:** ~16:9 or 2:1 landscape; legible at post width.

### A3 — Accounts & PDA map **[REUSE]**
- **Purpose:** the post's "three accounts" section.
- **Existing asset:** the three PDAs and how they relate — **SubscriptionAuthority** (the signing arm), **Plan** (the merchant's immutable offer), **SubscriptionDelegation** (one subscriber's frozen terms + live counters), with the gated/snapshots/destinations relationships drawn between them.
- **Dimensions:** ~2:1 landscape.

### A4 — Cap enforcement / "rejected pull" **[REUSE]**
- **Purpose:** the post's *u64::MAX paradox / what actually stops over-pulling*.
- **Existing asset:** a cap bar — $30 already pulled against a $50/period cap — a puller submits $35, the program returns **`AmountExceedsLimit (300)`** and the whole transaction reverts (no partial pull, even for a whitelisted puller).
- **Dimensions:** ~2:1 landscape.

### A5 — Card pre-auth analogy **[NEW, optional but nice]**
- **Purpose:** visualize the post's central metaphor — a hotel card pre-authorization, but on-chain.
- **Description:** a split/before-after vignette: left, a familiar **card pre-auth** (a card + a "hold" slip, charges captured later within a limit); right, the **on-chain equivalent** (the same relationship with the card network replaced by a program — the C-dot motif standing in for the program). Ink-on-paper, coral accents. **No real card-brand logos.**
- **Dimensions:** ~2:1 or square.

---

## POST C — "Canada's Stablecoin Subscription Layer"

Thesis: two 2026 events collide — Solana shipped the **authorization half** of programmable billing, and Canada got **CADD**, a regulated CAD stablecoin. Together they sketch a **CAD-native, code-enforced subscription rail** nobody has built yet. The post's defining quality is **intellectual honesty** (a strict LIVE / ANNOUNCED / HYPOTHETICAL framing).

### C1 — Hero **[NEW]** ⭐ (highest priority new piece)
- **Purpose:** top-of-post hero; evokes "CAD-native subscriptions on Solana" as a **vision**.
- **Description:** in the same field-notes ink-and-coral style — a **CAD-denominated stablecoin coin** (a subtle maple-leaf motif on the coin face is welcome, kept tasteful and hand-drawn) entering a **subscription rail / pull mechanism** (echo the cap-gate or metered-valve language from A's hero so the two posts feel related). A single teal "pulse" accent. Conceptual and clean.
- **GUARDRAIL:** must read as a *concept*, not a live product. No real company logos. Do not imply CADD is live on Solana.
- **Dimensions:** wide banner, ~2:1 (2400×1200), plus a 1200×630-friendly composition.

### C2 — The LIVE / ANNOUNCED / HYPOTHETICAL status graphic **[NEW]** ⭐ (most shareable)
- **Purpose:** render the post's "read this before anything else" table as a punchy standalone graphic. Its honesty is the differentiator — this is the most quotable visual in C.
- **Description:** a clean three-tier status board, **color-coded**:
  - **LIVE TODAY** (use a confident green or the coral-deep) — the Solana subscriptions program on mainnet; Cantina audit; SPL/USDC support; the TS SDK.
  - **ANNOUNCED / COMING** (amber/coral-soft) — CADD itself (on Base/Ethereum/Tempo, **not** Solana); CADD-on-Solana (planned, no date); CADD's backers ≠ a Solana integration.
  - **HYPOTHETICAL** (muted ink/grey) — every integration scenario in the memo (Shopify boxes, invoicing, recurring buys, AI budgets) are constructed archetypes, not announced products.
  - Layout as three labeled rows/columns with short chips. Clean, legible labels (this one **does** carry text — set it precisely, no AI text).
- **Dimensions:** ~4:3 or 16:9; must stay legible as a single shared image.

### C3 — Three archetypes → three primitives mapping **[REUSE + light NEW labeling]**
- **Purpose:** the post's "map the right tool to the job" section.
- **Existing assets:** the three primitive illustrations from the field guide — **jar** (Fixed Allowance), **clock** (Recurring Delegation), **punch-card** (Subscription Plan). Compose them as a labeled triptych:
  - **Fixed Allowance** (jar) → *AI-agent budget / recurring buy with a hard cap*
  - **Recurring Delegation** (clock) → *contractor-invoicing / payroll-style payouts*
  - **Subscription Plan** (punch-card) → *Shopify-style subscription box / SaaS billing*
- **New work:** arrange the three squares in a row with clean labels + the Canadian use-case under each. Keep the existing square crops.
- **Dimensions:** wide ~3:1 triptych (or stacked for mobile).

### C4 — "Stripe Billing for Solana, built in Canada" closer **[NEW, optional]**
- **Purpose:** a closing visual for the post's opportunity section.
- **Description:** a small, optimistic vignette — the C-dot motif + a maple accent over a simple "billing stack" outline, suggesting an unbuilt product opportunity. Conceptual, ink-and-coral.
- **Dimensions:** ~2:1 or square.

---

## Summary checklist

| ID | Post | Image | Status |
|----|------|-------|--------|
| A1 | A | Hero — bounded-pull flow | **REUSE** (`hero-pulls`) |
| A2 | A | Authorization-model flow | **REUSE** (existing diagram) |
| A3 | A | Accounts & PDA map | **REUSE** (existing diagram) |
| A4 | A | Cap enforcement / rejected pull | **REUSE** (existing diagram) |
| A5 | A | Card pre-auth analogy | NEW (optional) |
| C1 | C | Hero — CAD-native subscriptions (vision) | **NEW** ⭐ |
| C2 | C | LIVE / ANNOUNCED / HYPOTHETICAL status graphic | **NEW** ⭐ |
| C3 | C | 3 archetypes → 3 primitives triptych | REUSE primitives + new labels |
| C4 | C | "Stripe Billing for Solana, built in Canada" | NEW (optional) |

**Minimum viable set:** A1 (hero, ready) + A2–A4 (diagrams, ready) for Post A; **C1 (hero) + C2 (status graphic)** are the two new must-haves for Post C; C3 reuses existing art.

*All existing/reusable assets live in the field guide repo under `docs/assets/art/` (https://github.com/claude-do/solana-subscriptions-field-guide). Match new work to that set.*
