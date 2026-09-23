# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: bloqueada
- autorizacao_implementacao: ausente
- teste_humano: pendente
- verificacao_automatica: falhou — CT2 validada em leitura: 18.159 linhas válidas, filial 01, competências de 01/06/2026 a 30/06/2026, 293 contas com movimento e UUIDs únicos. Pela regra de sinais aprovada, o movimento técnico de junho soma débitos de R$ 138.064.479,82 e créditos de R$ 138.048.718,63, diferença de R$ 15.761,19. O arquivo DRE_Maio_2026_VF.xlsx contém a aba `Maio 2026` com saldo anterior, débito, crédito, movimento e saldo atual por conta; o saldo atual consolidado informado é R$ 139.168.539,50 e a fórmula saldo anterior + débito + crédito = saldo atual está consistente nas linhas com saldo. A aba `Balanço`/`Balanço Apresentação` confirma ativo de R$ 139.168.539,50 e passivo de R$ 139.168.539,00, diferença de R$ 0,50. O arquivo é `Todas as filiais`, enquanto a CT2 é filial 01; não é seguro usar o consolidado como abertura da filial 01. Há 16 contas CT2 ausentes no balancete de maio consolidado e 10 linhas de conta sem saldo atual, exigindo tratamento explícito.
- aprendizado: pendente
- ultima_acao: análise somente leitura do DRE/balancete de maio; nenhum arquivo financeiro foi copiado, publicado ou importado no repositório.
- proxima_acao: confirmar se a CT2 filial 01 deve ser comparada ao bloco `Atibaia`/escopo correspondente e fornecer ou aprovar o mapeamento da filial 01 para o saldo de maio; também obter o veredito sobre a diferença de R$ 0,50 do balanço.
- atualizado_em: 2026-09-23T12:20:08-03:00
