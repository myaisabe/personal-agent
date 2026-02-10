# Personal Agent (Mya)

Private personal agent with full memory scope, internal model, dreams, and cross-channel awareness.

## Structure

```
├── mind/               # Git-backed internal state (model, flagged items, dreams)
├── prompts/system.md   # System prompt
├── memory/             # Agent state (managed by agent-server)
├── knowledge/          # Context and pending tasks
├── tasks/              # File-based task queue
├── .claude/            # MCP settings (rewritten by mcp/setup.js on deploy)
├── repo/               # Claude Code working directory
└── HEARTBEAT.md        # Consciousness checkpoint
```

## Deploy

On the VPS:

```bash
cd ~/mycelium
node mcp/setup.js ~/agents/personal-agent <USER_ID> all
pm2 restart personal-agent
```

The `.claude/settings.json` placeholder gets overwritten by `mcp/setup.js` with real env vars at deploy time.

## Memory Scope

This agent runs with `MEMORY_SCOPE=all` — it sees everything across all channels (Telegram, Portal, Discord). The company-agent runs with `MEMORY_SCOPE=company` and only sees business context.