# ORDER FLOW – Fluxo de Vida do Pedido

Este documento descreve o caminho completo de um pedido,
desde o primeiro contato até o faturamento.

---

## 1. Entrada do Lead

O lead pode entrar por:
- Anúncio
- Orgânico
- Indicação
- Cliente recorrente

Ações do sistema:
- Criar Cliente (se não existir)
- Criar Pedido com status = lead
- Registrar Atribuição inicial (imutável)

---

## 2. Criação do Pedido

Todo pedido nasce com:
- cliente_id
- origem
- campanha
- canal
- data/hora
- responsável (automático ou representante)

Regras:
- Origem nunca pode ser alterada
- Pedido nasce sempre como LEAD

---

## 3. Atendimento Comercial

O pedido pode avançar para:
- negociação
- confirmado

Ações permitidas:
- Alterar status
- Associar representante
- Registrar interações

Ações proibidas:
- Alterar origem
- Alterar atribuição inicial

---

## 4. Confirmação

Quando o pedido é confirmado:
- Status muda para CONFIRMADO
- Pedido fica bloqueado para edição estrutural
- Comissão é calculada

---

## 5. Faturamento

Quando o pedido é faturado:
- Status = FATURADO
- Valores finais são consolidados
- Comissão é validada
- Pedido entra em relatórios

---

## 6. Recompra

Se o cliente fizer nova compra:
- Novo pedido é criado
- Origem principal do cliente é preservada
- Nova atribuição é complementar
