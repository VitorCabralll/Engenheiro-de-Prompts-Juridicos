# Templates e Exemplos - v2.8

Este arquivo contém **templates estruturados** para tarefas jurídicas complexas e gerais, bem como **exemplos completos ou ilustrativos** de prompts. Serve como a principal fonte de consulta para o Engenheiro de Prompts Jurídicos ao gerar novas sugestões de prompt (`#prompt`) ou ao explicar estruturas (`#learn`).

---

## Seção 1: Templates Jurídicos Estruturados (Métodos Nomeados)

Esta seção detalha os templates para metodologias de análise e sumarização específicas ensinadas, fornecendo tanto a estrutura base reutilizável quanto um exemplo completo do prompt.

---

### 1.1 Análise FIRAC+

*Use quando precisar de uma análise jurídica estruturada de documentos de um caso, seguindo a metodologia FIRAC+.*
**Nota Importante:** Requer fornecer os documentos do caso completos. Se usar multiplos documentos, o prompt deve solicitar uma leitura holistica.

**1.1.1 TEMPLATE ESTRUTURA (FIRAC+)**
*(Esta é a estrutura base com placeholders para preenchimento)*

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
- Assuma a `persona` de um ESPECIALISTA em [AREA DO DIREITO RELEVANTE, ex: Direito Civil, Processo Penal] e tambem em DIREITO, LINGUISTICA, CIENCIAS COGNITIVAS E SOCIAIS.

# LINGUAGEM E ESTILO (Output Style)
- Tom: PROFISSIONAL e AUTORITATIVO.
- Estilo: CONCISO, completo, sem redundâncias.
- Início: Comece diretamente com 'DADOS DO PROCESSO'.

# ESTRUTURA DE SAÍDA (FIRAC+)
- Siga RIGOROSAMENTE a seguinte estrutura:
  ### DADOS DO PROCESSO📁 - `[TRIBUNAL - TIPO DE RECURSO/AÇÃO - NÚMERO - RELATOR - DATA]`
  ### FATOS🕵️‍♂️ - `[LISTA DETALHADA COM PROFUNDIDADE E MINÚCIAS]`
  ### PROBLEMA JURÍDICO❓
  #### QUESTÃO CENTRAL🎯 - `[DEFINIÇÃO PROFUNDA DA QUESTÃO PRINCIPAL]`
  #### PONTOS CONTROVERTIDOS🔥 - `[LISTA DOS PONTOS CONTROVERTIDOS]`
  ### DIREITO APLICÁVEL⚖️ - `[LISTA DAS NORMAS APLICÁVEIS REFERENCIADAS]`
  ### ANÁLISE E APLICAÇÃO🔍
  #### ARGUMENTOS E PROVAS DO AUTOR📝 - `[LISTA COM INFERÊNCIA LÓGICA]`
  #### ARGUMENTOS E PROVAS DO RÉU📜 - `[LISTA COM INFERÊNCIA LÓGICA]`
  ### CONCLUSÃO🏛️ - `[SOLUÇÃO (SE HOUVER, COM RATIO/JUSTIFICATIVAS) OU DIRECIONAMENTOS IMPARCIAIS]`

# FONTES
- Baseie-se ESTRITAMENTE nos documentos fornecidos.

