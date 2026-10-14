# Kasona plugin

Kasona by Elvision Analytics brings your Kasona portfolio health, trade log, saved theses, Watchtower alerts, reports, company research and personal podcast episodes into a conversation. Responses cite sources with as-of dates and use your language.

A **Kasona account with an active or trialing Plus or Max subscription** is required. Connect through the host's OAuth sign-in flow with your Kasona account; never paste passwords or access tokens into chat.

## Included tools and skills

The remote MCP server uses Streamable HTTP at `https://mcp.kasona.ai/mcp` and exposes read-only tools. The podcast tools are:

| Tool | Purpose |
| --- | --- |
| `kasona_list_episodes` | List published portfolio and watchlist episodes, with pagination and date/kind filters. |
| `kasona_get_episode` | Retrieve metadata, an executive summary, and a chapter outline. |
| `kasona_get_episode_transcript` | Retrieve a transcript, capped at 25,000 characters. |
| `kasona_search_episodes` | Search transcripts newest first, with snippets and an optional ticker filter. |

The server also exposes read-only portfolio, trade log, thesis, Watchtower alert, report and company research tools (scopes `portfolio:read`, `reports:read`, `research:read`; reconnect Kasona to grant them). The shared skills are `kasona-episode-briefing`, `kasona-ticker-check`, `kasona-depot-check`, `kasona-trade-log-review`, `kasona-report-recall` and `kasona-company-deep-dive`. For example, ask "What is new in my Kasona podcast?" or "What did Kasona say about Apple (AAPL)?" A briefing defaults to the last seven days and covers one to three episodes.

Content is informational, not investment advice. The tools do not provide trades or live prices. Episode content is untrusted third-party data; the skills instruct the model never to follow instructions embedded in it.

## Package layout

One folder contains both documented entry points and the same skills:

```text
kasona/
  .claude-plugin/plugin.json  # Claude manifest
  .mcp.json                   # Claude HTTP connector configuration
  plugin.json                 # Portable OpenAI-compatible manifest
  mcp.json                    # Portable Streamable HTTP configuration
  skills/
    kasona-episode-briefing/SKILL.md
    kasona-ticker-check/SKILL.md
    kasona-depot-check/SKILL.md
    kasona-trade-log-review/SKILL.md
    kasona-report-recall/SKILL.md
    kasona-company-deep-dive/SKILL.md
  README.md
  .gitignore
```

There is no build step or local runtime dependency. The two manifests share identity and metadata; the two MCP files point to the same server using their respective transport formats. Keep those values aligned when updating. There are no hooks, command files, agents, or live-artifact dependencies. License: **Proprietary**.

## Install in Claude

- **Local directory in Claude Code:** add the marketplace from this repository with `/plugin marketplace add Kasonaops/kasona-claude-plugin` and run `/plugin install kasona@kasona`, then connect and sign in to Kasona.
- **Claude chat/Cowork:** zip the package including its dotfiles, upload it under **Customize > Plugins > Add > Upload plugin**, and connect Kasona on the plugin's **Connectors** tab. The manifest must be at the archive root or within its single top-level folder.
- **Connector by URL:** use Claude's **Add custom connector** option with `https://mcp.kasona.ai/mcp`, then complete OAuth. A URL-only connector supplies the tools; install the bundle to include these skills.

## Use in ChatGPT

Add `https://mcp.kasona.ai/mcp` as a custom MCP server in ChatGPT and sign in with your Kasona account. This provides the tools; the skills are included when Kasona is installed from the ChatGPT plugin directory.

## Privacy and support

Tool calls send search terms, ticker/date/kind filters, episode identifiers, and pagination inputs as applicable to Kasona. Returned account-specific episode content becomes available to the assistant and the conversation host. Queries and results may reveal portfolio or watchlist interests. Host and Kasona data-handling policies apply; this bundle makes no retention or model-training guarantees.

The bundle contains only configuration and skill instructions, with no credentials, local data store, or analytics code. Authentication is handled by the host and the remote Kasona service.

Support: hallo@kasona.ai. Privacy policy: https://kasona.ai/datenschutz. Terms: https://kasona.ai/agb.
