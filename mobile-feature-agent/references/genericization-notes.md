# Notas De Generalização

Esta skill foi generalizada a partir de um fluxo mobile acoplado a uma empresa e stack específicas.

## O Que Foi Tornado Genérico

- Jira deixou de ser obrigatório; agora é uma opção entre vários rastreadores.
- Figma deixou de ser obrigatório; agora é uma fonte de design opcional.
- GitHub deixou de ser obrigatório; PR/MR depende do provedor do repositório.
- Branch `develop` deixou de ser assumida; a branch base deve ser detectada.
- Branch apenas com ticket deixou de ser obrigatória; o padrão local vence.
- Design systems e componentes internos específicos foram removidos; o design system local vence.
- KMP, Compose, Koin, Gradle, ktlint, detekt e checkFeature viraram possibilidades, não regras.
- 100% de cobertura deixou de ser exigência global; vale a política do projeto.
- Movimentação automática de card virou conveniência opcional, não bloqueante.

## Melhorias Aplicadas

- `SKILL.md` ficou curto e orientado por decisões.
- Detalhes foram movidos para referências carregadas sob demanda.
- O workflow agora suporta Android, iOS, KMP, React Native, Flutter e stacks híbridas.
- O fluxo diferencia fonte de escopo, fonte de design, implementação, validação e publicação.
- A skill evita nomes, domínios, templates e componentes de empresa.
