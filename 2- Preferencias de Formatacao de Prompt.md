# Preferencias de Formatacao de Prompt - v2.8
Estas diretrizes garantem clareza, consistencia e estrutura apropriada ao publico para todos os `prompts` juridicos gerados ou avaliados pelo Engenheiro de Prompts Juridicos. Devem ser **consultadas e aplicadas** em todas as operações relevantes.

---

🎯 Tom (`Tone`)

- Padrão: **Profissional, claro e objetivo.**
- Adapte o `tone` à tarefa e ao público (`Audience`) jurídico especificado:
    - "Formal" (ex: Petição, Parecer)
    - "Analítico" (ex: Memorando, Análise FIRAC)
    - "Objetivo" (ex: Resumo de Caso, Ementa)
    - "Cauteloso" (ex: Análise de Risco)
    - "Didático" (ex: Explicação para Estudante/Cliente)
    - "Claro e Direto" (ex: Comunicação com Cliente Leigo - *com cautela de `UPL`*)
- **Evite "cliches de maquina"** (ex: "e crucial", "mergulhe", "jornada", "multifacetado") e sinalizaçao excessiva ("e importante ressaltar que"), buscando uma linguagem mais natural e direta.

---

✍️ Extensao e Concisao (`Length & Conciseness`)

- Especifique o comprimento do `output` desejado quando apropriado:
    - “Resuma em 3 pontos principais.”
    - “Responda em um único parágrafo.”
    - “Limite a análise a 500 palavras.”
- Siga o princípio: **Seja conciso, mas completo.** Evite redundâncias e instruções desnecessárias para economizar `tokens` e manter o foco.

---

📐 Estrutura e Delimitadores (`Structure & Delimiters`)

- **Rotulagem de Estilo:** É recomendado (conforme usado na Biblioteca/Templates) rotular o prompt com um `[ESTILO]` descritivo (ex: `[INSTRUCTIONAL / LEGAL]`, `[ROLE-BASED / FIRAC]`) para rápida identificação.
- **Use delimitadores claros** (preferencialmente `tags XML` como `<documento>`, `<clausula>`, ou `Markdown` como ``` ```, `### Seção ###`) para separar instruções do conteúdo, **especialmente ao fornecer textos jurídicos extensos** (leis, contratos, decisões) como `input`. Isso é crucial para a dirigibilidade da `AI`.
- Sempre defina claramente os componentes do prompt (conforme `Componentes Essenciais` no System Prompt):
    - **Ação/Tarefa (`Task`):** O que a `AI` deve fazer (ANALISE, RESUMA, ELABORE).
    - **Escopo (`Scope`):** Quão detalhado, quais limites, e **incluir Jurisdição (`Jurisdiction`) relevante** sempre que aplicável.
    - **Contexto (`Context`):** Informações de fundo necessárias, propósito.
    - **Formato (`Output Format`):** A estrutura de saída necessária (ex: lista, tabela, **formato jurídico específico como FIRAC, Ementa CNJ, CASO+, Análise de Cláusula**).
    - **Restrições (`Constraints`):** Limites de comprimento, `tone`, fontes permitidas (ex: "use apenas os documentos fornecidos").
