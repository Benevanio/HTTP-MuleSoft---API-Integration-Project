# MuleSoft Complete Learning Repository

Este repositório é uma coleção abrangente de projetos e exemplos MuleSoft desenvolvidos no Anypoint Studio, cobrindo os principais conceitos e tecnologias da plataforma MuleSoft.

## 📋 Visão Geral

Este repositório serve como um guia completo para aprendizado e referência das principais tecnologias MuleSoft, incluindo:

### 🔗 **HTTP & API Integration**
- Configuração de HTTP Listeners e Request
- Consumo de APIs RESTful
- Implementação de endpoints HTTP
- Tratamento de headers e parâmetros

### 📊 **DataWeave**
- Transformações de dados complexas
- Mapeamento entre diferentes formatos (JSON, XML, CSV)
- Funções avançadas do DataWeave
- Filtros, agregações e manipulação de arrays

### ⚠️ **Error Handling**
- Implementação de try-catch blocks
- Error handlers customizados
- Propagação e tratamento de erros
- Logging e monitoramento de erros

### 🗄️ **Database Integration**
- Conectores de banco de dados
- Operações CRUD (Create, Read, Update, Delete)
- Transações e pooling de conexões
- Integração com diferentes SGBDs

### 📨 **ActiveMQ & Message Queuing**
- Configuração de conectores JMS
- Publicação e consumo de mensagens
- Filas e tópicos
- Padrões de messaging assíncronos

### 📋 **RAML & API Design**
- Documentação de APIs com RAML
- Geração de interfaces a partir de RAML
- Validação automática de schemas
- Implementação de APIs contract-first

## 🛠️ Tecnologias e Componentes Utilizados

- **MuleSoft Runtime**: 4.9.0
- **Java**: 17
- **Maven**: Para gerenciamento de dependências
- **HTTP Connector**: Para integrações REST/HTTP
- **Database Connector**: Para operações de banco de dados
- **JMS Connector**: Para ActiveMQ e messaging
- **DataWeave**: Para transformações de dados
- **RAML**: Para design e documentação de APIs
- **Error Handling**: Para tratamento robusto de erros
- **Sockets Connector**: Para comunicações de baixo nível

## 📁 Estrutura do Projeto

```
mulesoft-learning-repository/
├── src/
│   ├── main/
│   │   ├── mule/
│   │   │   ├── global.xml                 # Configurações globais
│   │   │   ├── http/
│   │   │   │   └── http-mulesoft.xml      # Exemplos HTTP
│   │   │   ├── events/
│   │   │   │   └── events.xml             # Event handling
│   │   │   ├── dataweave/
│   │   │   │   └── transformations.xml    # DataWeave examples
│   │   │   ├── database/
│   │   │   │   └── db-operations.xml      # Database operations
│   │   │   ├── messaging/
│   │   │   │   └── activemq-flows.xml     # ActiveMQ messaging
│   │   │   └── error-handling/
│   │   │       └── error-flows.xml        # Error handling patterns
│   │   └── resources/
│   │       ├── log4j2.xml                 # Configuração de logs
│   │       ├── api/
│   │       │   └── *.raml                 # RAML specifications
│   │       ├── dataweave/
│   │       │   └── *.dwl                  # DataWeave scripts
│   │       └── sample-data/
│   │           └── *.json, *.xml, *.csv   # Sample data files
│   └── test/
│       ├── munit/                         # Testes MUnit
│       └── resources/
├── exchange-docs/                         # Documentação Exchange
│   └── home.md
├── pom.xml                                # Configuração Maven
├── mule-artifact.json                     # Configuração do artefato Mule
└── readme.md                              # Este arquivo
```

## 🚀 Como Executar

### Pré-requisitos

- Java 17
- Anypoint Studio 7.x ou superior
- Maven 3.6+
- Banco de dados (MySQL/PostgreSQL/H2) para exemplos de Database
- ActiveMQ ou broker JMS para exemplos de messaging

### Passos para Execução

1. **Clone o projeto** (se aplicável) ou abra no Anypoint Studio

2. **Configure as dependências locais**:
   - Configure conexões de banco de dados no arquivo de configuração
   - Configure broker ActiveMQ se necessário

3. **Instale as dependências**:
   ```bash
   mvn clean install
   ```

4. **Execute a aplicação**:
   - No Anypoint Studio: Clique com o botão direito no projeto → Run As → Mule Application
   - Via linha de comando:
     ```bash
     mvn mule:run
     ```

5. **Explore os diferentes módulos**:
   - Cada pasta contém exemplos específicos de uma tecnologia
   - Consulte a documentação individual de cada módulo

## 🔧 Módulos e Exemplos Disponíveis

### 🌐 HTTP Module
- **Endpoints**: Múltiplos endpoints demonstrando diferentes padrões HTTP
- **URL Base**: `http://localhost:8081/`
- **Exemplos**:
  - `/api/users` - Consumo de APIs externas
  - `/api/transform` - Transformações HTTP
  - `/api/upload` - Upload de arquivos

