# Templates de Prompt - (v2.6)

Use estes templates para gerar `prompts` estruturados, cientes do público e de alta qualidade para diversos casos de uso jurídicos. Eles refletem as estruturas e técnicas de Engenharia de `Prompt` Jurídico.

**Nota:** Textos em `[MAIÚSCULAS DENTRO DE COLCHETES]` e dentro de `<tags>` como `<exemplo>` ou `<doc1>` são placeholders que devem ser substituídos pelas informações específicas do seu caso ou tarefa.

---

**[TEMPLATES ESPECÍFICOS DO CURSO]**
# Templates baseados nas estruturas detalhadas ensinadas aqui.

1.  **[TEMPLATE SOLICITAÇÃO DE ANÁLISE FIRAC+]**
    *Use quando precisar de uma análise jurídica estruturada de documentos de um caso, seguindo a metodologia FIRAC+.*
    **Nota Importante:** Este template requer que você forneça os documentos do caso completos dentro das tags `<doc>`. Certifique-se de que a IA final possa acessá-los. Se usar múltiplos documentos, considere solicitar explicitamente uma leitura holística para captar contradições.

    `Prompt:`
    ```
    # TAREFA PRINCIPAL
    - ANALISE EM DETALHE os documentos do caso fornecidos usando a estrutura FIRAC+.
    - LEIA TODOS OS DOCUMENTOS integralmente, observando a ordem e potenciais contradições para uma análise holística.
    - Capture NUANCES e forneça uma ARGUMENTAÇÃO LÓGICA.

    # DOCUMENTOS (Use delimitadores <doc> para cada um)
    <doc1>[INSIRA O TEXTO DO DOCUMENTO 1 AQUI]</doc1>
    <doc2>[INSIRA O TEXTO DO DOCUMENTO 2 AQUI]</doc2>
    ... (adicione mais conforme necessário)

    # ROLE (PERSONA)
    - Assuma a `persona` de um ESPECIALISTA em [ÁREA DO DIREITO RELEVANTE, ex: Direito Civil, Processo Penal] e também em DIREITO, LINGUÍSTICA, CIÊNCIAS COGNITIVAS E SOCIAIS.

    # LINGUAGEM E ESTILO (Output Style)
    - Tom: PROFISSIONAL e AUTORITATIVO.
    - Estilo: CONCISO, completo, sem redundâncias.
    - Início: Comece diretamente com 'DADOS DO PROCESSO'.

    # ESTRUTURA DE SAÍDA (FIRAC+)
    - Siga RIGOROSAMENTE a seguinte estrutura:
      ### DADOS DO PROCESSO📁
      ### FATOS🕵️‍♂️
      ### PROBLEMA JURÍDICO❓ (Questão Central🎯, Pontos Controvertidos🔥)
      ### DIREITO APLICÁVEL⚖️
      ### ANÁLISE E APLICAÇÃO🔍 (Argumentos/Provas Autor📝, Argumentos/Provas Réu📜)
      ### CONCLUSÃO🏛️

    # FONTES
    - Baseie-se ESTRITAMENTE nos documentos fornecidos.

    # NOTAS ADICIONAIS (Cognitive/Emotional Prompts)
    - Vá passo a passo. Pense com profundidade. Sua análise é muito importante.
    - Lembrete: Evite incluir informações identificáveis ou confidenciais/privilegiadas, a menos que o ambiente da IA final seja seguro e apropriado.
    - Termine com 🏁.
    ```

2.  **[TEMPLATE SOLICITAÇÃO DE EMENTA CNJ]**
    *Use quando precisar gerar um resumo de decisão judicial no formato padrão CNJ.*
    **Nota Importante:** Este template requer o texto completo da decisão judicial dentro da tag `<decision>`. Você pode adicionar um texto finalizador após a estrutura, se desejar. Fornecer o exemplo completo do curso pode ajudar no `few-shot learning` se a IA tiver dificuldades.

    `Prompt:`
    ```
    # TAREFA
    - ESCREVA uma EMENTA para a decisão judicial fornecida, seguindo ESTRITAMENTE o formato padrão CNJ.
    - Analise a decisão com profundidade, precisão e detalhes para capturar as nuances.

    # DOCUMENTO (Use delimitadores <decision>)
    <decision>[INSIRA O TEXTO COMPLETO DA DECISÃO AQUI]</decision>

    # ROLE (PERSONA)
    - Assuma a `persona` de um Analista Jurídico especializado em sumarização de jurisprudência.

    # ESTRUTURA DE SAÍDA (EMENTA CNJ)
    - Siga RIGOROSAMENTE a seguinte estrutura:
      ## ***Ementa***: [CABEÇALHO CONFORME CNJ]
      ### I. CASO EM EXAME
      ### II. QUESTÃO EM DISCUSSÃO
      ### III. RAZÕES DE DECIDIR (numeradas, voz ativa, verbo presente)
      ### IV. DISPOSITIVO E TESE (resultado, teses numeradas, dispositivos citados, jurisprudência citada)

    # FONTES
    - Cite apenas fatos, normas e precedentes mencionados na decisão fornecida.

    # INÍCIO/FIM
    - Comece o texto com "***Ementa***".
    - (Opcional) Termine com [SEU TEXTO FINALIZADOR AQUI].
    ```

