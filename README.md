# Projeto VemSerTech - Ifood: Documentação de Diagrama de Entidade e Relacionamento (DER) #

---

## Introdução

Olá, pessoal! Este é o meu terceiro projeto, o "VemSerTech - Ifood", um e-commerce especializado em eletrodomésticos. Neste documento, vou compartilhar a documentação completa do Diagrama de Entidade e Relacionamento (DER) que desenvolvi para este projeto emocionante.

### Ferramenta Utilizada

Para criar o DER, escolhi a ferramenta **StarUML**. Esta aplicação de modelagem UML (Unified Modeling Language) oferece recursos avançados para criar diagramas e foi essencial na representação visual da estrutura de dados do meu e-commerce.

- **StarUML:** [https://staruml.io/](https://staruml.io/)

## Diagrama de Entidade e Relacionamento (DER) - Eletrodomésticos.

### [Imagem do Diagrama aqui]

## Detalhes das Entidades

Vamos mergulhar nos detalhes de cada entidade, destacando as características específicas relacionadas aos nossos eletrodomésticos.

### Usuário
- **Atributos:** UserID (PK), Nome, Endereço, Email, Senha, Nv Acesso.

### Pedido
- **Atributos:** PedidoID (PK), UserID (FK), Data Pedido, Status Pedido, Total Pedido, Data Compra, Método Pagto, End. Entrega, Status Entrega.

### Produto
- **Atributos:** ProdutoID (PK), Nome, Descrição, Preço, Fabricante, Especificações.

### Categoria
- **Atributos:** CategoriaID (PK), Nome, Descrição, Imagem.

### Avaliação
- **Atributos:** AvaliacaoID (PK), UserID (FK), ProdutoID (FK), Nota, Comentário.

### Carrinho
- **Atributos:** CarrinhoID (PK), UserID (FK), ProdutoID (FK), Quantidade, Subtotal.

### Cupom
- **Atributos:** CupomID (PK), Desconto, Expiração, Ativo.

### Compra
- **Atributos:** CompraID (PK), PedidoID (FK), End. Entrega, Data Compra, Total Compra.

### Promoção
- **Atributos:** PromoçãoID (PK), Nome, Descrição, PercentualDesc, Data Início, Data Fim.

### Fabricante
- **Atributos:** FabricanteID (PK), Nome, ...

### Opinião
- **Atributos:** OpiniaoID (PK), UserID (FK), Texto, Data.

### Cashback
- **Atributos:** CashbackID (PK), UserID (FK), Valor, Data.

### Entrega
- **Atributos:** EntregaID (PK), PedidoID (FK), Data, Status, Método, Endereço.

## Relacionamentos

Agora, vamos explorar os relacionamentos que unem nossas entidades e proporcionam a experiência completa de compras em nosso e-commerce de eletrodomésticos.

1. **Usuário e Pedido:**
   - **Descrição:** Cada pedido está associado a um único usuário, representando quem fez o pedido em nosso e-commerce de eletrodomésticos.
   - **Cardinalidade:** 1:N (um usuário pode realizar zero ou muitos pedidos).

2. **Pedido e Produto:**
   - **Descrição:** Cada pedido pode conter um ou muitos produtos de eletrodomésticos, refletindo os itens adquiridos em um pedido.
   - **Cardinalidade:** M:N (muitos produtos de eletrodomésticos podem estar em muitos pedidos).

3. **Produto e Categoria:**
   - **Descrição:** Cada produto de eletrodoméstico pode pertencer a uma ou muitas categorias, organizando os itens por tipo.
   - **Cardinalidade:** M:N (um produto de eletrodoméstico pode estar em muitas categorias e uma categoria pode conter muitos produtos).

4. **Avaliação e Produto:**
   - **Descrição:** Cada avaliação está associada a um único produto de eletrodoméstico, indicando a avaliação específica de um item.
   - **Cardinalidade:** 1:N (um produto pode ter zero ou muitas avaliações).

5. **Carrinho e Produto:**
   - **Descrição:** Cada carrinho pode conter zero ou muitos produtos de eletrodomésticos, representando os itens adicionados antes da compra.
   - **Cardinalidade:** M:N (muitos produtos de eletrodomésticos podem estar em muitos carrinhos).

6. **Cupom e Pedido:**
   - **Descrição:** Cada pedido pode ter zero ou um cupom associado, refletindo descontos específicos em eletrodomésticos.
   - **Cardinalidade:** 0..1:N (zero ou um cupom pode ser aplicado a muitos pedidos).

7. **Compra e Pedido:**
   - **Descrição:** Cada compra está associada a um único pedido de eletrodoméstico, representando uma transação específica.
   - **Cardinalidade:** 1:N (um pedido pode resultar em zero

 ou muitas compras).

8. **Promoção e Compra:**
   - **Descrição:** Cada promoção pode estar associada a zero ou muitas compras de eletrodomésticos, indicando descontos sazonais.
   - **Cardinalidade:** 0..1:N (zero ou uma promoção pode estar relacionada a muitas compras).

9. **Fabricante e Produto:**
   - **Descrição:** Cada produto de eletrodoméstico é produzido por um único fabricante, estabelecendo a origem dos itens.
   - **Cardinalidade:** 1:N (um fabricante pode produzir muitos produtos).

10. **Opinião e Usuário:**
    - **Descrição:** Cada opinião está associada a um único usuário, indicando quem expressou a opinião em nosso e-commerce de eletrodomésticos.
    - **Cardinalidade:** 1:N (um usuário pode ter zero ou muitas opiniões).

11. **Opinião e Produto:**
    - **Descrição:** Cada opinião está associada a zero ou muitos produtos de eletrodomésticos, permitindo comentários gerais ou específicos.
    - **Cardinalidade:** M:N (muitas opiniões podem estar relacionadas a muitos produtos).

12. **Cashback e Usuário:**
    - **Descrição:** Cada cashback está associado a um único usuário, representando quem recebeu o retorno de dinheiro em transações com eletrodomésticos.
    - **Cardinalidade:** 1:N (um usuário pode ter zero ou muitos cashbacks).

13. **Entrega e Pedido:**
    - **Descrição:** Cada entrega está associada a um único pedido de eletrodoméstico, representando o envio de produtos para o cliente.
    - **Cardinalidade:** 1:1 (uma entrega está relacionada a um único pedido).

## Conclusão

O processo de criação do Diagrama de Entidade e Relacionamento foi incrível! Representar visualmente a estrutura de dados do meu e-commerce de eletrodomésticos no "VemSerTech - Ifood" utilizando o StarUML proporcionou uma visão clara e abrangente do sistema.

Essa experiência foi inovadora e essencial no desenvolvimento do projeto. Mal posso esperar para ver o "VemSerTech - Ifood" se tornar realidade e oferecer uma experiência de compra excepcional para os amantes de eletrodomésticos!

--- 
