## 🔐 Teste de Segurança Manual (Foco: Navegabilidade e Dados Visíveis)

**Prioridade:** ALTA
**Objetivo:**
Verificar aspectos básicos de segurança perceptíveis ao usuário durante a navegação.

---

### 🛡️ Abordagem

#### 🔒 HTTPS

* Todas as páginas críticas (login, cadastro, minha conta, checkout) são servidas **exclusivamente via HTTPS**?
* Verificar a presença do **cadeado** na barra de endereço do navegador.

#### 🔗 Dados Sensíveis na URL

* Após login, envio de formulários ou navegação, **nenhuma informação sensível** (senhas, números de cartão de crédito, CPF, etc.) deve estar visível na URL.

#### 👁️ Mascaramento de Senhas

* Os campos de senha em **login, cadastro e alteração de senha** estão com os caracteres mascarados (ex: `•••••••`)?

#### 💾 Autocompletar Senhas

* O navegador oferece a opção de **salvar senha**?
* Os formulários estão utilizando os atributos `autocomplete` corretos (ex: `current-password`, `new-password`)?

#### 🔐 Gerenciamento de Sessão

* Após logout, tentar acessar diretamente uma URL da área logada:

  * O sistema **bloqueia corretamente** o acesso?
* Fechando e reabrindo o navegador:

  * O usuário **permanece logado** ou é solicitado a logar novamente?
  * Essa política de sessão está de acordo com o esperado?

#### ⚠️ Exposição de Mensagens de Erro

* As mensagens de erro são **genéricas** e não revelam detalhes internos do sistema?

  * Exemplo adequado: `"Ocorreu um erro, tente novamente."`
  * Exemplo inadequado: `"SQL Exception: missing column 'user_id' in table users"`
