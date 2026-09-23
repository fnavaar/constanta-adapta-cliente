# adapta-cliente
Estrutura operacional do cliente.

- 2026-09-23 · Rodolfo Cardoso · DEBUG task F1-T01: divergência de R$ 15.761,19 na CT2 → causa raiz: 750 registros de `Moeda Lancto = 02` foram somados à base real `Moeda Lancto = 01` → corrigido no dashboard; QA v0.0.13 passou e aguarda teste humano.
- 2026-09-23 · Rodolfo Cardoso · Task F1-T01 concluída: pacote CT2/Budget V5 aprovado no preview v0.0.13, com 17.409 linhas de moeda-base 01, 206/206 documentos balanceados, 0 divergências, R$ 0,00 e aprovação humana registrada; origem/Proteus não alterados.
- 2026-09-23 · Rodolfo Cardoso · F1-T07 bloqueada: análise da visão Realizado × Budget encontrou Budget V5 sem filial explícita e cobertura de 473 chaves conta+centro comuns, 424 só no realizado e 351 só no budget; aguarda mapeamento conta→DRE, regra de sinal/agregação e vínculo à Filial 01.
