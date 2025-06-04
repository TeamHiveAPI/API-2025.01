# 📚 Fluxo de Documentação

Este documento define o fluxo, organização e responsabilidades para a documentação do projeto, visando clareza, rastreabilidade e facilidade de manutenção.

---

## 🗂️ Estrutura Geral

A documentação está organizada em dois grandes grupos:

### 1. 📋 Documentos de Processo

> **Foco:** Como o time trabalha, padrões, versionamento e governança da documentação.

- **Changelog de Documentação:** [docs/changelog.md](../changelog.md)
- **Changelogs Técnicos:**
  - Backend: [changelog.md](https://github.com/TeamHiveAPI/API-2025.01-BACK/blob/main/changelog.md)
  - Frontend: [changelog.md](https://github.com/TeamHiveAPI/API-2025.01-FRONT/blob/main/changelog.md)
- **Política de Versionamento e Padrão de Branch:** [Wiki - Critérios para atualização de versões e controle de mudanças](https://github.com/TeamHiveAPI/API-2025.01/wiki/Controle-de-Vers%C3%A3o-e-Padr%C3%A3o-de-Branch#controle-de-vers%C3%A3o)
- **Backlog da Sprint:** [Wiki - Planejamento e acompanhamento das tarefas da sprint](https://github.com/TeamHiveAPI/API-2025.01/wiki/Rastreabilidade-de-Requisitos#sprint-backlog)
- **Template de Processo:**
  - [docs/templates/template_changelog.md](../templates/template_changelog.md)
- **Gestão Visual de Tarefas:** [Quality Assurance - Gestão Visual de Tarefas - Scrum](https://github.com/TeamHiveAPI/API-2025.01/wiki/Quality-Assurance#-gest%C3%A3o-visual-de-tarefas---scrum)
- **Documentação Contínua:** [Quality Assurance - Documentação Contínua](https://github.com/TeamHiveAPI/API-2025.01/wiki/Quality-Assurance#-documenta%C3%A7%C3%A3o-cont%C3%ADnua)
- **Escalabilidade de Processos:** [Quality Assurance - Escalabilidade de Processos](https://github.com/TeamHiveAPI/API-2025.01/wiki/Quality-Assurance#-escalabilidade-de-processos)
- **Automação de Build, Teste e Deploy:** [Quality Assurance - Automação de Build, Teste e Deploy](https://github.com/TeamHiveAPI/API-2025.01/wiki/Quality-Assurance#automação-de-build-teste-e-deploy)

---

### 2. 📦 Documentos de Produto

> **Foco:** O que o sistema entrega ao usuário final.

- **Guia de Instalação Geral:** [Guia de Instalação Geral - API Estação Meteorológica](https://github.com/TeamHiveAPI/API-2025.01/wiki/Docs#-guia-de-instala%C3%A7%C3%A3o-geral---api-esta%C3%A7%C3%A3o-meteorol%C3%B3gica)
- **Documentação de Rotas Backend:** [API Estação Meteorológica](https://github.com/TeamHiveAPI/API-2025.01/wiki/Docs#-api-esta%C3%A7%C3%A3o-meteorol%C3%B3gica)
- **Documentação de Arquitetura:** [Arquitetura do Sistema](https://github.com/TeamHiveAPI/API-2025.01/wiki/Docs#-arquitetura-do-sistema)
- **Requisitos Funcionais:** [Wiki - Lista de funcionalidades obrigatórias do sistema](https://github.com/TeamHiveAPI/API-2025.01/wiki/Rastreabilidade-de-Requisitos#requisitos-funcionais)
- **Requisitos Não Funcionais:** [Wiki - Restrições e qualidades do sistema](https://github.com/TeamHiveAPI/API-2025.01/wiki/Rastreabilidade-de-Requisitos#requisitos-n%C3%A3o-funcionais)
- **Backlog do Produto:** [Wiki - Lista priorizada de funcionalidades e requisitos do produto](https://github.com/TeamHiveAPI/API-2025.01/wiki/Rastreabilidade-de-Requisitos#product-backlog)
- **Templates de Produto:**
  - [docs/templates/template_arquitetura.md](../templates/template_arquitetura.md)
  - [docs/templates/template_rotasBackend.md](../templates/template_rotasBackend.md)
  - [docs/templates/template_manual.md](../templates/template_manual.md)
  - [docs/templates/template_instalacao.md](../templates/template_instalacao.md)

- **Cobertura de Testes:** [Quality Assurance - Cobertura de Testes](https://github.com/TeamHiveAPI/API-2025.01/wiki/Quality-Assurance#cobertura-de-testes)
- **Padrões de Código:** [Quality Assurance - Sobre Qualidade de Código](https://github.com/TeamHiveAPI/API-2025.01/wiki/Quality-Assurance#-sobre-qualidade-de-c%C3%B3digo)
- **Facilidade de Manutenção:** [Quality Assurance - Facilidade de Manutenção](https://github.com/TeamHiveAPI/API-2025.01/wiki/Quality-Assurance#-facilidade-de-manuten%C3%A7%C3%A3o)
- **Resultados do Quality Assurance:** [Quality Assurance - Resultados](https://github.com/TeamHiveAPI/API-2025.01/wiki/Quality-Assurance-%E2%80%90-Resultados)

---

## 🔄 Fluxo de Atualização

1. **Criação/alteração:** Sempre que houver mudança relevante, crie ou atualize o documento correspondente.
2. **Padronização:** Utilize os templates disponíveis para garantir uniformidade.
3. **Revisão:** Submeta a alteração para revisão de outro membro do time (preferencialmente).
4. **Registro:** Atualize o changelog de documentação detalhando a alteração. Atualize também os changelogs técnicos conforme necessário.
5. **Publicação:** Após revisão, publique a versão final na pasta correta.
6. **Comunicação:** Informe o time sobre mudanças relevantes.

---

## 📝 Boas Práticas

- **Clareza e objetividade:** Seja direto, evite jargões desnecessários.
- **Atualização contínua:** Mantenha os documentos sempre atualizados.
- **Controle de versão:** Sempre registre mudanças no changelog de documentação e nos changelogs técnicos.
- **Separação de contextos:** Mantenha claro o que é processo, projeto e produto.

---

## ℹ️ Justificativa da Classificação dos Documentos

**Documentos de Processo:**  
São aqueles que descrevem como o time trabalha, define padrões, políticas, templates e práticas de desenvolvimento. Eles garantem a organização, a qualidade e a previsibilidade do trabalho, independentemente do produto final. Exemplos: changelogs, políticas de versionamento, templates, gestão visual de tarefas, automação de processos, etc.

**Documentos de Produto:**  
São aqueles que descrevem o que o sistema entrega ao usuário final, detalhando funcionalidades, requisitos, arquitetura, rotas, manuais, padrões de código e resultados de qualidade. Eles documentam as características, funcionamento e qualidade do produto entregue. Exemplos: guia de instalação, documentação de rotas, arquitetura, requisitos, backlog do produto, padrões de código, resultados do quality assurance, etc.

> **Referência:**
> A distinção entre documentos de processo e de produto segue recomendações de frameworks e normas reconhecidas, como o PMBOK (PMI), ISO/IEC/IEEE 12207:2017 e o Scrum Guide, que orientam a separação entre artefatos que descrevem o "como fazer" (processo) e o "o que é entregue" (produto).

---
