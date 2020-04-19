## Produtos `[products]`
* **id** [integer unsigned auto increments]
* **title** [string] *{Nome ou título do produto}*
* **description_general** [longtext] (opcional) *{Descrição geral do produto. Aceita formato HTML}*
* **description_technical** [longtext] (opcional) *{Descrição tecnica do produto. Aceita formato HTML}*
* **price** [double] *{Preço do produto. Caso o produto tenha variações, este preço é substituido pelo preço da variação}*
* **price_promotional** [double] (opcional) *{Preço promocional do produto. Caso o produto tenha variações, este preço é substituido pelo preço promocional da variação}*
* **only_whatsapp** [boolean] (opcional) *{Flag para identificar que este produto deve ser vendido somente via Whatsapp}*
* **amount** [integer] *{Quantidade total do produto em estoque. Caso o produto tenha variações,  deve conter a soma do estoque de todas as variações.}*
* **featured** [boolean] (opcional) *{Flag para identificar se produto deve receber destaque}*
* **deactivated** [boolean] (opcional) *{Flag para desativar produto no site}*
* **video_url** [string] (opcional) *{Código de vídeo hospedado no Youtube}*
* **size_height** [double] *{Altura da embalagem do produto. Usado para cálculo do frete}*
* **size_width** [double] *{Largura da embalagem do produto. Usado para cálculo do frete}*
* **site_weight** [double] *{Peso da embalagem do produto. Usado para cálculo do frete}*
* **size_thickness** [double] *{Comprimento ou profundidade da embalagem do produto. Usado para cálculo do frete}*
* **seo_title** [string] (opcional) *{Título do produto para SEO, caso queira que o título da página seja diferente do nome do produto}*
* **seo_description** [text] (opcional) *{Descrição do produto para SEO. Caso não for informada, será utilizado parte da descrição geral}*
* **seo_keywords** [string] (opcional) *{Palavras-chave do produto para SEO}*
* **unit** [enum] *{Unidade de medida do produto. Valores disponível são 'un' e 'm²'. Valor padrão 'un'}*
* **meter_per_box** [double] (opcional) *{Obrigatório somente se unit for 'm²'. Preço total da caixa. Geralmente utilizado na venda de piso, onde existe o preço por metro quadrado e o preço da caixa}*
* **category_id** [integer unsigned] *{Chave estrangeira da tabela product_categories}*
* **brand_id** [integer unsigned] *{Chave estrangeira da tabela product_brands}*

___

### Create [POST] `/api/product-commerce/product-configurations`
#### Exemplo de requisição
```json
{
  "title": "Coifa Franke De Parede Glass Touch 90 Cm 220v",
  "description_general": "<p>A Coifa Glass Touch de Parede Franke é um misto de modernidade e eficiência. Com lâmpadas LED e acabamento em vidro preto com painel touch, a Coifa Glass Touch de Parede possui visual moderno e slim. Além disso, o produto ainda combina perfeitamente com outros produtos da linha Glass Franke, como o Cooktop de Indução, os Cooktops à gás e os fornos GL52, GL82 e GL86.</p><p> </p><p>Pode ser instalado como depurador ou exaustor, sendo ideal para casas ou apartamentos. Com acabamento em aço escovado e vidro preto com um formato minimalista, pode ser utilizada nos mais diferentes estilos de cozinha. O produto também acompanha filtro de carvão ativado e filtro metálico lavável em lava-louças. Com ruído baixo e uma das sucções mais fortes do mercado, tem vazão livre de 1.040 m³/h e deixa a sua casa casa livre de gorduras e odores.</p>",
  "description_technical": "<p><b>Características:</b></p><ul><li>Coifa de Parede</li><li>3 velocidades</li><li>220V</li><li>1040 m³/h de sucção</li><li>Ruído conforme norma europeia En 60704-3: 72dB</li><li>Lâmpadas: Led 2x1W</li><li>Comando Touch Screen</li></ul>",
  "price": 1699.00,
  "price_promotional": 1399.00,
  "only_whatsapp": 0,
  "amount": 2,
  "featured": 0,
  "deactivated": 0,
  "video_url": "vKuOsjmonPY",
  "size_height": 52.000,
  "size_width": 95.000,
  "site_weight": 10.000,
  "size_thickness": 39.000,
  "seo_title": null,
  "seo_description": null,
  "seo_keywords": "coifa,franke,touch,220,90,preta,digital,parede",
  "unit": "un",
  "meter_per_box": null,
  "category_id": 1,
  "brand_id": 1
}
```

#### Exemplo de resposta
```json
{
  "id": 1,
  "code": "442312",
  "title": "Coifa Franke De Parede Glass Touch 90 Cm 220v",
  "slug": "coifa-franke-de-parede-glass-touch-90-cm-220v",
  "description_general": "<p>A Coifa Glass Touch de Parede Franke é um misto de modernidade e eficiência. Com lâmpadas LED e acabamento em vidro preto com painel touch, a Coifa Glass Touch de Parede possui visual moderno e slim. Além disso, o produto ainda combina perfeitamente com outros produtos da linha Glass Franke, como o Cooktop de Indução, os Cooktops à gás e os fornos GL52, GL82 e GL86.</p><p> </p><p>Pode ser instalado como depurador ou exaustor, sendo ideal para casas ou apartamentos. Com acabamento em aço escovado e vidro preto com um formato minimalista, pode ser utilizada nos mais diferentes estilos de cozinha. O produto também acompanha filtro de carvão ativado e filtro metálico lavável em lava-louças. Com ruído baixo e uma das sucções mais fortes do mercado, tem vazão livre de 1.040 m³/h e deixa a sua casa casa livre de gorduras e odores.</p>",
  "description_technical": "<p><b>Características:</b></p><ul><li>Coifa de Parede</li><li>3 velocidades</li><li>220V</li><li>1040 m³/h de sucção</li><li>Ruído conforme norma europeia En 60704-3: 72dB</li><li>Lâmpadas: Led 2x1W</li><li>Comando Touch Screen</li></ul>",
  "price": 1699.00,
  "price_promotional": 1399.00,
  "only_whatsapp": 0,
  "amount": 2,
  "featured": 0,
  "deactivated": 0,
  "video_url": "vKuOsjmonPY",
  "size_height": 52.000,
  "size_width": 95.000,
  "site_weight": 10.000,
  "size_thickness": 39.000,
  "seo_title": null,
  "seo_description": null,
  "seo_keywords": "coifa,franke,touch,220,90,preta,digital,parede",
  "unit": "un",
  "meter_per_box": null,
  "category_id": 1,
  "brand_id": 1,
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```
