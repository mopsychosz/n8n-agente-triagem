# Agente Triador de Chamados de Suporte (n8n + OpenAI)

Este projeto consiste numa automação de ponta a ponta desenvolvida em **n8n** que utiliza modelos de Linguagem (LLM / OpenAI) para receber, analisar e classificar chamados de suporte ao cliente em tempo real, gerando respostas estruturadas e reduzindo o tempo de atendimento humano.

---

## Problema do Negócio Resolvido
Em equipas de atendimento ao cliente, a triagem manual de incidentes consome muito tempo. Esta solução automatiza:
- A leitura imediata da mensagem do cliente.
- A categorização da **urgência** (Alta, Média ou Baixa).
- A geração de um **resumo objetivo** do problema.
- A elaboração de uma **resposta sugestiva pronta** para a equipa de suporte enviar.

---

## Tecnologias e Ferramentas Utilizadas
- **n8n Cloud:** Orquestração do fluxo de automação e interface de formulário.
- **OpenAI API (GPT):** Processamento de linguagem natural e engenharia de prompts.
- **JSON:** Exportação e versionamento do workflow.

---

## Fluxo de Funcionamento (Workflow)
1. **n8n Form Trigger:** O utilizador/cliente envia o texto da reclamação ou dúvida através de um formulário web.
2. **Basic LLM Chain + OpenAI Chat Model:** A mensagem é enviada ao modelo de IA com instruções específicas (Prompt Engineering) para categorização e síntese.
3. **Form Ending Page:** A IA devolve o resultado formatado no próprio ecrã para rápida visualização do operador ou do cliente.

---

## Demonstração / Screenshots
<img width="1839" height="927" alt="Captura de tela 2026-11-04 132841" src="https://github.com/user-attachments/assets/f4047bbd-5caf-41b7-98cc-379d39d006f8" />

---

## Como Importar e Utilizar
1. Descarrega o ficheiro `workflow-agente-triagem.json` presente neste repositório.
2. No teu painel do n8n, clica em **Workflows** > **Import from File**.
3. Associa a tua credencial da **OpenAI API** ao nó do modelo.
4. Ativa o workflow e testa!
