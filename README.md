# DSList - Catálogo de Jogos

Projeto backend em Java com Spring Boot para gerenciamento de listas de jogos. Desenvolvido durante o Intensivão Java Spring da DevSuperior.

## Tecnologias

- Java 17
- Spring Boot
- Spring Data JPA
- PostgreSQL (produção/desenvolvimento)
- H2 Database (testes)
- Maven

## Como executar

1. Clone o repositório
2. Configure o banco de dados (PostgreSQL ou H2)
3. Ajuste as propriedades em `src/main/resources/application-*.properties`
4. Execute:
   ```bash
   ./mvnw spring-boot:run
   ```
5. Acesse a API em `http://localhost:8080`

## Modelo de Domínio

![Modelo de domínio DSList](https://raw.githubusercontent.com/devsuperior/java-spring-dslist/main/resources/dslist-model.png)

## Exemplos de configuração

**application.properties**

```
spring.profiles.active=${APP_PROFILE:test}
spring.jpa.open-in-view=false
cors.origins=${CORS_ORIGINS:http://localhost:5173,http://localhost:3000}
```

**application-dev.properties**

```
spring.datasource.url=jdbc:postgresql://localhost:5432/dscatalog
spring.datasource.username=postgres
spring.datasource.password=1234567
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
spring.jpa.hibernate.ddl-auto=none
```

**application-test.properties**

```
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

## Popular banco de dados (import.sql)

```sql
INSERT INTO tb_game_list (name) VALUES ('Aventura e RPG');
INSERT INTO tb_game_list (name) VALUES ('Jogos de plataforma');
-- demais inserts...
```

## Dúvidas

Acesse [devsuperior.com.br](https://devsuperior.com.br) para mais informações e suporte.

## 📫 Contato

<div align="center">

<a href="mailto:cardosofiles@outlook.com">
  <img src="https://img.shields.io/badge/Email-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white" alt="Email"/>
</a>
<a href="https://www.linkedin.com/in/joaobatista-dev/" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
</a>
<a href="https://github.com/Cardosofiles" target="_blank">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
</a>
<a href="https://cardosofiles.dev/" target="_blank">
  <img src="https://img.shields.io/badge/Portfólio-222222?style=for-the-badge&logo=about.me&logoColor=white" alt="Portfólio"/>
</a>

</div>
