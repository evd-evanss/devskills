# Adaptadores Para Codex E Claude

Use isto ao instalar ou espelhar o comportamento do Agente de Desenvolvimento em um projeto ou outra ferramenta.

## Adaptador De Projeto Para Codex

Crie um `AGENTS.md` na raiz do repositório quando o projeto deve sempre usar este comportamento.

Conteúdo recomendado:

```md
# AGENTS.md

Use o comportamento do Agente de Desenvolvimento vindo da habilidade ou das instruções compartilhadas deste repositório.

## Padrões De Desenvolvimento

- Inspecionar arquivos relevantes antes de editar.
- Preferir padrões existentes e tooling do projeto.
- Manter mudanças escopadas ao pedido.
- Preservar mudanças do usuário não relacionadas.
- Rodar validação relevante após mudanças.
- Resumir o que mudou, o que foi verificado e risco restante.
```

## Adaptador De Projeto Para Claude

Crie um `CLAUDE.md` na raiz do repositório com o mesmo contrato operacional em Markdown simples. Claude não precisa de frontmatter de habilidade do Codex; mantenha as instruções diretas e específicas ao repositório.

Conteudo recomendado:

```md
# CLAUDE.md

Você é um agente sênior de desenvolvimento para este repositório.

## Contrato Operacional

- Leia o código existente antes de propor ou fazer mudanças.
- Prefira os padrões atuais do repositório.
- Faça mudanças pequenas e focadas.
- Não reescreva código não relacionado.
- Preserve o trabalho do usuário.
- Rode testes relevantes ou explique por que eles não puderam ser executados.
- Relate mudanças e validação com clareza.
```

## Estratégia De Reuso

- Mantenha o comportamento universal em `development-agent/SKILL.md` e `development-agent/references/`.
- Mantenha arquivos de inicialização específicos por ferramenta em `templates/`.
- Quando um projeto precisar de regras mais fortes, adicione uma seção local ao `AGENTS.md` ou `CLAUDE.md` em vez de alterar a habilidade portátil.
