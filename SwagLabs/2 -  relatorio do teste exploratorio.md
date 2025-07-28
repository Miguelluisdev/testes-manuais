## 🧪 Relatório de Testes Exploratórios — Swag Labs

**URL:** [https://www.saucedemo.com/v1/index.html](https://www.saucedemo.com/v1/index.html)
**Data:** 28/07/2025
**Responsável:** Miguel Luis

---

### 🔍 Resultados Gerais

| Área                                    | Resultado                                                            |
| --------------------------------------- | -------------------------------------------------------------------- |
| ✅ Login                                 | Funcionando normalmente para usuários válidos                        |
| 🔐 Usuário travado (locked\_out\_user)  | Bloqueado corretamente                                               |
| 🧪 Usuário problemático (problem\_user) | Login OK, porém **imagens não carregam corretamente**                |
| 🛒 Processo de Compra                   | Funciona, mas **produto permanece no carrinho após finalização**     |
| 👁️‍🗨️ Usabilidade                     | Navegação fácil e rápida                                             |
| 📱 Responsividade                       | Funciona bem em geral, mas **quebra em alguns tamanhos específicos** |
| ⚙️ Performance (Lighthouse)             | Desempenho **muito bom**                                             |

---

### 📝 Observações Detalhadas

#### 🔐 Login

* Login funcional para `standard_user`.
* **Sugestão de melhoria:** o ícone de exibir senha desaparece ao retirar o mouse. O ideal seria que o ícone permanecesse visível até o usuário desativar manualmente.

#### 🛒 Checkout

* Processo completo de compra é realizado com sucesso.
* **Bug encontrado:** após finalizar a compra, o produto **não é removido automaticamente do carrinho**, o que pode confundir o usuário.

#### 📷 Imagens (problem\_user)

* Ao utilizar o usuário `problem_user`, algumas **imagens de produtos não são exibidas corretamente**.

#### 📱 Responsividade

* Quebra visual em alguns dispositivos com tamanhos intermediários. Layout desalinhado ou colunas comprimidas.
* Pode ser melhorado com uso de media queries adicionais.

---

### 📊 Relatório Lighthouse (DevTools)

| Métrica          | Pontuação                 |
| ---------------- | ------------------------- |
| ⚡ Desempenho     | 82                        |
| ♿ Acessibilidade | 57 (**ponto de atenção**) |
| ✔️ Boas práticas | 78                        |
| 🔍 SEO           | 83                        |

**Observação:** A **acessibilidade (57)** é o ponto mais fraco, indicando oportunidades de melhoria em contraste, navegação por teclado, atributos alt, entre outros.

---

### ✅ Conclusão

O site **Swag Labs** apresenta uma experiência geral sólida, com boa performance e fluxo funcional. Porém, foram identificados **pontos de melhoria e inconsistências**, principalmente:

* 🐞 **Bug:** Carrinho não é esvaziado após a compra;
* ♿ **Acessibilidade:** Pontuação baixa no Lighthouse (57);
* 🖼️ **Imagens quebradas** para usuários específicos;
* 🖱️ **Usabilidade do botão de senha** pode ser refinada;
* 📱 **Responsividade quebrando** em alguns tamanhos de tela.
