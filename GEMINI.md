# Zihin extension

This extension connects Gemini CLI to the Zihin.ai agent platform through the `zihin` MCP server
(`@zihin/mcp-server`, a stdio proxy to `https://llm.zihin.ai/mcp`).

- Use the `chat_with_agent` tool to talk to a Zihin agent; `list_agents` shows what is available.
- Auth, RBAC and tenant isolation are enforced server-side by the `ZIHIN_API_KEY` configured at
  install time; the key's role (admin/editor/member) determines which tools succeed.
- Agent runs can take minutes on long turns; do not assume a slow `chat_with_agent` call is stuck.
- The server also exposes platform skills (step-by-step playbooks) as MCP resources `zihin://skills/*`,
  for roles that can see resources. Read the relevant skill before multi-step work such as creating an
  agent, adding tools or configuring triggers.
- Do not rely on a fixed tool count or list: the available tools are whatever the server returns for
  the key's role.
