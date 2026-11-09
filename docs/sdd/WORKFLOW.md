# Fluxo de trabalho SDD

O fluxo abaixo é obrigatório para funcionalidades e alterações não triviais. Ajustes triviais podem usar uma versão reduzida, desde que mantenham escopo, verificação e evidências proporcionais ao risco.

## 0. Discovery

Identificar o contexto real antes de propor soluções.

- Ler instruções, código, documentação, testes, scripts, CI e histórico relevantes.
- Confirmar stack, padrões, limites do sistema e comportamento atual.
- Mapear pessoas afetadas, dependências, riscos, dados sensíveis e áreas de regressão.
- Reproduzir problemas antes de sugerir correções.
- Registrar fatos, lacunas como `Não verificado` e perguntas em aberto.

**Saída:** contexto e riscos registrados em `requirements.md`.

## 1. Specify

Definir o problema e o resultado esperado sem antecipar implementação.

- Preencher escopo, objetivos, não objetivos, histórias e restrições.
- Documentar requisitos funcionais e não funcionais.
- Escrever critérios de aceitação observáveis e verificáveis.
- Esboçar a matriz e os cenários esperados em `acceptance-tests.md`, sem registrar resultados ainda não executados.
- Identificar casos de borda, segurança, acessibilidade e desempenho aplicáveis.

**Saída:** `requirements.md` revisável e cenários iniciais em `acceptance-tests.md`.

## 2. Design

Descrever como o sistema atenderá aos requisitos.

- Mapear componentes, responsabilidades, fluxos, dados e interfaces afetados.
- Preservar a arquitetura e os padrões existentes.
- Comparar alternativas e registrar trade-offs.
- Para interfaces, especificar hierarquia visual, responsividade, tipografia, acessibilidade, consistência e estados de interação.
- Para defeitos, aplicar reprodução, hipótese, causa raiz, correção mínima e teste de regressão.

**Saída:** `design.md` rastreável aos requisitos.

## 3. Plan

Transformar o design em unidades pequenas e verificáveis.

- Decompor tarefas por resultado observável.
- Identificar arquivos, dependências, ordem e riscos.
- Finalizar os cenários esperados em `acceptance-tests.md` e associar testes e evidências a cada tarefa.
- Evitar refatorações, dependências e mudanças fora do escopo.

**Saída:** `tasks.md` com sequência executável e `acceptance-tests.md` pronto para revisão antes da implementação.

## 4. Approval

Apresentar `requirements.md`, `design.md`, `tasks.md` e os cenários esperados de `acceptance-tests.md` ao usuário.

- Destacar decisões, riscos, lacunas e comandos previstos.
- Aguardar confirmação explícita antes de implementar funcionalidades.
- Se o escopo mudar materialmente, atualizar os documentos e solicitar nova aprovação.

**Gate:** nenhuma implementação de funcionalidade começa sem aprovação registrada em `tasks.md`.

## 5. Implement

Executar somente o escopo aprovado.

- Seguir a ordem e os limites do plano.
- Manter alterações pequenas, simples e revisáveis.
- Não instalar dependências ou alterar infraestrutura sem autorização específica.
- Atualizar a especificação quando surgir uma descoberta que invalide o plano; pausar para nova decisão quando necessário.

**Saída:** implementação e testes correspondentes ao plano aprovado.

## 6. Verify

Executar as verificações pertinentes ao repositório e ao risco da alteração.

- Rodar type checking, lint, build e testes existentes quando disponíveis.
- Executar os cenários de regressão e aceitação definidos antes da implementação.
- Preencher evidências, resultados observados e estados em `acceptance-tests.md`.
- Registrar comando, ambiente, resultado e falhas reais.
- Não substituir execução por expectativa nem declarar sucesso com verificações pendentes.

**Saída:** `acceptance-tests.md` atualizado com execuções e `verification.md` preenchido com evidências.

## 7. Review

Revisar o diff completo antes da entrega.

- Confirmar escopo, arquitetura, segurança, privacidade e regressões.
- Quando aplicável, revisar acessibilidade, responsividade, performance e estados de UX.
- Procurar arquivos acidentais, segredos, dependências e mudanças não solicitadas.
- Confirmar rastreabilidade entre requisito, tarefa, teste e evidência.

**Saída:** checklist de revisão concluído em `verification.md`.

## 8. Report

Entregar um relato factual e auditável.

- Resumir o que mudou e por quê.
- Listar arquivos e comandos executados.
- Apresentar resultados, evidências, limitações e itens não verificados.
- Indicar riscos residuais e próximos passos sem ampliar o escopo automaticamente.

**Saída:** relatório final coerente com `verification.md` e com o diff.
