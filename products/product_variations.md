## Variações de produtos `[product_variations]`
* id [integer unsigned auto increments]
* name [string] *{Nome da variação que é um dos valores contidos na tabela product_variations no campo option_values. Ex.: 'vermelho'}*
* amount [integer] *{Quantidade no estoque do produto nesta variação. Ex.: Quantidade de cadeiras vermelhas}*
* price [double] *{Preço do produto nesta variação}*
* price_promotional [double] (opcional) *{Preço promocional do produto nesta variação}*
* options [string] *{Correspondência com a tabela product_configurations com campo option_name, contendo array no formato (["Cor", 'Tamanho'])}*
* product_id [integer unsigned] *{Chave estrangeira da tabela products}*

___

### Create [POST] `/api/product-commerce/products/1/variations`
#### Exemplo de requisição
```json
{
  "name": "Branco",
  "amount": 5,
  "price": 552.90,
  "price_promotional": 525.90,
  "options": ["Cor"],
  "product_id":  1
}
```

#### Exemplo de resposta
```json
{
  "id": 1,
  "name": "Branco",
  "amount":  5,
  "price": 552.90,
  "price_promotional": 525.90,
  "options": ["Cor"],
  "product_id":  1,
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```