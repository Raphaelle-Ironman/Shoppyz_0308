[service-shoppyz](../../../../README.md) / [API](../README.md) / [custom-rules](./README.md) / Add a custom rule

# Add a custom rule

Add custom rule setup.

```text
PUT /campaigns/:id_campaign/rules
```

## Body

| Name                | Description                                        |
|---------------------|----------------------------------------------------|
| `user`              | User doing the request.                            | 
| `rule_name`         | Name of the custom rule                            |
| `trigger_dimension` | Dimension of the trigger, lowercase                |
| `trigger_condition` | Condition of the trigger, lowercase                |
| `trigger_value`     | Value condition of the trigger, lowercase or float |
| `action_type`       | Type of action, lowercase                          |
| `action_value`      | Value of action, lowercase or float.               |

## Parameters

| Name          | Description         |
|---------------|---------------------|
| `id_campaign` | ID of the campaign. |

## Example

```text
PUT /campaigns/AiJ34A4j/rules

{ 
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "rule_name": "rule on brand",
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
  "rule_name": "rule on brand",
  "trigger_dimension": "brand",
  "trigger_condition": "is",
  "trigger_value": "eskimoz",
  "action_type": "increase",
  "action_value":"0.1"
}

```
