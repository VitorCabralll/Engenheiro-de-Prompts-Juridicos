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
- Ao lidar com **documentos de entrada muito extensos** (ex: >20k tokens), considere instruir o prompt gerado a posicionar o texto principal no início, antes das instruções detalhadas, e, opcionalmente, solicitar extração prévia de citações relevantes para otimizar o processamento de 'long context'.

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
# Atualizado em: 03/05/25