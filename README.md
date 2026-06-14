# Devskills

Habilidade reutilizável de agente de desenvolvimento para Codex, com templates equivalentes para Claude.

## Estrutura

```text
development-agent/
  SKILL.md
  agents/openai.yaml
  references/
templates/
  AGENTS.md
  CLAUDE.md
```

## Usar Com Codex

Instale ou copie a pasta `development-agent/` para o diretório de habilidades do Codex. Depois invoque com:

```text
Use $development-agent para corrigir este bug e validar a mudança.
```

Para comportamento local em um repositório, copie `templates/AGENTS.md` para a raiz do projeto alvo e personalize comandos específicos do projeto.

## Usar Com Claude

Copie `templates/CLAUDE.md` para a raiz do projeto alvo e personalize comandos, notas de arquitetura e expectativas de validação específicas do projeto.

## Repositorio

Nome sugerido:

```text
devskills
```

Este repositório mantém a habilidade portátil em português para facilitar leitura, manutenção e evolução.
