# Teamfight Tactics MCP Server

> Hosted MCP server connecting **Claude**, **ChatGPT**, and any MCP client to **Teamfight Tactics** data and AI-powered coaching - **19 tools**, **built-in Riot API key**, zero setup.

This repository is the public home and documentation for the **TFT MCP Server**, a remote (hosted) [Model Context Protocol](https://modelcontextprotocol.io) server. It runs on [Apify](https://apify.com/mrbridge/tft-mcp-server?fpr=mrbridge) in Standby mode - there's nothing to install or self-host. It's also listed in the [official MCP registry](https://registry.modelcontextprotocol.io) as `com.mr-bridge/tft-mcp-server`.

## Connect in 2 minutes

Connection URL (same for every client) - replace `YOUR_APIFY_TOKEN` with your [Apify API token](https://console.apify.com/account/integrations):

```
https://mrbridge--tft-mcp-server.apify.actor/mcp?token=YOUR_APIFY_TOKEN
```

- **Claude Desktop** - Settings → Connectors → Add custom connector → paste the URL.
- **ChatGPT** (Plus / Pro / Team / Enterprise) - Settings → Connectors → enable developer mode → Add custom connector → paste the URL.
- **Apify Universal MCP** - add `https://mcp.apify.com?tools=mrbridge/tft-mcp-server` to your existing config.

**No Riot API key needed** - a built-in, dedicated key ships with the server. No developer account, no 24-hour key to rotate.

## What it does

Ask your AI assistant in plain language; it pulls your real ranked games and coaches you on them.

**19 tools**, grouped:

- **Player & matches** - account, summoner, ranked (TFT / Hyper Roll / Double Up), full profile, match history, full match details, live game.
- **AI analysis** - placement diagnosis, champion analysis, improvement tips, player comparison.
- **Ladders & platform** - Challenger / Grandmaster / Master, any tier ladder, Hyper Roll rated ladder, league by id, server status, featured games.

All 16 regions (EUW, EUNE, NA, KR, BR, LAN, LAS, OCE, TR, RU, JP, PH, SG, TH, TW, VN). Champion mastery and match timeline are exposed for compatibility but report "not available for TFT" - Riot provides no such endpoint for Teamfight Tactics.

## Example prompts

- "Look up Kataamak#6015 on EUW - what's their rank and average placement?"
- "Analyze my last 20 ranked games and tell me what's costing me LP."
- "Give me 3 comps that fit how I play, with items and level-by-level spikes."
- "I'm in a game now - look up my lobby and tell me who's the biggest threat."

## Pricing

Pay-per-event on Apify - you only pay when a tool runs, no idle cost. **$5 free credits every month.** See the [Apify Actor page](https://apify.com/mrbridge/tft-mcp-server?fpr=mrbridge) for the full breakdown.

## Related MCP servers

- [League of Legends MCP Server](https://apify.com/mrbridge/lol-mcp-server?fpr=mrbridge) - 26 tools: profiles, ranked, match history, live game, AI coaching
- [ESPN MCP Server](https://apify.com/mrbridge/espn-mcp-server?fpr=mrbridge) - live scores, standings and odds across 25+ leagues
- [Latest News MCP Server](https://apify.com/mrbridge/latest-news-mcp-server?fpr=mrbridge) - 14 tools over 27 free news and data APIs
- [Todoist AI Assistant](https://apify.com/mrbridge/todoist-ai-assistant?fpr=mrbridge) - 35 tools for AI-powered task management

## Links

- **Run it:** [Apify Actor](https://apify.com/mrbridge/tft-mcp-server?fpr=mrbridge)
- **Official MCP registry:** `com.mr-bridge/tft-mcp-server`
- **Built by [MrBridge](https://mr-bridge.com)** - [MCP server catalog](https://mr-bridge.com/mcp-servers) · [what is MCP?](https://mr-bridge.com/articles/what-is-mcp-model-context-protocol)

---

The server runs as a managed Apify Actor; this repository hosts documentation and the public registry manifests (`server.json`, `glama.json`) only.
