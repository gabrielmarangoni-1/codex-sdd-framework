# Testes de aceitação — `<nome da alteração>`

> Requisitos: [requirements.md](requirements.md)
> Plano: [tasks.md](tasks.md)
> Última atualização: `AAAA-MM-DD`

## 1. Matriz de cobertura

| Critério | Cenário | Tipo | Automação | Estado |
|---|---|---|---|---|
| `CA-001` | `TA-001` | Positivo | Automatizado/Manual | Não verificado |

## 2. Cenários

### TA-001 — `<resultado esperado>`

- **Cobre:** `CA-001`, `RF-001`
- **Tipo:** Positivo | Negativo | Borda | Regressão
- **Pré-condições:** `<estado necessário>`
- **Dado:** `<contexto>`
- **Quando:** `<ação>`
- **Então:** `<resultado observável>`
- **E:** `<verificação adicional, se necessária>`
- **Automação:** `<arquivo e nome do teste, ou justificativa para manual>`
- **Evidência:** `<preencher após execução>`

Exemplo curto: “Dado um usuário sem permissão, quando solicita o recurso, então recebe a resposta negada e nenhum dado protegido é retornado.”

## 3. Casos transversais aplicáveis

### Erros e casos de borda

- [ ] Entrada vazia, inválida, extrema ou duplicada.
- [ ] Indisponibilidade, timeout e recuperação.
- [ ] Concorrência, repetição ou idempotência, quando relevantes.

### Segurança e dados

- [ ] Caminhos permitidos e negados de autenticação/autorização.
- [ ] Validação de entrada e ausência de segredos/dados sensíveis nas saídas.

### Interface

- [ ] Teclado, foco visível, semântica, rótulos e contraste.
- [ ] Tamanhos de tela e texto pertinentes.
- [ ] Estados de carregamento, vazio, erro, sucesso e desabilitado.

## 4. Resultado das execuções

| Data/ambiente | Cenário | Resultado observado | Evidência | Responsável |
|---|---|---|---|---|
| `AAAA-MM-DD / <ambiente>` | `TA-001` | Passou/Falhou/Não aplicável/Não verificado | `<log, comando, ou motivo e risco residual>` | `<nome>` |

## Checklist de aceitação

- [ ] Cada critério de aceitação está coberto por ao menos um cenário.
- [ ] Cenários negativos, de borda e regressão foram incluídos conforme o risco.
- [ ] Resultados observados estão separados de resultados esperados.
- [ ] Falhas e limitações estão registradas sem serem ocultadas.
