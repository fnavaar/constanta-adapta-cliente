# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: bloqueada
- autorizacao_implementacao: ausente
- teste_humano: pendente
- verificacao_automatica: falhou — CT2 validada em leitura: 18.159 linhas válidas, filial 01, competências de 01/06/2026 a 30/06/2026, 293 contas com movimento e UUIDs únicos. Pela regra de sinais aprovada, o movimento técnico de junho soma débitos de R$ 138.064.479,82 e créditos de R$ 138.048.718,63, diferença de R$ 15.761,19. O arquivo DRE_Maio_2026_VF.xlsx contém a aba `Maio 2026` com saldo anterior, débito, crédito, movimento e saldo atual por conta; o saldo atual consolidado informado é R$ 139.168.539,50 e a fórmula saldo anterior + débito + crédito = saldo atual está consistente nas linhas com saldo. O arquivo apresenta os blocos `Todas as filiais`, `Atibaia` e `Distribuição`; o cliente confirmou que a filial 01 da CT2 corresponde ao bloco `Atibaia`. O saldo de maio de Atibaia, R$ 113.408.440,91, é candidato a abertura de junho, ainda não publicado nem aceito. A aba `Balanço`/`Balanço Apresentação` confirma ativo de R$ 139.168.539,50 e passivo de R$ 139.168.539,00, diferença de R$ 0,50; o cliente determinou reconciliar essa diferença antes do aceite. Há 16 contas CT2 ausentes no balancete de maio consolidado e linhas de conta sem saldo atual, exigindo tratamento explícito.
- aprendizado: pendente
- ultima_acao: registro da decisão de escopo filial 01 = Atibaia e do tratamento obrigatório da diferença de R$ 0,50; nenhum arquivo financeiro foi copiado, publicado ou importado no repositório.
- proxima_acao: reconciliar e explicar a diferença de R$ 0,50 antes de aceitar o saldo de maio como abertura de junho.
- atualizado_em: 2026-09-23T12:23:55-03:00
