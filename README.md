# 🏠 LogiShelter - Plataforma de Apoio à Logística de Abrigos

**LogiShelter** é uma API REST desenvolvida em **Java com Quarkus** que tem como objetivo facilitar o gerenciamento de **voluntários** e **mantimentos** em abrigos emergenciais. O sistema permite cadastrar, consultar, atualizar e remover dados em um banco de dados **Oracle**.

---

## 🧪 Tecnologias Utilizadas

- 🔸 Java 17  
- 🔸 Quarkus 3.x (RESTEasy Reactive + Panache Hibernate)  
- 🔸 Oracle Database (FIAP - oracle.fiap.com.br)  
- 🔸 JDBC Oracle  
- 🔸 JSON-B / Jackson  
- 🔸 Postman (para testes de API)  
- 🔸 VS Code / IntelliJ IDEA  
- 🔸 Git + GitHub  

---

## 📁 Estrutura do Projeto

```
📦 src
 ┣ 📂 main
 ┃ ┣ 📂 java
 ┃ ┃ ┣ 📂 br.com.logishelter
 ┃ ┃ ┃ ┣ 📂 model         -> Entidades JPA (Voluntario, Mantimento)
 ┃ ┃ ┃ ┣ 📂 resource      -> Endpoints REST
 ┃ ┃ ┃ ┗ 📂 service       -> Regras de negócio
 ┃ ┣ 📂 resources
 ┃ ┃ ┣ application.properties  -> Configuração do banco Oracle
 ┃ ┃ ┗ import.sql              -> Inserts iniciais
```

---

## 🧍 Entidade: Voluntário

| Campo        | Tipo    | Descrição                  |
|--------------|---------|----------------------------|
| id           | Long    | ID do voluntário           |
| nome         | String  | Nome completo              |
| contato      | String  | Telefone com DDD           |
| idAbrigo     | Integer | ID do abrigo associado     |

---

## 📦 Entidade: Mantimento

| Campo        | Tipo    | Descrição                     |
|--------------|---------|-------------------------------|
| id           | Long    | ID do mantimento              |
| descricao    | String  | Tipo de item (ex: arroz)      |
| quantidade   | Integer | Quantidade disponível         |
| idAbrigo     | Integer | ID do abrigo onde está alocado|

---

## 🔁 Endpoints REST

### ✅ Voluntários

| Método | Endpoint                | Descrição                 |
|--------|-------------------------|---------------------------|
| GET    | `/voluntarios`          | Listar todos os voluntários |
| GET    | `/voluntarios/{id}`     | Buscar voluntário por ID    |
| POST   | `/voluntarios`          | Cadastrar novo voluntário   |
| PUT    | `/voluntarios/{id}`     | Atualizar voluntário        |
| DELETE | `/voluntarios/{id}`     | Remover voluntário          |

### ✅ Mantimentos

| Método | Endpoint                | Descrição                   |
|--------|-------------------------|-----------------------------|
| GET    | `/mantimentos`          | Listar todos os mantimentos |
| GET    | `/mantimentos/{id}`     | Buscar mantimento por ID    |
| POST   | `/mantimentos`          | Cadastrar novo mantimento   |
| PUT    | `/mantimentos/{id}`     | Atualizar mantimento        |
| DELETE | `/mantimentos/{id}`     | Remover mantimento          |


## ⚙️ Como Rodar Localmente

### 1. Clone o projeto:
```bash
git clone [https://github.com/seuusuario/logishelter.git](https://github.com/iAmFlavio/LogiShelter-java.git)
cd logishelter
```

### 2. Configure o banco Oracle:

No arquivo `src/main/resources/application.properties`, configure com seus dados FIAP:
```properties
quarkus.datasource.db-kind=oracle
quarkus.datasource.jdbc.url=jdbc:oracle:thin:@oracle.fiap.com.br:1521:ORCL
quarkus.datasource.username=SEU_USUARIO
quarkus.datasource.password=SUA_SENHA
quarkus.hibernate-orm.database.generation=none
```

### 3. Rode a aplicação:
```bash
./mvnw quarkus:dev
```

A API estará disponível em:  
📍 `http://localhost:8080`

---

## 📮 Testes com Postman

1. Abra o Postman
2. Clique em **Import**
3. Importe a coleção `LogiShelter.postman_collection.json` (disponível no repositório)
4. Teste os endpoints de forma prática!

---

## 🧑‍💻 Autor

**Flávio Patricio Felinto da Silva**  
Estudante de Análise e Desenvolvimento de Sistemas - FIAP  
📧 flaviopatricio.felinto@gmail.com  
📱 +55 11 93151-0869  
🔗 [LinkedIn](https://www.linkedin.com/in/flavio-felinto)

---

## 📌 Status do Projeto

✅ Finalizado - Backend funcional, aguardando integração com frontend em **Next.js**.

---

## 🔗 Repositório

👉 [(https://github.com/iAmFlavio/LogiShelter-java.git)]
