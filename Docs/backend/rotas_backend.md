# 🌦️ API Estação Meteorológica

**Versão:** 1.0.0
**Última atualização:** 19/05/2025

---

## 1️⃣ Visão Geral

API RESTful para gerenciamento de estações meteorológicas com:

- Cadastro de estações e sensores
- Armazenamento de medidas meteorológicas
- Sistema de alertas configuráveis
- Gerenciamento de usuários com autenticação JWT

---

## 2️⃣ Endpoints Principais

### 2.1 Estaçōes Meteorológicas

- **[GET]** `/estacoes/`  
  Lista todas as estações (**200**)

- **[POST]** `/estacoes/`  
  Cria nova estação (**201**)  
  **Body:**
  ```json
  {
    "nome": "string*",
    "latitude": "number*",
    "longitude": "number*"
    // ...
  }
  ```

- **[GET]** `/estacoes/{id}`  
  Detalhes da estação (**200/404**)

- **[PUT]** `/estacoes/{id}`  
  Atualiza estação (**200/404**)

- **[DELETE]** `/estacoes/{id}`  
  Remove estação (**204/404**)

**Modelo Completo:**
```json
{
  "id": 0,
  "uid": "string",
  "nome": "string",
  "cep": "string",
  "coordenadas": {
    "latitude": 0.0,
    "longitude": 0.0
  },
  "status": "ativa|inativa",
  "sensores": [
    {
      "id": 0,
      "nome": "string",
      "tipo": "string"
    }
  ]
}
```

---

### 2.2 Parâmetros/Sensores

- **[GET]** `/parametros/`  
  Lista parâmetros (**200**)

- **[POST]** `/parametros/`  
  Cria parâmetro (**201**)

- **[GET]** `/parametros/{id}`  
  Detalhes do parâmetro (**200/404**)

**Modelo Completo:**
```json
{
  "nome": "string*",
  "unidade": "string*",
  "escala": {
    "min": 0.0,
    "max": 100.0
  },
  "tipo_parametro_id": 0
}
```

---

### 2.3 Medições

- **[GET]** `/medidas/`  
  Lista medições (**200**)

- **[POST]** `/medidas/`  
  Registra medição (**201**)

- **[POST]** `/medidas/lote`  
  Registro em lote (**201**)

**Modelo Completo:**
```json
{
  "estacao_id": 0,
  "parametro_id": 0,
  "valor": 0.0,
  "data_hora": "datetime"
}
```

---

### 2.4 Sistema de Alertas

- **[GET]** `/alertas/`  
  Alertas ativos (**200**)

- **[GET]** `/alertas/passados`  
  Histórico (**200**)

- **[POST]** `/alertas-definidos/`  
  Configura alerta (**201**)

**Modelo de Alerta Definido:**
```json
{
  "parametro_id": 0,
  "condicao": "string",
  "valor_referencia": 0.0,
  "mensagem": "string"
}
```

---

### 2.5 Autenticação

- **[POST]** `/auth/login`  
  Autenticação (**200/401**)  
  **Body:**
  ```json
  {
    "username": "string*",
    "password": "string*"
  }
  ```
  **Resposta:**
  ```json
  {
    "access_token": "jwt_token",
    "user": {
      "id": 0,
      "nome": "string",
      "nivel_acesso": "string"
    }
  }
  ```

---

## 3️⃣ Segurança

- **Autenticação:** JWT Bearer Token
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

### 5.1 Registrar Medição

**POST** `/medidas/`  
**Headers:** `{ "Authorization": "Bearer {token}" }`  
**Body:**
```json
{
  "estacao_id": 1,
  "parametro_id": 3,
  "valor": 25.4,
  "data_hora": "2023-05-14T14:30:00Z"
}
```

### 5.2 Configurar Alerta

**POST** `/alertas-definidos/`  
**Body:**
```json
{
  "parametro_id": 3,
  "condicao": ">",
  "valor_referencia": 30.0,
  "mensagem": "Temperatura acima do limite"
}
```

---

## 6️⃣ Dashboard

- **[GET]** `/dashboard/contagem-entidades`  
  **Resposta:**
  ```json
  {
    "estacoes_ativas": 0,
    "alertas_ativos": 0,
    "medidas_hoje": 0
  }
  ```

---

\* Campos obrigatórios
