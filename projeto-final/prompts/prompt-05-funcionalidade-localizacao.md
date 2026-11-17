# PROMPT 05 — IMPLEMENTAÇÃO DA FUNCIONALIDADE DE LOCALIZAÇÃO

Quero implementar uma nova funcionalidade de localização no aplicativo Garimpo Delas para que as usuárias visualizem a região onde os itens estão disponíveis para retirada.

### 1. Atualização do Cadastro
Adicionar os campos obrigatórios: CEP, Bairro, Cidade, Estado e Local de retirada/ponto de encontro.

### 2. Tratamento das 10 Usuárias Já Cadastradas
* Nenhuma conta poderá ser excluída ou recriada.
* No primeiro acesso após a atualização, exibir um modal solicitando a complementação da localização (*"Vamos atualizar sua localização! 💜"*).
* Permitir atualizar o cadastro existente sem duplicar contas.

### 3. Ícone de Localização na Seção Garimpar
* Adicionar um ícone de mapa (pin) em cada card de publicação.
* Ao clicar, abrir um modal integrado exibindo um mapa do Google Maps com a localização aproximada de retirada.
* Proteger a privacidade: não exibir publicamente o endereço residencial completo.
