---
description: Describes the process of including Leopard on an external website.
---

# Embedding

Note that you can inject the Lepard Chat UI into a specific element on a page. This might be beneficial if you want to place it in a specific tab order. To enable this add a `<div id="leopardChatWindow"></div>` anywhere on the page. This is not required though and if absent the UI will automatically be injected at the beginning of the body.

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

<div id="leopardChatWindow"></div>

<script src="https://<your-leopard-host>/<leopard-ctx>/static/embed-leopard.js"></script>
```

The keys in the `TENEOCTX` object will be passed as individual request parameters to your TIE endpoint with every request.  

{% hint style="info" %}
Remember to update the **`tieUrl`** in **`embed-leopard.js`**
{% endhint %}

You can pick up any of the parameters in a pre-processing script in Teneo Studio.

{% code title="Pre-Processing in Teneo Studio" %}
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
{% endcode %}

## Dynamically passing information

### Pass information from website to Leopard and Teneo

You can also dynamically make Leopard and Teneo aware of some page information by posting a message to the frame using JavaScript.

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

### Pass information from Teneo through to the website

You can run JavaScript sent from Teneo on the website that embeds Teneo. Add an output parameter to any node in Teneo with the name "**script**" with the value containing the JavaScript you want to run.

![Creates a button and changes the site&apos;s background text to Red!!](.gitbook/assets/image%20%2819%29.png)



