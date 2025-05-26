# Templates e Exemplos - v2.8

Este arquivo contém **templates estruturados** para tarefas jurídicas complexas específicas (FIRAC+, Ementa CNJ, SuperAnálise), cada um com uma estrutura base e um exemplo completo. Serve como fonte de consulta para o Engenheiro de Prompts Jurídicos ao gerar novas sugestões de prompt (`#prompt`) ou ao explicar essas estruturas (`#learn`).

---

## Seção 1: Templates Jurídicos Estruturados (Métodos Nomeados)

Esta seção detalha os templates para metodologias de análise e sumarização específicas ensinadas, fornecendo tanto a estrutura base reutilizável quanto um exemplo completo do prompt.

---

### 1.1 Análise FIRAC+

*Use quando precisar de uma análise jurídica estruturada de documentos de um caso, seguindo a metodologia FIRAC+.*
**Nota Importante:** Requer fornecer os documentos do caso completos. Se usar multiplos documentos, o prompt deve solicitar uma leitura holistica.
**Para documentos muito extensos:** Se o documento for muito longo, considere aplicar técnicas de `chunking` ou meta-sumarização (conforme detalhado em `1- System Prompt.md` e `2- Preferencias de Formatacao de Prompt.md`), aplicando este template a porções menores e consolidando os resultados.
<!-- Exemplo de instrução para meta-sumarização (para o usuário adaptar):
<meta_sumarizacao>
  <passo1>Divida o documento em chunks de X paragraphs/paginas.</passo1>
  <passo2>Aplique o template de análise para cada chunk.</passo2>
  <passo3>Combine as análises dos chunks em um relatório consolidado, focando nos seguintes aspectos gerais: [Aspecto 1, Aspecto 2].</passo3>
</meta_sumarizacao>
-->

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

# CRITÉRIOS DE EXTRAÇÃO ESPECÍFICOS
<!-- Instrução para o usuário: Defina aqui critérios específicos para extração de informação, se necessário. Ex: Listar todas as datas mencionadas, extrair nomes de todas as partes e testemunhas, identificar valores monetários exatos. -->
<!-- Exemplo de Critérios (comente ou remova se não usar):
<criterios_extracao>
    <extrair item="datas_relevantes" />
    <extrair item="nomes_partes_testemunhas" />
    <extrair item="valores_monetarios" />
</criterios_extracao>
-->

# ROLE (PERSONA)
- Assuma a `persona` de um ESPECIALISTA em [AREA DO DIREITO RELEVANTE, ex: Direito Civil, Processo Penal] e tambem em DIREITO, LINGUISTICA, CIENCIAS COGNITIVAS E SOCIAIS.

# LINGUAGEM E ESTILO (Output Style)
- Tom: PROFISSIONAL e AUTORITATIVO.
- Estilo: CONCISO, completo, sem redundâncias.
- Início: Comece diretamente com 'DADOS DO PROCESSO'.

