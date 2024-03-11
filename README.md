## **Contexto**

Este conjunto de dados foi generosamente fornecido pela Olist, a maior loja de departamentos nos marketplaces brasileiros. A Olist conecta pequenas empresas de todo o Brasil a canais sem problemas e com um único contrato. Esses comerciantes podem vender seus produtos através da Loja Olist e enviá-los diretamente aos clientes usando os parceiros logísticos da Olist. Veja mais em nosso site: [www.olist.com](https://www.olist.com/)

Após um cliente comprar o produto na Loja Olist, um vendedor é notificado para cumprir esse pedido. Uma vez que o cliente recebe o produto, ou a data estimada de entrega é devida, o cliente recebe uma pesquisa de satisfação por e-mail, onde ele pode dar uma nota para a experiência de compra e escrever alguns comentários.


## **Esquema de Dados**

Os dados estão divididos em vários conjuntos de dados para melhor compreensão e organização. Por favor, consulte o seguinte esquema de dados ao trabalhar com ele:

![image](https://github.com/guizucolotto/olist_sql_test/assets/101340842/82d29901-abf4-43f2-b032-1cb276f796d9)


# **Customers Dataset**

Este conjunto de dados tem informações sobre o cliente e sua localização. Use-o para identificar clientes únicos no conjunto de dados de pedidos e para encontrar o local de entrega dos pedidos.

Em nosso sistema, cada pedido é atribuído a um customer_id único. Isso significa que o mesmo cliente receberá ids diferentes para pedidos diferentes. O propósito de ter um customer_unique_id no conjunto de dados é permitir que você identifique clientes que fizeram recompras na loja. Caso contrário, você descobriria que cada pedido tinha um cliente diferente associado.

# **Geolocation Dataset**

Este conjunto de dados contém informações sobre os códigos postais brasileiros e suas coordenadas lat/lng. Use-o para traçar mapas e encontrar distâncias entre vendedores e clientes.

# **Order Items Dataset**

Este conjunto de dados inclui informações sobre os itens comprados em cada pedido.

## **Exemplo:**

O order_id = `00143d0f86d6fbd9f9b38ab440ac16f5` tem 3 itens (mesmo produto). Cada item tem o frete calculado de acordo com suas medidas e peso. Para obter o valor total do frete para cada pedido, basta somar.

**The total order_item value is:** `21.33 * 3 = 63.99`

**The total freight value is:** `15.10 * 3 = 45.30`

**The total order value (product + freight) is:** `45.30 + 63.99 = 109.29`

# **Payments Dataset**

Este conjunto de dados inclui informações sobre as opções de pagamento dos pedidos.

# **Order Reviews Dataset**

Este conjunto de dados inclui informações sobre as avaliações feitas pelos clientes.

Após um cliente comprar o produto na Loja Olist, um vendedor é notificado para cumprir esse pedido. Uma vez que o cliente recebe o produto, ou a data estimada de entrega vence, o cliente recebe uma pesquisa de satisfação por e-mail onde ele pode dar uma nota para a experiência de compra e escrever alguns comentários.

# **Order Dataset**

Este é o conjunto de dados principal. De cada pedido, você pode encontrar todas as outras informações.

# **Products Dataset**

Este conjunto de dados inclui informações sobre os produtos vendidos pela Olist.

# **Sellers Dataset**

Este conjunto de dados inclui informações sobre os vendedores que atenderam aos pedidos feitos no Olist. Use-o para encontrar a localização do vendedor e identificar qual vendedor atendeu a cada produto.

# **Category Name Translation**

Traduz os product_category_name para Inglês.



## **Desafio**

1. **Relacionamento de Tabelas:**
    - Crie um modelo de relacionamento entre as tabelas, indicando as chaves primárias e estrangeiras.
2. **Análise de Vendas:**
    - Calcule o total de vendas realizadas.
    - Identifique os 5 produtos mais vendidos.
    - Liste os 10 clientes que mais gastaram.
    - Determine a quantidade média de itens por pedido.
3. **Geografia das Vendas:**
    - Descubra quais estados têm o maior número de vendas.
    - Liste as 5 cidades com mais pedidos.
4. **Tempo de Entrega:**
    - Calcule o tempo médio de entrega dos pedidos.
5. **Extra**
    - Qualquer insight ou informação que você ache relevante para apresentar suas capacidades no desafio apresentado

**Achados Esperados:**

Espera-se que os candidatos demonstrem habilidades em:

- Criar consultas SQL eficientes e bem estruturadas.
- Estabelecer relacionamentos adequados entre as tabelas.
- Apresentar resultados de forma clara e organizada (excel, powe bi, ou qualquer forma que lhe seja mais familiar para apresentação de relatório).
- Interpretar os dados para extrair insights relevantes sobre as vendas da Olist.

Boa sorte!
