# Documentação Técnica — Ele Agenda

## 1. Visão Geral
O **Ele Agenda** é uma solução de inteligência artificial autônoma projetada para gerenciar a jornada completa de atendimento, consulta de serviços e agendamento de horários para empresas de consultoria, auditoria e tecnologia.

---

## 2. Base de Conhecimento
- **Aba `serviços`:** Catálogo descritivo com 80 ofertas (nome, duração, valor, descrição e pré-requisitos).
- **Aba `regra de atendimento`:** 20 parâmetros e políticas comerciais (horários de funcionamento, limites de antecedência, prazos de cancelamento, políticas de atraso e formas de pagamento).

---

## 3. Arquitetura de Integrações
- **Google Calendar:** Checagem de disponibilidade em tempo real, criação do evento e geração do link de conferência no Google Meet.
- **Google Drive / Word (.docx):** Automação na criação e armazenamento do comprovante formal do agendamento.
- **Gmail:** Disparo automatizado de e-mail em HTML responsivo com card de resumo e comprovante anexado.

---

## 4. Regras Invioláveis de Negócio
- **Validação Estrita:** Proibido agendar fora dos parâmetros da aba `regra de atendimento`.
- **Integridade de Documentos:** Não disparar e-mails sem o comprovante `.docx` devidamente gerado e anexado.
- **Transparência:** Apresentação clara dos valores, políticas de reagendamento e formas de pagamento aceitas antes da confirmação final.
