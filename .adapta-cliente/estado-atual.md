# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: bloqueada
- autorizacao_implementacao: ausente
- teste_humano: pendente
- verificacao_automatica: falhou — CT2 validada em leitura: 18.159 linhas válidas, filial 01, competências de 01/06/2026 a 30/06/2026, 293 contas com movimento e UUIDs únicos. A regra de apresentação foi atualizada pelo cliente: `D` no balancete = negativo e `C` = positivo; a mesma regra é aplicada ao budget. Para a prévia, débitos/Partida Dobrada no lado débito receberam sinal negativo, créditos/Partida Dobrada no lado crédito receberam sinal positivo, e o budget recebeu o sinal da natureza D/C da conta no balancete Atibaia; variação = realizado - budget. O movimento total técnico invertido de junho é -R$ 15.761,19. No cruzamento junho/2026 por conta+centro, 586 chaves comuns com natureza válida resultaram em budget assinado de -R$ 1.058.456,09, realizado assinado de R$ 2.674.236,33 e variação de R$ 3.732.692,42; 226 chaves ficaram só no budget e 1.653 só no realizado. A CT2 tem 11.311 movimentos sem centro de custo. O budget analítico não informa filial explicitamente; por isso as variações continuam prévias técnicas, não aceitas/publicadas. Permanecem também o vínculo do budget com Atibaia, tratamento de centro de custo ausente e reconciliação dos R$ 0,50 do balanço.
- aprendizado: pendente
- ultima_acao: recalculo somente leitura da prévia com a regra D negativo/C positivo aplicada ao realizado e ao budget; nenhuma implementação, publicação ou alteração dos arquivos de origem.
- proxima_acao: validar o vínculo do budget analítico com a filial 01/Atibaia e o tratamento das linhas sem centro de custo antes de publicar destaques.
- atualizado_em: 2026-09-23T14:44:29-03:00
