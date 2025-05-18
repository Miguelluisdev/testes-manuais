# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Compartilhamento de projetos com outros usuários
> Sistema: [Demo SaaS](https://demo-saas.bugbug.io/)  
> Autor: Miguel Luis  
> Data: 2025-05-18  

---

## Cenário 07: Compartilhamento de projetos com outros usuários

### Caso de Teste 01: Gerar link público de compartilhamento (Happy Path)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C07-CT01 | O sistema deve permitir gerar um link público para compartilhar o projeto. |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| Usuário autenticado e visualizando um projeto próprio.                  |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela do projeto                                 |
| **E** clicamos na opção "Compartilhar"                                  |
| **QUANDO** selecionamos "Gerar link público"                            |
| **ENTÃO** o sistema deve gerar e exibir o link público para o projeto   |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| Link público é gerado com sucesso e permite acesso de visualização.     |

---

### Caso de Teste 02: Gerar link público com projeto inexistente (Teste Negativo)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C07-CT02 | O sistema deve impedir a geração de link público para projeto inexistente. |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| Usuário autenticado, mas tenta gerar link para projeto inexistente.     |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela de projeto                                |
| **E** tentamos gerar link público para um projeto que não existe        |
| **QUANDO** clicamos em "Gerar link público"                            |
| **ENTÃO** o sistema deve exibir uma mensagem de erro informando projeto inválido |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| Sistema não gera link e exibe mensagem de erro clara.                   |

---

### Caso de Teste 03: Gerar link público com limite máximo de caracteres atingido (Valor Limite)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C07-CT03 | O sistema deve tratar limite máximo no tamanho do link público gerado. |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| Usuário autenticado e tentando gerar link público para projeto.         |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela do projeto                               |
| **E** clicamos em "Gerar link público" repetidamente para tentar ultrapassar o limite |
| **QUANDO** o sistema gera o link                                       |
| **ENTÃO** o link deve estar dentro do limite máximo de caracteres permitido |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| Link gerado respeita o limite de tamanho definido sem truncar ou corromper. |

---

### Caso de Teste 04: Gerar link público para projeto privado com restrições (Caminho Alternativo)

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C07-CT04 | O sistema deve informar que o projeto está privado e solicitar confirmação antes de gerar o link público. |

| **Pré-condições**                                                        |
| :----------------------------------------------------------------------- |
| Usuário autenticado e visualizando um projeto marcado como privado.     |

| **Passos**                                                               |
| :----------------------------------------------------------------------- |
| **DADO** que estamos na tela do projeto privado                        |
| **E** clicamos em "Compartilhar"                                       |
| **QUANDO** selecionamos "Gerar link público"                           |
| **ENTÃO** o sistema exibe aviso sobre privacidade e pede confirmação    |

| **Critérios de aceitação**                                               |
| :----------------------------------------------------------------------- |
| Após confirmação, link é gerado; se cancelar, link não é gerado.        |
