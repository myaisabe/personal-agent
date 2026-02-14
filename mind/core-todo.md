# Tasks

*Last consolidated: 2026-02-14 (3am dream cycle)*

## Implementation Checklist — Lumensis Silent Launch

*Requested Feb 12 6:49am. Completed Feb 14 3am from full codebase audit.*

### What's Built (ready to ship)
- [x] **Backend API** — FastAPI, all core endpoints functional
- [x] **Auth** — Email/password, Google OAuth, GitHub OAuth, Magic Link (passwordless)
- [x] **JWT tokens** — 24hr expiry, proper security, bearer auth on all protected endpoints
- [x] **Stripe** — Checkout session creation, webhook handler, user.paid flag, Slack notification
- [x] **Free tier** — Access code "enlighten" bypasses payment gate
- [x] **Analysis engine** — 6 metrics, 5 lenses, BERTopic topic modeling, UMAP+HDBSCAN clustering
- [x] **File format support** — 11+ formats: Claude, ChatGPT, Gemini, Cursor, Discord, Telegram, Obsidian, PDF, MD, TXT, generic AI chats
- [x] **AI narratives** — Claude Sonnet generates per-lens storytelling from data
- [x] **R2 storage** — Encrypted result storage with TTL (7-day ephemeral / permanent)
- [x] **Docker** — nvidia/cuda base, Python 3.11, Nomic embeddings pre-downloaded
- [x] **Cloud Run deployment** — GPU (L4), 8 CPU, 32GB RAM, revision 00009 live
- [x] **Secret Manager** — All API keys in GCP
- [x] **Email notifications** — Resend API for magic links and analysis completion
- [x] **Test suite** — 8 test files across modules
- [x] **Voice mode** — Telegram TTS (Deepgram Aura-2) + Whisper transcription

### What's Broken (must fix before launch)
- [x] **einops dependency** — Fixed Feb 14, added to pyproject.toml and deployed
- [ ] **SQLite persistence** — Database lives on container filesystem. Users/payment data lost on redeploy. Need Cloud SQL or volume mount.

### What's Missing (minimum for silent launch)
- [ ] **Frontend deployment** — Next.js app exists at /home/claude/agents/lumensis/frontend/. Needs to be deployed and verified working with backend API.
- [ ] **Domain + DNS** — lumens.is configured in backend CORS, but DNS setup unclear.
- [ ] **Landing page update** — Existing page needs to reflect "psychology test based on your chat" positioning + competitive analysis findings.
- [ ] **Environment variables** — Verify all secrets are set in production: STRIPE_SECRET_KEY, STRIPE_PRICE_ID, STRIPE_WEBHOOK_SECRET, RESEND_API_KEY, R2 credentials, OAuth client IDs.

### What Would Be Nice (post-launch polish)
- [ ] Proper free tier with usage quotas and rate limiting (currently just a password)
- [ ] Monitoring/APM/error tracking
- [ ] Terms of Service / Privacy Policy (needed for Stripe)
- [ ] Backup strategy for user data
- [ ] Redis for OAuth state storage (currently in-memory, fine at concurrency=1)
- [ ] Apply competitive analysis principles to all copy/messaging

