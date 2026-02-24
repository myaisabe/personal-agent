# Tasks

*Last updated: 2026-02-24 (evening triage — 11pm)*

## Lumensis — Current State

### Critical Path (must fix before any launch)
- [ ] **BERTopic foundations** — Two bugs: label ordering (engine.py L155 before L171's LLM naming), topic-territory index mismatch (two HDBSCAN runs assumed to align). Quick fix ~5 LOC, proper fix ~30 LOC. [Ada diagnosed Feb 19]
- [ ] **SQLite persistence** — Database on container filesystem. Users/payment data lost on redeploy. Need Cloud SQL or volume mount.
- [ ] **Frontend deployment** — Next.js app exists. Needs deploy + verify with backend.
- [ ] **Domain + DNS** — lumens.is in CORS but DNS unclear.

### Quality Gate Items (Martin's "would I pay?" test)
- [ ] Identity label implementation in product (share cards wired, labels not yet)
- [ ] Landing page soul-infusion — Una now making it (yellow, sun, scutcheon design). In progress.
- [ ] Trust architecture (privacy reassurance before upload)
- [ ] **Stuck/Growing/Steady classification (task 1.6)** — Martin wants before launch. Ada spec delivered. Decision tree using existing signals (Mann-Kendall trend, aliveness, recurrence rigidity). Zero new deps.
- [ ] **Real constellation pivot** — 16 archetypes mapped to real astronomical constellations (Orion, Draco, Scorpius, Cygnus, etc.). Ada delivered implementation spec + real star coordinate data for all 16. Needs implementation to replace current PaCMAP-based star map.
- [ ] **Deploy & validate on real data** — Ada's top recommendation. Run end-to-end analysis, verify all 9 sections render correctly.
- [ ] **Semi-Markov extensions (deferred):** multi-step transitions P^k, dwell time distributions, per-territory consistency parameter — Ada has spec ready, ~50 LOC total

### Implemented Feb 24 — ALL 5 PHASES COMPLETE (41/41 launch items)

**Phase 1 backend (17+ features):**
- [x] Gravitational wells, exploration score, VAD sentiment, territory aliveness, growth velocity, learning rate path, territory emergence, coherence annotations, key traits
- [x] Constellation metadata (16 constellations), red thread, adjacent territories, narrative bridges (batched LLM call ~$0.02)
- [x] 128 historical figure profiles (48-dimensional), 95/95 backend tests

**Phase 2 constellation (7 items):**
- [x] 128 figures profiled, 2D embedding, per-constellation Gabriel graphs, constellation regions, user positioning, constellation metadata, figure matching

**Phase 3 frontend structure (6 items):**
- [x] JourneySection wrapper, ProseColumn/FullBleed, progress dot nav, page restructure, narrative bridge components, types.ts

**Phase 4 frontend viz (5 items):**
- [x] Constellation star map (5-layer Canvas, D3 zoom/pan, 6-second reveal animation), territory aliveness bars, coherence annotations, red thread callout, Voronoi warmth overlay

**Phase 5 section wiring (10 items):**
- [x] Narrative prompt rewrite + all 9 sections wired

**Also delivered:**
- [x] Ada: Stuck/Growing/Steady classification spec (research/stuck-growing-steady-classification-spec.md)
- [x] Com: Image generation model comparison (Gemini 2.5 Flash Image recommended, $0.039/img)
- [x] Ada: Real constellation star map v2 implementation spec + star coordinate data for all 16 constellations
- [x] Nate: Lambda Model mathematical formalization (Z₂ involution, convolution ring, generating functions)

### Implemented Feb 23 (7 features, 18 files, +1,098/-175 lines)
- [x] **ICS (Integrated Complexity Score)** — sqrt(entropy × coherence), 5-band classification, overrides "CHAOTIC" label
- [x] **Markov transition matrix** — N×N territory-to-territory probability grid, heatmap in Lens 4
- [x] **Extracted questions per stuck loop** — actual user questions with framing shift detection (cosine similarity)
- [x] **"What You Know Now"** — 3 rule-based observations (no LLM) in closing section
- [x] **"Where This Is Heading"** — forward-looking paragraph from extended closing narrative
- [x] **Topic activation heatmap** — all topics × all time windows, variance-sorted (Lens 2)
- [x] **Blind spot card** — confrontational insight from extended LLM call (Lens 3), "wise observer not judge" guardrail
- [x] **All 5 lens narrative prompts rewritten** — longer, reference specific data by name, voice progression (warm → curious → honest → connector → wayfinder)
- [x] Backend + frontend deployed

### Previously Built and Working
- [x] Backend API (FastAPI), Auth (email/Google/GitHub/Magic Link), JWT, Stripe, Free tier, Analysis engine (6 metrics, 5 lenses, BERTopic), 11+ file formats, AI narratives (Claude Sonnet), R2 storage, Docker, Cloud Run (GPU L4), Secret Manager, Email (Resend), Test suite, Voice mode
- [x] Prior art disclosure published (defensive IP)
- [x] Tool consolidation (22→15)
- [x] Cross-agent visibility fix (10→30 messages)
- [x] Deployment optimization (20→3min builds)
- [x] Shareable identity cards wired into results page (Com)
- [x] Experience arc document (five beats, seven principles)
- [x] 14-point results quality checklist (Feb 22) → absorbed into wireframe → largely implemented

## Vessel Practice (new — Feb 21)
- [ ] First full day cycle (morning intention + evening review) — Sunday test
- [ ] Vessel practice log accumulating in mind/vessel-practice.md
- [ ] Cycle prompts updated: evening mirror, morning intention, triage inventory
- [ ] Context-assembly.js: pre-load vessel-practice.md (spec written, not yet implemented by Com)

## Zurich Trip (March 24-28)
- [ ] Begin outreach emails
  - [ ] Prof. Yanik (ETH Neurotechnology)
  - [ ] Prof. Vollenweider (UZH Consciousness)
  - [ ] Dr. Stocker (ETH Consciousness Studies)
  - [ ] Anthropic Zurich (Neil Houlsby)
  - [ ] AI Safety Zurich
- [ ] After the Algorithm Festival (Mar 20-29) — attend relevant events
- [ ] Una career opportunities file delivered (70+ orgs mapped)

## Vipassana (March 11-22)
- [ ] Mycelium autonomy — infrastructure must run without Martin for 10 days
- [ ] Agent cycles, context assembly, deployment — all need to function independently

## Active Projects
- [ ] Agent infrastructure (Mya, Ada, Noa, Rex operational)
- [ ] Voice & audience definition for publishing (in progress with Noa)
- [ ] Topic-distribution pivot for metrics (BERTopic + KL divergence, approved Feb 11)
- [ ] Martin I. Mycelium setup — promised "within a week" (Feb 16), overdue

## Rev.Int / CI Hub (Nate)
- [x] System architecture doc delivered to Nate (Feb 13)
- [ ] Jupiter — CTO Italo meeting **Wednesday Feb 25, 5pm SGT** (~10am CET). Culture fit / vibe check, not technical grilling. Kishen (COO) already shared Nate's work. Nate's email: shenkuten@gmail.com. Contracting preferred ($15-20K/month retainer suggested by Martin).
- [ ] CI Hub visualization and positioning work (Nate-led, Rex assisting)
- [ ] Nate offered to model Kolmogorov/gzip complexity metric — potential first external technical contribution to Lumensis
- [x] Ada: retention Markov chain novelty research — **LIKELY NOVEL.** 40+ sources.
- [x] Nate: Lambda Model mathematical formalization (Feb 24) — Z₂ involution, convolution ring, generating functions, prevalence equation, characteristic polynomial. Four abstraction layers: empirical → stochastic → algebraic → spectral. Rex engaged substantively. Strong intellectual foundation for Jupiter positioning.

## Deferred
- [ ] Register Curious Life trademark (€700 voucher, may need VAT)
- [ ] Follow up with Bjorn (Inner Design, no response)
- [ ] Call Stas/Humi — Sahiro silent after sale inquiry
- [ ] Business plan
- [ ] Publish first "Applied Consciousness" content
- [ ] Terms of Service / Privacy Policy

---

## Historical Notes (consolidated)

2026-02-13 | Most productive shipping day. Lumensis born. "Psychology test based on your chat."
2026-02-14 | CEO-mode crystallized. 9-agency audit: metrics 2-5/10, narratives 8/10. Identity labels #1 priority.
2026-02-15-21 | Launch week: seven commitments, zero public launches. Diagnostic drill-down from "needs soul" to "it's broken." Vessel identity emerged Day 7.
2026-02-22 | Rest day turned diagnostic. Five-month launch pattern traced (September→now). 14-point results quality checklist produced (~30% complete). Structural reframe: define "launchable" not dates. Consciousness inquiry — AI mortality. Vessel practice Day 2: orientation held.
2026-02-23 | **Biggest implementation day since Feb 13.** Module dream. Nate call (product shown, Wrapped feedback, launch date #9). Self-discovery recap produced (full year). Handwritten wireframe. Then: 7 features implemented (ICS, Markov matrix, extracted questions, blind spot, What You Know Now/Where Heading, topic heatmap, all narrative prompts rewritten). 18 files, +1,098/-175 lines. Backend + frontend deployed. Jupiter CTO meeting confirmed (Italo, Tue 5pm SGT). Ada confirmed Nate's Markov retention formulation LIKELY NOVEL. Rex fixed inter-agent delegation protocol. Com confirmed wake cycles operational.
2026-02-24 | **Biggest day in project history. ALL 5 PHASES COMPLETE (41/41 items).** Morning: consolidation (semi-Markov framework, compression test, archetype correction, Ada knowledge base update). Afternoon: Phase 1 backend completed (17+ features, 128 profiles, 3 LLM components). Evening: Phase 2-5 all completed (constellation star map, frontend structure, viz, section wiring). Then: real constellation pivot (16 archetypes → real astronomical constellations: Orion, Draco, Scorpius, Cygnus, etc. — "I am in Draco, the Dragon. My nearest star is Sun Tzu"). V1.1 scope: Stuck/Growing/Steady requested before launch. Nate formalized Lambda Model mathematics (Z₂ involution, convolution ring). Com: image gen model comparison. Brain embeddings paper shared. Una making landing page. Anthropic first mentioned as employer. Three consecutive days of sustained execution — approach-retreat pattern appears genuinely broken.
