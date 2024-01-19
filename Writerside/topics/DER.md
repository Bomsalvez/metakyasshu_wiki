# Diagrama de Entidade-Relacionamento

## 1. Usuário

### 1.1. Descrição

O usuário é a entidade que representa o usuário do sistema. Ele sera o responsável por criar as despesas e metas, além
de convidar outros usuários para participar de suas metas.

### 1.2. Atributos

| Nome          | Tipo   | Descrição                      |
|---------------|--------|--------------------------------|
| user_id       | int    | Identificador único do usuário |
| user_name     | string | Nome do usuário                |
| user_email    | string | Email do usuário               |
| user_password | string | Senha do usuário               |
| user_cpf      | string | CPF do usuário                 |
| user_image    | file   | Imagem do usuário              |
| created_at    | date   | Data de criação do usuário     |

---

## 2. Categoria

### 2.1. Descrição

A categoria é a entidade que representa a categoria de despesa ou meta. Ela será utilizada para agrupar as despesas e
metas do usuário. Existe algumas categorias pré-definidas, mas o usuário pode criar novas categorias.

### 2.2. Atributos

| Nome           | Tipo   | Descrição                        |
|----------------|--------|----------------------------------|
| category_id    | int    | Identificador único da categoria |
| category_name  | string | Nome da categoria                |
| category_image | file   | Imagem da categoria              |
| category_type  | enum   | Tipo da categoria                |

### 2.3. Relacionamentos

| Nome     | Tipo      | Descrição             |
|----------|-----------|-----------------------|
| expenses | hasMany   | Despesas da categoria |
| goals    | hasMany   | Metas da categoria    |
| user     | belongsTo | Usuário da categoria  |

---

## 3. Despesa

### 3.1 Descrição

A despesa é a entidade que representa a despesa do usuário.

### 3.2. Atributos

| Nome           | Tipo   | Descrição                             |
|----------------|--------|---------------------------------------|
| expense_id     | int    | Identificador único da despesa        |
| expense_name   | string | Nome da despesa                       |
| expense_desc   | string | Descrição da despesa                  |
| expense_value  | float  | Valor da despesa                      |
| value_to_pay   | float  | Valor a pagar da despesa              |
| expenseDate    | date   | Data de criação da despesa            |
| date_to_pay    | date   | Data a pagar da despesa               |
| expense_type   | enum   | Tipo da despesa                       |
| expense_parcel | int    | Quantidade de parcelas                |
| access_level   | enum   | Nível de acesso da despesa            |
| category_id    | int    | Identificador da categoria da despesa |
| user_id        | int    | Identificador do usuário da despesa   |
| card_id        | int    | Identificador do cartão da despesa    |

### 3.3. Relacionamentos

| Nome     | Tipo      | Descrição            |
|----------|-----------|----------------------|
| category | belongsTo | Categoria da despesa |
| user     | belongsTo | Usuário da despesa   |
| card     | belongsTo | Cartão da despesa    |

---

## 4. Pagamento de Despesa

### 4.1. Descrição

O pagamento de despesa é a entidade que representa o pagamento de despesa do usuário.

### 4.2. Atributos

| Nome          | Tipo   | Descrição                            |
|---------------|--------|--------------------------------------|
| payment_id    | int    | Identificador único do pagamento     |
| expense_id    | int    | Identificador da despesa associada   |
| payment_value | float  | Valor do pagamento                   |
| paymentDate   | date   | Data do pagamento                    |
| card_id       | int    | Identificador do cartão de pagamento |
| code          | string | Código de barras do pagamento        |
| parcel        | int    | número da parcela do pagamento       |
| pix           | string | Chave pix do pagamento               |

### 4.3. Relacionamentos

| Nome    | Tipo      | Descrição            |
|---------|-----------|----------------------|
| expense | belongsTo | Despesa do pagamento |
| card    | belongsTo | Cartão do pagamento  |

---

## 5. Meta

### 5.1 Descrição

A meta é a entidade que representa a meta do usuário.

### 5.2. Atributos

