# Relatório de Bugs

**Software:** OrangeHRM

**QA responsável:** Miguel Luis

**Data:** 12.05.25

---

### 🐞 **Bug 01: Ícone de visualizar senha desaparece ao clicar fora do campo**

| **ID**     | **Descrição**                                                                                                                                             |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-001    | O ícone de “ver senha” desaparece ao clicar fora do campo de senha e não retorna ao clicar novamente, impedindo o usuário de visualizar a senha digitada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar a página de login                                   |
| 2. Digitar a senha no campo apropriado                         |
| 3. Clicar no ícone de "ver senha"                              |
| 4. Clicar fora do campo de senha                               |
| 5. Voltar a clicar no campo ou tentar ativar o ícone novamente |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O ícone de "ver senha" deve continuar visível mesmo após sair do campo. | O ícone desaparece e impede o usuário de visualizar a senha novamente. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Windows 11.  |
|  Microsoft Edge v.136.0    |
| OrangeHRM Demo           |

| **Funcionalidade Afetada** |        **Caso de Teste Relacionado**       |
| :------------------------: | :----------------------------------------: |
| Login / Criação de usuário | C01-CT01: Login com e-mail e senha válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/6ea09cdb-2ff1-402f-ba58-6554ce87dee8) |

---
#### Bug 02: Página de login atualiza ao ocorrer erro de autenticação

| **ID**     | **Descrição**                                                                                                          |
| ---------- | ------------------------------------------------------------------------------------------------------------------------ |
| BUG-002    | Ao inserir credenciais incorretas no login, a página é atualizada, o que prejudica a experiência do usuário (UX/UI).    |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                        |
| ----------------------------------------------------------- |
| 1. Acessar a página de login                                |
| 2. Inserir um nome de usuário ou senha inválidos            |
| 3. Clicar no botão "Login"                                  |

|                     **Comportamento Esperado**                      |                   **Comportamento Obtido**                   |
| :-----------------------------------------------------------------: | :-----------------------------------------------------------: |
| Exibir mensagem de erro sem atualizar a página                     | A página é atualizada e apenas então exibe a mensagem de erro |

| **Ambiente**             |
| ------------------------ |
| Ambiente de homologação. |
| Windows 11 + Microsoft Edge v.136.0 |
| OrangeHRM Demo           |

| **Funcionalidade Afetada** |         **Caso de Teste Relacionado**         |
| :------------------------: | :-------------------------------------------: |
|           Login            | C01-CT02: Login com credenciais inválidas     |

