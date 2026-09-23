# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: em_correcao
- autorizacao_implementacao: confirmada em 2026-09-23 16:17 — "Faça a reconciliação e após encontrado a diferença ajuste-a"; alteração de apresentação confirmada para 2 casas decimais
- teste_humano: pendente
- verificacao_automatica: pendente — causa técnica identificada: os 750 registros de `Moeda Lancto = 02` estavam sendo somados à base em reais pelo validador/dashboard; a reconciliação independente mostrou que os 17.409 registros da moeda-base `01` fecham em R$ 0,00 de diferença nos 206 documentos. Correção em andamento no dashboard: segregar moeda 02, exibir base em reais e formatar valores em R$ mil com 2 casas. Nenhum lançamento, arquivo de origem ou registro no Proteus foi alterado.
- aprendizado: pendente
- ultima_acao: diagnóstico e correção em andamento no projeto Skip 52774; filtro da moeda-base 01 aplicado ao parser e componentes de apresentação atualizados no working tree, ainda sem QA/build/publicação.
- proxima_acao: executar QA completo do projeto Skip, revisar a prévia e aguardar teste humano antes de qualquer publicação.
- atualizado_em: 2026-09-23T16:33:50-03:00