| Nome              | Tipo   | Descrição                          |
|-------------------|--------|------------------------------------|
| goal_id           | int    | Identificador único da meta        |
| goal_name         | string | Nome da meta                       |
| goal_desc         | string | Descrição da meta                  |
| goal_value        | float  | Valor da meta                      |
| value_to_pay      | float  | Valor a pagar da meta              |
| goal_coin         | enum   | Moeda da meta                      |
| access_level      | enum   | Nível de acesso da meta            |
| goal_availability | enum   | Disponibilidade da meta            |
| goal_expiration   | date   | Data de expiração da meta          |
| goalDate          | date   | Data de criação da meta            |
| executionDate     | date   | Data de execução da meta           |
| category_id       | int    | Identificador da categoria da meta |
| user_id           | int    | Identificador do usuário da meta   |

### 5.3. Relacionamentos

| Nome     | Tipo      | Descrição         |
|----------|-----------|-------------------|
| category | belongsTo | Categoria da meta |
| user     | belongsTo | Usuário da meta   |

---

## 6. Cartão

### 6.1. Descrição

O cartão é a entidade que representa o cartão do usuário.

### 6.2. Atributos

| Nome          | Tipo   | Descrição                          |
|---------------|--------|------------------------------------|
| card_id       | int    | Identificador único do cartão      |
| card_name     | string | Nome do cartão                     |
| card_number   | string | Número do cartão                   |
| card_validate | date   | Data da fatura do cartão           |
| card_type     | enum   | Tipo do cartão                     |
| user_id       | int    | Identificador do usuário do cartão |

### 6.3. Relacionamentos

| Nome     | Tipo      | Descrição          |
|----------|-----------|--------------------|
| user     | belongsTo | Usuário do cartão  |
| expenses | hasMany   | Despesas do cartão |

---

## 7. Saldo

### 7.1. Descrição

O saldo é a entidade que representa o saldo do usuário.

### 7.2. Atributos

| Nome          | Tipo  | Descrição                         |
|---------------|-------|-----------------------------------|
| balance_id    | int   | Identificador único do saldo      |
| balance_value | float | Valor do saldo                    |
| balanceDate   | date  | Data do saldo                     |
| user_id       | int   | Identificador do usuário do saldo |

### 7.3. Relacionamentos

| Nome     | Tipo      | Descrição         |
|----------|-----------|-------------------|
| user     | belongsTo | Usuário do saldo  |
| expenses | hasMany   | Despesas do saldo |
| goals    | hasMany   | Metas do saldo    |

---

## 8. Convidado

### 8.1. Descrição

O convidado é a entidade que representa o convidado do usuário.

### 8.2. Atributos

| Nome          | Tipo   | Descrição                                 |
|---------------|--------|-------------------------------------------|
| guest_id      | int    | Identificador único do convidado          |
| guest_access  | enum   | Acesso do convidado                       |
| guest_code    | string | Código do convite do convidado            |
| inviteDate    | date   | Data do convite do convidado              |
| acceptDate    | date   | Data da aceitação do convite do convidado |
| guest_user_id | int    | Identificador do usuário do convidado     |
| host_user_id  | int    | Identificador do usuário do anfitrião     |

### 8.3. Relacionamentos

| Nome | Tipo      | Descrição            |
|------|-----------|----------------------|
| user | belongsTo | Usuário do convidado |
| host | belongsTo | Usuário do anfitrião |

---

## 9. Participante

### 9.1. Descrição

O participante é a entidade que representa o participante da meta.

### 9.2. Atributos

| Nome                | Tipo    | Descrição                                |
|---------------------|---------|------------------------------------------|
| participant_id      | int     | Identificador único do participante      |
| participant_active  | boolean | Ativo do participante                    |
| participant_value   | float   | Valor do participante                    |
| participant_percent | float   | Porcentagem do participante              |
| paid_participant    | boolean | Pago do participante                     |
| expense_id          | int     | Identificador da despesa do participante |
| goal_id             | int     | Identificador da meta do participante    |
| user_id             | int     | Identificador do usuário do participante |

### 9.3. Relacionamentos

| Nome    | Tipo      | Descrição               |
|---------|-----------|-------------------------|
| expense | belongsTo | Despesa do participante |
| goal    | belongsTo | Meta do participante    |
| user    | belongsTo | Usuário do participante |