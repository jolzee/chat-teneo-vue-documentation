# Greeting Message

## Capture the Login command

Disable the following flow from the TDR's - `The user continues conversation after Timeout`  This flow is located in `Dialogue » Non-conversational » Timeout`

Capture the `command` request parameter. Leopard sends a `?command=login` whenever the chat window is opened. You will want to trigger the greeting message when this request parameter is present.

{% tabs %}
{% tab title="Pre-processing Script" %}
```groovy
if (engineEnvironment.getParameter("command")) {
	command = engineEnvironment.getParameter("command")
} else {
	command = ""
}
```
{% endtab %}
{% endtabs %}

In your greeting flow you will want to add a syntax trigger with the following condition

{% tabs %}
{% tab title="Trigger Condition in Greeting Flow" %}
```groovy
{command == "login"}
```
{% endtab %}
{% endtabs %}

![](../../.gitbook/assets/greeting.png)

