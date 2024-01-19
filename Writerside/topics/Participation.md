# Participação

## 1. PUT /participation/:id

Edita uma participação.

### 1.1. Parâmetros

| Nome                 | Tipo    | Descrição                                     | Requerido |
|----------------------|---------|-----------------------------------------------|-----------|
| activeParticipation  | boolean | Se o convidado participara da meta ou despesa | true      |
| sliceValue           | float   | Fatia do valor a ser pago pelo participante   | false     |
| percentParticipation | float   | Porcentagem do participante                   | false     |
| expense              | int     | Identificador da despesa do participante      | false     |
| goal                 | int     | Identificador da meta do participante         | false     |
| jwtToken             | string  | Token de autenticação                         | true      |

## 2. PATCH /participation/:id

Atualiza se o participante pagou ou não a parte dele.