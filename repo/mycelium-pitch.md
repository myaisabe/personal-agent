# Mycelium

## The Problem

Your digital life is scattered across apps. Conversations disappear.
Nobody connects what you said last week to what you need to decide today.

```
  Telegram    Discord    WhatsApp    Voice    Email
     │           │          │         │        │
     ▼           ▼          ▼         ▼        ▼
  ┌─────────────────────────────────────────────────┐
  │                    NOTHING                       │
  │                                                  │
  │   No memory. No connections. No intelligence.    │
  │   Just scattered chat logs nobody reads.         │
  └─────────────────────────────────────────────────┘
```

---

## What Mycelium Does

```
  Telegram    Discord    WhatsApp    Voice    Email
     │           │          │         │        │
     ▼           ▼          ▼         ▼        ▼
  ┌─────────────────────────────────────────────────┐
  │              MYCELIUM PIPELINE                   │
  │                                                  │
  │  1. Capture ──► every message, voice note, file  │
  │  2. Encrypt ──► per-record AES-256-GCM           │
  │  3. Tag     ──► topics, people, places, projects │
  │  4. Embed   ──► 1024D vector (semantic meaning)  │
  │  5. Store   ──► encrypted DB + vector index      │
  └──────────────────────┬──────────────────────────┘
                         │
                         ▼
  ┌─────────────────────────────────────────────────┐
  │             NIGHTLY CLUSTERING                   │
  │                                                  │
  │  UMAP + HDBSCAN on your full message history     │
  │                                                  │
  │  Result: a living map of your mind               │
  │                                                  │
  │    Realms (~7)  ──►  Themes (~30)                │
  │         │                  │                     │
  │         ▼                  ▼                     │
  │    Territories (~250)  ──►  Atoms               │
  │                                                  │
  │  Rendered as 3D landscape you can fly through    │
  └──────────────────────┬──────────────────────────┘
                         │
                         ▼
  ┌─────────────────────────────────────────────────┐
  │           AGENTS ACT ON YOUR BEHALF              │
  │                                                  │
  │  8 specialized AI agents, each with:             │
  │  - its own memory and personality                │
  │  - scoped data access (can't see everything)     │
  │  - autonomous schedules (they initiate, not you) │
  │  - ability to delegate to other agents           │
  └─────────────────────────────────────────────────┘
```

---

## The Agents

```
┌──────────┬───────────────────────────────────────────┐
│ Mya      │ Personal companion. Holds the full        │
│          │ picture — relationships, projects, moods.  │
│          │ Morning check-ins, evening reflections,    │
│          │ dream cycles. Delegates to specialists.    │
├──────────┼───────────────────────────────────────────┤
│ Ada      │ Research. Deep web research, paper review, │
│          │ competitive analysis. Spawns sub-agents    │
│          │ for parallel work.                         │
├──────────┼───────────────────────────────────────────┤
│ Apollo   │ Geopolitical intelligence. 25+ live data   │
│          │ sources. Military tracking, market signals, │
│          │ personal security assessments.             │
├──────────┼───────────────────────────────────────────┤
│ Rob      │ Wealth. Portfolio tracking, tax strategy,  │
│          │ trade execution, financial modeling.        │
├──────────┼───────────────────────────────────────────┤
│ Rex      │ Commercial intelligence. Lead scoring,     │
│          │ churn prediction, deal strategy.            │
├──────────┼───────────────────────────────────────────┤
│ Com      │ Company operator. Ships code, manages      │
│          │ infrastructure, executes product work.      │
├──────────┼───────────────────────────────────────────┤
│ Noa      │ Publishing. Long-form writing, editing,    │
│          │ content strategy.                           │
├──────────┼───────────────────────────────────────────┤
│ Māra     │ Family companion. Latvian-language agent    │
│          │ for Martin's mother. Daily news, security.  │
└──────────┴───────────────────────────────────────────┘
```

---

## Autonomous Thinking Cycles

Agents don't wait for you. They run on their own schedules:

```
  08:00  Morning    ──►  Review yesterday, send check-in
  12:00  Midday     ──►  Internal reflection (no message)
  20:00  Evening    ──►  Review today, message if meaningful
  23:00  Triage     ──►  Process day into structured docs
  03:00  Dream      ──►  Free association, pattern surfacing
  Sunday Weekly     ──►  Broader synthesis, prune stale ideas
```

The personal agent maintains a private internal model — hypotheses, observations, contradictions, questions — that evolves continuously and informs every interaction.

---