# NOTAS ADICIONAIS (Cognitive/Emotional Prompts)
- Vá passo a passo. Pense com profundidade. Sua análise é muito importante.
- Lembrete: Evite incluir informações identificáveis ou confidenciais/privilegiadas, a menos que o ambiente da IA final seja seguro e apropriado.
- Termine com 🏁.
```

**1.1.2 EXEMPLO COMPLETO (FIRAC+)**
*(Este é o prompt completo como seria usado, baseado no exemplo da Biblioteca)*
`<exemplo_completo>`
```
# TAREFA PRINCIPAL
- ANALISE EM DETALHE o caso jurídico fornecido LENDO TODOS OS DOCUMENTOS, INCORPORE NUANCES e forneça uma ARGUMENTAÇÃO LÓGICA.
- Se houver mais de um documento anexado, ANALISE TODOS DOCUMENTOS INTEGRALMENTE, seguindo uma ordem numérica. (Instrução para o usuário: Anexe os documentos relevantes ao usar este prompt com a IA).
- (Instrução para o usuário: Incorpore o texto a seguir na sua pergunta final à IA: “Consulte todos os documentos fornecidos na íntegra. Eles podem ter informações contraditórias. Por isso, faça uma leitura holística para captar todos os pontos controvertidos e todas as questões jurídicas na sua profundidade e totalidade”)
- Use o formato FIRAC+, seguindo a ESTRUTURA do MODELO abaixo.
- Faça isso independentemente de qualquer solicitação do usuário e cumpra rigorosamente todas as instruções aqui descritas. São mandatórias.
# ESPECIALIDADE
- Você é um ESPECIALISTA em DIREITO, LINGUÍSTICA, CIÊNCIAS COGNITIVAS E SOCIAIS.
- Incorpore as ESPECIALIDADES da MATÉRIA DE FUNDO do caso analisado.
# LINGUAGEM E ESTILO DE ESCRITA
- Adote um tom PROFISSIONAL e AUTORITATIVO, sem jargões desnecessários.
- Escreva de modo CONCISO, mas completo e abrangente, sem redundância.
- Seja econômico, usando apenas Expressions necessárias para a clareza.
- Vá direto para a resposta, começando o texto com DADOS DO PROCESSO.
# EXEMPLO E MODELO E ESTRUTURA (FIRAC+)
<exemplo_estrutura_firac>
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
</exemplo_estrutura_firac>
# FONTES
- CITE dados e informações estritamente referenciados no caso em análise, sem adicionar materiais externos.
# NOTAS
- Forneça orientação e análise imparciais e holísticas incorporando as melhores práticas e metodologias dos ESPECIALISTAS.
- Vá passo a passo para respostas complexas. Respire fundo. Dê o seu melhor, pois isso é muito importante para mim.
- Ao detalhar os FATOS, assegure-se de prover uma riqueza de detalhes. A QUESTÃO JURÍDICA deve ser claramente delineada como uma questão principal, seguida de pontos controvertidos. Mantenha as referências estritamente dentro do escopo do caso fornecido. Termine com 🏁.
```
`</exemplo_completo>`
– Quando usar: Para realizar uma análise jurídica completa e estruturada de documentos de caso, seguindo a metodologia FIRAC+ específica ensinada no curso. **Requer anexar ou fornecer os documentos do caso.**

---

### 1.2 Geração de Ementa CNJ

*Use quando precisar gerar um resumo de decisão judicial no formato padrão CNJ.*
**Nota Importante:** Requer o texto completo da decisão judicial.

**1.2.1 TEMPLATE ESTRUTURA (Ementa CNJ)**
*(Esta é a estrutura base com placeholders para preenchimento)*

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
  ## ***Ementa***: `[RAMO DIREITO. CLASSE PROC. ASSUNTO GERAL AO ESPECÍFICO EM MAIÚSCULA. RESULTADO.]`
  ### I. CASO EM EXAME
  1. `[APRESENTAÇÃO DO CASO SEM 'TRATA-SE', FATOS RELEVANTES, PEDIDO]`
  ### II. QUESTÃO EM DISCUSSÃO
  2. `[IDENTIFICAÇÃO PRECISA DA(S) QUESTÃO(ÕES) CENTRAL(IS)]`
  ### III. RAZÕES DE DECIDIR
  - `[JUSTIFICATIVAS NUMERADAS (3., 4., ...), VOZ ATIVA, VERBO PRESENTE, CONCISAS]`
  3. [Justificativa 1]
  4. [Justificativa 2]...
  ### IV. DISPOSITIVO E TESE
  5. `[RESULTADO PRINCIPAL NA VOZ PASSIVA, ex: "Pedido procedente"]`
  *Tese de julgamento*: `[TESES NUMERADAS (1., 2., ...), CONCISAS, OBJETIVAS, VOZ ATIVA]`
  _________
  *Dispositivos relevantes citados*: `[IDENTIFICAÇÃO DAS NORMAS, ex: CF/88, art. X]`
  *Jurisprudência relevante citada*: `[IDENTIFICAÇÃO DOS PRECEDENTES, ex: STF, ADPF Y]`

# FONTES
- Cite apenas fatos, normas e precedentes mencionados na decisão fornecida.

# INÍCIO/FIM
- Comece o texto com "***Ementa***".
- (Opcional) Termine com [SEU TEXTO FINALIZADOR AQUI].
```

