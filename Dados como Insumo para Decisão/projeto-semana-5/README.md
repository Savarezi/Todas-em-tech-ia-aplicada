# Projeto Final da Semana 5: Análise de Viabilidade do Trabalho Remoto (Desafio 20)

Este documento apresenta a resolução completa do Desafio 20, aplicando os conceitos de governança de dados, análise de vieses e a pirâmide DIKW para avaliar a transição do trabalho remoto para modelo padrão corporativo.

---

## 📋 Resolução das Tarefas Analíticas

### Tarefa 01: O que os dados DIZEM?
* **Produtividade Quantitativa por Indivíduo:** O grupo remoto registra uma média de 4,2 entregas por pessoa/mês; o híbrido, 3,8; e o presencial, 3,4.
* **Pontualidade nas Entregas:** A taxa de cumprimento de prazos é de 94% no modelo remoto, 92% no híbrido e 86% no presencial.
* **Turnover Anual:** A taxa de rotatividade de funcionários é de 9% no remoto, 12% no híbrido e 18% no presencial.
* **Métricas Apresentadas pela Defesa do Remoto:** A pesquisa de satisfação apresenta um índice 14 pontos maior no modelo remoto, o tempo de deslocamento foi eliminado para este grupo, e o absenteísmo caiu 21%.
* **Argumentos Levantados pelos Gestores:** As equipes remotas possuem maior senioridade média, existem funções operacionais incompatíveis com o trabalho remoto, há uma menor proporção de tarefas presenciais complexas nos projetos remotos, e novos colaboradores relatam maior dificuldade de integração.
* **Limitações Metodológicas Conhecidas:** Não houve randomização na alocação de pessoas entre os modelos de trabalho, a contagem de entregas não avalia qualidade ou inovação, e não existem dados consolidados sobre a colaboração de longo prazo ou o impacto das preferências individuais.
* **Observação vs. Interpretação:** Enquanto os dados brutos mostram superioridade do modelo remoto em volume e pontualidade, a Defesa conclui que o modelo é intrinsecamente eficiente, ao passo que os Gestores inferem que a aparente superioridade decorre de vieses de composição (como maior senioridade e menor complexidade das tarefas).

### Tarefa 02: O que os dados não DIZEM?
* **Falta de Padronização de Funções:** Comparação de médias gerais sem isolar o tipo de cargo ou complexidade das tarefas.
* **Viés de Seleção e Senioridade:** Omissão inicial de que as equipes remotas possuem maior senioridade média, atrelando a produtividade à experiência em vez do modelo.
* **Ausência de Indicadores Qualitativos:** O foco exclusivo em quantidade e prazos ignora a qualidade do entregável, o retrabalho ou a inovação de longo prazo.
* **Falta de Aleatoriedade (Randomização):** Ausência de um experimento controlado com distribuição aleatória de funcionários.
* **Custo-Benefício, Custos Ocultos e Denominadores Ausentes:** Não mensura custos de infraestrutura corporativa versus subsídios de home office, impactos de burnout, isolamento profissional ou o controle real sobre a jornada de trabalho.

### Tarefa 03: Duas perguntas que precisam de MAIS DADOS
1. **Qual é o impacto real da senioridade e do tipo de função na produtividade e na pontualidade, quando controlamos essas variáveis?** *(Requer histórico de desempenho normalizado por nível de senioridade e classificação de tarefas por complexidade).*
2. **Qual é o custo total e o impacto de longo prazo na inovação, no desenvolvimento de novos talentos e na retenção da cultura organizacional?** *(Requer métricas de qualidade/retrabalho, curva de aprendizado de novos funcionários em 12 meses e custo operacional consolidado).*

### Tarefa 04: Você tomaria a decisão? (Veredito)
* **Decisão:** **Eu não tomaria a decisão (Ainda não / Reprovado para adoção universal imediata).**
* **Justificativa:** Há insuficiência de evidências causais e presença forte de vieses de composição/senioridade. Adotar o modelo universalmente sem um piloto controlado ignora riscos sobre a qualidade, inovação, sustentabilidade da cultura e integração de novos colaboradores.

### Tarefa 05: Prompt do Agente de IA
O projeto estruturou um prompt voltado para um Cientista de Dados Sênior e Especialista em People Analytics, sob diretrizes rígidas de **proibição de dados fictícios** (exigindo resposta obrigatória *"Dado indisponível no cenário atual"* para lacunas) e estruturação de saída em Matriz de Riscos, Parecer Executivo e Nível de Confiança.

### Tarefa 06: Gráficos Analíticos
* **Gráfico 1:** Produtividade vs. Pontualidade por Modelo de Trabalho (Colunas Agrupadas / Eixos Duplos comparando Entregas e % de Pontualidade). Risco de interpretação errada: induzir um aumento linear de produtividade ignorando o viés de senioridade.
* **Gráfico 2:** Taxa de Turnover Corporativo vs. Satisfação por Modelo (Linhas com Múltiplas Séries). Risco de interpretação errada: assumir que a satisfação declarada traduz-se automaticamente em qualidade técnica de longo prazo.

### Tarefa 07: Mini Base de Dados Transacional
Estruturação de colunas, tipos de dados, frequências e fontes prováveis para unificar o controle de entregas individuais, senioridade, retrabalho e modalidade de trabalho.

### Tarefa 08: Camadas DIKW Aplicadas ao Cenário
* **Dado:** Registros numéricos brutos (ex: 4,2 entregas no remoto; 18% de turnover presencial).
* **Informação:** Relatório estruturado cruzando as métricas comparativas de desempenho e rotatividade.
* **Conhecimento:** Compreensão analítica de que a vantagem do remoto esconde vieses de senioridade e barreiras de integração para novos funcionários.
* **Sabedoria:** Decisão estratégica de condicionar a expansão a um piloto controlado com randomização de faixas de senioridade e métricas de qualidade.

---

## 🔗 Links e Acessos Oficiais do Projeto

* 📄 **Documentação Completa da Entrega:** [Google Docs](https://docs.google.com/document/d/1wkMveYLd02v_06WnSSLA_hb5xZVJD6xNGb_XL1R1QtQ/edit?usp=sharing)
* 📊 **Tabela Consolidada (Dados Oficiais):** [Google Sheets](https://docs.google.com/spreadsheets/d/1d3PFma4Ot1YAtuW0S-m7b5ummvThL-SoKYDeEqNHISE/edit?usp=sharing)
* 🗄️ **Base de Dados Transacional:** [Google Sheets (Base Completa)](https://docs.google.com/spreadsheets/d/1sAjrPXhMkM1yofOhINBG8c8lBpIjSkiPxBgYO9DDu3s/edit?usp=sharing) 
* 🐍 **Análise Estatística (Script Python):** [Google Colab](https://colab.research.google.com/drive/1P4_2vM2Wtf1lJltcUqxpGt_xrmuGM9R1?usp=sharing)
* 💻 **Dashboard Executivo Interativo:** [Dashboard](https://painel-executivo-de-pessoas-viabilidade-do-trabal-700125729949.us-east1.run.app/)
