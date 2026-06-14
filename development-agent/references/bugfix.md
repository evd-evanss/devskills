# Fluxo De Correção De Bug

Use este fluxo para testes falhando, builds quebrados, crashes, regressões, comportamento incorreto e incidentes parecidos com produção.

## Passos

1. Reproduzir ou localizar a falha a partir de logs, testes, screenshots, passos do usuário ou caminhos de código.
2. Separar sintoma de causa raiz.
3. Inspecionar a implementação próxima, testes e padrões recentes antes de editar.
4. Fazer a menor correção que resolva a causa raiz.
5. Adicionar ou atualizar cobertura de regressão quando for prático.
6. Rodar primeiro a verificação que falhava, depois verificações adjacentes relevantes.
7. Relatar causa raiz, correção, validação e qualquer incerteza restante.

## Regras De Proteção

- Não mascarar falhas enfraquecendo testes, a menos que o teste esteja comprovadamente errado.
- Não tratar falhas de sandbox, dependência, rede ou tooling nativo como falhas de código.
- Se a reprodução for cara, validar com unidade, tipo, build ou smoke check focado e declarar a limitação.
- Quando a primeira hipótese estiver errada, preservar o aprendizado e reler o caminho de código.

## Bom Resumo Final

```text
Corrigi o crash tratando o caminho de payload vazio antes do parsing.
Verifiquei com `pnpm test auth-parser`.
Risco restante: não consegui rodar a suíte de integração completa porque Docker não estava disponível.
```
