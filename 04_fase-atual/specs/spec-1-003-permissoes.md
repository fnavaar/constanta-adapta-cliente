# SPEC-1-003 — Controle de acesso inicial por função e filial

**Fase:** 1  
**Status:** bloqueada — matriz de permissões pendente  
**Dono:** Rodolfo (negócio) e TI (acesso)  
**Origem:** Fase 1; D-004; RQ-007  
**Degrau:** dependência existente ou construção mínima — usar autenticação/autorização aprovada; não criar novo IdP por suposição.

## Contexto e decisões fechadas

- Consumidores: Controladoria, Financeiro e diretoria; papéis/escopos ainda precisam confirmação.
- Autenticados consultam apenas funções/filiais liberadas; carga/configuração ficam separadas da consulta.
- D-004 determina função e filial; acesso sem autorização é recusado; exportação é fase posterior.
- **Bloqueios:** matriz de papéis, usuários/grupos, filiais, concessão/revogação, autenticação e auditoria devem ser aprovados por Rodolfo/TI.

## Resultado observável

Usuário de Controladoria consulta recorte liberado; usuário sem filial recebe recusa sem dados; usuário de consulta não importa arquivos nem altera mapeamentos.

## Limites e dependências

- **Inclui:** autorização por função/filial, separação consulta/carga-configuração, recusa verificável e auditoria sanitizada.
- **Fora:** SSO novo, gestão corporativa de identidade, exportação, delegação, exceções e permissões F2–F5.
- **Pré-condições:** matriz assinada, identidade autorizada, filiais canônicas e contas/grupos de teste.
- **Rollback:** revogar regra/papel e restaurar política anterior; nunca abrir acesso global.

## Dados e regras

| Origem/destino | Contrato | Erro |
|---|---|---|
| identidade → app | ID, função, filiais e status | negar se atributo ausente |
| app → auditoria | usuário pseudonimizado, ação, escopo, resultado e hora | não logar valores/tokens |

- **RN-301:** função+filial autorizam somente ação liberada.
- **RN-302:** função/filial/status ausente nega antes de recuperar dados.
- **RN-303:** consulta tentando importar/configurar é negada.
- **RN-304:** escopo não resolvido nega por padrão e escala.

## Fluxo

1. Usuário autentica no mecanismo aprovado.
2. App resolve função/filiais na fonte de verdade.
3. Antes de cada ação aplica política ao recorte.
4. Permitido retorna somente escopo; negado não revela dado financeiro.
5. Resultado é auditado de forma sanitizada.

## Instruções para o Ethos

1. Ler D-004, matriz assinada e documentação do mecanismo aprovado.
2. Alterar somente autorização/testes no ambiente do cliente.
3. Não alterar IdP, usuários reais, Proteus, políticas corporativas ou dados sem TI.
4. Ordem: matriz → contas teste → RED → política mínima → GREEN → regressão cruzada.
5. Parar se função, filial, atributos, sessão ou retenção de log forem indefinidos.

## Checklist

- [ ] Matriz e aprovadores assinados.
- [ ] Contas/grupos de teste isolados/autorizados.
- [ ] Permitido, negado por filial/função e operação proibida exercitados.
- [ ] Logs sem dados financeiros, tokens ou credenciais.

## Critérios de aceite

- [ ] **CA-1-11:** autorizado acessa apenas filial/consolidado liberado.
- [ ] **CA-1-12:** sem escopo de filial recebe negação antes de retorno financeiro.
- [ ] **CA-1-13:** consulta não importa arquivo nem altera mapeamento.
- [ ] **CA-1-14:** atributo ausente nega por padrão.
- [ ] **CA-1-15:** tentativas permitidas/recusadas têm log sanitizado.

## TDD da SPEC

| Etapa | Prova | Resultado | Evidência |
|---|---|---|---|
| RED | sem filial e consulta tentando importar | acesso/operação negados | saída sanitizada |
| GREEN | contas com matriz aprovada | CA-1-11–15 passam | capturas/log |
| REFACTOR/REGRESSÃO | revogar filial/repetir sessão | acesso anterior deixa de funcionar | relatório + TI |

## Tasks vinculadas

| ID | Task | Status |
|---|---|---|
| F1-T02 | Matriz e contas de teste | ☐ bloqueada |
| F1-T05 | Autorização por função/filial | ☐ bloqueada |
| F1-T06 | Regressão integrada | ☐ bloqueada |