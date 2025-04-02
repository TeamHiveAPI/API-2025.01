# Sistema de Coleta de Dados de Estações Meteorológicas

## 🌟 Visão Geral
Projeto da Fatec SJC em parceria com a Tecsus para criar um sistema IoT de monitoramento meteorológico, com foco em coleta, processamento e visualização de dados, além de alertas e educação ambiental.

---
# Sistema de Coleta de Dados de Estações Meteorológicas

## Sprint 2 - Sprint Backlog

### 🎯 Objetivo da Sprint
Desenvolver funcionalidades que permitam a coleta, processamento e visualização de dados meteorológicos, além de gerar alertas automáticos com base nas condições definidas.

---

### 📋 Sprint Backlog

Abaixo estão as atividades planejadas para a Sprint 2, detalhando as tarefas necessárias para implementar os requisitos priorizados.

| **ID**     | **Atividade**                                                                                                          | **Estimativa de Esforço** | **Estimativa de Dificuldade** |
|------------|-----------------------------------------------------------------------------------------------------------------------|---------------------------|-------------------------------|
| **SB2-01** | Configurar o endpoint da API para receber dados das estações meteorológicas via protocolo (ex.: Sigfox, LoRa).         | 8 horas                   | Média                        |
| **SB2-02** | Implementar a lógica de autenticação e autorização para a recepção de dados, se necessário.                            | 4 horas                   | Baixa                        |
| **SB2-03** | Criar um serviço para processar os dados recebidos, incluindo validação de integridade e conversão de formatos.         | 12 horas                  | Alta                         |
| **SB2-04** | Implementar cálculos de agregados (ex.: médias, máximos, mínimos) para os dados processados.                            | 6 horas                   | Média                        |
| **SB2-05** | Desenvolver a lógica para armazenar os dados processados no banco de dados, associando-os à estação e parâmetro.        | 8 horas                   | Média                        |
| **SB2-06** | Criar endpoints da API para consulta de dados em tempo real e histórico.                                               | 10 horas                  | Alta                         |
| **SB2-07** | Desenvolver a interface do dashboard para visualização em tempo real, incluindo gráficos e tabelas.                     | 12 horas                  | Alta                         |
| **SB2-08** | Implementar a atualização automática do dashboard a cada 5 minutos.                                                    | 4 horas                   | Baixa                        |
| **SB2-09** | Criar a interface do dashboard para visualização do histórico de dados, com filtros por data e estação.                 | 10 horas                  | Alta                         |
| **SB2-10** | Implementar a funcionalidade de exportação de dados históricos em CSV.                                                 | 6 horas                   | Média                        |
| **SB2-11** | Desenvolver a lógica para verificar as condições de alerta a cada ciclo de dados recebidos.                             | 8 horas                   | Média                        |
| **SB2-12** | Implementar o disparo de notificações (ex.: e-mail, SMS) quando uma condição de alerta é atingida.                      | 10 horas                  | Alta                         |
| **SB2-13** | Criar uma interface para administradores definirem as condições de alerta (ex.: temperatura > 35°C).                    | 8 horas                   | Média                        |
| **SB2-14** | Integrar a definição de condições de alerta com o backend.                                                             | 4 horas                   | Baixa                        |
| **SB2-15** | Desenvolver a lógica para notificar os usuários sobre os alertas gerados, incluindo detalhes da condição disparada.     | 6 horas                   | Média                        |
| **SB2-16** | Implementar a exibição de alertas no dashboard para usuários públicos.                                                 | 4 horas                   | Baixa                        |
| **SB2-17** | Integrar conceitos estatísticos nos dashboards, como médias diárias, tendências e correlações.                          | 10 horas                  | Alta                         |
| **SB2-18** | Desenvolver pelo menos três relatórios distintos (ex.: resumo diário, análise mensal, alertas disparados).             | 12 horas                  | Alta                         |
| **SB2-19** | Criar a interface para geração e exportação de relatórios em PDF ou Excel.                                             | 8 horas                   | Média                        |
| **SB2-20** | Testar a recepção de dados simulando o envio de diferentes tipos de dados e condições.                                 | 6 horas                   | Média                        |
| **SB2-21** | Testar o processamento de dados, incluindo casos de dados inválidos ou incompletos.                                     | 4 horas                   | Baixa                        |
| **SB2-22** | Testar o armazenamento de dados, verificando a integridade e a recuperação correta.                                     | 4 horas                   | Baixa                        |
| **SB2-23** | Testar a visualização em tempo real, garantindo que os dados são atualizados corretamente.                              | 4 horas                   | Baixa                        |
| **SB2-24** | Testar a visualização do histórico, aplicando filtros e exportando dados.                                               | 4 horas                   | Baixa                        |
| **SB2-25** | Testar a geração de alertas, simulando condições que disparam notificações.                                             | 6 horas                   | Média                        |
| **SB2-26** | Testar a definição de condições de alerta, garantindo que são salvas e aplicadas corretamente.                          | 4 horas                   | Baixa                        |
| **SB2-27** | Testar a notificação de usuários, verificando se as mensagens são enviadas e recebidas corretamente.                    | 4 horas                   | Baixa                        |
| **SB2-28** | Testar a integração de conceitos estatísticos nos dashboards, verificando a precisão dos cálculos.                      | 4 horas                   | Média                        |
| **SB2-29** | Testar a geração de relatórios, garantindo que os dados são corretos e os formatos de exportação funcionam.             | 4 horas                   | Baixa                        |

