# Templates e Exemplos - v2.8

Este arquivo contém **templates estruturados** para tarefas jurídicas complexas e gerais, bem como **exemplos completos ou ilustrativos** de prompts. Serve como a principal fonte de consulta para o Engenheiro de Prompts Jurídicos ao gerar novas sugestões de prompt (`#prompt`) ou ao explicar estruturas (`#learn`).

---

## Seção 1: Templates Jurídicos Estruturados (Métodos Nomeados)

Esta seção detalha os templates para metodologias de análise e sumarização específicas ensinadas, fornecendo tanto a estrutura base reutilizável quanto um exemplo completo do prompt.

---

### 1.1 Análise FIRAC+

*Use quando precisar de uma análise jurídica estruturada de documentos de um caso, seguindo a metodologia FIRAC+.*
**Nota Importante:** Requer fornecer os documentos do caso completos. Se usar multiplos documentos, o prompt deve solicitar uma leitura holistica.
**Para documentos muito extensos:** Se o documento fornecido for muito longo e puder exceder o limite de contexto da IA, considere dividi-lo em seções menores (chunking) e aplicar este template a cada seção. Depois, compile as análises parciais. Alternativamente, instrua a IA a realizar uma meta-sumarização: primeiro resumir as seções e depois resumir os resumos, mantendo o foco nos critérios de extração definidos.
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
**Para documentos muito extensos:** Se a decisão fornecida for muito longa e puder exceder o limite de contexto da IA, considere dividi-la em seções menores (chunking) e aplicar este template a cada seção para capturar os pontos essenciais de cada parte. Depois, compile as ementas parciais ou os pontos chave em uma ementa final consolidada. Alternativamente, instrua a IA a realizar uma meta-sumarização: primeiro resumir as seções da decisão e depois gerar a ementa a partir dos resumos, mantendo o foco nos critérios de extração definidos para uma ementa.
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
- Você é uma analista jurídico especializado em analisar um caso fornecido com profundidade, precisão e detalhes, captando as nuances, com o propósito de escrever uma EMENTA, conforme ESTRUTURA fornecida.
- ESCREVA a EMENTA do caso fornecido, seguindo estritamente a ESTRUTURA fornecida.
- Cite apenas fatos, normas e precedentes do caso fornecido.
- Comece o texto com ***Ementa***
- (Instrução para o usuário: Adicione um finalizador se desejar, como o exemplo do curso: Termine com "**** ✨👨‍⚖️💡 Aprenda a fazer prompts poderosos com o Curso de Escrita Jurídica com o ChatGPT 🖋️⚖️📖: [link]")
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

### 1.3 Estudo de Caso Jurídico (CASO+)

*Use quando precisar criar um estudo de caso detalhado para fins acadêmicos ou de treinamento.*
**Nota Importante:** Requer fornecer os documentos relevantes do caso.
**Para documentos muito extensos:** Se os documentos do caso forem muito longos, considere aplicar o template CASO+ a seções ou documentos individuais primeiramente. Depois, sintetize as análises parciais em um estudo de caso consolidado. Se a IA tiver capacidade de processar grandes volumes, pode-se fornecer tudo, mas instrua-a a focar na criação de uma narrativa coesa e nos pontos chave para debate, conforme os critérios de extração.
<!-- Exemplo de instrução para meta-sumarização (para o usuário adaptar):
<meta_sumarizacao_caso>
  <passo1>Analise cada documento/seção chave do caso (ex: petição inicial, contestação, sentença, recurso).</passo1>
  <passo2>Extraia os elementos do CASO+ (fatos, argumentos, decisão) de cada parte.</passo2>
  <passo3>Compile um estudo de caso integrado, garantindo que as 'Questões para Debate' reflitam a complexidade total do caso.</passo3>
</meta_sumarizacao_caso>
-->

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

# CRITÉRIOS DE EXTRAÇÃO ESPECÍFICOS
<!-- Instrução para o usuário: Defina aqui critérios específicos para extração de informação, se necessário. Ex: Focar nos argumentos sobre responsabilidade civil, extrair detalhes sobre a produção de provas periciais, identificar os pontos de maior divergência entre as partes. -->
<!-- Exemplo de Critérios (comente ou remova se não usar):
<criterios_extracao>
    <extrair item="argumentos_responsabilidade_civil" />
    <extrair item="detalhes_provas_periciais" />
    <extrair item="pontos_divergencia_partes" />
</criterios_extracao>
-->

# ROLE (PERSONA)
- Assuma a `persona` de um ESPECIALISTA em [ÁREA DO DIREITO RELEVANTE] e também em DIREITO, LINGUÍSTICA, CIÊNCIAS COGNITIVAS E SOCIAIS.

