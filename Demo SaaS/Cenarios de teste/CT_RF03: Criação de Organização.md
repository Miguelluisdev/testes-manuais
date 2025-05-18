# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Criação de uma organização após o cadastro  
> Sistema: [Demo SaaS](https://demo-saas.bugbug.io/)  
> Autor: Miguel Luis  
> Data: 2025-05-18  

---

## Cenário 03: Criação de uma organização após o cadastro

### Caso de Teste 01: Criar organização com nome válido (Happy Path)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C03-CT01 | O sistema deve permitir criar uma organização com nome válido.     |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| O usuário deve ter concluído o cadastro e estar na tela de criação de organização. |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela de criação de organização                    |
| **E** inserimos um nome válido no campo "Organization Name"              |
| **QUANDO** clicamos no botão "Create"                                    |
| **ENTÃO** a organização deve ser criada e o usuário redirecionado ao Dashboard |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| A organização deve ser criada com sucesso e o sistema deve prosseguir para o próximo fluxo. |

### Caso de Teste 02: Tentar criar organização sem nome (Teste Negativo)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C03-CT02 | O sistema deve impedir a criação de uma organização sem nome.      |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| O usuário deve estar na tela de criação de organização.                 |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela de criação de organização                    |
| **E** deixamos o campo "Organization Name" em branco                     |
| **QUANDO** clicamos no botão "Create"                                    |
| **ENTÃO** o sistema deve exibir uma mensagem de erro solicitando o preenchimento do campo |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| O campo obrigatório deve ser validado e o sistema não deve prosseguir até o preenchimento correto. |

### Caso de Teste 03: Nome da organização com 1 caractere (Valor Limite)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C03-CT03 | O sistema deve permitir nomes curtos válidos para a organização.    |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| O usuário deve estar na tela de criação de organização.                 |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela de criação de organização                    |
| **E** inserimos um nome de organização com apenas 1 caractere válido     |
| **QUANDO** clicamos no botão "Create"                                    |
| **ENTÃO** o sistema deve aceitar e criar a organização normalmente       |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| O sistema deve aceitar valores mínimos válidos no campo "Organization Name". |

### Caso de Teste 04: Criação de organização com configuração extra marcada (Caminho Alternativo)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C03-CT04 | O sistema deve permitir a criação da organização com opções adicionais marcadas. |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| O usuário deve estar na tela de criação de organização.                 |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela de criação de organização                    |
| **E** inserimos um nome válido                                            |
| **E** marcamos a checkbox de configuração extra                          |
| **QUANDO** clicamos no botão "Create"                                    |
| **ENTÃO** a organização deve ser criada com as configurações adicionais aplicadas |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| O sistema deve registrar corretamente a criação da organização com as configurações extras. |


