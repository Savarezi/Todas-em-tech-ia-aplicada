# Registro de Prompts — Engenharia de Dados & Limpeza

Prompt sênior em Python (Pandas) utilizado para a estruturação, tratamento de coordenadas corrompidas e limpeza do dataset de pedidos de delivery online do iFood.

```text
Atue como um Engenheiro de Dados Sênior e Especialista em Python (Pandas). 

Anexe a esta conversa o arquivo Excel do projeto (`dataset_projeto_semana8_Conjuto-de-dados-de-pedido-de-comida-online.xlsx`). Preciso que você execute um script em Python para realizar a limpeza, o tratamento e a normalização dessa base de dados, seguindo rigorosamente estas três diretrizes:

1. REMOÇÃO DE COLUNA FANTASMAS/REDUNDANTES:
   - Identifique e exclua permanentemente a coluna "Unnamed: 13", pois ela é uma duplicata exata e residual da coluna "Output".

2. CORREÇÃO DA COLUNA DE LATITUDE CORROMPIDA:
   - A coluna "latitude" veio corrompida do arquivo original, contendo uma mistura de números inteiros incorretos e datas inválidas geradas pelo Excel (ex: valores como "9766-12-01 00:00:00" e "12977").
   - Desenvolva uma rotina de parsing/limpeza robusta para extrair, converter e normalizar os valores da latitude para o formato numérico padrão (ponto flutuante correto), garantindo a integridade geográfica para cruzamento com a "longitude" e o "Pin code".

3. VALIDAÇÃO E EXPORTAÇÃO:
   - Verifique se restou algum valor nulo ou anomalia nas demais colunas (demográficas, geográficas e de feedback).
   - Ao finalizar o tratamento, gere e me disponibilize o link para download de uma nova versão limpa da planilha (em formato .xlsx ou .csv) pronta para uso acadêmico e analítico.
