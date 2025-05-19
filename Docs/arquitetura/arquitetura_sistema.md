# 🏗️ Arquitetura do Sistema - Estação Meteorológica

Este documento descreve a arquitetura do sistema, detalhando os principais componentes, fluxos de dados e integrações.

---

## 📊 Visão Geral

O sistema é composto por quatro grandes blocos:

1. **Estação Meteorológica (Dispositivo Físico/ESP32)**
2. **Broker MQTT (Mosquitto)**
3. **Banco de Dados Temporário (MongoDB)**
4. **Banco de Dados Principal (PostgreSQL)**
5. **Backend (API FastAPI)**
6. **Frontend (Vite + Chart.js)**

---

## 🔄 Fluxo de Dados

1. **Coleta de Dados:**
   A estação meteorológica (ESP32) coleta dados dos sensores (temperatura, umidade, etc).

2. **Envio via MQTT:**
   O ESP32 publica os dados coletados em tópicos MQTT para o broker.

3. **Armazenamento Temporário (MongoDB):**
   Um serviço/worker consome os dados do broker MQTT e armazena temporariamente no MongoDB.

4. **Migração para PostgreSQL:**
   Outro serviço/worker consome os dados do MongoDB (também via MQTT) e os insere no banco de dados relacional PostgreSQL, que é o banco principal do sistema.

5. **Disponibilização via API:**
   O backend (FastAPI) expõe endpoints HTTP para consulta, cadastro e gerenciamento dos dados armazenados no PostgreSQL.

6. **Consumo pelo Frontend:**
   O frontend (Vite + Chart.js) consome a API via HTTP para exibir dashboards, gráficos e informações ao usuário.

---

## 📐 Diagrama de Arquitetura (ASCII)

```plaintext
+-------------------+      MQTT      +-------------+      |      +-----------------+
| Estação FÍSICA    |  ----------->  |  Broker     |      |      |   Frontend      |
| (ESP32 + sensores)|                |   MQTT      |      |      | (Vite + Chart.js)|
+-------------------+                +-------------+      |      +-----------------+
         |                                   |           |              ^
         |                                   v           |              |
         |                             +-----------+      |              |
         |                             |  MongoDB   |      |              |
         |                             +-----------+      |              |
         |                                   |           |              |
         |                                   v           |              |
         |                             +-----------+      |              |
         |                             |  Worker    |      |              |
         |                             | (MQTT->PG) |      |              |
         |                             +-----------+      |              |
         |                                   |           |              |
         |                                   v           |              |
         |                             +-----------+      |              |
         |                             | PostgreSQL |<-----+--------------+
         |                             +-----------+      |
         |                                   ^
         |                                   |
         |                             +-----------+
         |                             |  Backend  |
         +---------------------------->| (FastAPI) |
                                       +-----------+
```

---

## 📝 Descrição dos Componentes

- **Estação Meteorológica (ESP32):**
  - Coleta dados dos sensores físicos.
  - Envia os dados via protocolo MQTT para o broker.

- **Broker MQTT (Mosquitto):**
  - Responsável por receber e distribuir mensagens entre dispositivos e serviços.
  - Atua como intermediário entre a estação e os serviços de backend.
  - Utiliza o software Mosquitto como broker MQTT.

- **MongoDB:**
  - Armazena temporariamente os dados recebidos via MQTT.
  - Facilita o desacoplamento e a persistência inicial dos dados.

- **Worker (MQTT → PostgreSQL):**
  - Serviço responsável por consumir dados do MongoDB (via MQTT ou polling).
  - Realiza transformações/validações e insere os dados no PostgreSQL.

- **PostgreSQL:**
  - Banco de dados relacional principal do sistema.
  - Armazena dados normalizados e prontos para consulta via API.

- **Backend (FastAPI):**
  - Expõe endpoints HTTP RESTful para CRUD de estações, sensores, medições, alertas e usuários.
  - Realiza autenticação, autorização e regras de negócio.

- **Frontend (Vite + Chart.js):**
  - Interface web para visualização dos dados meteorológicos.
  - Consome a API do backend para exibir dashboards, gráficos e relatórios.

---

## 🔒 Segurança

- **Comunicação entre frontend e backend:** via HTTPS (recomendado).
- **Autenticação:** JWT nos endpoints protegidos da API.
- **Controle de acesso:** Níveis de usuário (admin, operador, leitura).

---


## 🗂️ Resumo Visual Simplificado

```plaintext
[ESP32] --MQTT--> [Broker MQTT] --(persistência)--> [MongoDB] --(worker)--> [PostgreSQL] <--HTTP--> [Backend FastAPI] <--HTTP--> [Frontend]
```

