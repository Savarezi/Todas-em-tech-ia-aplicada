
# 🤖 Projeto Prático: Agente Virtual Interno para Colaboradores

Desenvolvido como o projeto final da **Semana 10** (*Modelagem de Negócio + Precificação*) do programa **Todas em Tech Futuro+** .

---

## 🎯 Sobre o Projeto
O **Agente Virtual Interno** é um protótipo de automação inteligente via interface de chat projetado para fornecer autonomia, agilidade e padronização no acesso a informações funcionais dos colaboradores, reduzindo a necessidade de atendimento humano para consultas rotineiras e operacionais.

---

## 📂 Fonte de Dados e Escopo
* **Base de Dados Fictícia:** `base_colaboradores_agente_virtual.xlsx` (contendo identificadores, nome, matrícula, CPF fictício, e-mail corporativo, data de admissão e cargo).
* **Consultas Permitidas:** 
  * Identificação por CPF ou Matrícula.
  * Consulta de dados cadastrais/funcionais (e-mail, matrícula, cargo).
  * Cálculo dinâmico de tempo de empresa (anos, meses e dias).
  * Regras de elegibilidade e solicitação de férias (antecipação de 45 dias, restrições nas duas primeiras semanas do mês, abono pecuniário e antecipação de 13º)[cite: 109, 110].
  * Controle de período de treinamento inicial de 3 meses.

---

## 🛡️ Governança e Restrições Críticas
* **Segurança e Privacidade:** A identificação do colaborador via CPF ou matrícula é obrigatória antes de qualquer fornecimento de dados funcionais individuais[cite: 108].
* **Princípio de Não Invenção:** O agente trabalha estritamente com os dados disponíveis na base oficial e regras documentadas, respondendo explicitamente quando uma informação não estiver disponível.
* **Escopo e Limitações:** Assuntos administrativos complexos ou fora do escopo (como alteração de dados cadastrais ou redefinição de senhas) utilizam a resposta padrão obrigatória: *"Este assunto eu ainda não estou autorizado a falar."*

---

## 📋 Documentação Técnica do Projeto
O escopo completo, fluxos de decisão e as regras de negócio detalhadas deste protótipo estão versionados nesta pasta para validação e testes de conformidade.
