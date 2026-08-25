# SPEC-1-002 — Visão reconciliável de DRE, balanço e budget versus realizado

**Fase:** 1  
**Status:** bloqueada — depende da importação validada e do mapeamento aprovado  
**Dono:** Rodolfo (Controladoria)  
**Origem:** Fase 1; D-002; RQ-002, RQ-003, RQ-005, RQ-006, RQ-008  
**Degrau:** construção mínima — primeira superfície utilizável, sem antecipar a análise avançada da Fase 3.

## Contexto e decisões fechadas

- DRE, balanço e budget são montados por balancete/CT2 e planilhas separadas.
- Controladoria deve consultar por período, reconciliar DRE/balanço e comparar budget-realizado quando completo, sempre com origem, versão, estado e exceções.
- DRE/balanço entram na primeira entrega; forecast, fluxo de caixa e índices ficam fora.
- **Bloqueios:** mapeamento conta→linha DRE, sinal/agregação, saldo inicial, regra de balanço, budget e totais de referência devem ser fornecidos/aprovados.

## Resultado observável

Com carga válida, Rodolfo demonstra DRE e balanço por período, seleciona matriz ou filial autorizada e confere totais com a referência. Budget parcial/ausente fica explicitamente sinalizado.

## Limites e dependências

- **Inclui:** DRE/balanço por período, regras aprovadas, comparação básica budget-realizado, matriz/filial, proveniência/estado e exceções.
- **Fora:** comparação avançada, gráficos/variações Fase 3, forecast, fluxo de caixa, índices, exportação e conexão direta.
- **Pré-condições:** versão válida da SPEC-1-001, mapeamento/referências assinados, filiais canônicas e política de saldo inicial.
- **Rollback:** retornar a versão anterior da carga sem alterar origem.

## Dados e regras

| Origem/destino | Contrato | Tratamento |
|---|---|---|
| versão válida → DRE/balanço | período, entidade, conta, valor/saldo, versão, estado | não mascarar dado parcial/inválido |
| mapeamento → linhas | conta, linha, sinal, ordem, agregação, vigência | conta ausente vira exceção |
| budget → comparação | conta, período, filial, valor, versão | parcial/indisponível se incompatível |

- **RN-201:** conta mapeada entra com sinal/agregação aprovados.
- **RN-202:** conta sem mapeamento não vira zero; abre exceção.
- **RN-203:** budget sem chave/versão não é comparação completa.
- **RN-204:** estado, origem e versão da carga ficam visíveis.

## Fluxo

1. Usuário autorizado escolhe período e entidade no escopo.
2. Sistema recupera versão válida, mapeamento aprovado e budget compatível.
3. Mostra DRE/balanço, totais, origem, status e exceções.
4. Rodolfo reconcilia e registra veredito.

## Instruções para o Ethos

1. Ler Fase 1, SPEC-1-001, contrato/mapeamento assinado e permissões.
2. Alterar somente consulta/cálculo aprovado.
3. Não alterar Proteus, origem, regras sem assinatura ou fases 2–5.
4. Ordem: validar dados/mapeamento → cenários → RED → visão mínima → GREEN → regressão.
5. Parar se sinal, agregação, saldo inicial ou chave de budget forem indefinidos.

## Checklist

- [ ] Mapeamento e referências aprovados.
- [ ] Cenários DRE, balanço, budget completo/parcial e conta sem mapeamento exercitados.
- [ ] Visão informa período, entidade, fonte, versão e estado.
- [ ] Divergência não explicada impede aceite.

## Critérios de aceite

- [ ] **CA-1-06:** DRE/balanço reproduzem referência sem divergência não explicada.
- [ ] **CA-1-07:** período/matriz/filial altera somente o recorte autorizado.
- [ ] **CA-1-08:** budget-realizado mostra chave/período/versão; ausência é parcial/indisponível.
- [ ] **CA-1-09:** conta sem mapeamento/saldo ausente vira exceção, não zero.
- [ ] **CA-1-10:** visão informa origem, versão e estado da carga.

## TDD da SPEC

| Etapa | Prova | Resultado | Evidência |
|---|---|---|---|
| RED | conta sem mapeamento, budget sem versão e saldo ausente | total não completo; falha CA-1-08/09 | suíte/captura |
| GREEN | fixture reconciliada | CA-1-06/07/08/10 passam | roteiro/IDs |
| REFACTOR/REGRESSÃO | alternar período/filial e consultar versão anterior | sem mistura; proveniência preservada | relatório |

## Tasks vinculadas

| ID | Task | Status |
|---|---|---|
| F1-T01 | Pacote de dados e referências | ☐ bloqueada |
| F1-T04 | Visão reconciliável | ☐ bloqueada |
| F1-T06 | Regressão integrada | ☐ bloqueada |
| F1-T07 | Mapeamento/reconciliação | ☐ bloqueada |