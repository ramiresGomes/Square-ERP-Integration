## Marcas `[product_brands]`
* **id** [integer unsigned auto increments]
* **name** [string]
* **image** [string] (opcional) *{URI para acessar o logo da marca. O sistema fará o download da imagem e hospedará junto ao site.}*

___

### Create [POST] `/api/product-commerce/product-brands`
#### Exemplo de requisição
```json
{
  "name": "Stone Mater",
  "image": "https://example.com/stone-mater.jpg"
}
```

#### Exemplo de resposta
```json
{
  "id": "1",
  "name": "Stone Mater",
  "slug": "stone-mater",
  "image": "uploads/product_commerce/brand/1/stone-mater.jpg",
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```