# ESTRUTURA DE SAÍDA (FIRAC+)
- Siga RIGOROSAMENTE a seguinte estrutura XML:
  <firac_plus>
    <dados_processo tribunal="[NOME DO TRIBUNAL]" tipo_recurso_acao="[TIPO DE RECURSO/AÇÃO]" numero_processo="[NÚMERO DO PROCESSO]" relator="[NOME DO RELATOR]" data_julgamento="[DATA DE JULGAMENTO]">
      <!-- Outras informações relevantes podem ser adicionadas como atributos ou elementos filhos -->
    </dados_processo>
    <fatos>
      <!-- LISTA DETALHADA COM PROFUNDIDADE E MINÚCIAS DOS FATOS RELEVANTES -->
      <fato>[FATO 1]</fato>
      <fato>[FATO 2]</fato>
      <!-- ... -->
    </fatos>
    <problema_juridico>
      <questao_central>
        <!-- DEFINIÇÃO PROFUNDA DA QUESTÃO PRINCIPAL -->
      </questao_central>
      <pontos_controvertidos>
        <!-- LISTA DOS PONTOS CONTROVERTIDOS -->
        <ponto_controvertido>[PONTO 1]</ponto_controvertido>
        <ponto_controvertido>[PONTO 2]</ponto_controvertido>
        <!-- ... -->
      </pontos_controvertidos>
    </problema_juridico>
    <direito_aplicavel>
      <!-- LISTA DAS NORMAS APLICÁVEIS REFERENCIADAS -->
      <norma>[NORMA 1, ex: Art. 5, CF/88]</norma>
      <norma>[NORMA 2]</norma>
      <!-- ... -->
    </direito_aplicavel>
    <analise_e_aplicacao>
      <argumentos_provas_autor>
        <!-- LISTA COM INFERÊNCIA LÓGICA DOS ARGUMENTOS E PROVAS DO AUTOR -->
        <argumento_autor>[ARGUMENTO 1]</argumento_autor>
        <prova_autor>[PROVA 1]</prova_autor>
        <!-- ... -->
      </argumentos_provas_autor>
      <argumentos_provas_reu>
        <!-- LISTA COM INFERÊNCIA LÓGICA DOS ARGUMENTOS E PROVAS DO RÉU -->
        <argumento_reu>[ARGUMENTO 1]</argumento_reu>
        <prova_reu>[PROVA 1]</prova_reu>
        <!-- ... -->
      </argumentos_provas_reu>
    </analise_e_aplicacao>
    <conclusao>
      <!-- SOLUÇÃO (SE HOUVER, COM RATIO/JUSTIFICATIVAS) OU DIRECIONAMENTOS IMPARCIAIS -->
    </conclusao>
  </firac_plus>

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
  <firac_plus>
    <dados_processo tribunal="TRIBUNAL EXEMPLO" tipo_recurso_acao="APELAÇÃO CÍVEL" numero_processo="1234567-89.2023.8.26.0000" relator="DES. EXEMPLO RELATOR" data_julgamento="01/01/2024">
      <!-- Informações específicas do caso aqui -->
    </dados_processo>
    <fatos>
      <fato>Descrição detalhada do fato 1, com minúcias.</fato>
      <fato>Descrição detalhada do fato 2, explorando nuances.</fato>
    </fatos>
    <problema_juridico>
      <questao_central>Definição aprofundada da questão jurídica principal que o caso levanta.</questao_central>
      <pontos_controvertidos>
        <ponto_controvertido>Ponto específico de desacordo ou debate 1.</ponto_controvertido>
        <ponto_controvertido>Ponto específico de desacordo ou debate 2.</ponto_controvertido>
      </pontos_controvertidos>
    </problema_juridico>
    <direito_aplicavel>
      <norma>Código Civil, Art. 186</norma>
      <norma>Constituição Federal, Art. 5, Inciso X</norma>
    </direito_aplicavel>
    <analise_e_aplicacao>
      <argumentos_provas_autor>
        <argumento_autor>Argumento chave do autor 1, com base na prova X.</argumento_autor>
        <prova_autor>Referência à prova documental Y que suporta o argumento 1.</prova_autor>
      </argumentos_provas_autor>
      <argumentos_provas_reu>
        <argumento_reu>Argumento chave do réu 1, contestando o fato Z.</argumento_reu>
        <prova_reu>Referência à testemunha W que corrobora o argumento 1.</prova_reu>
      </argumentos_provas_reu>
    </analise_e_aplicacao>
    <conclusao>Descrição da solução do caso, se houver, com ratio decidendi e justificativas. Se não solucionado, apresentar direcionamentos imparciais.</conclusao>
  </firac_plus>