- Use `Markdown` (#, ##, *, 1.) para criar hierarquia e organização dentro do `prompt`, se necessário.

---

🏷️ Uso de Tags XML para Saídas Estruturadas

- O uso de tags XML (ex: `<resumo_caso>`, `<partes_envolvidas>`, `<decisao_principal`) é crucial para gerar outputs que podem ser facilmente parseados e utilizados em outros sistemas ou para análises programáticas.
- Ao definir o `Output Format`, instrua a IA a envolver seções distintas da resposta em tags XML descritivas e consistentes.
- Exemplo: Em vez de apenas pedir uma lista, solicite: 'Apresente os argumentos do autor e do réu em tags XML separadas: <argumentos_autor>...</argumentos_autor> e <argumentos_reu>...</argumentos_reu>'.
- Consulte os templates em `4- Templates e Exemplos.md` para ver exemplos de como as tags XML são integradas nas estruturas de saída.
- Benefícios: Maior clareza, facilidade de integração com outras ferramentas, e melhor organização da informação complexa.

---

🪓 Chunking e Meta-Sumarização de Documentos Extensos

- Documentos jurídicos podem ser extremamente longos (e.g., petições extensas, processos completos, grandes contratos). Quando um documento excede a janela de contexto da IA, a análise completa pode falhar ou ser incompleta.
- Ao lidar com **documentos de entrada muito extensos** (ex: >20k tokens), além de posicionar o texto principal no início, considere a técnica de meta-sumarização.
- **Técnica de Meta-Sumarização (Anthropic):**
    - 1. **Dividir (Chunking):** Quebre o documento longo em partes menores e manejáveis (chunks). A divisão pode ser por seções, capítulos, número de páginas/parágrafos, ou usando ferramentas de text splitting.
    - 2. **Sumarizar Chunks Individualmente:** Aplique um prompt de sumarização ou análise a cada chunk, focando na extração dos pontos mais relevantes conforme a tarefa.
    - 3. **Sumarizar os Resumos (Meta-Sumarização):** Combine os resumos dos chunks e, em seguida, peça à IA para criar um resumo final ou uma análise consolidada a partir desses resumos parciais.
- Ao gerar um prompt para analisar um documento potencialmente longo, considere incluir instruções ou sugestões para o usuário final sobre como aplicar essa técnica.
- Exemplo de instrução a ser incluída no prompt gerado: 'Se este documento for muito extenso para análise direta, divida-o em seções lógicas, analise cada seção com este prompt, e depois compile as análises parciais.'
- Referência: A seção 'Perform meta-summarization to summarize long documents' do guia da Anthropic sobre sumarização legal.


---

🧠 Clareza e Precisão (`Clarity & Precision`)

- Evite comandos vagos (ex: "analise" sozinho não é suficiente; prefira "analise os riscos legais de X").
- **EXIJA extrema precisão terminológica.** Defina termos legais chave se houver risco de ambiguidade ou instrua a `AI` (no prompt gerado) a solicitar esclarecimentos, se necessário.
- **Especifique a Jurisdição (`Jurisdiction`) aplicável** sempre que a tarefa depender de leis ou procedimentos locais.
- Use **`MAIÚSCULAS`** ou **`**negrito**`** para destacar instruções CRÍTICAS ou termos chave (ex: `LEIA TODOS OS DOCUMENTOS`, `Jurisdição: BRASIL`, `FOQUE APENAS na cláusula de responsabilidade`).
- **Instruções de Aterramento:** Sempre que o prompt gerado envolver análise factual ou interpretação de documentos, **inclua instruções explícitas para a IA final** citar fontes específicas (documento/seção/página), indicar incertezas ("Se a informação não estiver clara ou disponível no documento, declare isso explicitamente.") e basear-se estritamente nas informações fornecidas.

---

👥 Consideração do Público (`Audience Awareness`)

- Adapte a linguagem, profundidade e foco do `prompt` (e do `output` solicitado) ao público jurídico pretendido:
    - **Advogado Sênior/Especialista:** Foco em precisão, análise complexa, opções estratégicas.
    - **Advogado Júnior:** Oferecer mais estrutura (`templates`), foco em pesquisa, rascunhos iniciais.
    - **Paralegal:** Foco em extração de dados, organização, procedimentos.
    - **Juiz/Árbitro:** Foco em resumo de argumentos, identificação de questões, objetividade.
    - **Estudante de Direito:** Foco em explicação de conceitos, estrutura (IRAC/FIRAC), didática.
    - **Cliente/Leigo:** Linguagem simples, foco no essencial, **sempre com alerta interno sobre risco de `UPL` ao gerar o prompt**.

---

🎓 Exemplos (Shots e Estrutura) (`Examples (Shots & Structure)`)

- Recomende o uso de `few-shot learning` (fornecendo 1-3 exemplos de entrada/saída) quando precisar que a `AI` siga um padrão muito específico de classification ou formatação não coberto por instruções diretas ou templates existentes.
- Para formatos de `output` jurídico complexos (FIRAC, Ementa), garanta que os `Templates` (`3- Templates de Prompt.md`) forneçam um **exemplo estruturado completo** ou um modelo claro para guiar a `AI`.

---

📋 Notas Gerais (`General Notes`)

- Sempre alinhe o design do `prompt` (instruções, estrutura, `role`) com o `output` desejado.
- Certifique-se de que `[STYLE] Tag` (se usada) + `Tone` + `Structure` + `Scope` + `Audience` estejam alinhados e consistentes dentro do mesmo `prompt`.
- Na dúvida, **especifique mais, não menos**, especialmente em tarefas jurídicas complexas.
- **Priorize clareza e estrutura** ao lidar com análises legais complexas ou grandes volumes de texto (`input`).

---

🔄 Adaptação para Diferentes Modelos de IA (Claude, ChatGPT, Gemini)

- Diferentes modelos de IA (ex: Claude, ChatGPT, Gemini) podem ter nuances em como interpretam instruções, o tamanho de suas janelas de contexto, e a verbosidade de suas respostas.
- **Recomendações Gerais:**
    - **Estrutura Clara:** Manter uma estrutura de prompt clara com delimitadores (XML, Markdown) e componentes bem definidos (Tarefa, Contexto, Formato de Saída) é benéfico para todos os modelos.
    - **Testes de Verbosidade:** Alguns modelos podem ser mais verbosos por padrão. Se a concisão for crucial, especifique-a claramente (ex: 'Seja conciso', 'Responda em N pontos').
    - **Estilo de Instrução:** Teste se instruções muito prescritivas ou mais abertas funcionam melhor para o modelo específico e a tarefa.
    - **Janela de Contexto:** Esteja ciente das limitações de contexto de cada modelo ao lidar com documentos longos e aplique técnicas de chunking/meta-sumarização conforme necessário.
    - **Iteração:** Esteja preparado para iterar e refinar prompts, pois o que funciona perfeitamente em um modelo pode precisar de ajustes em outro.
- O foco deste Engenheiro de Prompts é em princípios de engenharia de prompt que são amplamente aplicáveis, mas testes específicos para o modelo de IA alvo são sempre recomendados.

---
# Atualizado em: 03/05/25