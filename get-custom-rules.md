[service-shoppyz](../../../../README.md) / [API](../README.md) / [custom-rules](./README.md) / Get custom rules

# Get custom rules

Get all custom rules settings by campaign.

```text
GET /campaigns/:id_campaign/rules
```
## Body

| Name   | Description             |
|--------|-------------------------|
| `user` | User doing the request. | 

## Parameters

| Name          | Description        |
|---------------|--------------------|
| `id_campaign` | ID of the campaign.|

## Exemple

```text
GET /campaigns/AiJ34A4j/rules
{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  }
}
```

Response

```text
200 Ok
```

```json
{ 
  "custom_rules": [
    {
      "id_rule": "iH87m6",
      "rule_name": "rule on brand",
      "trigger_dimension": "brand",
      "trigger_condition": "is",
      "trigger_value": "eskimoz",
      "action_type": "increase",
      "action_value":"0.1"
    },
  ]
}
```
