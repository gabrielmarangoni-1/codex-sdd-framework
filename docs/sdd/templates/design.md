# Design — `<nome da alteração>`

> Requisitos: [requirements.md](requirements.md)
> Status: Rascunho | Em revisão | Aprovado
> Última atualização: `AAAA-MM-DD`

## 1. Resumo da solução

`<como a solução atende aos requisitos, em poucas frases>`

## 2. Estado atual confirmado

- **Componentes envolvidos:** `<caminhos e responsabilidades>`
- **Fluxo atual:** `<sequência observada>`
- **Padrões a preservar:** `<convenções confirmadas>`
- **Não verificado:** `<lacunas relevantes>`

## 3. Arquitetura proposta

| Componente | Responsabilidade | Alteração | Requisitos atendidos |
|---|---|---|---|
| `<nome/caminho>` | `<responsabilidade>` | `<mudança>` | `RF-001` |

## 4. Fluxos

1. `<origem ou ação>`
2. `<processamento>`
3. `<resultado, erro ou fallback>`

## 5. Dados e interfaces

- **Entradas:** `<formato, validação e origem>`
- **Saídas:** `<formato e consumidores>`
- **Persistência:** `<mudanças ou “Não aplicável”>`
- **Contratos/APIs:** `<mudanças ou “Não aplicável”>`
- **Compatibilidade/migração:** `<estratégia ou “Não aplicável”>`

## 6. Segurança, privacidade e falhas

- **Limites de confiança:** `<onde dados cruzam fronteiras>`
- **Autenticação/autorização:** `<impacto ou “Não aplicável”>`
- **Dados sensíveis:** `<tratamento ou “Não aplicável”>`
- **Erros e recuperação:** `<estados, mensagens, retry ou rollback>`

## 7. Interface e experiência, quando aplicável

- **Hierarquia visual e tipografia:** `<decisões>`
- **Responsividade:** `<breakpoints/condições confirmados>`
- **Acessibilidade:** `<semântica, teclado, foco, contraste e rótulos>`
- **Estados:** `<carregando, vazio, erro, sucesso, desabilitado>`
- **Consistência:** `<componentes e tokens existentes a reutilizar>`

## 8. Alternativas e trade-offs

| Alternativa | Vantagens | Desvantagens | Decisão |
|---|---|---|---|
| A — `<nome>` | `<vantagem>` | `<custo>` | Escolhida/Rejeitada: `<motivo>` |

## 9. Estratégia de testes

- **Unidade:** `<comportamentos>`
- **Integração:** `<fronteiras>`
- **Aceitação/regressão:** `<cenários>`
- **Verificação manual:** `<quando indispensável>`

## 10. Rollout, reversão e observabilidade

- **Rollout:** `<etapas ou “Não aplicável”>`
- **Reversão:** `<como desfazer com segurança>`
- **Observabilidade:** `<logs, métricas ou alertas, sem segredos>`

## Checklist de Design

- [ ] A solução é rastreável aos requisitos e critérios de aceitação.
- [ ] O design preserva padrões e arquitetura confirmados.
- [ ] Alternativas e trade-offs foram registrados.
- [ ] Fluxos de erro e casos de borda foram tratados.
- [ ] Segurança, dados, acessibilidade, responsividade e performance foram avaliados quando aplicáveis.
- [ ] A solução evita complexidade e dependências desnecessárias.
