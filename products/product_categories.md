## Categorias de Produtos [product_categories]`
* **id** [integer  unsigned auto increments]
* **name** [string]
* **seo_title** [string] (opcional)
* **seo_description** [string] (opcional)
* **seo_keywords** [string] (opcional)
* **image** [string] (optional) *{Imagem para SEO exibida no compartilhamento da página de listagem de produtos}*
* **image_dimensions** [string] (opcional | obrigatório se imagem for preenchido) *{dimensões da imagem, ex.: '1024x1024'}*
* **category_id** [integer unsigned] *{Chave estrangeira da tabela product_categories, usado para criar subcategorias}*

___

### Create [POST] `/api/product-commerce/product-categories`
#### Exemplo de requisição
```json
{
  "name": "Área Gourmet",
  "seo_title": "Área Gourmet", 
  "seo_description": "Encontre em Uberlândia com melhor preço: CADEIRA ÁREA GOURMET / BALCÃO ESCRITÓRIO / LANCHONETE / RESIDENCIAL / CADEIRA CONFORTÁVEL",
  "seo_keywords": "area gourmet,cadeira,sofá,balcão escritório,lanchonete,residencial,cadeira confortável",
  "image": "https://example.com/area-gourmet.png",
  "image_dimensions": "1024x1024", 
  "category_id": null
}
```

#### Exemplo de resposta
```json
{
  "id": 1,
  "name": "Área Gourmet",
  "slug": "area-gourmet",
  "seo_title": "Área Gourmet", 
  "seo_description": "Encontre em Uberlândia com melhor preço: CADEIRA ÁREA GOURMET / BALCÃO ESCRITÓRIO / LANCHONETE / RESIDENCIAL / CADEIRA CONFORTÁVEL",
  "seo_keywords": "area gourmet,cadeira,sofá,balcão escritório,lanchonete,residencial,cadeira confortável",
  "image": "uploads/product_commerce/category/2/area-gourmet.jpg",
  "image_dimensions": "", 
  "category_id": "",
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```
