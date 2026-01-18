# ROADMAP – Execução do MVP

Objetivo: entregar o MVP funcionando com login, pedidos, atribuição e relatórios
(total vendas, total peças, comissão e 1% quebra de caixa).

---

## Semana 1 – Fundação
- Criar repositório do app (front + back) e estrutura de pastas
- Configurar banco (Postgres) e migrations
- Implementar entidades do DATA-MODEL
- Implementar autenticação (admin + representante)
- Seed de dados para testes (clientes, representantes, pedidos)

Entrega da semana:
- Login funcionando
- Banco com tabelas criadas
- Admin acessa painel vazio

---

## Semana 2 – Pedidos e Fluxo
- CRUD de clientes
- CRUD de pedidos (criar/listar/detalhe)
- Implementar status do funil (lead → negociação → confirmado → faturado)
- Implementar regras do ORDER-FLOW
- Implementar atribuição inicial e histórico (imutável)

Entrega da semana:
- Representante consegue ver e atualizar pedidos do seu escopo
- Admin consegue ver tudo
- Origem/campanha/canal registrados

---

## Semana 3 – Financeiro e Relatórios
- Calcular comissão por representante (regra simples configurável)
- Calcular 1% quebra de caixa no período
- Relatórios:
  - total vendas
  - total peças
  - por representante
  - por origem/campanha

Entrega da semana:
- Relatório fecha números e comissões corretamente

---

## Semana 4 – UI e Qualidade
- Ajustes de UI (tabelas, filtros, carregamento)
- Performance e paginação
- Logs básicos e tratamento de erro
- Preparar deploy (staging e prod)

Entrega da semana:
- MVP pronto para uso real com estabilidade