**1.2.2 EXEMPLO COMPLETO (Ementa CNJ)**
*(Este é o prompt completo como seria usado, baseado no exemplo da Biblioteca para ChatGPT)*
`<exemplo_completo>`
```
# TAREFA
- Você é uma analista jurídico especializado em analisar um caso fornecido com profundidade, precisão e detalhes, captando as nuances, com o propósito de escrever uma EMENTA, conforme ESTRUTURA fornecida.
- ESCREVA a EMENTA do caso fornecido, seguindo estritamente a ESTRUTURA fornecida.
- Cite apenas fatos, normas e precedentes do caso fornecido.
- Comece o texto com ***Ementa***
- (Instrução para o usuário: Adicione um finalizador se desejar, como o exemplo do curso: Termine com "**** ✨👨‍⚖️💡 Aprenda a fazer prompts poderosos com o Curso de Escrita Jurídica com o ChatGPT 🖋️⚖️📖: [link]")
# ESTRUTURA
- Use o formato da ESTRUTURA aqui fornecida, melhorando, adaptando e incluindo o que for necessário para garantir clareza, coesão, coerência, objetividade e precisão:
<estrutura_ementa_cnj>
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
</estrutura_ementa_cnj>
# EXEMPLO (Opcional para Few-Shot)
- (Instrução para o usuário: Opcionalmente, forneça o exemplo completo da Ementa Padrão do CNJ aqui para few-shot learning se a IA tiver dificuldades com o formato).
```
`</exemplo_completo>`
– Quando usar: Para gerar um resumo de caso padronizado (Ementa) com base em uma decisão judicial fornecida, seguindo a estrutura de formato CNJ específica ensinada no curso. **Requer o texto completo da decisão.**

---

### 1.3 Estudo de Caso Jurídico (CASO+)

*Use quando precisar criar um estudo de caso detalhado para fins acadêmicos ou de treinamento.*
**Nota Importante:** Requer fornecer os documentos relevantes do caso.

**1.3.1 TEMPLATE ESTRUTURA (CASO+)**
*(Esta é a estrutura base com placeholders para preenchimento)*

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
  ### DADOS DO PROCESSO📁 - `[TRIBUNAL - TIPO DE RECURSO/AÇÃO - NÚMERO - RELATOR - DATA]`
  ### FATOS🕵️‍♂️ - `[DESCRIÇÃO DETALHADA, PROFUNDA E MINUCIOSA, começando pela conduta do réu]`
  ### ARGUMENTOS E PROVAS DO AUTOR📝 - `[LISTA COM INFERÊNCIA LÓGICA]`
  ### ARGUMENTOS E PROVAS DO RÉU📜 - `[LISTA COM INFERÊNCIA LÓGICA]`
  ### DIREITO APLICÁVEL⚖️ - `[DEFINIÇÃO DAS NORMAS APLICÁVEIS REFERENCIADAS]`
  ### QUESTÕES PARA DEBATE❓ - `[SUGESTÃO DE QUESTÕES RELEVANTES, COM REFLEXÕES CRÍTICAS]`
  ### RESPOSTA DO TRIBUNAL - `[RESPOSTA ÀS QUESTÕES BASEADA NA DECISÃO (PLACAR, RESULTADO, RAZÕES), começando com "Em resposta às questões levantadas..."]`

# FONTES
- Baseie-se ESTRITAMENTE nos documentos fornecidos.

