# 🔐 Teste de Segurança Manual – PrestaShop

**Foco:** Navegabilidade e Dados Visíveis
**Prioridade:** Alta
**Tipo de Teste:** Manual
**Objetivo:** Verificar **aspectos básicos de segurança perceptíveis ao usuário** durante a navegação.

---

## 🔧 Ambiente de Testes

* **Navegador (Desktop):** Microsoft Edge 137.0
* **Sistema Operacional:** Windows 11 x86
* **Mobile:** Motorola com Chrome (versão não especificada)

---

## 🔍 Itens Avaliados

### 🔒 HTTPS

| Verificação                                       | Resultado |
| ------------------------------------------------- | --------- |
| Todas as páginas críticas são servidas via HTTPS? | ✅ Sim     |
| Cadeado visível na barra de endereço?             | ✅ Sim     |

---

### 🔗 Dados Sensíveis na URL

| Verificação                                                         | Resultado |
| ------------------------------------------------------------------- | --------- |
| Nenhuma informação sensível visível na URL após login ou navegação? | ✅ Sim     |

---

### 👁️ Mascaramento de Senhas

| Verificação                                             | Resultado |
| ------------------------------------------------------- | --------- |
| Campos de senha estão com caracteres mascarados (••••)? | ✅ Sim     |

---

### 💾 Autocompletar Senhas

| Verificação                                                                                     | Resultado                      |
| ----------------------------------------------------------------------------------------------- | ------------------------------ |
| Navegador oferece salvar senha?                                                                 | ✅ Sim                          |
| Atributos de autocomplete estão sendo usados corretamente? (`current-password`, `new-password`) | ✅ Sim verificado no devtools |

---

### 🔐 Gerenciamento de Sessão

| Cenário                                                          | Resultado                                                                              |
| ---------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Após logout, acessar diretamente URL da área logada é bloqueado? | ✅ Sim                                                                                  |
| Fechar e reabrir navegador mantém sessão ativa ou força login?   | ✅ Sessão mantida                                                                       |
| Política de sessão condiz com o esperado?                        | ⚠️ Depende do contexto de segurança do projeto (sessão persistente pode ser aceitável) |

---

### ⚠️ Exposição de Mensagens de Erro

| Verificação                                                      | Resultado                                    |
| ---------------------------------------------------------------- | -------------------------------------------- |
| Mensagens de erro são genéricas e não revelam detalhes técnicos? | ✅ Sim – Nenhuma mensagem crítica foi exposta |

---

## ❗ Comportamento Inseguro Encontrado

* **Cenário Crítico:**

  * Ao tentar adicionar um item à **lista de desejos** sem estar logado, o sistema corretamente solicita o login.
  * **Porém**, ao prosseguir e **enviar o item para o carrinho**, o sistema permite o acesso ao **checkout completo**, mesmo **sem conta criada/logada**.
  * Esse fluxo permite que um **usuário deslogado** adicione produtos e acesse a **etapa de finalização de compra**, o que pode causar:

    * Falhas em integração com gateways de pagamento
    * Problemas de rastreabilidade e segurança da transação
    * Abertura de brechas para exploração

---

## ✅ Conclusão

* Os itens básicos de **segurança visível ao usuário estão corretamente implementados** (HTTPS, mascaramento, URLs limpas, feedback genérico).
* **Ponto crítico identificado:** fluxo inseguro ao interagir com a lista de desejos e carrinho sem autenticação.

  * **Recomendação:** Forçar verificação de login **antes** de liberar acesso ao carrinho e ao checkout.
* A sessão mantida após fechar o navegador pode ser aceitável, mas é importante revisar conforme as **políticas de segurança definidas para o sistema.**

