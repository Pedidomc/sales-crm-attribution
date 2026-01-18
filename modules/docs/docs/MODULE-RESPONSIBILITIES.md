# MODULE RESPONSIBILITIES

Este documento define o papel de cada módulo do sistema.
Nenhum módulo pode acessar dados fora da sua responsabilidade direta.

---

## 1. Auth

Responsável por:
- Login
- Sessão
- Permissões
- Tipo de usuário

Pode acessar:
- Representante
- Perfil do usuário logado

Não pode:
- Criar ou alterar pedidos
- Alterar comissão
- Alterar origem

---

## 2. Catalog

Responsável por:
- Exibir produtos
- Criar pedidos
- Registrar origem inicial
- Capturar campanha e canal

Pode acessar:
- Cliente
- Pedido (criação)
- Atribuição (criação)

Não pode:
- Alterar status do pedido
- Alterar comissão

---

## 3. CRM

Responsável por:
- Visualizar pedidos
- Alterar status
- Acompanhar clientes
- Fluxo comercial

Pode acessar:
- Cliente
- Pedido
- Representante

Não pode:
- Criar pedidos
- Alterar origem inicial
- Alterar regras de comissão

---

## 4. Attribution

Responsável por:
- Registrar origem
- Campanha
- Canal
- Histórico de atribuições

Pode acessar:
- Pedido
- Atribuição

Não pode:
- Alterar pedido
- Alterar cliente
- Alterar comissão

---

## 5. Commissions

Responsável por:
- Calcular comissão
- Aplicar quebra de caixa
- Gerar relatórios financeiros

Pode acessar:
- Pedido (confirmado)
- Representante
- Comissão

Não pode:
- Alterar pedido
- Alterar origem
- Criar pedidos
