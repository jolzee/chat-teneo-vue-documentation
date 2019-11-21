---
description: >-
  You can show a loading image in the chat window when you know that a response
  might take longer than usual. This expected delay can be sent as a hint to
  Leopard.
---

# Expensive Operations

## Instructions

Add an output parameter of `command = delay` to any output node. Leopard will then show the "thinking" graphic until it next receives a response from Teneo. When the graphic is shown Teneo automatically sends back an empty input to Teneo with a request parameter of `command=continue` .  You can then begin your expensive operation and return the response as per usual. 

![](../../.gitbook/assets/delay.jpg)

Remember you can retrieve request parameters in Teneo in Pre-Processing.

{% code title="Pre-Processing script grabs command parameter and sets it as a global variable" %}
```groovy
if (engineEnvironment.getParameter("command")) {
	command = engineEnvironment.getParameter("command")
} else {
	command = ""
}
```
{% endcode %}

### Screenshots

![](../../.gitbook/assets/delayleopard.gif)

### Output Parameter

```text
command = delay
```

## 

