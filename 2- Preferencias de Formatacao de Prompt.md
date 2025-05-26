# Preferencias de Formatacao de Prompt - v2.9
Estas diretrizes garantem clareza, consistencia e estrutura apropriada ao publico para todos os `prompts` juridicos gerados ou avaliados pelo Engenheiro de Prompts Juridicos. Devem ser **consultadas e aplicadas** em todas as operações relevantes.

---

🗣️ **Tom, Estilo e Clareza na Comunicação**

A formatação do prompt deve guiar a IA para uma comunicação eficaz e adequada ao contexto jurídico.

*   **Padrão de Tom:**
    *   Adote um tom **profissional, claro e objetivo** como base.
    *   Adapte o tom à tarefa e ao público-alvo (conforme seção "👥 Consideração do Público"). Exemplos: "Formal" (Petições), "Analítico" (Memorandos), "Didático" (Explicações a clientes).
    *   Evite "clichês de IA" (ex: "é crucial", "mergulhe", "jornada") e linguagem excessivamente sinalizadora (ex: "é importante ressaltar que"), preferindo uma comunicação natural e direta.

*   **Clareza e Precisão das Instruções:**
    *   Formule comandos específicos e inequívocos (ex: "Analise os riscos legais de X na cláusula Y do contrato Z" em vez de apenas "Analise o contrato").
    *   Exija precisão terminológica. Se houver termos legais chave com potencial de ambiguidade, instrua no prompt a definição ou o pedido de esclarecimento pela IA final.
    *   **Especifique a Jurisdição aplicável** (ex: `Jurisdição: BRASIL - Código Civil`) sempre que a tarefa envolver leis ou procedimentos locais.

*   **Concisão e Foco:**
    *   Instrua sobre o comprimento desejado do output quando relevante (ex: "Resuma em até 3 parágrafos", "Liste os 5 pontos principais").
    *   Oriente para ser **conciso, mas completo**, evitando redundâncias para otimizar `tokens` e manter o foco da IA.

*   **Destaque e Ênfase:**
    *   Utilize **`MAIÚSCULAS`** ou **`**negrito**`** para destacar instruções CRÍTICAS, termos chave ou partes do contexto que exigem atenção especial da IA (ex: `LEIA TODOS OS DOCUMENTOS ANEXADOS`, `FOQUE APENAS na análise da cláusula de responsabilidade civil`, `Prazo prescricional: CINCO ANOS`).

*(Nota: A subseção "Instruções de Aterramento" da antiga seção "Clareza e Precisão" foi integrada às técnicas essenciais em `1- System Prompt.md`. Seu princípio é fundamental, mas aqui focamos nos aspectos de formatação do comando em si para clareza e precisão.)*
---

🔩 **Estrutura do Prompt e Formato de Saída**

Uma estrutura clara no prompt e instruções precisas sobre o formato de saída são essenciais para resultados jurídicos de alta qualidade e utilizáveis.

*   **Componentes Essenciais do Prompt:**
    *   Ao construir um prompt, defina explicitamente os `Componentes Essenciais` (detalhados em `1- System Prompt.md`):
        *   **Ação/Tarefa (`Task`):** Verbos imperativos claros (ANALISE, RESUMA, ELABORE).
        *   **Escopo (`Scope`):** Detalhamento, limites e **Jurisdição relevante**.
        *   **Contexto (`Context`):** Informações de fundo, propósito do prompt.
        *   **Formato de Saída (`Output Format`):** Estrutura desejada (lista, tabela, ou formatos jurídicos específicos como FIRAC, Ementa CNJ). Veja abaixo sobre XML.
        *   **Restrições (`Constraints`):** Limites (extensão, fontes) e outras diretrizes.

*   **Delimitadores e Hierarquia:**
    *   Utilize **delimitadores claros** para separar blocos de instruções de blocos de conteúdo textual (contexto). Prefira `tags XML` (ex: `<documento_legal>...</documento_legal>`, `<pergunta>...</pergunta>`) ou `Markdown` (ex: ```text ... ```, `### Instrução Principal ###`).
    *   Isto é **crucial ao fornecer textos jurídicos extensos** (leis, contratos, jurisprudência) como input, para melhor controle da IA.
    *   Use `Markdown` (ex: `# Título`, `## Subtítulo`, `* Item de lista`) para criar hierarquia e organização visual dentro das instruções do prompt, se necessário.

*   **Saídas Estruturadas com XML:**
    *   Para gerar outputs que possam ser facilmente processados por outros sistemas ou para análises programáticas, **instrua o uso de tags XML descritivas e consistentes** para envolver seções distintas da resposta.
    *   *Exemplo de instrução:* "Apresente sua análise em XML, com as seguintes tags: `<fatos_relevantes>...</fatos_relevantes>`, `<fundamentacao_juridica>...</fundamentacao_juridica>`, e `<conclusao>...</conclusao>."
    *   Consulte `4- Templates e Exemplos.md` para exemplos de integração de tags XML em estruturas de saída.
    *   *Benefícios:* Clareza, interoperabilidade e melhor organização de informações complexas.

*   **Rotulagem de Estilo do Prompt (Opcional):**
    *   Para facilitar a identificação e organização, especialmente em bibliotecas de prompts, pode-se rotular o prompt com um `[ESTILO]` descritivo (ex: `[INSTRUCIONAL / RESUMO DE CASO]`, `[ROLE-BASED / ANALISE_CONTRATUAL]`).

---

🪓 **Chunking e Meta-Sumarização para Documentos Extensos**

Documentos jurídicos extensos podem exceder a janela de contexto da IA, resultando em análises incompletas. A meta-sumarização é uma técnica para mitigar isso.

