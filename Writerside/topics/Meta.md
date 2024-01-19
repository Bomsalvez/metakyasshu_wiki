# Meta

## 1. GET /goal

Retorna todas as metas de um usuário. Retorna todas as metas a qual o usuário tem acesso.

### 1.1. Parâmetros

| Nome             | Tipo    | Descrição               | Requerido |
|------------------|---------|-------------------------|-----------|
| goalName         | string  | Nome da meta            | false     |
| goalDateInicial  | date    | Data da meta            | false     |
| goalDateFinal    | date    | Data da meta            | false     |
| goalType         | enum    | Tipo da meta            | false     |
| category         | int     | ID da categoria da meta | false     |
| goalAvailability | enum    | Disponibilidade da meta | false     |
| jwtToken         | string  | Token de autenticação   | true      |
| goalExecution    | boolean | Meta foi executada      | false     |

## 2. GET /goal/:id

Retorna uma meta.

### 2.1. Parâmetros

| Nome | Tipo | Descrição  | Requerido |
|------|------|------------|-----------|
| id   | int  | ID da meta | true      |

## 3. POST /goal

Cria uma meta.

### 3.1. Parâmetros

| Nome            | Tipo   | Descrição                          | Requerido |
|-----------------|--------|------------------------------------|-----------|
| goal_name       | string | Nome da meta                       | true      |
| goal_desc       | string | Descrição da meta                  | false     |
| goal_value      | float  | Valor da meta                      | true      |
| goal_coin       | enum   | Moeda da meta                      | false     |
| access_level    | enum   | Nível de acesso da meta            | false     |
| goal_expiration | date   | Data de expiração da meta          | false     |
| executionDate   | date   | Data de execução da meta           | false     |
| category_id     | int    | Identificador da categoria da meta | true      |
| jwt             | string | Token de autenticação              | true      |

## 4. PUT /goal/:id

Atualiza uma meta.

### 4.1. Parâmetros

| Nome            | Tipo   | Descrição                          | Requerido |
|-----------------|--------|------------------------------------|-----------|
| goal_name       | string | Nome da meta                       | false     |
| goal_desc       | string | Descrição da meta                  | false     |
| goal_value      | float  | Valor da meta                      | false     |
| goal_coin       | enum   | Moeda da meta                      | false     |
| access_level    | enum   | Nível de acesso da meta            | false     |
| goal_expiration | date   | Data de expiração da meta          | false     |
| executionDate   | date   | Data de execução da meta           | false     |
| category_id     | int    | Identificador da categoria da meta | false     |

