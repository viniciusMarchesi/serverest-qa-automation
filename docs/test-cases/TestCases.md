# Test Cases - ServeRest API

## TC001 - Login com Credenciais Válidas

**Cenário Relacionado:** TS001

### Prioridade

Alta

### Pré-condição

Usuário previamente cadastrado na aplicação.

### Dados de Teste

| Campo | Valor                               |
| ----- | ----------------------------------- |
| Email | [qa@teste.com](mailto:qa@teste.com) |
| Senha | 123456                              |

### Passos

1. Enviar requisição POST para /login.
2. Informar email válido.
3. Informar senha válida.
4. Executar requisição.

### Resultado Esperado

* Status Code 200.
* Token retornado na resposta.
* Mensagem de sucesso.

---

## TC002 - Login com Senha Inválida

**Cenário Relacionado:** TS002

### Prioridade

Alta

### Pré-condição

Usuário previamente cadastrado.

### Dados de Teste

| Campo | Valor                               |
| ----- | ----------------------------------- |
| Email | [qa@teste.com](mailto:qa@teste.com) |
| Senha | senha_incorreta                     |

### Passos

1. Enviar requisição POST para /login.
2. Informar email válido.
3. Informar senha inválida.

### Resultado Esperado

* Status Code 401.
* Mensagem informando credenciais inválidas.

---

## TC003 - Cadastro de Usuário Válido

**Cenário Relacionado:** TS007

### Prioridade

Alta

### Pré-condição

Nenhuma.

### Dados de Teste

| Campo | Valor                                         |
| ----- | --------------------------------------------- |
| Nome  | Usuário Teste                                 |
| Email | [usuario@teste.com](mailto:usuario@teste.com) |
| Senha | 123456                                        |

### Passos

1. Enviar requisição POST para /usuarios.
2. Informar dados válidos.
3. Executar requisição.

### Resultado Esperado

* Status Code 201.
* Cadastro realizado com sucesso.
* ID do usuário retornado.

---

## TC004 - Cadastro de Usuário com Email Duplicado

**Cenário Relacionado:** TS008

### Prioridade

Alta

### Pré-condição

Email já cadastrado.

### Passos

1. Enviar requisição POST para /usuarios.
2. Informar email já existente.
3. Executar requisição.

### Resultado Esperado

* Status Code 400.
* Mensagem informando email já utilizado.

---

## TC005 - Consulta de Usuário Existente

**Cenário Relacionado:** TS011

### Prioridade

Alta

### Pré-condição

Usuário cadastrado.

### Passos

1. Executar GET /usuarios/{id}.

### Resultado Esperado

* Status Code 200.
* Dados do usuário retornados corretamente.

---

## TC006 - Cadastro de Produto Válido

**Cenário Relacionado:** TS017

### Prioridade

Alta

### Pré-condição

Usuário autenticado.

### Passos

1. Executar POST /produtos.
2. Informar dados válidos.

### Resultado Esperado

* Status Code 201.
* Produto cadastrado com sucesso.

---

## TC007 - Cadastro de Produto sem Nome

**Cenário Relacionado:** TS018

### Prioridade

Alta

### Passos

1. Executar POST /produtos.
2. Omitir campo nome.

### Resultado Esperado

* Status Code 400.
* Mensagem de validação.

---

## TC008 - Criação de Carrinho

**Cenário Relacionado:** TS024

### Prioridade

Alta

### Pré-condição

Produto cadastrado.

### Passos

1. Executar POST /carrinhos.
2. Informar produto válido.

### Resultado Esperado

* Status Code 201.
* Carrinho criado com sucesso.

---

## TC009 - Acesso sem Token

**Cenário Relacionado:** TS028

### Prioridade

Alta

### Passos

1. Executar endpoint protegido sem token.

### Resultado Esperado

* Status Code 401.
* Mensagem de acesso negado.

---

## TC010 - Validação de Tempo de Resposta

**Cenário Relacionado:** TS031

### Prioridade

Média

### Passos

1. Executar login.
2. Medir tempo de resposta.

### Resultado Esperado

* Tempo inferior a 2000 ms.
* Status Code 200.
