# CORE LOGIC – Sistema de Atribuição de Vendas

Este documento define as regras centrais do sistema.
Nenhuma implementação pode contrariar este arquivo.

---

## 1. Origem do Pedido

Todo pedido nasce com:
- origem (anúncio, orgânico, indicação, recorrente)
- campanha
- data e hora
- responsável (representante ou automático)

A origem nunca é sobrescrita, apenas complementada.

---

## 2. Cliente

- Um cliente pode ter múltiplos pedidos
- O primeiro pedido define a origem principal do cliente
- Recompras mantêm vínculo com a origem inicial para análise

---

## 3. Pedido

Estados possíveis:
- Lead
- Em negociação
- Confirmado
- Faturado
- Cancelado

Somente pedidos **Confirmados** geram comissão.

---

## 4. Comissão

- Comissão é calculada no pedido confirmado
- Percentual por representante
- Regras especiais podem existir por campanha
- Comissão não pode ser editada manualmente após faturamento

---

## 5. Quebra de Caixa

- Todo pedido confirmado gera 1% para caixa geral
- Esse valor é separado da comissão
- O caixa é usado para custos operacionais e marketing

---

## 6. Relatórios

O sistema deve permitir:
- Relatório por origem
- Relatório por representante
- Relatório por campanha
- Relatório de recompra
