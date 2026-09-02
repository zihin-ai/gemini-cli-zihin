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

- The `zihin` MCP server (96 tools: chat with agents, list/manage them, triggers, skills).
- A `GEMINI.md` context file teaching Gemini CLI how to use the tools well.

## License

MIT — see [zihin-ai/zihin-mcp](https://github.com/zihin-ai/zihin-mcp) for the underlying server.
