# Instalação rápida

Prefeitura RJ Rio de Janeiro: Emissão de IPTU é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_pref_rj_rio_janeiro_iptu`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Prefeitura RJ Rio de Janeiro: Emissão de IPTU` / `https://api.mcp.ai/p_pref_rj_rio_janeiro_iptu`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "pref_rj_rio_janeiro_iptu": { "type": "http", "url": "https://api.mcp.ai/p_pref_rj_rio_janeiro_iptu" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pref_rj_rio_janeiro_iptu&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wcmVmX3JqX3Jpb19qYW5laXJvX2lwdHUifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "pref_rj_rio_janeiro_iptu": { "url": "https://api.mcp.ai/p_pref_rj_rio_janeiro_iptu" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=pref_rj_rio_janeiro_iptu&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pref_rj_rio_janeiro_iptu%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "pref_rj_rio_janeiro_iptu": { "type": "http", "url": "https://api.mcp.ai/p_pref_rj_rio_janeiro_iptu" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_pref_rj_rio_janeiro_iptu
```

Dúvidas? [pref_rj_rio_janeiro_iptu@mcp.ai](mailto:pref_rj_rio_janeiro_iptu@mcp.ai)
