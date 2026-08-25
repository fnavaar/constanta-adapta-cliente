# SPEC-1-001 — Contrato de dados e importação controlada

**Fase:** 1  
**Status:** bloqueada — pré-condições de dados pendentes  
**Dono:** Rodolfo (Controladoria), com TI responsável pelo ambiente autorizado  
**Origem:** Fase 1; D-001, D-002; RQ-001, RQ-004, RQ-006, RQ-008  
**Degrau:** construção mínima — ponte XLSX/CSV antes de qualquer conector produtivo ao Proteus.

## Contexto e decisões fechadas

- CT2 e budget são trabalhados em Excel; API/SQL depende de validação de TI.
- A entrega recebe CT2/budget, valida e registra origem, período, versão e estado sem publicar dados inválidos.
- CT2 é a fonte prioritária; não há escrita no Proteus; carga inválida não substitui a última válida.
- **Bloqueio:** Rodolfo deve entregar amostra autorizada, dicionário CT2, budget versionado, chave conta-período-filial-versão, saldo inicial e regra de reconciliação. Sem isso, não criar schema nem implementar.

## Resultado observável

O champion seleciona arquivos autorizados, vê a validação antes da publicação e identifica origem, período, versão, status e exceções. Arquivo inválido é recusado e preserva a última versão válida.

## Limites e dependências

- **Inclui:** contrato de importação, prévia, validação, versionamento, registro, rejeição e evidência.
- **Fora:** API/SQL/ODBC produtivo, agendamento diário, transformação silenciosa, correção automática e escrita no ERP.
- **Pré-condições:** layout, campos, tipos, chaves, exemplos válidos/inválidos e critério de reconciliação aprovados por Rodolfo/TI.
- **Risco/plano B:** layout inconsistente bloqueia publicação; corrigir e reenviar preservando última versão válida.
- **Rollback:** descartar staging ou restaurar última carga válida por ID, com motivo/autor.

## Dados e regras

| Origem/destino | Contrato | Regra de erro |
|---|---|---|
| XLSX/CSV CT2 → staging | período, filial, conta, valor/saldo, ID de lançamento confirmados por dicionário | rejeitar coluna/tipo/período/filial inválidos |
| XLSX/CSV budget → staging | conta, período, filial, versão e valor | marcar parcial/indisponível sem chave/versão |
| staging → versão válida | origem, hash, período, versão, status, autor, hora e exceções | publicação atômica; manter última válida |

- **RN-101:** divergência de campo/tipo/período/filial recusa publicação.
- **RN-102:** hash repetido não cria nova versão.
- **RN-103:** conta sem mapeamento ou budget sem chave/versão não é completo.
- **RN-104:** só validação e reconciliação aprovadas publicam versão válida.

## Fluxo

1. Importador autorizado envia CT2 e budget; sistema cria staging com hash/metadados.
2. Sistema valida e apresenta prévia, totais, período, filiais e rejeições.
3. Rodolfo confronta totais com a origem.
4. Após conferência, publica versão; em rejeição preserva a última válida e mostra relatório.

## Instruções para o Ethos

1. Ler escopo definitivo Fase 1, esta SPEC e contrato aprovado.
2. Alterar somente importação/staging do repositório informado.
3. Não alterar Proteus, dados de origem, conectores diretos ou permissões produtivas.
4. Ordem: confirmar bloqueios → fixtures sanitizadas → RED → implementação mínima → GREEN → regressão/rollback.
5. Parar se campo, chave, reconciliação, acesso ou destino estiverem indefinidos.

## Checklist

- [ ] Contrato de campos/chaves aprovado por Rodolfo/TI.
- [ ] Fixtures válida, inválida e duplicada sanitizadas/autorizadas.
- [ ] Caminhos principal, parcial, inválido e duplicado exercitados.
- [ ] Falha preserva última válida sem dado sensível no log.

## Critérios de aceite

- [ ] **CA-1-01:** CT2 aprovada publicada com origem, hash/ID, período, versão, autor, data/hora e status.
- [ ] **CA-1-02:** coluna ausente, tipo inválido ou filial desconhecida é recusada antes da publicação.
- [ ] **CA-1-03:** arquivo repetido não cria nova versão; reprocessamento exige ID/justificativa.
- [ ] **CA-1-04:** budget sem chave/versão não aparece como comparação completa.
- [ ] **CA-1-05:** falha preserva última versão válida consultável.

## TDD da SPEC

| Etapa | Prova | Resultado | Evidência |
|---|---|---|---|
| RED | CT2 sem campo obrigatório e budget sem versão | falha RN-101/RN-103; nenhum publish | log sanitizado |
| GREEN | CT2 válida + budget com chave/versão | versão criada; CA-1-01/04 passam | ID, prévia, totais |
| REFACTOR/REGRESSÃO | duplicidade e falha | bloqueia duplicidade/preserva última válida | relatório |

**Erros obrigatórios:** arquivo vazio, tipo inválido, período/filial desconhecido, conta sem mapeamento, budget ausente, duplicidade e falha de publicação.

## Tasks vinculadas

| ID | Task | Status |
|---|---|---|
| F1-T01 | Consolidar pacote de dados | ☐ bloqueada |
| F1-T03 | Importação e validação em staging | ☐ bloqueada |
| F1-T06 | Regressão integrada | ☐ bloqueada |