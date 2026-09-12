# Validação de Gráficos e Sugestões com IA

Este arquivo documenta o prompt utilizado com inteligência artificial para validar a escolha dos gráficos, verificar o alinhamento com as perguntas de negócio e refinar a visualização do projeto de análise da Netflix.

---

## 🤖 Prompt Utilizado

> Valide minhas escolhas de gráficos para o meu dashboard da Netflix e sugira melhorias. Sou leigo, então explique de forma simples.
> 
> Base de dados: netflix_titles.csv com 8.807 títulos. Período validado: ano_lancamento de 1925 a 2021 e data_adicao de 01/01/2008 a 25/09/2021.
> 
> Minhas escolhas foram:
> Pergunta 1: A Netflix tem mais Filmes ou Séries? Tipo: Comparar - Gráfico escolhido: Gráfico de Pizza / Donut
> Pergunta 2: Quais são os gêneros mais populares? Tipo: Distribuir / Compor - Gráfico escolhido: Gráfico de Barra Horizontal Top 10
> Pergunta 3: Como cresceu a quantidade de títulos ao longo dos anos? Tipo: Tendência - Gráfico escolhido: Gráfico de Linha
> Pergunta 4: Quais países mais produzem conteúdo? (United States = Estados Unidos com 2.818 títulos) Tipo: Comparar - Gráfico escolhido: Gráfico de Barra Horizontal Top 10
> 
> Me diga:
> 1. Se minhas escolhas estão corretas
> 2. O que posso melhorar
> 3. Se tem algum gráfico melhor que esse para leigos

---

## ✅ Resultado da Validação da IA

A IA avaliou e validou todas as 4 escolhas como **corretas e altamente adequadas** para facilitar a leitura de um público leigo.

### 💡 Melhorias Sugeridas e Implementadas
1. **Foco Temporal:** Utilização da coluna `data_adicao` (01/01/2008 a 25/09/2021) no gráfico de tendência para refletir o ritmo real de expansão da plataforma.
2. **Padronização Linguística:** Tradução oficial da categoria de *United States* para *Estados Unidos* na base e nos eixos, mantendo a consistência em português.
3. **Identidade Visual:** Aplicação de títulos orientados a conclusão e sugestão de uso de identidade visual limpa inspirada na paleta da plataforma.
4. **Filtro de Relevância:** Manutenção do padrão Top 10 para gêneros e países, evitando a poluição visual decorrente da alta granularidade de registros brutos.

---
*Documentação de engenharia de prompt e refinamento técnico por Patrícia Oliveira.*
