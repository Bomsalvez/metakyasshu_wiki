# Saldo

## 1. GET /balance

Retorna os saldos de um usuário.

### 1.1. Parâmetros

| Nome               | Tipo   | Descrição             | Requerido |
|--------------------|--------|-----------------------|-----------|
| jwt                | string | Token de autenticação | true      |
| balanceDateInicial | date   | Data do saldo         | false     |
| balanceDateFinal   | date   | Data do saldo         | false     |

## 2. GET /balance/:id

Retorna um saldo.

### 2.1. Parâmetros

| Nome | Tipo | Descrição     | Requerido |
|------|------|---------------|-----------|
| id   | int  | ID do usuário | true      |

## 3. POST /balance

Adiciona um novo saldo.

### 3.1. Parâmetros

| Nome         | Tipo   | Descrição             | Requerido |
|--------------|--------|-----------------------|-----------|
| balanceValue | float  | Valor do saldo        | true      |
| jwt          | string | Token de autenticação | true      |

## 4. GET /balance/expense

Retorna o saldo, assim como o saldo faltante ou restante dos pagamentos das despesas, além do valor das despesas não
pagas.

### 4.1. Parâmetros

| Nome               | Tipo   | Descrição             | Requerido |
|--------------------|--------|-----------------------|-----------|
| jwt                | string | Token de autenticação | true      |
| balanceDateInicial | date   | Data do saldo         | false     |
| balanceDateFinal   | date   | Data do saldo         | false     |

## 5. GET /balance/goal

Retorna o saldo, assim como o saldo faltante ou restante dos pagamentos das metas, além do valor das metas não pagas.

### 5.1. Parâmetros

| Nome               | Tipo   | Descrição             | Requerido |
|--------------------|--------|-----------------------|-----------|
| jwt                | string | Token de autenticação | true      |
| balanceDateInicial | date   | Data do saldo         | false     |
| balanceDateFinal   | date   | Data do saldo         | false     |