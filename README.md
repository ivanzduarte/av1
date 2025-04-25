# Persistência de Dados - Spring Boot com MariaDB

Este projeto foi desenvolvido utilizando Spring Boot em conjunto com MariaDB para gerenciar um sistema de tarefas. O objetivo é possibilitar operações CRUD (Criar, Ler, Atualizar, Deletar) para usuários e suas respectivas tarefas.

## Índice

- [Requisitos](#requisitos)
- [Configuração do Banco de Dados](#configuração-do-banco-de-dados)
  - [Instalar XAMPP](#instalar-xampp)
  - [Criar Banco de Dados](#criar-banco-de-dados)
- [Configuração da Aplicação](#configuração-da-aplicação)
  - [application.properties](#applicationproperties)
  - [Dependências](#dependências)
- [Executando o Projeto](#executando-o-projeto)
  - [Iniciar MariaDB](#iniciar-mariadb)
  - [Executar Aplicação](#executar-aplicação)
  - [Testar Endpoints](#testar-endpoints)
- [Testes e Validação](#testes-e-validação)
  - [Testes com Postman](#testes-com-postman)
  - [Verificação no Banco de Dados](#verificação-no-banco-de-dados)
- [Conclusão](#conclusão)

## Requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas:

- JDK 11+ (Java Development Kit)
- XAMPP (para rodar o MariaDB)
- IDE de sua preferência (IntelliJ IDEA, Eclipse, VSCode, etc.)
- Postman (opcional, para testar os endpoints da API)

## Configuração do Banco de Dados

### Instalar XAMPP

1. Baixe e instale o [XAMPP](https://www.apachefriends.org/index.html).
2. Abra o painel de controle do XAMPP e inicie o MariaDB clicando em "Start" ao lado do MariaDB.

### Criar Banco de Dados

1. Acesse o phpMyAdmin em [http://localhost/phpmyadmin/](http://localhost/phpmyadmin/).
2. Na aba "Databases", crie um novo banco de dados chamado `taskmanager`.

   Se preferir usar o terminal, execute o comando SQL:

   ```sql
   CREATE DATABASE taskmanager;
Configuração da Aplicação
application.properties
O arquivo de configuração do Spring Boot é o application.properties. Faça as seguintes modificações para conectar à sua instância do MariaDB:

properties
Copiar
Editar
spring.application.name=persistenciadadosav1
spring.datasource.url=jdbc:mariadb://localhost:3306/taskmanager
spring.datasource.username=root
spring.datasource.password=senha_aqui
spring.datasource.driver-class-name=org.mariadb.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MariaDBDialect
Executando o Projeto
Iniciar MariaDB
Abra o painel do XAMPP e clique em "Start" para iniciar o MariaDB.

Verifique se o banco de dados taskmanager foi criado corretamente e está funcionando.

Executar Aplicação
Abra a sua IDE e execute a classe principal do Spring Boot (com a anotação @SpringBootApplication).

A aplicação será iniciada na porta 8080 por padrão (ou na porta configurada no arquivo application.properties).

Testar Endpoints
Agora, você pode testar os endpoints da API utilizando ferramentas como o Postman. Alguns exemplos de endpoints são:

POST /usuarios: Criar um novo usuário.

GET /usuarios: Listar todos os usuários.

PUT /usuarios/{id}: Atualizar um usuário existente.

DELETE /usuarios/{id}: Deletar um usuário.

Testes e Validação
Testes com Postman
Utilize o Postman para fazer requisições para os endpoints da API, por exemplo:

Criar Usuário:

Método: POST URL: http://localhost:8080/usuarios Corpo: JSON com os dados do usuário.

Listar Usuários:

Método: GET URL: http://localhost:8080/usuarios

Atualizar Usuário:

Método: PUT URL: http://localhost:8080/usuarios/{id} Corpo: JSON com os dados atualizados.

Deletar Usuário:

Método: DELETE URL: http://localhost:8080/usuarios/{id}

Verificação no Banco de Dados
Você pode usar o phpMyAdmin ou comandos SQL para verificar se as alterações realizadas na aplicação foram aplicadas corretamente ao banco de dados:

Listar tabelas:

sql
Copiar
Editar
SHOW TABLES;
Verificar dados na tabela de usuários:

sql
Copiar
Editar
SELECT * FROM usuarios;
Verificar dados na tabela de tarefas:

sql
Copiar
Editar
SELECT * FROM tarefas;
Conclusão
Este projeto demonstra como integrar Spring Boot com MariaDB para gerenciar um sistema de tarefas com operações CRUD. Através da configuração adequada do banco de dados e da aplicação, é possível realizar as operações de criação, leitura, atualização e exclusão de usuários e tarefas. A validação dos dados pode ser feita via Postman e verificação direta no banco de dados utilizando SQL.