</exemplo_estrutura_firac>
# FONTES
- CITE dados e informações estritamente referenciados no caso em análise, sem adicionar materiais externos.
# NOTAS
- Forneça análise imparcial e holística.
- Vá passo a passo para respostas complexas.
- Ao detalhar os FATOS, assegure riqueza de detalhes. A QUESTÃO JURÍDICA deve ser claramente delineada como principal, seguida de pontos controvertidos.
- Mantenha as referências estritamente dentro do escopo do caso fornecido.
- Termine com 🏁.
```
`</exemplo_completo>`
– Quando usar: Para realizar uma análise jurídica completa e estruturada de documentos de caso, seguindo a metodologia FIRAC+ específica ensinada no curso. **Requer anexar ou fornecer os documentos do caso.**

---

### 1.2 Geração de Ementa CNJ

*Use quando precisar gerar um resumo de decisão judicial no formato padrão CNJ.*
**Nota Importante:** Requer o texto completo da decisão judicial.
**Para documentos muito extensos:** Se a decisão for muito longa, considere aplicar técnicas de `chunking` ou meta-sumarização (conforme `1- System Prompt.md` e `2- Preferencias de Formatacao de Prompt.md`), focando na extração dos pontos essenciais para a ementa de cada parte e consolidando-os.
<!-- Exemplo de instrução para meta-sumarização (para o usuário adaptar):
<meta_sumarizacao>
  <passo1>Divida a decisão em seções lógicas (ex: relatório, fundamentação, dispositivo).</passo1>
  <passo2>Extraia os pontos chave de cada seção para a ementa.</passo2>
  <passo3>Compile os pontos chave na estrutura da Ementa CNJ.</passo3>
</meta_sumarizacao>
-->

**1.2.1 TEMPLATE ESTRUTURA (Ementa CNJ)**
*(Esta é a estrutura base com placeholders para preenchimento)*

```
# TAREFA
- ESCREVA uma EMENTA para a decisão judicial fornecida, seguindo ESTRITAMENTE o formato padrão CNJ.
- Analise a decisão com profundidade, precisão e detalhes para capturar as nuances.

# DOCUMENTO (Use delimitadores <decision>)
<decision>[INSIRA O TEXTO COMPLETO DA DECISÃO AQUI]</decision>

# CRITÉRIOS DE EXTRAÇÃO ESPECÍFICOS
<!-- Instrução para o usuário: Defina aqui critérios específicos para extração de informação, se necessário. Ex: Focar em teses sobre dano moral, extrair menções a artigos específicos do CDC, etc. -->
<!-- Exemplo de Critérios (comente ou remova se não usar):
<criterios_extracao>
    <extrair item="teses_dano_moral" />
    <extrair item="artigos_cdc_mencionados" />
</criterios_extracao>
-->

# ROLE (PERSONA)
- Assuma a `persona` de um Analista Jurídico especializado em sumarização de jurisprudência.

