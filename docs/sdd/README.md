# Spec-Driven Development

Este diretório define o processo persistente de Spec-Driven Development (SDD) do repositório. O objetivo é transformar pedidos em requisitos verificáveis, decisões explícitas, tarefas pequenas e evidências reais antes de declarar uma alteração concluída.

O fluxo foi escrito para funcionar tanto no OpenAI Codex Cloud quanto em conversas do ChatGPT no iPhone: toda a memória relevante fica versionada no repositório, e não depende do histórico de uma única conversa.

## Documentos do sistema

- [Fluxo de trabalho](WORKFLOW.md): fases obrigatórias do discovery ao relatório final.
- [Quality gates](QUALITY_GATES.md): critérios mínimos de qualidade e evidência.
- [Arquitetura confirmada](ARCHITECTURE.md): estado técnico observado no repositório.
- [Decisões](DECISIONS.md): decisões duráveis sobre o processo SDD.
- Templates reutilizáveis:
  - [Requisitos](templates/requirements.md)
  - [Design](templates/design.md)
  - [Plano de tarefas](templates/tasks.md)
  - [Testes de aceitação](templates/acceptance-tests.md)
  - [Verificação](templates/verification.md)
- [`specs/`](specs/): uma pasta por funcionalidade ou alteração não trivial.

## Estrutura de uma especificação

Cada alteração não trivial deve usar um slug curto em kebab-case:

```text
docs/sdd/specs/<feature-slug>/
├── requirements.md
├── design.md
├── tasks.md
├── acceptance-tests.md
└── verification.md
```

Copie os arquivos de `docs/sdd/templates/` para a pasta da alteração. Distinga fatos observados de propostas, hipóteses, premissas e resultados esperados; nunca apresente estes últimos como evidência executada. Campos não aplicáveis devem ser marcados como `Não aplicável`, com justificativa breve; lacunas factuais ainda não confirmadas devem ser marcadas como `Não verificado`.

## Como iniciar uma tarefa

1. Peça ao agente para ler `AGENTS.md` e `docs/sdd/`.
2. Crie `docs/sdd/specs/<feature-slug>/` a partir dos templates.
3. Conclua Discovery, Specify, Design e Plan.
4. Revise os documentos e aprove explicitamente o plano.
5. Autorize a implementação somente depois da aprovação.
6. Exija o preenchimento de `verification.md` com comandos, resultados, limitações e revisão do diff.

Exemplo de instrução curta no ChatGPT: “Leia `AGENTS.md` e execute o fluxo SDD para `<objetivo>`. Faça discovery e apresente a especificação, o design e o plano antes de alterar código.”

## Metodologias incorporadas

O processo aplica princípios de Superpowers — brainstorming, decomposição e execução disciplinada —; Systematic Debugging; Verification Before Completion; e, quando houver interface, Frontend Design Premium e Impeccable. Esses nomes descrevem práticas de trabalho. A disponibilidade de skills ou ferramentas externas deve ser verificada no ambiente antes de seu uso e nunca presumida.
