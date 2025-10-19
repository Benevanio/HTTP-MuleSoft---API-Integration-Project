# HTTP MuleSoft - API Integration Project

Este projeto é uma aplicação MuleSoft desenvolvida no Anypoint Studio que demonstra a integração HTTP com APIs externas, especificamente consumindo dados da API ReqRes.

## 📋 Visão Geral

O projeto implementa um fluxo simples que:
- Expõe um endpoint HTTP local na porta 8081
- Consome dados da API externa ReqRes (https://reqres.in)
- Retorna os dados dos usuários obtidos da API externa

## 🛠️ Tecnologias Utilizadas

- **MuleSoft Runtime**: 4.9.0
- **Java**: 17
- **Maven**: Para gerenciamento de dependências
- **HTTP Connector**: 1.10.3
- **Sockets Connector**: 1.2.5

## 📁 Estrutura do Projeto

```
http-mulesoft/
├── src/
│   ├── main/
│   │   ├── mule/
│   │   │   └── http-mulesoft.xml          # Fluxo principal da aplicação
│   │   └── resources/
│   │       ├── log4j2.xml                 # Configuração de logs
│   │       └── api/                       # Recursos da API
│   └── test/
│       ├── munit/                         # Testes MUnit
│       └── resources/
├── pom.xml                                # Configuração Maven
├── mule-artifact.json                     # Configuração do artefato Mule
└── readme.md                              # Este arquivo
```

## 🚀 Como Executar

### Pré-requisitos

- Java 17
- Anypoint Studio 7.x ou superior
- Maven 3.6+

### Passos para Execução

1. **Clone o projeto** (se aplicável) ou abra no Anypoint Studio

2. **Instale as dependências**:
   ```bash
   mvn clean install
   ```

3. **Execute a aplicação**:
   - No Anypoint Studio: Clique com o botão direito no projeto → Run As → Mule Application
   - Via linha de comando:
     ```bash
     mvn mule:run
     ```

4. **Teste a aplicação**:
   A aplicação estará disponível em: `http://localhost:8081/api`

## 🔧 Endpoints Disponíveis

### GET /api
- **Descrição**: Retorna uma lista de usuários da API ReqRes
- **URL**: `http://localhost:8081/api`
- **Método**: GET
- **Response**: JSON com dados dos usuários

**Exemplo de resposta**:
```json
{
  "page": 1,
  "per_page": 6,
  "total": 12,
  "total_pages": 2,
  "data": [
    {
      "id": 1,
      "email": "george.bluth@reqres.in",
      "first_name": "George",
      "last_name": "Bluth",
      "avatar": "https://reqres.in/img/faces/1-image.jpg"
    }
  ]
}
```

## 🏗️ Arquitetura

### Fluxo Principal (http-mulesoftFlow)

1. **HTTP Listener**: Escuta requisições na porta 8081, path `/api`
2. **HTTP Request**: Faz uma requisição GET para `https://reqres.in/api/users`
3. **Logger**: Registra o payload recebido nos logs

### Configurações

- **HTTP Listener Config**: Configurado para escutar em `0.0.0.0:8081`
- **HTTP Request Config**: Configurado para acessar `reqres.in` via HTTPS

## 📝 Logs

Os logs são configurados através do arquivo `log4j2.xml` e incluem:
- Informações sobre as requisições recebidas
- Dados do payload retornado pela API externa
- Erros e informações de debug

## 🧪 Testes

Para executar os testes MUnit:

```bash
mvn test
```

Os testes estão localizados em `src/test/munit/` e utilizam o framework MUnit do MuleSoft.

## 📦 Build e Deploy

### Build Local
```bash
mvn clean package
```

### Deploy para CloudHub
1. Configure suas credenciais do Anypoint Platform
2. Execute:
   ```bash
   mvn deploy -DmuleDeploy
   ```

## 🔒 Configurações de Segurança

- A aplicação utiliza HTTPS para comunicação com APIs externas
- Configurações de TLS podem ser ajustadas conforme necessário
- Para ambientes de produção, considere implementar políticas de segurança adicionais

## 📋 Próximos Passos / Melhorias

- [ ] Implementar tratamento de erros mais robusto
- [ ] Adicionar autenticação/autorização
- [ ] Implementar cache para otimizar performance
- [ ] Adicionar mais endpoints
- [ ] Implementar validação de dados
- [ ] Adicionar métricas e monitoramento

## 🤝 Contribuição

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença [inserir licença]. Veja o arquivo `LICENSE` para mais detalhes.

## 📞 Suporte

Para suporte técnico ou dúvidas sobre o projeto:
- Crie uma issue no repositório
- Entre em contato com a equipe de desenvolvimento

---

**Desenvolvido com ❤️ usando MuleSoft Anypoint Platform**