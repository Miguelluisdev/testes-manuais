# 🐞 Relatório de Bugs e Melhorias – Módulo de Busca (PHP Travels)

## 📘 Informações Gerais

* **Sistema:** PHP Travels (Demo)
* **Módulo:** Módulo de Busca
* **Responsável pelos testes:** Miguel Luis
* **Data:** 09/11/2025
* **Tipo de teste:** Funcional / Validação de regras e fluxos
* **Técnicas aplicadas:** Partição de Equivalência, Análise de Valor Limite , tabela de deci~sao
* **Referência:** Casos de Teste CT-001 a CT-011

---

## 🧩 Bugs Identificados

### 🐛 BUG-01 – Exibição incorreta em “Infants -2 Years”

| Campo                                                                                                                                              | Detalhe                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Descrição**                                                                                                                                      | Ao selecionar “Infants -2 Years”, o campo exibe valores como “NaN” e “Injection”, indicando falha de conversão e risco de vulnerabilidade. |
| **Requisito Relacionado**                                                                                                                          | RF-01 (Travellers - Campo de Idade)                                                                                                        |
| **Severidade**                                                                                                                                     | Alta                                                                                                                                       |
| **Prioridade**                                                                                                                                     | Alta                                                                                                                                       |
| **Status**                                                                                                                                         | Aberto                                                                                                                                     |
| **Ambiente**                                                                                                                                       | Google Chrome (Windows 10)                                                                                                                 |
| **Passos para Reproduzir**                                                                                                                         |                                                                                                                                            |
| 1. Acesse o site PHP Travels. <br> 2. Vá até a aba “Hotels” ou “Flights”. <br> 3. Clique em “Travellers”. <br> 4. Adicione um “Infant (-2 Years)”. |                                                                                                                                            |
| **Comportamento Esperado**                                                                                                                         | Exibir a quantidade de bebês de forma numérica correta, sem valores inválidos.                                                             |
| **Comportamento Obtido**                                                                                                                           | Exibe “NaN” e “Injection” no campo, indicando falha de conversão e possível vulnerabilidade.                                               |
| **Causa Raiz (RCA)**                                                                                                                               | Falta de sanitização e validação de entrada de dados no campo “Infants”.                                                                   |
| **Solução Recomendada**                                                                                                                            | Implementar validação de tipo e formato no front-end e back-end para impedir valores não numéricos.                                        |

---

### 🐛 BUG-02 – Busca de voo não finaliza (loop infinito)

| Campo                                                                                                                                                                     | Detalhe                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Descrição**                                                                                                                                                             | Ao realizar busca de voo (Round Trip), o sistema entra em loop de carregamento infinito sem retornar resultados. |
| **Requisito Relacionado**                                                                                                                                                 | RF-01.4 (Flights)                                                                                                |
| **Severidade**                                                                                                                                                            | Alta                                                                                                             |
| **Prioridade**                                                                                                                                                            | Alta                                                                                                             |
| **Status**                                                                                                                                                                | Aberto                                                                                                           |
| **Ambiente**                                                                                                                                                              | Google Chrome (Windows 10)                                                                                       |
| **Passos para Reproduzir**                                                                                                                                                |                                                                                                                  |
| 1. Acesse o site PHP Travels. <br> 2. Vá até a aba “Flights”. <br> 3. Selecione “Round Trip”. <br> 4. Insira origem, destino e datas válidas. <br> 5. Clique em “Search”. |                                                                                                                  |
| **Comportamento Esperado**                                                                                                                                                | Exibir resultados de voos compatíveis com os parâmetros informados.                                              |
| **Comportamento Obtido**                                                                                                                                                  | O sistema permanece carregando indefinidamente, sem retorno de resultados.                                       |
| **Causa Raiz (RCA)**                                                                                                                                                      | Falha de integração com API externa de voos ou endpoint incorreto/inacessível.                                   |
| **Solução Recomendada**                                                                                                                                                   | Validar o endpoint e resposta da API antes da execução; implementar tratamento de timeout e mensagens amigáveis. |

---

### 🐛 BUG-03 – Busca sem passageiros