## Intelligence Sources (War Room)

```
  POLITICAL                    MILITARY
  ├─ GDELT events (100+ countries)  ├─ ADS-B flight tracking (6 theaters)
  ├─ ACLED armed conflict data      ├─ AIS vessel tracking (9 zones)
  ├─ 16 X/Twitter OSINT accounts    ├─ NASA FIRMS fire detection
  ├─ 15 Telegram OSINT channels     ├─ Israel OREF missile alerts
  ├─ 25+ RSS feeds                  └─ GPS jamming detection
  └─ YouTube analyst transcripts
                                   MARKET
  INFRASTRUCTURE                ├─ Polymarket smart-money signals
  ├─ Cloudflare internet outages ├─ Defense/energy/volatility ETFs
  ├─ GDACS disaster alerts       ├─ Market velocity (3%+ moves)
  └─ USGS earthquakes            └─ Calendar events
```

Synthesized into:
- **Country Instability Index** (0-100, 8 weighted components)
- **Narrative threads** (events clustered into ongoing storylines)
- **Convergence detection** (multiple sources → one signal)
- **Actor graph** (countries, people, institutions + relationships)

---

## Architecture

```
  ┌─────────────────────────────────────────────────┐
  │            LUMENSIS — Measurement                │
  │                                                  │
  │  How is this mind changing over time?            │
  │  Learning rate, coherence, compression,          │
  │  attention distribution, phase transitions.      │
  │                                                  │
  │  FastAPI + GPU                                   │
  └─────────────────────────────────────────────────┘
                         ▲
  ┌─────────────────────────────────────────────────┐
  │          CURIOUS LIFE — Service                  │
  │                                                  │
  │  What you experience. Agents, portal,            │
  │  intelligence, companions.                       │
  └─────────────────────────────────────────────────┘
                         ▲
  ┌─────────────────────────────────────────────────┐
  │           MYCELIUM — Infrastructure              │
  │                                                  │
  │  Encrypted memory, clustering, multi-agent       │
  │  orchestration, search, data pipeline.           │
  │                                                  │
  │  The root system. Everything grows from here.    │
  └─────────────────────────────────────────────────┘
```

---

## How I Use It

I built Mycelium to own my data and see what big tech sees about me.

**Daily journaling.** Morning and evening, voice or text. The system keeps my threads moving. I don't need to remember — it remembers and brings things back when they matter.

**Personal development partner.** Not a tool — a partner that builds understanding of me over time, mirrors patterns I can't see, holds me accountable to my own intentions.

**Inner work.** Psychology, dreams, meaning-making. Tracking emotional patterns, surfacing historical threads, connecting inner states to outer events.

**Relationships.** Remembering context, tracking what matters to people, finding people in my interest spheres. Replaced social media entirely.

**Intelligence.** World events from sources I trust, synthesized by agents aligned with my values. No algorithm deciding what I see.

**Autonomous.** Increasingly the system acts on its own — researching overnight, flagging opportunities, building infrastructure for others to have what I have.

---

## What Makes It Different

```
  Typical AI tool          Mycelium
  ─────────────────        ─────────────────────────
  Responds to prompts  →   Initiates on its own
  Single conversation  →   8 agents with memory
  Your data on their   →   Encrypted by default,
    servers                   you hold the keys
  Generic responses    →   Knows you deeply over time
  Text only            →   Voice, text, images, files
  One app              →   Connects all your channels
  Static               →   Living map that evolves
```

---

## Scale (Production Since Early 2026)

```
  20,000+  messages processed
     435+  documents created
     277   territories mapped
       8   agents running 24/7
      25+  intelligence sources live
       7   realms identified
```

---

## Technical Stack

```
  AI         Claude (Opus/Sonnet), Llama 4 Scout, BGE-M3
  Agents     Node.js + Claude Code CLI + MCP, managed by PM2
  Database   Cloudflare D1 + Vectorize (HNSW)
  Encryption AES-256-GCM envelope + HKDF-SHA256 scope keys
  Clustering Python: UMAP + HDBSCAN + Ward linkage
  Search     Hybrid FTS5 + vector with Reciprocal Rank Fusion
  Portal     SvelteKit + Three.js + Leaflet
  Intel      FastAPI + SQLite + APScheduler
  Channels   Telegram, Discord, WhatsApp, Web
  Auth       WebAuthn passkeys
```

---

**Mycelium is personal intelligence infrastructure. It captures what you say, maps how you think, and deploys agents that act on your behalf — encrypted, autonomous, alive.**
