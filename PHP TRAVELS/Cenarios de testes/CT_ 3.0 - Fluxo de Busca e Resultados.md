### **RF-03: Fluxo de Busca e Resultados**

#### **RF-03.1 e RF-03.2: Redirecionamento e Exibição de Resultados**

**CT-025: Redirecionamento para a página de resultados e exibição de itens (Hotels)**
*   **Módulo:** Fluxo de Busca e Resultados
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  No formulário da aba "Hotels" (padrão), preencher:
        *   "Search by city or hotel name": `Dubai` (e selecionar do auto-complete)
        *   "Check-in": Data futura
        *   "Check-out": Data futura (posterior ao check-in)
        *   "Travelers": 2 adultos
    3.  Clicar no botão "Search".
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para a página de resultados de hotéis (`/hotels/search/...`).
    *   A página deve exibir uma lista de resultados de hotéis, com cada item contendo: imagem, nome do hotel, preço e um link "Details" ou "Book Now".
    *   As informações de busca (cidade, datas, viajantes) devem ser refletidas na página de resultados.

**CT-026: Exibição de mensagem "No results found" para busca sem resultados (Hotels)**
*   **Módulo:** Fluxo de Busca e Resultados
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  No formulário da aba "Hotels", preencher:
        *   "Search by city or hotel name": `CidadeInexistenteXYZ` (ou um termo que se espera não ter resultados)
        *   "Check-in": Data futura
        *   "Check-out": Data futura (posterior ao check-in)
        *   "Travelers": 1 adulto
    3.  Clicar no botão "Search".
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para a página de resultados de hotéis.
    *   Uma mensagem clara como "No results found", "Nenhum resultado encontrado" ou similar deve ser exibida na área de resultados.
    *   Nenhum item de hotel deve ser exibido na lista.

---

#### **RF-03.3 – Filtros (para Hotéis)**

**CT-027: Aplicar filtro "Star Grade" na página de resultados de hotéis**
*   **Módulo:** Fluxo de Busca e Resultados (Filtros)
*   **Pré-condições:** Estar na página de resultados de hotéis com resultados exibidos (realizar CT-025 primeiro).
*   **Passos:**
    1.  Na página de resultados de hotéis, localizar a seção de filtros.
    2.  Na categoria "Star Grade", selecionar um ou mais checkboxes (ex: "5 Star").
*   **Resultados Esperados:**
    *   A lista de hotéis deve ser atualizada dinamicamente (sem recarregar a página).
    *   Apenas os hotéis que correspondem ao filtro de "5 Star" devem ser exibidos.

**CT-028: Aplicar filtro "Price Range" na página de resultados de hotéis**
*   **Módulo:** Fluxo de Busca e Resultados (Filtros)
*   **Pré-condições:** Estar na página de resultados de hotéis com resultados exibidos.
*   **Passos:**
    1.  Na página de resultados de hotéis, localizar a seção de filtros.
    2.  Na categoria "Price Range", ajustar o slider ou inserir valores para definir uma faixa de preço (ex: "$100 - $300").
*   **Resultados Esperados:**
    *   A lista de hotéis deve ser atualizada dinamicamente.
    *   Apenas os hotéis cujos preços se encaixam na faixa selecionada devem ser exibidos.

**CT-029: Aplicar múltiplos filtros simultaneamente (Star Grade + Amenities)**
*   **Módulo:** Fluxo de Busca e Resultados (Filtros)
*   **Pré-condições:** Estar na página de resultados de hotéis com resultados exibidos.
*   **Passos:**
    1.  Na página de resultados de hotéis, localizar a seção de filtros.
    2.  Na categoria "Star Grade", selecionar "4 Star".
    3.  Na categoria "Amenities", selecionar "WiFi".
*   **Resultados Esperados:**
    *   A lista de hotéis deve ser atualizada dinamicamente.
    *   Apenas os hotéis que são "4 Star" E possuem "WiFi" devem ser exibidos.

