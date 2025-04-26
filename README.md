# Sistema CRUD Java com Relacionamentos Complexos

## 📝 Descrição do Projeto
Aplicação Java robusta demonstrando operações CRUD avançadas com múltiplos relacionamentos entre entidades. Desenvolvido como material didático para mostrar:
- Padrões de persistência com JPA/Hibernate
- Boas práticas em arquitetura Java EE
- Implementação de relacionamentos complexos
- Interface web responsiva com JSF

## 🧱 Estrutura Técnica
Organização em camadas bem definidas:
1. **Domínio**: Entidades JPA com anotações de relacionamento
2. **Repositórios**: DAOs especializados para cada entidade
3. **Serviços**: Regras de negócio e transações
4. **Web**: Controles JSF e páginas Facelets
5. **Utilitários**: Conversores, validadores e helpers

## ⛓ Relacionamentos Chave
### 1. Composição (One-to-Many)
- `Cliente` → `Endereço` (um cliente com múltiplos endereços)
- Deleção em cascata configurada
- Ordenação de coleções com `@OrderColumn`

### 2. Matrícula (Many-to-Many)
- `Estudante` ↔ `Disciplina` via tabela associativa
- Atributos extras na relação (data_matricula, status)
- Consultas JPQL otimizadas

### 3. Herança (Single Table)
- `Funcionario` como superclasse
- Subclasses `Gerente` e `Vendedor`
- Estratégia SINGLE_TABLE com discriminador

## 🛠️ Stack Tecnológico
- **Core**: Java 11+, CDI 2.0, EJB Lite 3.2
- **Persistência**: JPA 2.2, Hibernate 5.4, Flyway
- **Web**: JSF 2.3, PrimeFaces 10, AJAX
- **Infra**: Maven, Docker (perfis de deploy)
- **Testes**: Arquillian, DBUnit

## ✅ Funcionalidades Destacadas
- Associação/desassociação de entidades via UI
- Paginação e filtros em listagens
- Relatórios Jasper integrados
- Exportação para Excel/PDF
- Validação cross-field
- Histórico de alterações (Envers)

## ⚙️ Configuração
1. Pré-requisitos:
   - Docker (para banco de dados)
   - Maven configurado
   - Java JDK 11+

2. Comandos:
```bash
git clone [repositório]
cd projeto-crud
mvn clean package tomee:run
