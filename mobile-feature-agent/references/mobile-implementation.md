# Implementação Mobile

Use esta referência para adaptar o fluxo à stack real do projeto.

## Detectar Stack

Procure sinais:

- Android nativo: `build.gradle`, `settings.gradle`, `AndroidManifest.xml`, Kotlin/Java.
- iOS nativo: `.xcodeproj`, `.xcworkspace`, `Package.swift`, Swift/Objective-C.
- KMP: `commonMain`, `androidMain`, `iosMain`, Kotlin Multiplatform plugin.
- React Native: `package.json`, `ios/`, `android/`, Metro, Expo.
- Flutter: `pubspec.yaml`, `lib/`, `android/`, `ios/`.

## Camadas

Não imponha Clean Architecture se o projeto não usar. Identifique a organização local:

- UI/presentation.
- State management/ViewModel/Presenter/Controller/Store.
- Domain/use cases/services.
- Data/repository/API/local storage.
- DI/composition/root modules.
- Navigation/routing.

Quando houver arquitetura clara, siga-a. Quando não houver, faça a menor mudança coesa.

## Tipos De Tarefa

### UI Completa

Use quando houver tela, design, fluxo visual ou interação.

- Reutilizar componentes do projeto.
- Seguir design system local, se existir.
- Implementar estados de loading, vazio, erro e sucesso quando fizer sentido.
- Adicionar screenshots ou notas de teste manual ao PR/MR.

### Sem UI

Use quando a tarefa for API, integração, data/domain, service, bug interno ou preparação técnica.

- Não criar telas, navigation ou ViewModels se o escopo não pedir.
- Focar em contratos, mappers, repositories, use cases, services ou stores existentes.
- Validar com testes unitários e build/compilação.

### Refatoração

- Preservar comportamento.
- Fazer mudanças pequenas e revisáveis.
- Rodar checks antes e depois quando possível.
- Não misturar refatoração com feature sem necessidade.

## Design System

Não mencione componentes específicos de empresa. Para componentes visuais:

1. Buscar componentes locais equivalentes.
2. Verificar tokens, tema, espaçamento, tipografia e ícones usados no projeto.
3. Se não houver componente, implementar de forma mínima e consistente.
4. Se o usuário especificar um design system, seguir esse design system.

## Migração De Plataforma

Para migrações Android/iOS/KMP/RN/Flutter:

- Identificar APIs específicas da plataforma.
- Procurar equivalente multiplataforma ou abstração existente.
- Evitar trocar design system ou arquitetura sem necessidade.
- Validar cada plataforma afetada quando houver tooling disponível.
