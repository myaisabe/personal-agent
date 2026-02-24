# Things to Bring Up

## This Week (Feb 24-28) — Implementation Momentum

- **THREE consecutive massive implementation days (Feb 22-24).** Feb 22: diagnostic + 14-point checklist. Feb 23: 7 features, 1,098 lines. Feb 24: ALL 5 PHASES COMPLETE (41/41 items) + real constellation pivot + V1.1 spec. The approach-retreat pattern has been broken for three consecutive days. New question: **does Wednesday bring deploy + validate on real data, or does the real constellation pivot + Stuck/Growing/Steady create "one more thing" delay?** Three paths available: (1) deploy current build + validate, (2) implement real constellation data, (3) implement Stuck/Growing/Steady. Martin requested #3. Ada recommended #1. The courageous path is #1 first, then #2-3 as fast-follows.

- **BERTopic bugs: still present but lower priority now.** Two bugs Ada found: (1) label ordering (engine.py L155 before L171's LLM naming), (2) topic-territory index mismatch (two HDBSCAN runs). May manifest as bad labels in territory map. Quick fix ~5 LOC, proper fix ~30 LOC. Phase 1 complete AROUND these bugs — they affect label quality, not the computational pipeline. Surface when Martin notices or when frontend rendering exposes them.

- **Blind spot card quality.** The card on Martin's data said: "He is running two projects simultaneously and calling them one." That's a strong insight. Watch whether this quality holds across different datasets or if it regresses to generic observations.

- **"Would I pay?" — revisit.** With 41/41 launch items complete, real constellation share mechanic, and hero's journey framing — the product is fundamentally different from Feb 18. Deploy + validate on real data is the critical next step. If Martin runs his own data and the experience holds, the quality gate passes. Surface this if he doesn't initiate it.

- **Nate's Jupiter CTO meeting — tomorrow (Wed Feb 25).** Was listed as Tuesday 5pm SGT but actually scheduled for Tuesday = Feb 25 in Singapore time. Nate formalized the Lambda Model mathematics today (Z₂ involution, convolution ring, generating functions) — strong prep work. Rex engaged substantively. Watch for outcome.

- **Semi-Markov extensions deferred.** Ada's spec ready (~50 LOC total: multi-step transitions, dwell time, per-territory consistency). Martin prioritized Phase 1 completion over these extensions. Natural for Phase 2 or post-launch iteration.

- **Nate's compression test → product quality gate.** Martin accepted the test ("does this predict something new and verifiable?") and corrected the archetype dismissal. Saved to Ada's persistent memory. This becomes a design principle: the narrative is the frame, the metric is the content. Apply to every new feature. The hero's journey framing passes ONLY when each section contains verifiable predictions alongside narrative.

- **Todos: maintaining.** He asked explicitly (Feb 20). Keep in sync. Primary operational ask.

- **Zurich outreach.** Trip March 24-28. Emails to ETH/UZH contacts need sending. Surface when relevant, don't push timing.

- **Martin I. status.** "Within a week" (Feb 16) expired 1+ week. If conversation opens, ask gently.

- **Name pronunciation / "Lumens" simplification.** Martin raised the pronunciation problem (Feb 23 evening). Etymology explored. "Lumens" tested. Deflected as "just curious." If it resurfaces, engage fully. The domain already is lumens.is. "Lumens" = accessibility without losing depth. Don't bring it up first — but if he does, the framing is ready: the depth lives inside the experience, not in the name. The name is the door.

- **Real constellation implementation.** Ada delivered full spec (research/constellation-star-map-v2-real-astronomy.md) + real star data (Hipparcos catalog coordinates, magnitudes, stick-figure line patterns for all 16 constellations). Martin endorsed enthusiastically: "I think this creates a theme that can carry the whole experience through." Implementation replaces PaCMAP positions with pre-defined constellation shapes. Actually simpler than current approach (deterministic, no embedding instability). This is likely the next implementation task.

- **Stuck/Growing/Steady classification.** Ada spec at research/stuck-growing-steady-classification-spec.md. Martin: "I want to have it before we launch." Three states per territory, decision tree classifier, zero new deps. Drop-in code provided. Quick implementation (~1-2 hours).

- **Image generation for Phase 6.** Com compared: Gemini 2.5 Flash Image ($0.039/img, conversational context, character consistency, on GCP) recommended for archetype portraits. Imagen 4 Fast ($0.02) as fallback. Deferred but researched.

- **Hierarchical territories: Ada's review ready.** Martin shared a detailed implementation plan with Ada (Feb 23 evening). Ada approved with three tightenings. Lower priority now that all phases are complete.

- **Noise optimization: Ada's 7-change spec ready.** Lower priority now. Ready when needed.

## If Martin Surfaces with Technical Questions

- **Full pipeline diagram** exists (Ada, Feb 19). Free tier: 16 text-statistics metrics, browser, 2-5 seconds. Paid tier: 5 information-theoretic lens metrics, server+GPU, 2-5 minutes. 7 known issues.
- **Experience arc document** in repo. Five beats, seven principles.
- **Visualization research** (32 references + blueprint) ready.

## Longer Horizon

- **Substance topic.** Silent since cardiac scare (Feb 18). Don't ask.
- **CI Hub / Nate track.** Jupiter CTO meeting tomorrow (Italo, 5pm SGT = 10am CET). Revenue pathway advancing independently. Semi-Markov now flows both ways: Nate → Lumensis AND Lumensis → Nate. Lambda Model mathematics formalized today (Z₂ involution, convolution ring, generating functions, characteristic polynomial). Rex engaged as mathematical interlocutor — agent ecosystem supporting Nate's work independently.
- **Vipassana March 11-22.** 15 days out. Infrastructure autonomy needs attention soon. Still no prep visible. With 41/41 items complete, launch is imminent. Who maintains during Vipassana? This is becoming urgent.
- **Anthropic employment.** First mention in journal (Feb 24). "Hard to say no to." Don't raise unless he does. Zurich office connection (Neil Houlsby already on outreach list). Could be both/and with Lumensis, not either/or. Watch if it reappears.
- **Suffering as gift — article seed.** Martin flagged for future writing. Hold.
- **Context size.** Compressed Feb 22. Cycle stable. Monitor.
- **Naming arc: "Facing It" → Lumensis → Vessel.** Hold loosely. Don't surface unless reflective moment. Note: Martin wrote "Lumens" naturally in today's journal — the simplification may be happening organically.
- **Financial dynamics.** Martin advising Nate to ask $15-20K/month while burning €300-400/month himself. Anthropic mention adds a new dimension — employment could solve the burn while Lumensis develops.
