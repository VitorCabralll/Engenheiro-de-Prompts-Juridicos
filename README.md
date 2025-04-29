# Engenheiro de Prompts Jurídicos

Um sistema especializado para geração, avaliação e refinamento de prompts de IA no contexto jurídico.

![Licença MIT](https://img.shields.io/badge/Licença-MIT-blue.svg)

## 📋 Visão Geral

O Engenheiro de Prompts Jurídicos é um sistema estruturado baseado em restrições, projetado para criar instruções de alta qualidade para sistemas de IA no contexto jurídico. Ele combina as melhores práticas de engenharia de prompts com conhecimentos específicos do domínio jurídico brasileiro e internacional.

**Este sistema não é um chatbot ou assistente legal** — ele atua como um Orquestrador de Prompts Jurídicos que:

- ⚖️ Gera sugestões de prompts jurídicos bem formatados (`#prompt`)
- 📜 Avalia e melhora prompts legais do usuário (`#qa`)
- ⚠️ Identifica riscos, ambiguidades e limitações (`#analise`)
- 📋 Organiza por área do direito e tipo de documento (`#categorias`)
- 🛠️ Recomenda otimizações seguindo práticas jurídicas (`#melhores-praticas`)

## 💡 Por que usar o Engenheiro de Prompts Jurídicos?

- **Precisão Terminológica**: Garante o uso correto da terminologia jurídica
- **Conformidade Legal**: Compatível com a Resolução do CNJ Nº 615 de 11/03/2025
- **Atualização Constante**: Adaptável a mudanças regulatórias
- **Especialização por Área**: Prompts específicos para diferentes ramos do direito
- **Redução de Risco**: Minimiza interpretações errôneas em contextos jurídicos

## 🚀 Como Utilizar

O sistema pode ser implantado em qualquer ambiente GPT compatível (por exemplo, GPT-4 Personalizado) que permita:

1. Carregamento de instruções personalizadas
2. Entrada de prompt do usuário
3. Capacidade de resposta estruturada

### Principais Comandos

O sistema responde a tags específicas que ativam diferentes modos:

- `#prompt` - Gera sugestões de prompt (modo padrão)
- `#qa` - Revisa um prompt, encontra falhas e sugere melhorias
- `#analise` - Analisa potenciais problemas de um prompt
- `#categorias` - Organiza por área do direito
- `#melhores-praticas` - Recomenda otimizações
- `#learn` - Explica a estrutura de um prompt (modo educacional)
- `#edge` - Gera prompts de teste para casos extremos

## 📝 Exemplos de Uso

### Avaliar um Prompt Jurídico

```
#qa Verifique este prompt: "Analise esta cláusula contratual e identifique possíveis vulnerabilidades legais."
```

### Gerar um Novo Prompt

```
#prompt Preciso de um prompt que ajude a IA a criar um modelo de petição inicial para uma ação de indenização por danos morais.
```

### Analisar Potenciais Problemas

```
#analise Meu prompt "Aja como um juiz e dê um parecer sobre este caso de divórcio" tem algum problema?
```

### Categorizar por Área do Direito

```
#categorias Preciso de prompts relacionados ao direito trabalhista para análise de acordos coletivos.
```

## 📚 Métodos de Análise Incluídos

O sistema suporta vários métodos estruturados de análise jurídica:

- **FIRAC+**: Fatos, Issue (Problema Jurídico), Regra, Análise, Conclusão (expandido)
- **Ementa CNJ**: Formato padronizado para resumo de decisões judiciais
- **CASO+**: Estrutura para estudos de caso jurídicos detalhados
- **SuperAnálise**: Método para análise profunda de artigos e textos jurídicos

## 🔍 Recursos Especializados

O Engenheiro de Prompts Jurídicos inclui recursos específicos para diferentes áreas do direito:

- **Direito Civil**: Contratos, responsabilidade civil, direito de família
- **Direito Penal**: Análise de tipos penais, defesas e procedimentos criminais
- **Direito Trabalhista**: Reclamações, acordos e análise de legislação
- **Direito Tributário**: Consultas sobre tributação e planejamento fiscal
- **Direito Administrativo**: Processos administrativos e licitações
- **Direito Digital**: LGPD, crimes cibernéticos e direito digital

## 🌟 Benefícios para Profissionais Jurídicos

- **Economia de Tempo**: Criação eficiente de prompts para tarefas repetitivas
- **Maior Precisão**: Resultados mais exatos das IAs em contextos jurídicos
- **Terminologia Correta**: Uso adequado da linguagem jurídica
- **Redução de Erros**: Minimização de interpretações equivocadas
- **Consistência**: Padrão uniforme nos documentos gerados

## 📂 Estrutura do Repositório

- `LICENSE` - Licença MIT
- `README.md` - Este arquivo
- `Prompt Formatting Preferences` - Diretrizes de formatação
- `Prompt Library` - Biblioteca de prompts pré-configurados
- `Prompt Templates` - Templates para diversos casos de uso
- `QA Module` - Módulo de garantia de qualidade
- `Specialized Prompt Examples` - Exemplos de prompts especializados
- `System Prompt` - Configuração do sistema

## 👥 Contribuição

Contribuições de profissionais do direito são especialmente bem-vindas! Por favor, leia as diretrizes de contribuição antes de enviar pull requests.

## ⚖️ Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).

## ⚠️ Aviso Legal

Este sistema é uma ferramenta de produtividade para profissionais do direito e não substitui aconselhamento jurídico qualificado. Todas as saídas geradas devem ser revisadas por profissionais competentes antes do uso.

---

**Última atualização:** 29/04/2025

© 2025 Vitor Cabral
