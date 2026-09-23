# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: bloqueada
- autorizacao_implementacao: ausente
- teste_humano: pendente
- verificacao_automatica: falhou — escopo confirmado: o Budget V5/2026 deve ser comparado exclusivamente com a Filial 01 — Atibaia; Matriz, Distribuição e Consolidado não entram no comparativo. CT2 validada em leitura: 18.159 linhas válidas, filial 01, competências de 01/06/2026 a 30/06/2026, 293 contas com movimento e UUIDs únicos. A regra de apresentação é `D` no balancete = negativo e `C` = positivo, aplicada também ao budget; variação = realizado - budget. O movimento total técnico invertido de junho é -R$ 15.761,19. No cruzamento junho/2026 por conta+centro, 586 chaves comuns com natureza válida resultaram em budget assinado de -R$ 1.058.456,09, realizado assinado de R$ 2.674.236,33 e variação de R$ 3.732.692,42; 226 chaves ficaram só no budget e 1.653 só no realizado. A CT2 tem 11.311 movimentos sem centro de custo. O budget analítico não informa filial explicitamente; o escopo Atibaia foi confirmado pelo cliente, mas a aplicação operacional dessa seleção no budget ainda precisa ser documentada/validada. Permanecem também a reconciliação dos R$ 0,50 do balanço e o tratamento de centro de custo ausente.
- aprendizado: pendente
- ultima_acao: registro da decisão de comparar o Budget somente com a Filial 01 — Atibaia; nenhuma implementação, publicação ou alteração dos arquivos de origem.
- proxima_acao: validar a seleção operacional do budget para Atibaia e definir o tratamento das linhas CT2 sem centro de custo antes de publicar destaques.
- atualizado_em: 2026-09-23T14:48:43-03:00
