# 🔐 Testes de Privacidade e LGPD — PHPTRAVELS.NET

## 🧾 Cenário 1 — Consentimento para Coleta de Dados Pessoais

**Descrição:**
Verificar se o sistema solicita o consentimento explícito do usuário para o uso de dados pessoais antes do cadastro ou envio de formulários.

**Tipo de Teste:** Privacidade / LGPD — Consentimento
**Prioridade:** Alta
**Dados de teste:**

* Nome: “João Teste”
* Email: [joao@teste.com](mailto:joao@teste.com)
* Senha: 12345678

**Passos:**

1. Acessar “My Account” > “Sign Up”.
2. Preencher os campos obrigatórios.
3. Procurar por checkbox ou texto informando sobre o uso dos dados pessoais.
4. Tentar concluir o cadastro sem marcar o consentimento (caso exista).

**Resultado Esperado:**

* O sistema deve solicitar consentimento antes do envio do formulário.
* Caso o usuário não aceite, o cadastro não deve ser concluído.
* O texto deve explicar claramente a finalidade da coleta (“para criação e gestão da conta de usuário”).

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 2 — Exibição de Política de Privacidade

**Descrição:**
Verificar se há um link visível e acessível para a Política de Privacidade em todas as páginas do site.

**Tipo de Teste:** Privacidade / LGPD — Transparência
**Prioridade:** Alta

**Passos:**

1. Acessar a página inicial.
2. Rolar até o rodapé (footer).
3. Procurar o link “Privacy Policy” ou “Política de Privacidade”.
4. Clicar no link e verificar se o documento é exibido corretamente.

**Resultado Esperado:**

* O link deve estar presente em todas as páginas (footer).
* O conteúdo deve explicar claramente como os dados são coletados, usados e armazenados.
* Deve conter informações de contato do controlador de dados.

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 3 — Solicitação de Exclusão de Conta (Direito de Exclusão)

**Descrição:**
Garantir que o usuário consiga solicitar a exclusão de seus dados pessoais (direito ao esquecimento).

**Tipo de Teste:** Privacidade / LGPD — Direito do Titular
**Prioridade:** Alta
**Passos:**

1. Fazer login no sistema.
2. Acessar “My Profile” ou “Account Settings”.
3. Verificar se existe opção “Delete Account” ou formulário de contato para solicitar exclusão.
4. Clicar na opção e confirmar a solicitação.

**Resultado Esperado:**

* O sistema deve exibir mensagem de confirmação (“Sua conta será excluída permanentemente”).
* Dados do usuário devem ser removidos da base após confirmação.
* O site deve indicar um prazo ou canal de confirmação do processo.

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 4 — Máscara e Segurança de Campos Sensíveis

**Descrição:**
Verificar se campos de senha e dados sensíveis estão mascarados e protegidos.

**Tipo de Teste:** Privacidade / LGPD — Segurança
**Prioridade:** Alta

**Passos:**

1. Acessar página de Login e Cadastro.
2. Observar o campo “Password”.
3. Digitar senha e verificar se os caracteres estão mascarados (••••••).
4. Verificar se não é possível ver a senha via código-fonte (HTML).

**Resultado Esperado:**

* Campos de senha mascarados visualmente.
* Nenhum dado sensível (senha, token, CPF, e-mail) exposto no código-fonte ou em URLs.
* Página deve utilizar HTTPS.

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 5 — Proteção contra Exposição de Dados em URL

**Descrição:**
Validar se informações pessoais não aparecem em URLs durante o uso do sistema.

**Tipo de Teste:** Privacidade / LGPD — Segurança da Informação
**Prioridade:** Média

**Passos:**

1. Realizar login no sistema.
2. Acessar o perfil de usuário e as reservas.
3. Observar a URL exibida no navegador.

**Resultado Esperado:**
Nenhum dado sensível (e-mail, nome, ID de sessão, token) deve estar visível na URL.

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 6 — Retirada de Consentimento (Opt-out)

**Descrição:**
Verificar se o usuário pode revogar o consentimento para uso de dados pessoais.

**Tipo de Teste:** Privacidade / LGPD — Direito de Revogação
**Prioridade:** Média

**Passos:**

1. Fazer login.
2. Acessar configurações de conta ou notificações.
3. Verificar se há opção de “Revogar consentimento” ou “Desativar comunicações”.
4. Ativar a opção e salvar.

**Resultado Esperado:**

* Consentimento é revogado.
* O sistema deve parar de enviar comunicações automáticas (ex: e-mails promocionais).
* Usuário deve ser informado sobre as consequências da revogação.

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 7 — Acesso aos Dados Pessoais (Direito de Acesso)

**Descrição:**
Garantir que o usuário possa visualizar todas as informações pessoais armazenadas sobre ele.

**Tipo de Teste:** Privacidade / LGPD — Direito do Titular
**Prioridade:** Alta

**Passos:**

1. Fazer login.
2. Acessar “My Profile” ou seção de dados pessoais.
3. Verificar se todas as informações cadastradas (nome, e-mail, telefone, reservas) são exibidas de forma completa e legível.

**Resultado Esperado:**

* Usuário tem acesso a todos os dados pessoais que o sistema mantém sobre ele.
* Informações são exibidas de forma clara e organizada.

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 8 — Solicitação de Correção de Dados

**Descrição:**
Verificar se o usuário pode corrigir ou atualizar dados pessoais incorretos.

**Tipo de Teste:** Privacidade / LGPD — Retificação de Dados
**Prioridade:** Média

**Passos:**

1. Fazer login.
2. Acessar “My Profile”.
3. Editar informações incorretas (ex: número de telefone).
4. Salvar alterações.

**Resultado Esperado:**

* Dados são atualizados com sucesso.
* Sistema exibe mensagem “Dados atualizados com sucesso”.

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 9 — Retenção e Minimização de Dados

**Descrição:**
Verificar se o sistema armazena apenas dados necessários para o funcionamento da conta.

**Tipo de Teste:** Privacidade / LGPD — Minimização de Dados
**Prioridade:** Baixa

**Passos:**

1. Realizar cadastro.
2. Observar os campos obrigatórios.
3. Verificar se há solicitação de dados excessivos (ex: CPF, endereço completo, documento).

**Resultado Esperado:**
O sistema deve solicitar apenas dados essenciais (nome, e-mail, telefone, senha).

**Resultado Obtido:**
*Aguardando execução.*

---

## 🧾 Cenário 10 — Logs e Rastreamento de Sessão

**Descrição:**
Verificar se o sistema não armazena cookies ou logs indevidos sem consentimento.

**Tipo de Teste:** Privacidade / LGPD — Segurança e Consentimento
**Prioridade:** Baixa

**Passos:**

1. Acessar o site em modo anônimo.
2. Observar se há aviso de uso de cookies.
3. Verificar se cookies são criados antes do consentimento.

**Resultado Esperado:**

* Banner de cookies deve aparecer na primeira visita.
* Nenhum cookie de rastreamento deve ser criado antes do consentimento.

**Resultado Obtido:**
*Aguardando execução.*
