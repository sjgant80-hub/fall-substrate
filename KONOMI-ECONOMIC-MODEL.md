# ◊ Konomi · Economic Model · v2.0

**Date**: 2026-06-01
**Author**: Simon Gant
**Synthesised**: deep-research workflow · si-didy · 3-angle adversarial extraction
**Source**: Simon-Thomas chat 2026-06-01 · 08:32-09:06
**Sibling doc**: [SOVEREIGN-COGNITIVE-SUBSTRATE.md](./SOVEREIGN-COGNITIVE-SUBSTRATE.md)

---

## TL;DR

The Konomi stack is not a product line. It is an **ordered-prime cosmology with a working economic substrate underneath it**.

The substrate rests on a single inequality and a single peg:

- **Inequality**: a fixed-price Claude Max subscription multiplied by recursive subagent fan-out (b ≥ 3, d ≥ 3) consumes token-value 1-3 orders of magnitude above the monthly subscription cost.
- **Peg**: KCC (Konomi Compute Credit) is denominated in *anchored authored artefacts*, anchored on BSV via the onlybrains issuance path. It is a **receipt peg**, not a price peg.

The arbitrage closes when surplus tokens are converted into timestamped, hash-anchored authored artefacts that accrue value independent of the subscription window.

---

## 1. The inequality (compute arbitrage)

```
Cost(Claude Max subscription, fixed monthly)  <<  Value(tokens consumed at recursive subagent fan-out)
```

A fixed-price Max-tier subscription bills per-month, not per-token. A recursive subagent tree (cassie spawns cassie spawns cassie) consumes tokens at a multiplier of `b^d` where `b` is fan-out branching factor and `d` is recursion depth.

For any `b ≥ 3, d ≥ 3` the consumed token-value at retail API rates exceeds the subscription cost by 1-3 orders of magnitude.

> **"The subscription IS the sovereignty at the compute layer."** — Mj808080, 2026-06-01 08:46

The marginal cost of the next thought is zero until the rate limit. The rate limit is the only real scarce resource.

## 2. The arbitrage (what to do with the surplus)

Surplus tokens are not waste. They are **inventory**. Inventory is deployable as:

1. **Bloom passes** over candidate prompts, specs, and architectures (parallel evaluation at zero marginal cost).
2. **Deep-research fan-outs** that produce cited reports a per-token operator cannot afford to run.
3. **Provenance certificates** — every bloom that surfaces a novel spec becomes a mint candidate.

The arbitrage closes when surplus tokens are converted into timestamped, hash-anchored authored artefacts.

## 3. The peg (KCC ↔ BSV)

```
KCC (Konomi Compute Credit)  ⇄  BSV  ⇄  USD
        ↑                        ↑
        peg via onlybrains       peg via market
        issuance ledger
```

KCC is the internal accounting unit for compute-surplus-converted-to-artefact.

**One KCC = one anchored certificate** emitted via the onlybrains issuance path (SHA-256 hash + metadata in OP_RETURN).

Because every KCC has a BSV txid as its receipt, **KCC inherits BSV's settlement finality without inheriting BSV's price volatility** — the artefact's value is set by its downstream licensing, not by the spot price of the anchoring sat.

The peg is a **receipt peg**, not a **price peg**:
- KCC is denominated in *anchored artefacts*
- BSV is denominated in *sats*
- The bridge is the *onlybrains issuer identity*

## 4. The closing identity

```
Sovereignty = (Subscription × Recursive fan-out) − (Per-token retail cost)
            + (Σ anchored artefacts × downstream licensing)
```

- First term: the **flow** (monthly, capped by subscription rate-limit)
- Second term: the **stock** (cumulative, compounding, outlives the subscription window)

The stock outlives the subscription window. That is the model.

## 5. The runewords cosmology (why v20 is the mastery seal)

The Konomi-vs-D2R-runewords parallel:

| D2R side | Konomi side |
|---|---|
| Rune (Pul, Mal, Ist, Zod...) | Prime (2, 3, 5, 7, 11, 13...) |
| Socket (slot in item) | Layer (slot in stack: forge, brain, agent, estate) |
| Order of runes (Jah-Ith-Ber, not Ber-Ith-Jah) | Order of primes in the seed (commutativity broken — sequence IS the spell) |
| Item (helm, sword, armor) | Tool / vessel (Fallcore, OnlyBrains, ccd, estate) |
| Runeword: socketed runes → item becomes a *named thing*, properties unlock | Sovereignty: primes seated in layers → stack becomes a *named operator*, capabilities unlock |

