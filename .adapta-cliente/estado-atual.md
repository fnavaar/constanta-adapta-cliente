# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: bloqueada
- autorizacao_implementacao: ausente
- teste_humano: pendente
- verificacao_automatica: falhou — CT2 validada em leitura: 18.159 linhas válidas, filial 01, competências de 01/06/2026 a 30/06/2026, 293 contas com movimento e UUIDs únicos. Pela regra de sinais aprovada, o movimento técnico de junho soma débitos de R$ 138.064.479,82 e créditos de R$ 138.048.718,63, diferença de R$ 15.761,19. O arquivo DRE_Maio_2026_VF.xlsx contém a aba `Maio 2026` com saldo anterior, débito, crédito, movimento e saldo atual por conta; o saldo atual consolidado informado é R$ 139.168.539,50 e a fórmula saldo anterior + débito + crédito = saldo atual está consistente nas linhas com saldo. O arquivo apresenta os blocos `Todas as filiais`, `Atibaia` e `Distribuição`; o cliente confirmou que a filial 01 da CT2 corresponde ao bloco `Atibaia`. O saldo de maio de Atibaia, R$ 113.408.440,91, é candidato a abertura de junho, ainda não publicado nem aceito. A aba `Balanço`/`Balanço Apresentação` confirma ativo de R$ 139.168.539,50 e passivo de R$ 139.168.539,00, diferença de R$ 0,50; o cliente determinou reconciliar essa diferença antes do aceite. Há 16 contas CT2 ausentes no balancete de maio consolidado e linhas de conta sem saldo atual, exigindo tratamento explícito. O cliente definiu a chave mensal do budget como `Filial | Conta contábil | Centro de custo (quando aplicável) | Mês/Ano | Versão do Budget`; a competência mensal é a chave temporal principal. Trimestre, YTD e ano serão consolidações dos meses correspondentes, sem chaves temporais adicionais. O budget V5/2026 contém meses e visões de Matriz/Filial/Consolidado e um plano de contas, mas não expõe uma tabela normalizada de valores por centro de custo; o de/para e a aplicabilidade do centro de custo ainda precisam ser validados.
- aprendizado: pendente
- ultima_acao: registro da chave do budget e das janelas mensal, trimestral, YTD e anual; nenhuma implementação ou publicação foi realizada.
- proxima_acao: reconciliar a diferença de R$ 0,50 e validar a aplicação da chave do budget no de/para conta/centro de custo/filial.
- atualizado_em: 2026-09-23T12:28:58-03:00
