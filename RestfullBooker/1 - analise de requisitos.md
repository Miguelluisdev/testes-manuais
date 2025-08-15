# 📖 Análise de Requisitos – Site BookCart

## 1. Visão Geral do Sistema
O **BookCart** é uma aplicação web de e-commerce simplificada, focada na venda de livros.  
A plataforma permite que usuários naveguem por um catálogo de livros, pesquisem por títulos específicos, gerenciem um carrinho de compras e uma lista de desejos, e finalizem uma compra.  

O sistema possui:  
- **Áreas públicas** (acessíveis a todos).  
- **Áreas restritas** (que exigem autenticação).  

---

## 2. Perfis de Usuário (Atores)
- **Usuário Visitante (Não Autenticado):** qualquer pessoa que acesse o site sem login.  
- **Usuário Registrado (Autenticado):** usuário que criou uma conta e está logado.  

---

## 3. Requisitos Funcionais (RF)

### **RF01: Gestão de Contas de Usuário**
#### RF01.1 - Registro de Novo Usuário
- Registrar novo usuário com: Primeiro Nome, Sobrenome, Nome de Usuário, Senha, Confirmação de Senha e Gênero.  
- Nome de Usuário deve ser único.  
- Senha e Confirmação de Senha devem coincidir.  
- Exibir mensagens de erro quando necessário.  
- Após sucesso, redirecionar para página de **Login**.  

#### RF01.2 - Login de Usuário
- Login com Nome de Usuário e Senha.  
- Sucesso → redirecionar para catálogo de livros.  
- Atualizar cabeçalho com: `Meus Pedidos`, `Lista de Desejos` e `Logout`.  
- Falha → mensagem de erro clara.  

#### RF01.3 - Logout de Usuário
- Usuário logado deve ter opção de **Logout**.  
- Logout → encerrar sessão e redirecionar para página inicial como visitante.  

---

### **RF02: Catálogo e Visualização de Livros**
#### RF02.1 - Listagem de Livros
- Página principal deve listar todos os livros.  
- Cada livro exibe: capa, título, autor e preço.  
- Botões: `Adicionar ao Carrinho` e `Adicionar à Lista de Desejos`.  

#### RF02.2 - Pesquisa de Livros
- Barra de pesquisa no topo da página.  
- Filtrar livros por título em **tempo real**.  
- Ao limpar campo → lista completa reexibida.  

#### RF02.3 - Filtragem por Categoria
- Filtro de categorias (ex: *Biography*, *Fiction*, *Mystery*).  
- Exibir apenas livros da categoria selecionada.  

---

### **RF03: Carrinho de Compras**
#### RF03.1 - Adicionar Livro ao Carrinho
- Visitantes → redirecionados para página de **Login**.  
- Usuários logados → item adicionado ao carrinho.  
- Exibir notificação de sucesso (toast).  
- Ícone do carrinho deve atualizar contagem.  
- Botão muda para `Adicionado ao Carrinho`.  

#### RF03.2 - Visualização do Carrinho
- Página deve listar: capa, título, quantidade, preço unitário.  
- Exibir preço total.  

#### RF03.3 - Gerenciamento do Carrinho
- Alterar quantidade de itens.  
- Remover item do carrinho.  
- Total recalculado automaticamente.  

#### RF03.4 - Limpar Carrinho
- Opção para remover **todos os itens** de uma vez.  

---

### **RF04: Lista de Desejos (Wishlist)**
#### RF04.1 - Adicionar à Lista de Desejos
- Apenas usuários logados podem adicionar itens.  
- Ao clicar no coração → item adicionado.  
- Exibir notificação de sucesso.  

#### RF04.2 - Visualização e Gerenciamento da Lista de Desejos
- Acessar pelo menu do usuário.  
- Listar todos os itens.  
- Remover item da lista.  
- Mover item da lista para o carrinho.  

---

### **RF05: Checkout e Pedidos**
#### RF05.1 - Finalizar Compra (Checkout)
- Botão `Checkout` na página do carrinho → redireciona para finalização.  
- Solicitar informações de entrega: Nome, Endereço (linha 1 e 2), CEP, Estado.  
- Botão `Fazer Pedido` (Place Order).  

#### RF05.2 - Confirmação do Pedido
- Ao confirmar pedido:  
  - Pedido é processado.  
  - Carrinho é esvaziado.  
  - Redirecionar para `Meus Pedidos`.  
  - Exibir mensagem de sucesso.  

#### RF05.3 - Histórico de Pedidos
- Acessar página `Meus Pedidos` via menu.  
- Listar todos os pedidos já realizados.  
- Exibir: ID do Pedido, Data, Título do Livro, Preço.  

---

## 4. Requisitos Não Funcionais (RNF)

### RNF01 - Usabilidade
- Interface intuitiva e simples.  
- Mensagens de feedback claras e visíveis.  
- Fluxo de compra deve ser direto.  

### RNF02 - Desempenho
- Páginas devem carregar em até **3 segundos**.  
- Resposta da busca e filtros deve ser rápida.  
- Ações como adicionar ao carrinho devem ser instantâneas.  

### RNF03 - Compatibilidade
- Compatível com: Chrome, Firefox, Edge.  
- Layout responsivo (desktop, tablet e mobile).  

### RNF04 - Segurança
- Senhas devem ser armazenadas com **hash**.  
- Sessões devem ser seguras contra acessos indevidos.  
- Páginas restritas não devem ser acessíveis sem login.  

### RNF05 - Confiabilidade
- Erros tratados com mensagens amigáveis.  
- Contagem de itens no carrinho e totais sempre corretos.  

---

## 5. Como Usar Esta Análise para Testes Manuais

### Criar Casos de Teste
Para cada requisito funcional, crie **casos de teste**.

**Exemplo RF01.1 (Registro):**  
- **CT01 (Positivo):** Registro com dados válidos.  
- **CT02 (Negativo):** Nome de usuário já existente.  
- **CT03 (Negativo):** Senhas não coincidem.  
- **CT04 (Validação):** Campos obrigatórios em branco.  

### Testar Fluxos Completos
- **Fluxo 1:** Registro → Login → Pesquisa de livro → Adicionar ao Carrinho → Checkout → Fazer Pedido → Verificar em `Meus Pedidos` → Logout.  
- **Fluxo 2:** Login → Adicionar à Lista de Desejos → Mover para Carrinho → Remover item.  

### Verificar Requisitos Não Funcionais
- Abrir site em navegadores diferentes.  
- Testar responsividade em dispositivos móveis.  
- Avaliar tempo de carregamento e velocidade das ações.  


✅ Esta análise servirá como **guia sólido** para execução de testes manuais completos e eficientes no **BookCart**.

