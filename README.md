# 💸 PRD — FinChat AI

> **Aplicativo Inteligente de Organização de Finanças Pessoais utilizando IA Conversacional, desenvolvido com Lovable e Supabase.**

---

# 📌 Visão Geral

O **FinChat AI** é um aplicativo de finanças pessoais que utiliza Inteligência Artificial para permitir que os usuários registrem receitas, despesas e metas financeiras através de uma conversa natural.

Em vez de preencher formulários, o usuário simplesmente conversa com um assistente financeiro inteligente, que interpreta as mensagens, registra automaticamente as transações, organiza os dados e fornece recomendações personalizadas para melhorar a saúde financeira.

O objetivo é criar uma experiência extremamente simples, intuitiva e moderna, tornando o controle financeiro acessível até mesmo para quem nunca utilizou um aplicativo desse tipo.

---

# 🎯 Objetivo do Projeto

Desenvolver um MVP funcional que permita aos usuários:

- 💬 Registrar receitas e despesas por conversa.
- 🤖 Utilizar IA para interpretar linguagem natural.
- 📊 Visualizar dashboards financeiros em tempo real.
- 🎯 Criar metas financeiras.
- 💡 Receber recomendações inteligentes para economizar.

---

# 🚨 Problema

Grande parte das pessoas abandona aplicativos financeiros porque:

- exigem muito cadastro manual;
- possuem interfaces complexas;
- obrigam o usuário a organizar todas as categorias;
- não oferecem orientação personalizada.

O FinChat AI resolve esse problema utilizando IA Conversacional para automatizar praticamente todo o processo.

---

# 👥 Público-Alvo

O aplicativo é destinado para:

- Jovens adultos
- Trabalhadores assalariados
- Profissionais autônomos
- Pequenos empreendedores
- Pessoas iniciando sua educação financeira

Faixa etária:

**18 a 50 anos**

---

# 💡 Proposta de Valor

> **Organizar suas finanças deve ser tão simples quanto enviar uma mensagem no WhatsApp.**

O usuário conversa com a IA e ela cuida do restante.

---

# ✨ Funcionalidades do MVP

## 💬 1. Chat Financeiro

Tela principal do aplicativo.

O usuário poderá conversar naturalmente.

### Exemplos

> Gastei 5.000 Kz em combustível.

> Recebi meu salário hoje.

> Paguei internet de 12.000 Kz.

A IA deverá interpretar automaticamente:

- valor
- categoria
- data
- tipo da transação
- descrição

e salvar tudo no banco de dados.

---

## 🤖 2. Classificação Inteligente

A IA identifica automaticamente categorias como:

- 🍔 Alimentação
- 🚗 Transporte
- 🏠 Moradia
- 💡 Serviços
- 🎓 Educação
- 🛍 Compras
- 🎮 Lazer
- 🏥 Saúde
- 💼 Salário
- 📈 Investimentos

Sem qualquer seleção manual.

---

## 🎯 3. Metas Financeiras

O usuário poderá criar objetivos dizendo frases como:

> Quero economizar 200.000 Kz até dezembro.

A IA deverá:

- criar a meta;
- calcular quanto economizar por mês;
- acompanhar o progresso;
- mostrar percentual concluído;
- enviar incentivos.

---

## 📊 4. Dashboard

O Dashboard deve apresentar:

- Saldo Atual
- Total de Receitas
- Total de Despesas
- Gastos por Categoria
- Evolução Mensal
- Metas Financeiras
- Últimas Movimentações

Os gráficos devem atualizar automaticamente.

---

## 💡 5. Agente Financeiro

O agente será chamado **FinBot**.

Seu papel será:

- analisar gastos;
- identificar excessos;
- sugerir economia;
- incentivar metas;
- ensinar educação financeira.

Exemplo:

> Você gastou 22% mais com alimentação este mês.

Ou

> Se reduzir 10% das despesas com delivery poderá economizar aproximadamente 15.000 Kz por mês.

---

# 📱 Fluxo das Telas

```text
🚀 Splash

      │

🔐 Login

      │

📝 Cadastro

      │

🏠 Dashboard
      │
      ├── 💬 Chat Financeiro
      ├── 📜 Histórico
      ├── 🎯 Metas
      ├── 📊 Dashboard
      ├── 👤 Perfil
      └── ⚙️ Configurações
```

---

# 🎨 Design

## Estilo

- Moderno
- Clean
- Minimalista
- Responsivo

## Cores

Primária

