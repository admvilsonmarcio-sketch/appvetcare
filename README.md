📘 VETCARE CRM — Sistema Multi-Tenant com IA Integrada

Sistema de Gestão para Clínicas Odontológicas e Veterinárias com Agendamento Inteligente, CRM Completo e Dashboards Multi-Nível

Bem-vindo ao repositório oficial do VETCARE CRM, um sistema SaaS de próxima geração projetado para clínicas que desejam operar com automação total, inteligência artificial, gestão multi-unidades e uma experiência moderna de CRM.

Este projeto foi arquitetado para suportar operações clínicas complexas, incluindo:

Múltiplas clínicas/unidades (multi-tenant)

Agendamentos automáticos por IA (N8n + agentes)

Painel administrativo geral (Super Admin)

Painéis independentes por clínica

CRM profundo (pacientes, tutores, pets, histórico, tags, segmentação)

Agenda integrada para recepção e profissionais

Segurança avançada e isolamento de dados

Prontuário digital, odontograma, histórico de atendimentos

Módulos de marketing, comunicação e automação

🏗️ Arquitetura do Sistema

O VETCARE CRM é construído sobre uma arquitetura moderna, escalável e totalmente orientada a SaaS.

🧩 Componentes Principais
1. Backend (Node + TRPC + Drizzle ORM + MySQL)

TRPC como camada de API tipada

Drizzle ORM para acesso seguro e escalável ao banco

MySQL como banco principal

Multi-tenancy com isolamento por clinicaId

RBAC granular

Middlewares avançados (tenant resolver, auth, audit)

Preparado para webhooks da IA

2. Frontend (React + Vite + TypeScript + shadcn/UI)

Dashboard moderno e responsivo

Interfaces independentes para:

Super Admin

Clínica

Dentistas

Recepção

React Query para data loading

Shadcn/ui + Tailwind para UI profissional

3. IA e Automação (N8n + Agentes Inteligentes)

Primeiro contato por IA (WhatsApp / Chat)

Coleta de dados (nome, procedimento, horário, preferências)

Criação automática de agendamentos via API

Notificações, lembretes e confirmações automáticas

Histórico de interações integrado ao CRM

🔐 Multi-Tenancy (SaaS Profissional)

O sistema utiliza Shared Schema Multi-Tenant com isolamento por linha (clinicaId).

Recursos:

Isolamento total entre clínicas

Super Admin com visão global

Usuários vinculados a uma clínica

Tenant carregado automaticamente no contexto TRPC

Segurança empresarial

Estrutura Básica:
clinicas
users (com clinicaId)
tutores
pets
veterinarios
agendamentos
financeiro
prontuarios

🤖 Integração com IA (Workflow Ativo)

O VETCARE CRM foi projetado para se integrar perfeitamente com agentes de IA:

Fluxos Implementados:

Captação de leads

Qualificação automática

Agendamento por WhatsApp

Registro automático no sistema

Follow-up inteligente

Reagendamentos automáticos

Cancelamentos por IA

Confirmação pré-consulta

Plataforma recomendada:

N8n (já validado)

Suporte para Make, Zapier ou agentes próprios

📅 Sistema de Agendamento

Agenda por dentista

Agenda da clínica

Agendamentos criados via IA

Agendamentos manuais (recepção)

Lista de espera

Bloqueios de horário

Notificações automáticas

Gestão de conflito

Visualização por dia/semana/mês

👨‍⚕️ CRM Clínico Completo
Funcionalidades:

Cadastro de pacientes e tutores

Histórico de atendimentos

Timeline de interações IA + recepção

Tags e segmentações

Anamneses e condições médicas

Prontuários digitais

Planos de tratamento

Documentos e anexos

📊 Dashboards Multi-Nível
Super Admin

Todas as clínicas

Agendamentos gerais

Receita consolidada

Ranking de unidades

Alertas de performance

Relatórios comparativos

Clínica

Dashboard da unidade

Consultas do dia

Produção por dentista

Taxa de ocupação

Agendamentos por status

Pipeline de pacientes

🔒 Segurança e Compliance

RBAC completo

Controle de permissões por módulo

Auditoria de ações sensíveis

Logs estruturados

Políticas LGPD

Sanitização de dados

Proteção contra cross-tenant access

🚀 Tecnologias Utilizadas
Frontend

React

TypeScript

Vite

TailwindCSS

Shadcn/UI

React Query

Backend

Node.js (ESM)

TRPC

Drizzle ORM

MySQL

Zod (validação)

Infra

Docker + Docker Compose

Nginx (proxy)

Módulos IA customizados

Scripts de deploy

🛠️ Como Rodar o Projeto
1. Clonar o repositório
git clone https://github.com/seu-usuario/vetcare-crm.git
cd vetcare-crm

2. Instalar dependências
pnpm install

3. Configurar variáveis de ambiente

Criar .env:

DATABASE_URL=mysql://user:pass@mysql:3306/vetcarecrm
JWT_SECRET=sua_chave
VITE_APP_ID=...
OAUTH_SERVER_URL=...

4. Subir containers
docker-compose up -d

5. Rodar migrations
pnpm drizzle:push

6. Rodar localmente
pnpm dev

📚 Documentação Necessária (em progresso)

/docs/architecture.md

/docs/multi-tenant.md

/docs/ia-integration.md

/docs/api-reference.md

/docs/modules/

🧱 Roadmap Inicial
🟥 Sprint 1 (Fundação Multi-Tenant)

Tenant resolver

RBAC inicial

Filtro global TRPC

Vínculo user → clínica

🟥 Sprint 2 (Agenda + IA)

Webhook N8n

Rotas de agendamento

UI conectada

IA → Sistema funcionando

🟧 Sprint 3 (CRM Completo)

Timeline

Histórico

Tags

Prontuário básico

🟩 Sprint 4 (Dashboards)

Super Admin

Painel da clínica

KPIs reais

👥 Contribuição

Pull requests são bem-vindos!
Mantemos padrões corporativos de arquitetura, segurança e testes.

📄 Licença

© 2025 VetCare CRM — Todos os direitos reservados.
