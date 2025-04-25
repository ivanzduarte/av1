📋 Task Manager - Aplicação Spring Boot com MariaDB
Este projeto é uma aplicação web desenvolvida com Spring Boot e banco de dados MariaDB, com o objetivo de gerenciar usuários e tarefas. Ele permite realizar todas as operações básicas de um sistema CRUD (Criar, Consultar, Atualizar e Deletar).

🗂️ Sumário
Requisitos para rodar

Configurando o Banco de Dados

Instalação do XAMPP

Criação do banco taskmanager

Configuração de acesso

Configurações do Projeto

Arquivo application.properties

Dependências utilizadas

Como executar o sistema

Iniciando os serviços

Rodando a aplicação

Testando os endpoints

Validação dos dados

Considerações finais

1. Requisitos para rodar
Para conseguir compilar e executar o projeto, é necessário ter o seguinte ambiente configurado:

Java 11 ou superior instalado (JDK)

XAMPP com MariaDB ativo

Alguma IDE Java (IntelliJ, Eclipse, VSCode, etc.)

Postman (opcional, mas útil para testar a API)

2. Configurando o Banco de Dados
Instalação do XAMPP
Acesse o site https://www.apachefriends.org e baixe o instalador.

Instale e abra o painel do XAMPP.

Inicie o serviço MariaDB clicando em "Start".

Criação do banco taskmanager
Abra o phpMyAdmin acessando http://localhost/phpmyadmin/ e siga os passos:

Vá até a aba "Databases"

Crie um banco com o nome taskmanager

Ou, se preferir usar o console do MariaDB:

sql
Copiar
Editar
CREATE DATABASE taskmanager;
Configuração de acesso
A porta padrão do MariaDB geralmente é 3306, mas pode ser necessário usar 3307 dependendo da instalação. O acesso ao banco é configurado no arquivo application.properties.

3. Configurações do Projeto
Arquivo application.properties
Configure este arquivo em src/main/resources/ com as credenciais corretas do seu ambiente:

properties
Copiar
Editar
spring.application.name=persistenciadadosav1
spring.datasource.url=jdbc:mariadb://localhost:3306/taskmanager
spring.datasource.username=root
spring.datasource.password= # coloque a senha do seu banco ou deixe em branco se não houver
spring.datasource.driver-class-name=org.mariadb.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MariaDBDialect
Dependências utilizadas
O projeto usa bibliotecas e frameworks como:

Spring Boot Starter Web

Spring Data JPA

MariaDB Driver

4. Como executar o sistema
Iniciando os serviços
Abra o XAMPP e inicie o MariaDB

Verifique se o banco taskmanager está criado e acessível

Rodando a aplicação
Importe o projeto na sua IDE

Execute a classe principal com a anotação @SpringBootApplication

O sistema será iniciado na porta 8080

Acesse em: http://localhost:8080

Testando os endpoints
Com o Postman (ou outro cliente HTTP), envie requisições para testar os recursos da API. Exemplos:

POST /usuarios → cria um novo usuário

GET /usuarios → retorna a lista de usuários

PUT /usuarios/{id} → atualiza um usuário

DELETE /usuarios/{id} → remove um usuário

5. Validação dos dados
Você pode validar se os dados estão sendo salvos corretamente consultando diretamente no banco via phpMyAdmin ou terminal com os seguintes comandos:

sql
Copiar
Editar
SHOW TABLES;
SELECT * FROM usuarios;
SELECT * FROM tarefas;
6. Considerações finais
Esse projeto é uma ótima base para qualquer aplicação que precise de um backend estruturado com Java. Ele cobre desde a configuração inicial até testes com ferramentas reais, e pode ser expandido facilmente para incluir autenticação, relacionamentos mais complexos e deploy em produção.
