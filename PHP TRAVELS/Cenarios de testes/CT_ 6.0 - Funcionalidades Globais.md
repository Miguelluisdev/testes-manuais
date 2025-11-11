### **RF-06: Funcionalidades Globais**

#### **RF-06.1 – Idioma**

**CT-051: Alterar o idioma do site para Inglês (English)**
*   **Módulo:** Funcionalidades Globais (Idioma)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  Localizar o seletor de idioma (geralmente no cabeçalho).
    3.  Clicar no seletor e selecionar "English" (se não for o padrão) ou outro idioma disponível.
*   **Resultados Esperados:**
    *   Toda a interface do usuário (textos de menu, botões, campos, mensagens) deve ser atualizada para o idioma selecionado (Inglês).
    *   A URL pode ou não refletir a mudança de idioma (ex: `/en/`).

**CT-052: Alterar o idioma do site para outro idioma disponível (ex: Português, Espanhol)**
*   **Módulo:** Funcionalidades Globais (Idioma)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  Localizar o seletor de idioma.
    3.  Clicar no seletor e selecionar um idioma diferente do padrão e do Inglês (ex: "Português", "Espanhol").
*   **Resultados Esperados:**
    *   Toda a interface do usuário deve ser atualizada para o idioma selecionado.
    *   A funcionalidade do site não deve ser comprometida pela mudança de idioma.

---

#### **RF-06.2 – Moeda**

**CT-053: Alterar a moeda do site para Dólar Americano (USD)**
*   **Módulo:** Funcionalidades Globais (Moeda)
*   **Pré-condições:** O site deve exibir preços em uma moeda padrão diferente de USD.
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  Localizar o seletor de moeda (geralmente no cabeçalho).
    3.  Clicar no seletor e selecionar "USD" (Dólar Americano).
*   **Resultados Esperados:**
    *   Todos os valores monetários exibidos no site (preços de hotéis, tours, carros, resumo de reservas) devem ser convertidos e exibidos em Dólar Americano.
    *   O símbolo da moeda deve ser atualizado para "$" ou "USD".

**CT-054: Alterar a moeda do site para outra moeda disponível (ex: Euro, Real Brasileiro)**
*   **Módulo:** Funcionalidades Globais (Moeda)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  Localizar o seletor de moeda.
    3.  Clicar no seletor e selecionar outra moeda disponível (ex: "EUR", "BRL").
*   **Resultados Esperados:**
    *   Todos os valores monetários exibidos no site devem ser convertidos e exibidos na moeda selecionada.
    *   O símbolo da moeda deve ser atualizado.
    *   A conversão deve parecer razoável (valores esperados para a moeda).

---

#### **RF-06.3 – Navegação**

**CT-055: Verificar links do cabeçalho de navegação (Home, Hotels, Flights, etc.)**
*   **Módulo:** Funcionalidades Globais (Navegação - Cabeçalho)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  Clicar sequencialmente em cada link principal do cabeçalho (ex: "Home", "Hotels", "Flights", "Tours", "Cars", "Visa").
*   **Resultados Esperados:**
    *   Cada link deve redirecionar corretamente para sua respectiva página.
    *   A página de destino deve carregar sem erros.

**CT-056: Verificar links do rodapé (institucionais)**
*   **Módulo:** Funcionalidades Globais (Navegação - Rodapé)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  Rolar a página até o rodapé.
    3.  Clicar em alguns links institucionais (ex: "About Us", "Contact Us", "Privacy Policy", "Terms of Use").
*   **Resultados Esperados:**
    *   Cada link do rodapé deve redirecionar corretamente para sua respectiva página de informação.
    *   As páginas de destino devem carregar sem erros e exibir conteúdo relevante.

---

### **Requisitos Não Funcionais (RNF)**

Agora que cobrimos os funcionais, vamos aos requisitos não funcionais. Para estes, os casos de teste serão mais orientados à observação e execução em diferentes cenários.

#### **RNF-01: Usabilidade**

**CT-057: Avaliar a intuitividade e consistência da navegação**
*   **Módulo:** Usabilidade
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Navegar por diferentes seções do site (home, resultados de busca, detalhes, perfil do usuário).
    2.  Observar a localização de menus, botões de ação e fluxo.
