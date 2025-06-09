# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Autenticação de Usuário  
> Sistema: [Presta Shop](https://demo.prestashop.com/#/en/front)  
> Autor: Miguel Luis  
> Data: 2025-06-09  

---

## Cenário 01: Login com sucesso

### Caso de Teste 01: Login com as credenciais válidas (Happy Path)

| ID               | Descrição                                                 |
| :--------------- | :-------------------------------------------------------- |
| AUTH\_LOGIN\_001 | O login será realizado com um e-mail e uma senha válidos. |

| **Pré-condições**                   |
| :---------------------------------- |
| Usuário com conta válida existente. |

| **Passos**                                                                    |
| :---------------------------------------------------------------------------- |
| **DADO** que o usuário está na página de login                                |
| **QUANDO** ele insere o e-mail cadastrado e a senha correta                   |
| **E** clica no botão "Entrar"                                                 |
| **ENTÃO** ele deve ser redirecionado para a página da sua conta (ou homepage) |
| **E** o nome do usuário ou uma saudação deve ser visível                      |

| **Critérios de aceitação**                                                            |
| :------------------------------------------------------------------------------------ |
| O sistema deve redirecionar corretamente para a área logada com uma saudação visível. |

## Cenário 01.2: Login com credenciais inválidas

### Caso de Teste 02: Login com senha incorreta

| ID               | Descrição                                                    |
| :--------------- | :----------------------------------------------------------- |
| AUTH\_LOGIN\_002 | O login será tentado com e-mail válido, mas senha incorreta. |

| **Pré-condições** |
| :---------------- |
| Nenhuma.          |

| **Passos**                                                                                     |
| :--------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página de login                                                 |
| **QUANDO** ele insere um e-mail cadastrado e uma senha incorreta                               |
| **E** clica no botão "Entrar"                                                                  |
| **ENTÃO** uma mensagem de erro indicando "credenciais inválidas" (ou similar) deve ser exibida |
| **E** ele deve permanecer na página de login                                                   |

| **Critérios de aceitação**                                       |
| :--------------------------------------------------------------- |
| Mensagem de erro visível. Página de login não deve redirecionar. |

## Cenário 01.3: Tentativa de login com e-mail não cadastrado

### Caso de Teste 03: Login com e-mail inexistente

| ID               | Descrição                                                     |
| :--------------- | :------------------------------------------------------------ |
| AUTH\_LOGIN\_003 | O login será tentado com um e-mail não cadastrado no sistema. |

| **Pré-condições** |
| :---------------- |
| Nenhuma.          |

| **Passos**                                                                                 |
| :----------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página de login                                             |
| **QUANDO** ele insere um e-mail não cadastrado e uma senha qualquer                        |
| **E** clica no botão "Entrar"                                                              |
| **ENTÃO** uma mensagem de erro indicando que o e-mail não está registrado deve ser exibida |
| **E** ele deve permanecer na página de login                                               |

| **Critérios de aceitação**                                                  |
| :-------------------------------------------------------------------------- |
| Mensagem de erro clara e específica. Página de login não deve redirecionar. |

## Cenário 01.4: Validação de campos obrigatórios no login

### Caso de Teste 04: Tentativa de login com campos vazios

| ID               | Descrição                                                                              |
| :--------------- | :------------------------------------------------------------------------------------- |
| AUTH\_LOGIN\_004 | Verificar se o sistema valida corretamente os campos obrigatórios no formulário login. |

| **Pré-condições** |
| :---------------- |
| Nenhuma.          |

| **Passos**                                                                              |
| :-------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página de login                                          |
| **QUANDO** ele tenta submeter o formulário sem preencher o campo "e-mail" e/ou "senha"  |
| **ENTÃO** mensagens de erro indicando que os campos são obrigatórios devem ser exibidas |
| **E** o login não deve ser realizado                                                    |

| **Critérios de aceitação**                                                                                  |
| :---------------------------------------------------------------------------------------------------------- |
| Mensagens claras devem ser exibidas junto aos campos não preenchidos. O botão "Entrar" não deve prosseguir. |

## Cenário 01.5: Registro de novo usuário com sucesso

### Caso de Teste 05: Registro com dados válidos

| ID             | Descrição                                                                       |
| :------------- | :------------------------------------------------------------------------------ |
| AUTH\_REG\_001 | Verificar se o sistema permite o registro de um novo usuário com dados válidos. |

| **Pré-condições**                                                 |
| :---------------------------------------------------------------- |
| O e-mail usado no registro não deve estar cadastrado previamente. |

| **Passos**                                                                                                          |
| :------------------------------------------------------------------------------------------------------------------ |
| **DADO** que o usuário está na página de registro                                                                   |
| **QUANDO** ele preenche todos os campos obrigatórios com dados válidos (nome, sobrenome, e-mail único, senha forte) |
| **E** aceita os termos de uso (se houver)                                                                           |
| **E** clica no botão "Registrar" (ou "Salvar")                                                                      |
| **ENTÃO** uma mensagem de sucesso deve ser exibida                                                                  |
| **E** o usuário deve ser logado automaticamente **OU** redirecionado para a página de login                         |

| **Critérios de aceitação**                                                                                             |
| :--------------------------------------------------------------------------------------------------------------------- |
| O registro deve ser concluído com sucesso, sem erros. O usuário deve ser redirecionado ou autenticado automaticamente. |

## Cenário 01.6: Tentativa de registro com e-mail já existente

### Caso de Teste 06: Registro com e-mail duplicado

| ID             | Descrição                                                                                      |
| :------------- | :--------------------------------------------------------------------------------------------- |
| AUTH\_REG\_002 | Verificar se o sistema impede o registro de um novo usuário utilizando um e-mail já existente. |

| **Pré-condições**                                                              |
| :----------------------------------------------------------------------------- |
| O e-mail inserido no formulário já deve estar vinculado a uma conta existente. |

| **Passos**                                                                             |
| :------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página de registro                                      |
| **QUANDO** ele preenche os campos obrigatórios com um e-mail já cadastrado             |
| **E** clica no botão "Registrar" (ou "Salvar")                                         |
| **ENTÃO** uma mensagem de erro informando que o e-mail já está em uso deve ser exibida |
| **E** o registro **não** deve ser realizado                                            |

## Cenário 01.7: Validação de força de senha no registro

### Caso de Teste 07: Registro com senha fraca

| ID             | Descrição                                                                        |
| :------------- | :------------------------------------------------------------------------------- |
| AUTH\_REG\_003 | Verificar se o sistema realiza a validação de força de senha durante o registro. |

| **Pré-condições**                           |
| :------------------------------------------ |
| O usuário deve estar na página de registro. |

| **Passos**                                                                                                            |
| :-------------------------------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página de registro                                                                     |
| **QUANDO** ele insere uma senha que não atende aos critérios de segurança (ex: muito curta, sem caracteres especiais) |
| **E** clica no botão "Registrar"                                                                                      |
| **ENTÃO** uma mensagem de erro indicando os requisitos da senha deve ser exibida                                      |
| **E** o registro **não** deve ser concluído                                                                           |

| **Critérios de aceitação**                                                                                         |
| :----------------------------------------------------------------------------------------------------------------- |
| A mensagem de erro deve listar os critérios mínimos exigidos (ex: mínimo de caracteres, uso de números, símbolos). |

## Cenário 01.8: Recuperação de senha

### Caso de Teste 08: Recuperação de senha com e-mail válido

| ID                 | Descrição                                                                                                 |
| :----------------- | :-------------------------------------------------------------------------------------------------------- |
| AUTH\_PASSREC\_001 | Verificar se o sistema permite a recuperação de senha a partir de um e-mail válido cadastrado no sistema. |

| **Pré-condições**                                         |
| :-------------------------------------------------------- |
| O usuário deve ter uma conta válida com e-mail acessível. |

| **Passos**                                                                                                        |
| :---------------------------------------------------------------------------------------------------------------- |
| **DADO** que o usuário está na página de login                                                                    |
| **E** clica no link "Esqueceu sua senha?"                                                                         |
| **QUANDO** ele insere seu e-mail cadastrado no campo indicado                                                     |
| **E** clica no botão "Recuperar Senha"                                                                            |
| **ENTÃO** uma mensagem de sucesso informando que as instruções de redefinição foram enviadas deve ser exibida     |
| *(Opcional)* **E** se houver simulação de e-mail, o link de redefinição deve permitir criar uma nova senha válida |
| **E** o usuário deve conseguir fazer login com a nova senha                                                       |

| **Critérios de aceitação**                                                                                                    |
| :---------------------------------------------------------------------------------------------------------------------------- |
| Mensagem de feedback positivo visível após o envio.                                                                           |
| *(Se aplicável)* Link de redefinição deve estar funcional e permitir a criação de nova senha conforme critérios de segurança. |

## Cenário 01.9: Logout

### Caso de Teste 09: Logout com sessão ativa

| ID                | Descrição                                                       |
| :---------------- | :-------------------------------------------------------------- |
| AUTH\_LOGOUT\_001 | Verificar se o usuário consegue encerrar a sessão corretamente. |

| **Pré-condições**                                        |
| :------------------------------------------------------- |
| O usuário deve estar logado no sistema com sessão ativa. |

| **Passos**                                                                               |
| :--------------------------------------------------------------------------------------- |
| **DADO** que o usuário está logado no sistema                                            |
| **QUANDO** ele clica no botão ou link "Sair" ou "Logout"                                 |
| **ENTÃO** a sessão do usuário deve ser encerrada                                         |
| **E** o usuário deve ser redirecionado para a página inicial ou login                    |
| **E** não deve mais ter acesso a informações ou funcionalidades restritas à conta logada |

| **Critérios de aceitação**                                       |
| :--------------------------------------------------------------- |
| Sessão encerrada com sucesso e redirecionamento correto.         |
| Informações pessoais e áreas restritas inacessíveis após logout. |
