# Validação

Use esta referência para escolher testes e checks sem assumir Gradle, KMP ou ferramentas específicas.

## Descobrir Comandos

Procure nesta ordem:

1. README, CONTRIBUTING, AGENTS.md, CLAUDE.md.
2. Scripts em `package.json`, `Makefile`, `Justfile`, `Taskfile`, `fastlane`, `gradlew`, `xcodebuild`, `flutter`.
3. CI em `.github/workflows`, `.gitlab-ci.yml`, Azure Pipelines ou Bitrise.
4. Padrões da stack.

## Checks Por Stack

### Android/KMP

- Testes: `./gradlew test`, `./gradlew allTests`, módulos específicos.
- Build: `./gradlew assembleDebug`, `./gradlew build`.
- Qualidade: ktlint, detekt, lint, checks customizados, conforme repo.

### iOS

- Testes: `xcodebuild test` com workspace/scheme detectados.
- Build: `xcodebuild build`.
- Qualidade: SwiftLint, SwiftFormat ou checks do projeto.

### React Native

- Testes: `npm test`, `yarn test`, `pnpm test`.
- Typecheck/lint: scripts do package manager.
- Build/smoke: comandos documentados do app.

### Flutter

- Testes: `flutter test`.
- Análise: `flutter analyze`.
- Build: `flutter build` apropriado ao alvo.

## Cobertura

Não exigir 100% por padrão. Use a política local:

- Se houver baseline de cobertura, não reduzir sem explicação.
- Cobrir lógica nova e caminhos de erro relevantes.
- Para bugfix, adicionar regressão quando prático.
- Se cobertura for impossível ou cara, explicar o risco.

## Falhas

Se um check falhar:

1. Mostrar o erro relevante.
2. Separar falha de código de falha de ambiente.
3. Corrigir automaticamente apenas quando for seguro.
4. Reexecutar o check focado.
5. Não prosseguir para PR/MR se a falha indicar regressão real.

## Teste Manual

Quando houver UI:

- Rodar em simulador/emulador/device quando disponível.
- Pedir confirmação do usuário se a validação manual depender da tela aberta.
- Incluir screenshots/vídeos no PR/MR quando o projeto pedir.
