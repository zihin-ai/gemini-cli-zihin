# gemini-cli-zihin

[Gemini CLI](https://geminicli.com) extension for the [Zihin.ai](https://zihin.ai) agent platform —
chat with your Zihin agents, manage them and load platform skills, via the official
[`@zihin/mcp-server`](https://www.npmjs.com/package/@zihin/mcp-server).

## Install

```bash
gemini extensions install https://github.com/zihin-ai/gemini-cli-zihin
```

You will be prompted for your Zihin API Key (get one at the Zihin console; format `zhn_live_*`,
`zhn_test_*` or `zhn_dev_*`). The key is stored in your system keychain.

Requires Node.js >= 20 (the MCP server runs via `npx @zihin/mcp-server`).

## What you get

- The `zihin` MCP server (88 tools for an admin key, as of 2026-10-04: chat with agents, list/manage them,
  triggers, governance). The exact set depends on the key's role and is discovered from the server.
- A `GEMINI.md` context file teaching Gemini CLI how to use the tools well.

## Update

```bash
gemini extensions update zihin
```

Restart the Gemini CLI session afterwards. The MCP server itself runs through `npx @zihin/mcp-server`,
and the tools come from the Zihin server, so the tool list is current regardless of the extension version.

## License

MIT — see [zihin-ai/zihin-mcp](https://github.com/zihin-ai/zihin-mcp) for the underlying server.
