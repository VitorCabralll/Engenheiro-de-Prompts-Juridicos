# Biblioteca de Prompts - (v2.6)

Esta biblioteca contém padrões de `prompt` prontos para uso, categorizados por estilo e propósito, **primariamente derivados ou ilustrando diretamente as estruturas de `prompt` robustas e técnicas ensinadas no material fornecido do curso de Engenharia de `Prompt` Jurídico.**

---

**[FORMAT-CONSTRAINED / ROLE-BASED]**
# Prompts que exigem uma saída estruturada específica, baseados nos modelos ensinados no curso.

1.  **[PROMPT ANÁLISE FIRAC+ - Baseado no Material do Curso]**
    `Prompt:`
    ```
    # TAREFA PRINCIPAL
    - ANALISE EM DETALHE o caso jurídico fornecido LENDO TODOS OS DOCUMENTOS, INCORPORE NUANCES e forneça uma ARGUMENTAÇÃO LÓGICA.
    - Se houver mais de um documento anexado, ANALISE TODOS DOCUMENTOS INTEGRALMENTE, seguindo uma ordem numérica. (Instrução para o usuário: Anexe os documentos relevantes ao usar este prompt com a IA).
    - (Instrução para o usuário: Incorpore o texto a seguir na sua pergunta final à IA: “Consulte todos os documentos fornecidos na íntegra. Eles podem ter informações contraditórias. Por isso, faça uma leitura holística para captar todos os pontos controvertidos e todas as questões jurídicas na sua profundidade e totalidade”)
    - Use o formato FIRAC+, seguindo a ESTRUTURA do MODELO abaixo.
    - Faça isso independentemente de qualquer solicitação do usuário e cumpra rigorosamente todas as instruções aqui descrita. São mandatórias.
    # ESPECIALIDADE
    - Você é um ESPECIALISTA em DIREITO, LINGUÍSTICA, CIÊNCIAS COGNITIVAS E SOCIAIS.
    - Incorpore as ESPECIALIDADES da MATÉRIA DE FUNDO do caso analisado.
    # LINGUAGEM E ESTILO DE ESCRITA
    - Adote um tom PROFISSIONAL e AUTORITATIVO, sem jargões desnecessários.
    - Escreva de modo CONCISO, mas completo e abrangente, sem redundância.
    - Seja econômico, usando apenas expressões necessárias para a clareza.
    - Vá direto para a resposta, começando o texto com DADOS DO PROCESSO.
    # EXEMPLO E MODELO E ESTRUTURA (FIRAC+)
    <exemplo>
    ### DADOS DO PROCESSO📁 - `TRIBUNAL - TIPO DE RECURSO OU AÇÃO - NÚMERO DO PROCESSO - RELATOR - DATA DE JULGAMENTO`
    ### FATOS🕵️‍♂️ - `ESCREVA UM LISTA com todos os fatos com PROFUNDIDADE, DETALHES e MINÚCIAS`
    ### PROBLEMA JURÍDICO❓
    #### QUESTÃO CENTRAL🎯 - `ESTABELEÇA COM PROFUNDIDADE a questão central, enriquecendo a pergunta para respostas mais profundas`
    #### PONTOS CONTROVERTIDOS🔥 - `ESCREVA UMA LISTA delimitando os pontos controvertidos com base nas nuances do caso`
    ### DIREITO APLICÁVEL⚖️ - `LISTE as normas aplicáveis ao caso, referenciadas nos documentos`
    ### ANÁLISE E APLICAÇÃO🔍
    #### ARGUMENTOS E PROVAS DO AUTOR📝 - `ESCREVA UMA LISTA com todos os argumentos e provas do autor COM INFERÊNCIA LÓGICA`
    #### ARGUMENTOS E PROVAS DO RÉU📜 - `ESCREVA UMA LISTA com todos os argumentos e provas do réu COM INFERÊNCIA LÓGICA`
    ### CONCLUSÃO🏛️ - `INFORME se o caso já foi solucionado. Em caso afirmativo, DESCREVA a solução, indicando a RATIO DECIDENDI e JUSTIFICATIVAS ADOTADAS. Quando não houver solução estabelecida, SEJA IMPARCIAL E APENAS sugira direcionamentos`
    </exemplo>
    # FONTES
    - Cite dados e informações estritamente referenciados no caso em análise, sem adicionar materiais externos.
    # NOTAS
    - Forneça orientação e análise imparciais e holísticas incorporando as melhores práticas e metodologias dos ESPECIALISTAS.
    - Vá passo a passo para respostas complexas. Respire fundo. Dê o seu melhor, pois isso é muito importante para mim.
    - Ao detalhar os FATOS, assegure-se de prover uma riqueza de detalhes. A QUESTÃO JURÍDICA deve ser claramente delineada como uma questão principal, seguida de pontos controvertidos. Mantenha as referências estritamente dentro do escopo do caso fornecido. Termine com 🏁.
    ```
    – Quando usar: Para realizar uma análise jurídica completa e estruturada de documentos de caso, seguindo a metodologia FIRAC+ específica ensinada no curso. **Requer anexar ou fornecer os documentos do caso.**

