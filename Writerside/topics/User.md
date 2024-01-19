# User

## 1. GET /user

Retorna um usuário.

### 1.1. Parâmetros

| Nome | Tipo   | Descrição     | Requerido |
|------|--------|---------------|-----------|
| jtw  | string | ID do usuário | true      |

## 2. POST /user

Cria um usuário.

### 2.1. Parâmetros

| Nome          | Tipo   | Descrição         | Requerido |
|---------------|--------|-------------------|-----------|
| user_name     | string | Nome do usuário   | true      |
| user_email    | string | Email do usuário  | true      |
| user_password | string | Senha do usuário  | true      |
| user_cpf      | string | CPF do usuário    | true      |
| user_image    | file   | Imagem do usuário | false     |

## 3. PUT /user

Atualiza um usuário.

### 3.1. Parâmetros

| Nome          | Tipo   | Descrição         | Requerido |
|---------------|--------|-------------------|-----------|
| user_name     | string | Nome do usuário   | false     |
| user_email    | string | Email do usuário  | false     |
| user_password | string | Senha do usuário  | false     |
| user_cpf      | string | CPF do usuário    | false     |
| user_image    | file   | Imagem do usuário | false     |
| jtw           | string | ID do usuário     | true      |

## 4. DELETE /user

Desativa um usuário.

### 4.1. Parâmetros

| Nome | Tipo   | Descrição     | Requerido |
|------|--------|---------------|-----------|
| jtw  | string | ID do usuário | true      |

## 5. PATCH /user

Atualiza a imagem de perfil do usuário.

### 5.1. Parâmetros

| Nome       | Tipo   | Descrição         | Requerido |
|------------|--------|-------------------|-----------|
| user_image | file   | Imagem do usuário | true      |
| jtw        | string | ID do usuário     | true      |
