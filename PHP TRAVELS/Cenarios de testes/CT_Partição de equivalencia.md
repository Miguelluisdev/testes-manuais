# 🧩 Tabelas de Partição de Equivalência – PHPTRAVELS.NET

## 🔹 RF-01: Módulo de Busca Principal (Página Inicial)

### 🏨 Aba Hotels

| Campo        | Classe                            | Tipo     | Valor Exemplo | Resultado Esperado                                     |
| ------------ | --------------------------------- | -------- | ------------- | ------------------------------------------------------ |
| Cidade/Hotel | C1: Vazio                         | Inválido | ""            | Mostrar alerta “Campo obrigatório”                     |
| Cidade/Hotel | C2: Nome válido                   | Válido   | “Paris”       | Exibir resultados correspondentes                      |
| Check-in     | C1: Antes da data atual           | Inválido | Ontem         | Exibir erro “Data inválida”                            |
| Check-in     | C2: Hoje ou posterior             | Válido   | Amanhã        | Aceitar data                                           |
| Check-out    | C1: Igual ou anterior ao Check-in | Inválido | Mesmo dia     | Exibir erro “Check-out deve ser posterior ao check-in” |
| Check-out    | C2: Posterior ao Check-in         | Válido   | +2 dias       | Aceitar busca                                          |
| Adultos      | C1: 0                             | Inválido | 0             | Erro “Mínimo 1 adulto”                                 |
| Adultos      | C2: 1–10                          | Válido   | 3             | Permitir busca                                         |
| Adultos      | C3: >10                           | Inválido | 15            | Exibir erro “Máximo 10 adultos”                        |

---

### ✈️ Aba Flights

| Campo          | Classe                          | Tipo     | Valor Exemplo   | Resultado Esperado                                  |
| -------------- | ------------------------------- | -------- | --------------- | --------------------------------------------------- |
| Flying From    | C1: Vazio                       | Inválido | ""              | Mostrar alerta “Campo obrigatório”                  |
| Flying From    | C2: Aeroporto válido            | Válido   | “GRU”           | Buscar voos a partir de GRU                         |
| To Destination | C1: Igual ao campo origem       | Inválido | “GRU”           | Exibir erro “Origem e destino devem ser diferentes” |
| To Destination | C2: Diferente da origem         | Válido   | “CDG”           | Permitir busca                                      |
| Departure Date | C1: Antes de hoje               | Inválido | Ontem           | Bloquear data                                       |
| Departure Date | C2: Hoje ou depois              | Válido   | Amanhã          | Aceitar                                             |
| Return Date    | C1: Habilitado com “Round Trip” | Válido   | +3 dias         | Aceitar                                             |
| Return Date    | C2: Desabilitado com “One Way”  | Válido   | Campo bloqueado | Não aceitar input                                   |
| Passageiros    | C1: 0                           | Inválido | 0               | Exibir erro                                         |
| Passageiros    | C2: 1–9                         | Válido   | 2               | Aceitar                                             |
| Passageiros    | C3: >9                          | Inválido | 15              | Exibir erro “Limite de 9 passageiros”               |

---

### 🚗 Aba Cars

| Campo             | Classe               | Tipo     | Valor Exemplo | Resultado Esperado  |
| ----------------- | -------------------- | -------- | ------------- | ------------------- |
| Pick-up Location  | C1: Vazio            | Inválido | ""            | Exibir alerta       |
| Pick-up Location  | C2: Local válido     | Válido   | “Lisboa”      | Aceitar busca       |
| Drop-off Location | C1: Igual ao Pick-up | Válido   | “Lisboa”      | Aceitar (permitido) |
| Drop-off Location | C2: Vazio            | Inválido | ""            | Bloquear busca      |
| Pick-up Date      | C1: Antes de hoje    | Inválido | Ontem         | Rejeitar            |
| Pick-up Date      | C2: Hoje ou futuro   | Válido   | Amanhã        | Aceitar             |
| Drop-off Date     | C1: Antes do Pick-up | Inválido | Ontem         | Exibir erro         |
| Drop-off Date     | C2: Após Pick-up     | Válido   | +2 dias       | Aceitar             |

---

### 🎫 Aba Visa

| Campo        | Classe             | Tipo     | Valor Exemplo | Resultado Esperado                        |
| ------------ | ------------------ | -------- | ------------- | ----------------------------------------- |
| From Country | C1: Vazio          | Inválido | ""            | Exibir alerta                             |
| From Country | C2: País válido    | Válido   | “Brasil”      | Aceitar                                   |
| To Country   | C1: Igual ao From  | Inválido | “Brasil”      | Exibir erro “Países devem ser diferentes” |
| To Country   | C2: Diferente      | Válido   | “EUA”         | Aceitar                                   |
| Date         | C1: Antes de hoje  | Inválido | Ontem         | Exibir erro                               |
| Date         | C2: Hoje ou futuro | Válido   | Amanhã        | Aceitar                                   |

---

## 🔹 RF-02: Autenticação e Conta

