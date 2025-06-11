# 🚀 Teste de Performance Manual – PrestaShop

**Foco:** Velocidade Percebida e Responsividade
**Prioridade:** Alta
**Tipo de Teste:** Manual
**Objetivo:** Avaliar a **velocidade de carregamento percebida** das páginas e a **responsividade das ações principais** no sistema.

---

## 🔧 Ambiente de Testes

* **Navegador (Desktop):** Microsoft Edge 137.0
* **Sistema Operacional:** Windows 11 x86
* **Ferramenta:** DevTools (F12 - Network)
* **Testes complementares:** Simulação de conexão lenta com *Throttling*

---

## ⏱️ Carregamento de Páginas-Chave

### Páginas Testadas:

* Homepage
* Página de Categoria (PLP)
* Página de Produto (PDP)
* Carrinho
* Checkout

| Página       | Velocidade Percebida              | Observações                                                               |
| ------------ | --------------------------------- | ------------------------------------------------------------------------- |
| **Homepage** | ❌ Lenta no primeiro acesso        | Carregamento inicial demorado. Home visivelmente atrasada ao iniciar uso. |
| **PLP**      | ⚠️ Demora inicial, melhora depois | Primeira visita demora, mas após o cache, o carregamento melhora.         |
| **PDP**      | ✅ Boa                             | Carregamento considerado rápido e fluido.                                 |
| **Carrinho** | ✅ Boa                             | Resposta rápida ao abrir e modificar itens.                               |
| **Checkout** | ✅ Fluida                          | Etapas carregam bem, sem travamentos ou lentidão aparente.                |

---

## 📊 Análise com DevTools (Network)

### Procedimentos:

* Cache limpo antes dos testes
* Modo "Disable Cache" ativado
* Métricas observadas: `DOMContentLoaded`, `Load`, tamanhos de arquivos

### Resultados:

* **DOMContentLoaded:** Tempo aceitável na maioria das páginas após o primeiro carregamento
* **Load:** Sem bloqueios pesados após o cache inicial
* **Arquivos grandes:** Algumas imagens e recursos JS pesados na homepage
* **Problemas identificados:**

```plaintext
Access to XMLHttpRequest at 'https://sincere-reaction.demo.prestashop.com/error500.html' 
from origin 'https://demo.prestashop.com' has been blocked by CORS policy: 
No 'Access-Control-Allow-Origin' header is present on the requested resource.
```

```plaintext
host-network-events.js:1 HEAD https://sincere-reaction.demo.prestashop.com/error500.html 
net::ERR_FAILED 502 (Bad Gateway)
```

* **Impacto:** Esses erros podem afetar SEO, desempenho e usabilidade inicial do site.

---

## ⚡ Responsividade de Ações Interativas

| Ação                           | Resultado     | Observação                                                  |
| ------------------------------ | ------------- | ----------------------------------------------------------- |
| Adicionar produto ao carrinho  | ✅ Imediato    | Feedback claro e fluido                                     |
| Aplicar filtros na PLP         | ✅ Rápido      | Produtos atualizam dinamicamente                            |
| Alterar quantidade no carrinho | ✅ Instantâneo | Recalcula preço e atualização visual sem atraso             |
| Etapas do checkout             | ✅ Contínuo    | Navegação suave entre etapas, sem recarregamentos completos |

---

## 🖼️ Impacto de Imagens

* **Imagens otimizadas?** ⚠️ Parcialmente – algumas são pesadas na homepage
* **Testes com rede lenta:**

  * Imagens demoram a carregar visivelmente
  * Há **pequenas quebras de layout** até a renderização completa
* **Observações:** Melhoria recomendada na compactação e carregamento progressivo

---

## 📷 Evidência

![Print de performance com DevTools](https://cdn.discordapp.com/attachments/960636027398160407/1382451620150902784/Captura_de_tela_2025-06-11_170556.png?ex=684b33e6\&is=6849e266\&hm=6518a5f44161885b16b62ec56b59276878e417a24cb121bb22a2edfc37c81ceb&)

---

## ✅ Conclusão

* **Carregamento inicial da homepage é lento**, prejudicando a experiência do primeiro acesso.
* Após o cache, o desempenho melhora consideravelmente nas demais páginas.
* Erros de CORS e Bad Gateway detectados no console precisam de atenção urgente.
* A responsividade das ações (carrinho, filtros, checkout) está **excelente**.
* Algumas **imagens pesadas e não otimizadas** afetam o carregamento perceptível.
* No geral, o sistema apresenta **boa performance após a primeira interação**, mas precisa de **otimizações de primeira carga** e **recursos estáticos**.
