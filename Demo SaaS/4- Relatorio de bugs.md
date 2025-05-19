# 🐞 Relatório de Bugs - BugBug Demo SaaS

**Sistema testado:** [https://demo-saas.bugbug.io/](https://demo-saas.bugbug.io/)  
**Tipo de teste:** Manual  
**Ambiente de Testes:**  
- SO: Windows (x86) 11 / Motorola g75 5g
- Navegador: Google Chrome 124.0 mobile / Microsoft Edge 136.0.
- Resolução de tela: 1920x1080  
- Data de execução:  19 de maio de 2025
- **QA responsável:** Miguel Luis

---

### 🐞 **Bug 01: Mensagem de erro incorreta ao tentar login com campo email vazio**

| **ID**     | **Descrição**                                                                                                   |
| ---------- | ------------------------------------------------------------------------------------------------------------- |
| BUG-001    | Ao tentar login com o campo de email vazio, o sistema exibe a mensagem "Invalid email" ao invés de "Campo de email vazio". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug**                     |
| -------------------------------------------------------- |
| 1. Acessar a tela de login                               |
| 2. Deixar o campo email vazio                            |
| 3. Inserir senha válida                                  |
| 4. Clicar no botão "Login"                               |
| 5. Observar a mensagem de erro exibida                   |

|                        **Comportamento Esperado**                        |                      **Comportamento Obtido**                      |
| :----------------------------------------------------------------------: | :----------------------------------------------------------------: |
| Exibir mensagem clara indicando que o campo de email está vazio.          | Exibe mensagem "Invalid email" que não corresponde ao campo vazio. |

| **Ambiente**                      |
| -------------------------------- |
| Ambiente de homologação           |
| Desktop Windows 11, Microsoft Edge v136.0 |

| **Funcionalidade Afetada** |       **Caso de Teste Relacionado**        |
| :------------------------: | :----------------------------------------: |
| Tela de Login               | C01-CT02: Login com campos vazios           |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/d20c313c-430d-4d26-b12e-0bc4024b2d56) |

### 🐞 **Bug 02: Sistema envia email de recuperação para email não cadastrado**

| **ID**     | **Descrição**                                                                                              |
| ---------- | -------------------------------------------------------------------------------------------------------- |
| BUG-002    | O sistema envia email com instruções de recuperação mesmo quando o email informado não está cadastrado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|        Crítico        |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                   |
| ------------------------------------------------------ |
| 1. Acessar a tela "Esqueceu a senha?"                 |
| 2. Inserir um email que não está cadastrado no sistema |
| 3. Clicar em "Enviar"                                  |
| 4. Verificar se o sistema envia o email de recuperação |

|                        **Comportamento Esperado**                          |                      **Comportamento Obtido**                        |
| :------------------------------------------------------------------------: | :------------------------------------------------------------------: |
| O sistema deve exibir uma mensagem de erro informando que o email não existe.| O sistema envia email de recuperação mesmo para email não cadastrado. |

| **Ambiente**                      |
| -------------------------------- |
| Ambiente de homologação           |
| Desktop Windows 11, Microsoft Edge v136.0 |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**           |
| :------------------------: | :-----------------------------------------------: |
| Recuperação de senha        | C08-CT02: Solicitar recuperação com email inválido |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f3bfa413-16b1-40e0-92af-f26f7ef980f3) |

### 🐞 **Bug 03: Permissão para criar ticket após encerramento da sessão do usuário**

| **ID**     | **Descrição**                                                                                           |
| ---------- | ----------------------------------------------------------------------------------------------------- |
| BUG-003    | O sistema permite criar um ticket de task mesmo após o usuário encerrar a sessão (logout) no navegador.|

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|        Crítico        |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**               |
| -------------------------------------------------- |
| 1. Logar no sistema                                |
| 2. Criar tickets normalmente                        |
| 3. Encerrar a sessão no navegador (logout)         |
| 4. Tentar criar um novo ticket                      |

|                        **Comportamento Esperado**                        |                        **Comportamento Obtido**                         |
| :----------------------------------------------------------------------: | :---------------------------------------------------------------------: |
| O sistema deve bloquear a criação de tickets após logout.                 | O sistema permite criar tickets mesmo após o encerramento da sessão.    |

| **Ambiente**                      |
| -------------------------------- |
| Ambiente de homologação           |
| Desktop Windows 11, Microsoft Edge v136.0  |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**           |
| :------------------------: | :-----------------------------------------------: |
| Gestão de Tickets           | C04-CT03: Criar tickets com sessão encerrada        |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f3bfa413-16b1-40e0-92af-f26f7ef980f3) |

