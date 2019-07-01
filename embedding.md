---
description: Describes the process of including Leopard on an external website.
---

# Embedding

```markup
<script type="text/javascript">
window.TENEOCTX ||(TENEOCTX={});
TENEOCTX = {
	pageTitle: document.title,
	pageUrl: window.location.href,
	pageTopic: "Help",
	message: "This was sent from the customer's web site"
}
</script>
<script src="https://<your-tie-url>/<ctx>/static/embed-leopard.js"></script>
```

The keys in the `TENEOCTX` object will be passed as individual request parameters to your TIE endpoint with every request.  

{% hint style="info" %}
Remember to update the **`tieUrl`** in **`embed-leopard.js`**
{% endhint %}

You can pick up any of the parameters in a pre-processing script in Teneo Studio.

{% code-tabs %}
{% code-tabs-item title="Pre-Processing in Teneo Studio" %}
```groovy
if (engineEnvironment.getParameter("pageTitle")) {
	pageTile = engineEnvironment.getParameter("pageTitle")
}

if (engineEnvironment.getParameter("pageUrl")) {
	pageUrl = engineEnvironment.getParameter("pageUrl")
}

if (engineEnvironment.getParameter("pageTopic")) {
	pageTopic = engineEnvironment.getParameter("pageTopic")
}

if (engineEnvironment.getParameter("message")) {
	message = engineEnvironment.getParameter("message")
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Dynamically passing information

You can also dynamically make Leopard aware of some page information by posting a message to the frame using JavaScript.

{% hint style="info" %}
Only use this method when some dynamic HTML or action has happened on the page and you want Leopard to be updated.
{% endhint %}

```javascript
var teneoFrameWindow = window.frames.teneochatwidget;
if (teneoFrameWindow) {
  var newInformation = {
    message: "something interesting just happened",
    otherParam: "lorem ipsum"
  };
  teneoFrameWindow.postMessage(JSON.stringify(newInformation), "*");
}
```
