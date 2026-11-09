# Quality gates

Os gates são proporcionais ao risco e à stack confirmada durante Discovery. Um gate só pode ser marcado como aprovado com evidência executada.

## Estados permitidos

- `Passou`: a verificação foi executada e a evidência atende ao critério.
- `Falhou`: a verificação foi executada e a evidência não atende ao critério.
- `Não aplicável`: o critério não é pertinente à alteração; exige justificativa.
- `Não verificado`: o critério é pertinente, mas não foi executado ou não está configurado; exige motivo e registro do risco residual.

## Gate 1 — Requisitos e escopo

- Requisitos funcionais e não funcionais estão identificados.
- Critérios de aceitação são objetivos e rastreáveis.
- Objetivos, não objetivos, restrições e riscos estão explícitos.
- O diff não contém alterações fora do escopo aprovado.

## Gate 2 — Qualidade automatizada existente

- Os comandos de type checking, lint, build e testes foram descobertos no repositório, sem serem presumidos.
- Todas as verificações existentes pertinentes foram executadas.
- Novos testes cobrem o comportamento alterado e casos de borda relevantes.
- Falhas preexistentes são separadas de regressões introduzidas e documentadas com evidência.

## Gate 3 — Regressão e aceitação

- Cada critério de aceitação possui ao menos um cenário em `acceptance-tests.md`.
- Caminhos afetados têm teste de regressão automatizado quando viável.
- Verificações manuais informam ambiente, passos, resultado esperado e observado.
- Correções de defeitos demonstram reprodução anterior e ausência da falha após a correção.

## Gate 4 — Segurança e proteção de dados

Quando aplicável:

- Autenticação e autorização são verificadas em caminhos permitidos e negados.
- Entradas, saídas, uploads e integrações são validados nos limites de confiança.
- Segredos e dados pessoais não aparecem em código, diff, logs, fixtures ou documentação.
- Armazenamento, transmissão, retenção e exposição de dados seguem os padrões confirmados do projeto.
- Dependências e alterações de permissão têm justificativa e impacto revisados.

## Gate 5 — Interface, acessibilidade e responsividade

Quando aplicável:

- Hierarquia visual, tipografia, espaçamento e componentes permanecem consistentes.
- Fluxos contemplam carregamento, vazio, erro, sucesso, desabilitado e foco.
- Navegação por teclado, foco visível, semântica, rótulos e contraste são verificados.
- Layout e conteúdo são testados nos breakpoints e tamanhos de texto pertinentes.
- Mudanças são avaliadas quanto a clareza, feedback, prevenção e recuperação de erros.

## Gate 6 — Performance e dependências

Quando aplicável:

- O impacto em tempo de resposta, renderização, memória, rede e tamanho de artefatos é avaliado.
- Não há consultas, recomputações ou transferências evitáveis introduzidas.
- Toda nova dependência tem necessidade, manutenção, licença, segurança e custo de bundle avaliados.
- Dependências externas só são adicionadas com aprovação explícita.

## Gate 7 — Revisão final e evidências

- O diff completo foi revisado e corresponde ao plano aprovado.
- Não há arquivos gerados, temporários, segredos ou alterações incidentais.
- `verification.md` contém comandos exatos, códigos de saída ou resultados observados e data da verificação.
- Limitações, testes não executados e riscos residuais estão explícitos.
- A conclusão usa apenas afirmações sustentadas por evidências; sem evidência, não há declaração de sucesso.
