# Projeto Prático: Análise Geoespacial iFood — Concentração de Clientes e Renda

Este projeto foi desenvolvido como entregável final da **Semana 8: Dados Avançado — De Bruto a Insight** da formação **Todas em Tech Futuro+ IA** (Reprograma / FIAP). O objetivo consistiu em analisar a base de dados de pedidos de delivery online em Bangalore (Índia), aplicando um recorte temático focado em **Geografia e Inteligência Espacial**.

---

## 🎯 Escopo do Projeto e Desafio
* **Tema do Grupo:** Investigação da concentração geográfica de clientes fiéis (*Frequent*), correlação espacial com renda, raio de dispersão de pedidos e mapeamento de feedbacks negativos.
* **Abordagem Analítica:** Substituição de gráficos de barras tradicionais por geovisualizações (mapas de calor, clusters espaciais e análise de raio de alcance).

---

## 🧹 Tratamento e Limpeza da Base de Dados
1. **Remoção de Duplicatas e Auditoria:** Validação e limpeza de linhas duplicadas para garantir precisão nas coordenadas geográficas de 388 registros.
2. **Eliminação de Coluna Fantasma:** Exclusão definitiva da coluna `Unnamed: 13` (cópia residual exata da coluna `Output`).
3. **Correção de Latitude Corrompida:** Tratamento de 228 registros em formatos de data inválida e 160 em números inteiros corrompidos via rotina de parsing, restaurando o tipo numérico correto.
4. **Enriquecimento Geoespacial (Coluna L):** Mapeamento dos códigos postais (*Pin codes* da série 560xxx) para identificar bairros e polos urbanos consolidados de Bangalore (como *Indiranagar*, *Koramangala* e *Whitefield*).

---

## 📍 Principais Achados e Respostas Analíticas

1. **Concentração de Clientes Fiéis (*Frequent*):** Polos consolidados e bairros residenciais específicos concentram a maior proporção de clientes fiéis, enquanto áreas de transição concentram perfis novos ou regulares.
2. **Correlação com Renda (*Monthly Income*):** Regiões centrais e hubs tecnológicos concentram faixas salariais mais elevadas, ao passo que zonas acadêmicas registram alta densidade de clientes sem renda própria (estudantes).
3. **Raio de Alcance:** O mapeamento a partir dos pontos centrais definiu o limite geográfico de tolerância de distância dos consumidores.
4. **Distribuição de Feedbacks Negativos:** A geolocalização de insatisfações permitiu isolar potenciais gargalos logísticos e de atendimento por praça.

---

## 🎯 Recomendações Estratégicas

* **👤 Persona A (Operação & Logística):** Otimização e realocação de frotas e entregadores em anéis concêntricos de alta densidade nos horários de pico; monitoramento preventivo de zonas com maior incidência de feedbacks negativos.
* **🏢 Persona B (Mercado & Negócio):** Criação de programas de fidelidade hiper-segmentados para os clientes *Frequent* de alta renda e campanhas direcionadas de aquisição para o público universitário em zonas periféricas.

---
*Projeto desenvolvido em grupo no âmbito do programa Todas em Tech Futuro+ IA.*
