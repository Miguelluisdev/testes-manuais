# 📖 Regras de Negócio – Testes Manuais PHPTRAVELS.NET

Este documento apresenta uma análise completa das **Regras de Negócio (RN)** do sistema de demonstração [phptravels.net](https://phptravels.net), com foco em orientar a criação de casos de teste manuais que validem a lógica, restrições e consistência da plataforma, além dos fluxos funcionais.

---

## 📌 1. Regras de Negócio Gerais (Globais)

- **RN-GL-01 – Moeda**  
  A moeda padrão do sistema é o **Dólar Americano (USD)**.  
  Quando alterada pelo usuário, **todos os valores monetários do site** (como preços, taxas e totais) devem ser **recalculados e exibidos na nova moeda selecionada**, mantendo essa configuração **durante toda a sessão** do usuário.

- **RN-GL-02 – Idioma**  
  O idioma padrão da aplicação é o **Inglês**.  
  A alteração do idioma deve **traduzir todos os textos estáticos da interface** (menus, botões, rótulos) e, quando possível, também o **conteúdo dinâmico**, como descrições de hotéis e passeios, **caso estejam disponíveis na linguagem selecionada**.

- **RN-GL-03 – Acesso Condicional ao Menu de Conta**  
  O menu “My Account” deve:
  - Exibir "Login" e "Sign Up" para usuários **não autenticados**
  - Exibir "Dashboard", "My Profile" e "Logout" para usuários **autenticados**

---

## 🔍 2. Regras de Negócio da Busca

Regras que controlam a lógica de preenchimento e restrições dos formulários de busca.

- **RN-BUSCA-01 – Lógica de Datas (Geral)**  
  Nenhuma data de início (Check-in, Departure, Pick up) pode ser anterior à data atual.  
  O sistema **deve restringir a seleção apenas a datas atuais ou futuras**.

- **RN-BUSCA-02 – Datas em Hotéis**  
  A data de **Check-out deve ser, no mínimo, um dia após o Check-in**.  
  O sistema não deve permitir datas iguais ou anteriores.

- **RN-BUSCA-03 – Datas em Voos**  
  Para voos do tipo "Round Trip", a data de retorno **deve ser igual ou posterior à de partida**.

- **RN-BUSCA-04 – Datas em Aluguel de Carros**  
  A **data e hora de Drop off devem ser posteriores à de Pick up**.

- **RN-BUSCA-05 – Ocupantes Mínimos**  
  Todas as buscas devem incluir **ao menos 1 adulto**.  
  **Não é permitido buscar apenas para crianças**.

- **RN-BUSCA-06 – Restrição de Localização (Voos)**  
  O campo "Flying From" **não pode ser igual** ao "To Destination".  
  O sistema deve bloquear ou exibir erro ao tentar pesquisar com **origem e destino idênticos**.

- **RN-BUSCA-07 – Restrição de Localização (Vistos)**  
  O campo "From Country" **não pode ser o mesmo** que "To Country" em buscas por vistos.

- **RN-BUSCA-08 – Campos Obrigatórios**  
  Todos os campos principais (como local de origem/destino, datas) são **obrigatórios**.  
  O botão **"Search" só deve ser habilitado quando os campos obrigatórios estiverem preenchidos corretamente**.

---

## 🔐 3. Regras de Negócio da Conta de Usuário e Autenticação

- **RN-CONTA-01 – Unicidade de E-mail**  
  O e-mail é o identificador único do usuário.  
  **Não é permitido cadastrar dois usuários com o mesmo e-mail**.

- **RN-CONTA-02 – Validação de Senha**  
  Durante o cadastro, os campos "Password" e "Confirm Password" **devem ser idênticos**.  
  O sistema **só deve permitir o envio do formulário caso a correspondência seja válida**.

- **RN-CONTA-03 – Política de Senha**  
  A senha deve conter **no mínimo 6 caracteres** (regra mínima de complexidade).

- **RN-CONTA-04 – Associação de Reservas**  
  Reservas feitas por um usuário autenticado devem ser **automaticamente associadas ao seu perfil**, aparecendo na seção “Bookings”.

- **RN-CONTA-05 – Persistência de Dados**  
  Alterações feitas no perfil do usuário (“My Profile”) devem ser **salvas permanentemente** e refletidas em futuras reservas (com preenchimento automático dos campos).

---

## 💳 4. Regras de Negócio do Fluxo de Reserva e Preços

- **RN-RESERVA-01 – Cálculo de Preço (Hotéis)**  
  O cálculo total deve seguir a fórmula:  
  **(Preço por Noite × Nº de Noites) + Taxas Fixas (se houver) + Impostos Percentuais (se houver)**  
  O resumo da reserva deve **detalhar claramente esses valores**.

- **RN-RESERVA-02 – Disponibilidade**  
  Só é possível concluir uma reserva se o item (ex: quarto de hotel) **estiver disponível** para o período e quantidade selecionados.  
  QA deve validar **tentando reservar o mesmo quarto em sessões simultâneas**.

- **RN-RESERVA-03 – Dados do Hóspede**  
  O preenchimento dos dados do hóspede principal é **obrigatório mesmo para usuários logados**:  
  - Nome  
  - Sobrenome  
  - E-mail  
  - Telefone

- **RN-RESERVA-04 – Concordância Obrigatória**  
  A caixa de seleção "I agree with the Terms and Conditions" é **obrigatória**.  
  O botão “Confirm Booking” **deve permanecer desabilitado** até que ela seja marcada.

- **RN-RESERVA-05 – Status Inicial da Reserva**  
  Toda reserva é criada inicialmente com o status **“Pending”**.  
  Esse status deve ser exibido:
  - Na página de confirmação
  - Na listagem de “Bookings” do cliente

- **RN-RESERVA-06 – Geração de Fatura (Invoice)**  
  Após confirmação, o sistema deve **gerar uma fatura única**, contendo:
  - Código da reserva  
  - Datas  
  - Itens reservados  
  - Valores e totais  
  - Dados do cliente  
  Essa fatura deve ser **acessível ao usuário**.

- **RN-RESERVA-07 – Pagamento Simulado**  
  Os métodos de pagamento disponíveis ("Pay by Deposit", "Pay Later") **não processam transações reais**, mas:
  - Devem permitir o avanço para a próxima etapa do processo  
  - Devem manter a lógica de fluxo intacta, como se fossem reais

---

## 📌 Observações Finais

> As regras de negócio representam o **coração da lógica da aplicação** e devem ser **testadas com rigor**, mesmo em ambientes de demonstração. Elas garantem integridade de dados, coerência de fluxo e previsibilidade de comportamento — pilares fundamentais para uma aplicação confiável.

🧪 Casos de teste específicos para essas regras serão criados individualmente e associados aos respectivos fluxos (busca, conta, reserva), organizados por pastas.

