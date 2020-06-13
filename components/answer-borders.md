---
description: >-
  Assistant responses / answers can have a left aligned colored border
  configured
---

# Answer Borders

If the **output parameter** "`border`" exists then it's value will be used as the left border or the response or [response chunks](splitting-a-response.md). 

```javascript
border = #FF4C5B
```

If you want to control the borders for each [response chunk](splitting-a-response.md) the you will need a "`borders`" **output parameter** and an array of colors. 

```javascript
borders = ["Red", "#00FF00", "", "Blue"]
```

{% hint style="info" %}
borders will always take precedence if both output parameters are present on a response.
{% endhint %}

## Screenshots

{% tabs %}
{% tab title="Separate Border Colors for Answer Chunks" %}
![](../.gitbook/assets/borders.png)
{% endtab %}

{% tab title="Single Border Color " %}
![](../.gitbook/assets/border-color.png)
{% endtab %}
{% endtabs %}

