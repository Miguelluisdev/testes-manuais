## 📜 Regras de Negócio do E-commerce

---

### I. 👥 Gerenciamento de Usuários e Acesso

* **Autenticação Obrigatória para Ações Específicas:**

  * Login obrigatório para:

    * Acessar histórico de pedidos
    * Gerenciar endereços
    * Editar informações pessoais
    * Finalizar compras como usuário registrado

* **Unicidade de E-mail:**

  * Cada conta deve ter um e-mail único
  * Não é permitido cadastro duplicado com o mesmo e-mail

* **Critérios de Senha:**

  * Senhas devem atender a requisitos mínimos (ex: comprimento, tipos de caracteres)

* **Recuperação de Conta:**

  * Possível via e-mail cadastrado

* **Checkout como Convidado:**

  * Permitido sem criar conta
  * Informações de contato e endereço são obrigatórias

---

### II. 🛍️ Catálogo e Gerenciamento de Produtos

* **Exibição de Informações do Produto:**

  * Nome, descrição, preço, imagens e status de estoque devem estar visíveis

* **Variações de Produto:**

  * Produtos podem ter variações (ex: cor, tamanho)
  * Variações podem alterar preço, imagem e disponibilidade
  * Seleção de variações obrigatórias antes de adicionar ao carrinho

* **Precificação e Promoções:**

  * Produtos podem exibir:

    * Preço base
    * Preço promocional com valor original riscado

* **Disponibilidade de Estoque:**

  * Status de estoque claramente indicado
  * Produtos fora de estoque:

    * Não podem ser adicionados ao carrinho
    * Ou botão de adicionar é desabilitado

* **Busca e Filtro:**

  * Busca por termos (nome, SKU, descrição)
  * Filtros por:

    * Preço, atributos, marca
    * Ordenação por critérios diversos

* **Avaliações de Produto:**

  * Permitidas para usuários logados ou visitantes (dependendo da configuração)
  * Comentários e avaliações visíveis por produto

---

### III. 🛒 Carrinho de Compras e Processo de Pedido

* **Adição ao Carrinho:**

  * Usuário especifica a quantidade desejada

* **Gerenciamento do Carrinho:**

  * Visualizar, alterar quantidades e remover produtos
  * Recalcular automaticamente subtotal e total após alterações

* **Cupons de Desconto:**

  * Aplicáveis no carrinho
  * Cupons inválidos/expirados não serão aplicados

* **Cálculo do Total do Pedido:**

  * Composição:

    * Subtotal dos produtos
    * * Envio (se aplicável)
    * * Impostos (se aplicável)
    * * Descontos (se aplicável)

* **Informações de Endereço:**

  * Obrigatórias para entrega e cobrança

* **Métodos de Envio:**

  * Vários métodos com custos distintos
  * Influenciam no valor total do pedido

* **Métodos de Pagamento:**

  * Exemplo no demo: “Pay by Check”, “Pay by Bank Wire”

* **Confirmação do Pedido:**

  * Após finalização, o sistema exibe:

    * Número do pedido
    * Resumo da compra

* **Termos de Serviço:**

  * Pode ser necessário aceitar os termos antes de finalizar

---

### IV. 🔐 Gerenciamento de Conta (Pós-Login)

* **Histórico de Pedidos:**

  * Listagem e detalhes dos pedidos realizados

* **Gerenciamento de Endereços:**

  * Adicionar, editar e excluir múltiplos endereços

* **Informações Pessoais:**

  * Atualização de nome, e-mail e senha

---

### V. 🌐 Conteúdo e Interação Geral

* **Internacionalização:**

  * Suporte a múltiplos idiomas e moedas

* **Newsletter:**

  * Inscrição por e-mail

* **Páginas de Conteúdo (CMS):**

  * Informações como:

    * Sobre Nós
    * Termos de Uso
    * Política de Privacidade
    * Contato

* **Formulário de Contato:**

  * Envio de mensagens
  * Requer campos válidos
