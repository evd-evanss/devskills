---
name: mobile-dev-workflow
description: Fluxo genérico de desenvolvimento mobile para Android, iOS, KMP, React Native, Flutter ou stacks híbridas. Use quando Codex precisar conduzir uma tarefa mobile de ponta a ponta: entender item de trabalho em Jira, Linear, GitHub Issues, Azure Boards ou texto livre; analisar design opcional em Figma ou outra fonte; criar branch seguindo o padrão do projeto; implementar feature, bugfix ou refatoração; rodar testes e checks disponíveis; abrir PR/MR; e atualizar o rastreador quando a integração existir.
---

# Mobile Dev Workflow

Use esta skill para conduzir trabalho mobile sem assumir ferramenta, empresa, design system ou padrão de branch específico.

## Princípios

- Detectar as ferramentas reais do projeto antes de agir.
- Tratar Jira, Linear, GitHub Issues, Azure Boards e texto livre como fontes possíveis de escopo.
- Tratar Figma, screenshots, specs, design tokens ou descrição textual como fontes possíveis de design.
- Usar o design system do projeto quando existir; se não existir, seguir componentes e estilos locais.
- Usar o padrão de branch, commit, PR/MR e checks já documentado no repo.
- Confirmar plano antes de mudanças grandes ou quando o escopo vier de ticket/design ambíguo.
- Não bloquear o trabalho por automações externas opcionais, como mover card ou atribuir ticket.

## Seleção De Referências

Leia apenas o arquivo necessário:

- Para configurar ou detectar ferramentas: `references/tooling.md`.
- Para criar branch, commit e PR/MR de forma genérica: `references/git-and-pr.md`.
- Para implementação mobile por stack: `references/mobile-implementation.md`.
- Para testes, build e quality checks: `references/validation.md`.
- Para design system e fontes de design: `references/design.md`.
- Para analisar o que foi removido da skill original e por quê: `references/genericization-notes.md`.

## Fluxo Padrão

1. Capturar o item de trabalho:
   - ID de ticket, URL, issue, descrição livre ou bug report.
   - Ferramenta disponível, se houver.
   - Critérios de aceite, comentários recentes e links/anexos relevantes.
2. Detectar contexto do repositório:
   - Stack mobile, módulos, arquitetura, gerenciador de pacotes, comandos e branch base.
   - Padrões locais de branch, commit, PR/MR, testes e design system.
3. Classificar a tarefa:
   - UI completa, integração/data/domain sem UI, bugfix, refatoração, teste, build ou melhoria técnica.
4. Criar um plano curto:
   - Arquivos prováveis, camadas afetadas, checks a rodar, riscos e decisões pendentes.
5. Implementar seguindo padrões locais.
6. Validar com os comandos disponíveis.
7. Fazer revisão do diff antes de commit/PR quando o trabalho for substancial.
8. Criar commit e PR/MR se solicitado ou se o fluxo do usuário pedir.
9. Atualizar o rastreador apenas quando a integração estiver configurada e a ação for segura.
10. Resumir o que mudou, validação e próximos passos.

## Regras De Portabilidade

- Não assuma Jira como obrigatório.
- Não assuma Figma como obrigatório.
- Não assuma GitHub como único provedor de PR.
- Não assuma `develop` como branch base.
- Não assuma branch com apenas o ticket.
- Não assuma Gradle, KMP, Compose, Koin, Arco ou qualquer design system.
- Não exija 100% de cobertura por padrão; siga a política do projeto e aumente cobertura onde houver risco.
- Não crie UI quando o escopo for explicitamente sem UI.
- Não altere status de ticket quando a automação não estiver clara ou puder causar ruído.

## Uso Com Subagentes

Use subagentes quando disponíveis e quando a tarefa for longa:

- Pesquisa de padrões existentes.
- Implementação com múltiplas edições.
- Escrita e execução de testes.
- Correção de lint/formatação.
- Revisão read-only do diff.
- Preparação de PR/MR.

Ao delegar, passe contexto explícito: objetivo, stack, arquivos de referência, plano aprovado, comandos permitidos e limites do que não deve ser alterado.
