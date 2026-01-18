# UI MAP – Mapa de Telas do Sistema

Este documento define todas as telas do sistema,
quem acessa e o que cada tela permite.

---

## 1. Tela de Login

Acesso:
- Representante
- Administrador

Funções:
- Autenticação
- Redirecionamento por perfil

---

## 2. Dashboard Geral

Acesso:
- Administrador

Exibe:
- Total de leads
- Pedidos por status
- Faturamento
- Origem de vendas
- Performance por representante

---

## 3. Funil de Vendas (CRM)

Acesso:
- Representante
- Administrador

Exibe:
- Leads
- Negociação
- Confirmados
- Faturados

Ações permitidas:
- Arrastar pedido entre etapas
- Abrir detalhes do pedido

Ações bloqueadas:
- Alterar origem
- Alterar atribuição inicial

---

## 4. Tela de Pedido (Detalhe)

Acesso:
- Representante responsável
- Administrador

Exibe:
- Dados do cliente
- Origem e campanha
- Histórico de interações
- Status atual
- Valor

Regras:
- Origem é somente leitura
- Status segue ORDER-FLOW

---

## 5. Tela de Cliente

Acesso:
- Administrador

Exibe:
- Dados do cliente
- Origem principal
- Histórico de pedidos

---

## 6. Tela de Comissões

Acesso:
- Administrador

Exibe:
- Pedido
- Representante
- Valor
- Status da comissão

---

## 7. Tela de Atribuição / Origem

Acesso:
- Administrador

Exibe:
- Origem por pedido
- Campanha
- Canal
- Histórico imutável

---

## 8. Configurações

Acesso:
- Administrador

Funções:
- Gerenciar representantes
- Permissões
- Regras globais
