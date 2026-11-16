# rota-connector

Plugin do Claude Code que mostra o símbolo da [ROTA](https://rotasaas.com) ao lado de toda chamada de ferramenta do connector [MCP ROTA](https://github.com/rota-scale/mcp-rota).

- **Desktop, editor e celular:** o símbolo verde da ROTA aparece na linha de cada chamada.
- **Terminal:** um losango verde `◆`, na mesma cor.

O plugin só desenha o ícone. Ele não conecta o MCP: para isso siga o README do `mcp-rota` (Settings > Connectors > Add > Custom connector, `https://mcp.rotasaas.com/mcp`).

## Instalar

No prompt de uma sessão de terminal:

```
/plugin install rota-connector --marketplace rota-scale/rota-connector
```

Num shell:

```
claude plugin install rota-connector --marketplace rota-scale/rota-connector
```

No app desktop: clique em + ao lado da caixa de texto, Plugins, Add marketplace com `rota-scale/rota-connector`, depois Add plugin.

## Como reconhece a ROTA

O ícone aparece em ferramentas cujo nome começa com `mcp__` seguido de um servidor com "rota" no nome (por exemplo `mcp__rota__...`). Se o seu connector chegar com outro nome, ajuste `IS_ROTA` em `hooks/register.tsx`.

## Licença

MIT.
