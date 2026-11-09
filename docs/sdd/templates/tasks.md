# Plano de tarefas — `<nome da alteração>`

> Requisitos: [requirements.md](requirements.md)
> Design: [design.md](design.md)
> Status: Rascunho | Aguardando aprovação | Aprovado | Em execução | Concluído
> Aprovação explícita: `<quem, data e referência da confirmação; vazio até aprovação>`

## 1. Restrições de execução

- Executar somente o escopo aprovado.
- Não instalar dependências, alterar infraestrutura ou ampliar permissões sem nova aprovação.
- Preservar padrões confirmados e pausar se uma descoberta invalidar o design.
- Registrar resultados reais em [verification.md](verification.md).

## 2. Mapa do plano

| Tarefa | Resultado verificável | Depende de | Requisitos/CA | Estado |
|---|---|---|---|---|
| T-01 | `<resultado>` | Nenhuma | `RF-001`, `CA-001` | Pendente |

## 3. Tarefas

### T-01 — `<título orientado a resultado>`

- **Objetivo:** `<um resultado independente>`
- **Dependências:** `<IDs ou “Nenhuma”>`
- **Arquivos previstos:** `<criar/modificar/testar caminhos exatos>`
- **Risco principal:** `<risco e mitigação>`

- [ ] Confirmar o comportamento inicial ou criar teste que falha pela razão esperada.
- [ ] Implementar a menor mudança que atende ao requisito.
- [ ] Executar os testes específicos e registrar o resultado.
- [ ] Revisar o diff da tarefa quanto a escopo, segurança e regressão.

**Evidência esperada:** `<comando e resultado que demonstram conclusão>`

**Definição de pronto:** `<condição objetiva; exemplo: CA-001 passa e nenhum arquivo fora da lista mudou>`

> Duplique a seção para T-02, T-03 e demais unidades independentes.

## 4. Verificações finais previstas

- **Type checking:** `<comando confirmado ou “Não disponível no repositório”>`
- **Lint:** `<comando confirmado ou “Não disponível no repositório”>`
- **Build:** `<comando confirmado ou “Não disponível no repositório”>`
- **Testes:** `<comandos confirmados>`
- **Aceitação/manual:** `<cenários em acceptance-tests.md>`
- **Revisão do diff:** `<comando e foco>`

`Não disponível no repositório` descreve o planejamento, não uma aprovação: se a verificação for pertinente, registre-a como `Não verificado` em `verification.md`, com motivo e risco residual.

## Gate de aprovação

- [ ] `requirements.md` está revisado.
- [ ] `design.md` está revisado.
- [ ] Tarefas, dependências e testes estão claros.
- [ ] Riscos e lacunas foram apresentados.
- [ ] O usuário aprovou explicitamente este plano e a aprovação foi registrada no cabeçalho.

**Não iniciar a implementação de funcionalidades enquanto o último item estiver desmarcado.**
