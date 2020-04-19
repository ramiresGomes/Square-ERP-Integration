## Transações *(Somente consulta)* `[product_images]`
* **id** [integer unsigned auto increments]
* **gateway_code_transaction** [string] *{Código da transação gerado no gateway de pagamento}*
* **payment_method** [string] *{Método de pagamento ('credit_card' ou 'banking_billet')}*
* **banking_billet_url** [string] *{Url para acessar boleto em caso de pagamento por boleto bancário}*
* **bar_code** [string] *{Código de barras do boleto em caso de pagamento por boleto bancário}*
* **previous_status** [string] *{Estado anterior da compra. Inicia como null}*
* **current_status** [string] *{Estado atual da compra. Inicia com 'waiting_payment'. ('processing', 'authorized', 'paid', 'refunded', 'waiting_payment', 'pending_refund', 'refused', 'canceled', 'closed', 'preparing')}*
* **total** [string] *{Valor total da compra (subtotal + shippingCost}*
* **shipping** [string] *{Custo do frete/envio}*
* **shipping_method** [string] *{Método de entrega ('delivery', 'private', 'pac', 'sedex' ou 'withdrawinstore')}*
* **gateway** [string] *{Nome do gateway de pagamento utilizado ('PagSeguro', 'PagarMe')}*
* **client_id** [string] *{Chave estrangeira da tabela clients}*

## Produtos da Transação *(Somente consulta)* `[product_images]`
* **id** [integer unsigned auto increments]
* **title** [string]
* **quantity** [string]
* **unit_price** [string]
* **product_id** [string]
* **transaction_id** [string]
___

### Create [GET] `/api/product-commerce/transactions/1`
#### Exemplo de requisição
`Body null`

#### Exemplo de resposta
```json
{
  "id": 1,
  "gateway_code_transaction": "6C1E0BCF-8B68-43A5-AC2F-9C69EF0A5F17",
  "payment_method": "banking_billet",
  "banking_billet_url": "https://pagseguro.uol.com.br/checkout/payment/booklet/print.jhtml?c=27e512a1e1d97bbec2a4c409aa115f7ace5f",
  "bar_code": "03399.58974 97857.056846 12515.948513 1 75160000045869", 
  "previous_status": "waiting_payment",
  "current_status": "canceled", 
  "total": 688.8,
  "shipping": 0, 
  "shipping_method": "delivery",
  "gateway": "PagSeguro", 
  "client_id": 1,
  "tracking_code": "",
  "products": [
    {
      "id": 1,
      "title": "Assento PP Plus Fit Branco Celite",
      "quantity": 2, 
      "unit_price": 249.9,
      "product_id": 182, 
      "transaction_id": 1,
      "created_at": "2020-10-10 00:00:00",
      "updated_at": "2020-10-10 00:00:00",
      "deleted_at": null
    },
    {
      "id": 2,
      "title": "Cadeira Tramontina Safira sem Braços - AMARELO",
      "quantity": 1, 
      "unit_price": 189,
      "product_id": 21, 
      "transaction_id": 1,
      "created_at": "2020-10-10 00:00:00",
      "updated_at": "2020-10-10 00:00:00",
      "deleted_at": null
    }
  ],
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```

___
 > Atualizar compra com código de rastreio
### Create [PUT] `/api/product-commerce/transactions/1`
#### Exemplo de requisição
```json
{
  "tracking_code": "AB123456789BR"
}
```

#### Exemplo de resposta
```json
{
  "id": 1,
  "gateway_code_transaction": "6C1E0BCF-8B68-43A5-AC2F-9C69EF0A5F17",
  "payment_method": "banking_billet",
  "banking_billet_url": "https://pagseguro.uol.com.br/checkout/payment/booklet/print.jhtml?c=27e512a1e1d97bbec2a4c409aa115f7ace5f",
  "bar_code": "03399.58974 97857.056846 12515.948513 1 75160000045869", 
  "previous_status": "waiting_payment",
  "current_status": "canceled", 
  "total": 688.8,
  "shipping": 0, 
  "shipping_method": "delivery",
  "gateway": "PagSeguro", 
  "client_id": 1,
  "tracking_code": "AB123456789BR",
  "products": [
    {
      "id": 1,
      "title": "Assento PP Plus Fit Branco Celite",
      "quantity": 2, 
      "unit_price": 249.9,
      "product_id": 182, 
      "transaction_id": 1,
      "created_at": "2020-10-10 00:00:00",
      "updated_at": "2020-10-10 00:00:00",
      "deleted_at": null
    },
    {
      "id": 2,
      "title": "Cadeira Tramontina Safira sem Braços - AMARELO",
      "quantity": 1, 
      "unit_price": 189,
      "product_id": 21, 
      "transaction_id": 1,
      "created_at": "2020-10-10 00:00:00",
      "updated_at": "2020-10-10 00:00:00",
      "deleted_at": null
    }
  ],
  "created_at": "2020-10-10 00:00:00",
  "updated_at": "2020-10-10 00:00:00",
  "deleted_at": null
}
```