# LINGUAGEM E ESTILO (Output Style)
- Tom: PROFISSIONAL e AUTORITATIVO.
- Estilo: CONCISO, completo, sem redundâncias.
- Público-Alvo (`Audience`): Estudantes de pós-graduação.
- Início: Comece diretamente com 'DADOS DO PROCESSO'.

# ESTRUTURA DE SAÍDA (CASO+)
- Siga RIGOROSAMENTE a seguinte estrutura XML:
  <estudo_caso_plus>
    <dados_processo tribunal="[NOME DO TRIBUNAL]" tipo_recurso_acao="[TIPO DE RECURSO/AÇÃO]" numero_processo="[NÚMERO DO PROCESSO]" relator="[NOME DO RELATOR]" data_julgamento="[DATA DE JULGAMENTO]">
      <!-- Outras informações relevantes -->
    </dados_processo>
    <fatos_detalhados>
      <!-- DESCRIÇÃO DETALHADA, PROFUNDA E MINUCIOSA, começando pela conduta do réu -->
      <fato_relevante>[FATO 1]</fato_relevante>
      <fato_relevante>[FATO 2]</fato_relevante>
      <!-- ... -->
    </fatos_detalhados>
    <argumentos_provas_autor>
      <!-- LISTA COM INFERÊNCIA LÓGICA -->
      <argumento_autor>[ARGUMENTO 1]</argumento_autor>
      <prova_autor>[PROVA 1 ASSOCIADA]</prova_autor>
      <!-- ... -->
    </argumentos_provas_autor>
    <argumentos_provas_reu>
      <!-- LISTA COM INFERÊNCIA LÓGICA -->
      <argumento_reu>[ARGUMENTO 1]</argumento_reu>
      <prova_reu>[PROVA 1 ASSOCIADA]</prova_reu>
      <!-- ... -->
    </argumentos_provas_reu>
    <direito_aplicavel_caso>
      <!-- DEFINIÇÃO DAS NORMAS APLICÁVEIS REFERENCIADAS -->
      <norma_aplicada>[NORMA 1]</norma_aplicada>
      <norma_aplicada>[NORMA 2]</norma_aplicada>
      <!-- ... -->
    </direito_aplicavel_caso>
    <questoes_para_debate>
      <!-- SUGESTÃO DE QUESTÕES RELEVANTES, COM REFLEXÕES CRÍTICAS -->
      <questao_debate>[QUESTÃO 1 PARA DEBATE]</questao_debate>
      <questao_debate>[QUESTÃO 2 PARA DEBATE]</questao_debate>
      <!-- ... -->
    </questoes_para_debate>
    <resposta_tribunal>
      <!-- RESPOSTA ÀS QUESTÕES BASEADA NA DECISÃO (PLACAR, RESULTADO, RAZÕES), começando com "Em resposta às questões levantadas..." -->
      <resultado_julgamento placar="[PLACAR SE HOUVER]" resultado="[RESULTADO]">[DESCRIÇÃO DAS RAZÕES DE DECIDIR EM RELAÇÃO ÀS QUESTÕES]</resultado_julgamento>
    </resposta_tribunal>
  </estudo_caso_plus>

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
  <estudo_caso_plus>
    <dados_processo tribunal="TJSP" tipo_recurso_acao="APELAÇÃO CÍVEL SEM REVISÃO" numero_processo="0005555-55.2020.8.26.0100" relator="DES. JURISTA EXEMPLO" data_julgamento="10/03/2023">
    </dados_processo>
    <fatos_detalhados>
      <fato_relevante>Em 01/02/2020, o Réu (empresa de telefonia) efetuou cobrança indevida na fatura do Autor referente a serviço não solicitado.</fato_relevante>
      <fato_relevante>O Autor tentou resolver administrativamente por 3 vezes, sem sucesso.</fato_relevante>
    </fatos_detalhados>
    <argumentos_provas_autor>
      <argumento_autor>Cobrança indevida configura falha na prestação de serviço (Art. 14, CDC).</argumento_autor>
      <prova_autor>Faturas detalhadas, protocolos de atendimento.</prova_autor>
      <argumento_autor>Dano moral presumido (in re ipsa) pela perda de tempo útil e desgaste.</argumento_autor>
    </argumentos_provas_autor>
    <argumentos_provas_reu>
      <argumento_reu>Serviço foi efetivamente disponibilizado e erro na cobrança foi pontual.</argumento_reu>
      <prova_reu>Telas sistêmicas (impugnadas pelo Autor por unilateralidade).</prova_reu>
      <argumento_reu>Mero aborrecimento não configura dano moral.</argumento_reu>
    </argumentos_provas_reu>
    <direito_aplicavel_caso>
      <norma_aplicada>Código de Defesa do Consumidor (Lei 8.078/90), Arts. 6, 14, 42.</norma_aplicada>
      <norma_aplicada>Código Civil, Arts. 186, 927.</norma_aplicada>
    </direito_aplicavel_caso>
    <questoes_para_debate>
      <questao_debate>A cobrança indevida por serviço não solicitado, mesmo após tentativas de resolução administrativa, configura mero aborrecimento ou dano moral indenizável?</questao_debate>
      <questao_debate>Qual o peso probatório de telas sistêmicas unilaterais apresentadas pelo fornecedor?</questao_debate>
      <questao_debate>A teoria da perda do tempo útil é aplicável ao caso?</questao_debate>
    </questoes_para_debate>
    <resposta_tribunal>
      <resultado_julgamento placar="Unânime" resultado="Provido em parte o recurso do Autor">Em resposta às questões levantadas, o tribunal decidiu que a cobrança indevida persistente configura dano moral, fixando indenização. Considerou as telas sistêmicas com baixo valor probatório isoladamente e aplicou a teoria da perda do tempo útil.</resultado_julgamento>
    </resposta_tribunal>
  </estudo_caso_plus>
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
**Para documentos muito extensos:** Se o texto for excepcionalmente longo (e.g., um livro inteiro), aplique a SuperAnálise por capítulos ou seções significativas. Depois, crie uma "SuperAnálise da SuperAnálise" para consolidar os achados, ou instrua a IA a focar nos elementos chave de cada análise parcial para construir um panorama geral.
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