| Campo                  | Classe                 | Tipo     | Valor Exemplo                                       | Resultado Esperado                |
| ---------------------- | ---------------------- | -------- | --------------------------------------------------- | --------------------------------- |
| E-mail                 | C1: Vazio              | Inválido | ""                                                  | Mostrar erro “Campo obrigatório”  |
| E-mail                 | C2: Formato inválido   | Inválido | “user@”                                             | Exibir erro “E-mail inválido”     |
| E-mail                 | C3: Formato válido     | Válido   | “[user@test.com](mailto:user@test.com)”             | Aceitar login                     |
| Senha                  | C1: Vazia              | Inválido | ""                                                  | Mostrar erro “Campo obrigatório”  |
| Senha                  | C2: < 6 caracteres     | Inválido | “123”                                               | Exibir erro “Mínimo 6 caracteres” |
| Senha                  | C3: ≥ 6 caracteres     | Válido   | “123456”                                            | Aceitar login                     |
| Checkbox “Remember Me” | C1: Marcado            | Válido   | ✔️                                                  | Sessão mantida                    |
| Checkbox “Remember Me” | C2: Desmarcado         | Válido   | ❌                                                   | Sessão expira no logout           |
| Forgot Password        | C1: E-mail inexistente | Inválido | “[naoexiste@teste.com](mailto:naoexiste@teste.com)” | Exibir erro                       |
| Forgot Password        | C2: E-mail cadastrado  | Válido   | “[user@teste.com](mailto:user@teste.com)”           | Enviar link de redefinição        |

---

## 🔹 RF-03: Resultados de Busca

| Campo     | Classe                                       | Tipo     | Valor Exemplo | Resultado Esperado        |
| --------- | -------------------------------------------- | -------- | ------------- | ------------------------- |
| Resultado | C1: Nenhum item encontrado                   | Inválido | “Zyxwq”       | Exibir “No results found” |
| Resultado | C2: Itens encontrados                        | Válido   | “Paris”       | Exibir lista              |
| Filtros   | C1: Valores incoerentes (ex: preço negativo) | Inválido | -100          | Ignorar filtro            |
| Filtros   | C2: Valores válidos                          | Válido   | 100–500       | Aplicar filtro            |
| Ordenação | C1: Critério inexistente                     | Inválido | “Cor”         | Ignorar                   |
| Ordenação | C2: Critério válido                          | Válido   | “Preço”       | Reordenar lista           |

---

## 🔹 RF-04: Página de Detalhes

| Campo            | Classe                    | Tipo     | Valor Exemplo | Resultado Esperado           |
| ---------------- | ------------------------- | -------- | ------------- | ---------------------------- |
| Item selecionado | C1: ID inexistente        | Inválido | ID 000        | Exibir erro 404              |
| Item selecionado | C2: ID válido             | Válido   | ID 123        | Exibir detalhes completos    |
| Disponibilidade  | C1: Datas fora do período | Inválido | Ontem–Hoje    | Exibir “Sem disponibilidade” |
| Disponibilidade  | C2: Datas válidas         | Válido   | +2 dias       | Exibir opções                |

---

## 🔹 RF-05: Reserva e Pagamento

| Campo              | Classe                 | Tipo     | Valor Exemplo                                   | Resultado Esperado   |
| ------------------ | ---------------------- | -------- | ----------------------------------------------- | -------------------- |
| Nome               | C1: Vazio              | Inválido | ""                                              | Exibir alerta        |
| Nome               | C2: Válido             | Válido   | “João Silva”                                    | Aceitar              |
| Pagamento          | C1: Sem aceitar termos | Inválido | ❌                                               | Bloquear confirmação |
| Pagamento          | C2: Aceitou termos     | Válido   | ✔️                                              | Confirmar reserva    |
| Valor Depósito     | C1: < $50              | Inválido | $30                                             | Exibir erro          |
| Valor Depósito     | C2: ≥ $50              | Válido   | $80                                             | Confirmar pagamento  |
| E-mail Confirmação | C1: Inválido           | Inválido | “abc@”                                          | Exibir erro          |
| E-mail Confirmação | C2: Válido             | Válido   | “[cliente@teste.com](mailto:cliente@teste.com)” | Enviar confirmação   |

---

## 🔹 RF-06: Funcionalidades Globais

| Campo              | Classe                 | Tipo     | Valor Exemplo | Resultado Esperado   |
| ------------------ | ---------------------- | -------- | ------------- | -------------------- |
| Idioma             | C1: Código inexistente | Inválido | “xx”          | Ignorar troca        |
| Idioma             | C2: Código válido      | Válido   | “en”, “pt”    | Traduzir interface   |
| Moeda              | C1: Símbolo inválido   | Inválido | “¤”           | Ignorar troca        |
| Moeda              | C2: Moeda suportada    | Válido   | “USD”, “EUR”  | Converter valores    |
| Link Header/Footer | C1: Link quebrado      | Inválido | 404           | Exibir erro          |
| Link Header/Footer | C2: Link ativo         | Válido   | “About Us”    | Abrir página correta |