---

### 📝 Notas sobre o Sprint Backlog

- **Estimativa de Esforço**: Calculada em horas para facilitar o planejamento. Total: **190 horas**.
- **Estimativa de Dificuldade**:
  - **Baixa**: Tarefas simples ou repetitivas, como testes básicos ou integrações menores.
  - **Média**: Tarefas que requerem esforço moderado ou conhecimento específico, como cálculos estatísticos ou interfaces básicas.
  - **Alta**: Tarefas complexas que envolvem integração de sistemas, desenvolvimento de interfaces avançadas ou lógica crítica.
- **Ajustes**: As estimativas e dificuldades podem ser refinadas com base na experiência da equipe durante a sprint.

---

## 📋 Requisitos Funcionais

**Funcionalidades que o sistema deve oferecer para atender aos objetivos do projeto.**

| **ID**   | **Descrição**                                                                                                          | **Prioridade** |
|----------|-----------------------------------------------------------------------------------------------------------------------|----------------|
| **RF01** | O sistema deve permitir que administradores criem, leiam, atualizem e excluam (CRUD) estações meteorológicas, incluindo localização (latitude e longitude), sensores instalados e status operacional. | Alta 🚀        |
| **RF02** | O sistema deve permitir que administradores definam, visualizem, modifiquem e removam parâmetros meteorológicos (ex.: temperatura, umidade) associados a cada estação. | Alta 🚀        |
| **RF03** | O sistema deve permitir que administradores configurem, consultem, alterem e removam alertas baseados em limites (thresholds) de parâmetros meteorológicos. | Alta 🚀        |
| **RF04** | O sistema deve permitir que administradores gerenciem usuários, incluindo criação, leitura, atualização e exclusão. | Alta 🚀        |
| **RF05** | O sistema deve receber dados enviados pelas estações meteorológicas via protocolos como Sigfox, LoRa ou NB-IoT. | Média 🛠️       |
| **RF06** | O sistema deve processar os dados recebidos, validando integridade, convertendo formatos e calculando agregados (ex.: médias), se necessário. | Média 🛠️       |
| **RF07** | O sistema deve armazenar os dados processados em um banco de dados relacional ou não relacional, garantindo integridade e disponibilidade. | Média 🛠️       |
| **RF08** | O sistema deve fornecer dashboards interativos que exibam dados meteorológicos em tempo real, atualizados a cada 5 minutos. | Média 🛠️       |
| **RF09** | O sistema deve permitir a visualização do histórico de dados meteorológicos em dashboards, com filtros por data e estação. | Média 🛠️       |
| **RF10** | O sistema deve gerar notificações automáticas (via e-mail ou SMS) quando condições meteorológicas predefinidas forem atingidas. | Média 🛠️       |
| **RF11** | Administradores devem poder definir condições para disparo de alertas, como "temperatura > 35°C" ou "umidade < 20%". | Média 🛠️       |
| **RF12** | O sistema deve enviar notificações aos usuários sobre alertas gerados, incluindo detalhes da condição que os disparou. | Média 🛠️       |
| **RF13** | O sistema deve implementar um datalogger que colete dados dos sensores a cada 10 minutos e os armazene localmente. | Baixa 🌱       |
| **RF14** | O datalogger deve armazenar dados localmente por até 24 horas antes de enviá-los ao servidor. | Baixa 🌱       |
| **RF15** | O datalogger deve enviar os dados coletados ao servidor central a cada hora, via Wi-Fi ou conexão celular. | Baixa 🌱       |
| **RF16** | A equipe deve selecionar componentes de baixo custo para a estação meteorológica, incluindo sensores de vento, pluviômetro, umidade, temperatura e pressão. | Baixa 🌱       |
| **RF17** | A equipe deve montar fisicamente a estação meteorológica, garantindo que todos os sensores estejam calibrados e operacionais. | Baixa 🌱       |
| **RF18** | A equipe deve testar e calibrar a estação meteorológica para garantir precisão dos dados dentro de ±2% de erro. | Baixa 🌱       |
| **RF19** | O sistema deve incluir um guia educativo no portal, explicando o significado de cada parâmetro meteorológico medido. | Baixa 🌱       |
| **RF20** | O guia educativo deve explicar conceitos matemáticos (ex.: média, desvio padrão) usados nos cálculos dos parâmetros. | Baixa 🌱       |
| **RF21** | O tutorial educativo deve ser acessível no portal do sistema, com navegação intuitiva para usuários públicos. | Baixa 🌱       |
| **RF22** | O sistema deve implementar controle de acesso para administradores, permitindo gerenciar estações, parâmetros, alertas e usuários. | Baixa 🌱        |
| **RF23** | O sistema deve permitir que usuários públicos visualizem dashboards e relatórios, sem permissões de edição. | Baixa 🌱        |
| **RF24** | Os dashboards devem incluir análises estatísticas, como médias diárias, tendências e correlações entre parâmetros. | Média 🛠️       |
| **RF25** | O sistema deve gerar pelo menos três tipos de relatórios (resumo diário, análise mensal e alertas disparados), exportáveis em PDF ou Excel. | Média 🛠️       |