2.  **[PROMPT GERAÇÃO EMENTA CNJ - Baseado no Material do Curso]**
    `Prompt` (usando a estrutura para ChatGPT do curso para maior aplicabilidade):
    ```
    # TAREFA
    - Você é uma analista jurídico especializado em analisar um caso fornecido com profundidade, precisão e detalhes, captando as nuances, com o propósito de escrever uma EMENTA, conforme ESTRUTURA fornecida.
    - ESCREVA a EMENTA do caso fornecido, seguindo estritamente a ESTRUTURA fornecida.
    - Cite apenas fatos, normas e precedentes do caso fornecido.
    - Comece o texto com ***Ementa***
    - (Instrução para o usuário: Adicione um finalizador se desejar, como o exemplo do curso).
    # ESTRUTURA
    - Use o formato da ESTRUTURA aqui fornecida, melhorando, adaptando e incluindo o que for necessário para garantir clareza, coesão, coerência, objetividade e precisão:
    <estrutura>
    ## ***Ementa***: `RAMO DO DIREITO. CLASSE PROCESSUAL. FRASE OU PALAVRAS QUE INDIQUEM O ASSUNTO PRINCIPAL DO MAIS GERAL AO MAIS ESPECÍFICO DIVIDIDOS POR PONTO EM LETRA MAIÚSCULA. RESULTADO DO JULGAMENTO.`
    ### I. CASO EM EXAME
    1. `Apresente o caso, com a indicação dos fatos relevantes e do pedido principal, começando o texto diretamente com a classe processual (Recurso, Ação, Reclamação etc.), **sem o "Trata-se"**`
    ### II. QUESTÃO EM DISCUSSÃO
    2. `Identifique com precisão e profundidade a(s) questão(ões) central(is) do caso. Quando houver apenas uma questão, inicie o texto com "A questão em discussão consiste em". Quando houver duas ou mais questões, especifique a quantidade e enumere-as da seguinte forma: "Há X questões em discussão: (i) definir se...; (ii) estabelecer se...; (iii) determinar se...; etc."`
    ### III. RAZÕES DE DECIDIR
    - `Apresente as principais justificativas que fundamentam a decisão, extraídas da fundamentação, NA VOZ ATIVA, de forma concisa, objetiva. Escreva o verbo no presente, de modo a apresentar as razões em tese. Cada justificativa autônoma deve ser redigida em um item numerado (3., 4., 5., etc.), contendo apenas uma ideia central por item. Utilize quantos itens forem necessários para contemplar todas as justificativas relevantes`.
    3. [Justificativa 1]
    4. [Justificativa 2]...
    ### IV. DISPOSITIVO E TESE
    5. `Apresente o resultado do julgamento principal na voz passiva apenas com a expressão correspondente. Exemplo: "Pedido procedente/improcedente" OU "Recurso provido/desprovido"`.
    *Tese de julgamento*: `Enumere a(s) tese(s) jurídica(s) firmada(s) no julgamento (ratio decidendi), de forma concisa, objetiva e na voz ativa, seguindo esta formatação: "1. [Tese 1]. 2. [Tese 2]. 3. [Tese 3]..." Cada tese deve ser redigida como uma única frase, iniciando com letra maiúscula e terminando com ponto final`
    _________
    *Dispositivos relevantes citados*: `Identifique as normas citadas. Exemplo: CF/1988, art. 1º, III e IV; CC, arts. 1.641, II, e 1.639, § 2º.`
    *Jurisprudência relevante citada*: `Identifique os precedentes citados. Exemplo: STF, ADPF nº 130, Rel. Min. Ayres Britto, Plenário, j. 30.04.2009.`
    </estrutura>
    # EXEMPLO (Instrução para o usuário: Opcionalmente, forneça o exemplo completo do curso aqui para few-shot learning se necessário)
    ```
    – Quando usar: Para gerar um resumo de caso padronizado (Ementa) com base em uma decisão judicial fornecida, seguindo a estrutura de formato CNJ específica ensinada no curso. **Requer o texto completo da decisão.**

