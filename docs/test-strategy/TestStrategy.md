# Test Strategy - ServeRest API

## 1. Objetivo

Definir a estratégia de testes para validação da API ServeRest, garantindo a qualidade das funcionalidades, segurança, desempenho e conformidade com os requisitos do sistema.

---

## 2. Escopo

Os testes contemplam os seguintes módulos:

### Login

* Autenticação de usuários
* Geração de token
* Validação de credenciais

### Usuários

* Cadastro
* Consulta
* Atualização
* Exclusão

### Produtos

* Cadastro
* Consulta
* Atualização
* Exclusão

### Carrinhos

* Criação
* Consulta
* Conclusão de compra
* Cancelamento

### Segurança

* Autenticação
* Autorização
* Controle de acesso

### Performance

* Testes de carga
* Testes de concorrência
* Análise de tempo de resposta

---

## 3. Fora de Escopo

Os seguintes itens não serão contemplados nesta fase:

* Testes de interface mobile
* Testes de compatibilidade entre navegadores
* Testes de acessibilidade
* Testes de recuperação de desastre

---

## 4. Tipos de Teste

### Testes Funcionais

Validação dos requisitos funcionais da API.

Exemplos:

* Cadastro de usuário
* Login
* Cadastro de produto
* Criação de carrinho

### Testes Negativos

Validação do comportamento do sistema diante de entradas inválidas.

Exemplos:

* Email duplicado
* Senha inválida
* Token inválido

### Testes de API

Validação dos endpoints REST utilizando Postman.

Serão avaliados:

* Status Code
* Payload
* Headers
* Tempo de resposta

### Testes de Performance

Validação do comportamento da API sob carga utilizando JMeter.

Serão realizados:

* Load Test
* Stress Test
* Concurrency Test

### Testes de Segurança

Validação de autenticação e autorização.

Exemplos:

* Acesso sem token
* Token inválido
* Usuário sem permissão

---

## 5. Critérios de Entrada

Os testes poderão ser iniciados quando:

* API estiver disponível
* Endpoints documentados
* Ambiente configurado
* Massa de testes preparada

---

## 6. Critérios de Saída

Os testes serão considerados concluídos quando:

* Todos os cenários críticos forem executados
* Defeitos críticos forem resolvidos
* Evidências forem registradas
* Relatórios forem gerados

---

## 7. Riscos

| Risco                     | Impacto |
| ------------------------- | ------- |
| Indisponibilidade da API  | Alto    |
| Dados inconsistentes      | Médio   |
| Mudança de requisitos     | Médio   |
| Instabilidade do ambiente | Alto    |

---

## 8. Ferramentas Utilizadas

| Ferramenta     | Finalidade            |
| -------------- | --------------------- |
| Postman        | Testes de API         |
| Newman         | Execução automatizada |
| Cypress        | Automação de testes   |
| Cucumber       | BDD                   |
| JMeter         | Performance           |
| Jira           | Gestão de defeitos    |
| GitHub         | Controle de versão    |
| GitHub Actions | Integração contínua   |

---

## 9. Evidências

Todas as evidências geradas durante a execução dos testes serão armazenadas nos diretórios:

* docs/test-cases
* docs/bug-reports
* postman/reports
* performance/jmeter/reports

---

## 10. Aprovação

Este documento define a estratégia inicial para execução dos testes da API ServeRest e servirá como base para os próximos artefatos do projeto:

* Test Scenarios
* Test Cases
* Bug Reports
* Automação com Cypress
* BDD com Cucumber
* Testes de Performance
* CI/CD
