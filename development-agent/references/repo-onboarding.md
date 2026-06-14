# Onboarding De Repositório

Use isto ao iniciar em um repositório desconhecido ou quando o pedido do usuário depender das convenções do projeto.

## Orientacao Rapida

1. Listar arquivos e diretorios de topo.
2. Ler manifests de pacote/build e arquivos de setup parecidos com README.
3. Buscar implementações existentes similares ao pedido.
4. Identificar comandos de teste, lint, formatação, build e dev.
5. Checar se a worktree está suja antes de editar quando houver controle de versão.

## Sinais Para Capturar

- Linguagem, framework, gerenciador de pacotes e ferramenta de build.
- Fronteiras da app e responsabilidades: frontend, backend, mobile, packages, módulos.
- Stack de testes e convenções de nomes.
- Onde vivem utilitários compartilhados, componentes de UI, serviços e tipos.
- Estilo existente para erros, logs, configuração e acesso a dados.

## Quando Parar E Perguntar

Pergunte ao usuário apenas quando uma decisão não puder ser inferida e uma suposição errada seria custosa, como mudanças destrutivas de dados, quebras de API pública, serviços pagos, credenciais ou publicação.
