### **RF-02: Módulo de Autenticação e Gestão de Conta**

#### **RF-02.1 – Login**

**CT-012: Realizar Login com credenciais válidas**
*   **Módulo:** Autenticação (Login)
*   **Pré-condições:** Usuário cadastrado e com credenciais válidas (e-mail, senha).
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  Clicar em "My Account" no cabeçalho.
    3.  Selecionar "Login" no menu dropdown.
    4.  Na página de Login, preencher o campo "Email" com um e-mail válido.
    5.  Preencher o campo "Password" com a senha correspondente.
    6.  Clicar no botão "Login".
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para o painel da área do cliente (`/account/dashboard`).
    *   O nome do usuário ou uma mensagem de boas-vindas deve ser exibido na área logada.

**CT-013: Tentar Login com e-mail inválido**
*   **Módulo:** Autenticação (Login)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a página de Login (`https://phptravels.net/login`).
    2.  Preencher o campo "Email" com um e-mail que não existe no sistema (ex: `email.nao.cadastrado@teste.com`).
    3.  Preencher o campo "Password" com qualquer senha.
    4.  Clicar no botão "Login".
*   **Resultados Esperados:**
    *   Uma mensagem de erro clara e visível deve ser exibida, informando que o e-mail não foi encontrado ou as credenciais são inválidas.
    *   O usuário **não** deve ser logado e permanecer na página de Login.

**CT-014: Tentar Login com senha inválida**
*   **Módulo:** Autenticação (Login)
*   **Pré-condições:** Usuário cadastrado e com e-mail válido.
*   **Passos:**
    1.  Acessar a página de Login (`https://phptravels.net/login`).
    2.  Preencher o campo "Email" com um e-mail válido de um usuário cadastrado.
    3.  Preencher o campo "Password" com uma senha incorreta.
    4.  Clicar no botão "Login".
*   **Resultados Esperados:**
    *   Uma mensagem de erro clara e visível deve ser exibida, informando que a senha está incorreta ou as credenciais são inválidas.
    *   O usuário **não** deve ser logado e permanecer na página de Login.

**CT-015: Verificar funcionalidade "Remember Me"**
*   **Módulo:** Autenticação (Login)
*   **Pré-condições:** Usuário cadastrado e com credenciais válidas.
*   **Passos:**
    1.  Acessar a página de Login (`https://phptravels.net/login`).
    2.  Preencher o campo "Email" com um e-mail válido.
    3.  Preencher o campo "Password" com a senha correspondente.
    4.  Marcar o checkbox "Remember Me".
    5.  Clicar no botão "Login".
    6.  Após o login bem-sucedido, fechar o navegador ou limpar os cookies da sessão (simulando um fechamento) e reabrir `https://phptravels.net/`.
*   **Resultados Esperados:**
    *   Ao reabrir o site, o usuário deve estar logado automaticamente (o nome do usuário ou "My Account" deve indicar que está logado), ou o campo de e-mail na página de login deve estar pré-preenchido. (Observação: A implementação pode variar entre manter o login ou apenas lembrar o e-mail).

**CT-016: Verificar link "Forgot Password?"**
*   **Módulo:** Autenticação (Login)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a página de Login (`https://phptravels.net/login`).
    2.  Clicar no link "Forgot Password?".
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para a página de recuperação de senha (`/forgot-password`).
    *   A página deve conter um campo para inserir o e-mail e um botão para enviar as instruções de recuperação.

---

#### **RF-02.2 – Cadastro (Sign Up)**

**CT-017: Realizar Cadastro de novo usuário com dados válidos**
*   **Módulo:** Autenticação (Sign Up)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a URL: `https://phptravels.net/`
    2.  Clicar em "My Account" no cabeçalho.
    3.  Selecionar "Sign Up" no menu dropdown.
    4.  Na página de Cadastro, preencher:
        *   "First Name": `Testador`
        *   "Last Name": `Sobrenome`
        *   "Phone": `11999999999`
        *   "Email": `email_valido_e_unico@teste.com` (garantir que seja um e-mail ainda não cadastrado)
        *   "Password": `Senha@123`
        *   "Confirm Password": `Senha@123`
    5.  Clicar no botão "Sign Up".
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para o painel da área do cliente (`/account/dashboard`) após o cadastro bem-sucedido.
    *   Uma mensagem de sucesso no cadastro pode ser exibida.

