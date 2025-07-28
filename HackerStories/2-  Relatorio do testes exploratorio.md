## 📋 Relatório de Testes Exploratórios com Heurísticas — HackerNews Clone

**🔗 URL:** [https://hackernews-seven.vercel.app/](https://hackernews-seven.vercel.app/)
**📆 Data:** 28/07/2025
**👤 Responsável:** Miguel Luis
**🔍 Tipo de teste:** Exploratório baseado em Heurísticas de Usabilidade
**🎯 Público-alvo:** Desenvolvedores que buscam artigos, livros e recursos técnicos

---

### 📈 Resultados Lighthouse

![Lighthouse Score](attachment)

| Métrica           | Pontuação |
| ----------------- | --------- |
| ⚡ Desempenho      | 85        |
| ♿ Acessibilidade  | **100** ✅ |
| 🛠️ Boas Práticas | 78        |
| 🔍 SEO            | 82        |

---

### ✅ Resultados Gerais dos Testes

| Categoria          | Resultado                                                                |
| ------------------ | ------------------------------------------------------------------------ |
| 🐞 Bugs críticos   | **Nenhum bug funcional foi encontrado**                                  |
| 📱 Responsividade  | **Inconsistências visuais em dispositivos móveis e tamanhos menores**    |
| 👁️ UX/UI          | **Graves problemas de experiência de uso identificados por heurísticas** |
| 🎨 Estética/Design | Interface considerada pouco atrativa e visualmente pobre                 |
| 🧭 Navegação       | Funcional, mas sem feedback adequado e controle de fluxo claro           |
| 🔗 Links/Conteúdo  | Links funcionam e direcionam corretamente para conteúdos externos        |

---

### 🔍 Problemas e Melhorias Identificadas com Base em Heurísticas

| Heurística                            | Observação                                                                              | Impacto |
| ------------------------------------- | --------------------------------------------------------------------------------------- | ------- |
| 1. Visibilidade do status do sistema  | **Falta feedback visual ao carregar mais itens (scroll)**                               | Alto    |
| 3. Controle e liberdade do usuário    | **Usuário não tem opção clara de voltar ao topo ou navegar por seções**                 | Médio   |
| 4. Consistência e padrões             | Alguns estilos visuais parecem desconectados ou inconsistentes entre componentes        | Médio   |
| 5. Prevenção de erros                 | Sistema não possui entradas do usuário, mas não lida bem com falha de rede              | Médio   |
| 7. Flexibilidade e eficiência de uso  | Interface não apresenta atalhos, filtros ou ordenação de conteúdo                       | Médio   |
| 8. Estética e design minimalista      | **Layout visualmente pobre, pouco atrativo, impacta negativamente a experiência geral** | Alto    |
| 9. Diagnóstico e recuperação de erros | Ausência de mensagens claras ao simular falha de rede                                   | Médio   |

---

### 📱 Responsividade

* Em resoluções pequenas (ex: 360x640), os elementos se sobrepõem ou ficam espremidos.
* Scroll vertical excessivo sem divisão de seções.
* Falta de media queries refinadas para ajuste de layout.

---

### 📝 Conclusão

Embora o site **tenha ótimo desempenho técnico**, com **100 em acessibilidade** e **links funcionais**, ele **peca fortemente na experiência do usuário**, com **problemas graves de usabilidade, estética e navegação**, especialmente para o **público-alvo (desenvolvedores)** que valorizam clareza, praticidade e design limpo.

---

### ✅ Sugestões de Melhoria

* ✅ Adicionar feedback visual ao carregar itens (ex: spinner ou mensagem de carregando).
* ✅ Criar botão “voltar ao topo”.
* ✅ Melhorar o layout e paleta de cores para tornar o site mais atrativo.
* ✅ Reorganizar o conteúdo em seções visuais (ex: "Livros", "Tutoriais", "Artigos").
* ✅ Ajustar o layout para melhor responsividade em mobile.
* ✅ Exibir mensagens amigáveis quando a conexão falha.

---

Se quiser, posso transformar esse conteúdo em **Markdown** para publicação no GitHub/portfólio. Deseja que eu gere esse arquivo?

