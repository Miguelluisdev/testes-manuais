# 🧪 Análise de Valor de Limite – Regras de Negócio (PHPTRAVELS.NET)

Este documento apresenta uma análise detalhada de **valores de limite** aplicada às **Regras de Negócio (RN)** do sistema de demonstração [PHPTRAVELS.NET](https://phptravels.net/).  
O objetivo é identificar os **limites mínimos, máximos e inválidos** que devem ser validados em testes manuais para garantir a confiabilidade da aplicação.

---

## 📊 Tabela de Análise de Valor de Limite

| **ID RN** | **Regra de Negócio** | **Campo / Variável** | **Valor Mínimo Aceitável** | **Valor Máximo Aceitável** | **Valor Abaixo do Limite (Inválido)** | **Valor Acima do Limite (Inválido)** | **Comportamento Esperado (Validação)** |
|------------|----------------------|------------------------|-----------------------------|-----------------------------|----------------------------------------|----------------------------------------|----------------------------------------|
| **RN-BUSCA-01** | Lógica de Datas (geral) | Data de início (Check-in, Pick up, Departure) | **Data atual (hoje)** | — | Data **anterior ao dia atual** | — | O sistema deve bloquear seleção de datas passadas. |
| **RN-BUSCA-02** | Datas em Hotéis | Diferença entre Check-in e Check-out | **1 dia após Check-in** | — | Check-out **igual ou anterior** ao Check-in | — | Exibir mensagem de erro ou impedir pesquisa. |
| **RN-BUSCA-03** | Datas em Voos | Retorno vs. Partida (Round Trip) | **Retorno ≥ partida** | — | Retorno **antes** da partida | — | Bloquear campo ou exibir erro “Invalid return date”. |
| **RN-BUSCA-04** | Aluguel de Carros | Drop-off vs. Pick-up | **Drop-off > Pick-up** | — | Drop-off **antes** do Pick-up | — | Impedir pesquisa até corrigir as datas. |
| **RN-BUSCA-05** | Ocupantes mínimos | Número de adultos | **1 adulto** | — | 0 adultos (somente crianças) | — | Exibir mensagem “At least one adult required”. |
| **RN-BUSCA-06** | Localização (Voos) | Origem vs. Destino | Origem ≠ Destino | — | Origem = Destino | — | Mostrar erro “Origin and destination cannot be the same”. |
| **RN-BUSCA-07** | Localização (Vistos) | From Country vs. To Country | Países diferentes | — | Países iguais | — | Impedir submissão e exibir mensagem de erro. |
| **RN-BUSCA-08** | Campos obrigatórios | Todos os campos essenciais | Todos preenchidos | — | 1 ou mais campos vazios | — | Botão “Search” deve ficar desabilitado. |
| **RN-CONTA-01** | Unicidade de e-mail | Campo E-mail | E-mail único | — | E-mail já cadastrado | — | Exibir erro “Email already exists”. |
| **RN-CONTA-02** | Validação de senha | Password vs. Confirm Password | Iguais | — | Diferentes | — | Bloquear envio e exibir alerta “Passwords do not match”. |
| **RN-CONTA-03** | Política de senha | Tamanho da senha | **6 caracteres** | (sem limite definido) | 5 caracteres ou menos | — | Mostrar mensagem “Password must be at least 6 characters”. |
| **RN-CONTA-05** | Persistência de dados | Dados do perfil | Salvar e refletir em novas reservas | — | Não salvar alterações | — | Garantir persistência na base de dados. |
| **RN-RESERVA-01** | Cálculo de preço (Hotéis) | Nº de noites e valores | **1 noite** | — | 0 noites | — | Impedir reserva sem diárias válidas. |
| **RN-RESERVA-01** | Cálculo de preço | Taxas e impostos | 0% (mínimo) | 100% (limite máximo aceitável) | Negativos | >100% | Impedir valores fora do intervalo. |
| **RN-RESERVA-02** | Disponibilidade | Quartos / Itens disponíveis | ≥1 | — | 0 disponíveis | — | Bloquear reserva e exibir “No rooms available”. |
| **RN-RESERVA-03** | Dados obrigatórios do hóspede | Nome, Sobrenome, E-mail, Telefone | Todos preenchidos | — | Um campo vazio | — | Impedir continuação da reserva. |
| **RN-RESERVA-04** | Concordância obrigatória | Checkbox “I agree with Terms” | Marcado | — | Desmarcado | — | Botão “Confirm Booking” desativado até marcar. |
| **RN-RESERVA-05** | Status inicial da reserva | Status | “Pending” | — | Outro status inicial | — | Exibir “Pending” após criação. |
| **RN-RESERVA-06** | Geração de fatura | Campos da fatura | Todos obrigatórios preenchidos | — | Campo faltante (ex: valor, data) | — | Exibir erro ou impedir geração. |
| **RN-GL-01** | Moeda | Conversão de valores | USD padrão | — | Moeda inválida | — | Exibir erro ou ignorar alteração. |
| **RN-GL-02** | Idioma | Idioma selecionado | Inglês, Espanhol, Árabe, etc. | — | Idioma não suportado | — | Reverter ao idioma padrão. |
| **RN-GL-03** | Menu de conta | Estado de login | Usuário autenticado / não autenticado | — | Estado inconsistente | — | Exibir corretamente as opções do menu. |

---

## 🧩 Casos de Limite Adicionais (Complementares)

| **Área** | **Campo / Regra** | **Valor de Limite Inferior** | **Valor de Limite Superior** | **Valor Inválido Inferior** | **Valor Inválido Superior** | **Resultado Esperado** |
|-----------|-------------------|-------------------------------|-------------------------------|------------------------------|------------------------------|-------------------------|
| **Cadastro de Usuário** | Comprimento do nome | 1 caractere (ex: “A”) | 50 caracteres | 0 caracteres (vazio) | 51+ caracteres | Deve aceitar entre 1 e 50 caracteres; truncar ou exibir erro acima disso. |
| **Cadastro de Usuário** | Telefone | 8 dígitos | 15 dígitos | 7 dígitos | 16 dígitos | Mensagem de erro ou bloqueio na validação. |
| **Busca de Hotéis** | Número de quartos | 1 | 5 | 0 | 6+ | Não permitir 0 ou mais que 5 quartos por reserva. |
| **Busca de Voos** | Passageiros (Adultos + Crianças) | 1 | 9 | 0 | 10+ | Mensagem “Maximum 9 passengers allowed”. |
| **Busca de Vistos** | Número de países disponíveis | ≥2 diferentes | — | 1 (mesmo país) | — | Exibir erro de seleção. |
| **Reserva (Hotéis)** | Valor total da reserva | ≥ 1 USD | 10.000 USD (limite estimado) | 0 ou negativo | >10.000 | Bloquear valores negativos ou excessivos. |
| **Pagamento Simulado** | Métodos disponíveis | 2 métodos visíveis | — | Nenhum método | — | Exibir alerta “No payment methods available”. |
| **Idioma e Moeda** | Persistência de sessão | Configuração mantida durante sessão | — | Perda da configuração | — | Deve persistir até logout ou limpeza de cookies. |
| **Login** | Tentativas incorretas | 1-4 tentativas | — | 5+ tentativas consecutivas | — | Exibir mensagem de bloqueio ou captcha. |
| **Campos de Texto (Formulários)** | Comprimento máximo permitido | — | 255 caracteres (texto comum) | 0 | 256+ | Exibir erro ou impedir envio. |
| **Reserva Simultânea** | Múltiplas sessões tentando o mesmo quarto | 1 reserva aceita | — | 2+ reservas simultâneas | — | Segunda tentativa deve falhar com erro de disponibilidade. |

---

## 🧠 Observações Técnicas

- **Datas e numéricos** → usar testes com “valor do dia”, “um dia antes” e “um dia depois”.  
- **Textos e senhas** → validar mínimo e máximo de caracteres.  
- **Combinações lógicas** → (ex: origem = destino, checkbox não marcado).  
- **Sessões simultâneas** → testar consistência e concorrência de reservas.  

---