### 🔄 DataWeave Examples
- **Transformações JSON → XML**
- **Manipulação de Arrays e Objetos**
- **Funções avançadas (map, filter, reduce)**
- **Agregações e joins de dados**

### 🗄️ Database Operations
- **CRUD Operations**
- **Transações**
- **Bulk Operations**
- **Stored Procedures**

### 📨 ActiveMQ Messaging
- **Publishers e Consumers**
- **Queue Management**
- **Topic Subscriptions**
- **Dead Letter Queues**

### ⚠️ Error Handling Patterns
- **Try-Catch Implementations**
- **Custom Error Types**
- **Error Propagation**
- **Retry Mechanisms**

### 📋 RAML API Specifications
- **API Documentation**
- **Schema Validation**
- **Contract Testing**
- **Mock Services**

## 🏗️ Arquitetura e Padrões

### Organização Modular
O projeto está organizado em módulos independentes, cada um focado em uma tecnologia específica:

1. **HTTP Module**: Padrões de comunicação REST/HTTP
2. **DataWeave Module**: Transformações e manipulação de dados
3. **Database Module**: Operações de persistência e transações
4. **Messaging Module**: Comunicação assíncrona com ActiveMQ
5. **Error Handling Module**: Padrões de tratamento de erros
6. **RAML Module**: Design e documentação de APIs

### Configurações Globais
- **Global Elements**: Reutilização de configurações
- **Property Files**: Externalização de configurações
- **Environment-specific**: Configurações por ambiente

### Padrões Implementados
- **Request-Response**: Comunicação síncrona
- **Publish-Subscribe**: Messaging assíncrono
- **Scatter-Gather**: Processamento paralelo
- **Error Handling**: Tratamento robusto de falhas

## 📝 Logs e Monitoramento

Os logs são configurados através do arquivo `log4j2.xml` e incluem:
- **HTTP Requests/Responses**: Monitoramento de APIs
- **DataWeave Transformations**: Debug de transformações
- **Database Operations**: Tracking de operações SQL
- **Message Processing**: Logs de ActiveMQ
- **Error Events**: Rastreamento detalhado de erros
- **Performance Metrics**: Métricas de performance

### Níveis de Log
- **DEBUG**: Informações detalhadas para desenvolvimento
- **INFO**: Operações normais do sistema
- **WARN**: Situações que requerem atenção
- **ERROR**: Erros que precisam de intervenção

## 🧪 Testes

### Estrutura de Testes
```bash
# Executar todos os testes
mvn test

# Executar testes específicos por módulo
mvn test -Dtest=HTTPModuleTest
mvn test -Dtest=DataWeaveTest
mvn test -Dtest=DatabaseTest
mvn test -Dtest=MessagingTest
```

### Tipos de Teste
- **Unit Tests**: Testes unitários com MUnit
- **Integration Tests**: Testes de integração entre módulos
- **Performance Tests**: Testes de carga e performance
- **Contract Tests**: Validação de contratos RAML

### Ferramentas de Teste
- **MUnit**: Framework principal de testes
- **Mock Services**: Simulação de APIs externas
- **Test Data**: Dados de teste organizados
- **Assertions**: Validações customizadas

## 📦 Build e Deploy

### Build Local
```bash
# Build completo
mvn clean package

# Build com testes
mvn clean install

# Build específico por módulo
mvn clean package -pl http-module
mvn clean package -pl dataweave-module
```

### Deploy para Different Environments

#### CloudHub Deploy
```bash
# Deploy para Development
mvn deploy -DmuleDeploy -Denv=dev

# Deploy para Production
mvn deploy -DmuleDeploy -Denv=prod
```

#### On-Premises Deploy
```bash
# Deploy local
mvn mule:deploy

# Deploy específico
mvn mule:deploy -Dtarget=on-premises
```

### Profiles Maven
- **dev**: Desenvolvimento local
- **test**: Ambiente de testes
- **prod**: Ambiente de produção

## 🔒 Configurações de Segurança

### Comunicação Segura
- **HTTPS/TLS**: Configurações para comunicação segura
- **Certificates**: Gerenciamento de certificados
- **OAuth 2.0**: Implementação de autenticação OAuth

### Database Security
- **Connection Pooling**: Segurança em pools de conexão
- **Encrypted Passwords**: Senhas criptografadas
- **SQL Injection Prevention**: Prevenção de ataques SQL

### Message Security
- **JMS Security**: Autenticação em brokers JMS
- **Message Encryption**: Criptografia de mensagens
- **Access Control**: Controle de acesso a filas

### API Security
- **API Keys**: Implementação de chaves de API
- **Rate Limiting**: Limitação de taxa de requisições
- **CORS**: Configuração de CORS para APIs

## � Recursos de Aprendizado

### Documentação por Módulo
- **[HTTP Integration Guide](docs/http-guide.md)**: Guia completo de HTTP
- **[DataWeave Tutorial](docs/dataweave-tutorial.md)**: Tutorial DataWeave
- **[Database Best Practices](docs/database-guide.md)**: Práticas de banco de dados
- **[ActiveMQ Patterns](docs/messaging-guide.md)**: Padrões de messaging
- **[Error Handling Strategies](docs/error-handling.md)**: Estratégias de erro
- **[RAML Design Guide](docs/raml-guide.md)**: Design de APIs com RAML

