# 🧾 Análise de Requisitos Funcionais – Testes Manuais PHPTRAVELS

Este repositório documenta os requisitos funcionais e não funcionais identificados na plataforma de demonstração [phptravels.net](https://phptravels.net), com foco na elaboração de um plano de testes manuais completo.

---

## 📌 Escopo da Análise

### ✅ Em Escopo:
- Funcionalidades acessíveis ao **usuário final (autenticado e não autenticado)**.
- Módulos de **busca, visualização de resultados**, **processo de reserva (demonstrativo)** e **gestão de conta**.

### ❌ Fora de Escopo:
- Painel de Administração (backend).
- Integrações reais com APIs de terceiros (GDS, provedores de hotéis, gateways de pagamento).
- Testes de performance de carga e estresse (focaremos nos testes manuais).
- Testes de penetração de segurança avançados.

---

## 📚 Requisitos Funcionais Detalhados

### 🔹 RF-01: Módulo de Busca Principal (Página Inicial)

- **RF-01.1**: O sistema deve exibir um widget de busca com as seguintes abas:
  - **Hotels**, **Flights**, **Tours**, **Cars**, **Visa**.
- **RF-01.2**: A aba "Hotels" deve ser selecionada por padrão ao carregar a página.

#### 🔸 RF-01.3 – Hotels
- Campo: "Search by city or hotel name" com auto-complete.
- Campo: Check-in (calendário).
- Campo: Check-out (calendário).
- Campo: Travelers (adultos e crianças).
- Botão "Search" habilitado após preenchimento válido.

#### 🔸 RF-01.4 – Flights
- Campo: Flying from (auto-complete).
- Campo: To destination (auto-complete).
- Campo: Trip Type ("Round Trip", "One Way").
- Campo: Departure Date (calendário).
- Campo: Return Date (desabilitado se "One Way").
- Campo: Passengers (adultos, crianças, bebês).
- Botão "Search" habilitado.

#### 🔸 RF-01.5 – Tours
- Campo: Search by tour name or city (auto-complete).
- Campo: Date (calendário).
- Campo: Guests (número de viajantes).
- Botão "Search" habilitado.

#### 🔸 RF-01.6 – Cars
- Campo: Pick up location e Drop off location (auto-complete).
- Campos: Pick up/Drop off date e time.
- Botão "Search" habilitado.

#### 🔸 RF-01.7 – Visa
- Campo: From Country / To Country (dropdown).
- Campo: Date (calendário).
- Botão "Submit" habilitado.

---

### 🔹 RF-02: Módulo de Autenticação e Gestão de Conta

#### 🔸 RF-02.1 – Login
- Acesso via "My Account" > "Login".
- Login com e-mail e senha válidos.
- Mensagem de erro clara para credenciais inválidas.
- Checkbox "Remember Me".
- Link "Forgot Password?" disponível.

#### 🔸 RF-02.2 – Cadastro (Sign Up)
- Acesso via "My Account" > "Sign Up".
- Campos obrigatórios: First Name, Last Name, Phone, Email, Password, Confirm Password.
- Validação de formato e senha correspondente.
- Redirecionamento para o painel do usuário após sucesso.

#### 🔸 RF-02.3 – Área do Cliente (Dashboard)
- Acesso exclusivo para usuários autenticados.
- Menu com: Bookings, My Profile, Logout.
- Bookings: lista de reservas do usuário.
- My Profile: visualização/edição de dados pessoais.
- Alteração de senha disponível (sem exibição do campo).
- Logout: encerra sessão e redireciona para a home.

---

### 🔹 RF-03: Fluxo de Busca e Resultados

- **RF-03.1**: Redirecionamento para a página de resultados após busca válida.
- **RF-03.2**: Exibição de lista de resultados (hotéis, voos, etc.) com dados relevantes.
- **RF-03.3 – Filtros**:
  - Tipos: Star Grade, Price Range, Property Types, Amenities (para hotéis).
  - Atualização dinâmica (AJAX) sem reload.
- **RF-03.4 – Ordenação**:
  - Por: preço, nome, popularidade, etc.
- **RF-03.5 – Visualização**:
  - Alternância entre lista e grade.
- **RF-03.6**: Mensagem clara de "No results found" quando aplicável.
- **RF-03.7**: Cada item deve mostrar imagem, nome, preço e link "Details" ou "Book Now".

---

### 🔹 RF-04: Página de Detalhes do Item

- **RF-04.1**: Redirecionamento ao clicar em item da lista.
- **RF-04.2**: Exibição completa do item:
  - Nome, galeria de imagens, descrição, amenidades, mapa, avaliações.
- **RF-04.3 – Preços e disponibilidade**:
  - Tipos de quartos ou cabines.
  - Preço, políticas e botão para reservar.

---

### 🔹 RF-05: Reserva e Pagamento (Checkout)

- **RF-05.1**: Redirecionamento à página de checkout após escolha.
- **RF-05.2**: Usuário não logado deve preencher dados; logado vê campos preenchidos.
- **RF-05.3**: Exibição de resumo da reserva.
- **RF-05.4**: Pagamento simulado (Pay by Deposit, Pay Later).
- **RF-05.5**: Checkbox de aceite dos termos obrigatória.
- **RF-05.6**: Confirmação via página final com status da reserva.
- **RF-05.7**: Detalhes da reserva exibidos na confirmação.
- **RF-05.8**: Envio simulado de e-mail de confirmação.
- **RF-05.9**: Reserva visível em "Bookings" na área do cliente.

---

### 🔹 RF-06: Funcionalidades Globais

- **RF-06.1 – Idioma**: O site deve permitir mudança de idioma, refletindo na UI.
- **RF-06.2 – Moeda**: Conversão dinâmica dos valores com base na seleção.
- **RF-06.3 – Navegação**:
  - Cabeçalho com links fixos.
  - Rodapé com links institucionais (About Us, Contact, etc.).

---

# 📘 Requisitos Não Funcionais – PHPTRAVELS.NET

## 🔹 RNF-01: Usabilidade

- **RNF-01.1**: A navegação deve ser **intuitiva e consistente** entre todas as páginas da aplicação.
- **RNF-01.2**: Mensagens de erro (ex: login incorreto, campos obrigatórios) devem ser:
  - Claras e diretas
  - Visíveis próximas ao campo que gerou o erro
- **RNF-01.3**: Componentes interativos (botões, links, formulários) devem apresentar:
  - **Feedback visual** em ações do usuário, como hover, clique ou foco.

---

## 🔹 RNF-02: Compatibilidade

- **RNF-02.1 – Navegadores**: O sistema deve funcionar corretamente nas versões atualizadas dos principais navegadores:
  - Google Chrome
  - Mozilla Firefox
  - Safari
  - Microsoft Edge

- **RNF-02.2 – Responsividade**:
  - O layout deve se adaptar a múltiplos tamanhos de tela (desktop, tablet, smartphone) sem comprometer a experiência do usuário.
  - Elementos não devem se sobrepor, quebrar ou sumir em resoluções menores.

---

## 🔹 RNF-03: Desempenho

- **RNF-03.1**: As páginas principais (**Home, Resultados, Detalhes**) devem carregar em **menos de 5 segundos** em uma conexão padrão (4G ou banda larga doméstica).

- **RNF-03.2**: As interações do usuário (ex: aplicar filtros, ordenar resultados, mudar de aba) devem:
  - Ser processadas rapidamente (preferencialmente em menos de 1 segundo).
  - Não travar a interface ou recarregar desnecessariamente a página.

---

## 🔹 RNF-04: Segurança (Nível Básico)

- **RNF-04.1**: A aplicação deve utilizar **HTTPS** para criptografar dados em trânsito.
- **RNF-04.2**: Campos de senha devem **mascarar os caracteres** digitados (•••••).
- **RNF-04.3**: **Informações sensíveis não devem aparecer em URLs**, como senhas, tokens ou dados pessoais.

---

## 🔹 RNF-05: Consistência

- **RNF-05.1**: A **identidade visual** deve ser mantida em todas as páginas:
  - Cores institucionais
  - Tipografia
  - Logos e ícones
  - Estilo dos botões e formulários

- **RNF-05.2**: A **terminologia** deve ser consistente:
  - Exemplo: usar sempre **"Booking"** ou sempre **"Reservation"**, evitando alternância entre os dois sem critério.

---

## ✅ Aplicação nos Testes Manuais

Esses requisitos serão validados em conjunto com os testes funcionais, através de:

- Testes exploratórios focados em **experiência do usuário**
- Execução em diferentes navegadores e dispositivos
- Acompanhamento de tempos de resposta e carregamento
- Avaliação visual de componentes interativos
- Análise de boas práticas de segurança visível


## 🔍 Abordagem de Testes

- 📌 **Baseada em Requisitos**: Todos os testes manuais derivam diretamente dos requisitos descritos acima.
- 🧪 **Tipos de teste aplicados**:
  - Cenários **positivos** (happy path)
  - **Negativos** (campos inválidos, ações incorretas)
  - **Limites** (datas mínimas/máximas, quantidade de hóspedes)
  - **Alternativos** (interações fora da ordem esperada)

- 🛠️ **Estratégia**:
  - Casos de teste por priorização critica.
  - Registro de **evidências visuais** (prints, vídeos).
  - Acompanhamento em relatórios .

- 💡 **Objetivo Final**: Garantir que a experiência do usuário esteja alinhada com os requisitos do sistema, reduzindo riscos e garantindo entregas com qualidade.
