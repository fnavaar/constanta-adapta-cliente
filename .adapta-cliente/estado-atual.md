# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: bloqueada
- autorizacao_implementacao: confirmada em 2026-09-23 16:13 — "siga com a publicação no layout do sistema"; não efetiva enquanto a F1-T01 permanecer bloqueada pelos gates da SPEC-1-001
- teste_humano: pendente
- verificacao_automatica: falhou — a pré-verificação da publicação encontrou o projeto Skip 52774 (Nova Página) não publicado (`isPublished=false`), versão 0.0.11 com alteração pendente em `.skip.config.json` e layout atual com formatação BRL padrão de 2 casas, sem escala R$ mil. A SPEC-1-001 continua exigindo contrato de campos/chaves aprovado por Rodolfo/TI, fixtures autorizadas, critério de reconciliação, saldo inicial/fechamento anterior e reconciliação da diferença técnica da CT2 de R$ 15.761,19. O escopo do Budget V5/2026 está confirmado exclusivamente para a Filial 01 — Atibaia; Matriz, Distribuição e Consolidado não entram no comparativo. CT2 validada em leitura: 18.159 linhas válidas, filial 01, competências de 01/06/2026 a 30/06/2026, 293 contas com movimento e UUIDs únicos. A regra de apresentação é `D` no balancete = negativo e `C` = positivo, aplicada também ao budget; variação = realizado - budget. A CT2 possui 11.311 linhas/partidas sem centro de custo; elas devem permanecer no comparativo com o rótulo `(sem centro de custo)`. Na reconciliação do DRE_Maio_2026_VF.xlsx, as linhas detalhadas do Ativo e Passivo fecham individualmente; o residual de R$ 0,50 foi aceito pelo cliente como diferença de arredondamento para fins de apresentação, sem alterar a origem contábil. A configuração desejada é 3 casas decimais e escala visual R$ mil, mas ela ainda não foi implementada nem publicada.
- aprendizado: pendente
- ultima_acao: pré-verificação da autorização de publicação, do estado da F1-T01 e do projeto Skip; publicação não executada, dashboard não alterado e nenhum dado financeiro publicado.
- proxima_acao: obter e registrar a reconciliação formal da CT2 de R$ 15.761,19 e o saldo inicial/fechamento anterior antes de liberar qualquer implementação ou publicação.
- atualizado_em: 2026-09-23T16:15:22-03:00
