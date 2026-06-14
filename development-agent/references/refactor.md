# Fluxo De Refatoração

Use este fluxo para limpeza, reestruturação, nomes, modularização, deduplicação e trabalho de manutenção.

## Passos

1. Identificar o comportamento que deve permanecer inalterado.
2. Encontrar testes ou comandos que protejam esse comportamento.
3. Fazer uma mudança estrutural coerente por vez.
4. Preservar APIs públicas, a menos que o usuário queira explicitamente uma quebra.
5. Rodar testes antes e depois quando for viável.
6. Relatar a melhoria estrutural e a validação.

## Regras De Proteção

- Não combinar refatorações com mudanças de comportamento não relacionadas.
- Não introduzir uma abstração apenas para reduzir poucas linhas.
- Preferir simplificação local antes de arquitetura entre projetos.
- Manter nomes alinhados com a linguagem de domínio existente.
- Se não houver testes, usar smoke checks focados e explicar a lacuna.

## Bons Alvos De Refatoração

- Ramificações repetidas que já apontam para um conceito claro de domínio.
- Funções longas com fases separáveis de parsing, validação ou renderização.
- Setup duplicado entre testes.
- Nomes confusos que entram em conflito com a terminologia do projeto.
