# Casos de Teste – API

Este documento descreve os casos de teste manuais executados para validação da API.

---
## CT-01 - Validar GET /posts

**Objetivo:** Verificar se a API retorna a lista de posts corretamente. 

**Endpoint:** GET /posts

**Pré-condição:** API disponível. 

**Passos:** 
1. Enviar requisição GET para /posts

**Resultado esperado:**
- Status HTTP 200
- Retorno de uma lista de posts
- Cada post contém os campos: userID, id, title, body

---

## CT-02 - Validar GET /posts/{id}

**Objetivo:** Validar retorno de post específico por ID válido. 

**Endpoint:** GET /posts/1

**Pré-condição:** API disponível. 

**Passos:** 
1. Enviar requisição GET para /posts/1

**Resultado esperado:** 
- Status HTTP 200
- Retorno de um post
- ID retornado igual ao ID solicitado

---

## CT-03 - Validar GET /posts/{id} inválido 

**Objetivo:** Validar comportamento da API ao consultar um ID inexistente. 

**Endpoint:** GET /posts/9999

**Pré-condição:** API disponível. 

**Passos:** 
1. Enviar requisição GET para /posts/9999

**Resultado esperado:**
- Status HTTP 404 ou resposta vazia
