# Documentação do Módulo: Assistente Acadêmico Inteligente com IA e RAG

<img width="901" height="514" alt="image" src="https://github.com/user-attachments/assets/39d7997e-cf50-4f61-a69c-6e9055896e87" />


Este documento detalha a arquitetura, o fluxo de execução e a estrutura de configuração do cenário de automação responsável pelo tutor virtual do programa **Todas em Tech - IA Aplicada**.

---

## 1. Visão Geral da Automação

O fluxo foi desenhado para atuar como o ponto de contato principal entre a aluna e o programa educacional. Ele opera por meio de uma interface de chat interativa, processando a intenção da usuária, aplicando regras de negócio e restrições de escopo, consultando bases de conhecimento externas (Documentação do Curso via RAG) e devolvendo uma resposta contextualizada, acolhedora e precisa.

### Arquitetura do Fluxo no Make
1. **Chat Trigger:** Recebe a mensagem enviada pela usuária na interface de chat.
2. **Make AI Agent (ou Módulo de IA com Ferramentas):** Processa a mensagem utilizando o prompt do sistema, gerencia o histórico de conversas e decide quando acionar ferramentas auxiliares.
3. **Ferramenta de Conhecimento (Knowledge / Documentação):** Consulta os documentos oficiais do curso (cronograma, links e guias) para recuperar informações precisas.
4. **Chat Response:** Devolve o conteúdo processado e estruturado de volta para a tela da aluna.

---

## 2. Detalhamento dos Componentes e Módulos

### Módulo 1: Chat Trigger (Gatilho de Entrada)
* **Função:** Captura a mensagem enviada pela usuária na interface do chat em tempo real.
* **Dados Recebidos:** Texto da mensagem (`text`), identificador da sessão/usuário e metadados da conversa.

### Módulo 2: Make AI Agent / Assistente de IA
* **Função:** O núcleo inteligente da automação. Ele é configurado com as diretrizes de comportamento, restrições e o prompt acadêmico oficial.
* **Responsabilidades lógicas:**
  * Identificar o nome da usuária no início da interação.
  * Validar o escopo do conteúdo (permitindo apenas as Semanas 1 a 4 para conteúdos práticos).
  * Acionar de forma obrigatória e imediata a ferramenta de documentos sempre que um link, manual ou ferramenta for solicitado.
  * Detectar intenções de encerramento (`fim`, `acabou`, `já concluí`) para encerrar o fluxo com uma mensagem motivacional, omitindo perguntas de engajamento.

### Módulo 3: Ferramenta de Consulta de Documentação (Knowledge Tool)
* **Função:** Conectada aos documentos oficiais (como o Google Docs de links e cronograma), permite que a IA busque referências reais e evite alucinações ao fornecer links de instalação (como n8n, Supabase, Google AI Studio, Make).

### Módulo 4: Chat Response (Resposta ao Usuário)
* **Função:** Envia a resposta final gerada pela IA de volta para a interface de chat da aluna, mantendo a formatação em Markdown estruturada.

---

<img width="808" height="395" alt="image" src="https://github.com/user-attachments/assets/b1b37563-a1a9-4c4c-b85f-36bf0b16eee7" />


## 3. Regras de Negócio e Guardrails Implementados

* **Restrição de Escopo Prático:** Conteúdos a partir da Semana 5 são bloqueados preventivamente com a diretriz de manter o foco nas Semanas 1 a 4.
* **Busca Obrigatória de Links:** O agente possui ordem imperativa para acionar a ferramenta de documentos imediatamente quando solicitadas ferramentas ou manuais, sem solicitar autorizações intermediárias ou relutar.
* **Fluxo de Encerramento Automático:** Caso a usuária utilize termos de finalização, o agente omite as perguntas padrão de engajamento (*"Gostaria de saber mais..."* ou *"Quer treinar seu conhecimento?"*) e foca exclusivamente em uma despedida calorosa e de incentivo.
