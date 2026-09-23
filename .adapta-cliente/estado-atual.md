# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: bloqueada
- autorizacao_implementacao: ausente
- teste_humano: pendente
- verificacao_automatica: falhou — leitura da SPEC-1-001 confirmou que o pacote CT2/budget só pode avançar após contrato de campos e chaves aprovado por Rodolfo/TI, fixtures autorizadas e critério de reconciliação definido. Permanecem sem evidência formal: aprovação do contrato por Rodolfo/TI, saldo inicial/fechamento anterior para junho e reconciliação da diferença técnica da CT2 de R$ 15.761,19. O escopo do Budget V5/2026 está confirmado exclusivamente para a Filial 01 — Atibaia; Matriz, Distribuição e Consolidado não entram no comparativo. CT2 validada em leitura: 18.159 linhas válidas, filial 01, competências de 01/06/2026 a 30/06/2026, 293 contas com movimento e UUIDs únicos. A regra de apresentação é `D` no balancete = negativo e `C` = positivo, aplicada também ao budget; variação = realizado - budget. A CT2 possui 11.311 linhas/partidas sem centro de custo; elas devem permanecer no comparativo com o rótulo `(sem centro de custo)`. Na reconciliação do DRE_Maio_2026_VF.xlsx, as linhas detalhadas do Ativo e Passivo fecham individualmente; o residual de R$ 0,50 foi aceito pelo cliente como diferença de arredondamento para fins de apresentação, sem alterar a origem contábil. Valores de dashboard devem ser exibidos com 3 casas decimais e escala visual R$ mil. A aceitação do arredondamento e a escala visual não encerram os gates de publicação da SPEC-1-001.
- aprendizado: pendente
- ultima_acao: verificação somente leitura da SPEC-1-001, fase e estado; nenhum dado financeiro, dashboard ou publicação foi alterado.
- proxima_acao: obter evidência formal de aprovação do contrato e fechar saldo inicial/fechamento anterior e reconciliação da CT2 antes de qualquer implementação.
- atualizado_em: 2026-09-23T16:08:22-03:00
