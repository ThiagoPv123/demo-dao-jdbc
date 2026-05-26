# Demo DAO JDBC

Implementação do padrão DAO (Data Access Object) com JDBC puro e MySQL,
desenvolvida durante o curso Java Completo da Udemy. Objetivo: entender
acesso a dados sem abstração de framework.

## O que apliquei

- Padrão DAO com interfaces (`SellerDao`, `DepartmentDao`) e implementação concreta via JDBC (`SellerDaoJDBC`)
- `DaoFactory` para centralizar a criação dos DAOs e desacoplar a implementação do cliente
- Classe `DB` com conexão singleton, carregamento de `db.properties` e métodos utilitários para fechar `Statement` e `ResultSet` sem vazamento de recursos
- Exceções customizadas (`DbException`, `DbIntegrityException`) para separar erros de SQL de violações de integridade referencial
- Operações CRUD com `PreparedStatement` em entidades com relacionamento (`Seller` → `Department`)

## Stack

Java · JDBC · MySQL · Maven

## Como executar

1. Clonar o repositório
2. Criar o banco `coursejdbc` no MySQL local
3. Copiar `db.properties.example` para `db.properties` e preencher com suas credenciais
4. Executar `application/Program.java` pela IDE

## Status

Concluído como estudo do curso. O projeto cobre apenas `SellerDaoJDBC`; `DepartmentDaoJDBC` pode ser implementado como extensão do estudo.