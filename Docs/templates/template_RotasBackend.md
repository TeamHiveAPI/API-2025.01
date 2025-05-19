# 📚 API - Documentação de Rotas (Template)

**Versão:** x.x.x  
**Última atualização:** DD/MM/YYYY

---

## 1️⃣ Visão Geral

Descreva aqui o propósito da API, principais recursos e contexto de uso.

---

## 2️⃣ Endpoints Principais

### 2.1 [Nome do Recurso]

- **[GET]** `/recurso/`  
  Descrição da listagem (**200**)

- **[POST]** `/recurso/`  
  Descrição da criação (**201**)  
  **Body:**
  ```json
  {
    "campo1": "tipo*",
    "campo2": "tipo"
    // ...
  }
  ```

- **[GET]** `/recurso/{id}`  
  Descrição do detalhe (**200/404**)

- **[PUT]** `/recurso/{id}`  
  Descrição da atualização (**200/404**)

- **[DELETE]** `/recurso/{id}`  
  Descrição da exclusão (**204/404**)

**Modelo Completo:**
```json
{
  "id": 0,
  "campo1": "valor",
  "campo2": "valor"
  // ...
}
```

---

### 2.2 [Outro Recurso]

- **[GET]** `/outro-recurso/`  
  Descrição (**200**)
- **[POST]** `/outro-recurso/`  
  Descrição (**201**)
- **[GET]** `/outro-recurso/{id}`  
  Descrição (**200/404**)

**Modelo Completo:**
```json
{
  "campoA": "tipo*",
  "campoB": "tipo"
  // ...
}
```

---

## 3️⃣ Segurança

- **Autenticação:** [Tipo de autenticação, ex: JWT Bearer Token]
- **Header obrigatório:**  
  `Authorization: Bearer <token>`
- **Níveis de acesso:**
  - Admin (CRUD completo)
  - Operador (Leitura/Escrita)
  - Leitura (Apenas consulta)

---

## 4️⃣ Códigos de Resposta

- **200** - OK (Sucesso)
- **201** - Created (Recurso criado)
- **204** - No Content (Exclusão)
- **400** - Bad Request (Dados inválidos)
- **401** - Unauthorized (Autenticação)
- **404** - Not Found (Recurso não existe)
- **422** - Unprocessable Entity (Validação)
- **500** - Server Error (Erro interno)

---

## 5️⃣ Exemplos Práticos

### 5.1 Exemplo de Requisição

**POST** `/recurso/`  
**Headers:** `{ "Authorization": "Bearer {token}" }`  
**Body:**
```json
{
  "campo1": "valor",
  "campo2": "valor"
}
```

---

## 6️⃣ Dashboard (Opcional)

- **[GET]** `/dashboard/algum-endpoint`  
  **Resposta:**
  ```json
  {
    "campoX": 0,
    "campoY": 0
  }
  ```

---

\* Campos obrigatórios