**CT-018: Tentar Cadastro com e-mail já existente**
*   **Módulo:** Autenticação (Sign Up)
*   **Pré-condições:** Usuário já cadastrado com um e-mail específico.
*   **Passos:**
    1.  Acessar a página de Cadastro (`https://phptravels.net/signup`).
    2.  Preencher todos os campos obrigatórios com dados válidos, exceto "Email".
    3.  No campo "Email", inserir um e-mail que já está cadastrado no sistema.
    4.  Preencher "Password" e "Confirm Password" com senhas válidas.
    5.  Clicar no botão "Sign Up".
*   **Resultados Esperados:**
    *   Uma mensagem de erro clara e visível deve ser exibida, informando que o e-mail já está em uso ou que o cadastro falhou.
    *   O usuário **não** deve ser redirecionado para o dashboard e permanecer na página de Cadastro.

**CT-019: Tentar Cadastro com senhas que não correspondem**
*   **Módulo:** Autenticação (Sign Up)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a página de Cadastro (`https://phptravels.net/signup`).
    2.  Preencher todos os campos obrigatórios com dados válidos.
    3.  No campo "Password", inserir uma senha (ex: `Senha@123`).
    4.  No campo "Confirm Password", inserir uma senha diferente (ex: `Senha@321`).
    5.  Clicar no botão "Sign Up".
*   **Resultados Esperados:**
    *   Uma mensagem de erro clara e visível deve ser exibida, informando que as senhas não coincidem.
    *   O usuário **não** deve ser redirecionado para o dashboard e permanecer na página de Cadastro.

**CT-020: Tentar Cadastro com campos obrigatórios vazios**
*   **Módulo:** Autenticação (Sign Up)
*   **Pré-condições:** N/A
*   **Passos:**
    1.  Acessar a página de Cadastro (`https://phptravels.net/signup`).
    2.  Deixar um ou mais campos obrigatórios (First Name, Last Name, Phone, Email, Password, Confirm Password) vazios.
    3.  Tentar clicar no botão "Sign Up".
*   **Resultados Esperados:**
    *   Mensagens de erro de validação devem ser exibidas para cada campo obrigatório não preenchido.
    *   O botão "Sign Up" pode estar desabilitado ou, se clicável, o cadastro não deve prosseguir.
    *   O usuário **não** deve ser redirecionado para o dashboard.

---

#### **RF-02.3 – Área do Cliente (Dashboard)**

**CT-021: Verificar acesso ao Dashboard após Login bem-sucedido**
*   **Módulo:** Área do Cliente (Dashboard)
*   **Pré-condições:** Usuário logado (realizar CT-012 primeiro).
*   **Passos:**
    1.  Após realizar o login com sucesso.
*   **Resultados Esperados:**
    *   O URL deve ser `https://phptravels.net/account/dashboard`.
    *   A página deve exibir um painel com informações do usuário.
    *   O menu de navegação lateral ou superior deve conter links para "Bookings", "My Profile", "Logout".

**CT-022: Acessar "Bookings" no menu do cliente**
*   **Módulo:** Área do Cliente (Bookings)
*   **Pré-condições:** Usuário logado.
*   **Passos:**
    1.  Acessar o Dashboard.
    2.  Clicar no link "Bookings" no menu da área do cliente.
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para a página de reservas (`/account/bookings`).
    *   A página deve exibir uma lista das reservas feitas pelo usuário (se houver).

**CT-023: Acessar "My Profile" no menu do cliente e verificar dados**
*   **Módulo:** Área do Cliente (My Profile)
*   **Pré-condições:** Usuário logado.
*   **Passos:**
    1.  Acessar o Dashboard.
    2.  Clicar no link "My Profile" no menu da área do cliente.
*   **Resultados Esperados:**
    *   O usuário deve ser redirecionado para a página de perfil (`/account/profile`).
    *   Os campos de dados pessoais (First Name, Last Name, Email, Phone) devem estar pré-preenchidos com as informações do usuário.
    *   Deve existir uma opção para alterar a senha, mas o campo da senha atual não deve ser exibido.

**CT-024: Realizar Logout da área do cliente**
*   **Módulo:** Área do Cliente (Logout)
*   **Pré-condições:** Usuário logado.
*   **Passos:**
    1.  Acessar o Dashboard.
    2.  Clicar no link "Logout" no menu da área do cliente.
*   **Resultados Esperados:**
    *   O usuário deve ser deslogado da aplicação.
    *   O usuário deve ser redirecionado para a página inicial (`https://phptravels.net/`) ou para a página de login.
    *   O menu "My Account" no cabeçalho deve exibir "Login" e "Sign Up", indicando que o usuário não está logado.