---

## 🔧 Requisitos Não Funcionais

**Qualidades e restrições que garantem a excelência e usabilidade do sistema.**

| **ID**    | **Descrição**                                                                                                          | **Prioridade** |
|-----------|-----------------------------------------------------------------------------------------------------------------------|----------------|
| **RNF01** | Os dashboards devem ter uma interface intuitiva, com tempo de aprendizado inferior a 10 minutos para novos usuários. | Média 🛠️       |
| **RNF02** | Os dashboards devem seguir um design profissional, com cores consistentes e gráficos claros, avaliados por feedback de usuários. | Média 🛠️       |
| **RNF03** | O portal deve incluir elementos educacionais (ex.: quizzes ou infográficos) para engajar alunos do ensino médio. | Baixa 🌱       |
| **RNF04** | O portal deve demonstrar como conceitos matemáticos (ex.: médias) são aplicados aos dados meteorológicos. | Baixa 🌱       |
| **RNF05** | O sistema deve promover aprendizado baseado em problemas, permitindo simular cenários e visualizar impactos nos dados. | Baixa 🌱       |
| **RNF06** | A documentação da API deve ser completa, com descrições de rotas, parâmetros e respostas, usando ferramentas como Swagger. | Alta 🚀        |
| **RNF07** | A documentação da API deve incluir exemplos de requisições e respostas para cada rota. | Alta 🚀        |
| **RNF08** | O projeto deve configurar um pipeline de integração contínua que execute testes automatizados a cada commit. | Alta 🚀        |
| **RNF09** | O pipeline deve incluir testes unitários e de integração, com cobertura mínima de 80% do código. | Alta 🚀        |
| **RNF10** | O deploy deve ser automático para ambientes de teste após merge na branch principal e para produção após aprovação manual. | Alta 🚀        |
| **RNF11** | O deploy automático deve garantir zero downtime, usando estratégias como blue-green deployment ou rolling updates. | Alta 🚀        |

