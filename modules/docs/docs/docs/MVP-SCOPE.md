# MVP-SCOPE – V1 (o que entra / o que fica fora)

Objetivo do MVP: ter um CRM funcional com atribuição + relatórios essenciais
(total peças, total vendas, comissão e 1% quebra de caixa), sem depender de planilhas.

---

## ✅ Entra na V1 (MVP)

### 1) Autenticação
- Login simples (admin + representante)
- Perfis: admin / representante

### 2) Cadastro base
- Clientes (nome, telefone, email)
- Representantes (nome, ativo, tipo humano)

### 3) Pedidos
- Criar pedido com:
  - cliente
  - origem + campanha + canal
  - representante (manual ou automático)
  - status do funil (lead > negociação > confirmado > faturado)
  - valor
  - total de peças

### 4) Atribuição (regras)
- Primeiro pedido define origem principal do cliente
- Recompra mantém vínculo com origem inicial (histórico)
- Origem nunca sobrescreve, só complementa

### 5) Relatórios (o que estava faltando no teu CRM atual)
- Total de vendas (R$) por período
- Total de peças por período
- Total por representante:
  - vendas
  - peças
- 1% quebra de caixa calculado automaticamente:
  - 1% sobre o total de vendas do período
- Comissão por representante (regra simples configurável)

### 6) Dashboard (tela simples)
- KPIs do período:
  - total vendas
  - total peças
  - total pedidos
  - ticket médio
  - leads / confirmados / faturados

---

## ❌ Fora da V1 (V2+)

- Catálogo completo com carrinho e checkout
- Integração WhatsApp automática
- Pagamento online
- Multi-loja / multi-empresa
- Permissões avançadas (por filial, por região)
- Automação de atribuição por regras complexas
- Exportação PDF/Excel
- App mobile

---

## Critério de “pronto”
O MVP é considerado pronto quando:
1) consigo cadastrar cliente e pedido em 1 minuto
2) consigo filtrar por representante e período
3) vejo total de peças e total de vendas no relatório
4) o 1% aparece automático no resumo
