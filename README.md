# 🎲 Mesa em Rede
### Plataforma de Matchmaking para Grupos de RPG

## 👥 Integrantes do Grupo
- THIAGO HENRIQUE CIRIANO NEVES
- ALVARO LUANDREY DE SANTANA DE FREITAS
- MATHEUS DE OLIVEIRA MOTA

---

## 📖 Descrição do Projeto

O **Mesa em Rede** é uma plataforma mobile voltada para conectar jogadores e mestres de RPG de mesa através de um sistema inteligente de compatibilidade.

O projeto busca solucionar a dificuldade de encontrar grupos compatíveis considerando fatores como:
- Sistema de RPG preferido
- Estilo de jogo
- Nível de experiência
- Disponibilidade de horários

A aplicação realizará o cadastro de usuários, criação de campanhas, sistema de matchmaking e gerenciamento de sessões.

---

## 🎯 Problema

Jogadores frequentemente têm dificuldade em encontrar mesas compatíveis com seu estilo e disponibilidade. Mestres enfrentam evasão de jogadores e dificuldade para formar grupos consistentes.

---

## 💡 Solução Proposta

Uma aplicação mobile com backend dedicado que:

- Permite cadastro de jogadores e mestres
- Calcula compatibilidade entre perfis
- Cria salas de campanha
- Gerencia sessões e confirmações
- Implementa sistema de reputação
- Oferece notificações de compatibilidade

---

## 🏗 Arquitetura do Projeto

O sistema será dividido em:

- **Mobile:** Kotlin + Jetpack Compose  
- **Backend:** Kotlin (Ktor ou Spring Boot)  
- **Banco de Dados:** PostgreSQL ou MongoDB  
- **Arquitetura:** Camadas (Presentation, Application, Domain, Infrastructure)

---

## 🧩 Padrões de Projeto Aplicados

### 📌 1ª Unidade (AV1)

- **Factory Method**  
  Criação de diferentes tipos de perfil (Jogador, Mestre, Iniciante, Veterano).

- **Facade**  
  Interface simplificada para o sistema de matchmaking, abstraindo o cálculo de compatibilidade.

---

### 📌 2ª Unidade (AV2)

- **Strategy**  
  Diferentes estratégias de cálculo de compatibilidade (estrito, flexível, por afinidade).

- **Observer**  
  Sistema de notificações para:
  - Novo match compatível
  - Sessão criada
  - Confirmação de presença

---

## 🔄 Funcionalidades Principais (AV1)

- Cadastro de usuário
- Criação de perfil (Jogador ou Mestre)
- CRUD de campanhas
- Sistema inicial de matchmaking

---

## 🚀 Funcionalidades Futuras (AV2)

- Chat interno entre membros
- Sistema de sessões com confirmação
- Sistema de avaliação pós-campanha
- Testes unitários no backend

---

## 🗄 Banco de Dados

O sistema utilizará banco de dados relacional ou não relacional para armazenar:

- Usuários
- Perfis
- Campanhas
- Sessões
- Avaliações

---

## 🧪 Testes

Na segunda unidade serão implementados testes unitários para:

- Algoritmo de matchmaking
- Estratégias de compatibilidade
- Validações de regras de negócio

---

## 🎓 Objetivo Acadêmico

O projeto tem como objetivo aplicar na prática os padrões de projeto estudados na disciplina, integrando frontend, backend e banco de dados em uma aplicação funcional e coesa.

---
