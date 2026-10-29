# 🚀 Ele Agenda — Agente IA de Agendamento Autônomo

Projeto prático desenvolvido para o desafio final da **Semana 13** (*Agentic AI, RAG e Automação Avançada*) do programa **Todas em Tech Futuro+** .

---

## 📌 Sobre o Projeto
O **Ele Agenda** é um assistente virtual autônomo projetado para gerenciar o ciclo completo de atendimento, apresentação de catálogo e agendamento de serviços de consultoria, auditoria e tecnologia. O agente atende mais de 80 serviços catalogados, valida 20 regras comerciais e executa integrações diretas com o ecossistema Google.

---

## 🛠️ Arquitetura e Integrações
- **Base de Conhecimento:** Google Sheets (`serviços` e `regra de atendimento`).
- **Gestão de Agenda:** Google Calendar API (verificação de disponibilidade e criação de reuniões com Google Meet).
- **Documentação Automática:** Geração de comprovante em formato Word (`.docx`) salvo no Google Drive.
- **Comunicação:** Gmail com disparo de e-mail formatado em HTML/CSS inline responsivo com o arquivo `.docx` anexado.

---

## 📄 Arquivos do Projeto nesta Pasta
- `instrucoes_agente.md`: System Prompt completo e diretrizes do agente.
- `documentacao_tecnica.md`: Especificações arquiteturais, regras de negócio e fluxo detalhado de 5 passos.
- `pitch_slides.md`: Roteiro executivo e estrutura de slides da apresentação.
