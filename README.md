# ◊ fall-substrate · the cognitive substrate

> **Research-question → sovereign tool · in one pipeline.**
> The flagship of the 7-product Sovereign Cognitive Substrate.
> Prime 389 · κ=1 · MIT.

**Live:** [sjgant80-hub.github.io/fall-substrate](https://sjgant80-hub.github.io/fall-substrate/)
**Doctrine:** [`SOVEREIGN-COGNITIVE-SUBSTRATE.md`](./SOVEREIGN-COGNITIVE-SUBSTRATE.md)

---

## For users · what this is

Ask a question. Get a cited sovereign HTML tool that answers it. Live on GitHub Pages. Cited from real research. In one pipeline.

The site runs a live, scripted demo that walks the full 6-phase pipeline so you can see exactly what happens before you point a real Anthropic key at it:

1. **Research** — 5-angle search fan-out · fetch sources · extract claims · 3-vote adversarial verification panel
2. **Spec** — confirmed findings become an evidence-graded feature spec (refuted features get cut)
3. **Generate** — sovereign single-file HTML, feature-by-feature, using estate patterns
4. **Verify** — fall-verify checks the output against the spec
5. **Ship** — repo create · push · Pages enable · poll until HTTP 200
6. **Audit** — every step signed via Konomi Ed25519 · prevHash → questionHash → specHash → toolHash

The demo on the landing page is pre-baked (no API call) so anyone can see the pipeline run from a cold start. Generated HTML is real and downloadable.

### Three tiers

| Tier | Cost | What you get |
|---|---|---|
| **Free** | £0 | 1 build/month · ≤20KB output · branded footer |
| **Sovereign** | MIT | Unlimited, self-hosted · BYO Anthropic key · zero phone-home |
| **Pro** | £99/mo | Multi-tenant · auto-push to your GitHub · Ed25519 audit-export |

Sovereign is the recommended tier for individuals. Fork this repo, drop in your key, never look back.

### Quickstart (sovereign, on your own GitHub)

```bash
gh repo fork sjgant80-hub/fall-substrate --clone
cd fall-substrate
# Open index.html locally — works from file://
# Paste your Anthropic key into the Config panel (stored in IndexedDB · never sent to a server)
# Click "Run live demo" to see the pipeline
```

To deploy your own copy on Pages:

```bash
gh repo create your-org/fall-substrate --public --source=. --homepage=https://your-org.github.io/fall-substrate/
git push -u origin main
gh api -X POST repos/your-org/fall-substrate/pages -f 'source[branch]=main' -f 'source[path]=/'
```

---

## For developers · architecture

### File map

```
fall-substrate/
├── index.html                            (~28KB · landing + demo · vanilla JS, no build)
├── SOVEREIGN-COGNITIVE-SUBSTRATE.md      (the canonical doctrine · v1.0)
├── README.md                             (you are here)
├── LICENSE                               (MIT · Simon Gant 2026)
└── .nojekyll                             (Pages doesn't Jekyll-process)
```

### Doctrine constraints (non-negotiable)

- **Single HTML file** · sovereign · works from `file://`
- **<400KB** target · vanilla JS only · no frameworks, no build step
- **IndexedDB** primary persistence (settings · builds · audit) · localStorage fallback
- **No phone-home** · no analytics · no telemetry
- **Luxury brutalist palette** · `--ox #8b1a1a` · `--brass #b8974a` · `--cream #c4bfb2` · `--void #0b0a0f` · `--gold #d4a853`
- **Phase colours** · research `--brass` · spec `--c87e3a` · generate `--gold` · verify `--4a8a4a` · ship `--ox` · audit `--6f6b78`
- **Fonts** · Libre Baskerville · Syne · DM Mono · DM Sans
- **PWA manifest** · baked via `data:` URL · Add-to-Home-Screen works
- **Konomi licence shim** · dead-file-until-activated · 3 tiers · sovereign default
- **fall-signal hook** · `BroadcastChannel('fall-signal')` · prime 389 · emits `substrate_build_started`, `substrate_build_complete`, `substrate_loaded`
- **BYO Anthropic key** · password input · IndexedDB only · never sent to any server
- The architecture doctrine (`SOVEREIGN-COGNITIVE-SUBSTRATE.md`) is committed alongside the code · served at `/SOVEREIGN-COGNITIVE-SUBSTRATE.md` on Pages

### The pipeline

```
question  →  fall-raas (research)
              ├─ 5-angle fan-out
              ├─ source fetch (browser)
              ├─ claim extraction
              └─ 3-vote adversarial verification

confirmed → fall-substrate (spec)
              ├─ evidence-graded features
              └─ refuted features cut

spec      →  fallcore-factory (generate)
              ├─ HTML shell · estate palette
              ├─ feature-by-feature
              ├─ Konomi shim + fall-signal hook
              └─ minify + PWA manifest

output    →  fall-verify (verify)
              ├─ feature-presence sweep
              └─ adversarial 3-vote per claimed feature

verdict   →  ship (gh CLI)
              ├─ gh repo create
              ├─ git push
              ├─ POST /pages
              └─ poll until HTTP 200

audit     →  Konomi Ed25519 sign
              prevHash → questionHash → specHash → toolHash → configVer
```

### The 7-product substrate (this is the flagship)

| Prime | Product | One-sentence |
|---|---|---|
| **389** | **fall-substrate** | research-question → sovereign tool (this repo) |
| 397 | fall-raas | research-as-a-service · 5-angle fan-out |
| 401 | fall-verify | adversarial verification · 3-vote panel |
| 409 | fall-cogmesh | 343 specialist subagent streams · vote to consensus |
| 419 | fall-rcube | 15,700× empirical speedup · high-dim search |
| 421 | fall-sdk | universal SDK · TS/Py/Rust · BYO keys |
| 431 | fall-mcp² | MCP server · every substrate cap as native LLM tool |

Read [`SOVEREIGN-COGNITIVE-SUBSTRATE.md`](./SOVEREIGN-COGNITIVE-SUBSTRATE.md) for the full doctrine.

### fall-signal events emitted

| Kind | When | Payload |
|---|---|---|
| `substrate_loaded` | page load | `{ prime: 389, ts }` |
| `substrate_build_started` | demo run begins | `{ question (truncated 80) }` |
| `substrate_build_complete` | demo run ends | `{ question, sizeKB, confirmed, refuted, auditHash }` |

Any sister tool listening on `BroadcastChannel('fall-signal')` will hear these.

### Konomi licence tiers

The shim is baked into `index.html` (~50 lines). Default tier is **sovereign** — unlimited self-hosted, MIT, no gate. To switch programmatically in console:

```js
await Konomi.activate('sovereign');   // or 'free' or 'pro'
const t = await Konomi.current();
```

Pro-tier activation in production requires a signed licence file (Ed25519). The shim verifies signatures locally — no server check.

### Live demo · pre-baked scenario

The demo on the landing is a scripted scenario (UK Section 21 landlord compliance tracker) with realistic streaming timings:

- Phase 1 Research · 8s · 5 angles → 23 sources → 9 confirmed / 4 refuted
- Phase 2 Spec · 4s · 11 features, 2 cuts (insurance, Section 21 still-issuable)
- Phase 3 Generate · 12s · 11/11 features implemented · 4.8KB
- Phase 4 Verify · 5s · 32/33 panel votes confirm (97%)
- Phase 5 Ship · 3s · live at fake URL in 47s
- Phase 6 Audit · 1.5s · Ed25519 chain signed

The generated HTML is real (~5KB, fully working `FallSection21` tool) and downloadable. To run an unscripted build against a different question, paste your Anthropic key into the Config panel and a future build of this repo will run the real pipeline (currently the demo is the only path).

### Pages deployment · estate pattern

This repo follows the standard estate Pages pattern. Don't reinvent.

```
1. .nojekyll at repo root         — Pages skips Jekyll processing
2. Source: legacy · branch=main · path=/
3. gh api -X POST repos/{org}/{repo}/pages -f 'source[branch]=main' -f 'source[path]=/'
4. Poll https://{org}.github.io/{repo}/ until HTTP 200 (60-180s)
```

No GitHub Actions workflow needed. The `.nojekyll` is the entire trick.

---

## Provenance

- Workflow architecture · Claude Code Agent SDK
- Sovereign single-file pattern · across 80 tools in Simon's estate
- Konomi Ed25519 audit chain · Simon Gant
- Adversarial verification pattern · this session's deep-research run · empirical 52% kill rate on plausible claims
- RCNESTED 15,700× verified · CASSIE v20.2 · Gant + Moore + Hohman

## Licence

MIT · Simon Gant · 2026 · the substrate is the destination.
