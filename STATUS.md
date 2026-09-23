# adapta-cliente

**Fase atual:** Fase 1 — contrato, staging e visão financeira controlada  
**Objetivo:** validar o pacote CT2/Budget, importar com segurança e preparar visão reconciliável de DRE/balanço e Realizado versus Budget.

## Estado executivo

- **Tasks da Fase 1:** 1 de 7 concluída (**14,3%**).
- **Concluída:** F1-T01 — pacote CT2 e Budget V5 aprovado no preview.
- **Ativa:** nenhuma; fechamento de F1-T01 confirmado.
- **Próximo trabalho:** analisar a próxima task elegível, sem iniciar implementação nesta conclusão.
- **Produção:** não publicada; o preview do projeto Skip 52774 está na versão 0.0.13.

## Evidências F1-T01

- CT2 de junho/2026 carregada e validada no preview.
- Moeda-base `01`: 17.409 linhas, 206/206 documentos balanceados, 0 divergências, diferença R$ 0,00.
- Moeda `02`: 750 registros segregados e auditáveis, fora da soma em reais.
- Dashboard: escala R$ mil com 2 casas decimais.
- Budget V5 carregado no fluxo de fontes.
- QA da versão 0.0.13: setup, análise estática, build, integrações e teste passaram.
- Teste humano aprovado por Rodolfo em 2026-09-23: “Teste humano F1-T01: funcionou; pode concluir a task e seguir para o DRE Realizado versus Budget”.
- Origem contábil e Proteus não foram alterados.

## Bloqueios e limites

- F1-T02..F1-T07 permanecem bloqueadas conforme pré-condições da fase.
- Não iniciar o DRE Realizado versus Budget na mesma rodada do fechamento; requer nova análise/autorização de task.
- Não ativar comparativo mensal/loop sem fonte, métrica, cadência, permissões, recuperação e responsável aprovados.
