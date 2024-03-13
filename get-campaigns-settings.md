[service-shoppyz](../../../../README.md) / [API](../README.md) / [campaign](./README.md) / Get campaigns settings

# Get campaigns settings

Get settings of all campaigns for a customer.

```text
GET /campaigns
```

## Body

| Name   | Description             |
|--------|-------------------------|
| `user` | User doing the request. | 

## Example

```text
GET /campaigns

{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  }
}
```

Response

```json
{
  "campaigns": [
    {
      "name":"nom_campagne_test",
      "id_campaign": "iK123jP345",
      "analytics_solution": "ga3",
      "analytics_id": "123",
      "googleads_id": "123",
      "product_feed_type": "xml",
      "product_url_feed": "https://test.xml",
      "shoppyz_url": "",
      "dashboard_url": "https://url_test_looker.test",
      "feed_mapping": [
        {
          "name": "id",
          "name_in_feed": "g:id"
        },
        {
          "name": "category",
          "name_in_feed": "g:google_product_category"
        },
        {
          "name": "price",
          "name_in_feed": "g:price"
        }, 
        {
          "name": "item_group_id",
          "name_in_feed": "g:item_group_id"
        }
      ],
      "label_campaign": "0",
      "creation_date": "28 Dec 2023, 11:34:32.595",  
      "scoring_modification_date":"28 Dec 2023, 11:34:32.595",
      "users_emails": ["solene.vinsot@eskimoz.fr"]
    },
  ]
}
```
