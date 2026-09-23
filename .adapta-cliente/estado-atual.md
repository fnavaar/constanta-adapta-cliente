# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: bloqueada
- autorizacao_implementacao: ausente
- teste_humano: pendente
- verificacao_automatica: falhou — escopo confirmado: o Budget V5/2026 deve ser comparado exclusivamente com a Filial 01 — Atibaia; Matriz, Distribuição e Consolidado não entram no comparativo. CT2 validada em leitura: 18.159 linhas válidas, filial 01, competências de 01/06/2026 a 30/06/2026, 293 contas com movimento e UUIDs únicos. A regra de apresentação é `D` no balancete = negativo e `C` = positivo, aplicada também ao budget; variação = realizado - budget. O movimento total técnico invertido de junho é -R$ 15.761,19. No cruzamento junho/2026 por conta+centro, 586 chaves comuns com natureza válida resultaram em budget assinado de -R$ 1.058.456,09, realizado assinado de R$ 2.674.236,33 e variação de R$ 3.732.692,42; 226 chaves ficaram só no budget e 1.653 só no realizado. A CT2 possui 11.311 linhas/partidas sem centro de custo; elas devem permanecer no comparativo com o rótulo `(sem centro de custo)`. Na reconciliação do DRE_Maio_2026_VF.xlsx, as linhas detalhadas do Ativo e Passivo fecham individualmente; o saldo detalhado soma R$ 0,50. Não existe conta isolada com saldo exatamente R$ 0,50. O Ativo fecha em R$ 139.168.539,50 e o Passivo em R$ 139.168.539,00 porque a composição do Patrimônio Líquido usa `Lucro do Exercício` de R$ 673.167,04, puxado de `DRE_YTD S_ABS!N57`, enquanto o resultado líquido acumulado exibido em `DRE_YTD S_ABS!L57` é -R$ 782.168; o residual foi aceito pelo cliente como diferença de arredondamento para fins de apresentação, sem alterar a origem contábil. Valores de dashboard devem ser exibidos com 3 casas decimais. Pedido de publicar a prévia recebido em 2026-09-23, mas não executado: a SPEC-1-001 exige reconciliação e validação antes de publicar versão válida, e dados parciais/não reconciliados não podem ser publicados. A escala adicional solicitada para os números (“multiplique o número”) permanece indefinida; não será aplicada por inferência.
- aprendizado: pendente
- ultima_acao: registro da aceitação do residual de R$ 0,50 como arredondamento de apresentação e da preferência por 3 casas decimais; nenhum dado foi publicado e nenhuma implementação foi iniciada.
- proxima_acao: confirmar se a escala visual deve ser milhares (R$ mil), milhões (R$ mi) ou sem escala antes de alterar o dashboard.
- atualizado_em: 2026-09-23T16:03:55-03:00
