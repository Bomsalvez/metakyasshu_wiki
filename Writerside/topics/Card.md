# Card

## 1. GET /cards

Retorna todos os cartões.

### 1.1. Parâmetros

| Nome      | Tipo   | Descrição      | Requerido |
|-----------|--------|----------------|-----------|
| card_name | string | Nome do cartão | false     |
| card_type | enum   | Tipo do cartão | false     |
| jtw       | string | ID do usuário  | true      |

## 2. GET /cards/:id

Retorna um cartão.

### 2.1. Parâmetros

| Nome | Tipo | Descrição    | Requerido |
|------|------|--------------|-----------|
| id   | int  | ID do cartão | true      |

## 3. POST /cards

Cria um cartão.

### 3.1. Parâmetros

| Nome          | Tipo   | Descrição                | Requerido |
|---------------|--------|--------------------------|-----------|
| card_name     | string | Nome do cartão           | false     |
| card_number   | string | Número do cartão         | true      |
| card_validate | date   | Data da fatura do cartão | false     |
| card_type     | enum   | Tipo do cartão           | true      |
| jtw           | string | ID do usuário            | true      |

## 4. PUT /cards/:id

Atualiza um cartão.

### 4.1. Parâmetros

| Nome          | Tipo   | Descrição                | Requerido |
|---------------|--------|--------------------------|-----------|
| card_name     | string | Nome do cartão           | false     |
| card_number   | string | Número do cartão         | false     |
| card_validate | date   | Data da fatura do cartão | false     |
| card_type     | enum   | Tipo do cartão           | false     |
| jtw           | string | ID do usuário            | true      |
| id            | int    | ID do cartão             | true      |

## 5. DELETE /cards/:id

Deleta um cartão.

### 5.1. Parâmetros

| Nome | Tipo | Descrição    | Requerido |
|------|------|--------------|-----------|
| id   | int  | ID do cartão | true      |

## 6. PATCH /cards/:id

Atualiza a funcionalidade de um cartão.

### 6.1. Parâmetros

| Nome      | Tipo   | Descrição      | Requerido |
|-----------|--------|----------------|-----------|
| card_type | enum   | Tipo do cartão | true      |
| jtw       | string | ID do usuário  | true      |
| id        | int    | ID do cartão   | true      |
