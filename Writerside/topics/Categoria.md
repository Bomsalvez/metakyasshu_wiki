# Category

## 1. GET /categories

Retorna todas as categorias que o usuário tem acesso

### 1.1. Parâmetros

| Nome          | Tipo   | Descrição         | Requerido |
|---------------|--------|-------------------|-----------|
| category_name | string | Nome da categoria | false     |

## 2. POST /categories

Cria uma categoria.

### 2.1. Parâmetros

| Nome           | Tipo   | Descrição           | Requerido |
|----------------|--------|---------------------|-----------|
| category_name  | string | Nome da categoria   | true      |
| category_image | file   | Imagem da categoria | false     |
| category_type  | enum   | Tipo da categoria   | true      |

## 3. PUT /categories/:id

Atualiza uma categoria.

### 3.1. Parâmetros

| Nome           | Tipo   | Descrição           | Requerido |
|----------------|--------|---------------------|-----------|
| category_name  | string | Nome da categoria   | false     |
| category_image | file   | Imagem da categoria | false     |
| category_type  | enum   | Tipo da categoria   | false     |

## 4. PATCH /categories/:id

Atualiza a imagem de uma categoria.

### 4.1. Parâmetros

| Nome           | Tipo | Descrição           | Requerido |
|----------------|------|---------------------|-----------|
| category_image | file | Imagem da categoria | true      |
| id             | int  | ID da categoria     | true      |