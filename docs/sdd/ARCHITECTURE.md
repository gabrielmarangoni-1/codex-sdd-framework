# Arquitetura confirmada

Este documento registra somente fatos observados no repositório. Ele deve ser atualizado durante futuras fases de Discovery à medida que componentes reais forem adicionados. Informações não demonstradas por arquivos versionados são marcadas como `Não verificado`.

## Estado observado

Snapshot inspecionado em 9 de novembro de 2026, antes da instalação do SDD, no commit base `9d0d75bd1c561d9f9f34aaf306bfc14b3c810118`:

| Área | Evidência | Estado |
|---|---|---|
| Propósito | `README.md` descreve um framework de Spec-Driven Development para OpenAI Codex | Confirmado |
| Licença | `LICENSE` contém a licença MIT, copyright de 2026 | Confirmado |
| Código de produção | Nenhum arquivo de código presente | Não existente no snapshot |
| Linguagens e frameworks | Nenhum manifesto ou arquivo-fonte presente | Não verificado |
| Scripts e gerenciador de pacotes | Nenhum manifesto ou arquivo de scripts presente | Não verificado |
| Testes, lint, type checking e build | Nenhuma configuração ou suíte presente | Não verificado |
| Integração contínua | Nenhum workflow em `.github/workflows/` presente | Não verificado |
| Banco de dados e persistência | Nenhum esquema ou configuração presente | Não verificado |
| Autenticação e autorização | Nenhuma implementação presente | Não verificado |
| Infraestrutura e deploy | Nenhuma configuração presente | Não verificado |

## Estrutura documental SDD

```text
AGENTS.md                    # regras persistentes para agentes
docs/sdd/
├── README.md                # entrada e uso do sistema
├── WORKFLOW.md              # fases e gates do processo
├── QUALITY_GATES.md         # critérios de qualidade
├── ARCHITECTURE.md          # fatos técnicos confirmados
├── DECISIONS.md             # decisões duráveis do processo
├── templates/               # modelos reutilizáveis
└── specs/                   # uma pasta por alteração não trivial
```

## Restrições arquiteturais atuais

- A instalação SDD é exclusivamente documental.
- `README.md` e `LICENSE` existentes permanecem inalterados.
- Nenhuma tecnologia, comando, dependência ou arquitetura de produto é presumida.
- Futuras decisões de produto devem ser derivadas de evidências do repositório e registradas na especificação correspondente.

## Lacunas a confirmar futuramente

- Stack e versões suportadas.
- Comandos oficiais de desenvolvimento, testes, lint, type checking e build.
- Organização de módulos e limites de domínio.
- Estratégia de dados, segurança, observabilidade, CI e deploy.
- Padrões de frontend, acessibilidade, responsividade e performance, caso aplicáveis.