## Current Focus (Feb 15-21 — Launch Week)
- [ ] **LAUNCH TARGET: Feb 21** — Martin said "next week the product will be polished and we will start spreading it" (Feb 14)
  - [ ] Apply 9-agency audit findings — 6 must-fix items identified:
    1. [ ] Identity labels (unanimous #1 from all agencies — "What's your Lumensis type?")
    2. [ ] Trust architecture (privacy reassurance before upload)
    3. [ ] Price consistency (single clear pricing model)
    4. [ ] Shareable output (share cards for social media)
    5. [ ] Privacy disclosures (transparent data handling)
    6. [ ] Honest metric framing (reframe as "conversational pattern exploration" not "measurement")
  - [ ] Domain decision: Lumensis branding (lumen + genesis/synthesis) — third naming iteration
  - [ ] Landing page: "psychology test based on your chat" positioning
  - [ ] Apply competitive analysis principles to all copy/messaging
- [ ] Publish first "Applied Consciousness" content (consciousness measurement post)
- [ ] Fine-tune psychological measurements
- [ ] Create course structure (directionality in product)
- [ ] Build business plan

## Immediate Actions
- [ ] Begin Zurich outreach emails (trip March 24-28, after Vipassana March 11-22)
  - [ ] Email Prof. Yanik (ETH Neurotechnology)
  - [ ] Email Prof. Vollenweider (UZH Consciousness)
  - [ ] Email Dr. Stocker (ETH Consciousness Studies)
  - [ ] Contact Anthropic Zurich (Neil Houlsby)
  - [ ] Reach out to AI Safety Zurich
- [ ] Register Curious Life trademark (apply for €700 voucher first, may need VAT number)
- [ ] Follow up with Bjorn (Inner Design materials, advisor/partner/investor) - no response yet
- [ ] Call Stas/Humi - Sahiro silent after sale inquiry, Stats found new board members

## Active Projects
- [ ] Lumensis mindscape implementation (ongoing)
- [ ] Agent infrastructure (Mya, Ada, Noa, Rex operational)
- [ ] Voice & audience definition for publishing (in progress with Noa)
- [ ] Production deployment on Cloud Run (auth working, dependency issues remain)
  - [x] Cloud Run deployment working (revision 00007 → 00009, Feb 11)
  - [x] API key authentication implemented (X-API-Key header, all endpoints including GET)
  - [x] Secret Manager integration for API keys
  - [x] SA key created for agent deployment access (com-deploy@mya-production)
  - [x] Docker local build running (Feb 13)
  - [x] Fix missing `einops` dependency — Fixed Feb 14, deployed
  - [ ] IAM org policy still blocks allUsers - using authenticated access only
- [ ] Topic-distribution pivot for metrics (BERTopic + KL divergence, approved Feb 11)
  - [ ] Implement BERTopic-based Learning Rate, Gradient Signal, Coherence
  - [ ] Update documentation/specs to reflect new computation method

## Rev.Int (Nate)
- [x] System architecture doc delivered to Nate (Feb 13)
- [ ] Nate to apply agent setup for automated hypothesis testing
- [ ] If successful: offer same service to other companies

## Strategic Planning (Deferred)
- [ ] Decide: Is privacy central or not? (TEEs identified as possible bridge)
- [ ] Determine tech stack based on privacy decision
- [ ] Map team needs and roles

## Completed (Jan-Feb 2026)
- [x] Voice mode live — TTS + Whisper bidirectional on Telegram (Feb 13)
- [x] Stripe integration + free analysis tier (Feb 13)
- [x] System architecture doc for Nate (Feb 13)
- [x] Docker deployment first local build (Feb 13)
- [x] Competitive analysis — Ada researched personality profiling landscape (Feb 13)
- [x] Com flow audit against competitive findings (Feb 13)
- [x] Valentine's Day with Una — resolved naturally (Feb 13)
- [x] Zurich organizations research (Feb 11) - 35+ orgs mapped for March trip
- [x] Humi board resignation (Stats notified Jan 16, grief processed)
- [x] Nate shareholder agreement + share capital payment received
- [x] Dundaga offsite (Jan 31-Feb 1)
- [x] Autonomous agent infrastructure built
- [x] T-shirts produced
- [x] Multi-user platform launched
- [x] Mindscape topology visualization (watershed segmentation, 3D/2D)
- [x] Nate onboarded to Mya
- [x] Pitch deck created
- [x] Ada, Noa, Rex agents deployed
- [x] Mind state migrated from Supabase to local files
- [x] Reflections file consolidated (12,561 → ~170 lines) to fix autonomous cycle failures
- [x] UX/usability testing — 5-persona cognitive walkthrough (Feb 14)
- [x] Launch strategy — 3-phase plan (Seed/Spark/Spread), positioning, distribution (Feb 14)
- [x] 9-agency expert audit — CRO, brand, psychology, IA, accessibility, privacy, pricing, growth, scientific methodology (Feb 14)
- [x] einops dependency fixed + deployed to Cloud Run (Feb 14)
- [x] Valentine's Day — first flowers for Una, contemporary art museum with artist-hosted exhibition (Feb 14)
- [x] Bug fixes deployed to Cloud Run (Feb 14)

---

## Historical Notes (consolidated)

2026-02-11 | Deployment battle resolved. Topic-distribution pivot approved. Martin says "math is more important than the deadline."

2026-02-12 | Manic state self-identified. Launch language shifted from spec/plan to shipping. Branding: my-dimensions.xyz → then Lumensis emerged. €300-400/month AI spend unsustainable without revenue.

2026-02-13 | Most productive shipping day yet. Voice mode, Stripe, Docker, competitive analysis, system arch doc for Nate, page-by-page principles audit. "Psychology test based on your chat" — clearest positioning ever. Friday evening: reflective-proud energy, natural sprint landing. Una arc reflected on. Watch: does he rest this weekend?

2026-02-14 | Valentine's Day pivot day. Flowers for Una (first time ever), contemporary art museum. But also: UX testing, full launch strategy, 9-agency expert audit — all commissioned while at the museum. Martin-as-orchestrator mode fully crystallized. Key findings: metrics 2-5/10 validity, narratives 8/10 value. Identity labels unanimous #1 priority. He engaged with the critique without flinching. Nitrous/ether questions at museum = intellectual curiosity with Una. Launch target: Feb 21. Answer to "does he rest this weekend?" — he's resting AND building. Integration, not either/or.