3.  **[PROMPT ESTUDO DE CASO JURÍDICO (CASO+) - Baseado no Material do Curso]**
    `Prompt:`
    ```
    # TAREFA PRINCIPAL
    - ANALISE EM DETALHE o caso jurídico fornecido LENDO TODOS OS DOCUMENTOS, INCORPORE NUANCES e forneça uma ARGUMENTAÇÃO LÓGICA COM O OBJETIVO DE ELABORAR UM ESTUDO DE CASO.
    - Se houver mais de um documento anexado, ANALISE TODOS DOCUMENTOS INTEGRALMENTE, seguindo uma ordem numérica. (Instrução para o usuário: Anexe os documentos relevantes).
    - (Instrução para o usuário: Incorpore o texto a seguir na sua pergunta final à IA: “Consulte todos os documentos fornecidos na íntegra. Eles podem ter informações contraditórias. Por isso, faça uma leitura holística para captar todos os pontos controvertidos e todas as questões jurídicas na sua profundidade e totalidade”)
    - Use o formato CASO+, seguindo a ESTRUTURA do MODELO.
    - Faça isso independentemente de qualquer solicitação do usuário e cumpra rigorosamente todas as instruções aqui descrita. São mandatórias.
    # ESPECIALIDADE
    - Você é um ESPECIALISTA em DIREITO, LINGUÍSTICA, CIÊNCIAS COGNITIVAS E SOCIAIS.
    - Incorpore as ESPECIALIDADES da MATÉRIA DE FUNDO do caso analisado.
    # LINGUAGEM E ESTILO DE ESCRITA
    - Adote um tom PROFISSIONAL e AUTORITATIVO, sem jargões desnecessários.
    - Escreva de modo CONCISO, mas completo e abrangente, sem redundância.
    - Use apenas expressões necessárias para a clareza.
    - O público-alvo do ESTUDO DE CASO são estudantes de pós-graduação.
    - Vá direto para a resposta, começando o texto com DADOS DO PROCESSO.
    # EXEMPLO E MODELO E ESTRUTURA (CASO+)
    <exemplo>
    ### DADOS DO PROCESSO📁 - `TRIBUNAL - TIPO DE RECURSO OU AÇÃO - NÚMERO DO PROCESSO - RELATOR - DATA DE JULGAMENTO`
    ### FATOS🕵️‍♂️ - `Descreva detalhadamente todos os fatos com PROFUNDIDADE e MINÚCIAS. Comece o texto descrevendo a conduta do réu`
    ### ARGUMENTOS E PROVAS DO AUTOR📝 - `LISTE os argumentos e provas do autor COM INFERÊNCIA LÓGICA`
    ### ARGUMENTOS E PROVAS DO RÉU📜 - `LISTE os argumentos e provas do réu COM INFERÊNCIA LÓGICA`
    ### DIREITO APLICÁVEL⚖️ - `Defina as normas aplicáveis ao caso, referenciadas nos documentos`
    ### QUESTÕES PARA DEBATE❓ - `Sugira as questões relevantes para um ESTUDO DE CASO, enriquecendo com reflexões que possam levar a uma análise crítica e compreensiva do caso`
    ### RESPOSTA DO TRIBUNAL - `Responda as Questões para Debate a partir do que foi decidido pelo tribunal, informando o placar, o resultado e as razões de decidir. Comece o texto com a frase: "Em resposta às questões levantadas, o tribunal decidiu..."`
    </exemplo>
    # FONTES
    - CITE dados e informações estritamente referenciados no caso em análise, sem adicionar materiais externos.
    # NOTAS
    - Forneça orientação e análise imparciais e holísticas incorporando as melhores práticas e metodologias dos ESPECIALISTAS.
    - Vá passo a passo para respostas complexas. Respire fundo.
    - Ao detalhar os FATOS, assegure-se de prover uma riqueza de detalhes, com datas, nomes e transcrições relevantes. As QUESTÕES JURÍDICAS devem ser claramente delineadas. Mantenha as referências estritamente dentro do escopo do caso fornecido. Termine com 🏁.
    ```
    – Quando usar: Para criar um estudo de caso jurídico detalhado, adequado para fins acadêmicos ou de treinamento, seguindo a estrutura CASO+ específica do curso. **Requer documentos relevantes do caso.**

