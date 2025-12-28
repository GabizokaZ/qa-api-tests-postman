# API Documentation – JSONPlaceholder

Esta documentação descreve os endpoints utilizados nos testes manuais da API JSONPlaceholder.

---

## Base URL

https://jsonplaceholder.typicode.com/

---

## Endpoints

### GET /posts
Retorna a lista de posts.

**Método:** GET  
**Endpoint:** /posts  

**Resposta de Sucesso:**
- **200 OK**

**Exemplo de Resposta:**
```json
[
  {
    "userId": 1,
    "id": 1,
    "title": "Post title",
    "body": "Post content"
  }
]

-----------------------------------------------------------------------------

GET /posts/{id}

Retorna um post específico pelo ID.

Método: GET
Endpoint: /posts/{id}

Parâmetros de URL:

id (integer) — ID do post

Resposta de Sucesso:

200 OK

Resposta de Erro:

404 Not Found (quando ID não existe)
----------------------------------------------------------------------------
**POST /posts**

Cria um novo post.

Método: POST
Endpoint: /posts

Body (JSON):
{
  "title": "Post title",
  "body": "Post content",
  "userId": 1
}

Resposta de Sucesso:

201 Created

Observação:
A API aceita payloads inválidos sem validação de campos obrigatórios.
---------------------------------------------------------------------
PUT /posts/{id}

Atualiza um post existente.

Método: PUT
Endpoint: /posts/{id}

Body (JSON):

{
  "id": 1,
  "title": "Updated title",
  "body": "Updated content",
  "userId": 1
}

Resposta de Sucesso:

200 OK
---------------------------------------------------------------------------

DELETE /posts/{id}

Remove um post.

Método: DELETE
Endpoint: /posts/{id}

Resposta de Sucesso:

200 OK