| Campo                                                                                                                       | Detalhe                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| **Descrição**                                                                                                               | O sistema permite realizar busca sem selecionar “Travellers”.                                   |
| **Requisito Relacionado**                                                                                                   | RF-01.3 (Validação de campos obrigatórios)                                                      |
| **Severidade**                                                                                                              | Alta                                                                                            |
| **Prioridade**                                                                                                              | Alta                                                                                            |
| **Status**                                                                                                                  | Aberto                                                                                          |
| **Ambiente**                                                                                                                | Google Chrome (Windows 10)                                                                      |
| **Passos para Reproduzir**                                                                                                  |                                                                                                 |
| 1. Acesse a página inicial. <br> 2. Escolha a aba “Hotels”. <br> 3. Não selecione “Travellers”. <br> 4. Clique em “Search”. |                                                                                                 |
| **Comportamento Esperado**                                                                                                  | Exibir mensagem “Selecione pelo menos 1 adulto”.                                                |
| **Comportamento Obtido**                                                                                                    | O sistema executa a busca mesmo sem passageiros definidos.                                      |
| **Causa Raiz (RCA)**                                                                                                        | Ausência de validação de campo obrigatório no front-end.                                        |
| **Solução Recomendada**                                                                                                     | Adicionar verificação no botão “Search” para impedir requisição com campos obrigatórios vazios. |

---

## 💡 Melhorias Identificadas

### 🔧 MELH-01 – Botão “Search” deve ser desabilitado com campos inválidos

| Campo                   | Detalhe                                                                        |
| ----------------------- | ------------------------------------------------------------------------------ |
| **Descrição**           | O botão “Search” continua habilitado mesmo com campos inválidos ou vazios.     |
| **Impacto**             | O usuário pode realizar buscas incorretas e gerar requisições desnecessárias.  |
| **Causa Raiz (RCA)**    | Lógica de validação incompleta no JavaScript responsável pelo estado do botão. |
| **Solução Recomendada** | Implementar desativação dinâmica com base nos campos obrigatórios preenchidos. |

---

### 🔧 MELH-02 – Notificações e mensagens de erro com design ruim

| Campo                   | Detalhe                                                                                                     |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Descrição**           | As mensagens de erro são visualmente confusas e mal posicionadas.                                           |
| **Impacto**             | Dificulta a compreensão do erro e prejudica a UX.                                                           |
| **Causa Raiz (RCA)**    | Falta de padronização de estilo e ausência de hierarquia visual nas notificações.                           |
| **Solução Recomendada** | Implementar notificações claras, padronizadas (ex: toast ou alert estilizado) e alinhadas ao design system. |

---

### 🔧 MELH-03 – Validação de “Travellers” mais amigável

| Campo                   | Detalhe                                                                                                     |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Descrição**           | Mensagens genéricas ou ausência de mensagens ao não selecionar viajantes.                                   |
| **Impacto**             | O usuário não entende o motivo da busca falhar.                                                             |
| **Causa Raiz (RCA)**    | Falta de mapeamento de mensagens específicas por tipo de erro de campo.                                     |
| **Solução Recomendada** | Exibir mensagens específicas (“Selecione pelo menos 1 adulto”) com feedback visual (ex: campo em vermelho). |

---

## 🧠 Resumo da Análise de Causa Raiz (RCA)

| Categoria                | Causa Identificada                                                           | Impacto                                                    |
| ------------------------ | ---------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **Validação de Entrada** | Falta de sanitização e checagem de dados nos campos “Travellers” e “Infants” | Risco de vulnerabilidade e resultados incorretos           |
| **Integração de API**    | Endpoint de voo falhando ou sem retorno                                      | Impede a busca completa no módulo “Flights”                |
| **Interface/UX**         | Botão ativo e mensagens confusas                                             | Gera erros de usabilidade e falhas de fluxo                |
| **Lógica de Negócio**    | Ausência de controle de pré-condições antes da execução da busca             | Permite ações inválidas e degrada a experiência do usuário |

---

## 🧾 Conclusão

O módulo de busca apresenta **três bugs críticos** e **três melhorias prioritárias** relacionados principalmente à **validação de dados e usabilidade**.
Os testes mostraram que, apesar do bom funcionamento nas abas *Hotels* e *Visa*, há falhas graves nos fluxos de *Flights* e *Travellers*, com impacto direto na confiabilidade e experiência do usuário.

A implementação das correções e melhorias propostas permitirá:

* Maior consistência nos resultados;
* Redução de erros de entrada e requisições inválidas;
* Melhor UX e clareza de mensagens;
* Alinhamento às boas práticas da ISO/IEC/IEEE 29119-3 (Documentação) e 29119-4 (Técnicas de Teste).