## 🎨 Estilização e Priorização
- **🚀 Alta**: Requisitos críticos para a base do sistema (Sprint 01 e fundamentos técnicos).
- **🛠️ Média**: Funcionalidades importantes para o uso do sistema (Sprint 02).
- **🌱 Baixa**: Complementos e objetivos educacionais (Sprint 03 e atividades paralelas).

---

## 📌 Product Backlog

**Planejamento das funcionalidades a serem desenvolvidas ao longo das sprints.**

| **ID** | **Descrição da Funcionalidade**                                          | **Requisito Relacionado** | **Sprint**   |
|--------|--------------------------------------------------------------------------|---------------------------|--------------|
| 1      | Implementar CRUD de estações meteorológicas                              | RF01                      | Sprint 01    |
| 2      | Implementar CRUD de parâmetros meteorológicos                            | RF02                      | Sprint 01    |
| 3      | Implementar CRUD de alertas                                              | RF03                      | Sprint 01    |
| 4      | Implementar CRUD de usuários                                             | RF04                      | Sprint 01    |
| 5      | Desenvolver recepção de dados das estações meteorológicas                | RF05                      | Sprint 02    |
| 6      | Implementar processamento dos dados recebidos                            | RF06                      | Sprint 02    |
| 7      | Armazenar os dados processados no banco de dados                         | RF07                      | Sprint 02    |
| 8      | Criar dashboard interativo para visualização de dados em tempo real      | RF08                      | Sprint 02    |
| 9      | Criar dashboard interativo para visualização de histórico de dados       | RF09                      | Sprint 02    |
| 10     | Implementar geração automática de notificações                           | RF10                      | Sprint 02    |
| 11     | Definir condições para disparo de alertas                                | RF11                      | Sprint 02    |
| 12     | Implementar notificação de usuários sobre os alertas                     | RF12                      | Sprint 02    |
| 13     | Integrar conceitos estatísticos nos dashboards                           | RF24                      | Sprint 02    |
| 14     | Criar pelo menos três relatórios distintos com insights                  | RF25                      | Sprint 02    |
| 15     | Implementar controle de acesso para administradores                      | RF22                      | Sprint 03    |
| 16     | Implementar controle de acesso para usuários públicos                    | RF23                      | Sprint 03    |
| 17     | Desenvolver um datalogger para coleta de dados                           | RF13                      | Sprint 03    |
| 18     | Implementar armazenamento temporário dos dados coletados pelo datalogger | RF14                      | Sprint 03    |
| 19     | Enviar os dados coletados pelo datalogger para o servidor                | RF15                      | Sprint 03    |
| 20     | Selecionar componentes para montagem da estação meteorológica            | RF16                      | Sprint 03    |
| 21     | Montar fisicamente a estação meteorológica                               | RF17                      | Sprint 03    |
| 22     | Testar e calibrar a estação meteorológica                                | RF18                      | Sprint 03    |
| 23     | Criar guia explicativo sobre os parâmetros meteorológicos                | RF19                      | Sprint 03    |
| 24     | Incluir conceitos matemáticos no guia educativo                          | RF20                      | Sprint 03    |
| 25     | Disponibilizar o tutorial educativo no portal do sistema                 | RF21                      | Sprint 03    |

## 📋 User Stories

**Histórias de usuário definidas para as funcionalidades do sistema.**

