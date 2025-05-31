
# LogiShelter - Backend Java com Quarkus e Oracle

![Java](https://img.shields.io/badge/java-17-blue.svg)
![Quarkus](https://img.shields.io/badge/quarkus-framework-green)
![OracleDB](https://img.shields.io/badge/oracle-database-orange)

## 💡 Sobre o Projeto

O **LogiShelter** é um sistema backend desenvolvido com **Java + Quarkus**, que oferece suporte à gestão de **voluntários** e **mantimentos** durante eventos extremos. O sistema integra um banco de dados **Oracle** e expõe uma **API RESTful**, permitindo sua conexão com um frontend para facilitar a coordenação de recursos em abrigos emergenciais.

Este projeto foi desenvolvido como parte do desafio da FIAP no tema **Eventos Extremos**, com foco em soluções tecnológicas para situações de desastres naturais.

---

## 🔧 Tecnologias Utilizadas

- Java 17
- Quarkus Framework
- RESTEasy (JAX-RS)
- Hibernate ORM com Panache
- JDBC Driver - Oracle
- REST Jackson
- Banco de Dados Oracle (FIAP)
- IntelliJ IDEA

---

## 📂 Estrutura do Projeto

```
src/
└── main/
    ├── java/
    │   └── br.com.gsquarkus/
    │       ├── model/               # Entidades JPA (Voluntario, Mantimento)
    │       ├── repository/          # Interfaces PanacheRepository
    │       ├── service/             # Regras de negócio com @Transactional
    │       ├── resource/            # API REST com endpoints
    │       ├── bo/                  # Camada BO intermediária
    │       └── exception/           # Tratamento personalizado de exceções
    └── resources/
        └── application.properties   # Configuração da conexão com o banco
```

---

## 📌 Funcionalidades

- ✅ Cadastro, consulta, edição e exclusão de **voluntários**
- ✅ Cadastro, consulta, edição e exclusão de **mantimentos**
- ✅ API REST com endpoints para integração com o frontend
- ✅ Integração com banco de dados Oracle via JDBC
- ✅ Tratamento de exceções personalizado com pacote próprio
- ✅ Camada BO para regras intermediárias

---

## 🔗 Endpoints da API

### Voluntário

| Método | Endpoint           | Descrição                     |
|--------|--------------------|-------------------------------|
| GET    | /voluntarios       | Lista todos os voluntários    |
| GET    | /voluntarios/{id}  | Busca voluntário por ID       |
| POST   | /voluntarios       | Cadastra um novo voluntário   |
| PUT    | /voluntarios/{id}  | Atualiza dados do voluntário  |
| DELETE | /voluntarios/{id}  | Remove um voluntário          |

### Mantimento

| Método | Endpoint           | Descrição                     |
|--------|--------------------|-------------------------------|
| GET    | /mantimentos       | Lista todos os mantimentos    |
| GET    | /mantimentos/{id}  | Busca mantimento por ID       |
| POST   | /mantimentos       | Cadastra um novo mantimento   |
| PUT    | /mantimentos/{id}  | Atualiza dados do mantimento  |
| DELETE | /mantimentos/{id}  | Remove um mantimento          |

---

## ⚙️ Configuração do Banco de Dados

No arquivo `application.properties`:

```properties
quarkus.datasource.db-kind=oracle
quarkus.datasource.jdbc.url=jdbc:oracle:thin:@oracle.fiap.com.br:1521:ORCL
quarkus.datasource.username=SEU_USUARIO
quarkus.datasource.password=SUA_SENHA
quarkus.hibernate-orm.database.generation=update
quarkus.hibernate-orm.log.sql=true
```

---

## 🧪 Como Executar Localmente

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/logishelter.git
   cd logishelter
   ```

2. Compile e rode com Quarkus:
   ```bash
   ./mvnw compile quarkus:dev
   ```

3. Acesse os endpoints em:
   ```
   http://localhost:8080/voluntarios
   http://localhost:8080/mantimentos
   ```

---

## 👥 Integrantes

- Flávio Patricio Felinto da Silva – RM: 560149
- Bruno Carlos Soares – RM: 559250

---

## 📎 Repositório

🔗 GitHub: 

---

## 🎓 FIAP - Análise e Desenvolvimento de Sistemas

Desenvolvido para o desafio de **Eventos Extremos** com foco em soluções para situações emergenciais e sociais.