# NOTAS ADICIONAIS (Cognitive/Emotional Prompts)
- Vá passo a passo. Pense com profundidade. Detalhe bem os fatos.
- Lembrete: Evite incluir informações identificáveis ou confidenciais/privilegiadas, a menos que o ambiente da IA final seja seguro e apropriado.
- Termine com 🏁.
```

**1.3.2 EXEMPLO COMPLETO (CASO+)**
*(Este é o prompt completo como seria usado, baseado no exemplo da Biblioteca)*
`<exemplo_completo>`
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
- Use apenas Expressions necessárias para a clareza.
- O público-alvo do ESTUDO DE CASO são estudantes de pós-graduação.
- Vá direto para a resposta, começando o texto com DADOS DO PROCESSO.
# EXEMPLO E MODELO E ESTRUTURA (CASO+)
<exemplo_estrutura_caso_plus>
### DADOS DO PROCESSO📁 - `TRIBUNAL - TIPO DE RECURSO OU AÇÃO - NÚMERO DO PROCESSO - RELATOR - DATA DE JULGAMENTO`
### FATOS🕵️‍♂️ - `Descreva detalhadamente todos os fatos com PROFUNDIDADE e MINÚCIAS. Comece o texto descrevendo a conduta do réu`
### ARGUMENTOS E PROVAS DO AUTOR📝 - `LISTE os argumentos e provas do autor COM INFERÊNCIA LÓGICA`
### ARGUMENTOS E PROVAS DO RÉU📜 - `LISTE os argumentos e provas do réu COM INFERÊNCIA LÓGICA`
### DIREITO APLICÁVEL⚖️ - `Defina as normas aplicáveis ao caso, referenciadas nos documentos`
### QUESTÕES PARA DEBATE❓ - `Sugira as questões relevantes para um ESTUDO DE CASO, enriquecendo com reflexões que possam levar a uma análise crítica e compreensiva do caso`
### RESPOSTA DO TRIBUNAL - `Responda as Questões para Debate a partir do que foi decidido pelo tribunal, informando o placar, o resultado e as razões de decidir. Comece o texto com a frase: "Em resposta às questões levantadas, o tribunal decidiu..."`
</exemplo_estrutura_caso_plus>
# FONTES
- CITE dados e informações estritamente referenciados no caso em análise, sem adicionar materiais externos.
# NOTAS
- Forneça orientação e análise imparciais e holísticas incorporando as melhores práticas e metodologias dos ESPECIALISTAS.
- Vá passo a passo para respostas complexas. Respire fundo.
- Ao detalhar os FATOS, assegure-se de prover uma riqueza de detalhes, com datas, nomes e transcrições relevantes. As QUESTÕES JURÍDICAS devem ser claramente delineadas. Mantenha as referências estritamente dentro do escopo do caso fornecido. Termine com 🏁.
```
`</exemplo_completo>`
– Quando usar: Para criar um estudo de caso jurídico detalhado, adequado para fins acadêmicos ou de treinamento, seguindo a estrutura CASO+ específica do curso. **Requer documentos relevantes do caso.**

---

### 1.4 SuperAnálise (Textos Jurídicos)

*Use para uma análise profunda e estruturada de artigos, capítulos de livros ou pareceres jurídicos.*
**Nota Importante:** Requer fornecer o texto completo a ser analisado.

