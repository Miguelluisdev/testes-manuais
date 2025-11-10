# 🧩 **Tabelas de Decisão – PHPTRAVELS.NET**

---

## 🔹 **RF-01 – Módulo de Busca Principal (Página Inicial)**

| Condição                               | Regra 1                     | Regra 2                           | Regra 3                                | Regra 4                    | Regra 5                                    |
| -------------------------------------- | --------------------------- | --------------------------------- | -------------------------------------- | -------------------------- | ------------------------------------------ |
| Tipo de aba selecionada                | Hotels                      | Flights                           | Tours                                  | Cars                       | Visa                                       |
| Campos obrigatórios preenchidos        | V                           | V                                 | F                                      | F                          | F                                          |
| Datas válidas (não anteriores à atual) | V                           | F                                 | V                                      | F                          | V                                          |
| Local origem/destino diferentes        | V                           | F                                 | V                                      | V                          | V                                          |
| **Ação esperada**                      | Busca executada com sucesso | Mensagem de erro de data inválida | Mensagem de erro “Campos obrigatórios” | Bloqueio do botão “Search” | Mensagem de erro “Origem e destino iguais” |

---

## 🔹 **RF-02 – Módulo de Autenticação e Conta**

| Condição                        | Regra 1            | Regra 2                | Regra 3               | Regra 4                     | Regra 5                              |
| ------------------------------- | ------------------ | ---------------------- | --------------------- | --------------------------- | ------------------------------------ |
| E-mail válido                   | V                  | V                      | F                     | V                           | F                                    |
| Senha correta                   | V                  | F                      | F                     | F                           | V                                    |
| Confirmação de senha (cadastro) | V                  | V                      | -                     | F                           | -                                    |
| **Ação esperada**               | Login bem-sucedido | Erro “senha incorreta” | Erro “email inválido” | Erro “senhas não coincidem” | Cadastro bloqueado (email duplicado) |

---

## 🔹 **RF-03 – Resultados de Busca**

| Condição                       | Regra 1                     | Regra 2                     | Regra 3           | Regra 4                                     | Regra 5                         |
| ------------------------------ | --------------------------- | --------------------------- | ----------------- | ------------------------------------------- | ------------------------------- |
| Resultados disponíveis         | V                           | F                           | V                 | V                                           | F                               |
| Filtros aplicados corretamente | V                           | -                           | F                 | V                                           | -                               |
| Ordenação funcional            | V                           | V                           | V                 | F                                           | -                               |
| **Ação esperada**              | Lista de resultados exibida | Mensagem “No results found” | Filtros ignorados | Ordenação incorreta exibida (bug potencial) | Página vazia com feedback claro |

---

## 🔹 **RF-04 – Página de Detalhes do Item**

| Condição                      | Regra 1                                | Regra 2                              | Regra 3                      | Regra 4                       |
| ----------------------------- | -------------------------------------- | ------------------------------------ | ---------------------------- | ----------------------------- |
| Item selecionado na lista     | V                                      | F                                    | V                            | V                             |
| Dados carregados corretamente | V                                      | V                                    | F                            | F                             |
| Botão “Book Now” ativo        | V                                      | V                                    | V                            | F                             |
| **Ação esperada**             | Exibe detalhes completos + botão ativo | Redirecionamento inválido (sem item) | Erro de carregamento parcial | Botão “Book Now” desabilitado |

---

## 🔹 **RF-05 – Reserva e Pagamento (Checkout)**

| Condição                        | Regra 1                            | Regra 2                            | Regra 3                       | Regra 4                     | Regra 5                                 | Regra 6                     |
| ------------------------------- | ---------------------------------- | ---------------------------------- | ----------------------------- | --------------------------- | --------------------------------------- | --------------------------- |
| Usuário autenticado             | V                                  | F                                  | V                             | F                           | V                                       | V                           |
| Campos obrigatórios preenchidos | V                                  | V                                  | F                             | V                           | F                                       | V                           |
| Termos aceitos                  | V                                  | V                                  | V                             | F                           | V                                       | F                           |
| Método de pagamento válido      | V                                  | V                                  | F                             | V                           | V                                       | V                           |
| **Ação esperada**               | Reserva confirmada e fatura gerada | Solicita login antes de prosseguir | Bloqueia botão de confirmação | Alerta “Termos não aceitos” | Mensagem “Campos obrigatórios faltando” | Falha no pagamento simulado |

---

## 🔹 **RF-06 – Funcionalidades Globais**

| Condição                    | Regra 1                                   | Regra 2                   | Regra 3             | Regra 4                    | Regra 5                                |
| --------------------------- | ----------------------------------------- | ------------------------- | ------------------- | -------------------------- | -------------------------------------- |
| Idioma alterado com sucesso | V                                         | F                         | V                   | V                          | F                                      |
| Moeda alterada corretamente | V                                         | V                         | F                   | V                          | F                                      |
| Sessão mantida após troca   | V                                         | V                         | V                   | F                          | V                                      |
| **Ação esperada**           | Interface traduzida e preços recalculados | Falha na tradução parcial | Conversão incorreta | Sessão expirada após troca | Exibição inconsistente de idioma/moeda |

---

## 🔹 **RFN – Requisitos Não Funcionais (Usabilidade, Segurança, Desempenho)**

| Condição                   | Regra 1                       | Regra 2                         | Regra 3                   | Regra 4                    | Regra 5                         |
| -------------------------- | ----------------------------- | ------------------------------- | ------------------------- | -------------------------- | ------------------------------- |
| HTTPS ativo                | V                             | F                               | V                         | F                          | F                               |
| Feedback visual nos botões | V                             | V                               | F                         | F                          | -                               |
| Tempo de carregamento < 5s | V                             | F                               | F                         | V                          | F                               |
| **Ação esperada**          | Sessão segura + UI responsiva | Alerta de segurança (sem HTTPS) | Sem feedback visual (bug) | Carregamento dentro do SLA | Página lenta (possível gargalo) |

---

## 🔒 **LGPD – Testes de Privacidade e Proteção de Dados**

| Condição                                | Regra 1                               | Regra 2                            | Regra 3                                | Regra 4                            | Regra 5                                           |
| --------------------------------------- | ------------------------------------- | ---------------------------------- | -------------------------------------- | ---------------------------------- | ------------------------------------------------- |
| Consentimento do usuário ativo          | V                                     | F                                  | F                                      | V                                  | F                                                 |
| Solicitação de exclusão de conta aceita | V                                     | V                                  | F                                      | F                                  | V                                                 |
| Dados pessoais mascarados               | V                                     | V                                  | F                                      | V                                  | F                                                 |
| Armazenamento de cookies autorizado     | V                                     | F                                  | F                                      | V                                  | F                                                 |
| **Ação esperada**                       | Dados tratados conforme consentimento | Bloqueio de coleta sem autorização | Dados sensíveis visíveis (falha grave) | Solicitação de exclusão confirmada | Cookies armazenados sem permissão (violação LGPD) |

---

## 🧠 **Como usar as Tabelas de Decisão**

Cada **coluna representa um cenário de teste** que pode ser transformado em **caso de teste manual**, por exemplo:

> **Cenário:** Realizar reserva com usuário logado, todos os campos válidos e termos aceitos.
> **Base:** RF-05 – Regra 1
> **Resultado esperado:** Reserva confirmada e status “Pending” visível no Dashboard.
