# Debug Summary — F1-T01 — 2026-09-23

**Task e problema:** F1-T01 — divergência líquida de R$ 15.761,19 na reconciliação da CT2 de junho/2026.

**Reprodução:** o cálculo original agrupava a CT2 e somava `Debito`/`Credito` sem filtrar `Moeda Lancto`. O CSV contém 17.409 registros em moeda `01` e 750 registros em moeda `02`. A soma conjunta produzia débito de R$ 138.064.479,82, crédito de R$ 138.048.718,63 e diferença de R$ 15.761,19. Considerando somente moeda `01`, os 206 documentos fecham sem diferença.

**Causa raiz:** registros de moeda secundária `02` foram tratados como reais pela métrica do dashboard. A diferença não era arredondamento e não exigia alteração de lançamento.

**Correção:** o parser passou a exigir `Moeda Lancto`, filtrar explicitamente a moeda-base `01`, manter os registros de moeda `02` segregados e auditáveis e exibir valores em R$ mil com 2 casas decimais. Nenhum arquivo de origem, lançamento ou registro do Proteus foi alterado.

**Verificação automática:** Skip projeto 52774, versão 0.0.13: setup, análise estática, build, integrações e teste passaram. Preview com CT2 e Budget V5 reais: 17.409 linhas, 206/206 documentos balanceados, 0 divergências, R$ 0,00 mil na moeda-base e 750 registros de moeda 02 segregados.

**Gate atual:** aguardando teste humano. Produção permanece não publicada.