# ESTRUTURA DE SAÍDA (EMENTA CNJ)
- Siga RIGOROSAMENTE a seguinte estrutura XML:
  <ementa_cnj>
    <cabecalho_ementa>[RAMO DIREITO. CLASSE PROC. ASSUNTO GERAL AO ESPECÍFICO EM MAIÚSCULA. RESULTADO.]</cabecalho_ementa>
    <caso_em_exame>
      <item_caso_exame numero="1">[APRESENTAÇÃO DO CASO SEM 'TRATA-SE', FATOS RELEVANTES, PEDIDO]</item_caso_exame>
    </caso_em_exame>
    <questao_em_discussao>
      <item_questao numero="2">[IDENTIFICAÇÃO PRECISA DA(S) QUESTÃO(ÕES) CENTRAL(IS)]</item_questao>
    </questao_em_discussao>
    <razoes_de_decidir>
      <!-- JUSTIFICATIVAS NUMERADAS, VOZ ATIVA, VERBO PRESENTE, CONCISAS -->
      <justificativa numero="3">[Justificativa 1]</justificativa>
      <justificativa numero="4">[Justificativa 2]</justificativa>
      <!-- ... -->
    </razoes_de_decidir>
    <dispositivo_e_tese>
      <resultado_principal numero="5">[RESULTADO PRINCIPAL NA VOZ PASSIVA, ex: "Pedido procedente"]</resultado_principal>
      <teses_julgamento>
        <!-- TESES NUMERADAS, CONCISAS, OBJETIVAS, VOZ ATIVA -->
        <tese numero="1">[TESE 1]</tese>
        <tese numero="2">[TESE 2]</tese>
        <!-- ... -->
      </teses_julgamento>
    </dispositivo_e_tese>
    <referencias>
      <dispositivos_relevantes_citados>[IDENTIFICAÇÃO DAS NORMAS, ex: CF/88, art. X]</dispositivos_relevantes_citados>
      <jurisprudencia_relevante_citada>[IDENTIFICAÇÃO DOS PRECEDENTES, ex: STF, ADPF Y]</jurisprudencia_relevante_citada>
    </referencias>
  </ementa_cnj>

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
- Como um analista jurídico especializado, ANALISE o caso fornecido com profundidade e precisão para ESCREVER uma EMENTA.
- Siga ESTRITAMENTE a ESTRUTURA CNJ fornecida.
- Cite apenas fatos, normas e precedentes do caso original.
- Comece o texto com ***Ementa***.
# ESTRUTURA
- Use o formato da ESTRUTURA aqui fornecida, melhorando, adaptando e incluindo o que for necessário para garantir clareza, coesão, coerência, objetividade e precisão:
<estrutura_ementa_cnj>
  <ementa_cnj>
    <cabecalho_ementa>DIREITO CIVIL. RECURSO ESPECIAL. CONTRATOS. ALIENAÇÃO FIDUCIÁRIA. BEM IMÓVEL. LEILÃO EXTRAJUDICIAL. NOTIFICAÇÃO PESSOAL DO DEVEDOR. NECESSIDADE. PROVIMENTO.</cabecalho_ementa>
    <caso_em_exame>
      <item_caso_exame numero="1">Recurso Especial interposto contra acórdão que entendeu desnecessária a notificação pessoal do devedor acerca da data do leilão extrajudicial de imóvel alienado fiduciariamente.</item_caso_exame>
    </caso_em_exame>
    <questao_em_discussao>
      <item_questao numero="2">A questão em discussão consiste em definir se é necessária a notificação pessoal do devedor fiduciante sobre a data, horário e local do leilão extrajudicial do imóvel objeto de alienação fiduciária.</item_questao>
    </questao_em_discussao>
    <razoes_de_decidir>
      <justificativa numero="3">A Lei nº 9.514/97, embora não exija expressamente a notificação pessoal do devedor sobre o leilão, deve ser interpretada de forma sistemática com o Decreto-Lei nº 70/66, que prevê tal comunicação.</justificativa>
      <justificativa numero="4">A notificação pessoal visa garantir ao devedor o exercício do direito de preferência na arrematação do bem ou a purgação da mora antes da alienação a terceiros.</justificativa>
    </razoes_de_decidir>
    <dispositivo_e_tese>
      <resultado_principal numero="5">Recurso especial provido.</resultado_principal>
      <teses_julgamento>
        <tese numero="1">No âmbito do contrato de alienação fiduciária de bem imóvel, regido pela Lei nº 9.514/97, é necessária a notificação pessoal do devedor acerca da data, horário e local do leilão extrajudicial.</tese>
      </teses_julgamento>
    </dispositivo_e_tese>
    <referencias>
      <dispositivos_relevantes_citados>Lei nº 9.514/1997, arts. 26 e 27. Decreto-Lei nº 70/1966, art. 36.</dispositivos_relevantes_citados>
      <jurisprudencia_relevante_citada>STJ, REsp XXXXX/XX.</jurisprudencia_relevante_citada>
    </referencias>
  </ementa_cnj>
