# Convidado

## 1. GET /guest

Retorna todos os convidados de um usuário que estão ativos.

### 1.1. Parâmetros

| Nome        | Tipo   | Descrição                    | Requerido |
|-------------|--------|------------------------------|-----------|
| nameGuest   | string | Nome do convidado            | false     |
| accessLevel | enum   | Nível de acesso do convidado | false     |
| jwt         | string | Token de autenticação        | true      |

## 2. GET /guest/:id

Retorna um convidado e todas as participações de meta e despesas.

### 2.1. Parâmetros

| Nome | Tipo | Descrição     | Requerido |
|------|------|---------------|-----------|
| id   | int  | ID do usuário | true      |

## 3. POST /guest

Cria um convidado.

### 3.1. Parâmetros

| Nome        | Tipo   | Descrição                             | Requerido |
|-------------|--------|---------------------------------------|-----------|
| accessLevel | enum   | Nível de acesso do convidado          | true      |
| user        | int    | Identificador do usuário do convidado | true      |
| jwt         | string | Token de autenticação                 | true      |

## 4. DELETE /guest/:id

Deleta um convidado.

### 4.1. Parâmetros

| Nome | Tipo | Descrição     | Requerido |
|------|------|---------------|-----------|
| id   | int  | ID do usuário | true      |
