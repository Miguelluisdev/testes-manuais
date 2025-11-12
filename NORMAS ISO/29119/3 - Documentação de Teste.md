# 🧾 ISO/IEC/IEEE 29119-3 – Test Documentation

## 📘 Visão Geral

A **ISO/IEC/IEEE 29119-3**, intitulada **“Test Documentation”**, tem como **escopo e objetivo principal** fornecer um conjunto **padronizado de modelos (templates)** e **exemplos práticos** para toda a documentação relacionada ao **teste de software**.
Ela cobre **todo o ciclo de vida do teste**, garantindo **clareza, rastreabilidade e repetibilidade** das atividades.

Esta parte da norma **substitui o antigo padrão IEEE 829**, consolidando uma abordagem mais moderna e flexível para documentar testes em diferentes tipos de projeto — desde os **tradicionais (cascata)** até os **ágeis**.

---

## 🎯 Objetivo e Importância

A documentação de teste é **fundamental para a comunicação eficaz** entre as partes interessadas, **garantia de rastreabilidade** dos requisitos e **reprodutibilidade** das atividades de teste.
A ISO/IEC/IEEE 29119-3 busca **padronizar esses documentos**, de forma que possam ser compreendidos e utilizados **universalmente**, independentemente do modelo de ciclo de vida adotado.

Entre seus principais propósitos estão:

* Garantir **consistência e clareza** nas informações de teste.
* Viabilizar **auditorias e conformidade** com requisitos regulatórios.
* Fornecer uma **base documental sólida** para equipes de QA, desenvolvimento e stakeholders.
* Promover **reutilização e rastreabilidade** de informações entre os artefatos de teste.

---

## 🧩 Estrutura e Conteúdo da Norma

Os **modelos de documentação** propostos pela 29119-3 são **alinhados** com a estrutura de processos definida na **ISO/IEC/IEEE 29119-2**, garantindo **consistência** entre as atividades e seus artefatos.

Ela contempla diversos tipos de teste:

* ✅ Testes dinâmicos
* ✅ Testes funcionais e não funcionais
* ✅ Testes manuais e automatizados
* ✅ Testes baseados em script e não scriptados (exploratórios)

A norma também suporta a **integração com metodologias ágeis**, permitindo que os documentos sejam adaptados por meio do conceito de **"sensible tailoring"** — ou seja, a **adaptação sensata** do nível de detalhe e da quantidade de documentação conforme o contexto do projeto.

---

## 🧱 Principais Artefatos de Documentação

| **Nome do Artefato**                                                      | **Propósito Principal**                                                                                        |
| ------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Política de Teste**                                                     | Define os princípios, intenções e direção da organização em relação ao teste.                                  |
| **Práticas de Teste Organizacional**                                      | Detalha métodos, procedimentos e atividades de teste específicas da organização.                               |
| **Plano de Teste (Test Plan)**                                            | Descreve o escopo, abordagem, recursos e cronograma das atividades de teste planejadas.                        |
| **Relatório de Status de Teste (Test Status Report)**                     | Fornece atualizações periódicas sobre o progresso e o estado atual das atividades de teste.                    |
| **Relatório de Conclusão de Teste (Test Completion Report)**              | Resume os resultados e as atividades de teste realizadas ao final de uma fase ou projeto.                      |
| **Especificação de Modelo de Teste (Test Model Specification)**           | Representação abstrata do sistema sob teste usada para derivar casos de teste (substitui “condição de teste”). |
| **Especificação de Caso de Teste (Test Case Specification)**              | Detalha entradas, condições de execução e resultados esperados de cada caso de teste.                          |
| **Especificação de Procedimento de Teste (Test Procedure Specification)** | Define as instruções passo a passo para executar um ou mais casos de teste.                                    |
| **Relatório de Incidente (Incident Report)**                              | Documenta qualquer desvio do comportamento esperado (também conhecido como *bug report*).                      |
| **Log de Execução de Teste (Test Execution Log)**                         | Registra cronologicamente as atividades e os resultados observados durante a execução dos testes.              |

---

## 🧑‍💼 Público-Alvo

A **ISO/IEC/IEEE 29119-3** é voltada a **organizações e profissionais** que criam, utilizam ou gerenciam documentação de teste, tais como:

* Engenheiros e Analistas de QA
* Gerentes de Teste e de Projeto
* Auditores de Qualidade
* Clientes e Stakeholders
* Equipes que operam em **ambientes regulados** (banco, saúde, governo etc.)

---

## ⚖️ Adaptação em Ambientes Ágeis

Embora seja uma norma detalhada, ela **não impõe documentação excessiva**.
O princípio do **“sensible tailoring”** permite que o conteúdo seja ajustado de acordo com o contexto — garantindo **eficiência** sem sacrificar a **qualidade e rastreabilidade**.

Por exemplo:

* Em projetos ágeis, o **Plano de Teste** pode ser substituído por **documentos leves** ou **tickets no Azure DevOps**.
* O **Relatório de Incidente** pode ser um **bug registrado** diretamente no sistema de gestão de tarefas.
* O **Log de Execução** pode ser automatizado via **Cypress, Postman ou Jenkins**.

---

## 🔗 Relação com Outras Partes da Série 29119

A Parte 3 se **integra diretamente** às demais partes da norma:

* **Parte 1 – Concepts and Definitions:** fornece o vocabulário e os conceitos fundamentais.
* **Parte 2 – Test Processes:** define a estrutura de processos de teste que esta parte documenta.
* **Parte 4 – Test Techniques:** descreve as técnicas de design de teste aplicáveis aos documentos aqui definidos.
* **Parte 5 – Keyword-Driven Testing:** complementa a documentação com abordagens automatizadas baseadas em palavras-chave.

---

## 🧠 Conclusão

A **ISO/IEC/IEEE 29119-3** é essencial para garantir **padronização, rastreabilidade e qualidade documental** nos processos de teste.
Mais do que exigir “papelada”, ela propõe uma estrutura **adaptável e inteligente**, que pode ser moldada conforme a **realidade de cada projeto e metodologia** — desde empresas ágeis até corporações que precisam atender **requisitos regulatórios rigorosos**.

> 🧩 **Em resumo:** documentar bem é testar com clareza, e testar com clareza é garantir qualidade e confiança no produto final.
