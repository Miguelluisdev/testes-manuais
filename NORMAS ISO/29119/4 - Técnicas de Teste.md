# 🧮 ISO/IEC/IEEE 29119-4 – Test Techniques

## 📘 Visão Geral

A **ISO/IEC/IEEE 29119-4**, intitulada **“Test Techniques”**, é a parte da série que trata do **“como” projetar testes eficazes**.
Seu objetivo principal é **definir e descrever técnicas de design de teste de software** (ou *métodos de criação de casos de teste*) que podem ser aplicadas durante o processo de **design e implementação** de testes, conforme definido na **ISO/IEC/IEEE 29119-2**.

Esta norma é essencial para os profissionais de QA, pois fornece um **conjunto estruturado de abordagens** que ajudam a **maximizar a detecção de defeitos** e a **garantir cobertura adequada** das funcionalidades do sistema.

---

## 🎯 Escopo e Objetivo

O propósito da ISO/IEC/IEEE 29119-4 é **guiar os testadores** na escolha e aplicação das melhores técnicas de teste, levando em conta o **contexto, riscos e objetivos de qualidade** de cada projeto.

Ela fornece uma **estrutura metodológica** para a criação de casos de teste que sejam:

* Eficientes e eficazes
* Reprodutíveis e rastreáveis
* Proporcionem boa cobertura funcional e estrutural
* Adaptáveis a diferentes níveis de teste (unitário, integração, sistema, aceitação)

---

## 🧩 Estrutura da Norma

A norma organiza as **técnicas de design de teste** em **três grandes categorias**, cada uma baseada em diferentes fontes de informação e propósitos:

---

### ⚫ 1. Técnicas Baseadas em Especificação (*Caixa-Preta*)

Nessas técnicas, os testes são **derivados a partir da especificação funcional** ou de documentos que descrevem o comportamento esperado do sistema, **sem conhecimento do código-fonte**.
O objetivo é verificar **se o software faz o que deveria fazer**, conforme os requisitos.

🔹 **Exemplos:**

* Particionamento de Equivalência
* Análise de Valor Limite
* Tabelas de Decisão
* Grafos de Causa e Efeito
* Teste de Transição de Estado
* Teste de Cenário
* Método da Árvore de Classificação
* Teste de Sintaxe
* Técnicas Combinatórias (como *pairwise testing*)

📘 **Quando usar:**

* Em testes funcionais.
* Quando o comportamento esperado está bem documentado.
* Para validar regras de negócio e fluxos principais.

---

### ⚪ 2. Técnicas Baseadas em Estrutura (*Caixa-Branca*)

Essas técnicas utilizam o **conhecimento da estrutura interna** do código, arquitetura ou lógica do software para projetar os testes.
O foco é **verificar se todas as partes do código foram exercitadas** adequadamente.

🔹 **Exemplos:**

* Teste de Comando (*Statement Coverage*)
* Teste de Decisão (*Decision Coverage*)
* Teste de Condição e Ramificação (*Branch Condition Coverage*)
* Teste de Fluxo de Dados (*Data Flow Testing*)
* Cobertura de Decisão/Condição Modificada (*MCDC*)

📘 **Quando usar:**

* Em testes de unidade e integração.
* Quando há acesso ao código-fonte.
* Para garantir que todos os caminhos lógicos do sistema sejam validados.

---

### ⚪ 3. Técnicas Baseadas em Experiência

Essas técnicas dependem da **intuição, conhecimento e vivência do testador**.
Elas são úteis para encontrar **defeitos sutis ou inesperados** que podem escapar das técnicas mais formais.

🔹 **Exemplos:**

* Adivinhação de Erro (*Error Guessing*)
* Teste Exploratório
* Teste Baseado em Checklist
* Teste Aleatório

📘 **Quando usar:**

* Em fases iniciais de teste (descoberta).
* Quando não há documentação completa.
* Para complementar outras técnicas e aumentar a cobertura.

---

## 📊 Tabela 3 – Categorias e Exemplos de Técnicas de Teste

| **Categoria da Técnica**                   | **Técnicas de Exemplo**                                                                                                     |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------- |
| **Baseada em Especificação (Caixa-Preta)** | Particionamento de Equivalência, Análise de Valor Limite, Tabela de Decisão, Teste de Transição de Estado, Teste de Cenário |
| **Baseada em Estrutura (Caixa-Branca)**    | Teste de Comando, Teste de Decisão, Teste de Condição, Teste de Fluxo de Dados, MCDC                                        |
| **Baseada em Experiência**                 | Adivinhação de Erro (Error Guessing), Teste Exploratório, Teste Baseado em Checklist                                        |

---

## 🧠 Aplicação e Combinação de Técnicas

A norma enfatiza que **as técnicas não são excludentes** — pelo contrário, elas se tornam **mais eficazes quando combinadas**.

Por exemplo:

> 💡 Em um módulo de negócio complexo, pode-se aplicar:
>
> * **Tabelas de Decisão** para cobrir as regras de negócio (caixa-preta);
> * **Cobertura de Decisão** para validar a lógica interna (caixa-branca);
> * **Teste Exploratório** para encontrar comportamentos inesperados (baseado em experiência).

Essa **combinação orientada por risco** — princípio herdado da **ISO/IEC/IEEE 29119-2** — assegura um equilíbrio entre **eficiência, profundidade e custo de teste**.

---

## 👥 Público-Alvo

A **ISO/IEC/IEEE 29119-4** é voltada para todos os profissionais envolvidos no **design e execução de testes**, incluindo:

* Analistas e Engenheiros de Teste
* Líderes e Gerentes de QA
* Desenvolvedores que realizam testes de unidade
* Consultores e profissionais de garantia de qualidade

---

## 🔗 Integração com as Demais Partes da Série 29119

Esta parte da norma se conecta de forma direta com as demais:

* **Parte 1 – Concepts and Definitions:** fornece a base conceitual e terminológica.
* **Parte 2 – Test Processes:** define onde e quando as técnicas devem ser aplicadas.
* **Parte 3 – Test Documentation:** especifica como registrar os artefatos de design e execução das técnicas.
* **Parte 5 – Keyword-Driven Testing:** descreve a automação baseada em palavras-chave, aplicável às técnicas aqui apresentadas.

---

## 🧩 Conclusão

A **ISO/IEC/IEEE 29119-4** é o **coração técnico da série**, pois define **as ferramentas mentais e práticas** que transformam requisitos em **casos de teste eficazes**.
Ela permite que o QA atue de forma **estratégica e fundamentada**, combinando técnicas conforme o contexto, o risco e os objetivos do projeto.
