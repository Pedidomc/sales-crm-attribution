# ARCHITECTURE – Arquitetura do Sistema

Este documento define como o sistema é estruturado tecnicamente.
Nenhuma implementação deve violar esta arquitetura.

---

## 1. Visão Geral

O sistema é composto por:

- Front-end (interface)
- Back-end (regras e dados)
- Banco de dados
- Integrações externas

Arquitetura modular, desacoplada e escalável.

---

## 2. Front-end

Responsável por:
- Exibição das telas
- Interações do usuário
- Consumo de APIs

Tecnologias possíveis:
- Web (HTML / CSS / JS ou framework)
- Mobile (futuro)

O front **não contém regras de negócio**.

---

## 3. Back-end

Responsável por:
- Aplicar CORE-LOGIC
- Validar dados
- Controlar permissões
- Processar atribuições e status

Todo fluxo crítico passa pelo back-end.

---

## 4. Banco de Dados

Baseado no DATA-MODEL.

Entidades principais:
- Cliente
- Pedido
- Representante
- Atribuição

Regras:
- Origem nunca é alterada
- Histórico é permanente
- Dados críticos são imutáveis

---

## 5. Integrações

Possíveis integrações:
- WhatsApp
- Plataformas de anúncios
- Pagamentos
- ERPs

Integrações **nunca alteram CORE-LOGIC**.

---

## 6. Controle de Acesso

Gerenciado pelo módulo AUTH.

Perfis:
- Administrador
- Representante
- Sistema (automático)

---

## 7. Escalabilidade

Sistema preparado para:
- Múltiplas empresas (SaaS)
- Múltiplos usuários
- Crescimento de volume

Separação clara entre dados e regras.