</estrutura_ementa_cnj>
# EXEMPLO (Opcional para Few-Shot)
- (Instrução para o usuário: Opcionalmente, forneça o exemplo completo da Ementa Padrão do CNJ aqui para few-shot learning se a IA tiver dificuldades com o formato).
```
`</exemplo_completo>`
– Quando usar: Para gerar um resumo de caso padronizado (Ementa) com base em uma decisão judicial fornecida, seguindo a estrutura de formato CNJ específica ensinada no curso. **Requer o texto completo da decisão.**

---

### 1.4 SuperAnálise (Textos Jurídicos)

*Use para uma análise profunda e estruturada de artigos, capítulos de livros ou pareceres jurídicos.*
**Nota Importante:** Requer fornecer o texto completo a ser analisado.
**Para documentos muito extensos:** Se o texto for muito longo (ex: um livro), aplique a SuperAnálise por capítulos ou seções, e depois consolide os achados, possivelmente usando técnicas de meta-sumarização (conforme `1- System Prompt.md` e `2- Preferencias de Formatacao de Prompt.md`).
<!-- Exemplo de instrução para meta-sumarização (para o usuário adaptar):
<meta_sumarizacao_texto_longo>
  <passo1>Divida o livro/texto em capítulos/seções principais.</passo1>
  <passo2>Aplique a SuperAnálise a cada capítulo/seção.</passo2>
  <passo3>Sintetize os 'Resultados', 'Importância' e 'Lições Práticas' de cada SuperAnálise parcial em um relatório consolidado.</passo3>
  <passo4>Identifique os 5 conceitos jurídicos mais relevantes que perpassam todo o texto.</passo4>
</meta_sumarizacao_texto_longo>
-->

**1.4.1 TEMPLATE ESTRUTURA (SuperAnálise)**
*(Esta é a estrutura base com placeholders para preenchimento)*

```
# TAREFA
- REALIZE uma SUPERANÁLISE do texto jurídico fornecido.
- ANALISE EM DETALHE e na ÍNTEGRA.

# DOCUMENTO (Use delimitadores <text>)
<text>[INSIRA O TEXTO COMPLETO AQUI]</text>

# CRITÉRIOS DE EXTRAÇÃO ESPECÍFICOS
<!-- Instrução para o usuário: Defina aqui critérios específicos para extração de informação, se necessário. Ex: Focar na análise de jurisprudência citada, identificar argumentos a favor de uma tese específica, extrair todas as propostas de alteração legislativa. -->
<!-- Exemplo de Critérios (comente ou remova se não usar):
<criterios_extracao>
    <extrair item="analise_jurisprudencia_citada" />
    <extrair item="argumentos_tese_especifica" />
    <extrair item="propostas_alteracao_legislativa" />
</criterios_extracao>
-->

# ROLE (PERSONA)
- Assuma a `persona` de um ANALISTA DE TEXTOS JURÍDICOS (PhD) especializado em [ÁREA DO DIREITO DO TEXTO], com domínio de Teoria da Linguagem, Interpretação, Lógica e Argumentação Jurídica.

