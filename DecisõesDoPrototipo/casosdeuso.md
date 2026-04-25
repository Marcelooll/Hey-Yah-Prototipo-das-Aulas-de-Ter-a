Para o seu repositório, o documento de **Casos de Uso** é o que conecta a visão de negócio (o que o usuário quer) com a implementação técnica (o que o código faz). Ele serve como o "manual de instruções" para o desenvolvimento em Java.

Aqui está a proposta de `CASOS_DE_USO.md` baseada na apresentação do seu grupo:

---

# 📑 Casos de Uso – Hey Ya!

Este documento descreve as funcionalidades do sistema sob a perspectiva do usuário e as interações entre os diferentes componentes do ecossistema  **Hey Ya!** .

---

## 👥 1. Atores e Fronteiras do Sistema

Definimos os limites do nosso software identificando quem interage com ele:

* **Usuário:** O ator principal que interage com a interface Android para gerenciar sua rotina.
* **Assistente de IA (OpenAI API):** Ator externo que recebe contextos de tarefas e devolve inteligência logística (cronogramas e prioridades).
* **Banco de Dados (MongoDB):** Responsável pela persistência e integridade das informações do usuário.

O foco aqui é garantir que o escopo do projeto permaneça fiel à entrega de valor direto, sem dispersão de recursos.

---

## 🔗 2. Funcionalidades e Relacionamentos

Utilizamos o mapeamento de casos de uso para entender o fluxo de navegação e as dependências do sistema:

* **Ações Essenciais (Include):** Funcionalidades fundamentais, como "Editar Tarefa" e "Gerar Cronograma", que formam o núcleo da aplicação.
* **Ações Complementares (Extend):** Funcionalidades opcionais ou condicionais que enriquecem a experiência do usuário.
* **Objetivo:** Ter uma visão clara das interações antes da codificação final, garantindo que a lógica de navegação seja intuitiva e funcional.

---

## 🛠️ 3. Especificação e Regras de Negócio

Para cada caso de uso, detalhamos não apenas o comportamento esperado, mas também o tratamento de erros:

* **Caminho Feliz (Fluxo Principal):** O cenário ideal onde o usuário executa as ações e o sistema responde perfeitamente.
* **Fluxos de Exceção:** Previsão de falhas críticas, como queda de conexão com a internet ou erros de resposta da API de IA.
* **Aplicação em Java:** Essas especificações servem como base para o desenvolvimento das classes, ajudando a prever exceções e validar dados antes da implementação.

---

## ✅ 4. Validação e Entrega de Valor

Os casos de uso funcionam como o nosso **Guia de Testes** e Garantia de Qualidade (QA):

* **Viabilidade Operacional:** Cada funcionalidade mapeada deve, obrigatoriamente, resolver um problema real identificado na fase de levantamento.
* **Critério de Sucesso:** O sistema final será considerado bem-sucedido se executar com precisão todas as funções prometidas e documentadas nestes diagramas e especificações.
