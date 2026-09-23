# Estado atual — Adapta Cliente

- task_id: F1-T07
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-002-visao-financeira.md
- etapa: aguardando_autorizacao
- autorizacao_implementacao: ausente — o owner confirmou em 2026-09-23 18:33 que o mapeamento conta→DRE, a regra D = negativo/C = positivo/Variação = Realizado − Budget e o vínculo Budget V5→Filial 01 já estão aprovados; essa confirmação desbloqueia a análise, mas ainda não autoriza alterar o layout
- teste_humano: pendente
- verificacao_automatica: pendente — diagnóstico somente leitura: CT2 moeda-base 01 de junho/2026 tem 17.409 linhas, 87 contas, 73 centros de custo e 1.640 partidas sem centro; Budget V5/2026 tem 1.161 linhas de junho, 458 `APROVADO`, 84 contas e 42 centros, sem filial explícita no arquivo. Foram encontradas 473 chaves conta+centro comuns, 424 só no realizado e 351 só no budget. Decisões confirmadas: vínculo do Budget V5 com as informações realizadas de 2026 da CT2/Filial 01 — Atibaia; sinal D negativo, C positivo; variação = Realizado − Budget.
- aprendizado: pendente
- ultima_acao: bloqueios de F1-T07 considerados resolvidos por confirmação do owner; nenhum arquivo de produto ou origem alterado.
- proxima_acao: aguardar autorização explícita para implementar o layout Realizado × Budget por conta/centro, com período, filial, versão, origem, cobertura e exceções.
- atualizado_em: 2026-09-23T18:34:27-03:00
