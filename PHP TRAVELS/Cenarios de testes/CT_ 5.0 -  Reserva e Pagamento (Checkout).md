### **RF-05: Reserva e Pagamento (Checkout)**

#### **RF-05.1, RF-05.2 e RF-05.3: Redirecionamento, Preenchimento de Dados e Resumo**

**CT-041: Redirecionamento para a página de checkout após selecionar um item para reservar**
*   **Módulo:** Reserva e Pagamento (Checkout)
*   **Pré-condições:** Estar na página de detalhes de um hotel e selecionar um quarto (realizar CT-036 e CT-039).
*   **Passos:**
    1.  Na página de detalhes de um hotel, selecionar um tipo de quarto e clicar em "Book Now".
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para a página de checkout (`/hotels/booking/...` ou similar).
    *   A página de checkout deve exibir o nome do hotel, o tipo de quarto e as datas de check-in/check-out.

**CT-042: Verificação do preenchimento automático de dados para usuário logado**
*   **Módulo:** Reserva e Pagamento (Checkout)
*   **Pré-condições:** Usuário logado antes de iniciar o processo de busca/reserva (realizar CT-012 e depois CT-025 e CT-039).
*   **Passos:**
    1.  Após clicar em "Book Now" como um usuário logado.
*   **Resultados Esperados:**
    *   Na página de checkout, os campos de dados pessoais (First Name, Last Name, Email, Phone) devem estar pré-preenchidos com as informações do usuário logado.
    *   O usuário não deve ser solicitado a fazer login novamente.

**CT-043: Preenchimento manual de dados para usuário não logado no checkout**
*   **Módulo:** Reserva e Pagamento (Checkout)
*   **Pré-condições:** Usuário **não** logado ao iniciar o processo de busca/reserva (realizar CT-025 e CT-039 sem login prévio).
*   **Passos:**
    1.  Após clicar em "Book Now" como um usuário não logado.
    2.  Na página de checkout, preencher manualmente os campos obrigatórios de dados pessoais (First Name, Last Name, Email, Phone).
*   **Resultados Esperados:**
    *   Os campos devem permitir o preenchimento de dados.
    *   Nenhuma mensagem de erro deve aparecer por não estar logado, desde que os dados sejam preenchidos.
    *   O processo de checkout deve poder continuar.

**CT-044: Exibição clara do resumo da reserva na página de checkout**
*   **Módulo:** Reserva e Pagamento (Checkout)
*   **Pré-condições:** Estar na página de checkout.
*   **Passos:**
    1.  Observar a seção de resumo da reserva na página de checkout.
*   **Resultados Esperados:**
    *   A página deve exibir um resumo detalhado da reserva, incluindo:
        *   Nome do hotel/item.
        *   Datas da reserva.
        *   Tipo de quarto/item.
        *   Número de hóspedes/passageiros.
        *   Preço unitário e total.
        *   Eventuais taxas ou impostos.
        *   O valor total final da reserva.

---

#### **RF-05.4 e RF-05.5: Pagamento e Termos**

**CT-045: Selecionar método de pagamento "Pay by Deposit" e aceitar termos**
*   **Módulo:** Reserva e Pagamento (Métodos de Pagamento)
*   **Pré-condições:** Estar na página de checkout com o resumo da reserva preenchido.
*   **Passos:**
    1.  Na seção de métodos de pagamento, selecionar a opção "Pay by Deposit" (ou similar).
    2.  Marcar o checkbox de aceite dos termos e condições ("I Agree with Terms and Conditions").
    3.  Clicar no botão para finalizar a reserva (ex: "Confirm Booking", "Complete Reservation").
*   **Resultados Esperados:**
    *   O botão de finalizar deve estar habilitado após a seleção do método e aceite dos termos.
    *   O usuário deve ser redirecionado para a página de confirmação da reserva.

**CT-046: Selecionar método de pagamento "Pay Later" e aceitar termos**
*   **Módulo:** Reserva e Pagamento (Métodos de Pagamento)
*   **Pré-condições:** Estar na página de checkout com o resumo da reserva preenchido.
*   **Passos:**
    1.  Na seção de métodos de pagamento, selecionar a opção "Pay Later" (ou similar).
    2.  Marcar o checkbox de aceite dos termos e condições.
    3.  Clicar no botão para finalizar a reserva.
*   **Resultados Esperados:**
    *   O botão de finalizar deve estar habilitado após a seleção do método e aceite dos termos.
    *   O usuário deve ser redirecionado para a página de confirmação da reserva.

**CT-047: Tentar finalizar reserva sem aceitar os termos e condições**
*   **Módulo:** Reserva e Pagamento (Termos e Condições)
*   **Pré-condições:** Estar na página de checkout, com dados e método de pagamento selecionados.
*   **Passos:**
    1.  Na seção de métodos de pagamento, selecionar um método.
    2.  **Não** marcar o checkbox de aceite dos termos e condições.
    3.  Tentar clicar no botão para finalizar a reserva.
*   **Resultados Esperados:**
    *   Uma mensagem de erro clara deve ser exibida, informando que é necessário aceitar os termos e condições.
    *   O processo de reserva **não** deve ser concluído.

---

#### **RF-05.6, RF-05.7, RF-05.8 e RF-05.9: Confirmação e Integração com Conta**

**CT-048: Exibição da página de confirmação de reserva com status e detalhes**
*   **Módulo:** Reserva e Pagamento (Confirmação)
*   **Pré-condições:** Ter concluído o processo de reserva (realizar CT-045 ou CT-046).
*   **Passos:**
    1.  Após o redirecionamento para a página de confirmação.
*   **Resultados Esperados:**
    *   A página deve exibir uma mensagem de sucesso na reserva.
    *   O status da reserva (ex: "Pending", "Confirmed") deve ser visível.
    *   Detalhes completos da reserva (Número da Reserva, Nome do Hotel, Datas, Hóspedes, Valor Total, Método de Pagamento) devem ser exibidos na página.

**CT-049: Verificar recebimento simulado de e-mail de confirmação**
*   **Módulo:** Reserva e Pagamento (Confirmação - E-mail)
*   **Pré-condições:** Ter concluído o processo de reserva com sucesso (realizar CT-045 ou CT-046) e ter um e-mail válido cadastrado/informado.
*   **Passos:**
    1.  Após a conclusão da reserva, verificar a caixa de entrada do e-mail utilizado na reserva.
*   **Resultados Esperados:**
    *   Um e-mail de confirmação de reserva (simulado, conforme requisito) deve ser recebido, contendo os detalhes da reserva. (Nota: Para testes manuais, pode ser necessário verificar logs internos se o e-mail não for realmente enviado para um cliente de e-mail).

**CT-050: Verificação da reserva na área "My Bookings" para usuário logado**
*   **Módulo:** Reserva e Pagamento (Integração com Conta)
*   **Pré-condições:** Usuário logado e ter concluído uma reserva com sucesso.
*   **Passos:**
    1.  Realizar o login na área do cliente (se necessário).
    2.  Navegar até a seção "My Account" > "Bookings".
*   **Resultados Esperados:**
    *   A reserva recém-criada deve estar listada na seção "My Bookings" do usuário.
    *   Os detalhes da reserva (nome do item, datas, status) devem corresponder aos da reserva.
