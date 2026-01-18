# DATA MODEL — Sistema de Atribuição de Vendas

Este documento define as entidades, campos e relacionamentos do sistema.
Ele deve respeitar integralmente o CORE-LOGIC.

---

## 1. Cliente

Campos:
- id (único)
- nome
- telefone
- email
- origem_principal (imutável, definida no primeiro pedido)
- data_criacao

Regras:
- Um cliente pode ter vários pedidos
- A origem_principal nunca muda

---

## 2. Pedido

Campos:
- id
- cliente_id
- origem
- campanha
- canal
- representante_id (ou automático)
- status (lead | negociação | confirmado | faturado)
- valor
- data_criacao

Regras:
- Todo pedido nasce com origem
- Origem nunca é sobrescrita
- Status segue o funil definido no CORE

---

## 3. Representante

Campos:
- id
- nome
- tipo (humano | automático)
- ativo

---

## 4. Atribuição

Campos:
- pedido_id
- origem
- campanha
- canal
- representante_id
- timestamp

Regras:
- A atribuição inicial é permanente
- Novas interações apenas complementam

