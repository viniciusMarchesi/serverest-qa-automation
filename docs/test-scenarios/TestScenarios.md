# Test Scenarios - ServeRest API

## Legenda de Prioridade

* Alta (P1) → Funcionalidades críticas do negócio
* Média (P2) → Funcionalidades importantes
* Baixa (P3) → Funcionalidades complementares

| ID    | Módulo      | Cenário de Teste                                    | Prioridade |
| ----- | ----------- | --------------------------------------------------- | ---------- |
| TS001 | Login       | Realizar login com credenciais válidas              | P1         |
| TS002 | Login       | Realizar login com senha inválida                   | P1         |
| TS003 | Login       | Realizar login com email inexistente                | P1         |
| TS004 | Login       | Realizar login sem informar email                   | P1         |
| TS005 | Login       | Realizar login sem informar senha                   | P1         |
| TS006 | Login       | Validar geração de token após login                 | P1         |
| TS007 | Usuários    | Cadastrar usuário válido                            | P1         |
| TS008 | Usuários    | Cadastrar usuário com email duplicado               | P1         |
| TS009 | Usuários    | Cadastrar usuário sem nome                          | P1         |
| TS010 | Usuários    | Cadastrar usuário sem email                         | P1         |
| TS011 | Usuários    | Consultar usuário existente                         | P1         |
| TS012 | Usuários    | Consultar usuário inexistente                       | P2         |
| TS013 | Usuários    | Atualizar usuário existente                         | P2         |
| TS014 | Usuários    | Atualizar usuário inexistente                       | P2         |
| TS015 | Usuários    | Excluir usuário existente                           | P2         |
| TS016 | Usuários    | Excluir usuário inexistente                         | P2         |
| TS017 | Produtos    | Cadastrar produto válido                            | P1         |
| TS018 | Produtos    | Cadastrar produto sem nome                          | P1         |
| TS019 | Produtos    | Cadastrar produto sem preço                         | P1         |
| TS020 | Produtos    | Consultar produto existente                         | P2         |
| TS021 | Produtos    | Consultar produto inexistente                       | P2         |
| TS022 | Produtos    | Atualizar produto existente                         | P2         |
| TS023 | Produtos    | Excluir produto existente                           | P2         |
| TS024 | Carrinhos   | Criar carrinho com produto válido                   | P1         |
| TS025 | Carrinhos   | Criar carrinho com produto inexistente              | P1         |
| TS026 | Carrinhos   | Consultar carrinho existente                        | P2         |
| TS027 | Carrinhos   | Concluir compra com sucesso                         | P1         |
| TS028 | Segurança   | Acessar endpoint protegido sem token                | P1         |
| TS029 | Segurança   | Acessar endpoint protegido com token inválido       | P1         |
| TS030 | Segurança   | Validar permissões de usuário comum                 | P2         |
| TS031 | Performance | Validar tempo de resposta do login                  | P2         |
| TS032 | Performance | Executar teste de carga no endpoint de login        | P2         |
| TS033 | Performance | Executar teste de concorrência                      | P3         |
| TS034 | Contrato    | Validar estrutura JSON da resposta de login         | P2         |
| TS035 | Contrato    | Validar campos obrigatórios da resposta de usuários | P2         |

## Resumo

### Total de Cenários

* P1 (Alta): 17
* P2 (Média): 17
* P3 (Baixa): 1

### Cobertura

* Login
* Usuários
* Produtos
* Carrinhos
* Segurança
* Performance
* Contrato da API
