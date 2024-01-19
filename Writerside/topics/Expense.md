# Expense

## 1. GET /expenses

Retorna todas as despesas de um usuário. Retorna todas as despesas a qual o usuário tem acesso.

### 1.1. Parâmetros

| Nome                 | Tipo   | Descrição                  | Requerido |
|----------------------|--------|----------------------------|-----------|
| expense_name         | string | Nome da despesa            | false     |
| expenseDateInicial | date   | Data da despesa            | false     |
| expenseDateFinal  | date   | Data da despesa            | false     |
| expense_type         | enum   | Tipo da despesa            | false     |
| expense_cat          | int    | ID da categoria da despesa | false     |
| jwt                  | string | Token de autenticação      | true      |

## 2. GET /expenses/:id

Retorna uma despesa.

### 2.1. Parâmetros

| Nome | Tipo | Descrição     | Requerido |
|------|------|---------------|-----------|
| id   | int  | ID da despesa | true      |

## 3. POST /expenses

Cria uma despesa onde e calculado o valor da parcela. O valor que sera dividido entre os participantes e o valor da
parcela.

### 3.1. Parâmetros

| Nome           | Tipo   | Descrição                             | Requerido |
|----------------|--------|---------------------------------------|-----------|
| expense_name   | string | Nome da despesa                       | true      |
| expense_desc   | string | Descrição da despesa                  | false     |
| expense_value  | float  | Valor da despesa                      | true      |
| date_to_pay    | date   | Data a pagar da despesa               | true      |
| expense_type   | enum   | Tipo da despesa                       | true      |
| expense_parcel | int    | Quantidade de parcelas                | false     |
| access_level   | enum   | Nível de acesso da despesa            | false     |
| category_id    | int    | Identificador da categoria da despesa | true      |
| card_id        | int    | Identificador do cartão da despesa    | false     |
| jwt            | string | Token de autenticação                 | true      |

## 4. PUT /expenses/:id

Atualiza uma despesa.

### 4.1. Parâmetros

| Nome           | Tipo   | Descrição                             | Requerido |
|----------------|--------|---------------------------------------|-----------|
| expense_name   | string | Nome da despesa                       | false     |
| expense_desc   | string | Descrição da despesa                  | false     |
| expense_value  | float  | Valor da despesa                      | false     |
| date_to_pay    | date   | Data a pagar da despesa               | false     |
| expense_type   | enum   | Tipo da despesa                       | false     |
| expense_parcel | int    | Quantidade de parcelas                | false     |
| access_level   | enum   | Nível de acesso da despesa            | false     |
| category_id    | int    | Identificador da categoria da despesa | false     |
| card_id        | int    | Identificador do cartão da despesa    | false     |
| jwt            | string | Token de autenticação                 | true      |

