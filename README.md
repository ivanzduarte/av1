
# Sistema Java com Gerenciamento de Relacionamentos entre Entidades

### 📋 Descrição Geral

Este sistema foi desenvolvido em Java para ilustrar o funcionamento de operações básicas de CRUD (criação, leitura, atualização e remoção) junto com a manipulação de vínculos entre diferentes entidades no banco de dados. Foram utilizadas tecnologias modernas como Java 17, Spring Boot 3.1.0, Spring Data JPA, Lombok, MariaDB e Maven para garantir a robustez da aplicação.

### 🏗️ Estrutura e Organização

O projeto adota a arquitetura baseada no padrão MVC (Model-View-Controller), separando as responsabilidades em diferentes camadas para maior clareza e manutenção. As entidades representam o modelo de dados. Os repositórios lidam com o acesso ao banco. A camada de serviços centraliza as regras de negócio e as validações. Já a interface com o usuário é construída através de JSF e páginas XHTML.

### 🔗 Modelagem de Relacionamentos

Foram implementadas duas relações entre entidades. A primeira é a associação Um-para-Muitos (One-to-Many), entre Pessoa e Telefone, onde cada pessoa pode possuir vários telefones, com o controle de integridade feito por operações em cascata. A segunda é uma ligação Muitos-para-Muitos (Many-to-Many) entre Aluno e Curso, permitindo que vários alunos possam se inscrever em vários cursos simultaneamente, utilizando uma tabela auxiliar para armazenar essas associações.

### 🚀 Funcionalidades Disponíveis

Entre os principais recursos desenvolvidos, destacam-se o cadastro de novos registros, a visualização e busca de dados, a edição e remoção de informações existentes, a navegação entre entidades relacionadas e a apresentação de mensagens de validação e erro, garantindo maior usabilidade.

### 🛠️ Ferramentas e Tecnologias

O sistema utiliza Java 17, Spring Boot 3.1.0, Spring Data JPA, Lombok, MariaDB e Maven, proporcionando uma infraestrutura moderna e eficiente para desenvolvimento web.

### 📌 Ambiente Necessário

Para executar o projeto localmente, é preciso ter o JDK 11 ou superior, o Maven instalado, uma IDE de preferência (como Eclipse, IntelliJ IDEA ou Visual Studio Code) e um servidor de aplicações compatível com Java EE, como TomEE, WildFly ou GlassFish.

### 🛠️ Guia de Execução

Primeiramente, é necessário clonar o repositório e ajustar as configurações de conexão com o banco de dados MariaDB. Depois, o projeto deve ser compilado através do Maven e feito o deploy no servidor de aplicações. Por fim, a aplicação poderá ser acessada através do navegador.

### 📚 Considerações Finais

Este trabalho tem um propósito acadêmico, mas a estrutura implementada foi pensada para facilitar futuras expansões e integrações com outros módulos. O código organizado e a separação de camadas tornam a aplicação flexível, segura e de fácil manutenção.


### 👨‍💻 Autor

**Ivan Duarte Câmara Rocha (RA:12120866)**