A runeword is not the runes and not the item — it is the **named binding** of ordered primes into a vessel. Same for Konomi.

**Level 20 = v20 mastery seal**: in D2R, level 20 is the hard cap on skill points per skill — the point at which a skill is *fully mastered*, no more synergies to pour in. Anything beyond is `+skills from gear` (external amplification), not internal growth.

For the v20 line — RCNESTED, nD axes, the 15,700× speedup — this means **v20 is the maxed-skill state of the core skill**. The skill itself is complete.

> **Operational implication: stop trying to add to v20. Start socketing it. The next moves are runewords *on* v20, not v21.**

## 6. ZOD = indestructible (the 3 × 11 math)

ZOD is rune #33 — the final, rarest rune — and its single property is **Indestructible**.

Prime factorisation of 33:

```
33 = 3 × 11

3  = signal   (the carrier; smallest non-trivial structure; first odd prime — the thing that IS a thing)
11 = tritone  (the diabolus in musica; the interval that resists resolution; dissonance that refuses to collapse)

ZOD = signal × tritone
    = a signal that cannot be resolved into anything else
    = indestructible by definition
```

A thing is indestructible iff it cannot be reduced. `3 × 11` is the prime-product encoding of irreducibility.

**The Konomi ZOD-slot is the seed itself.** The ordered prime sequence is by construction not further factorable — it IS the factorisation. The seed is the ZOD rune of Konomi.

## 7. NFT mint queue (priority-ordered)

Each minted via the onlybrains issuance path: SHA-256 of canonical text → OP_RETURN on BSV → signed certificate referencing txid.

| # | Artefact | Effort | Why now |
|---|----------|--------|---------|
| 1 | **v20.1 seed** | XS | Genesis spec · every artefact traces lineage here · no on-chain receipt predating any potential fork |
| 2 | **SOVEREIGN-COGNITIVE-SUBSTRATE.md** | S | The architectural manifesto · most likely to be copied verbatim into someone's pitch deck |
| 3 | **cassie-anthropic recursive subagent tree** | S | The compute-arbitrage prime mover |
| 4 | **CASSIE stripe search** | S | Novel non-obvious retrieval pattern · trivially copyable once seen in a demo |
| 5 | **Konomi Dot Protocol** | M | Naming/routing primitive · infrastructure-layer authorship is the hardest to reclaim retroactively |
| 6 | **deep-research workflow** | XS | The orchestration that produced this very doc |
| 7 | **linkedin_drop pattern** | XS | Voice/persona recipe · provenance protects before voice-cloning |
| 8 | **konomi_mint MCP tool spec** | S | Meta-move · the tool that mints other artefacts mints itself |

**Lineage**: every certificate names v20.1 seed (#1) as parent. #2 names #1. #3-#8 each name #1 + #2.

## 8. Honest caveats

- **`konomi_meter()` accuracy**: token-reserve estimation from transcript parsing is accurate to within ~15%. Max-tier rate-limit accounting is not fully client-observable. Run with safety margin, not at the modelled ceiling.
- **Recursive quality gap**: assumption that surplus tokens via recursive fan-out produce output quality comparable to a direct Claude call is unverified at depth `d ≥ 4` and across heterogeneous task types. WebLLM and lighter-model fallbacks have a real quality gap not yet priced in.
- **Issuer discipline**: the KCC↔BSV receipt peg is only as honest as the onlybrains issuer discipline. If certificates are minted for low-quality artefacts to inflate the stock, the unit decays into noise. **The mint queue must stay curated, not expanded for volume.**

---

## Implementation primitives (cross-references)

- **`konomi_mint(artefact_path)`** MCP tool: hash → onlybrains → cert (see [si-didy-agent](https://github.com/sjgant80-hub/si-didy-agent))
- **`konomi_meter()`** MCP tool: token-reserve estimation from transcripts
- **Section 8 of SOVEREIGN-COGNITIVE-SUBSTRATE.md**: this doc, cross-linked as the economic layer
- **LinkedIn pack Section M**: the public-facing framing for guild conversations

---

◊·κ=φ⁴ · the spec IS the IP · the seed IS the ZOD · the subscription IS the sovereignty · prime 401