3.  **[TEMPLATE SOLICITAÇÃO DE ESTUDO DE CASO (CASO+)]**
    *Use quando precisar criar um estudo de caso detalhado para fins acadêmicos ou de treinamento.*
    **Nota Importante:** Este template requer que você forneça os documentos relevantes do caso dentro das tags `<doc>`. Considere solicitar explicitamente uma leitura holística se houver múltiplos documentos.

    `Prompt:`
    ```
    # TAREFA PRINCIPAL
    - ELABORE UM ESTUDO DE CASO detalhado baseado nos documentos fornecidos, usando a estrutura CASO+.
    - ANALISE EM DETALHE, leia TODOS os documentos integralmente, incorpore NUANCES e forneça ARGUMENTAÇÃO LÓGICA.

    # DOCUMENTOS (Use delimitadores <doc> para cada um)
    <doc1>[INSIRA O TEXTO DO DOCUMENTO 1 AQUI]</doc1>
    <doc2>[INSIRA O TEXTO DO DOCUMENTO 2 AQUI]</doc2>
    ... (adicione mais conforme necessário)

    # ROLE (PERSONA)
    - Assuma a `persona` de um ESPECIALISTA em [ÁREA DO DIREITO RELEVANTE] e também em DIREITO, LINGUÍSTICA, CIÊNCIAS COGNITIVAS E SOCIAIS.

    # LINGUAGEM E ESTILO (Output Style)
    - Tom: PROFISSIONAL e AUTORITATIVO.
    - Estilo: CONCISO, completo, sem redundâncias.
    - Público-Alvo (`Audience`): Estudantes de pós-graduação.
    - Início: Comece diretamente com 'DADOS DO PROCESSO'.

    # ESTRUTURA DE SAÍDA (CASO+)
    - Siga RIGOROSAMENTE a seguinte estrutura:
      ### DADOS DO PROCESSO📁
      ### FATOS🕵️‍♂️ (começando pela conduta do réu)
      ### ARGUMENTOS E PROVAS DO AUTOR📝
      ### ARGUMENTOS E PROVAS DO RÉU📜
      ### DIREITO APLICÁVEL⚖️
      ### QUESTÕES PARA DEBATE❓
      ### RESPOSTA DO TRIBUNAL

    # FONTES
    - Baseie-se ESTRITAMENTE nos documentos fornecidos.

    # NOTAS ADICIONAIS (Cognitive/Emotional Prompts)
    - Vá passo a passo. Pense com profundidade. Detalhe bem os fatos.
    - Lembrete: Evite incluir informações identificáveis ou confidenciais/privilegiadas, a menos que o ambiente da IA final seja seguro e apropriado.
    - Termine com 🏁.
    ```

4.  **[TEMPLATE SOLICITAÇÃO DE SUPERANÁLISE (Textos Jurídicos)]**
    *Use para uma análise profunda e estruturada de artigos, capítulos de livros ou pareceres jurídicos.*
    **Nota Importante:** Este template requer que você forneça o texto completo a ser analisado dentro da tag `<text>`.

    `Prompt:`
    ```
    # TAREFA
    - REALIZE uma SUPERANÁLISE do texto jurídico fornecido.
    - ANALISE EM DETALHE e na ÍNTEGRA.

    # DOCUMENTO (Use delimitadores <text>)
    <text>[INSIRA O TEXTO COMPLETO AQUI]</text>

    # ROLE (PERSONA)
    - Assuma a `persona` de um ANALISTA DE TEXTOS JURÍDICOS (PhD) especializado em [ÁREA DO DIREITO DO TEXTO], com domínio de Teoria da Linguagem, Interpretação, Lógica e Argumentação Jurídica.

    # ESTRUTURA DE SAÍDA (SUPERANÁLISE)
    - Siga RIGOROSAMENTE a seguinte estrutura:
      ### DADOS DO TEXTO📁
      ### ESPECIALIDADE 📚
      ### SUMÁRIO📋 (dois níveis)
      ### TABELA📊 (Objetivos | Ideias Centrais)
      ### O QUE O TEXTO PRETENDE MOSTRAR 🧐 (propósito, questão central, questões secundárias)
      ### RESULTADOS✅ (conclusões pragmáticas)
      ### POR QUE ISSO É IMPORTANTE?🌟 (relevância, impacto)
      ### QUE LIÇÕES PRÁTICAS PODEMOS TIRAR? 🤔 (aplicação prática)
      ### IR MAIS FUNDO🔍 (5 conceitos relevantes + pergunta final)

    # NOTAS ADICIONAIS (Cognitive/Emotional Prompts)
    - Pense passo a passo. Sua análise é muito importante. Dê o seu melhor.
    ```

---

**[TEMPLATES GERAIS ADAPTADOS PARA USO JURÍDICO]**
# Templates genéricos adaptados para maior utilidade no contexto jurídico.

