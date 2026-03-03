# DONGNATE

**DONGNATE** é um aplicativo mobile que conecta ONGs a doadores, funcionando como uma plataforma de intermediação digital. 
O DONGNATE busca promover impacto social ao facilitar a conexão entre organizações sociais e doadores, incentivando solidariedade e colaboração comunitária através da tecnologia. O sistema **não realiza logística, armazenamento ou entrega de itens**.Seu objetivo é apenas conectar quem precisa de doação com quem deseja doar.

---

## 🎯 Objetivo do Projeto

Criar uma aplicação mobile com backend estruturado utilizando **Padrões de Projeto**, permitindo que:

* ONGs publiquem necessidades
* Doadores encontrem essas necessidades
* Doadores manifestem interesse em ajudar
* O sistema registre a conexão entre as partes

Após a conexão, a comunicação e entrega acontecem externamente ao sistema.

---

## 👥 Integrantes do Grupo

* THIAGO HENRIQUE CIRIANO NEVES
* ALVARO LUANDREY DE SANTANA DE FREITAS
* MATHEUS DE OLIVEIRA MOTA

---

## 🛠 Tecnologias Utilizadas

### Backend

* Kotlin
* Framework: (Ktor)
* PostgreSQL (Supabase)

### Mobile

* Kotlin
* Jetpack Compose
* Arquitetura MVVM
* Retrofit para consumo de API

### Banco de Dados

* Supabase (PostgreSQL)

---

## 🧠 Padrões de Projeto – AV1

### 1️⃣ Factory Method

Utilizado para criação de usuários:

* ONG
* DOADOR

Permite encapsular a lógica de criação e evitar condicionais excessivas no código.

### 2️⃣ Facade

Utilizado para centralizar a lógica de criação de conexões (Match), organizando:

* Validações
* Criação de registros
* Controle de status

Reduz acoplamento entre controllers e serviços.

---

## 🗄 Modelagem do Banco de Dados

### 📌 users

* id
* name
* email
* password
* role (ONG | DONOR)

### 📌 needs

* id
* title
* description
* quantity_requested
* urgency
* ong_id (FK → users)

### 📌 matches

* id
* donor_id (FK → users)
* need_id (FK → needs)
* message
* status (PENDING | ACCEPTED | DECLINED)

---

## 🔄 Funcionalidades – AV1

### 👤 Usuários

* Cadastro de usuário (ONG ou DOADOR)
* Listagem de usuários

### 🏢 ONGs

* Criar necessidade
* Listar suas necessidades

### 🎁 Doadores

* Visualizar necessidades disponíveis
* Manifestar interesse em doar

### 🤝 Sistema

* Criar Match
* Atualizar status do Match

---

## 📋 Checklist AV1

### 🟢 Planejamento

* [ ] Definir escopo final
* [ ] Confirmar padrões escolhidos
* [ ] Modelar banco no papel

---

### 🗄 Banco (Supabase)

* [ ] Criar projeto no Supabase
* [ ] Criar tabela users
* [ ] Criar tabela needs
* [ ] Criar tabela matches
* [ ] Definir chaves estrangeiras
* [ ] Testar inserção manual via SQL

---

### ⚙ Backend

* [ ] Criar estrutura do projeto
* [ ] Configurar conexão com banco
* [ ] Implementar entidade User
* [ ] Implementar Factory Method
* [ ] Criar endpoint POST /users
* [ ] Implementar entidade Need
* [ ] Criar endpoints POST e GET /needs
* [ ] Implementar MatchFacade
* [ ] Criar endpoint POST /matches
* [ ] Criar endpoint PATCH /matches/{id}/status
* [ ] Testar todos os endpoints no Postman

---

### 📱 Mobile

* [ ] Criar estrutura base do app
* [ ] Configurar Retrofit
* [ ] Criar tela de cadastro
* [ ] Criar tela de listagem de necessidades
* [ ] Criar tela de manifestação de interesse
* [ ] Integrar com backend
* [ ] Testar fluxo completo

---

### 🎤 Preparação da Apresentação

* [ ] Explicar objetivo social do projeto
* [ ] Demonstrar funcionamento do app
* [ ] Explicar onde foi aplicado Factory
* [ ] Explicar onde foi aplicado Facade
* [ ] Justificar escolha dos padrões

---

## 📌 Estrutura do Projeto

```
dongnate/
├── dongnate-backend/
├── dongnate-mobile/
├── database/
└── docs/
```

---

## 🚀 Futuras Melhorias (AV2)

* Sistema automático de recomendação de Match
* Notificações
* Testes unitários no backend
* Melhorias de UI/UX
* Deploy online da aplicação

---


---
