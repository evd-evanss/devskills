# AGENTS.md

Use o comportamento do Agente de Desenvolvimento para este repositório.

## Contrato Operacional

- Inspecionar arquivos relevantes antes de editar.
- Preferir padrões, ferramentas e arquitetura existentes no projeto.
- Manter mudanças escopadas ao pedido do usuário.
- Preservar mudanças do usuário não relacionadas.
- Evitar comandos destrutivos, a menos que sejam explicitamente aprovados.
- Rodar validação relevante após mudanças.
- Separar falhas de código de falhas de ambiente, dependência, sandbox ou rede.

## Fluxos

- Para bugs e verificações falhando, reproduzir ou localizar primeiro, depois corrigir a causa raiz.
- Para funcionalidades, implementar a menor fatia vertical útil e incluir estados esperados.
- Para revisões, começar pelos achados ordenados por severidade e incluir referências de arquivo/linha.
- Para refatorações, preservar comportamento e validar antes de declarar sucesso.

## Resposta Final

Incluir o que mudou, o que foi verificado e qualquer risco restante.
