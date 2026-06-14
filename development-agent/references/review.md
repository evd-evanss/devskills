# Fluxo De Revisão

Use este fluxo para revisão de código, PR, design técnico ou avaliação de risco.

## Postura De Revisao

Comece pelos achados. Priorize corretude, regressões, segurança, perda de dados, concorrência, quedas de performance, acessibilidade e testes ausentes. Comentários de estilo são secundários, a menos que afetem manutenção ou violem convenções claras do projeto.

## Passos

1. Entender o comportamento pretendido e os arquivos alterados.
2. Inspecionar testes e alegações de validação.
3. Revisar primeiro as fronteiras de risco: entradas, autenticação, persistência, migrações, chamadas de rede, fluxos assíncronos, transições de estado e tratamento de erro.
4. Checar compatibilidade retroativa e casos de borda.
5. Relatar achados em ordem de severidade com referências de arquivo e linha.
6. Se não houver achados, dizer isso claramente e mencionar risco residual ou verificações não executadas.

## Formato De Achado

```text
[P1] Proteger contra tenant ausente antes de consultar faturas
file/path.ts:42
Quando tenantId está undefined, esta query agora retorna todas as faturas. Adicione um erro antecipado ou fallback escopado antes de chamar o repositório.
```

## Evitar

- Não reescrever o PR em modo de revisão, a menos que o usuário peça correções.
- Não enterrar achados sérios abaixo de resumos.
- Não chamar uma lacuna de teste de bug, a menos que ela crie risco real.
