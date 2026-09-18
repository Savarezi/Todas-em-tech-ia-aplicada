# Projeto Prático: RAG Ops — Notificações e Relatórios

Este projeto foi desenvolvido como parte da **Semana 7: Visão Estratégica — Selecionando o Problema Certo** da formação **Todas em Tech Futuro+ IA** (Reprograma / FIAP). O objetivo foi aplicar os conceitos de visão estratégica, auditoria de tarefas, validação de hipóteses e escolha do nível tecnológico ideal (**RAG**), criando um ambiente de design e teste para o envio automatizado de e-mails de notificação, relatórios gerenciais e avisos de status.

---

## 🎯 Definição Estratégica do Problema
* **O Problema Selecionado:** A necessidade de automatizar a geração e o envio de relatórios e notificações operacionais sem correr riscos de alucinação ou perda de contexto em dados sensíveis.
* **Justificativa Tecnológica (Por que RAG?):** Um prompt simples não resolveria pois a IA precisa consultar bases de dados e documentos específicos da operação em tempo real. Um agente completo seria complexo demais para a demanda atual. O **RAG (Retrieval-Augmented Generation)** garante precisão ao buscar o contexto correto antes de gerar a resposta.

---

## 🛠️ Entregáveis e Links do Projeto
* **🔗 [Acesse o Projeto / Chat no Claude](https://claude.ai/share/aa3b704a-12ee-44c8-8a9d-6e156caf7871)**
* **📊 [Acesse a Planilha de Estruturação e Dados](https://docs.google.com/spreadsheets/d/1D_Ux5PPpS2x0pRIkGV0tdT1G9BmHIQqDBkoV8T3NAEk/edit?usp=sharing)**
* **📝 [Acesse a Documentação Completa no Notion](https://app.notion.com/p/Task-Audit-IA-Ops-Refinamento-de-System-Prompts-3dc7e4dfc6f1800bb374f1e169e63541)**

---

## 🤖 Engenharia de Instruções (Prompt System) do Projeto
O sistema foi configurado no Claude utilizando as diretrizes de comportamento sênior para arquitetura de automação e RAG:

> **Papel:** Você é um Arquiteto de Automação e Especialista em RAG (Retrieval-Augmented Generation), focado em projetar sistemas inteligentes para envio automatizado de e-mails de notificação, relatórios operacionais e avisos de status.
> 
> **Diretrizes de Comportamento:**
> 1. Atue sempre com postura sênior, técnica e voltada para eficiência de arquitetura de dados e integração.
> 2. Ao estruturar soluções de RAG para e-mails, foque na recuperação precisa de contexto (bases de conhecimento/documentos), formatação limpa (HTML/Markdown) e segurança contra alucinações em dados sensíveis.
> 3. Responda de forma estruturada, utilizando blocos lógicos, fluxos passo a passo e critérios de validação claros.

---
*Projeto estruturado por Patrícia Oliveira no âmbito do programa Todas em Tech Futuro+ IA.*
