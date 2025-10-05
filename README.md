
# 🎯 RAG e Suas Alternativas: Um Framework para o Aprimoramento de Grandes Modelos de Linguagem 

## Um Guia de Decisão Prático para Desenvolvedores

[](https://opensource.org/licenses/MIT)
[](https://www.python.org/downloads/)
[](https://www.google.com/search?q=LINK_DO_SEU_ARTIGO)
[](https://www.google.com/search?q=CONTRIBUTING.md)

> Apresentamos um framework prático de decisão para escolher entre RAG e outras técnicas de aprimoramento de Grandes Modelos de Linguagem (LLMs), com foco no contexto brasileiro.

[**Artigo Científico**](https://drive.google.com/file/d/1aMzeUXOVJrcXkTpRxJLBJ6c9-tD00dic/view?usp=sharing) | [**Estudo de Caso**](https://github.com/evellynnicole/FutChat.git) | [**Árvore de Decisão**](https://www.mermaidchart.com/d/669786ad-edbd-4709-8c3f-00de22da399a)

-----

# 📋 Índice

### [1 Visão Geral](#1-visão-geral-1)
  - [**1.1 Sobre o Projeto**](#-11-sobre-o-projeto)
  - [**1.2. Para Quem é Este Repositório**](#12-para-quem-é-este-repositório)

### [2 Guia de Uso Prático](#2-guia-de-uso-prático-1)
  - [**2.1. Quick Start:**](#21-quick-start)
  - [**2.2. Como Usar o Repositório (Guias por Perfil)**](#22--como-usar-o-repositório-por-perfil)
    - [Para Arquitetos de Soluções](#para-arquitetos-de-soluções)
    - [Para Desenvolvedores](#para-desenvolvedores)
    - [Para Pesquisadores](#para-pesquisadores)
    - [Para Estudantes](#para-estudantes)

### [3 Fundamentos da RAG](#3-fundamentos-da-rag-1)

### [4 Contribuições Brasileiras (SBC)](#4-contribuições-brasileiras-sbc-1)

### [5 Taxonomia Temporal: Categorias C1-C5](#5-taxonomia-temporal-categorias-c1-c5-1)

### [6 Framework de Decisão](#6-framework-de-decisão-1)
  - [6.1 Árvore de Decisão](#61-árvore-de-decisão)
  - [6.2 Tabela Comparativa Multidimensional](#62-tabela-comparativa-multidimensional)
  - [6.3 Matriz de Adequação Técnica por Cenário](#63-matriz-de-adequação-técnica-por-cenário)

### [7 Validação e Estudo de Caso: Chatbot para o Campeonato Brasileiro](#7-estudo-de-caso-chatbot-para-o-campeonato-brasileiro-1)

### [8 Bibliografia](#8-bibliografia-1)
    
-----
# 1. Visão Geral

## 🎯 1.1 Sobre o Projeto

### O Desafio

LLMs enfrentam limitações fundamentais:

  - **Conhecimento estático**: informações desatualizadas após o treinamento
  - **Ausência de dados especializados**: sem acesso a informações proprietárias ou de domínio específico
  - **Múltiplas soluções disponíveis**: RAG, Fine-Tuning, Long Context, Tool-Augmented... mas qual escolher?

### A Solução

Este repositório apresenta um **framework prático de decisão** que transforma o debate teórico sobre técnicas de aprimoramento de LLMs em uma ferramenta aplicável, especialmente relevante para a comunidade brasileira de IA.

### Principais Contribuições

✅ **Taxonomia Temporal (C1-C5)**: Classificação organizada das técnicas pelo momento de disponibilização do conhecimento ao modelo

✅ **Árvore de Decisão**: Guia visual para seleção técnica baseada em critérios objetivos

✅ **Matriz de Adequação**: Mapeamento de técnicas por cenários reais de aplicação

✅ **Validação Prática**: Análise comparativa de aplicações reais contra o framework proposto

✅ **Contexto Brasileiro**: Destaque para contribuições da comunidade SBC e aplicações nacionais

## 1.2. Para Quem é Este Repositório

  - **Arquitetos de Soluções**: Decisões fundamentadas sobre qual técnica usar
  - **Desenvolvedores**: Referência prática com código reproduzível
  - **Pesquisadores**: Base consolidada da literatura com foco em contribuições brasileiras
  - **Estudantes**: Material didático estruturado sobre aprimoramento de LLMs

-----

# 2. Guia de Uso Prático

## 2.1⚡ Quick Start

### Descubra Rapidamente Qual Técnica Usar

**Seus dados são privados/proprietários?**

  - ✅ **SIM** → Vá para a [Árvore de Decisão - Ramo A](https://github.com/gdaias/RAG-Alternatives-Framework/blob/main/assets/arvore de decisao/arvore_decisao_A.png)
  - ❌ **NÃO** → Vá para a [Árvore de Decisão - Ramo B](https://github.com/gdaias/RAG-Alternatives-Framework/blob/main/assets/arvore_decisao_B.png)

**Já sabe seu cenário?** Consulte a [Matriz de Adequação por Cenário](https://github.com/gdaias/RAG-Alternatives-Framework/blob/main/assets/matriz de adequacao.png)

**Quer ver na prática?** Explore o [Estudo de Caso: Chatbot do Campeonato Brasileiro de Futebol](https://github.com/evellynnicole/FutChat.git)

### Navegação Rápida por Categoria

| Categoria | O que é | Quando usar | Exemplos |
|-----------|---------|-------------|----------|
| [**C1**](#categoria-1-internalização-de-conhecimento-no-treino) | Internalização de conhecimento no treino (modificação de pesos do modelo) | Conhecimento estável, recursos disponíveis | Fine-Tuning, LoRA, QLoRA |
| [**C2**](#categoria-2-recuperação-de-conhecimento-externo-tempo-real) | Recuperação de conhecimento externo em tempo real | Dados dinâmicos, atualizações frequentes | RAG tradicional, Hybrid Retrieval, GraphRAG, Search-First, Tool-Augmented |
| [**C3**](#categoria-3-expansão-da-janela-de-contexto) | Expansãoo da janela de contexto (no prompt) | Documentos completos, \<1M tokens | Long Context |
| [**C4**](#categoria-4-otimização-do-raciocínio) | Otimização do raciocínio (processamento da informação) | Problemas complexos, sem dados externos, técnica complementar | Chain-of-Thought |
| [**C5**](#categoria-5-protocolos-e-frameworks-de-habilitação) | Protocolos e Frameworks de Habilitação | Infraestrutura de suporte para outras categorias | Knowledge Graphs, Neuro-Simbólico, Model Context Protocol |

## 2.2 🚀 Como Usar o Repositório (por perfil)

### Para Arquitetos de Soluções

**Objetivo**: Escolher a técnica adequada para seu projeto

1.  **Identifique as características do seu problema**

      - Volume de dados a processar
      - Frequência de atualização necessária
      - Requisitos de privacidade
      - Recursos computacionais disponíveis

2.  **Consulte a Árvore de Decisão**

      - Siga o fluxo de perguntas em [Árvore de Decisão Completa](https://www.mermaidchart.com/d/669786ad-edbd-4709-8c3f-00de22da399a)

3.  **Valide com a Matriz de Cenários**

      - Encontre cenários similares em [Matriz de Adequação por Cenário](#63-matriz-de-adequação-técnica-por-cenário)
      - Compare com a [Tabela Comparativa Multidimensional](#62-tabela-comparativa-multidimensional)

4.  **Consulte o Estudo de Caso**

      - Veja implementação prática em [Estudo de Caso: Chatbot do Campeonato Brasileiro de Futebol](https://github.com/evellynnicole/FutChat.git)

### Para Desenvolvedores

**Objetivo**: Implementar a técnica escolhida

1.  **Estude a categoria selecionada**

      - Leia a documentação da categoria (C1-C5)
      - Revise as referências acadêmicas citadas

2.  **Analise o código de exemplo**

      - Explore o estudo de caso em [Estudo de Caso: Chatbot do Campeonato Brasileiro de Futebol](https://github.com/evellynnicole/FutChat.git)
      - Consulte o [TCC completo da Evellyn](http://repositorio.bc.ufg.br//handle/ri/27277)

3.  **Adapte para seu contexto**

      - Use a arquitetura como referência
      - Considere as lições aprendidas documentadas

### Para Pesquisadores

**Objetivo**: Fundamentação teórica e referências

1.  **Revisão bibliográfica**

      - [Fundamentos da RAG](#3--fundamentos-da-rag): artigos seminais
      - [Contribuições Brasileiras](#4--contribuições-brasileiras-sbc): trabalhos SBC

2.  **Framework acadêmico**

      - [Taxonomia conceitual](#5-️-taxonomia-temporal-categorias-c1-c5)
      - Artigo completo em [RAG e Suas Alternativas: Um Framework para o Aprimoramento de Grandes Modelos de Linguagem](https://drive.google.com/file/d/1aMzeUXOVJrcXkTpRxJLBJ6c9-tD00dic/view?usp=sharing)

3.  **Citação do trabalho**

(Adicionar a citação do artigo)

### Para Estudantes

**Objetivo**: Aprendizado estruturado

**Caminho recomendado**:

1.  Comece com [Sobre o Projeto](#-11-sobre-o-projeto)
2.  Leia [Fundamentos da RAG](#3--fundamentos-da-rag)
3.  Explore a [Taxonomia C1-C5](#5-️-taxonomia-temporal-categorias-c1-c5)
4.  Pratique com o [Estudo de Caso](#7--estudo-de-caso-chatbot-para-o-campeonato-brasileiro)
5.  Teste sua compreensão usando o [Framework de Decisão](#6--framework-de-decisão)

-----

# 3 📚 Fundamentos da RAG

### O que é Retrieval-Augmented Generation?

A Geração Aumentada por Recuperação (**RAG**) foi introduzida por Lewis et al. (2020) para superar a limitação de **conhecimento paramétrico estático** dos LLMs. A arquitetura combina um componente de recuperação densa com um modelo generativo, permitindo que o modelo acesse informações atualizadas sem necessidade de retreinamento.

### Arquitetura Original

A RAG fundamenta-se em três componentes principais:

1.  **Indexador**: Processa e armazena representações vetoriais de uma base de conhecimento externa
2.  **Recuperador**: Identifica documentos mais relevantes para uma consulta específica
3.  **Gerador**: Produz respostas utilizando tanto a consulta quanto os documentos recuperados como contexto

### Evolução Arquitetural

#### 2022: Integração Profunda

**RETRO (Retrieval-Enhanced Transformer)** - Borgeaud et al. incorporaram mecanismos de recuperação diretamente na arquitetura do transformer, permitindo acesso a trilhões de tokens.

#### 2023: Otimizações e Especializações

  - **Modelos de embedding especializados** por domínio
  - **Chunking semântico** preservando coerência contextual
  - **Busca híbrida** combinando similaridade semântica com filtros de metadados
  - **In-Context RAL** - Ram et al. propuseram atualização dinâmica via contexto estendido

### 📖 Artigos Seminais

| Ano | Trabalho | Contribuição | Link |
|-----|----------|--------------|------|
| 2020 | **Lewis et al.** - RAG | Arquitetura fundacional da RAG | [NeurIPS 2020](https://arxiv.org/abs/2005.11401) |
| 2021 | **Izacard & Grave** - FiD | Escalabilidade em QA | [TACL 2021](https://arxiv.org/abs/2007.01282) |
| 2022 | **Borgeaud et al.** - RETRO | Integração com transformer | [ICML 2022](https://arxiv.org/abs/2112.04426) |
| 2023 | **Ram et al.** - In-Context RAL | Contexto estendido dinâmico | [arXiv 2023](https://arxiv.org/abs/2302.00083) |
| 2023 | **Shi et al.** - LLM Retrievers | LLMs como recuperadores zero-shot | [arXiv 2023](https://arxiv.org/abs/2304.14233) |

-----

## 4 🇧🇷 Contribuições Brasileiras (SBC)

A partir de 2024, a comunidade acadêmica brasileira demonstrou assimilação e adaptação da RAG ao contexto nacional, com publicações em eventos da Sociedade Brasileira de Computação (**SBC**).

**Domínio Jurídico**

> **Arquiteturas RAG para Documentação Legal**
> - Paranhos et al. (2024) - Avaliação de padrões arquiteturais RAG em domínios jurídicos
>    - [XII ERI-GO 2024](http://repositorio.bc.ufg.br/handle/ri/27276)
>    - Desafios: complexidade terminológica e hierarquias normativas brasileiras

> **Extração Automatizada de Dados Legais**
> - Aquino et al. (2024) - 90% de precisão em identificação de elementos jurídicos
>   - [SBBD 2024](https://sol.sbc.org.br/index.php/sbbd_estendido/article/view/31268)

**Domínio Educacional**

> **Questões Multimodais do ENEM**
> - Taschetto & Fileto (2024) - RAG para processamento texto-imagem
>   - [SBBD 2024](https://sol.sbc.org.br/index.php/sbbd/article/view/30233)
>   - Relevância: especificidade cultural e linguística do sistema educacional brasileiro

> **Assistentes Virtuais Institucionais**
> - Kuratomi et al. (2024) - Aumento de precisão de 13,68% para 54,02%
>   - [ENIAC 2024](https://sol.sbc.org.br/index.php/eniac/article/view/31884)
> - Souza et al. (2024) - IFBot para instituições educacionais
>   - [WICS 2024](https://sol.sbc.org.br/index.php/wics/article/view/31611)

**Contribuições Metodológicas**

> - Souza et al. (2024) - TableRAG
>   - [STIL 2024](https://sol.sbc.org.br/index.php/stil/article/view/31349)
>   - 86,7% eficácia em recuperação | 74% acurácia em QA sobre tabelas
>   - Pipeline especializado para dados tabulares
    
**Estudos Comparativos**
> - da Costa et al. (2024) - Comparação Fine-Tuning vs RAG para tarefas em português
>   - [STIL 2024](https://sol.sbc.org.br/index.php/stil/article/view/31350)

**Implementação Local**
> - Rocha & Pessoa (2024) - Análise crítica de limitações em LLMs locais
>   - [ENIAC 2024](https://sol.sbc.org.br/index.php/eniac/article/view/31880)
>   - Foco: soberania tecnológica no contexto brasileiro

**Aplicações Empresariais**
> - Siqueira et al. (2024) - Integração de dados estruturados em chatbots empresariais
>   - [STIL 2024](https://sol.sbc.org.br/index.php/stil/article/view/31348)

-----

## 5 🗂️ Taxonomia Temporal: Categorias C1-C5

A classificação organiza as técnicas de aprimoramento segundo o **momento em que o conhecimento é disponibilizado ao modelo**, estruturadas em uma linha temporal do treinamento à infraestrutura de suporte.


### Categoria 1: Internalização de Conhecimento (no Treino)

**Momento**: Modificação dos pesos do modelo antes da inferência

Técnicas que incorporam conhecimento de forma permanente através do ajuste de parâmetros.

| Técnica | Descrição | Quando Usar |
|---------|-----------|-------------|
| **Fine-Tuning Completo** | Retreinamento de todos os parâmetros | Especialização profunda com recursos abundantes |
| **LoRA** (Low-Rank Adaptation) | Adaptação de baixo rank, modificando subconjuntos | Especialização eficiente com recursos limitados |
| **QLoRA** (Quantized LoRA) | LoRA com quantização para ainda mais eficiência | Dispositivos edge ou ambientes com restrições severas |

**Vantagens**

  - ✅ Independência de infraestrutura externa na inferência
  - ✅ Latência reduzida (sem busca em tempo real)
  - ✅ Privacidade total dos dados

**Limitações**

  - ❌ Custos elevados para atualizações frequentes
  - ❌ Risco de catastrophic forgetting
  - ❌ Inadequado para informações altamente dinâmicas

**Referências**: [Howard & Ruder, 2018](https://arxiv.org/abs/1801.06146) | [Hu et al., 2022](https://arxiv.org/abs/2106.09685) | [Dettmers et al., 2023](https://arxiv.org/abs/2305.14314)


### Categoria 2: Recuperação de Conhecimento Externo (Tempo Real)

**Momento**: Acesso a fontes externas durante a inferência

Paradigma "just-in-time knowledge" - a categoria mais ampla da taxonomia.

| Técnica | Descrição | Caso de Uso Ideal |
|---------|-----------|-------------------|
| **RAG Tradicional** | Recuperação densa + geração contextual | Bases internas extensas, atualizações frequentes |
| **Hybrid Retrieval** | Busca densa (semântica) + esparsa (BM25) | Máxima cobertura e precisão em grandes volumes |
| **GraphRAG** | Integração com grafos de conhecimento | Navegação relacional e raciocínio multi-hop |
| **Search-First** | APIs de busca externa direta | Informações públicas, sem infraestrutura própria |
| **Tool-Augmented** | LLM chama ferramentas especializadas | Acesso a APIs, calculadoras, bancos de dados |
| **Neuro-Simbólico** | Recuperação neural + raciocínio simbólico | Domínios que exigem garantias lógicas formais |

**Vantagens**

  - ✅ Máxima flexibilidade para dados dinâmicos
  - ✅ Atualização sem retreinamento
  - ✅ Acesso a conhecimento especializado sob demanda

**Limitações**

  - ❌ Complexidade operacional
  - ❌ Dependência de infraestrutura externa
  - ❌ Latência adicional na recuperação

**Referências**: [Lewis et al., 2020](https://arxiv.org/abs/2005.11401) | [Ma et al., 2021](https://arxiv.org/abs/2104.08663) | [Edge et al., 2024](https://arxiv.org/abs/2404.16130) | [Qin et al., 2023](https://arxiv.org/abs/2307.16789)


### Categoria 3: Expansão da Janela de Contexto

**Momento**: Fornecimento do conhecimento completo no prompt

Abordagem de "força bruta" viabilizada por avanços arquiteturais recentes.

| Subcategoria | Descrição | Exemplo |
|--------------|-----------|---------|
| **C3A - Expansão Passiva** | Usuário fornece manualmente todo o contexto | Upload de documentos completos |
| **C3B - Expansão Ativa** | Modelo gerencia contexto automaticamente | Sistemas emergentes com gerenciamento autônomo |

**Modelos Disponíveis**: Gemini 1.5 (1M+ tokens), Claude (1M+ tokens)

**Vantagens**

  - ✅ Simplicidade arquitetural (sem chunking)
  - ✅ Compreensão holística de documentos
  - ✅ Sem infraestrutura de recuperação

**Limitações**

  - ❌ Volume total limitado pela janela
  - ❌ Custos elevados por token
  - ❌ Inadequado para bases massivas (\>1M tokens)


### Categoria 4: Otimização do Raciocínio

**Momento**: Durante a inferência, na estruturação do prompt

Técnicas que melhoram o processamento da informação existente, sem adicionar conhecimento novo.

| Técnica | Descrição | Aplicação Ideal |
|---------|-----------|-----------------|
| **Chain-of-Thought (CoT)** | Raciocínio passo a passo explícito | Problemas matemáticos e lógicos complexos |
| **Prompting Avançado** | Estruturação estratégica de instruções | Decomposição de tarefas complexas |

**Vantagens**

  - ✅ Baixo custo de implementação
  - ✅ Sem infraestrutura adicional
  - ✅ Complementar a outras categorias

**Limitações**

  - ❌ Limitado ao conhecimento paramétrico
  - ❌ Não resolve obsolescência de dados

**Referências**: [Wei et al., 2022](https://arxiv.org/abs/2201.11903)


### Categoria 5: Protocolos e Frameworks de Habilitação

**Momento**: Define a infraestrutura sobre a qual o sistema opera

Não são técnicas de aprimoramento direto, mas habilitam outras categorias.

| Protocolo | Função | Habilita |
|-----------|--------|----------|
| **Knowledge Graphs** | Ontologias formais com garantias lógicas | GraphRAG, Neuro-Simbólico |
| **Model Context Protocol (MCP)** | Descoberta e uso autônomo de ferramentas | Tool-Augmented Generation em escala |

**Características**

  - 🔧 Infraestrutura de suporte
  - 🔧 Auditabilidade e rastreabilidade
  - 🔧 Padronização de interfaces

**Referências**: [Ji et al., 2022](https://ieeexplore.ieee.org/document/9416312)

-----

## 6 🎯 Framework de Decisão

### 6.1 Árvore de Decisão

[**Árvore de Decisão Completa**](https://www.mermaidchart.com/d/669786ad-edbd-4709-8c3f-00de22da399a)
A árvore orienta a seleção técnica através de perguntas sequenciais sobre características fundamentais do problema:

**Ramo A - Dados Privados/Proprietários**

![Árvore de Decisão - Dados Privados](assets/arvore de decisao/arvore_decisao_A.png)

**Ramo B - Dados Públicos**

![Árvore de Decisão - Dados Públicos](assets/arvore de decisao/arvore_decisao_B.png)

### 6.2 Tabela Comparativa Multidimensional

| Cat. | Técnica | Volume | Freq. Atual. | Privacidade | Recursos | Latência | Orçamento | Expertise |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| C1 | Fine-tuning | M-G | Baixa | Total | Alto | Baixa | Alto | Alto |
| | LoRA/QLoRA | P-M | Baixa | Total | Médio | Baixa | Médio | Médio |
| C2 | RAG Tradicional | Grande | Alta | Configurável | M-A | Média | M-A | Médio |
| | Hybrid Retrieval| Grande | Alta | Configurável | Alto | Média | Alto | Alto |
| | GraphRAG | M-G | Média | Configurável | Alto | Alta | Alto | Alto |
| | Search-First | Ilimitado\* | Máxima | Limitada | Baixo | Média | Baixo-M | Baixo |
| | Tool-Augmented | Configurável | Alta | Configurável | Médio | Variável | Médio | M-A |
| C3 | Long Context | Pequeno\*\* | N/A\*\*\* | Variável | M-A | Média-A | Alto | Baixo-M |
| C4 | Chain-of-Thought | N/A\*\*\*\* | N/A\*\*\*\* | Total | Baixo | Baixa | Baixo | Baixo-M |
| C5 | Knowledge Graphs | M-G | Baixa-M | Total | Médio | Baixa | Alto | Alto |
| | Neuro-Simbólico | Médio | Baixa | Total | Muito Alto | Média-A | Muito Alto| Muito Alto|


**Legenda:** P=Pequeno (<1GB), M=Médio (1GB-100GB), G=Grande (>100GB), A=Alto, M-A=Médio-Alto, M-G=Médio-Grande.
- **\*** Limitado apenas por disponibilidade pública de informações.
- **\*\*** Limitado à janela de contexto (tipicamente <1M tokens).
- **\*\*\*** Atualização depende da fonte de contexto fornecida.
- **\*\*\*\*** Opera sobre conhecimento paramétrico existente.


### 6.3 Matriz de Adequação Técnica por Cenário

| Cenário de Aplicação | Técnica Primária | Justificativa | Alternativas Complementares |
|---------------------|------------------|---------------|----------------------------|
| **Suporte ao Cliente** | RAG Tradicional (C2) | Bases internas extensas requerem precisão factual e atualização dinâmica | Tool-Augmented (C2) para integração com CRM e sistemas transacionais |
| **Conformidade Regulatória** | GraphRAG (C2) | Navegação em hierarquias normativas com rastreabilidade de fontes legais | Fine-tuning (C1) quando terminologia é específica e estável |
| **Pesquisa Acadêmica** | Hybrid Retrieval (C2) | Maximiza cobertura e precisão em grandes volumes de literatura | Long Context (C3) para análise holística de artigos individuais |
| **Desenvolvimento de Software** | Tool-Augmented (C2) | Integração com ferramentas especializadas (linters, testes, docs) | RAG Tradicional (C2) para repositórios com patterns específicos |
| **Aplicações Mobile/Edge** | LoRA/QLoRA (C1) | Execução local eficiente com recursos limitados e privacidade | Chain-of-Thought (C4) para raciocínio sem infraestrutura adicional |
| **Análise de Documentos Legais** | GraphRAG (C2) | Hierarquias normativas brasileiras complexas | Knowledge Graphs (C5) para auditabilidade completa |
| **Chatbots Educacionais** | RAG Tradicional (C2) | Conteúdo institucional dinâmico, atualizações frequentes | Long Context (C3) para materiais didáticos extensos |
| **Assistentes Médicos** | Neuro-Simbólico (C2) | Garantias lógicas formais, rastreabilidade de raciocínio | GraphRAG (C2) para bases de conhecimento médico |

-----

## 7 🔬 Estudo de Caso: Chatbot para o Campeonato Brasileiro

### Contexto e Motivação

**Domínio**: Campeonato Brasileiro de Futebol Série A

**Objetivo**: Fornecer respostas precisas sobre partidas, estatísticas de jogadores e classificações em tempo real.

**Desafios Identificados**:

1.  Dados inerentemente dinâmicos (atualizações diárias/semanais)
2.  Informações estruturadas em formato tabular (artilharia, resultados, classificações)
3.  Conhecimento paramétrico dos LLMs não inclui eventos recentes
4.  Dados tabulares não são nativos ao conhecimento dos modelos

### Decisão Arquitetural

**Técnica Escolhida**: Tool-Augmented RAG (Categoria C2) - Padrão Text-to-SQL

**Justificativa pela Taxonomia**:

  - ✅ Dados estruturados (SQL) + dinâmicos (atualizações frequentes) → C2
  - ✅ Necessidade de acesso a ferramentas especializadas (banco de dados)
  - ✅ Precisão factual crítica (estatísticas esportivas)

### Arquitetura Implementada

```mermaid
graph TD
    A[Pergunta do Usuário] --> B{Banco Vetorial - Qdrant};
    B --> C{LLM - Geração SQL};
    C --> D[Banco SQLite - Execução da Query];
    D --> E{LLM - Síntese Final};
    E --> F[Resposta ao Usuário];
    B & C & D & E -.- G[Contexto/Resultados];
    style G fill:#cf04cf,stroke:#333
```

### Componentes Técnicos

**1. Banco de Dados Vetorial (Qdrant)**

Armazena três tipos de informações recuperáveis:

  - **Esquemas de Tabelas**: Trechos dos `CREATE TABLE` relevantes
  - **Documentação Semântica**: Descrições em linguagem natural de tabelas e colunas
  - **Exemplos Few-Shot**: Pares "pergunta-SQL" validados

**2. Pipeline de Recuperação**

```python
# Exemplo conceitual do fluxo
pergunta = "Quem fez mais gols no Brasileirão?"

# Busca vetorial retorna:
contexto = {
    "esquema": "CREATE TABLE artilharia (jogador TEXT, gols INTEGER, ...)",
    "docs": "A tabela artilharia contém estatísticas de gols por jogador",
    "exemplos": [
        {"Q": "Quantos gols tem o Pedro?", "SQL": "SELECT gols FROM..."}
    ]
}

# LLM gera SQL contextualizado
sql_gerado = llm.generate(pergunta, contexto)
```

**3. Validação e Resultados**

Dataset de validação contendo:

  - Perguntas em linguagem natural
  - SQL de referência correspondente
  - Resultado esperado

**Dificuldades Iniciais**:

  - ❌ Lógica temporal complexa (datas)
  - ❌ Sequências (vitórias consecutivas)
  - ❌ Perguntas compostas

**Melhorias Implementadas**:

  - ✅ Enriquecimento do banco vetorial com mais exemplos
  - ✅ Documentação detalhada de casos edge
  - ✅ Geração de SQL idêntico ao de referência para perguntas diversas

**Alinhamento com o Framework**

| Critério | Avaliação | Confirmação da Escolha |
|---------|-----------|------------------------|
| Volume de Dados | Médio (tabelas estruturadas) | ✅ C2 adequado |
| Frequência de Atualização | Alta (jogos semanais) | ✅ C2 necessário |
| Privacidade | Dados públicos | ✅ C2 sem restrições |
| Recursos Computacionais | Médios | ✅ RAG mais eficiente que Fine-tuning |
| Latência | Média aceitável | ✅ Tool-Augmented viável |
| Especialização | Domínio específico mas dinâmico | ✅ C2 \> C1 (dados mudam constantemente) |

**Código e Documentação Completa**

O desenvolvimento completo deste estudo de caso está documentado no trabalho de conclusão de curso:

ROSA, Evellyn Nicole Machado. Automatização de consultas SQL com Retrieval-Augmented Generation (RAG): uma abordagem para a conversão de texto aplicada a dados do campeonato brasileiro. 2025. 99 f. Trabalho de Conclusão de Curso (Bacharelado em Inteligência Artificial) - Instituto de Informática, Universidade Federal de Goiás, Goiânia, 2024.

📄 [Acesso ao TCC Completo](https://repositorio.bc.ufg.br/items/2aec1425-bf78-41b7-b559-dd95078aebc4) | 🔗 [Repositório de Código](https://github.com/evellynnicole/FutChat.git)

**Lições Aprendidas**

  - **Tool-Augmented RAG é eficaz para dados estruturados dinâmicos**

      - Combina flexibilidade da RAG com precisão de consultas estruturadas

  - **Qualidade da recuperação é crítica**

      - Exemplos few-shot e documentação semântica melhoram significativamente a geração

  - **Validação iterativa é essencial**

      - Dataset de validação permitiu identificar e corrigir casos edge

  - **Framework confirmado na prática**

      - Decisão por C2 (Tool-Augmented) alinhada com características do problema

-----

### 8 Bibliografia

  * Aquino, I. V. d., Santos, M. M. d., Dorneles, C. F., and Carvalho, J. T. (2024). *Extracting information from brazilian legal documents with retrieval augmented generation.*
  * Borgeaud, S. et al. (2022). *Improving language models by retrieving from trillions of tokens.*
  * da Costa, L. Y. et al. (2024). *A comparative study of fine-tuning and rag strategies for portuguese qa tasks.*
  * Howard, J. and Ruder, S. (2018). *Universal language model fine-tuning for text classification.*
  * Kuratomi, G., Pirozelli, P., Cozman, F., and Peres, S. M. (2024). *A rag-based institutional assistant.*
  * Lewis, P. et al. (2020). *Retrieval-augmented generation for knowledge-intensive nlp tasks.*
  * Paranhos, S. L. et al. (2024). *Avaliação do impacto de diferentes padrões arquiteturais rag em domínios jurídicos.*
  * Souza, E. A. d. et al. (2024a). *Tablerag: A novel approach for augmenting Ilms with information from retrieved tables.*
  * Taschetto, L. d. C. and Fileto, R. (2024). *Using retrieval-augmented generation to improve performance of large language models on the brazilian university admission exam (enem).*
  * Wei, J. et al. (2022). *Chain-of-thought prompting elicits reasoning in large language models.*