*   **Resultados Esperados:**
    *   A navegação entre as páginas deve ser fluida e previsível.
    *   Elementos de navegação (cabeçalho, rodapé, menus laterais) devem manter uma posição e estilo consistentes.
    *   O usuário deve conseguir realizar as principais ações sem precisar de instruções.

**CT-058: Verificar clareza e posicionamento das mensagens de erro (ex: Login inválido)**
*   **Módulo:** Usabilidade
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Tentar realizar um login com credenciais inválidas (conforme CT-013 ou CT-014).
    2.  Tentar um cadastro com senhas que não correspondem (conforme CT-019).
    3.  Tentar finalizar uma reserva sem aceitar os termos (conforme CT-047).
*   **Resultados Esperados:**
    *   Mensagens de erro devem ser exibidas de forma clara e compreensível para o usuário.
    *   As mensagens devem estar visíveis, idealmente próximas ao campo que gerou o erro.
    *   O texto da mensagem deve indicar o que deu errado e, se possível, como corrigir.

**CT-059: Observar feedback visual de componentes interativos**
*   **Módulo:** Usabilidade
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Passar o mouse sobre botões, links e campos de formulário.
    2.  Clicar em botões e links.
    3.  Focar em campos de formulário.
*   **Resultados Esperados:**
    *   Botões e links devem mudar de cor, sublinhado ou apresentar algum efeito visual ao passar o mouse (hover).
    *   Botões devem apresentar um estado visual de "clique" ou "ativo" ao serem pressionados.
    *   Campos de formulário devem ter um destaque visual (ex: borda colorida) ao receberem foco.

---

#### **RNF-02: Compatibilidade**

**CT-060: Testar funcionalidade em Google Chrome**
*   **Módulo:** Compatibilidade (Navegadores)
*   **Pré-condições:** Google Chrome (versão atualizada) instalado.
*   **Passos:**
    1.  Realizar os principais fluxos de teste (busca, login, reserva) no Google Chrome.
*   **Resultados Esperados:**
    *   Todas as funcionalidades devem operar corretamente.
    *   O layout e os elementos visuais devem ser exibidos sem distorções.

**CT-061: Testar funcionalidade em Mozilla Firefox**
*   **Módulo:** Compatibilidade (Navegadores)
*   **Pré-condições:** Mozilla Firefox (versão atualizada) instalado.
*   **Passos:**
    1.  Realizar os principais fluxos de teste no Mozilla Firefox.
*   **Resultados Esperados:**
    *   Todas as funcionalidades devem operar corretamente.
    *   O layout e os elementos visuais devem ser exibidos sem distorções.

**CT-062: Testar funcionalidade em Microsoft Edge**
*   **Módulo:** Compatibilidade (Navegadores)
*   **Pré-condições:** Microsoft Edge (versão atualizada) instalado.
*   **Passos:**
    1.  Realizar os principais fluxos de teste no Microsoft Edge.
*   **Resultados Esperados:**
    *   Todas as funcionalidades devem operar corretamente.
    *   O layout e os elementos visuais devem ser exibidos sem distorções.

**CT-063: Avaliar responsividade do layout em diferentes tamanhos de tela (desktop, tablet, smartphone)**
*   **Módulo:** Compatibilidade (Responsividade)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar o site em um navegador desktop e redimensionar a janela para simular tamanhos de tablet e smartphone (ou usar o modo de desenvolvedor do navegador).
    2.  Acessar o site diretamente em um tablet e/ou smartphone.
    3.  Navegar por diferentes páginas (Home, Resultados, Detalhes).
*   **Resultados Esperados:**
    *   O layout deve se adaptar fluidamente, sem barras de rolagem horizontais desnecessárias.
    *   Elementos não devem se sobrepor, quebrar ou desaparecer.
    *   Menus de navegação devem se transformar em formatos adequados para dispositivos móveis (ex: menu hambúrguer).
    *   A experiência do usuário deve ser mantida em todas as resoluções.

---

#### **RNF-03: Desempenho**

