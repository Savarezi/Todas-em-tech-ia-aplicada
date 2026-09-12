# Análise de Conteúdo Netflix: Um Estudo com 8.807 Títulos

Este projeto foi desenvolvido como parte da **Semana 6: Comunicação + Narrativa Potencializada** da formação **Todas em Tech Futuro+ IA** (Reprograma / FIAP). O objetivo foi aplicar técnicas avançadas de *Storytelling com Dados*, tradução de bases, mapeamento de perguntas de negócio e seleção dos gráficos corretos para estruturar uma análise executiva sobre o catálogo da Netflix.

---

## 📊 Escolha e Tratamento da Base de Dados
* **Base utilizada:** `netflix_titles.csv` (Kaggle).
* **Volume validado:** 8.807 linhas e 12 colunas.
* **Período de lançamento:** 1925 a 2021.
* **Período de adição à plataforma:** 01/01/2008 a 25/09/2021.
* **Ferramentas:** Google Docs (documentação), Claude (tradução de colunas e suporte analítico) e Kaggle.

### Processo de Tradução e Adequação (De-Para):
* `show_id` -> `id`
* `type` -> `tipo`
* `title` -> `titulo`
* `director` -> `diretor`
* `cast` -> `elenco`
* `country` -> `pais`
* `date_added` -> `data_adicao`
* `release_year` -> `ano_lancamento`
* `rating` -> `classificacao`
* `duration` -> `duracao`
* `listed_in` -> `genero`
* `descricao` -> `descricao`

*(Destaque: O país líder em produção é **United States (Estados Unidos)**, contabilizando 2.818 títulos como país principal).*

---

## 🎯 Mapeamento de Dados ao Gráfico Certo

O projeto foi estruturado respondendo a 4 perguntas fundamentais de negócio, classificando cada uma e selecionando a visualização ideal:

1. **A Netflix tem mais Filmes ou Séries?**
   * **Classificação:** Comparar / Compor.
   * **Gráfico Escolhido:** Gráfico de Donut com porcentagem (ideal para exibir a proporção entre 2 categorias).
   * **Insights:** A grande maioria do catálogo é composta por **Filmes** (6.131 títulos, 69,6%), enquanto as **Séries** totalizam 2.676 títulos (30,4%). Há mais que o dobro de filmes em relação a séries.
  
     <img width="320" height="344" alt="image" src="https://github.com/user-attachments/assets/4b1f0121-b97f-4e6f-b464-1fc929d4fc08" />

---
 2. **Quais são os gêneros mais populares?**
   * **Classificação:** Distribuir / Compor.
   * **Gráfico Escolhido:** Gráfico de Barra Horizontal (Top 10).
   * **Insights:** *Filmes Internacionais* lideram com 2.752 títulos, seguidos de perto por *Dramas* (2.427 títulos) e *Comédias* (1.674 títulos). As *Séries Internacionais* também possuem forte presença (1.351).
  
   <img width="460" height="343" alt="image" src="https://github.com/user-attachments/assets/07b25934-83ce-4273-afb0-81e770e57047" />

---
 4. **Como cresceu a quantidade de títulos ao longo dos anos?**
   * **Classificação:** Tendência no tempo.
   * **Gráfico Escolhido:** Gráfico de Linha (evidenciando a adição de conteúdos de 2008 a 2021).
   * **Insights:** O estudo apontou um forte **auge de expansão global entre 2018 e 2020**, registrando seu pico histórico em **2019**.
  
   <img width="458" height="333" alt="image" src="https://github.com/user-attachments/assets/e0244185-432c-4c54-99a4-f690c7c484ed" />

---
 6. **Quais países mais produzem?**
   * **Classificação:** Comparar categorias.
   * **Gráfico Escolhido:** Gráfico de Barra Horizontal (Top 10) com destaque para os Estados Unidos.
   * **Insights:** Os Estados Unidos lideram isoladamente o ranking de produção principal com 2.818 títulos catalogados.
  
     <img width="325" height="326" alt="image" src="https://github.com/user-attachments/assets/a67576d7-73d1-46c3-bc1c-10f5ad17193a" />

---
>>## 🚀 Projeto Prático: Análise de Conteúdo Netflix
Aplicando os conceitos da semana em uma base de 8.807 títulos validados:
* **🔗 [Acesse o Dashboard Interativo do Projeto Aqui](https://dashboard-netflix-nu.vercel.app/)**
* **📄 [Acesse a Documentação Completa (Google Docs)](https://docs.google.com/document/d/1lhdr9HoYjmS8nCDcvdNW18gHa7LmgIlfqhthQEGqKok/edit?usp=sharinghttps://docs.google.com/document/d/1lhdr9HoYjmS8nCDcvdNW18gHa7LmgIlfqhthQEGqKok/edit?usp=sharing)**

---
*Projeto documentado por Patrícia Oliveira no âmbito do programa Todas em Tech Futuro+ IA.*