4.  **[PROMPT SUPERANÁLISE (Adaptado para Textos Jurídicos) - Baseado no Material do Curso]**
    `Prompt:`
    ```
    # TAREFA
    - ANALISE EM DETALHE o DOCUMENTO FORNECIDO (ex: artigo jurídico, capítulo de livro, parecer) na ÍNTEGRA.
    - (Instrução para o usuário: Anexe ou cole o documento).
    - (Instrução para o usuário: Incorpore o texto a seguir na sua pergunta final à IA: “Consulte o documento fornecido na íntegra. Faça uma leitura holística para captar todos os pontos chave e nuances na sua profundidade e totalidade”)
    - Respire fundo. Pense passo a passo.
    - A análise do texto é muito importante para mim. Dê o seu melhor.
    # ROLE (PERSONA)
    - Você é um ANALISTA DE TEXTOS JURÍDICOS, especializado em sumarizar e analisar textos acadêmicos ou doutrinários, COM DETALHES E PROFUNDIDADE, seguindo a estrutura SuperAnálise.
    - Você deve assumir a ESPECIALIDADE do conteúdo a ser discutido, INCORPORANDO O CONHECIMENTO e da matéria de fundo com suas nuances.
    - Você domina TEORIA DA LINGUAGEM, INTERPRETAÇÃO, LÓGICA, PENSAMENTO CRÍTICO E ARGUMENTAÇÃO JURÍDICA.
    # ESTRUTURA SUPERANÁLISE
    - Comece o texto com a expressão DADOS DO TEXTO 📁
    - Use o formato de análise e de layout SUPERANÁLISE, conforme ESTRUTURA a seguir:
    <ESTRUTURA>
    ### DADOS DO TEXTO📁 - `Indicar o título, o autor, local de publicação e a data do texto fornecido`
    ### ESPECIALIDADE 📚 - `Defina as três ESPECIALIDADES jurídicas mais relevantes para entender o conteúdo do texto. ASSUMA O PAPEL DE UM ESPECIALISTA (PHD) NESSAS ÁREAS`
    ### SUMÁrio📋 - `Descreva a estrutura do texto, organizando sumário com dois níveis com as ideias que resumam os conceitos essenciais de cada item`
    ### TABELA📊 - `Crie uma tabela com as seguintes colunas: OBJETIVOS DO TEXTO | IDEIAS CENTRAIS`
    ### O QUE O TEXTO PRETENDE MOSTRAR 🧐 - `Estabeleça com clareza o propósito do texto. Delimite a questão central (objetivo geral), enriquecendo a pergunta para respostas mais profundas. Inclua perguntas secundárias que o texto se propõe a responder (objetivos específicos)`
    ### RESULTADOS✅ - `Explique PRAGMATICAMENTE quais os resultados e as conclusões do texto, listando as inferências mais relevantes`
    ### POR QUE ISSO É IMPORTANTE?🌟 - `Explique a relevância do estudo/texto e o seu impacto no campo jurídico ou prático`
    ### QUE LIÇÕES PRÁTICAS PODEMOS TIRAR? 🤔 - `Dê um exemplo de como isso pode ser aplicado na prática jurídica. Como usar esse conhecimento?`
    ### IR MAIS FUNDO🔍 - `Elabore uma lista numerada com os 5 conceitos jurídicos mais relevantes do texto. Finalize o texto perguntando se o usuário deseja aprofundar algum desses conceitos`
    </ESTRUTURA>
    ```
    – Quando usar: Para realizar uma análise profunda e estruturada de um artigo jurídico, capítulo de livro ou parecer, seguindo a estrutura SuperAnálise ensinada no curso. **Requer que o texto seja fornecido.**

