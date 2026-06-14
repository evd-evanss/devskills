# Devskills

Habilidades reutilizáveis para agentes de desenvolvimento no Codex, com templates equivalentes para Claude.

## Estrutura

```text
development-agent/
  SKILL.md
  agents/openai.yaml
  references/
mobile-feature-agent/
  SKILL.md
  agents/openai.yaml
  references/
templates/
  AGENTS.md
  CLAUDE.md
```

## Skills

### `development-agent`

Agente geral de desenvolvimento para implementar, depurar, testar, refatorar e revisar projetos de software.

### `mobile-feature-agent`

Fluxo genérico de desenvolvimento mobile para Android, iOS, KMP, React Native, Flutter ou stacks híbridas. Ele não assume Jira, Figma, GitHub, branch `develop`, design system, framework de UI, injeção de dependência ou qualquer padrão de empresa; detecta e segue as ferramentas e convenções do projeto atual.

## Usar Com Codex

Instale ou copie a pasta da skill desejada para o diretório de habilidades do Codex. Depois invoque com:

```text
Use $development-agent para corrigir este bug e validar a mudança.
Use $mobile-feature-agent para implementar este card mobile seguindo as ferramentas do projeto.
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
