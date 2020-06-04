---
description: >-
  If you have dialog flows with Prompt Triggers then Leopard can poll your TIE
  at a configurable interval. Polling is disabled by default but can be enabled
  and configured in the Solution config.
---

# Prompt Trigger Polling

{% hint style="success" %}
Leopard sends no user input when polling. It does add a**`command=prompt`**request parameter to each poll request.
{% endhint %}

{% hint style="danger" %}
Your Teneo solution must return the number of active flows to Leopard for every request. This is needed so that the polling is only active when there are no active flows \(you are not mid dialog\) 
{% endhint %}

{% code title="Post Processing" %}
```groovy
_.putOutputParameter("numActiveFlows", "" + _.getActiveFlows().size())
```
{% endcode %}

## Screenshots

![](../.gitbook/assets/poll.png)

![A catch all flow that handles every poll request](../.gitbook/assets/catch-all-flow-polling.jpg)

![A contrived flow with a Prompt Trigger that only executes when the current minutes are even numbers ](../.gitbook/assets/prompt-triggered-flow.jpg)

![Answers form Flows triggered via Prompt Triggers showing in Leopard](../.gitbook/assets/polling-working-in-leopard.jpg)

