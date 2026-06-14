# Fluxo De Funcionalidade

Use este fluxo para novo comportamento, mudanças de produto, fluxos de UI, APIs, integrações e adições de modelo de dados.

## Passos

1. Identificar o resultado visível para o usuário e os critérios de aceite.
2. Encontrar funcionalidades similares existentes e copiar convenções locais.
3. Esboçar o menor caminho de implementação entre UI, domínio, API, persistência, testes e docs quando aplicável.
4. Implementar em fatias verticais finas quando a mudança atravessar camadas.
5. Adicionar validação para comportamento relevante e casos de borda.
6. Rodar verificações focadas, depois verificações mais amplas se contratos compartilhados mudaram.
7. Resumir a funcionalidade, superfície alterada e validação.

## Padroes De Design

- Preferir componentes, serviços, helpers e padrões existentes.
- Manter textos de UI concretos e orientados a ação.
- Incluir estados de carregamento, vazio, erro e desabilitado quando o fluxo naturalmente precisar deles.
- Evitar mudanças amplas de schema, roteamento ou gerenciamento de estado para uma funcionalidade estreita.
- Deixar pontos de extensão apenas quando o caso de uso de curto prazo for real.

## Checklist De Aceite

- O caminho principal de sucesso funciona.
- Estados esperados de falha e vazio são tratados.
- O comportamento existente permanece compatível.
- Testes ou verificações cobrem o caminho de maior risco.
