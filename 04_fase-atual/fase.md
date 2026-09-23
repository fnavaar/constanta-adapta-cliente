# Fase 1 — Tarefas gerais

**Regra de execução:** gerar tasks não autoriza implementação. Execute no máximo **uma** task elegível por vez; ao concluí-la, rode a prova indicada e aguarde teste/autorização humana antes da próxima.

## Tasks

| ID | Task | Dono | SPEC | Critério | Recorte da prova | Evidência esperada | Pré-condições | Status |
|---|---|---|---|---|---|---|---|---|
| F1-T01 | Consolidar pacote CT2 e budget | Rodolfo / TI | SPEC-1-001 | pacote aprovado | Pré-condições + RED | pacote e aprovação | ambiente seguro | ✅ concluída — 2026-09-23 |
| F1-T02 | Consolidar permissões e contas de teste | Rodolfo / TI | SPEC-1-003 | matriz aprovada | Pré-condições + RED | matriz e confirmação | identidade autorizada | ☐ bloqueada |
| F1-T03 | Implementar importação em staging | Executor técnico | SPEC-1-001 | validação segura | CA-1-01..05 | testes e prévia | F1-T01 | ☐ bloqueada |
| F1-T04 | Implementar visão reconciliável | Executor técnico | SPEC-1-002 | totais conferem | CA-1-06..10 | roteiro e captura | F1-T03/F1-T07 | ☐ bloqueada |
| F1-T05 | Aplicar autorização | Executor técnico | SPEC-1-003 | recorte segregado | CA-1-11..15 | suíte e logs | F1-T02 | ☐ bloqueada |
| F1-T06 | Regressão e demonstração | Rodolfo / Executor | SPEC-1-002 | roteiro integrado passa | regressão F1 | relatório/veredito | F1-T03..05 | ☐ bloqueada |
| F1-T07 | Aprovar mapeamento/reconciliação | Rodolfo | SPEC-1-002 | mapeamento assinado | Pré-condições + RED | referências aprovadas | F1-T01 | ☐ bloqueada |

## Não autorizado nesta fase

Conectar ao Proteus, publicar em produção, ativar carga diária, criar/exportar dados financeiros fora do ambiente aprovado, ativar loops/agentes ou iniciar Fase 2.
