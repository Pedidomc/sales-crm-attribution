# DATA MODEL – Sistema de Atribuição de Vendas

Este documento define as entidades e campos do sistema.
Ele deve obedecer integralmente o CORE-LOGIC.

---

## 1. Cliente

Representa o comprador (CPF ou CNPJ).

Campos:
- id (único)
- nome
- telefone
- email
- origem_principal (imutável, definida no primeiro pedido)
- data_criacao

Regras:
- Um cliente pode ter vários pedidos
- A origem_principal nunca muda após o primeiro pedido

---

## 2. Pedido

Representa uma oportunidade ou venda.

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
- Todo pedido nasce com uma origem
- A origem nunca é sobrescrita
- O status deve seguir o funil definido no CORE-LOGIC

---

## 3. Representante

Usuário responsável pelo atendimento ou fechamento.

Campos:
- id
- nome
- tipo (humano | sistema)
- ativo

Regras:
- Um representante pode ser humano ou automático
- Representantes inativos não recebem novos pedidos

---

## 4. Atribuição

Registro da origem e responsabilidade do pedido.

Campos:
- id
- pedido_id
- origem
- campanha
- canal
- responsavel_id
- data_atribuicao

Regras:
- A atribuição inicial é permanente
- Novas interações apenas complementam o histórico

