## 🧪 Plano de Testes Baseado em Heurísticas — HackerNews Clone

**URL:** [https://hackernews-seven.vercel.app/](https://hackernews-seven.vercel.app/)
**Tipo de Teste:** Exploratório com foco em **Heurísticas de Usabilidade e Qualidade de Software**
**Responsável:** Miguel Luis
**Data:** 28/07/2025

---

### 🎯 Objetivo

Explorar o site usando **heurísticas conhecidas de design e usabilidade** para identificar problemas de experiência do usuário, erros visuais, comportamentos inesperados, dificuldades de navegação e falhas de acessibilidade.

---

### 🔎 Heurísticas utilizadas como base

Baseado nas **10 Heurísticas de Usabilidade de Jakob Nielsen**, adaptadas para contexto web:

| #  | Heurística                                                        | Como será aplicada                                             |
| -- | ----------------------------------------------------------------- | -------------------------------------------------------------- |
| 1  | **Visibilidade do status do sistema**                             | O site informa o que está carregando? Feedback visual?         |
| 2  | **Correspondência entre sistema e mundo real**                    | Termos e rótulos fazem sentido para o usuário comum?           |
| 3  | **Controle e liberdade do usuário**                               | Há como desfazer ações? O usuário se sente no controle?        |
| 4  | **Consistência e padrões**                                        | Os elementos seguem padrões visuais e comportamentais?         |
| 5  | **Prevenção de erros**                                            | O sistema evita ações incorretas ou entradas inválidas?        |
| 6  | **Reconhecimento em vez de memorização**                          | Navegação fácil, menus e estrutura previsível?                 |
| 7  | **Flexibilidade e eficiência de uso**                             | Funciona bem para iniciantes e usuários avançados?             |
| 8  | **Estética e design minimalista**                                 | Interface limpa, sem poluição visual ou excesso de informação? |
| 9  | **Ajudar o usuário a reconhecer, diagnosticar e recuperar erros** | Mensagens de erro são claras e orientativas?                   |
| 10 | **Ajuda e documentação**                                          | Existe alguma documentação ou orientação visível no site?      |

---

### 🧭 Escopo dos Testes

* Página principal (lista de notícias)
* Campo de busca (se aplicável)
* Links de notícias
* Comportamento da rolagem infinita ou paginação
* Responsividade (telas menores)
* Feedback visual ao carregar dados
* Experiência de navegação e acessibilidade

---

### 🔍 Charter Exploratório com Heurísticas

| Charter | Explorar o comportamento da homepage com base nas heurísticas                                                   |
| ------- | --------------------------------------------------------------------------------------------------------------- |
| Meta    | Avaliar se a página oferece uma experiência agradável, clara e sem erros, conforme boas práticas de usabilidade |

**Áreas a explorar:**

* O site indica quando está carregando novas notícias? (Heurística 1)
* Os títulos e rótulos dos elementos são compreensíveis? (Heurística 2)
* O usuário pode retornar ao topo facilmente? (Heurística 3)
* Os elementos da UI têm padrão visual e são consistentes entre si? (Heurística 4)
* É possível causar erros? (Heurística 5)
* É fácil identificar quais links foram clicados? (Heurística 6)
* O design funciona em telas pequenas? (Heurística 7 + responsividade)
* O site tem boa estética? Não é poluído? (Heurística 8)
* Em caso de erro (ex: rede desconectada), há mensagem clara? (Heurística 9)
* Existe alguma forma de ajuda ou instrução (ex: placeholder explicativo)? (Heurística 10)

---

### 📋 Roteiro de Execução Sugerido

1. **Acessar a página inicial:** avaliar clareza, carregamento, títulos, e feedback de sistema.
2. **Clicar em links de notícias:** eles abrem? Abrem na mesma aba ou nova?
3. **Simular internet offline e atualizar:** feedback ou página quebrada?
4. **Abrir em celular (modo responsivo):** layout quebra? Elementos sumindo?
5. **Verificar comportamento de rolagem:** há carregamento infinito? Feedback visual?
6. **Testar com leitor de tela (ou inspecionar com ferramentas como axe):** navegação acessível?

---

### 📌 Ferramentas úteis

* **DevTools > Lighthouse** (para performance, acessibilidade, SEO)
* **axe DevTools** (extensão para ver problemas de acessibilidade)
* **Responsively App** ou modo "Mobile" do navegador
* **Ferramentas de rede** para simular lentidão e quedas

---

### ✅ Registro de Descobertas (Modelo)

| Tipo              | Descrição                                                             |
| ----------------- | --------------------------------------------------------------------- |
| 🐞 Bug            | Notícia abre na mesma aba, impedindo voltar ao site                   |
| ⚠️ UX             | Ausência de feedback de carregamento ao rolar a página                |
| 💡 Ideia          | Adicionar botão de “voltar ao topo”                                   |
| 🤯 Erro           | Desconectar a internet resulta em tela em branco sem mensagem de erro |
| 📱 Responsividade | Layout quebra em dispositivos com resolução 360x640                   |

---

### 📌 Conclusão

Esse plano usa heurísticas para **avaliar a qualidade da experiência do usuário além do funcional**, identificando falhas de comunicação, design, acessibilidade e navegação. Ideal para testes exploratórios com foco em **UX e valor para o usuário final**.
