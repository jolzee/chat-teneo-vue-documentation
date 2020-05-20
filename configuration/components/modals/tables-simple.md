---
description: >-
  Provides a structure for displaying simple inline tables. Useful when you want
  to summarize the entities captured via conversation.
---

# Tables - Simple

## Screenshot

![](../../../.gitbook/assets/simple-inline-table.png)

## JSON

No Extension Helper method provided but it's simple to pass back the configuration to Leopard. You will need to define an **`extensions`** output parameter with the following JSON structure.

If you want to omit the headers then remove the property.

```javascript
{
    "name": "displaySimpleTable",
    "inline": true,
    "dense": true,
    "height": null,
    "fixedHeader": false,
    "headers": ["Account", "Balance"],
    "rows": [["Current", "$1271.21"], ["Private", "$137.54"]]
}
```