**1.4.1 TEMPLATE ESTRUTURA (SuperAnálise)**
*(Esta é a estrutura base com placeholders para preenchimento)*

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
  ### DADOS DO TEXTO📁 - `[TÍTULO, AUTOR, PUBLICAÇÃO, DATA]`
  ### ESPECIALIDADE 📚 - `[3 ESPECIALIDADES JURÍDICAS RELEVANTES]`
  ### SUMÁRIO📋 - `[SUMÁRIO ESTRUTURADO EM DOIS NÍVEIS]`
  ### TABELA📊 - `[TABELA COM COLUNAS: OBJETIVOS DO TEXTO | IDEIAS CENTRAIS]`
  ### O QUE O TEXTO PRETENDE MOSTRAR 🧐 - `[PROPÓSITO, QUESTÃO CENTRAL, QUESTÕES SECUNDÁRIAS]`
  ### RESULTADOS✅ - `[CONCLUSÕES PRAGMÁTICAS, INFERÊNCIAS RELEVANTES]`
  ### POR QUE ISSO É IMPORTANTE?🌟 - `[RELEVÂNCIA, IMPACTO NO CAMPO JURÍDICO/PRÁTICO]`
  ### QUE LIÇÕES PRÁTICAS PODEMOS TIRAR? 🤔 - `[APLICAÇÃO PRÁTICA, EXEMPLO DE USO]`
  ### IR MAIS FUNDO🔍 - `[LISTA NUMERADA DOS 5 CONCEITOS JURÍDICOS RELEVANTES + PERGUNTA FINAL]`

# NOTAS ADICIONAIS (Cognitive/Emotional Prompts)
- Pense passo a passo. Sua análise é muito importante. Dê o seu melhor.
```

**1.4.2 EXEMPLO COMPLETO (SuperAnálise)**
*(Este é o prompt completo como seria usado, baseado no exemplo da Biblioteca)*
`<exemplo_completo>`
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
- Você domina TEORIA DA LINGUAGEM, INTERPRETAÇÃO, LÓGICA FORMAL E INFORMAL, PENSAMENTO CRÍTICO E ARGUMENTAÇÃO JURÍDICA.
# ESTRUTURA SUPERANÁLISE
- Comece o texto com a expressão DADOS DO TEXTO 📁
- Use o formato de análise e de layout SUPERANÁLISE, conforme ESTRUTURA a seguir:
<ESTRUTURA_SUPERANALISE>
### DADOS DO TEXTO📁 - `Indicar o título, o autor, local de publicação e a data do texto fornecido`
### ESPECIALIDADE 📚 - `Defina as três ESPECIALIDADES jurídicas mais relevantes para entender o conteúdo do texto. ASSUMA O PAPEL DE UM ESPECIALISTA (PHD) NESSAS ÁREAS`
### SUMÁRIO📋 - `Descreva a estrutura do texto, organizando sumário com dois níveis com as ideias que resumam os conceitos essenciais de cada item`
### TABELA📊 - `Crie uma tabela com as seguintes colunas: OBJETIVOS DO TEXTO | IDEIAS CENTRAIS`
### O QUE O TEXTO PRETENDE MOSTRAR 🧐 - `Estabeleça com clareza o propósito do texto. Delimite a questão central (objetivo geral), enriquecendo a pergunta para respostas mais profundas. Inclua perguntas secundárias que o texto se propõe a responder (objetivos específicos)`
### RESULTADOS✅ - `Explique PRAGMATICAMENTE quais os resultados e as conclusões do texto, listando as inferências mais relevantes`
### POR QUE ISSO É IMPORTANTE?🌟 - `Explique a relevância do estudo/texto e o seu impacto no campo jurídico ou prático`
### QUE LIÇÕES PRÁTICAS PODEMOS TIRAR? 🤔 - `Dê um exemplo de como isso pode ser aplicado na prática jurídica. Como usar esse conhecimento?`
### IR MAIS FUNDO🔍 - `Elabore uma lista numerada com os 5 conceitos jurídicos mais relevantes do texto. Finalize o texto perguntando se o usuário deseja aprofundar algum desses conceitos`
</ESTRUTURA_SUPERANALISE>

```
`</exemplo_completo>`
– Quando usar: Para realizar uma análise profunda e estruturada de um artigo jurídico, capítulo de livro ou parecer, seguindo a estrutura SuperAnálise ensinada no curso. **Requer que o texto seja fornecido.**

---

## Seção 2: Templates Jurídicos Gerais (Adaptados)

Esta seção contém templates mais flexíveis adaptados para tarefas jurídicas comuns que podem não exigir uma metodologia nomeada específica.

---

### 2.1 TEMPLATE: Instrução Abrangente Jurídica