- Azul (#2563EB)

Secundária

- Verde (#22C55E)

Neutras

- Branco
- Cinza Claro
- Cinza Escuro

---

# 🤖 Personalidade da IA

Nome:

**FinBot**

Características:

- Educado
- Motivador
- Objetivo
- Didático
- Conversacional
- Nunca julgador

A IA sempre deve explicar suas recomendações de forma simples.

---

# 🛠 Stack Tecnológica

| Camada | Tecnologia |
|---------|------------|
| 🎨 Frontend | Lovable |
| ⚙ Backend | Supabase |
| 🗄 Banco de Dados | PostgreSQL (Supabase) |
| 🔐 Autenticação | Supabase Auth |
| 🤖 IA | OpenAI GPT |
| 📊 Gráficos | Recharts |
| ☁ Deploy | Lovable + Supabase |

---

# 🏗 Arquitetura

```text
                 👤 Usuário
                      │
                      ▼
                Frontend (Lovable)
                      │
        ┌─────────────┴─────────────┐
        │                           │
        ▼                           ▼
     OpenAI GPT              Supabase Auth
        │                           │
        └─────────────┬─────────────┘
                      ▼
               Supabase Backend
                      │
                      ▼
              PostgreSQL Database
```

---

# 🗄 Banco de Dados

## users

- id
- nome
- email
- created_at

---

## transactions

- id
- user_id
- tipo
- categoria
- descricao
- valor
- data
- created_at

---

## goals

- id
- user_id
- titulo
- valor_meta
- valor_atual
- data_limite
- status

---

## conversations

- id
- user_id
- mensagem
- resposta_ia
- created_at

---

# 🔐 Autenticação

Utilizar Supabase Auth com:

- Login por e-mail
- Cadastro
- Recuperação de senha
- Sessão persistente
- Logout

---

# 📈 Dashboard

O Dashboard deverá possuir:

- Card de Saldo
- Card de Receitas
- Card de Despesas
- Card de Economia
- Gráfico de Pizza por Categoria
- Gráfico Mensal
- Lista das Últimas Transações

---

# 🚀 Requisitos para o Lovable

Desenvolver uma aplicação completa utilizando React e TypeScript gerados pelo Lovable, com interface totalmente responsiva para desktop e dispositivos móveis.

Implementar autenticação utilizando Supabase Auth.

Persistir todos os dados no PostgreSQL do Supabase.

Criar todas as tabelas e relacionamentos necessários.

Utilizar Row Level Security (RLS) para garantir que cada usuário acesse apenas seus próprios dados.

Consumir a OpenAI API para interpretar mensagens em linguagem natural e gerar recomendações financeiras.

Criar componentes reutilizáveis.

Utilizar boas práticas de UX/UI.

Adicionar estados de carregamento (loading), tratamento de erros e mensagens de sucesso.

Organizar o projeto de forma modular e escalável.

---

# 📊 Critérios de Validação

O MVP será considerado validado quando:

- ✅ O usuário conseguir registrar uma despesa apenas conversando.
- ✅ As transações forem classificadas corretamente.
- ✅ O Dashboard atualizar automaticamente.
- ✅ As metas forem acompanhadas em tempo real.
- ✅ O FinBot fornecer recomendações relevantes.

---

# 🔮 Evoluções Futuras

- 🏦 Integração bancária (Open Finance)
- 💳 Importação automática de extratos
- 📸 OCR para leitura de recibos
- 🎤 Registro por voz
- 📅 Planejamento financeiro
- 📈 Controle de investimentos
- 👨‍👩‍👧 Finanças familiares
- 🔔 Alertas inteligentes
- 🌎 Multi-moeda
- 📱 Aplicativo mobile nativo

---

# ✅ Resultado Esperado

O FinChat AI deverá oferecer uma experiência moderna e intuitiva, permitindo que qualquer pessoa organize suas finanças de forma simples através de conversas com um assistente inteligente.

O objetivo é reduzir a fricção no registro de transações, incentivar hábitos financeiros saudáveis e demonstrar o potencial do Vibe Coding na criação de aplicações completas com IA, utilizando Lovable e Supabase.

> **"Converse. Registre. Economize. Evolua."** 💙


# ✅ Fotos do processo
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6aa84722-4a45-46b8-bdc2-eb40c5757de3" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/727ace45-d97b-4e95-b311-58d7e57897d4" />

# ✅  Fotos do APP no Lovable

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d32d36d2-6151-4c3e-87de-a5b173717b84" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/94eb0b5c-1646-46b8-bd8b-b6480d0a6f39" />

# 🧠 Reflexão sobre o PRD

A criação do PRD do **FinChat AI** ajudou a transformar uma ideia em uma solução estruturada, definindo claramente o problema, o público-alvo, as funcionalidades e os objetivos do MVP.

O principal aprendizado foi perceber que a qualidade das respostas da IA depende da clareza das instruções fornecidas. No **Vibe Coding**, a IA funciona como uma parceira de criação, mas é necessário ter uma visão bem definida para orientar o desenvolvimento.

Durante o processo, também aprendi a importância de priorizar funcionalidades essenciais e evitar adicionar recursos demais antes de validar a solução principal.

Este projeto mostrou que, com bons prompts e uma estratégia clara, é possível utilizar a IA para acelerar a criação de produtos digitais.




