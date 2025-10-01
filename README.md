# RAG-Alternatives-Framework 
**Framework de Decisão Prático (RAG e Alternativas)**

Apresentamos o repositório com materiais utilizados e gerados pelo artigo "RAG e Suas Alternativas: Um Framework para o
Aprimoramento de Grandes Modelos de Linguagem". Aqui você encontra mais informações sobre:

* Taxonomia (C1-C5)
* Árvore de Decisão (Framework)
* Matriz de Cenários para **Aprimoramento de Grandes Modelos de Linguagem (LLMs)**
* Estudos de caso ("Chatbot para o Campeonato Brasileiro de Futebol" e "Sistema RAG para Análise de Reações Químicas")

Esse guia para desenvolvedores de IA auxilia na escolha da melhor técnica para aprimoramento de LLMs (*RAG, Fine-Tuning, Tool-Augmented etc*) considerando as necessidades e restrições de desenvolvimento tendo em vista o cenário brasileiro.

---

## Estrutura Principal do Framework

### 1. Taxonomia Temporal: Categorias de Aprimoramento (C1-C5)

A taxonomia organiza as técnicas pelo **momento em que o conhecimento é disponibilizado** ao modelo.

| Cat. | Nome | Momento de Disponibilização | Técnicas Chave |
| :--- | :--- | :--- | :--- |
| **C1** | Internalizac ̧ao de Conhecimento (no Treino) | Modificação dos pesos do modelo para incorporar conhecimento de forma permanente antes da inferência | Fine-Tuning, LoRA/QLORA |
| **C2** | Recuperação de Conhecimento Externo (em Tempo Real) | Acesso a fontes externas em Tempo Real/Inferência | RAG Tradicional, GraphRAG, Search-First, Tool-Augmented |
| **C3** | Expansão da Janela de Contexto | Fornecimento do conhecimento completo no prompt | Long Context Models (>1M tokens) |
| **C4** | Otimização do Raciocínio | Melhora do processamento da informação existente | Chain-of-Thought (CoT) |
| **C5** | Protocolos e Frameworks de Habilitação | Infraestrutura de suporte que viabiliza outras categorias | Knowledge Graphs (KG), Model Context Protocol (MCP) |

### 2. Árvore de Decisão

![](https://drive.google.com/uc?export=download&id=1wXpMsHPtxQD9ud6OsDoOdTZFvzw1YHfM)

### 3. Matriz de Adequação Técnica por Cenário

| Cenário de Aplicação | Técnica Primária | Justificativa e Opções |
| :--- | :--- | :--- |
| **Suporte ao Cliente** | RAG Tradicional (C2) | Bases internas extensas requerem RAG para precisao factual e atualização dinâmica. Alternativa: Tool-Augmented (C2) para integração com CRM e sistemas transacionais |
| **Conformidade Regulatória** | GraphRAG (C2) | Navegação em hierarquias normativas complexas com rastreabilidade de fontes legais. Alternativa: Fine-tuning (C1) quando terminologia e específica e estável |
| **Pesquisa Acadêmica** | Hybrid Retrieval (C2) | Maximiza cobertura e precisao em grandes volumes de literatura científica. Complementar: Long Context (C3) para análise holística de artigos individuais |
| **Desenvolvimento de Software** | Tool-Augmented (C2) | Integração com ferramentas especializadas (linters, testes, documentação). Complementar: RAG Tradicional (C2) para repositorios com patterns específicos |
| **Aplicações Mobile/Edge** | LORA/QLORA (C1) | Execução local eficiente com recursos limitados e preservação de privacidade. Complementar: Chain-of-Thought (C4) para racioc ́ınio sem infraestrutura adicional |

---

## 🔬 Estudos de Caso

Validação da versatilidade da RAG através de dois estudos de caso em domínios que exigem **dados atualizados, dinâmicos e especializados**.

1. **Chatbot para o Campeonato Brasileiro de Futebol:** Aplicação de **Tool-Augmented RAG** (padrão Text-to-SQL) para lidar com dados estruturados e em tempo real, exigindo que o LLM execute código SQL.
2.  **Sistema RAG para Análise de Reações Químicas:** Utilização de **RAG Avançado** em um domínio altamente especializado (ORD), justificada pela necessidade de atualizações frequentes e limitação de recursos computacionais.

---

## 🔗 Referência

Este repositório serve como material de apoio e detalhamento para o artigo:

**RAG e Suas Alternativas: Um Framework para o Aprimoramento de Grandes Modelos de Linguagem**

* **Link para o Artigo Completo ()**
