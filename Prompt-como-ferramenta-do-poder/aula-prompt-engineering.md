# Aula de Prompt Engineering & Inteligência Artificial

## O que é IA?
Inteligência Artificial (IA) é um ramo da ciência da computação que se dedica a criar sistemas, softwares ou máquinas capazes de simular a inteligência humana para resolver problemas, tomar decisões, aprender e realizar tarefas de forma autônoma.
Diferente de um programa tradicional — que executa apenas regras rígidas e programadas manualmente —, a IA utiliza grandes volumes de dados e algoritmos avançados para reconhecer padrões, fazer previsões e se adaptar a novas situações.

### Principais Conceitos Relacionados
* **Machine Learning (Aprendizado de Máquina):** Vertente em que os sistemas aprendem com os dados ao longo do tempo, sem programação explícita para cada tarefa.
* **Deep Learning (Aprendizado Profundo):** Técnica avançada baseada em redes neurais artificiais inspiradas no cérebro humano, ideal para dados complexos (imagens, sons e textos).
* **Processamento de Linguagem Natural (PLN):** Área que permite aos computadores entenderem, interpretarem e gerarem a linguagem humana.
* **IA Generativa:** Sistemas capazes de criar conteúdos novos e originais (textos, imagens, códigos, áudios e vídeos) a partir de comandos (prompts).

---

## Estrutura PAPO
Para delegar bem uma tarefa para a IA, utilize a estrutura:
* **P**ersonagem (quem a IA deve ser, ex: especialista em dados).
* **A**ção (o que exatamente ela deve fazer).
* **P**adrão (formato da resposta, ex: lista, tabela, curto).
* **O**bjetivo (qual o resultado esperado).

---

## Harness Engineering
Engenharia de harness refere-se ao design de toda a infraestrutura — sistemas, restrições, ferramentas e loops de feedback — que envolve um modelo de IA para torná-lo confiável, seguro e produtivo em ambientes de produção.

* **Conceito básico:** `Agent = Model + Harness` (O modelo é o motor potente; o harness são as rédeas, sela e cabresto que canalizam a força de forma útil).
* **Pilares:**
  1. *Orquestração de Ferramentas (Tool Orchestration):* Acesso controlado a bancos de dados, terminais e APIs.
  2. *Guardrails e Restrições de Segurança:* Regras determinísticas para evitar ações destrutivas.
  3. *Recuperação de Erros e Loops de Feedback:* Mecanismos de correção baseados em testes e mensagens de erro.
  4. *Observabilidade:* Monitoramento de ações, custos de tokens e pontos de decisão.
  5. *Pontos de Checagem Humanos (Human-in-the-Loop):* Aprovação obrigatória em ações de alto impacto.

---

## Técnicas de Prompt Engineering

1. **Zero-shot:** Enviar um comando diretamente para a IA sem fornecer exemplos, confiando apenas no conhecimento prévio do modelo.
2. **Few-shot:** Fornecer exemplos práticos de entrada e saída antes da solicitação principal para ensinar tom, estilo ou lógica esperada.
3. **ReAct (Reasoning and Acting):** Técnica em que o modelo intercala raciocínio lógico com ações práticas para resolver problemas complexos passo a passo.
4. **RAG (Retrieval-Augmented Generation):** Conecta a IA a uma base de dados externa ou documentos privados para buscar informações precisas, reduzindo alucinações.