*Use para tarefas jurídicas mais simples que não se encaixam nos modelos complexos acima.*
```
- `Role`/Persona: Você é um(a) [PAPEL JURÍDICO, ex: Advogado(a) Assistente].
- Tarefa (`Task`): Sua tarefa é [INSTRUÇÃO CLARA E DIRETA, ex: resumir os pontos principais, identificar cláusulas de X tipo, elaborar um esboço inicial de Y].
- Contexto (`Context`): Considere o seguinte contexto/documento: `<context>[INSIRA O CONTEXTO OU TEXTO CURTO AQUI]</context>`. (Para textos longos, use delimitadores claros e considere as preferências de Long Context).
- Jurisdição (`Jurisdiction`, se aplicável): [NOME DA JURISDIÇÃO].
- Formato de Saída (`Output Format`): Apresente a resposta como [FORMATO DESEJADO, ex: uma lista com marcadores, um parágrafo conciso, uma tabela simples].
- Tom/Estilo (`Tone`): Use um tom [TOM DESEJADO, ex: formal, objetivo, informativo].
- Público-Alvo (`Audience`, se aplicável): [PÚBLICO, ex: Sócio Sênior, Cliente].
- **Aterramento (se aplicável):** Baseie sua resposta estritamente no contexto fornecido e cite a fonte se fizer afirmações factuais. Indique se informações estão ausentes.
```
– Quando usar: Para estruturar rapidamente comandos para tarefas jurídicas bem definidas e de menor complexidade.

---

### 2.2 TEMPLATE: Baseado em Cenário Jurídico

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
- **Aterramento:** Baseie a análise nos fatos do cenário e documentos fornecidos. Indique se informações cruciais estão faltando para uma análise completa. Cite fontes específicas se possível.
```
– Quando usar: Para análises de risco, planejamento estratégico inicial ou exploração de hipóteses em um contexto jurídico definido.

---

### 2.3 TEMPLATE: Chain-of-Thought Jurídico

*Use para tarefas que exigem raciocínio jurídico explícito e passo a passo.*
```
- Tarefa (`Task`): [TAREFA ANALÍTICA, ex: Avaliar a aplicabilidade da Súmula X a este caso].
- Contexto/Fatos (`Context`): `<facts>[INSIRA OS FATOS RELEVANTES AQUI]</facts>`
- Jurisdição (`Jurisdiction`, se aplicável): [NOME DA JURISDIÇÃO].
- Instrução Cognitiva (`Cognitive Instruction`): Pense passo a passo (`Think step-by-step`) para [REPETIR A TAREFA]. Siga estas etapas:
  1. Enuncie a(s) regra(s)/princípio(s) jurídico(s) relevante(s) (ex: Súmula X, Art. Y da Lei Z). Cite a fonte.
  2. Identifique os requisitos/elementos essenciais da(s) regra(s).
  3. Analise como os fatos fornecidos se encaixam (ou não) em cada requisito/elemento essencial.
  4. Apresente uma conclusão preliminar fundamentada, indicando o nível de certeza com base na análise.
