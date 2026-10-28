# UGCHooks plugin for Claude

Turn a product link into TikTok and Instagram Reels posts with [UGCHooks](https://ugchooks.app), then work on the hooks, slide text, captions and hashtags in Claude.

## Install

```sh
/plugin marketplace add saeedmsdi-ugchooks/plugin
/plugin install ugchooks@ugchooks
```

The plugin adds the remote MCP server `https://ugchooks.app/mcp` and a skill. The first tool call opens ugchooks.app for sign-in and consent. Without the plugin, add the same URL as a custom connector in Claude (Settings → Connectors) or run `claude mcp add --transport http ugchooks https://ugchooks.app/mcp`.

## Tools

| Tool | Permission | What it does |
| --- | --- | --- |
| `get_profile` | profile:read | Your email and credit balance. |
| `list_batches` | batches:read | Your newest 100 batches. |
| `get_batch` | batches:read | Brief, written posts, locked parts, saved render links. |
| `create_batch` | batches:write | Product link → brief + first 10 posts. Free, 20 a day. |
| `write_part` | batches:write | Parts 1–9 of a batch you unlocked in the app. |

It cannot buy credits, unlock a batch or post. Publish with [UGC API](https://ugcapi.dev). Revoke access at https://ugchooks.app/oauth/mcp/connections.

[Website](https://ugchooks.app) · [Privacy](https://ugchooks.app/privacy/) · MIT license
