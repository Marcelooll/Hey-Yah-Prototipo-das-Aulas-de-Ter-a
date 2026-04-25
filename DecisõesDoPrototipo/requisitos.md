Essa é a parte onde o projeto deixa de ser apenas uma "ideia legal" e passa a ter um  **projeto de engenharia** . Para um estudante de Sistemas de Informação, detalhar bem os requisitos é o que separa um programador de um Analista de Sistemas.

Aqui está uma proposta de como estruturar essa **Análise de Requisitos** no seu GitHub, refinando o que você já tem e adicionando pontos cruciais para a viabilidade do  **Hey Ya!** :

---

# 📋 Análise de Requisitos – Hey Ya!

Este documento define as fronteiras do sistema, identificando os atores envolvidos e as regras que regem o funcionamento da aplicação.

## 👥 1. Identificação dos Stakeholders

* **Usuário Final:** Estudantes, freelancers e profissionais em regime de escala (ex: 12x36) que possuem rotinas variáveis e alta carga de tarefas.
* **Equipe de Desenvolvimento:** Responsáveis pela arquitetura, codificação (Java/Android) e modelagem de dados (MongoDB).
* **Provedores de Infraestrutura/API:** OpenAI (Processamento de Linguagem Natural), MongoDB Atlas (Hospedagem de Dados) e Google (Serviços de Calendário/Android).
* **Avaliadores Acadêmicos:** Professores da UNICID que validarão os critérios de prototipagem e engenharia de software.

---

## ✅ 2. Requisitos Funcionais (RF)

*O que o sistema deve entregar.*

* **RF01 - Configuração de Ciclo de Trabalho:** O sistema deve permitir que o usuário defina sua escala (ex: 12x36, 5x2, plantões esporádicos).
* **RF02 - Gestão de Tarefas (CRUD):** O sistema deve permitir criar, ler, atualizar e excluir tarefas com título, descrição, prazo e categoria.
* **RF03 - Inteligência Preditiva (IA):** O sistema deve sugerir janelas de estudo/descanso baseadas no nível de cansaço reportado e na escala de trabalho.
* **RF04 - Dashboard de Produtividade:** O sistema deve gerar visualizações (gráficos) do tempo gasto por área (Estudo, Trabalho, Saúde).
* **RF05 - Sincronização de Calendário:** O sistema deve permitir a importação de eventos de calendários externos para evitar conflitos de horários.
* **RF06 - Gamificação:** O sistema deve atribuir pontos e "níveis" conforme o usuário cumpre tarefas dentro do prazo.

---

## ⚙️ 3. Requisitos Não Funcionais (RNF)

*As qualidades e restrições do sistema.*

* **RNF01 - Compatibilidade:** A aplicação deve ser compatível com versões do Android 10.0 ou superior.
* **RNF02 - Persistência Flexível:** O sistema deve utilizar uma estrutura de dados orientada a documentos (JSON) para permitir mudanças rápidas no perfil do usuário sem quebrar o esquema do banco.
* **RNF03 - Baixa Latência:** O processamento local das tarefas deve ser instantâneo, com exceção das chamadas de IA que dependem da rede.
* **RNF04 - Offline-First:** O usuário deve conseguir visualizar e criar tarefas mesmo sem conexão à internet, com sincronização automática assim que a rede for restaurada.
* **RNF05 - Estética e Usabilidade:** A interface deve seguir as diretrizes do  *Material Design 3* , com foco em reduzir a carga cognitiva do usuário.

---

## 🏗️ 4. Regras de Negócio (RN)

*As leis que regem como o app toma decisões.*

* **RN01 - Priorização Eisenhower:** Nenhuma tarefa pode ser marcada como "Urgente e Importante" simultaneamente pela IA se o usuário já possuir mais de 3 tarefas nesse quadrante no mesmo dia (Prevenção de Burnout).
* **RN02 - Cálculo de Escala:** Se o usuário estiver em dia de plantão (12h), o app deve bloquear automaticamente sugestões de tarefas de alta densidade cognitiva (ex: estudar cálculos complexos) após a 8ª hora de trabalho.
* **RN03 - Privacidade de Dados:** Dados processados pela API da OpenAI não devem conter informações de identificação pessoal direta (PII) sensíveis, enviando apenas o contexto da tarefa.
