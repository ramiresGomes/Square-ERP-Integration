## Configurações de variações `[product_configurations]`
* **id** [integer unsigned auto increments]
* **option_name** [string] *{Nome da variação. Ex.: 'Cor', 'Tamanho', 'Voltagem'}*
* **option_values** [string] *{Lista de valores disponíveis para esta variação, separados por vírgula (,). Ex.: Para a variação 'Tamanho' tem-se os valores 'p,m,g,gg'}*

___

### Create [POST] `/api/product-commerce/product-configurations`
#### Exemplo de requisição
```json
{
  "option_name": "Cor",
  "option_values": "vermelho, verde, azul, amarelo"
}
```

#### Exemplo de resposta
```json
{
  "id": 1,
  "option_name": "Cor",
  "option_values": "vermelho, verde, azul, amarelo",
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```