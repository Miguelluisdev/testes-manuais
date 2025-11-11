### **RF-04: Página de Detalhes do Item**

#### **RF-04.1 e RF-04.2: Redirecionamento e Exibição Completa do Item**

**CT-036: Redirecionamento para a página de detalhes do hotel ao clicar em um item**
*   **Módulo:** Página de Detalhes do Item
*   **Pré-condições:** Estar na página de resultados de hotéis com resultados exibidos (realizar CT-025 primeiro).
*   **Passos:**
    1.  Na página de resultados de hotéis, clicar no link "Details" ou "Book Now" de um dos hotéis listados.
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para a página de detalhes do hotel selecionado (`/hotel/detail/...`).
    *   A URL deve conter o identificador único do hotel.

**CT-037: Exibição completa das informações do hotel na página de detalhes**
*   **Módulo:** Página de Detalhes do Item
*   **Pré-condições:** Estar na página de detalhes de um hotel (realizar CT-036 primeiro).
*   **Passos:**
    1.  Observar o conteúdo da página de detalhes do hotel.
*   **Resultados Esperados:**
    *   A página deve exibir o nome do hotel em destaque.
    *   Uma galeria de imagens/carrossel com fotos do hotel deve estar presente.
    *   Uma descrição detalhada do hotel deve ser visível.
    *   Uma lista de amenidades/facilidades do hotel (ex: WiFi, piscina, academia) deve ser exibida.
    *   Um mapa mostrando a localização do hotel deve estar integrado.
    *   Seções para avaliações de clientes devem ser visíveis.

---

#### **RF-04.3 – Preços e Disponibilidade**

**CT-038: Exibição de tipos de quartos e seus detalhes na página de detalhes do hotel**
*   **Módulo:** Página de Detalhes do Item (Preços e Disponibilidade)
*   **Pré-condições:** Estar na página de detalhes de um hotel.
*   **Passos:**
    1.  Observar a seção de seleção de quartos na página de detalhes.
*   **Resultados Esperados:**
    *   Diferentes tipos de quartos (ex: Standard, Deluxe, Suite) devem ser listados.
    *   Para cada tipo de quarto, deve ser exibido:
        *   Nome do quarto.
        *   Preço (por noite ou total para as datas selecionadas).
        *   Número de pessoas que o quarto acomoda.
        *   Informações adicionais como políticas de cancelamento ou o que está incluído.
    *   Um botão para "Book Now" ou "Add to Cart" deve estar disponível para cada tipo de quarto.

**CT-039: Verificar a funcionalidade do botão "Book Now" para um quarto específico**
*   **Módulo:** Página de Detalhes do Item (Preços e Disponibilidade)
*   **Pré-condições:** Estar na página de detalhes de um hotel.
*   **Passos:**
    1.  Na seção de tipos de quartos, selecionar um quarto específico.
    2.  Clicar no botão "Book Now" ou "Reserve" associado a esse quarto.
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para a página de checkout/reserva (`/hotels/booking/...`), com as informações do hotel e quarto pré-selecionadas.

**CT-040: Verificar a atualização de preço ao mudar a quantidade de quartos ou hóspedes (se aplicável)**
*   **Módulo:** Página de Detalhes do Item (Preços e Disponibilidade)
*   **Pré-condições:** Estar na página de detalhes de um hotel que permite seleção de quantidade de quartos/hóspedes.
*   **Passos:**
    1.  Na seção de seleção de quartos, alterar a quantidade de quartos ou o número de hóspedes para um tipo de quarto.
*   **Resultados Esperados:**
    *   O preço total exibido para o quarto (e possivelmente para a reserva completa) deve ser atualizado dinamicamente para refletir a nova seleção.
