# Bug Reports – API

Este documento contém os bugs identificados durante os testes manuais da API JSONPlaceholder.

---

## BUG-01 – API retorna status incorreto ao enviar payload inválido

**ID:** BUG-01  
**Título:** API retorna status 201 ao enviar payload inválido  
**Endpoint:** POST /posts  
**Método:** POST  
**Ambiente:** Produção (API pública)  

### Descrição
Ao enviar uma requisição POST com payload inválido (campos obrigatórios ausentes), a API retorna status de sucesso (201), quando o esperado seria um erro de validação.

### Passos para reprodução
1. Enviar uma requisição POST para o endpoint `/posts`
2. Enviar o body sem o campo `title`

### Resultado esperado
- Status HTTP 400 (Bad Request)
- Mensagem informando erro de validação

### Resultado atual
- Status HTTP 201 (Created)
- Recurso criado mesmo com dados inválidos

### Severidade
Média

### Status
Aberto

### Evidência
A requisição POST foi executada via Postman com payload inválido.
Mesmo sem o campo obrigatório `title`, a API retornou status 201 (Created)
e gerou um ID para o recurso.
### Evidência
![Bug-01 Evidence](evidences/bug-01-postman-evidence.png)
