# TECH STACK – Tecnologias do Sistema

Este documento define as tecnologias escolhidas para construir o MVP.
A escolha prioriza rapidez, clareza e possibilidade de escalar.

---

## 1. Front-end

Objetivo:
- Construir telas do UI-MAP
- Consumo exclusivo da API

Opções:
- Web: React + Vite
- Estilo: Tailwind CSS
- Estado: simples (hooks / context)

Regras:
- Sem regra de negócio no front
- Tudo passa pela API

---

## 2. Back-end

Objetivo:
- Aplicar CORE-LOGIC
- Orquestrar ORDER-FLOW
- Calcular comissões e 1%

Opções:
- Node.js + TypeScript
- Framework: NestJS (ou Express, se simples)

Regras:
- Validações no back
- Logs de ações críticas
- Controle de permissões via AUTH

---

## 3. Banco de Dados

Objetivo:
- Persistir entidades do DATA-MODEL

Opções:
- PostgreSQL
- ORM: Prisma

Regras:
- Origem imutável
- Histórico preservado
- Migrations versionadas

---

## 4. Autenticação

Objetivo:
- Login e sessão

Opções:
- JWT
- Refresh token simples

Perfis:
- Admin
- Representante
- Sistema

---

## 5. Infraestrutura (MVP)

Opções:
- Deploy: Vercel (front) + Railway/Fly.io (back)
- Banco: Postgres gerenciado
- Ambiente: dev / prod

---

## 6. Integrações (V1)

- Nenhuma automática no MVP
- Entrada manual de origem/campanha
- Preparado para WhatsApp e Ads (V2)

---

## 7. Observabilidade

- Logs básicos
- Erros críticos registrados
- Métricas simples (KPIs do dashboard)