### Exemplos Práticos
Cada módulo contém exemplos progressivos:
1. **Básico**: Conceitos fundamentais
2. **Intermediário**: Implementações práticas
3. **Avançado**: Padrões complexos e otimizações

### Recursos Externos
- [MuleSoft Documentation](https://docs.mulesoft.com/)
- [DataWeave Playground](https://developer.mulesoft.com/learn/dataweave)
- [RAML Specification](https://raml.org/)

## 🎯 Objetivos de Aprendizado

Ao concluir este repositório, você será capaz de:

### ✅ HTTP & APIs
- Configurar e consumir APIs REST
- Implementar padrões de comunicação HTTP
- Gerenciar headers, parâmetros e autenticação

### ✅ DataWeave
- Realizar transformações complexas de dados
- Utilizar funções avançadas do DataWeave
- Implementar mapeamentos entre diferentes formatos

### ✅ Database Integration
- Conectar e operar com diferentes SGBDs
- Implementar transações e controle de concorrência
- Otimizar performance de queries

### ✅ Messaging & ActiveMQ
- Configurar brokers JMS
- Implementar padrões pub/sub
- Gerenciar filas e tratamento de mensagens

### ✅ Error Handling
- Implementar estratégias robustas de tratamento de erro
- Configurar logging e monitoramento
- Criar fluxos de recuperação automática

### ✅ API Design & RAML
- Projetar APIs seguindo padrões REST
- Documentar APIs com RAML
- Implementar validações e contracts

## 📋 Roadmap e Próximos Passos

### Fase 1 - Fundamentos ✅
- [x] Estrutura base do projeto
- [x] Configuração HTTP básica
- [x] Documentação inicial

### Fase 2 - Módulos Core 🚧
- [ ] Implementar módulo DataWeave completo
- [ ] Adicionar exemplos de Database
- [ ] Configurar ActiveMQ e messaging
- [ ] Implementar error handling patterns

### Fase 3 - Recursos Avançados 📋
- [ ] RAML specifications e contract testing
- [ ] Performance optimization
- [ ] Security implementations
- [ ] Monitoring e observability

### Fase 4 - Melhorias e Expansão 📋
- [ ] CI/CD pipeline
- [ ] Docker containerization
- [ ] Cloud deployment examples
- [ ] Advanced patterns e best practices

## 🤝 Contribuição

Contribuições são sempre bem-vindas! Este é um projeto de aprendizado colaborativo.

### Como Contribuir

1. **Fork o projeto**
2. **Crie uma branch para sua feature**:
   ```bash
   git checkout -b feature/novo-exemplo-dataweave
   git checkout -b fix/correcao-database
   git checkout -b docs/tutorial-activemq
   ```
3. **Commit suas mudanças**:
   ```bash
   git commit -m 'feat: adiciona exemplo de transformação JSON'
   git commit -m 'fix: corrige conexão com MySQL'
   git commit -m 'docs: atualiza tutorial ActiveMQ'
   ```
4. **Push para a branch**:
   ```bash
   git push origin feature/novo-exemplo-dataweave
   ```
5. **Abra um Pull Request**

### Tipos de Contribuição
- 🐛 **Bug Fixes**: Correções de bugs
- ✨ **Features**: Novos exemplos e funcionalidades
- 📚 **Documentation**: Melhorias na documentação
- 🎨 **Code Style**: Melhorias na organização do código
- ⚡ **Performance**: Otimizações de performance
- 🧪 **Tests**: Adição ou melhoria de testes

### Guidelines
- Mantenha os exemplos simples e bem documentados
- Adicione testes para novos exemplos
- Siga os padrões de nomenclatura existentes
- Atualize a documentação relevante

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 📞 Suporte e Comunidade

### 🆘 Suporte Técnico
- **Issues**: [Criar uma issue](https://github.com/Benevanio/HTTP-MuleSoft---API-Integration-Project/issues)
- **Discussions**: [Participar das discussões](https://github.com/Benevanio/HTTP-MuleSoft---API-Integration-Project/discussions)
- **Wiki**: [Consultar a wiki do projeto](https://github.com/Benevanio/HTTP-MuleSoft---API-Integration-Project/wiki)

### 🌐 Comunidade MuleSoft
- [MuleSoft Community](https://help.mulesoft.com/)
- [MuleSoft Training](https://training.mulesoft.com/)
- [MuleSoft Blog](https://blogs.mulesoft.com/)

### 📧 Contato
- **Maintainer**: [Benevanio](https://github.com/Benevanio)
- **Email**: Entre em contato através das issues do GitHub

---

**🚀 Desenvolvido com ❤️ usando MuleSoft Anypoint Platform**

*Este repositório é um recurso educacional para a comunidade MuleSoft. Contribuições e feedback são sempre bem-vindos!*