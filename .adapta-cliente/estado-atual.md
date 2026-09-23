# Estado atual — Adapta Cliente

- task_id: F1-T07
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-002-visao-financeira.md
- etapa: bloqueada
- autorizacao_implementacao: ausente — análise da visão Realizado versus Budget concluída; nenhuma alteração de produto autorizada
- teste_humano: pendente
- verificacao_automatica: pendente — diagnóstico somente leitura: CT2 moeda-base 01 de junho/2026 tem 17.409 linhas, 87 contas, 73 centros de custo e 1.640 partidas sem centro; Budget V5/2026 tem 1.161 linhas de junho, 458 `APROVADO`, 84 contas e 42 centros, mas a aba analítica não possui filial explícita. Foram encontradas 473 chaves conta+centro comuns, 424 só no realizado e 351 só no budget. O total líquido da CT2 é R$ 0,00 por equilíbrio débito/crédito e não representa o total de despesas DRE. A implementação oficial está bloqueada até aprovação do mapeamento conta→linha DRE, natureza/sinal/agregação e vínculo do Budget V5 à Filial 01 — Atibaia.
- aprendizado: pendente
- ultima_acao: análise da SPEC-1-002, layout atual e arquivos CT2/Budget; confirmado que o layout atual só mostra reconciliação CT2, enquanto `handleBudget` registra nome/hash sem ler valores e não existe tabela Realizado × Budget por conta.
- proxima_acao: obter a evidência/aprovação do mapeamento conta→DRE, regra de sinal/agregação e vínculo do budget à Filial 01; depois analisar F1-T04 para atualizar o layout.
- atualizado_em: 2026-09-23T17:38:19-03:00
