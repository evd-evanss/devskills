# Design E Fonte Visual

Use esta referência quando a tarefa tiver UI ou interação visual.

## Fontes Possíveis

- Figma.
- Zeplin, Sketch, Adobe XD ou outro design tool.
- Screenshots.
- Protótipo navegável.
- Design tokens.
- Componentes existentes no app.
- Descrição textual do usuário.

## Fluxo

1. Identificar se há design anexado ou linkado ao ticket.
2. Se houver integração disponível, buscar specs, frames, estados e assets.
3. Se não houver integração, pedir screenshot/link ou seguir componentes existentes.
4. Mapear design para componentes reais do projeto.
5. Validar estados principais: loading, vazio, erro, sucesso, disabled.

## Design System

Não assumir Arco, Material, UIKit, SwiftUI, Chakra, Tailwind ou outro sistema.

Detectar:

- Pacotes de UI no projeto.
- Componentes compartilhados.
- Tokens de cor, tipografia, espaçamento e radius.
- Regras de acessibilidade.

Se o projeto não tiver design system claro, seguir a linguagem visual existente e manter a implementação simples.

## Entrega Visual

Para PR/MR com UI:

- Incluir screenshot, vídeo ou descrição do teste manual quando possível.
- Indicar diferenças conscientes em relação ao design.
- Não criar assets novos quando houver assets equivalentes no projeto.
