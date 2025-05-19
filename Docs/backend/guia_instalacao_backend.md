# 🌦️ API-2025.01-BACK - Weather Station API

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![FastAPI](https://img.shields.io/badge/FastAPI-0.68%2B-green) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-blue) ![GitHub](https://img.shields.io/badge/GitHub-Repository-lightgrey)

Bem-vindo ao backend da **Weather Station API**! Este projeto foi desenvolvido pela equipe **TeamHiveAPI** para gerenciar dados de estações meteorológicas, incluindo informações de estações, parâmetros, medidas, alertas e usuários. Utilizamos o framework **FastAPI** para criar uma API RESTful eficiente e o **PostgreSQL** como banco de dados relacional.

---

## 📋 Sobre o Projeto

Este é o backend da API para o projeto de estações meteorológicas do curso **2025.01**. Ele foi projetado para:

- Armazenar e gerenciar dados de estações meteorológicas.
- Monitorar parâmetros como temperatura, umidade, etc.
- Gerenciar alertas baseados em condições definidas.
- Oferecer autenticação e gerenciamento de usuários.

### **Funcionalidades**
- **Estações Meteorológicas**: Cadastro e gerenciamento de estações com informações como localização, status e data de instalação.
- **Parâmetros**: Registro de parâmetros de medição com unidades e fatores de conversão.
- **Medidas**: Armazenamento de medições realizadas pelas estações.
- **Alertas**: Definição e monitoramento de alertas com base em condições específicas.
- **Usuários**: Gerenciamento de usuários com níveis de acesso.

---

## 🚀 Como Começar

Siga os passos abaixo para clonar, configurar e rodar o projeto na sua máquina.

### **Pré-requisitos**
Antes de começar, você precisará instalar as seguintes ferramentas:

- [Git](https://git-scm.com/downloads) (para clonar o repositório)
- [Python 3.8+](https://www.python.org/downloads/) (para executar o backend)
- [PostgreSQL 15+](https://www.postgresql.org/download/) (para o banco de dados)
- [DBeaver](https://dbeaver.io/download/) ou [pgAdmin](https://www.pgadmin.org/download/) (opcional, para gerenciar o banco)
- [VS Code](https://code.visualstudio.com/) (opcional, para editar o código)

---

### **Passo 1: Clonar o Repositório**

1. Abra o terminal (PowerShell ou CMD no Windows).
2. Navegue até o diretório onde deseja salvar o projeto:
   ```bash
   cd Desktop
   ```
3. Clone o repositório:
  ```bash
  git clone https://github.com/TeamHiveAPI/API-2025.01-BACK.git
  ```
4. Entre na pasta do projeto:
  ```bash
  cd API-2025.01-BACK
  ```
Passo 2: Configurar o Ambiente Virtual
Crie um ambiente virtual para isolar as dependências:
  ```bash
  python -m venv venv
  ```
Ative o ambiente virtual:
No Windows:
  ```bash
  venv\Scripts\activate
  ```
No Linux/Mac:
  ```bash
  source venv/bin/activate
  ```
Passo 3: Instalar as Dependências
Instale as dependências listadas no arquivo requirements.txt:
  ```bash
  pip install -r requirements.txt
  ```
Nota: Se o arquivo requirements.txt não existir, instale as bibliotecas manualmente:
  ```bash
  pip install fastapi uvicorn sqlalchemy psycopg2-binary
  ```
Passo 4: Configurar o Banco de Dados
Crie o banco de dados no PostgreSQL:
Abra o DBeaver ou pgAdmin.
Conecte-se com o usuário e senha do PostgreSQL (ex.: usuário postgres, senha 1234).
Crie um banco chamado api:
No DBeaver: clique com o botão direito em "Databases" > "Create New Database" > nomeie como api.
No terminal do PostgreSQL:
```sql
CREATE DATABASE api;
```
Atualize a URL de conexão:
Abra o arquivo database.py e verifique a variável DATABASE_URL:
```python
DATABASE_URL = "postgresql://postgres:1234@localhost:5432/api"
```
Ajuste o usuário (postgres), senha (1234), host (localhost), porta (5432) e nome do banco (api) conforme sua configuração.

Passo 5: Rodar a Aplicação
Inicie o servidor FastAPI com Uvicorn:
```bash
uvicorn main:app --reload
```
O parâmetro --reload faz o servidor reiniciar automaticamente ao alterar o código.
O servidor será iniciado em http://127.0.0.1:8000.

Passo 6: Aplicar Variáveis de Ambiente
Este projeto já contém um arquivo .env.sample com os exemplos de variáveis necessárias.

Copie esse arquivo para criar seu próprio .env:

```bash
cp .env.sample .env
```
# 🚀 Como Rodar o Código ESP32 (`esp32.ino`)

Este guia explica como configurar a IDE do Arduino, instalar bibliotecas, configurar o Mosquitto e rodar o código `esp32.ino` para o projeto de estação meteorológica.

---

## 1️⃣ Instalar a IDE do Arduino

- Baixe a IDE do Arduino (versão recomendada: **1.8.19**).

---

## 2️⃣ Instalar Bibliotecas Necessárias

1. Abra a IDE do Arduino.
2. Vá em **Sketch > Incluir Biblioteca > Gerenciar Bibliotecas...**
3. Procure e instale exatamente estas bibliotecas:
   - `DHT sensor library`
   - `PubSubClient`
   - `Adafruit Undefined Sensor` *(caso tenha problemas com o sensor)*
   - `WIFI` *(já vem incluída com o ESP32)*

---

## 3️⃣ Instalar a Placa do ESP32 na IDE do Arduino

1. Vá em **Arquivo > Preferências**.
2. No campo **URLs adicionais para Gerenciadores de Placas**, adicione:
   ```
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   ```
3. Abra **Ferramentas > Placa > Gerenciador de Placas...**
4. Procure por `esp32` e instale:
   - `esp32 by Espressif Systems`
   - `Arduino ESP32 Boards`

---

## 4️⃣ Configurar a Placa e Porta COM

1. Vá em **Ferramentas > Placa > ESP32 Arduino > ESP32 Dev Module** (exatamente esse nome).
2. Vá em **Ferramentas > Porta** e selecione a COM correta do seu ESP32 (geralmente COM3 ou COM4).

---

## 5️⃣ Configurar o Monitor Serial

1. Vá em **Ferramentas > Monitor serial**.
2. Ajuste a velocidade para **115200**.
   > *O monitor serial só funciona se o ESP32 estiver conectado e a porta COM correta selecionada.*

---

## 6️⃣ Instalar e Configurar o Mosquitto

1. Baixe e instale do site oficial:  
   [https://mosquitto.org/download/](https://mosquitto.org/download/)
2. Torne o Mosquitto acessível de outras máquinas (ESP32):
   - Vá até a pasta de instalação (geralmente `C:\Program Files\mosquitto`).
   - Edite ou crie o arquivo `mosquitto.config` e adicione ao final:
     ```
     # Permite conexões de qualquer IP
     listener 1883 0.0.0.0

     # Permite conexões anônimas (para testes)
     allow_anonymous true

     # Habilita logging
     log_dest file C:\Program Files\mosquitto\mosquitto.log
     log_type all
     ```
     > *Para editar na pasta do Mosquitto, abra o editor como administrador.*
3. Execute e teste o Mosquitto:
   - No terminal (como administrador):
     ```
     net stop mosquitto
     net start mosquitto
     ```
   - Em outro terminal (também como administrador):
     ```
     mosquitto -v
     ```
   - Para testar:
     ```
     mosquitto_sub -t "api-fatec/estacao/dados/" -h 127.0.0.1 -p 1883
     ```

---

## 7️⃣ Solução de Problemas: Erro "rc=-2" ao conectar com MQTT

1. Crie uma variável de ambiente `Path` com o caminho para o arquivo `mosquitto.exe`.
2. Verifique o firewall e crie regras de entrada para permitir conexões externas na porta **1883**.

---

## 8️⃣ Montar o Esquema Físico e Carregar o Código no ESP32

1. Pegue a placa fornecida pelo professor com o ESP32 e ligue o sensor no módulo 3 (pino 14).
   > *Atenção ao encaixar o GND do sensor com o GND da placa!*
2. Conecte o ESP32 ao computador e configure a porta COM conforme explicado.
3. Copie o código do arquivo `esp32.ino` para a IDE do Arduino:
   - Preencha o nome da sua rede Wi-Fi (SSID).
   - Preencha a senha da sua rede (password).
   - Edite o IP local da sua máquina para configurar corretamente o MQTT.
   - Para testes, altere o tempo de envio de `60000` (10 minutos) para `30000` (30 segundos).
4. Clique no botão de upload (seta para a direita) para compilar e enviar o código ao ESP32.
   > *IMPORTANTE: Feche o monitor serial antes de gravar o código no ESP32, senão a porta COM estará ocupada.*

---
