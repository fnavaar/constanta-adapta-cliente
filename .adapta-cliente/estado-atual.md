# Estado atual — Adapta Cliente

- task_id: F1-T07
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-002-visao-financeira.md
- etapa: aguardando_autorizacao
- autorizacao_implementacao: ausente para o novo recorte DRE — a autorização de 2026-09-23 18:37 cobria o plano anterior por conta contábil, antes da exclusão das contas de balanço
- teste_humano: pendente — roteiro da versão 0.0.14 invalidado pela alteração de escopo; não usar o teste anterior para aceite
- verificacao_automatica: pendente para o novo recorte — reanálise somente leitura concluída. Regra solicitada: considerar apenas contas cujo código começa com `3`. CT2 moeda 01/Filial 01/junho 2026: 1.746 linhas, 67 contas, 73 centros e 10 partidas sem centro; débitos técnicos R$ 1.754.622,97, créditos técnicos R$ 148.214,29 e líquido assinado R$ -1.606.408,68. Budget V5/junho 2026: 1.089 linhas, 412 `APROVADO`, 77 contas e 42 centros; bruto R$ 2.130.981,40 e aprovado R$ 457.588,70. Cobertura: 473 chaves comuns, 403 só realizado e 312 só budget. Quatro contas do Budget sem natureza D/C identificada na referência usada: 32223006, 33211007, 33211009 e 33213018; validar antes de publicar sinais/variações.
- aprendizado: pendente
- ultima_acao: escopo reanalisado somente para contas de resultado/DRE (`startswith(\"3\")`); layout e produção não foram alterados; versão 0.0.14 permanece não publicada.
- proxima_acao: aguardar autorização explícita para implementar o recorte DRE e confirmar o tratamento das quatro contas sem natureza D/C identificada.
- atualizado_em: 2026-09-23T18:58:00-03:00
