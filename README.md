# Sightkick skill — retired

> **This skill is retired (2026-09-20) and no longer maintained.** Nothing here
> needs to be installed. Its playbook now ships inside the Sightkick MCP server
> itself, in the protocol's `instructions` field, so **every** client gets it on
> connect — including claude.ai and ChatGPT connectors, which could never
> install a skill file.

## What to do instead

Just connect the MCP server. There is nothing else to install.

```sh
claude mcp add --transport http sightkick https://app.sightkick.so/mcp
```

For any other client — Claude desktop and claude.ai, ChatGPT, Cursor, VS Code —
add a custom or remote MCP server and paste the same endpoint. There is no API
key; the first call opens a sign-in, and one OAuth grant is bound to one
workspace.

Your agent receives the operating playbook automatically: the writing dial and
its rails, the division of labour with Sightkick's own autopilot, the named
plays (weekly pulse, gap fixer, coverage pitch, proof report), and how to
report. The `search_guidance` tool returns Sightkick's SEO/AEO method on demand.

## Why it was retired

A skill file only reaches agents with a local filesystem, so most clients never
saw it. Most of its content repeated what the tool descriptions and
`search_guidance` already say. And it was the one description of the tool
catalog that shipped outside the product's deploy, so it went stale twice while
the server it described had already moved on.

## Links

- [Server page](https://sightkick.so/mcp)
- [Agent guide](https://sightkick.so/llm-info)
- [MCP server repo](https://github.com/sightkick-so/mcp) — registry entry and tool catalog
- [sightkick.so](https://sightkick.so)

MIT © Sprike LLC (Sightkick)
