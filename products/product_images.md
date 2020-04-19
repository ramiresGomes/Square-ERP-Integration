## Imagens `[product_images]`
* **id** [integer unsigned auto increments]
* **name** [string]
* **label** [string] *{Texto para ser usado no atributo 'alt' da tag img do HTML}*
* **order** [integer]
* **product_variation** [integer unsigned] *{Nome da variação de produto para associar imagem do produto com variação do produto}*
* **product_id** [integer unsigned] *{Chave estrangeira da tabela products}*

___

### Create [POST] `/api/product-commerce/products/1/images`
#### Exemplo de requisição
```json
{
    "name": "https://example.com/piso-delta.jpg",
    "label": "Piso Delta",
    "order": 1,
    "product_variation": "Branco",
    "product_id": 1
}
```

#### Exemplo de resposta
```json
{
  "id": 1,
  "name": "uploads/product_commerce/image/1/piso-delta-8ff4b9.png",
  "label": "Piso Delta",
  "dimensions": "1600x1103",
  "order": 1,
  "product_variation": "Branco",
  "product_id": 1,
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```