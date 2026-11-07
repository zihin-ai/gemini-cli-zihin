# Zihin extension

This extension connects Gemini CLI to the Zihin.ai agent platform through the `zihin` MCP server
(`@zihin/mcp-server`, a stdio proxy to `https://llm.zihin.ai/mcp`).

- Use the `chat_with_agent` tool to talk to a Zihin agent. To see which agents you can talk to, use
  `list_published_agents` (available to every role, including `member`); `list_agents` (owner,
  admin and editor only) lists all of the company's agents, published or not, for management.
- Auth, RBAC and tenant isolation are enforced server-side by the `ZIHIN_API_KEY` configured at
  install time; the key's role (owner/admin/editor/member) determines which tools are listed at all,
  so a tool that is missing is not available to this key.
- Agent runs can take minutes on long turns; do not assume a slow `chat_with_agent` call is stuck.
- The server also exposes platform skills (step-by-step playbooks) as MCP resources `zihin://skills/*`,
  for roles that can see resources. Read the relevant skill before multi-step work such as creating an
  agent, adding tools or configuring triggers.
- Do not rely on a fixed tool count or list: the available tools are whatever the server returns for
  the key's role.
