# ✅ Teste de Usabilidade – PrestaShop

**Prioridade:** Altíssima
**Tipo de Teste:** Manual
**Objetivo:** Avaliar a **facilidade de uso**, **intuitividade**, **clareza da navegação**, **consistência visual** e **responsividade** da aplicação.

---

## 🔧 Ambiente de Testes

* **Desktop:**

  * Navegador: Microsoft Edge 137.0
  * Sistema Operacional: Windows 11 x86

* **Mobile:**

  * Dispositivo: Motorola (modelo não especificado)
  * Navegador: Chrome Mobile
  * *Versões exatas dos navegadores não anotadas*

---

## 🔍 Abordagem

### 🧭 Navegação Geral

| Item                                                       | Resultado                                                     |
| ---------------------------------------------------------- | ------------------------------------------------------------- |
| Os menus são fáceis de entender e usar?                    | ✅ Sim                                                         |
| Os links são descritivos?                                  | ✅ Sim                                                         |
| Os breadcrumbs são precisos e úteis?                       | ✅ Sim                                                         |
| O logo sempre leva à homepage?                             | ✅ Sim                                                         |
| Os links no rodapé funcionam e levam aos lugares corretos? | ✅ Sim – Todos funcionaram corretamente                        |
| Navegação direta pela URL possui proteção?                 | ✅ Sim – Testes indicaram proteção ativa contra URLs inválidas |

---

### 🎨 Consistência Visual

| Item                                                   | Resultado                                                                                                  |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| Fontes, cores, botões e ícones são consistentes?       | ⚠️ Parcial – Algumas inconsistências devido à **falta de tradução**                                        |
| Espaçamento e alinhamento agradáveis e organizados?    | ✅ Sim – Layout bem distribuído [🖼️ Evidência JAM](https://jam.dev/c/5f1800ff-0d98-48d0-a977-2964f35acc16) |
| Descrição de produtos, políticas e filtros traduzidos? | ❌ Não – Alguns textos permanecem em inglês mesmo após mudança de idioma                                    |
| Conversão de moeda para o país configurado?            | ❌ Não – Preços permanecem em moeda padrão (ex: dólar/euro)                                                 |
| PDF gerado com dados do usuário está correto?          | ✅ Sim                                                                                                      |
| Link JAM de evidência visual                           | [🔗 JAM](https://jam.dev/c/a329e0a0-cbb4-45d9-b73b-2ec9125f86e2)                                           |

---

### 🗨️ Clareza e Feedback

| Item                                                                | Resultado                                             |
| ------------------------------------------------------------------- | ----------------------------------------------------- |
| CTAs como "Adicionar ao Carrinho", "Comprar" são claros e visíveis? | ✅ Sim                                                 |
| Há feedback para ações do usuário?                                  | ✅ Sim – Mensagens de sucesso/erro exibidas claramente |
| Textos são legíveis e compreensíveis?                               | ✅ Sim – Linguagem acessível e clara                   |

---

### 📱 Responsividade

| Item                                                                   | Resultado                                                                                       |
| ---------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Layout se adapta corretamente em dispositivos móveis?                  | ⚠️ Parcial – Funcionamento geral bom, mas com **quebra de layout** em tablets                   |
| Menu hambúrguer visível e funcional no mobile?                         | ❌ Não – **Menu invisível** mas funcional via clique                                             |
| Grid de produtos se comporta bem em todas dimensões?                   | ⚠️ Não totalmente – Quebra em algumas larguras intermediárias                                   |
| Comportamento ao deixar o site aberto no celular por tempo e retornar? | ❌ Erro detectado – Site apresenta falha ao retomar após o celular ser bloqueado automaticamente |

---

## ✅ Conclusão

* **Testes executados e refeitos**, forçando tanto caminhos de sucesso quanto de falha.
* A aplicação, em geral, se mostra **intuitiva, responsiva e clara**, com foco na **experiência do usuário**.
* **Principais problemas encontrados:**

  * **Falta de tradução** em textos de produtos, filtros e políticas
  * **Conversão de moeda não aplicada**
  * **Menu invisível no mobile (erro grave)**
  * **Quebra de grid** em resoluções intermediárias
  * **Falha de recuperação ao retornar ao app após bloqueio automático do celular**

---

### 📌 Recomendações

* Corrigir problemas de **internacionalização** (i18n) e tradução automática
* Garantir que a **conversão de moeda** esteja atrelada à seleção de país
* Ajustar **responsividade no grid** para tablets
* Corrigir o problema de **visibilidade do menu hambúrguer**
* Investigar e corrigir o **erro ao retornar ao site após bloqueio automático do celular**
