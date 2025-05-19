# 🌦️ Guia de Instalação Geral - API Estação Meteorológica

Este guia reúne os passos para instalar e rodar **tanto o backend quanto o frontend** do projeto Estação Meteorológica da equipe **TeamHiveAPI**.

---

## 📋 Sobre o Projeto

O projeto é composto por dois módulos principais:

- **Backend:** API RESTful desenvolvida em Python (FastAPI) para gerenciar dados meteorológicos, usuários, alertas e integrações.
- **Frontend:** Interface web desenvolvida em JavaScript (Vite + Chart.js) para visualização dos dados meteorológicos.

---

## ✅ Pré-requisitos

Antes de começar, instale:

- [Git](https://git-scm.com/downloads)
- [Node.js 18+](https://nodejs.org/) (para o frontend)
- [Python 3.8+](https://www.python.org/downloads/) (para o backend)
- [PostgreSQL 15+](https://www.postgresql.org/download/) (para o backend)
- [DBeaver](https://dbeaver.io/download/) ou [pgAdmin](https://www.pgadmin.org/download/) (opcional, para gerenciar o banco)
- [VS Code](https://code.visualstudio.com/) (opcional)

---

## 🚀 Instalação do Backend

### 1. Clonar o Repositório Backend

```bash
cd Desktop
git clone https://github.com/TeamHiveAPI/API-2025.01-BACK.git
cd API-2025.01-BACK
```

### 2. Configurar Ambiente Virtual

```bash
python -m venv venv
# Ative o ambiente virtual:
# No Windows:
venv\Scripts\activate
# No Linux/Mac:
source venv/bin/activate
```

### 3. Instalar Dependências

```bash
pip install -r requirements.txt
# Se não houver requirements.txt:
pip install fastapi uvicorn sqlalchemy psycopg2-binary
```

### 4. Configurar o Banco de Dados

- Crie um banco chamado `api` no PostgreSQL.
- Atualize a string de conexão no arquivo `database.py`:
  ```python
  DATABASE_URL = "postgresql://postgres:1234@localhost:5432/api"
  ```
  *(Ajuste usuário, senha, host e porta conforme sua configuração.)*

### 5. Variáveis de Ambiente

```bash
cp .env.sample .env
# Edite o arquivo .env conforme necessário.
```

### 6. Rodar o Backend

```bash
uvicorn main:app --reload
# Acesse: http://127.0.0.1:8000
```

---

## 🚀 Instalação do Frontend

### 1. Clonar o Repositório Frontend

```bash
cd Desktop
git clone https://github.com/TeamHiveAPI/API-2025.01-FRONT.git
cd API-2025.01-FRONT
```

### 2. Instalar Dependências

```bash
npm install
```

### 3. Rodar o Frontend

```bash
npm run dev
# Acesse: http://localhost:5173
```

---

## 🛠️ Observações

- Certifique-se de que o backend esteja rodando antes de acessar o frontend.
- Ajuste URLs de API no frontend se necessário.
- Consulte os guias específicos de backend e frontend para detalhes avançados.

---
