# Estado atual — Adapta Cliente

- task_id: F1-T07
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-002-visao-financeira.md
- etapa: aguardando_teste_humano
- autorizacao_implementacao: confirmada em 2026-09-23 18:37 — "Autorizo a implementação do layout Realizado versus Budget por conta contábil conforme o plano apresentado"
- teste_humano: pendente
- verificacao_automatica: passou — Skip projeto 52774, versão 0.0.14, setup/análise estática/build/integrações/teste aprovados. Preview confirmou a região `Realizado versus Budget por conta contábil`, tabela com conta, descrição, realizado, budget, variação e status, valores em R$ mil com 2 casas, filtros de cobertura e busca/ordenação. A visão mostra amostra priorizada de 20 contas, com contadores de cobertura completa: 473 chaves comuns, 424 só realizado, 351 só budget, 458 linhas de Budget aprovado e 1.640 partidas realizadas sem centro de custo. Ausências aparecem como `—`, não como zero. Regras exibidas: D negativo, C positivo, variação = Realizado − Budget; período 06/2026; Filial 01 — Atibaia; Budget V5/2026.
- aprendizado: pendente
- ultima_acao: visão Realizado × Budget implementada no layout; QA v0.0.14 aprovado; preview verificado visualmente e filtro de cobertura acionado; produção permanece não publicada.
- proxima_acao: executar o teste humano da nova tabela no preview e informar se funcionou.
- atualizado_em: 2026-09-23T18:53:29-03:00
