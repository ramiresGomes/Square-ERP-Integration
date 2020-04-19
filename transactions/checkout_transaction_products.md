## Imagens `[product_images]`
* **id** [integer unsigned auto increments]
* **name** [string]
* **label** [string] *{Texto para ser usado no atributo 'alt' da tag img do HTML}*
* **dimensions** [string] *{dimensões da imagem, ex.: '1024x1024'}*
* **order** [integer]
* **product_variation** [integer unsigned] *{Nome da variação de produto para associar imagem do produto com variação do produto}*
* **product_id** [integer unsigned] *{Chave estrangeira da tabela products}*

___

#### Exemplo de requisição
```json
{
    "name" : "",
    "label" :  "",
    "dimensions" : "",
    "order" :  "",
    "product_variation" : "",
    "product_id" :  ""
}
```

#### Exemplo de resposta
```json
{
  "id": "",
  "name": "",
  "label":  "",
  "dimensions": "",
  "order":  "",
  "product_variation": "",
  "product_id":  "",
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```