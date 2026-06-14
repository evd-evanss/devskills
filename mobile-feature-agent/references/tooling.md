# Tooling E Rastreador De Trabalho

Use esta referência para descobrir quais ferramentas estão disponíveis no projeto atual.

## Rastreador De Trabalho

Aceite qualquer uma destas fontes:

- Jira.
- Linear.
- GitHub Issues.
- Azure Boards.
- Notion, Trello ou outro board.
- Texto livre do usuário.

## Como Detectar

1. Se o usuário fornecer URL ou ID, identificar a ferramenta pelo formato.
2. Se houver MCP/app/conector disponível, usar para buscar título, descrição, comentários, anexos e links.
3. Se não houver integração, pedir ao usuário o conteúdo essencial ou trabalhar com a descrição fornecida.
4. Sempre considerar comentários recentes, porque podem substituir o escopo original.

## Operações Opcionais

Estas ações são convenientes, mas não obrigatórias:

- Atribuir ticket ao usuário atual.
- Mover para "Em andamento".
- Adicionar comentário com plano.
- Mover para "Code Review", "In Review" ou equivalente.
- Adicionar link do PR/MR.

Se falharem, avisar e continuar quando o código e o PR/MR estiverem corretos.

## Estados Genéricos

Ao mover cards, não use nomes fixos. Procure equivalentes:

- Início: "Em andamento", "In Progress", "Doing", "Started".
- Revisão: "Code Review", "In Review", "Review", "Revisando".
- Conclusão: "Done", "Merged", "Ready for QA", conforme o processo do projeto.

Se houver ambiguidade, pergunte antes de mudar o estado.