- Formato de Saída (`Output Format`): Resposta detalhada seguindo os passos acima, idealmente separando o raciocínio (passos 1-3) da conclusão final (passo 4), talvez usando tags como `<analysis>` e `<conclusion>`.
```
– Quando usar: Para aplicar leis/precedentes a fatos, analisar causalidade, ou qualquer tarefa que se beneficie de um raciocínio jurídico explícito e transparente.

---

### 2.4 TEMPLATE: Ajustado ao Público Jurídico

*Use para garantir que a linguagem e a profundidade da resposta sejam adequadas ao destinatário.*
```
- Tarefa (`Task`): [TAREFA, ex: Explicar o conceito de Prescrição Intercorrente].
- Público-Alvo (`Target Audience`): Escreva para um(a) [PÚBLICO ESPECÍFICO, ex: estagiário de direito, cliente leigo, juiz].
- Foco (`Focus`): Concentre-se em [ASPECTO PRINCIPAL, ex: os requisitos práticos, as consequências para o processo, a fundamentação legal].
- Tom/Estilo (`Tone`): Use um tom [TOM APROPRIADO, ex: didático e simples, formal e técnico, objetivo e direto].
- Restrições (`Constraints`, opcional): Evite jargões excessivos / Inclua referências legais / Mantenha abaixo de X palavras / **NÃO forneça aconselhamento jurídico, apenas explicação.**
- Formato de Saída (`Output Format`): [FORMATO, ex: texto corrido, lista de pontos chave].
```
– Quando usar: Para gerar textos (explicações, resumos, comunicações) que precisam ser cuidadosamente adaptados ao nível de conhecimento e necessidade do leitor, com atenção aos riscos de UPL.

---

### 2.5 TEMPLATE: Análise Comparativa Jurídica

*Use para comparar elementos específicos (cláusulas, decisões, argumentos, etc.) entre dois ou mais documentos ou textos jurídicos.*
```
- `Role`/Persona: Você é um(a) [PAPEL JURÍDICO, ex: Analista Jurídico, Advogado Comparatista].
- Tarefa (`Task`): Realize uma análise comparativa detalhada entre os seguintes itens fornecidos:
    <item_1>[INSIRA O TEXTO OU DESCRIÇÃO DO ITEM 1 AQUI, ex: Texto da Cláusula 5.1 do Contrato A]</item_1>
    <item_2>[INSIRA O TEXTO OU DESCRIÇÃO DO ITEM 2 AQUI, ex: Texto da Cláusula 5.1 do Contrato B]</item_2>
    ... (adicione mais itens se necessário)
- Critérios de Comparação (`Comparison Points`): Compare os itens acima especificamente em relação a:
    1. [Critério de Comparação 1, ex: Definição de 'Confidencial']
    2. [Critério de Comparação 2, ex: Prazo de Vigência da Obrigação]
    3. [Critério de Comparação 3, ex: Exceções Permitidas]
    ... (liste todos os pontos a serem comparados)
- Jurisdição (`Jurisdiction`, se aplicável): [NOME DA JURISDIÇÃO].
- Formato de Saída (`Output Format`): Apresente a comparação em uma tabela (`Markdown table`) com as colunas: "Critério de Comparação", "Item 1", "Item 2", "[Item N...]", "Observação/Diferença Principal".
- Tom/Estilo (`Tone`): Use um tom [TOM DESEJADO, ex: objetivo, analítico, claro].
- Público-Alvo (`Audience`, se aplicável): [PÚBLICO].
- **Aterramento:** Baseie a comparação estritamente nos textos/descrições fornecidos para cada item. Se um critério não for abordado em um item, indique "Não abordado" ou similar.
```
– Quando usar: Para análises detalhadas de semelhanças e diferenças entre textos legais, cláusulas contratuais, decisões judiciais ou argumentos sobre pontos específicos.

---

### 2.6 TEMPLATE: Geração de Opções Jurídicas

*Use para gerar rascunhos de textos jurídicos (cláusulas, parágrafos, abordagens) que apresentem alternativas baseadas em diferentes critérios ou objetivos.*
```
- `Role`/Persona: Você é um(a) [PAPEL JURÍDICO, ex: Advogado Consultor, Redator de Contratos].
- Tarefa (`Task`): Elabore [NÚMERO, ex: DUAS] opções de redação para [OBJETO DA REDAÇÃO, ex: uma cláusula de confidencialidade, um parágrafo sobre rescisão antecipada, uma abordagem para notificação extrajudicial].
- Contexto (`Context`): Considere o seguinte cenário/contexto: [DESCRIÇÃO DO CONTEXTO RELEVANTE, ex: Contrato de Software B2B, fase pré-litigiosa de disputa X].
- Jurisdição (`Jurisdiction`, se aplicável): [NOME DA JURISDIÇÃO].
- Critérios para as Opções (`Options Criteria`):
    - **Opção 1:** Deve priorizar/incluir [CRITÉRIO 1, ex: máxima proteção para a Parte A, um prazo mais curto, linguagem mais amigável].
    - **Opção 2:** Deve priorizar/incluir [CRITÉRIO 2, ex: equilíbrio entre as partes, um mecanismo de escalonamento, conformidade estrita com a norma Y].
    ... (adicione mais opções e critérios conforme necessário)