# ESTRUTURA DE SAÍDA (SUPERANÁLISE)
- Siga RIGOROSAMENTE a seguinte estrutura XML:
  <super_analise_texto>
    <dados_texto titulo="[TÍTULO DO TEXTO]" autor="[AUTOR(ES)]" publicacao="[LOCAL DE PUBLICAÇÃO/VEÍCULO]" data="[DATA DA PUBLICAÇÃO]">
      <!-- Outras informações bibliográficas relevantes -->
    </dados_texto>
    <especialidades_relevantes>
      <especialidade>[ESPECIALIDADE JURÍDICA 1]</especialidade>
      <especialidade>[ESPECIALIDADE JURÍDICA 2]</especialidade>
      <especialidade>[ESPECIALIDADE JURÍDICA 3]</especialidade>
    </especialidades_relevantes>
    <sumario_estruturado>
      <!-- SUMÁRIO ESTRUTURADO EM DOIS NÍVEIS -->
      <nivel1 titulo="[TÍTULO NÍVEL 1]">
        <nivel2 titulo="[TÍTULO NÍVEL 2]">[RESUMO CONCEITO NÍVEL 2]</nivel2>
      </nivel1>
      <!-- ... -->
    </sumario_estruturado>
    <tabela_objetivos_ideias>
      <item_tabela>
        <objetivo_texto>[OBJETIVO 1 DO TEXTO]</objetivo_texto>
        <ideia_central>[IDEIA CENTRAL ASSOCIADA AO OBJETIVO 1]</ideia_central>
      </item_tabela>
      <item_tabela>
        <objetivo_texto>[OBJETIVO 2 DO TEXTO]</objetivo_texto>
        <ideia_central>[IDEIA CENTRAL ASSOCIADA AO OBJETIVO 2]</ideia_central>
      </item_tabela>
      <!-- ... -->
    </tabela_objetivos_ideias>
    <proposito_texto>
      <questao_central_texto>[PROPÓSITO PRINCIPAL, QUESTÃO CENTRAL QUE O TEXTO BUSCA RESPONDER]</questao_central_texto>
      <questoes_secundarias>
        <questao_secundaria>[QUESTÃO SECUNDÁRIA 1]</questao_secundaria>
        <questao_secundaria>[QUESTÃO SECUNDÁRIA 2]</questao_secundaria>
      </questoes_secundarias>
    </proposito_texto>
    <resultados_conclusoes>
      <!-- CONCLUSÕES PRAGMÁTICAS, INFERÊNCIAS RELEVANTES -->
      <resultado>[RESULTADO/CONCLUSÃO 1]</resultado>
      <resultado>[RESULTADO/CONCLUSÃO 2]</resultado>
    </resultados_conclusoes>
    <relevancia_impacto>
      <!-- RELEVÂNCIA, IMPACTO NO CAMPO JURÍDICO/PRÁTICO -->
      <importancia>[DESCRIÇÃO DA IMPORTÂNCIA/IMPACTO]</importancia>
    </relevancia_impacto>
    <licoes_praticas>
      <!-- APLICAÇÃO PRÁTICA, EXEMPLO DE USO -->
      <licao>[LIÇÃO PRÁTICA 1]</licao>
      <exemplo_uso>[EXEMPLO DE USO DA LIÇÃO 1]</exemplo_uso>
    </licoes_praticas>
    <aprofundamento_conceitos>
      <conceitos_chave>
        <conceito_juridico_relevante>[CONCEITO 1]</conceito_juridico_relevante>
        <conceito_juridico_relevante>[CONCEITO 2]</conceito_juridico_relevante>
        <conceito_juridico_relevante>[CONCEITO 3]</conceito_juridico_relevante>
        <conceito_juridico_relevante>[CONCEITO 4]</conceito_juridico_relevante>
        <conceito_juridico_relevante>[CONCEITO 5]</conceito_juridico_relevante>
      </conceitos_chave>
      <pergunta_final>Deseja aprofundar algum desses conceitos?</pergunta_final>
    </aprofundamento_conceitos>
  </super_analise_texto>

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
# ROLE (PERSONA)
- Você é um ANALISTA DE TEXTOS JURÍDICOS, especializado em sumarizar e analisar textos acadêmicos ou doutrinários, COM DETALHES E PROFUNDIDADE, seguindo a estrutura SuperAnálise.
- Você deve assumir a ESPECIALIDADE do conteúdo a ser discutido, INCORPORANDO O CONHECIMENTO e da matéria de fundo com suas nuances.
- Você domina TEORIA DA LINGUAGEM, INTERPRETAÇÃO, LÓGICA FORMAL E INFORMAL, PENSAMENTO CRÍTICO E ARGUMENTAÇÃO JURÍDICA.
# ESTRUTURA SUPERANÁLISE
- Comece o texto com a expressão DADOS DO TEXTO 📁
- Use o formato de análise e de layout SUPERANÁLISE, conforme ESTRUTURA a seguir:
<ESTRUTURA_SUPERANALISE>
  <super_analise_texto>
    <dados_texto titulo="A Responsabilidade Civil das Inteligências Artificiais" autor="Prof. Dr. Jurista Exemplo" publicacao="Revista de Direito Digital Avançado" data="Jan/Mar 2024">
    </dados_texto>
    <especialidades_relevantes>
      <especialidade>Direito Civil (Responsabilidade Civil)</especialidade>
      <especialidade>Direito Digital (Inteligência Artificial)</especialidade>
      <especialidade>Teoria Geral do Direito</especialidade>
    </especialidades_relevantes>
    <sumario_estruturado>
      <nivel1 titulo="Introdução à IA e seus desafios jurídicos">
        <nivel2 titulo="Conceitos básicos de IA">Resumo do conceito de IA.</nivel2>
        <nivel2 titulo="O problema da imputação">Resumo do problema da imputação na IA.</nivel2>
      </nivel1>
      <nivel1 titulo="Teorias de Responsabilidade Civil Aplicáveis">
        <nivel2 titulo="Responsabilidade subjetiva e suas limitações">Análise da culpa.</nivel2>
        <nivel2 titulo="Responsabilidade objetiva e o risco da atividade">Análise do risco.</nivel2>
      </nivel1>
    </sumario_estruturado>
    <tabela_objetivos_ideias>
      <item_tabela>
        <objetivo_texto>Analisar a adequação dos regimes tradicionais de responsabilidade civil aos danos causados por IAs.</objetivo_texto>
        <ideia_central>Os regimes tradicionais são insuficientes ou exigem adaptação significativa.</ideia_central>
      </item_tabela>
      <item_tabela>
        <objetivo_texto>Propor critérios para atribuição de responsabilidade em casos envolvendo IAs autônomas.</objetivo_texto>
        <ideia_central>Sugestão de um sistema híbrido ou específico para IAs.</ideia_central>
      </item_tabela>
    </tabela_objetivos_ideias>
    <proposito_texto>
      <questao_central_texto>Como o Direito Civil deve responder aos desafios impostos pela crescente autonomia das Inteligências Artificiais em relação à causação de danos?</questao_central_texto>
      <questoes_secundarias>
        <questao_secundaria>É possível aplicar a teoria da culpa a um agente não humano?</questao_secundaria>
        <questao_secundaria>Quem deve ser responsabilizado: o programador, o usuário, o proprietário da IA, ou a própria IA (se personificada)?</questao_secundaria>
      </questoes_secundarias>
    </proposito_texto>
    <resultados_conclusoes>
      <resultado>O texto conclui que a responsabilidade objetiva, baseada no risco da atividade de desenvolvimento e uso de IAs complexas, é o caminho mais promissor.</resultado>
      <resultado>Aponta para a necessidade de seguros obrigatórios e fundos de compensação.</resultado>
    </resultados_conclusoes>
    <relevancia_impacto>
      <importancia>Este estudo é crucial para orientar legisladores e juristas na formulação de novas leis e interpretações que acomodem os avanços tecnológicos, garantindo segurança jurídica e proteção às vítimas de danos causados por IA.</importancia>
    </relevancia_impacto>
    <licoes_praticas>
      <licao>Advogados que atuam com tecnologia devem se aprofundar nas discussões sobre a personalidade jurídica e responsabilidade de IAs.</licao>
      <exemplo_uso>Um caso de carro autônomo que causa um acidente poderia ser analisado sob a ótica da responsabilidade pelo fato do produto (IA como produto) ou pela atividade de risco (uso do carro autônomo).</exemplo_uso>
    </licoes_praticas>
    <aprofundamento_conceitos>
      <conceitos_chave>
        <conceito_juridico_relevante>Agência autônoma</conceito_juridico_relevante>
        <conceito_juridico_relevante>Risco da atividade tecnológica</conceito_juridico_relevante>
        <conceito_juridico_relevante>Nexo de causalidade algorítmico</conceito_juridico_relevante>
        <conceito_juridico_relevante>Seguro de responsabilidade para IA</conceito_juridico_relevante>
        <conceito_juridico_relevante>Personalidade eletrônica (e-person)</conceito_juridico_relevante>
      </conceitos_chave>
      <pergunta_final>Deseja aprofundar algum desses conceitos?</pergunta_final>
    </aprofundamento_conceitos>
  </super_analise_texto>
</ESTRUTURA_SUPERANALISE>

```
`</exemplo_completo>`
– Quando usar: Para realizar uma análise profunda e estruturada de um artigo jurídico, capítulo de livro ou parecer, seguindo a estrutura SuperAnálise ensinada no curso. **Requer que o texto seja fornecido.**

---
# Atualizado em: 03/05/25