### 🐞 **Bug 04: Navegação e exibição incorreta do perfil após encerramento da sessão**

| **ID**     | **Descrição**                                                                                              |
| ---------- | -------------------------------------------------------------------------------------------------------- |
| BUG-004    | Após encerrar a sessão no navegador, o usuário ainda visualiza o perfil, projeto e navegação como se estivesse logado, podendo acessar conteúdos indevidamente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|        Crítico        |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                      |
| --------------------------------------------------------- |
| 1. Fazer login no sistema                                 |
| 2. Navegar pela plataforma, visualizando perfil e projetos|
| 3. Encerrar a sessão pelo navegador (logout)              |
| 4. Observar que o perfil, projeto e header permanecem visíveis e acessíveis |

|                        **Comportamento Esperado**                        |                         **Comportamento Obtido**                          |
| :----------------------------------------------------------------------: | :-----------------------------------------------------------------------: |
| O sistema deve ocultar o perfil, projetos e navegação após logout.        | Perfil, projeto e navegação permanecem visíveis e acessíveis após logout.|

| **Ambiente**                      |
| -------------------------------- |
| Ambiente de homologação           |
| Desktop Windows 11, Microsoft Edge v136.0  |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
| Navegação / Sessão          | C04-CT04: Encerrar sessão e verificar navegação    |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f3bfa413-16b1-40e0-92af-f26f7ef980f3) |

### 🐞 **Bug 05: Falta de mensagem de erro 404 ao acessar rota inválida**

| **ID**     | **Descrição**                                                                                      |
| ---------- | ------------------------------------------------------------------------------------------------ |
| BUG-005    | Ao inserir uma rota inválida na URL, o sistema não exibe uma mensagem de erro 404, mostrando apenas uma tela em branco. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug**                    |
| ------------------------------------------------------- |
| 1. Acessar o sistema                                   |
| 2. Inserir uma URL com rota inválida (exemplo: /rota-invalida) |
| 3. Observar a tela apresentada                         |

|                        **Comportamento Esperado**                         |                        **Comportamento Obtido**                         |
| :------------------------------------------------------------------------: | :----------------------------------------------------------------------: |
| O sistema deve exibir uma página de erro 404 informando que a rota não existe.| O sistema exibe apenas uma tela em branco, sem mensagem de erro clara.  |

| **Ambiente**                      |
| -------------------------------- |
| Ambiente de homologação           |
| Desktop Windows 11, Microsoft Edge v136.0  |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
| Navegação                   | C05-CT02: Inserir rota inválida                      |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/01d215b2-52af-46ac-8eb9-d45bb89ce3db) |

### 🐞 **Bug 06: Acesso indevido a projeto e dados após encerramento da sessão, com erro de feedback ausente**

| **ID**     | **Descrição**                                                                                                  |
| ---------- | -------------------------------------------------------------------------------------------------------------- |
| BUG-006    | Após encerrar a sessão no navegador, ainda é possível acessar projetos e dados do usuário. Ao tentar alterar o nome, o sistema sinaliza um erro, porém sem exibir mensagem explicativa, apenas um ícone de exclamação. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|        Crítico        |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                      |
| --------------------------------------------------------- |
| 1. Fazer login no sistema                                 |
| 2. Navegar até um projeto e acessar dados da conta       |
| 3. Encerrar a sessão no navegador (logout)               |
| 4. Tentar acessar o projeto e dados novamente            |
| 5. Tentar alterar o nome do usuário                       |
| 6. Observar que aparece um ícone de erro sem mensagem     |

|                        **Comportamento Esperado**                          |                        **Comportamento Obtido**                            |
| :------------------------------------------------------------------------: | :------------------------------------------------------------------------: |
| Após logout, o sistema deve bloquear o acesso a projetos e dados; ao sinalizar erro, deve exibir mensagem clara explicativa. | Acesso a projetos e dados permanece; erro é sinalizado apenas por ícone sem mensagem. |

| **Ambiente**                      |
| -------------------------------- |
| Ambiente de homologação           |
| Desktop Windows 11, Microsoft Edge v136.0 |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
| Sessão / Gestão de Conta    | C04-CT04: Encerrar sessão e tentar modificar nome   |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f3bfa413-16b1-40e0-92af-f26f7ef980f3) |

