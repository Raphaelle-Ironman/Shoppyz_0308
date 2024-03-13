[service-shoppyz](../../../../README.md) / [API](../README.md) / [custom-rules](./README.md) / Modify a custom rule

# Modify a custom rule

Modify custom rule setup. The name of the rule can't be modified.

```
PUT /campaigns/:id_campaign/rules/:id_rule
```

## Body

| Name                | Description                                        |
|---------------------|----------------------------------------------------|
| `user`              | User doing the request.                            | 
| `trigger_dimension` | Dimension of the trigger, lowercase                |
| `trigger_condition` | Condition of the trigger, lowercase                |
| `trigger_value`     | Value condition of the trigger, lowercase or float |
| `action_type`       | Type of action, lowercase                          |
| `action_value`      | Value of action, lowercase or float.               |

## Parameters

| Name          | Description        |
|---------------|--------------------|
| `id_campaign` | ID of the campaign.|
| `id_rule`     | ID of the rule.    |

## Example

```text
PUT /campaigns/AiJ34A4j/rules/AjK0iP5

{ 
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "trigger_dimension": "brand",
  "trigger_condition": "is",
  "trigger_value": "eskimoz",
  "action_type": "increase",
  "action_value":"0.1"
}

```

Response

```text
200 Ok
```

```json
{ 
  "trigger_dimension": "brand",
  "trigger_condition": "is",
  "trigger_value": "eskimoz",
  "action_type": "increase",
  "action_value":"0.1"
}

```