5.  **[INSTRUÇÃO ABRANGENTE JURÍDICA]**
    *Use para tarefas jurídicas mais simples que não se encaixam nos modelos complexos acima.*
    ```
    - `Role`/Persona: Você é um(a) [PAPEL JURÍDICO, ex: Advogado(a) Assistente].
    - Tarefa (`Task`): Sua tarefa é [INSTRUÇÃO CLARA E DIRETA, ex: resumir os pontos principais, identificar cláusulas de X tipo, elaborar um esboço inicial de Y].
    - Contexto (`Context`): Considere o seguinte contexto/documento: `<context>[INSIRA O CONTEXTO OU TEXTO CURTO AQUI]</context>`. (Para textos longos, use um template específico ou delimitadores claros).
    - Jurisdição (`Jurisdiction`, se aplicável): [NOME DA JURISDIÇÃO].
    - Formato de Saída (`Output Format`): Apresente a resposta como [FORMATO DESEJADO, ex: uma lista com marcadores, um parágrafo conciso, uma tabela simples].
    - Tom/Estilo (`Tone`): Use um tom [TOM DESEJADO, ex: formal, objetivo, informativo].
    - Público-Alvo (`Audience`, se aplicável): [PÚBLICO, ex: Sócio Sênior, Cliente].
    ```
    – Quando usar: Para estruturar rapidamente comandos para tarefas jurídicas bem definidas e de menor complexidade.

6.  **[BASEADO EM CENÁRIO JURÍDICO]**
    *Use quando precisar simular uma situação ou análise baseada em um conjunto específico de circunstâncias.*
    ```
    - Cenário (`Scenario`): [DESCRIÇÃO DETALHADA DO CENÁRIO JURÍDICO].
    - Jurisdição (`Jurisdiction`, se aplicável): [NOME DA JURISDIÇÃO].
    - Área do Direito (`Legal Area`): [ÁREA PRINCIPAL, ex: Direito Contratual, Responsabilidade Civil].
    - Documentos Fornecidos (`Input Documents`, opcional, usar delimitadores): `<doc1>[TEXTO]</doc1>`
    - Objetivo (`Goal`): [O QUE DEVE SER ANALISADO OU PRODUZIDO, ex: Identificar os principais riscos legais, Esboçar possíveis argumentos para a parte X].
    - Restrições (`Constraints`, opcional): [LIMITAÇÕES, ex: Focar apenas no aspecto Y, Não considerar a lei Z].
    - Formato de Saída (`Output Format`): [FORMATO].
    - Tom (`Tone`): [TOM].
    ```
    – Quando usar: Para análises de risco, planejamento estratégico inicial ou exploração de hipóteses em um contexto jurídico definido.

7.  **[CHAIN-OF-THOUGHT JURÍDICO]**
    *Use para tarefas que exigem raciocínio jurídico explícito e passo a passo.*
    ```
    - Tarefa (`Task`): [TAREFA ANALÍTICA, ex: Avaliar a aplicabilidade da Súmula X a este caso].
    - Contexto/Fatos (`Context`): `<facts>[INSIRA OS FATOS RELEVANTES AQUI]</facts>`
    - Instrução Cognitiva (`Cognitive Instruction`): Pense passo a passo (`Think step-by-step`):
      1. Enuncie a regra/princípio jurídico relevante (ex: Súmula X).
      2. Identifique os requisitos/elementos da regra.
      3. Analise como os fatos fornecidos se encaixam (ou não) em cada requisito.
      4. Apresente uma conclusão preliminar fundamentada.
    - Formato de Saída (`Output Format`): Resposta detalhada seguindo os passos acima.
    ```
    – Quando usar: Para aplicar leis/precedentes a fatos, analisar causalidade, ou qualquer tarefa que se beneficie de um raciocínio jurídico explícito.

8.  **[AJUSTADO AO PÚBLICO JURÍDICO]**
    *Use para garantir que a linguagem e a profundidade da resposta sejam adequadas ao destinatário.*
    ```
    - Tarefa (`Task`): [TAREFA, ex: Explicar o conceito de Prescrição Intercorrente].
    - Público-Alvo (`Target Audience`): Escreva para um(a) [PÚBLICO ESPECÍFICO, ex: estagiário de direito, cliente leigo, juiz].
    - Foco (`Focus`): Concentre-se em [ASPECTO PRINCIPAL, ex: os requisitos práticos, as consequências para o processo, a fundamentação legal].
    - Tom/Estilo (`Tone`): Use um tom [TOM APROPRIADO, ex: didático e simples, formal e técnico, objetivo e direto].
    - Restrições (`Constraints`, opcional): Evite jargões excessivos / Inclua referências legais / Mantenha abaixo de X palavras.
    ```
    – Quando usar: Para gerar textos (explicações, resumos, comunicações) que precisam ser cuidadosamente adaptados ao nível de conhecimento e necessidade do leitor.

---

*Templates como `[FEW-SHOT]`, `[STYLE COMPARISON]` e `[MULTI-PROMPT ITERATION]` do arquivo original podem ser mantidos como estão, pois são técnicas de `prompting` mais genéricas, mas ainda aplicáveis.*
