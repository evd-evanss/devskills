# Git, Branch, Commit E PR/MR

Use esta referência para evitar padrões de empresa e respeitar o repositório atual.

## Branch Base

Detectar nesta ordem:

1. Instruções em `AGENTS.md`, `CLAUDE.md`, README, CONTRIBUTING ou docs internos.
2. Branch padrão remota: `git remote show origin`.
3. Branches comuns: `main`, `master`, `develop`, `trunk`.
4. Perguntar ao usuário quando a escolha afetar PR/MR ou histórico compartilhado.

## Nome Da Branch

Detectar o padrão local antes de criar:

- Branches existentes: `git branch -a`.
- Docs do projeto.
- Convenções em PRs recentes, se disponíveis.

Padrões genéricos aceitáveis:

- `feat/short-description`.
- `fix/short-description`.
- `chore/short-description`.
- `refactor/short-description`.
- `ticket-id-short-description`.
- `ticket-id` somente se o projeto usar esse padrão.

Se houver ticket, incluir o ID quando isso ajudar rastreabilidade. Não assumir que a branch deve ser apenas o ticket.

## Proteção Antes De Commit E Push

Antes de `git add`, `git commit` ou `git push`:

1. Rodar `git status -sb`.
2. Confirmar branch atual.
3. Não commitar em branch protegida (`main`, `master`, `develop`, `trunk`) sem pedido explícito.
4. Não stagear mudanças não relacionadas.

## Commit

Seguir a convenção local. Se não houver padrão, usar Conventional Commits:

```text
feat: add login validation
fix: avoid crash on empty response
refactor: simplify payment mapper
```

Inclua ID do ticket apenas se o projeto fizer isso.

## PR/MR

Detectar provedor:

- GitHub: `gh pr create`, GitHub app ou URL remota.
- GitLab: `glab mr create` ou fluxo web/manual.
- Bitbucket/Azure: seguir docs ou informar instrução manual.

Usar template do projeto quando existir:

- `.github/pull_request_template.md`.
- `.gitlab/merge_request_templates/`.
- Docs de contribuição.

O corpo deve conter:

- O que mudou.
- Por que mudou.
- Como foi validado.
- Screenshots/vídeos quando houver UI.
- Links para ticket/design quando disponíveis.
