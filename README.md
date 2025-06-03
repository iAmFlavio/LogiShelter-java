# 🛡️ LogiShelter - API de Gestão de Abrigos

Projeto desenvolvido para apoiar a gestão de **voluntários** e **mantimentos** em abrigos emergenciais, com backend em **Java + Quarkus** e banco de dados **Oracle**.

---

## 🚀 Tecnologias utilizadas

- Java 17
- Quarkus 3.x
- Hibernate ORM com Panache
- RESTEasy Reactive
- Oracle JDBC Driver
- JSON-B / Jackson
- Postman (testes de API)
- VS Code / IntelliJ

---

## 🧱 Estrutura de Entidades

### 🧍 Voluntário

| Campo         | Tipo     | Descrição                    |
|---------------|----------|------------------------------|
| id            | Long     | Identificador do voluntário  |
| nome          | String   | Nome completo                |
| contato       | String   | Telefone                     |
| idAbrigo      | Integer  | ID do abrigo associado       |

### 📦 Mantimento

| Campo         | Tipo     | Descrição                          |
|---------------|----------|------------------------------------|
| id            | Long     | Identificador do mantimento        |
| descricao     | String   | Tipo/descrição do mantimento       |
| quantidade    | Integer  | Quantidade disponível              |
| idAbrigo      | Integer  | ID do abrigo em que está armazenado|

---

## 🔁 Endpoints REST

### 📍 Voluntários

| Método | Rota                         | Descrição                    |
|--------|------------------------------|------------------------------|
| GET    | `/voluntarios`               | Listar todos                 |
| GET    | `/voluntarios/{id}`          | Buscar por ID                |
| POST   | `/voluntarios`               | Criar novo                   |
| PUT    | `/voluntarios/{id}`          | Atualizar por ID             |
| DELETE | `/voluntarios/{id}`          | Remover por ID               |

### 📍 Mantimentos

| Método | Rota                         | Descrição                    |
|--------|------------------------------|------------------------------|
| GET    | `/mantimentos`               | Listar todos                 |
| GET    | `/mantimentos/{id}`          | Buscar por ID                |
| POST   | `/mantimentos`               | Criar novo                   |
| PUT    | `/mantimentos/{id}`          | Atualizar por ID             |
| DELETE | `/mantimentos/{id}`          | Remover por ID               |

---

## ⚙️ Como executar o projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/seuusuario/sheltersync.git
   cd sheltersync