| **ID** | **User Story**                                                                                          | **Critérios de Aceitação**                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **US01** | Como administrador, eu quero criar uma nova estação meteorológica fornecendo nome, CEP, rua, bairro, cidade, número, latitude, longitude, data de instalação e status, para registrar uma nova estação no sistema. | - Entrada de todos os campos mencionados. <br> - Validação de campos obrigatórios (nome, CEP, latitude, longitude, data, status). <br> - Suporte a inserção manual ou via CEP. <br> - Estação exibida na lista após criação. |
| **US02** | Como administrador, eu quero visualizar a lista de todas as estações meteorológicas cadastradas, com nome, cidade, status e data de instalação, para ter uma visão geral. | - Lista com nome, cidade, status e data. <br> - Suporte a paginação ou rolagem. <br> - Filtros ou ordenação por nome ou status. |
| **US03** | Como administrador, eu quero visualizar os detalhes completos de uma estação meteorológica específica, para verificar suas informações. | - Exibição de todos os campos ao selecionar uma estação. <br> - Dados recuperados corretamente do banco. |
| **US04** | Como administrador, eu quero atualizar as informações de uma estação meteorológica existente, podendo alterar qualquer campo, para manter os dados atualizados. | - Edição de todos os campos. <br> - Validação de dados obrigatórios. <br> - Salvamento apenas com dados válidos. |
| **US05** | Como administrador, eu quero excluir uma estação meteorológica que não está mais em uso, para manter o sistema organizado. | - Confirmação antes da exclusão. <br> - Estação removida da lista após exclusão. <br> - Registro da ação (ex.: log). |
| **US06** | Como administrador, eu quero criar um novo parâmetro meteorológico com nome, unidade e descrição, para associá-lo a estações. | - Entrada de nome, unidade e descrição. <br> - Nome único. <br> - Parâmetro disponível na lista após criação. |
| **US07** | Como administrador, eu quero visualizar a lista de todos os parâmetros meteorológicos cadastrados, com nome, unidade e descrição, para gerenciá-los. | - Lista com nome, unidade e descrição. <br> - Suporte a paginação ou rolagem. <br> - Filtros ou ordenação por nome. |
| **US08** | Como administrador, eu quero visualizar os detalhes completos de um parâmetro meteorológico específico, para verificar suas informações. | - Exibição de todos os campos. <br> - Dados recuperados corretamente. |
| **US09** | Como administrador, eu quero atualizar as informações de um parâmetro meteorológico existente, para mantê-lo atualizado. | - Edição de nome, unidade e descrição. <br> - Validação de nome único. <br> - Salvamento com dados válidos. |
| **US10** | Como administrador, eu quero excluir um parâmetro meteorológico que não está mais em uso, para organizar o sistema. | - Confirmação antes da exclusão. <br> - Parâmetro removido da lista. <br> - Impedir exclusão se associado a estações. |
| **US11** | Como administrador, eu quero criar um alerta com nome, descrição e condição, para monitorar eventos específicos. | - Entrada de nome, descrição e condição. <br> - Validação da condição. <br> - Alerta disponível após criação. |
| **US12** | Como administrador, eu quero visualizar a lista de alertas cadastrados, para gerenciá-los. | - Lista com nome, descrição e condição. <br> - Suporte a paginação. <br> - Filtros por nome ou status. |
| **US13** | Como administrador, eu quero atualizar um alerta existente, para ajustá-lo às necessidades atuais. | - Edição de nome, descrição e condição. <br> - Validação da condição. <br> - Salvamento com dados válidos. |
| **US14** | Como administrador, eu quero excluir um alerta que não é mais necessário, para manter o sistema limpo. | - Confirmação antes da exclusão. <br> - Alerta removido da lista. |
| **US15** | Como administrador, eu quero criar um usuário com nome, e-mail, senha e nível de acesso, para gerenciar permissões. | - Entrada de nome, e-mail, senha e nível. <br> - Validação de e-mail único. <br> - Usuário disponível após criação. |
| **US16** | Como administrador, eu quero visualizar a lista de usuários cadastrados, para gerenciá-los. | - Lista com nome, e-mail e nível de acesso. <br> - Suporte a paginação. <br> - Filtros por nome ou nível. |
| **US17** | Como administrador, eu quero atualizar os dados de um usuário existente, para mantê-los atualizados. | - Edição de nome, e-mail, senha e nível. <br> - Validação de e-mail único. <br> - Salvamento com dados válidos. |
| **US18** | Como administrador, eu quero excluir um usuário que não precisa mais de acesso, para manter o sistema seguro. | - Confirmação antes da exclusão. <br> - Usuário removido da lista. |
| **US19** | Como sistema, eu quero receber dados das estações via Sigfox, LoRa ou NB-IoT, para iniciar o processamento. | - Suporte a um protocolo. <br> - Registro de data e hora de recebimento. <br> - Tratamento de falhas. |
| **US20** | Como sistema, eu quero processar os dados recebidos, convertendo-os e validando-os, para garantir sua utilidade. | - Conversão de dados brutos (ex.: °C). <br> - Validação de valores (ex.: -50°C a 60°C). <br> - Rejeição de dados inválidos. |
| **US21** | Como sistema, eu quero armazenar os dados processados no banco, associando-os à estação e parâmetro, para consulta futura. | - Armazenamento com estação, parâmetro, valor, data e hora. <br> - Integridade e eficiência na recuperação. |
| **US22** | Como usuário público, eu quero visualizar um dashboard em tempo real, atualizado a cada 5 minutos, para acompanhar os dados. | - Gráficos ou tabelas em tempo real. <br> - Atualização a cada 5 minutos. <br> - Filtros por estação ou parâmetro. |
| **US23** | Como usuário público, eu quero visualizar o histórico de dados de uma estação, com filtros por período, para análise. | - Seleção de estação, parâmetro e período. <br> - Exibição em tabela ou gráfico. <br> - Exportação em CSV. |
| **US24** | Como sistema, eu quero gerar notificações automáticas quando uma condição de alerta for atingida, para informar usuários. | - Verificação a cada ciclo de dados. <br> - Geração de notificação com mensagem. <br> - Registro do disparo. |
| **US25** | Como administrador, eu quero definir condições de alertas (ex.: temperatura > 35°C), para monitoramento. | - Entrada de condições. <br> - Associação a um alerta. <br> - Validação da lógica. |
| **US26** | Como sistema, eu quero enviar notificações de alertas via e-mail ou SMS, para usuários cadastrados. | - Suporte a e-mail e/ou SMS. <br> - Inclusão da mensagem do alerta. <br> - Registro de envio. |
| **US27** | Como sistema, eu quero coletar dados dos sensores a cada 10 minutos com um datalogger, para armazenamento local. | - Coleta periódica. <br> - Armazenamento temporário. <br> - Registro de falhas. |
| **US28** | Como sistema, eu quero armazenar dados localmente por até 24 horas, antes de enviá-los ao servidor. | - Capacidade para 24 horas. <br> - Gerenciamento de espaço. <br> - Priorização de dados antigos. |
| **US29** | Como sistema, eu quero enviar os dados do datalogger ao servidor a cada hora, via Wi-Fi ou celular. | - Envio periódico. <br> - Confirmação de recebimento. <br> - Retentativas em caso de falha. |
| **US30** | Como equipe, eu quero selecionar componentes de baixo custo para a estação, para viabilizar o projeto. | - Lista de componentes aprovada. <br> - Orçamento respeitado. <br> - Compatibilidade técnica. |
| **US31** | Como equipe, eu quero montar a estação meteorológica, garantindo que os sensores estejam calibrados. | - Montagem completa. <br> - Testes de funcionalidade. <br> - Calibração inicial. |
| **US32** | Como equipe, eu quero testar e calibrar a estação, para garantir precisão dentro de ±2% de erro. | - Protocolo de testes definido. <br> - Ajustes de calibração. <br> - Documentação dos resultados. |
| **US33** | Como usuário público, eu quero acessar um guia educativo que explique os parâmetros meteorológicos. | - Conteúdo claro e acessível. <br> - Navegação intuitiva. <br> - Exemplos incluídos. |
| **US34** | Como usuário público, eu quero entender conceitos matemáticos (ex.: média, desvio padrão) aplicados aos dados. | - Explicações didáticas. <br> - Exemplos práticos. <br> - Quizzes interativos. |
| **US35** | Como usuário público, eu quero navegar pelo tutorial educativo de forma intuitiva no portal. | - Interface amigável. <br> - Menu claro. <br> - Suporte a busca por tópicos. |
| **US36** | Como administrador, eu quero fazer login no sistema, para acessar funcionalidades restritas. | - Formulário com e-mail e senha. <br> - Redirecionamento ao painel após autenticação. <br> - Erro para credenciais inválidas. |
| **US37** | Como usuário público, eu quero visualizar dashboards e relatórios sem login, para acesso fácil. | - Dashboards acessíveis sem autenticação. <br> - Sem permissões de edição para não autenticados. |
| **US38** | Como usuário público, eu quero ver análises estatísticas nos dashboards, como médias e tendências. | - Exibição de médias, máximos e mínimos. <br> - Gráficos de tendências. <br> - Correlações entre parâmetros. |
| **US39** | Como usuário público, eu quero gerar relatórios (diário, mensal, alertas) e exportá-los em PDF ou Excel. | - Seleção de tipo de relatório. <br> - Geração em formato exportável. <br> - Dados relevantes incluídos. |