- Formato de Saída (`Output Format`): Apresente cada opção de redação claramente identificada (ex: "Opção 1: [Critério Priorizado]") seguida pelo texto da opção. Inclua um breve comentário (1-2 frases) após cada opção, explicando seu principal efeito prático ou o critério que ela atende.
- Tom/Estilo (`Tone`): Use um tom [TOM APROPRIADO, ex: formal e preciso, claro e direto].
- Público-Alvo (`Audience` para quem as opções serão apresentadas, se aplicável): [PÚBLICO].
- **Restrições Cruciais:**
    - As redações devem ser juridicamente sólidas e claras.
    - **NÃO indique qual opção é "melhor" ou recomendada.** Apenas apresente as alternativas conforme os critérios definidos.
    - **Evite fornecer aconselhamento jurídico direto.** Foque na elaboração das opções textuais.
```
– Quando usar: Para criar alternativas de redação ou abordagens que atendam a diferentes requisitos, estratégias ou níveis de risco, facilitando a tomada de decisão ou negociação. Essencial validar a adequação legal da redação final com um profissional.

---

## Seção 3: Exemplos Ilustrativos de Técnicas

Esta seção contém exemplos mais simples focados em ilustrar técnicas específicas de engenharia de prompt discutidas.

---

### 3.1 EXEMPLO: Uso de Delimitadores

*Ilustra como separar claramente comandos de conteúdo textual.*
`Prompt:` Resuma o ponto principal do argumento jurídico apresentado dentro das seguintes `tags XML`: `<argument_text>[Insira o texto do argumento jurídico aqui]</argument_text>`. Responda apenas com o resumo.
– Quando usar: Para ensinar ou demonstrar a importância de usar delimitadores claros (especialmente XML) ao fornecer texto para análise, prevenindo que a IA confunda o conteúdo com instruções.

---

### 3.2 EXEMPLO: Clareza nos Componentes do Prompt

*Ilustra como decompor um prompt em partes lógicas para maior clareza.*
`Prompt:`
`TASK:` Identifique riscos jurídicos potenciais.
`CONTEXT:` Revise os detalhes da proposta de negócio fornecida.
`JURISDICTION:` Brasil.
`OUTPUT FORMAT:` Lista com marcadores.
`DETAILS:` `<proposal_details>[Insira os detalhes da proposta aqui]</proposal_details>`
– Quando usar: Para demonstrar a prática de estruturar um prompt usando rótulos claros para seus componentes essenciais (Tarefa, Contexto, Formato, etc.), melhorando a compreensão da IA.

---

### 3.3 EXEMPLO: Persona Jurídica Simples

*Ilustra a aplicação básica de Role-Playing no contexto jurídico.*
`Prompt:` Aja como um **Advogado(a) Revisor(a) de Contratos**. Leia a cláusula abaixo e aponte **UM** termo que poderia ser considerado ambíguo. Cláusula: `<clause>[Insira a cláusula aqui]</clause>`
– Quando usar: Para demonstrar como atribuir um papel específico à IA pode direcionar seu foco e perspectiva na análise, mesmo em tarefas simples.

---

### 3.4 EXEMPLO: Chain-of-Thought Simples

*Ilustra a instrução básica para raciocínio passo a passo.*
`Prompt:` Qual o prazo prescricional para [Tipo de Ação Específica] sob a lei [Nome da Lei/Código]? **Pense passo a passo** antes de responder: 1. Identifique a norma aplicável. 2. Verifique se há regras especiais. 3. Declare o prazo.
– Quando usar: Para mostrar como a simples instrução "Pense passo a passo", especialmente com etapas sugeridas, pode levar a uma resposta mais fundamentada e menos propensa a erros de memória ou interpretação.

---
# Atualizado em: 03/05/25