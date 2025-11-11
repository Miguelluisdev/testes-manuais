# 🧭 RF-01 – Módulo de Busca Principal (Página Inicial)

## 🔹 RF-01.1 e RF-01.2 – Exibição e Seleção Padrão da Aba *Hotels*

### **CT-001 – Verificar exibição das abas de busca e seleção padrão da aba "Hotels"**

**Módulo:** Busca Principal (Home)
**Pré-condições:** N/A

**Passos:**

1. Acessar a URL: [https://phptravels.net/](https://phptravels.net/)

**Resultados Esperados:**

* As abas **"Hotels"**, **"Flights"**, **"Tours"**, **"Cars"**, **"Visa"** devem estar visíveis.
* A aba **"Hotels"** deve estar **selecionada/ativa por padrão**.
* O conteúdo do formulário da aba **"Hotels"** deve ser exibido.

---

## 🔹 RF-01.3 – Hotels

### **CT-002 – Realizar busca de hotel com dados válidos (Happy Path)**

**Módulo:** Busca Principal (Hotels)
**Pré-condições:** Aba "Hotels" selecionada.

**Passos:**

1. Acessar a URL: [https://phptravels.net/](https://phptravels.net/)
2. No campo **"Search by city or hotel name"**, digitar um nome de cidade ou hotel (ex: *Dubai*).
3. Selecionar uma opção do **auto-complete**.
4. Selecionar uma **data futura** no campo *Check-in*.
5. Selecionar uma **data posterior** no campo *Check-out*.
6. No campo *Travelers*, definir adultos = 2, crianças = 0.
7. Clicar em **"Search"**.

**Resultados Esperados:**

* O botão **"Search"** deve estar habilitado após preenchimento válido.
* O usuário deve ser redirecionado para `/hotels/search/...`.
* A página de resultados deve exibir **hotéis correspondentes** à busca.

---

### **CT-003 – Verificar campo "Search by city or hotel name" com auto-complete**

**Módulo:** Busca Principal (Hotels)
**Pré-condições:** Aba "Hotels" selecionada.

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. No campo *Search by city or hotel name*, digitar parcialmente (ex: *Lon*).

**Resultados Esperados:**

* Exibir lista de **sugestões (auto-complete)** com cidades/hotéis correspondentes (ex: *London*).
* Ao selecionar uma sugestão, o campo deve ser preenchido com o **valor completo**.

---

### **CT-004 – Tentar buscar hotel sem preencher o campo "Search by city or hotel name"**

**Módulo:** Busca Principal (Hotels)
**Pré-condições:** Aba "Hotels" selecionada.

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. Deixar o campo *Search by city or hotel name* vazio.
3. Selecionar datas de *Check-in* e *Check-out* válidas.
4. Definir número de *Travelers*.
5. Clicar em **"Search"**.

**Resultados Esperados:**

* O botão **"Search"** deve estar **desabilitado** ou exibir uma **mensagem de validação**.
* O redirecionamento **não deve ocorrer**.

---

### **CT-005 – Tentar buscar hotel com Check-out anterior ao Check-in**

**Módulo:** Busca Principal (Hotels)
**Pré-condições:** Aba "Hotels" selecionada.

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. Preencher *Search by city or hotel name* com valor válido.
3. Selecionar *Check-in* = 20/12/2024 e *Check-out* = 19/12/2024.
4. Definir número de *Travelers*.
5. Clicar em **"Search"**.

**Resultados Esperados:**

* O botão **"Search"** deve estar **desabilitado** ou exibir mensagem de **validação de data**.
* O redirecionamento **não deve ocorrer**.

---

## 🔹 RF-01.4 – Flights

### **CT-006 – Realizar busca de voo (Round Trip) com dados válidos**

**Módulo:** Busca Principal (Flights)
**Pré-condições:** N/A

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. Clicar na aba **"Flights"**.
3. Garantir que **"Round Trip"** esteja selecionado.
4. Preencher **origem** (*Flying from* = Dubai) e **destino** (*To destination* = London).
5. Selecionar *Departure Date* e *Return Date* (retorno posterior).
6. Definir *Passengers* (Adultos = 1, Crianças/Bebês = 0).
7. Clicar em **"Search"**.

**Resultados Esperados:**

* O botão **"Search"** deve estar habilitado.
* Redirecionar para `/flights/search/...`.
* Exibir **voos de ida e volta** compatíveis.

---

### **CT-007 – Realizar busca de voo (One Way) com dados válidos**

**Módulo:** Busca Principal (Flights)
**Pré-condições:** N/A

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. Clicar em **"Flights"**.
3. Selecionar **"One Way"** em *Trip Type*.
4. Preencher **origem** e **destino** válidos.
5. Selecionar *Departure Date* futura.
6. Definir *Passengers*.
7. Clicar em **"Search"**.

**Resultados Esperados:**

* O campo **"Return Date"** deve estar **desabilitado ou oculto**.
* O botão **"Search"** deve estar habilitado.
* Redirecionar para resultados de **voos apenas de ida**.

---

### **CT-008 – Verificar validação de data de retorno anterior à de partida**

**Módulo:** Busca Principal (Flights)
**Pré-condições:** Aba "Flights" selecionada, "Round Trip" ativo.

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. Clicar na aba **"Flights"**.
3. Preencher **origem** e **destino** válidos.
4. Selecionar *Departure Date* = 20/12/2024 e *Return Date* = 19/12/2024.
5. Definir *Passengers*.
6. Clicar em **"Search"**.

**Resultados Esperados:**

* Exibir **mensagem de validação** informando erro de data.
* O redirecionamento **não deve ocorrer**.

---

## 🔹 RF-01.5 – Tours

### **CT-009 – Realizar busca de tour com dados válidos**

**Módulo:** Busca Principal (Tours)
**Pré-condições:** N/A

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. Clicar na aba **"Tours"**.
3. No campo *Search by tour name or city*, digitar e selecionar (ex: *Dubai*).
4. Selecionar data futura em *Date*.
5. Definir *Guests* = 1.
6. Clicar em **"Search"**.

**Resultados Esperados:**

* O botão **"Search"** deve estar habilitado.
* O usuário deve ser redirecionado para a **página de resultados de tours**.

---

## 🔹 RF-01.6 – Cars

### **CT-010 – Realizar busca de carro com dados válidos**

**Módulo:** Busca Principal (Cars)
**Pré-condições:** N/A

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. Clicar na aba **"Cars"**.
3. Preencher *Pick up location* e *Drop off location*.
4. Selecionar *Pick up date/time* futura.
5. Selecionar *Drop off date/time* posterior.
6. Clicar em **"Search"**.

**Resultados Esperados:**

* O botão **"Search"** deve estar habilitado.
* Redirecionar para **/cars/search/...** com resultados correspondentes.

---

## 🔹 RF-01.7 – Visa

### **CT-011 – Realizar busca de visto com dados válidos**

**Módulo:** Busca Principal (Visa)
**Pré-condições:** N/A

**Passos:**

1. Acessar [https://phptravels.net/](https://phptravels.net/)
2. Clicar na aba **"Visa"**.
3. No dropdown *From Country*, selecionar *United States*.
4. No dropdown *To Country*, selecionar *Brazil*.
5. Selecionar *Date* futura.
6. Clicar em **"Submit"**.

**Resultados Esperados:**

* O botão **"Submit"** deve estar habilitado.
* Redirecionar para **página de resultados ou informações sobre visto**.