## Seção 2: Templates Jurídicos Gerais (Adaptados)

Esta seção contém templates mais flexíveis adaptados para tarefas jurídicas comuns que podem não exigir uma metodologia nomeada específica.
**Nota sobre Adaptação:** Estes templates gerais podem ser adaptados para diversas análises jurídicas. Para tarefas que exigem uma estrutura de output altamente detalhada e específica (e.g., análise completa de caso, geração de ementa), considere usar ou se inspirar nos templates da 'Seção 1: Templates Jurídicos Estruturados (Métodos Nomeados)', que já incorporam formatos de saída mais elaborados e podem ser um bom ponto de partida para personalização.

---

### 2.1 TEMPLATE: Instrução Abrangente Jurídica

*Use para tarefas jurídicas mais simples que não se encaixam nos modelos complexos acima.*
```
- `Role`/Persona: Você é um(a) [PAPEL JURÍDICO, ex: Advogado(a) Assistente].
- Tarefa (`Task`): Sua tarefa é [INSTRUÇÃO CLARA E DIRETA, ex: resumir os pontos principais, identificar cláusulas de X tipo, elaborar um esboço inicial de Y].
- Contexto (`Context`): Considere o seguinte contexto/documento: `<context>[INSIRA O CONTEXTO OU TEXTO CURTO AQUI]</context>`. (Para textos longos, use delimitadores claros e considere as preferências de Long Context).
- Jurisdição (`Jurisdiction`, se aplicável): [NOME DA JURISDIÇÃO].
- Formato de Saída (`Output Format`): Apresente a resposta como [FORMATO DESEJADO, ex: uma lista com marcadores, um parágrafo conciso, uma tabela simples, ou uma estrutura XML como <resumo_pontos_principais><ponto>...</ponto></resumo_pontos_principais>].
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
- Formato de Saída (`Output Format`): [FORMATO DESEJADO, ex: relatório narrativo, lista de riscos com níveis de criticidade, ou uma estrutura XML como <analise_cenario><riscos_legais><risco tipo="">...</risco></riscos_legais><argumentos_possiveis><argumento parte="X">...</argumento></argumentos_possiveis></analise_cenario>].
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
- Formato de Saída (`Output Format`): Resposta detalhada seguindo os passos acima, idealmente separando o raciocínio (passos 1-3) da conclusão final (passo 4), talvez usando tags como <analise_juridica_cot><regras_aplicaveis><regra fonte="">...</regra></regras_aplicaveis><requisitos_elementos><requisito>...</requisito></requisitos_elementos><analise_fatos_nos_requisitos><analise_requisito>...</analise_requisito></analise_fatos_nos_requisitos></analise_juridica_cot> e <conclusao_preliminar certeza="">...</conclusao_preliminar>.
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
- Formato de Saída (`Output Format`): Apresente a comparação em uma tabela (`Markdown table`) com as colunas: "Critério de Comparação", "Item 1", "Item 2", "[Item N...]", "Observação/Diferença Principal". Alternativamente, para dados mais complexos, pode-se sugerir uma estrutura XML: `<analise_comparativa><comparacao criterio="[Critério 1]"><item_1_detalhe>...</item_1_detalhe><item_2_detalhe>...</item_2_detalhe><observacao>...</observacao></comparacao></analise_comparativa>`.
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