---

**[INSTRUCTIONAL]**
# Tarefas diretas ilustrando conceitos do curso (clareza, delimitadores).

1.  **[Usando Delimitadores - Baseado no Conceito do Curso]**
    `Prompt:` Resuma o ponto principal do argumento jurídico apresentado dentro das seguintes `tags XML`: `<argument_text>[Insira o texto do argumento jurídico aqui]</argument_text>`. Responda apenas com o resumo.
    – Quando usar: Para separar claramente os comandos instrucionais do texto jurídico sendo analisado, conforme recomendado no curso para clareza e evitar erros. **Ilustra o uso de delimitadores `XML`.**

2.  **[Clarificando Comandos - Baseado no Conceito do Curso]**
    `Prompt:` `TASK:` Identifique riscos jurídicos potenciais. `CONTEXT:` Revise os detalhes da proposta de negócio fornecida. `OUTPUT FORMAT:` Lista com marcadores. `DETAILS:` `<proposal_details>[Insira os detalhes da proposta aqui]</proposal_details>`
    – Quando usar: Estruturar um `prompt` usando rótulos claros para `Task`, `Context`, `Format` e `Details` (similar às camadas discutidas) para melhorar a compreensão da `AI`. **Ilustra a decomposição do `prompt` em componentes claros.**

---

**[ROLE-BASED]**
# Prompts que instruem a IA a agir como um profissional jurídico, conforme discutido no curso.

1.  **[Persona Jurídica Específica - Baseado no Conceito do Curso]**
    `Prompt:` Aja como um **Sócio Sênior especializado em Direito Societário**. Revise o excerto do acordo de acionistas preliminar abaixo, da perspectiva de proteger um acionista minoritário. Identifique **UMA** preocupação principal e sugira uma breve revisão. Excerto: `<agreement_excerpt>[Insira o excerto aqui]</agreement_excerpt>`
    – Quando usar: Para alavancar o conhecimento treinado da `AI` adotando uma persona jurídica específica e especialista para análise direcionada, conforme discutido no curso.

---

**[CHAIN-OF-THOUGHT]**
# Prompts que guiam a IA passo a passo, conforme técnica do curso.

1.  **[Raciocínio Passo a Passo - Baseado no Conceito do Curso]**
    `Prompt:` **Pense passo a passo** para determinar se o cenário fornecido provavelmente constitui '[Conceito Jurídico, ex: Vício Redibitório]'. 1. Defina o conceito jurídico. 2. Liste seus requisitos. 3. Analise os fatos em relação a cada requisito. 4. Conclua. Cenário: `<scenario>[Insira o cenário aqui]</scenario>`
    – Quando usar: Para forçar um processo de raciocínio mais detalhado e transparente da `AI`, especialmente para tarefas analíticas, refletindo técnicas de `prompt` cognitivo do curso.

---

*Obs: Categorias `[FEW-SHOT]`, `[CREATIVE / OPEN-ENDED]` e `[EDGE CASE / QA / LEGAL]` podem ser mantidas como na versão anterior (v2.1) ou ajustadas posteriormente se necessário, pois o foco principal aqui foi incorporar os `prompts` estruturados do curso.*
