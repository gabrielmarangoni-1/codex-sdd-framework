# Verificação — `<nome da alteração>`

> Requisitos: [requirements.md](requirements.md)
> Testes de aceitação: [acceptance-tests.md](acceptance-tests.md)
> Data: `AAAA-MM-DD`
> Ambiente/commit: `<ambiente e SHA>`

## 1. Resumo do que foi verificado

`<escopo efetivamente verificado; não confundir com o escopo planejado>`

## 2. Comandos e resultados reais

| Verificação | Comando exato | Resultado observado | Estado |
|---|---|---|---|
| Type checking | `<comando>` | `<saída resumida e código de saída>` | Passou/Falhou/Não aplicável/Não verificado |
| Lint | `<comando>` | `<saída resumida e código de saída>` | `<estado>` |
| Build | `<comando>` | `<saída resumida e código de saída>` | `<estado>` |
| Testes | `<comando>` | `<quantidade, falhas e código de saída>` | `<estado>` |

Não escreva “passou” sem executar. Use `Não aplicável — <justificativa>` somente quando a categoria não for pertinente à alteração. Se a verificação for pertinente, mas o comando não existir, não estiver configurado ou não puder ser executado, registre `Não verificado — <motivo e risco residual>`.

## 3. Critérios de aceitação

| Critério | Cenário/evidência | Resultado |
|---|---|---|
| `CA-001` | `TA-001 — <evidência>` | Passou/Falhou/Não verificado |

## 4. Quality gates

| Gate | Estado | Evidência ou justificativa |
|---|---|---|
| Requisitos e escopo | `<estado>` | `<referência>` |
| Qualidade automatizada | `<estado>` | `<referência>` |
| Regressão e aceitação | `<estado>` | `<referência>` |
| Segurança e dados | `<estado>` | `<referência>` |
| Interface e acessibilidade | `<estado>` | `<referência>` |
| Performance e dependências | `<estado>` | `<referência>` |
| Revisão final | `<estado>` | `<referência>` |

## 5. Revisão do diff

- **Arquivos alterados:** `<lista ou referência ao diff>`
- **Mudanças fora do escopo:** Nenhuma | `<descrever e justificar>`
- **Código de produção não planejado:** Nenhum | `<descrever>`
- **Segredos ou dados sensíveis:** Não encontrados | `<achado e ação>`
- **Dependências/lockfiles:** Inalterados | `<descrever>`
- **Compatibilidade e regressões:** `<resultado da revisão>`

## 6. Verificações específicas, quando aplicáveis

- **Segurança/autorização:** `<evidência ou “Não aplicável — motivo”>`
- **Acessibilidade/responsividade:** `<evidência ou “Não aplicável — motivo”>`
- **Performance:** `<evidência ou “Não aplicável — motivo”>`
- **Observabilidade:** `<evidência ou “Não aplicável — motivo”>`

## 7. Limitações e riscos residuais

- `<teste não executado, limitação do ambiente ou risco restante>`

## 8. Conclusão baseada em evidências

`<o que pode ser afirmado com base nas evidências acima; não extrapolar>`

## Checklist final

- [ ] Comandos e resultados correspondem a execuções reais.
- [ ] Critérios de aceitação estão rastreados.
- [ ] O diff completo foi revisado.
- [ ] Segurança, acessibilidade, responsividade e performance foram avaliadas quando aplicáveis.
- [ ] Limitações e riscos residuais estão explícitos.
- [ ] Nenhum sucesso é declarado sem evidência.