**CT-064: Medir tempo de carregamento da página inicial**
*   **Módulo:** Desempenho
*   **Pré-condições:** Ferramenta de desenvolvedor do navegador aberta (aba "Network").
*   **Passos:**
    1.  Abrir a aba "Network" no navegador.
    2.  Acessar a URL: `https://phptravels.net/`
    3.  Observar o tempo de carregamento total da página.
*   **Resultados Esperados:**
    *   O tempo de carregamento da página inicial deve ser **inferior a 5 segundos**.

**CT-065: Medir tempo de carregamento da página de resultados de busca**
*   **Módulo:** Desempenho
*   **Pré-condições:** Ferramenta de desenvolvedor do navegador aberta (aba "Network").
*   **Passos:**
    1.  Realizar uma busca de hotel válida (conforme CT-025).
    2.  Observar o tempo de carregamento total da página de resultados.
*   **Resultados Esperados:**
    *   O tempo de carregamento da página de resultados deve ser **inferior a 5 segundos**.

**CT-066: Observar tempo de resposta ao aplicar filtros e ordenação**
*   **Módulo:** Desempenho
*   **Pré-condições:** Estar na página de resultados de busca (ex: hotéis).
*   **Passos:**
    1.  Aplicar um filtro (conforme CT-027).
    2.  Alterar a ordenação (conforme CT-031).
    3.  Observar o tempo que leva para os resultados serem atualizados na tela.
*   **Resultados Esperados:**
    *   As atualizações de filtros e ordenação devem ocorrer **rapidamente (preferencialmente em menos de 1 segundo)**, sem travamento da interface ou recarregamento completo da página.

---

#### **RNF-04: Segurança (Nível Básico)**

**CT-067: Verificar uso de HTTPS em todas as páginas**
*   **Módulo:** Segurança
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Navegar por diversas páginas do site (Home, Login, Cadastro, Detalhes, Checkout).
    2.  Observar o ícone de cadeado na barra de endereço do navegador.
    3.  Verificar se a URL começa com `https://`.
*   **Resultados Esperados:**
    *   Todas as páginas do site devem utilizar HTTPS.
    *   O ícone de cadeado deve estar presente e indicar uma conexão segura.

**CT-068: Verificar mascaramento de caracteres em campos de senha**
*   **Módulo:** Segurança
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a página de Login (`https://phptravels.net/login`).
    2.  Acessar a página de Cadastro (`https://phptravels.net/signup`).
    3.  Digitar algo nos campos "Password" e "Confirm Password".
*   **Resultados Esperados:**
    *   Os caracteres digitados nos campos de senha devem ser mascarados (ex: exibidos como "•••••").

**CT-069: Verificar ausência de informações sensíveis em URLs**
*   **Módulo:** Segurança
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Realizar login.
    2.  Navegar para a página de perfil do usuário.
    3.  Realizar uma busca de hotel.
    4.  Observar a URL em cada uma dessas ações.
*   **Resultados Esperados:**
    *   Nenhum dado sensível (senhas, e-mails completos, tokens de sessão) deve aparecer na URL da página.
    *   A URL deve ser clara e não expor informações confidenciais.

---

#### **RNF-05: Consistência**

**CT-070: Avaliar consistência da identidade visual (cores, tipografia, logos, ícones)**
*   **Módulo:** Consistência
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Navegar por diferentes páginas do site (Home, Resultados, Detalhes, Login, Perfil).
    2.  Observar o uso de cores, fontes, estilos de botões e ícones.
*   **Resultados Esperados:**
    *   As cores da marca, tipografia e estilos de botões/formulários devem ser consistentes em todas as páginas.
    *   O logo e os ícones devem ser exibidos de forma padronizada.

**CT-071: Avaliar consistência da terminologia utilizada**
*   **Módulo:** Consistência
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Navegar pelo site e observar termos chave como "Booking" / "Reservation", "Guest" / "Traveler", "Search" / "Find".
*   **Resultados Esperados:**
    *   A terminologia utilizada para conceitos iguais deve ser consistente em todo o site. Por exemplo, se usa "Bookings" para reservas, deve-se manter "Bookings" e não alternar com "Reservations" sem uma razão clara.
