# API-MAP – Endpoints do Sistema

Este documento define quais APIs existem, o que recebem e o que devolvem.
O front-end só pode operar através dessas rotas.

---

## 1) Auth

### POST /auth/login
Body:
- email
- senha
Return:
- token
- user (id, nome, perfil)

### POST /auth/logout
Return:
- ok

### GET /auth/me
Return:
- user (id, nome, perfil, representante_id?)

---

## 2) Representantes

### GET /representantes
Filtros:
- ativo=true/false
Return:
- lista de representantes

### POST /representantes
Body:
- nome
- tipo (humano | automatico)
- ativo
Return:
- representante criado

---

## 3) Clientes

### GET /clientes
Filtros:
- telefone
- nome
Return:
- lista de clientes

### POST /clientes
Body:
- nome
- telefone
- email
Return:
- cliente criado

### GET /clientes/:id
Return:
- dados do cliente + origem_principal

---

## 4) Pedidos

### GET /pedidos
Filtros:
- status
- representante_id
- canal
- campanha
- periodo (data_inicio, data_fim)
Return:
- lista de pedidos

### POST /pedidos
Body:
- cliente_id
- origem (anuncio | organico | indicacao | recorrente)
- campanha
- canal
- valor
- itens_total (qtd_pecas)
- representante_id (opcional)
Regra:
- se primeiro pedido: atribuição automática para fábrica (separação justa)
- se recompra: mantém representante do cliente
Return:
- pedido criado + atribuição registrada

### PATCH /pedidos/:id/status
Body:
- status (lead | negociacao | confirmado | faturado)
Return:
- pedido atualizado

---

## 5) Atribuição (origem)

### GET /atribuicoes
Filtros:
- pedido_id
- cliente_id
Return:
- histórico de atribuições

### POST /atribuicoes
Body:
- pedido_id
- origem
- campanha
- canal
- identificador (ex: fbclid, gclid, utm_id)
Regra:
- não sobrescreve: só complementa histórico
Return:
- atribuição criada

---

## 6) Comissão / Quebra de Caixa

### GET /financeiro/resumo
Filtros:
- periodo
Return:
- total_vendas
- total_pecas
- 1_porcento_quebra_caixa
- comissao_por_representante

### GET /financeiro/representantes
Filtros:
- periodo
Return:
- lista com total_vendas, total_pecas, comissao, 1%

---

## 7) Dashboard / Relatórios

### GET /dashboard/kpis
Filtros:
- periodo
- representante_id (opcional)
Return:
- total_vendas
- total_pecas
- total_pedidos
- ticket_medio
- leads
- confirmados
- faturados