*   **Quando Aplicar:** Ao lidar com documentos de entrada muito longos (ex: >20k tokens), além de posicionar o texto principal no início do prompt (conforme `1- System Prompt.md`), considere sugerir ou instruir sobre esta técnica.
*   **Técnica de Meta-Sumarização (inspirada na Anthropic):**
    1.  **Dividir (Chunking):** Instrua o usuário (ou a IA, se for uma etapa automatizada) a quebrar o documento longo em partes menores e manejáveis (chunks) por seções, capítulos, ou volume de texto.
    2.  **Analisar/Sumarizar Chunks Individualmente:** Oriente a aplicação de um prompt específico para analisar ou sumarizar cada chunk, focando na extração de pontos relevantes para a tarefa principal.
    3.  **Consolidar Análises/Resumos:** Instrua a combinar as análises/resumos parciais para criar um resultado final consolidado.
*   **Exemplo de Instrução no Prompt Gerado:** Ao gerar um prompt para analisar um documento potencialmente longo, considere adicionar: "NOTA: Se este documento for excessivamente longo para uma análise direta pela IA, recomenda-se dividi-lo em seções menores, aplicar este prompt a cada seção individualmente e, em seguida, consolidar as respostas parciais."

---

👥 **Diretrizes de Adaptação ao Público-Alvo (`Audience Awareness`)**

A estrutura e o conteúdo do prompt devem ser adaptados ao público jurídico pretendido, influenciando o tipo de informação solicitada e o formato da resposta esperada.

*   **Advogado Sênior/Especialista:** Prompts podem focar em análise complexa, nuances estratégicas e exigir respostas altamente precisas e técnicas.
*   **Advogado Júnior:** Prompts podem incluir mais estrutura (sugerindo o uso de templates de `4- Templates_e_Exemplos.md`), com foco em pesquisa e elaboração de rascunhos.
*   **Paralegal:** Prompts devem ser diretos para extração de dados, organização de informações e acompanhamento de procedimentos.
*   **Juiz/Árbitro:** Prompts devem visar resumos objetivos de argumentos, identificação clara de questões controversas e análise imparcial.
*   **Estudante de Direito:** Prompts podem ser formulados para explicar conceitos, aplicar estruturas didáticas (ex: FIRAC, IRAC) e facilitar o aprendizado.
*   **Cliente/Leigo:** Prompts devem solicitar linguagem simples e foco no essencial. **Atenção redobrada ao risco de UPL** (Prática Não Autorizada da Lei) ao gerar prompts que resultarão em respostas para este público; inclua disclaimers apropriados conforme `1- System Prompt.md`.

---

🎓 **Formatação ao Usar Exemplos (`Examples & Shots`)**

Quando a técnica de `Few-Shot Learning` (conforme `1- System Prompt.md`) for utilizada, ou quando se referir a exemplos complexos:

*   **Clareza na Apresentação de Exemplos (Few-Shot):**
    *   Se incorporar exemplos de entrada/saída diretamente no prompt, use delimitadores claros para separar cada exemplo e para distinguir entre a "entrada de exemplo" e a "saída de exemplo".
    *   *Exemplo de formatação:*
        ```
        <exemplo_1>
          <entrada_exemplo>Texto da pergunta exemplo 1...</entrada_exemplo>
          <saida_exemplo>Texto da resposta exemplo 1...</saida_exemplo>
        </exemplo_1>
        <exemplo_2>
          <entrada_exemplo>Texto da pergunta exemplo 2...</entrada_exemplo>
          <saida_exemplo>Texto da resposta exemplo 2...</saida_exemplo>
        </exemplo_2>
        ```

*   **Referência a Exemplos Estruturados (Templates):**
    *   Para formatos de saída jurídica complexos (ex: FIRAC, Ementa CNJ), em vez de replicar longos exemplos no prompt, refira-se aos modelos e exemplos completos disponíveis em `4- Templates_e_Exemplos.md`.
    *   *Exemplo de instrução:* "Siga o formato de Ementa CNJ demonstrado no Exemplo X do arquivo `4- Templates_e_Exemplos.md`."

---

📋 **Princípios Gerais de Formatação de Prompt**

- Sempre alinhe o design do `prompt` (instruções, estrutura, `role`) com o `output` desejado.
- Certifique-se de que `[STYLE] Tag` (se usada) + `Tone` + `Structure` + `Scope` + `Audience` estejam alinhados e consistentes dentro do mesmo `prompt`.
- Na dúvida, **especifique mais, não menos**, especialmente em tarefas jurídicas complexas.
- **Priorize clareza e estrutura** ao lidar com análises legais complexas ou grandes volumes de texto (`input`).

---

🔄 **Considerações de Formatação entre Modelos de IA**

Embora os princípios de formatação deste guia sejam amplamente aplicáveis, diferentes modelos de IA (ex: Claude, ChatGPT, Gemini) podem ter nuances. Considere o seguinte ao adaptar prompts:

*   **Verbosidade da Resposta:** Modelos variam na verbosidade padrão. Se a concisão for um requisito crítico do formato de saída, instrua explicitamente no prompt (ex: 'Seja conciso e direto.', 'Limite a resposta a N pontos principais.').
*   **Sensibilidade a Instruções:** Alguns modelos podem responder melhor a instruções de formatação extremamente detalhadas, enquanto outros podem performar bem com diretrizes mais gerais. Testes podem revelar a necessidade de ajustar a granularidade das instruções de formatação.
*   **Consistência de Delimitadores:** Embora XML e Markdown sejam robustos, verifique se o modelo escolhido tem alguma preferência ou peculiaridade no processamento de delimitadores específicos, especialmente em prompts muito longos ou complexos.

Testes específicos para o modelo de IA alvo são sempre uma boa prática para otimizar a eficácia das preferências de formatação.

---
# Atualizado em: 24/07/24