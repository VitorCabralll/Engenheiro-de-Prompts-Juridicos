![Logo](logo.png)

# ⚖️ Engenheiro de Prompts Jurídicos

**(v2.9)**

**Descrição:** Um sistema especializado, estruturado e baseado em restrições, projetado para auxiliar na geração, avaliação e refinamento de prompts de Inteligência Artificial (IA) especificamente para o contexto jurídico.

![Licença MIT](https://img.shields.io/badge/Licença-MIT-blue.svg)

---
## 🎯 Objetivo

O **Engenheiro de Prompts Jurídicos** atua como um orquestrador, ajudando usuários a criar instruções (prompts) eficazes e seguras para sistemas de IA no domínio do direito. Ele integra técnicas avançadas de engenharia de prompt com as nuances e exigências do contexto jurídico.

**Importante:** Este sistema **NÃO é um chatbot, assistente jurídico ou consultor legal**. Sua única função é ajudar a construir e refinar os *prompts* que serão usados em outras IAs. Ele não executa as tarefas jurídicas descritas nos prompts que gera ou avalia.

## 🔧 Funcionalidades Principais

O agente opera através de modos específicos, ativados por tags:

*   **Geração de Prompts (`#prompt`):** Cria sugestões de prompts jurídicos estruturados e detalhados, consultando templates e aplicando preferências de formatação. Faz perguntas clarificadoras se a solicitação inicial for vaga.
*   **Avaliação de Qualidade (`#qa`):** Analisa prompts fornecidos pelo usuário, identifica falhas (ambiguidade, riscos jurídicos como UPL (Unauthorized Practice of Law - Exercício Ilegal da Profissão), falta de contexto, problemas estruturais) e sugere melhorias com justificativa.
*   **Modo Educacional (`#learn`):** Gera um prompt e explica sua estrutura, destacando as técnicas de engenharia de prompt utilizadas e sua relevância jurídica, baseando-se no conhecimento interno do sistema.
*   **Teste de Estresse (`#edge`):** Gera prompts ambíguos ou desafiadores para testar a robustez e os guardrails de sistemas de IA no contexto jurídico.

## ✨ Benefícios

*   **Prompts mais Eficazes:** Gera prompts claros, estruturados e detalhados, aumentando a probabilidade de obter resultados úteis da IA final.
*   **Foco na Segurança Jurídica:** Ajuda a identificar e mitigar riscos nos prompts (ex: solicitações que podem levar a UPL, falta de contexto essencial).
*   **Consistência:** Aplica um conjunto definido de preferências de formatação e estilo.
*   **Uso de Melhores Práticas:** Incorpora técnicas avançadas de engenharia de prompt adaptadas ao direito.
*   **Estruturação de Tarefas Complexas:** Oferece templates para metodologias jurídicas específicas.

## 💡 Fundamentação Técnica

O design e as técnicas empregadas por este agente são **baseados nas melhores e mais avançadas práticas de engenharia de prompts da indústria**, incluindo princípios e diretrizes de fontes reconhecidas como os guias de prompting da **OpenAI** e da **Anthropic**. As técnicas como Role-Playing, Chain-of-Thought (CoT), uso de delimitadores (XML), few-shot learning, aterramento factual e otimização de contexto foram adaptadas e integradas especificamente para o domínio jurídico.

## 🚀 Como Utilizar

Este sistema é projetado para ser implementado em plataformas de IA que suportam instruções de sistema personalizadas e acesso a uma base de conhecimento (os arquivos `.md` do projeto).

A interação básica se dá fornecendo uma tag de modo seguida pela sua solicitação:

1.  **Para Gerar um Prompt:**
    ```
    #prompt Crie um prompt para analisar uma cláusula de não concorrência em um contrato de trabalho, sob a ótica do empregado, considerando a legislação brasileira. O tom deve ser analítico.
    ```
    *(Se a solicitação for vaga, o agente fará perguntas.)*

2.  **Para Avaliar um Prompt:**
    ```
    #qa Avalie este prompt: "Resuma a decisão anexa."
    ```

3.  **Para Aprender sobre um Prompt:**
    ```
    #learn Gere um prompt para aplicar FIRAC+ a um caso simples e explique como ele foi construído.
    ```

4.  **Para Gerar um Teste:**
    ```
    #edge Gere um prompt que teste a capacidade da IA de lidar com instruções contraditórias sobre jurisdição.
    ```

## 📚 Métodos e Templates Incluídos

O agente utiliza uma base de conhecimento (`4- Templates_e_Exemplos.md`) que inclui templates e exemplos para diversas tarefas, como:

*   Análise **FIRAC+**
*   Geração de **Ementa (formato CNJ)**
*   Criação de **Estudo de Caso (CASO+)**
*   **SuperAnálise** de Textos Jurídicos
*   Análise Comparativa Jurídica
*   Geração de Opções Jurídicas
*   Templates Gerais (Instrução Abrangente, Cenário, CoT, Ajuste ao Público)
*   Exemplos que ilustram técnicas específicas (Delimitadores, Personas, etc.)

## 🛠️ Casos de Uso Práticos

Esta seção demonstra como o **Engenheiro de Prompts Jurídicos** pode ser utilizado por profissionais do direito para gerar prompts eficazes para diversas tarefas. Cada exemplo ilustra a tradução de uma necessidade jurídica em um prompt detalhado e estruturado, pronto para ser usado em um modelo de linguagem de grande porte (LLM).

---

**Exemplo 1: Análise de Cláusula Contratual com Metodologia Específica**

*   **Necessidade do Usuário:** Um advogado precisa analisar uma cláusula de "Vigência e Rescisão" em um contrato de prestação de serviços de desenvolvimento de software, sob a ótica da empresa contratante. Ele quer identificar possíveis ambiguidades, riscos e sugerir melhorias, utilizando uma abordagem estruturada.

*   **Input para o Sistema:**
    ```
    #prompt Crie um prompt para analisar criticamente uma cláusula de 'Vigência e Rescisão' de um contrato de desenvolvimento de software, do ponto de vista da empresa CONTRATANTE. O objetivo é identificar ambiguidades, riscos potenciais e sugerir melhorias na redação. Utilize a metodologia 'SuperAnálise de Textos Jurídicos' e especifique o público como 'advogado sênior'. O tom deve ser formal e analítico.
    ```

*   **Prompt Gerado pelo Sistema:**
    ```text
    <SYSTEM_PROMPT_CORE>
    <TASK_DEFINITION>
    Você é um especialista em análise contratual, com foco em contratos de tecnologia. Sua tarefa é realizar uma análise crítica e detalhada da cláusula de "Vigência e Rescisão" fornecida abaixo, seguindo a metodologia "SuperAnálise de Textos Jurídicos". A perspectiva da análise deve ser estritamente a da empresa CONTRATANTE.

    **Metodologia Aplicável:** SuperAnálise de Textos Jurídicos
    **Foco da Análise:** Identificação de ambiguidades, avaliação de riscos para a CONTRATANTE, e sugestão de melhorias redacionais.
    **Público-Alvo do Resultado:** Advogado Sênior da CONTRATANTE.
    **Tom e Estilo:** Formal, analítico, preciso e objetivo.
    </TASK_DEFINITION>

    <CONTEXT>
    **Tipo de Contrato:** Prestação de Serviços de Desenvolvimento de Software.
    **Parte Analisando:** CONTRATANTE.
    **Cláusula para Análise (Delimitada por <CLAUSULA_VIGENCIA_RESCISAO_CONTRATO_SOFTWARE_CONTRATANTE_001>):**
    <CLAUSULA_VIGENCIA_RESCISAO_CONTRATO_SOFTWARE_CONTRATANTE_001>
    [Aqui o usuário inserirá a cláusula completa do contrato]
    </CLAUSULA_VIGENCIA_RESCISAO_CONTRATO_SOFTWARE_CONTRATANTE_001>
    </CONTEXT>

    <INSTRUCTIONS>
    Execute a análise da cláusula fornecida, estruturando sua resposta da seguinte forma:

    **1. Resumo da Cláusula (Perspectiva CONTRATANTE):**
       - Breve descrição das principais disposições da cláusula sob a ótica da CONTRATANTE.

    **2. Pontos Fortes para a CONTRATANTE:**
       - Identifique os aspectos da cláusula que são claramente benéficos ou protetivos para a CONTRATANTE.

    **3. Identificação de Ambiguidades e Incertezas:**
       - Liste e explique quaisquer termos, frases ou disposições que possam ser interpretados de múltiplas maneiras ou que careçam de clareza.
       - Para cada ambiguidade, descreva o impacto potencial para a CONTRATANTE.

    **4. Análise de Riscos (Perspectiva CONTRATANTE):**
       - Detalhe os riscos contratuais, financeiros, operacionais ou legais que a redação atual da cláusula apresenta para a CONTRATANTE. Considere cenários de rescisão antecipada, não cumprimento de prazos, etc.
       - Priorize os riscos identificados (Alto, Médio, Baixo).

    **5. Sugestões de Melhoria (Foco na Proteção da CONTRATANTE):**
       - Para cada ambiguidade ou risco identificado, proponha alterações específicas na redação da cláusula.
       - Justifique cada sugestão, explicando como ela mitiga o risco ou aumenta a clareza em favor da CONTRATANTE.
       - Se aplicável, sugira a inclusão de novas sub-cláusulas para proteger os interesses da CONTRATANTE.

    **6. Considerações Adicionais:**
       - Outros pontos relevantes não cobertos acima que o advogado sênior da CONTRATANTE deva considerar.

    **Formato da Resposta:**
    Utilize headings claros para cada seção. Seja conciso, mas completo. Fundamente suas análises.
    </INSTRUCTIONS>

    <OUTPUT_EXAMPLE>
    (Opcional: Se um exemplo de output fosse fornecido no template 'SuperAnálise', ele seria incluído aqui para guiar o LLM.)
    </OUTPUT_EXAMPLE>
    </SYSTEM_PROMPT_CORE>
    ```

---

**Exemplo 2: Geração de Estrutura Inicial para Petição com FIRAC+**

*   **Necessidade do Usuário:** Uma advogada precisa redigir os fundamentos jurídicos para uma petição inicial referente a um caso de responsabilidade civil por erro médico. Ela quer que a IA a ajude a estruturar os argumentos principais usando a metodologia FIRAC+ (Facts, Issue, Rule, Analysis, Conclusion + Policy).

*   **Input para o Sistema:**
    ```
    #prompt Gere uma estrutura de argumentação jurídica para uma petição inicial, usando FIRAC+, sobre um caso de responsabilidade civil por erro médico (diagnóstico tardio de apendicite resultando em complicações). Foque nos elementos que demonstram negligência. O cliente é o paciente. O tom deve ser persuasivo e técnico-jurídico.
    ```

*   **Prompt Gerado pelo Sistema:**
    ```text
    <SYSTEM_PROMPT_CORE>
    <TASK_DEFINITION>
    Você é um assistente de redação jurídica especializado em responsabilidade civil. Sua tarefa é gerar uma estrutura detalhada de argumentação para os fundamentos jurídicos de uma petição inicial, utilizando a metodologia FIRAC+ (Fatos, Questão, Regra, Análise, Conclusão e Política/Princípio). O caso envolve responsabilidade civil por erro médico (diagnóstico tardio de apendicite que levou a peritonite e maior tempo de recuperação). O objetivo é demonstrar a negligência da parte Ré.

    **Metodologia Aplicável:** FIRAC+
    **Tipo de Peça:** Fundamentação Jurídica para Petição Inicial.
    **Área do Direito:** Responsabilidade Civil (Erro Médico).
    **Parte Representada:** Autor (Paciente).
    **Tom e Estilo:** Persuasivo, técnico-jurídico, formal.
    **Público-Alvo da Peça:** Juízo de primeira instância.
    </TASK_DEFINITION>

    <CONTEXT>
    **Resumo do Caso (a ser expandido pelo usuário):**
    Paciente (Autor) buscou atendimento médico com sintomas X, Y, Z. O médico Réu diagnosticou erroneamente como [diagnóstico incorreto], prescrevendo [tratamento incorreto]. Dias depois, com piora do quadro, o Paciente buscou outro profissional que diagnosticou corretamente apendicite aguda, já evoluída para peritonite. O Paciente necessitou de cirurgia de emergência e teve um período de recuperação significativamente mais longo e complicado do que teria se o diagnóstico fosse feito corretamente na primeira consulta.

    **Informações Essenciais a serem consideradas (e detalhadas pelo usuário ao usar este prompt no LLM):**
    *   Detalhes dos sintomas iniciais.
    *   Procedimentos realizados (ou não realizados) pelo médico Réu.
    *   Padrão de cuidado esperado para os sintomas apresentados.
    *   Evidências da relação causal entre o diagnóstico tardio e as complicações (ex: prontuários, laudos, pareceres técnicos preliminares).
    *   Danos sofridos pelo Autor (materiais, morais, estéticos, lucros cessantes, etc.).
    </CONTEXT>

    <INSTRUCTIONS>
    Desenvolva a estrutura da argumentação jurídica seguindo cada componente do FIRAC+:

    **I. FATOS (Facts):**
        a.  **Descrição Cronológica Relevante:** Apresente os fatos pertinentes ao erro médico de forma clara e cronológica, destacando os eventos que configuram a negligência.
        b.  **Conduta do Réu:** Detalhe a ação ou omissão do profissional/instituição médica que resultou no diagnóstico tardio.
        c.  **Sofrimento e Danos do Autor:** Descreva as consequências diretas do erro médico para o Autor (complicações, cirurgias adicionais, tempo de recuperação, impacto emocional e financeiro).

    **II. QUESTÃO (Issue):**
        a.  **Questão Jurídica Principal:** Formule a(s) pergunta(s) jurídica(s) central(is) a ser(em) respondida(s). Ex: "Configura-se a responsabilidade civil do Réu pelo diagnóstico tardio de apendicite, resultando em [complicações específicas], face à demonstração de negligência e do nexo causal com os danos sofridos pelo Autor?"
        b.  **Questões Secundárias (se houver):** Ex: "Qual a extensão dos danos morais e materiais a serem compensados?"

    **III. REGRA (Rule):**
        a.  **Legislação Aplicável:**
            i.  Código Civil (arts. 186, 927, 949, 950, 951 - responsabilidade civil subjetiva, dano material, moral, lucros cessantes, especificidades do erro profissional).
            ii. Código de Defesa do Consumidor (se aplicável à relação médico-paciente no caso concreto, ex: art. 14 - responsabilidade objetiva do fornecedor de serviços, exceto profissionais liberais mediante culpa).
            iii. Código de Ética Médica (dever de diligência, imperícia).
        b.  **Doutrina Relevante:** Citar autores renomados sobre responsabilidade civil médica, erro de diagnóstico, nexo causal, teoria da perda de uma chance (se aplicável).
        c.  **Jurisprudência Correlata:** Mencionar entendimentos consolidados dos Tribunais (especialmente do Tribunal local e Superiores) em casos análogos de erro de diagnóstico de apendicite ou situações similares.

    **IV. ANÁLISE (Analysis):**
        a.  **Subsunção dos Fatos à Norma:** Conecte os fatos específicos do caso com as regras jurídicas apresentadas.
            i.  **Demonstração da Culpa (Negligência/Imperícia):** Argumente como a conduta do Réu (diagnóstico tardio) desviou do padrão de cuidado esperado. Detalhe por que o diagnóstico correto era esperado e possível.
            ii. **Nexo de Causalidade:** Estabeleça a ligação direta entre a conduta negligente do Réu e os danos sofridos pelo Autor (a peritonite e suas consequências decorreram do atraso no diagnóstico e tratamento).
            iii. **Caracterização dos Danos:** Detalhe cada tipo de dano (material, moral, estético, etc.) e como ele se manifestou no caso concreto, vinculando-os à conduta do Réu.
        b.  **Aplicação da Doutrina e Jurisprudência:** Utilize os entendimentos doutrinários e os precedentes jurisprudenciais para reforçar a tese do Autor. Compare o caso concreto com os julgados favoráveis.
        c.  **Refutação de Possíveis Argumentos Contrários (Antecipação):** Se pertinente, antecipe e refute brevemente possíveis defesas (ex: complexidade do caso, sintomas atípicos – se não for o caso).

    **V. CONCLUSÃO (Conclusion):**
        a.  **Retomada da Questão:** Responda afirmativamente à(s) questão(ões) jurídica(s) formulada(s).
        b.  **Síntese da Argumentação:** Reafirme sucintamente que, com base nos fatos, regras e análise, restou configurada a responsabilidade civil do Réu.
        c.  **Pedido (Referência aos Pedidos da Petição):** Indique que, em face do exposto, serão formulados os pedidos de condenação correspondentes.

    **VI. POLÍTICA/PRINCÍPIO (Policy/Principle - Opcional, mas recomendável):**
        a.  **Justificativa Social/Ética:** Argumente brevemente sobre a importância da responsabilização em casos de erro médico para a proteção da saúde, a manutenção da confiança no sistema médico e o desestímulo a condutas negligentes.
        b.  **Princípios Jurídicos Fundamentais:** Refira-se a princípios como dignidade da pessoa humana, direito à saúde, reparação integral do dano.

    **Formato da Resposta:**
    Apresente a estrutura em tópicos e subtópicos claros, conforme o modelo FIRAC+ detalhado acima. Use linguagem jurídica apropriada.
    </INSTRUCTIONS>
    </SYSTEM_PROMPT_CORE>
    ```

---

**Exemplo 3: Aprendizagem sobre a Construção de um Prompt para Due Diligence**

*   **Necessidade do Usuário:** Um advogado júnior está aprendendo a usar IA para auxiliar em processos de *due diligence* e quer entender como um prompt eficaz para essa finalidade é construído, incluindo as técnicas de engenharia de prompt envolvidas.

*   **Input para o Sistema:**
    ```
    #learn Gere um prompt para identificar cláusulas de 'Declarações e Garantias' e 'Condições Precedentes' em um Acordo de Acionistas, e analisar seus potenciais riscos para um investidor minoritário. Explique a estrutura do prompt, as técnicas de prompting usadas e sua relevância jurídica.
    ```

*   **Prompt Gerado pelo Sistema:**
    ```text
    <SYSTEM_PROMPT_CORE>
    <TASK_DEFINITION>
    **Objetivo Educacional:** Explicar a construção de um prompt para análise de cláusulas específicas em um Acordo de Acionistas, sob a ótica de um investidor minoritário, com foco em *due diligence*.

    **Prompt Gerado para Análise:**
    ```text
    <PROMPT_ANALISADO>
    <ROLE_DEFINITION>
    Assuma o papel de um advogado especialista em direito societário e fusões e aquisições (M&A), com vasta experiência na análise de Acordos de Acionistas sob a perspectiva de investidores minoritários.
    </ROLE_DEFINITION>

    <CONTEXT_SETTING>
    **Documento para Análise:** Acordo de Acionistas (o texto completo será fornecido pelo usuário).
    **Seções de Interesse Principal:**
        1. Cláusulas de "Declarações e Garantias" (Representations and Warranties) fornecidas pela empresa e/_ou pelos sócios majoritários.
        2. Cláusulas de "Condições Precedentes" (Conditions Precedent) para a efetivação do investimento ou para outros direitos do investidor.
    **Perspectiva da Análise:** Investidor minoritário realizando *due diligence* antes de um aporte.
    **Objetivo da Análise:** Identificar riscos, omissões significativas e pontos de atenção crítica para o investidor minoritário nas cláusulas mencionadas.
    </CONTEXT_SETTING>

    <INPUT_DOCUMENT_SPECIFICATION>
    **Texto do Acordo de Acionistas (Delimitado por <ACORDO_ACIONISTAS_TEXT_002>):**
    <ACORDO_ACIONISTAS_TEXT_002>
    [O usuário inserirá aqui o texto completo do Acordo de Acionistas ou as seções relevantes]
    </ACORDO_ACIONISTAS_TEXT_002>
    </INPUT_DOCUMENT_SPECIFICATION>

    <DETAILED_INSTRUCTIONS>
    Realize as seguintes tarefas:

    **Tarefa 1: Identificação e Extração de Cláusulas**
        a. Localize e extraia textualmente todas as cláusulas ou sub-cláusulas que se refiram a "Declarações e Garantias" (ou sinônimos) feitas pela empresa-alvo ou seus controladores.
        b. Localize e extraia textualmente todas as cláusulas ou sub-cláusulas que se refiram a "Condições Precedentes" (ou sinônimos) que impactem o investidor minoritário.
        c. Apresente as cláusulas extraídas de forma organizada, indicando a numeração original.

    **Tarefa 2: Análise de Riscos (Perspectiva do Investidor Minoritário)**
        Para cada cláusula de "Declarações e Garantias" identificada:
            i.  Avalie sua abrangência e especificidade.
            ii. Identifique quais garantias essenciais para um investidor minoritário estão presentes e quais estão ausentes.
            iii. Aponte possíveis brechas, ambiguidades ou limitações que representem risco (ex: prazos de validade curtos, limites de responsabilidade baixos, ausência de garantias sobre litígios importantes ou passivos ocultos).
        Para cada cláusula de "Condições Precedentes" identificada:
            i.  Analise a razoabilidade e a viabilidade de cumprimento de cada condição.
            ii. Identifique condições que dependam excessivamente de terceiros ou da discricionariedade da empresa/majoritários.
            iii. Avalie o impacto para o investidor minoritário caso alguma condição não seja cumprida (ex: perda do investimento, não aquisição de direitos).

    **Tarefa 3: Recomendações e Pontos de Atenção**
        a. Com base na análise, liste os principais riscos (Top 3-5) para o investidor minoritário.
        b. Sugira pontos específicos que deveriam ser negociados ou melhor esclarecidos antes da assinatura do acordo.
        c. Indique se há necessidade de solicitar informações ou documentos adicionais com base nas cláusulas analisadas.

    <OUTPUT_FORMATTING>
    **Formato da Resposta:**
    Utilize headings claros para cada tarefa e subtarefa.
    Para a extração (Tarefa 1), use citações diretas.
    Para a análise de riscos (Tarefa 2), seja específico e justifique cada risco apontado.
    Para as recomendações (Tarefa 3), seja pragmático e direto.
    O tom deve ser o de um consultor jurídico experiente se reportando ao seu cliente (investidor).
    </OUTPUT_FORMATTING>
    </PROMPT_ANALISADO>
    ```

    **Explicação da Estrutura e Técnicas do Prompt Gerado:**

    1.  **`<ROLE_DEFINITION>` (Role-Playing / Definição de Persona):**
        *   **Técnica:** Atribui um papel específico à IA ("advogado especialista em direito societário e M&A...").
        *   **Relevância Jurídica:** Ajuda a IA a adotar o jargão, o nível de detalhe e a perspectiva analítica esperados de um profissional com essa especialização, tornando a resposta mais alinhada com as necessidades de uma *due diligence*.

    2.  **`<CONTEXT_SETTING>` (Aterramento / Configuração de Contexto):**
        *   **Técnica:** Fornece informações cruciais sobre o documento, as seções de interesse, a perspectiva da análise e o objetivo.
        *   **Relevância Jurídica:** Garante que a IA compreenda o escopo da tarefa. Especificar "investidor minoritário" e "due diligence" direciona a IA para focar em riscos e proteções típicas dessa parte, que são diferentes das de um majoritário ou da própria empresa.

    3.  **`<INPUT_DOCUMENT_SPECIFICATION>` (Uso de Delimitadores):**
        *   **Técnica:** Indica claramente onde o texto do Acordo de Acionistas será inserido, usando delimitadores XML (`<ACORDO_ACIONISTAS_TEXT_002>`).
        *   **Relevância Jurídica:** Previne que a IA confunda o texto do acordo com as instruções do prompt. Essencial para processar documentos extensos e complexos, garantindo que a análise se concentre no local correto.

    4.  **`<DETAILED_INSTRUCTIONS>` (Chain-of-Thought (CoT) Implícito / Decomposição da Tarefa):**
        *   **Técnica:** Divide a tarefa complexa de *due diligence* em subtarefas menores e sequenciais (Identificação, Análise de Riscos, Recomendações).
        *   **Relevância Jurídica:** Reflete o processo mental que um advogado seguiria: primeiro entender o que está escrito, depois analisar criticamente e, por fim, aconselhar. Isso guia a IA a produzir uma resposta estruturada e lógica, cobrindo os aspectos essenciais da análise de cláusulas contratuais.

    5.  **Especificidade nas Instruções (Clareza e Precisão):**
        *   **Técnica:** As instruções para cada subtarefa são detalhadas (ex: "Avalie sua abrangência e especificidade", "Identifique quais garantias essenciais... estão ausentes").
        *   **Relevância Jurídica:** No direito, os detalhes importam. Instruções precisas reduzem a ambiguidade e aumentam a chance de a IA identificar os tipos exatos de riscos e informações que um advogado procuraria (ex: passivos ocultos, prazos, limites de responsabilidade).

    6.  **`<OUTPUT_FORMATTING>` (Formatação da Saída):**
        *   **Técnica:** Define como a resposta deve ser estruturada (headings, citações, tom).
        *   **Relevância Jurídica:** Facilita a leitura e a utilização da resposta pelo advogado. Um relatório de *due diligence* precisa ser claro e organizado para ser útil. O "tom de consultor jurídico experiente" reforça a persona.

    **Benefício da Abordagem:**
    Este prompt é construído para maximizar a relevância e a precisão da resposta da IA para uma tarefa jurídica específica e complexa. Ao invés de uma pergunta genérica como "analise este contrato", o prompt detalhado guia a IA através de um processo analítico estruturado, resultando em insights mais úteis e acionáveis para o advogado.
    </SYSTEM_PROMPT_CORE>
    ```

---

## 📂 Estrutura dos Arquivos do Projeto

A base de conhecimento e controle do agente é composta pelos seguintes arquivos:

1.  **`1- System Prompt.md`**: O núcleo do sistema, definindo identidade, fluxo de trabalho, modos, técnicas, guardrails e como usar os outros arquivos.
2.  **`2- Preferencias de Formatacao Prompt.md`**: Define as regras gerais de estilo, tom, estrutura, concisão, clareza e considerações de público para todos os prompts.
3.  **`3- Modulo_QA.md`**: Contém os protocolos e critérios para avaliação de prompts (`#qa`) e geração de testes (`#edge`), com foco nos riscos e desafios específicos do domínio jurídico.
4.  **`4- Templates_e_Exemplos.md`**: A biblioteca central contendo templates estruturados para metodologias jurídicas, templates gerais adaptados e exemplos ilustrativos de técnicas de prompt.

## ⚙️ Guia de Implementação

Esta seção fornece um guia passo a passo para configurar o **Engenheiro de Prompts Jurídicos** em diferentes plataformas de Inteligência Artificial. A correta implementação garante que o sistema funcione conforme projetado, utilizando sua base de conhecimento para gerar, avaliar e refinar prompts jurídicos.

**Arquivos Essenciais do Sistema:**

Para o funcionamento ideal, o Engenheiro de Prompts Jurídicos necessita que a plataforma de IA tenha acesso ao conteúdo dos seguintes arquivos:

1.  **`1- System Prompt.md`**: O prompt principal do sistema que define a identidade, o fluxo de trabalho e as capacidades do Engenheiro de Prompts Jurídicos.
2.  **`2- Preferencias de Formatacao Prompt.md`**: Contém as regras de estilo, tom e estrutura para os prompts gerados.
3.  **`3- Modulo_QA.md`**: Define os critérios para avaliação de qualidade (`#qa`) e testes de estresse (`#edge`).
4.  **`4- Templates_e_Exemplos.md`**: Uma biblioteca de templates e exemplos de prompts jurídicos.

A seguir, detalhamos como implementar o sistema nas principais plataformas de IA:

---

### **ChatGPT (OpenAI)**

#### Método 1: Usando Custom GPT (Recomendado para Usuários Plus/Team)

1.  **Criar um Custom GPT:**
    *   Acesse o editor de GPTs (geralmente em "Explore" > "Create a GPT").
    *   Na aba "Configure", defina um nome para o seu GPT (ex: "Engenheiro de Prompts Jurídicos Pro").
    *   No campo "Instructions", copie e cole **todo o conteúdo** do arquivo `1- System Prompt.md`.
2.  **Disponibilizar a Base de Conhecimento:**
    *   Na seção "Knowledge" do configurador do Custom GPT, clique em "Upload files".
    *   Faça o upload dos seguintes arquivos:
        *   `2- Preferencias de Formatacao Prompt.md`
        *   `3- Modulo_QA.md`
        *   `4- Templates_e_Exemplos.md`
    *   Certifique-se de que a opção "Code Interpreter" ou "Retrieval" (dependendo da interface atual da OpenAI) esteja habilitada para permitir que o GPT acesse o conteúdo desses arquivos.
3.  **Testar e Salvar:**
    *   Utilize a janela de "Preview" para testar algumas das funcionalidades (ex: `#prompt Crie um prompt para...`).
    *   Salve o seu Custom GPT (escolha a visibilidade: "Only me", "Anyone with a link", ou "Public").

#### Método 2: Usando "Custom Instructions" (Para Usuários Individuais sem acesso à criação de GPTs)

1.  **Configurar Custom Instructions:**
    *   Acesse as configurações do seu perfil ChatGPT e procure por "Custom Instructions".
    *   No campo destinado a "What would you like ChatGPT to know about you to provide better responses?" (ou instrução similar sobre como o ChatGPT deve se comportar), copie e cole **todo o conteúdo** do arquivo `1- System Prompt.md`.
2.  **Disponibilizar a Base de Conhecimento (Manualmente no Chat):**
    *   Como as "Custom Instructions" não suportam upload de arquivos, você precisará fornecer o conteúdo dos arquivos `2`, `3` e `4` no início de cada sessão de chat ou quando relevante.
    *   **Exemplo de abordagem:** Ao iniciar uma nova conversa, você pode dizer:
        ```
        Antes de começarmos, considere as seguintes informações como parte da sua base de conhecimento para esta sessão:

        <CONTEUDO_DO_ARQUIVO_2-PREFERENCIAS_DE_FORMATACAO_PROMPT.MD>
        [Cole aqui o conteúdo completo do arquivo 2]
        </CONTEUDO_DO_ARQUIVO_2-PREFERENCIAS_DE_FORMATACAO_PROMPT.MD>

        <CONTEUDO_DO_ARQUIVO_3-MODULO_QA.MD>
        [Cole aqui o conteúdo completo do arquivo 3]
        </CONTEUDO_DO_ARQUIVO_3-MODULO_QA.MD>

        <CONTEUDO_DO_ARQUIVO_4-TEMPLATES_E_EXEMPLOS.MD>
        [Cole aqui o conteúdo completo do arquivo 4]
        </CONTEUDO_DO_ARQUIVO_4-TEMPLATES_E_EXEMPLOS.MD>

        Agora, estou pronto para usar o Engenheiro de Prompts Jurídicos.
        ```
    *   **Nota:** Este método pode consumir uma parte significativa da janela de contexto do modelo. Para tarefas complexas, pode ser necessário fornecer apenas as seções mais relevantes dos arquivos de conhecimento.

#### Método 3: API da OpenAI

1.  **System Message:**
    *   Ao fazer chamadas para a API, utilize o conteúdo do arquivo `1- System Prompt.md` como a mensagem de sistema (`system message`).
2.  **Fornecendo Contexto Adicional:**
    *   Para os arquivos `2`, `3` e `4`, você pode:
        *   Incluir seus conteúdos como parte de uma mensagem de usuário (`user message`) no início da conversa.
        *   Se estiver usando técnicas de RAG (Retrieval Augmented Generation), adicione esses documentos à sua base de vetores para que possam ser recuperados e injetados no contexto do prompt conforme necessário.

---

```

## ⚠️ Aviso Legal Importante

*   Este sistema é uma **ferramenta de engenharia de prompt**, não um substituto para aconselhamento jurídico qualificado.
*   Ele **não fornece consultoria, pareceres ou estratégias legais**. Seu propósito é ajudar a *formular as perguntas certas* para outras IAs.
*   Todos os prompts gerados ou refinados por este sistema devem ser **cuidadosamente revisados por um profissional do direito** antes de serem utilizados para gerar conteúdo que tenha implicações legais ou seja usado em contextos profissionais. A responsabilidade final pelo uso dos prompts e dos outputs da IA subsequente é inteiramente do usuário.

## ⚖️ Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).

---

**Última atualização:** 23/05/25 (v2.9)
