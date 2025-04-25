# ✅ Gerenciador de Tarefas com Spring Boot & MariaDB

Este projeto é uma API RESTful feita com **Spring Boot** e **MariaDB** para controle de usuários e tarefas. A aplicação permite cadastrar, listar, atualizar e excluir registros, seguindo o padrão CRUD.

Ideal para quem está aprendendo back-end com Java e quer ver na prática como funciona a integração com banco de dados relacional.

---

## 📚 Conteúdo

- [O que você vai precisar](#o-que-você-vai-precisar)
- [Configurando o Banco de Dados](#configurando-o-banco-de-dados)
- [Ajustando o Projeto](#ajustando-o-projeto)
- [Executando a Aplicação](#executando-a-aplicação)
- [Como testar a API](#como-testar-a-api)
- [Verificando os dados no banco](#verificando-os-dados-no-banco)
- [Considerações finais](#considerações-finais)

---

## 🧰 O que você vai precisar

Antes de rodar a aplicação, é importante ter algumas ferramentas já instaladas:

- **Java 11 ou superior**
- **XAMPP** (para rodar o MariaDB)
- **IDE Java** de sua preferência (ex: IntelliJ, Eclipse ou VSCode)
- **Postman** ou Insomnia (para testar os endpoints da API)

---

## 🛠️ Configurando o Banco de Dados

### 1. Instalando e ativando o MariaDB

- Acesse o site oficial do [XAMPP](https://www.apachefriends.org/) e faça o download.
- Instale normalmente e abra o painel de controle.
- Inicie o serviço do **MariaDB** clicando em “Start”.

### 2. Criando o banco de dados

Abra o **phpMyAdmin** acessando `http://localhost/phpmyadmin` e:

- Clique em **Databases**
- Crie um novo banco com o nome: `taskmanager`

Ou, se preferir linha de comando:

```sql
CREATE DATABASE taskmanager;