**CT-030: Remover filtros aplicados**
*   **Módulo:** Fluxo de Busca e Resultados (Filtros)
*   **Pré-condições:** Estar na página de resultados de hotéis com filtros aplicados e resultados filtrados.
*   **Passos:**
    1.  Na página de resultados de hotéis, com filtros aplicados, localizar a opção para remover ou desmarcar os filtros.
    2.  Desmarcar um dos checkboxes de filtro (ex: "5 Star").
*   **Resultados Esperados:**
    *   A lista de hotéis deve ser atualizada dinamicamente.
    *   Os hotéis que foram anteriormente filtrados devem reaparecer, refletindo a remoção do filtro.
    *   Se todos os filtros forem removidos, a lista completa original deve ser exibida.

---

#### **RF-03.4 – Ordenação**

**CT-031: Ordenar resultados de hotéis por "Price (Low to High)"**
*   **Módulo:** Fluxo de Busca e Resultados (Ordenação)
*   **Pré-condições:** Estar na página de resultados de hotéis com múltiplos resultados.
*   **Passos:**
    1.  Na página de resultados de hotéis, localizar o dropdown ou botão de ordenação.
    2.  Selecionar a opção "Price (Low to High)" (ou similar, dependendo do texto no site).
*   **Resultados Esperados:**
    *   A lista de hotéis deve ser reordenada dinamicamente.
    *   O primeiro item na lista deve ser o hotel com o menor preço, e a ordem deve ser crescente de preço.

**CT-032: Ordenar resultados de hotéis por "Name (A-Z)"**
*   **Módulo:** Fluxo de Busca e Resultados (Ordenação)
*   **Pré-condições:** Estar na página de resultados de hotéis com múltiplos resultados.
*   **Passos:**
    1.  Na página de resultados de hotéis, localizar o dropdown ou botão de ordenação.
    2.  Selecionar a opção "Name (A-Z)" (ou similar).
*   **Resultados Esperados:**
    *   A lista de hotéis deve ser reordenada dinamicamente.
    *   O primeiro item na lista deve ser o hotel com o nome que começa com a letra mais próxima de 'A', e a ordem deve ser alfabética crescente.

---

#### **RF-03.5 – Visualização**

**CT-033: Alternar visualização dos resultados para "Grid View"**
*   **Módulo:** Fluxo de Busca e Resultados (Visualização)
*   **Pré-condições:** Estar na página de resultados de hotéis (provavelmente em "List View" por padrão).
*   **Passos:**
    1.  Na página de resultados de hotéis, localizar os ícones ou botões para alternar a visualização.
    2.  Clicar no ícone/botão de "Grid View" (visualização em grade).
*   **Resultados Esperados:**
    *   O layout dos resultados deve mudar para um formato de grade, onde os itens são dispostos em colunas.
    *   A informação de cada item (imagem, nome, preço) deve ser visível no novo layout.

**CT-034: Alternar visualização dos resultados de volta para "List View"**
*   **Módulo:** Fluxo de Busca e Resultados (Visualização)
*   **Pré-condições:** Estar na página de resultados de hotéis com a visualização em "Grid View".
*   **Passos:**
    1.  Na página de resultados de hotéis (em "Grid View"), localizar os ícones ou botões para alternar a visualização.
    2.  Clicar no ícone/botão de "List View" (visualização em lista).
*   **Resultados Esperados:**
    *   O layout dos resultados deve mudar para um formato de lista, onde os itens são dispostos verticalmente.
    *   A informação de cada item deve ser visível no novo layout.

---

#### **RF-03.7: Detalhes do Item na Lista de Resultados**

**CT-035: Verificar exibição de informações essenciais em cada item da lista (Hotels)**
*   **Módulo:** Fluxo de Busca e Resultados (Detalhes do Item)
*   **Pré-condições:** Estar na página de resultados de hotéis com resultados exibidos.
*   **Passos:**
    1.  Observar os elementos de um item individual na lista de resultados (ex: o primeiro hotel).
*   **Resultados Esperados:**
    *   Cada item de hotel deve exibir:
        *   Uma imagem representativa do hotel.
        *   O nome do hotel.
        *   O preço (por noite ou total, dependendo da apresentação).
        *   Um link ou botão "Details" ou "Book Now" que redirecione para a página de detalhes do hotel.
