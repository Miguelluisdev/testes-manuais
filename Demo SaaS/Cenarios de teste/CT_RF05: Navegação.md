# 🧪 Plano de Testes Manuais - Demo SaaS  
> Funcionalidade: Navegar pelas seções principais da plataforma  
> Sistema: [Demo SaaS](https://demo-saas.bugbug.io/)  
> Autor: Miguel Luis  
> Data: 2025-05-18  

---

## Cenário 05: Navegar pelas seções principais da plataforma

### Caso de Teste 01: Navegar entre as páginas principais com sucesso (Happy Path)

| ID       | Descrição                                                                       |
| :------- | :------------------------------------------------------------------------------ |
| C05-CT01 | O usuário deve conseguir navegar entre Dashboard, Projetos, Execução e Configurações. |

| **Pré-condições**                                                       |
| :---------------------------------------------------------------------- |
| O usuário deve estar autenticado e visualizando a interface principal. |

| **Passos**                                                              |
| :---------------------------------------------------------------------- |
| **DADO** que estamos na interface principal do sistema                  |
| **QUANDO** clicarmos nos links "Dashboard", "Projetos", "Execução" e "Configurações" |
| **ENTÃO** devemos ser redirecionados corretamente para cada uma dessas seções |

| **Critérios de aceitação**                                              |
| :---------------------------------------------------------------------- |
| A navegação entre seções deve ser rápida e fluida, com carregamento correto de conteúdo. |

### Caso de Teste 02: Acessar link quebrado no menu (Teste Negativo)

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C05-CT02 | O sistema deve exibir erro apropriado se algum link do menu estiver indisponível. |

| **Pré-condições**                                               |
| :-------------------------------------------------------------- |
| O usuário deve estar autenticado.                               |

| **Passos**                                                      |
| :-------------------------------------------------------------- |
| **DADO** que clicamos em um link do menu                       |
| **E** o link está com rota incorreta ou página fora do ar       |
| **QUANDO** o sistema tentar carregar a página                   |
| **ENTÃO** uma mensagem de erro ou página 404 deve ser exibida   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve lidar com erros de navegação sem travar a aplicação. |

### Caso de Teste 03: Verificar responsividade dos ícones e links de navegação (Valor Limite / UI)

| ID       | Descrição                                                                       |
| :------- | :------------------------------------------------------------------------------ |
| C05-CT03 | O sistema deve manter a funcionalidade dos menus em resolução mínima (mobile). |

| **Pré-condições**                                                    |
| :------------------------------------------------------------------- |
| O usuário deve estar autenticado e acessando via dispositivo móvel. |

| **Passos**                                                           |
| :------------------------------------------------------------------- |
| **DADO** que estamos acessando o sistema em um dispositivo móvel     |
| **QUANDO** abrimos o menu lateral ou navegação reduzida              |
| **ENTÃO** os links e ícones devem estar acessíveis e funcionais      |

| **Critérios de aceitação**                                           |
| :------------------------------------------------------------------- |
| A navegação deve ser responsiva e usável mesmo em telas menores.     |

### Caso de Teste 04: Utilizar atalho via teclado para navegação (Caminho Alternativo)

| ID       | Descrição                                                                |
| :------- | :------------------------------------------------------------------------ |
| C05-CT04 | O usuário pode utilizar atalhos de teclado (se aplicável) para navegação.|

| **Pré-condições**                                                |
| :--------------------------------------------------------------- |
| O sistema deve suportar atalhos de teclado (caso disponíveis).   |

| **Passos**                                                       |
| :--------------------------------------------------------------- |
| **DADO** que estamos na tela principal                           |
| **QUANDO** pressionamos atalhos como `Alt + D` para "Dashboard" |
| **ENTÃO** devemos ser redirecionados corretamente para a seção correspondente |

| **Critérios de aceitação**                                       |
| :--------------------------------------------------------------- |
| Os atalhos devem funcionar corretamente e melhorar a acessibilidade. |