|              **Evidência(s)**              |
| :----------------------------------------: |
| [Vídeo](https://jam.dev/c/6ea09cdb-2ff1-402f-ba58-6554ce87dee8) |

---
#### Bug 03: Não há mensagem clara de sucesso ou falha no login

| **ID**     | **Descrição**                                                                                                     |
| ---------- | ------------------------------------------------------------------------------------------------------------------- |
| BUG-003    | O sistema não exibe mensagens de sucesso ou erro de forma clara após login, apenas redireciona ou atualiza a página. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média          |           Média            |   Aberto   |

| **Passo a passo para simular o bug**              |
| ------------------------------------------------- |
| 1. Acessar a página de login                      |
| 2. Inserir credenciais válidas                    |
| 3. Clicar em "Login"                              |

|                   **Comportamento Esperado**                   |                 **Comportamento Obtido**                  |
| :-------------------------------------------------------------: | :--------------------------------------------------------: |
| Mensagem como "Login realizado com sucesso" deve ser exibida   | Usuário é redirecionado diretamente sem mensagem alguma    |

| **Ambiente**             |
| ------------------------ |
| Ambiente de homologação. |
| Windows 11 + Microsoft Edge v.136.0 |
| OrangeHRM Demo           |

| **Funcionalidade Afetada** |         **Caso de Teste Relacionado**         |
| :------------------------: | :-------------------------------------------: |
|           Login            | C01-CT01: Login com e-mail e senha válidos    |

|               **Evidência(s)**               |
| :------------------------------------------: |
| [Vídeo](https://jam.dev/c/6ea09cdb-2ff1-402f-ba58-6554ce87dee8)  |

---
#### Bug 04: Não é possível aplicar licença de férias - "No Leave Types with Leave Balance"

| **ID**     | **Descrição**                                                                                                                |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------ |
| BUG-004    | Ao tentar aplicar uma licença no módulo de férias, nenhuma opção de licença é exibida, impossibilitando a solicitação.        |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|        Alta            |           Alta             |   Aberto   |

| **Passo a passo para simular o bug**                     |
| -------------------------------------------------------- |
| 1. Acessar o menu "Leave"                                |
| 2. Clicar em "Apply"                                     |
| 3. Verificar se aparecem tipos de licença disponíveis    |

|                      **Comportamento Esperado**                       |                        **Comportamento Obtido**                         |
| :-------------------------------------------------------------------: | :----------------------------------------------------------------------: |
| Deve-se exibir uma lista de tipos de licença com saldo disponível     | A mensagem "No Leave Types with Leave Balance" é exibida e nada é listado |

| **Ambiente**             |
| ------------------------ |
| Ambiente de homologação. |
| Windows 11 + Microsoft Edge v.136.0 |
| OrangeHRM Demo           |

| **Funcionalidade Afetada** |               **Caso de Teste Relacionado**               |
| :------------------------: | :-------------------------------------------------------: |
|    Férias (Leave Module)   | C04-CT01: Aplicar licença de férias com dados válidos     |

|              **Evidência(s)**              |
| :----------------------------------------: |
| [Vídeo](https://jam.dev/c/ca4c9890-a4b8-4f65-b067-a5ea08f4c26e) |

---
#### Bug 05: Ícone de “ver senha” desaparece ao sair do campo no formulário de criação de funcionário

| **ID**     | **Descrição**                                                                                                                                                  |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-005    | No formulário de criação de funcionário no módulo PIM, o ícone de "ver senha" desaparece ao clicar fora do campo de senha ou confirmação de senha.             |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Alta             |   Aberto   |

| **Passo a passo para simular o bug**                             |
| ---------------------------------------------------------------- |
| 1. Navegar até o módulo "PIM"                                    |
| 2. Clicar em "Add Employee"                                      |
| 3. Marcar a opção "Create Login Details"                         |
| 4. Observar o campo de senha e clique no ícone de visualizar     |
| 5. Clicar fora do campo e tentar clicar novamente no campo senha |

|                      **Comportamento Esperado**                      |                         **Comportamento Obtido**                          |
| :------------------------------------------------------------------: | :------------------------------------------------------------------------: |
| O ícone de "ver senha" deve permanecer visível e funcional           | O ícone desaparece após sair do campo e não retorna, impedindo visualização |

| **Ambiente**             |
| ------------------------ |
| Ambiente de homologação. |
| Windows 11 + Microsoft Edge v.136.0 |
| OrangeHRM Demo           |

| **Funcionalidade Afetada** |            **Caso de Teste Relacionado**             |
| :------------------------: | :--------------------------------------------------: |
| Cadastro de funcionário    | C03-CT01: Criar novo funcionário com dados válidos   |

|               **Evidência(s)**               |
| :------------------------------------------: |
| [Vídeo](mesmol bug) |

---

### 🐞 **Bug 06: Erro de carregamento ao tentar agendar entrevista já agendada**

| **ID**     | **Descrição**                                                                                                                                                        |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-002    | Ao acessar o perfil de um candidato no módulo de Recrutamento e tentar clicar no botão de agendamento de entrevista (já agendada), ocorre um erro de carregamento.   |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                              |
| ----------------------------------------------------------------- |
| 1. Acessar o módulo “Recruitment” (Recrutamento)                  |
| 2. Abrir o perfil de um dos candidatos listados                   |
| 3. Identificar uma entrevista que já está agendada                |
| 4. Clicar no botão para reagendar ou visualizar detalhes da entrevista |
| 5. Observar a falha de carregamento                               |

|                     **Comportamento Esperado**                      |                        **Comportamento Obtido**                        |
| :-----------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve carregar as informações da entrevista agendada       | O botão não responde e/ou gera erro de carregamento, impedindo a ação |

| **Ambiente**             |
| ------------------------ |
| Ambiente de homologação. |
| Desktop com Windows 11.  |
| Microsoft Edge v.136.0    |
| OrangeHRM Demo           |

| **Funcionalidade Afetada** |             **Caso de Teste Relacionado**              |
| :------------------------: | :----------------------------------------------------: |
| Recrutamento de candidatos | C05-CT03: Buscar e interagir com candidatos existentes |

|                    **Evidência(s)**                     |
| :-----------------------------------------------------: |
| [Vídeo](https://jam.dev/c/e2ad5a4e-f82d-45dc-a73f-2eb01942e7b2)      |
