# Estado atual — Adapta Cliente

- task_id: F1-T01
- champion: Rodolfo Cardoso
- spec: 04_fase-atual/specs/spec-1-001-contrato-importacao.md
- etapa: aguardando_teste_humano
- autorizacao_implementacao: confirmada em 2026-09-23 16:17 — "Faça a reconciliação e após encontrado a diferença ajuste-a"; alteração de apresentação confirmada para 2 casas decimais
- teste_humano: pendente
- verificacao_automatica: passou — causa confirmada: 750 registros de `Moeda Lancto = 02` contaminavam a soma em reais; os 17.409 registros da moeda-base `01` fecham nos 206 documentos com diferença R$ 0,00. Skip projeto 52774, versão 0.0.13, passou em setup, análise estática, build, integrações e teste. Preview com CT2 e Budget V5 reais confirmou 17.409 linhas, 206/206 documentos balanceados, 0 divergências, R$ 0,00 mil e 750 registros de moeda 02 segregados. Dashboard formatado em R$ mil com 2 casas. Nenhum lançamento, arquivo de origem ou registro no Proteus foi alterado.
- aprendizado: capturado:06_notas/aprendizado-continuo/AP-2026-09-23-1638-moeda-base-ct2.md
- ultima_acao: correção aplicada e verificada no preview do Skip com os arquivos CT2 e Budget V5; debug summary, aprendizado e changelog registrados; produção permanece não publicada.
- proxima_acao: executar o teste humano no preview e informar se funcionou.
- atualizado_em: 2026-09-23T16:39:13-03:00
