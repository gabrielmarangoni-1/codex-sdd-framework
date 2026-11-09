# Registro de decisões SDD

Este arquivo registra decisões duráveis sobre o processo. Decisões de uma funcionalidade específica devem permanecer na respectiva pasta em `docs/sdd/specs/<feature-slug>/`.

## SDD-001 — Documentação versionada como memória persistente

- **Status:** aceita
- **Contexto:** sessões do Codex Cloud e conversas no ChatGPT podem ser retomadas em dispositivos diferentes, inclusive no iPhone.
- **Decisão:** requisitos, design, plano, testes de aceitação e verificação ficam versionados no repositório.
- **Consequência:** o trabalho pode ser retomado sem depender exclusivamente do histórico da conversa; os documentos precisam acompanhar mudanças aprovadas.

## SDD-002 — Uma pasta por alteração não trivial

- **Status:** aceita
- **Contexto:** documentos globais não oferecem rastreabilidade suficiente entre decisão e implementação.
- **Decisão:** usar `docs/sdd/specs/<feature-slug>/` com os cinco documentos definidos nos templates.
- **Consequência:** cada alteração mantém contexto, aprovação e evidências independentes; pequenas correções podem usar documentos proporcionais, sem omitir verificação.

## SDD-003 — Aprovação explícita antes de funcionalidades

- **Status:** aceita
- **Contexto:** implementar antes de alinhar escopo aumenta retrabalho e mudanças incidentais.
- **Decisão:** funcionalidades exigem aprovação explícita de requisitos, design e plano antes da implementação.
- **Consequência:** mudanças materiais posteriores exigem atualização dos documentos e nova decisão do usuário.

## SDD-004 — Evidência antes de conclusão

- **Status:** aceita
- **Contexto:** afirmações baseadas apenas em inspeção ou expectativa não demonstram que uma alteração funciona.
- **Decisão:** registrar comandos, resultados observados, limitações e revisão do diff em `verification.md`.
- **Consequência:** gates não executados ficam como `Não verificado`; sucesso não é declarado sem evidência correspondente.

## SDD-005 — Processo independente de ferramentas externas

- **Status:** aceita
- **Contexto:** skills e ferramentas podem variar entre ambientes.
- **Decisão:** as metodologias são descritas como práticas; disponibilidade de automações externas deve ser verificada, não presumida.
- **Consequência:** o fluxo continua utilizável por documentação mesmo quando uma skill ou integração específica não está disponível.
