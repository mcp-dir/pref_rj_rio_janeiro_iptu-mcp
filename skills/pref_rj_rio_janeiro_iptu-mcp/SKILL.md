---
name: pref_rj_rio_janeiro_iptu-mcp
description: Skill da REST API do Prefeitura RJ Rio de Janeiro: Emissão de IPTU na MCP.AI: 1 endpoint em /api/pref_rj_rio_janeiro_iptu. Prefeitura RJ Rio de Janeiro: Emissão de IPTU, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Prefeitura RJ Rio de Janeiro: Emissão de IPTU — REST API skill

Você tem acesso à **Prefeitura RJ Rio de Janeiro: Emissão de IPTU** REST API na MCP.AI.

> Prefeitura RJ Rio de Janeiro: Emissão de IPTU, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pref_rj_rio_janeiro_iptu
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/pref_rj_rio_janeiro_iptu/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"inscricao":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pref_rj_rio_janeiro_iptu/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pref_rj_rio_janeiro_iptu_consultar`

Prefeitura RJ Rio de Janeiro: Emissão de IPTU, consulta em fonte oficial. _(POST /api/pref_rj_rio_janeiro_iptu/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `inscricao` | string | Sim | Parâmetro de consulta "inscricao". |
| `guia_exercicio` | string | Não | Parâmetro de consulta "guia_exercicio". |
| `cota` | string | Não | Parâmetro de consulta "cota". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pref_rj_rio_janeiro_iptu` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
