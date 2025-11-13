# 🧾 Relatório de Testes – Módulo de Busca (PHP Travels)

## 📌 Identificação

* **Sistema:** PHP Travels (Demo)
* **Módulo:** Módulo de Busca
* **Requisitos Funcionais:** RF-01.1 a RF-01.7
* **Responsável pelos testes:** Miguel Luis
* **Tipo de teste:** Funcional / Caixa-Preta
* **Técnicas utilizadas:** Partição de Equivalência, Análise de Valor Limite , Tabela de decisão
* **Ambiente:** Firefox 145v 64 bits windows 11 – Modo Web
* **Data da execução:** 12/11/2025

---

## 🎯 Objetivo do Teste

Validar o comportamento funcional do **módulo de busca principal**, assegurando que todas as abas (Hotels, Flights, Tours, Cars e Visa) executem buscas corretas, validem os campos obrigatórios e apresentem mensagens de erro adequadas.

---

## ✅ Resultados dos Casos de Teste

| ID     | Requisito | Descrição do Caso de Teste                                               | Resultado              | Observações                                         |
| ------ | --------- | ------------------------------------------------------------------------ | ---------------------- | --------------------------------------------------- |
| CT-001 | RF-01.1   | Verificar exibição das abas de busca e seleção padrão da aba "Hotels"    | ✅ Passou               | Aba "Hotels" exibida por padrão                     |
| CT-002 | RF-01.2   | Realizar busca de hotel com dados válidos (Happy Path)                   | ✅ Passou               | Resultados exibidos corretamente                    |
| CT-003 | RF-01.3   | Verificar campo “Search by city or hotel name” com auto-complete         | ✅ Passou               | Auto-complete funcionando corretamente              |
| CT-004 | RF-01.3   | Tentar buscar hotel sem preencher o campo “Search by city or hotel name” | ⚠️ Travado             | O campo não permite vazio e mantém nome padrão      |
| CT-005 | RF-01.3   | Tentar buscar hotel com Check-out anterior ao Check-in                   | ✅ Passou               | Sistema exibe validação correta                     |
| CT-006 | RF-01.4   | Realizar busca de voo (Round Trip) com dados válidos                     | ❌ Falhou               | Loop infinito de busca, sem resultados              |
| CT-007 | RF-01.4   | Realizar busca de voo (One Way) com partição de equivalência             | ❌ Falhou               | Busca não retorna resultados válidos                |
| CT-008 | RF-01.4   | Verificar validação de data de retorno anterior à partida                | ❌ Falhou               | Validação de data ineficaz                          |
| CT-009 | RF-01.5   | Realizar busca de tour com dados válidos                                 | ⚠️ Passou parcialmente | Erro ao buscar por locais específicos (ex: “Jedda”) |
| CT-010 | RF-01.6   | Realizar busca de carro com dados válidos                                | ⚠️ Passou parcialmente | Mesmo erro de busca em “Jedda”                      |
| CT-011 | RF-01.7   | Realizar busca de visto com dados válidos                                | ✅ Passou               | Busca executada corretamente                        |

---

## 🔍 Técnicas Aplicadas

### 🔸 Análise de Valor Limite

| Regra       | Valor Testado                       | Resultado Esperado                            | Resultado Obtido                                    |
| ----------- | ----------------------------------- | --------------------------------------------- | --------------------------------------------------- |
| RN-BUSCA-05 | 0 adultos                           | Exibir mensagem “At least one adult required” | ❌ Falhou – Busca foi executada                      |
| RN-BUSCA-08 | Botão de busca com campos inválidos | Botão desabilitado                            | ⚠️ Passou parcialmente – Botão permanece habilitado |

### 🔸 Partição de Equivalência

| Requisito | Resultado                                                |
| --------- | -------------------------------------------------------- |
| RF-01     | ❌ Falhou – Sistema permite busca sem definir passageiros |

---

## 📈 Conclusão

O **Módulo de Busca** do PHP Travels apresenta **boa funcionalidade nas abas “Hotels” e “Visa”**, mas há **falhas críticas** no fluxo de voos e na validação de campos obrigatórios.
Os **principais riscos** estão relacionados à **ausência de validação**, **tratamento de dados inconsistentes** e **problemas de integração na busca de voos**.

A correção dessas falhas é essencial para garantir a confiabilidade e a experiência do usuário no sistema.
