# Paiment

## 1. GET /paiments

Retorna todos os pagamentos.

### 1.1. Parâmetros

| Nome                 | Tipo    | Descrição                     | Requerido |
|----------------------|---------|-------------------------------|-----------|
| expense_name         | string  | nome do credor                | false     |
| payment_value        | float   | Valor do pagamento            | false     |
| paymentDateInicial | date    | Data do pagamento             | false     |
| paymentDateFinal  | date    | Data do pagamento             | false     |
| paid_full            | boolean | todas as parcelas foram pagas | false     |
| card                 | boolean | se foi pago com cartão        | false     |
| code                 | boolean | se foi pago com boleto        | false     |
| pix                  | boolean | se foi pago com pix           | false     |

## 2. GET /paiments/:id

Retorna um pagamento.

### 2.1. Parâmetros

| Nome | Tipo | Descrição     | Requerido |
|------|------|---------------|-----------|
| id   | int  | ID do usuário | true      |

## 3. POST /paiments

Efetua o pagamento de uma despesa. Em caso de despesa compartilhada, o dono da despesa pode efetuar o pagamento somente após os outros participantes terem efetuado o pagamento. 

### 3.1. Parâmetros

| Nome          | Tipo   | Descrição                            | Requerido |
|---------------|--------|--------------------------------------|-----------|
| payment_id    | int    | Identificador único do pagamento     | true      |
| expense_id    | int    | Identificador da despesa associada   | true      |
| payment_value | float  | Valor do pagamento                   | true      |
| card_id       | int    | Identificador do cartão de pagamento | false     |
| code          | string | Código de barras do pagamento        | false     |
| parcel        | int    | número da parcela do pagamento       | false     |
| pix           | string | Chave pix do pagamento               | false     |


