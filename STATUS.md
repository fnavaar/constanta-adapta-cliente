# adapta-cliente

**Fase atual:** Fase 1 — contrato, staging e visão financeira controlada  
**Objetivo:** validar o pacote CT2/Budget, importar com segurança e preparar visão reconciliável de DRE/balanço e Realizado versus Budget.

## Estado executivo

- **Tasks da Fase 1:** 1 de 7 concluída (**14,3%**).
- **Concluída:** F1-T01 — pacote CT2 e Budget V5 aprovado no preview.
- **Task em análise/bloqueada:** F1-T07 — aprovar mapeamento/reconciliação para a visão Realizado versus Budget.
- **Layout atual:** mostra reconciliação CT2; o Budget é carregado apenas com nome/hash e ainda não alimenta uma tabela por conta.
- **Produção:** não publicada; o preview do projeto Skip 52774 está na versão 0.0.13.

## Diagnóstico da visão Realizado × Budget

- CT2 moeda-base `01`, junho/2026: 17.409 linhas, 87 contas, 73 centros de custo e 1.640 partidas sem centro.
- Budget V5/2026, junho: 1.161 linhas, 458 `APROVADO`, 84 contas e 42 centros de custo.
- A aba analítica do Budget não possui filial explícita; o vínculo com Filial 01 — Atibaia ainda precisa ser aprovado.
- Cobertura: 473 chaves conta+centro comuns, 424 somente no realizado e 351 somente no budget.
- A CT2 fecha em R$ 0,00 na moeda-base, mas isso é reconciliação de lançamentos e não total de despesas DRE.

## Bloqueios e próximos gates

- F1-T07 bloqueada até aprovação do mapeamento conta→linha DRE, natureza/sinal/agregação e vínculo Budget V5→Filial 01 — Atibaia.
- F1-T04 (atualização do layout) não será implementada antes desses gates.
- Não ativar comparativo mensal/loop sem fonte, métrica, cadência, permissões, recuperação e responsável aprovados.
